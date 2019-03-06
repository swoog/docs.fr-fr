---
title: 'Procédure : Créer des arborescences simples ou complexes'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], creating
- Control class [WPF], TreeView [WPF], creating
ms.assetid: 1defbb78-b8e7-4c0e-b650-576453ac828d
ms.openlocfilehash: 9b19443c80818809122b0bbfc7c7dae7b4b40da5
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57368912"
---
# <a name="how-to-create-simple-or-complex-treeviews"></a><span data-ttu-id="f7dcd-102">Procédure : Créer des arborescences simples ou complexes</span><span class="sxs-lookup"><span data-stu-id="f7dcd-102">How to: Create Simple or Complex TreeViews</span></span>
<span data-ttu-id="f7dcd-103">Cet exemple montre comment créer une simple ou complexe <xref:System.Windows.Controls.TreeView> contrôles.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-103">This example shows how to create simple or complex <xref:System.Windows.Controls.TreeView> controls.</span></span>  
  
 <span data-ttu-id="f7dcd-104">Un <xref:System.Windows.Controls.TreeView> se compose d’une hiérarchie de <xref:System.Windows.Controls.TreeViewItem> contrôles, qui peuvent contenir des chaînes de texte simple et contenu également plus complexe, tel que <xref:System.Windows.Controls.Button> contrôles ou un <xref:System.Windows.Controls.StackPanel> avec contenu incorporé.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-104">A <xref:System.Windows.Controls.TreeView> consists of a hierarchy of <xref:System.Windows.Controls.TreeViewItem> controls, which can contain simple text strings and also more complex content, such as <xref:System.Windows.Controls.Button> controls or a <xref:System.Windows.Controls.StackPanel> with embedded content.</span></span> <span data-ttu-id="f7dcd-105">Vous pouvez définir explicitement le <xref:System.Windows.Controls.TreeView> contenu ou une source de données peut fournir le contenu.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-105">You can explicitly define the <xref:System.Windows.Controls.TreeView> content or a data source can provide the content.</span></span> <span data-ttu-id="f7dcd-106">Cette rubrique fournit des exemples de ces concepts.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-106">This topic provides examples of these concepts.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7dcd-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7dcd-107">Example</span></span>  
 <span data-ttu-id="f7dcd-108">Le <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> propriété de la <xref:System.Windows.Controls.TreeViewItem> contient le contenu qui les <xref:System.Windows.Controls.TreeView> affiche pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-108">The <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> property of the <xref:System.Windows.Controls.TreeViewItem> contains the content that the <xref:System.Windows.Controls.TreeView> displays for that item.</span></span> <span data-ttu-id="f7dcd-109">Un <xref:System.Windows.Controls.TreeViewItem> peut également avoir <xref:System.Windows.Controls.TreeViewItem> contrôles en tant que ses éléments enfants et vous peuvent définir ces éléments enfants à l’aide de la <xref:System.Windows.Controls.ItemsControl.Items%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-109">A <xref:System.Windows.Controls.TreeViewItem> can also have <xref:System.Windows.Controls.TreeViewItem> controls as its child elements and you can define these child elements by using the <xref:System.Windows.Controls.ItemsControl.Items%2A> property.</span></span>  
  
 <span data-ttu-id="f7dcd-110">L’exemple suivant montre comment définir explicitement <xref:System.Windows.Controls.TreeViewItem> contenu en définissant le <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> propriété à une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-110">The following example shows how to explicitly define <xref:System.Windows.Controls.TreeViewItem> content by setting the <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> property to a text string.</span></span>  
  
 [!code-xaml[TreeViewSimple#1](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#1)]  
  
 <span data-ttu-id="f7dcd-111">L’exemple suivant montre comment définir les éléments enfants d’un <xref:System.Windows.Controls.TreeViewItem> en définissant <xref:System.Windows.Controls.ItemsControl.Items%2A> qui sont <xref:System.Windows.Controls.Button> contrôles.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-111">The following example show how to define child elements of a <xref:System.Windows.Controls.TreeViewItem> by defining <xref:System.Windows.Controls.ItemsControl.Items%2A> that are <xref:System.Windows.Controls.Button> controls.</span></span>  
  
 [!code-xaml[TreeViewSimple#3](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#3)]  
  
 <span data-ttu-id="f7dcd-112">L’exemple suivant montre comment créer un <xref:System.Windows.Controls.TreeView> où un <xref:System.Windows.Data.XmlDataProvider> fournit <xref:System.Windows.Controls.TreeViewItem> contenu et un <xref:System.Windows.HierarchicalDataTemplate> définit l’apparence du contenu.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-112">The following example shows how to create a <xref:System.Windows.Controls.TreeView> where an <xref:System.Windows.Data.XmlDataProvider> provides <xref:System.Windows.Controls.TreeViewItem> content and a <xref:System.Windows.HierarchicalDataTemplate> defines the appearance of the content.</span></span>  
  
 [!code-xaml[TreeViewSimple#6](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#6)]  
  
 [!code-xaml[TreeViewSimple#7](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#7)]  
  
 [!code-xaml[TreeViewSimple#5](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#5)]  
  
 <span data-ttu-id="f7dcd-113">L’exemple suivant montre comment créer un <xref:System.Windows.Controls.TreeView> où le <xref:System.Windows.Controls.TreeViewItem> contient du contenu <xref:System.Windows.Controls.DockPanel> contrôles qui ont un contenu incorporé.</span><span class="sxs-lookup"><span data-stu-id="f7dcd-113">The following example shows how to create a <xref:System.Windows.Controls.TreeView> where the <xref:System.Windows.Controls.TreeViewItem> content contains <xref:System.Windows.Controls.DockPanel> controls that have embedded content.</span></span>  
  
 [!code-xaml[TreeViewSimple#9](~/samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#9)]  
  
## <a name="see-also"></a><span data-ttu-id="f7dcd-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7dcd-114">See also</span></span>
- <xref:System.Windows.Controls.TreeView>
- <xref:System.Windows.Controls.TreeViewItem>
- [<span data-ttu-id="f7dcd-115">Vue d'ensemble de TreeView</span><span class="sxs-lookup"><span data-stu-id="f7dcd-115">TreeView Overview</span></span>](treeview-overview.md)
- [<span data-ttu-id="f7dcd-116">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="f7dcd-116">How-to Topics</span></span>](treeview-how-to-topics.md)
