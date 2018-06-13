---
title: Configuration de la sérialisation dans un service de workflow
ms.date: 03/30/2017
ms.assetid: aa70b290-a2ee-4c3c-90ea-d0a7665096ae
ms.openlocfilehash: 74d9a812b9e0cd51a401fa3526c947d52413807a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33488870"
---
# <a name="configuring-serialization-in-a-workflow-service"></a><span data-ttu-id="34937-102">Configuration de la sérialisation dans un service de workflow</span><span class="sxs-lookup"><span data-stu-id="34937-102">Configuring Serialization in a Workflow Service</span></span>
<span data-ttu-id="34937-103">Services de workflow sont des services Windows Communication Foundation (WCF) et avoir la possibilité d’utiliser soit le <xref:System.Runtime.Serialization.DataContractSerializer> (la valeur par défaut) ou le <xref:System.Xml.Serialization.XmlSerializer>.</span><span class="sxs-lookup"><span data-stu-id="34937-103">Workflow services are Windows Communication Foundation (WCF) services and so have the option of using either the <xref:System.Runtime.Serialization.DataContractSerializer> (the default) or the <xref:System.Xml.Serialization.XmlSerializer>.</span></span> <span data-ttu-id="34937-104">Lors de l'écriture de services en dehors du workflow, le type de sérialiseur à utiliser est spécifié dans le contrat de service ou d'opération.</span><span class="sxs-lookup"><span data-stu-id="34937-104">When writing non-workflow services the type of serializer to use is specified on the service or operation contract.</span></span> <span data-ttu-id="34937-105">Lors de la création de services de workflow WCF vous ne spécifiez pas ces contrats dans le code, mais ils sont générés lors de l’exécution par inférence de contrat.</span><span class="sxs-lookup"><span data-stu-id="34937-105">When creating WCF workflow services you don’t specify these contracts in code, but rather they are generated at runtime by contract inference.</span></span> <span data-ttu-id="34937-106">Pour plus d’informations sur l’inférence de contrat, consultez [à l’aide de contrats dans le Workflow](../../../../docs/framework/wcf/feature-details/using-contracts-in-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="34937-106">For more information about contract inference, see  [Using Contracts in Workflow](../../../../docs/framework/wcf/feature-details/using-contracts-in-workflow.md).</span></span>  <span data-ttu-id="34937-107">Le sérialiseur est spécifié à l'aide de la propriété <xref:System.ServiceModel.Activities.Receive.SerializerOption%2A>.</span><span class="sxs-lookup"><span data-stu-id="34937-107">The serializer is specified using the <xref:System.ServiceModel.Activities.Receive.SerializerOption%2A> property.</span></span> <span data-ttu-id="34937-108">Celle-ci peut être définie dans le concepteur comme le montre l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="34937-108">This can be set in the designer as shown in the following illustration.</span></span>  
  
 <span data-ttu-id="34937-109">![Définition du sérialiseur](../../../../docs/framework/wcf/feature-details/media/settingserialzier.png "SettingSerialzier")</span><span class="sxs-lookup"><span data-stu-id="34937-109">![Setting the serializer](../../../../docs/framework/wcf/feature-details/media/settingserialzier.png "SettingSerialzier")</span></span>  
  
 <span data-ttu-id="34937-110">Le sérialiseur peut également être défini dans le code, comme le montre l'exemple suivant,</span><span class="sxs-lookup"><span data-stu-id="34937-110">The serializer can also be set in code as shown in the following example,</span></span>  
  
```  
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
```  
  
 <span data-ttu-id="34937-111">Les types connus peuvent également être spécifiés dans des services de workflow.</span><span class="sxs-lookup"><span data-stu-id="34937-111">Known types can be specified on Workflow services as well.</span></span> <span data-ttu-id="34937-112">Pour plus d’informations sur les Types connus, consultez [Types connus de contrat de données](../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span><span class="sxs-lookup"><span data-stu-id="34937-112">For more information about Known Types see [Data Contract Known Types](../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).</span></span> <span data-ttu-id="34937-113">Les types connus peuvent être spécifiés dans le concepteur ou dans du code.</span><span class="sxs-lookup"><span data-stu-id="34937-113">Known types can be specified in the designer or in code.</span></span> <span data-ttu-id="34937-114">Pour spécifier les types courants dans le concepteur, cliquez sur le bouton de sélection en regard de la propriété KnownTypes dans la fenêtre Propriétés pour une activité <xref:System.ServiceModel.Activities.Receive>, comme le montre l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="34937-114">To specify known types in the designer, click the ellipsis button next to the KnownTypes property in the properties window for a <xref:System.ServiceModel.Activities.Receive> activity as shown in the following illustration.</span></span>  
  
 <span data-ttu-id="34937-115">![Propriété KnownTypes](../../../../docs/framework/wcf/feature-details/media/knowntypes.png "KnownTypes")</span><span class="sxs-lookup"><span data-stu-id="34937-115">![KnownTypes property](../../../../docs/framework/wcf/feature-details/media/knowntypes.png "KnownTypes")</span></span>  
  
 <span data-ttu-id="34937-116">L’Éditeur de collections de types s’affiche et vous permet de rechercher et de spécifier des types connus.</span><span class="sxs-lookup"><span data-stu-id="34937-116">This will display the Type Collections Editor that will allow you to search for and specify known types.</span></span>  
  
 <span data-ttu-id="34937-117">![Ajout de Types connus](../../../../docs/framework/wcf/feature-details/media/typecollectionseditor.gif "TypeCollectionsEditor")</span><span class="sxs-lookup"><span data-stu-id="34937-117">![Adding Known Types](../../../../docs/framework/wcf/feature-details/media/typecollectionseditor.gif "TypeCollectionsEditor")</span></span>  
  
 <span data-ttu-id="34937-118">Cliquez sur le **ajouter le nouveau type** lien et utilisez la liste déroulante pour sélectionner ou rechercher un type à ajouter à la collection de types connus.</span><span class="sxs-lookup"><span data-stu-id="34937-118">Click the **Add new type** link and use the drop down to select or search for a type to add to the known types collection.</span></span> <span data-ttu-id="34937-119">Pour spécifier des types connus dans le code, utilisez la propriété <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A>, comme le montre l'exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="34937-119">To specify known types in code use the <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A> property as shown in the following example.</span></span>  
  
```  
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
            approveExpense.KnownTypes.Add(typeof(Travel));  
            approveExpense.KnownTypes.Add(typeof(Meal));  
```  
  
 <span data-ttu-id="34937-120">Pour voir un exemple de code complet illustrant comment configurer la sérialisation pour un service de flux de travail voir [mise en forme des messages dans les Services de Workflow](../../../../docs/framework/windows-workflow-foundation/samples/formatting-messages-in-workflow-services.md).</span><span class="sxs-lookup"><span data-stu-id="34937-120">To see a complete code example showing how to configure serialization for a workflow service see [Formatting messages in Workflow Services](../../../../docs/framework/windows-workflow-foundation/samples/formatting-messages-in-workflow-services.md).</span></span>
