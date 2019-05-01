---
title: 3507 - ServiceEndpointAdded
ms.date: 03/30/2017
ms.assetid: c068fc0e-07ee-4551-9824-ea7216e1fe37
ms.openlocfilehash: c787a1a5af752a3d08e2049cfa0b600b7739e56c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009836"
---
# <a name="3507---serviceendpointadded"></a>3507 - ServiceEndpointAdded
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|3507|  
|Mots clés|WFServices|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Indique qu'un point de terminaison du service a été ajouté.  
  
## <a name="message"></a>Message  
 Un point de terminaison du service a été ajouté pour l'adresse « %1 », la liaison « %2 » et le contrat « %3 ».  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Adresse|xs:string|Adresse du point de terminaison.|  
|Liaison|xs:string|Liaison du point de terminaison.|  
|Contrat|xs:string|Contrat du point de terminaison.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
