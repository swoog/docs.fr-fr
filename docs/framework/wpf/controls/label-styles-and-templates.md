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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137083"
---
# <a name="label-styles-and-templates"></a><span data-ttu-id="71270-102">Styles et modèles Label</span><span class="sxs-lookup"><span data-stu-id="71270-102">Label Styles and Templates</span></span>
<span data-ttu-id="71270-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="71270-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Label> control.</span></span> <span data-ttu-id="71270-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="71270-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="71270-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="71270-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="label-parts"></a><span data-ttu-id="71270-106">Parties de l’étiquette</span><span class="sxs-lookup"><span data-stu-id="71270-106">Label Parts</span></span>  
 <span data-ttu-id="71270-107">Le <xref:System.Windows.Controls.Label> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="71270-107">The <xref:System.Windows.Controls.Label> control does not have any named parts.</span></span>  
  
## <a name="label-states"></a><span data-ttu-id="71270-108">États de l’étiquette</span><span class="sxs-lookup"><span data-stu-id="71270-108">Label States</span></span>  
 <span data-ttu-id="71270-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="71270-109">The following table lists the visual states for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
|<span data-ttu-id="71270-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="71270-110">VisualState Name</span></span>|<span data-ttu-id="71270-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="71270-111">VisualStateGroup Name</span></span>|<span data-ttu-id="71270-112">Description</span><span class="sxs-lookup"><span data-stu-id="71270-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="71270-113">Valide</span><span class="sxs-lookup"><span data-stu-id="71270-113">Valid</span></span>|<span data-ttu-id="71270-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="71270-114">ValidationStates</span></span>|<span data-ttu-id="71270-115">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="71270-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="71270-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="71270-116">InvalidFocused</span></span>|<span data-ttu-id="71270-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="71270-117">ValidationStates</span></span>|<span data-ttu-id="71270-118">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="71270-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="71270-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="71270-119">InvalidUnfocused</span></span>|<span data-ttu-id="71270-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="71270-120">ValidationStates</span></span>|<span data-ttu-id="71270-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="71270-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="label-controltemplate-example"></a><span data-ttu-id="71270-122">Exemple de ControlTemplate d’étiquette</span><span class="sxs-lookup"><span data-stu-id="71270-122">Label ControlTemplate Example</span></span>  
 <span data-ttu-id="71270-123">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.Label> contrôle.</span><span class="sxs-lookup"><span data-stu-id="71270-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Label](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/label.xaml#label)]  
  
 <span data-ttu-id="71270-124">Le <xref:System.Windows.Controls.ControlTemplate> utilise un ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="71270-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="71270-125">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="71270-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71270-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71270-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="71270-127">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="71270-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="71270-128">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="71270-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="71270-129">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="71270-129">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="71270-130">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="71270-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
