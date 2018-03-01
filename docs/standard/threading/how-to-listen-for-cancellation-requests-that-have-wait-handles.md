---
title: "Comment : écouter les demandes d'annulation avec des handles d'attente"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cancellation, waiting with wait handles
ms.assetid: 6e2aa49b-fc84-4bcf-962b-17db98b7edcb
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: a0998703ef5b27b4de725a2c2adcfc3d9a2135b9
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-listen-for-cancellation-requests-that-have-wait-handles"></a>Comment : écouter les demandes d'annulation avec des handles d'attente
Si une méthode est bloquée pendant qu’elle attend qu’un événement soit signalé, elle ne peut pas vérifier la valeur du jeton d’annulation ni répondre en temps voulu. Le premier exemple montre comment résoudre ce problème quand vous travaillez avec des événements tels que <xref:System.Threading.ManualResetEvent?displayProperty=nameWithType> qui ne prennent pas en charge l’infrastructure d’annulation unifiée. Le deuxième exemple montre une approche plus simple qui utilise <xref:System.Threading.ManualResetEventSlim?displayProperty=nameWithType>, qui prend en charge l’annulation unifiée.  
  
> [!NOTE]
>  Quand l'option Uniquement mon code est activée, Visual Studio, dans certains cas, peut s'arrêter sur la ligne qui lève l'exception et afficher un message d'erreur indiquant que l'exception n'est pas gérée par le code utilisateur. Cette erreur est sans gravité. Vous pouvez appuyer sur F5 pour continuer et voir le comportement de gestion des exceptions qui est illustré dans les exemples ci-dessous. Pour empêcher Visual Studio de s'arrêter sur la première erreur, il suffit de désactiver la case à cocher « Uniquement mon code » sous **Outils, Options, Débogage, Général**.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Threading.ManualResetEvent> pour montrer comment débloquer des handles d’attente qui ne prennent pas en charge l’annulation unifiée.  
  
 [!code-csharp[Cancellation#9](../../../samples/snippets/csharp/VS_Snippets_Misc/cancellation/cs/cancellationex9.cs#9)]
 [!code-vb[Cancellation#9](../../../samples/snippets/visualbasic/VS_Snippets_Misc/cancellation/vb/cancellationex9.vb#9)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise un <xref:System.Threading.ManualResetEventSlim> pour montrer comment débloquer des primitives de coordination qui ne prennent pas en charge l’annulation unifiée. La même approche peut être utilisée avec d’autres primitives de coordination légères, telles que <xref:System.Threading.Semaphore>`Slim` et <xref:System.Threading.CountdownEvent>.  
  
 [!code-csharp[Cancellation#10](../../../samples/snippets/csharp/VS_Snippets_Misc/cancellation/cs/cancellationex10.cs#10)]
 [!code-vb[Cancellation#10](../../../samples/snippets/visualbasic/VS_Snippets_Misc/cancellation/vb/cancellationex10.vb#10)]  
  
## <a name="see-also"></a>Voir aussi  
 [Annulation dans les threads managés](../../../docs/standard/threading/cancellation-in-managed-threads.md)
