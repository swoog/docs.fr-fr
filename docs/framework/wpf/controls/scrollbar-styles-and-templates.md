---
title: Styles et modèles ScrollBar
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], ScrollBar
- ControlTemplate [WPF], ScrollBar
- states [WPF], ScrollBar
- ScrollBar [WPF], styles and templates
- templates [WPF], ScrollBar
- parts [WPF], ScrollBar
ms.assetid: 066ea45a-e27d-43b0-adfe-cce6934c22f5
ms.openlocfilehash: 22b2206067302f621a94a1e9abca1607792b3393
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59144506"
---
# <a name="scrollbar-styles-and-templates"></a><span data-ttu-id="1499c-102">Styles et modèles ScrollBar</span><span class="sxs-lookup"><span data-stu-id="1499c-102">ScrollBar Styles and Templates</span></span>
<span data-ttu-id="1499c-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Primitives.ScrollBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1499c-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span> <span data-ttu-id="1499c-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="1499c-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="1499c-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="1499c-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="scrollbar-parts"></a><span data-ttu-id="1499c-106">Parties de la barre de défilement</span><span class="sxs-lookup"><span data-stu-id="1499c-106">ScrollBar Parts</span></span>  
 <span data-ttu-id="1499c-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.Primitives.ScrollBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1499c-107">The following table lists the named parts for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span>  
  
|<span data-ttu-id="1499c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1499c-108">Part</span></span>|<span data-ttu-id="1499c-109">Type</span><span class="sxs-lookup"><span data-stu-id="1499c-109">Type</span></span>|<span data-ttu-id="1499c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1499c-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="1499c-111">PART_Track</span><span class="sxs-lookup"><span data-stu-id="1499c-111">PART_Track</span></span>|<xref:System.Windows.Controls.Primitives.Track>|<span data-ttu-id="1499c-112">Le conteneur de l’élément qui indique la position de la <xref:System.Windows.Controls.Primitives.ScrollBar>.</span><span class="sxs-lookup"><span data-stu-id="1499c-112">The container for the element that indicates the position of the <xref:System.Windows.Controls.Primitives.ScrollBar>.</span></span>|  
  
## <a name="scrollbar-states"></a><span data-ttu-id="1499c-113">États de la barre de défilement</span><span class="sxs-lookup"><span data-stu-id="1499c-113">ScrollBar States</span></span>  
 <span data-ttu-id="1499c-114">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Primitives.ScrollBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1499c-114">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span>  
  
|<span data-ttu-id="1499c-115">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="1499c-115">VisualState Name</span></span>|<span data-ttu-id="1499c-116">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="1499c-116">VisualStateGroup Name</span></span>|<span data-ttu-id="1499c-117">Description</span><span class="sxs-lookup"><span data-stu-id="1499c-117">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="1499c-118">Normale</span><span class="sxs-lookup"><span data-stu-id="1499c-118">Normal</span></span>|<span data-ttu-id="1499c-119">CommonStates</span><span class="sxs-lookup"><span data-stu-id="1499c-119">CommonStates</span></span>|<span data-ttu-id="1499c-120">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="1499c-120">The default state.</span></span>|  
|<span data-ttu-id="1499c-121">MouseOver</span><span class="sxs-lookup"><span data-stu-id="1499c-121">MouseOver</span></span>|<span data-ttu-id="1499c-122">CommonStates</span><span class="sxs-lookup"><span data-stu-id="1499c-122">CommonStates</span></span>|<span data-ttu-id="1499c-123">Le pointeur de souris est positionné sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="1499c-123">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="1499c-124">Désactivé</span><span class="sxs-lookup"><span data-stu-id="1499c-124">Disabled</span></span>|<span data-ttu-id="1499c-125">CommonStates</span><span class="sxs-lookup"><span data-stu-id="1499c-125">CommonStates</span></span>|<span data-ttu-id="1499c-126">Le contrôle est désactivé.</span><span class="sxs-lookup"><span data-stu-id="1499c-126">The control is disabled.</span></span>|  
|<span data-ttu-id="1499c-127">Valide</span><span class="sxs-lookup"><span data-stu-id="1499c-127">Valid</span></span>|<span data-ttu-id="1499c-128">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1499c-128">ValidationStates</span></span>|<span data-ttu-id="1499c-129">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="1499c-129">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="1499c-130">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="1499c-130">InvalidFocused</span></span>|<span data-ttu-id="1499c-131">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1499c-131">ValidationStates</span></span>|<span data-ttu-id="1499c-132">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="1499c-132">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="1499c-133">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="1499c-133">InvalidUnfocused</span></span>|<span data-ttu-id="1499c-134">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1499c-134">ValidationStates</span></span>|<span data-ttu-id="1499c-135">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="1499c-135">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="scrollbar-controltemplate-example"></a><span data-ttu-id="1499c-136">Exemple de ControlTemplate de barre de défilement</span><span class="sxs-lookup"><span data-stu-id="1499c-136">ScrollBar ControlTemplate Example</span></span>  
 <span data-ttu-id="1499c-137">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Primitives.ScrollBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1499c-137">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ScrollBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollbar.xaml#scrollbar)]  
  
 <span data-ttu-id="1499c-138">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="1499c-138">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="1499c-139">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="1499c-139">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1499c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1499c-140">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="1499c-141">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="1499c-141">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="1499c-142">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="1499c-142">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="1499c-143">Application d'un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="1499c-143">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="1499c-144">Personnalisation de l'apparence d'un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="1499c-144">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
