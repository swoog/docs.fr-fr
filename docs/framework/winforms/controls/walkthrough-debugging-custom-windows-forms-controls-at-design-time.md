---
title: 'Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- debugging [Visual Studio], walkthroughs
- custom controls [Windows Forms], walkthroughs
- visual editors
- debugging [Visual Studio], Windows Forms
- custom controls [Windows Forms], debugging
- designers
- controls [Windows Forms], debugging
- walkthroughs [Windows Forms], debugging
- design-time debugging
ms.assetid: 1fd83ccd-3798-42fc-85a3-6cba99467387
ms.openlocfilehash: b5c54acc89317104eddc3b1f5b350edcb263d208
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213687"
---
# <a name="walkthrough-debugging-custom-windows-forms-controls-at-design-time"></a><span data-ttu-id="73a2f-102">Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design</span><span class="sxs-lookup"><span data-stu-id="73a2f-102">Walkthrough: Debugging Custom Windows Forms Controls at Design Time</span></span>
<span data-ttu-id="73a2f-103">Lorsque vous créez un contrôle personnalisé, vous trouverez souvent il nécessaires pour déboguer son comportement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="73a2f-103">When you create a custom control, you will often find it necessary to debug its design-time behavior.</span></span> <span data-ttu-id="73a2f-104">Cela est particulièrement vrai si vous créez un concepteur personnalisé pour votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-104">This is especially true if you are authoring a custom designer for your custom control.</span></span> <span data-ttu-id="73a2f-105">Pour plus d’informations, consultez [procédure pas à pas : Création d’un Windows Forms de contrôle qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md).</span><span class="sxs-lookup"><span data-stu-id="73a2f-105">For details, see [Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features](creating-a-wf-control-design-time-features.md).</span></span>  
  
 <span data-ttu-id="73a2f-106">Vous pouvez déboguer vos contrôles personnalisés à l’aide de Visual Studio, simplement comme pour toutes les autres classes .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="73a2f-106">You can debug your custom controls using Visual Studio, just as you would debug any other .NET Framework classes.</span></span> <span data-ttu-id="73a2f-107">La différence est que vous devez déboguer une instance distincte de Visual Studio qui exécute le code de votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="73a2f-107">The difference is that you will debug a separate instance of Visual Studio that is running your custom control's code</span></span>  
  
 <span data-ttu-id="73a2f-108">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="73a2f-108">Tasks illustrated in this walkthrough include:</span></span>  
  
-   <span data-ttu-id="73a2f-109">Création d’un projet Windows Forms pour héberger votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="73a2f-109">Creating a Windows Forms project to host your custom control</span></span>  
  
-   <span data-ttu-id="73a2f-110">Création d’un projet de bibliothèque de contrôle</span><span class="sxs-lookup"><span data-stu-id="73a2f-110">Creating a control library project</span></span>  
  
-   <span data-ttu-id="73a2f-111">Ajout d’une propriété à votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="73a2f-111">Adding a property to your custom control</span></span>  
  
-   <span data-ttu-id="73a2f-112">Ajout de votre contrôle personnalisé au formulaire hôte</span><span class="sxs-lookup"><span data-stu-id="73a2f-112">Adding your custom control to the host form</span></span>  
  
-   <span data-ttu-id="73a2f-113">Configuration du projet pour le débogage au moment du design</span><span class="sxs-lookup"><span data-stu-id="73a2f-113">Setting up the project for design-time debugging</span></span>  
  
-   <span data-ttu-id="73a2f-114">Débogage de votre contrôle personnalisé au moment du design</span><span class="sxs-lookup"><span data-stu-id="73a2f-114">Debugging your custom control at design time</span></span>  
  
 <span data-ttu-id="73a2f-115">Lorsque vous avez terminé, vous devez comprendre les tâches nécessaires pour déboguer le comportement au moment du design d’un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-115">When you are finished, you will have an understanding of the tasks necessary for debugging the design-time behavior of a custom control.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="73a2f-116">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="73a2f-116">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="73a2f-117">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="73a2f-117">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="73a2f-118">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="73a2f-118">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="73a2f-119">Création du projet</span><span class="sxs-lookup"><span data-stu-id="73a2f-119">Creating the Project</span></span>  
 <span data-ttu-id="73a2f-120">La première étape consiste à créer le projet d’application.</span><span class="sxs-lookup"><span data-stu-id="73a2f-120">The first step is to create the application project.</span></span> <span data-ttu-id="73a2f-121">Vous utiliserez ce projet pour générer l’application qui héberge le contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-121">You will use this project to build the application that hosts the custom control.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="73a2f-122">Pour créer le projet</span><span class="sxs-lookup"><span data-stu-id="73a2f-122">To create the project</span></span>  
  
-   <span data-ttu-id="73a2f-123">Créer un projet d’Application de Windows appelé « DebuggingExample » (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="73a2f-123">Create a Windows Application project called "DebuggingExample" (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
## <a name="creating-a-control-library-project"></a><span data-ttu-id="73a2f-124">Création d’un projet de bibliothèque de contrôle</span><span class="sxs-lookup"><span data-stu-id="73a2f-124">Creating a Control Library Project</span></span>  
 <span data-ttu-id="73a2f-125">L’étape suivante consiste à créer le projet de bibliothèque de contrôle et de configurer le contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-125">The next step is to create the control library project and set up the custom control.</span></span>  
  
#### <a name="to-create-the-control-library-project"></a><span data-ttu-id="73a2f-126">Pour créer le projet de bibliothèque de contrôle</span><span class="sxs-lookup"><span data-stu-id="73a2f-126">To create the control library project</span></span>  
  
1.  <span data-ttu-id="73a2f-127">Ajouter un **bibliothèque de contrôles Windows** projet à la solution.</span><span class="sxs-lookup"><span data-stu-id="73a2f-127">Add a **Windows Control Library** project to the solution.</span></span>  
  
2.  <span data-ttu-id="73a2f-128">Ajouter un nouveau **UserControl** élément au projet DebugControlLibrary.</span><span class="sxs-lookup"><span data-stu-id="73a2f-128">Add a new **UserControl** item to the DebugControlLibrary project.</span></span> <span data-ttu-id="73a2f-129">Pour plus d’informations, consultez [Guide pratique pour Ajouter de nouveaux éléments de projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="73a2f-129">For details, see [How to: Add New Project Items](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span></span> <span data-ttu-id="73a2f-130">Nommez le nouveau fichier source une base « DebugControl ».</span><span class="sxs-lookup"><span data-stu-id="73a2f-130">Give the new source file a base name of "DebugControl".</span></span>  
  
3.  <span data-ttu-id="73a2f-131">À l’aide de la **l’Explorateur de solutions**, supprimer le contrôle du projet par défaut en supprimant le fichier de code avec un nom de base «`UserControl1`».</span><span class="sxs-lookup"><span data-stu-id="73a2f-131">Using the **Solution Explorer**, delete the project's default control by deleting the code file with a base name of "`UserControl1`".</span></span> <span data-ttu-id="73a2f-132">Pour plus d’informations, consultez [Guide pratique pour Supprimer, suppression et exclure des éléments](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="73a2f-132">For details, see [How to: Remove, Delete, and Exclude Items](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span></span>  
  
4.  <span data-ttu-id="73a2f-133">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="73a2f-133">Build the solution.</span></span>  
  
## <a name="checkpoint"></a><span data-ttu-id="73a2f-134">Point de contrôle</span><span class="sxs-lookup"><span data-stu-id="73a2f-134">Checkpoint</span></span>  
 <span data-ttu-id="73a2f-135">À ce stade, vous serez en mesure de voir votre contrôle personnalisé dans le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="73a2f-135">At this point, you will be able to see your custom control in the **Toolbox**.</span></span>  
  
#### <a name="to-check-your-progress"></a><span data-ttu-id="73a2f-136">Pour vérifier votre progression</span><span class="sxs-lookup"><span data-stu-id="73a2f-136">To check your progress</span></span>  
  
-   <span data-ttu-id="73a2f-137">Recherchez le nouvel onglet appelé **Composants DebugControlLibrary** et cliquez sur pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="73a2f-137">Find the new tab called **DebugControlLibrary Components** and click to select it.</span></span> <span data-ttu-id="73a2f-138">Quand il s’ouvre, vous verrez votre contrôle répertorié comme **DebugControl** avec l’icône par défaut en regard de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="73a2f-138">When it opens, you will see your control listed as **DebugControl** with the default icon beside it.</span></span>  
  
## <a name="adding-a-property-to-your-custom-control"></a><span data-ttu-id="73a2f-139">Ajout d’une propriété à votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="73a2f-139">Adding a Property to Your Custom Control</span></span>  
 <span data-ttu-id="73a2f-140">Pour montrer que le code de votre contrôle personnalisé s’exécute au moment du design, vous ajoutez une propriété et définissez un point d’arrêt dans le code qui implémente la propriété.</span><span class="sxs-lookup"><span data-stu-id="73a2f-140">To demonstrate that your custom control's code is running at design-time, you will add a property and set a breakpoint in the code that implements the property.</span></span>  
  
#### <a name="to-add-a-property-to-your-custom-control"></a><span data-ttu-id="73a2f-141">Pour ajouter une propriété à votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="73a2f-141">To add a property to your custom control</span></span>  
  
1.  <span data-ttu-id="73a2f-142">Ouvrez **DebugControl** dans le **éditeur de Code**.</span><span class="sxs-lookup"><span data-stu-id="73a2f-142">Open **DebugControl** in the **Code Editor**.</span></span> <span data-ttu-id="73a2f-143">Ajoutez le code suivant à la définition de classe :</span><span class="sxs-lookup"><span data-stu-id="73a2f-143">Add the following code to the class definition:</span></span>  
  
    ```vb  
    Private demoStringValue As String = Nothing  
    <BrowsableAttribute(true)>  
    Public Property DemoString() As String  
  
        Get  
            Return Me.demoStringValue  
        End Get  
  
        Set(ByVal value As String)  
            Me.demoStringValue = value  
        End Set  
  
    End Property  
    ```  
  
    ```csharp  
    private string demoStringValue = null;  
    [Browsable(true)]  
    public string DemoString  
    {  
        get  
        {  
            return this.demoStringValue;  
        }  
        set  
        {  
            demoStringValue = value;  
        }  
    }  
    ```  
  
2.  <span data-ttu-id="73a2f-144">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="73a2f-144">Build the solution.</span></span>  
  
## <a name="adding-your-custom-control-to-the-host-form"></a><span data-ttu-id="73a2f-145">Ajout de votre contrôle personnalisé au formulaire hôte</span><span class="sxs-lookup"><span data-stu-id="73a2f-145">Adding Your Custom Control to the Host Form</span></span>  
 <span data-ttu-id="73a2f-146">Pour déboguer le comportement au moment du design de votre contrôle personnalisé, vous devez placer une instance de la classe de contrôle personnalisé sur un formulaire hôte.</span><span class="sxs-lookup"><span data-stu-id="73a2f-146">To debug the design-time behavior of your custom control, you will place an instance of the custom control class on a host form.</span></span>  
  
#### <a name="to-add-your-custom-control-to-the-host-form"></a><span data-ttu-id="73a2f-147">Pour ajouter votre contrôle personnalisé au formulaire hôte</span><span class="sxs-lookup"><span data-stu-id="73a2f-147">To add your custom control to the host form</span></span>  
  
1.  <span data-ttu-id="73a2f-148">Dans le projet « DebuggingExample », ouvrez Form1 dans le **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="73a2f-148">In the "DebuggingExample" project, open Form1 in the **Windows Forms Designer**.</span></span>  
  
2.  <span data-ttu-id="73a2f-149">Dans le **boîte à outils**, ouvrez le **Composants DebugControlLibrary** onglet et faites glisser un **DebugControl** instance vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="73a2f-149">In the **Toolbox**, open the **DebugControlLibrary Components** tab and drag a **DebugControl** instance onto the form.</span></span>  
  
3.  <span data-ttu-id="73a2f-150">Rechercher la `DemoString` propriété personnalisée dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="73a2f-150">Find the `DemoString` custom property in the **Properties** window.</span></span> <span data-ttu-id="73a2f-151">Notez que vous pouvez modifier sa valeur comme vous le feriez pour toute autre propriété.</span><span class="sxs-lookup"><span data-stu-id="73a2f-151">Note that you can change its value as you would any other property.</span></span> <span data-ttu-id="73a2f-152">Notez également que lorsque la `DemoString` propriété est sélectionnée, la chaîne de la propriété description s’affiche en bas de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="73a2f-152">Also note that when the `DemoString` property is selected, the property's description string appears at the bottom of the **Properties** window.</span></span>  
  
## <a name="setting-up-the-project-for-design-time-debugging"></a><span data-ttu-id="73a2f-153">Configuration du projet pour le débogage au moment du Design</span><span class="sxs-lookup"><span data-stu-id="73a2f-153">Setting Up the Project for Design-Time Debugging</span></span>  
 <span data-ttu-id="73a2f-154">Pour déboguer le comportement au moment du design de votre contrôle personnalisé, vous allez déboguer une instance distincte de Visual Studio qui exécute le code de votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-154">To debug your custom control's design-time behavior, you will debug a separate instance of Visual Studio that is running your custom control's code.</span></span>  
  
#### <a name="to-set-up-the-project-for-design-time-debugging"></a><span data-ttu-id="73a2f-155">Pour configurer le projet pour le débogage au moment du design</span><span class="sxs-lookup"><span data-stu-id="73a2f-155">To set up the project for design-time debugging</span></span>  
  
1.  <span data-ttu-id="73a2f-156">Avec le bouton droit sur le **DebugControlLibrary** de projet dans le **l’Explorateur de solutions** et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="73a2f-156">Right-click on the **DebugControlLibrary** project in the **Solution Explorer** and select **Properties**.</span></span>  
  
2.  <span data-ttu-id="73a2f-157">Dans le **DebugControlLibrary** feuille de propriétés, sélectionnez le **déboguer** onglet.</span><span class="sxs-lookup"><span data-stu-id="73a2f-157">In the **DebugControlLibrary** property sheet, select the **Debug** tab.</span></span>  
  
     <span data-ttu-id="73a2f-158">Dans le **Action de démarrage** section, sélectionnez **démarrer le programme externe**.</span><span class="sxs-lookup"><span data-stu-id="73a2f-158">In the **Start Action** section, select **Start external program**.</span></span> <span data-ttu-id="73a2f-159">Vous serez le débogage d’une instance distincte de Visual Studio, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) pour le rechercher l’IDE Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73a2f-159">You will be debugging a separate instance of Visual Studio, so click the ellipsis (![VisualStudioEllipsesButton screenshot](../media/vbellipsesbutton.png "vbEllipsesButton")) button to browse for the Visual Studio IDE.</span></span> <span data-ttu-id="73a2f-160">Le nom du fichier exécutable est **devenv.exe**, et si vous avez installé à l’emplacement par défaut, son chemin d’accès est %programfiles%\Microsoft Visual Studio 9.0\Common7\IDE\devenv.exe.</span><span class="sxs-lookup"><span data-stu-id="73a2f-160">The name of the executable file is **devenv.exe**, and if you installed to the default location, its path is %programfiles%\Microsoft Visual Studio 9.0\Common7\IDE\devenv.exe.</span></span>  
  
3.  <span data-ttu-id="73a2f-161">Cliquez sur **OK** pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="73a2f-161">Click **OK** to close the dialog box.</span></span>  
  
4.  <span data-ttu-id="73a2f-162">Avec le bouton droit le **DebugControlLibrary** de projet et sélectionnez **définir comme projet de démarrage** pour activer cette configuration de débogage.</span><span class="sxs-lookup"><span data-stu-id="73a2f-162">Right-click the **DebugControlLibrary** project and select **Set as StartUp Project** to enable this debugging configuration.</span></span>  
  
## <a name="debugging-your-custom-control-at-design-time"></a><span data-ttu-id="73a2f-163">Débogage de votre contrôle personnalisé au moment du Design</span><span class="sxs-lookup"><span data-stu-id="73a2f-163">Debugging Your Custom Control at Design Time</span></span>  
 <span data-ttu-id="73a2f-164">Vous êtes maintenant prêt à déboguer votre contrôle personnalisé en cours d’exécution en mode Création.</span><span class="sxs-lookup"><span data-stu-id="73a2f-164">Now you are ready to debug your custom control as it runs in design mode.</span></span> <span data-ttu-id="73a2f-165">Lorsque vous démarrez la session de débogage, une nouvelle instance de Visual Studio sera créée, et vous allez l’utiliser pour charger la solution « DebuggingExample ».</span><span class="sxs-lookup"><span data-stu-id="73a2f-165">When you start the debugging session, a new instance of Visual Studio will be created, and you will use it to load the "DebuggingExample" solution.</span></span> <span data-ttu-id="73a2f-166">Lorsque vous ouvrez Form1 dans le **Concepteur Forms**, une instance de votre contrôle personnalisé est créée et commence à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="73a2f-166">When you open Form1 in the **Forms Designer**, an instance of your custom control will be created and will start running.</span></span>  
  
#### <a name="to-debug-your-custom-control-at-design-time"></a><span data-ttu-id="73a2f-167">Pour déboguer votre contrôle personnalisé au moment du design</span><span class="sxs-lookup"><span data-stu-id="73a2f-167">To debug your custom control at design time</span></span>  
  
1.  <span data-ttu-id="73a2f-168">Ouvrir le **DebugControl** fichier source dans le **éditeur de Code** et placer un point d’arrêt sur la `Set` l’accesseur de la `DemoString` propriété.</span><span class="sxs-lookup"><span data-stu-id="73a2f-168">Open the **DebugControl** source file in the **Code Editor** and place a breakpoint on the `Set` accessor of the `DemoString` property.</span></span>  
  
2.  <span data-ttu-id="73a2f-169">Appuyez sur F5 pour démarrer la session de débogage.</span><span class="sxs-lookup"><span data-stu-id="73a2f-169">Press F5 to start the debugging session.</span></span> <span data-ttu-id="73a2f-170">Notez qu’une nouvelle instance de Visual Studio est créée.</span><span class="sxs-lookup"><span data-stu-id="73a2f-170">Note that a new instance of Visual Studio is created.</span></span> <span data-ttu-id="73a2f-171">Vous pouvez faire la distinction entre les instances de deux manières :</span><span class="sxs-lookup"><span data-stu-id="73a2f-171">You can distinguish between the instances in two ways:</span></span>  
  
    -   <span data-ttu-id="73a2f-172">L’instance de débogage a le mot **en cours d’exécution** dans sa barre de titre</span><span class="sxs-lookup"><span data-stu-id="73a2f-172">The debugging instance has the word **Running** in its title bar</span></span>  
  
    -   <span data-ttu-id="73a2f-173">L’instance de débogage a le **Démarrer** bouton sur son **déboguer** barre d’outils désactivé</span><span class="sxs-lookup"><span data-stu-id="73a2f-173">The debugging instance has the **Start** button on its **Debug** toolbar disabled</span></span>  
  
     <span data-ttu-id="73a2f-174">Votre point d’arrêt est défini dans l’instance de débogage.</span><span class="sxs-lookup"><span data-stu-id="73a2f-174">Your breakpoint is set in the debugging instance.</span></span>  
  
3.  <span data-ttu-id="73a2f-175">Dans la nouvelle instance de Visual Studio, ouvrez la solution « DebuggingExample ».</span><span class="sxs-lookup"><span data-stu-id="73a2f-175">In the new instance of Visual Studio, open the "DebuggingExample" solution.</span></span> <span data-ttu-id="73a2f-176">Vous pouvez facilement trouver la solution en sélectionnant **projets récents** à partir de la **fichier** menu.</span><span class="sxs-lookup"><span data-stu-id="73a2f-176">You can easily find the solution by selecting **Recent Projects** from the **File** menu.</span></span> <span data-ttu-id="73a2f-177">Le fichier de solution « DebuggingExample.sln » apparaît comme étant le dernier fichier utilisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-177">The "DebuggingExample.sln" solution file will be listed as the most recently used file.</span></span>  
  
4.  <span data-ttu-id="73a2f-178">Ouvrez Form1 dans le **Concepteur Forms** et sélectionnez le **DebugControl** contrôle.</span><span class="sxs-lookup"><span data-stu-id="73a2f-178">Open Form1 in the **Forms Designer** and select the **DebugControl** control.</span></span>  
  
5.  <span data-ttu-id="73a2f-179">Modifiez la valeur de la propriété `DemoString` .</span><span class="sxs-lookup"><span data-stu-id="73a2f-179">Change the value of the `DemoString` property.</span></span> <span data-ttu-id="73a2f-180">Notez que lorsque vous validez la modification, l’instance de débogage de Visual Studio acquiert le focus et l’exécution s’arrête au point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="73a2f-180">Note that when you commit the change, the debugging instance of Visual Studio acquires focus and execution stops at your breakpoint.</span></span> <span data-ttu-id="73a2f-181">Vous pouvez pas dans l’accesseur de propriété comme votre serait tout autre code.</span><span class="sxs-lookup"><span data-stu-id="73a2f-181">You can single-step through the property accessor just as your would any other code.</span></span>  
  
6.  <span data-ttu-id="73a2f-182">Lorsque vous avez terminé de votre session de débogage, vous pouvez quitter en fermant l’instance hébergée de Visual Studio ou en cliquant sur le **arrêter le débogage** bouton dans l’instance de débogage.</span><span class="sxs-lookup"><span data-stu-id="73a2f-182">When you are finished with your debugging session, you can exit by dismissing the hosted instance of Visual Studio or by clicking the **Stop Debugging** button in the debugging instance.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="73a2f-183">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="73a2f-183">Next Steps</span></span>  
 <span data-ttu-id="73a2f-184">Maintenant que vous pouvez déboguer vos contrôles personnalisés au moment du design, il existe de nombreuses possibilités pour le développement d’interaction de votre contrôle avec l’IDE Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73a2f-184">Now that you can debug your custom controls at design time, there are many possibilities for expanding your control's interaction with the Visual Studio IDE.</span></span>  
  
-   <span data-ttu-id="73a2f-185">Vous pouvez utiliser la <xref:System.ComponentModel.Component.DesignMode%2A> propriété de la <xref:System.ComponentModel.Component> classe pour écrire du code qui s’exécutera seulement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="73a2f-185">You can use the <xref:System.ComponentModel.Component.DesignMode%2A> property of the <xref:System.ComponentModel.Component> class to write code that will only execute at design time.</span></span> <span data-ttu-id="73a2f-186">Pour plus d'informations, consultez <xref:System.ComponentModel.Component.DesignMode%2A>.</span><span class="sxs-lookup"><span data-stu-id="73a2f-186">For details, see <xref:System.ComponentModel.Component.DesignMode%2A>.</span></span>  
  
-   <span data-ttu-id="73a2f-187">Il existe plusieurs attributs que vous pouvez appliquer aux propriétés de votre contrôle pour manipuler l’interaction de votre contrôle personnalisé avec le concepteur.</span><span class="sxs-lookup"><span data-stu-id="73a2f-187">There are several attributes you can apply to your control's properties to manipulate your custom control's interaction with the designer.</span></span> <span data-ttu-id="73a2f-188">Vous pouvez trouver ces attributs dans le <xref:System.ComponentModel?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="73a2f-188">You can find these attributes in the <xref:System.ComponentModel?displayProperty=nameWithType> namespace.</span></span>  
  
-   <span data-ttu-id="73a2f-189">Vous pouvez écrire un concepteur personnalisé pour votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="73a2f-189">You can write a custom designer for your custom control.</span></span> <span data-ttu-id="73a2f-190">Cela vous donne un contrôle complet sur l’expérience de conception à l’aide de l’infrastructure du concepteur extensible exposée par Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="73a2f-190">This gives you complete control over the design experience using the extensible designer infrastructure exposed by Visual Studio.</span></span> <span data-ttu-id="73a2f-191">Pour plus d’informations, consultez [procédure pas à pas : Création d’un Windows Forms de contrôle qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md).</span><span class="sxs-lookup"><span data-stu-id="73a2f-191">For details, see [Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features](creating-a-wf-control-design-time-features.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73a2f-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73a2f-192">See also</span></span>

- [<span data-ttu-id="73a2f-193">Procédure pas à pas : création d’un contrôle Windows Forms qui tire parti des fonctionnalités au moment du design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="73a2f-193">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)
- [<span data-ttu-id="73a2f-194">Procédure : Services d’accès au moment du Design</span><span class="sxs-lookup"><span data-stu-id="73a2f-194">How to: Access Design-Time Services</span></span>](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171822(v=vs.120))
- [<span data-ttu-id="73a2f-195">Procédure : Prise en charge d’accès au moment du Design dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="73a2f-195">How to: Access Design-Time Support in Windows Forms</span></span>](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171827(v=vs.120))
