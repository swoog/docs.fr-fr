---
title: "Types de nœuds reconnus avec les requêtes XPath"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1d33e22d-18e5-43f8-a466-2e3d0a8dd094
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: db309bf0d04dfab4fd9fbdd2c8b145c1705d8428
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="node-types-recognized-with-xpath-queries"></a>Types de nœuds reconnus avec les requêtes XPath
Les types de nœuds reconnus dans une requête XPath ne sont pas les mêmes que ceux trouvés dans le DOM (Document Object Model).  
  
## <a name="w3c-xpath-node-types"></a>Types de nœuds XPath du W3C  
 Les types de nœuds reconnus dans une requête XPath ne sont pas les mêmes que ceux trouvés dans le DOM (Document Object Model). Les types de nœuds suivants sont les types de nœuds XPath représentés par l'énumération <xref:System.Xml.XPath.XPathNodeType>.  
  
-   <xref:System.Xml.XPath.XPathNodeType.All>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Attribute>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Comment>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Element>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Namespace>  
  
-   <xref:System.Xml.XPath.XPathNodeType.ProcessingInstruction>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Root>  
  
-   <xref:System.Xml.XPath.XPathNodeType.SignificantWhitespace>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Text>  
  
-   <xref:System.Xml.XPath.XPathNodeType.Whitespace>  
  
 Ces types de nœuds sont basés sur le modèle de données XPath, dans lequel les nœuds sont dérivés du jeu d’informations XML. Les types de nœuds <xref:System.Xml.XPath.XPathNodeType.SignificantWhitespace> et <xref:System.Xml.XPath.XPathNodeType.Whitespace> sont des extensions Microsoft .NET Framework des types de nœuds de base décrits dans le modèle de données XPath.  
  
 Le type de nœud d'attribut est utilisé de manière différente dans le modèle de données XPath que dans le DOM. Dans le modèle de données XPath, le nœud d'élément est associé à un ensemble de nœuds d'attribut et le nœud d'élément est le parent de chaque nœud d'attribut. Toutefois, dans le DOM, le nœud d'élément est le propriétaire et non le parent. Dans ces deux modèles, les nœuds d'attribut et d'espace de noms ne sont pas considérés comme des nœuds enfants du nœud d'élément.  
  
 Le type de nœud d’espace de noms a été ajouté au modèle de données XPath et n’est pas un type de nœud DOM reconnu.  
  
 Pour plus d’informations sur la navigation dans les nœuds d’élément, d’attribut et d’espace de noms, consultez les rubriques [Navigation entre les nœuds d’attribut et d’espace de noms à l’aide de XPathNavigator](../../../../docs/standard/data/xml/node-set-navigation-using-xpathnavigator.md) et [Navigation entre les nœuds d’attribut et d’espace de noms à l’aide de XPathNavigator](../../../../docs/standard/data/xml/attribute-and-namespace-node-navigation-using-xpathnavigator.md).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.XmlDocument>  
 <xref:System.Xml.XPath.XPathDocument>  
 <xref:System.Xml.XPath.XPathNavigator>  
 [Traitement des données XML à l’aide du modèle de données XPath](../../../../docs/standard/data/xml/process-xml-data-using-the-xpath-data-model.md)  
 [Sélection de données XML à l’aide de XPathNavigator](../../../../docs/standard/data/xml/select-xml-data-using-xpathnavigator.md)  
 [Évaluation d’expressions XPath à l’aide de XPathNavigator](../../../../docs/standard/data/xml/evaluate-xpath-expressions-using-xpathnavigator.md)  
 [Mise en correspondance de nœuds avec XPathNavigator](../../../../docs/standard/data/xml/matching-nodes-using-xpathnavigator.md)  
 [Requêtes et espaces de noms XPath](../../../../docs/standard/data/xml/xpath-queries-and-namespaces.md)  
 [Expressions XPath compilées](../../../../docs/standard/data/xml/compiled-xpath-expressions.md)
