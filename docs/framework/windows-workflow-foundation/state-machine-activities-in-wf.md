---
title: Activités de l'ordinateur d'état dans WF
ms.date: 03/30/2017
ms.assetid: 93312eaf-07e0-4a55-b4f7-4cdbbc4dee2d
ms.openlocfilehash: 5aee2a7cb078d9d62c9296f7dda9f28ff812a88a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120911"
---
# <a name="state-machine-activities-in-wf"></a><span data-ttu-id="a8643-102">Activités de l'ordinateur d'état dans WF</span><span class="sxs-lookup"><span data-stu-id="a8643-102">State Machine Activities in WF</span></span>
[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] <span data-ttu-id="a8643-103">fournit plusieurs activités et concepteurs d'activités fournis par le système pour créer des workflows de machine à états.</span><span class="sxs-lookup"><span data-stu-id="a8643-103">provides several system-provided activities and activity designers for creating state machine workflows.</span></span>  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.StateMachine>|<span data-ttu-id="a8643-104">Exécute des activités contenues à l'aide du modèle de machine à états familier.</span><span class="sxs-lookup"><span data-stu-id="a8643-104">Executes contained activities using the familiar state machine paradigm.</span></span>|  
|<xref:System.Activities.Statements.State>|<span data-ttu-id="a8643-105">Représente un état dans un ordinateur d'état.</span><span class="sxs-lookup"><span data-stu-id="a8643-105">Represents a state in a state machine.</span></span>|  
|<xref:System.Activities.Core.Presentation.FinalState>|<span data-ttu-id="a8643-106">Représente un état d'arrêt au sein d'une machine à états.</span><span class="sxs-lookup"><span data-stu-id="a8643-106">Represents a terminating state in a state machine.</span></span> <span data-ttu-id="a8643-107"><xref:System.Activities.Core.Presentation.FinalState> est un concepteur d'activités qui en cas d'utilisation crée un <xref:System.Activities.Statements.State> préconfiguré comme état d'arrêt.</span><span class="sxs-lookup"><span data-stu-id="a8643-107"><xref:System.Activities.Core.Presentation.FinalState> is an activity designer that when used creates a <xref:System.Activities.Statements.State> preconfigured as a terminating state.</span></span> <span data-ttu-id="a8643-108">Pour plus d’informations, consultez [Concepteur d’activités FinalState](/visualstudio/workflow-designer/finalstate-activity-designer).</span><span class="sxs-lookup"><span data-stu-id="a8643-108">For more information, see [FinalState Activity Designer](/visualstudio/workflow-designer/finalstate-activity-designer).</span></span>|  
|<xref:System.Activities.Statements.Transition>|<span data-ttu-id="a8643-109">Représente la transition entre deux états.</span><span class="sxs-lookup"><span data-stu-id="a8643-109">Represents the transition between two states.</span></span> <span data-ttu-id="a8643-110">Il existe aucune **boîte à outils** d’élément pour <xref:System.Activities.Statements.Transition>; les transitions sont créées sur le Concepteur de workflow en faisant glisser une ligne entre deux États, ou en déposant un état sur les triangles qui s’affichent lorsqu’un état se trouve sur un autre .</span><span class="sxs-lookup"><span data-stu-id="a8643-110">There is no **Toolbox** item for <xref:System.Activities.Statements.Transition>; transitions are created on the workflow designer by dragging and dropping a line between two states, or by dropping a state on the triangles that appear when one state is hovered over another.</span></span> <span data-ttu-id="a8643-111">Pour plus d’informations, consultez [Concepteur d’activités Transition](/visualstudio/workflow-designer/transition-activity-designer).</span><span class="sxs-lookup"><span data-stu-id="a8643-111">For more information, see [Transition Activity Designer](/visualstudio/workflow-designer/transition-activity-designer).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a8643-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8643-112">See also</span></span>

- [<span data-ttu-id="a8643-113">Didacticiel Bien démarrer</span><span class="sxs-lookup"><span data-stu-id="a8643-113">Getting Started Tutorial</span></span>](getting-started-tutorial.md)
