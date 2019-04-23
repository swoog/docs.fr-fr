---
title: Services demande-réponse
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Communication Foundation [WCF], request-reply services
- contracts [WCF], request-reply services
- WCF [WCF], request-reply services
- request-reply contracts [WCF]
ms.assetid: 2fa710f1-47f4-4598-b063-3ab3bd22ebba
ms.openlocfilehash: 1ff11b1cae4ec8f6fe886a55cb0add27831048d0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59177812"
---
# <a name="request-reply-services"></a>Services demande-réponse
Services demande-réponse sont le type de valeur par défaut de contrat d’opération dans Windows Communication Foundation (WCF). Les clients effectuent des appels aux opérations de service et attendent une réponse du service. Vous pouvez effectuer des appels à une opération de service de façon synchrone (le client se bloque jusqu'à ce qu'il reçoive une réponse du service ou que l'appel expire) ou de façon asynchrone (le client effectue un appel à l'opération de service, continue à fonctionner et reçoit la réponse du service sur un autre thread).  
  
 Pour créer un contrat de service demande-réponse, définissez votre contrat de service et appliquez la classe <xref:System.ServiceModel.OperationContractAttribute> à chaque opération, tel qu'indiqué dans l'exemple de code suivant.  
  
```  
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public interface IRequestReplyCalculator  
{  
    [OperationContract]  
    double Add(double n1, double n2);  
}  
```  
  
 Il n'est pas nécessaire d'affecter <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> à la propriété `false`car il s'agit du comportement par défaut.  
  
## <a name="see-also"></a>Voir aussi

- [Services unidirectionnels](../../../../docs/framework/wcf/feature-details/one-way-services.md)
- [Services duplex](../../../../docs/framework/wcf/feature-details/duplex-services.md)
