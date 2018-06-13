---
title: 'Comment : créer des ListViewItems avec une case à cocher'
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], ListView
- controls [WPF], CheckBox
- ListView controls [WPF], CheckBox controls
- CheckBox control [WPF], ListView control
ms.assetid: f6d66c7f-906c-4f65-a55a-0ede9d00e26a
ms.openlocfilehash: 424bc25f9c584017d80ba1c8f1517211595fd247
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552673"
---
# <a name="how-to-create-listviewitems-with-a-checkbox"></a><span data-ttu-id="d6f27-102">Comment : créer des ListViewItems avec une case à cocher</span><span class="sxs-lookup"><span data-stu-id="d6f27-102">How to: Create ListViewItems with a CheckBox</span></span>
<span data-ttu-id="d6f27-103">Cet exemple montre comment afficher une colonne de <xref:System.Windows.Controls.CheckBox> des contrôles dans un <xref:System.Windows.Controls.ListView> contrôle qui utilise un <xref:System.Windows.Controls.GridView>.</span><span class="sxs-lookup"><span data-stu-id="d6f27-103">This example shows how to display a column of <xref:System.Windows.Controls.CheckBox> controls in a <xref:System.Windows.Controls.ListView> control that uses a <xref:System.Windows.Controls.GridView>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d6f27-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="d6f27-104">Example</span></span>  
 <span data-ttu-id="d6f27-105">Pour créer une colonne qui contient <xref:System.Windows.Controls.CheckBox> des contrôles dans un <xref:System.Windows.Controls.ListView>, créez un <xref:System.Windows.DataTemplate> qui contient un <xref:System.Windows.Controls.CheckBox>.</span><span class="sxs-lookup"><span data-stu-id="d6f27-105">To create a column that contains <xref:System.Windows.Controls.CheckBox> controls in a <xref:System.Windows.Controls.ListView>, create a <xref:System.Windows.DataTemplate> that contains a <xref:System.Windows.Controls.CheckBox>.</span></span> <span data-ttu-id="d6f27-106">Puis définissez la <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> d’un <xref:System.Windows.Controls.GridViewColumn> à la <xref:System.Windows.DataTemplate>.</span><span class="sxs-lookup"><span data-stu-id="d6f27-106">Then set the <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> of a <xref:System.Windows.Controls.GridViewColumn> to the <xref:System.Windows.DataTemplate>.</span></span>  
  
 <span data-ttu-id="d6f27-107">L’exemple suivant montre un <xref:System.Windows.DataTemplate> qui contient un <xref:System.Windows.Controls.CheckBox>.</span><span class="sxs-lookup"><span data-stu-id="d6f27-107">The following example shows a <xref:System.Windows.DataTemplate> that contains a <xref:System.Windows.Controls.CheckBox>.</span></span> <span data-ttu-id="d6f27-108">L’exemple lie la <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> propriété de la <xref:System.Windows.Controls.CheckBox> à la <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> valeur de propriété de la <xref:System.Windows.Controls.ListViewItem> qui le contient.</span><span class="sxs-lookup"><span data-stu-id="d6f27-108">The example binds the <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> property of the <xref:System.Windows.Controls.CheckBox> to the <xref:System.Windows.Controls.ListBoxItem.IsSelected%2A> property value of the <xref:System.Windows.Controls.ListViewItem> that contains it.</span></span> <span data-ttu-id="d6f27-109">Par conséquent, lorsque le <xref:System.Windows.Controls.ListViewItem> qui contient le <xref:System.Windows.Controls.CheckBox> est sélectionnée, le <xref:System.Windows.Controls.CheckBox> est activée.</span><span class="sxs-lookup"><span data-stu-id="d6f27-109">Therefore, when the <xref:System.Windows.Controls.ListViewItem> that contains the <xref:System.Windows.Controls.CheckBox> is selected, the <xref:System.Windows.Controls.CheckBox> is checked.</span></span>  
  
 [!code-xaml[ListViewChkBox#CheckBoxDataTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#checkboxdatatemplate)]  
  
 <span data-ttu-id="d6f27-110">L’exemple suivant montre comment créer une colonne de <xref:System.Windows.Controls.CheckBox> contrôles.</span><span class="sxs-lookup"><span data-stu-id="d6f27-110">The following example shows how to create a column of <xref:System.Windows.Controls.CheckBox> controls.</span></span> <span data-ttu-id="d6f27-111">Modifier la colonne, l’exemple définit le <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> propriété de la <xref:System.Windows.Controls.GridViewColumn> à la <xref:System.Windows.DataTemplate>.</span><span class="sxs-lookup"><span data-stu-id="d6f27-111">To make the column, the example sets the <xref:System.Windows.Controls.GridViewColumn.CellTemplate%2A> property of the <xref:System.Windows.Controls.GridViewColumn> to the <xref:System.Windows.DataTemplate>.</span></span>  
  
 [!code-xaml[ListViewChkBox#GridViewColumnCheckBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#gridviewcolumncheckbox)]  
  
## <a name="see-also"></a><span data-ttu-id="d6f27-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6f27-112">See Also</span></span>  
 <xref:System.Windows.Controls.Control>  
 <xref:System.Windows.Controls.ListView>  
 <xref:System.Windows.Controls.GridView>  
 [<span data-ttu-id="d6f27-113">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="d6f27-113">ListView Overview</span></span>](../../../../docs/framework/wpf/controls/listview-overview.md)  
 [<span data-ttu-id="d6f27-114">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="d6f27-114">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)  
 [<span data-ttu-id="d6f27-115">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="d6f27-115">GridView Overview</span></span>](../../../../docs/framework/wpf/controls/gridview-overview.md)
