---
title: ServiceAppDomain
ms.date: 03/30/2017
ms.assetid: f28e5186-a66d-46c1-abe9-b50e07f8cb4f
ms.openlocfilehash: aef0a0da9d107b92d9d3017968d5554205a6fd71
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485666"
---
# <a name="serviceappdomain"></a>ServiceAppDomain
Mappe un service à un domaine d'application.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class ServiceAppDomain  
{  
  Service ref;  
  AppDomainInfo ref;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceAppDomain ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe ServiceAppDomain a les propriétés suivantes :  
  
### <a name="ref"></a>ref  
 Type de données : service  
Qualificateurs : clé  
  
 Type d'accès : lecture seule  
  
 Service de ce domaine d'application.  
  
### <a name="ref"></a>ref  
 Type de données : AppDomainInfo  
Qualificateurs : clé  
  
 Type d'accès : lecture seule  
  
 Contient des propriétés du domaine d'application.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|
