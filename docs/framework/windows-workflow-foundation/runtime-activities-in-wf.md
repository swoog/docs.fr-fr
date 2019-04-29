---
title: Activités d'exécution dans WF
ms.date: 03/30/2017
ms.assetid: e5ae8c31-19bc-4655-88b3-6b75cd6a1bd5
ms.openlocfilehash: 7981d3f75c8fd2d0ddd2ae0233f425c2907c270c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938097"
---
# <a name="runtime-activities-in-wf"></a><span data-ttu-id="0efe6-102">Activités d'exécution dans WF</span><span class="sxs-lookup"><span data-stu-id="0efe6-102">Runtime Activities in WF</span></span>
[!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] <span data-ttu-id="0efe6-103">offre plusieurs activités fournies par le système pour l'accès aux fonctionnalités de l'exécution du workflow, telles que la persistance et l'arrêt de workflow.</span><span class="sxs-lookup"><span data-stu-id="0efe6-103">provides several system-provided activities for accessing the features of the workflow runtime, such as persistence and termination.</span></span>  
  
|<span data-ttu-id="0efe6-104">Activité</span><span class="sxs-lookup"><span data-stu-id="0efe6-104">Activity</span></span>|<span data-ttu-id="0efe6-105">Description</span><span class="sxs-lookup"><span data-stu-id="0efe6-105">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.Activities.Statements.Persist>|<span data-ttu-id="0efe6-106">Demande de façon explicite à ce que le workflow rende son état persistant.</span><span class="sxs-lookup"><span data-stu-id="0efe6-106">Explicitly requests that the workflow persist its state.</span></span>|  
|<xref:System.Activities.Statements.TerminateWorkflow>|<span data-ttu-id="0efe6-107">Arrête l'instance de workflow en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="0efe6-107">Terminates the running workflow instance.</span></span>|  
|<xref:System.Activities.Statements.NoPersistScope>|<span data-ttu-id="0efe6-108">Activité de conteneur qui empêche la persistance des activités enfants.</span><span class="sxs-lookup"><span data-stu-id="0efe6-108">A container activity that prevents child activities from persisting.</span></span>|
