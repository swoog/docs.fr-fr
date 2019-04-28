---
title: Styles et modèles DocumentViewer
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], DocumentViewer
- DocumentViewer [WPF], styles and templates
- states [WPF], DocumentViewer
- ControlTemplate [WPF], DocumentViewer
- parts [WPF], DocumentViewer
- styles [WPF], DocumentViewer
ms.assetid: 6bd4ff8f-ea6a-4084-ac58-e7a67446ce1c
ms.openlocfilehash: 4e91a640b36e4793567c9e728fd71ec8ce596743
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61911766"
---
# <a name="documentviewer-styles-and-templates"></a><span data-ttu-id="09198-102">Styles et modèles DocumentViewer</span><span class="sxs-lookup"><span data-stu-id="09198-102">DocumentViewer Styles and Templates</span></span>
<span data-ttu-id="09198-103">Cette rubrique décrit les styles et modèles pour la <xref:System.Windows.Controls.DocumentViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="09198-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span> <span data-ttu-id="09198-104">Vous pouvez modifier la valeur par défaut <xref:System.Windows.Controls.ControlTemplate> pour donner le contrôle une apparence unique.</span><span class="sxs-lookup"><span data-stu-id="09198-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="09198-105">Pour plus d’informations, consultez [Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="09198-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="documentviewer-parts"></a><span data-ttu-id="09198-106">Composants de DocumentViewer</span><span class="sxs-lookup"><span data-stu-id="09198-106">DocumentViewer Parts</span></span>  
 <span data-ttu-id="09198-107">Le tableau suivant répertorie les composants nommés pour le <xref:System.Windows.Controls.DocumentViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="09198-107">The following table lists the named parts for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span>  
  
|<span data-ttu-id="09198-108">Élément</span><span class="sxs-lookup"><span data-stu-id="09198-108">Part</span></span>|<span data-ttu-id="09198-109">Type</span><span class="sxs-lookup"><span data-stu-id="09198-109">Type</span></span>|<span data-ttu-id="09198-110">Description</span><span class="sxs-lookup"><span data-stu-id="09198-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="09198-111">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="09198-111">PART_ContentHost</span></span>|<xref:System.Windows.Controls.ScrollViewer>|<span data-ttu-id="09198-112">Le contenu et la zone de défilement.</span><span class="sxs-lookup"><span data-stu-id="09198-112">The content and scrolling area.</span></span>|  
|<span data-ttu-id="09198-113">PART_FindToolBarHost</span><span class="sxs-lookup"><span data-stu-id="09198-113">PART_FindToolBarHost</span></span>|<xref:System.Windows.Controls.ContentControl>|<span data-ttu-id="09198-114">La zone de recherche, en bas par défaut.</span><span class="sxs-lookup"><span data-stu-id="09198-114">The search box, at the bottom by default.</span></span>|  
  
## <a name="documentviewer-states"></a><span data-ttu-id="09198-115">États de DocumentViewer</span><span class="sxs-lookup"><span data-stu-id="09198-115">DocumentViewer States</span></span>  
 <span data-ttu-id="09198-116">Le tableau suivant répertorie les états visuels pour le <xref:System.Windows.Controls.DocumentViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="09198-116">The following table lists the visual states for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span>  
  
|<span data-ttu-id="09198-117">Nom VisualState</span><span class="sxs-lookup"><span data-stu-id="09198-117">VisualState Name</span></span>|<span data-ttu-id="09198-118">Nom VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="09198-118">VisualStateGroup Name</span></span>|<span data-ttu-id="09198-119">Description</span><span class="sxs-lookup"><span data-stu-id="09198-119">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="09198-120">Valide</span><span class="sxs-lookup"><span data-stu-id="09198-120">Valid</span></span>|<span data-ttu-id="09198-121">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="09198-121">ValidationStates</span></span>|<span data-ttu-id="09198-122">Le contrôle utilise le <xref:System.Windows.Controls.Validation> classe et le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `false`.</span><span class="sxs-lookup"><span data-stu-id="09198-122">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="09198-123">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="09198-123">InvalidFocused</span></span>|<span data-ttu-id="09198-124">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="09198-124">ValidationStates</span></span>|<span data-ttu-id="09198-125">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle a le focus.</span><span class="sxs-lookup"><span data-stu-id="09198-125">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="09198-126">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="09198-126">InvalidUnfocused</span></span>|<span data-ttu-id="09198-127">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="09198-127">ValidationStates</span></span>|<span data-ttu-id="09198-128">Le <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> propriété jointe est `true` a le contrôle n’a pas le focus.</span><span class="sxs-lookup"><span data-stu-id="09198-128">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="documentviewer-controltemplate-example"></a><span data-ttu-id="09198-129">Exemple de ControlTemplate DocumentViewer</span><span class="sxs-lookup"><span data-stu-id="09198-129">DocumentViewer ControlTemplate Example</span></span>  
 <span data-ttu-id="09198-130">L’exemple suivant montre comment définir un <xref:System.Windows.Controls.ControlTemplate> pour la <xref:System.Windows.Controls.DocumentViewer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="09198-130">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#DocumentViewer](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/documentviewer.xaml#documentviewer)]  
  
 <span data-ttu-id="09198-131">L’exemple précédent utilise une ou plusieurs des ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="09198-131">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="09198-132">Pour voir l’exemple complet, consultez [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating) (Exemple de style avec ControlTemplates).</span><span class="sxs-lookup"><span data-stu-id="09198-132">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09198-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09198-133">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="09198-134">Styles et modèles Control</span><span class="sxs-lookup"><span data-stu-id="09198-134">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="09198-135">Personnalisation des contrôles</span><span class="sxs-lookup"><span data-stu-id="09198-135">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="09198-136">Application d’un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="09198-136">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="09198-137">Personnalisation de l’apparence d’un contrôle existant en créant un ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="09198-137">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](customizing-the-appearance-of-an-existing-control.md)
