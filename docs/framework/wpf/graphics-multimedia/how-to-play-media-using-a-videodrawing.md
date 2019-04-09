---
title: 'Procédure : Lire un média à l’aide d’un VideoDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- playback of media [WPF]
- classes [WPF], MediaPlayer
ms.assetid: 165d47ed-22ce-4ded-aa6a-aa9b7467de87
ms.openlocfilehash: 186c9ae8167dafd09f029418c1d23f81f7a9e906
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59203611"
---
# <a name="how-to-play-media-using-a-videodrawing"></a>Procédure : Lire un média à l’aide d’un VideoDrawing
Pour lire un fichier audio ou vidéo, vous utilisez un <xref:System.Windows.Media.VideoDrawing> et un <xref:System.Windows.Media.MediaPlayer>. Il y a deux façons de charger et de lire des médias. La première consiste à utiliser un <xref:System.Windows.Media.MediaPlayer> et un <xref:System.Windows.Media.VideoDrawing> par eux-mêmes et la seconde méthode consiste à créer votre propre <xref:System.Windows.Media.MediaTimeline> à utiliser avec le <xref:System.Windows.Media.MediaPlayer> et <xref:System.Windows.Media.VideoDrawing>.  
  
> [!NOTE]
>  Lorsque vous distribuez un contenu multimédia avec votre application, vous ne pouvez pas utiliser de fichier multimédia comme ressource de projet, comme pour une image. Dans votre fichier projet, vous devez plutôt définir le type de média sur `Content` et définir `CopyToOutputDirectory` sur `PreserveNewest` ou `Always`.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.VideoDrawing> et un <xref:System.Windows.Media.MediaPlayer> pour lire un fichier vidéo une seule fois.  
  
 [!code-csharp[DrawingMiscSnippets_snip#VideoDrawingExampleInline](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/VideoDrawingExample.cs#videodrawingexampleinline)]  
  
 Pour optimiser le contrôle du minutage du média, utilisez un <xref:System.Windows.Media.MediaTimeline> avec la <xref:System.Windows.Media.MediaPlayer> et <xref:System.Windows.Media.VideoDrawing> objets. Le <xref:System.Windows.Media.MediaTimeline> vous permet de spécifier si la vidéo doit se répéter.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Windows.Media.MediaTimeline> avec la <xref:System.Windows.Media.MediaPlayer> et <xref:System.Windows.Media.VideoDrawing> objets pour lire une vidéo à plusieurs reprises.  
  
 [!code-csharp[DrawingMiscSnippets_snip#RepeatingVideoDrawingExampleInline](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/VideoDrawingExample.cs#repeatingvideodrawingexampleinline)]  
  
 Notez que, lorsque vous utilisez un <xref:System.Windows.Media.MediaTimeline>, vous utilisez la commande interactive <xref:System.Windows.Media.Animation.ClockController> retourné à partir de la <xref:System.Windows.Media.Animation.Clock.Controller%2A> propriété de la <xref:System.Windows.Media.MediaClock> pour contrôler la lecture média au lieu de méthodes interactives de <xref:System.Windows.Media.MediaPlayer>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.VideoDrawing>
- [Vue d'ensemble des objets Drawing](drawing-objects-overview.md)
