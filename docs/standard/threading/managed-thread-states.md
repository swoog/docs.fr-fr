---
title: États des threads managés
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], states
ms.assetid: 63890d5e-6025-4a7c-aaf0-d8bfd54b455f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a55409cd2c3bed2bc09db10622de1cceab934112
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46711144"
---
# <a name="managed-thread-states"></a>États des threads managés
La propriété <xref:System.Threading.Thread.ThreadState%2A?displayProperty=nameWithType> fournit un masque de bits qui indique l’état actuel du thread. Un thread se trouve toujours dans au moins un des états possibles de l’énumération <xref:System.Threading.ThreadState> et peut être dans plusieurs états en même temps.  
  
> [!IMPORTANT]
>  L’état des threads n’est utile que dans quelques scénarios de débogage. Votre code ne doit jamais utiliser l’état des threads pour synchroniser les activités des threads.  
  
 Quand vous créez un thread managé, il est dans l’état <xref:System.Threading.ThreadState.Unstarted> . Le thread reste dans l’état <xref:System.Threading.ThreadState.Unstarted> jusqu’à ce qu’il soit placé dans l’état Démarré par le système d’exploitation. L’appel à <xref:System.Threading.Thread.Start%2A> informe le système d’exploitation que le thread peut être démarré ; il ne change pas l’état du thread.  
  
 Les threads non managés qui entrent l’environnement managé sont déjà dans l’état Démarré. Une fois qu’un thread est dans l’état Démarré, plusieurs actions peut le faire changer d’état. Le tableau suivant répertorie les actions qui provoquent un changement d’état, ainsi que le nouvel état correspondant.  
  
|Action|Nouvel état résultant|  
|------------|-------------------------|  
|Le constructeur de la classe <xref:System.Threading.Thread> est appelé.|<xref:System.Threading.ThreadState.Unstarted>|  
|Un autre thread appelle <xref:System.Threading.Thread.Start%2A?displayProperty=nameWithType>.|<xref:System.Threading.ThreadState.Unstarted>|  
|Le thread répond à <xref:System.Threading.Thread.Start%2A?displayProperty=nameWithType> et démarre l’exécution.|<xref:System.Threading.ThreadState.Running>|  
|Le thread appelle <xref:System.Threading.Thread.Sleep%2A?displayProperty=nameWithType>.|<xref:System.Threading.ThreadState.WaitSleepJoin>|  
|Le thread appelle <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> sur un autre objet.|<xref:System.Threading.ThreadState.WaitSleepJoin>|  
|Le thread appelle <xref:System.Threading.Thread.Join%2A?displayProperty=nameWithType> sur un autre thread.|<xref:System.Threading.ThreadState.WaitSleepJoin>|  
|Un autre thread appelle <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType>.|<xref:System.Threading.ThreadState.SuspendRequested>|  
|Le thread répond à une demande <xref:System.Threading.Thread.Suspend%2A?displayProperty=nameWithType> .|<xref:System.Threading.ThreadState.Suspended>|  
|Un autre thread appelle <xref:System.Threading.Thread.Resume%2A?displayProperty=nameWithType>.|<xref:System.Threading.ThreadState.Running>|  
|Un autre thread appelle <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType>.|<xref:System.Threading.ThreadState.AbortRequested>|  
|Le thread répond à un <xref:System.Threading.Thread.Abort%2A?displayProperty=nameWithType>.|<xref:System.Threading.ThreadState.Aborted>, puis <xref:System.Threading.ThreadState.Stopped>|  
  
 Étant donné que l’état de <xref:System.Threading.ThreadState.Running> a la valeur 0, il n’est pas possible d’effectuer un test de bits pour découvrir cet état. Au lieu de cela, le test suivant (en pseudo-code) peut être utilisé :  
  
```  
if ((state & (Unstarted | Stopped)) == 0)   // implies Running     
```  
  
 Les threads se trouvent souvent dans plusieurs états à un moment donné. Par exemple, si un thread est bloqué sur un appel de <xref:System.Threading.Monitor.Wait%2A?displayProperty=nameWithType> et qu’un autre thread appelle <xref:System.Threading.Thread.Abort%2A> sur ce même thread, le thread sera à la fois dans l’état <xref:System.Threading.ThreadState.WaitSleepJoin> et dans l’état <xref:System.Threading.ThreadState.AbortRequested>. Dans ce cas, dès que le thread retourne de l’appel à <xref:System.Threading.Monitor.Wait%2A> ou est interrompu, il reçoit <xref:System.Threading.ThreadAbortException>.  
  
 Une fois qu’un thread quitte l’état <xref:System.Threading.ThreadState.Unstarted> à la suite d’un appel à <xref:System.Threading.Thread.Start%2A>, il ne peut jamais revenir à l’état <xref:System.Threading.ThreadState.Unstarted> . Un thread ne peut jamais quitter l’état <xref:System.Threading.ThreadState.Stopped> .  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.ThreadAbortException>  
- <xref:System.Threading.Thread>  
- <xref:System.Threading.ThreadState>  
- [Thread](../../../docs/standard/threading/index.md)
