---
title: 'Procédure : configurer la persistance avec WorkflowServiceHost'
ms.date: 03/30/2017
ms.assetid: e31cd4df-13a3-4a9a-9be8-5243e0055356
ms.openlocfilehash: b8839f42a9b8b5f4da0a1a8364c7eac5a4c06d4e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59337160"
---
# <a name="how-to-configure-persistence-with-workflowservicehost"></a>Procédure : configurer la persistance avec WorkflowServiceHost
Cette rubrique décrit comment configurer la fonctionnalité de magasin d'instances de workflow SQL pour activer la persistance des workflows hébergés dans <xref:System.ServiceModel.Activities.WorkflowServiceHost> à l'aide d'un fichier de configuration. Avant d’utiliser la fonctionnalité de magasin d’instances de workflow SQL, vous devez créer une base de données SQL utilisée pour rendre des instances de workflow persistantes. Pour plus d'informations, voir [Procédure : Activer la persistance SQL pour les Workflows et les Services de Workflow](../../../../docs/framework/windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md).  
  
### <a name="to-configure-the-sql-workflow-instance-store-in-configuration"></a>Pour configurer le magasin d'instances de workflow SQL en mode Configuration  
  
1. Les propriétés du magasin d'instances de workflow de SQL peuvent être configurées via le <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior>, un comportement de service qui vous permet de modifier les paramètres par configuration XML. L’exemple de configuration suivant montre comment configurer le magasin d’instances de workflow SQL à l’aide de la <`sqlWorkflowInstanceStore`> élément de comportement dans un fichier de configuration.  
  
    ```xml  
    <serviceBehaviors>  
        <behavior name="">  
            <sqlWorkflowInstanceStore   
                 connectionString="provider=System.Data.SqlClient;Data Source=(local);Initial Catalog=DefaultPersistenceProviderDb;Integrated Security=True;Async=true"  
                 instanceEncodingOption="GZip | None"  
                 instanceCompletionAction="DeleteAll | DeleteNothing"  
                 instanceLockedExceptionAction="NoRetry | SimpleRetry | AggressiveRetry"  
                 hostLockRenewalPeriod="00:00:30"   
                 runnableInstancesDetectionPeriod="00:00:05">  
            <sqlWorkflowInstanceStore/>  
        </behavior>  
    </serviceBehaviors>  
    ```  
  
     Pour plus d’informations sur la façon de configurer le magasin d’instances de workflow SQL, consultez [Comment : Activer la persistance SQL pour les Workflows et les Services de Workflow](../../../../docs/framework/windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md). Pour plus d’informations sur les différents paramètres pour le <`sqlWorkflowInstanceStore`> élément de comportement, consultez [SQL Workflow Instance Store](../../../../docs/framework/windows-workflow-foundation/sql-workflow-instance-store.md). Windows Server App Fabric fournit son propre magasin de persistance. Pour plus d’informations, consultez [persistance de Windows Server App Fabric](https://go.microsoft.com/fwlink/?LinkId=193121).  
  
    > [!NOTE]
    >  L'exemple de configuration précédent utilise une configuration simplifiée. Pour plus d’informations, consultez [Configuration simplifiée](../../../../docs/framework/wcf/simplified-configuration.md)  
  
### <a name="to-configure-the-sql-workflow-instance-store-in-code"></a>Pour configurer le magasin d'instances de workflow SQL en code  
  
1. Les propriétés du magasin d'instances de workflow de SQL peuvent être configurées via le <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior>, un comportement de service qui vous permet de modifier les paramètres par code. L'exemple suivant indique comment configurer le magasin d'instances de workflow SQL en utilisant l'élément de comportement <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior> dans un code.  
  
    ```csharp  
    host.Description.Behaviors.Add(new SqlWorkflowInstanceStoreBehavior  
    {  
       ConnectionString = "provider=System.Data.SqlClient;Data Source=(local);Initial Catalog=DefaultPersistenceProviderDb;Integrated Security=True;Async=true",  
       InstanceEncodingOption = "GZip | None",  
       InstanceCompletionAction = "DeleteAll | DeleteNothing",  
       InstanceLockedExceptionAction = "NoRetry | SimpleRetry | AggressiveRetry",  
       HostLockRenewalPeriod = new TimeSpan(00, 00, 30),  
       RunnableInstancesDetectionPeriod = new TimeSpan(00, 00, 05)  
    });  
    ```  
  
     Pour plus d’informations sur la façon de configurer le magasin d’instances de workflow SQL, consultez [Comment : Activer la persistance SQL pour les Workflows et les Services de Workflow](../../../../docs/framework/windows-workflow-foundation/how-to-enable-sql-persistence-for-workflows-and-workflow-services.md). Pour plus d’informations sur les différents paramètres pour le <xref:System.ServiceModel.Activities.Description.SqlWorkflowInstanceStoreBehavior> élément de comportement, consultez [SQL Workflow Instance Store](../../../../docs/framework/windows-workflow-foundation/sql-workflow-instance-store.md). Windows Server App Fabric fournit son propre magasin de persistance. Pour plus d’informations, consultez [persistance de Windows Server App Fabric](https://go.microsoft.com/fwlink/?LinkId=193121).  
  
    > [!NOTE]
    >  L'exemple de configuration précédent utilise une configuration simplifiée. Pour plus d’informations, consultez [Configuration simplifiée](../../../../docs/framework/wcf/simplified-configuration.md)  
  
     Pour obtenir un exemple montrant comment configurer la persistance par programme, consultez [Comment : Activer la persistance pour les Workflows et les Services de flux de travail](../../../../docs/framework/windows-workflow-foundation/how-to-enable-persistence-for-workflows-and-workflow-services.md).  
  
## <a name="see-also"></a>Voir aussi

- [Services de workflow](../../../../docs/framework/wcf/feature-details/workflow-services.md)
- [Persistance du workflow](../../../../docs/framework/windows-workflow-foundation/workflow-persistence.md)
- [Persistance de Windows Server AppFabric](https://go.microsoft.com/fwlink/?LinkId=193121)
