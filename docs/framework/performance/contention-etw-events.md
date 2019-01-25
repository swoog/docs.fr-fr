---
title: Événements ETW de conflit - .NET
ms.date: 03/30/2017
helpviewer_keywords:
- contention events [.NET Framework]
- ETW, contention events (CLR)
ms.assetid: 6933e753-2f2a-425b-ae84-42138c957d76
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 95f56a6c8b51c58ed36d5d0de428bf57b728009c
ms.sourcegitcommit: 5dcfeb59179e81071f54840d4902cbe00b184294
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54857643"
---
# <a name="contention-etw-events"></a>Événements ETW de conflit

Les événements de conflit sont déclenchés chaque fois qu’il existe un conflit sur les verrous <xref:System.Threading.Monitor?displayProperty=nameWithType> ou les verrous natifs utilisés par le runtime. Le conflit se produit quand un thread attend un verrou alors qu’un autre thread possède ce verrou.

Le tableau suivant montre le mot clé sous lequel les événements de conflit sont déclenchés, ainsi que le niveau des événements. Pour plus d’informations, consultez [CLR ETW Keywords and Levels](clr-etw-keywords-and-levels.md).

|Mot clé pour déclencher l'événement|Niveau|
|-----------------------------------|-----------|
|`ContentionKeyword` (0x4000)|Informatif (4)|

Le tableau suivant présente des informations sur les événements :

|Événement|ID d'événement|Moment du déclenchement|
|-----------|--------------|-----------------|
|`ContentionStart_V1`|81|Le conflit démarre. Cet événement n’inclut pas le temps qui s’écoule avant qu’un thread ne commence à attendre l’acquisition d’un verrou. Il est déclenché uniquement quand l’attente commence.|
|`ContentionStop`|91|Le conflit se termine.|

Le tableau suivant présente les données d’événement :

|Nom du champ|Type de données|Description|
|----------------|---------------|-----------------|
|Indicateurs|win:UInt8|0 pour managé ; 1 pour natif.|
|ClrInstanceID|win:UInt16|ID unique de l’instance de CLR.|

## <a name="see-also"></a>Voir aussi

- [Événements ETW du CLR](clr-etw-events.md)
