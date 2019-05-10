---
title: 'Procédure : aligner un contrôle sur les bords des formulaires au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: b08e01eb9adb984a32a8fc435cf1f3b93b159a14
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65210381"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a><span data-ttu-id="c4dc5-102">Procédure : aligner un contrôle sur les bords des formulaires au moment du design</span><span class="sxs-lookup"><span data-stu-id="c4dc5-102">How to: Align a Control to the Edges of Forms at Design Time</span></span>

<span data-ttu-id="c4dc5-103">Vous pouvez aligner un contrôle sur le bord de vos formulaires en définissant la valeur de la <xref:System.Windows.Forms.Control.Dock%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-103">You can make your control align to the edge of your forms by setting the value of the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span> <span data-ttu-id="c4dc5-104">Cette propriété désigne l’emplacement de votre contrôle dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-104">This property designates where your control resides in the form.</span></span> <span data-ttu-id="c4dc5-105">La propriété <xref:System.Windows.Forms.Control.Dock%2A> peut avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4dc5-105">The <xref:System.Windows.Forms.Control.Dock%2A> property can be set to the following values:</span></span>

|<span data-ttu-id="c4dc5-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c4dc5-106">Setting</span></span>|<span data-ttu-id="c4dc5-107">Effet sur le contrôle</span><span class="sxs-lookup"><span data-stu-id="c4dc5-107">Effect on your control</span></span>|
|-------------|----------------------------|
|<xref:System.Windows.Forms.DockStyle.Bottom>|<span data-ttu-id="c4dc5-108">S'ancre en bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-108">Docks to the bottom of the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Fill>|<span data-ttu-id="c4dc5-109">Remplit tout l'espace restant dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-109">Fills all remaining space in the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Left>|<span data-ttu-id="c4dc5-110">S'ancre sur le côté gauche du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-110">Docks to the left side of the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.None>|<span data-ttu-id="c4dc5-111">Ne s’ancre en tout lieu et il s’affiche à l’emplacement spécifié par son <xref:System.Windows.Forms.Control.Location%2A>.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-111">Does not dock anywhere, and it appears at the location specified by its <xref:System.Windows.Forms.Control.Location%2A>.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Right>|<span data-ttu-id="c4dc5-112">S'ancre sur le côté droit du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-112">Docks to the right side of the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Top>|<span data-ttu-id="c4dc5-113">S'ancre en haut du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-113">Docks to the top of the form.</span></span>|

<span data-ttu-id="c4dc5-114">Ces valeurs peuvent également être définies dans le code.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-114">These values can also be set in code.</span></span> <span data-ttu-id="c4dc5-115">Pour plus d'informations, voir [Procédure : Aligner un contrôle sur les bords des formulaires](how-to-align-a-control-to-the-edges-of-forms.md).</span><span class="sxs-lookup"><span data-stu-id="c4dc5-115">For more information, see [How to: Align a Control to the Edges of Forms](how-to-align-a-control-to-the-edges-of-forms.md).</span></span>

## <a name="set-the-dock-property-for-your-control-at-design-time"></a><span data-ttu-id="c4dc5-116">Définir la propriété Dock de votre contrôle au moment du design</span><span class="sxs-lookup"><span data-stu-id="c4dc5-116">Set the Dock property for your control at design time</span></span>

1. <span data-ttu-id="c4dc5-117">Dans le Concepteur de formulaires Windows dans Visual Studio, sélectionnez votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-117">In the Windows Forms Designer in Visual Studio, select your control.</span></span>

2. <span data-ttu-id="c4dc5-118">Dans le **propriétés** , cliquez sur la liste déroulante située en regard du <xref:System.Windows.Forms.Control.Dock%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-118">In the **Properties** window, click the drop-down box next to the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span>

     <span data-ttu-id="c4dc5-119">Une interface graphique représentant les six possibles <xref:System.Windows.Forms.Control.Dock%2A> paramètres s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-119">A graphical interface representing the six possible <xref:System.Windows.Forms.Control.Dock%2A> settings is displayed.</span></span>

3. <span data-ttu-id="c4dc5-120">Choisissez le paramètre approprié.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-120">Choose the appropriate setting.</span></span>

4. <span data-ttu-id="c4dc5-121">Votre contrôle s’ancre maintenant de la manière spécifiée par le paramètre.</span><span class="sxs-lookup"><span data-stu-id="c4dc5-121">Your control will now dock in the manner specified by the setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="c4dc5-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4dc5-122">See also</span></span>

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [<span data-ttu-id="c4dc5-123">Guide pratique pour Aligner un contrôle sur les bords des formulaires</span><span class="sxs-lookup"><span data-stu-id="c4dc5-123">How to: Align a Control to the Edges of Forms</span></span>](how-to-align-a-control-to-the-edges-of-forms.md)
- [<span data-ttu-id="c4dc5-124">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement</span><span class="sxs-lookup"><span data-stu-id="c4dc5-124">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [<span data-ttu-id="c4dc5-125">Guide pratique pour Ancrer les contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c4dc5-125">How to: Anchor Controls on Windows Forms</span></span>](how-to-anchor-controls-on-windows-forms.md)
- [<span data-ttu-id="c4dc5-126">Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="c4dc5-126">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="c4dc5-127">Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="c4dc5-127">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="c4dc5-128">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="c4dc5-128">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [<span data-ttu-id="c4dc5-129">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide d’un FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="c4dc5-129">Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [<span data-ttu-id="c4dc5-130">Développement de contrôles Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="c4dc5-130">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
