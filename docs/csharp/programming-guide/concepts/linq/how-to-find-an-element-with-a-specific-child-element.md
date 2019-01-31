---
title: 'Procédure : Rechercher un élément avec un élément enfant spécifique (C#)'
ms.date: 07/20/2015
ms.assetid: 00cf5555-374e-4369-bf93-7bd2e7f21db3
ms.openlocfilehash: 6888de3bc255691fbbb05f2a1debae05492661c7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547278"
---
# <a name="how-to-find-an-element-with-a-specific-child-element-c"></a><span data-ttu-id="2f165-102">Procédure : Rechercher un élément avec un élément enfant spécifique (C#)</span><span class="sxs-lookup"><span data-stu-id="2f165-102">How to: Find an Element with a Specific Child Element (C#)</span></span>
<span data-ttu-id="2f165-103">Cette rubrique montre comment rechercher un élément particulier qui a un élément enfant avec une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="2f165-103">This topic shows how to find a particular element that has a child element with a specific value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2f165-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f165-104">Example</span></span>  
 <span data-ttu-id="2f165-105">L'exemple recherche l'élément `Test` qui a un élément enfant `CommandLine` avec la valeur « Examp2.EXE ».</span><span class="sxs-lookup"><span data-stu-id="2f165-105">The example finds the `Test` element that has a `CommandLine` child element with the value of "Examp2.EXE".</span></span>  
  
 <span data-ttu-id="2f165-106">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Configuration de test (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-test-configuration-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="2f165-106">This example uses the following XML document: [Sample XML File: Test Configuration (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-test-configuration-linq-to-xml.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("TestConfig.xml");  
IEnumerable<XElement> tests =  
    from el in root.Elements("Test")  
    where (string)el.Element("CommandLine") == "Examp2.EXE"  
    select el;  
foreach (XElement el in tests)  
    Console.WriteLine((string)el.Attribute("TestId"));  
```  
  
 <span data-ttu-id="2f165-107">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="2f165-107">This code produces the following output:</span></span>  
  
```  
0002  
0006  
```  
  
## <a name="example"></a><span data-ttu-id="2f165-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f165-108">Example</span></span>  
 <span data-ttu-id="2f165-109">L'exemple suivant illustre la même requête pour du code XML qui est dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2f165-109">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="2f165-110">Pour plus d’informations, consultez [Utilisation des espaces de noms XML (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="2f165-110">For more information, see [Working with XML Namespaces (C#)](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="2f165-111">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Configuration de test dans un espace de noms](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-test-configuration-in-a-namespace1.md).</span><span class="sxs-lookup"><span data-stu-id="2f165-111">This example uses the following XML document: [Sample XML File: Test Configuration in a Namespace](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-test-configuration-in-a-namespace1.md).</span></span>  
  
```csharp  
XElement root = XElement.Load("TestConfigInNamespace.xml");  
XNamespace ad = "http://www.adatum.com";  
IEnumerable<XElement> tests =  
    from el in root.Elements(ad + "Test")  
    where (string)el.Element(ad + "CommandLine") == "Examp2.EXE"  
    select el;  
foreach (XElement el in tests)  
    Console.WriteLine((string)el.Attribute("TestId"));  
```  
  
 <span data-ttu-id="2f165-112">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="2f165-112">This code produces the following output:</span></span>  
  
```  
0002  
0006  
```  
  
## <a name="see-also"></a><span data-ttu-id="2f165-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f165-113">See also</span></span>

- <xref:System.Xml.Linq.XElement.Attribute%2A>
- <xref:System.Xml.Linq.XContainer.Elements%2A>
- [<span data-ttu-id="2f165-114">Requêtes de base (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="2f165-114">Basic Queries (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
- [<span data-ttu-id="2f165-115">Vue d’ensemble des opérateurs de requête standard (C#)</span><span class="sxs-lookup"><span data-stu-id="2f165-115">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)
- [<span data-ttu-id="2f165-116">Opérations de projection (C#)</span><span class="sxs-lookup"><span data-stu-id="2f165-116">Projection Operations (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/projection-operations.md)
