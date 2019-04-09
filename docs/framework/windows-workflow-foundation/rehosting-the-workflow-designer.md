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
# <a name="rehosting-the-workflow-designer"></a><span data-ttu-id="318fb-102">Réhébergement du Workflow Designer</span><span class="sxs-lookup"><span data-stu-id="318fb-102">Rehosting the Workflow Designer</span></span>
<span data-ttu-id="318fb-103">Le [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] peut être réhébergé dans des environnements en dehors de Visual Studio 2012 dans le cadre de la création, la modification et la surveillance des flux de travail.</span><span class="sxs-lookup"><span data-stu-id="318fb-103">The [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] can be rehosted in environments outside of Visual Studio 2012 for the purposes of creating, modifying, and monitoring workflows.</span></span>

 <span data-ttu-id="318fb-104">Le type <xref:System.Activities.Presentation.WorkflowDesigner> est un wrapper de la zone de dessin, de la grille des propriétés et d'autres éléments, et expose un modèle de programmation de base conçu pour gérer la majorité des scénarios de réhébergement du concepteur.</span><span class="sxs-lookup"><span data-stu-id="318fb-104">The <xref:System.Activities.Presentation.WorkflowDesigner> type is a wrapper of the canvas, property grid, and other elements, and exposes a basic programming model to handle the majority of designer rehosting scenarios.</span></span> <span data-ttu-id="318fb-105">Hébergement du <xref:System.Activities.Presentation.WorkflowDesigner> à l’intérieur de Windows Presentation Foundation (WPF) l’application est un scénario de réhébergement commun pour [!INCLUDE[wfd2](../../../includes/wfd2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="318fb-105">Hosting the <xref:System.Activities.Presentation.WorkflowDesigner> inside a Windows Presentation Foundation (WPF) application is a common rehosting scenario for [!INCLUDE[wfd2](../../../includes/wfd2-md.md)].</span></span>

## <a name="in-this-section"></a><span data-ttu-id="318fb-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="318fb-106">In This Section</span></span>
 [<span data-ttu-id="318fb-107">Tâche 1 : créer une application Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="318fb-107">Task 1: Create a New Windows Presentation Foundation Application</span></span>](task-1-create-a-new-wpf-app.md)

 [<span data-ttu-id="318fb-108">Tâche 2 : héberger le concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="318fb-108">Task 2: Host the Workflow Designer</span></span>](task-2-host-the-workflow-designer.md)

 [<span data-ttu-id="318fb-109">Tâche 3 : créer les volets Toolbox et PropertyGrid</span><span class="sxs-lookup"><span data-stu-id="318fb-109">Task 3: Create the Toolbox and PropertyGrid Panes</span></span>](task-3-create-the-toolbox-and-propertygrid-panes.md)

 [<span data-ttu-id="318fb-110">Prise en charge de nouvelles fonctionnalités Workflow Foundation 4.5 dans le concepteur de workflow réhébergé</span><span class="sxs-lookup"><span data-stu-id="318fb-110">Support for New Workflow Foundation 4.5 Features in the Rehosted Workflow Designer</span></span>](wf-features-in-the-rehosted-workflow-designer.md)

## <a name="see-also"></a><span data-ttu-id="318fb-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="318fb-111">See also</span></span>

- [<span data-ttu-id="318fb-112">Personnalisation de l'expérience de conception de workflow</span><span class="sxs-lookup"><span data-stu-id="318fb-112">Customizing the Workflow Design Experience</span></span>](customizing-the-workflow-design-experience.md)
