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
ms.openlocfilehash: f948cf2b4f4cd2a4cb73b0cd5fc754240c850b83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770524"
---
# <a name="progressbar-styles-and-templates"></a><span data-ttu-id="747db-102">Styles et modèles ProgressBar</span><span class="sxs-lookup"><span data-stu-id="747db-102">ProgressBar Styles and Templates</span></span>
<span data-ttu-id="747db-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="747db-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ProgressBar> control.</span></span> <span data-ttu-id="747db-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="747db-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="747db-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="747db-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="progressbar-parts"></a><span data-ttu-id="747db-106">Composants de ProgressBar</span><span class="sxs-lookup"><span data-stu-id="747db-106">ProgressBar Parts</span></span>  
 <span data-ttu-id="747db-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="747db-107">The following table lists the named parts for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="747db-108">Élément</span><span class="sxs-lookup"><span data-stu-id="747db-108">Part</span></span>|<span data-ttu-id="747db-109">Type</span><span class="sxs-lookup"><span data-stu-id="747db-109">Type</span></span>|<span data-ttu-id="747db-110">Description</span><span class="sxs-lookup"><span data-stu-id="747db-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="747db-111">PART_Indicator</span><span class="sxs-lookup"><span data-stu-id="747db-111">PART_Indicator</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="747db-112">Objet qui indique la progression.</span><span class="sxs-lookup"><span data-stu-id="747db-112">The object that indicates progress.</span></span>|  
|<span data-ttu-id="747db-113">PART_Track</span><span class="sxs-lookup"><span data-stu-id="747db-113">PART_Track</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="747db-114">Objet qui définit le chemin d’accès de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="747db-114">The object that defines the path of the progress indicator.</span></span>|  
|<span data-ttu-id="747db-115">PART_GlowRect</span><span class="sxs-lookup"><span data-stu-id="747db-115">PART_GlowRect</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="747db-116">Objet qui embellit la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="747db-116">An object that embellishes the progress bar.</span></span>|  
  
## <a name="progressbar-states"></a><span data-ttu-id="747db-117">États de ProgressBar</span><span class="sxs-lookup"><span data-stu-id="747db-117">ProgressBar States</span></span>  
 <span data-ttu-id="747db-118">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="747db-118">The following table lists the visual states for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="747db-119">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="747db-119">VisualState Name</span></span>|<span data-ttu-id="747db-120">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="747db-120">VisualStateGroup Name</span></span>|<span data-ttu-id="747db-121">Description</span><span class="sxs-lookup"><span data-stu-id="747db-121">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="747db-122">Déterminée</span><span class="sxs-lookup"><span data-stu-id="747db-122">Determinate</span></span>|<span data-ttu-id="747db-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="747db-123">CommonStates</span></span>|<span data-ttu-id="747db-124"><xref:System.Windows.Controls.ProgressBar> signale la progression selon le <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="747db-124"><xref:System.Windows.Controls.ProgressBar> reports progress based on the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> property.</span></span>|  
|<span data-ttu-id="747db-125">Indeterminate</span><span class="sxs-lookup"><span data-stu-id="747db-125">Indeterminate</span></span>|<span data-ttu-id="747db-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="747db-126">CommonStates</span></span>|<span data-ttu-id="747db-127"><xref:System.Windows.Controls.ProgressBar> signale la progression générale avec un motif répétitif.</span><span class="sxs-lookup"><span data-stu-id="747db-127"><xref:System.Windows.Controls.ProgressBar> reports generic progress with a repeating pattern.</span></span>|  
|<span data-ttu-id="747db-128">Valide</span><span class="sxs-lookup"><span data-stu-id="747db-128">Valid</span></span>|<span data-ttu-id="747db-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="747db-129">ValidationStates</span></span>|<span data-ttu-id="747db-130">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="747db-130">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="747db-131">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="747db-131">InvalidFocused</span></span>|<span data-ttu-id="747db-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="747db-132">ValidationStates</span></span>|<span data-ttu-id="747db-133">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="747db-133">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="747db-134">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="747db-134">InvalidUnfocused</span></span>|<span data-ttu-id="747db-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="747db-135">ValidationStates</span></span>|<span data-ttu-id="747db-136">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="747db-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="progressbar-controltemplate-example"></a><span data-ttu-id="747db-137">Exemple de ControlTemplate de ProgressBar</span><span class="sxs-lookup"><span data-stu-id="747db-137">ProgressBar ControlTemplate Example</span></span>  
 <span data-ttu-id="747db-138">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ProgressBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="747db-138">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ProgressBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/progressbar.xaml#progressbar)]  
  
 <span data-ttu-id="747db-139">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="747db-139">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="747db-140">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="747db-140">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="747db-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="747db-141">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="747db-142">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="747db-142">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="747db-143">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="747db-143">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="747db-144">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="747db-144">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="747db-145">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="747db-145">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
