---
title: Guide pratique pour rechercher l’élément racine (XPath-LINQ to XML) (C#)
ms.date: 07/20/2015
ms.assetid: 4fd824e0-4d39-429b-b092-f6a5c046ee6c
ms.openlocfilehash: a7c15c8eb688f70b2d1633fc5c094b02cc97031c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43421020"
---
# <a name="how-to-find-the-root-element-xpath-linq-to-xml-c"></a><span data-ttu-id="1c797-102">Guide pratique pour rechercher l’élément racine (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="1c797-102">How to: Find the Root Element (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="1c797-103">Cette rubrique montre comment obtenir l'élément racine avec XPath et [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="1c797-103">This topic shows how to get the root element with XPath and [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span></span>  
  
 <span data-ttu-id="1c797-104">L’expression XPath est la suivante :</span><span class="sxs-lookup"><span data-stu-id="1c797-104">The XPath expression is:</span></span>  
  
 `/PurchaseOrders`  
  
## <a name="example"></a><span data-ttu-id="1c797-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="1c797-105">Example</span></span>  
 <span data-ttu-id="1c797-106">Cet exemple recherche l'élément racine.</span><span class="sxs-lookup"><span data-stu-id="1c797-106">This example finds the root element.</span></span>  
  
 <span data-ttu-id="1c797-107">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Plusieurs commandes fournisseur (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="1c797-107">This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span></span>  
  
```csharp  
XDocument po = XDocument.Load("PurchaseOrders.xml");  
  
// LINQ to XML query  
XElement el1 = po.Root;  
  
// XPath expression  
XElement el2 = po.XPathSelectElement("/PurchaseOrders");  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1.Name);  
```  
  
 <span data-ttu-id="1c797-108">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="1c797-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
PurchaseOrders  
```  
  
## <a name="see-also"></a><span data-ttu-id="1c797-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c797-109">See Also</span></span>  
 [<span data-ttu-id="1c797-110">LINQ to XML pour les utilisateurs XPath (C#)</span><span class="sxs-lookup"><span data-stu-id="1c797-110">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
