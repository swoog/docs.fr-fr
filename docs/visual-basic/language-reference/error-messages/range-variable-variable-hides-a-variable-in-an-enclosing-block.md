---
title: La variable de portée '<variable>' masque une variable dans un bloc englobant, une variable de portée précédemment définie ou une variable déclarée implicitement dans une expression de requête
ms.date: 07/20/2015
f1_keywords:
- bc36633
- vbc36633
helpviewer_keywords:
- BC36633
ms.assetid: 5d5470e4-3de5-49c2-8831-1087625f4a77
ms.openlocfilehash: 8d898d2d3c5f36177a6363c1a24940fe46de83d3
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259870"
---
# <a name="range-variable-variable-hides-a-variable-in-an-enclosing-block-a-previously-defined-range-variable-or-an-implicitly-declared-variable-in-a-query-expression"></a><span data-ttu-id="e2402-102">Variable de portée \<variable > masque une variable dans un bloc englobant, une variable de portée précédemment définie ou une variable déclarée implicitement dans une expression de requête</span><span class="sxs-lookup"><span data-stu-id="e2402-102">Range variable \<variable> hides a variable in an enclosing block, a previously defined range variable, or an implicitly declared variable in a query expression</span></span>
<span data-ttu-id="e2402-103">Un nom de variable de plage spécifié dans un `Select`, `From`, `Aggregate`, ou `Let` clause duplique le nom d’une variable de portée spécifié précédemment dans la requête ou le nom d’une variable qui est déclaré implicitement par la requête, comme un nom de champ ou le nom d’une fonction d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="e2402-103">A range variable name specified in a `Select`, `From`, `Aggregate`, or `Let` clause duplicates the name of a range variable already specified previously in the query, or the name of a variable that is implicitly declared by the query, such as a field name or the name of an aggregate function.</span></span>  
  
 <span data-ttu-id="e2402-104">**ID d’erreur :** BC36633</span><span class="sxs-lookup"><span data-stu-id="e2402-104">**Error ID:** BC36633</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e2402-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="e2402-105">To correct this error</span></span>  
  
-   <span data-ttu-id="e2402-106">Assurez-vous que toutes les variables de plage dans une étendue de requête particulière ont des noms uniques.</span><span class="sxs-lookup"><span data-stu-id="e2402-106">Ensure that all range variables in a particular query scope have unique names.</span></span> <span data-ttu-id="e2402-107">Vous pouvez placer une requête entre parenthèses pour garantir que les requêtes imbriquées ont une étendue unique.</span><span class="sxs-lookup"><span data-stu-id="e2402-107">You can enclose a query in parentheses to ensure that nested queries have a unique scope.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2402-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2402-108">See also</span></span>
- [<span data-ttu-id="e2402-109">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="e2402-109">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="e2402-110">From (clause)</span><span class="sxs-lookup"><span data-stu-id="e2402-110">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
- [<span data-ttu-id="e2402-111">Let (clause)</span><span class="sxs-lookup"><span data-stu-id="e2402-111">Let Clause</span></span>](../../../visual-basic/language-reference/queries/let-clause.md)
- [<span data-ttu-id="e2402-112">Aggregate (clause)</span><span class="sxs-lookup"><span data-stu-id="e2402-112">Aggregate Clause</span></span>](../../../visual-basic/language-reference/queries/aggregate-clause.md)
- [<span data-ttu-id="e2402-113">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="e2402-113">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
