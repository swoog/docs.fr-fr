---
title: Styles et modèles Label
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], Label
- parts [WPF], Label
- ControlTemplate [WPF], Label
- styles [WPF], Label
- Label [WPF], styles and templates
- states [WPF], Label
ms.assetid: c1d5359a-8e4a-4925-ab3e-e92bf6694859
ms.openlocfilehash: 9d2f5e4d886d8fc46ecb14dd4f1bda67debdae97
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
ms.locfileid: "34457642"
---
# <a name="label-styles-and-templates"></a><span data-ttu-id="822de-102">Styles et modèles Label</span><span class="sxs-lookup"><span data-stu-id="822de-102">Label Styles and Templates</span></span>
<span data-ttu-id="822de-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="822de-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Label> control.</span></span> <span data-ttu-id="822de-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner une apparence unique au contrôle.</span><span class="sxs-lookup"><span data-stu-id="822de-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="822de-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="822de-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="label-parts"></a><span data-ttu-id="822de-106">Parties de l’étiquette</span><span class="sxs-lookup"><span data-stu-id="822de-106">Label Parts</span></span>  
 <span data-ttu-id="822de-107">Le <xref:System.Windows.Controls.Label> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="822de-107">The <xref:System.Windows.Controls.Label> control does not have any named parts.</span></span>  
  
## <a name="label-states"></a><span data-ttu-id="822de-108">États d’étiquette</span><span class="sxs-lookup"><span data-stu-id="822de-108">Label States</span></span>  
 <span data-ttu-id="822de-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="822de-109">The following table lists the visual states for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
|<span data-ttu-id="822de-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="822de-110">VisualState Name</span></span>|<span data-ttu-id="822de-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="822de-111">VisualStateGroup Name</span></span>|<span data-ttu-id="822de-112">Description</span><span class="sxs-lookup"><span data-stu-id="822de-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="822de-113">Valide</span><span class="sxs-lookup"><span data-stu-id="822de-113">Valid</span></span>|<span data-ttu-id="822de-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="822de-114">ValidationStates</span></span>|<span data-ttu-id="822de-115">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="822de-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="822de-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="822de-116">InvalidFocused</span></span>|<span data-ttu-id="822de-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="822de-117">ValidationStates</span></span>|<span data-ttu-id="822de-118">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="822de-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="822de-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="822de-119">InvalidUnfocused</span></span>|<span data-ttu-id="822de-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="822de-120">ValidationStates</span></span>|<span data-ttu-id="822de-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="822de-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="label-controltemplate-example"></a><span data-ttu-id="822de-122">Exemple de ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="822de-122">Label ControlTemplate Example</span></span>  
 <span data-ttu-id="822de-123">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="822de-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Label](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/label.xaml#label)]  
  
 <span data-ttu-id="822de-124">Le <xref:System.Windows.Controls.ControlTemplate> utilise un ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="822de-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="822de-125">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="822de-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="822de-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="822de-126">See Also</span></span>  
 <xref:System.Windows.FrameworkElement.Style%2A>  
 <xref:System.Windows.Controls.ControlTemplate>  
 [<span data-ttu-id="822de-127">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="822de-127">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)  
 [<span data-ttu-id="822de-128">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="822de-128">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)  
 [<span data-ttu-id="822de-129">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="822de-129">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)  
 [<span data-ttu-id="822de-130">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="822de-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
