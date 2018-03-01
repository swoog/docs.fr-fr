---
title: "Développement sans conservation des références d’entité"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ffd97806-ab43-4538-8de2-5828bfbbde57
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 00b997865c614756ea5fd9567ded3baa469f4c62
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="entity-references-are-expanded-and-not-preserved"></a>Développement sans conservation des références d’entité
Quand une référence d’entité est développée et remplacée par le texte qu’elle représente, le nœud **XmlEntityReference** n’est pas créé. En revanche, la déclaration d'entité est analysée et les nœuds créés à partir du contenu de la déclaration sont copiés à la place de **XmlEntityReference**. Par conséquent, dans l'exemple `&publisher;`, `&publisher;` n'est pas enregistré, mais un nœud **XmlText** est créé.  
  
 ![Arborescence développée](../../../../docs/standard/data/xml/media/xmlentityref-expanded-nodes.gif "xmlentityref_expanded_nodes")  
Structure d’arborescence avec références d’entité développées  
  
 Les entités de caractère, telles que `B` ou `<`, ne sont pas conservées. En revanche, elles sont toujours développées et représentées sous la forme de nœuds de texte.  
  
 Pour préserver les nœuds **XmlEntityReference**, ainsi que les nœuds enfants de la référence d’entité joints, affectez à l’indicateur **EntityHandling** la valeur **ExpandCharEntities**. Sinon, conservez la valeur par défaut de l’indicateur **EntityHandling**, à savoir **ExpandEntities**. Dans ce cas, le DOM ne comprendra pas de nœud de référence d'entité. Ces nœuds sont remplacés par ceux qui constituent des copies des nœuds enfants de la déclaration d'entité.  
  
 La non-conservation des références d'entité présente un effet pervers : lorsque le document est enregistré et passé à une autre application, cette application réceptrice ne sait pas que les nœuds ont été générés par une référence d'entité. Toutefois, lorsque les références d'entité sont préservées, une application réceptrice voit une référence d'entité et lit les nœuds enfants. Il est manifeste que les nœuds enfants représentent les informations qui figuraient dans la déclaration d'entité. Par exemple, en théorie, le DOM possède la structure suivante s'il existe une conservation des références d'entité.  
  
 XmlElement : éditeur  
  
 XmlEntityReference : `&publisher;`  
  
 XmlText : Microsoft Press  
  
 Si des références d'entité sont développées dans le DOM (ce qui constitue la méthode par défaut), la structure possède ce type d'arborescence :  
  
 XmlElement : éditeur  
  
 XmlText : Microsoft Press  
  
 Observez la disparition du nœud de référence d'entité. L'application réceptrice ne peut pas déterminer que le nœud **XmlText** contenant « Microsoft Press » a été créé à partir d'une déclaration d'entité.  
  
 Si vous avez recours à un lecteur incapable de résoudre les entités, la méthode **Load** lève une exception quand elle rencontre une référence d'entité.  
  
## <a name="see-also"></a>Voir aussi  
 [DOM (Document Object Model) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
