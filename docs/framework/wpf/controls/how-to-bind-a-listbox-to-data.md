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
# <a name="how-to-bind-a-listbox-to-data"></a><span data-ttu-id="4b332-102">Procédure : Lier un ListBox à des données</span><span class="sxs-lookup"><span data-stu-id="4b332-102">How to: Bind a ListBox to Data</span></span>
<span data-ttu-id="4b332-103">Un développeur peut créer <xref:System.Windows.Controls.ListBox> contrôles sans spécifier le contenu de chaque <xref:System.Windows.Controls.ListBoxItem> séparément.</span><span class="sxs-lookup"><span data-stu-id="4b332-103">An application developer can create <xref:System.Windows.Controls.ListBox> controls without specifying the contents of each <xref:System.Windows.Controls.ListBoxItem> separately.</span></span> <span data-ttu-id="4b332-104">Vous pouvez utiliser la liaison de données pour lier des données aux éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="4b332-104">You can use data binding to bind data to the individual items.</span></span>  
  
 <span data-ttu-id="4b332-105">L’exemple suivant montre comment créer un <xref:System.Windows.Controls.ListBox> qui remplit la <xref:System.Windows.Controls.ListBoxItem> éléments via la liaison de données à une source de données appelée *couleurs*.</span><span class="sxs-lookup"><span data-stu-id="4b332-105">The following example shows how to create a <xref:System.Windows.Controls.ListBox> that populates the <xref:System.Windows.Controls.ListBoxItem> elements by data binding to a data source called *Colors*.</span></span> <span data-ttu-id="4b332-106">Dans ce cas il n’est pas nécessaire d’utiliser <xref:System.Windows.Controls.ListBoxItem> balises pour spécifier le contenu de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="4b332-106">In this case it is not necessary to use <xref:System.Windows.Controls.ListBoxItem> tags to specify the content of each item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b332-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b332-107">Example</span></span>  
 [!code-xaml[ListBoxEvent#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#7)]  
[!code-xaml[ListBoxEvent#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#3)]  
  
## <a name="see-also"></a><span data-ttu-id="4b332-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b332-108">See also</span></span>
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.Controls.ListBoxItem>
- [<span data-ttu-id="4b332-109">Contrôles</span><span class="sxs-lookup"><span data-stu-id="4b332-109">Controls</span></span>](../../../../docs/framework/wpf/advanced/optimizing-performance-controls.md)
