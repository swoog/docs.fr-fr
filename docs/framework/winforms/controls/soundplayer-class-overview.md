---
title: Vue d'ensemble de la classe SoundPlayer
ms.date: 03/30/2017
helpviewer_keywords:
- playing sounds [Windows Forms], SoundPlayer class
- SoundPlayer class [Windows Forms], about SoundPlayer class
- sounds [Windows Forms], playing
ms.assetid: fcebb938-62b9-4677-9cbe-6465bc863e22
ms.openlocfilehash: 31ce87303b7b96cfd14d4daf07fd21c9de91a548
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="soundplayer-class-overview"></a>Vue d'ensemble de la classe SoundPlayer
La classe <xref:System.Media.SoundPlayer> vous permet d'inclure facilement des sons dans vos applications.  
  
 La <xref:System.Media.SoundPlayer> classe peut lire des fichiers audio au format .wav, à partir d’une ressource ou d’emplacements UNC ou HTTP. En outre, la <xref:System.Media.SoundPlayer> classe vous permet de charger ou lire des sons de façon asynchrone.  
  
 Vous pouvez également utiliser la classe <xref:System.Media.SystemSounds> pour jouer l'un des sons système courants, tel qu'un signal sonore.  
  
## <a name="commonly-used-properties-methods-and-events"></a>Propriétés, méthodes et événements couramment utilisés  
  
|Name|Description|  
|----------|-----------------|  
|Propriété <xref:System.Media.SoundPlayer.SoundLocation%2A>|Chemin du fichier ou adresse web du son. Les valeurs acceptables peuvent être UNC ou HTTP.|  
|Propriété <xref:System.Media.SoundPlayer.LoadTimeout%2A>|Nombre de millisecondes que votre programme attend pour charger un son avant de lever une exception. La valeur par défaut est 10 secondes.|  
|Propriété <xref:System.Media.SoundPlayer.IsLoadCompleted%2A>|Valeur booléenne indiquant si le chargement du son est terminé.|  
|Méthode <xref:System.Media.SoundPlayer.Load%2A>|Charge un son de façon synchrone.|  
|Méthode <xref:System.Media.SoundPlayer.LoadAsync%2A>|Commence à charger un son de façon asynchrone. Lorsque le chargement est terminé, il déclenche le <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> événement.|  
|Méthode <xref:System.Media.SoundPlayer.Play%2A>|Lit le son spécifié dans le <xref:System.Media.SoundPlayer.SoundLocation%2A> ou <xref:System.Media.SoundPlayer.Stream%2A> propriété dans un nouveau thread.|  
|Méthode <xref:System.Media.SoundPlayer.PlaySync%2A>|Lit le son spécifié dans le <xref:System.Media.SoundPlayer.SoundLocation%2A> ou <xref:System.Media.SoundPlayer.Stream%2A> propriété dans le thread actuel.|  
|Méthode <xref:System.Media.SoundPlayer.Stop%2A>|Arrête le son actuellement émis.|  
|<xref:System.Media.SoundPlayer.LoadCompleted> Événement|Déclenché après une tentative de chargement d’un son.|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Media.SoundPlayer>  
 <xref:System.Media.SystemSounds>
