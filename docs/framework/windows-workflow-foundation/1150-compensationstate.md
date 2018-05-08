---
title: 1150 - CompensationState
ms.date: 03/30/2017
ms.assetid: eb015842-cc5a-47be-bce5-6af39e567723
ms.openlocfilehash: 61613a27c4d4d8fb0b206246fef25ae87def47a5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="1150---compensationstate"></a>1150 - CompensationState
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|1150|  
|Mots clés|WFActivities|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique un changement d'état d'un CompensableActivity.  
  
## <a name="message"></a>Message  
 CompensableActivity « %1 » est dans l'état « %2 ».  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|DisplayName|xs:string|Nom complet de l'activité.|  
|État|xs:string|État de compensation.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
