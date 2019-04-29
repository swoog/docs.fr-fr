---
title: 3557 - TransactedReceiveScopeEndCommitFailed
ms.date: 03/30/2017
ms.assetid: 079f0188-8146-49ee-b6ae-a08f4e4d2b9b
ms.openlocfilehash: 444fa2e51322edd793f709fd3f92c5f9fe826522
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774450"
---
# <a name="3557---transactedreceivescopeendcommitfailed"></a>3557 - TransactedReceiveScopeEndCommitFailed
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|3557|  
|Mots clés|WFServices|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Indique que l'appel à EndCommit sur un CommittableTransaction a levé une exception TransactionException.  
  
## <a name="message"></a>Message  
 L'appel à EndCommit sur le CommittableTransaction avec l'ID = « %1 » a levé un TransactionException avec le message suivant : « %2 ».  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|TransactionId|xs:string|ID de CommittableTransaction.|  
|Exception|xs:string|Détails de l'exception|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
