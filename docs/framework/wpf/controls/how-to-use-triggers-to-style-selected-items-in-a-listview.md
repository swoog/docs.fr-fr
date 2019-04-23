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
# <a name="how-to-use-triggers-to-style-selected-items-in-a-listview"></a><span data-ttu-id="e2403-102">Procédure : Utiliser des déclencheurs pour appliquer un style aux éléments sélectionnés d’un ListView</span><span class="sxs-lookup"><span data-stu-id="e2403-102">How to: Use Triggers to Style Selected Items in a ListView</span></span>
<span data-ttu-id="e2403-103">Cet exemple montre comment définir <xref:System.Windows.Style.Triggers%2A> pour un <xref:System.Windows.Controls.ListViewItem> contrôle afin que lorsqu’une valeur de propriété d’un <xref:System.Windows.Controls.ListViewItem> modifications, la <xref:System.Windows.Style> de la <xref:System.Windows.Controls.ListViewItem> change en fonction.</span><span class="sxs-lookup"><span data-stu-id="e2403-103">This example shows how to define <xref:System.Windows.Style.Triggers%2A> for a <xref:System.Windows.Controls.ListViewItem> control so that when a property value of a <xref:System.Windows.Controls.ListViewItem> changes, the <xref:System.Windows.Style> of the <xref:System.Windows.Controls.ListViewItem> changes in response.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e2403-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e2403-104">Example</span></span>  
 <span data-ttu-id="e2403-105">Si vous souhaitez que le <xref:System.Windows.Style> d’un <xref:System.Windows.Controls.ListViewItem> pour modifier en réponse aux modifications de propriétés, définissez <xref:System.Windows.Style.Triggers%2A> pour la <xref:System.Windows.Style> modifier.</span><span class="sxs-lookup"><span data-stu-id="e2403-105">If you want the <xref:System.Windows.Style> of a <xref:System.Windows.Controls.ListViewItem> to change in response to property changes, define <xref:System.Windows.Style.Triggers%2A> for the <xref:System.Windows.Style> change.</span></span>  
  
 <span data-ttu-id="e2403-106">L’exemple suivant définit un <xref:System.Windows.Trigger> qui définit le <xref:System.Windows.Controls.Control.Foreground%2A> propriété <xref:System.Windows.Media.Brushes.Blue%2A> et modifie le <xref:System.Windows.FrameworkElement.Cursor%2A> pour afficher un <xref:System.Windows.Input.CursorType.Hand> lorsque le <xref:System.Windows.UIElement.IsMouseOver%2A> modifications apportées aux propriétés `true`.</span><span class="sxs-lookup"><span data-stu-id="e2403-106">The following example defines a <xref:System.Windows.Trigger> that sets the <xref:System.Windows.Controls.Control.Foreground%2A> property to <xref:System.Windows.Media.Brushes.Blue%2A> and changes the <xref:System.Windows.FrameworkElement.Cursor%2A> to display a <xref:System.Windows.Input.CursorType.Hand> when the <xref:System.Windows.UIElement.IsMouseOver%2A> property changes to `true`.</span></span>  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#Trigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#trigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
 <span data-ttu-id="e2403-107">L’exemple suivant définit un <xref:System.Windows.MultiTrigger> qui définit le <xref:System.Windows.Controls.Control.Foreground%2A> propriété d’un <xref:System.Windows.Controls.ListViewItem> à <xref:System.Windows.Media.Brushes.Yellow%2A> lorsque le <xref:System.Windows.Controls.ListViewItem> est l’élément sélectionné et a le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="e2403-107">The following example defines a <xref:System.Windows.MultiTrigger> that sets the <xref:System.Windows.Controls.Control.Foreground%2A> property of a <xref:System.Windows.Controls.ListViewItem> to <xref:System.Windows.Media.Brushes.Yellow%2A> when the <xref:System.Windows.Controls.ListViewItem> is the selected item and has keyboard focus.</span></span>  
  
 [!code-xaml[ListViewChkBox#ListViewItemTriggersStart](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersstart)]  
[!code-xaml[ListViewChkBox#MultiTrigger](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#multitrigger)]  
[!code-xaml[ListViewChkBox#ListViewItemTriggersEnd](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewChkBox/CS/window1.xaml#listviewitemtriggersend)]  
  
## <a name="see-also"></a><span data-ttu-id="e2403-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2403-108">See also</span></span>

- <xref:System.Windows.Controls.Control>
- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="e2403-109">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="e2403-109">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="e2403-110">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="e2403-110">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="e2403-111">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="e2403-111">GridView Overview</span></span>](gridview-overview.md)
