---
title: Vue d'ensemble du contrôle ToolStripContainer
ms.date: 03/30/2017
f1_keywords:
- ToolStripContainer
helpviewer_keywords:
- toolbars [Windows Forms], built-in rafting
- ToolStripContainer control [Windows Forms], about ToolStripContainer control
ms.assetid: c7d63bff-64e2-4a63-bd89-d31bc96dacb8
ms.openlocfilehash: c279316c2a372a1498707b27ec8658813306304b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59768330"
---
# <a name="toolstripcontainer-control-overview"></a><span data-ttu-id="4d2f9-102">Vue d'ensemble du contrôle ToolStripContainer</span><span class="sxs-lookup"><span data-stu-id="4d2f9-102">ToolStripContainer Control Overview</span></span>
<span data-ttu-id="4d2f9-103">Un <xref:System.Windows.Forms.ToolStripContainer> a des panneaux sur sa gauche, droite, haut et côtés pour le positionnement et le rafting <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.MenuStrip>, et <xref:System.Windows.Forms.StatusStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-103">A <xref:System.Windows.Forms.ToolStripContainer> has panels on its left, right, top, and bottom sides for positioning and rafting <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.MenuStrip>, and <xref:System.Windows.Forms.StatusStrip> controls.</span></span> <span data-ttu-id="4d2f9-104">Plusieurs contrôles <xref:System.Windows.Forms.ToolStrip> s'empilent verticalement si vous les placez dans le <xref:System.Windows.Forms.ToolStripContainer> de gauche ou de droite.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-104">Multiple <xref:System.Windows.Forms.ToolStrip> controls stack vertically if you put them in the left or right <xref:System.Windows.Forms.ToolStripContainer>.</span></span> <span data-ttu-id="4d2f9-105">Ils s'empilent horizontalement si vous les placez dans le <xref:System.Windows.Forms.ToolStripContainer> du haut ou du bas.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-105">They stack horizontally if you put them in the top or bottom <xref:System.Windows.Forms.ToolStripContainer>.</span></span> <span data-ttu-id="4d2f9-106">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStripContentPanel> central du <xref:System.Windows.Forms.ToolStripContainer> pour positionner les contrôles traditionnels sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-106">You can use the central <xref:System.Windows.Forms.ToolStripContentPanel> of the <xref:System.Windows.Forms.ToolStripContainer> to position traditional controls on the form.</span></span>  
  
 <span data-ttu-id="4d2f9-107">Tous les contrôles <xref:System.Windows.Forms.ToolStripContainer> sont directement sélectionnables au moment du design et peuvent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-107">Any or all <xref:System.Windows.Forms.ToolStripContainer> controls are directly selectable at design time and can be deleted.</span></span> <span data-ttu-id="4d2f9-108">Chaque panneau d’un <xref:System.Windows.Forms.ToolStripContainer> est extensible et réductible et est redimensionné avec les contrôles qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-108">Each panel of a <xref:System.Windows.Forms.ToolStripContainer> is expandable and collapsible, and resizes with the controls that it contains.</span></span>  
  
### <a name="important-toolstripcontainer-members"></a><span data-ttu-id="4d2f9-109">Membres ToolStripContainer importants</span><span class="sxs-lookup"><span data-stu-id="4d2f9-109">Important ToolStripContainer Members</span></span>  
  
|<span data-ttu-id="4d2f9-110">Nom</span><span class="sxs-lookup"><span data-stu-id="4d2f9-110">Name</span></span>|<span data-ttu-id="4d2f9-111">Description</span><span class="sxs-lookup"><span data-stu-id="4d2f9-111">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripContainer.BottomToolStripPanel%2A>|<span data-ttu-id="4d2f9-112">Obtient le panneau inférieur de <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-112">Gets the bottom panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.BottomToolStripPanelVisible%2A>|<span data-ttu-id="4d2f9-113">Obtient ou définit une valeur indiquant si le panneau inférieur de <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-113">Gets or sets a value indicating whether the bottom panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.LeftToolStripPanel%2A>|<span data-ttu-id="4d2f9-114">Obtient le panneau gauche de <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-114">Gets the left panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.LeftToolStripPanelVisible%2A>|<span data-ttu-id="4d2f9-115">Obtient ou définit une valeur indiquant si le panneau gauche de <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-115">Gets or sets a value indicating whether the left panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.RightToolStripPanel%2A>|<span data-ttu-id="4d2f9-116">Obtient le panneau droit de <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-116">Gets the right panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.RightToolStripPanelVisible%2A>|<span data-ttu-id="4d2f9-117">Obtient ou définit une valeur indiquant si le panneau droit de <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-117">Gets or sets a value indicating whether the right panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A>|<span data-ttu-id="4d2f9-118">Obtient le panneau supérieur de <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-118">Gets the top panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanelVisible%2A>|<span data-ttu-id="4d2f9-119">Obtient ou définit une valeur indiquant si le panneau supérieur de <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="4d2f9-119">Gets or sets a value indicating whether the top panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4d2f9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d2f9-120">See also</span></span>

- <xref:System.Windows.Forms.ToolStripContainer>
- <xref:System.Windows.Forms.ToolStripContentPanel>
