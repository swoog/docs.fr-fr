---
title: "Procédure : Retourner des sous-ensembles de propriétés d'éléments dans une requête - Guide de programmation C#"
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- anonymous types [C#], for subsets of element properties
ms.assetid: fabdf349-f443-4e3f-8368-6c471be1dd7b
ms.openlocfilehash: da4ecb11c51f42c2297b6d40ed9a963590b3f441
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64599987"
---
# <a name="how-to-return-subsets-of-element-properties-in-a-query-c-programming-guide"></a><span data-ttu-id="0cae9-102">Procédure : Retourner des sous-ensembles de propriétés d'éléments dans une requête (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="0cae9-102">How to: Return Subsets of Element Properties in a Query (C# Programming Guide)</span></span>
<span data-ttu-id="0cae9-103">Utilisez un type anonyme dans une expression de requête lorsque les deux conditions suivantes s’appliquent :</span><span class="sxs-lookup"><span data-stu-id="0cae9-103">Use an anonymous type in a query expression when both of these conditions apply:</span></span>  
  
- <span data-ttu-id="0cae9-104">Vous souhaitez retourner uniquement certaines propriétés de chaque élément source.</span><span class="sxs-lookup"><span data-stu-id="0cae9-104">You want to return only some of the properties of each source element.</span></span>  
  
- <span data-ttu-id="0cae9-105">Vous n’avez pas besoin de stocker les résultats de requête en dehors de la portée de la méthode dans laquelle la requête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="0cae9-105">You do not have to store the query results outside the scope of the method in which the query is executed.</span></span>  
  
 <span data-ttu-id="0cae9-106">Si vous souhaitez uniquement retourner une propriété ou un champ de chaque élément source, vous pouvez utiliser l’opérateur point dans la clause `select`.</span><span class="sxs-lookup"><span data-stu-id="0cae9-106">If you only want to return one property or field from each source element, then you can just use the dot operator in the `select` clause.</span></span> <span data-ttu-id="0cae9-107">Par exemple, pour retourner uniquement l’`ID` de chaque `student`, écrivez la clause `select` de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="0cae9-107">For example, to return only the `ID` of each `student`, write the `select` clause as follows:</span></span>  
  
```  
select student.ID;  
```  
  
## <a name="example"></a><span data-ttu-id="0cae9-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="0cae9-108">Example</span></span>  
 <span data-ttu-id="0cae9-109">L’exemple suivant montre comment utiliser un type anonyme pour retourner uniquement un sous-ensemble des propriétés de chaque élément source qui répond à la condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0cae9-109">The following example shows how to use an anonymous type to return only a subset of the properties of each source element that matches the specified condition.</span></span>  
  
 [!code-csharp[csProgGuideLINQ#31](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideLINQ/CS/csRef30LangFeatures_2.cs#31)]  
  
 <span data-ttu-id="0cae9-110">Notez que le type anonyme utilise les noms de l’élément source pour ses propriétés si aucun nom n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="0cae9-110">Note that the anonymous type uses the source element's names for its properties if no names are specified.</span></span> <span data-ttu-id="0cae9-111">Pour attribuer de nouveaux noms aux propriétés du type anonyme, écrivez l’instruction `select` de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="0cae9-111">To give new names to the properties in the anonymous type, write the `select` statement as follows:</span></span>  
  
```  
select new { First = student.FirstName, Last = student.LastName };  
```  
  
 <span data-ttu-id="0cae9-112">Si vous effectuez cette opération dans l’exemple précédent, l’instruction `Console.WriteLine` doit également changer :</span><span class="sxs-lookup"><span data-stu-id="0cae9-112">If you try this in the previous example, then the `Console.WriteLine` statement must also change:</span></span>  
  
```csharp  
Console.WriteLine(student.First + " " + student.Last);  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0cae9-113">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0cae9-113">Compiling the Code</span></span>  
  
- <span data-ttu-id="0cae9-114">Pour exécuter ce code, copiez et collez la classe dans un projet d’application console Visual C# qui a été créé dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0cae9-114">To run this code, copy and paste the class into a Visual C# console application project that has been created in Visual Studio.</span></span> <span data-ttu-id="0cae9-115">Par défaut, ce projet cible la version 3.5 du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], et il comporte une référence à System.Core.dll et une directive `using` pour System.Linq.</span><span class="sxs-lookup"><span data-stu-id="0cae9-115">By default, this project targets version 3.5 of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)], and it will have a reference to System.Core.dll and a `using` directive for System.Linq.</span></span> <span data-ttu-id="0cae9-116">Si un ou plusieurs de ces éléments sont manquants dans le projet, vous pouvez les ajouter manuellement.</span><span class="sxs-lookup"><span data-stu-id="0cae9-116">If one or more of these requirements are missing from the project, you can add them manually.</span></span>   
  
## <a name="see-also"></a><span data-ttu-id="0cae9-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cae9-117">See also</span></span>

- [<span data-ttu-id="0cae9-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0cae9-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="0cae9-119">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="0cae9-119">Anonymous Types</span></span>](../../../csharp/programming-guide/classes-and-structs/anonymous-types.md)
- [<span data-ttu-id="0cae9-120">Expressions de requête LINQ</span><span class="sxs-lookup"><span data-stu-id="0cae9-120">LINQ Query Expressions</span></span>](../../../csharp/programming-guide/linq-query-expressions/index.md)
