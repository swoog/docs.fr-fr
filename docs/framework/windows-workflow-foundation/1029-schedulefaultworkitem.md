---
title: 1029 - ScheduleFaultWorkItem
ms.date: 03/30/2017
ms.assetid: 3a56b29e-f740-459d-8576-d81e58bf5a03
ms.openlocfilehash: f5beab91f7dd39a3f8ed3b76d6c0a1ddd9bd77c3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="1029---schedulefaultworkitem"></a>1029 - ScheduleFaultWorkItem
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|1029|  
|Mots clés|WFRuntime|  
|Niveau|Verbose|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'un FaultWorkItem a été planifié.  
  
## <a name="message"></a>Message  
 Un FaultWorkItem a été planifié pour l’activité '%1', DisplayName : '%2', InstanceId : '%3'.  L'exception a été propagée à partir de l'activité « %4 », DisplayName : « %5 », InstanceId : « %6 ».  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|FaultActivity|xs:string|Nom de type de l'activité d'erreur.|  
|FaultActivityDisplayName|xs:string|Nom complet de l'activité d'erreur.|  
|FaultActivityInstanceId|xs:string|ID d'instance de l'activité d'erreur.|  
|ExceptionActivity|xs:string|Nom de type de l'activité qui a levé l'exception.|  
|ExceptionActivityDisplayName|xs:string|Nom complet de l'activité qui a levé l'exception.|  
|ExceptionActivityInstanceId|xs:string|ID d'instance de l'activité ayant levé l'exception.|  
|Exception|xs:string|Détails de l'exception|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
