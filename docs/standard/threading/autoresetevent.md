---
title: AutoResetEvent
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], AutoResetEvent class
- AutoResetEvent class
ms.assetid: 6d39c48d-6b37-4a9b-8631-f2924cfd9c18
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 38efbe0ecd88c02752d610de4b1eec8b62eca1f8
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46937543"
---
# <a name="autoresetevent"></a>AutoResetEvent
La classe <xref:System.Threading.AutoResetEvent> représente un événement de handle d’attente local qui se réinitialise automatiquement quand il est signalé, après avoir libéré un thread en attente unique. Cette classe représente un cas spécial de sa classe de base, <xref:System.Threading.EventWaitHandle>. Consultez la documentation conceptuelle de [EventWaitHandle](../../../docs/standard/threading/eventwaithandle.md) relative à l’utilisation et aux fonctionnalités des événements de réinitialisation automatique.  
  
 Un objet <xref:System.Threading.AutoResetEvent> est automatiquement réinitialisé à l’état non signalé par le système après la libération d’un thread en attente unique. Si aucun thread n’attend, l’état de l’objet d’événement reste signalé.
  
 Pour obtenir un exemple qui utilise <xref:System.Threading.AutoResetEvent>, consultez <xref:System.Threading.Monitor>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.ManualResetEvent>  
- <xref:System.Threading.Monitor>  
- [EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent](../../../docs/standard/threading/eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)  
- [Thread](../../../docs/standard/threading/index.md)  
- [Fonctionnalités et objets de threading](../../../docs/standard/threading/threading-objects-and-features.md)  
- [Descripteurs d’attente](https://msdn.microsoft.com/library/48d10b6f-5fd7-407c-86ab-0179aef72489)
