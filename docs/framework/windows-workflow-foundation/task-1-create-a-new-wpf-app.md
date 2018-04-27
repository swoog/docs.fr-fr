---
title: 'Tâche 1 : créer une nouvelle application Windows Presentation Foundation.'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 270eaeba-9492-4532-af9f-403ce5c9935b
caps.latest.revision: 14
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: cd21013331e19fa9e18ad7cbee0a7bb07abaf3d2
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="task-1-create-a-new-windows-presentation-foundation-application"></a><span data-ttu-id="62e47-102">Tâche 1 : créer une nouvelle application Windows Presentation Foundation.</span><span class="sxs-lookup"><span data-stu-id="62e47-102">Task 1: Create a New Windows Presentation Foundation Application</span></span>
<span data-ttu-id="62e47-103">Dans cette tâche, vous créez une application Windows Presentation Foundation (WPF) vide en utilisant le modèle Visual Studio d’Application WPF et ajouter des références approprié [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] assemblys de workflow.</span><span class="sxs-lookup"><span data-stu-id="62e47-103">In this task, you will create an empty Windows Presentation Foundation (WPF) application by using the WPF Application Visual Studio template and add references to the appropriate [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] workflow assemblies.</span></span>  
  
### <a name="to-create-the-wpf-application-project"></a><span data-ttu-id="62e47-104">Pour créer le projet d'application WPF</span><span class="sxs-lookup"><span data-stu-id="62e47-104">To create the WPF Application project</span></span>  
  
1.  <span data-ttu-id="62e47-105">Ouvrez Visual Studio et sur le **fichier** menu, pointez sur **nouveau**, puis cliquez sur **projet**.</span><span class="sxs-lookup"><span data-stu-id="62e47-105">Open Visual Studio and on the **File** menu, point to **New**, and then click **Project**.</span></span>  
  
2.  <span data-ttu-id="62e47-106">Dans le **nouveau projet** boîte de dialogue, sélectionnez soit **Visual C#** ou **Visual Basic** à partir de la **modèles installés** volet situé à gauche de la zone.</span><span class="sxs-lookup"><span data-stu-id="62e47-106">In the **New Project** dialog box, select either **Visual C#** or **Visual Basic** from the **Installed Templates** pane on the left side of the box.</span></span> <span data-ttu-id="62e47-107">Si la langue de votre choix n’apparaît pas, regardez sous **autres langages**.</span><span class="sxs-lookup"><span data-stu-id="62e47-107">If the language of your choice does not appear, look under **Other Languages**.</span></span>  
  
3.  <span data-ttu-id="62e47-108">Sélectionnez **Windows** dans les **modèles installés** volet.</span><span class="sxs-lookup"><span data-stu-id="62e47-108">Select **Windows** in the **Installed Templates** pane.</span></span>  
  
4.  <span data-ttu-id="62e47-109">Dans le volet supérieur, vérifiez que (la valeur par défaut) **.NET Framework 4** a été sélectionné dans la zone de liste déroulante, puis sélectionnez **Application WPF**.</span><span class="sxs-lookup"><span data-stu-id="62e47-109">In the top pane, confirm that (the default value) **.NET Framework 4** has been selected in the drop-down list box, and then select **WPF Application**.</span></span>  
  
5.  <span data-ttu-id="62e47-110">Définissez le nom du projet pour **HostingApplication** au bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="62e47-110">Set the name of the project to **HostingApplication** at the bottom of the window.</span></span>  
  
6.  <span data-ttu-id="62e47-111">Définissez le nom de la solution sur **RehostingTheDesigner**.</span><span class="sxs-lookup"><span data-stu-id="62e47-111">Set the solution name to **RehostingTheDesigner**.</span></span>  
  
7.  <span data-ttu-id="62e47-112">Cliquez sur **OK** pour créer le projet d’application.</span><span class="sxs-lookup"><span data-stu-id="62e47-112">Click **OK** to create the application project.</span></span> <span data-ttu-id="62e47-113">Visual Studio crée une base WPF UI pour votre application et inclut les fichiers code-behind XAML approprié.</span><span class="sxs-lookup"><span data-stu-id="62e47-113">Visual Studio creates a basic WPF UI for your application and includes the appropriate XAML and code-behind files.</span></span>  
  
8.  <span data-ttu-id="62e47-114">Ajoutez des références aux **WorkflowModel** assemblys.</span><span class="sxs-lookup"><span data-stu-id="62e47-114">Add references to **WorkflowModel** assemblies.</span></span> <span data-ttu-id="62e47-115">Pour ce faire, dans **l’Explorateur de solutions**, avec le bouton droit le **HostingApplication** de projet et sélectionnez **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="62e47-115">To do this, in **Solution Explorer**, right-click the **HostingApplication** project and select **Add Reference**.</span></span>  
  
9. <span data-ttu-id="62e47-116">Dans le **ajouter une référence** boîte de dialogue, cliquez sur le **.NET** onglet, maintenez la touche CTRL enfoncée, sélectionnez les assemblys suivants, puis cliquez sur **OK**:</span><span class="sxs-lookup"><span data-stu-id="62e47-116">In the **Add Reference** dialog box, click the **.NET** tab, hold down the CTRL key, select the following assemblies, and then click **OK**:</span></span>  
  
    -   <span data-ttu-id="62e47-117">System.Activities</span><span class="sxs-lookup"><span data-stu-id="62e47-117">System.Activities</span></span>  
  
    -   <span data-ttu-id="62e47-118">System.Activities.Presentation</span><span class="sxs-lookup"><span data-stu-id="62e47-118">System.Activities.Presentation</span></span>  
  
    -   <span data-ttu-id="62e47-119">System.Activities.Core.Presentation</span><span class="sxs-lookup"><span data-stu-id="62e47-119">System.Activities.Core.Presentation</span></span>  
  
10. <span data-ttu-id="62e47-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="62e47-120">Click **OK**.</span></span>  
  
11. <span data-ttu-id="62e47-121">Consultez [tâche 2 : héberger le Workflow Designer](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md) pour en savoir plus sur l’hôte de la zone de conception du Concepteur de workflow.</span><span class="sxs-lookup"><span data-stu-id="62e47-121">See [Task 2: Host the Workflow Designer](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md) to learn how to host the workflow designer design canvas.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62e47-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62e47-122">See Also</span></span>  
 [<span data-ttu-id="62e47-123">Réhébergement du concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="62e47-123">Rehosting the Workflow Designer</span></span>](../../../docs/framework/windows-workflow-foundation/rehosting-the-workflow-designer.md)  
 [<span data-ttu-id="62e47-124">Tâche 2 : Héberger le concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="62e47-124">Task 2: Host the Workflow Designer</span></span>](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md)
