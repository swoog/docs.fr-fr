---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: edc154fcce0058455f1376a2a45807c92f7f2457
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49373693"
---
# <a name="servicethrottlingbehavior"></a>ServiceThrottlingBehavior
ServiceThrottlingBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceThrottlingBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceThrottlingBehavior a les propriétés suivantes :  
  
### <a name="maxconcurrentcalls"></a>MaxConcurrentCalls  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 Nombre maximal de messages en cours de traitement actif sur tous les objets de répartiteur dans un ServiceHost.  
  
### <a name="maxconcurrentinstances"></a>MaxConcurrentInstances  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 Nombre maximal d'objets de service simultanément exécutables.  
  
### <a name="maxconcurrentsessions"></a>MaxConcurrentSessions  
 Type de données : sint32  
  
 Type d'accès : lecture seule  
  
 Nombre maximal de sessions qu'un hôte peut accepter à la fois.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
