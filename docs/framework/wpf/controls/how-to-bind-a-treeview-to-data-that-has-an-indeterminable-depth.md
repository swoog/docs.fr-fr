---
title: 'Procédure : Lier un TreeView à des données dont la profondeur ne peut pas être déterminée'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], binding to data of indeterminate depth
ms.assetid: daddcd74-1b0f-4ffd-baeb-ec934c5e0f53
ms.openlocfilehash: 7da0a121cdb854c787c105c92cec70b7c4b3244e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61911077"
---
# <a name="how-to-bind-a-treeview-to-data-that-has-an-indeterminable-depth"></a>Procédure : Lier un TreeView à des données dont la profondeur ne peut pas être déterminée
Il peut arriver lorsque vous souhaitez lier un <xref:System.Windows.Controls.TreeView> à une source de données dont la profondeur n’est pas connue.  Cela peut se produire lorsque les données sont récursifs par nature, par exemple un système de fichiers, dont les dossiers peuvent contenir des dossiers, ou de la structure organisationnelle d’une entreprise, où les employés ont les collaborateurs directs d’autres employés.  
  
 La source de données doit avoir un modèle d’objet hiérarchique. Par exemple, un `Employee` classe peut contenir une collection d’objets Employee qui sont les rapports directs d’un employé. Si les données sont représentées de manière qui n’est pas hiérarchique, vous devez générer une représentation hiérarchique des données.  
  
 Lorsque vous définissez la <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A?displayProperty=nameWithType> propriété et, si le <xref:System.Windows.Controls.ItemsControl> génère une <xref:System.Windows.Controls.ItemsControl> pour chaque élément enfant, puis l’enfant <xref:System.Windows.Controls.ItemsControl> utilise les mêmes <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> comme parent. Par exemple, si vous définissez la <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> propriété sur une limite de données <xref:System.Windows.Controls.TreeView>, chaque <xref:System.Windows.Controls.TreeViewItem> qui est généré utilise le <xref:System.Windows.DataTemplate> qui a été affectée à la <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A> propriété de la <xref:System.Windows.Controls.TreeView>.  
  
 Le <xref:System.Windows.HierarchicalDataTemplate> vous permet de spécifier le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour un <xref:System.Windows.Controls.TreeViewItem>, ou n’importe quel <xref:System.Windows.Controls.HeaderedItemsControl>, sur le modèle de données. Lorsque vous définissez la <xref:System.Windows.HierarchicalDataTemplate.ItemsSource%2A?displayProperty=nameWithType> propriété, cette valeur est utilisée lorsque le <xref:System.Windows.HierarchicalDataTemplate> est appliqué. En utilisant un <xref:System.Windows.HierarchicalDataTemplate>, vous pouvez définir de manière récursive le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour chaque <xref:System.Windows.Controls.TreeViewItem> dans le <xref:System.Windows.Controls.TreeView>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment lier un <xref:System.Windows.Controls.TreeView> à des données hiérarchiques et utiliser un <xref:System.Windows.HierarchicalDataTemplate> pour spécifier le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour chaque <xref:System.Windows.Controls.TreeViewItem>.  Le <xref:System.Windows.Controls.TreeView> lie aux données XML qui représentent les employés dans une entreprise.  Chaque `Employee` élément peut contenir d’autres `Employee` éléments pour indiquer les employés auxquels. Les données étant récursive, le <xref:System.Windows.HierarchicalDataTemplate> peut être appliqué à chaque niveau.  
  
 [!code-xaml[TreeViewWithUnknownDepth#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewWithUnknownDepth/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Vue d’ensemble des modèles de données](../data/data-templating-overview.md)
