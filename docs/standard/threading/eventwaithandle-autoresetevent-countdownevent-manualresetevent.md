---
title: EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent
ms.date: 09/14/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- wait handles
- threading [.NET Framework], EventWaitHandle class
- event wait handles [.NET Framework]
ms.assetid: cd94fc34-ac15-427f-b723-a1240a4fab7d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: be9c858d7c76fdcc1b3e02485eb0b459f4e7555c
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47205917"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a>EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent

Les handles d’attente d’événements permettent aux threads de synchroniser les activités en se signalant et en attendant les signaux des uns et des autres. Ces événements de synchronisation s’appuient sur des handles d’attente de système d’exploitation et se divisent en deux types : ceux qui se réinitialisent automatiquement et ceux qui sont réinitialisés manuellement.  
  
Les handles d’attente d’événements sont utiles dans la majorité des scénarios de synchronisation de la classe <xref:System.Threading.Monitor>. Les handles d’attente d’événement sont souvent plus faciles à utiliser que les méthodes <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> et <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType>, et ils offrent un meilleur contrôle du signalement. Les handles d’attente d’événements nommés peuvent également servir à synchroniser les activités entre les différents processus et domaines d’application, tandis que les moniteurs sont liés localement à un domaine d’application.  
  
## <a name="in-this-section"></a>Dans cette section

 [EventWaitHandle](eventwaithandle.md)  
 La classe <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType> peut représenter des événements à réinitialisation automatique ou manuelle et des événements locaux ou des événements système nommés.  
  
 [AutoResetEvent](autoresetevent.md)  
 La classe <xref:System.Threading.AutoResetEvent?displayProperty=nameWithType> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui se réinitialise automatiquement.  
  
 [ManualResetEvent and ManualResetEventSlim](manualresetevent-and-manualreseteventslim.md)  
 La classe <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui doit être réinitialisé manuellement. La classe <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> est une version légère et plus rapide qui peut être utilisée pour les événements dans le même processus.  
  
 [CountdownEvent](countdownevent.md)  
 La classe <xref:System.Threading.CountdownEvent?displayProperty=nameWithType> représente un moyen simple d’implémenter des modèles de parallélisme de type duplication/jointure dans un code qui utilise des handles d’attente.  

## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.Threading.Barrier?displayProperty=nameWithType>
- [Fonctionnalités et objets de threading](threading-objects-and-features.md)
- [Éléments fondamentaux du threading managé](managed-threading-basics.md)
