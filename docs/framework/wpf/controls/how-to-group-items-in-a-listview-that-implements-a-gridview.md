---
title: 'Procédure : Grouper des éléments dans un ListView implémentant un GridView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], grouping items with GridViews
- grouping items in ListViews implementing GridViews [WPF]
- GridView controls [WPF], grouping items
ms.assetid: eebef25b-ddc6-424e-a66d-ea228d1bf33d
ms.openlocfilehash: b3dd6891976a942b299c87fca25e430e9ee59a51
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177669"
---
# <a name="how-to-group-items-in-a-listview-that-implements-a-gridview"></a>Procédure : Grouper des éléments dans un ListView implémentant un GridView
Cet exemple montre comment afficher les groupes d’éléments dans le <xref:System.Windows.Controls.GridView> mode d’affichage d’un <xref:System.Windows.Controls.ListView> contrôle.  
  
## <a name="example"></a>Exemple  
 Pour afficher les groupes d’éléments dans un <xref:System.Windows.Controls.ListView>, définir un <xref:System.Windows.Data.CollectionViewSource>. L’exemple suivant montre un <xref:System.Windows.Data.CollectionViewSource> qui regroupe les éléments de données en fonction de la valeur de la `Catalog` champ de données.  
  
 [!code-xaml[GridViewWithGroups#GroupingCollectionViewSource](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#groupingcollectionviewsource)]  
  
 L’exemple suivant définit la <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour le <xref:System.Windows.Controls.ListView> à la <xref:System.Windows.Data.CollectionViewSource> qui définit l’exemple précédent. L’exemple définit également un <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> qui implémente un <xref:System.Windows.Controls.Expander> contrôle.  
  
 [!code-xaml[GridViewWithGroups#ListViewGroups](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewgroups)]  
[!code-xaml[GridViewWithGroups#ListViewEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewend)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Rubriques de guide pratique](listview-how-to-topics.md)
- [Vue d’ensemble de ListView](listview-overview.md)
- [Vue d’ensemble de GridView](gridview-overview.md)
