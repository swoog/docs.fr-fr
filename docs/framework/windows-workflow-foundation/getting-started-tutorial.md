---
title: Mise en route Tutorial2
ms.date: 03/30/2017
helpviewer_keywords:
- WF [WF], getting started
- Windows Workflow Foundation [WF], getting started
ms.assetid: c2d3585f-6b1a-4d4f-9865-bd7cd31c5d42
ms.openlocfilehash: 540765c09dceef583798ceaf1abf9f191f444697
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59217430"
---
# <a name="getting-started-tutorial"></a><span data-ttu-id="a3f11-102">Didacticiel de mise en route</span><span class="sxs-lookup"><span data-stu-id="a3f11-102">Getting Started Tutorial</span></span>
<span data-ttu-id="a3f11-103">Cette section contient un ensemble de rubriques de procédure pas à pas qui vous présentent à la programmation d’applications de Windows Workflow Foundation (WF).</span><span class="sxs-lookup"><span data-stu-id="a3f11-103">This section contains a set of walkthrough topics that introduce you to programming Windows Workflow Foundation (WF) applications.</span></span> <span data-ttu-id="a3f11-104">En suivant les procédures dans ces rubriques, vous générerez une application qui est un jeu d'estimation de nombre.</span><span class="sxs-lookup"><span data-stu-id="a3f11-104">By following the procedures in these topics, you will build an application that is a number guessing game.</span></span> <span data-ttu-id="a3f11-105">La première rubrique du didacticiel vous guide tout au long des étapes de création des activités personnalisées obligatoires pour le workflow.</span><span class="sxs-lookup"><span data-stu-id="a3f11-105">The first topic in the tutorial leads you through the steps to create the custom activities required for the workflow.</span></span> <span data-ttu-id="a3f11-106">Dans la deuxième rubrique, ces activités sont assemblées avec les activités de workflow intégrées dans un workflow d'organigramme.</span><span class="sxs-lookup"><span data-stu-id="a3f11-106">In the second topic, these activities are assembled along with built-in workflow activities into a flowchart workflow.</span></span> <span data-ttu-id="a3f11-107">Dans la troisième rubrique, l'application hôte est configurée pour exécuter le workflow et la persistance est introduite dans la dernière rubrique.</span><span class="sxs-lookup"><span data-stu-id="a3f11-107">In the third topic, the host application is configured to run the workflow, and in the final topic persistence is introduced.</span></span> <span data-ttu-id="a3f11-108">Chaque étape de ce processus dépendant des étapes précédentes, nous vous recommandons de les exécuter dans l'ordre.</span><span class="sxs-lookup"><span data-stu-id="a3f11-108">Each step in this process depends on the previous steps, so we recommend that you complete them in order.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="a3f11-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a3f11-109">In This Section</span></span>  
 [<span data-ttu-id="a3f11-110">Procédure : créer une activité</span><span class="sxs-lookup"><span data-stu-id="a3f11-110">How to: Create an Activity</span></span>](how-to-create-an-activity.md)  
 <span data-ttu-id="a3f11-111">Décrit comment créer une activité personnalisée qui dérive de <xref:System.Activities.NativeActivity%601> et comment composer cette activité avec une activité intégrée dans une activité composite à l'aide du concepteur d'activités.</span><span class="sxs-lookup"><span data-stu-id="a3f11-111">Describes how to create a custom activity that derives from <xref:System.Activities.NativeActivity%601>, and how to compose this activity along with a built-in activity into a composite activity using the activity designer.</span></span>  
  
 [<span data-ttu-id="a3f11-112">Procédure : créer un workflow</span><span class="sxs-lookup"><span data-stu-id="a3f11-112">How to: Create a Workflow</span></span>](how-to-create-a-workflow.md)  
 <span data-ttu-id="a3f11-113">Décrit comment créer des workflows d'organigramme, séquentiels et de machine à états à l'aide des activités prédéfinies et des activités personnalisées du didacticiel précédent.</span><span class="sxs-lookup"><span data-stu-id="a3f11-113">Describes how to create flowchart, sequential, and state machine workflows by using built-in activities and the custom activities from the preceding tutorial.</span></span>  
  
 [<span data-ttu-id="a3f11-114">Procédure : exécuter un workflow</span><span class="sxs-lookup"><span data-stu-id="a3f11-114">How to: Run a Workflow</span></span>](how-to-run-a-workflow.md)  
 <span data-ttu-id="a3f11-115">Décrit comment appeler un workflow à partir d'un environnement hôte, passer des données à l'intérieur et à l'extérieur d'un workflow, et reprendre des signets.</span><span class="sxs-lookup"><span data-stu-id="a3f11-115">Describes how to invoke a workflow from a host environment, pass data into and out of a workflow, and how to resume bookmarks.</span></span>  
  
 [<span data-ttu-id="a3f11-116">Procédure : créer et exécuter un workflow durable</span><span class="sxs-lookup"><span data-stu-id="a3f11-116">How to: Create and Run a Long Running Workflow</span></span>](how-to-create-and-run-a-long-running-workflow.md)  
 <span data-ttu-id="a3f11-117">Décrit comment ajouter la persistance à une application de workflow.</span><span class="sxs-lookup"><span data-stu-id="a3f11-117">Describes how to add persistence to a workflow application.</span></span>  
  
 [<span data-ttu-id="a3f11-118">Procédure : créer un participant de suivi de personnalisé</span><span class="sxs-lookup"><span data-stu-id="a3f11-118">How to: Create a Custom Tracking Participant</span></span>](how-to-create-a-custom-tracking-participant.md)  
 <span data-ttu-id="a3f11-119">Décrit comment créer un participant de suivi personnalisé et un modèle de suivi.</span><span class="sxs-lookup"><span data-stu-id="a3f11-119">Describes how to create a custom tracking participant and tracking profile.</span></span>  
  
 [<span data-ttu-id="a3f11-120">Procédure : héberger plusieurs versions d’un workflow côte à côte</span><span class="sxs-lookup"><span data-stu-id="a3f11-120">How to: Host Multiple Versions of a Workflow Side-by-Side</span></span>](how-to-host-multiple-versions-of-a-workflow-side-by-side.md)  
 <span data-ttu-id="a3f11-121">Décrit comment utiliser `WorkflowIdentity` pour héberger plusieurs versions d'un workflow côte à côte.</span><span class="sxs-lookup"><span data-stu-id="a3f11-121">Describes how to use `WorkflowIdentity` to host multiple versions of a workflow side-by-side.</span></span>  
  
 [<span data-ttu-id="a3f11-122">Procédure : mettre à jour la définition d’une instance de workflow en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="a3f11-122">How to: Update the Definition of a Running Workflow Instance</span></span>](how-to-update-the-definition-of-a-running-workflow-instance.md)  
 <span data-ttu-id="a3f11-123">Décrit comment utiliser la mise à jour dynamique pour modifier des instances en cours de exécution de workflow.</span><span class="sxs-lookup"><span data-stu-id="a3f11-123">Describes how to use dynamic update to modify running workflow instances.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3f11-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f11-124">See also</span></span>

- [<span data-ttu-id="a3f11-125">Programmation Windows Workflow Foundation</span><span class="sxs-lookup"><span data-stu-id="a3f11-125">Windows Workflow Foundation Programming</span></span>](programming.md)
