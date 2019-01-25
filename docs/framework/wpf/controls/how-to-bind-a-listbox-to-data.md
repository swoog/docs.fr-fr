---
title: 'Procédure : Lier un ListBox à des données'
ms.date: 03/30/2017
helpviewer_keywords:
- ListBox controls [WPF], binding data to
- data binding [WPF], ListBox control
- binding data [WPF], to ListBox control
ms.assetid: de93a907-709a-44a7-84bf-578b846a3d8b
ms.openlocfilehash: 6d37cda057ea1e7ca6761363857a2647da37afee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650650"
---
# <a name="how-to-bind-a-listbox-to-data"></a>Procédure : Lier un ListBox à des données
Un développeur peut créer <xref:System.Windows.Controls.ListBox> contrôles sans spécifier le contenu de chaque <xref:System.Windows.Controls.ListBoxItem> séparément. Vous pouvez utiliser la liaison de données pour lier des données aux éléments individuels.  
  
 L’exemple suivant montre comment créer un <xref:System.Windows.Controls.ListBox> qui remplit la <xref:System.Windows.Controls.ListBoxItem> éléments via la liaison de données à une source de données appelée *couleurs*. Dans ce cas il n’est pas nécessaire d’utiliser <xref:System.Windows.Controls.ListBoxItem> balises pour spécifier le contenu de chaque élément.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[ListBoxEvent#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#7)]  
[!code-xaml[ListBoxEvent#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#3)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.Controls.ListBoxItem>
- [Contrôles](../../../../docs/framework/wpf/advanced/optimizing-performance-controls.md)
