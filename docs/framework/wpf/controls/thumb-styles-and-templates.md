---
title: Thumb Styles et modèles
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], Thumb
- styles [WPF], Thumb
- templates [WPF], Thumb
- Thumb [WPF], styles and templates
- ControlTemplate [WPF], Thumb
- parts [WPF], Thumb
ms.assetid: 86a49235-62d9-414e-923e-53126e3f930a
ms.openlocfilehash: b7fc595f0c592d42f118c6b5542edf93716c2fca
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57509568"
---
# <a name="thumb-styles-and-templates"></a><span data-ttu-id="cc5da-102">Thumb Styles et modèles</span><span class="sxs-lookup"><span data-stu-id="cc5da-102">Thumb Styles and Templates</span></span>

<span data-ttu-id="cc5da-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Primitives.Thumb> contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc5da-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span> <span data-ttu-id="cc5da-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="cc5da-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="cc5da-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="cc5da-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>

## <a name="thumb-parts"></a><span data-ttu-id="cc5da-106">Composants de Thumb</span><span class="sxs-lookup"><span data-stu-id="cc5da-106">Thumb Parts</span></span>

<span data-ttu-id="cc5da-107">Le <xref:System.Windows.Controls.Primitives.Thumb> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="cc5da-107">The <xref:System.Windows.Controls.Primitives.Thumb> control does not have any named parts.</span></span>

## <a name="thumb-states"></a><span data-ttu-id="cc5da-108">États de Thumb</span><span class="sxs-lookup"><span data-stu-id="cc5da-108">Thumb States</span></span>

<span data-ttu-id="cc5da-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Primitives.Thumb> contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc5da-109">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span>

|<span data-ttu-id="cc5da-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="cc5da-110">VisualState Name</span></span>|<span data-ttu-id="cc5da-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="cc5da-111">VisualStateGroup Name</span></span>|<span data-ttu-id="cc5da-112">Description</span><span class="sxs-lookup"><span data-stu-id="cc5da-112">Description</span></span>|
|-|-|-|
|<span data-ttu-id="cc5da-113">Normale</span><span class="sxs-lookup"><span data-stu-id="cc5da-113">Normal</span></span>|<span data-ttu-id="cc5da-114">CommonStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-114">CommonStates</span></span>|<span data-ttu-id="cc5da-115">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="cc5da-115">The default state.</span></span>|
|<span data-ttu-id="cc5da-116">MouseOver</span><span class="sxs-lookup"><span data-stu-id="cc5da-116">MouseOver</span></span>|<span data-ttu-id="cc5da-117">CommonStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-117">CommonStates</span></span>|<span data-ttu-id="cc5da-118">Le pointeur de la souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc5da-118">The mouse pointer is positioned over the control.</span></span>|
|<span data-ttu-id="cc5da-119">Appuyé</span><span class="sxs-lookup"><span data-stu-id="cc5da-119">Pressed</span></span>|<span data-ttu-id="cc5da-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-120">CommonStates</span></span>|<span data-ttu-id="cc5da-121">Le contrôle est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="cc5da-121">The control is pressed.</span></span>|
|<span data-ttu-id="cc5da-122">Désactivé</span><span class="sxs-lookup"><span data-stu-id="cc5da-122">Disabled</span></span>|<span data-ttu-id="cc5da-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-123">CommonStates</span></span>|<span data-ttu-id="cc5da-124">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cc5da-124">The control is disabled.</span></span>|
|<span data-ttu-id="cc5da-125">Avec focus</span><span class="sxs-lookup"><span data-stu-id="cc5da-125">Focused</span></span>|<span data-ttu-id="cc5da-126">FocusStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-126">FocusStates</span></span>|<span data-ttu-id="cc5da-127">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="cc5da-127">The control has focus.</span></span>|
|<span data-ttu-id="cc5da-128">Sans focus</span><span class="sxs-lookup"><span data-stu-id="cc5da-128">Unfocused</span></span>|<span data-ttu-id="cc5da-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-129">FocusStates</span></span>|<span data-ttu-id="cc5da-130">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="cc5da-130">The control does not have focus.</span></span>|
|<span data-ttu-id="cc5da-131">Valide</span><span class="sxs-lookup"><span data-stu-id="cc5da-131">Valid</span></span>|<span data-ttu-id="cc5da-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-132">ValidationStates</span></span>|<span data-ttu-id="cc5da-133">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="cc5da-133">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|
|<span data-ttu-id="cc5da-134">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="cc5da-134">InvalidFocused</span></span>|<span data-ttu-id="cc5da-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-135">ValidationStates</span></span>|<span data-ttu-id="cc5da-136">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="cc5da-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|
|<span data-ttu-id="cc5da-137">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="cc5da-137">InvalidUnfocused</span></span>|<span data-ttu-id="cc5da-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="cc5da-138">ValidationStates</span></span>|<span data-ttu-id="cc5da-139">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="cc5da-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|

## <a name="thumb-controltemplate-example"></a><span data-ttu-id="cc5da-140">Exemple de ControlTemplate Thumb</span><span class="sxs-lookup"><span data-stu-id="cc5da-140">Thumb ControlTemplate Example</span></span>

<span data-ttu-id="cc5da-141">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Primitives.Thumb> contrôle.</span><span class="sxs-lookup"><span data-stu-id="cc5da-141">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span>

[!code-xaml[ControlTemplateExamples#Thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/slider.xaml#thumb)]

<span data-ttu-id="cc5da-142">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc5da-142">The preceding example uses one or more of the following resources.</span></span>

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

<span data-ttu-id="cc5da-143">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="cc5da-143">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>

## <a name="see-also"></a><span data-ttu-id="cc5da-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc5da-144">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="cc5da-145">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="cc5da-145">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="cc5da-146">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="cc5da-146">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="cc5da-147">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="cc5da-147">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="cc5da-148">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="cc5da-148">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
