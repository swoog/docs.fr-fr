---
title: ServiceDebugBehavior
ms.date: 03/30/2017
ms.assetid: a5ec9061-1e95-43fb-b0d9-dbd0a7bc3c44
ms.openlocfilehash: 68b2350f257bc95d8e17f4b9049d67c7f67becae
ms.sourcegitcommit: b22705f1540b237c566721018f974822d5cd8758
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/19/2018
ms.locfileid: "49452860"
---
# <a name="servicedebugbehavior"></a>ServiceDebugBehavior
ServiceDebugBehavior  
  
## <a name="syntax"></a>Syntaxe  
  
```csharp
class ServiceDebugBehavior : Behavior  
{  
  boolean HttpHelpPageEnabled;  
  string HttpHelpPageUrl;  
  boolean HttpsHelpPageEnabled;  
  string HttpsHelpPageUrl;  
  boolean IncludeExceptionDetailInFaults;  
};  
```  
  
## <a name="methods"></a>Méthodes  
 La classe ServiceDebugBehavior ne définit pas de méthode.  
  
## <a name="properties"></a>Properties  
 La classe ServiceDebugBehavior possède les propriétés suivantes :  
  
### <a name="httphelppageenabled"></a>HttpHelpPageEnabled  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Vérifie si le service publie son WSDL à l'adresse contrôlée par l'attribut `HttpGetUrl`.  
  
### <a name="httphelppageurl"></a>HttpHelpPageUrl  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTP.  
  
### <a name="httpshelppageenabled"></a>HttpsHelpPageEnabled  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Vérifie si le service publie son WSDL sur HTTPS à l'adresse contrôlée par l'attribut `HttpsGetUrl`.  
  
### <a name="httpshelppageurl"></a>HttpsHelpPageUrl  
 Type de données : chaîne  
  
 Type d'accès : lecture seule  
  
 Définit l'emplacement auquel le service WSDL est publié pour récupération à l'aide de HTTPS.  
  
### <a name="includeexceptiondetailinfaults"></a>IncludeExceptionDetailInFaults  
 Type de données : booléen  
  
 Type d'accès : lecture seule  
  
 Spécifie s'il convient d'inclure des informations d'exception gérées dans les détails des fautes SOAP renvoyées aux clients à des fins de débogage.  
  
## <a name="requirements"></a>Configuration requise  
  
|MOF|Déclaré dans Servicemodel.mof.|  
|---------|-----------------------------------|  
|Espace de noms|Défini dans root\ServiceModel|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.ServiceModel.Description.ServiceDebugBehavior>
