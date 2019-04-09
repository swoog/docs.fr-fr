---
title: Événement ETW de pile
ms.date: 03/30/2017
helpviewer_keywords:
- stack event [.NET Framework]
- ETW, stack event (CLR)
ms.assetid: f612fa5b-4b62-4593-a19e-85c9b1018dce
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a7cba2bd1dd5b83e29c7a6c192a1a7e5e2d33ecc
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59076471"
---
# <a name="stack-etw-event"></a>Événement ETW de pile
L’événement de pile doit être utilisé conjointement avec d’autres événements pour générer des arborescences d’appels de procédure après le déclenchement d’un événement. Il est enregistré quand le fournisseur du runtime est activé. Il s’agit d’un événement très fréquent, car il est déclenché à chaque déclenchement d’un autre événement runtime. Pour cette raison, nous vous recommandons d’utiliser cet événement avec précaution.  
  
 Le tableau suivant montre les mots clés et les niveaux. (Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)  
  
|Mot clé pour déclencher l'événement|Niveau|  
|-----------------------------------|-----------|  
|`StackKeyword` (0 x 40000000)|LogAlways(0)|  
  
 Le tableau ci-dessous montre les informations liées aux événements.  
  
|Événement|ID d'événement|Moment du déclenchement|  
|-----------|--------------|-----------------|  
|`CLRStackWalk`|82|Conjointement avec d’autres événements pour générer les arborescences des appels de procédure après un événement.|  
  
 Le tableau ci-dessous montre les données liées aux événements.  
  
|Nom du champ|Type de données|Description|  
|----------------|---------------|-----------------|  
|ClrInstanceID|win:Uint16|Identificateur de runtime unique.|  
|Reserved1|win:UInt8|Réservé.|  
|Reserved2|win:UInt8|Réservé.|  
|FrameCount|win:UInt32|Nombre de frames dans l’arborescence des appels de procédure.|  
|Stack|win:Pointer|Colonnes de pointeurs d’instruction.|  
  
## <a name="see-also"></a>Voir aussi

- [Événements ETW du CLR](../../../docs/framework/performance/clr-etw-events.md)
