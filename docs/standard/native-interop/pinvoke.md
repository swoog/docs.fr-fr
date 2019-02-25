---
title: Appel de code non managé (P/Invoke)
description: Découvrez comment appeler des fonctions natives via P/Invoke dans .NET.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: f243fee2b246afff36732d469c6295d7e4b2fd87
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "56411379"
---
# <a name="platform-invoke-pinvoke"></a><span data-ttu-id="b13f5-103">Appel de code non managé (P/Invoke)</span><span class="sxs-lookup"><span data-stu-id="b13f5-103">Platform Invoke (P/Invoke)</span></span>

<span data-ttu-id="b13f5-104">P/Invoke est une technologie qui vous permet d’accéder aux structures, aux rappels et aux fonctions des bibliothèques non managées à partir de votre code managé.</span><span class="sxs-lookup"><span data-stu-id="b13f5-104">P/Invoke is a technology that allows you to access structs, callbacks, and functions in unmanaged libraries from your managed code.</span></span> <span data-ttu-id="b13f5-105">Une grande partie de l’API P/Invoke est contenue dans deux espaces de noms : `System` et `System.Runtime.InteropServices`.</span><span class="sxs-lookup"><span data-stu-id="b13f5-105">Most of the P/Invoke API is contained in two namespaces: `System` and `System.Runtime.InteropServices`.</span></span> <span data-ttu-id="b13f5-106">Utiliser ces deux espaces de noms vous donne les outils pour décrire la façon dont vous voulez communiquer avec le composant natif.</span><span class="sxs-lookup"><span data-stu-id="b13f5-106">Using these two namespaces give you the tools to describe how you want to communicate with the native component.</span></span>

<span data-ttu-id="b13f5-107">Commençons par l’exemple le plus courant, c’est-à-dire appeler des fonctions non managées dans votre code managé.</span><span class="sxs-lookup"><span data-stu-id="b13f5-107">Let’s start from the most common example, and that is calling unmanaged functions in your managed code.</span></span> <span data-ttu-id="b13f5-108">Nous allons afficher une zone de message à partir d’une application de ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="b13f5-108">Let’s show a message box from a command-line application:</span></span>

```csharp
using System.Runtime.InteropServices;

public class Program {

    // Import user32.dll (containing the function we need) and define
    // the method corresponding to the native function.
    [DllImport("user32.dll")]
    public static extern int MessageBox(IntPtr hWnd, String text, String caption, int options);

    public static void Main(string[] args) {
        // Invoke the function as a regular managed method.
        MessageBox(IntPtr.Zero, "Command-line message box", "Attention!", 0);
    }
}
```

<span data-ttu-id="b13f5-109">L’exemple précédent est simple, mais il ne montre pas ce dont vous avez besoin pour appeler des fonctions non managées à partir de code managé.</span><span class="sxs-lookup"><span data-stu-id="b13f5-109">The previous example is simple, but it does show off what's needed to invoke unmanaged functions from managed code.</span></span> <span data-ttu-id="b13f5-110">Examinons l’exemple :</span><span class="sxs-lookup"><span data-stu-id="b13f5-110">Let’s step through the example:</span></span>

*   <span data-ttu-id="b13f5-111">La ligne 1 montre l’instruction d’utilisation de l’espace de noms `System.Runtime.InteropServices`, qui contient tous les éléments dont nous avons besoin.</span><span class="sxs-lookup"><span data-stu-id="b13f5-111">Line #1 shows the using statement for the `System.Runtime.InteropServices` namespace that holds all the items needed.</span></span>
*   <span data-ttu-id="b13f5-112">La ligne 7 introduit l’attribut `DllImport`.</span><span class="sxs-lookup"><span data-stu-id="b13f5-112">Line #7 introduces the `DllImport` attribute.</span></span> <span data-ttu-id="b13f5-113">Cet attribut est crucial, car il indique au runtime qu’il doit charger la DLL non managée.</span><span class="sxs-lookup"><span data-stu-id="b13f5-113">This attribute is crucial, as it tells the runtime that it should load the unmanaged DLL.</span></span> <span data-ttu-id="b13f5-114">La chaîne passée est la DLL où se trouve notre fonction cible.</span><span class="sxs-lookup"><span data-stu-id="b13f5-114">The string passed in is the DLL our target function is in.</span></span>
*   <span data-ttu-id="b13f5-115">La ligne 8 est l’essentiel du travail de P/Invoke.</span><span class="sxs-lookup"><span data-stu-id="b13f5-115">Line #8 is the crux of the P/Invoke work.</span></span> <span data-ttu-id="b13f5-116">Elle définit une méthode managée qui a **exactement la même signature** que la méthode non managée.</span><span class="sxs-lookup"><span data-stu-id="b13f5-116">It defines a managed method that has the **exact same signature** as the unmanaged one.</span></span> <span data-ttu-id="b13f5-117">Notez que la déclaration a un nouveau mot clé, `extern`, qui indique au runtime qu’il s’agit d’une méthode externe et que, quand vous l’appelez, le runtime doit la trouver dans la DLL spécifiée dans l’attribut `DllImport`.</span><span class="sxs-lookup"><span data-stu-id="b13f5-117">The declaration has a new keyword that you can notice, `extern`, which tells the runtime this is an external method, and that when you invoke it, the runtime should find it in the DLL specified in `DllImport` attribute.</span></span>

<span data-ttu-id="b13f5-118">Le reste de l’exemple appelle simplement la méthode comme toute autre méthode managée.</span><span class="sxs-lookup"><span data-stu-id="b13f5-118">The rest of the example is just invoking the method as you would any other managed method.</span></span>

<span data-ttu-id="b13f5-119">L’exemple est similaire pour Mac OS.</span><span class="sxs-lookup"><span data-stu-id="b13f5-119">The sample is similar for macOS.</span></span> <span data-ttu-id="b13f5-120">Le nom de la bibliothèque dans l’attribut `DllImport` doit être modifié, car Mac OS a un schéma de nommage des bibliothèques dynamiques différent.</span><span class="sxs-lookup"><span data-stu-id="b13f5-120">The name of the library in the `DllImport` attribute needs to change since macOS has a different scheme of naming dynamic libraries.</span></span> <span data-ttu-id="b13f5-121">L’exemple suivant utilise la fonction `getpid(2)` pour obtenir l’ID de processus de l’application et l’afficher dans la console :</span><span class="sxs-lookup"><span data-stu-id="b13f5-121">The following sample uses the `getpid(2)` function to get the process ID of the application and print it out to the console:</span></span>

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

<span data-ttu-id="b13f5-122">Le processus est semblable sur Linux.</span><span class="sxs-lookup"><span data-stu-id="b13f5-122">It is also similar on Linux.</span></span> <span data-ttu-id="b13f5-123">Le nom de fonction est le même, car `getpid(2)` est un appel système [POSIX](https://en.wikipedia.org/wiki/POSIX) standard.</span><span class="sxs-lookup"><span data-stu-id="b13f5-123">The function name is the same, since `getpid(2)` is a standard [POSIX](https://en.wikipedia.org/wiki/POSIX) system call.</span></span>

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

## <a name="invoking-managed-code-from-unmanaged-code"></a><span data-ttu-id="b13f5-124">Appel de code managé à partir de code non managé</span><span class="sxs-lookup"><span data-stu-id="b13f5-124">Invoking managed code from unmanaged code</span></span>

<span data-ttu-id="b13f5-125">Le runtime permet une communication fluide dans les deux directions, ce qui vous donne la possibilité d’effectuer des rappels dans du code managés à partir de fonctions natives, à l’aide de pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="b13f5-125">The runtime allows communication to flow in both directions, enabling you to call back into managed code from native functions by using function pointers.</span></span> <span data-ttu-id="b13f5-126">Ce qui ressemble le plus à un pointeur de fonction dans le code managé est un **délégué**, c’est donc ce qui est utilisé pour autoriser les rappels du code natif dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="b13f5-126">The closest thing to a function pointer in managed code is a **delegate**, so this is what is used to allow callbacks from native code into managed code.</span></span>

<span data-ttu-id="b13f5-127">La façon d’utiliser cette fonctionnalité est similaire au processus code managé vers du code natif préalablement décrit.</span><span class="sxs-lookup"><span data-stu-id="b13f5-127">The way to use this feature is similar to the managed to native process previously described.</span></span> <span data-ttu-id="b13f5-128">Pour un rappel donné, vous définissez un délégué qui correspond à la signature et vous le passez dans la méthode externe.</span><span class="sxs-lookup"><span data-stu-id="b13f5-128">For a given callback, you define a delegate that matches the signature and pass that into the external method.</span></span> <span data-ttu-id="b13f5-129">Le runtime s’occupe du reste.</span><span class="sxs-lookup"><span data-stu-id="b13f5-129">The runtime will take care of everything else.</span></span>

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

<span data-ttu-id="b13f5-130">Avant de parcourir l’exemple, passons en revue les signatures des fonctions non managées dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="b13f5-130">Before walking through the example, it's good to review the signatures of the unmanaged functions you need to work with.</span></span> <span data-ttu-id="b13f5-131">La fonction à appeler pour énumérer toutes les fenêtres a la signature suivante : `BOOL EnumWindows (WNDENUMPROC lpEnumFunc, LPARAM lParam);`</span><span class="sxs-lookup"><span data-stu-id="b13f5-131">The function to be called to enumerate all of the windows has the following signature: `BOOL EnumWindows (WNDENUMPROC lpEnumFunc, LPARAM lParam);`</span></span>

<span data-ttu-id="b13f5-132">Le premier paramètre est un rappel.</span><span class="sxs-lookup"><span data-stu-id="b13f5-132">The first parameter is a callback.</span></span> <span data-ttu-id="b13f5-133">Ce rappel a la signature suivante : `BOOL CALLBACK EnumWindowsProc (HWND hwnd, LPARAM lParam);`</span><span class="sxs-lookup"><span data-stu-id="b13f5-133">The said callback has the following signature: `BOOL CALLBACK EnumWindowsProc (HWND hwnd, LPARAM lParam);`</span></span>

<span data-ttu-id="b13f5-134">Examinons maintenant l’exemple en détail :</span><span class="sxs-lookup"><span data-stu-id="b13f5-134">Now, let’s walk through the example:</span></span>

*   <span data-ttu-id="b13f5-135">la ligne 9 dans l’exemple définit un délégué qui correspond à la signature du rappel dans le code non managé.</span><span class="sxs-lookup"><span data-stu-id="b13f5-135">Line #9 in the example defines a delegate that matches the signature of the callback from unmanaged code.</span></span> <span data-ttu-id="b13f5-136">Notez la façon dont les types LPARAM et HWND sont représentés à l’aide de `IntPtr` dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="b13f5-136">Notice how the LPARAM and HWND types are represented using `IntPtr` in the managed code.</span></span>
*   <span data-ttu-id="b13f5-137">Les lignes 13 et 14 introduisent la fonction `EnumWindows` de la bibliothèque user32.dll.</span><span class="sxs-lookup"><span data-stu-id="b13f5-137">Lines #13 and #14 introduce the `EnumWindows` function from the user32.dll library.</span></span>
*   <span data-ttu-id="b13f5-138">Les lignes 17 à 20 implémentent le délégué.</span><span class="sxs-lookup"><span data-stu-id="b13f5-138">Lines #17 - 20 implement the delegate.</span></span> <span data-ttu-id="b13f5-139">Dans cet exemple simple, nous voulons simplement générer le handle dans la console.</span><span class="sxs-lookup"><span data-stu-id="b13f5-139">For this simple example, we just want to output the handle to the console.</span></span>
*   <span data-ttu-id="b13f5-140">Enfin, dans la ligne 24, la méthode externe est appelée et transmise au délégué.</span><span class="sxs-lookup"><span data-stu-id="b13f5-140">Finally, in line #24, the external method is called and passed in the delegate.</span></span>

<span data-ttu-id="b13f5-141">Les exemples de Linux et Mac OS sont présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b13f5-141">The Linux and macOS examples are shown below.</span></span> <span data-ttu-id="b13f5-142">Dans ces exemples, nous utilisons la fonction `ftw` qui se trouve dans `libc`, la bibliothèque C.</span><span class="sxs-lookup"><span data-stu-id="b13f5-142">For them, we use the `ftw` function that can be found in `libc`, the C library.</span></span> <span data-ttu-id="b13f5-143">Cette fonction est utilisée pour parcourir des hiérarchies de répertoires et accepte un pointeur vers une fonction comme l’un de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="b13f5-143">This function is used to traverse directory hierarchies and it takes a pointer to a function as one of its parameters.</span></span> <span data-ttu-id="b13f5-144">Cette fonction a la signature suivante : `int (*fn) (const char *fpath, const struct stat *sb, int typeflag)`.</span><span class="sxs-lookup"><span data-stu-id="b13f5-144">The said function has the following signature: `int (*fn) (const char *fpath, const struct stat *sb, int typeflag)`.</span></span>

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

<span data-ttu-id="b13f5-145">Un exemple Mac OS utilise la même fonction et la seule différence réside dans l’argument de l’attribut `DllImport`, car Mac OS conserve `libc` dans un emplacement différent.</span><span class="sxs-lookup"><span data-stu-id="b13f5-145">macOS example uses the same function, and the only difference is the argument to the `DllImport` attribute, as macOS keeps `libc` in a different place.</span></span>

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

<span data-ttu-id="b13f5-146">Les deux exemples précédents dépendent de paramètres et dans les deux cas, les paramètres sont fournis comme des types managés.</span><span class="sxs-lookup"><span data-stu-id="b13f5-146">Both of the previous examples depend on parameters, and in both cases, the parameters are given as managed types.</span></span> <span data-ttu-id="b13f5-147">Le runtime prend « la bonne décision » et les traite dans leurs équivalents de l’autre côté.</span><span class="sxs-lookup"><span data-stu-id="b13f5-147">Runtime does the "right thing" and processes these into its equivalents on the other side.</span></span> <span data-ttu-id="b13f5-148">En savoir plus sur la façon dont les types sont marshalés en code natif sur notre page consacrée au [Marshalling de types](type-marshalling.md).</span><span class="sxs-lookup"><span data-stu-id="b13f5-148">Learn about how types are marshalled to native code in our page on [Type marshalling](type-marshalling.md).</span></span>


## <a name="more-resources"></a><span data-ttu-id="b13f5-149">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="b13f5-149">More resources</span></span>

*   <span data-ttu-id="b13f5-150">[Wiki PInvoke.net](https://www.pinvoke.net/), un excellent Wiki avec des informations sur les API Win32 courantes et comment les appeler.</span><span class="sxs-lookup"><span data-stu-id="b13f5-150">[PInvoke.net wiki](https://www.pinvoke.net/) an excellent Wiki with information on common Win32 APIs and how to call them.</span></span>
*   [<span data-ttu-id="b13f5-151">P/Invoke sur MSDN</span><span class="sxs-lookup"><span data-stu-id="b13f5-151">P/Invoke on MSDN</span></span>](https://msdn.microsoft.com/library/zbz07712.aspx)
*   [<span data-ttu-id="b13f5-152">Documentation Mono sur P/Invoke</span><span class="sxs-lookup"><span data-stu-id="b13f5-152">Mono documentation on P/Invoke</span></span>](https://www.mono-project.com/docs/advanced/pinvoke/)
