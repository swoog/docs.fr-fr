---
title: 'Comment : projeter un nouveau Type (LINQ to XML) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 8cfb24f5-89b2-4cfb-b85d-e7963f8f1845
ms.openlocfilehash: da45c527ef9943cabf207a0b475a8a2114d5c6d9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33642030"
---
# <a name="how-to-project-a-new-type-linq-to-xml-visual-basic"></a>Comment : projeter un nouveau Type (LINQ to XML) (Visual Basic)
Les autres exemples de cette section ont illustré des requêtes qui retournent des résultats comme <xref:System.Collections.Generic.IEnumerable%601> de <xref:System.Xml.Linq.XElement>, <xref:System.Collections.Generic.IEnumerable%601> de `string` et <xref:System.Collections.Generic.IEnumerable%601> de `int`. Il s'agit de types de résultats courants, mais ils ne conviennent pas à chaque scénario. Dans de nombreux cas, vous souhaiterez que vos requêtes retournent un objet <xref:System.Collections.Generic.IEnumerable%601> d'un autre type.  
  
## <a name="example"></a>Exemple  
 Cet exemple montre comment instancier des objets dans la clause `Select`. Le code définit tout d'abord une nouvelle classe avec un constructeur, puis modifie l'instruction `Select` de sorte que l'expression soit une nouvelle instance de la nouvelle classe.  
  
 Cet exemple utilise le document XML suivant : [Exemple de fichier XML : commande fournisseur typique (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-typical-purchase-order-linq-to-xml.md).  
  
```vb  
Public Class NameQty  
    Public name As String  
    Public qty As Integer  
    Public Sub New(ByVal n As String, ByVal q As Integer)  
        name = n  
        qty = q  
    End Sub  
End Class  
  
Public Class Program  
    Shared Sub Main()  
        Dim po As XElement = XElement.Load("PurchaseOrder.xml")  
  
        Dim nqList As IEnumerable(Of NameQty) = _  
            From n In po...<Item> _  
            Select New NameQty( _  
                n.<ProductName>.Value, CInt(n.<Quantity>.Value))  
  
        For Each n As NameQty In nqList  
            Console.WriteLine(n.name & ":" & n.qty)  
        Next  
    End Sub  
End Class  
```  
  
 Cet exemple utilise le `M:System.Xml.Linq.XElement.Element` méthode qui a été introduite dans la rubrique [Comment : récupérer un seul élément enfant (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-retrieve-a-single-child-element-linq-to-xml.md). Il utilise également des casts pour récupérer les valeurs des éléments retournés par la méthode `M:System.Xml.Linq.XElement.Element`.  
  
 Cet exemple génère la sortie suivante :  
  
```  
Lawnmower:1  
Baby Monitor:2  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Projections et Transformations (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/projections-and-transformations-linq-to-xml.md)
