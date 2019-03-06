---
title: 'Procédure : Appliquer un style à une ligne dans un ListView implémentant un GridView'
ms.date: 03/30/2017
helpviewer_keywords:
- GridView controls [WPF], styling rows
- styling rows in ListViews implementing GridViews [WPF]
- ListView controls [WPF], styling rows with GridViews
ms.assetid: 2e406ba2-70a0-4e62-841f-0934859de76e
ms.openlocfilehash: 0c8806c399959fdc1466e0839ba469881718092b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57361627"
---
# <a name="how-to-style-a-row-in-a-listview-that-implements-a-gridview"></a>Procédure : Appliquer un style à une ligne dans un ListView implémentant un GridView
Cet exemple montre comment appliquer un style une ligne dans un <xref:System.Windows.Controls.ListView> contrôle qui implémente un <xref:System.Windows.Controls.GridView> <xref:System.Windows.Controls.ListView.View%2A> mode.  
  
## <a name="example"></a>Exemple  
 Vous pouvez appliquer un style une ligne dans un <xref:System.Windows.Controls.ListView> contrôle en définissant une <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> sur la <xref:System.Windows.Controls.ListView> contrôle. Définir le style pour ses éléments sont représentés en tant que <xref:System.Windows.Controls.ListViewItem> objets. Le <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> références le <xref:System.Windows.Controls.ControlTemplate> objets qui sont utilisés pour afficher le contenu de la ligne.  
  
 L’exemple complet, dont sont extraits les exemples suivants, affiche une collection d’informations sur des chansons, stockée dans une base de données [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)]. Chaque chanson de la base de données est associée à un champ d’évaluation. La valeur de ce champ spécifie comment afficher une ligne d’informations sur la chanson.  
  
 L’exemple suivant montre comment définir <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> pour le <xref:System.Windows.Controls.ListViewItem> les objets qui représentent les chansons de la collection. Le <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> références <xref:System.Windows.Controls.ControlTemplate> objets qui spécifient comment afficher une ligne d’informations sur la chanson.  
  
 [!code-xaml[ListViewItemStyleSnippet#ItemContainerStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#itemcontainerstyle)]  
  
 L’exemple suivant montre un <xref:System.Windows.Controls.ControlTemplate> qui ajoute la chaîne de texte `"Strongly Recommended"` à la ligne. Ce modèle est référencé dans le <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> et s’affiche lorsque l’évaluation de la chanson a la valeur 5 (cinq). Le <xref:System.Windows.Controls.ControlTemplate> inclut un <xref:System.Windows.Controls.GridViewRowPresenter> objet dispose le contenu de la ligne dans les colonnes comme défini par le <xref:System.Windows.Controls.GridView> mode d’affichage.  
  
 [!code-xaml[ListViewItemStyleSnippet#ControlTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#controltemplate)]  
  
 L’exemple suivant définit <xref:System.Windows.Controls.GridView>.  
  
 [!code-xaml[ListViewItemStyleSnippet#GridView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#gridview)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Rubriques de guide pratique](listview-how-to-topics.md)
- [Vue d’ensemble de ListView](listview-overview.md)
- [Application d’un style et création de modèles](styling-and-templating.md)
