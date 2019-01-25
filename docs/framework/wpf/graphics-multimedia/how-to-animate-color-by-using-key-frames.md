---
title: "Procédure : Animer une couleur à l'aide d'images clés"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [WPF], animating with key frames
- animation [WPF], colors with key frames
- key frames [WPF], animating colors with
ms.assetid: ab04ffa6-4de9-4d5b-a3b4-4e35d5b2ef35
ms.openlocfilehash: 8d7dbe70f25b4712d1384a751a02053fb7f287ee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54645091"
---
# <a name="how-to-animate-color-by-using-key-frames"></a><span data-ttu-id="f35ea-102">Procédure : Animer une couleur à l'aide d'images clés</span><span class="sxs-lookup"><span data-stu-id="f35ea-102">How to: Animate Color by Using Key Frames</span></span>
<span data-ttu-id="f35ea-103">Cet exemple montre comment animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> d’un <xref:System.Windows.Media.SolidColorBrush> à l’aide d’images clés.</span><span class="sxs-lookup"><span data-stu-id="f35ea-103">This example shows how to animate the <xref:System.Windows.Media.SolidColorBrush.Color%2A> of a <xref:System.Windows.Media.SolidColorBrush> by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f35ea-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f35ea-104">Example</span></span>  
 <span data-ttu-id="f35ea-105">L’exemple suivant utilise le <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.SolidColorBrush.Color%2A> propriété d’un <xref:System.Windows.Media.SolidColorBrush>.</span><span class="sxs-lookup"><span data-stu-id="f35ea-105">The following example uses the <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.SolidColorBrush.Color%2A> property of a <xref:System.Windows.Media.SolidColorBrush>.</span></span> <span data-ttu-id="f35ea-106">Cette animation utilise trois images clés de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="f35ea-106">This animation uses three key frames in the following manner:</span></span>  
  
1.  <span data-ttu-id="f35ea-107">Pendant les deux premières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.LinearColorKeyFrame> classe à modifier progressivement la couleur du vert au rouge.</span><span class="sxs-lookup"><span data-stu-id="f35ea-107">During the first two seconds, uses an instance of the <xref:System.Windows.Media.Animation.LinearColorKeyFrame> class to gradually change the color from green to red.</span></span> <span data-ttu-id="f35ea-108">Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearColorKeyFrame> créent une transition linéaire fluide entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f35ea-108">Linear key frames like <xref:System.Windows.Media.Animation.LinearColorKeyFrame> create a smooth linear transition between values.</span></span>  
  
2.  <span data-ttu-id="f35ea-109">Lors de la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> classe pour rapidement changer la couleur du rouge au jaune.</span><span class="sxs-lookup"><span data-stu-id="f35ea-109">During the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> class to quickly change the color from red to yellow.</span></span> <span data-ttu-id="f35ea-110">Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> créent des changements soudains entre les valeurs, autrement dit, la modification de couleur dans cette partie de l’animation se produit rapidement et n’est pas subtile.</span><span class="sxs-lookup"><span data-stu-id="f35ea-110">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteColorKeyFrame> create sudden changes between values, that is, the color change in this part of the animation occurs quickly and is not subtle.</span></span>  
  
3.  <span data-ttu-id="f35ea-111">Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineColorKeyFrame> classe pour modifier la couleur à nouveau, cette fois du jaune au vert.</span><span class="sxs-lookup"><span data-stu-id="f35ea-111">During the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineColorKeyFrame> class to change the color again—this time from yellow back to green.</span></span> <span data-ttu-id="f35ea-112">Les images clés spline comme <xref:System.Windows.Media.Animation.SplineColorKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineColorKeyFrame.KeySpline%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="f35ea-112">Spline key frames like <xref:System.Windows.Media.Animation.SplineColorKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplineColorKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="f35ea-113">Dans cet exemple, le changement de couleur commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.</span><span class="sxs-lookup"><span data-stu-id="f35ea-113">In this example, the change in color begins slowly and speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-csharp[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/ColorAnimationUsingKeyFramesExample.cs#coloranimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/coloranimationusingkeyframesexample.vb#coloranimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#ColorAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ColorAnimationUsingKeyFramesExample.xaml#coloranimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="f35ea-114">Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).</span><span class="sxs-lookup"><span data-stu-id="f35ea-114">For the complete sample, see [KeyFrame Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f35ea-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f35ea-115">See also</span></span>
- <xref:System.Windows.Media.SolidColorBrush.Color%2A>
- <xref:System.Windows.Media.SolidColorBrush>
- <xref:System.Windows.Media.Animation.ColorAnimationUsingKeyFrames>
- [<span data-ttu-id="f35ea-116">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="f35ea-116">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)
- [<span data-ttu-id="f35ea-117">Guides pratiques relatifs aux images clés</span><span class="sxs-lookup"><span data-stu-id="f35ea-117">Key-Frame How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
