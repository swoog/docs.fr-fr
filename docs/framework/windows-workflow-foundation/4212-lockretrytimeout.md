---
title: 4212 - LockRetryTimeout
ms.date: 03/30/2017
ms.assetid: d4ad415a-9871-49fc-85b8-8ee2ea149b1d
ms.openlocfilehash: 9b7a463851d380eba1ef7b28fbc6decd0cfc979c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774216"
---
# <a name="4212---lockretrytimeout"></a>4212 - LockRetryTimeout
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|4212|  
|Mots clés|WFInstanceStore|  
|Niveau|Warning|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Le fournisseur SQL a rencontré une expiration du délai d'attente lors de la tentative d'acquisition du verrou d'instance.  
  
## <a name="message"></a>Message  
 Délai d’expiration essaie d’acquérir le verrou d’instance.  L'opération ne s'est pas terminée dans le délai imparti de %1. Le temps alloué à cette opération peut avoir été une partie d'un délai d'expiration plus long.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Délai|xs:string|Délai entre les tentatives.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
