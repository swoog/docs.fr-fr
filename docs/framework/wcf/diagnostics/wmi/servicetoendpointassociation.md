---
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: b1e5b87b053e947432cba9f6e716f7d1ea8f013f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="servicetoendpointassociation"></a>ServiceToEndpointAssociation
Mappe un service à un point de terminaison.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceToEndpointAssociation ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe ServiceToEndpointAssociation a les propriétés suivantes :  
  
### <a name="ref"></a>ref  
 Type de données : service  
  
 Type d'accès : lecture seule  
Qualificateurs : clé  
  
 Service associé au point de terminaison.  
  
### <a name="ref"></a>ref  
 Type de données : point de terminaison  
  
 Type d'accès : lecture seule  
Qualificateurs : clé  
  
 Point de terminaison associé au service.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
