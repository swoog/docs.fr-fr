---
title: Vue d'ensemble de la classe SoundPlayer
ms.date: 03/30/2017
helpviewer_keywords:
- playing sounds [Windows Forms], SoundPlayer class
- SoundPlayer class [Windows Forms], about SoundPlayer class
- sounds [Windows Forms], playing
ms.assetid: fcebb938-62b9-4677-9cbe-6465bc863e22
ms.openlocfilehash: 3ff23cbfa78b803d4526e7a7c389fd5d458a967c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195005"
---
# <a name="soundplayer-class-overview"></a>Vue d'ensemble de la classe SoundPlayer
La classe <xref:System.Media.SoundPlayer> vous permet d'inclure facilement des sons dans vos applications.  
  
 Le <xref:System.Media.SoundPlayer> classe peut lire des fichiers audio au format .wav, à partir d’une ressource ou à partir d’emplacements UNC ou HTTP. En outre, la <xref:System.Media.SoundPlayer> classe vous permet de charger ou lire des sons de façon asynchrone.  
  
 Vous pouvez également utiliser la classe <xref:System.Media.SystemSounds> pour jouer l'un des sons système courants, tel qu'un signal sonore.  
  
## <a name="commonly-used-properties-methods-and-events"></a>Propriétés, méthodes et événements couramment utilisés  
  
|Nom|Description|  
|----------|-----------------|  
|<xref:System.Media.SoundPlayer.SoundLocation%2A> propriété|Chemin du fichier ou adresse web du son. Les valeurs acceptables peuvent être UNC ou HTTP.|  
|<xref:System.Media.SoundPlayer.LoadTimeout%2A> propriété|Nombre de millisecondes que votre programme attend pour charger un son avant de lever une exception. La valeur par défaut est 10 secondes.|  
|<xref:System.Media.SoundPlayer.IsLoadCompleted%2A> propriété|Valeur booléenne indiquant si le chargement du son est terminé.|  
|<xref:System.Media.SoundPlayer.Load%2A> méthode|Charge un son de façon synchrone.|  
|<xref:System.Media.SoundPlayer.LoadAsync%2A> méthode|Commence à charger un son de façon asynchrone. Lorsque le chargement est terminé, il déclenche le <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> événement.|  
|<xref:System.Media.SoundPlayer.Play%2A> méthode|Lit le son spécifié dans le <xref:System.Media.SoundPlayer.SoundLocation%2A> ou <xref:System.Media.SoundPlayer.Stream%2A> propriété dans un nouveau thread.|  
|<xref:System.Media.SoundPlayer.PlaySync%2A> méthode|Lit le son spécifié dans le <xref:System.Media.SoundPlayer.SoundLocation%2A> ou <xref:System.Media.SoundPlayer.Stream%2A> propriété dans le thread actuel.|  
|<xref:System.Media.SoundPlayer.Stop%2A> méthode|Arrête le son actuellement émis.|  
|<xref:System.Media.SoundPlayer.LoadCompleted> événement|Déclenché après une tentative de chargement d’un son.|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
