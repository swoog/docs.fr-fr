---
title: "Annulation de threads de façon coopérative"
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
- threads, cancellation
ms.assetid: d2d6d5fd-e263-4fa0-847b-2fc3e0d82337
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 334cbcf8b4a888dbac5962c0fd668673e15e0e29
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="canceling-threads-cooperatively"></a>Annulation de threads de façon coopérative
Avant [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], .NET Framework n’offrait aucune fonction intégrée permettant d’annuler, de manière coopérative, un thread après son démarrage. Toutefois, dans [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], vous pouvez utiliser des jetons d’annulation pour annuler des threads, tout comme vous pouvez les utiliser pour annuler des objets <xref:System.Threading.Tasks.Task?displayProperty=nameWithType> ou des requêtes PLINQ. Bien que la classe <xref:System.Threading.Thread?displayProperty=nameWithType> n’offre pas de prise en charge intégrée pour les jetons d’annulation, vous pouvez transmettre un jeton à une procédure de thread à l’aide du constructeur <xref:System.Threading.Thread> qui prend un délégué <xref:System.Threading.ParameterizedThreadStart>. L'exemple suivant illustre la procédure à suivre pour réaliser cette opération.  
  
 [!code-csharp[Cancellation#14](../../../samples/snippets/csharp/VS_Snippets_Misc/cancellation/cs/CooperativeThreads.cs#14)]
 [!code-vb[Cancellation#14](../../../samples/snippets/visualbasic/VS_Snippets_Misc/cancellation/vb/CooperativeThreads.vb#14)]  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation des threads et du threading](../../../docs/standard/threading/using-threads-and-threading.md)
