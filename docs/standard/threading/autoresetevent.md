---
title: AutoResetEvent
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- threading [.NET Framework], AutoResetEvent class
- AutoResetEvent class
ms.assetid: 6d39c48d-6b37-4a9b-8631-f2924cfd9c18
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 71933d0be804fdf68b0dc602902343f2d88b8c82
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="autoresetevent"></a>AutoResetEvent
La classe <xref:System.Threading.AutoResetEvent> représente un événement de handle d’attente local qui se réinitialise automatiquement quand il est signalé, après avoir libéré un thread en attente unique. Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle>. Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation automatique.  
  
 Un objet <xref:System.Threading.AutoResetEvent> est automatiquement réinitialisé à l’état non signalé par le système après la libération d’un thread en attente unique. Si aucun thread n’attend, l’état de l’objet d’événement reste signalé. <xref:System.Threading.AutoResetEvent> correspond à un appel `CreateEvent` Win32 spécifiant `false` pour l’argument `bManualReset`.  
  
 Pour obtenir un exemple utilisant <xref:System.Threading.AutoResetEvent>, consultez [Monitor](http://msdn.microsoft.com/library/33fe4aef-b44b-42fd-9e72-c908e39e75db).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Threading.ManualResetEvent>  
 <xref:System.Threading.Monitor>  
 [EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
 [Thread](../../../docs/standard/threading/index.md)  
 [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)  
 [Descripteurs d’attente](http://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
