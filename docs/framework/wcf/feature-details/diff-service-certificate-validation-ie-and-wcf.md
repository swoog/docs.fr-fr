---
title: Différences entre la validation de certificat de service effectuée par Internet Explorer et celle effectuée par WCF
ms.date: 03/30/2017
helpviewer_keywords:
- service certificate validation [WCF]
- certificates [WCF], service certificate validation
ms.assetid: 9dffcab2-70a9-40f0-99fd-d3a0b296028f
ms.openlocfilehash: 0bced548cdc9423d1907de09e8b52ebe078d7c19
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59225913"
---
# <a name="differences-between-service-certificate-validation-done-by-internet-explorer-and-wcf"></a>Différences entre la validation de certificat de service effectuée par Internet Explorer et celle effectuée par WCF
En raison de la différence entre la façon dont Internet Explorer et Windows Communication Foundation (WCF) valident les certificats de service lorsque HTTPS est utilisé, il est possible qu’Internet Explorer ne soit pas en mesure d’accéder à la page d’aide ou Web Services Description Language (WSDL) d’un service même si un client WCF est correctement en mesure d’envoyer des messages aux points de terminaison de service. Il s’agit, car Internet Explorer vérifie si le certificat de service a le `ServerAuthentication` de l’objet (OID) d’identificateurs dans les indicateurs d’utilisation améliorés, alors que WCF n’applique pas une telle contrainte. Si Internet Explorer ne peut pas accéder à la page d’aide ou le WSDL pour le service, utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour accéder aux métadonnées de service.  
  
## <a name="see-also"></a>Voir aussi

- [Différences de validation des certificats entre HTTPS, SSL sur TCP et la sécurité SOAP](../../../../docs/framework/wcf/feature-details/cert-val-diff-https-ssl-over-tcp-and-soap.md)
- [Procédure : récupérer des métadonnées et implémenter un service conforme](../../../../docs/framework/wcf/feature-details/how-to-retrieve-metadata-and-implement-a-compliant-service.md)
