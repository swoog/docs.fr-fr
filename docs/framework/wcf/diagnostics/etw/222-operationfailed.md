---
title: 222 - OperationFailed
ms.date: 03/30/2017
ms.assetid: 6b530ded-8f20-4d78-8bfe-1875276df6ba
ms.openlocfilehash: c49aad0f93ce47b66306d75741267530dc6d3fe5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781639"
---
# <a name="222---operationfailed"></a>222 - OperationFailed
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|222|  
|Mots clés|EndToEndMonitoring, HealthMonitoring, Dépannage, ServiceModel|  
|Niveau|Warning|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis lorsque l'`OperationInvoker` par défaut du modèle de service a rencontré une exception lors de l'appel de sa méthode. Notez que les exceptions dérivant de `FaultException` empêchent cet événement d'être émis.  
  
## <a name="message"></a>Message  
 La méthode '%1' a levé une exception non gérée lors de l'appel effectué par l'OperationInvoker. Durée de l'appel de méthode : '%2' ms.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Nom de la méthode|`xs:string`|Nom CLR de la méthode qui a été appelée par l'`OperationInvoker`.|  
|Duration|`xs:long`|Durée, en millisecondes, prise par l'`OperationInvoker` pour appeler la méthode.|  
|HostReference|`xs:string`|Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web. Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'. Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».|  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
