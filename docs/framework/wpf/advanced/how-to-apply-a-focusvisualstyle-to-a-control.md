---
title: 'Procédure : Appliquer un FocusVisualStyle à un contrôle'
ms.date: 03/30/2017
helpviewer_keywords:
- properties [WPF], FocusVisualStyle
- FocusVisualStyle property [WPF]
ms.assetid: 363de99e-8ecc-438c-ac4a-f9147432ebd6
ms.openlocfilehash: 53d4984946143c15c4a2b71095529fb5ee7de4b1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59133547"
---
# <a name="how-to-apply-a-focusvisualstyle-to-a-control"></a><span data-ttu-id="14675-102">Procédure : Appliquer un FocusVisualStyle à un contrôle</span><span class="sxs-lookup"><span data-stu-id="14675-102">How to: Apply a FocusVisualStyle to a Control</span></span>
<span data-ttu-id="14675-103">Cet exemple vous montre comment créer un style de focus visuel dans les ressources et appliquer le style à un contrôle, à l’aide de la <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="14675-103">This example shows you how to create a focus visual style in resources and apply the style to a control, using the <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="14675-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="14675-104">Example</span></span>  
 <span data-ttu-id="14675-105">L’exemple suivant définit un style qui crée une composition de contrôle supplémentaire qui s’applique uniquement lorsque ce contrôle est clavier actif dans le [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)].</span><span class="sxs-lookup"><span data-stu-id="14675-105">The following example defines a style that creates additional control compositing that only applies when that control is keyboard focused in the [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)].</span></span> <span data-ttu-id="14675-106">Cela s’effectue en définissant un style avec une <xref:System.Windows.Controls.ControlTemplate>, puis de référencer ce style en tant que ressource lors de la définition du <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="14675-106">This is accomplished by defining a style with a <xref:System.Windows.Controls.ControlTemplate>, then referencing that style as a resource when setting the <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> property.</span></span>  
  
 <span data-ttu-id="14675-107">Un rectangle externe ressemblant à une bordure est placé en dehors de la zone rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="14675-107">An external rectangle resembling a border is placed outside of the rectangular area.</span></span> <span data-ttu-id="14675-108">À défaut de modification, le dimensionnement du style utilise le <xref:System.Windows.FrameworkElement.ActualHeight%2A> et <xref:System.Windows.FrameworkElement.ActualWidth%2A> du contrôle rectangulaire où le style de focus visuel est appliqué.</span><span class="sxs-lookup"><span data-stu-id="14675-108">Unless otherwise modified, the sizing of the style uses the <xref:System.Windows.FrameworkElement.ActualHeight%2A> and <xref:System.Windows.FrameworkElement.ActualWidth%2A> of the rectangular control where the focus visual style is applied.</span></span> <span data-ttu-id="14675-109">Cet exemple définit des valeurs négatives pour le <xref:System.Windows.FrameworkElement.Margin%2A> pour rendre la bordure apparaissent légèrement en dehors du contrôle ayant le focus.</span><span class="sxs-lookup"><span data-stu-id="14675-109">This example sets negative values for the <xref:System.Windows.FrameworkElement.Margin%2A> to make the border appear slightly outside the focused control.</span></span>  
  
 [!code-xaml[FEFocusVisualStyle#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFocusVisualStyle/CS/page1.xaml#xaml)]  
  
 <span data-ttu-id="14675-110">Un <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> est additif pour tout style de modèle de contrôle qui est fourni à partir d’un style explicite ou un style de thème ; le style principal pour un contrôle peut toujours être créé à l’aide un <xref:System.Windows.Controls.ControlTemplate> et en définissant ce style sur la <xref:System.Windows.FrameworkElement.Style%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="14675-110">A <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> is additive to any control template style that comes either from an explicit style or a theme style; the primary style for a control can still be created by using a <xref:System.Windows.Controls.ControlTemplate> and setting that style to the <xref:System.Windows.FrameworkElement.Style%2A> property.</span></span>  
  
 <span data-ttu-id="14675-111">Le focus de styles visuels doivent être utilisés de manière cohérente entre un thème ou une interface utilisateur, au lieu d’utiliser une autre pour chaque élément pouvant être actif.</span><span class="sxs-lookup"><span data-stu-id="14675-111">Focus visual styles should be used consistently across a theme or a UI, rather than using a different one for each focusable element.</span></span> <span data-ttu-id="14675-112">Pour plus d’informations, consultez [focus dans les contrôles et FocusVisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md).</span><span class="sxs-lookup"><span data-stu-id="14675-112">For details, see [Styling for Focus in Controls, and FocusVisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="14675-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14675-113">See also</span></span>

- <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>
- [<span data-ttu-id="14675-114">Application d'un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="14675-114">Styling and Templating</span></span>](../controls/styling-and-templating.md)
- [<span data-ttu-id="14675-115">FocusVisualStyle et application d'un style au focus dans les contrôles</span><span class="sxs-lookup"><span data-stu-id="14675-115">Styling for Focus in Controls, and FocusVisualStyle</span></span>](styling-for-focus-in-controls-and-focusvisualstyle.md)
