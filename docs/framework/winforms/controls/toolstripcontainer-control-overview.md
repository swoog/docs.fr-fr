---
title: Vue d'ensemble du contrôle ToolStripContainer
ms.date: 03/30/2017
f1_keywords:
- ToolStripContainer
helpviewer_keywords:
- toolbars [Windows Forms], built-in rafting
- ToolStripContainer control [Windows Forms], about ToolStripContainer control
ms.assetid: c7d63bff-64e2-4a63-bd89-d31bc96dacb8
ms.openlocfilehash: 59afb9de3a97545407fe96f5ded60faee9d9f725
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33536339"
---
# <a name="toolstripcontainer-control-overview"></a><span data-ttu-id="da71d-102">Vue d'ensemble du contrôle ToolStripContainer</span><span class="sxs-lookup"><span data-stu-id="da71d-102">ToolStripContainer Control Overview</span></span>
<span data-ttu-id="da71d-103">A <xref:System.Windows.Forms.ToolStripContainer> a des panneaux sur sa gauche, droite, haut et quatre côtés pour le positionnement et le rafting <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.MenuStrip>, et <xref:System.Windows.Forms.StatusStrip> contrôles.</span><span class="sxs-lookup"><span data-stu-id="da71d-103">A <xref:System.Windows.Forms.ToolStripContainer> has panels on its left, right, top, and bottom sides for positioning and rafting <xref:System.Windows.Forms.ToolStrip>, <xref:System.Windows.Forms.MenuStrip>, and <xref:System.Windows.Forms.StatusStrip> controls.</span></span> <span data-ttu-id="da71d-104">Plusieurs contrôles <xref:System.Windows.Forms.ToolStrip> s'empilent verticalement si vous les placez dans le <xref:System.Windows.Forms.ToolStripContainer> de gauche ou de droite.</span><span class="sxs-lookup"><span data-stu-id="da71d-104">Multiple <xref:System.Windows.Forms.ToolStrip> controls stack vertically if you put them in the left or right <xref:System.Windows.Forms.ToolStripContainer>.</span></span> <span data-ttu-id="da71d-105">Ils s'empilent horizontalement si vous les placez dans le <xref:System.Windows.Forms.ToolStripContainer> du haut ou du bas.</span><span class="sxs-lookup"><span data-stu-id="da71d-105">They stack horizontally if you put them in the top or bottom <xref:System.Windows.Forms.ToolStripContainer>.</span></span> <span data-ttu-id="da71d-106">Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStripContentPanel> central du <xref:System.Windows.Forms.ToolStripContainer> pour positionner les contrôles traditionnels sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="da71d-106">You can use the central <xref:System.Windows.Forms.ToolStripContentPanel> of the <xref:System.Windows.Forms.ToolStripContainer> to position traditional controls on the form.</span></span>  
  
 <span data-ttu-id="da71d-107">Tous les contrôles <xref:System.Windows.Forms.ToolStripContainer> sont directement sélectionnables au moment du design et peuvent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="da71d-107">Any or all <xref:System.Windows.Forms.ToolStripContainer> controls are directly selectable at design time and can be deleted.</span></span> <span data-ttu-id="da71d-108">Chaque panneau de configuration d’un <xref:System.Windows.Forms.ToolStripContainer> est extensible et réductible et peut être redimensionné avec les contrôles qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="da71d-108">Each panel of a <xref:System.Windows.Forms.ToolStripContainer> is expandable and collapsible, and resizes with the controls that it contains.</span></span>  
  
### <a name="important-toolstripcontainer-members"></a><span data-ttu-id="da71d-109">Membres ToolStripContainer importants</span><span class="sxs-lookup"><span data-stu-id="da71d-109">Important ToolStripContainer Members</span></span>  
  
|<span data-ttu-id="da71d-110">Name</span><span class="sxs-lookup"><span data-stu-id="da71d-110">Name</span></span>|<span data-ttu-id="da71d-111">Description</span><span class="sxs-lookup"><span data-stu-id="da71d-111">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripContainer.BottomToolStripPanel%2A>|<span data-ttu-id="da71d-112">Obtient le panneau inférieur de la <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="da71d-112">Gets the bottom panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.BottomToolStripPanelVisible%2A>|<span data-ttu-id="da71d-113">Obtient ou définit une valeur indiquant si le panneau inférieur de la <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="da71d-113">Gets or sets a value indicating whether the bottom panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.LeftToolStripPanel%2A>|<span data-ttu-id="da71d-114">Obtient le panneau gauche de la <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="da71d-114">Gets the left panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.LeftToolStripPanelVisible%2A>|<span data-ttu-id="da71d-115">Obtient ou définit une valeur indiquant si le panneau gauche de la <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="da71d-115">Gets or sets a value indicating whether the left panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.RightToolStripPanel%2A>|<span data-ttu-id="da71d-116">Obtient le panneau droit de la <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="da71d-116">Gets the right panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.RightToolStripPanelVisible%2A>|<span data-ttu-id="da71d-117">Obtient ou définit une valeur indiquant si le volet droit de la <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="da71d-117">Gets or sets a value indicating whether the right panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanel%2A>|<span data-ttu-id="da71d-118">Obtient le panneau supérieur de la <xref:System.Windows.Forms.ToolStripContainer>.</span><span class="sxs-lookup"><span data-stu-id="da71d-118">Gets the top panel of the <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripContainer.TopToolStripPanelVisible%2A>|<span data-ttu-id="da71d-119">Obtient ou définit une valeur indiquant si le panneau supérieur de la <xref:System.Windows.Forms.ToolStripContainer> est visible.</span><span class="sxs-lookup"><span data-stu-id="da71d-119">Gets or sets a value indicating whether the top panel of the <xref:System.Windows.Forms.ToolStripContainer> is visible.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="da71d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da71d-120">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStripContainer>  
 <xref:System.Windows.Forms.ToolStripContentPanel>
