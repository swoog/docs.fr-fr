---
title: 'Comment : utiliser le verrouillage spinlock pour une synchronisation de bas niveau'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SpinLock, how to use
ms.assetid: a9ed3e4e-4f29-4207-b730-ed0a51ecbc19
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 216480e893f6dbebbb204cbf2bfebae8dc139ec4
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45593854"
---
# <a name="how-to-use-spinlock-for-low-level-synchronization"></a>Comment : utiliser le verrouillage spinlock pour une synchronisation de bas niveau
L'exemple suivant montre comment utiliser un verrouillage <xref:System.Threading.SpinLock>.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, la section critique exécute une quantité minimale de travail, ce qui en fait un bon candidat pour un <xref:System.Threading.SpinLock>. Le fait d’augmenter un petit peu le volume de travail augmente le niveau de performance du <xref:System.Threading.SpinLock> par rapport à un verrouillage standard. Toutefois, à un moment, le verrouillage tournant devient plus coûteux qu’un verrouillage standard. Vous pouvez utiliser la fonctionnalité de profilage d'accès concurrentiel dans les outils de profilage pour voir quel type de verrouillage offre les meilleures performances pour votre programme. Pour plus d’informations, consultez [Visualiseur concurrentiel](/visualstudio/profiling/concurrency-visualizer).  
  
 [!code-csharp[CDS_SpinLock#02](../../../samples/snippets/csharp/VS_Snippets_Misc/cds_spinlock/cs/spinlockdemo.cs#02)]
 [!code-vb[CDS_SpinLock#02](../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_spinlock/vb/spinlock_vb.vb#02)]  
  
 <xref:System.Threading.SpinLock> peut être utile quand vous avez besoin d’un verrouillage de courte durée sur une ressource partagée. Dans ce cas, sur les ordinateurs multicœurs, le thread bloqué peut efficacement tourner pendant quelques cycles jusqu'à ce que le verrouillage soit libéré. En tournant, le thread ne se bloque pas. Ce processus est exigeant en ressources. <xref:System.Threading.SpinLock> cesse de tourner sous certaines conditions pour empêcher toute défaillance des processeurs logiques ou toute inversion des priorités sur les systèmes avec Hyper-Threading.  
  
 Cet exemple utilise la classe <xref:System.Collections.Generic.Queue%601?displayProperty=nameWithType>, qui exige la synchronisation utilisateur pour l’accès multithread. Dans les applications qui ciblent .NET Framework version 4, il est également possible d’utiliser le verrouillage <xref:System.Collections.Concurrent.ConcurrentQueue%601?displayProperty=nameWithType>, qui ne nécessite aucun verrouillage utilisateur.  
  
 Notez l’utilisation de `false` (`False` en Visual Basic) dans l’appel à <xref:System.Threading.SpinLock.Exit%2A>. Cela fournit les meilleures performances. Dans les architectures IA64, spécifiez `true` (`True`) pour utiliser la barrière mémoire, qui vide les tampons d’écriture pour garantir que le verrouillage est disponible pour la sortie des autres threads.  
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)
