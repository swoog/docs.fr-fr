---
title: 3502 - InferredOperationDescription
ms.date: 03/30/2017
ms.assetid: 6aebb614-3c72-4537-ba11-3cc7200ef1f1
ms.openlocfilehash: 752cd73066c3c15ecbb36c40c417ee84b3fcf184
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33512003"
---
# <a name="3502---inferredoperationdescription"></a>3502 - InferredOperationDescription
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|3502|  
|Mots clés|WFServices|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Indique qu'un OperationDescription a été déduit de WorkflowService.  
  
## <a name="message"></a>Message  
 OperationDescription avec Name='%1' dans le contrat « %2 » a été déduit de WorkflowService. IsOneWay=%3.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|OperationName|xs:string|Nom de l'opération.|  
|ContractName|xs:string|Nom du contrat.|  
|IsOneWay|xs:string|True ou False indiquant si le contrat est unidirectionnel.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
