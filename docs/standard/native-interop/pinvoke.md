---
title: Appel de code non managé (P/Invoke)
description: Découvrez comment appeler des fonctions natives via P/Invoke dans .NET.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: 1a5f2f9d13429f84d5b5bb58d36f015004fb746b
ms.sourcegitcommit: 680a741667cf6859de71586a0caf6be14f4f7793
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/12/2019
ms.locfileid: "59517861"
---
# <a name="platform-invoke-pinvoke"></a>Appel de code non managé (P/Invoke)

P/Invoke est une technologie qui vous permet d’accéder aux structures, aux rappels et aux fonctions des bibliothèques non managées à partir de votre code managé. Une grande partie de l’API P/Invoke est contenue dans deux espaces de noms : `System` et `System.Runtime.InteropServices`. Utiliser ces deux espaces de noms vous donne les outils pour décrire la façon dont vous voulez communiquer avec le composant natif.

Commençons par l’exemple le plus courant, c’est-à-dire appeler des fonctions non managées dans votre code managé. Nous allons afficher une zone de message à partir d’une application de ligne de commande :

```csharp
using System.Runtime.InteropServices;

public class Program {

    // Import user32.dll (containing the function we need) and define
    // the method corresponding to the native function.
    [DllImport("user32.dll", CharSet = CharSet.Unicode, SetLastError = true)]
    public static extern int MessageBox(IntPtr hWnd, String text, String caption, int options);

    public static void Main(string[] args) {
        // Invoke the function as a regular managed method.
        MessageBox(IntPtr.Zero, "Command-line message box", "Attention!", 0);
    }
}
```

L’exemple précédent est simple, mais il ne montre pas ce dont vous avez besoin pour appeler des fonctions non managées à partir de code managé. Examinons l’exemple :

*   La ligne 1 montre l’instruction d’utilisation de l’espace de noms `System.Runtime.InteropServices`, qui contient tous les éléments dont nous avons besoin.
*   La ligne 7 introduit l’attribut `DllImport`. Cet attribut est crucial, car il indique au runtime qu’il doit charger la DLL non managée. La chaîne passée est la DLL où se trouve notre fonction cible. En outre, il définit le [jeu de caractères](./charset.md) à utiliser pour marshaler les chaînes. Il spécifie enfin que cette fonction appelle [SetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) et que le runtime doit capturer ce code d’erreur pour que l’utilisateur puisse le récupérer avec <xref:System.Runtime.InteropServices.Marshal.GetLastWin32Error?displayProperty=nameWithType>.
*   La ligne 8 est l’essentiel du travail de P/Invoke. Elle définit une méthode managée qui a **exactement la même signature** que la méthode non managée. Notez que la déclaration a un nouveau mot clé, `extern`, qui indique au runtime qu’il s’agit d’une méthode externe et que, quand vous l’appelez, le runtime doit la trouver dans la DLL spécifiée dans l’attribut `DllImport`.

Le reste de l’exemple appelle simplement la méthode comme toute autre méthode managée.

L’exemple est similaire pour Mac OS. Le nom de la bibliothèque dans l’attribut `DllImport` doit être modifié, car Mac OS a un schéma de nommage des bibliothèques dynamiques différent. L’exemple suivant utilise la fonction `getpid(2)` pour obtenir l’ID de processus de l’application et l’afficher dans la console :

```csharp
using System;
using System.Runtime.InteropServices;

namespace PInvokeSamples {
    public static class Program {

        // Import the libSystem shared library and define the method corresponding to the native function.
        [DllImport("libSystem.dylib")]
        private static extern int getpid();

        public static void Main(string[] args){
            // Invoke the function and get the process ID.
            int pid = getpid();
            Console.WriteLine(pid);
        }
    }
}
```

Le processus est semblable sur Linux. Le nom de fonction est le même, car `getpid(2)` est un appel système [POSIX](https://en.wikipedia.org/wiki/POSIX) standard.

```csharp
using System;
using System.Runtime.InteropServices;

namespace PInvokeSamples {
    public static class Program {

        // Import the libc shared library and define the method corresponding to the native function.
        [DllImport("libc.so.6")]
        private static extern int getpid();

        public static void Main(string[] args){
            // Invoke the function and get the process ID.
            int pid = getpid();
            Console.WriteLine(pid);
        }
    }
}
```

## <a name="invoking-managed-code-from-unmanaged-code"></a>Appel de code managé à partir de code non managé

Le runtime permet une communication fluide dans les deux directions, ce qui vous donne la possibilité d’effectuer des rappels dans du code managés à partir de fonctions natives, à l’aide de pointeurs de fonction. Ce qui ressemble le plus à un pointeur de fonction dans le code managé est un **délégué**, c’est donc ce qui est utilisé pour autoriser les rappels du code natif dans le code managé.

La façon d’utiliser cette fonctionnalité est similaire au processus code managé vers du code natif préalablement décrit. Pour un rappel donné, vous définissez un délégué qui correspond à la signature et vous le passez dans la méthode externe. Le runtime s’occupe du reste.

```csharp
using System;
using System.Runtime.InteropServices;

namespace ConsoleApplication1 {

    class Program {

        // Define a delegate that corresponds to the unmanaged function.
        delegate bool EnumWC(IntPtr hwnd, IntPtr lParam);

        // Import user32.dll (containing the function we need) and define
        // the method corresponding to the native function.
        [DllImport("user32.dll")]
        static extern int EnumWindows(EnumWC lpEnumFunc, IntPtr lParam);

        // Define the implementation of the delegate; here, we simply output the window handle.
        static bool OutputWindow(IntPtr hwnd, IntPtr lParam) {
            Console.WriteLine(hwnd.ToInt64());
            return true;
        }

        static void Main(string[] args) {
            // Invoke the method; note the delegate as a first parameter.
            EnumWindows(OutputWindow, IntPtr.Zero);
        }
    }
}
```

Avant de parcourir l’exemple, passons en revue les signatures des fonctions non managées dont vous avez besoin. La fonction à appeler pour énumérer toutes les fenêtres a la signature suivante : `BOOL EnumWindows (WNDENUMPROC lpEnumFunc, LPARAM lParam);`

Le premier paramètre est un rappel. Ce rappel a la signature suivante : `BOOL CALLBACK EnumWindowsProc (HWND hwnd, LPARAM lParam);`

Examinons maintenant l’exemple en détail :

*   la ligne 9 dans l’exemple définit un délégué qui correspond à la signature du rappel dans le code non managé. Notez la façon dont les types LPARAM et HWND sont représentés à l’aide de `IntPtr` dans le code managé.
*   Les lignes 13 et 14 introduisent la fonction `EnumWindows` de la bibliothèque user32.dll.
*   Les lignes 17 à 20 implémentent le délégué. Dans cet exemple simple, nous voulons simplement générer le handle dans la console.
*   Enfin, dans la ligne 24, la méthode externe est appelée et transmise au délégué.

Les exemples de Linux et Mac OS sont présentés ci-dessous. Dans ces exemples, nous utilisons la fonction `ftw` qui se trouve dans `libc`, la bibliothèque C. Cette fonction est utilisée pour parcourir des hiérarchies de répertoires et accepte un pointeur vers une fonction comme l’un de ses paramètres. Cette fonction a la signature suivante : `int (*fn) (const char *fpath, const struct stat *sb, int typeflag)`.

```csharp
using System;
using System.Runtime.InteropServices;

namespace PInvokeSamples {
    public static class Program {

            // Define a delegate that has the same signature as the native function.
            delegate int DirClbk(string fName, StatClass stat, int typeFlag);

            // Import the libc and define the method to represent the native function.
            [DllImport("libc.so.6")]
            static extern int ftw(string dirpath, DirClbk cl, int descriptors);

            // Implement the above DirClbk delegate;
            // this one just prints out the filename that is passed to it.
            static int DisplayEntry(string fName, StatClass stat, int typeFlag) {
                    Console.WriteLine(fName);
                    return 0;
            }

            public static void Main(string[] args){
                    // Call the native function.
                    // Note the second parameter which represents the delegate (callback).
                    ftw(".", DisplayEntry, 10);
            }
    }

    // The native callback takes a pointer to a struct. The below class
    // represents that struct in managed code. You can find more information
    // about this in the section on marshalling below.
    [StructLayout(LayoutKind.Sequential)]
    public class StatClass {
            public uint DeviceID;
            public uint InodeNumber;
            public uint Mode;
            public uint HardLinks;
            public uint UserID;
            public uint GroupID;
            public uint SpecialDeviceID;
            public ulong Size;
            public ulong BlockSize;
            public uint Blocks;
            public long TimeLastAccess;
            public long TimeLastModification;
            public long TimeLastStatusChange;
    }
}
```

Un exemple Mac OS utilise la même fonction et la seule différence réside dans l’argument de l’attribut `DllImport`, car Mac OS conserve `libc` dans un emplacement différent.

```csharp
using System;
using System.Runtime.InteropServices;

namespace PInvokeSamples {
        public static class Program {

                // Define a delegate that has the same signature as the native function.
                delegate int DirClbk(string fName, StatClass stat, int typeFlag);

                // Import the libc and define the method to represent the native function.
                [DllImport("libSystem.dylib")]
                static extern int ftw(string dirpath, DirClbk cl, int descriptors);

                // Implement the above DirClbk delegate;
                // this one just prints out the filename that is passed to it.
                static int DisplayEntry(string fName, StatClass stat, int typeFlag) {
                        Console.WriteLine(fName);
                        return 0;
                }

                public static void Main(string[] args){
                        // Call the native function.
                        // Note the second parameter which represents the delegate (callback).
                        ftw(".", DisplayEntry, 10);
                }
        }

        // The native callback takes a pointer to a struct. The below class
        // represents that struct in managed code.
        [StructLayout(LayoutKind.Sequential)]
        public class StatClass {
                public uint DeviceID;
                public uint InodeNumber;
                public uint Mode;
                public uint HardLinks;
                public uint UserID;
                public uint GroupID;
                public uint SpecialDeviceID;
                public ulong Size;
                public ulong BlockSize;
                public uint Blocks;
                public long TimeLastAccess;
                public long TimeLastModification;
                public long TimeLastStatusChange;
        }
}
```

Les deux exemples précédents dépendent de paramètres et dans les deux cas, les paramètres sont fournis comme des types managés. Le runtime prend « la bonne décision » et les traite dans leurs équivalents de l’autre côté. En savoir plus sur la façon dont les types sont marshalés en code natif sur notre page consacrée au [Marshalling de types](type-marshalling.md).

## <a name="more-resources"></a>Autres ressources

*   [Wiki PInvoke.net](https://www.pinvoke.net/), un excellent Wiki avec des informations sur les API Windows courantes et comment les appeler.
*   [P/Invoke sur MSDN](/cpp/dotnet/native-and-dotnet-interoperability)
*   [Documentation Mono sur P/Invoke](https://www.mono-project.com/docs/advanced/pinvoke/)
