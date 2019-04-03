---
title: 'Procédure : Trier les éléments (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: c2c09279-6c8a-482e-8e71-b1453a815052
ms.openlocfilehash: b6f2e0056582e60066b2c0715a663022b72a6c9c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58841214"
---
# <a name="how-to-sort-elements-visual-basic"></a><span data-ttu-id="b1b32-102">Procédure : Trier les éléments (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b1b32-102">How to: Sort Elements (Visual Basic)</span></span>
<span data-ttu-id="b1b32-103">Cet exemple montre comment écrire une requête qui trie ses résultats.</span><span class="sxs-lookup"><span data-stu-id="b1b32-103">This example shows how to write a query that sorts its results.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b1b32-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b1b32-104">Example</span></span>  
 <span data-ttu-id="b1b32-105">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Données numériques (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="b1b32-105">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```vb  
Dim root As XElement = XElement.Load("Data.xml")  
Dim prices As IEnumerable(Of Decimal) = _  
    From el In root.<Data> _  
    Let price = Convert.ToDecimal(el.<Price>.Value) _  
    Order By (price) _  
    Select price  
For Each el As Decimal In prices  
    Console.WriteLine(el)  
Next  
```  
  
 <span data-ttu-id="b1b32-106">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="b1b32-106">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="example"></a><span data-ttu-id="b1b32-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="b1b32-107">Example</span></span>  
 <span data-ttu-id="b1b32-108">L'exemple suivant illustre la même requête pour du code XML qui est dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b1b32-108">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="b1b32-109">Pour plus d’informations, consultez [utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="b1b32-109">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="b1b32-110">Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Données numériques dans un espace de noms](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="b1b32-110">This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span></span>  
  
```vb  
Imports <xmlns='http://www.adatum.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("DataInNamespace.xml")  
        Dim prices As IEnumerable(Of Decimal) = _  
            From el In root.<Data> _  
            Let price = Convert.ToDecimal(el.<Price>.Value) _  
            Order By (price) _  
            Select price  
        For Each el As Decimal In prices  
            Console.WriteLine(el)  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="b1b32-111">Ce code génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="b1b32-111">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="see-also"></a><span data-ttu-id="b1b32-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1b32-112">See also</span></span>

- [<span data-ttu-id="b1b32-113">Tri des données</span><span class="sxs-lookup"><span data-stu-id="b1b32-113">Sorting Data</span></span>](../../../../visual-basic/programming-guide/concepts/linq/sorting-data.md)
- [<span data-ttu-id="b1b32-114">Requêtes de base (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b1b32-114">Basic Queries (LINQ to XML) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
