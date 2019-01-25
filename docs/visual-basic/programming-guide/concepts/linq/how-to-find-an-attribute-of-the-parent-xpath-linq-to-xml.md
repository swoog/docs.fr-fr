---
title: 'Procédure : Rechercher un attribut du Parent (XPath-LINQ to XML) (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: 9d2572fd-27d4-426c-b079-16854cb9ec7d
ms.openlocfilehash: 15752805f35b145514d25208b6de44a7ed8ade47
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580536"
---
# <a name="how-to-find-an-attribute-of-the-parent-xpath-linq-to-xml-visual-basic"></a>Procédure : Rechercher un attribut du Parent (XPath-LINQ to XML) (Visual Basic)
Cette rubrique montre comment naviguer jusqu'à l'élément parent et rechercher un attribut de celui-ci.  
  
 L’expression XPath est la suivante :  
  
 `../@id`  
  
## <a name="example"></a>Exemple  
 Cet exemple recherche d'abord un élément `Author`. Il recherche ensuite l'attribut `id` de l'élément parent.  
  
 Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Livres (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md).  
  
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
  
 Cet exemple génère la sortie suivante :  
  
```  
Results are identical  
id="bk101"  
```  
  
## <a name="see-also"></a>Voir aussi
- [LINQ to XML pour les utilisateurs de XPath (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
