---
title: 'Procédure pas à pas : Attribution de contenu WPF dans Windows Forms au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- WPF content [Windows Forms], assigning at design time
- ElementHost control [Windows Forms], assigning WPF content at design time
- interoperability [WPF]
- Windows Forms, content assignments
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: b3e9ef93-7e0f-4a2f-8f1e-3437609a1eb7
ms.openlocfilehash: 09427bfc836f40ca9c7aa76f4904bfe7083bf8dc
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211235"
---
# <a name="walkthrough-assign-wpf-content-on-windows-forms-at-design-time"></a><span data-ttu-id="d7ba6-102">Procédure pas à pas : Assigner un contenu WPF dans les Windows Forms au moment du design</span><span class="sxs-lookup"><span data-stu-id="d7ba6-102">Walkthrough: Assign WPF content on Windows Forms at design time</span></span>

<span data-ttu-id="d7ba6-103">Cette procédure pas à pas montre comment sélectionner les types de contrôle WPF (Windows Presentation Foundation) que vous souhaitez afficher sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-103">This walkthrough show you how to select the Windows Presentation Foundation (WPF) control types you want to display on your form.</span></span> <span data-ttu-id="d7ba6-104">Vous pouvez sélectionner tout type de contrôle WPF inclus dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-104">You can select any WPF control types which are included in your project.</span></span>

<span data-ttu-id="d7ba6-105">Lors de cette procédure pas à pas, vous allez exécuter les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7ba6-105">In this walkthrough, you perform the following tasks:</span></span>

- <span data-ttu-id="d7ba6-106">créer le projet ;</span><span class="sxs-lookup"><span data-stu-id="d7ba6-106">Create the project.</span></span>

- <span data-ttu-id="d7ba6-107">créer les types de contrôles WPF ;</span><span class="sxs-lookup"><span data-stu-id="d7ba6-107">Create the WPF control types.</span></span>

- <span data-ttu-id="d7ba6-108">sélectionner les contrôles WPF.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-108">Select WPF controls.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d7ba6-109">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d7ba6-109">Prerequisites</span></span>

<span data-ttu-id="d7ba6-110">Cette procédure pas à pas nécessite Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-110">You need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="d7ba6-111">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="d7ba6-111">Create the project</span></span>

<span data-ttu-id="d7ba6-112">Ouvrez Visual Studio et créez un nouveau projet d’Application de Windows Forms dans Visual Basic ou Visual C# nommé `SelectingWpfContent`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-112">Open Visual Studio and create a new Windows Forms Application project in Visual Basic or Visual C# named `SelectingWpfContent`.</span></span>

> [!NOTE]
> <span data-ttu-id="d7ba6-113">Lors de l'hébergement de contenu WPF, seuls les projets Visual Basic et C# sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-113">When hosting WPF content, only C# and Visual Basic projects are supported.</span></span>

## <a name="create-the-wpf-control-types"></a><span data-ttu-id="d7ba6-114">Créer des types de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="d7ba6-114">Create the WPF control types</span></span>

<span data-ttu-id="d7ba6-115">Après avoir ajouté des types de contrôles WPF au projet, vous pouvez les héberger dans différents contrôles <xref:System.Windows.Forms.Integration.ElementHost>.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-115">After you add WPF control types to the project, you can host them in different <xref:System.Windows.Forms.Integration.ElementHost> controls.</span></span>

## <a name="create-wpf-control-types"></a><span data-ttu-id="d7ba6-116">Créer des types de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="d7ba6-116">Create WPF control types</span></span>

1. <span data-ttu-id="d7ba6-117">Ajoutez un nouveau projet <xref:System.Windows.Controls.UserControl> WPF à la solution.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-117">Add a new WPF <xref:System.Windows.Controls.UserControl> project to the solution.</span></span> <span data-ttu-id="d7ba6-118">Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-118">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="d7ba6-119">Pour plus d’informations, consultez [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="d7ba6-119">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>

2. <span data-ttu-id="d7ba6-120">En mode Design, assurez-vous que `UserControl1` est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-120">In Design view, make sure that `UserControl1` is selected.</span></span> <span data-ttu-id="d7ba6-121">Pour plus d'informations, voir [Procédure : Sélectionner et déplacer des éléments sur l’aire de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="d7ba6-121">For more information, see [How to: Select and Move Elements on the Design Surface](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).</span></span>

3. <span data-ttu-id="d7ba6-122">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à `200`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-122">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to `200`.</span></span>

4. <span data-ttu-id="d7ba6-123">Ajouter un <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> le contrôle à la <xref:System.Windows.Controls.UserControl> et définissez la valeur de la <xref:System.Windows.Controls.TextBox.Text%2A> propriété **le contenu hébergé**.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-123">Add a <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control to the <xref:System.Windows.Controls.UserControl> and set the value of the <xref:System.Windows.Controls.TextBox.Text%2A> property to **Hosted Content**.</span></span>

5. <span data-ttu-id="d7ba6-124">Ajoutez un deuxième <xref:System.Windows.Controls.UserControl> WPF au projet.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-124">Add a second WPF <xref:System.Windows.Controls.UserControl> to the project.</span></span> <span data-ttu-id="d7ba6-125">Utilisez le nom par défaut pour le type de contrôle, `UserControl2.xaml`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-125">Use the default name for the control type, `UserControl2.xaml`.</span></span>

6. <span data-ttu-id="d7ba6-126">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à `200`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-126">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to `200`.</span></span>

7. <span data-ttu-id="d7ba6-127">Ajouter un <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> le contrôle à la <xref:System.Windows.Controls.UserControl> et définissez la valeur de la <xref:System.Windows.Controls.TextBox.Text%2A> propriété **contenu hébergé 2**.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-127">Add a <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control to the <xref:System.Windows.Controls.UserControl> and set the value of the <xref:System.Windows.Controls.TextBox.Text%2A> property to **Hosted Content 2**.</span></span>

 <span data-ttu-id="d7ba6-128">**Remarque** en général, vous devez héberger le contenu WPF plus sophistiqué.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-128">**Note** In general, you should host more sophisticated WPF content.</span></span> <span data-ttu-id="d7ba6-129">Le contrôle <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> est utilisé ici uniquement à titre d'illustration.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-129">The <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control is used here for illustrative purposes only.</span></span>

1. <span data-ttu-id="d7ba6-130">Générez le projet.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-130">Build the project.</span></span>

## <a name="select-wpf-controls"></a><span data-ttu-id="d7ba6-131">Sélectionner les contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="d7ba6-131">Select WPF controls</span></span>

<span data-ttu-id="d7ba6-132">Vous pouvez assigner du contenu WPF différent à un contrôle <xref:System.Windows.Forms.Integration.ElementHost> qui héberge déjà du contenu.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-132">You can assign different WPF content to an <xref:System.Windows.Forms.Integration.ElementHost> control, which is already hosting content.</span></span>

1. <span data-ttu-id="d7ba6-133">Ouvrez `Form1` dans le Concepteur Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-133">Open `Form1` in the Windows Forms Designer.</span></span>

2. <span data-ttu-id="d7ba6-134">Dans le **boîte à outils**, double-cliquez sur `UserControl1` pour créer une instance de `UserControl1` sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-134">In the **Toolbox**, double-click `UserControl1` to create an instance of `UserControl1` on the form.</span></span>

     <span data-ttu-id="d7ba6-135">Une instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-135">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>

3. <span data-ttu-id="d7ba6-136">Dans le panneau des balises actives pour `elementHost1`, ouvrez le **sélectionner le contenu hébergé** liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-136">In the smart tag panel for `elementHost1`, open the **Select Hosted Content** drop-down list.</span></span>

4. <span data-ttu-id="d7ba6-137">Sélectionnez **UserControl2** dans la zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-137">Select **UserControl2** from the drop-down list box.</span></span>

     <span data-ttu-id="d7ba6-138">Le contrôle `elementHost1` héberge maintenant une instance du type `UserControl2`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-138">The `elementHost1` control now hosts an instance of the `UserControl2` type.</span></span>

5. <span data-ttu-id="d7ba6-139">Dans le **propriétés** fenêtre, vérifiez que le <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> propriété est définie sur **UserControl2**.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-139">In the **Properties** window, confirm that the <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> property is set to **UserControl2**.</span></span>

6. <span data-ttu-id="d7ba6-140">À partir de la **boîte à outils**, dans le **interopérabilité WPF** de groupe, faites glisser un <xref:System.Windows.Forms.Integration.ElementHost> contrôle vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-140">From the **Toolbox**, in the **WPF Interoperability** group, drag an <xref:System.Windows.Forms.Integration.ElementHost> control onto the form.</span></span>

     <span data-ttu-id="d7ba6-141">Le nom par défaut du nouveau contrôle est `elementHost2`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-141">The default name for the new control is `elementHost2`.</span></span>

7. <span data-ttu-id="d7ba6-142">Dans le panneau des balises actives pour `elementHost2`, ouvrez le **sélectionner le contenu hébergé** liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-142">In the smart tag panel for `elementHost2`, open the **Select Hosted Content** drop-down list.</span></span>

8. <span data-ttu-id="d7ba6-143">Sélectionnez **UserControl1** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-143">Select **UserControl1** from the drop-down list.</span></span>

9. <span data-ttu-id="d7ba6-144">Le contrôle `elementHost2` héberge maintenant une instance du type `UserControl1`.</span><span class="sxs-lookup"><span data-stu-id="d7ba6-144">The `elementHost2` control now hosts an instance of the `UserControl1` type.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7ba6-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7ba6-145">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="d7ba6-146">Migration et interopérabilité</span><span class="sxs-lookup"><span data-stu-id="d7ba6-146">Migration and Interoperability</span></span>](../../wpf/advanced/migration-and-interoperability.md)
- [<span data-ttu-id="d7ba6-147">Utilisation de contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="d7ba6-147">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="d7ba6-148">Concevoir en XAML dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d7ba6-148">Design XAML in Visual Studio</span></span>](/visualstudio/designers/designing-xaml-in-visual-studio)
