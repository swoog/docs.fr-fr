---
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 3d23a3ee10c47e04ea7bdba202ea5063c0d84fac
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62048229"
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
 Type de données : Service  
  
 Type d’accès : Propriétés en lecture seule  
Qualificateurs : Touche  
  
 Service associé au point de terminaison.  
  
### <a name="ref"></a>ref  
 Type de données : Point de terminaison  
  
 Type d’accès : Propriétés en lecture seule  
Qualificateurs : Touche  
  
 Point de terminaison associé au service.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
