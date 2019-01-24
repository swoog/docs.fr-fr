---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: 809e9d809bce456c831aab83c7ac19a882b2959b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571322"
---
# <a name="deliveryrequirementsattribute"></a>DeliveryRequirementsAttribute
DeliveryRequirementsAttribute  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe DeliveryRequirementsAttribute ne définit pas de méthodes.  
  
## <a name="properties"></a>Properties  
 La classe DeliveryRequirementsAttribute a les propriétés suivantes :  
  
### <a name="queueddeliveryrequirements"></a>QueuedDeliveryRequirements  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie si la liaison pour un service prend en charge des contrats.  
  
### <a name="requireordereddelivery"></a>RequireOrderedDelivery  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Spécifie si la liaison prend en charge les messages ordonnés.  
  
### <a name="targetcontract"></a>TargetContract  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Contrat auquel il s'applique.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.DeliveryRequirementsAttribute>
