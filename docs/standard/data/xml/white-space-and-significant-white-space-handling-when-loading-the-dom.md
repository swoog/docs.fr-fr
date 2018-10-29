---
title: Gestion des espaces blancs significatifs ou non lors du chargement du DOM
ms.date: 03/30/2017
ms.technology: dotnet-standard
ms.assetid: 1b141a0a-50d8-4ebd-83cd-a84449bb22b2
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1d9bbb14320b84a6d417c5c28026b169092de219
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49120984"
---
# <a name="white-space-and-significant-white-space-handling-when-loading-the-dom"></a>Gestion des espaces blancs significatifs ou non lors du chargement du DOM
Durant le chargement du document, vous pouvez définir une option qui préserve les espaces blancs et crée des nœuds **XmlWhitespace** dans l'arborescence du document. Pour créer des nœuds d'espaces blancs, attribuez la valeur true à la propriété **PreserveWhitespace**. Si cette propriété a pour valeur **false** (la valeur par défaut), les nœuds d'espaces blancs ne sont pas créés. Les nœuds d'espaces blancs significatifs sont toujours préservés et des nœuds **XmlSignificantWhitespace** sont toujours créés en mémoire pour représenter ces données, quelle que soit la valeur de l'indicateur **PreserveWhitespace**.  
  
 Si le document est chargé à partir d'un lecteur, la définition de la propriété d'indicateur **PreserveWhitespace** sur la classe **XmlDocument** affecte la création de nœuds **XmlWhitespace** uniquement quand la propriété **WhitespaceHandling** sur le **XmlTextReader** n'a pas la valeur **WhitespaceHandling.None**. C'est la valeur de la propriété **WhitespaceHandling** sur le lecteur qui prend le pas sur le paramétrage de cet indicateur sur le **XmlDocument**. Pour plus d'informations sur **XmlSignificantWhitespace**, consultez <xref:System.Xml.XmlSignificantWhitespace>.  
  
## <a name="see-also"></a>Voir aussi

- [DOM (Document Object Model) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
