---
title: '#endif - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#endif'
helpviewer_keywords:
- '#endif directive [C#]'
ms.assetid: 6a5fca55-5aee-441f-86f6-1c99fbe9ec05
ms.openlocfilehash: 58e29363ca1298966ecf88e6b456f33f43a176b0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54573044"
---
# <a name="endif-c-reference"></a><span data-ttu-id="ca3f7-102">#endif (référence C#)</span><span class="sxs-lookup"><span data-stu-id="ca3f7-102">#endif (C# Reference)</span></span>
<span data-ttu-id="ca3f7-103">`#endif` spécifie la fin d’une directive conditionnelle, qui a commencé avec la directive [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md).</span><span class="sxs-lookup"><span data-stu-id="ca3f7-103">`#endif` specifies the end of a conditional directive, which began with the [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) directive.</span></span> <span data-ttu-id="ca3f7-104">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ca3f7-104">For example,</span></span>  
  
```csharp
#define DEBUG  
// ...  
#if DEBUG  
    Console.WriteLine("Debug version");  
#endif  
```  
  
## <a name="remarks"></a><span data-ttu-id="ca3f7-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ca3f7-105">Remarks</span></span>  
 <span data-ttu-id="ca3f7-106">Une directive conditionnelle commençant par une directive `#if` doit se terminer explicitement par une directive `#endif`.</span><span class="sxs-lookup"><span data-stu-id="ca3f7-106">A conditional directive, beginning with a `#if` directive, must explicitly be terminated with a `#endif` directive.</span></span> <span data-ttu-id="ca3f7-107">Consultez [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) pour obtenir un exemple d’utilisation de `#endif`.</span><span class="sxs-lookup"><span data-stu-id="ca3f7-107">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#endif`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca3f7-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca3f7-108">See also</span></span>

- [<span data-ttu-id="ca3f7-109">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ca3f7-109">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="ca3f7-110">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ca3f7-110">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="ca3f7-111">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="ca3f7-111">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
