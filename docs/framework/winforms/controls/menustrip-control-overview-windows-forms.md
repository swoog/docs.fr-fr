---
title: Vue d'ensemble du contrôle MenuStrip (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- MenuStrip
helpviewer_keywords:
- MenuStrip control [Windows Forms], about MenuStrip control
- menus [Windows Forms], creating
ms.assetid: f45516e5-bf01-4468-b851-d45f4c33c055
ms.openlocfilehash: 7cd761697a09205294727043efc6cf73816803ce
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59975596"
---
# <a name="menustrip-control-overview-windows-forms"></a><span data-ttu-id="a9e38-102">Vue d'ensemble du contrôle MenuStrip (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="a9e38-102">MenuStrip Control Overview (Windows Forms)</span></span>
<span data-ttu-id="a9e38-103">Menus exposent des fonctionnalités à vos utilisateurs en maintenant les commandes regroupées par un thème commun.</span><span class="sxs-lookup"><span data-stu-id="a9e38-103">Menus expose functionality to your users by holding commands that are grouped by a common theme.</span></span>  
  
 <span data-ttu-id="a9e38-104">Le <xref:System.Windows.Forms.MenuStrip> contrôle est une nouveauté de cette version de Visual Studio et .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a9e38-104">The <xref:System.Windows.Forms.MenuStrip> control is new to this version of Visual Studio and the .NET Framework.</span></span> <span data-ttu-id="a9e38-105">Avec le contrôle, vous pouvez créer facilement des menus, telles que celles dans Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a9e38-105">With the control, you can easily create menus like those found in Microsoft Office.</span></span>  
  
 <span data-ttu-id="a9e38-106">Le <xref:System.Windows.Forms.MenuStrip> contrôle prend en charge l’interface multidocument (MDI) et que la fusion de menus, les info-bulles et le dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="a9e38-106">The <xref:System.Windows.Forms.MenuStrip> control supports the multiple-document interface (MDI) and menu merging, tool tips, and overflow.</span></span> <span data-ttu-id="a9e38-107">Vous pouvez améliorer la facilité d’utilisation et la lisibilité de vos menus en ajoutant des clés d’accès, des touches de raccourci, des coches, des images et des barres de séparation.</span><span class="sxs-lookup"><span data-stu-id="a9e38-107">You can enhance the usability and readability of your menus by adding access keys, shortcut keys, check marks, images, and separator bars.</span></span>  
  
 <span data-ttu-id="a9e38-108">Le <xref:System.Windows.Forms.MenuStrip> contrôle remplace et ajoute des fonctionnalités à la <xref:System.Windows.Forms.MainMenu> contrôler ; Toutefois, le <xref:System.Windows.Forms.MainMenu> contrôle est conservé pour la compatibilité descendante et l’utilisation future si vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="a9e38-108">The <xref:System.Windows.Forms.MenuStrip> control replaces and adds functionality to the <xref:System.Windows.Forms.MainMenu> control; however, the <xref:System.Windows.Forms.MainMenu> control is retained for backward compatibility and future use if you choose.</span></span>  
  
## <a name="ways-to-use-the-menustrip-control"></a><span data-ttu-id="a9e38-109">Façons d’utiliser le contrôle MenuStrip</span><span class="sxs-lookup"><span data-stu-id="a9e38-109">Ways to Use the MenuStrip Control</span></span>  
 <span data-ttu-id="a9e38-110">Utilisez le <xref:System.Windows.Forms.MenuStrip> le contrôle à :</span><span class="sxs-lookup"><span data-stu-id="a9e38-110">Use the <xref:System.Windows.Forms.MenuStrip> control to:</span></span>  
  
-   <span data-ttu-id="a9e38-111">Créez facilement personnalisées, employées couramment menus qui prennent en charge utilisateur interface et mise en page fonctionnalités avancées, telles que texte et image classement et alignement, les opérations de glisser-déplacer, MDI, dépassement de capacité et autres modes d’accès aux commandes de menu.</span><span class="sxs-lookup"><span data-stu-id="a9e38-111">Create easily customized, commonly employed menus that support advanced user interface and layout features, such as text and image ordering and alignment, drag-and-drop operations, MDI, overflow, and alternate modes of accessing menu commands.</span></span>  
  
-   <span data-ttu-id="a9e38-112">Prend en charge l’apparence classique et le comportement du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a9e38-112">Support the typical appearance and behavior of the operating system.</span></span>  
  
-   <span data-ttu-id="a9e38-113">Gérer les événements cohérente pour tous les conteneurs et les éléments de contenu, de la même façon que vous gérez des événements pour d’autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="a9e38-113">Handle events consistently for all containers and contained items, in the same way you handle events for other controls.</span></span>  
  
 <span data-ttu-id="a9e38-114">Le tableau suivant présente certaines propriétés particulièrement importantes de <xref:System.Windows.Forms.MenuStrip> et des classes associées.</span><span class="sxs-lookup"><span data-stu-id="a9e38-114">The following table shows some particularly important properties of <xref:System.Windows.Forms.MenuStrip> and associated classes.</span></span>  
  
|<span data-ttu-id="a9e38-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="a9e38-115">Property</span></span>|<span data-ttu-id="a9e38-116">Description</span><span class="sxs-lookup"><span data-stu-id="a9e38-116">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A>|<span data-ttu-id="a9e38-117">Obtient ou définit le <xref:System.Windows.Forms.ToolStripMenuItem> qui est utilisé pour afficher une liste des formulaires enfants MDI.</span><span class="sxs-lookup"><span data-stu-id="a9e38-117">Gets or sets the <xref:System.Windows.Forms.ToolStripMenuItem> that is used to display a list of MDI child forms.</span></span>|  
|<xref:System.Windows.Forms.ToolStripItem.MergeAction%2A?displayProperty=nameWithType>|<span data-ttu-id="a9e38-118">Obtient ou définit comment les menus enfants sont fusionnés avec les menus parents dans les applications MDI.</span><span class="sxs-lookup"><span data-stu-id="a9e38-118">Gets or sets how child menus are merged with parent menus in MDI applications.</span></span>|  
|<xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A?displayProperty=nameWithType>|<span data-ttu-id="a9e38-119">Obtient ou définit la position d’un élément fusionné dans un menu dans les applications MDI.</span><span class="sxs-lookup"><span data-stu-id="a9e38-119">Gets or sets the position of a merged item within a menu in MDI applications.</span></span>|  
|<xref:System.Windows.Forms.Form.IsMdiContainer%2A?displayProperty=nameWithType>|<span data-ttu-id="a9e38-120">Obtient ou définit une valeur indiquant si le formulaire est un conteneur de formulaires enfants MDI.</span><span class="sxs-lookup"><span data-stu-id="a9e38-120">Gets or sets a value indicating whether the form is a container for MDI child forms.</span></span>|  
|<xref:System.Windows.Forms.MenuStrip.ShowItemToolTips%2A>|<span data-ttu-id="a9e38-121">Obtient ou définit une valeur indiquant si les info-bulles sont indiquées pour le <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="a9e38-121">Gets or sets a value indicating whether tool tips are shown for the <xref:System.Windows.Forms.MenuStrip>.</span></span>|  
|<xref:System.Windows.Forms.MenuStrip.CanOverflow%2A>|<span data-ttu-id="a9e38-122">Obtient ou définit une valeur indiquant si le <xref:System.Windows.Forms.MenuStrip> prend en charge les fonctionnalités de dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="a9e38-122">Gets or sets a value indicating whether the <xref:System.Windows.Forms.MenuStrip> supports overflow functionality.</span></span>|  
|<xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys%2A>|<span data-ttu-id="a9e38-123">Obtient ou définit les touches de raccourci associées à <xref:System.Windows.Forms.ToolStripMenuItem>.</span><span class="sxs-lookup"><span data-stu-id="a9e38-123">Gets or sets the shortcut keys associated with the <xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripMenuItem.ShowShortcutKeys%2A>|<span data-ttu-id="a9e38-124">Obtient ou définit une valeur qui indique si les touches de raccourci associées à <xref:System.Windows.Forms.ToolStripMenuItem> sont affichées en regard de <xref:System.Windows.Forms.ToolStripMenuItem>.</span><span class="sxs-lookup"><span data-stu-id="a9e38-124">Gets or sets a value indicating whether the shortcut keys that are associated with the <xref:System.Windows.Forms.ToolStripMenuItem> are displayed next to the <xref:System.Windows.Forms.ToolStripMenuItem>.</span></span>|  
  
 <span data-ttu-id="a9e38-125">Le tableau suivant présente les importantes <xref:System.Windows.Forms.MenuStrip> classes auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="a9e38-125">The following table shows the important <xref:System.Windows.Forms.MenuStrip> companion classes.</span></span>  
  
|<span data-ttu-id="a9e38-126">Classe</span><span class="sxs-lookup"><span data-stu-id="a9e38-126">Class</span></span>|<span data-ttu-id="a9e38-127">Description</span><span class="sxs-lookup"><span data-stu-id="a9e38-127">Description</span></span>|  
|-----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripMenuItem>|<span data-ttu-id="a9e38-128">Représente une option pouvant être sélectionnée, qui est affichée sur un <xref:System.Windows.Forms.MenuStrip> ou un <xref:System.Windows.Forms.ContextMenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="a9e38-128">Represents a selectable option displayed on a <xref:System.Windows.Forms.MenuStrip> or <xref:System.Windows.Forms.ContextMenuStrip>.</span></span>|  
|<xref:System.Windows.Forms.ContextMenuStrip>|<span data-ttu-id="a9e38-129">Représente un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="a9e38-129">Represents a shortcut menu.</span></span>|  
|<xref:System.Windows.Forms.ToolStripDropDown>|<span data-ttu-id="a9e38-130">Représente un contrôle qui permet à l’utilisateur de sélectionner un élément unique dans une liste qui s’affiche lorsque l’utilisateur clique sur un <xref:System.Windows.Forms.ToolStripDropDownButton> ou un élément de menu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="a9e38-130">Represents a control that allows the user to select a single item from a list that is displayed when the user clicks a <xref:System.Windows.Forms.ToolStripDropDownButton> or a higher-level menu item.</span></span>|  
|<xref:System.Windows.Forms.ToolStripDropDownItem>|<span data-ttu-id="a9e38-131">Fournit des fonctionnalités de base pour les contrôles dérivés de <xref:System.Windows.Forms.ToolStripItem> qui affichent des éléments de liste déroulante lorsque vous cliquez sur.</span><span class="sxs-lookup"><span data-stu-id="a9e38-131">Provides basic functionality for controls derived from <xref:System.Windows.Forms.ToolStripItem> that display drop-down items when clicked.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a9e38-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9e38-132">See also</span></span>

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripDropDown>
