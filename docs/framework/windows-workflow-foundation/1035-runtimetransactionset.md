---
title: 1035 - RuntimeTransactionSet
ms.date: 03/30/2017
ms.assetid: 03b37de9-778c-4beb-b0e3-de73ece6088e
ms.openlocfilehash: 198e11dd94b0ad5cdc1e01c3611280754ca081d3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510032"
---
# <a name="1035---runtimetransactionset"></a>1035 - RuntimeTransactionSet
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|1035|  
|Mots clés|WFRuntime|  
|Niveau|Verbose|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'une activité a défini la transaction d'exécution.  
  
## <a name="message"></a>Message  
 La transaction runtime a été définie par l’activité '%1', DisplayName : '%2', InstanceId : '%3'.  L’exécution isolée à l’activité '%4', DisplayName : '%5', InstanceId : '%6'.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Activité|xs:string|Nom de type de l'activité.|  
|DisplayName|xs:string|Nom complet de l'activité.|  
|InstanceId|xs:string|ID d'instance de l'activité.|  
|IsolatedActivity|xs:string|Nom de type de l'activité dans laquelle la transaction est isolée.|  
|IsolatedActivityDisplayName|xs:string|Nom complet de l'activité dans laquelle la transaction est isolée.|  
|IsolatedActivityInstanceId|xs:string|ID d'instance de l'activité dans laquelle la transaction est isolée.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
