---
title: Réhébergement du Workflow Designer
ms.date: 03/30/2017
ms.assetid: bec1fc28-f902-4edb-86c5-436cec802c2b
ms.openlocfilehash: 98048ca58bf635f4e87241befa083dc240deaecf
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59206107"
---
# <a name="rehosting-the-workflow-designer"></a>Réhébergement du Workflow Designer
Le [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] peut être réhébergé dans des environnements en dehors de Visual Studio 2012 dans le cadre de la création, la modification et la surveillance des flux de travail.

 Le type <xref:System.Activities.Presentation.WorkflowDesigner> est un wrapper de la zone de dessin, de la grille des propriétés et d'autres éléments, et expose un modèle de programmation de base conçu pour gérer la majorité des scénarios de réhébergement du concepteur. Hébergement du <xref:System.Activities.Presentation.WorkflowDesigner> à l’intérieur de Windows Presentation Foundation (WPF) l’application est un scénario de réhébergement commun pour [!INCLUDE[wfd2](../../../includes/wfd2-md.md)].

## <a name="in-this-section"></a>Dans cette section
 [Tâche 1 : créer une application Windows Presentation Foundation](task-1-create-a-new-wpf-app.md)

 [Tâche 2 : héberger le concepteur de flux de travail](task-2-host-the-workflow-designer.md)

 [Tâche 3 : créer les volets Toolbox et PropertyGrid](task-3-create-the-toolbox-and-propertygrid-panes.md)

 [Prise en charge de nouvelles fonctionnalités Workflow Foundation 4.5 dans le concepteur de workflow réhébergé](wf-features-in-the-rehosted-workflow-designer.md)

## <a name="see-also"></a>Voir aussi

- [Personnalisation de l'expérience de conception de workflow](customizing-the-workflow-design-experience.md)
