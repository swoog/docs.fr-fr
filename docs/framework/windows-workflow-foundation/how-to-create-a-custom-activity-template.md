---
title: 'Procédure : créer un modèle d’activité personnalisé'
ms.date: 03/30/2017
ms.assetid: 6760a5cc-6eb8-465f-b4fa-f89b39539429
ms.openlocfilehash: ee6f249092c5cf8643e3c9bfd15d32e77791d8bb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59295846"
---
# <a name="how-to-create-a-custom-activity-template"></a><span data-ttu-id="7303b-102">Procédure : créer un modèle d’activité personnalisé</span><span class="sxs-lookup"><span data-stu-id="7303b-102">How to: Create a Custom Activity Template</span></span>

<span data-ttu-id="7303b-103">Les modèles d'activité personnalisés sont utilisés pour personnaliser la configuration des activités, parmi lesquelles les activités composites personnalisées, afin que les utilisateurs n'aient pas besoin de créer individuellement chaque activité et de configurer manuellement leurs propriétés et les autres paramètres.</span><span class="sxs-lookup"><span data-stu-id="7303b-103">Custom activity templates are used to customize the configuration of activities, including custom composite activities, so that users do not have to create each activity individually and configure their properties and other settings manually.</span></span> <span data-ttu-id="7303b-104">Ces modèles personnalisés peuvent être rendus disponibles dans le **boîte à outils** sur la [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] ou à partir d’un concepteur réhébergé, à partir de laquelle les utilisateurs peuvent les faire glisser sur l’aire de conception préconfigurée.</span><span class="sxs-lookup"><span data-stu-id="7303b-104">These custom templates can be made available in the **Toolbox** on the [!INCLUDE[wfd1](../../../includes/wfd1-md.md)] or from a rehosted designer, from which users can drag them onto the preconfigured design surface.</span></span> [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] <span data-ttu-id="7303b-105">est fourni avec de bons exemples de ces modèles : le [Concepteur de modèles SendAndReceiveReply](/visualstudio/workflow-designer/sendandreceivereply-template-designer) et [Concepteur de modèles ReceiveAndSendReply](/visualstudio/workflow-designer/receiveandsendreply-template-designer) dans le [concepteurs d’activités de messagerie](/visualstudio/workflow-designer/messaging-activity-designers) catégorie.</span><span class="sxs-lookup"><span data-stu-id="7303b-105">ships with good examples of such templates: the [SendAndReceiveReply Template Designer](/visualstudio/workflow-designer/sendandreceivereply-template-designer) and the [ReceiveAndSendReply Template Designer](/visualstudio/workflow-designer/receiveandsendreply-template-designer) in the [Messaging Activity Designers](/visualstudio/workflow-designer/messaging-activity-designers) category.</span></span>

 <span data-ttu-id="7303b-106">La première procédure de cette rubrique décrit comment créer un modèle d’activité personnalisée pour un **délai** activité et la seconde procédure explique brièvement comment rendre disponible dans un [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] pour vérifier que le modèle personnalisé fonctionne.</span><span class="sxs-lookup"><span data-stu-id="7303b-106">The first procedure in this topic describes how to create a custom activity template for a **Delay** activity and the second procedure describes briefly how to make it available in a [!INCLUDE[wfd2](../../../includes/wfd2-md.md)] to verify that the custom template works.</span></span>

 <span data-ttu-id="7303b-107">Les modèles d'activité personnalisés doivent implémenter l'<xref:System.Activities.Presentation.IActivityTemplateFactory>.</span><span class="sxs-lookup"><span data-stu-id="7303b-107">Custom activity templates must implement the <xref:System.Activities.Presentation.IActivityTemplateFactory>.</span></span> <span data-ttu-id="7303b-108">L'interface dispose d'une seule méthode <xref:System.Activities.Presentation.IActivityTemplateFactory.Create%2A> avec laquelle vous pouvez créer et configurer les instances d'activité utilisées dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="7303b-108">The interface has a single <xref:System.Activities.Presentation.IActivityTemplateFactory.Create%2A> method with which you can create and configure the activity instances used in the template.</span></span>

## <a name="to-create-a-template-for-the-delay-activity"></a><span data-ttu-id="7303b-109">Pour créer un modèle pour l'activité Delay</span><span class="sxs-lookup"><span data-stu-id="7303b-109">To create a template for the Delay activity</span></span>

1. <span data-ttu-id="7303b-110">Démarrez Visual Studio 2010.</span><span class="sxs-lookup"><span data-stu-id="7303b-110">Start Visual Studio 2010.</span></span>

2. <span data-ttu-id="7303b-111">Dans le menu **Fichier**, pointez sur **Nouveau**, puis sélectionnez **Projet**.</span><span class="sxs-lookup"><span data-stu-id="7303b-111">On the **File** menu, point to **New**, and then select **Project**.</span></span>

     <span data-ttu-id="7303b-112">La boîte de dialogue **Nouveau projet** s'affiche.</span><span class="sxs-lookup"><span data-stu-id="7303b-112">The **New Project** dialog box opens.</span></span>

3. <span data-ttu-id="7303b-113">Dans le **Types de projets** volet, sélectionnez **Workflow** à partir de le le **Visual C#** projets ou **Visual Basic** regroupements en fonction de votre langue de préférence.</span><span class="sxs-lookup"><span data-stu-id="7303b-113">In the **Project Types** pane, select **Workflow** from either the **Visual C#** projects or **Visual Basic** groupings depending on your language preference.</span></span>

4. <span data-ttu-id="7303b-114">Dans le **modèles** volet, sélectionnez **bibliothèque d’activités**.</span><span class="sxs-lookup"><span data-stu-id="7303b-114">In the **Templates** pane, select **Activity Library**.</span></span>

5. <span data-ttu-id="7303b-115">Dans le **nom** , entrez `DelayActivityTemplate`.</span><span class="sxs-lookup"><span data-stu-id="7303b-115">In the **Name** box, enter `DelayActivityTemplate`.</span></span>

6. <span data-ttu-id="7303b-116">Acceptez les valeurs par défaut dans le **emplacement** et **nom de la Solution** zones de texte, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7303b-116">Accept the defaults in the **Location** and **Solution name** text boxes, and then click **OK**.</span></span>

7. <span data-ttu-id="7303b-117">Cliquez sur le répertoire References du projet DelayActivityTemplate dans **l’Explorateur de solutions** et choisissez **ajouter une référence** pour ouvrir le **ajouter une référence** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7303b-117">Right-click the References directory of the DelayActivityTemplate project in **Solution Explorer** and choose **Add Reference** to open the **Add Reference** dialog box.</span></span>

8. <span data-ttu-id="7303b-118">Accédez à la **.NET** onglet et sélectionnez **PresentationFramework** à partir de la **nom du composant** colonne sur la gauche, puis sur **OK** pour ajouter une référence dans le fichier PresentationFramework.dll.</span><span class="sxs-lookup"><span data-stu-id="7303b-118">Go to the **.NET** tab and select **PresentationFramework** from the **Component Name** column on the left and click **OK** to add a reference to the PresentationFramework.dll file.</span></span>

9. <span data-ttu-id="7303b-119">Répétez cette procédure pour ajouter des références aux fichiers System.Activities.Presentation.dll et WindowsBase.dll.</span><span class="sxs-lookup"><span data-stu-id="7303b-119">Repeat this procedure to add references to the System.Activities.Presentation.dll and the WindowsBase.dll files.</span></span>

10. <span data-ttu-id="7303b-120">Cliquez sur le projet DelayActivityTemplate dans **l’Explorateur de solutions** et choisissez **ajouter** , puis **un nouvel élément** pour ouvrir le **ajouter un nouvel élément**boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7303b-120">Right-click the DelayActivityTemplate project in **Solution Explorer** and choose **Add** and then **New Item** to open the **Add New Item** dialog box.</span></span>

11. <span data-ttu-id="7303b-121">Sélectionnez le **classe** modèle, nommez-le MyDelayTemplate, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7303b-121">Select the **Class** template, name it MyDelayTemplate, and then click **OK**.</span></span>

12. <span data-ttu-id="7303b-122">Ouvrez le fichier MyDelayTemplate.cs et ajoutez les instructions suivantes.</span><span class="sxs-lookup"><span data-stu-id="7303b-122">Open the MyDelayTemplate.cs file and add the following statements.</span></span>

    ```
    //Namespaces added
    using System.Activities;
    using System.Activities.Statements;
    using System.Activities.Presentation;
    using System.Windows;
    ```

13. <span data-ttu-id="7303b-123">Implémentez <xref:System.Activities.Presentation.IActivityTemplateFactory> avec la classe `MyDelayActivity` dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7303b-123">Implement the <xref:System.Activities.Presentation.IActivityTemplateFactory> with the `MyDelayActivity` class with the following code.</span></span> <span data-ttu-id="7303b-124">Cela configure une durée de 10 secondes comme délai.</span><span class="sxs-lookup"><span data-stu-id="7303b-124">This configures the delay to have a duration of 10 seconds.</span></span>

    ```
    public sealed class MyDelayActivity : IActivityTemplateFactory
    {
        public Activity Create(System.Windows.DependencyObject target)
        {
            return new System.Activities.Statements.Delay
            {
                DisplayName = "DelayActivityTemplate",
                Duration = new TimeSpan(0, 0, 10)

            };
        }
    }
    ```

14. <span data-ttu-id="7303b-125">Sélectionnez **générer la Solution** à partir de la **Build** menu pour générer le fichier DelayActivityTemplate.dll.</span><span class="sxs-lookup"><span data-stu-id="7303b-125">Select **Build Solution** from the **Build** menu to generate the DelayActivityTemplate.dll file.</span></span>

### <a name="to-make-the-template-available-in-a-workflow-designer"></a><span data-ttu-id="7303b-126">Pour rendre le modèle disponible dans un concepteur de workflow</span><span class="sxs-lookup"><span data-stu-id="7303b-126">To make the template available in a Workflow Designer</span></span>

1. <span data-ttu-id="7303b-127">Avec le bouton droit de la solution DelayActivityTemplate dans **l’Explorateur de solutions** et choisissez **ajouter** , puis **nouveau projet** pour ouvrir le **ajouter un nouveau projet** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="7303b-127">Right-click the DelayActivityTemplate solution in **Solution Explorer** and choose **Add** and then **New Project** to open the **Add New Project** dialog box.</span></span>

2. <span data-ttu-id="7303b-128">Sélectionnez le **Application Console de Workflow** modèle, nommez-le `CustomActivityTemplateApp`, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7303b-128">Select the **Workflow Console Application** template, name it `CustomActivityTemplateApp`, and then click **OK**.</span></span>

3. <span data-ttu-id="7303b-129">Cliquez sur le répertoire References du projet CustomActivityTemplateApp dans **l’Explorateur de solutions** et choisissez **ajouter une référence** pour ouvrir le **ajouter une référence** boîte de dialogue zone.</span><span class="sxs-lookup"><span data-stu-id="7303b-129">Right-click the References directory of the CustomActivityTemplateApp project in **Solution Explorer** and choose **Add Reference** to open the **Add Reference** dialog box.</span></span>

4. <span data-ttu-id="7303b-130">Accédez à la **projets** onglet et sélectionnez **DelayActivityTemplate** à partir de la **nom_projet** colonne sur la gauche, puis sur **OK** pour ajouter un faire référence au fichier DelayActivityTemplate.dll que vous avez créé dans la première procédure.</span><span class="sxs-lookup"><span data-stu-id="7303b-130">Go to the **Projects** tab and select **DelayActivityTemplate** from the **Project Name** column on the left and click **OK** to add a reference to the DelayActivityTemplate.dll file that you created in the first procedure.</span></span>

5. <span data-ttu-id="7303b-131">Cliquez sur le projet CustomActivityTemplateApp dans **l’Explorateur de solutions** et choisissez **Build** pour compiler l’application.</span><span class="sxs-lookup"><span data-stu-id="7303b-131">Right-click the CustomActivityTemplateApp project in **Solution Explorer** and choose **Build** to compile the application.</span></span>

6. <span data-ttu-id="7303b-132">Cliquez sur le projet CustomActivityTemplateApp dans **l’Explorateur de solutions** et choisissez **définir comme projet de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="7303b-132">Right-click the CustomActivityTemplateApp project in **Solution Explorer** and choose **Set as Startup Project**.</span></span>

7. <span data-ttu-id="7303b-133">Sélectionnez **démarrer sans débogage** à partir de la **déboguer** menu, puis appuyez sur une touche pour continuer lorsque vous êtes invité à partir de la fenêtre cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="7303b-133">Select **Start Without Debugging** from the **Debug** menu and press any key to continue when prompted from the cmd.exe window.</span></span>

8. <span data-ttu-id="7303b-134">Ouvrez le fichier Workflow1.xaml et ouvrez le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="7303b-134">Open the Workflow1.xaml file and open the **Toolbox**.</span></span>

9. <span data-ttu-id="7303b-135">Recherchez le **MyDelayActivity** modèle dans le **DelayActivityTemplate** catégorie.</span><span class="sxs-lookup"><span data-stu-id="7303b-135">Locate the **MyDelayActivity** template in the **DelayActivityTemplate** category.</span></span> <span data-ttu-id="7303b-136">Faites-le glisser vers l'aire de conception.</span><span class="sxs-lookup"><span data-stu-id="7303b-136">Drag it onto the design surface.</span></span> <span data-ttu-id="7303b-137">Vérifiez dans le **propriétés** fenêtre qui le `Duration` propriété a été définie sur 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="7303b-137">Confirm in the **Properties** window that the `Duration` property has been set to 10 seconds.</span></span>

## <a name="example"></a><span data-ttu-id="7303b-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="7303b-138">Example</span></span>
 <span data-ttu-id="7303b-139">Le fichier MyDelayActivity.cs doit contenir le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7303b-139">The MyDelayActivity.cs file should contain the following code.</span></span>

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

//Namespaces added
using System.Activities;
using System.Activities.Statements;
using System.Activities.Presentation;
using System.Windows;

namespace DelayActivityTemplate
{
    public sealed class MyDelayActivity : IActivityTemplateFactory
    {
        public Activity Create(System.Windows.DependencyObject target)
        {
            return new System.Activities.Statements.Delay
            {
                DisplayName = "DelayActivityTemplate",
                Duration = new TimeSpan(0, 0, 10)

            };
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7303b-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7303b-140">See also</span></span>

- <xref:System.Activities.Presentation.IActivityTemplateFactory>
- [<span data-ttu-id="7303b-141">Personnalisation de l’expérience de conception de workflow</span><span class="sxs-lookup"><span data-stu-id="7303b-141">Customizing the Workflow Design Experience</span></span>](customizing-the-workflow-design-experience.md)