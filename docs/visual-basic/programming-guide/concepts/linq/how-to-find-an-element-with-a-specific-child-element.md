---
title: 'Comment : rechercher un élément avec un élément enfant spécifique (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: b0d0a463-6a85-46c3-8453-ad25b0ecf93c
ms.openlocfilehash: 9ebc7fd826e2245cea661b2441fa9989b0aee8b8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-find-an-element-with-a-specific-child-element-visual-basic"></a>Comment : rechercher un élément avec un élément enfant spécifique (Visual Basic)
Cette rubrique montre comment rechercher un élément particulier qui a un élément enfant avec une valeur spécifique.  
  
## <a name="example"></a>Exemple  
 L'exemple recherche l'élément `Test` qui a un élément enfant `CommandLine` avec la valeur « Examp2.EXE ».  
  
 Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Configuration test (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-test-configuration-linq-to-xml.md).  
  
```vb  
Dim root As XElement = XElement.Load("TestConfig.xml")  
Dim tests As IEnumerable(Of XElement) = _  
    From el In root.<Test> _  
    Where el.<CommandLine>.Value = "Examp2.EXE" _  
    Select el  
For Each el as XElement In tests  
    Console.WriteLine(el.@TestId)  
Next  
```  
  
 Ce code génère la sortie suivante :  
  
```  
0002  
0006  
```  
  
 Notez que cet exemple utilise le [propriété d’axe enfant XML](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md), le [propriété d’axe d’attribut XML](../../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md)et le [propriété de valeur XML](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md).  
  
## <a name="example"></a>Exemple  
 L'exemple suivant illustre la même requête pour du code XML qui est dans un espace de noms. Pour plus d’informations, consultez [utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).  
  
 Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Configuration test dans un espace de noms](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-test-configuration-in-a-namespace.md).  
  
```vb  
Imports <xmlns='http://www.adatum.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("TestConfigInNamespace.xml")  
        Dim tests As IEnumerable(Of XElement) = _  
            From el In root.<Test> _  
            Where el.<CommandLine>.Value = "Examp2.EXE" _  
            Select el  
        For Each el As XElement In tests  
            Console.WriteLine(el.@TestId)  
        Next  
    End Sub  
End Module  
```  
  
 Ce code génère la sortie suivante :  
  
```  
0002  
0006  
```  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.Linq.XElement.Attribute%2A>  
 <xref:System.Xml.Linq.XContainer.Elements%2A>  
 [Requêtes de base (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)  
 [Vue d’ensemble des opérateurs de requête standard (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md)  
 [Opérations de projection (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/projection-operations.md)
