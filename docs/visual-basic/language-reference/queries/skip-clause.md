---
title: Skip, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkip
helpviewer_keywords:
- queries [Visual Basic], Skip
- Skip statement [Visual Basic]
- Skip clause [Visual Basic]
ms.assetid: f00eb172-3907-4c43-9745-d8546ab86234
ms.openlocfilehash: 1810bf4a6573c6fa36f1d8149bf341d45cfd6f52
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602825"
---
# <a name="skip-clause-visual-basic"></a><span data-ttu-id="d5327-102">Skip, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d5327-102">Skip Clause (Visual Basic)</span></span>
<span data-ttu-id="d5327-103">Ignore un nombre spécifié d’éléments dans une collection, puis retourne les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="d5327-103">Bypasses a specified number of elements in a collection and then returns the remaining elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5327-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5327-104">Syntax</span></span>  
  
```  
Skip count  
```  
  
## <a name="parts"></a><span data-ttu-id="d5327-105">Composants</span><span class="sxs-lookup"><span data-stu-id="d5327-105">Parts</span></span>  
 `count`  
 <span data-ttu-id="d5327-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d5327-106">Required.</span></span> <span data-ttu-id="d5327-107">Une valeur ou une expression qui donne le nombre d’éléments de la séquence à ignorer.</span><span class="sxs-lookup"><span data-stu-id="d5327-107">A value or an expression that evaluates to the number of elements of the sequence to skip.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d5327-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d5327-108">Remarks</span></span>  
 <span data-ttu-id="d5327-109">Le `Skip` clause entraîne une requête à ignorer des éléments au début d’une liste de résultats et retourner les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="d5327-109">The `Skip` clause causes a query to bypass elements at the beginning of a results list and return the remaining elements.</span></span> <span data-ttu-id="d5327-110">Le nombre d’éléments à ignorer est identifié par le `count` paramètre.</span><span class="sxs-lookup"><span data-stu-id="d5327-110">The number of elements to skip is identified by the `count` parameter.</span></span>  
  
 <span data-ttu-id="d5327-111">Vous pouvez utiliser la `Skip` clause avec la `Take` clause pour retourner une plage de données à partir de n’importe quel segment d’une requête.</span><span class="sxs-lookup"><span data-stu-id="d5327-111">You can use the `Skip` clause with the `Take` clause to return a range of data from any segment of a query.</span></span> <span data-ttu-id="d5327-112">Pour ce faire, passez à l’index du premier élément de la plage à la `Skip` clause et la taille de la plage à la `Take` clause.</span><span class="sxs-lookup"><span data-stu-id="d5327-112">To do this, pass the index of the first element of the range to the `Skip` clause and the size of the range to the `Take` clause.</span></span>  
  
 <span data-ttu-id="d5327-113">Lorsque vous utilisez la `Skip` clause dans une requête, vous devrez peut-être également vous assurer que les résultats sont retournés dans un ordre qui activera le `Skip` clause pour ignorer les résultats concernés.</span><span class="sxs-lookup"><span data-stu-id="d5327-113">When you use the `Skip` clause in a query, you may also need to ensure that the results are returned in an order that will enable the `Skip` clause to bypass the intended results.</span></span> <span data-ttu-id="d5327-114">Pour plus d’informations sur le classement des résultats de la requête, consultez [une Clause Order By](../../../visual-basic/language-reference/queries/order-by-clause.md).</span><span class="sxs-lookup"><span data-stu-id="d5327-114">For more information about ordering query results, see [Order By Clause](../../../visual-basic/language-reference/queries/order-by-clause.md).</span></span>  
  
 <span data-ttu-id="d5327-115">Vous pouvez utiliser la `SkipWhile` clause pour spécifier que seuls certains éléments sont ignorés, selon une condition fournie.</span><span class="sxs-lookup"><span data-stu-id="d5327-115">You can use the `SkipWhile` clause to specify that only certain elements are ignored, depending on a supplied condition.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d5327-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="d5327-116">Example</span></span>  
 <span data-ttu-id="d5327-117">Le code suivant utilise des exemple le `Skip` clause avec la `Take` clause pour retourner des données à partir d’une requête dans des pages.</span><span class="sxs-lookup"><span data-stu-id="d5327-117">The following code example uses the `Skip` clause together with the `Take` clause to return data from a query in pages.</span></span> <span data-ttu-id="d5327-118">Le `GetCustomers` fonction utilise le `Skip` clause pour ignorer les clients dans la liste jusqu'à ce que le démarrage fourni valeur d’index et utilise le `Take` clause pour retourner une page de clients à partir de cette valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="d5327-118">The `GetCustomers` function uses the `Skip` clause to bypass the customers in the list until the supplied starting index value, and uses the `Take` clause to return a page of customers starting from that index value.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#1](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/skip-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="d5327-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5327-119">See Also</span></span>  
 [<span data-ttu-id="d5327-120">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d5327-120">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="d5327-121">Requêtes</span><span class="sxs-lookup"><span data-stu-id="d5327-121">Queries</span></span>](../../../visual-basic/language-reference/queries/queries.md)  
 [<span data-ttu-id="d5327-122">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="d5327-122">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="d5327-123">From (clause)</span><span class="sxs-lookup"><span data-stu-id="d5327-123">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
 [<span data-ttu-id="d5327-124">Order By (clause)</span><span class="sxs-lookup"><span data-stu-id="d5327-124">Order By Clause</span></span>](../../../visual-basic/language-reference/queries/order-by-clause.md)  
 [<span data-ttu-id="d5327-125">Skip While (clause)</span><span class="sxs-lookup"><span data-stu-id="d5327-125">Skip While Clause</span></span>](../../../visual-basic/language-reference/queries/skip-while-clause.md)  
 [<span data-ttu-id="d5327-126">Take (clause)</span><span class="sxs-lookup"><span data-stu-id="d5327-126">Take Clause</span></span>](../../../visual-basic/language-reference/queries/take-clause.md)
