---
title: "Vérification des noms d'attribut et d'élément XML lors de la création de nœuds"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: b489f647-a175-4659-ada4-170058bb41d0
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 36b9761cefb1dba47c88d053773c89e4312dee9d
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="xml-element-and-attribute-name-verification-when-creating-new-nodes"></a>Vérification des noms d'attribut et d'élément XML lors de la création de nœuds
Le DOM (Document Object Model) XML contrôle la validité des noms lors de la création de nœuds d'élément ou d'attribut. Si ces noms contiennent des caractères non conformes, une exception est levée. Pour être certain que les noms sont valides et encodés correctement, vous devez recourir à la classe **XmlConvert** pour encoder le nom et le décoder à nouveau au niveau de l'application. **XmlWriter** possède des méthodes qui effectuent des opérations supplémentaires afin de garantir un format correct pour le code XML qui est généré.  
  
## <a name="see-also"></a>Voir aussi  
 [DOM (Document Object Model) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
