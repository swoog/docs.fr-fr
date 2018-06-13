---
title: 216 - MessageSentByTransport
ms.date: 03/30/2017
ms.assetid: 150c3167-4154-4225-8d94-57cc94341233
ms.openlocfilehash: fa21568e4c8c38eefe359c417d47ec0a9d30a7c4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33458681"
---
# <a name="216---messagesentbytransport"></a>216 - MessageSentByTransport
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|Id|216|  
|Mots clés|Dépannage, ServiceModel|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement se produit lorsqu'un transport basé sur TCP envoie un message. Notez qu'au niveau du transport, plusieurs messages peuvent être échangés entre clients et services pour une seule opération. Cela peut être dû au comportement d'infrastructure, la sécurité étant un bon exemple. Par conséquent, le nombre de **MessageSentByTransport** les événements qui sont émis varient en fonction de la liaison de votre service et de sa configuration.  
  
## <a name="message"></a>Message  
 Le transport a envoyé un message à '%1.'  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|DestinationAddress|`xs:string`|Adresse à laquelle le message de demande a été envoyé.|  
|HostReference|xs:string|Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web. Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'. Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».|  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
