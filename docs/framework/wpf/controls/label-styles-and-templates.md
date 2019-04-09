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
ms.openlocfilehash: d2bb348fc9c0348fd8093452e022df7ab4e0b3f2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59137083"
---
# <a name="label-styles-and-templates"></a><span data-ttu-id="abcfe-102">Styles et modèles Label</span><span class="sxs-lookup"><span data-stu-id="abcfe-102">Label Styles and Templates</span></span>
<span data-ttu-id="abcfe-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="abcfe-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Label> control.</span></span> <span data-ttu-id="abcfe-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="abcfe-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="abcfe-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="abcfe-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="label-parts"></a><span data-ttu-id="abcfe-106">Parties de l’étiquette</span><span class="sxs-lookup"><span data-stu-id="abcfe-106">Label Parts</span></span>  
 <span data-ttu-id="abcfe-107">Le <xref:System.Windows.Controls.Label> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="abcfe-107">The <xref:System.Windows.Controls.Label> control does not have any named parts.</span></span>  
  
## <a name="label-states"></a><span data-ttu-id="abcfe-108">États de l’étiquette</span><span class="sxs-lookup"><span data-stu-id="abcfe-108">Label States</span></span>  
 <span data-ttu-id="abcfe-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="abcfe-109">The following table lists the visual states for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
|<span data-ttu-id="abcfe-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="abcfe-110">VisualState Name</span></span>|<span data-ttu-id="abcfe-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="abcfe-111">VisualStateGroup Name</span></span>|<span data-ttu-id="abcfe-112">Description</span><span class="sxs-lookup"><span data-stu-id="abcfe-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="abcfe-113">Valide</span><span class="sxs-lookup"><span data-stu-id="abcfe-113">Valid</span></span>|<span data-ttu-id="abcfe-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="abcfe-114">ValidationStates</span></span>|<span data-ttu-id="abcfe-115">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="abcfe-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="abcfe-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="abcfe-116">InvalidFocused</span></span>|<span data-ttu-id="abcfe-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="abcfe-117">ValidationStates</span></span>|<span data-ttu-id="abcfe-118">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="abcfe-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="abcfe-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="abcfe-119">InvalidUnfocused</span></span>|<span data-ttu-id="abcfe-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="abcfe-120">ValidationStates</span></span>|<span data-ttu-id="abcfe-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="abcfe-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="label-controltemplate-example"></a><span data-ttu-id="abcfe-122">Exemple de ControlTemplate d’étiquette</span><span class="sxs-lookup"><span data-stu-id="abcfe-122">Label ControlTemplate Example</span></span>  
 <span data-ttu-id="abcfe-123">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="abcfe-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Label](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/label.xaml#label)]  
  
 <span data-ttu-id="abcfe-124">Le <xref:System.Windows.Controls.ControlTemplate> utilise un ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="abcfe-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="abcfe-125">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="abcfe-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abcfe-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abcfe-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="abcfe-127">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="abcfe-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="abcfe-128">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="abcfe-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="abcfe-129">Application d'un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="abcfe-129">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="abcfe-130">Personnalisation de l'apparence d'un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="abcfe-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
