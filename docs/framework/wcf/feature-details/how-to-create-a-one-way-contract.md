---
title: 'Procédure : Créer un contrat unidirectionnel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 85084cd9-31cc-4e95-b667-42ef01336622
ms.openlocfilehash: f7636d7013c236e0c51e5326a84ae47f2f98e283
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693621"
---
# <a name="how-to-create-a-one-way-contract"></a>Procédure : Créer un contrat unidirectionnel
Cette rubrique décrit les étapes de base pour créer des méthodes qui utilisent un contrat unidirectionnel. Ces méthodes appeler des opérations sur un service Windows Communication Foundation (WCF) à partir d’un client, mais n’attendent pas une réponse. Ce type de contrat peut être utilisé, par exemple, pour publier des notifications destinées à de nombreux abonnés. Vous pouvez également utiliser des contrats unidirectionnels lors de la création d'un contrat duplex (bidirectionnel), qui autorise des clients et des serveurs à communiquer l'un l'autre indépendamment, afin qu'ils puissent initialiser des appels. Notamment, cela peut permettre au serveur d'effectuer des appels unidirectionnels au client, que le client peut traiter en tant qu'événements. Pour plus d'informations à propos de la spécification de méthodes unidirectionnelles, consultez la propriété <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> et la classe <xref:System.ServiceModel.OperationContractAttribute>.  
  
 Pour plus d’informations sur la création d’une application cliente pour un contrat duplex, consultez [Comment : Accéder aux Services avec unidirectionnel et contrats demande-réponse](../../../../docs/framework/wcf/feature-details/how-to-access-wcf-services-with-one-way-and-request-reply-contracts.md). Pour obtenir un exemple fonctionnel, consultez le [unidirectionnel](../../../../docs/framework/wcf/samples/one-way.md) exemple.  
  
### <a name="to-create-a-one-way-contract"></a>Pour créer un contrat unidirectionnel  
  
1.  Créez le contrat de service en appliquant la classe <xref:System.ServiceModel.ServiceContractAttribute> à l'interface qui définit les méthodes que le service doit implémenter.  
  
2.  Indiquez les méthodes qu'un client peut appeler dans l'interface en appliquant la classe <xref:System.ServiceModel.OperationContractAttribute>.  
  
3.  Désignez des opérations qui ne doivent avoir aucune sortie (aucune valeur de retour et aucun paramètre ref ou de sortie) en tant qu'unidirectionnelles en affectant à la propriété <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> la valeur `true`. Notez que les opérations qui retiennent la classe <xref:System.ServiceModel.OperationContractAttribute> satisfont un contrat de demande-réponse par défaut parce que la propriété <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> est par défaut `false`. Vous devez donc spécifier explicitement la valeur `true` pour la propriété d'attribut si vous souhaitez un contrat unidirectionnel pour la méthode.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant définit un contrat pour un service qui inclut plusieurs méthodes unidirectionnelles. Toutes les méthodes ont des contrats unidirectionnels sauf `Equals`, qui a comme valeur par défaut la demande-réponse et retourne un résultat.  
  
 [!code-csharp[S_Service_Session#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_service_session/cs/service.cs#1)]
 [!code-vb[S_Service_Session#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_service_session/vb/service.vb#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ServiceModel.ServiceContractAttribute>
- <xref:System.ServiceModel.OperationContractAttribute>
- [Conception et implémentation de services](../../../../docs/framework/wcf/designing-and-implementing-services.md)
- [Guide pratique pour Définir un contrat de Service](../../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md)
- [Session](../../../../docs/framework/wcf/samples/session.md)
- [Guide pratique pour Créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
