---
title: EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- wait handles
- threading [.NET Framework], EventWaitHandle class
- event wait handles [.NET Framework]
ms.assetid: cd94fc34-ac15-427f-b723-a1240a4fab7d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 543853f581436a5fb7e5c897012b99bef20dc289
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33582933"
---
# <a name="eventwaithandle-autoresetevent-countdownevent-manualresetevent"></a>EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent
Les handles d’attente d’événements permettent aux threads de synchroniser les activités en se signalant et en attendant les signaux des uns et des autres. Ces événements de synchronisation s’appuient sur des handles d’attente Win32 et se divisent en deux types : ceux qui se réinitialisent automatiquement et ceux qui sont réinitialisés manuellement.  
  
 Les handles d’attente d’événements sont utiles dans la majorité des scénarios de synchronisation de la classe <xref:System.Threading.Monitor>. Les handles d’attente d’événement sont souvent plus faciles à utiliser que les méthodes <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> et <xref:System.Threading.Monitor.Pulse%2A?displayProperty=nameWithType>, et ils offrent un meilleur contrôle du signalement. Les handles d’attente d’événements nommés peuvent également servir à synchroniser les activités entre les différents processus et domaines d’application, tandis que les moniteurs sont liés localement à un domaine d’application.  
  
## <a name="in-this-section"></a>Dans cette section  
 [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md)  
 La classe <xref:System.Threading.EventWaitHandle> peut représenter des événements à réinitialisation automatique ou manuelle et des événements locaux ou des événements système nommés.  
  
 [AutoResetEvent](../../../docs/standard/threading/autoresetevent.md)  
 La classe <xref:System.Threading.AutoResetEvent> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui se réinitialise automatiquement.  
  
 [ManualResetEvent and ManualResetEventSlim](../../../docs/standard/threading/manualresetevent-and-manualreseteventslim.md)  
 La classe <xref:System.Threading.ManualResetEvent> dérive de la classe <xref:System.Threading.EventWaitHandle> et représente un événement local qui doit être réinitialisé manuellement. La classe <xref:System.Threading.ManualResetEventSlim> est une version légère et plus rapide qui peut être utilisée pour les événements dans le même processus.  
  
 [CountdownEvent](../../../docs/standard/threading/countdownevent.md)  
 La classe <xref:System.Threading.CountdownEvent> représente un moyen simple d’implémenter des modèles de parallélisme de type duplication/jointure dans un code qui utilise des handles d’attente.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Descripteurs d’attente](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)  
 La classe <xref:System.Threading.WaitHandle> est la classe de base des classes <xref:System.Threading.EventWaitHandle>, <xref:System.Threading.Semaphore> et <xref:System.Threading.Mutex>. Elle contient des méthodes statiques telles que <xref:System.Threading.WaitHandle.SignalAndWait%2A> et <xref:System.Threading.WaitHandle.WaitAll%2A> qui sont utiles quand vous travaillez avec tous les types de handles d’attente.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.EventWaitHandle>  
 <xref:System.Threading.WaitHandle>  
 <xref:System.Threading.AutoResetEvent>  
 <xref:System.Threading.ManualResetEvent>  
 [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)  
 [Éléments fondamentaux du threading managé](../../../docs/standard/threading/managed-threading-basics.md)
