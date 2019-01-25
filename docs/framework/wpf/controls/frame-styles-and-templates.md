---
title: Styles et modèles Frame
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], Frame
- templates [WPF], Frame
- ControlTemplate [WPF], Frame
- Frame [WPF], styles and templates
- states [WPF], Frame
- styles [WPF], Frame
ms.assetid: a01c32e2-c951-46a0-a82f-2614ca241f0b
ms.openlocfilehash: fbe49ae98e0fe281500ae37d53a3d47ff1d0b03a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54700267"
---
# <a name="frame-styles-and-templates"></a><span data-ttu-id="1876a-102">Styles et modèles Frame</span><span class="sxs-lookup"><span data-stu-id="1876a-102">Frame Styles and Templates</span></span>
<span data-ttu-id="1876a-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1876a-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Frame> control.</span></span> <span data-ttu-id="1876a-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="1876a-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="1876a-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="1876a-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="frame-parts"></a><span data-ttu-id="1876a-106">Parties de frame</span><span class="sxs-lookup"><span data-stu-id="1876a-106">Frame Parts</span></span>  
 <span data-ttu-id="1876a-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1876a-107">The following table lists the named parts for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
|<span data-ttu-id="1876a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1876a-108">Part</span></span>|<span data-ttu-id="1876a-109">Type</span><span class="sxs-lookup"><span data-stu-id="1876a-109">Type</span></span>|<span data-ttu-id="1876a-110">Description</span><span class="sxs-lookup"><span data-stu-id="1876a-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="1876a-111">PART_FrameCP</span><span class="sxs-lookup"><span data-stu-id="1876a-111">PART_FrameCP</span></span>|<xref:System.Windows.Controls.ContentPresenter>|<span data-ttu-id="1876a-112">La zone de contenu.</span><span class="sxs-lookup"><span data-stu-id="1876a-112">The content area.</span></span>|  
  
## <a name="frame-states"></a><span data-ttu-id="1876a-113">États de frame</span><span class="sxs-lookup"><span data-stu-id="1876a-113">Frame States</span></span>  
 <span data-ttu-id="1876a-114">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1876a-114">The following table lists the visual states for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
|<span data-ttu-id="1876a-115">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="1876a-115">VisualState Name</span></span>|<span data-ttu-id="1876a-116">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="1876a-116">VisualStateGroup Name</span></span>|<span data-ttu-id="1876a-117">Description</span><span class="sxs-lookup"><span data-stu-id="1876a-117">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="1876a-118">Valide</span><span class="sxs-lookup"><span data-stu-id="1876a-118">Valid</span></span>|<span data-ttu-id="1876a-119">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1876a-119">ValidationStates</span></span>|<span data-ttu-id="1876a-120">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="1876a-120">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="1876a-121">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="1876a-121">InvalidFocused</span></span>|<span data-ttu-id="1876a-122">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1876a-122">ValidationStates</span></span>|<span data-ttu-id="1876a-123">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="1876a-123">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="1876a-124">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="1876a-124">InvalidUnfocused</span></span>|<span data-ttu-id="1876a-125">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="1876a-125">ValidationStates</span></span>|<span data-ttu-id="1876a-126">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="1876a-126">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="frame-controltemplate-example"></a><span data-ttu-id="1876a-127">Exemple de ControlTemplate de frame</span><span class="sxs-lookup"><span data-stu-id="1876a-127">Frame ControlTemplate Example</span></span>  
 <span data-ttu-id="1876a-128">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="1876a-128">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Frame](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/frame.xaml#frame)]  
  
 <span data-ttu-id="1876a-129">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="1876a-129">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="1876a-130">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="1876a-130">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1876a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1876a-131">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="1876a-132">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="1876a-132">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)
- [<span data-ttu-id="1876a-133">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="1876a-133">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)
- [<span data-ttu-id="1876a-134">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="1876a-134">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)
- [<span data-ttu-id="1876a-135">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="1876a-135">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
