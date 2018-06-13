---
title: 'Comment : rechercher un attribut du Parent (XPath-LINQ to XML) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 9d2572fd-27d4-426c-b079-16854cb9ec7d
ms.openlocfilehash: af2b6fc3aaebe4ba45be405c587c549ea73b3289
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33639361"
---
# <a name="how-to-find-an-attribute-of-the-parent-xpath-linq-to-xml-visual-basic"></a><span data-ttu-id="a369c-102">Comment : rechercher un attribut du Parent (XPath-LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a369c-102">How to: Find an Attribute of the Parent (XPath-LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="a369c-103">Cette rubrique montre comment naviguer jusqu'à l'élément parent et rechercher un attribut de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="a369c-103">This topic shows how to navigate to the parent element and find an attribute of it.</span></span>  
  
 <span data-ttu-id="a369c-104">L’expression XPath est la suivante :</span><span class="sxs-lookup"><span data-stu-id="a369c-104">The XPath expression is:</span></span>  
  
 `../@id`  
  
## <a name="example"></a><span data-ttu-id="a369c-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a369c-105">Example</span></span>  
 <span data-ttu-id="a369c-106">Cet exemple recherche d'abord un élément `Author`.</span><span class="sxs-lookup"><span data-stu-id="a369c-106">This example first finds an `Author` element.</span></span> <span data-ttu-id="a369c-107">Il recherche ensuite l'attribut `id` de l'élément parent.</span><span class="sxs-lookup"><span data-stu-id="a369c-107">It then finds the `id` attribute of the parent element.</span></span>  
  
 <span data-ttu-id="a369c-108">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Livres (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="a369c-108">This example uses the following XML document: [Sample XML File: Books (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md).</span></span>  
  
```vb  
Dim books As XDocument = XDocument.Load("Books.xml")  
Dim author As XElement = books.Root.<Book>.<Author>.FirstOrDefault()  
  
' LINQ to XML query  
Dim att1 As XAttribute = author.Parent.Attribute("id")  
  
' XPath expression  
Dim att2 As XAttribute = DirectCast(author.XPathEvaluate("../@id"),  _  
    IEnumerable).Cast(Of XAttribute)().First()  
  
If att1 Is att2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(att1)  
```  
  
 <span data-ttu-id="a369c-109">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="a369c-109">This example produces the following output:</span></span>  
  
```  
Results are identical  
id="bk101"  
```  
  
## <a name="see-also"></a><span data-ttu-id="a369c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a369c-110">See Also</span></span>  
 [<span data-ttu-id="a369c-111">LINQ to XML pour les utilisateurs de XPath (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a369c-111">LINQ to XML for XPath Users (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
