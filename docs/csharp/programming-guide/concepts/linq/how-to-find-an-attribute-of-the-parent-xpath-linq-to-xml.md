---
title: 'Procédure : Rechercher un attribut du parent (XPath-LINQ to XML) (C#)'
ms.date: 07/20/2015
ms.assetid: dbef9d89-a5c4-431f-80cc-7a2ebf323f86
ms.openlocfilehash: e139e278141a8f42cddf8103f1c5d8d3195751e4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621810"
---
# <a name="how-to-find-an-attribute-of-the-parent-xpath-linq-to-xml-c"></a>Procédure : Rechercher un attribut du parent (XPath-LINQ to XML) (C#)
Cette rubrique montre comment naviguer jusqu'à l'élément parent et rechercher un attribut de celui-ci.  
  
 L’expression XPath est la suivante :  
  
 `../@id`  
  
## <a name="example"></a>Exemple  
 Cet exemple recherche d'abord un élément `Author`. Il recherche ensuite l'attribut `id` de l'élément parent.  
  
 Cet exemple utilise le document XML suivant : [Exemple de fichier XML : Livres (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-books-linq-to-xml.md).  
  
```csharp  
XDocument books = XDocument.Load("Books.xml");  
  
XElement author =   
    books  
    .Root  
    .Element("Book")  
    .Element("Author");  
  
// LINQ to XML query  
XAttribute att1 =  
    author  
    .Parent  
    .Attribute("id");  
  
// XPath expression  
XAttribute att2 = ((IEnumerable)author.XPathEvaluate("../@id")).Cast<XAttribute>().First();  
  
if (att1 == att2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(att1);  
```  
  
 Cet exemple génère la sortie suivante :  
  
```  
Results are identical  
id="bk101"  
```  
  
## <a name="see-also"></a>Voir aussi

- [LINQ to XML pour les utilisateurs XPath (C#)](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
