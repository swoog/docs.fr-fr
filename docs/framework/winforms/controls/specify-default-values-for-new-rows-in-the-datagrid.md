---
title: 'Procédure : Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data grids [Windows Forms], default values for new rows
- DataGridView control [Windows Forms], data entry
- rows [Windows Forms], specifying default values
- DataGridView control [Windows Forms], default values for new rows
ms.assetid: 8d127963-d9f8-4e4e-9f7f-beb66688f1f2
ms.openlocfilehash: cc854f0cdbef8373b74a16c7d5bc044cfee5aa84
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57708026"
---
# <a name="how-to-specify-default-values-for-new-rows-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="5dda8-102">Procédure : Spécifiez les valeurs par défaut pour les nouvelles lignes dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5dda8-102">How to: Specify Default Values for New Rows in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="5dda8-103">Vous pouvez rendre saisie de données plus pratique lorsque l’application remplit par défaut des valeurs pour les nouvelles lignes ajoutées.</span><span class="sxs-lookup"><span data-stu-id="5dda8-103">You can make data entry more convenient when the application fills in default values for newly added rows.</span></span> <span data-ttu-id="5dda8-104">Avec le <xref:System.Windows.Forms.DataGridView> (classe), vous pouvez remplir dans valeurs par défaut avec le <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> événement.</span><span class="sxs-lookup"><span data-stu-id="5dda8-104">With the <xref:System.Windows.Forms.DataGridView> class, you can fill in default values with the <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> event.</span></span> <span data-ttu-id="5dda8-105">Cet événement est déclenché lorsque l’utilisateur entre la ligne pour les nouveaux enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5dda8-105">This event is raised when the user enters the row for new records.</span></span> <span data-ttu-id="5dda8-106">Lorsque votre code gère cet événement, vous pouvez remplir des cellules souhaitées avec des valeurs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="5dda8-106">When your code handles this event, you can populate desired cells with values of your choosing.</span></span>  
  
 <span data-ttu-id="5dda8-107">L’exemple de code suivant montre comment spécifier des valeurs par défaut pour les nouvelles lignes à l’aide de la <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> événement.</span><span class="sxs-lookup"><span data-stu-id="5dda8-107">The following code example demonstrates how to specify default values for new rows using the <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5dda8-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="5dda8-108">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#120](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#120)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#120](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#120)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5dda8-109">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="5dda8-109">Compiling the Code</span></span>  
 <span data-ttu-id="5dda8-110">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="5dda8-110">This example requires:</span></span>  
  
-   <span data-ttu-id="5dda8-111">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="5dda8-111">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="5dda8-112">Un `NewCustomerId` fonction permettant de générer unique `CustomerID` valeurs.</span><span class="sxs-lookup"><span data-stu-id="5dda8-112">A `NewCustomerId` function for generating unique `CustomerID` values.</span></span>  
  
-   <span data-ttu-id="5dda8-113">des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="5dda8-113">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5dda8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dda8-114">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded?displayProperty=nameWithType>
- [<span data-ttu-id="5dda8-115">Saisie de données dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5dda8-115">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="5dda8-116">Utilisation de la ligne pour les nouveaux enregistrements dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5dda8-116">Using the Row for New Records in the Windows Forms DataGridView Control</span></span>](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
