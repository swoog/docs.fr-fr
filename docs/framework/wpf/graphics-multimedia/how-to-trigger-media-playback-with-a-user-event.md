---
title: 'Procédure : Déclencher la lecture du média avec un événement utilisateur'
ms.date: 03/30/2017
helpviewer_keywords:
- synchronizing media playback with events [WPF]
- playback of media [WPF], synchronizing with events
- media [WPF], synchronizing playback with events
- multimedia [WPF], synchronizing media playback with events
ms.assetid: c4dbe632-6e7f-4d7f-9df5-98737a758bc3
ms.openlocfilehash: 1d71e69bcd0332ba7119977dcf67356a3d79a368
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57377974"
---
# <a name="how-to-trigger-media-playback-with-a-user-event"></a>Procédure : Déclencher la lecture du média avec un événement utilisateur
Cet exemple montre comment synchroniser la lecture du média avec un événement.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Controls.MediaElement> contrôle et le <xref:System.Windows.Media.MediaTimeline> classe pour lire un son qui se produit lorsque l’utilisateur clique sur un <xref:System.Windows.Controls.Button>.  
  
 [!code-xaml[MediaGallery_snippet#SoundFromUserEventExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/SoundFromUserEventExample.xaml#soundfromusereventexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Controls.MediaElement>
- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.EventTrigger.RoutedEvent%2A>
- <xref:System.Windows.Media.Animation.Storyboard>
- [Rubriques de guide pratique](audio-and-video-how-to-topics.md)
- [Graphiques et multimédia](index.md)
