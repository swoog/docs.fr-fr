---
title: ManualResetEvent et ManualResetEventSlim
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], ManualResetEvent class
- ManualResetEvent class, about ManualResetEvent class
ms.assetid: 465fdcf9-ba24-4d8d-a43f-d983b7cb0cc6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d69336bd9e4f4ec06e8319d19c1cdab5cf6e1c89
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33583316"
---
# <a name="manualresetevent-and-manualreseteventslim"></a>ManualResetEvent et ManualResetEventSlim
La classe <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> représente un événement de descripteur d’attente local qui doit être réinitialisé manuellement après avoir été signalé. Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle?displayProperty=nameWithType>. Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation manuelle.  
  
 Un <xref:System.Threading.ManualResetEvent> objet reste signalé jusqu'à ce que sa méthode <xref:System.Threading.EventWaitHandle.Reset%2A?displayProperty=nameWithType> soit appelée. Lorsque l’état de l’objet est signalé, un nombre indéterminé de threads en attente, ou de threads attendant l’événement une fois celui-ci signalé, peuvent être libérés. <xref:System.Threading.ManualResetEvent> correspond à un appel `CreateEvent` Win32 spécifiant `true` pour l’argument `bManualReset`.  
  
 Dans [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], vous pouvez utiliser la classe <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType> pour améliorer les performances lorsque les temps d’attente prévus sont très courts et lorsque l’événement ne franchit aucune limite de processus. <xref:System.Threading.ManualResetEventSlim> utilise la rotation intensive pendant une courte période, tout en attendant la signalisation de l’événement. Lorsque les temps d’attente sont courts, la rotation peut s’avérer beaucoup moins coûteuse que les descripteurs d’attente. Toutefois, si l’événement n’est pas signalé pendant une période définie, <xref:System.Threading.ManualResetEventSlim> recourt à une attente de descripteur d’événement classique.  
  
## <a name="see-also"></a>Voir aussi  
 [Thread](../../../docs/standard/threading/index.md)  
 [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)  
 [Descripteurs d’attente](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)  
 [AutoResetEvent](../../../docs/standard/threading/autoresetevent.md)  
 [SpinWait](../../../docs/standard/threading/spinwait.md)  
 [Semaphore et SemaphoreSlim](../../../docs/standard/threading/semaphore-and-semaphoreslim.md)
