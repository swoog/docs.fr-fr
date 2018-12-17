---
title: Interopérabilité native
description: Découvrez comment interagir avec les composants natifs dans .NET.
author: blackdwarf
ms.author: ronpet
ms.date: 06/20/2016
ms.technology: dotnet-standard
ms.assetid: 3c357112-35fb-44ba-a07b-6a1c140370ac
ms.openlocfilehash: 2f427eb5d8f41f730d4263425e268213db92236d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53143180"
---
# <a name="native-interoperability"></a><span data-ttu-id="cf9ec-103">Interopérabilité native</span><span class="sxs-lookup"><span data-stu-id="cf9ec-103">Native Interoperability</span></span>

<span data-ttu-id="cf9ec-104">Dans ce document, nous allons approfondir un peu les trois façons disponibles de faire de l’« interopérabilité native » à l’aide de .NET.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-104">In this document, we will dive a little bit deeper into all three ways of doing "native interoperability" that are available using .NET.</span></span>

<span data-ttu-id="cf9ec-105">Voici quelques-unes des raisons qui peuvent vous inciter à appeler du code natif :</span><span class="sxs-lookup"><span data-stu-id="cf9ec-105">There are a few of reasons why you would want to call into native code:</span></span>

*   <span data-ttu-id="cf9ec-106">Les systèmes d’exploitation sont fournis avec un volume important d’API qui ne sont pas présentes dans les bibliothèques de classes managées.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-106">Operating Systems come with a large volume of APIs that are not present in the managed class libraries.</span></span> <span data-ttu-id="cf9ec-107">Un bon exemple est l’accès à des fonctions de gestion de matériel ou de gestion de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-107">A prime example for this would be access to hardware or operating system management functions.</span></span>
*   <span data-ttu-id="cf9ec-108">La communication avec d’autres composants qui ont produit ou peuvent produire des ABI de style C (ABI natifs).</span><span class="sxs-lookup"><span data-stu-id="cf9ec-108">Communicating with other components that have or can produce C-style ABIs (native ABIs).</span></span> <span data-ttu-id="cf9ec-109">Cela concerne, par exemple, le code Java qui est exposé via l’[interface native Java (JNI)](https://docs.oracle.com/javase/8/docs/technotes/guides/jni/) ou tout autre langage managé qui peut produire un composant natif.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-109">This covers, for example, Java code that is exposed via [Java Native Interface (JNI)](https://docs.oracle.com/javase/8/docs/technotes/guides/jni/) or any other managed language that could produce a native component.</span></span>
*   <span data-ttu-id="cf9ec-110">Sur Windows, la plupart des logiciels qui sont installés, comme la suite Microsoft Office, inscrivent des composants COM qui représentent leurs programmes et permettent aux développeurs de les automatiser ou de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-110">On Windows, most of the software that gets installed, such as Microsoft Office suite, registers COM components that represent their programs and allow developers to automate them or use them.</span></span> <span data-ttu-id="cf9ec-111">Cela nécessite également l’interopérabilité native.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-111">This also requires native interoperability.</span></span>

<span data-ttu-id="cf9ec-112">Bien entendu, la liste ci-dessus n’englobe pas toutes les situations et scénarios potentiels dans lesquels le développeur voudrait ou aurait besoin d’interagir avec des composants natifs.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-112">Of course, the list above does not cover all of the potential situations and scenarios in which the developer would want/like/need to interface with native components.</span></span> <span data-ttu-id="cf9ec-113">La bibliothèque de classes .NET, par exemple, utilise la prise en charge de l’interopérabilité native pour implémenter un certain nombre de ses API, comme la prise en charge et la manipulation de la console, l’accès au système de fichiers, etc.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-113">.NET class library, for instance, uses the native interoperability support to implement a fair number of its APIs, like console support and manipulation, file system access and others.</span></span> <span data-ttu-id="cf9ec-114">Notez, toutefois, qu’il existe une option, en cas de besoin.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-114">However, it is important to note that there is an option, should one need it.</span></span>

> [!NOTE]
> <span data-ttu-id="cf9ec-115">La plupart des exemples de ce document sont présentés pour les trois plateformes prises en charge de .NET Core (Windows, Linux et Mac OS).</span><span class="sxs-lookup"><span data-stu-id="cf9ec-115">Most of the examples in this document will be presented for all three supported platforms for .NET Core (Windows, Linux and macOS).</span></span> <span data-ttu-id="cf9ec-116">Toutefois, pour certains exemples courts et illustratifs, seuls des noms de fichiers et des extensions Windows sont cités (par exemple, « dll » pour les bibliothèques).</span><span class="sxs-lookup"><span data-stu-id="cf9ec-116">However, for some short and illustrative examples, just one sample is shown that uses Windows filenames and extensions (that is, "dll" for libraries).</span></span> <span data-ttu-id="cf9ec-117">Cela ne signifie pas que ces fonctionnalités ne sont pas disponibles sur Linux ou Mac OS, cela a été décidé pour plus de commodité.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-117">This does not mean that those features are not available on Linux or macOS, it was done merely for convenience sake.</span></span>

## <a name="platform-invoke-pinvoke"></a><span data-ttu-id="cf9ec-118">Appel de code non managé (P/Invoke)</span><span class="sxs-lookup"><span data-stu-id="cf9ec-118">Platform Invoke (P/Invoke)</span></span>

<span data-ttu-id="cf9ec-119">P/Invoke est une technologie qui vous permet d’accéder aux structures, aux rappels et aux fonctions des bibliothèques non managées à partir de votre code managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-119">P/Invoke is a technology that allows you to access structs, callbacks and functions in unmanaged libraries from your managed code.</span></span> <span data-ttu-id="cf9ec-120">Une grande partie de l’API P/Invoke est contenue dans deux espaces de noms : `System` et `System.Runtime.InteropServices`.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-120">Most of the P/Invoke API is contained in two namespaces: `System` and `System.Runtime.InteropServices`.</span></span> <span data-ttu-id="cf9ec-121">À l’aide de ces deux espaces de noms, vous pouvez accéder aux attributs qui décrivent la façon dont vous voulez communiquer avec le composant natif.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-121">Using these two namespaces will allow you access to the attributes that describe how you want to communicate with the native component.</span></span>

<span data-ttu-id="cf9ec-122">Commençons par l’exemple le plus courant, c’est-à-dire appeler des fonctions non managées dans votre code managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-122">Let’s start from the most common example, and that is calling unmanaged functions in your managed code.</span></span> <span data-ttu-id="cf9ec-123">Nous allons afficher une zone de message à partir d’une application de ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="cf9ec-123">Let’s show a message box from a command-line application:</span></span>

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

<span data-ttu-id="cf9ec-124">L’exemple ci-dessus est relativement simple, mais il ne montre pas ce dont vous avez besoin pour appeler des fonctions non managées à partir de code managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-124">The example above is pretty simple, but it does show off what is needed to invoke unmanaged functions from managed code.</span></span> <span data-ttu-id="cf9ec-125">Examinons l’exemple :</span><span class="sxs-lookup"><span data-stu-id="cf9ec-125">Let’s step through the example:</span></span>

*   <span data-ttu-id="cf9ec-126">La ligne 1 montre l’instruction using de `System.Runtime.InteropServices`, qui est l’espace de noms qui contient tous les éléments dont nous avons besoin.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-126">Line #1 shows the using statement for the `System.Runtime.InteropServices` which is the namespace that holds all of the items we need.</span></span>
*   <span data-ttu-id="cf9ec-127">La ligne 5 introduit l’attribut `DllImport`.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-127">Line #5 introduces the `DllImport` attribute.</span></span> <span data-ttu-id="cf9ec-128">Cet attribut est crucial, car il indique au runtime qu’il doit charger la DLL non managée.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-128">This attribute is crucial, as it tells the runtime that it should load the unmanaged DLL.</span></span> <span data-ttu-id="cf9ec-129">Il s’agit de la DLL dans laquelle nous voulons effectuer des appels.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-129">This is the DLL into which we wish to invoke.</span></span>
*   <span data-ttu-id="cf9ec-130">La ligne 6 est l’essentiel du travail de P/Invoke.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-130">Line #6 is the crux of the P/Invoke work.</span></span> <span data-ttu-id="cf9ec-131">Elle définit une méthode managée qui a **exactement la même signature** que la méthode non managée.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-131">It defines a managed method that has the **exact same signature** as the unmanaged one.</span></span> <span data-ttu-id="cf9ec-132">Notez que la déclaration a un nouveau mot clé, `extern`, qui indique au runtime qu’il s’agit d’une méthode externe et que, quand vous l’appelez, le runtime doit la trouver dans la DLL spécifiée dans l’attribut `DllImport`.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-132">The declaration has a new keyword that you can notice, `extern`, which tells the runtime this is an external method, and that when you invoke it, the runtime should find it in the DLL specified in `DllImport` attribute.</span></span>

<span data-ttu-id="cf9ec-133">Le reste de l’exemple appelle simplement la méthode comme toute autre méthode managée.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-133">The rest of the example is just invoking the method as you would any other managed method.</span></span>

<span data-ttu-id="cf9ec-134">L’exemple est similaire pour Mac OS.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-134">The sample is similar for macOS.</span></span> <span data-ttu-id="cf9ec-135">La seule chose que vous devez modifier est, bien sûr, le nom de la bibliothèque dans l’attribut `DllImport`, car Mac OS a un schéma de nommage des bibliothèques dynamiques différent.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-135">One thing that needs to change is, of course, the name of the library in the `DllImport` attribute, as macOS has a different scheme of naming dynamic libraries.</span></span> <span data-ttu-id="cf9ec-136">L’exemple ci-dessous utilise la fonction `getpid(2)` pour obtenir l’ID de processus de l’application et l’afficher dans la console.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-136">The sample below uses the `getpid(2)` function to get the process ID of the application and print it out to the console.</span></span>

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

<span data-ttu-id="cf9ec-137">Le processus est semblable sur Linux.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-137">It is also similar on Linux.</span></span> <span data-ttu-id="cf9ec-138">Le nom de fonction est le même, car `getpid(2)` est un appel système [POSIX](https://en.wikipedia.org/wiki/POSIX) standard.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-138">The function name is the same, since `getpid(2)` is a standard [POSIX](https://en.wikipedia.org/wiki/POSIX) system call.</span></span>

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

### <a name="invoking-managed-code-from-unmanaged-code"></a><span data-ttu-id="cf9ec-139">Appel de code managé à partir de code non managé</span><span class="sxs-lookup"><span data-stu-id="cf9ec-139">Invoking managed code from unmanaged code</span></span>

<span data-ttu-id="cf9ec-140">Bien entendu, le runtime permet une communication fluide dans les deux sens, ce qui vous donne la possibilité d’effectuer des appels dans des artefacts managés à partir de fonctions natives, à l’aide de pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-140">Of course, the runtime allows communication to flow both ways which enables you to call into managed artifacts from native functions, using function pointers.</span></span> <span data-ttu-id="cf9ec-141">Ce qui ressemble le plus à un pointeur de fonction dans le code managé est un **délégué**, c’est donc ce qui est utilisé pour autoriser les rappels du code natif dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-141">The closest thing to a function pointer in managed code is a **delegate**, so this is what is used to allow callbacks from native code into managed code.</span></span>

<span data-ttu-id="cf9ec-142">La façon d’utiliser cette fonctionnalité est similaire au processus code managé vers code natif décrit plus haut.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-142">The way to use this feature is similar to managed to native process described above.</span></span> <span data-ttu-id="cf9ec-143">Pour un rappel donné, vous définissez un délégué qui correspond à la signature et vous le passez dans la méthode externe.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-143">For a given callback, you define a delegate that matches the signature, and pass that into the external method.</span></span> <span data-ttu-id="cf9ec-144">Le runtime s’occupe du reste.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-144">The runtime will take care of everything else.</span></span>

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

<span data-ttu-id="cf9ec-145">Avant de parcourir notre exemple, passons en revue les signatures des fonctions non managées dont nous avons besoin.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-145">Before we walk through our example, it is good to go over the signatures of the unmanaged functions we need to work with.</span></span> <span data-ttu-id="cf9ec-146">La fonction que nous voulons appeler pour énumérer toutes les fenêtres a la signature suivante : `BOOL EnumWindows (WNDENUMPROC lpEnumFunc, LPARAM lParam);`</span><span class="sxs-lookup"><span data-stu-id="cf9ec-146">The function we want to call to enumerate all of the windows has the following signature: `BOOL EnumWindows (WNDENUMPROC lpEnumFunc, LPARAM lParam);`</span></span>

<span data-ttu-id="cf9ec-147">Le premier paramètre est un rappel.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-147">The first parameter is a callback.</span></span> <span data-ttu-id="cf9ec-148">Ce rappel a la signature suivante : `BOOL CALLBACK EnumWindowsProc (HWND hwnd, LPARAM lParam);`</span><span class="sxs-lookup"><span data-stu-id="cf9ec-148">The said callback has the following signature: `BOOL CALLBACK EnumWindowsProc (HWND hwnd, LPARAM lParam);`</span></span>

<span data-ttu-id="cf9ec-149">Maintenant, examinons l’exemple :</span><span class="sxs-lookup"><span data-stu-id="cf9ec-149">With this in mind, let’s walk through the example:</span></span>

*   <span data-ttu-id="cf9ec-150">La ligne 8 dans l’exemple définit un délégué qui correspond à la signature du rappel dans le code non managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-150">Line #8 in the example defines a delegate that matches the signature of the callback from unmanaged code.</span></span> <span data-ttu-id="cf9ec-151">Notez la façon dont les types LPARAM et HWND sont représentés à l’aide de `IntPtr` dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-151">Notice how the LPARAM and HWND types are represented using `IntPtr` in the managed code.</span></span>
*   <span data-ttu-id="cf9ec-152">Les lignes 10 et 11 introduisent la fonction `EnumWindows` de la bibliothèque user32.dll.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-152">Lines #10 and #11 introduce the `EnumWindows` function from the user32.dll library.</span></span>
*   <span data-ttu-id="cf9ec-153">Les lignes 13 à 16 implémentent le délégué.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-153">Lines #13 - 16 implement the delegate.</span></span> <span data-ttu-id="cf9ec-154">Dans cet exemple simple, nous voulons simplement générer le handle dans la console.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-154">For this simple example, we just want to output the handle to the console.</span></span>
*   <span data-ttu-id="cf9ec-155">Enfin, dans la ligne 19, nous appelons la méthode externe et transmettons le délégué.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-155">Finally, in line #19 we invoke the external method and pass in the delegate.</span></span>

<span data-ttu-id="cf9ec-156">Les exemples de Linux et Mac OS sont présentés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-156">The Linux and macOS examples are shown below.</span></span> <span data-ttu-id="cf9ec-157">Dans ces exemples, nous utilisons la fonction `ftw` qui se trouve dans `libc`, la bibliothèque C.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-157">For them, we use the `ftw` function that can be found in `libc`, the C library.</span></span> <span data-ttu-id="cf9ec-158">Cette fonction est utilisée pour parcourir des hiérarchies de répertoires et accepte un pointeur vers une fonction comme l’un de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-158">This function is used to traverse directory hierarchies and it takes a pointer to a function as one of its parameters.</span></span> <span data-ttu-id="cf9ec-159">Cette fonction a la signature suivante : `int (*fn) (const char *fpath, const struct stat *sb, int typeflag)`.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-159">The said function has the following signature: `int (*fn) (const char *fpath, const struct stat *sb, int typeflag)`.</span></span>

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

<span data-ttu-id="cf9ec-160">Un exemple Mac OS utilise la même fonction et la seule différence réside dans l’argument de l’attribut `DllImport`, car Mac OS conserve `libc` dans un emplacement différent.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-160">macOS example uses the same function, and the only difference is the argument to the `DllImport` attribute, as macOS keeps `libc` in a different place.</span></span>

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

<span data-ttu-id="cf9ec-161">Les deux exemples ci-dessus dépendent de paramètres et dans les deux cas, les paramètres sont fournis comme des types managés.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-161">Both of the above examples depend on parameters, and in both cases, the parameters are given as managed types.</span></span> <span data-ttu-id="cf9ec-162">Le runtime prend « la bonne décision » et les traite dans leurs équivalents de l’autre côté.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-162">Runtime does the "right thing" and processes these into its equivalents on the other side.</span></span> <span data-ttu-id="cf9ec-163">Étant donné que ce processus est très important pour écrire du code interop natif de qualité, jetons un œil à ce qui se produit quand le runtime _marshale_ les types.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-163">Since this process is really important to writing quality native interop code, let’s take a look at what happens when the runtime _marshals_ the types.</span></span>

## <a name="type-marshalling"></a><span data-ttu-id="cf9ec-164">Marshaling de types</span><span class="sxs-lookup"><span data-stu-id="cf9ec-164">Type marshalling</span></span>

<span data-ttu-id="cf9ec-165">Le **marshaling** est le processus de transformation des types quand ils doivent franchir la limite entre code managé et code natif.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-165">**Marshalling** is the process of transforming types when they need to cross the managed boundary into native and vice versa.</span></span>

<span data-ttu-id="cf9ec-166">La raison pour laquelle le marshaling est nécessaire est que les types des codes managé et non managé sont différents.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-166">The reason marshalling is needed is because the types in the managed and unmanaged code are different.</span></span> <span data-ttu-id="cf9ec-167">Dans le code managé, par exemple, vous avez un élément `String`, tandis que dans le monde non managé, les chaînes peuvent être Unicode (« larges »), non-Unicode, terminées par Null, ASCII, etc. Par défaut, le sous-système P/Invoke tente de prendre la bonne décision en fonction du [comportement par défaut](../../docs/framework/interop/default-marshaling-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="cf9ec-167">In managed code, for instance, you have a `String`, while in the unmanaged world strings can be Unicode ("wide"), non-Unicode, null-terminated, ASCII, etc. By default, the P/Invoke subsystem will try to do the right thing based on the [default behavior](../../docs/framework/interop/default-marshaling-behavior.md).</span></span> <span data-ttu-id="cf9ec-168">Toutefois, dans les cas où vous avez besoin de plus de contrôle, vous pouvez employer l’attribut [MarshalAs](xref:System.Runtime.InteropServicxes.MarshalAs) pour spécifier le type attendu du côté du code non managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-168">However, for those situations where you need extra control, you can employ the [MarshalAs](xref:System.Runtime.InteropServicxes.MarshalAs) attribute to specify what is the expected type on the unmanaged side.</span></span> <span data-ttu-id="cf9ec-169">Par exemple, si nous voulons que la chaîne soit envoyée sous forme de chaîne ANSI terminée par Null, nous pouvons procéder comme suit :</span><span class="sxs-lookup"><span data-stu-id="cf9ec-169">For instance, if we want the string to be sent as a null-terminated ANSI string, we could do it like this:</span></span>

```csharp
[DllImport("somenativelibrary.dll")]
static extern int MethodA([MarshalAs(UnmanagedType.LPStr)] string parameter);
```

### <a name="marshalling-classes-and-structs"></a><span data-ttu-id="cf9ec-170">Marshaling de classes et de structures</span><span class="sxs-lookup"><span data-stu-id="cf9ec-170">Marshalling classes and structs</span></span>

<span data-ttu-id="cf9ec-171">Un autre aspect du marshaling de types consiste à passer une structure à une méthode non managée.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-171">Another aspect of type marshalling is how to pass in a struct to an unmanaged method.</span></span> <span data-ttu-id="cf9ec-172">Par exemple, certaines des méthodes non managées nécessitent une structure comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-172">For instance, some of the unmanaged methods require a struct as a parameter.</span></span> <span data-ttu-id="cf9ec-173">Dans ce cas, nous devons créer une structure ou une classe correspondante dans la partie managée de l’environnement pour l’utiliser comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-173">In these cases, we need to create a corresponding struct or a class in managed part of the world to use it as a parameter.</span></span> <span data-ttu-id="cf9ec-174">Toutefois, cela ne suffit pas de définir la classe, nous devons aussi indiquer au marshaleur comment mapper des champs de la classe à la structure non managée.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-174">However, just defining the class is not enough, we also need to instruct the marshaler how to map fields in the class to the unmanaged struct.</span></span> <span data-ttu-id="cf9ec-175">C’est là qu’intervient l’attribut `StructLayout`.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-175">This is where the `StructLayout` attribute comes into play.</span></span>

```csharp
[DllImport("kernel32.dll")]
static extern void GetSystemTime(SystemTime systemTime);

[StructLayout(LayoutKind.Sequential)]
class SystemTime {
    public ushort Year;
    public ushort Month;
    public ushort DayOfWeek;
    public ushort Day;
    public ushort Hour;
    public ushort Minute;
    public ushort Second;
    public ushort Milsecond;
}

public static void Main(string[] args) {
    SystemTime st = new SystemTime();
    GetSystemTime(st);
    Console.WriteLine(st.Year);
}
```

<span data-ttu-id="cf9ec-176">L’exemple ci-dessus illustre de manière simple les appels dans la fonction `GetSystemTime()`.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-176">The example above shows off a simple example of calling into `GetSystemTime()` function.</span></span> <span data-ttu-id="cf9ec-177">L’élément digne d’intérêt se trouve sur la ligne 4.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-177">The interesting bit is on line 4.</span></span> <span data-ttu-id="cf9ec-178">L’attribut spécifie que les champs de la classe doivent être mappés séquentiellement à la structure de l’autre côté (non managé).</span><span class="sxs-lookup"><span data-stu-id="cf9ec-178">The attribute specifies that the fields of the class should be mapped sequentially to the struct on the other (unmanaged) side.</span></span> <span data-ttu-id="cf9ec-179">Cela signifie que le nom des champs n’a pas d’importance, seul leur ordre compte, car il doit correspondre à la structure non managée, comme illustré ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="cf9ec-179">This means that the naming of the fields is not important, only their order is important, as it needs to correspond to the unmanaged struct, shown below:</span></span>

```c
typedef struct _SYSTEMTIME {
  WORD wYear;
  WORD wMonth;
  WORD wDayOfWeek;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
  WORD wMilliseconds;
} SYSTEMTIME, *PSYSTEMTIME*;
```

<span data-ttu-id="cf9ec-180">Nous avons déjà vu l’exemple correspondant sur Linux et Mac OS dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-180">We already saw the Linux and macOS example for this in the previous example.</span></span> <span data-ttu-id="cf9ec-181">Il est représenté ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-181">It is shown again below.</span></span>

```csharp
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
```

<span data-ttu-id="cf9ec-182">La classe `StatClass` représente une structure qui est retournée par l’appel du système `stat` sur les systèmes UNIX.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-182">The `StatClass` class represents a structure that is returned by the `stat` system call on UNIX systems.</span></span> <span data-ttu-id="cf9ec-183">Elle représente les informations d’un fichier donné.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-183">It represents information about a given file.</span></span> <span data-ttu-id="cf9ec-184">La classe ci-dessus est la représentation sous forme de structure stat dans du code managé.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-184">The class above is the stat struct representation in managed code.</span></span> <span data-ttu-id="cf9ec-185">Là encore, les champs de la classe doivent être dans le même ordre que la structure native (vous pouvez les trouver en parcourant les pages man de votre implémentation UNIX préférée) et ils doivent avoir le même type sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-185">Again, the fields in the class have to be in the same order as the native struct (you can find these by perusing man pages on your favorite UNIX implementation) and they have to be of the same underlying type.</span></span>

## <a name="more-resources"></a><span data-ttu-id="cf9ec-186">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="cf9ec-186">More resources</span></span>

*   <span data-ttu-id="cf9ec-187">[Wiki PInvoke.net](https://www.pinvoke.net/), un excellent Wiki avec des informations sur les API Win32 courantes et comment les appeler.</span><span class="sxs-lookup"><span data-stu-id="cf9ec-187">[PInvoke.net wiki](https://www.pinvoke.net/) an excellent Wiki with information on common Win32 APIs and how to call them.</span></span>
*   [<span data-ttu-id="cf9ec-188">P/Invoke sur MSDN</span><span class="sxs-lookup"><span data-stu-id="cf9ec-188">P/Invoke on MSDN</span></span>](https://msdn.microsoft.com/library/zbz07712.aspx)
*   [<span data-ttu-id="cf9ec-189">Documentation Mono sur P/Invoke</span><span class="sxs-lookup"><span data-stu-id="cf9ec-189">Mono documentation on P/Invoke</span></span>](https://www.mono-project.com/docs/advanced/pinvoke/)
