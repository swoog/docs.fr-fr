---
title: Styles et modèles ProgressBar
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ProgressBar
- ProgressBar [WPF], styles and templates
- styles [WPF], ProgressBar
- ControlTemplate [WPF], ProgressBar
- templates [WPF], ProgressBar
- states [WPF], ProgressBar
ms.assetid: 935aa600-16e6-4947-a905-37a189a583dd
ms.openlocfilehash: 89aea3e80fe17ece8a17f62f62290d34ddd55c60
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="progressbar-styles-and-templates"></a><span data-ttu-id="c92c1-102">Styles et modèles ProgressBar</span><span class="sxs-lookup"><span data-stu-id="c92c1-102">ProgressBar Styles and Templates</span></span>
<span data-ttu-id="c92c1-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c92c1-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ProgressBar> control.</span></span> <span data-ttu-id="c92c1-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner une apparence unique au contrôle.</span><span class="sxs-lookup"><span data-stu-id="c92c1-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="c92c1-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="c92c1-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="progressbar-parts"></a><span data-ttu-id="c92c1-106">Parties de la barre de progression</span><span class="sxs-lookup"><span data-stu-id="c92c1-106">ProgressBar Parts</span></span>  
 <span data-ttu-id="c92c1-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c92c1-107">The following table lists the named parts for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="c92c1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c92c1-108">Part</span></span>|<span data-ttu-id="c92c1-109">Type</span><span class="sxs-lookup"><span data-stu-id="c92c1-109">Type</span></span>|<span data-ttu-id="c92c1-110">Description</span><span class="sxs-lookup"><span data-stu-id="c92c1-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="c92c1-111">PART_Indicator</span><span class="sxs-lookup"><span data-stu-id="c92c1-111">PART_Indicator</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="c92c1-112">Objet qui indique la progression.</span><span class="sxs-lookup"><span data-stu-id="c92c1-112">The object that indicates progress.</span></span>|  
|<span data-ttu-id="c92c1-113">PART_Track</span><span class="sxs-lookup"><span data-stu-id="c92c1-113">PART_Track</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="c92c1-114">Objet qui définit le chemin d’accès de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="c92c1-114">The object that defines the path of the progress indicator.</span></span>|  
|<span data-ttu-id="c92c1-115">PART_GlowRect</span><span class="sxs-lookup"><span data-stu-id="c92c1-115">PART_GlowRect</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="c92c1-116">Objet qui embellit la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="c92c1-116">An object that embellishes the progress bar.</span></span>|  
  
## <a name="progressbar-states"></a><span data-ttu-id="c92c1-117">États de la barre de progression</span><span class="sxs-lookup"><span data-stu-id="c92c1-117">ProgressBar States</span></span>  
 <span data-ttu-id="c92c1-118">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c92c1-118">The following table lists the visual states for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="c92c1-119">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="c92c1-119">VisualState Name</span></span>|<span data-ttu-id="c92c1-120">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="c92c1-120">VisualStateGroup Name</span></span>|<span data-ttu-id="c92c1-121">Description</span><span class="sxs-lookup"><span data-stu-id="c92c1-121">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="c92c1-122">Déterminé</span><span class="sxs-lookup"><span data-stu-id="c92c1-122">Determinate</span></span>|<span data-ttu-id="c92c1-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c92c1-123">CommonStates</span></span>|<span data-ttu-id="c92c1-124"><xref:System.Windows.Controls.ProgressBar> signale la progression en fonction de la <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c92c1-124"><xref:System.Windows.Controls.ProgressBar> reports progress based on the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> property.</span></span>|  
|<span data-ttu-id="c92c1-125">Indéterminé</span><span class="sxs-lookup"><span data-stu-id="c92c1-125">Indeterminate</span></span>|<span data-ttu-id="c92c1-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c92c1-126">CommonStates</span></span>|<span data-ttu-id="c92c1-127"><xref:System.Windows.Controls.ProgressBar> signale la progression générale avec un modèle extensible.</span><span class="sxs-lookup"><span data-stu-id="c92c1-127"><xref:System.Windows.Controls.ProgressBar> reports generic progress with a repeating pattern.</span></span>|  
|<span data-ttu-id="c92c1-128">Valide</span><span class="sxs-lookup"><span data-stu-id="c92c1-128">Valid</span></span>|<span data-ttu-id="c92c1-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c92c1-129">ValidationStates</span></span>|<span data-ttu-id="c92c1-130">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="c92c1-130">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="c92c1-131">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="c92c1-131">InvalidFocused</span></span>|<span data-ttu-id="c92c1-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c92c1-132">ValidationStates</span></span>|<span data-ttu-id="c92c1-133">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="c92c1-133">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="c92c1-134">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="c92c1-134">InvalidUnfocused</span></span>|<span data-ttu-id="c92c1-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c92c1-135">ValidationStates</span></span>|<span data-ttu-id="c92c1-136">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="c92c1-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="progressbar-controltemplate-example"></a><span data-ttu-id="c92c1-137">ProgressBar ControlTemplate, exemple</span><span class="sxs-lookup"><span data-stu-id="c92c1-137">ProgressBar ControlTemplate Example</span></span>  
 <span data-ttu-id="c92c1-138">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c92c1-138">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ProgressBar](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/progressbar.xaml#progressbar)]  
  
 <span data-ttu-id="c92c1-139">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="c92c1-139">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="c92c1-140">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="c92c1-140">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c92c1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c92c1-141">See Also</span></span>  
 <xref:System.Windows.FrameworkElement.Style%2A>  
 <xref:System.Windows.Controls.ControlTemplate>  
 [<span data-ttu-id="c92c1-142">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="c92c1-142">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)  
 [<span data-ttu-id="c92c1-143">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="c92c1-143">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)  
 [<span data-ttu-id="c92c1-144">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="c92c1-144">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)  
 [<span data-ttu-id="c92c1-145">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="c92c1-145">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
