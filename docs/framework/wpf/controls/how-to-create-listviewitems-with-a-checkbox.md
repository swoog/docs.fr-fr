---
title: 'Procédure : Créer des ListViewItems avec une case à cocher'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: b09d5ad11b0961febf524cec1e19cb1e59832e44
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910778"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a>Procédure : Créer des ListViewItems avec une case à cocher
Cet exemple montre comment afficher une colonne de <xref:System.Windows.Controls.CheckBox> des contrôles dans un <xref:System.Windows.Controls.ListView> contrôle qui utilise un <xref:System.Windows.Controls.GridView>.  
  
## <a name="example"></a>Exemple  
 Pour créer une colonne qui contient <xref:System.Windows.Controls.CheckBox> des contrôles dans un <xref:System.Windows.Controls.ListView>, créer un <xref:System.Windows.DataTemplate> qui contient un <xref:System.Windows.Controls.CheckBox>. Puis définissez la <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> d’un <xref:System.Windows.Controls.GridViewColumn> à la <xref:System.Windows.DataTemplate>.  
  
 L’exemple suivant montre un <xref:System.Windows.DataTemplate> qui contient un <xref:System.Windows.Controls.CheckBox>. L’exemple lie la <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> propriété de la <xref:System.Windows.Controls.CheckBox> à la <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> valeur de propriété de la <xref:System.Windows.Controls.ListViewItem> qui le contient. Par conséquent, lorsque le <xref:System.Windows.Controls.ListViewItem> qui contient le <xref:System.Windows.Controls.CheckBox> est sélectionnée, le <xref:System.Windows.Controls.CheckBox> est activée.  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 L’exemple suivant montre comment créer une colonne de <xref:System.Windows.Controls.CheckBox> contrôles. Modifier la colonne, l’exemple définit le <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> propriété de la <xref:System.Windows.Controls.GridViewColumn> à la <xref:System.Windows.DataTemplate>.  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Vue d’ensemble de ListView](listview-overview.md)
- [Rubriques de guide pratique](listview-how-to-topics.md)
- [Vue d’ensemble de GridView](gridview-overview.md)
