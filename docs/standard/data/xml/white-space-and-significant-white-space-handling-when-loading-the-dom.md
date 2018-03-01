---
title: Gestion des espaces blancs significatifs ou non lors du chargement du DOM
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 1b141a0a-50d8-4ebd-83cd-a84449bb22b2
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8a16f90b6d48bc2ffabfd678722fa9b6e61328cd
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="white-space-and-significant-white-space-handling-when-loading-the-dom"></a>Gestion des espaces blancs significatifs ou non lors du chargement du DOM
Durant le chargement du document, vous pouvez définir une option qui préserve les espaces blancs et crée des nœuds **XmlWhitespace** dans l'arborescence du document. Pour créer des nœuds d'espaces blancs, attribuez la valeur true à la propriété **PreserveWhitespace**. Si cette propriété a pour valeur **false** (la valeur par défaut), les nœuds d'espaces blancs ne sont pas créés. Les nœuds d'espaces blancs significatifs sont toujours préservés et des nœuds **XmlSignificantWhitespace** sont toujours créés en mémoire pour représenter ces données, quelle que soit la valeur de l'indicateur **PreserveWhitespace**.  
  
 Si le document est chargé à partir d'un lecteur, la définition de la propriété d'indicateur **PreserveWhitespace** sur la classe **XmlDocument** affecte la création de nœuds **XmlWhitespace** uniquement quand la propriété **WhitespaceHandling** sur le **XmlTextReader** n'a pas la valeur **WhitespaceHandling.None**. C'est la valeur de la propriété **WhitespaceHandling** sur le lecteur qui prend le pas sur le paramétrage de cet indicateur sur le **XmlDocument**. Pour plus d'informations sur **XmlSignificantWhitespace**, consultez <xref:System.Xml.XmlSignificantWhitespace>.  
  
## <a name="see-also"></a>Voir aussi  
 [DOM (Document Object Model) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
