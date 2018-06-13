---
title: Order By, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryOrderBy
- vb.QueryAscending
- vb.QueryDescending
helpviewer_keywords:
- queries [Visual Basic], Order By
- Order By clause [Visual Basic]
- Order By statement [Visual Basic]
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
ms.openlocfilehash: 7c60156ee81618530b42d5f61dbcac6f59c4f675
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604118"
---
# <a name="order-by-clause-visual-basic"></a><span data-ttu-id="09779-102">Order By, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="09779-102">Order By Clause (Visual Basic)</span></span>
<span data-ttu-id="09779-103">Spécifie l’ordre de tri pour un résultat de requête.</span><span class="sxs-lookup"><span data-stu-id="09779-103">Specifies the sort order for a query result.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09779-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09779-104">Syntax</span></span>  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## <a name="parts"></a><span data-ttu-id="09779-105">Composants</span><span class="sxs-lookup"><span data-stu-id="09779-105">Parts</span></span>  
 `orderExp1`  
 <span data-ttu-id="09779-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="09779-106">Required.</span></span> <span data-ttu-id="09779-107">Un ou plusieurs champs à partir du résultat de la requête qui identifient l’ordre des valeurs renvoyées.</span><span class="sxs-lookup"><span data-stu-id="09779-107">One or more fields from the current query result that identify how to order the returned values.</span></span> <span data-ttu-id="09779-108">Les noms de champ doivent être séparés par des virgules (,).</span><span class="sxs-lookup"><span data-stu-id="09779-108">The field names must be separated by commas (,).</span></span> <span data-ttu-id="09779-109">Vous pouvez identifier chaque champ de tri dans l’ordre croissant ou décroissant à l’aide de la `Ascending` ou `Descending` mots clés.</span><span class="sxs-lookup"><span data-stu-id="09779-109">You can identify each field as sorted in ascending or descending order by using the `Ascending` or `Descending` keywords.</span></span> <span data-ttu-id="09779-110">Si aucun `Ascending` ou `Descending` mot clé est spécifié, l’ordre de tri par défaut est croissant.</span><span class="sxs-lookup"><span data-stu-id="09779-110">If no `Ascending` or `Descending` keyword is specified, the default sort order is ascending.</span></span> <span data-ttu-id="09779-111">Les champs d’ordre de tri prévalent de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="09779-111">The sort order fields are given precedence from left to right.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="09779-112">Notes</span><span class="sxs-lookup"><span data-stu-id="09779-112">Remarks</span></span>  
 <span data-ttu-id="09779-113">Vous pouvez utiliser la `Order By` clause pour trier les résultats d’une requête.</span><span class="sxs-lookup"><span data-stu-id="09779-113">You can use the `Order By` clause to sort the results of a query.</span></span> <span data-ttu-id="09779-114">Le `Order By` clause peut trier seulement un résultat basé sur la variable de portée de l’étendue actuelle.</span><span class="sxs-lookup"><span data-stu-id="09779-114">The `Order By` clause can only sort a result based on the range variable for the current scope.</span></span> <span data-ttu-id="09779-115">Par exemple, le `Select` clause introduit une nouvelle portée dans une expression de requête avec de nouvelles variables d’itération pour cette étendue.</span><span class="sxs-lookup"><span data-stu-id="09779-115">For example, the `Select` clause introduces a new scope in a query expression with new iteration variables for that scope.</span></span> <span data-ttu-id="09779-116">Les variables définies avant de plage un `Select` clause dans une requête ne sont pas disponibles après la `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="09779-116">Range variables defined before a `Select` clause in a query are not available after the `Select` clause.</span></span> <span data-ttu-id="09779-117">Par conséquent, si vous souhaitez classer vos résultats par un champ qui n’est pas disponible dans le `Select` clause, vous devez placer le `Order By` clause avant le `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="09779-117">Therefore, if you want to order your results by a field that is not available in the `Select` clause, you must put the `Order By` clause before the `Select` clause.</span></span> <span data-ttu-id="09779-118">Un exemple de lorsque vous devez pour cela est lorsque vous souhaitez trier votre requête en fonction de champs qui ne sont pas retournés en tant que partie du résultat.</span><span class="sxs-lookup"><span data-stu-id="09779-118">One example of when you would have to do this is when you want to sort your query by fields that are not returned as part of the result.</span></span>  
  
 <span data-ttu-id="09779-119">Ordre croissant ou décroissant pour un champ est déterminé par l’implémentation de la <xref:System.IComparable> interface pour le type de données du champ.</span><span class="sxs-lookup"><span data-stu-id="09779-119">Ascending and descending order for a field is determined by the implementation of the <xref:System.IComparable> interface for the data type of the field.</span></span> <span data-ttu-id="09779-120">Si le type de données n’implémente pas le <xref:System.IComparable> interface, l’ordre de tri est ignoré.</span><span class="sxs-lookup"><span data-stu-id="09779-120">If the data type does not implement the <xref:System.IComparable> interface, the sort order is ignored.</span></span>  
  
## <a name="example"></a><span data-ttu-id="09779-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="09779-121">Example</span></span>  
 <span data-ttu-id="09779-122">La requête suivante expression utilise une `From` clause pour déclarer une variable de portée `book` pour la `books` collection.</span><span class="sxs-lookup"><span data-stu-id="09779-122">The following query expression uses a `From` clause to declare a range variable `book` for the `books` collection.</span></span> <span data-ttu-id="09779-123">Le `Order By` clause trie les résultats de la requête par prix croissant (la valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="09779-123">The `Order By` clause sorts the query result by price in ascending order (the default).</span></span> <span data-ttu-id="09779-124">La documentation avec le même prix est triée par titre dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="09779-124">Books with the same price are sorted by title in ascending order.</span></span> <span data-ttu-id="09779-125">Le `Select` clause sélectionne le `Title` et `Price` propriétés comme valeurs retournées par la requête.</span><span class="sxs-lookup"><span data-stu-id="09779-125">The `Select` clause selects the `Title` and `Price` properties as the values returned by the query.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#24](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_1.vb)]  
  
## <a name="example"></a><span data-ttu-id="09779-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="09779-126">Example</span></span>  
 <span data-ttu-id="09779-127">La requête suivante expression utilise la `Order By` clause pour trier les résultats de la requête par prix dans l’ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="09779-127">The following query expression uses the `Order By` clause to sort the query result by price in descending order.</span></span> <span data-ttu-id="09779-128">La documentation avec le même prix est triée par titre dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="09779-128">Books with the same price are sorted by title in ascending order.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#25](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_2.vb)]  
  
## <a name="example"></a><span data-ttu-id="09779-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="09779-129">Example</span></span>  
 <span data-ttu-id="09779-130">La requête suivante expression utilise un `Select` clause pour sélectionner le titre du livre, prix, date de publication et l’auteur.</span><span class="sxs-lookup"><span data-stu-id="09779-130">The following query expression uses a `Select` clause to select the book title, price, publish date, and author.</span></span> <span data-ttu-id="09779-131">Il remplit ensuite le `Title`, `Price`, `PublishDate`, et `Author` champs de la variable de portée de la nouvelle étendue.</span><span class="sxs-lookup"><span data-stu-id="09779-131">It then populates the `Title`, `Price`, `PublishDate`, and `Author` fields of the range variable for the new scope.</span></span> <span data-ttu-id="09779-132">Le `Order By` clause classe la nouvelle variable de portée par nom de l’auteur, titre de livre, puis par prix.</span><span class="sxs-lookup"><span data-stu-id="09779-132">The `Order By` clause orders the new range variable by author name, book title, and then price.</span></span> <span data-ttu-id="09779-133">Chaque colonne est triée dans l’ordre par défaut (croissant).</span><span class="sxs-lookup"><span data-stu-id="09779-133">Each column is sorted in the default order (ascending).</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#26](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/order-by-clause_3.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="09779-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09779-134">See Also</span></span>  
 [<span data-ttu-id="09779-135">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="09779-135">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="09779-136">Requêtes</span><span class="sxs-lookup"><span data-stu-id="09779-136">Queries</span></span>](../../../visual-basic/language-reference/queries/queries.md)  
 [<span data-ttu-id="09779-137">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="09779-137">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="09779-138">From (clause)</span><span class="sxs-lookup"><span data-stu-id="09779-138">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
