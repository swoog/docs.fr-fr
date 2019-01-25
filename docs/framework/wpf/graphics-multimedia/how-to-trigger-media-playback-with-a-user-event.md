---
title: 'Procédure : Déclencher la lecture du média avec un événement utilisateur'
ms.date: 03/30/2017
helpviewer_keywords:
- synchronizing media playback with events [WPF]
- playback of media [WPF], synchronizing with events
- media [WPF], synchronizing playback with events
- multimedia [WPF], synchronizing media playback with events
ms.assetid: c4dbe632-6e7f-4d7f-9df5-98737a758bc3
ms.openlocfilehash: 5244c63aea0747c3d0f8d5bdd71496ccd3dc44d2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54530062"
---
# <a name="how-to-trigger-media-playback-with-a-user-event"></a><span data-ttu-id="80eab-102">Procédure : Déclencher la lecture du média avec un événement utilisateur</span><span class="sxs-lookup"><span data-stu-id="80eab-102">How to: Trigger Media Playback with a User Event</span></span>
<span data-ttu-id="80eab-103">Cet exemple montre comment synchroniser la lecture du média avec un événement.</span><span class="sxs-lookup"><span data-stu-id="80eab-103">This example shows how to synchronize media playback with an event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="80eab-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="80eab-104">Example</span></span>  
 <span data-ttu-id="80eab-105">L’exemple suivant utilise le <xref:System.Windows.Controls.MediaElement> contrôle et le <xref:System.Windows.Media.MediaTimeline> classe pour lire un son qui se produit lorsque l’utilisateur clique sur un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="80eab-105">The following example uses the <xref:System.Windows.Controls.MediaElement> control and the <xref:System.Windows.Media.MediaTimeline> class to play a sound that occurs when the user clicks a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[MediaGallery_snippet#SoundFromUserEventExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/SoundFromUserEventExample.xaml#soundfromusereventexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="80eab-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80eab-106">See also</span></span>
- <xref:System.Windows.Controls.MediaElement>
- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.EventTrigger.RoutedEvent%2A>
- <xref:System.Windows.Media.Animation.Storyboard>
- [<span data-ttu-id="80eab-107">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="80eab-107">How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/audio-and-video-how-to-topics.md)
- [<span data-ttu-id="80eab-108">Graphiques et multimédia</span><span class="sxs-lookup"><span data-stu-id="80eab-108">Graphics and Multimedia</span></span>](../../../../docs/framework/wpf/graphics-multimedia/index.md)
