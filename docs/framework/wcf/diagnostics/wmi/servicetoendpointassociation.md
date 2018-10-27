---
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 3d23a3ee10c47e04ea7bdba202ea5063c0d84fac
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452707"
---
# <a name="servicetoendpointassociation"></a>ServiceToEndpointAssociation
Mappe un service à un point de terminaison.  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceToEndpointAssociation ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
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
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
