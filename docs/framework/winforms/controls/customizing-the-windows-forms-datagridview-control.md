---
title: Personnalisation du contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], customization
- DataGridView control [Windows Forms], customization
ms.assetid: 01ea5d4c-a736-4596-b0e9-a67a1b86e15f
ms.openlocfilehash: 1f9c68ae85d7bad2b8cdcdaa63c1e7b46f9568ed
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57703333"
---
# <a name="customizing-the-windows-forms-datagridview-control"></a><span data-ttu-id="8d497-102">Personnalisation du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-102">Customizing the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="8d497-103">Le `DataGridView` contrôle fournit plusieurs propriétés que vous pouvez utiliser pour ajuster l’apparence et le comportement de base (aspect) de ses cellules, lignes et des colonnes.</span><span class="sxs-lookup"><span data-stu-id="8d497-103">The `DataGridView` control provides several properties that you can use to adjust the appearance and basic behavior (look and feel) of its cells, rows, and columns.</span></span> <span data-ttu-id="8d497-104">Si vous avez des besoins particuliers qui vont au-delà des capacités de la <xref:System.Windows.Forms.DataGridViewCellStyle> class, toutefois, vous pouvez également implémenter le dessin owner-drawn pour le contrôle ou étendre ses fonctionnalités en créant des cellules personnalisés, des colonnes et des lignes.</span><span class="sxs-lookup"><span data-stu-id="8d497-104">If you have special needs that go beyond the capabilities of the <xref:System.Windows.Forms.DataGridViewCellStyle> class, however, you can also implement owner drawing for the control or extend its capabilities by creating custom cells, columns, and rows.</span></span>  
  
 <span data-ttu-id="8d497-105">Pour peindre des cellules et des lignes vous-même, vous pouvez gérer différents `DataGridView` événements de peinture.</span><span class="sxs-lookup"><span data-stu-id="8d497-105">To paint cells and rows yourself, you can handle various `DataGridView` painting events.</span></span> <span data-ttu-id="8d497-106">Pour modifier des fonctionnalités existantes ou fournir de nouvelles fonctionnalités, vous pouvez créer vos propres types dérivés d’existant `DataGridViewCell`, `DataGridViewColumn`, et `DataGridViewRow` types.</span><span class="sxs-lookup"><span data-stu-id="8d497-106">To modify existing functionality or provide new functionality, you can create your own types derived from the existing `DataGridViewCell`, `DataGridViewColumn`, and `DataGridViewRow` types.</span></span> <span data-ttu-id="8d497-107">Vous pouvez également fournir les nouvelles fonctionnalités de modification en créant des types dérivés qui affichent un contrôle de votre choix lorsqu’une cellule est en mode édition.</span><span class="sxs-lookup"><span data-stu-id="8d497-107">You can also provide new editing capabilities by creating derived types that display a control of your choosing when a cell is in edit mode.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8d497-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8d497-108">In This Section</span></span>  
 [<span data-ttu-id="8d497-109">Guide pratique pour Personnaliser l’apparence des cellules dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-109">How to: Customize the Appearance of Cells in the Windows Forms DataGridView Control</span></span>](customize-the-appearance-of-cells-in-the-datagrid.md)  
 <span data-ttu-id="8d497-110">Décrit comment gérer les <xref:System.Windows.Forms.DataGridView.CellPainting> événement pour peindre les cellules manuellement.</span><span class="sxs-lookup"><span data-stu-id="8d497-110">Describes how to handle the <xref:System.Windows.Forms.DataGridView.CellPainting> event in order to paint cells manually.</span></span>  
  
 [<span data-ttu-id="8d497-111">Guide pratique pour Personnaliser l’apparence des lignes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-111">How to: Customize the Appearance of Rows in the Windows Forms DataGridView Control</span></span>](customize-the-appearance-of-rows-in-the-datagrid.md)  
 <span data-ttu-id="8d497-112">Décrit comment gérer les <xref:System.Windows.Forms.DataGridView.RowPrePaint> et <xref:System.Windows.Forms.DataGridView.RowPostPaint> événements afin de peindre les lignes avec un arrière-plan dégradé personnalisé et un contenu qui s’étend sur plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="8d497-112">Describes how to handle the <xref:System.Windows.Forms.DataGridView.RowPrePaint> and <xref:System.Windows.Forms.DataGridView.RowPostPaint> events in order to paint rows with a custom, gradient background and content that spans multiple columns.</span></span>  
  
 [<span data-ttu-id="8d497-113">Guide pratique pour Personnaliser des cellules et des colonnes dans le contrôle de DataGridView Windows Forms en étendant leur comportement et leur apparence</span><span class="sxs-lookup"><span data-stu-id="8d497-113">How to: Customize Cells and Columns in the Windows Forms DataGridView Control by Extending Their Behavior and Appearance</span></span>](customize-cells-and-columns-in-the-datagrid-by-extending-behavior.md)  
 <span data-ttu-id="8d497-114">Décrit comment créer des types personnalisés dérivés de `DataGridViewCell` et `DataGridViewColumn` afin de mettre en surbrillance les cellules lorsque le pointeur de la souris est placé dessus.</span><span class="sxs-lookup"><span data-stu-id="8d497-114">Describes how to create custom types derived from `DataGridViewCell` and `DataGridViewColumn` in order to highlight cells when the mouse pointer rests on them.</span></span>  
  
 [<span data-ttu-id="8d497-115">Guide pratique pour Désactiver les boutons d’une colonne de boutons dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-115">How to: Disable Buttons in a Button Column in the Windows Forms DataGridView Control</span></span>](disable-buttons-in-a-button-column-in-the-datagrid.md)  
 <span data-ttu-id="8d497-116">Décrit comment créer des types personnalisés dérivés de <xref:System.Windows.Forms.DataGridViewButtonCell> et <xref:System.Windows.Forms.DataGridViewButtonColumn> afin d’afficher les boutons désactivés dans une colonne de boutons.</span><span class="sxs-lookup"><span data-stu-id="8d497-116">Describes how to create custom types derived from <xref:System.Windows.Forms.DataGridViewButtonCell> and <xref:System.Windows.Forms.DataGridViewButtonColumn> in order to display disabled buttons in a button column.</span></span>  
  
 [<span data-ttu-id="8d497-117">Guide pratique pour Contrôles hôtes dans des cellules DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-117">How to: Host Controls in Windows Forms DataGridView Cells</span></span>](how-to-host-controls-in-windows-forms-datagridview-cells.md)  
 <span data-ttu-id="8d497-118">Décrit comment implémenter le `IDataGridViewEditingControl` interface et créer des types personnalisés dérivés de `DataGridViewCell` et `DataGridViewColumn` afin d’afficher un <xref:System.Windows.Forms.DateTimePicker> contrôler lorsqu’une cellule est en mode édition.</span><span class="sxs-lookup"><span data-stu-id="8d497-118">Describes how to implement the `IDataGridViewEditingControl` interface and create custom types derived from `DataGridViewCell` and `DataGridViewColumn` in order to display a <xref:System.Windows.Forms.DateTimePicker> control when a cell is in edit mode.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="8d497-119">Référence</span><span class="sxs-lookup"><span data-stu-id="8d497-119">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="8d497-120">Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="8d497-120">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewCell>  
 <span data-ttu-id="8d497-121">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewCell> classe.</span><span class="sxs-lookup"><span data-stu-id="8d497-121">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewCell> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewRow>  
 <span data-ttu-id="8d497-122">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewRow> classe.</span><span class="sxs-lookup"><span data-stu-id="8d497-122">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewRow> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewColumn>  
 <span data-ttu-id="8d497-123">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewColumn> classe.</span><span class="sxs-lookup"><span data-stu-id="8d497-123">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewColumn> class.</span></span>  
  
 <xref:System.Windows.Forms.IDataGridViewEditingControl>  
 <span data-ttu-id="8d497-124">Fournit la documentation de référence pour le <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.</span><span class="sxs-lookup"><span data-stu-id="8d497-124">Provides reference documentation for the <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="8d497-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d497-125">Related Sections</span></span>  
 [<span data-ttu-id="8d497-126">Mises en forme et styles de base dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-126">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="8d497-127">Fournit des rubriques qui décrivent comment modifier l'apparence de base du contrôle et le format d'affichage des données de cellules.</span><span class="sxs-lookup"><span data-stu-id="8d497-127">Provides topics that describe how to modify the basic appearance of the control and the display formatting of cell data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d497-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d497-128">See also</span></span>
- [<span data-ttu-id="8d497-129">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="8d497-129">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="8d497-130">Types de colonnes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8d497-130">Column Types in the Windows Forms DataGridView Control</span></span>](column-types-in-the-windows-forms-datagridview-control.md)
