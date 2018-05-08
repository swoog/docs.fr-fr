---
title: 1003 - WorkflowInstanceCanceled
ms.date: 03/30/2017
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
ms.openlocfilehash: c76a2dab6a95bda7f3969af07f814aba30071c7f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="1003---workflowinstancecanceled"></a>1003 - WorkflowInstanceCanceled
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|1003|  
|Mots clés|WFRuntime|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'une instance de workflow s'est terminée à l'état Canceled.  
  
## <a name="message"></a>Message  
 ID WorkflowInstance : « %1 » s'est terminé à l'état Canceled.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|WorkflowInstanceId|`xs:string`|ID d'instance pour le workflow|  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
