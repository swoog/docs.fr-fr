---
title: 'Procédure : configurer le suivi avec WorkflowServiceHost'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ed1485fe-7529-4351-bca3-8bb915260b17
caps.latest.revision: 14
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: e1de3349bb9766beeee95b9934fc1ca11fc7006f
ms.sourcegitcommit: 94d33cadc5ff81d2ac389bf5f26422c227832052
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2018
---
# <a name="how-to-configure-tracking-with-workflowservicehost"></a>Procédure : configurer le suivi avec WorkflowServiceHost
Cette rubrique explique comment configurer le suivi pour un workflow [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] hébergé dans <xref:System.ServiceModel.Activities.WorkflowServiceHost>. Il est configuré via un fichier Web.config en spécifiant un comportement de service.  
  
### <a name="configure-tracking-in-configuration"></a>Configurer le suivi dans le fichier de configuration  
  
1.  Ajoutez <xref:System.Activities.Tracking.EtwTrackingParticipant> à l'aide de l'élément <`behavior`> dans un fichier de configuration, comme indiqué dans l'exemple suivant.  
  
    ```xml  
    <behaviors>  
       <serviceBehaviors>  
         <behavior>  
           <etwTracking profileName="Sample Tracking Profile" />  
         </behavior>              
       </serviceBehaviors>  
    <behaviors>  
    ```  
  
    > [!NOTE]
    >  L'exemple de configuration précédent utilise la configuration simplifiée. Pour plus d’informations, consultez [Configuration simplifiée](../../../../docs/framework/wcf/simplified-configuration.md).  
  
     L'exemple de configuration précédent ajoute un objet <xref:System.Activities.Tracking.EtwTrackingParticipant> et spécifie un nom de modèle de suivi. Les modèles de suivi sont créés dans un élément <`trackingProfile`> au sein d'un élément <`tracking`>. Le modèle de suivi contient des requêtes de suivi qui permettent à un participant de suivi de s'abonner à des événements de workflow émis lorsque l'état d'une instance de workflow change au moment de l'exécution. L'exemple suivant montre comment créer un modèle de suivi.  
  
    ```xml  
    <system.serviceModel>  
        <tracking>   
         <trackingProfile name="Sample Tracking Profile">  
            <workflow activityDefinitionId="*">  
               <workflowInstanceQueries>  
                 <workflowInstanceQuery>  
                    <states>  
                       <state name="Started"/>  
                       <state name="Completed"/>  
                    </states>  
                </workflowInstanceQuery>  
             </workflowInstanceQueries>  
           </workflow>  
         </trackingProfile>   
       </tracking>  
    </system.serviceModel>  
    ```  
  
     Pour plus d’informations sur les profils de suivi, consultez [modèles de suivi](../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).  
  
     Pour plus d’informations sur le suivi en général, consultez [suivi et traçage de Workflow](../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md).  
  
### <a name="configure-tracking-in-code"></a>Configurer le suivi dans le code  
  
1.  Ajoutez le <xref:System.Activities.Tracking.EtwTrackingParticipant> à l'aide du comportement <xref:System.ServiceModel.Activities.Description.EtwTrackingBehavior> dans le code, comme indiqué dans l'exemple suivant.  
  
    ```csharp  
    host.Description.Behaviors.Add(new EtwTrackingBehavior { ProfileName = "Sample Tracking Profile" });  
    ```  
  
     L'exemple de code précédent ajoute un objet <xref:System.Activities.Tracking.EtwTrackingParticipant> et spécifie un nom de modèle de suivi. Les modèles de suivi sont créés dans un élément <`trackingProfile`> au sein d'un élément <`tracking`> comme indiqué sans la section précédente.  
  
     Pour plus d’informations sur les profils de suivi, consultez [modèles de suivi](../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md).  
  
     Pour plus d’informations sur le suivi en général, consultez [suivi et traçage de Workflow](../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md). Pour obtenir un exemple de configuration du suivi par programme, consultez [configuration du suivi d’un flux de travail](../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Configuration simplifiée pour les services WCF](../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md)  
 [Services de workflow](../../../../docs/framework/wcf/feature-details/workflow-services.md)  
 [Profils de suivi](../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
