---
title: System.Xml, utilisation
ms.date: 10/22/2008
ms.technology: dotnet-standard
ms.assetid: 82302f0d-a621-4c6f-b57d-999bd61f21a6
author: KrzysztofCwalina
ms.openlocfilehash: fc94ac62d1f2413c5f51446a8f6d0a52d9151557
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497954"
---
# <a name="systemxml-usage"></a>System.Xml, utilisation
Cette section présente à l’utilisation de plusieurs types résidant dans <xref:System.Xml?displayProperty=nameWithType> espaces de noms peut être utilisé pour représenter les données XML.  
  
 **X DO NOT** utiliser <xref:System.Xml.XmlNode> ou <xref:System.Xml.XmlDocument> pour représenter les données XML. Favoriser l’utilisation d’instances de <xref:System.Xml.XPath.IXPathNavigable>, <xref:System.Xml.XmlReader>, <xref:System.Xml.XmlWriter>, ou un sous-type de <xref:System.Xml.Linq.XNode> à la place. `XmlNode` et `XmlDocument` ne sont pas conçus pour exposer des API publiques.  
  
 **✓ DO** utiliser `XmlReader`, `IXPathNavigable`, ou un sous-type de `XNode` en tant qu’entrée ou sortie de membres qui acceptent ou retournent XML.  
  
 Utilisez ces abstractions au lieu de `XmlDocument`, `XmlNode`, ou <xref:System.Xml.XPath.XPathDocument>, car cela dissocie les méthodes à partir des implémentations spécifiques d’un document XML en mémoire et leur permet de travailler avec les sources de données XML virtuels qui exposent `XNode` , `XmlReader`, ou <xref:System.Xml.XPath.XPathNavigator>.  
  
 **X DO NOT** sous-classe `XmlDocument` si vous souhaitez créer un type qui représente une vue XML d’une source de données ou du modèle objet sous-jacent.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Indications relatives à l’utilisation](../../../docs/standard/design-guidelines/usage-guidelines.md)
