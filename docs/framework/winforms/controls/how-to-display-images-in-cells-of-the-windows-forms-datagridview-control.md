---
title: 'Procédure : Afficher des Images dans les cellules du contrôle DataGridView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cells [Windows Forms], displaying images
- data grids [Windows Forms], displaying in grids
- DataGridView control [Windows Forms], displaying images
- data grids [Windows Forms], displaying images in cells
ms.assetid: 53b13d31-1b56-476d-9ab4-18bfac138a22
ms.openlocfilehash: 280f274a0957f098add7fbf2e3b919c33c4c5233
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704400"
---
# <a name="how-to-display-images-in-cells-of-the-windows-forms-datagridview-control"></a><span data-ttu-id="ca934-102">Procédure : Afficher des Images dans les cellules du contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca934-102">How to: Display Images in Cells of the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="ca934-103">Une image ou un graphique est une des valeurs que vous pouvez afficher dans une ligne de données.</span><span class="sxs-lookup"><span data-stu-id="ca934-103">A picture or graphic is one of the values that you can display in a row of data.</span></span> <span data-ttu-id="ca934-104">Souvent, ces graphiques prennent la forme d’une photographie de salarié ou un logo de société.</span><span class="sxs-lookup"><span data-stu-id="ca934-104">Frequently, these graphics take the form of an employee's photograph or a company logo.</span></span>  
  
 <span data-ttu-id="ca934-105">Incorporation d’images est simple lorsque vous affichez des données dans le <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ca934-105">Incorporating pictures is simple when you display data within the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="ca934-106">Le <xref:System.Windows.Forms.DataGridView> contrôle gère en mode natif n’importe quel format d’image pris en charge par le <xref:System.Drawing.Image> classe, ainsi que le OLE image format utilisé par certaines bases de données.</span><span class="sxs-lookup"><span data-stu-id="ca934-106">The <xref:System.Windows.Forms.DataGridView> control natively handles any image format supported by the <xref:System.Drawing.Image> class, as well as the OLE picture format used by some databases.</span></span>  
  
 <span data-ttu-id="ca934-107">Si le <xref:System.Windows.Forms.DataGridView> source de données du contrôle a une colonne d’images, ils seront affichés automatiquement par le <xref:System.Windows.Forms.DataGridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ca934-107">If the <xref:System.Windows.Forms.DataGridView> control's data source has a column of images, they will be displayed automatically by the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <span data-ttu-id="ca934-108">L’exemple de code suivant montre comment extraire une icône d’une ressource incorporée et la convertir en une image bitmap à afficher dans chaque cellule d’une colonne image.</span><span class="sxs-lookup"><span data-stu-id="ca934-108">The following code example demonstrates how to extract an icon from an embedded resource and convert it to a bitmap for display in every cell of an image column.</span></span> <span data-ttu-id="ca934-109">Pour un autre exemple qui remplace les valeurs de cellules textuelles avec images correspondantes, consultez [Comment : Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).</span><span class="sxs-lookup"><span data-stu-id="ca934-109">For another example that replaces textual cell values with corresponding images, see [How to: Customize Data Formatting in the Windows Forms DataGridView Control](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ca934-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="ca934-110">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#050](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#050)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#050](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#050)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ca934-111">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="ca934-111">Compiling the Code</span></span>  
 <span data-ttu-id="ca934-112">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="ca934-112">This example requires:</span></span>  
  
-   <span data-ttu-id="ca934-113">un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;</span><span class="sxs-lookup"><span data-stu-id="ca934-113">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="ca934-114">Une ressource d’icône incorporée nommée `tree.ico`.</span><span class="sxs-lookup"><span data-stu-id="ca934-114">An embedded icon resource named `tree.ico`.</span></span>  
  
-   <span data-ttu-id="ca934-115">des références aux assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType> et <xref:System.Drawing?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ca934-115">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, and <xref:System.Drawing?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca934-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca934-116">See also</span></span>
- <xref:System.Windows.Forms.DataGridView>
- [<span data-ttu-id="ca934-117">Fonctionnalités de base liées aux colonnes, lignes et cellules dans le contrôle DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca934-117">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](basic-column-row-and-cell-features-wf-datagridview-control.md)
- [<span data-ttu-id="ca934-118">Guide pratique pour Personnaliser la mise en forme des données dans le contrôle de DataGridView Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca934-118">How to: Customize Data Formatting in the Windows Forms DataGridView Control</span></span>](how-to-customize-data-formatting-in-the-windows-forms-datagridview-control.md)
