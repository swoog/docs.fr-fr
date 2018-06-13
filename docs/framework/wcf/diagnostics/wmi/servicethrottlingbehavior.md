---
title: ServiceThrottlingBehavior
ms.date: 03/30/2017
ms.assetid: 37b9e517-1f1f-4ec4-9fcb-2b8016794f5b
ms.openlocfilehash: 9a7fbf93dbdbf1a6debcf865b4883b5784e2ff4a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33487605"
---
# <a name="servicethrottlingbehavior"></a>ServiceThrottlingBehavior
ServiceThrottlingBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class ServiceThrottlingBehavior : Behavior  
{  
  sint32 MaxConcurrentCalls;  
  sint32 MaxConcurrentInstances;  
  sint32 MaxConcurrentSessions;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceThrottlingBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
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
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Description.ServiceThrottlingBehavior>
