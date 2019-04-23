---
ms.openlocfilehash: 94fad6fe910da6c528c5e13f529a6db274e07d5c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235350"
---
### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Changement de comportement des méthodes Task.WaitAll avec des arguments de délai d’attente

|   |   |
|---|---|
|Détails|<xref:System.Threading.Tasks.Task.WaitAll%2A?displayProperty=nameWithType> Le comportement est devenu plus cohérent dans .NET Framework 4.5. Dans .NET Framework 4, ces méthodes présentaient un comportement incohérent. Lorsque le délai d'attente expirait, si une ou plusieurs tâches étaient terminées ou annulées avant l'appel de la méthode, la méthode levait une exception <xref:System.AggregateException?displayProperty=name>. Lorsque le délai d’attente expirait, si aucune tâche n’était terminée ou annulée avant l’appel de la méthode alors qu’une ou plusieurs tâches adoptaient ces états après l’appel de la méthode, la méthode retournait la valeur false.<br/><br/>Dans .NET Framework 4.5, ces surcharges de méthode retournent désormais la valeur false si des tâches sont toujours en cours d’exécution quand l’intervalle de délai d’attente expire, et elles ne lèvent une exception <xref:System.AggregateException?displayProperty=name> que si une tâche d’entrée a été annulée (que cette annulation soit intervenue avant ou après l’appel de méthode) et qu’aucune autre tâche n’est en cours d’exécution.|
|Suggestion|Si une exception <xref:System.AggregateException?displayProperty=name> a été interceptée dans le but de détecter une tâche ayant été annulée avant l’appel de <xref:System.Threading.Tasks.Task.WaitAll%2A>, ce code doit procéder à la même détection par le biais de la propriété <xref:System.Threading.Tasks.Task.IsCanceled%2A> (par exemple, .Any(t =&gt; t.IsCanceled)), puisque .NET Framework 4.6 lève une exception seulement si toutes les tâches attendues sont terminées avant le délai d’attente.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|
