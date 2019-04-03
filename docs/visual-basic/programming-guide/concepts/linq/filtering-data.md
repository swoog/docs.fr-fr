---
title: Filtrage des données (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 7749519a-7edc-49fe-aef9-6a353864af6c
ms.openlocfilehash: a673126d928a97bf522783e73fc254debe2a9de8
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58837441"
---
# <a name="filtering-data-visual-basic"></a><span data-ttu-id="21979-102">Filtrage des données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="21979-102">Filtering Data (Visual Basic)</span></span>
<span data-ttu-id="21979-103">Le filtrage fait référence à l’opération de restriction du jeu de résultats pour que celui-ci contienne uniquement les éléments qui répondent à une condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="21979-103">Filtering refers to the operation of restricting the result set to contain only those elements that satisfy a specified condition.</span></span> <span data-ttu-id="21979-104">Cette opération est également appelée « sélection ».</span><span class="sxs-lookup"><span data-stu-id="21979-104">It is also known as selection.</span></span>  
  
 <span data-ttu-id="21979-105">L’illustration suivante montre les résultats du filtrage d’une séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="21979-105">The following illustration shows the results of filtering a sequence of characters.</span></span> <span data-ttu-id="21979-106">Le prédicat de l’opération de filtrage spécifie que le caractère doit être « A ».</span><span class="sxs-lookup"><span data-stu-id="21979-106">The predicate for the filtering operation specifies that the character must be 'A'.</span></span>  
  
 ![Diagramme illustrant une opération de filtrage LINQ](./media/filtering-data/linq-filter-operation.png)  
  
 <span data-ttu-id="21979-108">Les méthodes d’opérateurs de requête standard qui effectuent des opérations de sélection sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="21979-108">The standard query operator methods that perform selection are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="21979-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="21979-109">Methods</span></span>  
  
|<span data-ttu-id="21979-110">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="21979-110">Method Name</span></span>|<span data-ttu-id="21979-111">Description</span><span class="sxs-lookup"><span data-stu-id="21979-111">Description</span></span>|<span data-ttu-id="21979-112">Syntaxe d’Expression de requête de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="21979-112">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="21979-113">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="21979-113">More Information</span></span>|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="21979-114">OfType</span><span class="sxs-lookup"><span data-stu-id="21979-114">OfType</span></span>|<span data-ttu-id="21979-115">Sélectionne des valeurs, en fonction de leur capacité à être castées en un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="21979-115">Selects values, depending on their ability to be cast to a specified type.</span></span>|<span data-ttu-id="21979-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="21979-116">Not applicable.</span></span>|<xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.OfType%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="21979-117">Où</span><span class="sxs-lookup"><span data-stu-id="21979-117">Where</span></span>|<span data-ttu-id="21979-118">Sélectionne les valeurs qui sont basées sur une fonction de prédicat.</span><span class="sxs-lookup"><span data-stu-id="21979-118">Selects values that are based on a predicate function.</span></span>|`Where`|<xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Where%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a><span data-ttu-id="21979-119">Exemple de syntaxe d’expression de requête</span><span class="sxs-lookup"><span data-stu-id="21979-119">Query Expression Syntax Example</span></span>  
 <span data-ttu-id="21979-120">L’exemple suivant utilise le `Where` à filtrer dans un tableau les chaînes qui ont une longueur spécifique.</span><span class="sxs-lookup"><span data-stu-id="21979-120">The following example uses the `Where` to filter from an array those strings that have a specific length.</span></span>  
  
```vb  
Dim words() As String = {"the", "quick", "brown", "fox", "jumps"}  
  
Dim query = From word In words   
            Where word.Length = 3   
            Select word  
  
Dim sb As New System.Text.StringBuilder()  
For Each str As String In query  
    sb.AppendLine(str)  
Next  
  
' Display the results.  
MsgBox(sb.ToString())  
  
' This code produces the following output:  
  
' the  
' fox  
```  
  
## <a name="see-also"></a><span data-ttu-id="21979-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21979-121">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="21979-122">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="21979-122">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="21979-123">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="21979-123">Where Clause</span></span>](../../../../visual-basic/language-reference/queries/where-clause.md)
- [<span data-ttu-id="21979-124">Guide pratique pour Filtrer les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="21979-124">How to: Filter Query Results</span></span>](../../../../visual-basic/programming-guide/language-features/linq/how-to-filter-query-results-by-using-linq.md)
- [<span data-ttu-id="21979-125">Guide pratique pour Interroger les métadonnées d’un Assembly avec réflexion (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="21979-125">How to: Query An Assembly's Metadata with Reflection (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-an-assembly-s-metadata-with-reflection-linq.md)
- [<span data-ttu-id="21979-126">Guide pratique pour Interroger des fichiers avec un attribut spécifié ou un nom (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="21979-126">How to: Query for Files with a Specified Attribute or Name (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-for-files-with-a-specified-attribute-or-name.md)
- [<span data-ttu-id="21979-127">Guide pratique pour Trier ou filtrer des données texte par mot ou par champ (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="21979-127">How to: Sort or Filter Text Data by Any Word or Field (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-sort-or-filter-text-data-by-any-word-or-field-linq.md)
