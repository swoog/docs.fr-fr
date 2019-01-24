---
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: 76e28b18cd595a4a18f573dfe9539b646196c944
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720338"
---
# <a name="servicemetadatabehavior"></a>ServiceMetadataBehavior
ServiceMetadataBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
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
  
## <a name="properties"></a>Properties  
 La classe ServiceMetadataBehavior a les propriétés suivantes :  
  
### <a name="externalmetadatalocation"></a>ExternalMetadataLocation  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Définit l'emplacement vers lequel le service redirige les demandes de métadonnées.  
  
### <a name="httpgetenabled"></a>HttpGetEnabled  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.  
  
### <a name="httpgeturl"></a>HttpGetUrl  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.  
  
### <a name="httpsgetenabled"></a>HttpsGetEnabled  
 Type de données : booléen  
  
 Type d’accès : Propriétés en lecture seule  
  
 Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.  
  
### <a name="httpsgeturl"></a>HttpsGetUrl  
 Type de données : chaîne  
  
 Type d’accès : Propriétés en lecture seule  
  
 Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.  
  
## <a name="requirements"></a>Spécifications  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
