---
title: '#else - Référence C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- '#else'
helpviewer_keywords:
- '#else directive [C#]'
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
ms.openlocfilehash: eabbbb97c42af058c7426d4b72a53b41a96488ed
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237361"
---
# <a name="else-c-reference"></a><span data-ttu-id="9dd64-102">#else (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9dd64-102">#else (C# Reference)</span></span>
<span data-ttu-id="9dd64-103">`#else` vous permet de créer une directive conditionnelle composée de sorte que si aucune des expressions contenues dans les précédentes directives [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) ou [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) (facultatif) n’a la valeur `true`, le compilateur évalue l’ensemble du code entre `#else` et la directive `#endif` suivante.</span><span class="sxs-lookup"><span data-stu-id="9dd64-103">`#else` lets you create a compound conditional directive, so that, if none of the expressions in the preceding [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) or (optional) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) directives evaluate to `true`, the compiler will evaluate all code between `#else` and the subsequent `#endif`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9dd64-104">Notes</span><span class="sxs-lookup"><span data-stu-id="9dd64-104">Remarks</span></span>  
 <span data-ttu-id="9dd64-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) doit être la directive de préprocesseur suivante après `#else`.</span><span class="sxs-lookup"><span data-stu-id="9dd64-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) must be the next preprocessor directive after `#else`.</span></span> <span data-ttu-id="9dd64-106">Consultez [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) pour obtenir un exemple d’utilisation de `#else`.</span><span class="sxs-lookup"><span data-stu-id="9dd64-106">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#else`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9dd64-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9dd64-107">See Also</span></span>

- [<span data-ttu-id="9dd64-108">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9dd64-108">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="9dd64-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9dd64-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="9dd64-110">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="9dd64-110">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
