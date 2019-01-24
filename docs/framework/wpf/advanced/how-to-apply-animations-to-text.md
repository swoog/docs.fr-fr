---
title: 'Procédure : Appliquer des animations à du texte'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], animations
- animation [WPF], text
ms.assetid: eec3d26c-0a21-420f-8012-671621c47089
ms.openlocfilehash: 56336c45639168c6432b92fe555c6d37448cb7cd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720507"
---
# <a name="how-to-apply-animations-to-text"></a><span data-ttu-id="2ba87-102">Procédure : Appliquer des animations à du texte</span><span class="sxs-lookup"><span data-stu-id="2ba87-102">How to: Apply Animations to Text</span></span>
<span data-ttu-id="2ba87-103">Les animations peuvent modifier l’affichage et l’apparence du texte dans votre application.</span><span class="sxs-lookup"><span data-stu-id="2ba87-103">Animations can alter the display and appearance of text in your application.</span></span> <span data-ttu-id="2ba87-104">Les exemples suivants utilisent différents types d’animations pour changer l’affichage du texte dans un <xref:System.Windows.Controls.TextBlock> contrôle.</span><span class="sxs-lookup"><span data-stu-id="2ba87-104">The following examples use different types of animations to affect the display of text in a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ba87-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="2ba87-105">Example</span></span>  
 <span data-ttu-id="2ba87-106">L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer la largeur du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="2ba87-106">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the width of the text block.</span></span> <span data-ttu-id="2ba87-107">La valeur de largeur change pour passer de la largeur du bloc de texte à 0 sur une durée de 10 secondes, puis les valeurs de largeur sont inversées et la procédure continue.</span><span class="sxs-lookup"><span data-stu-id="2ba87-107">The width value changes from the width of the text block to 0 over a duration of 10 seconds, and then reverses the width values and continues.</span></span> <span data-ttu-id="2ba87-108">Ce type d’animation crée un effet de balayage.</span><span class="sxs-lookup"><span data-stu-id="2ba87-108">This type of animation creates a wipe effect.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample1)]  
  
 <span data-ttu-id="2ba87-109">L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour animer l’opacité du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="2ba87-109">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the opacity of the text block.</span></span> <span data-ttu-id="2ba87-110">La valeur d’opacité passe de 1.0 à 0 sur une durée de 5 secondes, puis les valeurs d’opacité sont inversées et la procédure continue.</span><span class="sxs-lookup"><span data-stu-id="2ba87-110">The opacity value changes from 1.0 to 0 over a duration of 5 seconds, and then reverses the opacity values and continues.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample2)]  
  
 <span data-ttu-id="2ba87-111">Le diagramme suivant montre l’effet de la <xref:System.Windows.Controls.TextBlock> contrôle quand son opacité passe de `1.00` à `0.00` pendant l’intervalle de 5 secondes défini par le <xref:System.Windows.Media.Animation.Timeline.Duration%2A>.</span><span class="sxs-lookup"><span data-stu-id="2ba87-111">The following diagram shows the effect of the <xref:System.Windows.Controls.TextBlock> control changing its opacity from `1.00` to `0.00` during the 5-second interval defined by the <xref:System.Windows.Media.Animation.Timeline.Duration%2A>.</span></span>  
  
 <span data-ttu-id="2ba87-112">![Modification du texte Opacité de 1.00 à 0.00](../../../../docs/framework/wpf/advanced/media/fadedtext01.png "FadedText01")</span><span class="sxs-lookup"><span data-stu-id="2ba87-112">![Text changing opacity from 1.00 to 0.00](../../../../docs/framework/wpf/advanced/media/fadedtext01.png "FadedText01")</span></span>  
<span data-ttu-id="2ba87-113">Opacité du texte variant de 1.00 à 0.00</span><span class="sxs-lookup"><span data-stu-id="2ba87-113">Text Opacity changing from 1.00 to 0.00</span></span>  
  
 <span data-ttu-id="2ba87-114">L’exemple suivant utilise un <xref:System.Windows.Media.Animation.ColorAnimation> pour animer la couleur de premier plan du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="2ba87-114">The following example uses a <xref:System.Windows.Media.Animation.ColorAnimation> to animate the foreground color of the text block.</span></span> <span data-ttu-id="2ba87-115">La valeur de la couleur de premier plan passe d’une couleur à une autre sur une durée de 5 secondes, puis les valeurs de couleur sont inversées et la procédure continue.</span><span class="sxs-lookup"><span data-stu-id="2ba87-115">The foreground color value changes from one color to a second color over a duration of 5 seconds, and then reverses the color values and continues.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample3)]  
  
 <span data-ttu-id="2ba87-116">L’exemple suivant utilise un <xref:System.Windows.Media.Animation.DoubleAnimation> pour faire pivoter le bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="2ba87-116">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to rotate the text block.</span></span> <span data-ttu-id="2ba87-117">Le bloc de texte effectue une rotation complète sur une durée de 20 secondes, puis la procédure de rotation se répète.</span><span class="sxs-lookup"><span data-stu-id="2ba87-117">The text block performs a full rotation over a duration of 20 seconds, and then continues to repeat the rotation.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample4)]  
  
## <a name="see-also"></a><span data-ttu-id="2ba87-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ba87-118">See also</span></span>
- [<span data-ttu-id="2ba87-119">Vue d’ensemble de l’animation</span><span class="sxs-lookup"><span data-stu-id="2ba87-119">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
