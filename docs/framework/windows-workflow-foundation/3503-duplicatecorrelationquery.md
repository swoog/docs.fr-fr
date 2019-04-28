---
title: 3503 - DuplicateCorrelationQuery
ms.date: 03/30/2017
ms.assetid: b857f8e6-ce4d-4da4-bc9d-6cd63fa558a4
ms.openlocfilehash: 37a689b30b0bcab9124472deb98627afbe30dfee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755595"
---
# <a name="3503---duplicatecorrelationquery"></a>3503 - DuplicateCorrelationQuery
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|3503|  
|Mots clés|WFServices|  
|Niveau|Warning|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Indique qu'un CorrelationQuery en double a été trouvé. Cette requête en double ne sera pas utilisée lors du calcul de la corrélation.  
  
## <a name="message"></a>Message  
 CorrelationQuery en double trouvé avec Where='%1'. Cette requête en double ne sera pas utilisée lors du calcul de la corrélation.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Où|xs:string|Partie Where de la requête de corrélation.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
