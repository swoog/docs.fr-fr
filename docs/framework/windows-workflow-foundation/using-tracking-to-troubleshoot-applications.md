---
title: Utilisation du suivi pour résoudre les problèmes posés par les applications
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8851adde-c3c2-4391-9523-d8eb831490af
caps.latest.revision: 7
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: adc9a159b8887b0198cf19891f73fdee2a48437b
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2018
---
# <a name="using-tracking-to-troubleshoot-applications"></a>Utilisation du suivi pour résoudre les problèmes posés par les applications
Windows Workflow Foundation (WF) vous permet de vous permettent de suivre les informations relatives au flux de travail pour donner des détails concernant l’exécution d’une application Windows Workflow Foundation ou de service. Les hôtes de Windows Workflow Foundation sont en mesure de capturer des événements de workflow pendant l’exécution d’une instance de workflow. Si votre flux de travail génère des erreurs ou des exceptions, vous pouvez utiliser le suivi des détails pour la résolution des problèmes de son traitement Windows Workflow Foundation.  
  
## <a name="troubleshooting-a-wf-using-wf-tracking"></a>Dépannage d'un WF à l'aide du suivi WF  
 Pour détecter les erreurs dans le traitement d’une activité de Windows Workflow Foundation, vous pouvez activer le suivi avec un modèle de suivi des requêtes pour un <xref:System.Activities.Tracking.ActivityStateRecord> avec l’état Faulted. La requête correspondante est spécifiée dans le code suivant.  
  
```xml  
<activityStateQueries>  
              <activityStateQuery activityName="*">  
                <states>  
                  <state name="Faulted" />  
                </states>  
              </activityStateQuery>  
 </activityStateQueries>  
```  
  
 Si une erreur est propagée et gérée dans un gestionnaire d'erreur (tel qu'une activité <xref:System.Activities.Statements.TryCatch>), cette erreur peut être détectée à l'aide d'un <xref:System.Activities.Tracking.FaultPropagationRecord>. <xref:System.Activities.Tracking.FaultPropagationRecord> indique l'activité source de l'erreur et le nom du gestionnaire d'erreur. <xref:System.Activities.Tracking.FaultPropagationRecord> contient des détails sur l'erreur sous la forme d'une pile d'exception. La requête permettant de s'abonner à un <xref:System.Activities.Tracking.FaultPropagationRecord> est illustrée dans l'exemple suivant.  
  
```xml  
<faultPropagationQueries>  
              <faultPropagationQuery faultSourceActivityName ="*" faultHandlerActivityName="*"/>  
 </faultPropagationQueries>  
```  
  
 Si une erreur n'est pas gérée dans le workflow, cela génère une exception non prise en charge au niveau de l'instance du workflow et l'instance du workflow est abandonnée. Pour comprendre les détails de l'exception non prise en charge, le modèle de suivi doit interroger l'enregistrement de l'instance du workflow dont l'état est `state name="UnhandledException"`, comme spécifié dans l'exemple suivant.  
  
```xml  
<workflowInstanceQueries>  
              <workflowInstanceQuery>  
                <states>  
                  <state name="UnhandledException" />  
                </states>  
              </workflowInstanceQuery>  
</workflowInstanceQueries>  
```  
  
 Lorsqu’une instance de workflow rencontre une exception non gérée, un <xref:System.Activities.Tracking.WorkflowInstanceUnhandledExceptionRecord> objet est émis si le suivi de Windows Workflow Foundation a été activé.  
  
 Cet enregistrement de suivi contient les détails de l'erreur sous la forme d'une pile d'exception. Il comporte les détails de la source de l’erreur qui a échoué et a provoqué l’exception non gérée (par exemple, l’activité). Pour vous abonner aux événements d’erreur à partir d’un ordinateur Windows Workflow Foundation, activer le suivi en ajoutant un participant de suivi. Configurez ce participant avec un modèle de suivi qui recherche `ActivityStateQuery (state="Faulted")`, <xref:System.Activities.Tracking.FaultPropagationRecord> et `WorkflowInstanceQuery (state="UnhandledException")`.  
  
 Si le suivi est activé à l'aide du participant de suivi ETW, les événements d'erreur sont émis sur une session ETW. Les événements peuvent être visualisés à l'aide de l'Observateur d'événements. Il se trouve dans le nœud **Applications -> l’Observateur d’événements et journaux des Services -> Microsoft -> Windows -> serveur d’applications-Applications** dans le canal analytique.  
  
## <a name="see-also"></a>Voir aussi  
 [Analyse de Windows Server App Fabric](http://go.microsoft.com/fwlink/?LinkId=201273)  
 [Analyse des Applications avec AppFabric](http://go.microsoft.com/fwlink/?LinkId=201275)
