---
title: Bibliothèque d'activités
ms.date: 03/30/2017
ms.assetid: 5323e9d4-71d6-47eb-bfa6-31feac62044d
ms.openlocfilehash: 7e8777d0068e6cca9c9324a6fd2668e6ff9e9da7
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48844018"
---
# <a name="activity-library"></a>Bibliothèque d'activités
Cette section contient des exemples qui illustrent des activités personnalisées avancées dans Windows Workflow Foundation (WF).  
  
## <a name="in-this-section"></a>Dans cette section

 [Activité personnalisée SendMail](../../../../docs/framework/windows-workflow-foundation/samples/sendmail-custom-activity.md)  
 Montre comment créer une activité personnalisée dérivée de <xref:System.Activities.AsyncCodeActivity> pour envoyer du courrier à l'aide de SMTP afin de l'utiliser dans une application de workflow.  
  
 [ParallelForEach limité](../../../../docs/framework/windows-workflow-foundation/samples/throttled-parallel-foreach.md)  
 Montre comment l'activité `ThrottleParallelForEach` est semblable à l'activité <xref:System.Activities.Statements.ParallelForEach%601> hormis le seul fait qu'elle permet la définition d'un facteur de concurrence pour restreindre le nombre de branches simultanées à exécuter.
  
 [Activités d’accès aux bases de données](../../../../docs/framework/windows-workflow-foundation/samples/database-access-activities.md)  
 Montre comment créer des activités qui permettent l’accès aux bases de données pour récupérer ou modifier les informations et utilisez [ADO.NET](https://go.microsoft.com/fwlink/?LinkId=166081) pour accéder à la base de données.  
  
 [Activité de stratégie externalisée dans .NET Framework 4.5](../../../../docs/framework/windows-workflow-foundation/samples/externalized-policy-activity-in-net-framework-4-5.md)  
 Montre comment l’activité ExternalizedPolicy4 permet l’exécution existantes de Windows Workflow Foundation dans [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF 3.5) <xref:System.Workflow.Activities.Rules.RuleSet> objets dans Windows Workflow Foundation dans [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF 4.5) directement à l’aide du moteur de règles qui est fourni dans WF 3.5. 
  
 [ForEach non générique](../../../../docs/framework/windows-workflow-foundation/samples/non-generic-foreach.md)  
 Montre comment créer une version non générique de l'activité <xref:System.Activities.Statements.ForEach%601>.  
  
 [ParallelForEach non générique](../../../../docs/framework/windows-workflow-foundation/samples/non-generic-parallelforeach.md)  
 Montre comment créer une version non générique de l'activité <xref:System.Activities.Statements.ParallelForEach%601>.  
  
 [Obtenir WorkflowInstanceId](../../../../docs/framework/windows-workflow-foundation/samples/get-workflowinstanceid.md)  
 Montre comment utiliser l'activité personnalisée `GetWorkflowInstanceId` pour retourner l'ID d'instance de workflow.
