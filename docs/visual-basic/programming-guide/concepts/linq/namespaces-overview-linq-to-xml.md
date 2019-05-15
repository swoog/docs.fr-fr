---
title: Vue d'ensemble des espaces de noms (LINQ to XML)
ms.date: 07/20/2015
ms.assetid: b8eb31fa-4b26-4acf-8050-6e705687f458
ms.openlocfilehash: 3133a96c356138ddb70df01c11ee0dac8cf11b16
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592877"
---
# <a name="namespaces-overview-linq-to-xml"></a>Vue d'ensemble des espaces de noms (LINQ to XML)
Cette rubrique présente les espaces de noms, la classe <xref:System.Xml.Linq.XName> et la classe <xref:System.Xml.Linq.XNamespace>.  
  
## <a name="xml-names"></a>Noms XML  
 Les noms XML constituent souvent une source de complexité dans la programmation XML. Un nom XML est constitué d'un espace de noms XML (également appelé URI d'espace de noms XML) et d'un nom local. Un espace de noms XML est similaire à un espace de noms dans un programme basé sur le .NET Framework. Il permet de qualifier de manière unique les noms d'éléments et d'attributs. Cela permet d'éviter les conflits de noms entre différentes parties d'un document XML. Lorsque vous avez déclaré un espace de noms XML, vous pouvez sélectionner un nom local qui n'exige d'être unique que dans cet espace de noms.  
  
 Les *préfixes d’espace de noms* XML constituent un autre aspect des noms XML. Les préfixes XML sont la cause de la plupart de la complexité des noms XML. Ces préfixes vous permettent de créer un raccourci pour un espace de noms XML, ce qui rend le document XML plus concis et plus compréhensible. Toutefois, la signification des préfixes XML dépend de leur contexte, ce qui augmente la complexité. Par exemple, le préfixe XML `aw` pourrait être associé à un espace de noms XML dans une partie d'une arborescence XML et à un espace de noms XML différent dans une autre partie de l'arborescence XML.  
  
 Lorsque vous utilisez [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] avec des littéraux XML et Visual Basic, vous devez utiliser des préfixes d’espace de noms lorsque vous travaillez avec des documents dans les espaces de noms.  
  
 Dans [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], la classe qui représente les noms XML est <xref:System.Xml.Linq.XName>. Les noms XML apparaissent fréquemment dans l’API [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], et chaque fois qu’un nom XML est requis, vous trouverez un paramètre <xref:System.Xml.Linq.XName>. Cependant, il est rare de travailler directement dans un objet <xref:System.Xml.Linq.XName>. <xref:System.Xml.Linq.XName> contient une conversion implicite de chaîne.  
  
 Pour plus d’informations, consultez <xref:System.Xml.Linq.XNamespace> et <xref:System.Xml.Linq.XName>.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation des espaces de noms XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)
