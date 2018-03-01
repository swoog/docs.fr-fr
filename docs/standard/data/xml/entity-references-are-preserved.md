---
title: "Conservation des références d'entité"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 000a6cae-5972-40d6-bd6c-a9b7d9649b3c
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: f5a867d1301355f4c9a77654556229274f96d00c
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="entity-references-are-preserved"></a>Conservation des références d'entité
Si une référence d’entité n’est pas développée, mais préservée, le DOM (Document Object Model) XML crée un nœud **XmlEntityReference** quand il rencontre une référence d’entité.  
  
 À l'aide du code XML suivant,  
  
```xml  
<author>Fred</author>  
<pubinfo>Published by &publisher;</pubinfo>  
```  
  
 le DOM crée un nœud **XmlEntityReference** quand il rencontre la référence `&publisher;`. **XmlEntityReference** contient des nœuds enfants copiés à partir du contenu dans la déclaration d'entité. L'exemple de code précédent contient du texte dans la déclaration d'entité, c'est pourquoi un nœud **XmlText** est créé en tant que nœud enfant du nœud de référence d'entité.  
  
 ![Arborescence pour références d’entité préservées](../../../../docs/standard/data/xml/media/xmlentityref-notexpanded-nodes.gif "xmlentityref_notexpanded_nodes")  
Structure d’arborescence avec références d’entité préservées  
  
 Les nœuds enfants de **XmlEntityReference** sont des copies de tous les nœuds enfants créés à partir du nœud **XmlEntity** quand la déclaration d'entité a été rencontrée.  
  
> [!NOTE]
>  Les nœuds copiés à partir de **XmlEntity** ne constituent pas toujours des copies exactes une fois placés sous le nœud de référence d'entité. Il peut y avoir des espaces de noms qui sont dans la portée au niveau du nœud de référence d'entité et qui ont une incidence sur la configuration finale des nœuds enfants.  
  
 Par défaut, des entités générales telles que `&abc;` sont préservées et les nœuds **XmlEntityReference** sont toujours créés.  
  
## <a name="see-also"></a>Voir aussi  
 [DOM (Document Object Model) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
