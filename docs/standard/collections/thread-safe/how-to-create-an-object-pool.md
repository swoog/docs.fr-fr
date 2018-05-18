---
title: "Guide pratique : créer un pool d'objets à l'aide d'un ConcurrentBag"
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- object pool, in .NET Framework
ms.assetid: 0480e7ff-b6f9-480e-a889-2ed4264d8372
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9239a38d1970a052567f111b57be2b6596f1e5f1
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="how-to-create-an-object-pool-by-using-a-concurrentbag"></a>Comment : créer un pool d'objets à l'aide d'un ConcurrentBag
L’exemple suivant montre comment utiliser un conteneur simultané pour implémenter un pool d’objets. Les pools d’objet peuvent améliorer les performances de l’application dans les cas où vous avez besoin de plusieurs instances d’une classe et que la création ou la destruction de la classe est coûteuse. Quand un programme client demande un nouvel objet, le pool d’objets tente d’abord d’en fournir un qui a été créé et retourné au pool. Si aucun n’est disponible, et uniquement dans ce cas, un nouvel objet est créé.  
  
 <xref:System.Collections.Concurrent.ConcurrentBag%601> est utilisé pour stocker les objets, car il prend en charge l’insertion et la suppression rapides, en particulier quand le même thread ajoute et supprime des éléments. Cet exemple peut être augmenté davantage pour être généré autour d’un <xref:System.Collections.Concurrent.IProducerConsumerCollection%601>, que la structure de données de conteneur implémente, comme le font <xref:System.Collections.Concurrent.ConcurrentQueue%601> et <xref:System.Collections.Concurrent.ConcurrentStack%601>.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[CDS#04](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds/cs/objectpool.cs#04)]
 [!code-vb[CDS#04](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds/vb/objectpool04.vb#04)]  
  
## <a name="see-also"></a>Voir aussi  
 [Collections thread-safe](../../../../docs/standard/collections/thread-safe/index.md)
