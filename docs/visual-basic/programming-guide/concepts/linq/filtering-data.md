---
title: Le filtrage des données (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 7749519a-7edc-49fe-aef9-6a353864af6c
ms.openlocfilehash: d3f44d0b6478103a10fb731988aeebc005cde82e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33644340"
---
# <a name="filtering-data-visual-basic"></a><span data-ttu-id="56573-102">Le filtrage des données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56573-102">Filtering Data (Visual Basic)</span></span>
<span data-ttu-id="56573-103">Le filtrage fait référence à l’opération de restriction du jeu de résultats pour que celui-ci contienne uniquement les éléments qui répondent à une condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="56573-103">Filtering refers to the operation of restricting the result set to contain only those elements that satisfy a specified condition.</span></span> <span data-ttu-id="56573-104">Cette opération est également appelée « sélection ».</span><span class="sxs-lookup"><span data-stu-id="56573-104">It is also known as selection.</span></span>  
  
 <span data-ttu-id="56573-105">L’illustration suivante montre les résultats du filtrage d’une séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="56573-105">The following illustration shows the results of filtering a sequence of characters.</span></span> <span data-ttu-id="56573-106">Le prédicat de l’opération de filtrage spécifie que le caractère doit être « A ».</span><span class="sxs-lookup"><span data-stu-id="56573-106">The predicate for the filtering operation specifies that the character must be 'A'.</span></span>  
  
 <span data-ttu-id="56573-107">![Opération de filtrage LINQ](../../../../csharp/programming-guide/concepts/linq/media/linq_filter.png "LINQ_Filter")</span><span class="sxs-lookup"><span data-stu-id="56573-107">![LINQ Filtering Operation](../../../../csharp/programming-guide/concepts/linq/media/linq_filter.png "LINQ_Filter")</span></span>  
  
 <span data-ttu-id="56573-108">Les méthodes d’opérateurs de requête standard qui effectuent des opérations de sélection sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="56573-108">The standard query operator methods that perform selection are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="56573-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="56573-109">Methods</span></span>  
  
|<span data-ttu-id="56573-110">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="56573-110">Method Name</span></span>|<span data-ttu-id="56573-111">Description</span><span class="sxs-lookup"><span data-stu-id="56573-111">Description</span></span>|<span data-ttu-id="56573-112">Syntaxe d’Expression de requête Visual Basic</span><span class="sxs-lookup"><span data-stu-id="56573-112">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="56573-113">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="56573-113">More Information</span></span>|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="56573-114">OfType</span><span class="sxs-lookup"><span data-stu-id="56573-114">OfType</span></span>|<span data-ttu-id="56573-115">Sélectionne des valeurs, en fonction de leur capacité à être castées en un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="56573-115">Selects values, depending on their ability to be cast to a specified type.</span></span>|<span data-ttu-id="56573-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="56573-116">Not applicable.</span></span>|<xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.OfType%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="56573-117">Où</span><span class="sxs-lookup"><span data-stu-id="56573-117">Where</span></span>|<span data-ttu-id="56573-118">Sélectionne les valeurs qui sont basées sur une fonction de prédicat.</span><span class="sxs-lookup"><span data-stu-id="56573-118">Selects values that are based on a predicate function.</span></span>|`Where`|<xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Where%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a><span data-ttu-id="56573-119">Exemple de syntaxe d’expression de requête</span><span class="sxs-lookup"><span data-stu-id="56573-119">Query Expression Syntax Example</span></span>  
 <span data-ttu-id="56573-120">L’exemple suivant utilise le `Where` à filtrer dans un tableau les chaînes qui ont une longueur spécifique.</span><span class="sxs-lookup"><span data-stu-id="56573-120">The following example uses the `Where` to filter from an array those strings that have a specific length.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="56573-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56573-121">See Also</span></span>  
 <xref:System.Linq>  
 [<span data-ttu-id="56573-122">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56573-122">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)  
 [<span data-ttu-id="56573-123">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="56573-123">Where Clause</span></span>](../../../../visual-basic/language-reference/queries/where-clause.md)  
 [<span data-ttu-id="56573-124">Guide pratique : filtrer les résultats d’une requête</span><span class="sxs-lookup"><span data-stu-id="56573-124">How to: Filter Query Results</span></span>](../../../../visual-basic/programming-guide/language-features/linq/how-to-filter-query-results-by-using-linq.md)  
 [<span data-ttu-id="56573-125">Comment : interroger les métadonnées d’un Assembly avec réflexion (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56573-125">How to: Query An Assembly's Metadata with Reflection (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-an-assembly-s-metadata-with-reflection-linq.md)  
 [<span data-ttu-id="56573-126">Comment : interroger des fichiers avec un attribut spécifié ou le nom (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56573-126">How to: Query for Files with a Specified Attribute or Name (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-query-for-files-with-a-specified-attribute-or-name.md)  
 [<span data-ttu-id="56573-127">Comment : trier ou filtrer des données texte par mot ou par champ (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56573-127">How to: Sort or Filter Text Data by Any Word or Field (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-sort-or-filter-text-data-by-any-word-or-field-linq.md)
