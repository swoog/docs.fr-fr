---
title: 39458 - TrackingRecordTruncated
ms.date: 03/30/2017
ms.assetid: 5352f0eb-d571-454a-bab5-e2162888b218
ms.openlocfilehash: 416feb4073b31178b016ae72c9cd85e15c4a68c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774411"
---
# <a name="39458---trackingrecordtruncated"></a>39458 - TrackingRecordTruncated
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|39458|  
|Mots clés|WFTracking|  
|Niveau|Warning|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'un enregistrement de suivi a été tronqué. Les données de variables/annotations/utilisateur ont été supprimées.  
  
## <a name="message"></a>Message  
 Enregistrement de suivi %1 tronqué écrit dans la session ETW avec le fournisseur %2. Les données de variables/annotations/utilisateur ont été supprimées  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|RecordNumber|xs:string|Numéro d'enregistrement de suivi.|  
|ProviderId|xs:string|ID du fournisseur ETW.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
