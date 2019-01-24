---
title: Styles et modèles PasswordBox
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], PasswordBox
- templates [WPF], PasswordBox
- ControlTemplate [WPF], PasswordBox
- states [WPF], PasswordBox
- PasswordBox [WPF], styles and templates
- parts [WPF], PasswordBox
ms.assetid: deb52107-959f-4a60-b303-d21a0a933060
ms.openlocfilehash: 464e2ff88b6e311470f6afe107d770922d9a395d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689232"
---
# <a name="passwordbox-syles-and-templates"></a><span data-ttu-id="33513-102">Styles et modèles PasswordBox</span><span class="sxs-lookup"><span data-stu-id="33513-102">PasswordBox Syles and Templates</span></span>
<span data-ttu-id="33513-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="33513-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.PasswordBox> control.</span></span> <span data-ttu-id="33513-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="33513-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="33513-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="33513-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="passwordbox-parts"></a><span data-ttu-id="33513-106">Composants de PasswordBox</span><span class="sxs-lookup"><span data-stu-id="33513-106">PasswordBox Parts</span></span>  
 <span data-ttu-id="33513-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="33513-107">The following table lists the named parts for the <xref:System.Windows.Controls.PasswordBox> control.</span></span>  
  
|<span data-ttu-id="33513-108">Élément</span><span class="sxs-lookup"><span data-stu-id="33513-108">Part</span></span>|<span data-ttu-id="33513-109">Type</span><span class="sxs-lookup"><span data-stu-id="33513-109">Type</span></span>|<span data-ttu-id="33513-110">Description</span><span class="sxs-lookup"><span data-stu-id="33513-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="33513-111">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="33513-111">PART_ContentHost</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="33513-112">Un élément visuel qui peut contenir un <xref:System.Windows.FrameworkElement>.</span><span class="sxs-lookup"><span data-stu-id="33513-112">A visual element that can contain a <xref:System.Windows.FrameworkElement>.</span></span> <span data-ttu-id="33513-113">Le texte de la <xref:System.Windows.Controls.PasswordBox> s’affiche dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="33513-113">The text of the <xref:System.Windows.Controls.PasswordBox> is displayed in this element.</span></span>|  
  
## <a name="passwordbox-states"></a><span data-ttu-id="33513-114">États de PasswordBox</span><span class="sxs-lookup"><span data-stu-id="33513-114">PasswordBox States</span></span>  
 <span data-ttu-id="33513-115">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="33513-115">The following table lists the visual states for the <xref:System.Windows.Controls.PasswordBox> control.</span></span>  
  
|<span data-ttu-id="33513-116">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="33513-116">VisualState Name</span></span>|<span data-ttu-id="33513-117">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="33513-117">VisualStateGroup Name</span></span>|<span data-ttu-id="33513-118">Description</span><span class="sxs-lookup"><span data-stu-id="33513-118">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="33513-119">Normale</span><span class="sxs-lookup"><span data-stu-id="33513-119">Normal</span></span>|<span data-ttu-id="33513-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="33513-120">CommonStates</span></span>|<span data-ttu-id="33513-121">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="33513-121">The default state.</span></span>|  
|<span data-ttu-id="33513-122">MouseOver</span><span class="sxs-lookup"><span data-stu-id="33513-122">MouseOver</span></span>|<span data-ttu-id="33513-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="33513-123">CommonStates</span></span>|<span data-ttu-id="33513-124">Le pointeur de souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="33513-124">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="33513-125">Désactivé</span><span class="sxs-lookup"><span data-stu-id="33513-125">Disabled</span></span>|<span data-ttu-id="33513-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="33513-126">CommonStates</span></span>|<span data-ttu-id="33513-127">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="33513-127">The control is disabled.</span></span>|  
|<span data-ttu-id="33513-128">Avec focus</span><span class="sxs-lookup"><span data-stu-id="33513-128">Focused</span></span>|<span data-ttu-id="33513-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="33513-129">FocusStates</span></span>|<span data-ttu-id="33513-130">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="33513-130">The control has focus.</span></span>|  
|<span data-ttu-id="33513-131">Sans focus</span><span class="sxs-lookup"><span data-stu-id="33513-131">Unfocused</span></span>|<span data-ttu-id="33513-132">FocusStates</span><span class="sxs-lookup"><span data-stu-id="33513-132">FocusStates</span></span>|<span data-ttu-id="33513-133">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="33513-133">The control does not have focus.</span></span>|  
|<span data-ttu-id="33513-134">Valide</span><span class="sxs-lookup"><span data-stu-id="33513-134">Valid</span></span>|<span data-ttu-id="33513-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="33513-135">ValidationStates</span></span>|<span data-ttu-id="33513-136">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="33513-136">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="33513-137">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="33513-137">InvalidFocused</span></span>|<span data-ttu-id="33513-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="33513-138">ValidationStates</span></span>|<span data-ttu-id="33513-139">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="33513-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="33513-140">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="33513-140">InvalidUnfocused</span></span>|<span data-ttu-id="33513-141">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="33513-141">ValidationStates</span></span>|<span data-ttu-id="33513-142">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="33513-142">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="passwordbox-controltemplate-example"></a><span data-ttu-id="33513-143">Exemple de ControlTemplate PasswordBox</span><span class="sxs-lookup"><span data-stu-id="33513-143">PasswordBox ControlTemplate Example</span></span>  
 <span data-ttu-id="33513-144">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.PasswordBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="33513-144">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.PasswordBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#PasswordBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#passwordbox)]  
  
 <span data-ttu-id="33513-145">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="33513-145">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="33513-146">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="33513-146">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33513-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33513-147">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="33513-148">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="33513-148">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="33513-149">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="33513-149">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="33513-150">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="33513-150">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="33513-151">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="33513-151">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
