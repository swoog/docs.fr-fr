---
title: 'Procédure : mettre les colonnes en lecture seule dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], read-only columns
- DataGridView control [Windows Forms], read-only columns
ms.assetid: 2bb73ebb-1a55-4362-9fda-e50574c087d5
ms.openlocfilehash: 2a4ca0a718373c56f77e8f3c45a9d6ee6d76a081
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59171923"
---
# <a name="how-to-make-columns-read-only-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="59134-102">Procédure : mettre les colonnes en lecture seule dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="59134-102">How to: Make Columns Read-Only in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="59134-103">Toutes les données ne sont pas censées être modifiées.</span><span class="sxs-lookup"><span data-stu-id="59134-103">Not all data is meant for editing.</span></span> <span data-ttu-id="59134-104">Dans le contrôle <xref:System.Windows.Forms.DataGridView>, la valeur de propriété de la colonne <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> détermine si les utilisateurs peuvent modifier des cellules dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="59134-104">In the <xref:System.Windows.Forms.DataGridView> control, the column <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> property value determines whether users can edit cells in that column.</span></span> <span data-ttu-id="59134-105">Pour plus d’informations sur la façon de rendre le contrôle entièrement en lecture seule, consultez [Comment : Empêcher l’ajout de ligne et de suppression dans les Windows Forms DataGridView Control](prevent-row-addition-and-deletion-datagridview.md).</span><span class="sxs-lookup"><span data-stu-id="59134-105">For information about how to make the control entirely read-only, see [How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control](prevent-row-addition-and-deletion-datagridview.md).</span></span>  
  
 <span data-ttu-id="59134-106">Cette tâche est prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="59134-106">There is support for this task in Visual Studio.</span></span>  <span data-ttu-id="59134-107">Voir également [Guide pratique pour Définir une colonne en lecture seule dans les Windows Forms DataGridView Control à l’aide du concepteur](make-columns-read-only-in-the-datagrid-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="59134-107">Also see [How to: Make Columns Read-Only in the Windows Forms DataGridView Control Using the Designer](make-columns-read-only-in-the-datagrid-using-the-designer.md).</span></span>  
  
### <a name="to-make-a-column-read-only-programmatically"></a><span data-ttu-id="59134-108">Pour configurer une colonne en lecture seule par programmation</span><span class="sxs-lookup"><span data-stu-id="59134-108">To make a column read-only programmatically</span></span>  
  
-   <span data-ttu-id="59134-109">Affectez à la propriété <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="59134-109">Set the <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType> property to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#064](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#064)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#064](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#064)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="59134-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="59134-110">Compiling the Code</span></span>  
 <span data-ttu-id="59134-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="59134-111">This example requires:</span></span>  
  
-   <span data-ttu-id="59134-112">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` avec une colonne nommée `CompanyName` ;</span><span class="sxs-lookup"><span data-stu-id="59134-112">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1` with a column named `CompanyName`.</span></span>  
  
-   <span data-ttu-id="59134-113">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="59134-113">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59134-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59134-114">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.Columns%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType>
- [<span data-ttu-id="59134-115">Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="59134-115">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](basic-column-row-and-cell-features-wf-datagridview-control.md)
- [<span data-ttu-id="59134-116">Procédure : empêcher l’ajout et la suppression de lignes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="59134-116">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control</span></span>](prevent-row-addition-and-deletion-datagridview.md)
