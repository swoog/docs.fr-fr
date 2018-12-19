---
title: '##region - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#region'
helpviewer_keywords:
- '#region directive [C#]'
ms.assetid: 672c87d1-9771-4f64-ab3f-0ad3d4ffb2b4
ms.openlocfilehash: c306511ad8133d0063ccf8b70f2d34d25d2ad3fa
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53244282"
---
# <a name="region-c-reference"></a><span data-ttu-id="9b90e-102">#region (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9b90e-102">#region (C# Reference)</span></span>
<span data-ttu-id="9b90e-103">`#region` vous permet de spécifier un bloc de code que vous pouvez développer ou réduire quand vous utilisez la fonctionnalité [Mode Plan](/visualstudio/ide/outlining) de l’éditeur de code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9b90e-103">`#region` lets you specify a block of code that you can expand or collapse when using the [outlining](/visualstudio/ide/outlining) feature of the Visual Studio Code Editor.</span></span> <span data-ttu-id="9b90e-104">Dans les fichiers de code volumineux, il peut être pratique de réduire ou masquer une ou plusieurs régions pour vous concentrer sur la partie du fichier sur laquelle vous êtes en train de travailler.</span><span class="sxs-lookup"><span data-stu-id="9b90e-104">In longer code files, it is convenient to be able to collapse or hide one or more regions so that you can focus on the part of the file that you are currently working on.</span></span> <span data-ttu-id="9b90e-105">L’exemple suivant montre comment définir une région :</span><span class="sxs-lookup"><span data-stu-id="9b90e-105">The following example shows how to define a region:</span></span>  
  
```csharp
#region MyClass definition  
public class MyClass   
{  
    static void Main()   
    {  
    }  
}  
#endregion  
```  
  
## <a name="remarks"></a><span data-ttu-id="9b90e-106">Notes</span><span class="sxs-lookup"><span data-stu-id="9b90e-106">Remarks</span></span>  
 <span data-ttu-id="9b90e-107">Un bloc `#region` doit se terminer par une directive [#endregion](../../../csharp/language-reference/preprocessor-directives/preprocessor-endregion.md).</span><span class="sxs-lookup"><span data-stu-id="9b90e-107">A `#region` block must be terminated with a [#endregion](../../../csharp/language-reference/preprocessor-directives/preprocessor-endregion.md) directive.</span></span>  
  
 <span data-ttu-id="9b90e-108">Un bloc `#region` ne peut pas chevaucher un bloc [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md).</span><span class="sxs-lookup"><span data-stu-id="9b90e-108">A `#region` block cannot overlap with a [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) block.</span></span> <span data-ttu-id="9b90e-109">Toutefois, un bloc `#region` peut être imbriqué dans un bloc `#if` et, inversement, un bloc `#if` peut être imbriqué dans un bloc `#region`.</span><span class="sxs-lookup"><span data-stu-id="9b90e-109">However, a `#region` block can be nested in a `#if` block, and a `#if` block can be nested in a `#region` block.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b90e-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b90e-110">See Also</span></span>

- [<span data-ttu-id="9b90e-111">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9b90e-111">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="9b90e-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9b90e-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9b90e-113">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="9b90e-113">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
