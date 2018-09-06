---
title: 'Comment : définir une colonne en lecture seule dans le contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], read-only columns
- DataGridView control [Windows Forms], read-only columns
ms.assetid: 2bb73ebb-1a55-4362-9fda-e50574c087d5
ms.openlocfilehash: a8b5c0f9492941cf0e01e016d9fb097e1df44d2e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43731973"
---
# <a name="how-to-make-columns-read-only-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="eb876-102">Comment : définir une colonne en lecture seule dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb876-102">How to: Make Columns Read-Only in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="eb876-103">Toutes les données ne sont pas censées être modifiées.</span><span class="sxs-lookup"><span data-stu-id="eb876-103">Not all data is meant for editing.</span></span> <span data-ttu-id="eb876-104">Dans le contrôle <xref:System.Windows.Forms.DataGridView>, la valeur de propriété de la colonne <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> détermine si les utilisateurs peuvent modifier des cellules dans cette colonne.</span><span class="sxs-lookup"><span data-stu-id="eb876-104">In the <xref:System.Windows.Forms.DataGridView> control, the column <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> property value determines whether users can edit cells in that column.</span></span> <span data-ttu-id="eb876-105">Pour plus d’informations sur la façon de rendre le contrôle entièrement en lecture seule, consultez [Comment : empêcher l’ajout ligne et la suppression dans le contrôle de DataGridView Windows Forms](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-datagridview.md).</span><span class="sxs-lookup"><span data-stu-id="eb876-105">For information about how to make the control entirely read-only, see [How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-datagridview.md).</span></span>  
  
 <span data-ttu-id="eb876-106">Cette tâche est prise en charge dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="eb876-106">There is support for this task in Visual Studio.</span></span>  <span data-ttu-id="eb876-107">Consultez également [Comment : colonnes rendre en lecture seule dans les Windows Forms DataGridView contrôle à l’aide du concepteur](https://msdn.microsoft.com/library/xd4k3c7e\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="eb876-107">Also see [How to: Make Columns Read-Only in the Windows Forms DataGridView Control Using the Designer](https://msdn.microsoft.com/library/xd4k3c7e\(v=vs.110\)).</span></span>  
  
### <a name="to-make-a-column-read-only-programmatically"></a><span data-ttu-id="eb876-108">Pour configurer une colonne en lecture seule par programmation</span><span class="sxs-lookup"><span data-stu-id="eb876-108">To make a column read-only programmatically</span></span>  
  
-   <span data-ttu-id="eb876-109">Affectez à la propriété <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="eb876-109">Set the <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType> property to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#064](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#064)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#064](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#064)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="eb876-110">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="eb876-110">Compiling the Code</span></span>  
 <span data-ttu-id="eb876-111">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="eb876-111">This example requires:</span></span>  
  
-   <span data-ttu-id="eb876-112">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` avec une colonne nommée `CompanyName` ;</span><span class="sxs-lookup"><span data-stu-id="eb876-112">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1` with a column named `CompanyName`.</span></span>  
  
-   <span data-ttu-id="eb876-113">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="eb876-113">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb876-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb876-114">See Also</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView.Columns%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="eb876-115">Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb876-115">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)  
 [<span data-ttu-id="eb876-116">Guide pratique pour empêcher l'ajout et la suppression de lignes dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb876-116">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/prevent-row-addition-and-deletion-datagridview.md)
