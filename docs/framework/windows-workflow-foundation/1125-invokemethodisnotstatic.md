---
title: 1125 - InvokeMethodIsNotStatic
ms.date: 03/30/2017
ms.assetid: ea2b3827-63da-497b-b2c3-d5cebefe57a1
ms.openlocfilehash: 692c5e56dac0a69ab5705acd284f048391145641
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33511941"
---
# <a name="1125---invokemethodisnotstatic"></a>1125 - InvokeMethodIsNotStatic
## <a name="properties"></a>Propriétés  
  
|||  
|-|-|  
|ID|1125|  
|Mots clés|WFRuntime|  
|Niveau|Information|  
|Canal|Microsoft-Windows-Application Server-Applications/Débogage|  
  
## <a name="description"></a>Description  
 Pendant l'étape CacheMetadata, l'activité InvokeMethod indique que la méthode à appeler n'est pas statique.  
  
## <a name="message"></a>Message  
 InvokeMethod « %1 » - la méthode n'est pas statique.  
  
## <a name="details"></a>Détails  
  
|Nom d'élément de données|Type d'élément de données|Description|  
|--------------------|--------------------|-----------------|  
|InvokeMethod|xs:string|Nom complet de l'activité InvokeMethod.|  
|AppDomain|xs:string|Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.|
