---
title: Styles et modèles TextBox
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], TextBox
- parts [WPF], TextBox
- states [WPF], TextBox
- styles [WPF], TextBox
- templates [WPF], TextBox
- TextBox [WPF], styles and templates
ms.assetid: aa99130c-43a1-450f-9b46-c40ae0db0cca
ms.openlocfilehash: ccc89e0e0c8977398ed162b246ff6cdede3b8351
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61790869"
---
# <a name="textbox-styles-and-templates"></a><span data-ttu-id="377d6-102">Styles et modèles TextBox</span><span class="sxs-lookup"><span data-stu-id="377d6-102">TextBox Styles and Templates</span></span>
<span data-ttu-id="377d6-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="377d6-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.TextBox> control.</span></span> <span data-ttu-id="377d6-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="377d6-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="377d6-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="377d6-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="textbox-parts"></a><span data-ttu-id="377d6-106">Parties de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="377d6-106">TextBox Parts</span></span>  
 <span data-ttu-id="377d6-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="377d6-107">The following table lists the named parts for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
|<span data-ttu-id="377d6-108">Élément</span><span class="sxs-lookup"><span data-stu-id="377d6-108">Part</span></span>|<span data-ttu-id="377d6-109">Type</span><span class="sxs-lookup"><span data-stu-id="377d6-109">Type</span></span>|<span data-ttu-id="377d6-110">Description</span><span class="sxs-lookup"><span data-stu-id="377d6-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="377d6-111">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="377d6-111">PART_ContentHost</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="377d6-112">Un élément visuel qui peut contenir un <xref:System.Windows.FrameworkElement>.</span><span class="sxs-lookup"><span data-stu-id="377d6-112">A visual element that can contain a <xref:System.Windows.FrameworkElement>.</span></span> <span data-ttu-id="377d6-113">Le texte de la <xref:System.Windows.Controls.TextBox> s’affiche dans cet élément.</span><span class="sxs-lookup"><span data-stu-id="377d6-113">The text of the <xref:System.Windows.Controls.TextBox> is displayed in this element.</span></span>|  
  
## <a name="textbox-states"></a><span data-ttu-id="377d6-114">États de la zone de texte</span><span class="sxs-lookup"><span data-stu-id="377d6-114">TextBox States</span></span>  
 <span data-ttu-id="377d6-115">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="377d6-115">The following table lists the visual states for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
|<span data-ttu-id="377d6-116">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="377d6-116">VisualState Name</span></span>|<span data-ttu-id="377d6-117">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="377d6-117">VisualStateGroup Name</span></span>|<span data-ttu-id="377d6-118">Description</span><span class="sxs-lookup"><span data-stu-id="377d6-118">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="377d6-119">Normale</span><span class="sxs-lookup"><span data-stu-id="377d6-119">Normal</span></span>|<span data-ttu-id="377d6-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="377d6-120">CommonStates</span></span>|<span data-ttu-id="377d6-121">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="377d6-121">The default state.</span></span>|  
|<span data-ttu-id="377d6-122">MouseOver</span><span class="sxs-lookup"><span data-stu-id="377d6-122">MouseOver</span></span>|<span data-ttu-id="377d6-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="377d6-123">CommonStates</span></span>|<span data-ttu-id="377d6-124">Le pointeur de souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="377d6-124">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="377d6-125">Désactivé</span><span class="sxs-lookup"><span data-stu-id="377d6-125">Disabled</span></span>|<span data-ttu-id="377d6-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="377d6-126">CommonStates</span></span>|<span data-ttu-id="377d6-127">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="377d6-127">The control is disabled.</span></span>|  
|<span data-ttu-id="377d6-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="377d6-128">ReadOnly</span></span>|<span data-ttu-id="377d6-129">CommonStates</span><span class="sxs-lookup"><span data-stu-id="377d6-129">CommonStates</span></span>|<span data-ttu-id="377d6-130">L’utilisateur ne peut pas modifier le texte dans le <xref:System.Windows.Controls.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="377d6-130">The user cannot change the text in the <xref:System.Windows.Controls.TextBox>.</span></span>|  
|<span data-ttu-id="377d6-131">Avec focus</span><span class="sxs-lookup"><span data-stu-id="377d6-131">Focused</span></span>|<span data-ttu-id="377d6-132">FocusStates</span><span class="sxs-lookup"><span data-stu-id="377d6-132">FocusStates</span></span>|<span data-ttu-id="377d6-133">Le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="377d6-133">The control has focus.</span></span>|  
|<span data-ttu-id="377d6-134">Sans focus</span><span class="sxs-lookup"><span data-stu-id="377d6-134">Unfocused</span></span>|<span data-ttu-id="377d6-135">FocusStates</span><span class="sxs-lookup"><span data-stu-id="377d6-135">FocusStates</span></span>|<span data-ttu-id="377d6-136">Le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="377d6-136">The control does not have focus.</span></span>|  
|<span data-ttu-id="377d6-137">Valide</span><span class="sxs-lookup"><span data-stu-id="377d6-137">Valid</span></span>|<span data-ttu-id="377d6-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="377d6-138">ValidationStates</span></span>|<span data-ttu-id="377d6-139">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="377d6-139">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="377d6-140">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="377d6-140">InvalidFocused</span></span>|<span data-ttu-id="377d6-141">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="377d6-141">ValidationStates</span></span>|<span data-ttu-id="377d6-142">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="377d6-142">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="377d6-143">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="377d6-143">InvalidUnfocused</span></span>|<span data-ttu-id="377d6-144">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="377d6-144">ValidationStates</span></span>|<span data-ttu-id="377d6-145">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="377d6-145">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="textbox-controltemplate-example"></a><span data-ttu-id="377d6-146">Exemple de ControlTemplate de zone de texte</span><span class="sxs-lookup"><span data-stu-id="377d6-146">TextBox ControlTemplate Example</span></span>  
 <span data-ttu-id="377d6-147">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.TextBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="377d6-147">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#TextBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#textbox)]  
  
 <span data-ttu-id="377d6-148">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="377d6-148">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="377d6-149">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="377d6-149">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="377d6-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="377d6-150">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="377d6-151">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="377d6-151">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="377d6-152">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="377d6-152">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="377d6-153">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="377d6-153">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="377d6-154">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="377d6-154">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
