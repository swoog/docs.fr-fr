---
title: Fonctions externes
description: En savoir plus sur les F# prise en charge linguistique pour appeler des fonctions en code natif.
ms.date: 05/16/2016
ms.openlocfilehash: 73e38d8942bfc8ddb3c51d126d7678e84903326b
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65642038"
---
# <a name="external-functions"></a><span data-ttu-id="aa13a-103">Fonctions externes</span><span class="sxs-lookup"><span data-stu-id="aa13a-103">External Functions</span></span>

<span data-ttu-id="aa13a-104">Cette rubrique décrit F# prise en charge linguistique pour appeler des fonctions en code natif.</span><span class="sxs-lookup"><span data-stu-id="aa13a-104">This topic describes F# language support for calling functions in native code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa13a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa13a-105">Syntax</span></span>

```fsharp
[<DllImport( arguments )>]
extern declaration
```

## <a name="remarks"></a><span data-ttu-id="aa13a-106">Notes</span><span class="sxs-lookup"><span data-stu-id="aa13a-106">Remarks</span></span>

<span data-ttu-id="aa13a-107">Dans la syntaxe précédente, *arguments* représente les arguments fournis à la `System.Runtime.InteropServices.DllImportAttribute` attribut.</span><span class="sxs-lookup"><span data-stu-id="aa13a-107">In the previous syntax, *arguments* represents arguments that are supplied to the `System.Runtime.InteropServices.DllImportAttribute` attribute.</span></span> <span data-ttu-id="aa13a-108">Le premier argument est une chaîne qui représente le nom de la DLL qui contient cette fonction, sans l’extension .dll.</span><span class="sxs-lookup"><span data-stu-id="aa13a-108">The first argument is a string that represents the name of the DLL that contains this function, without the .dll extension.</span></span> <span data-ttu-id="aa13a-109">Arguments supplémentaires peuvent être fournis pour une des propriétés publiques de la `System.Runtime.InteropServices.DllImportAttribute` classe, tels que la convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="aa13a-109">Additional arguments can be supplied for any of the public properties of the `System.Runtime.InteropServices.DllImportAttribute` class, such as the calling convention.</span></span>

<span data-ttu-id="aa13a-110">Vous possédez une DLL C++ qui contient la fonction exportée suivante natif.</span><span class="sxs-lookup"><span data-stu-id="aa13a-110">Assume you have a native C++ DLL that contains the following exported function.</span></span>

```cpp
#include <stdio.h>
extern "C" void __declspec(dllexport) HelloWorld()
{
    printf("Hello world, invoked by F#!\n");
}
```

<span data-ttu-id="aa13a-111">Vous pouvez appeler cette fonction à partir de F# en utilisant le code suivant.</span><span class="sxs-lookup"><span data-stu-id="aa13a-111">You can call this function from F# by using the following code.</span></span>

```fsharp
open System.Runtime.InteropServices

module InteropWithNative =
    [<DllImport(@"C:\bin\nativedll", CallingConvention = CallingConvention.Cdecl)>]
    extern void HelloWorld()

InteropWithNative.HelloWorld()
```

<span data-ttu-id="aa13a-112">Interopérabilité avec du code natif est appelée *non managé* et est une fonctionnalité du CLR.</span><span class="sxs-lookup"><span data-stu-id="aa13a-112">Interoperability with native code is referred to as *platform invoke* and is a feature of the CLR.</span></span> <span data-ttu-id="aa13a-113">Pour plus d’informations, consultez [Interopération avec du code non managé](../../../../docs/framework/interop/index.md).</span><span class="sxs-lookup"><span data-stu-id="aa13a-113">For more information, see [Interoperating with Unmanaged Code](../../../../docs/framework/interop/index.md).</span></span> <span data-ttu-id="aa13a-114">Les informations contenues dans cette section sont applique aux F#.</span><span class="sxs-lookup"><span data-stu-id="aa13a-114">The information in that section is applicable to F#.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa13a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa13a-115">See also</span></span>

- [<span data-ttu-id="aa13a-116">Fonctions</span><span class="sxs-lookup"><span data-stu-id="aa13a-116">Functions</span></span>](index.md)
