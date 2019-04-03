---
title: Partitionnement des données (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 69c59379-b66e-422c-b324-5b5c07760ef7
ms.openlocfilehash: 2da63a1f6b73c8592d6036a90fa374a0d4385f4c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58839572"
---
# <a name="partitioning-data-visual-basic"></a><span data-ttu-id="77f4a-102">Partitionnement des données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="77f4a-102">Partitioning Data (Visual Basic)</span></span>
<span data-ttu-id="77f4a-103">Le partitionnement dans LINQ désigne l’opération consistant à diviser une séquence d’entrée en deux sections, sans réorganiser les éléments, puis à retourner l’une des sections.</span><span class="sxs-lookup"><span data-stu-id="77f4a-103">Partitioning in LINQ refers to the operation of dividing an input sequence into two sections, without rearranging the elements, and then returning one of the sections.</span></span>  
  
 <span data-ttu-id="77f4a-104">L’illustration suivante montre les résultats de trois opérations de partitionnement différentes sur une séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="77f4a-104">The following illustration shows the results of three different partitioning operations on a sequence of characters.</span></span> <span data-ttu-id="77f4a-105">La première opération retourne les trois premiers éléments de la séquence.</span><span class="sxs-lookup"><span data-stu-id="77f4a-105">The first operation returns the first three elements in the sequence.</span></span> <span data-ttu-id="77f4a-106">La deuxième opération ignore les trois premiers éléments et retourne les éléments restants.</span><span class="sxs-lookup"><span data-stu-id="77f4a-106">The second operation skips the first three elements and returns the remaining elements.</span></span> <span data-ttu-id="77f4a-107">La troisième opération ignore les deux premiers éléments de la séquence et retourne les trois éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="77f4a-107">The third operation skips the first two elements in the sequence and returns the next three elements.</span></span>  
  
 ![Illustration des trois opérations de partitionnement LINQ.](./media/partitioning-data/linq-partitioning-operations.png)  
  
 <span data-ttu-id="77f4a-109">Les méthodes d’opérateurs de requête standard qui partitionnent des séquences sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="77f4a-109">The standard query operator methods that partition sequences are listed in the following section.</span></span>  
  
## <a name="operators"></a><span data-ttu-id="77f4a-110">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="77f4a-110">Operators</span></span>  
  
|<span data-ttu-id="77f4a-111">Nom d'opérateur</span><span class="sxs-lookup"><span data-stu-id="77f4a-111">Operator Name</span></span>|<span data-ttu-id="77f4a-112">Description</span><span class="sxs-lookup"><span data-stu-id="77f4a-112">Description</span></span>|<span data-ttu-id="77f4a-113">Syntaxe d’Expression de requête de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="77f4a-113">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="77f4a-114">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="77f4a-114">More Information</span></span>|  
|-------------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="77f4a-115">Ignorer</span><span class="sxs-lookup"><span data-stu-id="77f4a-115">Skip</span></span>|<span data-ttu-id="77f4a-116">Ignore les éléments jusqu’à une position spécifiée dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="77f4a-116">Skips elements up to a specified position in a sequence.</span></span>|`Skip`|<xref:System.Linq.Enumerable.Skip%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Skip%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="77f4a-117">SkipWhile</span><span class="sxs-lookup"><span data-stu-id="77f4a-117">SkipWhile</span></span>|<span data-ttu-id="77f4a-118">Ignore les éléments basés sur une fonction de prédicat jusqu’à un élément qui ne remplit pas la condition.</span><span class="sxs-lookup"><span data-stu-id="77f4a-118">Skips elements based on a predicate function until an element does not satisfy the condition.</span></span>|`Skip While`|<xref:System.Linq.Enumerable.SkipWhile%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.SkipWhile%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="77f4a-119">Take</span><span class="sxs-lookup"><span data-stu-id="77f4a-119">Take</span></span>|<span data-ttu-id="77f4a-120">Prend les éléments jusqu’à une position spécifiée dans une séquence.</span><span class="sxs-lookup"><span data-stu-id="77f4a-120">Takes elements up to a specified position in a sequence.</span></span>|`Take`|<xref:System.Linq.Enumerable.Take%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Take%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="77f4a-121">TakeWhile</span><span class="sxs-lookup"><span data-stu-id="77f4a-121">TakeWhile</span></span>|<span data-ttu-id="77f4a-122">Prend les éléments basés sur une fonction de prédicat jusqu’à un élément qui ne remplit pas la condition.</span><span class="sxs-lookup"><span data-stu-id="77f4a-122">Takes elements based on a predicate function until an element does not satisfy the condition.</span></span>|`Take While`|<xref:System.Linq.Enumerable.TakeWhile%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.TakeWhile%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-examples"></a><span data-ttu-id="77f4a-123">Exemples de syntaxe d'expression de requête</span><span class="sxs-lookup"><span data-stu-id="77f4a-123">Query Expression Syntax Examples</span></span>  
  
### <a name="skip"></a><span data-ttu-id="77f4a-124">Ignorer</span><span class="sxs-lookup"><span data-stu-id="77f4a-124">Skip</span></span>  
 <span data-ttu-id="77f4a-125">Le code suivant exemple utilise le `Skip` clause en Visual Basic pour ignorer les quatre premières chaînes dans un tableau de chaînes avant de retourner le reste des chaînes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="77f4a-125">The following code example uses the `Skip` clause in Visual Basic to skip over the first four strings in an array of strings before returning the remaining strings in the array.</span></span>  
  
 [!code-vb[CsLINQPartitioning#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQPartitioning/VB/Partitioning.vb#1)]  
  
### <a name="skipwhile"></a><span data-ttu-id="77f4a-126">SkipWhile</span><span class="sxs-lookup"><span data-stu-id="77f4a-126">SkipWhile</span></span>  
 <span data-ttu-id="77f4a-127">Le code suivant exemple utilise le `Skip While` clause en Visual Basic pour ignorer les chaînes dans un tableau pendant que la première lettre de la chaîne est « a ».</span><span class="sxs-lookup"><span data-stu-id="77f4a-127">The following code example uses the `Skip While` clause in Visual Basic to skip over the strings in an array while the first letter of the string is "a".</span></span> <span data-ttu-id="77f4a-128">Les chaînes restantes dans le tableau sont retournés.</span><span class="sxs-lookup"><span data-stu-id="77f4a-128">The remaining strings in the array are returned.</span></span>  
  
 [!code-vb[CsLINQPartitioning#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQPartitioning/VB/Partitioning.vb#2)]  
  
### <a name="take"></a><span data-ttu-id="77f4a-129">Take</span><span class="sxs-lookup"><span data-stu-id="77f4a-129">Take</span></span>  
 <span data-ttu-id="77f4a-130">Le code suivant exemple utilise le `Take` clause en Visual Basic pour retourner les deux premières chaînes dans un tableau de chaînes.</span><span class="sxs-lookup"><span data-stu-id="77f4a-130">The following code example uses the `Take` clause in Visual Basic to return the first two strings in an array of strings.</span></span>  
  
 [!code-vb[CsLINQPartitioning#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQPartitioning/VB/Partitioning.vb#3)]  
  
### <a name="takewhile"></a><span data-ttu-id="77f4a-131">TakeWhile</span><span class="sxs-lookup"><span data-stu-id="77f4a-131">TakeWhile</span></span>  
 <span data-ttu-id="77f4a-132">Le code suivant exemple utilise le `Take While` clause en Visual Basic pour retourner des chaînes à partir d’un tableau alors que la longueur de la chaîne est inférieur ou égal à cinq.</span><span class="sxs-lookup"><span data-stu-id="77f4a-132">The following code example uses the `Take While` clause in Visual Basic to return strings from an array while the length of the string is five or less.</span></span>  
  
 [!code-vb[CsLINQPartitioning#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/CsLINQPartitioning/VB/Partitioning.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="77f4a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77f4a-133">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="77f4a-134">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="77f4a-134">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="77f4a-135">Skip (clause)</span><span class="sxs-lookup"><span data-stu-id="77f4a-135">Skip Clause</span></span>](../../../../visual-basic/language-reference/queries/skip-clause.md)
- [<span data-ttu-id="77f4a-136">Skip While (clause)</span><span class="sxs-lookup"><span data-stu-id="77f4a-136">Skip While Clause</span></span>](../../../../visual-basic/language-reference/queries/skip-while-clause.md)
- [<span data-ttu-id="77f4a-137">Take (clause)</span><span class="sxs-lookup"><span data-stu-id="77f4a-137">Take Clause</span></span>](../../../../visual-basic/language-reference/queries/take-clause.md)
- [<span data-ttu-id="77f4a-138">Take While (clause)</span><span class="sxs-lookup"><span data-stu-id="77f4a-138">Take While Clause</span></span>](../../../../visual-basic/language-reference/queries/take-while-clause.md)
