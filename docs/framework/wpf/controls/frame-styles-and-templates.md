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
ms.openlocfilehash: 0d6860af587da89094663779c894689e8a911af8
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57357389"
---
# <a name="frame-styles-and-templates"></a><span data-ttu-id="0259f-102">Styles et modèles Frame</span><span class="sxs-lookup"><span data-stu-id="0259f-102">Frame Styles and Templates</span></span>
<span data-ttu-id="0259f-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0259f-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Frame> control.</span></span> <span data-ttu-id="0259f-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="0259f-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="0259f-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="0259f-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="frame-parts"></a><span data-ttu-id="0259f-106">Parties de frame</span><span class="sxs-lookup"><span data-stu-id="0259f-106">Frame Parts</span></span>  
 <span data-ttu-id="0259f-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0259f-107">The following table lists the named parts for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
|<span data-ttu-id="0259f-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0259f-108">Part</span></span>|<span data-ttu-id="0259f-109">Type</span><span class="sxs-lookup"><span data-stu-id="0259f-109">Type</span></span>|<span data-ttu-id="0259f-110">Description</span><span class="sxs-lookup"><span data-stu-id="0259f-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="0259f-111">PART_FrameCP</span><span class="sxs-lookup"><span data-stu-id="0259f-111">PART_FrameCP</span></span>|<xref:System.Windows.Controls.ContentPresenter>|<span data-ttu-id="0259f-112">La zone de contenu.</span><span class="sxs-lookup"><span data-stu-id="0259f-112">The content area.</span></span>|  
  
## <a name="frame-states"></a><span data-ttu-id="0259f-113">États de frame</span><span class="sxs-lookup"><span data-stu-id="0259f-113">Frame States</span></span>  
 <span data-ttu-id="0259f-114">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0259f-114">The following table lists the visual states for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
|<span data-ttu-id="0259f-115">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="0259f-115">VisualState Name</span></span>|<span data-ttu-id="0259f-116">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="0259f-116">VisualStateGroup Name</span></span>|<span data-ttu-id="0259f-117">Description</span><span class="sxs-lookup"><span data-stu-id="0259f-117">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="0259f-118">Valide</span><span class="sxs-lookup"><span data-stu-id="0259f-118">Valid</span></span>|<span data-ttu-id="0259f-119">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0259f-119">ValidationStates</span></span>|<span data-ttu-id="0259f-120">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="0259f-120">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="0259f-121">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="0259f-121">InvalidFocused</span></span>|<span data-ttu-id="0259f-122">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0259f-122">ValidationStates</span></span>|<span data-ttu-id="0259f-123">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="0259f-123">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="0259f-124">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="0259f-124">InvalidUnfocused</span></span>|<span data-ttu-id="0259f-125">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="0259f-125">ValidationStates</span></span>|<span data-ttu-id="0259f-126">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="0259f-126">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="frame-controltemplate-example"></a><span data-ttu-id="0259f-127">Exemple de ControlTemplate de frame</span><span class="sxs-lookup"><span data-stu-id="0259f-127">Frame ControlTemplate Example</span></span>  
 <span data-ttu-id="0259f-128">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Frame> contrôle.</span><span class="sxs-lookup"><span data-stu-id="0259f-128">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Frame](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/frame.xaml#frame)]  
  
 <span data-ttu-id="0259f-129">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="0259f-129">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="0259f-130">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="0259f-130">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0259f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0259f-131">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="0259f-132">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="0259f-132">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="0259f-133">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="0259f-133">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="0259f-134">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="0259f-134">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="0259f-135">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="0259f-135">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
