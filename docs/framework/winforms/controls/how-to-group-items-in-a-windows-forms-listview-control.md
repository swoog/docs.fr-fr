---
title: 'Procédure : regrouper des éléments dans un contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], grouping items
- lists [Windows Forms], grouping items
- grouping
- list views [Windows Forms], grouping items
- groups
- groups [Windows Forms], in Windows Forms controls
ms.assetid: 610416a1-8da4-436c-af19-5f19e654769b
ms.openlocfilehash: f616436671da449e4f7b47c0a5d0c1b576584a1a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61941391"
---
# <a name="how-to-group-items-in-a-windows-forms-listview-control"></a><span data-ttu-id="d2366-102">Procédure : regrouper des éléments dans un contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d2366-102">How to: Group Items in a Windows Forms ListView Control</span></span>
<span data-ttu-id="d2366-103">Avec la fonctionnalité de regroupement de la <xref:System.Windows.Forms.ListView> contrôle, vous pouvez afficher des jeux d’éléments liés dans les groupes.</span><span class="sxs-lookup"><span data-stu-id="d2366-103">With the grouping feature of the <xref:System.Windows.Forms.ListView> control, you can display related sets of items in groups.</span></span> <span data-ttu-id="d2366-104">Ces groupes sont séparés sur l’écran par des en-têtes de groupe horizontal qui contiennent les titres de groupe.</span><span class="sxs-lookup"><span data-stu-id="d2366-104">These groups are separated on the screen by horizontal group headers that contain the group titles.</span></span> <span data-ttu-id="d2366-105">Vous pouvez utiliser <xref:System.Windows.Forms.ListView> groupes pour faciliter la navigation dans les longues listes en regroupant les éléments par ordre alphabétique, par date, ou par tout autre regroupement logique.</span><span class="sxs-lookup"><span data-stu-id="d2366-105">You can use <xref:System.Windows.Forms.ListView> groups to make navigating large lists easier by grouping items alphabetically, by date, or by any other logical grouping.</span></span> <span data-ttu-id="d2366-106">L’illustration suivante montre des éléments regroupés.</span><span class="sxs-lookup"><span data-stu-id="d2366-106">The following image shows some grouped items.</span></span>  
  
 <span data-ttu-id="d2366-107">![Groupes de ListView](./media/listviewgroups.gif "ListViewGroups")</span><span class="sxs-lookup"><span data-stu-id="d2366-107">![ListView Groups](./media/listviewgroups.gif "ListViewGroups")</span></span>  
<span data-ttu-id="d2366-108">ListView des éléments groupés</span><span class="sxs-lookup"><span data-stu-id="d2366-108">ListView grouped items</span></span>  
  
 <span data-ttu-id="d2366-109">Pour activer le regroupement, vous devez d’abord créer un ou plusieurs groupes dans le concepteur ou par programme.</span><span class="sxs-lookup"><span data-stu-id="d2366-109">To enable grouping, you must first create one or more groups either in the designer or programmatically.</span></span> <span data-ttu-id="d2366-110">Une fois un groupe a été défini, vous pouvez affecter <xref:System.Windows.Forms.ListView> éléments à des groupes.</span><span class="sxs-lookup"><span data-stu-id="d2366-110">After a group has been defined, you can assign <xref:System.Windows.Forms.ListView> items to groups.</span></span> <span data-ttu-id="d2366-111">Vous pouvez également déplacer des éléments d’un groupe vers un autre par programmation.</span><span class="sxs-lookup"><span data-stu-id="d2366-111">You can also move items from one group to another programmatically.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d2366-112"><xref:System.Windows.Forms.ListView> les groupes sont disponibles uniquement sur [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] lorsque votre application appelle la <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> (méthode).</span><span class="sxs-lookup"><span data-stu-id="d2366-112"><xref:System.Windows.Forms.ListView> groups are available only on [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] when your application calls the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType> method.</span></span> <span data-ttu-id="d2366-113">Sur les systèmes d’exploitation antérieurs, tout code relatif aux groupes n’a aucun effet et les groupes n’apparaîtra pas.</span><span class="sxs-lookup"><span data-stu-id="d2366-113">On earlier operating systems, any code relating to groups has no effect and the groups will not appear.</span></span> <span data-ttu-id="d2366-114">Pour plus d'informations, consultez <xref:System.Windows.Forms.ListView.Groups%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="d2366-114">For more information, see <xref:System.Windows.Forms.ListView.Groups%2A?displayProperty=nameWithType>.</span></span>  
  
### <a name="to-add-groups"></a><span data-ttu-id="d2366-115">Pour ajouter des groupes</span><span class="sxs-lookup"><span data-stu-id="d2366-115">To add groups</span></span>  
  
1. <span data-ttu-id="d2366-116">Utilisez la méthode <xref:System.Windows.Forms.ListViewGroupCollection.Add%2A> de la collection <xref:System.Windows.Forms.ListView.Groups%2A> .</span><span class="sxs-lookup"><span data-stu-id="d2366-116">Use the <xref:System.Windows.Forms.ListViewGroupCollection.Add%2A> method of the <xref:System.Windows.Forms.ListView.Groups%2A> collection.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#21)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#21)]  
  
### <a name="to-remove-groups"></a><span data-ttu-id="d2366-117">Pour supprimer des groupes</span><span class="sxs-lookup"><span data-stu-id="d2366-117">To remove groups</span></span>  
  
1. <span data-ttu-id="d2366-118">Utilisez le <xref:System.Windows.Forms.ListViewGroupCollection.RemoveAt%2A> ou <xref:System.Windows.Forms.ListViewGroupCollection.Clear%2A> méthode de la <xref:System.Windows.Forms.ListView.Groups%2A> collection.</span><span class="sxs-lookup"><span data-stu-id="d2366-118">Use the <xref:System.Windows.Forms.ListViewGroupCollection.RemoveAt%2A> or <xref:System.Windows.Forms.ListViewGroupCollection.Clear%2A> method of the <xref:System.Windows.Forms.ListView.Groups%2A> collection.</span></span>  
  
     <span data-ttu-id="d2366-119">Le <xref:System.Windows.Forms.ListViewGroupCollection.RemoveAt%2A> méthode supprime un groupe unique ; le <xref:System.Windows.Forms.ListViewGroupCollection.Clear%2A> méthode supprime tous les groupes de la liste.</span><span class="sxs-lookup"><span data-stu-id="d2366-119">The <xref:System.Windows.Forms.ListViewGroupCollection.RemoveAt%2A> method removes a single group; the <xref:System.Windows.Forms.ListViewGroupCollection.Clear%2A> method removes all groups from the list.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="d2366-120">Suppression d’un groupe ne supprime pas les éléments au sein de ce groupe.</span><span class="sxs-lookup"><span data-stu-id="d2366-120">Removing a group does not remove the items within that group.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#22)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#22)]  
  
### <a name="to-assign-items-to-groups-or-move-items-between-groups"></a><span data-ttu-id="d2366-121">Pour affecter des éléments aux groupes ou déplacer des éléments entre les groupes</span><span class="sxs-lookup"><span data-stu-id="d2366-121">To assign items to groups or move items between groups</span></span>  
  
1. <span data-ttu-id="d2366-122">Définir le <xref:System.Windows.Forms.ListViewItem.Group%2A?displayProperty=nameWithType> propriété des éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="d2366-122">Set the <xref:System.Windows.Forms.ListViewItem.Group%2A?displayProperty=nameWithType> property of individual items.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#23)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#23)]  
  
## <a name="see-also"></a><span data-ttu-id="d2366-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2366-123">See also</span></span>

- <xref:System.Windows.Forms.ListView>
- <xref:System.Windows.Forms.ListView.Groups%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ListViewGroup>
- [<span data-ttu-id="d2366-124">Contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="d2366-124">ListView Control</span></span>](listview-control-windows-forms.md)
- [<span data-ttu-id="d2366-125">Vue d’ensemble du contrôle ListView</span><span class="sxs-lookup"><span data-stu-id="d2366-125">ListView Control Overview</span></span>](listview-control-overview-windows-forms.md)
- [<span data-ttu-id="d2366-126">Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d2366-126">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
