---
title: Styles et modèles Slider
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], Slider
- states [WPF], Slider
- Slider [WPF], styles and templates
- styles [WPF], Slider
- templates [WPF], Slider
- ControlTemplate [WPF], Slider
ms.assetid: d89aa97b-075a-4752-9c41-9679df65c491
ms.openlocfilehash: 385a69ad2bd17ae4c51437245915109aad446bdf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61970974"
---
# <a name="slider-styles-and-templates"></a><span data-ttu-id="2c63d-102">Styles et modèles Slider</span><span class="sxs-lookup"><span data-stu-id="2c63d-102">Slider Styles and Templates</span></span>
<span data-ttu-id="2c63d-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Slider> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c63d-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Slider> control.</span></span> <span data-ttu-id="2c63d-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="2c63d-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="2c63d-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="2c63d-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="slider-parts"></a><span data-ttu-id="2c63d-106">Parties de curseur</span><span class="sxs-lookup"><span data-stu-id="2c63d-106">Slider Parts</span></span>  
 <span data-ttu-id="2c63d-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.Slider> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c63d-107">The following table lists the named parts for the <xref:System.Windows.Controls.Slider> control.</span></span>  
  
|<span data-ttu-id="2c63d-108">Élément</span><span class="sxs-lookup"><span data-stu-id="2c63d-108">Part</span></span>|<span data-ttu-id="2c63d-109">Type</span><span class="sxs-lookup"><span data-stu-id="2c63d-109">Type</span></span>|<span data-ttu-id="2c63d-110">Description</span><span class="sxs-lookup"><span data-stu-id="2c63d-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="2c63d-111">PART_Track</span><span class="sxs-lookup"><span data-stu-id="2c63d-111">PART_Track</span></span>|<xref:System.Windows.Controls.Primitives.Track>|<span data-ttu-id="2c63d-112">Le conteneur de l’élément qui indique la position de la <xref:System.Windows.Controls.Slider>.</span><span class="sxs-lookup"><span data-stu-id="2c63d-112">The container for the element that indicates the position of the <xref:System.Windows.Controls.Slider>.</span></span>|  
|<span data-ttu-id="2c63d-113">PART_SelectionRange</span><span class="sxs-lookup"><span data-stu-id="2c63d-113">PART_SelectionRange</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="2c63d-114">L’élément qui affiche une plage de sélection le long de la <xref:System.Windows.Controls.Slider>.</span><span class="sxs-lookup"><span data-stu-id="2c63d-114">The element that displays a selection range along the <xref:System.Windows.Controls.Slider>.</span></span>  <span data-ttu-id="2c63d-115">La plage de sélection est visible uniquement si le <xref:System.Windows.Controls.Slider.IsSelectionRangeEnabled%2A> propriété est `true`.</span><span class="sxs-lookup"><span data-stu-id="2c63d-115">The selection range is visible only if the <xref:System.Windows.Controls.Slider.IsSelectionRangeEnabled%2A> property is `true`.</span></span>|  
  
## <a name="slider-states"></a><span data-ttu-id="2c63d-116">États de curseur</span><span class="sxs-lookup"><span data-stu-id="2c63d-116">Slider States</span></span>  
 <span data-ttu-id="2c63d-117">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Slider> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c63d-117">The following table lists the visual states for the <xref:System.Windows.Controls.Slider> control.</span></span>  
  
|<span data-ttu-id="2c63d-118">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="2c63d-118">VisualState Name</span></span>|<span data-ttu-id="2c63d-119">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="2c63d-119">VisualStateGroup Name</span></span>|<span data-ttu-id="2c63d-120">Description</span><span class="sxs-lookup"><span data-stu-id="2c63d-120">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="2c63d-121">Normale</span><span class="sxs-lookup"><span data-stu-id="2c63d-121">Normal</span></span>|<span data-ttu-id="2c63d-122">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-122">CommonStates</span></span>|<span data-ttu-id="2c63d-123">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="2c63d-123">The default state.</span></span>|  
|<span data-ttu-id="2c63d-124">MouseOver</span><span class="sxs-lookup"><span data-stu-id="2c63d-124">MouseOver</span></span>|<span data-ttu-id="2c63d-125">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-125">CommonStates</span></span>|<span data-ttu-id="2c63d-126">Le pointeur de souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c63d-126">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="2c63d-127">Désactivé</span><span class="sxs-lookup"><span data-stu-id="2c63d-127">Disabled</span></span>|<span data-ttu-id="2c63d-128">CommonStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-128">CommonStates</span></span>|<span data-ttu-id="2c63d-129">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="2c63d-129">The control is disabled.</span></span>|  
|<span data-ttu-id="2c63d-130">Avec focus</span><span class="sxs-lookup"><span data-stu-id="2c63d-130">Focused</span></span>|<span data-ttu-id="2c63d-131">FocusStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-131">FocusStates</span></span>|<span data-ttu-id="2c63d-132">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="2c63d-132">The control has focus.</span></span>|  
|<span data-ttu-id="2c63d-133">Sans focus</span><span class="sxs-lookup"><span data-stu-id="2c63d-133">Unfocused</span></span>|<span data-ttu-id="2c63d-134">FocusStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-134">FocusStates</span></span>|<span data-ttu-id="2c63d-135">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="2c63d-135">The control does not have focus.</span></span>|  
|<span data-ttu-id="2c63d-136">Valide</span><span class="sxs-lookup"><span data-stu-id="2c63d-136">Valid</span></span>|<span data-ttu-id="2c63d-137">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-137">ValidationStates</span></span>|<span data-ttu-id="2c63d-138">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="2c63d-138">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="2c63d-139">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="2c63d-139">InvalidFocused</span></span>|<span data-ttu-id="2c63d-140">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-140">ValidationStates</span></span>|<span data-ttu-id="2c63d-141">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="2c63d-141">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="2c63d-142">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="2c63d-142">InvalidUnfocused</span></span>|<span data-ttu-id="2c63d-143">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2c63d-143">ValidationStates</span></span>|<span data-ttu-id="2c63d-144">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="2c63d-144">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="slider-controltemplate-example"></a><span data-ttu-id="2c63d-145">Exemple de ControlTemplate de curseur</span><span class="sxs-lookup"><span data-stu-id="2c63d-145">Slider ControlTemplate Example</span></span>  
 <span data-ttu-id="2c63d-146">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Slider> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2c63d-146">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Slider> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Slider](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/slider.xaml#slider)]  
  
 <span data-ttu-id="2c63d-147">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="2c63d-147">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="2c63d-148">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="2c63d-148">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c63d-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c63d-149">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="2c63d-150">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="2c63d-150">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="2c63d-151">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="2c63d-151">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="2c63d-152">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="2c63d-152">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="2c63d-153">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="2c63d-153">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
