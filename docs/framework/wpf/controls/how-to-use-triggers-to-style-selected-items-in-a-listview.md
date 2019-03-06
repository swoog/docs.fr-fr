---
title: "Procédure : Utiliser des déclencheurs pour appliquer un style aux éléments sélectionnés d'un ListView"
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], styling
ms.assetid: 1e2bdce0-afe8-4507-9b18-f33de43de25a
ms.openlocfilehash: 8c2d4adb2471c0f1891288573ce6b6460b20151d
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367919"
---
# <a name="how-to-use-triggers-to-style-selected-items-in-a-listview"></a>Procédure : Utiliser des déclencheurs pour appliquer un style aux éléments sélectionnés d'un ListView
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
