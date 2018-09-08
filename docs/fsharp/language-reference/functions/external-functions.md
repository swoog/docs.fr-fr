---
title: Fonctions externes (F#)
description: 'En savoir plus sur la prise en charge de langage F # pour appeler des fonctions en code natif.'
ms.date: 05/16/2016
ms.openlocfilehash: db0d3362d867b07b333951f3380c6735ff471d5e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44181415"
---
# <a name="external-functions"></a><span data-ttu-id="66148-103">Fonctions externes</span><span class="sxs-lookup"><span data-stu-id="66148-103">External Functions</span></span>

<span data-ttu-id="66148-104">Cette rubrique décrit F # prise en charge linguistique pour appeler des fonctions en code natif.</span><span class="sxs-lookup"><span data-stu-id="66148-104">This topic describes F# language support for calling functions in native code.</span></span>

## <a name="syntax"></a><span data-ttu-id="66148-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66148-105">Syntax</span></span>

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a><span data-ttu-id="66148-106">Notes</span><span class="sxs-lookup"><span data-stu-id="66148-106">Remarks</span></span>

<span data-ttu-id="66148-107">Dans la syntaxe précédente, *arguments* représente les arguments fournis à la `System.Runtime.InteropServices.DllImportAttribute` attribut.</span><span class="sxs-lookup"><span data-stu-id="66148-107">In the previous syntax, *arguments* represents arguments that are supplied to the `System.Runtime.InteropServices.DllImportAttribute` attribute.</span></span> <span data-ttu-id="66148-108">Le premier argument est une chaîne qui représente le nom de la DLL qui contient cette fonction, sans l’extension .dll.</span><span class="sxs-lookup"><span data-stu-id="66148-108">The first argument is a string that represents the name of the DLL that contains this function, without the .dll extension.</span></span> <span data-ttu-id="66148-109">Arguments supplémentaires peuvent être fournis pour une des propriétés publiques de la `System.Runtime.InteropServices.DllImportAttribute` classe, tels que la convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="66148-109">Additional arguments can be supplied for any of the public properties of the `System.Runtime.InteropServices.DllImportAttribute` class, such as the calling convention.</span></span>

<span data-ttu-id="66148-110">Vous possédez une DLL C++ qui contient la fonction exportée suivante natif.</span><span class="sxs-lookup"><span data-stu-id="66148-110">Assume you have a native C++ DLL that contains the following exported function.</span></span>

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

<span data-ttu-id="66148-111">Vous pouvez appeler cette fonction à partir de F # en utilisant le code suivant.</span><span class="sxs-lookup"><span data-stu-id="66148-111">You can call this function from F# by using the following code.</span></span>

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

<span data-ttu-id="66148-112">Interopérabilité avec du code natif est appelée *non managé* et est une fonctionnalité du CLR.</span><span class="sxs-lookup"><span data-stu-id="66148-112">Interoperability with native code is referred to as *platform invoke* and is a feature of the CLR.</span></span> <span data-ttu-id="66148-113">Pour plus d’informations, consultez [Interopération avec du code non managé](../../../../docs/framework/interop/index.md).</span><span class="sxs-lookup"><span data-stu-id="66148-113">For more information, see [Interoperating with Unmanaged Code](../../../../docs/framework/interop/index.md).</span></span> <span data-ttu-id="66148-114">Les informations contenues dans cette section sont applique à F #.</span><span class="sxs-lookup"><span data-stu-id="66148-114">The information in that section is applicable to F#.</span></span>

## <a name="see-also"></a><span data-ttu-id="66148-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66148-115">See also</span></span>

- [<span data-ttu-id="66148-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="66148-116">Functions</span></span>](index.md)
