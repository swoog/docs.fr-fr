---
title: Styles et modèles ScrollViewer
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ScrollViewer
- states [WPF], ScrollViewer
- styles [WPF], ScrollViewer
- templates [WPF], ScrollViewer
- ControlTemplate [WPF], ScrollViewer
- ScrollViewer [WPF], styles and templates
ms.assetid: dffdd822-ae69-4946-abaf-710860cd65b2
ms.openlocfilehash: 5cd92a4cda40fd850824ae601821dab08c7389e6
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370109"
---
# <a name="scrollviewer-styles-and-templates"></a><span data-ttu-id="96d54-102">Styles et modèles ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="96d54-102">ScrollViewer Styles and Templates</span></span>
<span data-ttu-id="96d54-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ScrollViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="96d54-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span> <span data-ttu-id="96d54-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="96d54-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="96d54-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="96d54-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="scrollviewer-parts"></a><span data-ttu-id="96d54-106">Composants de ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="96d54-106">ScrollViewer Parts</span></span>  
 <span data-ttu-id="96d54-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.ScrollViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="96d54-107">The following table lists the named parts for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
|<span data-ttu-id="96d54-108">Élément</span><span class="sxs-lookup"><span data-stu-id="96d54-108">Part</span></span>|<span data-ttu-id="96d54-109">Type</span><span class="sxs-lookup"><span data-stu-id="96d54-109">Type</span></span>|<span data-ttu-id="96d54-110">Description</span><span class="sxs-lookup"><span data-stu-id="96d54-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="96d54-111">PART_ScrollContentPresenter</span><span class="sxs-lookup"><span data-stu-id="96d54-111">PART_ScrollContentPresenter</span></span>|<xref:System.Windows.Controls.ScrollContentPresenter>|<span data-ttu-id="96d54-112">L’espace réservé pour le contenu dans le <xref:System.Windows.Controls.ScrollViewer>.</span><span class="sxs-lookup"><span data-stu-id="96d54-112">The placeholder for content in the <xref:System.Windows.Controls.ScrollViewer>.</span></span>|  
|<span data-ttu-id="96d54-113">PART_HorizontalScrollBar</span><span class="sxs-lookup"><span data-stu-id="96d54-113">PART_HorizontalScrollBar</span></span>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="96d54-114">Le <xref:System.Windows.Controls.Primitives.ScrollBar> utilisé pour faire défiler le contenu horizontalement.</span><span class="sxs-lookup"><span data-stu-id="96d54-114">The <xref:System.Windows.Controls.Primitives.ScrollBar> used to scroll the content horizontally.</span></span>|  
|<span data-ttu-id="96d54-115">PART_VerticalScrollBar</span><span class="sxs-lookup"><span data-stu-id="96d54-115">PART_VerticalScrollBar</span></span>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="96d54-116">Le <xref:System.Windows.Controls.Primitives.ScrollBar> utilisé pour faire défiler le contenu verticalement.</span><span class="sxs-lookup"><span data-stu-id="96d54-116">The <xref:System.Windows.Controls.Primitives.ScrollBar> used to scroll the content vertically.</span></span>|  
  
## <a name="scrollviewer-states"></a><span data-ttu-id="96d54-117">États de ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="96d54-117">ScrollViewer States</span></span>  
 <span data-ttu-id="96d54-118">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ScrollViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="96d54-118">The following table lists the visual states for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
|<span data-ttu-id="96d54-119">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="96d54-119">VisualState Name</span></span>|<span data-ttu-id="96d54-120">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="96d54-120">VisualStateGroup Name</span></span>|<span data-ttu-id="96d54-121">Description</span><span class="sxs-lookup"><span data-stu-id="96d54-121">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="96d54-122">Valide</span><span class="sxs-lookup"><span data-stu-id="96d54-122">Valid</span></span>|<span data-ttu-id="96d54-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="96d54-123">ValidationStates</span></span>|<span data-ttu-id="96d54-124">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="96d54-124">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="96d54-125">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="96d54-125">InvalidFocused</span></span>|<span data-ttu-id="96d54-126">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="96d54-126">ValidationStates</span></span>|<span data-ttu-id="96d54-127">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="96d54-127">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="96d54-128">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="96d54-128">InvalidUnfocused</span></span>|<span data-ttu-id="96d54-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="96d54-129">ValidationStates</span></span>|<span data-ttu-id="96d54-130">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="96d54-130">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="scrollviewer-controltemplate-example"></a><span data-ttu-id="96d54-131">Exemple de ControlTemplate de ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="96d54-131">ScrollViewer ControlTemplate Example</span></span>  
 <span data-ttu-id="96d54-132">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ScrollViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="96d54-132">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ScrollViewer](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollviewer.xaml#scrollviewer)]  
  
 <span data-ttu-id="96d54-133">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="96d54-133">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="96d54-134">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="96d54-134">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96d54-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96d54-135">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="96d54-136">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="96d54-136">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="96d54-137">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="96d54-137">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="96d54-138">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="96d54-138">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="96d54-139">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="96d54-139">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
