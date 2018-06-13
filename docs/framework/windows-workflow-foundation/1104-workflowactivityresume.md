---
title: 1104 - WorkflowActivityResume
ms.date: 03/30/2017
ms.assetid: 7fe95d1e-34bd-43ca-b92e-587d2d248fff
ms.openlocfilehash: 4c9ae5fd386fc93ea19578097aa4e0afdda527e2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33511054"
---
# <a name="1104---workflowactivityresume"></a>1104 - WorkflowActivityResume
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|1104|  
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
