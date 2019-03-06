---
title: Styles et modèles ToolTip
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ToolTip
- styles [WPF], ToolTip
- states [WPF], ToolTip
- ToolTip [WPF], styles and templates
- ControlTemplate [WPF], ToolTip
- templates [WPF], ToolTip
ms.assetid: 405fe385-4de9-49ee-a448-d8f4d1f740dd
ms.openlocfilehash: 424cfc196474d342f1efdc049350acb71b8fb1eb
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57375361"
---
# <a name="tooltip-styles-and-templates"></a><span data-ttu-id="b3853-102">Styles et modèles ToolTip</span><span class="sxs-lookup"><span data-stu-id="b3853-102">ToolTip Styles and Templates</span></span>
<span data-ttu-id="b3853-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ToolTip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3853-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ToolTip> control.</span></span> <span data-ttu-id="b3853-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="b3853-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="b3853-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="b3853-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="tooltip-parts"></a><span data-ttu-id="b3853-106">Parties de l’info-bulle</span><span class="sxs-lookup"><span data-stu-id="b3853-106">ToolTip Parts</span></span>  
 <span data-ttu-id="b3853-107">Le <xref:System.Windows.Controls.ToolTip> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="b3853-107">The <xref:System.Windows.Controls.ToolTip> control does not have any named parts.</span></span>  
  
## <a name="tooltip-states"></a><span data-ttu-id="b3853-108">États de l’info-bulle</span><span class="sxs-lookup"><span data-stu-id="b3853-108">ToolTip States</span></span>  
 <span data-ttu-id="b3853-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ToolTip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3853-109">The following table lists the visual states for the <xref:System.Windows.Controls.ToolTip> control.</span></span>  
  
|<span data-ttu-id="b3853-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="b3853-110">VisualState Name</span></span>|<span data-ttu-id="b3853-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="b3853-111">VisualStateGroup Name</span></span>|<span data-ttu-id="b3853-112">Description</span><span class="sxs-lookup"><span data-stu-id="b3853-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="b3853-113">Closed</span><span class="sxs-lookup"><span data-stu-id="b3853-113">Closed</span></span>|<span data-ttu-id="b3853-114">OpenStates</span><span class="sxs-lookup"><span data-stu-id="b3853-114">OpenStates</span></span>|<span data-ttu-id="b3853-115">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="b3853-115">The default state.</span></span>|  
|<span data-ttu-id="b3853-116">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="b3853-116">Open</span></span>|<span data-ttu-id="b3853-117">OpenStates</span><span class="sxs-lookup"><span data-stu-id="b3853-117">OpenStates</span></span>|<span data-ttu-id="b3853-118">Le <xref:System.Windows.Controls.ToolTip> est visible.</span><span class="sxs-lookup"><span data-stu-id="b3853-118">The <xref:System.Windows.Controls.ToolTip> is visible.</span></span>|  
|<span data-ttu-id="b3853-119">Valide</span><span class="sxs-lookup"><span data-stu-id="b3853-119">Valid</span></span>|<span data-ttu-id="b3853-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="b3853-120">ValidationStates</span></span>|<span data-ttu-id="b3853-121">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="b3853-121">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="b3853-122">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="b3853-122">InvalidFocused</span></span>|<span data-ttu-id="b3853-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="b3853-123">ValidationStates</span></span>|<span data-ttu-id="b3853-124">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="b3853-124">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="b3853-125">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="b3853-125">InvalidUnfocused</span></span>|<span data-ttu-id="b3853-126">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="b3853-126">ValidationStates</span></span>|<span data-ttu-id="b3853-127">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="b3853-127">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="tooltip-controltemplate-example"></a><span data-ttu-id="b3853-128">Exemple de ControlTemplate info-bulle</span><span class="sxs-lookup"><span data-stu-id="b3853-128">ToolTip ControlTemplate Example</span></span>  
 <span data-ttu-id="b3853-129">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ToolTip> contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3853-129">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ToolTip> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/tooltip.xaml#tooltip)]  
  
 <span data-ttu-id="b3853-130">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="b3853-130">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="b3853-131">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="b3853-131">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3853-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3853-132">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="b3853-133">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="b3853-133">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="b3853-134">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="b3853-134">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="b3853-135">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="b3853-135">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="b3853-136">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="b3853-136">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
