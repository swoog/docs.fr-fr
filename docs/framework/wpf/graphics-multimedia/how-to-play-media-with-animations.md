---
title: 'Procédure : Lire le média avec des animations'
ms.date: 03/30/2017
helpviewer_keywords:
- multimedia [WPF], playback with animations
- playback of media [WPF], with animations
- animation [WPF], media playback with
- media [WPF], playback with animations
ms.assetid: 8982b7b7-1c6c-4b24-8801-b328862975f5
ms.openlocfilehash: 200f9d62c67a02088fe5a5789cdb41a04837d430
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079901"
---
# <a name="how-to-play-media-with-animations"></a><span data-ttu-id="2de52-102">Procédure : Lire le média avec des animations</span><span class="sxs-lookup"><span data-stu-id="2de52-102">How to: Play Media with Animations</span></span>
<span data-ttu-id="2de52-103">Cet exemple montre comment lire un média et des animations en même temps à l’aide de la <xref:System.Windows.Media.MediaTimeline> et <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> classes dans le même <xref:System.Windows.Media.Animation.Storyboard>.</span><span class="sxs-lookup"><span data-stu-id="2de52-103">This example shows how to play media and animations at the same time by using the <xref:System.Windows.Media.MediaTimeline> and <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> classes in the same <xref:System.Windows.Media.Animation.Storyboard>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2de52-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="2de52-104">Example</span></span>  
 <span data-ttu-id="2de52-105">Vous pouvez utiliser un ou plusieurs <xref:System.Windows.Media.MediaTimeline> des objets dans un <xref:System.Windows.Media.Animation.Storyboard> ainsi que d’autres <xref:System.Windows.Media.Animation.Timeline> objets, tels que les animations.</span><span class="sxs-lookup"><span data-stu-id="2de52-105">You can use one or more <xref:System.Windows.Media.MediaTimeline> objects in a <xref:System.Windows.Media.Animation.Storyboard> together with other <xref:System.Windows.Media.Animation.Timeline> objects, such as animations.</span></span>  
  
 <span data-ttu-id="2de52-106">L’exemple suivant définit la <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A> propriété de la <xref:System.Windows.Media.Animation.Storyboard> sur la valeur `Slip`, qui spécifie que l’animation ne progresse pas jusqu'à ce que le progresse multimédia (vidéo dans cet exemple).</span><span class="sxs-lookup"><span data-stu-id="2de52-106">The following example sets the <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A> property of the <xref:System.Windows.Media.Animation.Storyboard> to a value of `Slip`, which specifies that the animation does not progress until the media (video in this example) progresses.</span></span> <span data-ttu-id="2de52-107">Cette fonctionnalité peut être nécessaire si la lecture du média est retardée en raison du temps de chargement.</span><span class="sxs-lookup"><span data-stu-id="2de52-107">This functionality might be needed if media playback is delayed because of loading time.</span></span>  
  
 [!code-xaml[MediaGallery_snippet#MediaTimelinePlusAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/MediaTimelinePlusAnimationExample.xaml#mediatimelineplusanimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="2de52-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2de52-108">See also</span></span>

- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A>
- [<span data-ttu-id="2de52-109">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="2de52-109">How-to Topics</span></span>](audio-and-video-how-to-topics.md)
- [<span data-ttu-id="2de52-110">Vue d'ensemble des storyboards</span><span class="sxs-lookup"><span data-stu-id="2de52-110">Storyboards Overview</span></span>](storyboards-overview.md)
- [<span data-ttu-id="2de52-111">Vue d'ensemble des animations d'image clé</span><span class="sxs-lookup"><span data-stu-id="2de52-111">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="2de52-112">Vue d'ensemble de l'animation</span><span class="sxs-lookup"><span data-stu-id="2de52-112">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="2de52-113">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="2de52-113">Graphics and Multimedia</span></span>](index.md)
