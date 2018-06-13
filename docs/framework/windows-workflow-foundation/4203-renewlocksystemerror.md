---
title: 4203 - RenewLockSystemError
ms.date: 03/30/2017
ms.assetid: 6ec9ec6f-4ae2-45cf-b99b-02cdb9dc9ec9
ms.openlocfilehash: 984f7ddae8797cba17753a618d0820d21bde5eef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33513927"
---
# <a name="4203---renewlocksystemerror"></a>4203 - RenewLockSystemError
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|4203|  
|Mots clés|WFInstanceStore|  
|Niveau|Erreur|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique que le fournisseur SQL n'a pas pu étendre l'expiration du verrou, car l'expiration du verrou a déjà été passée ou le propriétaire de verrou a été supprimé. Le SqlWorkflowInstanceStore sera annulé.  
  
## <a name="message"></a>Message  
 Échec de l'extension de l'expiration du verrou ; l'expiration du verrou a déjà été passée ou le propriétaire de verrou a été supprimé. Abandon de SqlWorkflowInstanceStore.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
