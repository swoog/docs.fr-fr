---
title: 'Procédure : Écrire des requêtes à exécuter sur du code XML dans des espaces de noms (C#)'
ms.date: 07/20/2015
ms.assetid: 7c54df81-15e4-4091-8c81-a87637029130
ms.openlocfilehash: e6b966e90d1f7fc86efaa422ecd8afb030d97163
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722092"
---
# <a name="how-to-write-queries-on-xml-in-namespaces-c"></a><span data-ttu-id="8f6d9-102">Procédure : Écrire des requêtes à exécuter sur du code XML dans des espaces de noms (C#)</span><span class="sxs-lookup"><span data-stu-id="8f6d9-102">How to: Write Queries on XML in Namespaces (C#)</span></span>
<span data-ttu-id="8f6d9-103">Pour écrire des requêtes sur du code XML qui est dans un espace de noms, vous devez utiliser des objets <xref:System.Xml.Linq.XName> qui ont l'espace de noms correct.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-103">To write a query on XML that is in a namespace, you must use <xref:System.Xml.Linq.XName> objects that have the correct namespace.</span></span>  
  
 <span data-ttu-id="8f6d9-104">Pour C#, l'approche la plus courante consiste à initialiser un objet <xref:System.Xml.Linq.XNamespace> à l'aide d'une chaîne contenant l'URI, puis à utiliser la surcharge d'opérateur d'addition pour combiner l'espace de noms avec le nom local.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-104">For C#, the most common approach is to initialize an <xref:System.Xml.Linq.XNamespace> using a string that contains the URI, then use the addition operator overload to combine the namespace with the local name.</span></span>  
  
 <span data-ttu-id="8f6d9-105">Le premier ensemble d’exemples de cette rubrique montre comment créer une arborescence XML dans un espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-105">The first set of examples in this topic shows how to create an XML tree in a default namespace.</span></span> <span data-ttu-id="8f6d9-106">Le second ensemble illustre la création d’une arborescence XML dans un espace de noms avec un préfixe.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-106">The second set shows how to create an XML tree in a namespace with a prefix.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8f6d9-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f6d9-107">Example</span></span>  
 <span data-ttu-id="8f6d9-108">L’exemple suivant crée une arborescence XML qui est dans un espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-108">The following example creates an XML tree that is in a default namespace.</span></span> <span data-ttu-id="8f6d9-109">Il récupère ensuite une collection d'éléments.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-109">It then retrieves a collection of elements.</span></span>  
  
```csharp  
XNamespace aw = "http://www.adventure-works.com";  
XElement root = XElement.Parse(  
@"<Root xmlns='http://www.adventure-works.com'>  
    <Child>1</Child>  
    <Child>2</Child>  
    <Child>3</Child>  
    <AnotherChild>4</AnotherChild>  
    <AnotherChild>5</AnotherChild>  
    <AnotherChild>6</AnotherChild>  
</Root>");  
IEnumerable<XElement> c1 =  
    from el in root.Elements(aw + "Child")  
    select el;  
foreach (XElement el in c1)  
    Console.WriteLine((int)el);  
```  
  
 <span data-ttu-id="8f6d9-110">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="8f6d9-110">This example produces the following output:</span></span>  
  
```  
1  
2  
3  
```  
  
## <a name="example"></a><span data-ttu-id="8f6d9-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f6d9-111">Example</span></span>  
 <span data-ttu-id="8f6d9-112">En C#, vous écrivez des requêtes de la même manière, que ce soit sur une arborescence XML qui utilise un espace de noms avec un préfixe ou sur une arborescence XML avec un espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-112">In C#, you write queries in the same way regardless of whether you are writing queries on an XML tree that uses a namespace with a prefix or on an XML tree with a default namespace.</span></span>  
  
 <span data-ttu-id="8f6d9-113">L’exemple suivant crée une arborescence XML qui est dans un espace de noms avec un préfixe.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-113">The following example creates an XML tree that is in a namespace with a prefix.</span></span> <span data-ttu-id="8f6d9-114">Il récupère ensuite une collection d'éléments.</span><span class="sxs-lookup"><span data-stu-id="8f6d9-114">It then retrieves a collection of elements.</span></span>  
  
```csharp  
XNamespace aw = "http://www.adventure-works.com";  
XElement root = XElement.Parse(  
@"<aw:Root xmlns:aw='http://www.adventure-works.com'>  
    <aw:Child>1</aw:Child>  
    <aw:Child>2</aw:Child>  
    <aw:Child>3</aw:Child>  
    <aw:AnotherChild>4</aw:AnotherChild>  
    <aw:AnotherChild>5</aw:AnotherChild>  
    <aw:AnotherChild>6</aw:AnotherChild>  
</aw:Root>");  
IEnumerable<XElement> c1 =  
    from el in root.Elements(aw + "Child")  
    select el;  
foreach (XElement el in c1)  
    Console.WriteLine((int)el);  
```  
  
 <span data-ttu-id="8f6d9-115">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="8f6d9-115">This example produces the following output:</span></span>  
  
```  
1  
2  
3  
```  
  
## <a name="see-also"></a><span data-ttu-id="8f6d9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f6d9-116">See also</span></span>

- [<span data-ttu-id="8f6d9-117">Utilisation des espaces de noms XML (C#)</span><span class="sxs-lookup"><span data-stu-id="8f6d9-117">Working with XML Namespaces (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/working-with-xml-namespaces.md)
