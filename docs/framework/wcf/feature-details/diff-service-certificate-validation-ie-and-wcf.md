---
title: Différences entre la validation de certificat de service effectuée par Internet Explorer et celle effectuée par WCF
ms.date: 03/30/2017
helpviewer_keywords:
- service certificate validation [WCF]
- certificates [WCF], service certificate validation
ms.assetid: 9dffcab2-70a9-40f0-99fd-d3a0b296028f
ms.openlocfilehash: 0bced548cdc9423d1907de09e8b52ebe078d7c19
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225913"
---
# <a name="differences-between-service-certificate-validation-done-by-internet-explorer-and-wcf"></a><span data-ttu-id="448e6-102">Différences entre la validation de certificat de service effectuée par Internet Explorer et celle effectuée par WCF</span><span class="sxs-lookup"><span data-stu-id="448e6-102">Differences Between Service Certificate Validation Done by Internet Explorer and WCF</span></span>
<span data-ttu-id="448e6-103">En raison de la différence entre la façon dont Internet Explorer et Windows Communication Foundation (WCF) valident les certificats de service lorsque HTTPS est utilisé, il est possible qu’Internet Explorer ne soit pas en mesure d’accéder à la page d’aide ou Web Services Description Language (WSDL) d’un service même si un client WCF est correctement en mesure d’envoyer des messages aux points de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="448e6-103">Because of difference between the way Internet Explorer and Windows Communication Foundation (WCF) validate service certificates when HTTPS is used, it is possible that Internet Explorer will not be able to access the Help page or Web Services Description Language (WSDL) of a service even though a WCF client is able to successfully send messages to the service endpoints.</span></span> <span data-ttu-id="448e6-104">Il s’agit, car Internet Explorer vérifie si le certificat de service a le `ServerAuthentication` de l’objet (OID) d’identificateurs dans les indicateurs d’utilisation améliorés, alors que WCF n’applique pas une telle contrainte.</span><span class="sxs-lookup"><span data-stu-id="448e6-104">This is because Internet Explorer checks whether the service certificate has the `ServerAuthentication` object identifiers (OID) in the enhanced usage flags, whereas WCF does not enforce such a constraint.</span></span> <span data-ttu-id="448e6-105">Si Internet Explorer ne peut pas accéder à la page d’aide ou le WSDL pour le service, utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour accéder aux métadonnées de service.</span><span class="sxs-lookup"><span data-stu-id="448e6-105">If Internet Explorer is unable to access the service Help page or the WSDL for the service, use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to access the service metadata.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="448e6-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="448e6-106">See also</span></span>

- [<span data-ttu-id="448e6-107">Différences de validation des certificats entre HTTPS, SSL sur TCP et la sécurité SOAP</span><span class="sxs-lookup"><span data-stu-id="448e6-107">Certificate Validation Differences Between HTTPS, SSL over TCP, and SOAP Security</span></span>](../../../../docs/framework/wcf/feature-details/cert-val-diff-https-ssl-over-tcp-and-soap.md)
- [<span data-ttu-id="448e6-108">Guide pratique pour Récupérer les métadonnées et implémenter un Service conforme</span><span class="sxs-lookup"><span data-stu-id="448e6-108">How to: Retrieve Metadata and Implement a Compliant Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-retrieve-metadata-and-implement-a-compliant-service.md)
