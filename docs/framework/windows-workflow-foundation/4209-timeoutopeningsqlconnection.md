---
title: 4209 - TimeoutOpeningSqlConnection
ms.date: 03/30/2017
ms.assetid: f0e56518-9758-41dc-a760-50d1a10fba6e
ms.openlocfilehash: d61d710959f99dbc8a91441766a690eb7e9a365c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774268"
---
# <a name="4209---timeoutopeningsqlconnection"></a>4209 - TimeoutOpeningSqlConnection
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|4209|  
|Mots clés|WFInstanceStore|  
|Niveau|Error|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'une expiration de délai d'attente s'est produite lors de la tentative d'ouverture d'une connexion SQL.  
  
## <a name="message"></a>Message  
 Expiration du délai d'attente lors de la tentative d'ouverture d'une connexion SQL. L'opération ne s'est pas terminée dans le délai imparti de %1. Le temps alloué à cette opération peut avoir été une partie d'un délai d'expiration plus long.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|Délai|xs:string|Valeur de délai d'attente pour ouvrir la connexion SQL.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
