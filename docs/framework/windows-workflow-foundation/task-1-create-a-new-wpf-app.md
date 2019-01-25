---
title: 'Tâche 1 : Créer une nouvelle Application Windows Presentation Foundation'
ms.date: 03/30/2017
ms.assetid: 270eaeba-9492-4532-af9f-403ce5c9935b
ms.openlocfilehash: 39cd901c0129124bece8e8d3a573fd45209cfb00
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54679407"
---
# <a name="task-1-create-a-new-windows-presentation-foundation-application"></a><span data-ttu-id="988ef-102">Tâche 1 : Créer une nouvelle Application Windows Presentation Foundation</span><span class="sxs-lookup"><span data-stu-id="988ef-102">Task 1: Create a New Windows Presentation Foundation Application</span></span>
<span data-ttu-id="988ef-103">Dans cette tâche, vous créez une application Windows Presentation Foundation (WPF) vide à l’aide du modèle Application WPF Visual Studio et ajoutez des références appropriés [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] assemblys de workflow.</span><span class="sxs-lookup"><span data-stu-id="988ef-103">In this task, you will create an empty Windows Presentation Foundation (WPF) application by using the WPF Application Visual Studio template and add references to the appropriate [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] workflow assemblies.</span></span>  
  
### <a name="to-create-the-wpf-application-project"></a><span data-ttu-id="988ef-104">Pour créer le projet d'application WPF</span><span class="sxs-lookup"><span data-stu-id="988ef-104">To create the WPF Application project</span></span>  
  
1.  <span data-ttu-id="988ef-105">Ouvrez Visual Studio et sur le **fichier** menu, pointez sur **New**, puis cliquez sur **projet**.</span><span class="sxs-lookup"><span data-stu-id="988ef-105">Open Visual Studio and on the **File** menu, point to **New**, and then click **Project**.</span></span>  
  
2.  <span data-ttu-id="988ef-106">Dans le **nouveau projet** boîte de dialogue, sélectionnez soit **Visual C#**  ou **Visual Basic** à partir de la **modèles installés** volet de gauche côté de la zone.</span><span class="sxs-lookup"><span data-stu-id="988ef-106">In the **New Project** dialog box, select either **Visual C#** or **Visual Basic** from the **Installed Templates** pane on the left side of the box.</span></span> <span data-ttu-id="988ef-107">Si la langue de votre choix n’apparaît pas, regardez sous **autres langages**.</span><span class="sxs-lookup"><span data-stu-id="988ef-107">If the language of your choice does not appear, look under **Other Languages**.</span></span>  
  
3.  <span data-ttu-id="988ef-108">Sélectionnez **Windows** dans le **modèles installés** volet.</span><span class="sxs-lookup"><span data-stu-id="988ef-108">Select **Windows** in the **Installed Templates** pane.</span></span>  
  
4.  <span data-ttu-id="988ef-109">Dans le volet supérieur, vérifiez que (la valeur par défaut) **.NET Framework 4** a été sélectionné dans la zone de liste déroulante, puis sélectionnez **Application WPF**.</span><span class="sxs-lookup"><span data-stu-id="988ef-109">In the top pane, confirm that (the default value) **.NET Framework 4** has been selected in the drop-down list box, and then select **WPF Application**.</span></span>  
  
5.  <span data-ttu-id="988ef-110">Définissez le nom du projet à **HostingApplication** en bas de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="988ef-110">Set the name of the project to **HostingApplication** at the bottom of the window.</span></span>  
  
6.  <span data-ttu-id="988ef-111">La valeur est le nom de la solution **RehostingTheDesigner**.</span><span class="sxs-lookup"><span data-stu-id="988ef-111">Set the solution name to **RehostingTheDesigner**.</span></span>  
  
7.  <span data-ttu-id="988ef-112">Cliquez sur **OK** pour créer le projet d’application.</span><span class="sxs-lookup"><span data-stu-id="988ef-112">Click **OK** to create the application project.</span></span> <span data-ttu-id="988ef-113">Visual Studio crée une base UI WPF pour votre application et inclut les fichiers code-behind XAML appropriée.</span><span class="sxs-lookup"><span data-stu-id="988ef-113">Visual Studio creates a basic WPF UI for your application and includes the appropriate XAML and code-behind files.</span></span>  
  
8.  <span data-ttu-id="988ef-114">Ajouter des références aux **WorkflowModel** assemblys.</span><span class="sxs-lookup"><span data-stu-id="988ef-114">Add references to **WorkflowModel** assemblies.</span></span> <span data-ttu-id="988ef-115">Pour ce faire, dans **l’Explorateur de solutions**, avec le bouton droit le **HostingApplication** de projet et sélectionnez **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="988ef-115">To do this, in **Solution Explorer**, right-click the **HostingApplication** project and select **Add Reference**.</span></span>  
  
9. <span data-ttu-id="988ef-116">Dans le **ajouter une référence** boîte de dialogue, cliquez sur le **.NET** onglet, maintenez la touche CTRL enfoncée, sélectionnez les assemblys suivants, puis cliquez sur **OK**:</span><span class="sxs-lookup"><span data-stu-id="988ef-116">In the **Add Reference** dialog box, click the **.NET** tab, hold down the CTRL key, select the following assemblies, and then click **OK**:</span></span>  
  
    -   <span data-ttu-id="988ef-117">System.Activities</span><span class="sxs-lookup"><span data-stu-id="988ef-117">System.Activities</span></span>  
  
    -   <span data-ttu-id="988ef-118">System.Activities.Presentation</span><span class="sxs-lookup"><span data-stu-id="988ef-118">System.Activities.Presentation</span></span>  
  
    -   <span data-ttu-id="988ef-119">System.Activities.Core.Presentation</span><span class="sxs-lookup"><span data-stu-id="988ef-119">System.Activities.Core.Presentation</span></span>  
  
10. <span data-ttu-id="988ef-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="988ef-120">Click **OK**.</span></span>  
  
11. <span data-ttu-id="988ef-121">Consultez [tâche 2 : Héberger le Concepteur de flux de travail](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md) pour apprendre à héberger la zone de conception du Concepteur de workflow.</span><span class="sxs-lookup"><span data-stu-id="988ef-121">See [Task 2: Host the Workflow Designer](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md) to learn how to host the workflow designer design canvas.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="988ef-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="988ef-122">See also</span></span>
- [<span data-ttu-id="988ef-123">Réhébergement du concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="988ef-123">Rehosting the Workflow Designer</span></span>](../../../docs/framework/windows-workflow-foundation/rehosting-the-workflow-designer.md)
- [<span data-ttu-id="988ef-124">Tâche 2 : Héberger le Concepteur de flux de travail</span><span class="sxs-lookup"><span data-stu-id="988ef-124">Task 2: Host the Workflow Designer</span></span>](../../../docs/framework/windows-workflow-foundation/task-2-host-the-workflow-designer.md)
