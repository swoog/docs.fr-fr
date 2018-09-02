---
title: "Comment : animer une chaîne à l'aide d'images clés"
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], strings with key frames
- strings [WPF], animating with key frames
- key frames [WPF], animating strings with
ms.assetid: c62bc9fd-c09a-4227-bce0-0a1ab82049dd
ms.openlocfilehash: 1b55afd5938073a326789e67b66fec9cfce12015
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43403123"
---
# <a name="how-to-animate-a-string-by-using-key-frames"></a><span data-ttu-id="086ee-102">Comment : animer une chaîne à l'aide d'images clés</span><span class="sxs-lookup"><span data-stu-id="086ee-102">How to: Animate a String by Using Key Frames</span></span>
<span data-ttu-id="086ee-103">Cet exemple montre comment animer une chaîne qui, dans cet exemple est la <xref:System.Windows.Controls.ContentControl.Content%2A> propriété d’un <xref:System.Windows.Controls.Button> contrôle, à l’aide d’images clés.</span><span class="sxs-lookup"><span data-stu-id="086ee-103">This example shows how to animate a string, which in this example is the <xref:System.Windows.Controls.ContentControl.Content%2A> property of a <xref:System.Windows.Controls.Button> control, by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="086ee-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="086ee-104">Example</span></span>  
 <span data-ttu-id="086ee-105">L’exemple suivant utilise le <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> classe pour animer la <xref:System.Windows.Controls.ContentControl.Content%2A> propriété d’un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="086ee-105">The following example uses the <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Controls.ContentControl.Content%2A> property of a <xref:System.Windows.Controls.Button>.</span></span>  
  
 <span data-ttu-id="086ee-106">Toutes les images clés dans cet exemple montre comment utilisent une instance de la <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> classe car une animation de chaîne qui est créée avec des images clés peut uniquement utiliser les images clés discrètes.</span><span class="sxs-lookup"><span data-stu-id="086ee-106">All the key frames in this example use an instance of the <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> class because a string animation that is created with key frames can only use discrete key frames.</span></span> <span data-ttu-id="086ee-107">Images clés discrètes comme <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> créent des changements soudains entre les valeurs, autrement dit, les modifications apportées à l’animation se produisent rapidement et ne sont pas subtiles.</span><span class="sxs-lookup"><span data-stu-id="086ee-107">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> create sudden jumps between values, that is, changes to the animation occur quickly and are not subtle.</span></span>  
  
 [!code-xaml[keyframes_snip#StringAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/StringAnimationUsingKeyFramesExample.xaml#stringanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="086ee-108">Pour l’exemple complet, consultez la page [Animation d’image clé, exemple](https://go.microsoft.com/fwlink/?LinkID=160012).</span><span class="sxs-lookup"><span data-stu-id="086ee-108">For the complete sample, see [KeyFrame Animation Sample](https://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="086ee-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="086ee-109">See Also</span></span>  
 <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames>  
 <xref:System.Windows.Controls.ContentControl.Content%2A>  
 <xref:System.Windows.Controls.Button>  
 <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>  
 [<span data-ttu-id="086ee-110">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="086ee-110">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [<span data-ttu-id="086ee-111">Guides pratiques relatifs aux images clés</span><span class="sxs-lookup"><span data-stu-id="086ee-111">Key-Frame How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
