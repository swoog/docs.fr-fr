---
title: 'Procédure : Activer la réorganisation des colonnes dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], column order
- data grids [Windows Forms], reordering columns
- columns [Windows Forms], reordering
ms.assetid: cc20eae3-e4db-493f-95ce-a4215e29472a
ms.openlocfilehash: 3aff0b0262441fb6c9d24240b1fe1c24707f94b8
ms.sourcegitcommit: 07c4368273b446555cb2c85397ea266b39d5fe50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56584250"
---
# <a name="how-to-enable-column-reordering-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="11cce-102">Procédure : Activer la réorganisation des colonnes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="11cce-102">How to: Enable Column Reordering in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="11cce-103">Quand vous activez la réorganisation des colonnes dans le contrôle <xref:System.Windows.Forms.DataGridView>, les utilisateurs peuvent déplacer une colonne vers une nouvelle position en faisant glisser l'en-tête de colonne avec la souris.</span><span class="sxs-lookup"><span data-stu-id="11cce-103">When you enable column reordering in the <xref:System.Windows.Forms.DataGridView> control, users can move a column to a new position by dragging the column header with the mouse.</span></span> <span data-ttu-id="11cce-104">Dans le contrôle <xref:System.Windows.Forms.DataGridView>, la valeur de propriété <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> détermine si les utilisateurs peuvent déplacer des colonnes vers d'autres positions.</span><span class="sxs-lookup"><span data-stu-id="11cce-104">In the <xref:System.Windows.Forms.DataGridView> control, the <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> property value determines whether users can move columns to different positions.</span></span>  
  
 <span data-ttu-id="11cce-105">Cette tâche est prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="11cce-105">There is support for this task in Visual Studio.</span></span>  <span data-ttu-id="11cce-106">Voir également [Guide pratique pour Activer la réorganisation des colonnes dans les Windows Forms DataGridView Control à l’aide du concepteur](enable-column-reordering-in-the-datagrid-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="11cce-106">Also see [How to: Enable Column Reordering in the Windows Forms DataGridView Control Using the Designer](enable-column-reordering-in-the-datagrid-using-the-designer.md).</span></span>  
  
### <a name="to-enable-column-reordering-programmatically"></a><span data-ttu-id="11cce-107">Pour activer la réorganisation des colonnes par programmation</span><span class="sxs-lookup"><span data-stu-id="11cce-107">To enable column reordering programmatically</span></span>  
  
-   <span data-ttu-id="11cce-108">Affectez à la propriété <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="11cce-108">Set the <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType> property to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#060](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#060)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#060](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#060)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="11cce-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="11cce-109">Compiling the Code</span></span>  
 <span data-ttu-id="11cce-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="11cce-110">This example requires:</span></span>  
  
-   <span data-ttu-id="11cce-111">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="11cce-111">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="11cce-112">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="11cce-112">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11cce-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11cce-113">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.AllowUserToOrderColumns%2A?displayProperty=nameWithType>
- [<span data-ttu-id="11cce-114">Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="11cce-114">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)
- [<span data-ttu-id="11cce-115">Guide pratique pour Figer des colonnes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="11cce-115">How to: Freeze Columns in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-freeze-columns-in-the-windows-forms-datagridview-control.md)
