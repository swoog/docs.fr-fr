---
title: Skip While, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkipWhile
helpviewer_keywords:
- Skip While statement [Visual Basic]
- Skip While clause [Visual Basic]
- queries [Visual Basic], Skip While
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
ms.openlocfilehash: 9d95dc4a9f61a9ec3a50f9d594b31d673c2d3764
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602017"
---
# <a name="skip-while-clause-visual-basic"></a><span data-ttu-id="9a232-102">Skip While, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9a232-102">Skip While Clause (Visual Basic)</span></span>
<span data-ttu-id="9a232-103">Ignore les éléments d'une collection tant qu'une condition spécifiée a la valeur `true`, puis retourne les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="9a232-103">Bypasses elements in a collection as long as a specified condition is `true` and then returns the remaining elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a232-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a232-104">Syntax</span></span>  
  
```  
Skip While expression  
```  
  
## <a name="parts"></a><span data-ttu-id="9a232-105">Composants</span><span class="sxs-lookup"><span data-stu-id="9a232-105">Parts</span></span>  
  
|<span data-ttu-id="9a232-106">Terme</span><span class="sxs-lookup"><span data-stu-id="9a232-106">Term</span></span>|<span data-ttu-id="9a232-107">Définition</span><span class="sxs-lookup"><span data-stu-id="9a232-107">Definition</span></span>|  
|---|---|  
|`expression`|<span data-ttu-id="9a232-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9a232-108">Required.</span></span> <span data-ttu-id="9a232-109">Une expression qui représente une condition pour tester des éléments.</span><span class="sxs-lookup"><span data-stu-id="9a232-109">An expression that represents a condition to test elements for.</span></span> <span data-ttu-id="9a232-110">L’expression doit retourner un `Boolean` valeur ou un équivalent fonctionnel, comme un `Integer` soit évaluée comme une `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="9a232-110">The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9a232-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9a232-111">Remarks</span></span>  
 <span data-ttu-id="9a232-112">Le `Skip While` clause ignore des éléments à partir du début d’un résultat de requête jusqu'à ce que l’élément `expression` retourne `false`.</span><span class="sxs-lookup"><span data-stu-id="9a232-112">The `Skip While` clause bypasses elements from the beginning of a query result until the supplied `expression` returns `false`.</span></span> <span data-ttu-id="9a232-113">Après avoir `expression` retourne `false`, la requête retourne tous les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="9a232-113">After `expression` returns `false`, the query returns all the remaining elements.</span></span> <span data-ttu-id="9a232-114">Le `expression` est ignoré pour les autres résultats.</span><span class="sxs-lookup"><span data-stu-id="9a232-114">The `expression` is ignored for the remaining results.</span></span>  
  
 <span data-ttu-id="9a232-115">Le `Skip While` clause diffère de la `Where` clause qui le `Where` clause peut être utilisée pour exclure tous les éléments d’une requête qui ne respectent pas une condition particulière.</span><span class="sxs-lookup"><span data-stu-id="9a232-115">The `Skip While` clause differs from the `Where` clause in that the `Where` clause can be used to exclude all elements from a query that do not meet a particular condition.</span></span> <span data-ttu-id="9a232-116">Le `Skip While` clause exclut des éléments uniquement jusqu'à la première fois que la condition n’est pas satisfaite.</span><span class="sxs-lookup"><span data-stu-id="9a232-116">The `Skip While` clause excludes elements only until the first time that the condition is not satisfied.</span></span> <span data-ttu-id="9a232-117">Le `Skip While` clause est particulièrement utile lorsque vous travaillez avec un résultat de requête commandé.</span><span class="sxs-lookup"><span data-stu-id="9a232-117">The `Skip While` clause is most useful when you are working with an ordered query result.</span></span>  
  
 <span data-ttu-id="9a232-118">Vous pouvez ignorer un nombre spécifique de résultats à partir du début d’un résultat de requête à l’aide de la `Skip` clause.</span><span class="sxs-lookup"><span data-stu-id="9a232-118">You can bypass a specific number of results from the beginning of a query result by using the `Skip` clause.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a232-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a232-119">Example</span></span>  
 <span data-ttu-id="9a232-120">Le code suivant exemple utilise le `Skip While` clause d’ignorer les résultats jusqu'à ce que le premier client à partir des États-Unis est trouvé.</span><span class="sxs-lookup"><span data-stu-id="9a232-120">The following code example uses the `Skip While` clause to bypass results until the first customer from the United States is found.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#3](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/skip-while-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="9a232-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a232-121">See Also</span></span>  
 [<span data-ttu-id="9a232-122">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9a232-122">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="9a232-123">Requêtes</span><span class="sxs-lookup"><span data-stu-id="9a232-123">Queries</span></span>](../../../visual-basic/language-reference/queries/queries.md)  
 [<span data-ttu-id="9a232-124">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="9a232-124">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="9a232-125">From (clause)</span><span class="sxs-lookup"><span data-stu-id="9a232-125">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
 [<span data-ttu-id="9a232-126">Skip (clause)</span><span class="sxs-lookup"><span data-stu-id="9a232-126">Skip Clause</span></span>](../../../visual-basic/language-reference/queries/skip-clause.md)  
 [<span data-ttu-id="9a232-127">Take While (clause)</span><span class="sxs-lookup"><span data-stu-id="9a232-127">Take While Clause</span></span>](../../../visual-basic/language-reference/queries/take-while-clause.md)  
 [<span data-ttu-id="9a232-128">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="9a232-128">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
