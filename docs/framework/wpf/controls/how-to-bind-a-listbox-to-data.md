---
title: 'Procédure : Lier un ListBox à des données'
ms.date: 03/30/2017
helpviewer_keywords:
- ListBox controls [WPF], binding data to
- data binding [WPF], ListBox control
- binding data [WPF], to ListBox control
ms.assetid: de93a907-709a-44a7-84bf-578b846a3d8b
ms.openlocfilehash: 2cbcb0fb859605c33e2d92559b4a47aa1725472c
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372879"
---
# <a name="how-to-bind-a-listbox-to-data"></a><span data-ttu-id="dba84-102">Procédure : Lier un ListBox à des données</span><span class="sxs-lookup"><span data-stu-id="dba84-102">How to: Bind a ListBox to Data</span></span>
<span data-ttu-id="dba84-103">Un développeur peut créer <xref:System.Windows.Controls.ListBox> contrôles sans spécifier le contenu de chaque <xref:System.Windows.Controls.ListBoxItem> séparément.</span><span class="sxs-lookup"><span data-stu-id="dba84-103">An application developer can create <xref:System.Windows.Controls.ListBox> controls without specifying the contents of each <xref:System.Windows.Controls.ListBoxItem> separately.</span></span> <span data-ttu-id="dba84-104">Vous pouvez utiliser la liaison de données pour lier des données aux éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="dba84-104">You can use data binding to bind data to the individual items.</span></span>  
  
 <span data-ttu-id="dba84-105">L’exemple suivant montre comment créer un <xref:System.Windows.Controls.ListBox> qui remplit la <xref:System.Windows.Controls.ListBoxItem> éléments via la liaison de données à une source de données appelée *couleurs*.</span><span class="sxs-lookup"><span data-stu-id="dba84-105">The following example shows how to create a <xref:System.Windows.Controls.ListBox> that populates the <xref:System.Windows.Controls.ListBoxItem> elements by data binding to a data source called *Colors*.</span></span> <span data-ttu-id="dba84-106">Dans ce cas il n’est pas nécessaire d’utiliser <xref:System.Windows.Controls.ListBoxItem> balises pour spécifier le contenu de chaque élément.</span><span class="sxs-lookup"><span data-stu-id="dba84-106">In this case it is not necessary to use <xref:System.Windows.Controls.ListBoxItem> tags to specify the content of each item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dba84-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="dba84-107">Example</span></span>  
 [!code-xaml[ListBoxEvent#7](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#7)]  
[!code-xaml[ListBoxEvent#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#3)]  
  
## <a name="see-also"></a><span data-ttu-id="dba84-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dba84-108">See also</span></span>
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.Controls.ListBoxItem>
- [<span data-ttu-id="dba84-109">Contrôles</span><span class="sxs-lookup"><span data-stu-id="dba84-109">Controls</span></span>](../advanced/optimizing-performance-controls.md)
