---
title: Styles et modèles NavigationWindow
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], NavigationWindow
- NavigationWindow [WPF], styles and templates
- ControlTemplate [WPF], NavigationWindow
- parts [WPF], NavigationWindow
- styles [WPF], NavigationWindow
- templates [WPF], NavigationWindow
ms.assetid: 3656055e-3222-43c8-b868-fd0c90cc31a3
ms.openlocfilehash: 32d8aac99d40693e66c7b52a6c7d2c116d2f3baf
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225805"
---
# <a name="navigationwindow-styles-and-templates"></a><span data-ttu-id="d988e-102">Styles et modèles NavigationWindow</span><span class="sxs-lookup"><span data-stu-id="d988e-102">NavigationWindow Styles and Templates</span></span>
<span data-ttu-id="d988e-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Navigation.NavigationWindow> contrôle.</span><span class="sxs-lookup"><span data-stu-id="d988e-103">This topic describes the styles and templates for the <xref:System.Windows.Navigation.NavigationWindow> control.</span></span> <span data-ttu-id="d988e-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="d988e-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="d988e-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="d988e-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="navigationwindow-parts"></a><span data-ttu-id="d988e-106">Éléments de NavigationWindow</span><span class="sxs-lookup"><span data-stu-id="d988e-106">NavigationWindow Parts</span></span>  
 <span data-ttu-id="d988e-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Navigation.NavigationWindow> contrôle.</span><span class="sxs-lookup"><span data-stu-id="d988e-107">The following table lists the named parts for the <xref:System.Windows.Navigation.NavigationWindow> control.</span></span>  
  
|<span data-ttu-id="d988e-108">Élément</span><span class="sxs-lookup"><span data-stu-id="d988e-108">Part</span></span>|<span data-ttu-id="d988e-109">Type</span><span class="sxs-lookup"><span data-stu-id="d988e-109">Type</span></span>|<span data-ttu-id="d988e-110">Description</span><span class="sxs-lookup"><span data-stu-id="d988e-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="d988e-111">PART_NavWinCP</span><span class="sxs-lookup"><span data-stu-id="d988e-111">PART_NavWinCP</span></span>|<xref:System.Windows.Controls.ContentPresenter>|<span data-ttu-id="d988e-112">La zone pour le contenu.</span><span class="sxs-lookup"><span data-stu-id="d988e-112">The area for the content.</span></span>|  
  
## <a name="navigationwindow-states"></a><span data-ttu-id="d988e-113">États de NavigationWindow</span><span class="sxs-lookup"><span data-stu-id="d988e-113">NavigationWindow States</span></span>  
 <span data-ttu-id="d988e-114">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Navigation.NavigationWindow> contrôle.</span><span class="sxs-lookup"><span data-stu-id="d988e-114">The following table lists the visual states for the <xref:System.Windows.Navigation.NavigationWindow> control.</span></span>  
  
|<span data-ttu-id="d988e-115">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="d988e-115">VisualState Name</span></span>|<span data-ttu-id="d988e-116">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="d988e-116">VisualStateGroup Name</span></span>|<span data-ttu-id="d988e-117">Description</span><span class="sxs-lookup"><span data-stu-id="d988e-117">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="d988e-118">Valide</span><span class="sxs-lookup"><span data-stu-id="d988e-118">Valid</span></span>|<span data-ttu-id="d988e-119">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="d988e-119">ValidationStates</span></span>|<span data-ttu-id="d988e-120">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="d988e-120">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="d988e-121">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="d988e-121">InvalidFocused</span></span>|<span data-ttu-id="d988e-122">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="d988e-122">ValidationStates</span></span>|<span data-ttu-id="d988e-123">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="d988e-123">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="d988e-124">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="d988e-124">InvalidUnfocused</span></span>|<span data-ttu-id="d988e-125">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="d988e-125">ValidationStates</span></span>|<span data-ttu-id="d988e-126">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="d988e-126">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="navigationwindow-controltemplate-example"></a><span data-ttu-id="d988e-127">Exemple de ControlTemplate NavigationWindow</span><span class="sxs-lookup"><span data-stu-id="d988e-127">NavigationWindow ControlTemplate Example</span></span>  
 <span data-ttu-id="d988e-128">Bien que cet exemple contienne tous les éléments qui sont définies dans le <xref:System.Windows.Controls.ControlTemplate> d’un <xref:System.Windows.Navigation.NavigationWindow> par défaut, les valeurs spécifiques doivent être imaginées comme exemples.</span><span class="sxs-lookup"><span data-stu-id="d988e-128">Although this example contains all of the elements that are defined in the <xref:System.Windows.Controls.ControlTemplate> of a <xref:System.Windows.Navigation.NavigationWindow> by default, the specific values should be thought of as examples.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#NavigationWindow](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/navigationwindow.xaml#navigationwindow)]  
  
 <span data-ttu-id="d988e-129">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="d988e-129">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ResizeGrip](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/resizegrip.xaml#resizegrip)]  
[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="d988e-130">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="d988e-130">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d988e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d988e-131">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="d988e-132">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="d988e-132">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="d988e-133">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="d988e-133">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="d988e-134">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="d988e-134">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="d988e-135">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="d988e-135">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
