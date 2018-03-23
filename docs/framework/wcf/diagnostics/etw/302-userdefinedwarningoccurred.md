---
title: 302 - UserDefinedWarningOccurred
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d1f0bf1-0151-45e6-be92-573d397b54de
caps.latest.revision: ''
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: ae455c9eec2335fcf6eb5473932bd8d9e5d2db95
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2018
---
# <a name="302---userdefinedwarningoccurred"></a>302 - UserDefinedWarningOccurred
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|Id|302|  
|Mots clés|Dépannage, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring|  
|Niveau|Avertissement|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis à partir du code utilisateur. Les développeurs peuvent émettre cet événement lorsqu'un événement d'avertissement personnalisé se produit dans leur service. Cela peut s'effectuer à l'aide des API <xref:System.Diagnostics.Eventing>. En outre, il existe un exemple WCF qui encapsule cette API et montre comment émettre correctement cet événement.  
  
## <a name="message"></a>Message  
 Nom : '%1', Référence : '%2', Charge : %3  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Name|`xs:string`|Nom de l'événement défini par l'utilisateur.|  
|HostReference|`xs:string`|Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web. Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'. Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».|  
|Charge utile|`xs:string`|Charge utile de l'événement définie par l'utilisateur.|
