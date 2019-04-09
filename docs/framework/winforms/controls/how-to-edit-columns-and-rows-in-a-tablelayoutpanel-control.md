---
title: 'Procédure : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel'
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor
helpviewer_keywords:
- columns [Windows Forms], editing
- TableLayoutPanel control [Windows Forms], editing
- rows [Windows Forms], editing
ms.assetid: c367ed43-40dc-49eb-9e0f-ba70e83dfec0
ms.openlocfilehash: eb194052ecd78d585f251789730a1f9855c509d9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201960"
---
# <a name="how-to-edit-columns-and-rows-in-a-tablelayoutpanel-control"></a><span data-ttu-id="51eae-102">Procédure : modifier des colonnes et des lignes dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="51eae-102">How to: Edit Columns and Rows in a TableLayoutPanel Control</span></span>
<span data-ttu-id="51eae-103">Vous pouvez utiliser l’éditeur de collections de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle, appelé le **Styles de ligne et colonne** boîte de dialogue pour modifier les lignes et colonnes de vos contrôles.</span><span class="sxs-lookup"><span data-stu-id="51eae-103">You can use the collection editor of the <xref:System.Windows.Forms.TableLayoutPanel> control, called the **Column and Row Styles** dialog box, to edit the rows and columns of your controls.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="51eae-104">Si vous souhaitez un contrôle pour s’étendre sur plusieurs lignes ou colonnes, définissez la `RowSpan` et `ColumnSpan` propriétés sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="51eae-104">If you want a control to span multiple rows or columns, set the `RowSpan` and `ColumnSpan` properties on the control.</span></span> <span data-ttu-id="51eae-105">Pour plus d’informations, consultez [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).</span><span class="sxs-lookup"><span data-stu-id="51eae-105">For more information, see [Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).</span></span>  
>   
>  <span data-ttu-id="51eae-106">Si vous souhaitez aligner un contrôle dans une cellule, ou si vous souhaitez un contrôle à étendre au sein d’une cellule, utilisez le contrôle <xref:System.Windows.Forms.Control.Anchor%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="51eae-106">If you want to align a control within a cell, or if you want a control to stretch within a cell, use the control's <xref:System.Windows.Forms.Control.Anchor%2A> property.</span></span> <span data-ttu-id="51eae-107">Pour plus d’informations, consultez [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).</span><span class="sxs-lookup"><span data-stu-id="51eae-107">For more information, see [Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).</span></span>  
>   
>  <span data-ttu-id="51eae-108">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="51eae-108">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="51eae-109">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="51eae-109">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="51eae-110">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="51eae-110">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-edit-rows-and-columns"></a><span data-ttu-id="51eae-111">Pour modifier les lignes et colonnes</span><span class="sxs-lookup"><span data-stu-id="51eae-111">To edit rows and columns</span></span>  
  
1.  <span data-ttu-id="51eae-112">Faites glisser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> de la **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="51eae-112">Drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>  
  
2.  <span data-ttu-id="51eae-113">Cliquez sur le <xref:System.Windows.Forms.TableLayoutPanel> glyphe de balise active du contrôle (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) et sélectionnez **modifier les lignes et colonnes** pour ouvrir le  **Styles de ligne et colonne** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="51eae-113">Click the <xref:System.Windows.Forms.TableLayoutPanel> control's smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) and select **Edit Rows and Columns** to open the **Column and Row Styles** dialog box.</span></span> <span data-ttu-id="51eae-114">Vous pouvez également avec le bouton droit sur le <xref:System.Windows.Forms.TableLayoutPanel> contrôler et sélectionnez **modifier les lignes et colonnes** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="51eae-114">You can also right click on the <xref:System.Windows.Forms.TableLayoutPanel> control and select **Edit Rows and Columns** from the shortcut menu.</span></span>  
  
3.  <span data-ttu-id="51eae-115">Pour ajouter ou supprimer des colonnes, sélectionnez **colonnes** à partir de la **type de membre** zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="51eae-115">To add or remove columns, select **Columns** from the **Member type** drop-down list box.</span></span>  
  
4.  <span data-ttu-id="51eae-116">Pour ajouter ou supprimer des lignes, sélectionnez **lignes** à partir de la **type de membre** zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="51eae-116">To add or remove rows, select **Rows** from the **Member type** drop-down list box.</span></span>  
  
5.  <span data-ttu-id="51eae-117">Cliquez sur le **ajouter** pour ajouter une ligne ou une colonne à la fin de la **membre** liste.</span><span class="sxs-lookup"><span data-stu-id="51eae-117">Click the **Add** button to add a row or column to the end of the **Member** list.</span></span>  
  
6.  <span data-ttu-id="51eae-118">Cliquez sur le **insérer** pour ajouter une ligne ou une colonne avant l’élément actuellement sélectionné dans la liste.</span><span class="sxs-lookup"><span data-stu-id="51eae-118">Click the **Insert** button to add a row or column before the currently selected item in the list.</span></span>  
  
7.  <span data-ttu-id="51eae-119">Si vous ajoutez une ligne ou colonne, sélectionnez le **taille Type** pour la nouvelle ligne ou la colonne.</span><span class="sxs-lookup"><span data-stu-id="51eae-119">If you are adding a row or column, select the **Size Type** for the new row or column.</span></span> <span data-ttu-id="51eae-120">Pour plus d'informations, consultez <xref:System.Windows.Forms.SizeType>.</span><span class="sxs-lookup"><span data-stu-id="51eae-120">For more information, see <xref:System.Windows.Forms.SizeType>.</span></span>  
  
8.  <span data-ttu-id="51eae-121">Pour supprimer une ligne ou colonne, cliquez sur le **supprimer** bouton pour supprimer l’élément actuellement sélectionné dans le **membre** liste.</span><span class="sxs-lookup"><span data-stu-id="51eae-121">To remove a row or column, click the **Remove** button to delete the currently selected item in the **Member** list.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51eae-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51eae-122">See also</span></span>

- <xref:System.Windows.Forms.SizeType>
- [<span data-ttu-id="51eae-123">TableLayoutPanel, contrôle</span><span class="sxs-lookup"><span data-stu-id="51eae-123">TableLayoutPanel Control</span></span>](tablelayoutpanel-control-windows-forms.md)
