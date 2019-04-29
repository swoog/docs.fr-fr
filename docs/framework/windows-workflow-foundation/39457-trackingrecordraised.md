---
title: 39457 - TrackingRecordRaised
ms.date: 03/30/2017
ms.assetid: 5a2731d1-c731-4b79-bb69-016cb69ef481
ms.openlocfilehash: 104d3fb4b544172001051be7bccc3721cf8d6d1a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774437"
---
# <a name="39457---trackingrecordraised"></a>39457 - TrackingRecordRaised
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|39457|  
|Mots clés|WFRuntime|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'un TrackingRecord a été déclenché dans un TrackingParticipant.  
  
## <a name="message"></a>Message  
 Enregistrement suivi %1 élevé à %2.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|RecordNumber|xs:string|Numéro d'enregistrement de suivi.|  
|ParticipantId|xs:string|Participant de suivi.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
