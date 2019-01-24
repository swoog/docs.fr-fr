---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: 98e8a720e92547ca0a893dd988b91cb7907660b5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689849"
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
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de messages en cours de traitement actif sur tous les objets de répartiteur dans un ServiceHost.  
  
### <a name="maxconcurrentinstances"></a>MaxConcurrentInstances  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal d'objets de service simultanément exécutables.  
  
### <a name="maxconcurrentsessions"></a>MaxConcurrentSessions  
 Type de données : sint32  
  
 Type d’accès : Propriétés en lecture seule  
  
 Nombre maximal de sessions qu'un hôte peut accepter à la fois.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
