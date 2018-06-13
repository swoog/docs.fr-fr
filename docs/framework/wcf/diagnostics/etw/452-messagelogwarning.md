---
title: 452 - MessageLogWarning
ms.date: 03/30/2017
ms.assetid: 22a9f6ea-5b5f-4110-8a4e-9be9c983fbbb
ms.openlocfilehash: 22932c4de7a803307f2ee82adc958a30cf96f198
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33465895"
---
# <a name="452---messagelogwarning"></a>452 - MessageLogWarning
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|Id|452|  
|Mots clés|Dépannage, WCFMessageLogging|  
|Niveau|Avertissement|  
|Canal|Microsoft-Windows-Application Server-Applications/Analyse|  
  
## <a name="description"></a>Description  
 Cet événement est émis lorsque l'avertissement du journal des messages est envoyé.  
  
## <a name="message"></a>Message  
 %1  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|data1|`xs:string`||  
|AppDomain|`xs:string`|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
