---
title: Guide pratique pour rechercher le frère précédent (XPath-LINQ to XML) (C#)
ms.date: 07/20/2015
ms.assetid: 74c06201-0b1b-4b5e-b3ac-0092980614e6
ms.openlocfilehash: 82c0ee6e7340ada18fb2077c0b8b04fb6a41671a
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935191"
---
# <a name="how-to-find-the-immediate-preceding-sibling-xpath-linq-to-xml-c"></a><span data-ttu-id="e0838-102">Guide pratique pour rechercher le frère précédent (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="e0838-102">How to: Find the Immediate Preceding Sibling (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="e0838-103">Il peut arriver que vous souhaitiez rechercher le frère précédent d'un nœud.</span><span class="sxs-lookup"><span data-stu-id="e0838-103">Sometimes you want to find the immediate preceding sibling to a node.</span></span> <span data-ttu-id="e0838-104">Étant donné la différence de sémantique des prédicats de position pour les axes enfants précédents dans XPath par opposition à [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], il s'agit de l'une des comparaisons les plus intéressantes.</span><span class="sxs-lookup"><span data-stu-id="e0838-104">Due to the difference in the semantics of positional predicates for the preceding sibling axes in XPath as opposed to [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], this is one of the more interesting comparisons.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e0838-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="e0838-105">Example</span></span>  
 <span data-ttu-id="e0838-106">Dans cet exemple, la requête [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] utilise l'opérateur <xref:System.Linq.Enumerable.Last%2A> pour rechercher le dernier nœud dans la collection retournée par <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A>.</span><span class="sxs-lookup"><span data-stu-id="e0838-106">In this example, the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] query uses the <xref:System.Linq.Enumerable.Last%2A> operator to find the last node in the collection returned by <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A>.</span></span> <span data-ttu-id="e0838-107">Par contraste, l'expression XPath utilise un prédicat avec une valeur de 1 pour rechercher l'élément précédent.</span><span class="sxs-lookup"><span data-stu-id="e0838-107">By contrast, the XPath expression uses a predicate with a value of 1 to find the immediately preceding element.</span></span>  
  
```csharp  
XElement root = XElement.Parse(  
    @"<Root>  
    <Child1/>  
    <Child2/>  
    <Child3/>  
    <Child4/>  
</Root>");  
XElement child4 = root.Element("Child4");  
  
// LINQ to XML query  
XElement el1 =  
    child4  
    .ElementsBeforeSelf()  
    .Last();  
  
// XPath expression  
XElement el2 =  
    ((IEnumerable)child4  
                 .XPathEvaluate("preceding-sibling::*[1]"))  
                 .Cast<XElement>()  
                 .First();  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1);  
```  
  
 <span data-ttu-id="e0838-108">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="e0838-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
<Child3 />  
```  
  
## <a name="see-also"></a><span data-ttu-id="e0838-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0838-109">See Also</span></span>  
 [<span data-ttu-id="e0838-110">LINQ to XML pour les utilisateurs XPath (C#)</span><span class="sxs-lookup"><span data-stu-id="e0838-110">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
