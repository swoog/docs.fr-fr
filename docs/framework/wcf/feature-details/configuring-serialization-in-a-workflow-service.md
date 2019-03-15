---
title: Configuration de la sérialisation dans un service de workflow
ms.date: 03/30/2017
ms.assetid: aa70b290-a2ee-4c3c-90ea-d0a7665096ae
ms.openlocfilehash: 0e0f03a30aa8e8679cf849aa75948e0bc2314fe5
ms.sourcegitcommit: 69bf8b719d4c289eec7b45336d0b933dd7927841
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57843928"
---
# <a name="configuring-serialization-in-a-workflow-service"></a>Configuration de la sérialisation dans un service de workflow
Services de workflow sont des services Windows Communication Foundation (WCF) et n’ont donc la possibilité d’utiliser soit le <xref:System.Runtime.Serialization.DataContractSerializer> (la valeur par défaut) ou le <xref:System.Xml.Serialization.XmlSerializer>. Lors de l'écriture de services en dehors du workflow, le type de sérialiseur à utiliser est spécifié dans le contrat de service ou d'opération. Lors de la création de services de workflow WCF vous ne spécifiez pas ces contrats dans le code, mais ils sont générés lors de l’exécution par inférence de contrat. Pour plus d’informations sur l’inférence de contrat, consultez [à l’aide de contrats dans le Workflow](../../../../docs/framework/wcf/feature-details/using-contracts-in-workflow.md).  Le sérialiseur est spécifié à l'aide de la propriété <xref:System.ServiceModel.Activities.Receive.SerializerOption%2A>. Celle-ci peut être définie dans le concepteur comme le montre l'illustration suivante.  
  
 ![Définition de la propriété SerializerOption dans la fenêtre Propriétés.](./media/configuring-serialization-in-a-workflow-service/setting-serializer-property.png)  
  
 Le sérialiseur peut également être défini dans le code, comme le montre l'exemple suivant,  
  
```csharp  
Receive approveExpense = new Receive  
            {  
                OperationName = "ApproveExpense",  
                CanCreateInstance = true,  
                ServiceContractName = "FinanceService",  
                SerializerOption = SerializerOption.DataContractSerializer,  
                Content = ReceiveContent.Create(new OutArgument<Expense>(expense))  
            };  
```  
  
  Les types connus peuvent également être spécifiés dans des services de workflow. Pour plus d’informations sur les Types connus, consultez [Data Contract Known Types](data-contract-known-types.md). Les types connus peuvent être spécifiés dans le concepteur ou dans du code. Pour spécifier les types connus dans le concepteur, cliquez sur le bouton de sélection en regard de la propriété KnownTypes dans la **fenêtre Propriétés** pour un <xref:System.ServiceModel.Activities.Receive> activité, comme indiqué dans l’illustration suivante.   
  
 ![Capture d’écran de la boîte de dialogue des propriétés de types connus.](./media/configuring-serialization-in-a-workflow-service/known-types-properties.png)  
  
 Cela affiche l’éditeur de Collections de types qui vous permet de rechercher et spécifier des types connus.  
  
 ![Capture d’écran de l’éditeur de Collections de Type.](./media/configuring-serialization-in-a-workflow-service/type-collection-editor.gif)  
  
 Cliquez sur le **ajouter un nouveau type** lien et utilisez la liste déroulante pour sélectionner ou rechercher un type à ajouter à la collection de types connus. Pour spécifier des types connus dans le code, utilisez la propriété <xref:System.ServiceModel.Activities.Receive.KnownTypes%2A>, comme le montre l'exemple suivant :  
  
```csharp
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
