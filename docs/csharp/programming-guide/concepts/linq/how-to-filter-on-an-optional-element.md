---
title: Guide pratique pour filtrer sur un élément facultatif (C#)
ms.date: 07/20/2015
ms.assetid: f99e2f93-fca5-403f-8a0c-770761d4905a
ms.openlocfilehash: c781db261dbf673af7a11150971956b4c07da774
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46569080"
---
# <a name="how-to-filter-on-an-optional-element-c"></a><span data-ttu-id="c629b-102">Guide pratique pour filtrer sur un élément facultatif (C#)</span><span class="sxs-lookup"><span data-stu-id="c629b-102">How to: Filter on an Optional Element (C#)</span></span>
<span data-ttu-id="c629b-103">Parfois, vous souhaitez appliquer un filtrage sur un élément sans être certain qu'il existe dans votre document XML.</span><span class="sxs-lookup"><span data-stu-id="c629b-103">Sometimes you want to filter for an element even though you are not sure it exists in your XML document.</span></span> <span data-ttu-id="c629b-104">La recherche doit être exécutée de telle sorte que, si l'élément particulier ne possède pas l'élément enfant, aucune exception de référence Null ne soit déclenchée suite au filtrage.</span><span class="sxs-lookup"><span data-stu-id="c629b-104">The search should be executed so that if the particular element does not have the child element, you do not trigger a null reference exception by filtering for it.</span></span> <span data-ttu-id="c629b-105">Dans l'exemple suivant, l'élément `Child5` ne possède pas d'élément enfant `Type`, mais la requête s'exécute tout de même correctement.</span><span class="sxs-lookup"><span data-stu-id="c629b-105">In the following example, the `Child5` element does not have a `Type` child element, but the query still executes correctly.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c629b-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="c629b-106">Example</span></span>  
 <span data-ttu-id="c629b-107">Cet exemple utilise la méthode d'extension <xref:System.Xml.Linq.Extensions.Elements%2A>.</span><span class="sxs-lookup"><span data-stu-id="c629b-107">This example uses the <xref:System.Xml.Linq.Extensions.Elements%2A> extension method.</span></span>  
  
```csharp  
XElement root = XElement.Parse(@"<Root>  
  <Child1>  
    <Text>Child One Text</Text>  
    <Type Value=""Yes""/>  
  </Child1>  
  <Child2>  
    <Text>Child Two Text</Text>  
    <Type Value=""Yes""/>  
  </Child2>  
  <Child3>  
    <Text>Child Three Text</Text>  
    <Type Value=""No""/>  
  </Child3>  
  <Child4>  
    <Text>Child Four Text</Text>  
    <Type Value=""Yes""/>  
  </Child4>  
  <Child5>  
    <Text>Child Five Text</Text>  
  </Child5>  
</Root>");  
var cList =  
    from typeElement in root.Elements().Elements("Type")  
    where (string)typeElement.Attribute("Value") == "Yes"  
    select (string)typeElement.Parent.Element("Text");  
foreach(string str in cList)  
    Console.WriteLine(str);  
```  
  
 <span data-ttu-id="c629b-108">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="c629b-108">This code produces the following output:</span></span>  
  
```  
Child One Text  
Child Two Text  
Child Four Text  
```  
  
## <a name="example"></a><span data-ttu-id="c629b-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="c629b-109">Example</span></span>  
 <span data-ttu-id="c629b-110">L'exemple suivant illustre la même requête pour du code XML qui est dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c629b-110">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="c629b-111">Pour plus d’informations, consultez [Utilisation des espaces de noms XML (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="c629b-111">For more information, see [Working with XML Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
```csharp  
XElement root = XElement.Parse(@"<Root xmlns='http://www.adatum.com'>  
  <Child1>  
    <Text>Child One Text</Text>  
    <Type Value=""Yes""/>  
  </Child1>  
  <Child2>  
    <Text>Child Two Text</Text>  
    <Type Value=""Yes""/>  
  </Child2>  
  <Child3>  
    <Text>Child Three Text</Text>  
    <Type Value=""No""/>  
  </Child3>  
  <Child4>  
    <Text>Child Four Text</Text>  
    <Type Value=""Yes""/>  
  </Child4>  
  <Child5>  
    <Text>Child Five Text</Text>  
  </Child5>  
</Root>");  
XNamespace ad = "http://www.adatum.com";  
var cList =  
    from typeElement in root.Elements().Elements(ad + "Type")  
    where (string)typeElement.Attribute("Value") == "Yes"  
    select (string)typeElement.Parent.Element(ad + "Text");  
foreach (string str in cList)  
    Console.WriteLine(str);  
```  
  
 <span data-ttu-id="c629b-112">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="c629b-112">This code produces the following output:</span></span>  
  
```  
Child One Text  
Child Two Text  
Child Four Text  
```  
  
## <a name="see-also"></a><span data-ttu-id="c629b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c629b-113">See Also</span></span>

- <xref:System.Xml.Linq.XElement.Attribute%2A?displayProperty=nameWithType>  
- <xref:System.Xml.Linq.XContainer.Elements%2A?displayProperty=nameWithType>  
- <xref:System.Xml.Linq.Extensions.Elements%2A?displayProperty=nameWithType>  
- [<span data-ttu-id="c629b-114">Requêtes de base (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="c629b-114">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)  
- [<span data-ttu-id="c629b-115">Présentation des opérateurs de requête standard (C#)</span><span class="sxs-lookup"><span data-stu-id="c629b-115">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)  
- [<span data-ttu-id="c629b-116">Opérations de projection (C#)</span><span class="sxs-lookup"><span data-stu-id="c629b-116">Projection Operations (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/projection-operations.md)
