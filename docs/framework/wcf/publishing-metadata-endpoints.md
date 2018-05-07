---
title: Publication de points de terminaison de métadonnées
ms.date: 03/30/2017
ms.assetid: 29cd8a60-dfb7-460c-bf5a-c2b31b782671
ms.openlocfilehash: 6060850b78c890e043dfaf6f242460bc6e0ef627
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="publishing-metadata-endpoints"></a>Publication de points de terminaison de métadonnées
Les services Windows Communication Foundation (WCF) publient les métadonnées en publiant un ou plusieurs points de terminaison de métadonnées. La publication de métadonnées de service permet d'accéder à celles-ci à l'aide de protocoles standardisés, tels que WS-MetadataExchange (MEX) et les requêtes HTTP/GET. Les points de terminaison de métadonnées sont semblables aux autres points de terminaison de service dans le sens où ils ont une adresse, une liaison et un contrat, et qu'ils peuvent être ajoutés à un hôte de service via la configuration ou dans du code. Pour activer la publication de points de terminaison de métadonnées, vous devez ajouter le comportement de service <xref:System.ServiceModel.Description.ServiceMetadataBehavior> au service.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour publier les métadonnées d’un service à l’aide d’un fichier de configuration](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)  
 Indique comment configurer un service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] afin de publier les métadonnées et permettre ainsi aux clients de les récupérer à l'aide d'un échange WS-MetadataExchange ou d'une requête HTTP/GET en utilisant la chaîne de requête `?wsdl`.  
  
 [Guide pratique pour publier les métadonnées d’un service à l’aide de code](../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-code.md)  
 Indique comment activer la publication de métadonnées pour un service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] dans le code afin que les clients puissent les récupérer à l'aide d'un échange WS-MetadataExchange ou d'une requête HTTP/GET en utilisant la chaîne de requête `?wsdl`.  
  
## <a name="see-also"></a>Voir aussi  
 [Publication de métadonnées](../../../docs/framework/wcf/feature-details/publishing-metadata.md)
