---
title: 'Procédure : ajouter et prendre des éléments individuellement dans un BlockingCollection'
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- thread-safe collections, blocking dictionary
ms.assetid: 38f2f3d8-15e5-4bf4-9c83-2b5b6f22bad1
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0e24c6b5aa02e8bc7ca4bcbf2c69bffd06216962
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535439"
---
# <a name="how-to-add-and-take-items-individually-from-a-blockingcollection"></a>Procédure : ajouter et prendre des éléments individuellement dans un BlockingCollection
Cet exemple montre comment ajouter et supprimer des éléments dans un <xref:System.Collections.Concurrent.BlockingCollection%601> de manière bloquante et non bloquante. Pour plus d’informations sur <xref:System.Collections.Concurrent.BlockingCollection%601>, consultez [Vue d’ensemble de BlockingCollection](../../../../docs/standard/collections/thread-safe/blockingcollection-overview.md).  
  
 Pour un exemple illustrant comment énumérer un <xref:System.Collections.Concurrent.BlockingCollection%601> jusqu’à ce qu’il soit vide et qu’aucun autre élément ne soit ajouté, consultez [Guide pratique : utiliser la boucle ForEach pour supprimer les éléments d’un BlockingCollection](../../../../docs/standard/collections/thread-safe/how-to-use-foreach-to-remove.md).
  
## <a name="example"></a>Exemple  
 Ce premier exemple montre comment ajouter et prendre des éléments pour que les opérations soient bloquées si la collection est temporairement vide (lors de la prise) ou à la capacité maximale (lors de l’ajout), ou si un délai d’expiration spécifié s’est écoulé. Notez que le blocage en cas de capacité maximale est activé uniquement quand le BlockingCollection a été créé avec une capacité maximale spécifiée dans le constructeur.  
  
 [!code-csharp[CDS_BlockingCollection#01](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds_blockingcollection/cs/example01.cs#01)]
 [!code-vb[CDS_BlockingCollection#01](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_blockingcollection/vb/simpleblocking.vb#01)]  
  
## <a name="example"></a>Exemple  
 Ce deuxième exemple montre comment ajouter et prendre des éléments pour que les opérations ne soient pas bloquées. Si aucun élément n’est présent, si la capacité maximale sur une collection limitée a été atteinte ou si le délai d’expiration s’est écoulé, l’opération <xref:System.Collections.Concurrent.BlockingCollection%601.TryAdd%2A> ou <xref:System.Collections.Concurrent.BlockingCollection%601.TryTake%2A> retourne false. Cela permet au thread d’effectuer un autre travail utile pendant ce temps-là, puis de réessayer ultérieurement de récupérer un élément ou d’ajouter l’élément qui n’a pas pu être ajouté précédemment. Le programme montre aussi comment implémenter l’annulation lors de l’accès à un <xref:System.Collections.Concurrent.BlockingCollection%601>.  
  
 [!code-csharp[CDS_BlockingCollection#02](../../../../samples/snippets/csharp/VS_Snippets_Misc/cds_blockingcollection/cs/example02.cs#02)]
 [!code-vb[CDS_BlockingCollection#02](../../../../samples/snippets/visualbasic/VS_Snippets_Misc/cds_blockingcollection/vb/nonblockingbc.vb#02)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Collections.Concurrent?displayProperty=nameWithType>
- [Vue d'ensemble de BlockingCollection](../../../../docs/standard/collections/thread-safe/blockingcollection-overview.md)
