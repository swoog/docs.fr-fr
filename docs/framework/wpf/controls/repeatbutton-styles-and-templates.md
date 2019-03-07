---
title: Styles et modèles RepeatButton
ms.date: 03/30/2017
helpviewer_keywords:
- RepeatButton [WPF], styles and templates
- styles [WPF], RepeatButton
- templates [WPF], RepeatButton
- parts [WPF], RepeatButton
- ControlTemplate [WPF], RepeatButton
- states [WPF], RepeatButton
ms.assetid: fd340743-f44f-4990-9077-085301469670
ms.openlocfilehash: 86f212326bc707e4b07b8cab8d9a95d4f6ef8920
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57509588"
---
# <a name="repeatbutton-styles-and-templates"></a><span data-ttu-id="c61d7-102">Styles et modèles RepeatButton</span><span class="sxs-lookup"><span data-stu-id="c61d7-102">RepeatButton Styles and Templates</span></span>

<span data-ttu-id="c61d7-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Primitives.RepeatButton> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c61d7-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.RepeatButton> control.</span></span> <span data-ttu-id="c61d7-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="c61d7-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="c61d7-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="c61d7-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>

## <a name="repeatbutton-parts"></a><span data-ttu-id="c61d7-106">Composants de RepeatButton</span><span class="sxs-lookup"><span data-stu-id="c61d7-106">RepeatButton Parts</span></span>

<span data-ttu-id="c61d7-107">Le <xref:System.Windows.Controls.Primitives.RepeatButton> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="c61d7-107">The <xref:System.Windows.Controls.Primitives.RepeatButton> control does not have any named parts.</span></span>

## <a name="repeatbutton-states"></a><span data-ttu-id="c61d7-108">États de RepeatButton</span><span class="sxs-lookup"><span data-stu-id="c61d7-108">RepeatButton States</span></span>

<span data-ttu-id="c61d7-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Primitives.RepeatButton> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c61d7-109">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.RepeatButton> control.</span></span>

|<span data-ttu-id="c61d7-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="c61d7-110">VisualState Name</span></span>|<span data-ttu-id="c61d7-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="c61d7-111">VisualStateGroup Name</span></span>|<span data-ttu-id="c61d7-112">Description</span><span class="sxs-lookup"><span data-stu-id="c61d7-112">Description</span></span>|
|-|-|-|
|<span data-ttu-id="c61d7-113">Normale</span><span class="sxs-lookup"><span data-stu-id="c61d7-113">Normal</span></span>|<span data-ttu-id="c61d7-114">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-114">CommonStates</span></span>|<span data-ttu-id="c61d7-115">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="c61d7-115">The default state.</span></span>|
|<span data-ttu-id="c61d7-116">MouseOver</span><span class="sxs-lookup"><span data-stu-id="c61d7-116">MouseOver</span></span>|<span data-ttu-id="c61d7-117">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-117">CommonStates</span></span>|<span data-ttu-id="c61d7-118">Le pointeur de la souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c61d7-118">The mouse pointer is positioned over the control.</span></span>|
|<span data-ttu-id="c61d7-119">Appuyé</span><span class="sxs-lookup"><span data-stu-id="c61d7-119">Pressed</span></span>|<span data-ttu-id="c61d7-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-120">CommonStates</span></span>|<span data-ttu-id="c61d7-121">Le contrôle est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="c61d7-121">The control is pressed.</span></span>|
|<span data-ttu-id="c61d7-122">Désactivé</span><span class="sxs-lookup"><span data-stu-id="c61d7-122">Disabled</span></span>|<span data-ttu-id="c61d7-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-123">CommonStates</span></span>|<span data-ttu-id="c61d7-124">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="c61d7-124">The control is disabled.</span></span>|
|<span data-ttu-id="c61d7-125">Avec focus</span><span class="sxs-lookup"><span data-stu-id="c61d7-125">Focused</span></span>|<span data-ttu-id="c61d7-126">FocusStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-126">FocusStates</span></span>|<span data-ttu-id="c61d7-127">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="c61d7-127">The control has focus.</span></span>|
|<span data-ttu-id="c61d7-128">Sans focus</span><span class="sxs-lookup"><span data-stu-id="c61d7-128">Unfocused</span></span>|<span data-ttu-id="c61d7-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-129">FocusStates</span></span>|<span data-ttu-id="c61d7-130">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="c61d7-130">The control does not have focus.</span></span>|
|<span data-ttu-id="c61d7-131">Valide</span><span class="sxs-lookup"><span data-stu-id="c61d7-131">Valid</span></span>|<span data-ttu-id="c61d7-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-132">ValidationStates</span></span>|<span data-ttu-id="c61d7-133">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="c61d7-133">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|
|<span data-ttu-id="c61d7-134">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="c61d7-134">InvalidFocused</span></span>|<span data-ttu-id="c61d7-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-135">ValidationStates</span></span>|<span data-ttu-id="c61d7-136">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="c61d7-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|
|<span data-ttu-id="c61d7-137">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="c61d7-137">InvalidUnfocused</span></span>|<span data-ttu-id="c61d7-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c61d7-138">ValidationStates</span></span>|<span data-ttu-id="c61d7-139">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="c61d7-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|

## <a name="repeatbutton-controltemplate-example"></a><span data-ttu-id="c61d7-140">Exemple de ControlTemplate RepeatButton</span><span class="sxs-lookup"><span data-stu-id="c61d7-140">RepeatButton ControlTemplate Example</span></span>

<span data-ttu-id="c61d7-141">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Primitives.RepeatButton> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c61d7-141">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.RepeatButton> control.</span></span>

[!code-xaml[ControlTemplateExamples#RepeatButton](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollbar.xaml#repeatbutton)]

<span data-ttu-id="c61d7-142">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="c61d7-142">The preceding example uses one or more of the following resources.</span></span>

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

<span data-ttu-id="c61d7-143">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="c61d7-143">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>

## <a name="see-also"></a><span data-ttu-id="c61d7-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c61d7-144">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="c61d7-145">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="c61d7-145">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="c61d7-146">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="c61d7-146">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="c61d7-147">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="c61d7-147">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="c61d7-148">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="c61d7-148">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
