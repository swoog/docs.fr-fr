---
title: '#else (informations de référence sur C#)'
ms.date: 07/20/2015
f1_keywords:
- '#else'
helpviewer_keywords:
- '#else directive [C#]'
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
ms.openlocfilehash: 000cbaac4458a104214e3197442a21dcb4740a37
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932624"
---
# <a name="else-c-reference"></a><span data-ttu-id="1a15e-102">#else (référence C#)</span><span class="sxs-lookup"><span data-stu-id="1a15e-102">#else (C# Reference)</span></span>
<span data-ttu-id="1a15e-103">`#else` vous permet de créer une directive conditionnelle composée de sorte que si aucune des expressions contenues dans les précédentes directives [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) ou [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) (facultatif) n’a la valeur `true`, le compilateur évalue l’ensemble du code entre `#else` et la directive `#endif` suivante.</span><span class="sxs-lookup"><span data-stu-id="1a15e-103">`#else` lets you create a compound conditional directive, so that, if none of the expressions in the preceding [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) or (optional) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) directives evaluate to `true`, the compiler will evaluate all code between `#else` and the subsequent `#endif`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1a15e-104">Notes</span><span class="sxs-lookup"><span data-stu-id="1a15e-104">Remarks</span></span>  
 <span data-ttu-id="1a15e-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) doit être la directive de préprocesseur suivante après `#else`.</span><span class="sxs-lookup"><span data-stu-id="1a15e-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) must be the next preprocessor directive after `#else`.</span></span> <span data-ttu-id="1a15e-106">Consultez [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) pour obtenir un exemple d’utilisation de `#else`.</span><span class="sxs-lookup"><span data-stu-id="1a15e-106">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#else`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a15e-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a15e-107">See Also</span></span>

- [<span data-ttu-id="1a15e-108">Référence C#</span><span class="sxs-lookup"><span data-stu-id="1a15e-108">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="1a15e-109">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1a15e-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="1a15e-110">Directives de préprocesseur C#</span><span class="sxs-lookup"><span data-stu-id="1a15e-110">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
