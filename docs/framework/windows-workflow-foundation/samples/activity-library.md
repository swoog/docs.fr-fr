---
title: Bibliothèque d'activités
ms.date: 03/30/2017
ms.assetid: 5323e9d4-71d6-47eb-bfa6-31feac62044d
ms.openlocfilehash: b701d382c25644181b23f3c0f0cd8e019b8d37d1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61909179"
---
# <a name="activity-library"></a><span data-ttu-id="515bb-102">Bibliothèque d'activités</span><span class="sxs-lookup"><span data-stu-id="515bb-102">Activity Library</span></span>
<span data-ttu-id="515bb-103">Cette section contient des exemples qui illustrent des activités personnalisées avancées dans Windows Workflow Foundation (WF).</span><span class="sxs-lookup"><span data-stu-id="515bb-103">This section contains samples that demonstrate advanced custom activities in Windows Workflow Foundation (WF).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="515bb-104">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="515bb-104">In This Section</span></span>

 [<span data-ttu-id="515bb-105">Activité personnalisée SendMail</span><span class="sxs-lookup"><span data-stu-id="515bb-105">SendMail Custom Activity</span></span>](sendmail-custom-activity.md)  
 <span data-ttu-id="515bb-106">Montre comment créer une activité personnalisée dérivée de <xref:System.Activities.AsyncCodeActivity> pour envoyer du courrier à l'aide de SMTP afin de l'utiliser dans une application de workflow.</span><span class="sxs-lookup"><span data-stu-id="515bb-106">Demonstrates how to create a custom activity that derives from <xref:System.Activities.AsyncCodeActivity> to send mail using SMTP for use within a workflow application.</span></span>  
  
 [<span data-ttu-id="515bb-107">ParallelForEach limité</span><span class="sxs-lookup"><span data-stu-id="515bb-107">Throttled Parallel ForEach</span></span>](throttled-parallel-foreach.md)  
 <span data-ttu-id="515bb-108">Montre comment l’activité `ThrottleParallelForEach` est semblable à l’activité <xref:System.Activities.Statements.ParallelForEach%601> hormis le seul fait qu’elle permet la définition d’un facteur de concurrence pour restreindre le nombre de branches simultanées à exécuter.</span><span class="sxs-lookup"><span data-stu-id="515bb-108">Demonstrates how the `ThrottleParallelForEach` activity is similar to the <xref:System.Activities.Statements.ParallelForEach%601> activity with the one exception that it allows setting a concurrency factor to restrict the number of simultaneous branches to execute.</span></span>
  
 [<span data-ttu-id="515bb-109">Activités d’accès aux bases de données</span><span class="sxs-lookup"><span data-stu-id="515bb-109">Database Access Activities</span></span>](database-access-activities.md)  
 <span data-ttu-id="515bb-110">Montre comment créer des activités qui permettent l’accès aux bases de données pour récupérer ou modifier les informations et utilisez [ADO.NET](https://go.microsoft.com/fwlink/?LinkId=166081) pour accéder à la base de données.</span><span class="sxs-lookup"><span data-stu-id="515bb-110">Demonstrates how to create activities that allow accessing databases to retrieve or modify information and use [ADO.NET](https://go.microsoft.com/fwlink/?LinkId=166081) to access the database.</span></span>  
  
 [<span data-ttu-id="515bb-111">Activité de stratégie externalisée dans .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="515bb-111">Externalized Policy Activity in .NET Framework 4.5</span></span>](externalized-policy-activity-in-net-framework-4-5.md)  
 <span data-ttu-id="515bb-112">Montre comment l’activité ExternalizedPolicy4 permet l’exécution existantes de Windows Workflow Foundation dans [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF 3.5) <xref:System.Workflow.Activities.Rules.RuleSet> objets dans Windows Workflow Foundation dans [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF 4.5) directement à l’aide du moteur de règles qui est fourni dans WF 3.5.</span><span class="sxs-lookup"><span data-stu-id="515bb-112">Demonstrates how the ExternalizedPolicy4 activity allows executing existing Windows Workflow Foundation in [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF 3.5) <xref:System.Workflow.Activities.Rules.RuleSet> objects in Windows Workflow Foundation in [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF 4.5) directly by using the rules engine that is shipped in WF 3.5.</span></span> 
  
 [<span data-ttu-id="515bb-113">ForEach non générique</span><span class="sxs-lookup"><span data-stu-id="515bb-113">Non-Generic ForEach</span></span>](non-generic-foreach.md)  
 <span data-ttu-id="515bb-114">Montre comment créer une version non générique de l'activité <xref:System.Activities.Statements.ForEach%601>.</span><span class="sxs-lookup"><span data-stu-id="515bb-114">Demonstrates how to create a non-generic version of the <xref:System.Activities.Statements.ForEach%601> activity.</span></span>  
  
 [<span data-ttu-id="515bb-115">ParallelForEach non générique</span><span class="sxs-lookup"><span data-stu-id="515bb-115">Non-Generic ParallelForEach</span></span>](non-generic-parallelforeach.md)  
 <span data-ttu-id="515bb-116">Montre comment créer une version non générique de l'activité <xref:System.Activities.Statements.ParallelForEach%601>.</span><span class="sxs-lookup"><span data-stu-id="515bb-116">Demonstrates how to create a non-generic version of the <xref:System.Activities.Statements.ParallelForEach%601> activity.</span></span>  
  
 [<span data-ttu-id="515bb-117">Obtenir WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="515bb-117">Get WorkflowInstanceId</span></span>](get-workflowinstanceid.md)  
 <span data-ttu-id="515bb-118">Montre comment utiliser l'activité personnalisée `GetWorkflowInstanceId` pour retourner l'ID d'instance de workflow.</span><span class="sxs-lookup"><span data-stu-id="515bb-118">Demonstrates how to use the custom activity, `GetWorkflowInstanceId`, to return the workflow instance ID.</span></span>
