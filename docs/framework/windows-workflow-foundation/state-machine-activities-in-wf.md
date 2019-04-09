---
title: Activités de l'ordinateur d'état dans WF
ms.date: 03/30/2017
ms.assetid: 93312eaf-07e0-4a55-b4f7-4cdbbc4dee2d
ms.openlocfilehash: 5aee2a7cb078d9d62c9296f7dda9f28ff812a88a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59120911"
---
# <a name="state-machine-activities-in-wf"></a>Activités de l'ordinateur d'état dans WF
[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] fournit plusieurs activités fournies par le système et les concepteurs d’activités pour créer des workflows machine à états.  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.StateMachine>|Exécute des activités contenues à l'aide du modèle de machine à états familier.|  
|<xref:System.Activities.Statements.State>|Représente un état dans un ordinateur d'état.|  
|<xref:System.Activities.Core.Presentation.FinalState>|Représente un état d'arrêt au sein d'une machine à états. <xref:System.Activities.Core.Presentation.FinalState> est un concepteur d’activités que quand utilisé crée un <xref:System.Activities.Statements.State> préconfiguré comme un état d’arrêt. Pour plus d’informations, consultez [Concepteur d’activités FinalState](/visualstudio/workflow-designer/finalstate-activity-designer).|  
|<xref:System.Activities.Statements.Transition>|Représente la transition entre deux états. Il existe aucune **boîte à outils** d’élément pour <xref:System.Activities.Statements.Transition>; les transitions sont créées sur le Concepteur de workflow en faisant glisser une ligne entre deux États, ou en déposant un état sur les triangles qui s’affichent lorsqu’un état se trouve sur un autre . Pour plus d’informations, consultez [Concepteur d’activités Transition](/visualstudio/workflow-designer/transition-activity-designer).|  
  
## <a name="see-also"></a>Voir aussi

- [Didacticiel de mise en route](getting-started-tutorial.md)
