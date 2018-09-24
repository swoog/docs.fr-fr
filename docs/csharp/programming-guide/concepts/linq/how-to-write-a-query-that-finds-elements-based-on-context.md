---
title: Guide pratique pour écrire une requête qui recherche des éléments en fonction du contexte (C#)
ms.date: 07/20/2015
ms.assetid: 3ff79ef0-fc8b-42fe-8cc0-10dc32b06b4e
ms.openlocfilehash: c1c43bc47df1612be26c78351a9d30272a020160
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45987953"
---
# <a name="how-to-write-a-query-that-finds-elements-based-on-context-c"></a><span data-ttu-id="82673-102">Guide pratique pour écrire une requête qui recherche des éléments en fonction du contexte (C#)</span><span class="sxs-lookup"><span data-stu-id="82673-102">How to: Write a Query that Finds Elements Based on Context (C#)</span></span>
<span data-ttu-id="82673-103">Parfois, vous devez écrire une requête qui sélectionne des éléments en fonction de leur contexte.</span><span class="sxs-lookup"><span data-stu-id="82673-103">Sometimes you might have to write a query that selects elements based on their context.</span></span> <span data-ttu-id="82673-104">Vous souhaiterez peut-être filtrer en fonction des éléments frères qui précèdent ou qui suivent.</span><span class="sxs-lookup"><span data-stu-id="82673-104">You might want to filter based on preceding or following sibling elements.</span></span> <span data-ttu-id="82673-105">Vous souhaiterez peut-être filtrer en fonction des éléments enfants ou ancêtres.</span><span class="sxs-lookup"><span data-stu-id="82673-105">You might want to filter based on child or ancestor elements.</span></span>  
  
 <span data-ttu-id="82673-106">Vous pouvez pour cela écrire une requête et utiliser ses résultats dans la clause `where`.</span><span class="sxs-lookup"><span data-stu-id="82673-106">You can do this by writing a query and using the results of the query in the `where` clause.</span></span> <span data-ttu-id="82673-107">Si vous devez tout d'abord tester par rapport à la valeur Null, puis tester la valeur, il est plus pratique de créer la requête dans une clause `let`, puis d'utiliser les résultats dans la clause `where`.</span><span class="sxs-lookup"><span data-stu-id="82673-107">If you have to first test against null, and then test the value, it is more convenient to do the query in a `let` clause, and then use the results in the `where` clause.</span></span>  
  
## <a name="example"></a><span data-ttu-id="82673-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="82673-108">Example</span></span>  
 <span data-ttu-id="82673-109">L'exemple suivant sélectionne tous les éléments `p` qui sont suivis immédiatement d'un élément `ul`.</span><span class="sxs-lookup"><span data-stu-id="82673-109">The following example selects all `p` elements that are immediately followed by a `ul` element.</span></span>  
  
```csharp  
XElement doc = XElement.Parse(@"<Root>  
    <p id=""1""/>  
    <ul>abc</ul>  
    <Child>  
        <p id=""2""/>  
        <notul/>  
        <p id=""3""/>  
        <ul>def</ul>  
        <p id=""4""/>  
    </Child>  
    <Child>  
        <p id=""5""/>  
        <notul/>  
        <p id=""6""/>  
        <ul>abc</ul>  
        <p id=""7""/>  
    </Child>  
</Root>");  
  
IEnumerable<XElement> items =  
    from e in doc.Descendants("p")  
    let z = e.ElementsAfterSelf().FirstOrDefault()  
    where z != null && z.Name.LocalName == "ul"  
    select e;  
  
foreach (XElement e in items)  
    Console.WriteLine("id = {0}", (string)e.Attribute("id"));  
```  
  
 <span data-ttu-id="82673-110">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="82673-110">This code produces the following output:</span></span>  
  
```  
id = 1  
id = 3  
id = 6  
```  
  
## <a name="example"></a><span data-ttu-id="82673-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="82673-111">Example</span></span>  
 <span data-ttu-id="82673-112">L'exemple suivant illustre la même requête pour du code XML qui est dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="82673-112">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="82673-113">Pour plus d’informations, consultez [Utilisation des espaces de noms XML (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="82673-113">For more information, see [Working with XML Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
```csharp  
XElement doc = XElement.Parse(@"<Root xmlns='http://www.adatum.com'>  
    <p id=""1""/>  
    <ul>abc</ul>  
    <Child>  
        <p id=""2""/>  
        <notul/>  
        <p id=""3""/>  
        <ul>def</ul>  
        <p id=""4""/>  
    </Child>  
    <Child>  
        <p id=""5""/>  
        <notul/>  
        <p id=""6""/>  
        <ul>abc</ul>  
        <p id=""7""/>  
    </Child>  
</Root>");  
  
XNamespace ad = "http://www.adatum.com";  
  
IEnumerable<XElement> items =  
    from e in doc.Descendants(ad + "p")  
    let z = e.ElementsAfterSelf().FirstOrDefault()  
    where z != null && z.Name == ad.GetName("ul")  
    select e;  
  
foreach (XElement e in items)  
    Console.WriteLine("id = {0}", (string)e.Attribute("id"));  
```  
  
 <span data-ttu-id="82673-114">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="82673-114">This code produces the following output:</span></span>  
  
```  
id = 1  
id = 3  
id = 6  
```  
  
## <a name="see-also"></a><span data-ttu-id="82673-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82673-115">See Also</span></span>

- <xref:System.Xml.Linq.XElement.Parse%2A>  
- <xref:System.Xml.Linq.XContainer.Descendants%2A>  
- <xref:System.Xml.Linq.XNode.ElementsAfterSelf%2A>  
- <xref:System.Linq.Enumerable.FirstOrDefault%2A>  
- [<span data-ttu-id="82673-116">Requêtes de base (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="82673-116">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
