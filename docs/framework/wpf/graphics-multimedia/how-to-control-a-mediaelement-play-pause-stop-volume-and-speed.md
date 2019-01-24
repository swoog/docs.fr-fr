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
ms.openlocfilehash: e9939c2d3d740bfe9296c23e47ef8ea09d837e01
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498919"
---
# <a name="how-to-control-a-mediaelement-play-pause-stop-volume-and-speed"></a>Procédure : Contrôler un MediaElement (lecture, pause, arrêt, volume et vitesse)
L’exemple suivant montre comment contrôler la lecture de média à l’aide un <xref:System.Windows.Controls.MediaElement>. L’exemple crée un lecteur multimédia simple qui vous permet de lire, suspendre, arrêter et ignorer dans les deux sens dans le média ainsi qu’ajustez le ratio de volume et vitesse.  
  
## <a name="example"></a>Exemple  
 Le code suivant crée l’interface utilisateur.  
  
> [!NOTE]
>  Le <xref:System.Windows.Controls.MediaElement.LoadedBehavior%2A> propriété du <xref:System.Windows.Controls.MediaElement> doit être définie sur `Manual` afin d’être en mesure d’arrêter de manière interactive, interrompre et lire le média.  
  
 [!code-xaml[MediaGallery_snip#MediaElementExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaElementExample.xaml#mediaelementexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 Le code ci-dessous implémente les fonctionnalités de contrôles d’interface utilisateur de l’exemple. Le <xref:System.Windows.Controls.MediaElement.Play%2A>, <xref:System.Windows.Controls.MediaElement.Pause%2A>, et <xref:System.Windows.Controls.MediaElement.Stop%2A> méthodes sont utilisées pour lire, suspendre et arrêter le média, respectivement. Modification de la <xref:System.Windows.Controls.MediaElement.Position%2A> propriété de la <xref:System.Windows.Controls.MediaElement> vous permet de naviguer sur le média. Enfin, le <xref:System.Windows.Controls.MediaElement.Volume%2A> et <xref:System.Windows.Controls.MediaElement.SpeedRatio%2A> propriétés sont utilisées pour ajuster la vitesse de volume et la lecture du média.  
  
 [!code-csharp[MediaGallery_snip#CodeBehindMediaElementExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snip/CSharp/MediaElementExample.xaml.cs#codebehindmediaelementexamplewholepage)]
 [!code-vb[MediaGallery_snip#CodeBehindMediaElementExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaElementExample.xaml.vb#codebehindmediaelementexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Contrôler un MediaElement à l'aide d'un storyboard](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-mediaelement-by-using-a-storyboard.md)
