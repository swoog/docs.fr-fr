---
title: Utilisation de contrôles WPF
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
ms.openlocfilehash: 149a2da1303e6b801a439494254a416a38b145a7
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211314"
---
# <a name="use-wpf-controls"></a><span data-ttu-id="2f309-102">Utiliser des contrôles WPF</span><span class="sxs-lookup"><span data-stu-id="2f309-102">Use WPF controls</span></span>

<span data-ttu-id="2f309-103">Vous pouvez utiliser des contrôles Windows Presentation Foundation (WPF) dans vos applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="2f309-103">You can use Windows Presentation Foundation (WPF) controls in your Windows Forms-based applications.</span></span> <span data-ttu-id="2f309-104">Bien qu’il s’agit de deux technologies d’affichage différent, ils interagissent sans heurts.</span><span class="sxs-lookup"><span data-stu-id="2f309-104">Although these are two different view technologies, they interoperate smoothly.</span></span>

<span data-ttu-id="2f309-105">Le Concepteur de formulaires Windows dans Visual Studio fournit un environnement de conception visuelle pour l’hébergement de contrôles Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="2f309-105">The Windows Forms Designer in Visual Studio provides a visual design environment for hosting Windows Presentation Foundation controls.</span></span> <span data-ttu-id="2f309-106">Un contrôle WPF est hébergé par un contrôle Windows Forms spécial nommé <xref:System.Windows.Forms.Integration.ElementHost>.</span><span class="sxs-lookup"><span data-stu-id="2f309-106">A WPF control is hosted by a special Windows Forms control that is named <xref:System.Windows.Forms.Integration.ElementHost>.</span></span> <span data-ttu-id="2f309-107">Ce contrôle permet le contrôle WPF à participer à la disposition du formulaire et de recevoir des messages de clavier et souris.</span><span class="sxs-lookup"><span data-stu-id="2f309-107">This control enables the WPF control to participate in the form's layout and to receive keyboard and mouse messages.</span></span> <span data-ttu-id="2f309-108">Au moment du design, vous pouvez organiser les <xref:System.Windows.Forms.Integration.ElementHost> contrôler tout comme vous le feriez pour n’importe quel contrôle Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="2f309-108">At design time, you can arrange the <xref:System.Windows.Forms.Integration.ElementHost> control just as you would any Windows Forms control.</span></span>

<span data-ttu-id="2f309-109">Vous pouvez également utiliser des contrôles Windows Forms dans vos applications WPF.</span><span class="sxs-lookup"><span data-stu-id="2f309-109">You can also use Windows Forms controls in your WPF-based applications.</span></span> <span data-ttu-id="2f309-110">Pour plus d’informations, consultez [XAML de conception dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="2f309-110">For more information, see [Design XAML in Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f309-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2f309-111">In This Section</span></span>

<span data-ttu-id="2f309-112">[Guide pratique pour Copiez et collez un contrôle ElementHost au moment du Design](how-to-copy-and-paste-an-elementhost-control-at-design-time.md)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-112">[How to: Copy and Paste an ElementHost Control at Design Time](how-to-copy-and-paste-an-elementhost-control-at-design-time.md)\\</span></span>
<span data-ttu-id="2f309-113">Montre comment copier un contrôle Windows Presentation Foundation sur un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="2f309-113">Shows how to copy a Windows Presentation Foundation control on a Windows Form.</span></span>

<span data-ttu-id="2f309-114">[Procédure pas à pas : Réorganisation du contenu WPF dans les Windows Forms au moment du Design](walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-114">[Walkthrough: Arranging WPF Content on Windows Forms at Design Time](walkthrough-arranging-wpf-content-on-windows-forms-at-design-time.md)\\</span></span>
<span data-ttu-id="2f309-115">Montre comment utiliser les fonctionnalités de disposition Windows Forms, telles que l’ancrage et les lignes d’alignement, pour organiser les contrôles de Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="2f309-115">Shows how to use the Windows Forms layout features, such as anchoring and snaplines, to arrange Windows Presentation Foundation controls.</span></span>

<span data-ttu-id="2f309-116">[Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-116">[Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md)\\</span></span>
<span data-ttu-id="2f309-117">Montre comment créer un contrôle Windows Presentation Foundation pour une utilisation dans vos applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="2f309-117">Shows how to create a Windows Presentation Foundation control for use in your Windows Forms-based applications.</span></span>

<span data-ttu-id="2f309-118">[Procédure pas à pas : Assignation du contenu WPF dans les Windows Forms au moment du Design](walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-118">[Walkthrough: Assigning WPF Content on Windows Forms at Design Time](walkthrough-assigning-wpf-content-on-windows-forms-at-design-time.md)\\</span></span>
<span data-ttu-id="2f309-119">Montre comment sélectionner les types de contrôle Windows Presentation Foundation que vous souhaitez afficher sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="2f309-119">Shows how to select the Windows Presentation Foundation control types you want to display on your form.</span></span>

<span data-ttu-id="2f309-120">[Procédure pas à pas : Contenu WPF de style](walkthrough-styling-wpf-content.md)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-120">[Walkthrough: Styling WPF Content](walkthrough-styling-wpf-content.md)\\</span></span>
<span data-ttu-id="2f309-121">Affiche le workflow entre le Concepteur de formulaires Windows et le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] pour appliquer des styles à des contrôles Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="2f309-121">Shows the workflow between the Windows Forms Designer and the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)] for applying styles to Windows Presentation Foundation controls.</span></span>

## <a name="reference"></a><span data-ttu-id="2f309-122">Référence</span><span class="sxs-lookup"><span data-stu-id="2f309-122">Reference</span></span>

<xref:System.Windows.Forms.Integration.ElementHost>\
<span data-ttu-id="2f309-123">Décrit une classe que vous pouvez utiliser pour héberger des contrôles Windows Presentation Foundation dans vos applications Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="2f309-123">Describes a class which you can use to host Windows Presentation Foundation controls in your Windows Forms-based applications.</span></span>

<xref:System.Windows.Forms.Integration.WindowsFormsHost>\
<span data-ttu-id="2f309-124">Décrit une classe que vous pouvez utiliser pour héberger des contrôles Windows Forms dans votre application Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="2f309-124">Describes a class which you can use to host Windows Forms controls in your Windows Presentation Foundation-based application.</span></span>

## <a name="related-sections"></a><span data-ttu-id="2f309-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f309-125">Related sections</span></span>

<span data-ttu-id="2f309-126">[Migration et interopérabilité](../../wpf/advanced/migration-and-interoperability.md)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-126">[Migration and Interoperability](../../wpf/advanced/migration-and-interoperability.md)\\</span></span>
<span data-ttu-id="2f309-127">Décrit l’interopérabilité entre les technologies Windows Presentation Foundation et Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="2f309-127">Describes interoperation between the Windows Presentation Foundation and Windows Forms technologies.</span></span>

<span data-ttu-id="2f309-128">[Conception XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)\\</span><span class="sxs-lookup"><span data-stu-id="2f309-128">[Design XAML in Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)\\</span></span>
<span data-ttu-id="2f309-129">Explique comment concevoir des contrôles Windows Presentation Foundation dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2f309-129">Describes how to design Windows Presentation Foundation controls in Visual Studio.</span></span>
