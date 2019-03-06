---
title: 'Procédure : Lire le média avec des animations'
ms.date: 03/30/2017
helpviewer_keywords:
- multimedia [WPF], playback with animations
- playback of media [WPF], with animations
- animation [WPF], media playback with
- media [WPF], playback with animations
ms.assetid: 8982b7b7-1c6c-4b24-8801-b328862975f5
ms.openlocfilehash: 0dc39d08ef17a628675018c17602623f2efd0173
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372903"
---
# <a name="how-to-play-media-with-animations"></a>Procédure : Lire le média avec des animations
Cet exemple montre comment lire un média et des animations en même temps à l’aide de la <xref:System.Windows.Media.MediaTimeline> et <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> classes dans le même <xref:System.Windows.Media.Animation.Storyboard>.  
  
## <a name="example"></a>Exemple  
 Vous pouvez utiliser un ou plusieurs <xref:System.Windows.Media.MediaTimeline> des objets dans un <xref:System.Windows.Media.Animation.Storyboard> ainsi que d’autres <xref:System.Windows.Media.Animation.Timeline> objets, tels que les animations.  
  
 L’exemple suivant définit la <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A> propriété de la <xref:System.Windows.Media.Animation.Storyboard> sur la valeur `Slip`, qui spécifie que l’animation ne progresse pas jusqu'à ce que le progresse multimédia (vidéo dans cet exemple). Cette fonctionnalité peut être nécessaire si la lecture du média est retardée en raison du temps de chargement.  
  
 [!code-xaml[MediaGallery_snippet#MediaTimelinePlusAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/MediaTimelinePlusAnimationExample.xaml#mediatimelineplusanimationexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A>
- [Rubriques de guide pratique](audio-and-video-how-to-topics.md)
- [Vue d'ensemble des plans conceptuels](storyboards-overview.md)
- [Vue d'ensemble des animations d'image clé](key-frame-animations-overview.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
- [Graphiques et multimédia](index.md)
