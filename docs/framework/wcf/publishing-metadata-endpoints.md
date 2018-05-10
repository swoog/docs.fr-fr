---
title: Publication de points de terminaison de métadonnées
ms.date: 03/30/2017
ms.assetid: 29cd8a60-dfb7-460c-bf5a-c2b31b782671
ms.openlocfilehash: 42e0f82ca2c669bbde444cf6aac9ce8f0266f783
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
---
# <a name="publishing-metadata-endpoints"></a>Publication de points de terminaison de métadonnées
Les services Windows Communication Foundation (WCF) publient les métadonnées en publiant un ou plusieurs points de terminaison de métadonnées. La publication de métadonnées de service permet d'accéder à celles-ci à l'aide de protocoles standardisés, tels que WS-MetadataExchange (MEX) et les requêtes HTTP/GET. Les points de terminaison de métadonnées sont semblables aux autres points de terminaison de service dans le sens où ils ont une adresse, une liaison et un contrat, et qu'ils peuvent être ajoutés à un hôte de service via la configuration ou dans du code. Pour activer la publication de points de terminaison de métadonnées, vous devez ajouter le comportement de service <xref:System.ServiceModel.Description.ServiceMetadataBehavior> au service.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour publier les métadonnées d’un service à l’aide d’un fichier de configuration](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)  
 Montre comment configurer un service WCF pour publier les métadonnées afin que les clients peuvent récupérer les métadonnées à l’aide d’un échange WS-MetadataExchange ou une requête HTTP/GET en utilisant le `?wsdl` chaîne de requête.  
  
 [Guide pratique pour publier les métadonnées d’un service à l’aide de code](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-code.md)  
 Montre comment activer la publication de métadonnées pour un service WCF dans le code afin que les clients peuvent récupérer les métadonnées à l’aide d’un échange WS-MetadataExchange ou une requête HTTP/GET en utilisant le `?wsdl` chaîne de requête.  
  
## <a name="see-also"></a>Voir aussi  
 [Publication de métadonnées](../../../docs/framework/wcf/feature-details/publishing-metadata.md)
