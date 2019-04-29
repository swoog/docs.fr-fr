---
title: 4206 - UnlockInstanceException
ms.date: 03/30/2017
ms.assetid: 5a46dc5f-d517-4135-8905-25a42f01206b
ms.openlocfilehash: 3c981888b491f2797a431c2103ba3f5f0bd17046
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774320"
---
# <a name="4206---unlockinstanceexception"></a>4206 - UnlockInstanceException
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|4206|  
|Mots clés|WFInstanceStore|  
|Niveau|Error|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Indique qu'une exception s'est produite lors de la tentative de déverrouillage d'une instance.  
  
## <a name="message"></a>Message  
 Exception %1 rencontrée lors de la tentative de déverrouillage de l'instance.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|ExceptionMessage|xs:string|Message de l'exception SQL.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
