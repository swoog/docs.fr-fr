---
title: 'Procédure pas à pas : organiser le contenu WPF dans Windows Forms au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- WPF user control [Windows Forms], hosting in a layout panel
- WPF content [Windows Forms], arranging at design time
- Windows Forms, arranging WPF content at design time
- WPF content [Windows Forms], hosting in Windows Forms
- Windows Forms, anchoring and docking WPF content
- interoperability [WPF]
ms.assetid: 5efb1c53-1484-43d6-aa8a-f4861b99bb8a
ms.openlocfilehash: a8f690438136450cb12dbcf5e17ddfcca617457e
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211445"
---
# <a name="walkthrough-arrange-wpf-content-on-windows-forms-at-design-time"></a><span data-ttu-id="50813-102">Procédure pas à pas : Organiser le contenu WPF sur les Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="50813-102">Walkthrough: Arrange WPF content on Windows Forms at design time</span></span>

<span data-ttu-id="50813-103">Cette procédure pas à pas montre comment utiliser les fonctionnalités de disposition Windows Forms, telles que l'ancrage et les lignes d'alignement, pour disposer les contrôles WPF (Windows Presentation Foundation).</span><span class="sxs-lookup"><span data-stu-id="50813-103">This walkthrough shows you how to use the Windows Forms layout features, such as anchoring and snaplines, to arrange Windows Presentation Foundation (WPF) controls.</span></span>

<span data-ttu-id="50813-104">Lors de cette procédure pas à pas, vous allez exécuter les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="50813-104">In this walkthrough, you perform the following tasks:</span></span>

- <span data-ttu-id="50813-105">créer le projet ;</span><span class="sxs-lookup"><span data-stu-id="50813-105">Create the project.</span></span>

- <span data-ttu-id="50813-106">créer le contrôle WPF ;</span><span class="sxs-lookup"><span data-stu-id="50813-106">Create the WPF control.</span></span>

- <span data-ttu-id="50813-107">héberger des contrôles WPF dans un panneau de disposition ;</span><span class="sxs-lookup"><span data-stu-id="50813-107">Host WPF controls in a layout panel.</span></span>

- <span data-ttu-id="50813-108">utiliser des lignes d'alignement pour aligner des contrôles WPF ;</span><span class="sxs-lookup"><span data-stu-id="50813-108">Use snaplines to align WPF controls.</span></span>

- <span data-ttu-id="50813-109">ancrer des contrôles WPF.</span><span class="sxs-lookup"><span data-stu-id="50813-109">Anchor and dock WPF controls.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="50813-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="50813-110">Prerequisites</span></span>

<span data-ttu-id="50813-111">Cette procédure pas à pas nécessite Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="50813-111">You need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="50813-112">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="50813-112">Create the project</span></span>

<span data-ttu-id="50813-113">Ouvrez Visual Studio et créez un nouveau projet d’Application de Windows Forms dans Visual Basic ou Visual C# nommé `ArrangeElementHost`.</span><span class="sxs-lookup"><span data-stu-id="50813-113">Open Visual Studio and create a new Windows Forms Application project in Visual Basic or Visual C# named `ArrangeElementHost`.</span></span>

> [!NOTE]
> <span data-ttu-id="50813-114">Lors de l'hébergement de contenu WPF, seuls les projets Visual Basic et C# sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="50813-114">When hosting WPF content, only C# and Visual Basic projects are supported.</span></span>

## <a name="create-the-wpf-control"></a><span data-ttu-id="50813-115">Créer le contrôle WPF</span><span class="sxs-lookup"><span data-stu-id="50813-115">Create the WPF control</span></span>

<span data-ttu-id="50813-116">Après avoir ajouté un contrôle WPF au projet, vous pouvez le disposer sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="50813-116">After you add a WPF control to the project, you can arrange it on the form.</span></span>

1. <span data-ttu-id="50813-117">Ajoutez un nouveau <xref:System.Windows.Controls.UserControl> WPF au projet.</span><span class="sxs-lookup"><span data-stu-id="50813-117">Add a new WPF <xref:System.Windows.Controls.UserControl> to the project.</span></span> <span data-ttu-id="50813-118">Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`.</span><span class="sxs-lookup"><span data-stu-id="50813-118">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="50813-119">Pour plus d’informations, consultez [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="50813-119">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>

2. <span data-ttu-id="50813-120">En mode Design, assurez-vous que `UserControl1` est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="50813-120">In Design view, make sure that `UserControl1` is selected.</span></span> <span data-ttu-id="50813-121">Pour plus d'informations, voir [Procédure : Sélectionner et déplacer des éléments sur l’aire de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="50813-121">For more information, see [How to: Select and Move Elements on the Design Surface](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).</span></span>

3. <span data-ttu-id="50813-122">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à `200`.</span><span class="sxs-lookup"><span data-stu-id="50813-122">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to `200`.</span></span>

4. <span data-ttu-id="50813-123">Affectez à la propriété <xref:System.Windows.Controls.Control.Background%2A> la valeur `Blue`.</span><span class="sxs-lookup"><span data-stu-id="50813-123">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to `Blue`.</span></span>

5. <span data-ttu-id="50813-124">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="50813-124">Build the project.</span></span>

## <a name="hosting-wpf-controls-in-a-layout-panel"></a><span data-ttu-id="50813-125">Hébergement de contrôles WPF dans un panneau de disposition</span><span class="sxs-lookup"><span data-stu-id="50813-125">Hosting WPF Controls in a Layout Panel</span></span>
 <span data-ttu-id="50813-126">Vous pouvez utiliser des contrôles WPF dans des panneaux de disposition de la même façon que vous utilisez d'autres contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="50813-126">You can use WPF controls in layout panels in the same way you use other Windows Forms controls.</span></span>

#### <a name="to-host-wpf-controls-in-a-layout-panel"></a><span data-ttu-id="50813-127">Pour héberger des contrôles WPF dans un panneau de disposition</span><span class="sxs-lookup"><span data-stu-id="50813-127">To host WPF controls in a layout panel</span></span>

1. <span data-ttu-id="50813-128">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="50813-128">Open `Form1` in the Windows Forms Designer.</span></span>

2. <span data-ttu-id="50813-129">Dans le **boîte à outils**, faites glisser un <xref:System.Windows.Forms.TableLayoutPanel> contrôle vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="50813-129">In the **Toolbox**, drag a <xref:System.Windows.Forms.TableLayoutPanel> control onto the form.</span></span>

3. <span data-ttu-id="50813-130">Sur le <xref:System.Windows.Forms.TableLayoutPanel> panneau des balises actives du contrôle, sélectionnez **supprimer la dernière ligne**.</span><span class="sxs-lookup"><span data-stu-id="50813-130">On the <xref:System.Windows.Forms.TableLayoutPanel> control's smart tag panel, select **Remove Last Row**.</span></span>

4. <span data-ttu-id="50813-131">Augmentez la largeur et la hauteur du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="50813-131">Resize the <xref:System.Windows.Forms.TableLayoutPanel> control to a larger width and height.</span></span>

5. <span data-ttu-id="50813-132">Dans le **boîte à outils**, double-cliquez sur `UserControl1` pour créer une instance de `UserControl1` dans la première cellule de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="50813-132">In the **Toolbox**, double-click `UserControl1` to create an instance of `UserControl1` in the first cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

     <span data-ttu-id="50813-133">L'instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="50813-133">The instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>

6. <span data-ttu-id="50813-134">Dans le **boîte à outils**, double-cliquez sur `UserControl1` pour créer une autre instance dans la deuxième cellule de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="50813-134">In the **Toolbox**, double-click `UserControl1` to create another instance in the second cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

7. <span data-ttu-id="50813-135">Dans le **structure du Document** fenêtre, sélectionnez `tableLayoutPanel1`.</span><span class="sxs-lookup"><span data-stu-id="50813-135">In the **Document Outline** window, select `tableLayoutPanel1`.</span></span> <span data-ttu-id="50813-136">Pour plus d’informations, consultez [fenêtre Structure du Document](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/46xf4h0w(v=vs.100)#using-the-document-outline-window-for-silverlight-and-wpf).</span><span class="sxs-lookup"><span data-stu-id="50813-136">For more information, see [Document Outline Window](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/46xf4h0w(v=vs.100)#using-the-document-outline-window-for-silverlight-and-wpf).</span></span>

8. <span data-ttu-id="50813-137">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Control.Padding%2A> propriété `10, 10, 10, 10`.</span><span class="sxs-lookup"><span data-stu-id="50813-137">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Control.Padding%2A> property to `10, 10, 10, 10`.</span></span>

     <span data-ttu-id="50813-138">Les deux contrôles <xref:System.Windows.Forms.Integration.ElementHost> sont redimensionnés pour s'adapter à la nouvelle disposition.</span><span class="sxs-lookup"><span data-stu-id="50813-138">Both <xref:System.Windows.Forms.Integration.ElementHost> controls are resized to fit into the new layout.</span></span>

## <a name="using-snaplines-to-align-wpf-controls"></a><span data-ttu-id="50813-139">Utilisation de lignes d'alignement pour aligner des contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="50813-139">Using Snaplines to Align WPF Controls</span></span>
 <span data-ttu-id="50813-140">Les lignes d'alignement permettent d'aligner facilement les contrôles sur un formulaire.</span><span class="sxs-lookup"><span data-stu-id="50813-140">Snaplines enable easy alignment of controls on a form.</span></span> <span data-ttu-id="50813-141">Vous pouvez aussi utiliser des lignes d'alignement pour aligner vos contrôles WPF.</span><span class="sxs-lookup"><span data-stu-id="50813-141">You can use snaplines to align your WPF controls as well.</span></span> <span data-ttu-id="50813-142">Pour plus d’informations, consultez [Procédure pas à pas : Organisation des contrôles dans les Windows Forms à l’aide des lignes d’alignement](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).</span><span class="sxs-lookup"><span data-stu-id="50813-142">For more information, see [Walkthrough: Arranging Controls on Windows Forms Using Snaplines](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).</span></span>

#### <a name="to-use-snaplines-to-align-wpf-controls"></a><span data-ttu-id="50813-143">Pour utiliser des lignes d'alignement pour aligner des contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="50813-143">To use snaplines to align WPF controls</span></span>

1. <span data-ttu-id="50813-144">À partir de la **boîte à outils**, faites glisser une instance de `UserControl1` vers le formulaire et placez-le dans l’espace sous le <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="50813-144">From the **Toolbox**, drag an instance of `UserControl1` onto the form and place it in the space beneath the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

     <span data-ttu-id="50813-145">L'instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost3`.</span><span class="sxs-lookup"><span data-stu-id="50813-145">The instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost3`.</span></span>

2. <span data-ttu-id="50813-146">À l'aide des lignes d'alignement, alignez le bord gauche de `elementHost3` avec le bord gauche du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="50813-146">Using snaplines, align the left edge of `elementHost3` with the left edge of <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

3. <span data-ttu-id="50813-147">À l'aide des lignes d'alignement, affectez à `elementHost3` la même largeur que celle du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="50813-147">Using snaplines, size `elementHost3` to the same width as the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

4. <span data-ttu-id="50813-148">Déplacez `elementHost3` vers le contrôle <xref:System.Windows.Forms.TableLayoutPanel> jusqu'à ce qu'une ligne d'alignement centrale apparaisse entre les contrôles.</span><span class="sxs-lookup"><span data-stu-id="50813-148">Move `elementHost3` toward the <xref:System.Windows.Forms.TableLayoutPanel> control until a center snapline appears between the controls.</span></span>

5. <span data-ttu-id="50813-149">Dans le **propriétés** fenêtre, définissez la valeur de la propriété de marge à `20, 20, 20, 20`.</span><span class="sxs-lookup"><span data-stu-id="50813-149">In the **Properties** window, set the value of the Margin property to `20, 20, 20, 20`.</span></span>

6. <span data-ttu-id="50813-150">Déplacez le `elementHost3` hors du contrôle <xref:System.Windows.Forms.TableLayoutPanel> jusqu'à ce que la ligne d'alignement centrale réapparaisse.</span><span class="sxs-lookup"><span data-stu-id="50813-150">Move the `elementHost3` away from the <xref:System.Windows.Forms.TableLayoutPanel> control until the center snapline appears again.</span></span> <span data-ttu-id="50813-151">La ligne d'alignement centrale indique maintenant une marge de 20.</span><span class="sxs-lookup"><span data-stu-id="50813-151">The center snapline now indicates a margin of 20.</span></span>

7. <span data-ttu-id="50813-152">Déplacez `elementHost3` vers la droite jusqu'à ce que son bord gauche soit aligné avec le bord gauche de `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="50813-152">Move `elementHost3` to the right, until its left edge aligns with the left edge of `elementHost1`.</span></span>

8. <span data-ttu-id="50813-153">Modifiez la largeur de `elementHost3` jusqu'à ce que son bord droit soit aligné avec le bord droit de `elementHost2`.</span><span class="sxs-lookup"><span data-stu-id="50813-153">Change the width of `elementHost3` until its right edge aligns with the right edge of `elementHost2`.</span></span>

## <a name="anchoring-and-docking-wpf-controls"></a><span data-ttu-id="50813-154">Ancrage de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="50813-154">Anchoring and Docking WPF Controls</span></span>
 <span data-ttu-id="50813-155">Un contrôle WPF hébergé sur un formulaire a le même comportement d'ancrage que d'autres contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="50813-155">A WPF control hosted on a form has the same anchoring and docking behavior as other Windows Forms controls.</span></span>

#### <a name="to-anchor-and-dock-wpf-controls"></a><span data-ttu-id="50813-156">Pour ancrer des contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="50813-156">To anchor and dock WPF controls</span></span>

1. <span data-ttu-id="50813-157">Sélectionnez `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="50813-157">Select `elementHost1`.</span></span>

2. <span data-ttu-id="50813-158">Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.Control.Anchor%2A> propriété **Top, Bottom, Left, Right**.</span><span class="sxs-lookup"><span data-stu-id="50813-158">In the **Properties** window, set the <xref:System.Windows.Forms.Control.Anchor%2A> property to **Top, Bottom, Left, Right**.</span></span>

3. <span data-ttu-id="50813-159">Agrandissez le contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="50813-159">Resize the <xref:System.Windows.Forms.TableLayoutPanel> control to a larger size.</span></span>

     <span data-ttu-id="50813-160">Le contrôle `elementHost1` est redimensionné pour remplir la cellule.</span><span class="sxs-lookup"><span data-stu-id="50813-160">The `elementHost1` control resizes to fill the cell.</span></span>

4. <span data-ttu-id="50813-161">Sélectionnez `elementHost2`.</span><span class="sxs-lookup"><span data-stu-id="50813-161">Select `elementHost2`.</span></span>

5. <span data-ttu-id="50813-162">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="50813-162">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>

     <span data-ttu-id="50813-163">Le contrôle `elementHost2` est redimensionné pour remplir la cellule.</span><span class="sxs-lookup"><span data-stu-id="50813-163">The `elementHost2` control resizes to fill the cell.</span></span>

6. <span data-ttu-id="50813-164">Sélectionnez le contrôle <xref:System.Windows.Forms.TableLayoutPanel>.</span><span class="sxs-lookup"><span data-stu-id="50813-164">Select the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

7. <span data-ttu-id="50813-165">Affectez à sa propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Top>.</span><span class="sxs-lookup"><span data-stu-id="50813-165">Set the value of its <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Top>.</span></span>

8. <span data-ttu-id="50813-166">Sélectionnez `elementHost3`.</span><span class="sxs-lookup"><span data-stu-id="50813-166">Select `elementHost3`.</span></span>

9. <span data-ttu-id="50813-167">Affectez à sa propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="50813-167">Set the value of its <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>

     <span data-ttu-id="50813-168">Le contrôle `elementHost3` est redimensionné pour remplir l'espace restant sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="50813-168">The `elementHost3` control resizes to fill the remaining space on the form.</span></span>

10. <span data-ttu-id="50813-169">Redimensionnez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="50813-169">Resize the form.</span></span>

     <span data-ttu-id="50813-170">Les trois contrôles <xref:System.Windows.Forms.Integration.ElementHost> sont redimensionnés correctement.</span><span class="sxs-lookup"><span data-stu-id="50813-170">All three <xref:System.Windows.Forms.Integration.ElementHost> controls resize appropriately.</span></span>

     <span data-ttu-id="50813-171">Pour plus d'informations, voir [Procédure : Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md).</span><span class="sxs-lookup"><span data-stu-id="50813-171">For more information, see [How to: Anchor and Dock Child Controls in a TableLayoutPanel Control](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="50813-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50813-172">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="50813-173">Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="50813-173">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="50813-174">Guide pratique pour Aligner un contrôle sur les bords des formulaires au moment du Design</span><span class="sxs-lookup"><span data-stu-id="50813-174">How to: Align a Control to the Edges of Forms at Design Time</span></span>](../controls/how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)
- [<span data-ttu-id="50813-175">Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement</span><span class="sxs-lookup"><span data-stu-id="50813-175">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [<span data-ttu-id="50813-176">Migration et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="50813-176">Migration and Interoperability</span></span>](../../wpf/advanced/migration-and-interoperability.md)
- [<span data-ttu-id="50813-177">Utilisation de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="50813-177">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="50813-178">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="50813-178">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
