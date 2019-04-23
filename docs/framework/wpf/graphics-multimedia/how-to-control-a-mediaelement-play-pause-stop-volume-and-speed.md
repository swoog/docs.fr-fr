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
ms.openlocfilehash: bb7319fc7ccec0220cbd79a32d5d015f9f2422d0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59182856"
---
# <a name="how-to-control-a-mediaelement-play-pause-stop-volume-and-speed"></a>Procédure : Contrôler un MediaElement (lecture, pause, arrêt, volume et vitesse)
L’exemple suivant montre comment contrôler la lecture de média à l’aide un <xref:System.Windows.Controls.MediaElement>. L’exemple crée un lecteur multimédia simple qui vous permet de lire, suspendre, arrêter et ignorer dans les deux sens dans le média ainsi qu’ajustez le ratio de volume et vitesse.  
  
## <a name="example"></a>Exemple  
 Le code suivant crée l’interface utilisateur.  
  
> [!NOTE]
>  Le <xref:System.Windows.Controls.MediaElement.LoadedBehavior%2A> propriété du <xref:System.Windows.Controls.MediaElement> doit être définie sur `Manual` afin d’être en mesure d’arrêter de manière interactive, interrompre et lire le média.  
  
 [!code-xaml[MediaGallery_snip#MediaElementExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaElementExample.xaml#mediaelementexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 Le code ci-dessous implémente les fonctionnalités de contrôles d’interface utilisateur de l’exemple. Le <xref:System.Windows.Controls.MediaElement.Play%2A>, <xref:System.Windows.Controls.MediaElement.Pause%2A>, et <xref:System.Windows.Controls.MediaElement.Stop%2A> méthodes sont utilisées pour lire, suspendre et arrêter le média, respectivement. Modification de la <xref:System.Windows.Controls.MediaElement.Position%2A> propriété de la <xref:System.Windows.Controls.MediaElement> vous permet de naviguer sur le média. Enfin, le <xref:System.Windows.Controls.MediaElement.Volume%2A> et <xref:System.Windows.Controls.MediaElement.SpeedRatio%2A> propriétés sont utilisées pour ajuster la vitesse de volume et la lecture du média.  
  
 [!code-csharp[MediaGallery_snip#CodeBehindMediaElementExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snip/CSharp/MediaElementExample.xaml.cs#codebehindmediaelementexamplewholepage)]
 [!code-vb[MediaGallery_snip#CodeBehindMediaElementExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MediaGallery_snip/VB/MediaElementExample.xaml.vb#codebehindmediaelementexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Contrôler un MediaElement à l'aide d'un storyboard](how-to-control-a-mediaelement-by-using-a-storyboard.md)
