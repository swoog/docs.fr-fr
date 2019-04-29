---
title: 'Procédure : Rechercher des éléments descendants (XPath-LINQ to XML) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: e7e2dc9e-bda9-420d-a5b1-4fabf1cca46b
ms.openlocfilehash: 09f12dca7b6278327394126ffb0950682d285f88
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61780560"
---
# <a name="how-to-find-descendant-elements-xpath-linq-to-xml-visual-basic"></a><span data-ttu-id="4b632-102">Procédure : Rechercher des éléments descendants (XPath-LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4b632-102">How to: Find Descendant Elements (XPath-LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="4b632-103">Cette rubrique montre comment obtenir les éléments descendants avec un nom particulier.</span><span class="sxs-lookup"><span data-stu-id="4b632-103">This topic shows how to get the descendant elements with a particular name.</span></span>  
  
 <span data-ttu-id="4b632-104">L'expression XPath est `//Name`.</span><span class="sxs-lookup"><span data-stu-id="4b632-104">The XPath expression is `//Name`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b632-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b632-105">Example</span></span>  
 <span data-ttu-id="4b632-106">Cet exemple recherche tous les descendants nommés `Name`.</span><span class="sxs-lookup"><span data-stu-id="4b632-106">This example finds all descendants named `Name`.</span></span>  
  
 <span data-ttu-id="4b632-107">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Plusieurs commandes fournisseur (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="4b632-107">This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span></span>  
  
```vb  
      Dim po As XDocument = XDocument.Load("PurchaseOrders.xml")  
  
' LINQ to XML query  
Dim list1 As IEnumerable(Of XElement) = po...<Name>  
  
' XPath expression  
Dim list2 As IEnumerable(Of XElement) = po.XPathSelectElements("//Name")  
  
If (list1.Count() = list2.Count() And _  
        list1.Intersect(list2).Count() = list1.Count()) Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
For Each el As XElement In list1  
    Console.WriteLine(el)  
Next  
```  
  
 <span data-ttu-id="4b632-108">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="4b632-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
<Name>Ellen Adams</Name>  
<Name>Tai Yee</Name>  
<Name>Cristian Osorio</Name>  
<Name>Cristian Osorio</Name>  
<Name>Jessica Arnold</Name>  
<Name>Jessica Arnold</Name>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4b632-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b632-109">See also</span></span>

- [<span data-ttu-id="4b632-110">LINQ to XML pour les utilisateurs de XPath (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4b632-110">LINQ to XML for XPath Users (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
