---
title: 'Comment : grouper des éléments dans un ListView implémentant un GridView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], grouping items with GridViews
- grouping items in ListViews implementing GridViews [WPF]
- GridView controls [WPF], grouping items
ms.assetid: eebef25b-ddc6-424e-a66d-ea228d1bf33d
ms.openlocfilehash: 76074449d4ea1454689c51ecad54d7c495f00872
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33551906"
---
# <a name="how-to-group-items-in-a-listview-that-implements-a-gridview"></a><span data-ttu-id="2fec7-102">Comment : grouper des éléments dans un ListView implémentant un GridView</span><span class="sxs-lookup"><span data-stu-id="2fec7-102">How to: Group Items in a ListView That Implements a GridView</span></span>
<span data-ttu-id="2fec7-103">Cet exemple montre comment afficher les groupes d’éléments dans le <xref:System.Windows.Controls.GridView> mode d’affichage d’un <xref:System.Windows.Controls.ListView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2fec7-103">This example shows how to display groups of items in the <xref:System.Windows.Controls.GridView> view mode of a <xref:System.Windows.Controls.ListView> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2fec7-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2fec7-104">Example</span></span>  
 <span data-ttu-id="2fec7-105">Pour afficher les groupes d’éléments dans un <xref:System.Windows.Controls.ListView>, définir un <xref:System.Windows.Data.CollectionViewSource>.</span><span class="sxs-lookup"><span data-stu-id="2fec7-105">To display groups of items in a <xref:System.Windows.Controls.ListView>, define a <xref:System.Windows.Data.CollectionViewSource>.</span></span> <span data-ttu-id="2fec7-106">L’exemple suivant montre un <xref:System.Windows.Data.CollectionViewSource> qui regroupe les éléments de données en fonction de la valeur de la `Catalog` champ de données.</span><span class="sxs-lookup"><span data-stu-id="2fec7-106">The following example shows a <xref:System.Windows.Data.CollectionViewSource> that groups data items according to the value of the `Catalog` data field.</span></span>  
  
 [!code-xaml[GridViewWithGroups#GroupingCollectionViewSource](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#groupingcollectionviewsource)]  
  
 <span data-ttu-id="2fec7-107">L’exemple suivant définit la <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> pour le <xref:System.Windows.Controls.ListView> à le <xref:System.Windows.Data.CollectionViewSource> par l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="2fec7-107">The following example sets the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> for the <xref:System.Windows.Controls.ListView> to the <xref:System.Windows.Data.CollectionViewSource> that the previous example defines.</span></span> <span data-ttu-id="2fec7-108">L’exemple définit également un <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> qui implémente un <xref:System.Windows.Controls.Expander> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2fec7-108">The example also defines a <xref:System.Windows.Controls.ItemsControl.GroupStyle%2A> that implements an <xref:System.Windows.Controls.Expander> control.</span></span>  
  
 [!code-xaml[GridViewWithGroups#ListViewGroups](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewgroups)]  
[!code-xaml[GridViewWithGroups#ListViewEnd](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GridViewWithGroups/CS/Window1.xaml#listviewend)]  
  
## <a name="see-also"></a><span data-ttu-id="2fec7-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fec7-109">See Also</span></span>  
 <xref:System.Windows.Controls.ListView>  
 <xref:System.Windows.Controls.GridView>  
 [<span data-ttu-id="2fec7-110">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="2fec7-110">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)  
 [<span data-ttu-id="2fec7-111">Vue d’ensemble de ListView</span><span class="sxs-lookup"><span data-stu-id="2fec7-111">ListView Overview</span></span>](../../../../docs/framework/wpf/controls/listview-overview.md)  
 [<span data-ttu-id="2fec7-112">Vue d’ensemble de GridView</span><span class="sxs-lookup"><span data-stu-id="2fec7-112">GridView Overview</span></span>](../../../../docs/framework/wpf/controls/gridview-overview.md)
