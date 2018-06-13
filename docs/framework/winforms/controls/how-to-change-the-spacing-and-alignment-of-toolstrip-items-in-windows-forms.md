---
title: "Comment : modifier l'espacement et l'alignement d'éléments ToolStrip dans les Windows Forms"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], aligning items
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], aligning items
ms.assetid: cd483466-0f49-43df-addf-e2b5fcd64027
ms.openlocfilehash: 7951a545fd8cbd0ae30907922551216161171a8d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33531262"
---
# <a name="how-to-change-the-spacing-and-alignment-of-toolstrip-items-in-windows-forms"></a><span data-ttu-id="8e851-102">Comment : modifier l'espacement et l'alignement d'éléments ToolStrip dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8e851-102">How to: Change the Spacing and Alignment of ToolStrip Items in Windows Forms</span></span>
<span data-ttu-id="8e851-103">Le <xref:System.Windows.Forms.ToolStrip> contrôle prend entièrement en charge les fonctionnalités de disposition telles que le dimensionnement, l’espacement des <xref:System.Windows.Forms.ToolStripItem> contrôle entre eux, la disposition des contrôles sur le <xref:System.Windows.Forms.ToolStrip>et l’espacement des contrôles relatif à la <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="8e851-103">The <xref:System.Windows.Forms.ToolStrip> control fully supports layout features such as sizing, the spacing of <xref:System.Windows.Forms.ToolStripItem> controls relative to each other, the arrangement of controls on the <xref:System.Windows.Forms.ToolStrip>, and the spacing of controls relative to the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
 <span data-ttu-id="8e851-104">Étant donné que la valeur par défaut de la <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> propriété est `true`, les contrôles sont dimensionnés automatiquement, sauf si vous définissez la <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> propriété `false`.</span><span class="sxs-lookup"><span data-stu-id="8e851-104">Because the default value of the <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> property is `true`, controls are sized automatically unless you set the <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> property to `false`.</span></span>  
  
### <a name="to-manually-size-a-toolstripitem"></a><span data-ttu-id="8e851-105">Pour dimensionner manuellement un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="8e851-105">To manually size a ToolStripItem</span></span>  
  
1.  <span data-ttu-id="8e851-106">Définir le <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> propriété `false` pour le contrôle associé.</span><span class="sxs-lookup"><span data-stu-id="8e851-106">Set the <xref:System.Windows.Forms.ToolStripItem.AutoSize%2A> property to `false` for the associated control.</span></span>  
  
    ```vb  
    ToolStripButton1.AutoSize = False  
    ```  
  
    ```csharp  
    toolStripButton1.AutoSize = false;  
    ```  
  
2.  <span data-ttu-id="8e851-107">Définir le <xref:System.Windows.Forms.ToolStripItem.Size%2A> propriété comme vous le souhaitez pour associé <xref:System.Windows.Forms.ToolStripItem>.</span><span class="sxs-lookup"><span data-stu-id="8e851-107">Set the <xref:System.Windows.Forms.ToolStripItem.Size%2A> property the way you want for the associated <xref:System.Windows.Forms.ToolStripItem>.</span></span>  
  
### <a name="to-set-the-spacing-of-a-toolstripitem"></a><span data-ttu-id="8e851-108">Pour définir l’espacement d’un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="8e851-108">To set the spacing of a ToolStripItem</span></span>  
  
1.  <span data-ttu-id="8e851-109">Insérez les valeurs souhaitées, en pixels, dans le <xref:System.Windows.Forms.ToolStripItem.Margin%2A> propriété du contrôle associé.</span><span class="sxs-lookup"><span data-stu-id="8e851-109">Insert the desired values, in pixels, into the <xref:System.Windows.Forms.ToolStripItem.Margin%2A> property of the associated control.</span></span>  
  
     <span data-ttu-id="8e851-110">Les valeurs de la <xref:System.Windows.Forms.ToolStripItem.Margin%2A> propriété spécifient l’espacement entre l’élément et les éléments adjacents dans cet ordre : gauche, haut, droite et bas.</span><span class="sxs-lookup"><span data-stu-id="8e851-110">The values of the <xref:System.Windows.Forms.ToolStripItem.Margin%2A> property specify the spacing between the item and adjacent items in this order: Left, Top, Right, and Bottom.</span></span>  
  
    ```vb  
    ToolStripTextBox1.Margin = New System.Windows.Forms.Padding _  
        (3, 0, 3, 0)  
    ```  
  
    ```csharp  
    toolStripTextBox1.Margin = new System.Windows.Forms.Padding   
        (3, 0, 3, 0);  
    ```  
  
### <a name="to-align-a-toolstripitem-to-the-right-side-of-the-toolstrip"></a><span data-ttu-id="8e851-111">Pour aligner un ToolStripItem au côté droit du ToolStrip</span><span class="sxs-lookup"><span data-stu-id="8e851-111">To align a ToolStripItem to the right side of the ToolStrip</span></span>  
  
1.  <span data-ttu-id="8e851-112">Définir le <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> propriété <xref:System.Windows.Forms.ToolStripItemAlignment.Right> pour le contrôle associé.</span><span class="sxs-lookup"><span data-stu-id="8e851-112">Set the <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> property to <xref:System.Windows.Forms.ToolStripItemAlignment.Right> for the associated control.</span></span> <span data-ttu-id="8e851-113">Par défaut, <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> a la valeur <xref:System.Windows.Forms.ToolStripItemAlignment.Left>, qui aligne les contrôles sur le côté gauche de la <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="8e851-113">By default, <xref:System.Windows.Forms.ToolStripItem.Alignment%2A> is set to <xref:System.Windows.Forms.ToolStripItemAlignment.Left>, which aligns controls to the left side of the <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
    ```vb  
    ToolStripSplitButton1.Alignment = _  
        System.Windows.Forms.ToolStripItemAlignment.Right  
    ```  
  
    ```csharp  
    toolStripSplitButton1.Alignment =   
        System.Windows.Forms.ToolStripItemAlignment.Right;  
    ```  
  
### <a name="to-arrange-toolstrip-items-on-the-toolstrip"></a><span data-ttu-id="8e851-114">Pour organiser des éléments ToolStrip sur le ToolStrip</span><span class="sxs-lookup"><span data-stu-id="8e851-114">To arrange ToolStrip items on the ToolStrip</span></span>  
  
-   <span data-ttu-id="8e851-115">Définir le <xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A> à la valeur de propriété <xref:System.Windows.Forms.ToolStripLayoutStyle> souhaité.</span><span class="sxs-lookup"><span data-stu-id="8e851-115">Set the <xref:System.Windows.Forms.ToolStrip.LayoutStyle%2A> property to the value of <xref:System.Windows.Forms.ToolStripLayoutStyle> that you want.</span></span>  
  
    ```vb  
    ToolStripDropDown1.LayoutStyle = _  
        System.Windows.Forms.ToolStripLayoutStyle.Flow  
    ```  
  
    ```csharp  
    toolStripDropDown1.LayoutStyle =   
        System.Windows.Forms.ToolStripLayoutStyle.Flow;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="8e851-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e851-116">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.Control.Layout>  
 <xref:System.Windows.Forms.ToolStrip.LayoutCompleted>  
 <xref:System.Windows.Forms.ToolStrip.LayoutSettings%2A>  
 <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A>  
 <xref:System.Windows.Forms.ToolStripItem.Placement%2A>  
 <xref:System.Windows.Forms.ToolStrip.CanOverflow%2A>  
 [<span data-ttu-id="8e851-117">Vue d’ensemble du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="8e851-117">ToolStrip Control Overview</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)  
 [<span data-ttu-id="8e851-118">Architecture du contrôle ToolStrip</span><span class="sxs-lookup"><span data-stu-id="8e851-118">ToolStrip Control Architecture</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-architecture.md)  
 [<span data-ttu-id="8e851-119">Résumé de la technologie ToolStrip</span><span class="sxs-lookup"><span data-stu-id="8e851-119">ToolStrip Technology Summary</span></span>](../../../../docs/framework/winforms/controls/toolstrip-technology-summary.md)
