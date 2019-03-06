---
title: Styles et modèles GroupBox
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], GroupBox
- parts [WPF], GroupBox
- GroupBox [WPF], styles and templates
- states [WPF], GroupBox
- styles [WPF], GroupBox
- templates [WPF], GroupBox
ms.assetid: 33df7037-0a1b-476f-b9d0-41566a777699
ms.openlocfilehash: 26a935b40ede80aad533c7951f667afa37c57477
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57368958"
---
# <a name="groupbox-styles-and-templates"></a><span data-ttu-id="ff4b3-102">Styles et modèles GroupBox</span><span class="sxs-lookup"><span data-stu-id="ff4b3-102">GroupBox Styles and Templates</span></span>
<a name="introduction"></a> <span data-ttu-id="ff4b3-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.GroupBox> control.</span></span> <span data-ttu-id="ff4b3-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="ff4b3-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
<a name="groupbox_parts"></a>   
## <a name="groupbox-parts"></a><span data-ttu-id="ff4b3-106">Parties de la zone de groupe</span><span class="sxs-lookup"><span data-stu-id="ff4b3-106">GroupBox Parts</span></span>  
 <span data-ttu-id="ff4b3-107">Le <xref:System.Windows.Controls.GroupBox> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-107">The <xref:System.Windows.Controls.GroupBox> control does not have any named parts.</span></span>  
  
<a name="groupbox_states"></a>   
## <a name="groupbox-states"></a><span data-ttu-id="ff4b3-108">États de GroupBox</span><span class="sxs-lookup"><span data-stu-id="ff4b3-108">GroupBox States</span></span>  
 <span data-ttu-id="ff4b3-109">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-109">The following table lists the visual states for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
|<span data-ttu-id="ff4b3-110">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="ff4b3-110">VisualState Name</span></span>|<span data-ttu-id="ff4b3-111">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="ff4b3-111">VisualStateGroup Name</span></span>|<span data-ttu-id="ff4b3-112">Description</span><span class="sxs-lookup"><span data-stu-id="ff4b3-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="ff4b3-113">Valide</span><span class="sxs-lookup"><span data-stu-id="ff4b3-113">Valid</span></span>|<span data-ttu-id="ff4b3-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="ff4b3-114">ValidationStates</span></span>|<span data-ttu-id="ff4b3-115">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="ff4b3-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="ff4b3-116">InvalidFocused</span></span>|<span data-ttu-id="ff4b3-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="ff4b3-117">ValidationStates</span></span>|<span data-ttu-id="ff4b3-118">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="ff4b3-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="ff4b3-119">InvalidUnfocused</span></span>|<span data-ttu-id="ff4b3-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="ff4b3-120">ValidationStates</span></span>|<span data-ttu-id="ff4b3-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
<a name="groupbox_controltemplate_example"></a>   
## <a name="groupbox-controltemplate-example"></a><span data-ttu-id="ff4b3-122">Exemple de ControlTemplate GroupBox</span><span class="sxs-lookup"><span data-stu-id="ff4b3-122">GroupBox ControlTemplate Example</span></span>  
 <span data-ttu-id="ff4b3-123">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.GroupBox> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#GroupBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/groupbox.xaml#groupbox)]  
  
 <span data-ttu-id="ff4b3-124">Le <xref:System.Windows.Controls.ControlTemplate> utilise un ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="ff4b3-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="ff4b3-125">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="ff4b3-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff4b3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff4b3-126">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="ff4b3-127">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="ff4b3-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="ff4b3-128">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="ff4b3-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="ff4b3-129">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="ff4b3-129">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="ff4b3-130">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="ff4b3-130">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
