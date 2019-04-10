---
title: 'Procédure : aligner un contrôle sur les bords des formulaires au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: 8ca6fd64edbd73301fd298f42c3d4d97d021888a
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59331860"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a><span data-ttu-id="8aa1c-102">Procédure : aligner un contrôle sur les bords des formulaires au moment du design</span><span class="sxs-lookup"><span data-stu-id="8aa1c-102">How to: Align a Control to the Edges of Forms at Design Time</span></span>
<span data-ttu-id="8aa1c-103">Vous pouvez aligner un contrôle sur le bord de vos formulaires en définissant le <xref:System.Windows.Forms.Control.Dock%2A>.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-103">You can make your control align to the edge of your forms by setting the <xref:System.Windows.Forms.Control.Dock%2A>.</span></span> <span data-ttu-id="8aa1c-104">Cette propriété désigne l’emplacement de votre contrôle dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-104">This property designates where your control resides in the form.</span></span> <span data-ttu-id="8aa1c-105">La propriété <xref:System.Windows.Forms.Control.Dock%2A> peut avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8aa1c-105">The <xref:System.Windows.Forms.Control.Dock%2A> property can be set to the following values:</span></span>  
  
|<span data-ttu-id="8aa1c-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8aa1c-106">Setting</span></span>|<span data-ttu-id="8aa1c-107">Effet sur le contrôle</span><span class="sxs-lookup"><span data-stu-id="8aa1c-107">Effect on your control</span></span>|  
|-------------|----------------------------|  
|<xref:System.Windows.Forms.DockStyle.Bottom>|<span data-ttu-id="8aa1c-108">S'ancre en bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-108">Docks to the bottom of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Fill>|<span data-ttu-id="8aa1c-109">Remplit tout l'espace restant dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-109">Fills all remaining space in the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Left>|<span data-ttu-id="8aa1c-110">S'ancre sur le côté gauche du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-110">Docks to the left side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.None>|<span data-ttu-id="8aa1c-111">Ne s’ancre en tout lieu et il s’affiche à l’emplacement spécifié par son <xref:System.Windows.Forms.Control.Location%2A>.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-111">Does not dock anywhere, and it appears at the location specified by its <xref:System.Windows.Forms.Control.Location%2A>.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Right>|<span data-ttu-id="8aa1c-112">S'ancre sur le côté droit du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-112">Docks to the right side of the form.</span></span>|  
|<xref:System.Windows.Forms.DockStyle.Top>|<span data-ttu-id="8aa1c-113">S'ancre en haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-113">Docks to the top of the form.</span></span>|  
  
 <span data-ttu-id="8aa1c-114">Ces valeurs peuvent également être définies dans le code.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-114">These values can also be set in code.</span></span> <span data-ttu-id="8aa1c-115">Pour plus d'informations, voir [Procédure : Aligner un contrôle sur les bords des formulaires](how-to-align-a-control-to-the-edges-of-forms.md).</span><span class="sxs-lookup"><span data-stu-id="8aa1c-115">For more information, see [How to: Align a Control to the Edges of Forms](how-to-align-a-control-to-the-edges-of-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8aa1c-116">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-116">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="8aa1c-117">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="8aa1c-117">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="8aa1c-118">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="8aa1c-118">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-set-the-dock-property-for-your-control-at-design-time"></a><span data-ttu-id="8aa1c-119">Pour définir la propriété Dock de votre contrôle au moment du design</span><span class="sxs-lookup"><span data-stu-id="8aa1c-119">To set the Dock property for your control at design time</span></span>  
  
1. <span data-ttu-id="8aa1c-120">Dans le Concepteur Windows Forms, sélectionnez votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-120">In the Windows Forms Designer, select your control.</span></span>  
  
2. <span data-ttu-id="8aa1c-121">Dans le **propriétés** , cliquez sur la liste déroulante située en regard du <xref:System.Windows.Forms.Control.Dock%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-121">In the **Properties** window, click the drop-down box next to the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span>  
  
     <span data-ttu-id="8aa1c-122">Une interface graphique représentant les six possibles <xref:System.Windows.Forms.Control.Dock%2A> paramètres s’affiche.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-122">A graphical interface representing the six possible <xref:System.Windows.Forms.Control.Dock%2A> settings is displayed.</span></span>  
  
3. <span data-ttu-id="8aa1c-123">Choisissez le paramètre approprié.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-123">Choose the appropriate setting.</span></span>  
  
4. <span data-ttu-id="8aa1c-124">Votre contrôle s’ancre maintenant de la manière spécifiée par le paramètre.</span><span class="sxs-lookup"><span data-stu-id="8aa1c-124">Your control will now dock in the manner specified by the setting.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8aa1c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aa1c-125">See also</span></span>

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [<span data-ttu-id="8aa1c-126">Procédure : aligner un contrôle sur les bords des formulaires</span><span class="sxs-lookup"><span data-stu-id="8aa1c-126">How to: Align a Control to the Edges of Forms</span></span>](how-to-align-a-control-to-the-edges-of-forms.md)
- [<span data-ttu-id="8aa1c-127">Procédure pas à pas : organisation des contrôles dans des Windows Forms à l’aide de lignes d’alignement</span><span class="sxs-lookup"><span data-stu-id="8aa1c-127">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [<span data-ttu-id="8aa1c-128">Procédure : ancrer des contrôles dans des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="8aa1c-128">How to: Anchor Controls on Windows Forms</span></span>](how-to-anchor-controls-on-windows-forms.md)
- [<span data-ttu-id="8aa1c-129">Procédure : ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="8aa1c-129">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="8aa1c-130">Procédure : ancrer et arrimer des contrôles enfants dans un contrôle FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="8aa1c-130">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="8aa1c-131">Procédure pas à pas : organisation des contrôles dans Windows Forms à l’aide d’un TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="8aa1c-131">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [<span data-ttu-id="8aa1c-132">Procédure pas à pas : organisation des contrôles dans des Windows Forms à l’aide d’un FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="8aa1c-132">Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [<span data-ttu-id="8aa1c-133">Développement de contrôles Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="8aa1c-133">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
