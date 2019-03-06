---
title: Styles et modèles ToolBar
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], ToolBar
- styles [WPF], ToolBar
- ControlTemplate [WPF], ToolBar
- parts [WPF], ToolBar
- ToolBar [WPF], styles and templates
- templates [WPF], ToolBar
ms.assetid: bd875f46-4690-46f5-81e0-f11a9822484f
ms.openlocfilehash: 3e49683226f8c88a1d6bff678cc978c95a0d6864
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57376908"
---
# <a name="toolbar-styles-and-templates"></a><span data-ttu-id="c6a6b-102">Styles et modèles ToolBar</span><span class="sxs-lookup"><span data-stu-id="c6a6b-102">ToolBar Styles and Templates</span></span>
<span data-ttu-id="c6a6b-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ToolBar> control.</span></span> <span data-ttu-id="c6a6b-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="c6a6b-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="c6a6b-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="toolbar-parts"></a><span data-ttu-id="c6a6b-106">Parties de la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="c6a6b-106">ToolBar Parts</span></span>  
 <span data-ttu-id="c6a6b-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-107">The following table lists the named parts for the <xref:System.Windows.Controls.ToolBar> control.</span></span>  
  
|<span data-ttu-id="c6a6b-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c6a6b-108">Part</span></span>|<span data-ttu-id="c6a6b-109">Type</span><span class="sxs-lookup"><span data-stu-id="c6a6b-109">Type</span></span>|<span data-ttu-id="c6a6b-110">Description</span><span class="sxs-lookup"><span data-stu-id="c6a6b-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="c6a6b-111">PART_ToolBarPanel</span><span class="sxs-lookup"><span data-stu-id="c6a6b-111">PART_ToolBarPanel</span></span>|<xref:System.Windows.Controls.Primitives.ToolBarPanel>|<span data-ttu-id="c6a6b-112">L’objet qui contient les contrôles sur le <xref:System.Windows.Controls.ToolBar>.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-112">The object that contains the controls on the <xref:System.Windows.Controls.ToolBar>.</span></span>|  
|<span data-ttu-id="c6a6b-113">PART_ToolBarOverflowPanel</span><span class="sxs-lookup"><span data-stu-id="c6a6b-113">PART_ToolBarOverflowPanel</span></span>|<xref:System.Windows.Controls.Primitives.ToolBarOverflowPanel>|<span data-ttu-id="c6a6b-114">L’objet qui contient les contrôles qui se trouvent dans la zone de débordement de la <xref:System.Windows.Controls.ToolBar>.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-114">The object that contains the controls that are in the overflow area of the <xref:System.Windows.Controls.ToolBar>.</span></span>|  
  
 <span data-ttu-id="c6a6b-115">Lorsque vous créez un <xref:System.Windows.Controls.ControlTemplate> pour un <xref:System.Windows.Controls.ToolBar>, votre modèle peut contenir un <xref:System.Windows.Controls.ItemsPresenter> au sein d’un <xref:System.Windows.Controls.ScrollViewer>.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-115">When you create a <xref:System.Windows.Controls.ControlTemplate> for a <xref:System.Windows.Controls.ToolBar>, your template might contain an <xref:System.Windows.Controls.ItemsPresenter> within a <xref:System.Windows.Controls.ScrollViewer>.</span></span> <span data-ttu-id="c6a6b-116">(Le <xref:System.Windows.Controls.ItemsPresenter> affiche chaque élément dans le <xref:System.Windows.Controls.ToolBar>; le <xref:System.Windows.Controls.ScrollViewer> permet le défilement dans le contrôle).</span><span class="sxs-lookup"><span data-stu-id="c6a6b-116">(The <xref:System.Windows.Controls.ItemsPresenter> displays each item in the <xref:System.Windows.Controls.ToolBar>; the <xref:System.Windows.Controls.ScrollViewer> enables scrolling within the control).</span></span>  <span data-ttu-id="c6a6b-117">Si le <xref:System.Windows.Controls.ItemsPresenter> n’est pas l’enfant direct de la <xref:System.Windows.Controls.ScrollViewer>, vous devez donner le <xref:System.Windows.Controls.ItemsPresenter> le nom, `ItemsPresenter`.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-117">If the <xref:System.Windows.Controls.ItemsPresenter> is not the direct child of the <xref:System.Windows.Controls.ScrollViewer>, you must give the <xref:System.Windows.Controls.ItemsPresenter> the name, `ItemsPresenter`.</span></span>  
  
## <a name="toolbar-states"></a><span data-ttu-id="c6a6b-118">États de la barre d’outils</span><span class="sxs-lookup"><span data-stu-id="c6a6b-118">ToolBar States</span></span>  
 <span data-ttu-id="c6a6b-119">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-119">The following table lists the visual states for the <xref:System.Windows.Controls.ToolBar> control.</span></span>  
  
|<span data-ttu-id="c6a6b-120">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="c6a6b-120">VisualState Name</span></span>|<span data-ttu-id="c6a6b-121">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="c6a6b-121">VisualStateGroup Name</span></span>|<span data-ttu-id="c6a6b-122">Description</span><span class="sxs-lookup"><span data-stu-id="c6a6b-122">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="c6a6b-123">Valide</span><span class="sxs-lookup"><span data-stu-id="c6a6b-123">Valid</span></span>|<span data-ttu-id="c6a6b-124">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c6a6b-124">ValidationStates</span></span>|<span data-ttu-id="c6a6b-125">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-125">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="c6a6b-126">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="c6a6b-126">InvalidFocused</span></span>|<span data-ttu-id="c6a6b-127">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c6a6b-127">ValidationStates</span></span>|<span data-ttu-id="c6a6b-128">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-128">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="c6a6b-129">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="c6a6b-129">InvalidUnfocused</span></span>|<span data-ttu-id="c6a6b-130">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c6a6b-130">ValidationStates</span></span>|<span data-ttu-id="c6a6b-131">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-131">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="toolbar-controltemplate-example"></a><span data-ttu-id="c6a6b-132">Exemple de ControlTemplate de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="c6a6b-132">ToolBar ControlTemplate Example</span></span>  
 <span data-ttu-id="c6a6b-133">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.ToolBar> contrôle.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-133">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ToolBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ToolBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/toolbar.xaml#toolbar)]  
  
 <span data-ttu-id="c6a6b-134">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="c6a6b-134">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="c6a6b-135">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="c6a6b-135">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6a6b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6a6b-136">See also</span></span>
- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="c6a6b-137">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="c6a6b-137">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="c6a6b-138">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="c6a6b-138">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="c6a6b-139">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="c6a6b-139">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="c6a6b-140">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="c6a6b-140">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
