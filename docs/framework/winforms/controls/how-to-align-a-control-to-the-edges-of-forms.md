---
title: 'Procédure : aligner un contrôle sur les bords des formulaires'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dock property [Windows Forms], aligning controls (using code)
- forms [Windows Forms], aligning controls
- controls [Windows Forms], aligning on forms
- custom controls [Windows Forms], docking using code
ms.assetid: 5994cb59-242b-4e75-bd0e-62879c34d702
ms.openlocfilehash: beb8881dbd2aedaefe66510c2942ce6c082b9729
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59329971"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms"></a><span data-ttu-id="3e1b1-102">Procédure : aligner un contrôle sur les bords des formulaires</span><span class="sxs-lookup"><span data-stu-id="3e1b1-102">How to: Align a Control to the Edges of Forms</span></span>
<span data-ttu-id="3e1b1-103">Vous pouvez aligner un contrôle sur le bord de vos formulaires en définissant la propriété <xref:System.Windows.Forms.Control.Dock%2A>.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-103">You can make your control align to the edge of your forms by setting the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span> <span data-ttu-id="3e1b1-104">Cette propriété désigne l’emplacement de votre contrôle dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-104">This property designates where your control resides in the form.</span></span> <span data-ttu-id="3e1b1-105">La propriété <xref:System.Windows.Forms.Control.Dock%2A> peut avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="3e1b1-105">The <xref:System.Windows.Forms.Control.Dock%2A> property can be set to the following values:</span></span>  
  
|<span data-ttu-id="3e1b1-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3e1b1-106">Setting</span></span>|<span data-ttu-id="3e1b1-107">Effet sur le contrôle</span><span class="sxs-lookup"><span data-stu-id="3e1b1-107">Effect on your control</span></span>|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|<span data-ttu-id="3e1b1-108">S'ancre en bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-108">Docks to the bottom of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Fill>|<span data-ttu-id="3e1b1-109">Remplit tout l'espace restant dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-109">Fills all remaining space in the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Left>|<span data-ttu-id="3e1b1-110">S'ancre sur le côté gauche du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-110">Docks to the left side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.None>|<span data-ttu-id="3e1b1-111">Ne s'ancre nulle part et apparaît à l'emplacement spécifié par sa propriété <xref:System.Windows.Forms.Control.Location%2A>.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-111">Does not dock anywhere, and it appears at the location specified by its <xref:System.Windows.Forms.Control.Location%2A> property.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Right>|<span data-ttu-id="3e1b1-112">S'ancre sur le côté droit du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-112">Docks to the right side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Top>|<span data-ttu-id="3e1b1-113">S'ancre en haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-113">Docks to the top of the form.</span></span>|  
  
 <span data-ttu-id="3e1b1-114">Cette fonctionnalité est prise en charge au moment du design dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-114">There is design-time support for this feature in Visual Studio.</span></span>  
  
### <a name="to-set-the-dock-property-for-your-control-at-run-time"></a><span data-ttu-id="3e1b1-115">Pour définir la propriété Dock de votre contrôle au moment de l'exécution</span><span class="sxs-lookup"><span data-stu-id="3e1b1-115">To set the Dock property for your control at run time</span></span>  
  
1. <span data-ttu-id="3e1b1-116">Affectez la valeur appropriée à la propriété <xref:System.Windows.Forms.Control.Dock%2A> dans le code.</span><span class="sxs-lookup"><span data-stu-id="3e1b1-116">Set the <xref:System.Windows.Forms.Control.Dock%2A> property to the appropriate value in code.</span></span>  
  
    ```vb  
    ' To set the Dock property internally.  
    Me.Dock = DockStyle.Top  
    ' To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top  
    ```  
  
    ```csharp  
    // To set the Dock property internally.  
    this.Dock = DockStyle.Top;  
    // To set the Dock property from another object.  
    UserControl1.Dock = DockStyle.Top;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="3e1b1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e1b1-117">See also</span></span>

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [<span data-ttu-id="3e1b1-118">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3e1b1-118">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="3e1b1-119">Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="3e1b1-119">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="3e1b1-120">Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="3e1b1-120">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="3e1b1-121">Vue d’ensemble de la propriété AutoSize</span><span class="sxs-lookup"><span data-stu-id="3e1b1-121">AutoSize Property Overview</span></span>](autosize-property-overview.md)
