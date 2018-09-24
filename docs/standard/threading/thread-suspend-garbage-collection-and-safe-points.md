---
title: Thread.Suspend, Garbage Collection et les points sans risque
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- suspending threads
- safe points
- threading [.NET Framework], suspending
- threading [.NET Framework], garbage collection
- garbage collection, threads
ms.assetid: e8f58e17-2714-4821-802a-f8eb3b2baa62
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fc3af01167fe97b701bdb0c7bc37af02d8e8a77c
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46004177"
---
# <a name="threadsuspend-garbage-collection-and-safe-points"></a>Thread.Suspend, Garbage Collection et les points sans risque
Quand vous appelez <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> sur un thread, le système indique qu’une suspension du thread a été demandée et permet au thread de s’exécuter jusqu'à ce qu’il ait atteint un point sans risque avant de suspendre réellement le thread. Un point sans risque pour un thread est un point de son exécution auquel le nettoyage de la mémoire peut être exécuté.  
  
 Une fois atteint un point sans risque, le runtime garantit que le thread suspendu ne progressera pas dans le code managé. Un thread s’exécutant en dehors du code managé est toujours sûr pour le nettoyage de la mémoire, et son exécution se poursuit jusqu'à ce qu’il tente de reprendre l’exécution du code managé.  
  
> [!NOTE]
>  Pour effectuer un nettoyage de la mémoire, le runtime doit suspendre tous les threads, sauf celui qui exécute le nettoyage. Chaque thread doit être acheminé vers un point sans risque avant de pouvoir être suspendu.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.Thread>  
- <xref:System.GC>  
- [Thread](../../../docs/standard/threading/index.md)  
- [Gestion automatique de la mémoire](../../../docs/standard/automatic-memory-management.md)
