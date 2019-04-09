---
title: Utilisation de contrats dans le workflow
ms.date: 03/30/2017
ms.assetid: 939c64e9-e7cc-4abc-b41e-27cfce1d7e50
ms.openlocfilehash: dd35766011c412acc937eed75d523a0574f6b9cb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150057"
---
# <a name="using-contracts-in-workflow"></a><span data-ttu-id="9c071-102">Utilisation de contrats dans le workflow</span><span class="sxs-lookup"><span data-stu-id="9c071-102">Using Contracts in Workflow</span></span>
<span data-ttu-id="9c071-103">Lorsque vous implémentez un service, vous définissez plusieurs contrats qui décrivent le service et les données qu'il envoie et reçoit.</span><span class="sxs-lookup"><span data-stu-id="9c071-103">When implementing a service, you define a number of contracts that describe the service and the data that it sends and receives.</span></span> <span data-ttu-id="9c071-104">Les données sont représentées en tant que contrats de données et les contrats de message ; services WCF et de flux de travail utilisent des définitions de contrat de message et de contrat de données dans le cadre des descriptions de service.</span><span class="sxs-lookup"><span data-stu-id="9c071-104">The data is represented as data contracts and message contracts; both WCF and workflow services use data contract and message contract definitions as part of service descriptions.</span></span> <span data-ttu-id="9c071-105">Le service lui-même expose des métadonnées (au format WSDL) pour décrire les opérations du service.</span><span class="sxs-lookup"><span data-stu-id="9c071-105">The service itself exposes metadata (in the form of WSDL) in order to describe the operations of the service.</span></span> <span data-ttu-id="9c071-106">Dans WCF, les contrats de service et les contrats d'opération définissent le service et les opérations qu'il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="9c071-106">In WCF, service contracts and operation contracts define the service and the operations it supports.</span></span> <span data-ttu-id="9c071-107">Toutefois, dans un service de workflow, ces contrats font partie du processus d'entreprise lui-même ; ils sont exposés dans les métadonnées par un processus nommé inférence de contrat.</span><span class="sxs-lookup"><span data-stu-id="9c071-107">However, in a workflow service, these contracts are part of the business process itself; they are exposed in metadata by a process called contract inference.</span></span>  
  
## <a name="contract-inference"></a><span data-ttu-id="9c071-108">Inférence de contrat</span><span class="sxs-lookup"><span data-stu-id="9c071-108">Contract Inference</span></span>  
 <span data-ttu-id="9c071-109">Lorsqu'un service de workflow est hébergé à l'aide d'un objet <xref:System.ServiceModel.Activities.WorkflowServiceHost>, la définition du workflow est examinée et un contrat est généré en fonction du jeu d'activités de messagerie qui se trouvent dans le workflow.</span><span class="sxs-lookup"><span data-stu-id="9c071-109">When a workflow service is hosted using <xref:System.ServiceModel.Activities.WorkflowServiceHost>, the workflow definition is examined and a contract is generated based on the set of messaging activities found in the workflow.</span></span> <span data-ttu-id="9c071-110">En particulier, les activités et les propriétés suivantes sont utilisées pour générer le contrat :</span><span class="sxs-lookup"><span data-stu-id="9c071-110">In particular the following activities and properties are used to generate the contract:</span></span>  
  
 <xref:System.ServiceModel.Activities.Receive> <span data-ttu-id="9c071-111">Activité</span><span class="sxs-lookup"><span data-stu-id="9c071-111">Activity</span></span>  
  
-   <xref:System.ServiceModel.Activities.Receive.ServiceContractName%2A>  
  
-   <xref:System.ServiceModel.Activities.Receive.OperationName%2A>
  
-   <xref:System.ServiceModel.Activities.Receive.Action%2A>   
 
 <xref:System.ServiceModel.Activities.SendReply> <span data-ttu-id="9c071-112">Activité</span><span class="sxs-lookup"><span data-stu-id="9c071-112">Activity</span></span>  
  
-   <xref:System.ServiceModel.Activities.SendReply.Action%2A>  
  
 <xref:System.ServiceModel.Activities.TransactedReceiveScope> <span data-ttu-id="9c071-113">Activité</span><span class="sxs-lookup"><span data-stu-id="9c071-113">Activity</span></span>  
  
 <span data-ttu-id="9c071-114">Le résultat final de l'inférence de contrat est une description du service utilisant les mêmes structures de données que le service WCF et les contrats d'opération.</span><span class="sxs-lookup"><span data-stu-id="9c071-114">The end result of contract inference is a description of the service using the same data structures as WCF service and operation contracts.</span></span> <span data-ttu-id="9c071-115">Puis ces informations sont utilisées pour exposer WSDL pour le service de workflow.</span><span class="sxs-lookup"><span data-stu-id="9c071-115">This information is then used to expose WSDL for the workflow service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c071-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c071-116">See also</span></span>

- [<span data-ttu-id="9c071-117">Services de workflow</span><span class="sxs-lookup"><span data-stu-id="9c071-117">Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/workflow-services.md)
- [<span data-ttu-id="9c071-118">Activités de messagerie</span><span class="sxs-lookup"><span data-stu-id="9c071-118">Messaging Activities</span></span>](../../../../docs/framework/wcf/feature-details/messaging-activities.md)
- [<span data-ttu-id="9c071-119">Procédure : créer un service de workflow avec des activités de messagerie</span><span class="sxs-lookup"><span data-stu-id="9c071-119">How to: Create a Workflow Service with Messaging Activities</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-workflow-service-with-messaging-activities.md)
- [<span data-ttu-id="9c071-120">Procédure : créer un service de workflow qui consomme un contrat de service existant</span><span class="sxs-lookup"><span data-stu-id="9c071-120">How to: Create a workflow service that consumes an existing service contract</span></span>](../../../../docs/framework/windows-workflow-foundation/how-to-create-a-workflow-service-that-consumes-an-existing-service-contract.md)
