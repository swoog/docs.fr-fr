---
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: e96a732f8b3b4d78d597429905cc7dd290dcc606
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485998"
---
# <a name="servicemetadatabehavior"></a>ServiceMetadataBehavior
ServiceMetadataBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```  
class ServiceMetadataBehavior : Behavior  
{  
  string ExternalMetadataLocation;  
  boolean HttpGetEnabled;  
  string HttpGetUrl;  
  boolean HttpsGetEnabled;  
  string HttpsGetUrl;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceMetadataBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Propriétés  
 La classe ServiceMetadataBehavior a les propriétés suivantes :  
  
### <a name="externalmetadatalocation"></a>ExternalMetadataLocation  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Définit l'emplacement vers lequel le service redirige les demandes de métadonnées.  
  
### <a name="httpgetenabled"></a>HttpGetEnabled  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.  
  
### <a name="httpgeturl"></a>HttpGetUrl  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.  
  
### <a name="httpsgetenabled"></a>HttpsGetEnabled  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.  
  
### <a name="httpsgeturl"></a>HttpsGetUrl  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
