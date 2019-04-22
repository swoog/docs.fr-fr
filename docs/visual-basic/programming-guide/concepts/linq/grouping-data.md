---
title: Regroupement de données (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 8f3a0871-6958-4aef-8f6f-493e189fd57d
ms.openlocfilehash: c658ac5c46baec1bfa976074b78ac86d791b6515
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58842055"
---
# <a name="grouping-data-visual-basic"></a><span data-ttu-id="27134-102">Regroupement de données (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="27134-102">Grouping Data (Visual Basic)</span></span>
<span data-ttu-id="27134-103">Le regroupement consiste à placer des données dans des groupes afin que les éléments de chaque groupe partagent un attribut commun.</span><span class="sxs-lookup"><span data-stu-id="27134-103">Grouping refers to the operation of putting data into groups so that the elements in each group share a common attribute.</span></span>  
  
 <span data-ttu-id="27134-104">L’illustration suivante montre les résultats du regroupement d’une séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="27134-104">The following illustration shows the results of grouping a sequence of characters.</span></span> <span data-ttu-id="27134-105">La clé de chaque groupe est le caractère.</span><span class="sxs-lookup"><span data-stu-id="27134-105">The key for each group is the character.</span></span>  
  
 <span data-ttu-id="27134-106">![Opérations de regroupement LINQ](../../../../csharp/programming-guide/concepts/linq/media/linq_group.png "LINQ_Group")</span><span class="sxs-lookup"><span data-stu-id="27134-106">![LINQ Grouping Operations](../../../../csharp/programming-guide/concepts/linq/media/linq_group.png "LINQ_Group")</span></span>  
  
 <span data-ttu-id="27134-107">Les méthodes d’opérateurs de requête standard qui regroupent les éléments de données sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="27134-107">The standard query operator methods that group data elements are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="27134-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="27134-108">Methods</span></span>  
  
|<span data-ttu-id="27134-109">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="27134-109">Method Name</span></span>|<span data-ttu-id="27134-110">Description</span><span class="sxs-lookup"><span data-stu-id="27134-110">Description</span></span>|<span data-ttu-id="27134-111">Syntaxe d’Expression de requête de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="27134-111">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="27134-112">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="27134-112">More Information</span></span>|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="27134-113">GroupBy</span><span class="sxs-lookup"><span data-stu-id="27134-113">GroupBy</span></span>|<span data-ttu-id="27134-114">Regroupe les éléments qui partagent un attribut commun.</span><span class="sxs-lookup"><span data-stu-id="27134-114">Groups elements that share a common attribute.</span></span> <span data-ttu-id="27134-115">Chaque groupe est représenté par un objet <xref:System.Linq.IGrouping%602>.</span><span class="sxs-lookup"><span data-stu-id="27134-115">Each group is represented by an <xref:System.Linq.IGrouping%602> object.</span></span>|`Group … By … Into …`|<xref:System.Linq.Enumerable.GroupBy%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.GroupBy%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="27134-116">ToLookup</span><span class="sxs-lookup"><span data-stu-id="27134-116">ToLookup</span></span>|<span data-ttu-id="27134-117">Insère des éléments dans un <xref:System.Linq.Lookup%602> (un dictionnaire de type un-à-plusieurs) basé sur une fonction de sélecteur de clés.</span><span class="sxs-lookup"><span data-stu-id="27134-117">Inserts elements into a <xref:System.Linq.Lookup%602> (a one-to-many dictionary) based on a key selector function.</span></span>|<span data-ttu-id="27134-118">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="27134-118">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a><span data-ttu-id="27134-119">Exemple de syntaxe d’expression de requête</span><span class="sxs-lookup"><span data-stu-id="27134-119">Query Expression Syntax Example</span></span>  
 <span data-ttu-id="27134-120">L’exemple de code suivant utilise la clause `Group By` pour regrouper des entiers dans une liste selon qu’ils sont pairs ou impairs.</span><span class="sxs-lookup"><span data-stu-id="27134-120">The following code example uses the `Group By` clause to group integers in a list according to whether they are even or odd.</span></span>  
  
```vb  
Dim numbers As New System.Collections.Generic.List(Of Integer)(  
     New Integer() {35, 44, 200, 84, 3987, 4, 199, 329, 446, 208})  
  
Dim query = From number In numbers   
            Group By Remainder = (number Mod 2) Into Group  
  
Dim sb As New System.Text.StringBuilder()  
For Each group In query  
    sb.AppendLine(If(group.Remainder = 0, vbCrLf & "Even numbers:", vbCrLf & "Odd numbers:"))  
    For Each num In group.Group  
        sb.AppendLine(num)  
    Next  
Next  
  
' Display the results.  
MsgBox(sb.ToString())  
  
' This code produces the following output:  
  
' Odd numbers:  
' 35  
' 3987  
' 199  
' 329  
  
' Even numbers:  
' 44  
' 200  
' 84  
' 4  
' 446  
' 208  
```  
  
## <a name="see-also"></a><span data-ttu-id="27134-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27134-121">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="27134-122">Vue d’ensemble des opérateurs de requête standard (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="27134-122">Standard Query Operators Overview (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="27134-123">Group By (clause)</span><span class="sxs-lookup"><span data-stu-id="27134-123">Group By Clause</span></span>](../../../../visual-basic/language-reference/queries/group-by-clause.md)
- [<span data-ttu-id="27134-124">Guide pratique pour Regrouper les fichiers par Extension (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="27134-124">How to: Group Files by Extension (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-group-files-by-extension-linq.md)
- [<span data-ttu-id="27134-125">Guide pratique pour Fractionner un fichier en plusieurs fichiers à l’aide de groupes (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="27134-125">How to: Split a File Into Many Files by Using Groups (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/how-to-split-a-file-into-many-files-by-using-groups-linq.md)
