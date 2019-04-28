---
title: 1104 - WorkflowActivityResume
ms.date: 03/30/2017
ms.assetid: 7fe95d1e-34bd-43ca-b92e-587d2d248fff
ms.openlocfilehash: 4c9ae5fd386fc93ea19578097aa4e0afdda527e2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924122"
---
# <a name="1104---workflowactivityresume"></a>1104 - WorkflowActivityResume
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|1104|  
|Mots clés|WFRuntime|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'une activité du flux de travail a été reprise.  
  
## <a name="message"></a>Message  
 ID WorkflowInstance : « %1 » Activité E2E  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|WorkflowInstanceId|xs:string|ID de l'instance de flux de travail.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
