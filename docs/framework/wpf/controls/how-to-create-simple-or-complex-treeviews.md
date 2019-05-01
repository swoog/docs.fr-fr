---
title: 'Procédure : Créer des arborescences simples ou complexes'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], creating
- Control class [WPF], TreeView [WPF], creating
ms.assetid: 1defbb78-b8e7-4c0e-b650-576453ac828d
ms.openlocfilehash: 7edb4933ebcc0f0d2cb02754238c2342ee9dd4a2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62031913"
---
# <a name="how-to-create-simple-or-complex-treeviews"></a>Procédure : Créer des arborescences simples ou complexes
Cet exemple montre comment créer une simple ou complexe <xref:System.Windows.Controls.TreeView> contrôles.  
  
 Un <xref:System.Windows.Controls.TreeView> se compose d’une hiérarchie de <xref:System.Windows.Controls.TreeViewItem> contrôles, qui peuvent contenir des chaînes de texte simple et contenu également plus complexe, tel que <xref:System.Windows.Controls.Button> contrôles ou un <xref:System.Windows.Controls.StackPanel> avec contenu incorporé. Vous pouvez définir explicitement le <xref:System.Windows.Controls.TreeView> contenu ou une source de données peut fournir le contenu. Cette rubrique fournit des exemples de ces concepts.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> propriété de la <xref:System.Windows.Controls.TreeViewItem> contient le contenu qui les <xref:System.Windows.Controls.TreeView> affiche pour cet élément. Un <xref:System.Windows.Controls.TreeViewItem> peut également avoir <xref:System.Windows.Controls.TreeViewItem> contrôles en tant que ses éléments enfants et vous peuvent définir ces éléments enfants à l’aide de la <xref:System.Windows.Controls.ItemsControl.Items%2A> propriété.  
  
 L’exemple suivant montre comment définir explicitement <xref:System.Windows.Controls.TreeViewItem> contenu en définissant le <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> propriété à une chaîne de texte.  
  
 [!code-xaml[TreeViewSimple#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#1)]  
  
 L’exemple suivant montre comment définir les éléments enfants d’un <xref:System.Windows.Controls.TreeViewItem> en définissant <xref:System.Windows.Controls.ItemsControl.Items%2A> qui sont <xref:System.Windows.Controls.Button> contrôles.  
  
 [!code-xaml[TreeViewSimple#3](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#3)]  
  
 L’exemple suivant montre comment créer un <xref:System.Windows.Controls.TreeView> où un <xref:System.Windows.Data.XmlDataProvider> fournit <xref:System.Windows.Controls.TreeViewItem> contenu et un <xref:System.Windows.HierarchicalDataTemplate> définit l’apparence du contenu.  
  
 [!code-xaml[TreeViewSimple#6](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#6)]  
  
 [!code-xaml[TreeViewSimple#7](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#7)]  
  
 [!code-xaml[TreeViewSimple#5](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#5)]  
  
 L’exemple suivant montre comment créer un <xref:System.Windows.Controls.TreeView> où le <xref:System.Windows.Controls.TreeViewItem> contient du contenu <xref:System.Windows.Controls.DockPanel> contrôles qui ont un contenu incorporé.  
  
 [!code-xaml[TreeViewSimple#9](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#9)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.TreeView>
- <xref:System.Windows.Controls.TreeViewItem>
- [Vue d'ensemble de TreeView](treeview-overview.md)
- [Rubriques de guide pratique](treeview-how-to-topics.md)
