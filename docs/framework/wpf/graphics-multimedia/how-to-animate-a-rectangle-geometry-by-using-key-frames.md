---
title: 'Procédure : Animer une géométrie rectangle à l’aide d’images clés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating RectangleGeometry objects with
- RectangleGeometry objects [WPF], animating with key frames
- animation [WPF], RectangleGeometry objects with key frames
ms.assetid: a8b45ceb-0e32-4ba1-928f-df6d30db17c6
ms.openlocfilehash: 03953b79127ffceeb49e4ece2070d09f382448a5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62010096"
---
# <a name="how-to-animate-a-rectangle-geometry-by-using-key-frames"></a><span data-ttu-id="87a36-102">Procédure : Animer une géométrie rectangle à l’aide d’images clés</span><span class="sxs-lookup"><span data-stu-id="87a36-102">How to: Animate a Rectangle Geometry by Using Key Frames</span></span>
<span data-ttu-id="87a36-103">Cet exemple montre comment animer la <xref:System.Windows.Media.RectangleGeometry.Rect%2A> propriété d’un <xref:System.Windows.Media.RectangleGeometry> à l’aide d’images clés.</span><span class="sxs-lookup"><span data-stu-id="87a36-103">This example shows how to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry> by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="87a36-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="87a36-104">Example</span></span>  
 <span data-ttu-id="87a36-105">L’exemple suivant utilise le <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Media.RectangleGeometry.Rect%2A> propriété d’un <xref:System.Windows.Media.RectangleGeometry>.</span><span class="sxs-lookup"><span data-stu-id="87a36-105">The following example uses the <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry>.</span></span> <span data-ttu-id="87a36-106">Cette animation utilise trois images clés de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="87a36-106">This animation uses three key frames in the following manner:</span></span>  
  
1. <span data-ttu-id="87a36-107">Pendant les deux premières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.LinearRectKeyFrame> classe pour animer un changement graduel de position, la largeur et hauteur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="87a36-107">During the first two seconds, uses an instance of the <xref:System.Windows.Media.Animation.LinearRectKeyFrame> class to animate a gradual change in the position, width, and height of a rectangle.</span></span> <span data-ttu-id="87a36-108">Images clés linéaires comme <xref:System.Windows.Media.Animation.LinearRectKeyFrame> créent une transition linéaire fluide entre les valeurs.</span><span class="sxs-lookup"><span data-stu-id="87a36-108">Linear key frames like <xref:System.Windows.Media.Animation.LinearRectKeyFrame> create a smooth linear transition between values.</span></span>  
  
2. <span data-ttu-id="87a36-109">Lors de la fin de la prochaine demi-seconde, elle utilise une instance de la <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> classe pour réduire soudainement la hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="87a36-109">During the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> class to suddenly decrease the height of the rectangle.</span></span> <span data-ttu-id="87a36-110">Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> créent des changements soudains entre les valeurs, autrement dit, la diminution de la hauteur se produit rapidement et n’est pas subtile.</span><span class="sxs-lookup"><span data-stu-id="87a36-110">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> create sudden changes between values, that is, the decrease in height occurs quickly and is not subtle.</span></span>  
  
3. <span data-ttu-id="87a36-111">Pendant les deux dernières secondes, utilise une instance de la <xref:System.Windows.Media.Animation.SplineRectKeyFrame> classe pour modifier le rectangle à sa taille et sa position d’origine.</span><span class="sxs-lookup"><span data-stu-id="87a36-111">During the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineRectKeyFrame> class to change the rectangle back to its original size and position.</span></span> <span data-ttu-id="87a36-112">Les images clés spline comme <xref:System.Windows.Media.Animation.SplineRectKeyFrame> créent une transition variable entre des valeurs en fonction de la <xref:System.Windows.Media.Animation.SplineRectKeyFrame.KeySpline%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="87a36-112">Spline key frames like <xref:System.Windows.Media.Animation.SplineRectKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplineRectKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="87a36-113">Dans cet exemple, le changement commence lentement, puis accélère de façon exponentielle jusqu’à la fin du segment temporel.</span><span class="sxs-lookup"><span data-stu-id="87a36-113">In this example, the change begins slowly and speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-csharp[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/RectAnimationUsingKeyFramesExample.cs#rectanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/rectanimationusingkeyframesexample.vb#rectanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/RectAnimationUsingKeyFramesExample.xaml#rectanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="87a36-114">Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).</span><span class="sxs-lookup"><span data-stu-id="87a36-114">For the complete sample, see [KeyFrame Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87a36-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87a36-115">See also</span></span>

- <xref:System.Windows.Media.RectangleGeometry>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames>
- [<span data-ttu-id="87a36-116">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="87a36-116">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="87a36-117">Guides pratiques relatifs aux images clés</span><span class="sxs-lookup"><span data-stu-id="87a36-117">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
