---
title: Tri des données dans le contrôle Windows Forms DataGridView
ms.date: 02/13/2018
helpviewer_keywords:
- data [Windows Forms], sorting in grids
- data grids [Windows Forms], sorting data
- DataGridView control [Windows Forms], sorting data
ms.assetid: c1d4f24c-d961-4181-809d-5a5caa6122e4
ms.openlocfilehash: 606ffc7bd6136b775adaaaa79cf5042cf1e2dd70
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012145"
---
# <a name="sorting-data-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="3847b-102">Tri des données dans le contrôle Windows Forms DataGridView</span><span class="sxs-lookup"><span data-stu-id="3847b-102">Sorting data in the Windows Forms DataGridView control</span></span>

<span data-ttu-id="3847b-103">Par défaut, les utilisateurs peuvent trier les données dans un <xref:System.Windows.Forms.DataGridView> contrôle en cliquant sur l’en-tête d’une colonne de zone de texte (ou en appuyant sur F3 lorsqu’une cellule de zone de texte a le focus sur .NET Framework 4.7.2 et versions ultérieures).</span><span class="sxs-lookup"><span data-stu-id="3847b-103">By default, users can sort the data in a <xref:System.Windows.Forms.DataGridView> control by clicking the header of a text box column (or by pressing F3 when a text box cell is focused on .NET Framework 4.7.2 and later versions).</span></span> <span data-ttu-id="3847b-104">Vous pouvez modifier le <xref:System.Windows.Forms.DataGridViewColumn.SortMode> propriété des colonnes spécifiques pour permettre aux utilisateurs de trier par d’autres types de colonne lorsqu’il est judicieux de le faire.</span><span class="sxs-lookup"><span data-stu-id="3847b-104">You can modify the <xref:System.Windows.Forms.DataGridViewColumn.SortMode> property of specific columns to allow users to sort by other column types when it makes sense to do so.</span></span> <span data-ttu-id="3847b-105">Vous pouvez également trier les données par programme en n’importe quelle colonne, ou en plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="3847b-105">You can also sort the data programmatically by any column, or by multiple columns.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3847b-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3847b-106">In this section</span></span>

[<span data-ttu-id="3847b-107">Modes de tri des colonnes du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3847b-107">Column Sort Modes in the Windows Forms DataGridView Control</span></span>](column-sort-modes-in-the-windows-forms-datagridview-control.md)  
<span data-ttu-id="3847b-108">Décrit les options de tri des données dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="3847b-108">Describes the options for sorting data in the control.</span></span>

[<span data-ttu-id="3847b-109">Guide pratique pour Définir les Modes de tri des colonnes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3847b-109">How to: Set the Sort Modes for Columns in the Windows Forms DataGridView Control</span></span>](set-the-sort-modes-for-columns-wf-datagridview-control.md)  
<span data-ttu-id="3847b-110">Explique comment permettre aux utilisateurs de trier les colonnes qui ne sont pas pouvant être triées par défaut.</span><span class="sxs-lookup"><span data-stu-id="3847b-110">Describes how to enable users to sort by columns that are not sortable by default.</span></span>

[<span data-ttu-id="3847b-111">Guide pratique pour Personnaliser le tri dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3847b-111">How to: Customize Sorting in the Windows Forms DataGridView Control</span></span>](how-to-customize-sorting-in-the-windows-forms-datagridview-control.md)  
<span data-ttu-id="3847b-112">Décrit comment trier les données par programme et comment personnaliser le tri à l’aide de la <xref:System.Windows.Forms.DataGridView.SortCompare?displayProperty=nameWithType> événement ou en implémentant le <xref:System.Collections.IComparer> interface.</span><span class="sxs-lookup"><span data-stu-id="3847b-112">Describes how to sort data programmatically and how to customize sorting by using the <xref:System.Windows.Forms.DataGridView.SortCompare?displayProperty=nameWithType> event or by implementing the <xref:System.Collections.IComparer> interface.</span></span>

## <a name="reference"></a><span data-ttu-id="3847b-113">Référence</span><span class="sxs-lookup"><span data-stu-id="3847b-113">Reference</span></span>

<xref:System.Windows.Forms.DataGridView>  
<span data-ttu-id="3847b-114">Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="3847b-114">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  

<xref:System.Windows.Forms.DataGridView.Sort%2A?displayProperty=nameWithType>  
<span data-ttu-id="3847b-115">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.Sort%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3847b-115">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.Sort%2A> method.</span></span>

<xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType>  
<span data-ttu-id="3847b-116">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="3847b-116">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> property.</span></span>

<xref:System.Windows.Forms.DataGridViewColumnSortMode>  
<span data-ttu-id="3847b-117">Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridViewColumnSortMode> énumération.</span><span class="sxs-lookup"><span data-stu-id="3847b-117">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewColumnSortMode> enumeration.</span></span>

## <a name="see-also"></a><span data-ttu-id="3847b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3847b-118">See also</span></span>

- [<span data-ttu-id="3847b-119">DataGridView, contrôle</span><span class="sxs-lookup"><span data-stu-id="3847b-119">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="3847b-120">Types de colonnes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3847b-120">Column Types in the Windows Forms DataGridView Control</span></span>](column-types-in-the-windows-forms-datagridview-control.md)
