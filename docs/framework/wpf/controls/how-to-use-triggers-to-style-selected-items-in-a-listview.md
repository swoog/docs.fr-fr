---
title: 'Procédure : Utiliser des déclencheurs pour appliquer un style aux éléments sélectionnés d’un ListView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 1e2bdce0-afe8-4507-9b18-f33de43de25a
ms.openlocfilehash: ad64382b871bae9114a1e63257de3f8595376923
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59145403"
---
# <a name="how-to-use-triggers-to-style-selected-items-in-a-listview"></a>Procédure : Utiliser des déclencheurs pour appliquer un style aux éléments sélectionnés d’un ListView
Cet exemple montre comment définir <xref:System.Windows.Style.Triggers%2A> pour un <xref:System.Windows.Controls.ListViewItem> contrôle afin que lorsqu’une valeur de propriété d’un <xref:System.Windows.Controls.ListViewItem> modifications, la <xref:System.Windows.Style> de la <xref:System.Windows.Controls.ListViewItem> change en fonction.  
  
## <a name="example"></a>Exemple  
 Si vous souhaitez que le <xref:System.Windows.Style> d’un <xref:System.Windows.Controls.ListViewItem> pour modifier en réponse aux modifications de propriétés, définissez <xref:System.Windows.Style.Triggers%2A> pour la <xref:System.Windows.Style> modifier.  
  
 L’exemple suivant définit un <xref:System.Windows.Trigger> qui définit le <xref:System.Windows.Controls.Control.Foreground%2A> propriété <xref:System.Windows.Media.Brushes.Blue%2A> et modifie le <xref:System.Windows.FrameworkElement.Cursor%2A> pour afficher un <xref:System.Windows.Input.CursorType.Hand> lorsque le <xref:System.Windows.UIElement.IsMouseOver%2A> modifications apportées aux propriétés `true`.  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#Trigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#trigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
 L’exemple suivant définit un <xref:System.Windows.MultiTrigger> qui définit le <xref:System.Windows.Controls.Control.Foreground%2A> propriété d’un <xref:System.Windows.Controls.ListViewItem> à <xref:System.Windows.Media.Brushes.Yellow%2A> lorsque le <xref:System.Windows.Controls.ListViewItem> est l’élément sélectionné et a le focus clavier.  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#MultiTrigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#multitrigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Rubriques de guide pratique](listview-how-to-topics.md)
- [Vue d’ensemble de ListView](listview-overview.md)
- [Vue d’ensemble de GridView](gridview-overview.md)
