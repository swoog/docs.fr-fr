---
title: Sélection et utilisation du Presse-papiers avec le contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], Clipboard use
- cells [Windows Forms], selecting in grids
- Clipboard [Windows Forms], in DataGridView control
- selection [Windows Forms], in DataGridView control
- data grids [Windows Forms], selecting cells
- DataGridView control [Windows Forms], selecting cells
ms.assetid: 82cffcad-8b30-4897-bddb-c3a79d751b83
ms.openlocfilehash: c777366124a3cc5f43df8efca54fc366245bcb75
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33537640"
---
# <a name="selection-and-clipboard-use-with-the-windows-forms-datagridview-control"></a><span data-ttu-id="2a443-102">Sélection et utilisation du Presse-papiers avec le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2a443-102">Selection and Clipboard Use with the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="2a443-103">Le `DataGridView` contrôle vous fournit une vaste gamme d’options pour configurer la façon dont les utilisateurs peuvent sélectionner des cellules, lignes et colonnes.</span><span class="sxs-lookup"><span data-stu-id="2a443-103">The `DataGridView` control provides you with a variety of options for configuring how users can select cells, rows, and columns.</span></span> <span data-ttu-id="2a443-104">Par exemple, vous pouvez activer une ou plusieurs de sélection, la sélection de lignes entières ou des colonnes lorsque les utilisateurs cliquent sur des cellules ou de lignes entières ou des colonnes uniquement lorsque les utilisateurs cliquent sur leurs en-têtes, ce qui permet la sélection de la cellule.</span><span class="sxs-lookup"><span data-stu-id="2a443-104">For example, you can enable single or multiple selection, selection of whole rows or columns when users click cells, or selection of whole rows or columns only when users click their headers, which enables cell selection as well.</span></span> <span data-ttu-id="2a443-105">Si vous souhaitez fournir votre propre interface utilisateur pour la sélection, vous pouvez désactiver la sélection ordinaire et gérer toute la sélection par programme.</span><span class="sxs-lookup"><span data-stu-id="2a443-105">If you want to provide your own user interface for selection, you can disable ordinary selection and handle all selection programmatically.</span></span> <span data-ttu-id="2a443-106">En outre, vous pouvez activer les utilisateurs peuvent copier les valeurs sélectionnées dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="2a443-106">Additionally, you can enable users to copy the selected values to the Clipboard.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2a443-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2a443-107">In This Section</span></span>  
 [<span data-ttu-id="2a443-108">Modes de sélection dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2a443-108">Selection Modes in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/selection-modes-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="2a443-109">Décrit les options pour l’utilisateur et de la sélection par programmation dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="2a443-109">Describes the options for user and programmatic selection in the control.</span></span>  
  
 [<span data-ttu-id="2a443-110">Guide pratique pour définir le mode de sélection du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2a443-110">How to: Set the Selection Mode of the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-the-selection-mode-of-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="2a443-111">Décrit comment configurer le contrôle de sélection de ligne seule lorsqu’un utilisateur clique sur une cellule.</span><span class="sxs-lookup"><span data-stu-id="2a443-111">Describes how to configure the control for single-row selection when a user clicks a cell.</span></span>  
  
 [<span data-ttu-id="2a443-112">Guide pratique pour obtenir les cellules, lignes et colonnes sélectionnées dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2a443-112">How to: Get the Selected Cells, Rows, and Columns in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/selected-cells-rows-and-columns-datagridview.md)  
 <span data-ttu-id="2a443-113">Décrit comment travailler avec les collections de cellules, lignes et colonnes sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="2a443-113">Describes how to work with the selected cell, row, and column collections.</span></span>  
  
 [<span data-ttu-id="2a443-114">Guide pratique pour permettre aux utilisateurs de copier plusieurs cellules dans le Presse-papiers à partir du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2a443-114">How to: Enable Users to Copy Multiple Cells to the Clipboard from the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/enable-users-to-copy-multiple-cells-to-the-clipboard-datagridview.md)  
 <span data-ttu-id="2a443-115">Décrit comment activer la prise en charge du Presse-papiers dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="2a443-115">Describes how to enable Clipboard support in the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="2a443-116">Référence</span><span class="sxs-lookup"><span data-stu-id="2a443-116">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="2a443-117">Fournit la documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="2a443-117">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType>  
 <span data-ttu-id="2a443-118">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.SelectionMode%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="2a443-118">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.SelectionMode%2A> property.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.ClipboardCopyMode%2A>  
 <span data-ttu-id="2a443-119">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.ClipboardCopyMode%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="2a443-119">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.ClipboardCopyMode%2A> property.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewSelectedCellCollection>  
 <span data-ttu-id="2a443-120">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewSelectedCellCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="2a443-120">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewSelectedCellCollection> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewSelectedRowCollection>  
 <span data-ttu-id="2a443-121">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewSelectedRowCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="2a443-121">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewSelectedRowCollection> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewSelectedColumnCollection>  
 <span data-ttu-id="2a443-122">Fournit la documentation de référence pour la <xref:System.Windows.Forms.DataGridViewSelectedColumnCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="2a443-122">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewSelectedColumnCollection> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a443-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a443-123">See Also</span></span>  
 [<span data-ttu-id="2a443-124">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="2a443-124">DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)  
 [<span data-ttu-id="2a443-125">Gestion par défaut du clavier et de la souris dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2a443-125">Default Keyboard and Mouse Handling in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/default-keyboard-and-mouse-handling-in-the-windows-forms-datagridview-control.md)
