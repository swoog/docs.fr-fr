---
title: Réhébergement du Workflow Designer
ms.date: 03/30/2017
ms.assetid: bec1fc28-f902-4edb-86c5-436cec802c2b
ms.openlocfilehash: 98048ca58bf635f4e87241befa083dc240deaecf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61968179"
---
# <a name="rehosting-the-workflow-designer"></a>Réhébergement du Workflow Designer
Le [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] peut être réhébergé dans des environnements en dehors de Visual Studio 2012 dans le cadre de la création, la modification et la surveillance des flux de travail.

 Le type <xref:System.Activities.Presentation.WorkflowDesigner> est un wrapper de la zone de dessin, de la grille des propriétés et d'autres éléments, et expose un modèle de programmation de base conçu pour gérer la majorité des scénarios de réhébergement du concepteur. Hébergement du <xref:System.Activities.Presentation.WorkflowDesigner> à l’intérieur de Windows Presentation Foundation (WPF) l’application est un scénario de réhébergement commun pour [!INCLUDE[wfd2](../../../includes/wfd2-md.md)].

## <a name="in-this-section"></a>Dans cette section
 [Tâche 1 : Créer une nouvelle Application Windows Presentation Foundation](task-1-create-a-new-wpf-app.md)

 [Tâche 2 : Héberger le Concepteur de flux de travail](task-2-host-the-workflow-designer.md)

 [Tâche 3 : Créer les volets Toolbox et PropertyGrid](task-3-create-the-toolbox-and-propertygrid-panes.md)

 [Prise en charge des nouvelles fonctionnalités Workflow Foundation 4.5 dans le concepteur de flux de travail réhébergé](wf-features-in-the-rehosted-workflow-designer.md)

## <a name="see-also"></a>Voir aussi

- [Personnalisation de l’expérience de conception de workflow](customizing-the-workflow-design-experience.md)
