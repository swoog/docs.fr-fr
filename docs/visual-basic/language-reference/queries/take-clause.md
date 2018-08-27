---
title: Take, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryTake
helpviewer_keywords:
- Take statement [Visual Basic]
- queries [Visual Basic], Take
- Take clause [Visual Basic]
ms.assetid: 77bf87b2-1476-4456-957f-fee922fbad8c
ms.openlocfilehash: bfaccf470d93a6a72451e7ad8b41e8dbb1171c71
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932468"
---
# <a name="take-clause-visual-basic"></a><span data-ttu-id="36ec8-102">Take, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="36ec8-102">Take Clause (Visual Basic)</span></span>
<span data-ttu-id="36ec8-103">Retourne un nombre spécifié d’éléments contigus à partir du début d’une collection.</span><span class="sxs-lookup"><span data-stu-id="36ec8-103">Returns a specified number of contiguous elements from the start of a collection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="36ec8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36ec8-104">Syntax</span></span>  
  
```  
Take count  
```  
  
## <a name="parts"></a><span data-ttu-id="36ec8-105">Composants</span><span class="sxs-lookup"><span data-stu-id="36ec8-105">Parts</span></span>  
 `count`  
 <span data-ttu-id="36ec8-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="36ec8-106">Required.</span></span> <span data-ttu-id="36ec8-107">Une valeur ou une expression qui correspond au nombre d’éléments de la séquence à retourner.</span><span class="sxs-lookup"><span data-stu-id="36ec8-107">A value or an expression that evaluates to the number of elements of the sequence to return.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="36ec8-108">Notes</span><span class="sxs-lookup"><span data-stu-id="36ec8-108">Remarks</span></span>  
 <span data-ttu-id="36ec8-109">Le `Take` clause entraîne une requête inclure un nombre spécifié d’éléments contigus à partir du début d’une liste de résultats.</span><span class="sxs-lookup"><span data-stu-id="36ec8-109">The `Take` clause causes a query to include a specified number of contiguous elements from the start of a results list.</span></span> <span data-ttu-id="36ec8-110">Le nombre d’éléments à inclure est spécifié par le `count` paramètre.</span><span class="sxs-lookup"><span data-stu-id="36ec8-110">The number of elements to include is specified by the `count` parameter.</span></span>  
  
 <span data-ttu-id="36ec8-111">Vous pouvez utiliser la `Take` clause avec le `Skip` clause pour retourner une plage de données à partir de n’importe quel segment d’une requête.</span><span class="sxs-lookup"><span data-stu-id="36ec8-111">You can use the `Take` clause with the `Skip` clause to return a range of data from any segment of a query.</span></span> <span data-ttu-id="36ec8-112">Pour ce faire, passez à l’index du premier élément de la plage à la `Skip` clause et la taille de la plage à la `Take` clause.</span><span class="sxs-lookup"><span data-stu-id="36ec8-112">To do this, pass the index of the first element of the range to the `Skip` clause and the size of the range to the `Take` clause.</span></span> <span data-ttu-id="36ec8-113">Dans ce cas, le `Take` clause doit être spécifiée après le `Skip` clause.</span><span class="sxs-lookup"><span data-stu-id="36ec8-113">In this case, the `Take` clause must be specified after the `Skip` clause.</span></span>  
  
 <span data-ttu-id="36ec8-114">Lorsque vous utilisez le `Take` clause dans une requête, vous devez également vous assurer que les résultats sont retournés dans un ordre qui permettra la `Take` clause pour inclure les résultats prévus.</span><span class="sxs-lookup"><span data-stu-id="36ec8-114">When you use the `Take` clause in a query, you may also need to ensure that the results are returned in an order that will enable the `Take` clause to include the intended results.</span></span> <span data-ttu-id="36ec8-115">Pour plus d’informations sur le classement des résultats de la requête, consultez [Clause Order By](../../../visual-basic/language-reference/queries/order-by-clause.md).</span><span class="sxs-lookup"><span data-stu-id="36ec8-115">For more information about ordering query results, see [Order By Clause](../../../visual-basic/language-reference/queries/order-by-clause.md).</span></span>  
  
 <span data-ttu-id="36ec8-116">Vous pouvez utiliser le `TakeWhile` clause pour spécifier que seuls certains éléments soient retournés, selon une condition fournie.</span><span class="sxs-lookup"><span data-stu-id="36ec8-116">You can use the `TakeWhile` clause to specify that only certain elements be returned, depending on a supplied condition.</span></span>  
  
## <a name="example"></a><span data-ttu-id="36ec8-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="36ec8-117">Example</span></span>  
 <span data-ttu-id="36ec8-118">Le code suivant exemple utilise le `Take` clause conjointement avec le `Skip` clause pour retourner des données à partir d’une requête dans les pages.</span><span class="sxs-lookup"><span data-stu-id="36ec8-118">The following code example uses the `Take` clause together with the `Skip` clause to return data from a query in pages.</span></span> <span data-ttu-id="36ec8-119">La fonction GetCustomers utilise le `Skip` clause pour ignorer les clients dans la liste jusqu'à ce que le départ fournie valeur d’index et utilise le `Take` clause pour retourner une page de clients à partir de cette valeur d’index.</span><span class="sxs-lookup"><span data-stu-id="36ec8-119">The GetCustomers function uses the `Skip` clause to bypass the customers in the list until the supplied starting index value, and uses the `Take` clause to return a page of customers starting from that index value.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#1](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/take-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="36ec8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36ec8-120">See Also</span></span>  
 [<span data-ttu-id="36ec8-121">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="36ec8-121">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="36ec8-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="36ec8-122">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="36ec8-123">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="36ec8-123">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="36ec8-124">From (clause)</span><span class="sxs-lookup"><span data-stu-id="36ec8-124">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
 [<span data-ttu-id="36ec8-125">Order By (clause)</span><span class="sxs-lookup"><span data-stu-id="36ec8-125">Order By Clause</span></span>](../../../visual-basic/language-reference/queries/order-by-clause.md)  
 [<span data-ttu-id="36ec8-126">Take While (clause)</span><span class="sxs-lookup"><span data-stu-id="36ec8-126">Take While Clause</span></span>](../../../visual-basic/language-reference/queries/take-while-clause.md)  
 [<span data-ttu-id="36ec8-127">Skip (clause)</span><span class="sxs-lookup"><span data-stu-id="36ec8-127">Skip Clause</span></span>](../../../visual-basic/language-reference/queries/skip-clause.md)
