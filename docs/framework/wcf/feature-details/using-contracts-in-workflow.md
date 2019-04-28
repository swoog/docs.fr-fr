---
title: Utilisation de contrats dans le workflow
ms.date: 03/30/2017
ms.assetid: 939c64e9-e7cc-4abc-b41e-27cfce1d7e50
ms.openlocfilehash: dd35766011c412acc937eed75d523a0574f6b9cb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61918539"
---
# <a name="using-contracts-in-workflow"></a>Utilisation de contrats dans le workflow
Lorsque vous implémentez un service, vous définissez plusieurs contrats qui décrivent le service et les données qu'il envoie et reçoit. Les données sont représentées en tant que contrats de données et les contrats de message ; services WCF et de flux de travail utilisent des définitions de contrat de message et de contrat de données dans le cadre des descriptions de service. Le service lui-même expose des métadonnées (au format WSDL) pour décrire les opérations du service. Dans WCF, les contrats de service et les contrats d'opération définissent le service et les opérations qu'il prend en charge. Toutefois, dans un service de workflow, ces contrats font partie du processus d'entreprise lui-même ; ils sont exposés dans les métadonnées par un processus nommé inférence de contrat.  
  
## <a name="contract-inference"></a>Inférence de contrat  
 Lorsqu'un service de workflow est hébergé à l'aide d'un objet <xref:System.ServiceModel.Activities.WorkflowServiceHost>, la définition du workflow est examinée et un contrat est généré en fonction du jeu d'activités de messagerie qui se trouvent dans le workflow. En particulier, les activités et les propriétés suivantes sont utilisées pour générer le contrat :  
  
 Activité <xref:System.ServiceModel.Activities.Receive>  
  
- <xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A>  
  
- <xref:System.ServiceModel.Activities.Receive.OperationName%2A>
  
- <xref:System.ServiceModel.Activities.Receive.Action%2A>   
 
 Activité <xref:System.ServiceModel.Activities.SendReply>  
  
- <xref:System.ServiceModel.Activities.SendReply.Action%2A>  
  
 Activité <xref:System.ServiceModel.Activities.TransactedReceiveScope>  
  
 Le résultat final de l'inférence de contrat est une description du service utilisant les mêmes structures de données que le service WCF et les contrats d'opération. Puis ces informations sont utilisées pour exposer WSDL pour le service de workflow.  
  
## <a name="see-also"></a>Voir aussi

- [Services de workflow](../../../../docs/framework/wcf/feature-details/workflow-services.md)
- [Activités de messagerie](../../../../docs/framework/wcf/feature-details/messaging-activities.md)
- [Guide pratique pour Créer un Service de flux de travail avec les activités de messagerie](../../../../docs/framework/wcf/feature-details/how-to-create-a-workflow-service-with-messaging-activities.md)
- [Guide pratique pour Créer un service de flux de travail qui utilise un contrat de service existant](../../../../docs/framework/windows-workflow-foundation/how-to-create-a-workflow-service-that-consumes-an-existing-service-contract.md)
