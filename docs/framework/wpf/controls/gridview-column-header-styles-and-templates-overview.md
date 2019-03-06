---
title: Vue d'ensemble des modèles et styles d'en-tête de colonne GridView
ms.date: 03/30/2017
helpviewer_keywords:
- column headers [WPF], customizing
- ListView controls [WPF], GridView column header styles
- controls [WPF], ListView
- headers [WPF], customizing
- GridView view mode [WPF], customizing column headers
ms.assetid: 74835674-a39e-4ab5-9418-ad7f6ab7b956
ms.openlocfilehash: 6e5cf8a8b280a539feb73a54defbb0cd8c2c0f79
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366645"
---
# <a name="gridview-column-header-styles-and-templates-overview"></a>Vue d'ensemble des modèles et styles d'en-tête de colonne GridView
Cette présentation traite de l’ordre de priorité des propriétés que vous utilisez pour personnaliser un en-tête de colonne dans la <xref:System.Windows.Controls.GridView> mode d’affichage d’un <xref:System.Windows.Controls.ListView> contrôle.  
  
## <a name="customizing-a-column-header-in-a-gridview"></a>Personnalisation d’un en-tête de colonne dans un GridView  
 Les propriétés qui définissent le contenu, la disposition et le style d’un en-tête de colonne dans un <xref:System.Windows.Controls.GridView> se trouvent dans de nombreuses classes connexes. Certaines de ces propriétés ont des fonctionnalités semblables ou identiques.  
  
 Les lignes dans le tableau suivant affichent les groupes de propriétés qui exécutent la même fonction. Vous pouvez utiliser ces propriétés pour personnaliser les en-têtes de colonnes dans un <xref:System.Windows.Controls.GridView>. L’ordre de priorité des propriétés connexes est de droite à gauche où la propriété dans la colonne le plus à droite a la priorité la plus élevée. Par exemple, si un <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> est défini sur le <xref:System.Windows.Controls.GridViewColumnHeader> objet et le <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A> est défini sur associé <xref:System.Windows.Controls.GridViewColumn>, le <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> est prioritaire. Dans ce scénario, le <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A> n’a aucun effet.  
  
 **Propriétés connexes pour les en-têtes de colonne dans un GridView**  
  
|||||  
|-|-|-|-|  
|**Classes**|<xref:System.Windows.Controls.GridView>|<xref:System.Windows.Controls.GridViewColumn>|<xref:System.Windows.Controls.GridViewColumnHeader>|  
|**Propriétés du Menu contextuel**|<xref:System.Windows.Controls.GridView.ColumnHeaderContextMenu%2A>|Non applicable|<xref:System.Windows.FrameworkElement.ContextMenu%2A>|  
|**ToolTip**<br /><br /> **Propriétés**|<xref:System.Windows.Controls.GridView.ColumnHeaderToolTip%2A>|Non applicable|<xref:System.Windows.FrameworkElement.ToolTip%2A>|  
|**Modèle d’en-tête**<br /><br /> **Propriétés**|<xref:System.Windows.Controls.GridView.ColumnHeaderTemplate%2A> <sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.GridView.ColumnHeaderTemplateSelector%2A>|<xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> <sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A>|<xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> <sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.ContentControl.ContentTemplateSelector%2A>|  
|**Propriétés de style**|<xref:System.Windows.Controls.GridView.ColumnHeaderContainerStyle%2A>|<xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A>|<xref:System.Windows.FrameworkElement.Style%2A>|  
  
 <sup>1</sup>pour **propriétés de modèle d’en-tête**, si vous affectez à la fois le modèle et les propriétés du sélecteur de modèle, la propriété de modèle est prioritaire. Par exemple, si vous définissez à la fois le <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> et <xref:System.Windows.Controls.ContentControl.ContentTemplateSelector%2A> propriétés, le <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> propriété est prioritaire.  
  
## <a name="see-also"></a>Voir aussi
- [Rubriques de guide pratique](listview-how-to-topics.md)
- [Vue d’ensemble de ListView](listview-overview.md)
- [Vue d’ensemble de GridView](gridview-overview.md)
