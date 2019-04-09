---
title: Styles et modèles ContextMenu
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], ContextMenu
- parts [WPF], ContextMenu
- ContextMenu [WPF], styles and templates
- styles [WPF], ContextMenu
- ControlTemplate [WPF], ContextMenu
- states [WPF], ContextMenu
ms.assetid: 342d1f17-c406-4f94-8f55-867c5f3ea511
ms.openlocfilehash: 6650d5a7be8ebe8fc2dcd7af7c854da669de87f3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59123043"
---
# <a name="contextmenu-styles-and-templates"></a><span data-ttu-id="44513-102">Styles et modèles ContextMenu</span><span class="sxs-lookup"><span data-stu-id="44513-102">ContextMenu Styles and Templates</span></span>
<span data-ttu-id="44513-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ContextMenu> contrôle.</span><span class="sxs-lookup"><span data-stu-id="44513-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ContextMenu> control.</span></span> <span data-ttu-id="44513-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="44513-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="44513-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="44513-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="contextmenu-parts"></a><span data-ttu-id="44513-106">Éléments de ContextMenu</span><span class="sxs-lookup"><span data-stu-id="44513-106">ContextMenu Parts</span></span>  
 <span data-ttu-id="44513-107">Le <xref:System.Windows.Controls.ContextMenu> contrôle n’a pas de composants nommés.</span><span class="sxs-lookup"><span data-stu-id="44513-107">The <xref:System.Windows.Controls.ContextMenu> control does not have any named parts.</span></span>  
  
 <span data-ttu-id="44513-108">Lorsque vous créez un <xref:System.Windows.Controls.ControlTemplate> pour un <xref:System.Windows.Controls.ContextMenu>, votre modèle peut contenir un <xref:System.Windows.Controls.ItemsPresenter> au sein d’un <xref:System.Windows.Controls.ScrollViewer>.</span><span class="sxs-lookup"><span data-stu-id="44513-108">When you create a <xref:System.Windows.Controls.ControlTemplate> for a <xref:System.Windows.Controls.ContextMenu>, your template might contain an <xref:System.Windows.Controls.ItemsPresenter> within a <xref:System.Windows.Controls.ScrollViewer>.</span></span> <span data-ttu-id="44513-109">(Le <xref:System.Windows.Controls.ItemsPresenter> affiche chaque élément dans le <xref:System.Windows.Controls.ContextMenu>; le <xref:System.Windows.Controls.ScrollViewer> permet le défilement dans le contrôle).</span><span class="sxs-lookup"><span data-stu-id="44513-109">(The <xref:System.Windows.Controls.ItemsPresenter> displays each item in the <xref:System.Windows.Controls.ContextMenu>; the <xref:System.Windows.Controls.ScrollViewer> enables scrolling within the control).</span></span>  <span data-ttu-id="44513-110">Si le <xref:System.Windows.Controls.ItemsPresenter> n’est pas l’enfant direct de la <xref:System.Windows.Controls.ScrollViewer>, vous devez donner le <xref:System.Windows.Controls.ItemsPresenter> le nom, `ItemsPresenter`.</span><span class="sxs-lookup"><span data-stu-id="44513-110">If the <xref:System.Windows.Controls.ItemsPresenter> is not the direct child of the <xref:System.Windows.Controls.ScrollViewer>, you must give the <xref:System.Windows.Controls.ItemsPresenter> the name, `ItemsPresenter`.</span></span>  
  
## <a name="contextmenu-states"></a><span data-ttu-id="44513-111">États du menu contextuel</span><span class="sxs-lookup"><span data-stu-id="44513-111">ContextMenu States</span></span>  
 <span data-ttu-id="44513-112">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ContextMenu> contrôle.</span><span class="sxs-lookup"><span data-stu-id="44513-112">The following table lists the visual states for the <xref:System.Windows.Controls.ContextMenu> control.</span></span>  
  
|<span data-ttu-id="44513-113">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="44513-113">VisualState Name</span></span>|<span data-ttu-id="44513-114">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="44513-114">VisualStateGroup Name</span></span>|<span data-ttu-id="44513-115">Description</span><span class="sxs-lookup"><span data-stu-id="44513-115">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="44513-116">Valide</span><span class="sxs-lookup"><span data-stu-id="44513-116">Valid</span></span>|<span data-ttu-id="44513-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="44513-117">ValidationStates</span></span>|<span data-ttu-id="44513-118">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="44513-118">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="44513-119">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="44513-119">InvalidFocused</span></span>|<span data-ttu-id="44513-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="44513-120">ValidationStates</span></span>|<span data-ttu-id="44513-121">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="44513-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="44513-122">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="44513-122">InvalidUnfocused</span></span>|<span data-ttu-id="44513-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="44513-123">ValidationStates</span></span>|<span data-ttu-id="44513-124">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="44513-124">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="contextmenu-controltemplate-example"></a><span data-ttu-id="44513-125">Exemple de ControlTemplate ContextMenu</span><span class="sxs-lookup"><span data-stu-id="44513-125">ContextMenu ControlTemplate Example</span></span>  
 <span data-ttu-id="44513-126">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ContextMenu> contrôle.</span><span class="sxs-lookup"><span data-stu-id="44513-126">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ContextMenu> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ContextMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/menu.xaml#contextmenu)]  
  
 <span data-ttu-id="44513-127">Le <xref:System.Windows.Controls.ControlTemplate> utilise les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="44513-127">The <xref:System.Windows.Controls.ControlTemplate> uses the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="44513-128">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="44513-128">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44513-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44513-129">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="44513-130">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="44513-130">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="44513-131">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="44513-131">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="44513-132">Application d'un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="44513-132">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="44513-133">Personnalisation de l'apparence d'un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="44513-133">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
