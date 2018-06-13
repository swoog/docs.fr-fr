---
title: Modification des éléments, attributs et nœuds dans un Tree1 XML
ms.date: 07/20/2015
ms.assetid: 865cf54e-f8ac-4871-863b-a3e6fc61a4b9
ms.openlocfilehash: 91a7cca2e39e5ddc62d6010fbe4efad9bd7ff3c2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33645211"
---
# <a name="modifying-elements-attributes-and-nodes-in-an-xml-tree"></a>Modification d’éléments, d’attributs et de nœuds dans une arborescence XML
Le tableau suivant résume les méthodes et propriétés que vous pouvez utiliser pour modifier un élément, ses éléments enfants ou ses attributs.  
  
 Les méthodes suivantes modifient un objet <xref:System.Xml.Linq.XElement>.  
  
|Méthode|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=nameWithType>|Remplace un élément par du code XML analysé.|  
|<xref:System.Xml.Linq.XElement.RemoveAll%2A?displayProperty=nameWithType>|Supprime tout le contenu (nœuds enfants et attributs) d'un élément.|  
|<xref:System.Xml.Linq.XElement.RemoveAttributes%2A?displayProperty=nameWithType>|Supprime les attributs d'un élément.|  
|<xref:System.Xml.Linq.XElement.ReplaceAll%2A?displayProperty=nameWithType>|Remplace tout le contenu (nœuds enfants et attributs) d'un élément.|  
|<xref:System.Xml.Linq.XElement.ReplaceAttributes%2A?displayProperty=nameWithType>|Remplace les attributs d'un élément.|  
|<xref:System.Xml.Linq.XElement.SetAttributeValue%2A?displayProperty=nameWithType>|Définit la valeur d'un attribut. Crée l'attribut s'il n'existe pas. Si la valeur est définie à `null`, supprime l'attribut.|  
|<xref:System.Xml.Linq.XElement.SetElementValue%2A?displayProperty=nameWithType>|Définit la valeur d'un élément enfant. Crée l'élément s'il n'existe pas. Si la valeur est définie à `null`, supprime l'élément.|  
|<xref:System.Xml.Linq.XElement.Value%2A?displayProperty=nameWithType>|Remplace le contenu (nœuds enfants) d'un élément par le texte spécifié.|  
|<xref:System.Xml.Linq.XElement.SetValue%2A?displayProperty=nameWithType>|Définit la valeur d'un élément.|  
  
 Les méthodes suivantes modifient un objet <xref:System.Xml.Linq.XAttribute>.  
  
|Méthode|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XAttribute.Value%2A?displayProperty=nameWithType>|Définit la valeur d'un attribut.|  
|<xref:System.Xml.Linq.XAttribute.SetValue%2A?displayProperty=nameWithType>|Définit la valeur d'un attribut.|  
  
 Les méthodes suivantes modifient un objet <xref:System.Xml.Linq.XNode> (y compris un objet <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument>).  
  
|Méthode|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XNode.ReplaceWith%2A?displayProperty=nameWithType>|Remplace un nœud par du nouveau contenu.|  
  
 Les méthodes suivantes modifient un objet <xref:System.Xml.Linq.XContainer> (un objet <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument>).  
  
|Méthode|Description|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XContainer.ReplaceNodes%2A?displayProperty=nameWithType>|Remplace les nœuds enfants par du nouveau contenu.|  
  
## <a name="see-also"></a>Voir aussi  
 [Modification d’arborescences XML (LINQ to XML) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/modifying-xml-trees-linq-to-xml.md)
