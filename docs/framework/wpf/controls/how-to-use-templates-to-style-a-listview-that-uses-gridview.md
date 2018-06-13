---
title: 'Comment : utiliser des modèles pour appliquer un style à un ListView utilisant GridView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 94bf964b-96c8-4bdf-a0c3-f5271b7cb565
ms.openlocfilehash: 481d92d4301401f8ba87c4912cd44b17c5104b1b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33553830"
---
# <a name="how-to-use-templates-to-style-a-listview-that-uses-gridview"></a>Comment : utiliser des modèles pour appliquer un style à un ListView utilisant GridView
Cet exemple montre comment utiliser le <xref:System.Windows.DataTemplate> et <xref:System.Windows.Style> objets pour spécifier l’apparence d’un <xref:System.Windows.Controls.ListView> contrôle qui utilise un <xref:System.Windows.Controls.GridView> mode d’affichage.  
  
## <a name="example"></a>Exemple  
 Les exemples suivants montrent <xref:System.Windows.Style> et <xref:System.Windows.DataTemplate> objets permettant de personnaliser l’apparence d’un en-tête de colonne pour un <xref:System.Windows.Controls.GridViewColumn>.  
  
 [!code-xaml[ListViewTemplate#GridViewHeaderStyle](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewheaderstyle)]  
  
 [!code-xaml[ListViewTemplate#GridViewHeaderTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewheadertemplate)]  
  
 L’exemple suivant montre comment utiliser ces <xref:System.Windows.Style> et <xref:System.Windows.DataTemplate> objets pour définir le <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A> et <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> propriétés d’un <xref:System.Windows.Controls.GridViewColumn>. Le <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> propriété définit le contenu des cellules de la colonne.  
  
 [!code-xaml[ListViewTemplate#GridViewColumnTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewcolumntemplate)]  
  
 Le <xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A> et <xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> ne sont que deux de plusieurs propriétés que vous pouvez utiliser pour personnaliser l’apparence d’en-tête de colonne pour un <xref:System.Windows.Controls.GridView> contrôle. Pour plus d’informations, consultez [Vue d’ensemble des modèles et styles d’en-tête de colonne GridView](../../../../docs/framework/wpf/controls/gridview-column-header-styles-and-templates-overview.md).  
  
 L’exemple suivant montre comment définir un <xref:System.Windows.DataTemplate> qui personnalise l’apparence des cellules dans un <xref:System.Windows.Controls.GridViewColumn>.  
  
 [!code-xaml[ListViewTemplate#GridViewCellTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#gridviewcelltemplate)]  
  
 L’exemple suivant montre comment utiliser ce <xref:System.Windows.DataTemplate> pour définir le contenu d’un <xref:System.Windows.Controls.GridViewColumn> cellule. Ce modèle est utilisé à la place de la <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> propriété qui est indiquée dans le précédent <xref:System.Windows.Controls.GridViewColumn> exemple.  
  
 [!code-xaml[ListViewTemplate#CellTemplateProperty](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewTemplate/CS/window1.xaml#celltemplateproperty)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.ListView>  
 <xref:System.Windows.Controls.GridView>  
 [Vue d’ensemble de GridView](../../../../docs/framework/wpf/controls/gridview-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)  
 [Vue d’ensemble de ListView](../../../../docs/framework/wpf/controls/listview-overview.md)
