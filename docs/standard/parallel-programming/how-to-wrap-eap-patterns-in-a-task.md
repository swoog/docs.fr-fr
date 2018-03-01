---
title: "Comment : exposer des modèles EAP à l’aide d’une tâche"
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
- tasks, how to wrap EAP patterns
ms.assetid: f11ed467-af2f-4504-8a2e-299a6c36d44e
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 9e451c3ce8bb50cb17da7fef25ae0317bcb82c3e
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="how-to-wrap-eap-patterns-in-a-task"></a>Comment : exposer des modèles EAP à l’aide d’une tâche
L’exemple suivant montre comment exposer une séquence arbitraire d’opérations EAP (modèle asynchrone basé sur des événements) comme une seule tâche à l’aide d’un <xref:System.Threading.Tasks.TaskCompletionSource%601>. L’exemple montre également comment utiliser un <xref:System.Threading.CancellationToken> pour appeler les méthodes d’annulation intégrées sur les objets <xref:System.Net.WebClient>.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[FromAsync#08](../../../samples/snippets/csharp/VS_Snippets_Misc/fromasync/cs/fromasync.cs#08)]
 [!code-vb[FromAsync#08](../../../samples/snippets/visualbasic/VS_Snippets_Misc/fromasync/vb/module1.vb#08)]  
  
## <a name="see-also"></a>Voir aussi  
 [Bibliothèque parallèle de tâches (TPL) et programmation asynchrone .NET Framework](../../../docs/standard/parallel-programming/tpl-and-traditional-async-programming.md)
