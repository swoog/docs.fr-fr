---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: d294ba4f14472012b9e311ee53742633b5173f54
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485787"
---
# <a name="deliveryrequirementsattribute"></a>DeliveryRequirementsAttribute
DeliveryRequirementsAttribute  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe DeliveryRequirementsAttribute ne définit pas de méthodes.  
  
## <a name="properties"></a>Propriétés  
 La classe DeliveryRequirementsAttribute a les propriétés suivantes :  
  
### <a name="queueddeliveryrequirements"></a>QueuedDeliveryRequirements  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Spécifie si la liaison pour un service prend en charge des contrats.  
  
### <a name="requireordereddelivery"></a>RequireOrderedDelivery  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Spécifie si la liaison prend en charge les messages ordonnés.  
  
### <a name="targetcontract"></a>TargetContract  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Contrat auquel il s'applique.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.DeliveryRequirementsAttribute>
