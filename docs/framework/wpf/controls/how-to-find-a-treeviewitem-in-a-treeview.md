---
title: 'Procédure : Trouver un TreeViewItem dans un TreeView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- TreeView control [WPF], finding a TreeViewItem
- TreeViewItem [WPF], finding
ms.assetid: 72ecd40c-3939-4e01-b617-5e9daa6074d9
ms.openlocfilehash: 034ec2e57fb3b6a9b3a81f66f6888a68e2c113d7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910531"
---
# <a name="how-to-find-a-treeviewitem-in-a-treeview"></a>Procédure : Trouver un TreeViewItem dans un TreeView
Le <xref:System.Windows.Controls.TreeView> contrôle fournit un moyen pratique d’afficher des données hiérarchiques. Si votre <xref:System.Windows.Controls.TreeView> est lié à une source de données, le <xref:System.Windows.Controls.TreeView.SelectedItem%2A> propriété offre un moyen pratique pour vous permettre de récupérer rapidement l’objet de données sélectionnée. Il est généralement préférable d’utiliser l’objet de données sous-jacent, mais parfois vous devez manipuler par programmation les données contenant <xref:System.Windows.Controls.TreeViewItem>. Par exemple, vous devrez peut-être développer par programme le <xref:System.Windows.Controls.TreeViewItem>, ou sélectionnez un autre élément dans le <xref:System.Windows.Controls.TreeView>.  
  
 Pour rechercher un <xref:System.Windows.Controls.TreeViewItem> qui contient un objet de données spécifique, vous devez traverser chaque niveau de la <xref:System.Windows.Controls.TreeView>. Les éléments dans un <xref:System.Windows.Controls.TreeView> peuvent également être virtualisées pour améliorer les performances. Dans le cas où les éléments peuvent être virtualisés, vous devez également créer un <xref:System.Windows.Controls.TreeViewItem> pour vérifier si elle contient l’objet de données.  
  
## <a name="example"></a>Exemple  
  
## <a name="description"></a>Description  
 L’exemple suivant recherche une <xref:System.Windows.Controls.TreeView> pour un objet spécifique et retourne l’objet qui contient <xref:System.Windows.Controls.TreeViewItem>. L’exemple vérifie que chaque <xref:System.Windows.Controls.TreeViewItem> est instancié afin que ses éléments enfants peuvent être recherchés. Cet exemple fonctionne également si le <xref:System.Windows.Controls.TreeView> n’utilise pas d’éléments virtualisés.  
  
> [!NOTE]
>  L’exemple suivant fonctionne pour tout <xref:System.Windows.Controls.TreeView>, quel que soit le modèle de données sous-jacent et recherche chaque <xref:System.Windows.Controls.TreeViewItem> jusqu'à ce que l’objet est trouvé. Une autre technique qui offre de meilleures performances consiste à rechercher le modèle de données pour l’objet spécifié, effectuer le suivi de son emplacement dans la hiérarchie de données et ensuite trouver correspondant <xref:System.Windows.Controls.TreeViewItem> dans le <xref:System.Windows.Controls.TreeView>. Toutefois, la technique qui offre de meilleures performances requiert une connaissance du modèle de données et ne peut pas être généralisée pour tous <xref:System.Windows.Controls.TreeView>.  
  
## <a name="code"></a>Code  
 [!code-csharp[TreeViewFindTVI#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewFindTVI/CSharp/MainWindow.xaml.cs#1)]
 [!code-vb[TreeViewFindTVI#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TreeViewFindTVI/VisualBasic/MainWindow.xaml.vb#1)]  
  
 Le code précédent s’appuie sur un personnalisé <xref:System.Windows.Controls.VirtualizingStackPanel> qui expose une méthode nommée `BringIntoView`. Le code suivant définit personnalisé <xref:System.Windows.Controls.VirtualizingStackPanel>.  
  
 [!code-csharp[TreeViewFindTVI#2](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewFindTVI/CSharp/MainWindow.xaml.cs#2)]
 [!code-vb[TreeViewFindTVI#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TreeViewFindTVI/VisualBasic/MainWindow.xaml.vb#2)]  
  
 Le XAML suivant montre comment créer un <xref:System.Windows.Controls.TreeView> qui utilise personnalisé <xref:System.Windows.Controls.VirtualizingStackPanel>.  
  
 [!code-xaml[TreeViewFindTVI#3](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewFindTVI/CSharp/MainWindow.xaml#3)]  
  
## <a name="see-also"></a>Voir aussi

- [Améliorer les performances d'un contrôle TreeView](how-to-improve-the-performance-of-a-treeview.md)
