---
title: Styles et modèles Button
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], Button
- parts [WPF], Button
- styles [WPF], Button
- Button [WPF], styles and templates
- templates [WPF], Button
- ControlTemplate [WPF], Button
ms.assetid: e223c759-f8c4-4717-acfb-b1e40bdf5f3b
ms.openlocfilehash: ec64c7c2051b12cba01135054a90e54864b7386a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116335"
---
# <a name="button-styles-and-templates"></a><span data-ttu-id="115d9-102">Styles et modèles Button</span><span class="sxs-lookup"><span data-stu-id="115d9-102">Button Styles and Templates</span></span>
<span data-ttu-id="115d9-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Button> contrôle.</span><span class="sxs-lookup"><span data-stu-id="115d9-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Button> control.</span></span> <span data-ttu-id="115d9-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="115d9-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="115d9-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="115d9-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="button-parts"></a><span data-ttu-id="115d9-106">Parties de bouton</span><span class="sxs-lookup"><span data-stu-id="115d9-106">Button Parts</span></span>  
 <span data-ttu-id="115d9-107">Le <xref:System.Windows.Controls.Button> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="115d9-107">The <xref:System.Windows.Controls.Button> control does not have any named parts.</span></span>  
  
## <a name="button-states"></a><span data-ttu-id="115d9-108">États de bouton</span><span class="sxs-lookup"><span data-stu-id="115d9-108">Button States</span></span>  
 <span data-ttu-id="115d9-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Button> contrôle.</span><span class="sxs-lookup"><span data-stu-id="115d9-109">The following table lists the visual states for the <xref:System.Windows.Controls.Button> control.</span></span>  
  
|<span data-ttu-id="115d9-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="115d9-110">VisualState Name</span></span>|<span data-ttu-id="115d9-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="115d9-111">VisualStateGroup Name</span></span>|<span data-ttu-id="115d9-112">Description</span><span class="sxs-lookup"><span data-stu-id="115d9-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="115d9-113">Normale</span><span class="sxs-lookup"><span data-stu-id="115d9-113">Normal</span></span>|<span data-ttu-id="115d9-114">CommonStates</span><span class="sxs-lookup"><span data-stu-id="115d9-114">CommonStates</span></span>|<span data-ttu-id="115d9-115">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="115d9-115">The default state.</span></span>|  
|<span data-ttu-id="115d9-116">MouseOver</span><span class="sxs-lookup"><span data-stu-id="115d9-116">MouseOver</span></span>|<span data-ttu-id="115d9-117">CommonStates</span><span class="sxs-lookup"><span data-stu-id="115d9-117">CommonStates</span></span>|<span data-ttu-id="115d9-118">Le pointeur de la souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="115d9-118">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="115d9-119">Appuyé</span><span class="sxs-lookup"><span data-stu-id="115d9-119">Pressed</span></span>|<span data-ttu-id="115d9-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="115d9-120">CommonStates</span></span>|<span data-ttu-id="115d9-121">Le contrôle est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="115d9-121">The control is pressed.</span></span>|  
|<span data-ttu-id="115d9-122">Désactivé</span><span class="sxs-lookup"><span data-stu-id="115d9-122">Disabled</span></span>|<span data-ttu-id="115d9-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="115d9-123">CommonStates</span></span>|<span data-ttu-id="115d9-124">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="115d9-124">The control is disabled.</span></span>|  
|<span data-ttu-id="115d9-125">Avec focus</span><span class="sxs-lookup"><span data-stu-id="115d9-125">Focused</span></span>|<span data-ttu-id="115d9-126">FocusStates</span><span class="sxs-lookup"><span data-stu-id="115d9-126">FocusStates</span></span>|<span data-ttu-id="115d9-127">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="115d9-127">The control has focus.</span></span>|  
|<span data-ttu-id="115d9-128">Sans focus</span><span class="sxs-lookup"><span data-stu-id="115d9-128">Unfocused</span></span>|<span data-ttu-id="115d9-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="115d9-129">FocusStates</span></span>|<span data-ttu-id="115d9-130">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="115d9-130">The control does not have focus.</span></span>|  
|<span data-ttu-id="115d9-131">Valide</span><span class="sxs-lookup"><span data-stu-id="115d9-131">Valid</span></span>|<span data-ttu-id="115d9-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="115d9-132">ValidationStates</span></span>|<span data-ttu-id="115d9-133">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="115d9-133">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="115d9-134">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="115d9-134">InvalidFocused</span></span>|<span data-ttu-id="115d9-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="115d9-135">ValidationStates</span></span>|<span data-ttu-id="115d9-136">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` et le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="115d9-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control has focus.</span></span>|  
|<span data-ttu-id="115d9-137">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="115d9-137">InvalidUnfocused</span></span>|<span data-ttu-id="115d9-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="115d9-138">ValidationStates</span></span>|<span data-ttu-id="115d9-139">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` et le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="115d9-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control does not have focus.</span></span>|  
  
## <a name="button-controltemplate-example"></a><span data-ttu-id="115d9-140">Exemple de ControlTemplate de bouton</span><span class="sxs-lookup"><span data-stu-id="115d9-140">Button ControlTemplate Example</span></span>  
 <span data-ttu-id="115d9-141">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Button> contrôle.</span><span class="sxs-lookup"><span data-stu-id="115d9-141">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Button> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Button](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/button.xaml#button)]  
  
 <span data-ttu-id="115d9-142">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="115d9-142">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="115d9-143">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="115d9-143">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="115d9-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="115d9-144">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="115d9-145">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="115d9-145">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="115d9-146">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="115d9-146">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="115d9-147">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="115d9-147">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="115d9-148">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="115d9-148">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
