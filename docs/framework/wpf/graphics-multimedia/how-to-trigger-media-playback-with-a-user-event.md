---
title: 'Procédure : Déclencher la lecture du média avec un événement utilisateur'
ms.date: 03/30/2017
helpviewer_keywords:
- synchronizing media playback with events [WPF]
- playback of media [WPF], synchronizing with events
- media [WPF], synchronizing playback with events
- multimedia [WPF], synchronizing media playback with events
ms.assetid: c4dbe632-6e7f-4d7f-9df5-98737a758bc3
ms.openlocfilehash: ae8ba54cc852bb85350492c95e3e890aebf6534f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769276"
---
# <a name="how-to-trigger-media-playback-with-a-user-event"></a><span data-ttu-id="b1019-102">Procédure : Déclencher la lecture du média avec un événement utilisateur</span><span class="sxs-lookup"><span data-stu-id="b1019-102">How to: Trigger Media Playback with a User Event</span></span>
<span data-ttu-id="b1019-103">Cet exemple montre comment synchroniser la lecture du média avec un événement.</span><span class="sxs-lookup"><span data-stu-id="b1019-103">This example shows how to synchronize media playback with an event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b1019-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="b1019-104">Example</span></span>  
 <span data-ttu-id="b1019-105">L’exemple suivant utilise le <xref:System.Windows.Controls.MediaElement> contrôle et le <xref:System.Windows.Media.MediaTimeline> classe pour lire un son qui se produit lorsque l’utilisateur clique sur un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="b1019-105">The following example uses the <xref:System.Windows.Controls.MediaElement> control and the <xref:System.Windows.Media.MediaTimeline> class to play a sound that occurs when the user clicks a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[MediaGallery_snippet#SoundFromUserEventExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/SoundFromUserEventExample.xaml#soundfromusereventexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="b1019-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1019-106">See also</span></span>

- <xref:System.Windows.Controls.MediaElement>
- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.EventTrigger.RoutedEvent%2A>
- <xref:System.Windows.Media.Animation.Storyboard>
- [<span data-ttu-id="b1019-107">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="b1019-107">How-to Topics</span></span>](audio-and-video-how-to-topics.md)
- [<span data-ttu-id="b1019-108">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="b1019-108">Graphics and Multimedia</span></span>](index.md)
