---
title: 451 - MessageLogInfo
ms.date: 03/30/2017
ms.assetid: 485b4b29-dc21-4a35-93f8-5f4726d6aa5a
ms.openlocfilehash: e61ef49b947e59f65933f6cbf3ba6b8669aa3bba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757688"
---
# <a name="451---messageloginfo"></a>451 - MessageLogInfo
## <a name="properties"></a>Properties  
  
|||  
|-|-|  
|Id|451|  
|Mots clés|Dépannage, WCFMessageLogging|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis lorsque les informations du journal des messages sont envoyées.  
  
## <a name="message"></a>Message  
 %1  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|data1|`xs:string`||  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
