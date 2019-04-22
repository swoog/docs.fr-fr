---
title: Filtrage des données (C#)
ms.date: 07/20/2015
ms.assetid: fbaece0d-0f23-47f7-89c5-f3ea8db692b6
ms.openlocfilehash: 61d80674fd858063e77749342a33d714e3a57c6e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58826065"
---
# <a name="filtering-data-c"></a><span data-ttu-id="64e38-102">Filtrage des données (C#)</span><span class="sxs-lookup"><span data-stu-id="64e38-102">Filtering Data (C#)</span></span>
<span data-ttu-id="64e38-103">Le filtrage fait référence à l’opération de restriction du jeu de résultats pour que celui-ci contienne uniquement les éléments qui répondent à une condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="64e38-103">Filtering refers to the operation of restricting the result set to contain only those elements that satisfy a specified condition.</span></span> <span data-ttu-id="64e38-104">Cette opération est également appelée « sélection ».</span><span class="sxs-lookup"><span data-stu-id="64e38-104">It is also known as selection.</span></span>  
  
 <span data-ttu-id="64e38-105">L’illustration suivante montre les résultats du filtrage d’une séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="64e38-105">The following illustration shows the results of filtering a sequence of characters.</span></span> <span data-ttu-id="64e38-106">Le prédicat de l’opération de filtrage spécifie que le caractère doit être « A ».</span><span class="sxs-lookup"><span data-stu-id="64e38-106">The predicate for the filtering operation specifies that the character must be 'A'.</span></span>  
  
 ![Diagramme illustrant une opération de filtrage LINQ](./media/filtering-data/linq-filter-operation.png)  
  
 <span data-ttu-id="64e38-108">Les méthodes d’opérateurs de requête standard qui effectuent des opérations de sélection sont répertoriées dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="64e38-108">The standard query operator methods that perform selection are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="64e38-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="64e38-109">Methods</span></span>  
  
|<span data-ttu-id="64e38-110">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="64e38-110">Method Name</span></span>|<span data-ttu-id="64e38-111">Description</span><span class="sxs-lookup"><span data-stu-id="64e38-111">Description</span></span>|<span data-ttu-id="64e38-112">Syntaxe d'expression de requête C#</span><span class="sxs-lookup"><span data-stu-id="64e38-112">C# Query Expression Syntax</span></span>|<span data-ttu-id="64e38-113">Informations complémentaires</span><span class="sxs-lookup"><span data-stu-id="64e38-113">More Information</span></span>|  
|-----------------|-----------------|---------------------------------|----------------------|  
|<span data-ttu-id="64e38-114">OfType</span><span class="sxs-lookup"><span data-stu-id="64e38-114">OfType</span></span>|<span data-ttu-id="64e38-115">Sélectionne des valeurs, en fonction de leur capacité à être castées en un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="64e38-115">Selects values, depending on their ability to be cast to a specified type.</span></span>|<span data-ttu-id="64e38-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="64e38-116">Not applicable.</span></span>|<xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.OfType%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="64e38-117">Où</span><span class="sxs-lookup"><span data-stu-id="64e38-117">Where</span></span>|<span data-ttu-id="64e38-118">Sélectionne les valeurs qui sont basées sur une fonction de prédicat.</span><span class="sxs-lookup"><span data-stu-id="64e38-118">Selects values that are based on a predicate function.</span></span>|`where`|<xref:System.Linq.Enumerable.Where%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Where%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a><span data-ttu-id="64e38-119">Exemple de syntaxe d’expression de requête</span><span class="sxs-lookup"><span data-stu-id="64e38-119">Query Expression Syntax Example</span></span>  
 <span data-ttu-id="64e38-120">L’exemple suivant utilise la clause `where` pour filtrer les chaînes d’un tableau qui ont une longueur spécifique.</span><span class="sxs-lookup"><span data-stu-id="64e38-120">The following example uses the `where` clause to filter from an array those strings that have a specific length.</span></span>  
  
```csharp  
string[] words = { "the", "quick", "brown", "fox", "jumps" };  
  
IEnumerable<string> query = from word in words  
                            where word.Length == 3  
                            select word;  
  
foreach (string str in query)  
    Console.WriteLine(str);  
  
/* This code produces the following output:  
  
    the  
    fox  
*/  
```  
  
## <a name="see-also"></a><span data-ttu-id="64e38-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64e38-121">See also</span></span>

- <xref:System.Linq>
- [<span data-ttu-id="64e38-122">Vue d’ensemble des opérateurs de requête standard (C#)</span><span class="sxs-lookup"><span data-stu-id="64e38-122">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="64e38-123">where, clause</span><span class="sxs-lookup"><span data-stu-id="64e38-123">where clause</span></span>](../../../../csharp/language-reference/keywords/where-clause.md)
- [<span data-ttu-id="64e38-124">Guide pratique pour spécifier dynamiquement des filtres de prédicat au moment de l’exécution</span><span class="sxs-lookup"><span data-stu-id="64e38-124">How to: Dynamically Specify Predicate Filters at Runtime</span></span>](../../../../csharp/programming-guide/linq-query-expressions/how-to-dynamically-specify-predicate-filters-at-runtime.md)
- [<span data-ttu-id="64e38-125">Guide pratique pour interroger les métadonnées d’un assembly avec la réflexion (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="64e38-125">How to: Query An Assembly's Metadata with Reflection (LINQ) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-query-an-assembly-s-metadata-with-reflection-linq.md)
- [<span data-ttu-id="64e38-126">Guide pratique pour rechercher des fichiers ayant un attribut ou un nom donné (C#)</span><span class="sxs-lookup"><span data-stu-id="64e38-126">How to: Query for Files with a Specified Attribute or Name (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-query-for-files-with-a-specified-attribute-or-name.md)
- [<span data-ttu-id="64e38-127">Guide pratique pour trier ou filtrer des données texte par mot ou par champ (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="64e38-127">How to: Sort or Filter Text Data by Any Word or Field (LINQ) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-sort-or-filter-text-data-by-any-word-or-field-linq.md)
