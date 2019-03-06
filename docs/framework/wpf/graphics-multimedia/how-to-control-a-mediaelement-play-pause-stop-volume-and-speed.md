---
title: 'Procédure : Contrôler un MediaElement (lecture, pause, arrêt, volume et vitesse)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- playback of media [WPF], controlling
- controlling playback of media [WPF]
- multimedia [WPF], controlling playback of media
- media [WPF], controlling playback of
ms.assetid: 6885a730-e054-4c16-8c1e-ffe17b1f7c32
ms.openlocfilehash: 7fe8107f7b5b65f00f2c5ac029f806aeba758d20
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57368504"
---
# <a name="how-to-control-a-mediaelement-play-pause-stop-volume-and-speed"></a><span data-ttu-id="9b62b-102">Procédure : Contrôler un MediaElement (lecture, pause, arrêt, volume et vitesse)</span><span class="sxs-lookup"><span data-stu-id="9b62b-102">How to: Control a MediaElement (Play, Pause, Stop, Volume, and Speed)</span></span>
<span data-ttu-id="9b62b-103">L’exemple suivant montre comment contrôler la lecture de média à l’aide un <xref:System.Windows.Controls.MediaElement>.</span><span class="sxs-lookup"><span data-stu-id="9b62b-103">The following example shows how to control playback of media using a <xref:System.Windows.Controls.MediaElement>.</span></span> <span data-ttu-id="9b62b-104">L’exemple crée un lecteur multimédia simple qui vous permet de lire, suspendre, arrêter et ignorer dans les deux sens dans le média ainsi qu’ajustez le ratio de volume et vitesse.</span><span class="sxs-lookup"><span data-stu-id="9b62b-104">The example creates a simple media player that allows you to play, pause, stop, and skip back and forth in the media as well as adjust the volume and speed ratio.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9b62b-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="9b62b-105">Example</span></span>  
 <span data-ttu-id="9b62b-106">Le code suivant crée l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b62b-106">The code below creates the UI.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9b62b-107">Le <xref:System.Windows.Controls.MediaElement.LoadedBehavior%2A> propriété du <xref:System.Windows.Controls.MediaElement> doit être définie sur `Manual` afin d’être en mesure d’arrêter de manière interactive, interrompre et lire le média.</span><span class="sxs-lookup"><span data-stu-id="9b62b-107">The <xref:System.Windows.Controls.MediaElement.LoadedBehavior%2A> property of <xref:System.Windows.Controls.MediaElement> must be set to `Manual` in order to be able to interactively stop, pause, and play the media.</span></span>  
  
 [!code-xaml[MediaGallery_snip#MediaElementExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaElementExample.xaml#mediaelementexamplewholepage)]  
  
## <a name="example"></a><span data-ttu-id="9b62b-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="9b62b-108">Example</span></span>  
 <span data-ttu-id="9b62b-109">Le code ci-dessous implémente les fonctionnalités de contrôles d’interface utilisateur de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="9b62b-109">The code below implements the functionality of the sample UI controls.</span></span> <span data-ttu-id="9b62b-110">Le <xref:System.Windows.Controls.MediaElement.Play%2A>, <xref:System.Windows.Controls.MediaElement.Pause%2A>, et <xref:System.Windows.Controls.MediaElement.Stop%2A> méthodes sont utilisées pour lire, suspendre et arrêter le média, respectivement.</span><span class="sxs-lookup"><span data-stu-id="9b62b-110">The <xref:System.Windows.Controls.MediaElement.Play%2A>, <xref:System.Windows.Controls.MediaElement.Pause%2A>, and <xref:System.Windows.Controls.MediaElement.Stop%2A> methods are used to respectively play, pause and stop the media.</span></span> <span data-ttu-id="9b62b-111">Modification de la <xref:System.Windows.Controls.MediaElement.Position%2A> propriété de la <xref:System.Windows.Controls.MediaElement> vous permet de naviguer sur le média.</span><span class="sxs-lookup"><span data-stu-id="9b62b-111">Changing the <xref:System.Windows.Controls.MediaElement.Position%2A> property of the <xref:System.Windows.Controls.MediaElement> allows you to skip around in the media.</span></span> <span data-ttu-id="9b62b-112">Enfin, le <xref:System.Windows.Controls.MediaElement.Volume%2A> et <xref:System.Windows.Controls.MediaElement.SpeedRatio%2A> propriétés sont utilisées pour ajuster la vitesse de volume et la lecture du média.</span><span class="sxs-lookup"><span data-stu-id="9b62b-112">Finally, the <xref:System.Windows.Controls.MediaElement.Volume%2A> and <xref:System.Windows.Controls.MediaElement.SpeedRatio%2A> properties are used to adjust the volume and playback speed of the media.</span></span>  
  
 [!code-csharp[MediaGallery_snip#CodeBehindMediaElementExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snip/CSharp/MediaElementExample.xaml.cs#codebehindmediaelementexamplewholepage)]
 [!code-vb[MediaGallery_snip#CodeBehindMediaElementExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaElementExample.xaml.vb#codebehindmediaelementexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="9b62b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b62b-113">See also</span></span>
- [<span data-ttu-id="9b62b-114">Contrôler un MediaElement à l'aide d'un storyboard</span><span class="sxs-lookup"><span data-stu-id="9b62b-114">Control a MediaElement by Using a Storyboard</span></span>](how-to-control-a-mediaelement-by-using-a-storyboard.md)
