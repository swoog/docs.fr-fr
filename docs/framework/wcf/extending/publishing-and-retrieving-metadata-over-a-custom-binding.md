---
title: Publication et récupération de métadonnées sur une liaison personnalisée
ms.date: 03/30/2017
ms.assetid: 904e11b4-d90e-45c6-9ee5-c3472c90008c
ms.openlocfilehash: 528f7662ee3a1f956427e5e42f540816f55027f8
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33803882"
---
# <a name="publishing-and-retrieving-metadata-over-a-custom-binding"></a>Publication et récupération de métadonnées sur une liaison personnalisée
Le <xref:System.ServiceModel.Description.ServiceMetadataBehavior?displayProperty=nameWithType> fournit la prise en charge de l'ajout de points de terminaison de métadonnées à un service. Ces points de terminaison de métadonnées peuvent répondre aux demandes HTTP GET à l’URL qui a un `?wsdl` querystring et aux demandes WS-Transfer GET tel que défini dans la spécification WS-MetadataExchange (MEX). Les points de terminaison MEX implémentent le contrat <xref:System.ServiceModel.Description.IMetadataExchange?displayProperty=nameWithType>.  
  
## <a name="publishing-metadata-over-a-custom-binding"></a>Publication de métadonnées sur une liaison personnalisée  
 Les points de terminaison de métadonnées GET HTTP et les points de terminaison de métadonnées GET HTTPS sont activés en affectant à la propriété <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpGetEnabled%2A?displayProperty=nameWithType> ou <xref:System.ServiceModel.Description.ServiceMetadataBehavior.HttpsGetEnabled%2A?displayProperty=nameWithType> la valeur `true`. Les liaisons pour ces points de terminaison ne peuvent pas être configurées.  
  
 Le <xref:System.ServiceModel.Description.IMetadataExchange> contrat, toutefois, peut être utilisé avec n’importe quel point de terminaison, y compris ceux qui utilisent des liaisons personnalisées, car <xref:System.ServiceModel.Description.IMetadataExchange> points de terminaison sont identiques à n’importe quel autre terminaison de service Windows Communication Foundation (WCF). Si vous savez comment modifier la configuration d'une liaison fournie par le système ou comment configurer un <xref:System.ServiceModel.Channels.CustomBinding?displayProperty=nameWithType>, vous pouvez configurer une liaison pour une utilisation avec un point de terminaison <xref:System.ServiceModel.Description.IMetadataExchange>.  
  
## <a name="retrieving-metadata-over-a-custom-binding"></a>Récupération de métadonnées sur une liaison personnalisée  
 Les métadonnées peuvent être récupérées à partir de points de terminaison de métadonnées Get HTTP et Get HTTPS à l'aide de demandes GET HTTP ou HTTPS standard.  
  
 Pour récupérer des métadonnées à partir d’un point de terminaison de métadonnées MEX que vous pouvez généralement utiliser l’une des liaisons MEX standard prises en charge par WCF. Pour plus d'informations, consultez <xref:System.ServiceModel.Description.MetadataExchangeBindings?displayProperty=nameWithType>. Le type <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> et l'outil Svcutil.exe sélectionnent automatiquement l'une de ces liaisons MEX standard en fonction de l'adresse du point de terminaison de métadonnées spécifié.  
  
 Si un point de terminaison de métadonnées MEX utilise une liaison différente de l'une des liaisons MEX standard, vous pouvez configurer la liaison utilisée par le <xref:System.ServiceModel.Description.MetadataExchangeClient> à l'aide de code ou en fournissant une configuration de point de terminaison de client <xref:System.ServiceModel.Description.IMetadataExchange>. L'outil Svcutil.exe charge automatiquement à partir de son fichier de configuration une configuration de point de terminaison de client <xref:System.ServiceModel.Description.IMetadataExchange> qui a le même nom que le modèle d'URI pour l'adresse du point de terminaison de métadonnées.  
  
## <a name="security"></a>Sécurité  
 Lors de la publication de métadonnées sur une liaison personnalisée, assurez-vous que la liaison fournit la prise en charge de sécurité requise par vos métadonnées. Par exemple, pour empêcher la divulgation d'informations et vous assurer que votre client a le droit d'obtenir les métadonnées, vous pouvez rendre vos métadonnées et votre application plus sécurisées en configurant votre point de terminaison <xref:System.ServiceModel.Description.IMetadataExchange> de façon à exiger l'authentification et le chiffrement. L’exemple [personnalisé sécuriser les métadonnées de point de terminaison](../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md) illustre ce scénario.  
  
## <a name="see-also"></a>Voir aussi  
 [Sécurisation de services](../../../../docs/framework/wcf/securing-services.md)  
 [Liaisons WS-MetadataExchange](../../../../docs/framework/wcf/extending/ws-metadataexchange-bindings.md)  
 [Guide pratique pour configurer une liaison WS-Metadata Exchange personnalisée](../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md)  
 [Guide pratique pour récupérer des métadonnées sur une liaison non-MEX](../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)
