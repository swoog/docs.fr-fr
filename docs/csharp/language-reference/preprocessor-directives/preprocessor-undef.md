---
title: '#undef - Référence sur C#'
ms.custom: seodec18
ms.date: 06/30/2018
f1_keywords:
- '#undef'
helpviewer_keywords:
- '#undef directive [C#]'
ms.assetid: 686c92d2-7194-4be4-b2f4-80091712d513
ms.openlocfilehash: 0dedd1480dae15d2c04b47cee132ab3227098f56
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54739027"
---
# <a name="undef-c-reference"></a><span data-ttu-id="4843c-102">#undef (référence C#)</span><span class="sxs-lookup"><span data-stu-id="4843c-102">#undef (C# Reference)</span></span>
<span data-ttu-id="4843c-103">`#undef` vous permet d’annuler la définition d’un symbole de telle sorte qu’en utilisant le symbole comme expression dans une directive [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md), l’expression correspond à `false`.</span><span class="sxs-lookup"><span data-stu-id="4843c-103">`#undef` lets you undefine a symbol, such that, by using the symbol as the expression in a [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive, the expression will evaluate to `false`.</span></span>  
  
 <span data-ttu-id="4843c-104">Un symbole peut être défini avec la directive [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) ou l’option du compilateur [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="4843c-104">A symbol can be defined either with the [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) directive or the [-define](../../../csharp/language-reference/compiler-options/define-compiler-option.md) compiler option.</span></span> <span data-ttu-id="4843c-105">La directive `#undef` doit figurer dans le fichier préalablement à l’utilisation d’instructions qui ne sont pas aussi des directives.</span><span class="sxs-lookup"><span data-stu-id="4843c-105">The `#undef` directive must appear in the file before you use any statements that are not also directives.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4843c-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4843c-106">Example</span></span>  

```csharp
// preprocessor_undef.cs  
// compile with: /d:DEBUG  
#undef DEBUG  
using System;  
class MyClass
{  
    static void Main()
    {  
#if DEBUG  
        Console.WriteLine("DEBUG is defined");  
#else  
        Console.WriteLine("DEBUG is not defined");  
#endif  
    }  
}  
```

<span data-ttu-id="4843c-107">**DEBUG n’est pas défini**</span><span class="sxs-lookup"><span data-stu-id="4843c-107">**DEBUG is not defined**</span></span>

## <a name="see-also"></a><span data-ttu-id="4843c-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4843c-108">See also</span></span>

- [<span data-ttu-id="4843c-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="4843c-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="4843c-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="4843c-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="4843c-111">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="4843c-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
