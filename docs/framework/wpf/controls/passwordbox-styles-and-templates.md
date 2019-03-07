---
title: PasswordBox Styles et modèles
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], PasswordBox
- templates [WPF], PasswordBox
- ControlTemplate [WPF], PasswordBox
- states [WPF], PasswordBox
- PasswordBox [WPF], styles and templates
- parts [WPF], PasswordBox
ms.assetid: deb52107-959f-4a60-b303-d21a0a933060
ms.openlocfilehash: 7783330dd56ec5b2759e783a6935761eb3587978
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57509528"
---
# <a name="passwordbox-styles-and-templates"></a><span data-ttu-id="21924-102">PasswordBox Styles et modèles</span><span class="sxs-lookup"><span data-stu-id="21924-102">PasswordBox Styles and Templates</span></span>

<span data-ttu-id="21924-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="21924-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.PasswordBox> control.</span></span> <span data-ttu-id="21924-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="21924-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="21924-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="21924-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>

## <a name="passwordbox-parts"></a><span data-ttu-id="21924-106">Composants de PasswordBox</span><span class="sxs-lookup"><span data-stu-id="21924-106">PasswordBox Parts</span></span>

<span data-ttu-id="21924-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="21924-107">The following table lists the named parts for the <xref:System.Windows.Controls.PasswordBox> control.</span></span>

|<span data-ttu-id="21924-108">Élément</span><span class="sxs-lookup"><span data-stu-id="21924-108">Part</span></span>|<span data-ttu-id="21924-109">Type</span><span class="sxs-lookup"><span data-stu-id="21924-109">Type</span></span>|<span data-ttu-id="21924-110">Description</span><span class="sxs-lookup"><span data-stu-id="21924-110">Description</span></span>|
|-|-|-|
|<span data-ttu-id="21924-111">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="21924-111">PART_ContentHost</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="21924-112">Un élément visuel qui peut contenir un <xref:System.Windows.FrameworkElement>.</span><span class="sxs-lookup"><span data-stu-id="21924-112">A visual element that can contain a <xref:System.Windows.FrameworkElement>.</span></span> <span data-ttu-id="21924-113">Le texte de la <xref:System.Windows.Controls.PasswordBox> s’affiche dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="21924-113">The text of the <xref:System.Windows.Controls.PasswordBox> is displayed in this element.</span></span>|

## <a name="passwordbox-states"></a><span data-ttu-id="21924-114">États de PasswordBox</span><span class="sxs-lookup"><span data-stu-id="21924-114">PasswordBox States</span></span>

<span data-ttu-id="21924-115">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="21924-115">The following table lists the visual states for the <xref:System.Windows.Controls.PasswordBox> control.</span></span>

|<span data-ttu-id="21924-116">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="21924-116">VisualState Name</span></span>|<span data-ttu-id="21924-117">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="21924-117">VisualStateGroup Name</span></span>|<span data-ttu-id="21924-118">Description</span><span class="sxs-lookup"><span data-stu-id="21924-118">Description</span></span>|
|-|-|-|
|<span data-ttu-id="21924-119">Normale</span><span class="sxs-lookup"><span data-stu-id="21924-119">Normal</span></span>|<span data-ttu-id="21924-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="21924-120">CommonStates</span></span>|<span data-ttu-id="21924-121">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="21924-121">The default state.</span></span>|
|<span data-ttu-id="21924-122">MouseOver</span><span class="sxs-lookup"><span data-stu-id="21924-122">MouseOver</span></span>|<span data-ttu-id="21924-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="21924-123">CommonStates</span></span>|<span data-ttu-id="21924-124">Le pointeur de souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="21924-124">The mouse pointer is positioned over the control.</span></span>|
|<span data-ttu-id="21924-125">Désactivé</span><span class="sxs-lookup"><span data-stu-id="21924-125">Disabled</span></span>|<span data-ttu-id="21924-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="21924-126">CommonStates</span></span>|<span data-ttu-id="21924-127">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="21924-127">The control is disabled.</span></span>|
|<span data-ttu-id="21924-128">Avec focus</span><span class="sxs-lookup"><span data-stu-id="21924-128">Focused</span></span>|<span data-ttu-id="21924-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="21924-129">FocusStates</span></span>|<span data-ttu-id="21924-130">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="21924-130">The control has focus.</span></span>|
|<span data-ttu-id="21924-131">Sans focus</span><span class="sxs-lookup"><span data-stu-id="21924-131">Unfocused</span></span>|<span data-ttu-id="21924-132">FocusStates</span><span class="sxs-lookup"><span data-stu-id="21924-132">FocusStates</span></span>|<span data-ttu-id="21924-133">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="21924-133">The control does not have focus.</span></span>|
|<span data-ttu-id="21924-134">Valide</span><span class="sxs-lookup"><span data-stu-id="21924-134">Valid</span></span>|<span data-ttu-id="21924-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="21924-135">ValidationStates</span></span>|<span data-ttu-id="21924-136">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="21924-136">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|
|<span data-ttu-id="21924-137">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="21924-137">InvalidFocused</span></span>|<span data-ttu-id="21924-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="21924-138">ValidationStates</span></span>|<span data-ttu-id="21924-139">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="21924-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|
|<span data-ttu-id="21924-140">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="21924-140">InvalidUnfocused</span></span>|<span data-ttu-id="21924-141">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="21924-141">ValidationStates</span></span>|<span data-ttu-id="21924-142">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="21924-142">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|

## <a name="passwordbox-controltemplate-example"></a><span data-ttu-id="21924-143">Exemple de ControlTemplate PasswordBox</span><span class="sxs-lookup"><span data-stu-id="21924-143">PasswordBox ControlTemplate Example</span></span>

<span data-ttu-id="21924-144">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="21924-144">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.PasswordBox> control.</span></span>

[!code-xaml[ControlTemplateExamples#PasswordBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#passwordbox)]

<span data-ttu-id="21924-145">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="21924-145">The preceding example uses one or more of the following resources.</span></span>

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

<span data-ttu-id="21924-146">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="21924-146">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>

## <a name="see-also"></a><span data-ttu-id="21924-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21924-147">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="21924-148">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="21924-148">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="21924-149">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="21924-149">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="21924-150">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="21924-150">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="21924-151">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="21924-151">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
