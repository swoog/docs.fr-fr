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
ms.openlocfilehash: 39adcbd6d915f8b086df7e425efbe08ae8680a45
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882461"
---
# <a name="walkthrough-debugging-custom-windows-forms-controls-at-design-time"></a><span data-ttu-id="0edbf-102">Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design</span><span class="sxs-lookup"><span data-stu-id="0edbf-102">Walkthrough: Debugging Custom Windows Forms Controls at Design Time</span></span>

<span data-ttu-id="0edbf-103">Lorsque vous créez un contrôle personnalisé, vous trouverez souvent il nécessaires pour déboguer son comportement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="0edbf-103">When you create a custom control, you will often find it necessary to debug its design-time behavior.</span></span> <span data-ttu-id="0edbf-104">Cela est particulièrement vrai si vous créez un concepteur personnalisé pour votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edbf-104">This is especially true if you are authoring a custom designer for your custom control.</span></span> <span data-ttu-id="0edbf-105">Pour plus d’informations, consultez [procédure pas à pas : Création d’un Windows Forms de contrôle qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md).</span><span class="sxs-lookup"><span data-stu-id="0edbf-105">For details, see [Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features](creating-a-wf-control-design-time-features.md).</span></span>

<span data-ttu-id="0edbf-106">Vous pouvez déboguer vos contrôles personnalisés à l’aide de Visual Studio, simplement comme pour toutes les autres classes .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="0edbf-106">You can debug your custom controls using Visual Studio, just as you would debug any other .NET Framework classes.</span></span> <span data-ttu-id="0edbf-107">La différence est que vous devez déboguer une instance distincte de Visual Studio qui exécute le code de votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="0edbf-107">The difference is that you will debug a separate instance of Visual Studio that is running your custom control's code</span></span>

<span data-ttu-id="0edbf-108">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="0edbf-108">Tasks illustrated in this walkthrough include:</span></span>

- <span data-ttu-id="0edbf-109">Création d’un projet Windows Forms pour héberger votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="0edbf-109">Creating a Windows Forms project to host your custom control</span></span>

- <span data-ttu-id="0edbf-110">Création d’un projet de bibliothèque de contrôle</span><span class="sxs-lookup"><span data-stu-id="0edbf-110">Creating a control library project</span></span>

- <span data-ttu-id="0edbf-111">Ajout d’une propriété à votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="0edbf-111">Adding a property to your custom control</span></span>

- <span data-ttu-id="0edbf-112">Ajout de votre contrôle personnalisé au formulaire hôte</span><span class="sxs-lookup"><span data-stu-id="0edbf-112">Adding your custom control to the host form</span></span>

- <span data-ttu-id="0edbf-113">Configuration du projet pour le débogage au moment du design</span><span class="sxs-lookup"><span data-stu-id="0edbf-113">Setting up the project for design-time debugging</span></span>

- <span data-ttu-id="0edbf-114">Débogage de votre contrôle personnalisé au moment du design</span><span class="sxs-lookup"><span data-stu-id="0edbf-114">Debugging your custom control at design time</span></span>

<span data-ttu-id="0edbf-115">Lorsque vous avez terminé, vous devez comprendre les tâches nécessaires pour déboguer le comportement au moment du design d’un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edbf-115">When you are finished, you will have an understanding of the tasks necessary for debugging the design-time behavior of a custom control.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="0edbf-116">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="0edbf-116">Create the project</span></span>

<span data-ttu-id="0edbf-117">La première étape consiste à créer le projet d’application.</span><span class="sxs-lookup"><span data-stu-id="0edbf-117">The first step is to create the application project.</span></span> <span data-ttu-id="0edbf-118">Vous utiliserez ce projet pour générer l’application qui héberge le contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edbf-118">You will use this project to build the application that hosts the custom control.</span></span>

<span data-ttu-id="0edbf-119">Dans Visual Studio, créez un projet d’Application de Windows appelé « DebuggingExample » (**fichier** > **New** > **projet**  >  **Visual C#**  ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="0edbf-119">In Visual Studio, create a Windows Application project called "DebuggingExample" (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

## <a name="create-the-control-library-project"></a><span data-ttu-id="0edbf-120">Créer le projet de bibliothèque de contrôles</span><span class="sxs-lookup"><span data-stu-id="0edbf-120">Create the control library project</span></span>

1. <span data-ttu-id="0edbf-121">Ajouter un **bibliothèque de contrôles Windows** projet à la solution.</span><span class="sxs-lookup"><span data-stu-id="0edbf-121">Add a **Windows Control Library** project to the solution.</span></span>

2. <span data-ttu-id="0edbf-122">Ajouter un nouveau **UserControl** élément au projet DebugControlLibrary.</span><span class="sxs-lookup"><span data-stu-id="0edbf-122">Add a new **UserControl** item to the DebugControlLibrary project.</span></span> <span data-ttu-id="0edbf-123">Pour plus d’informations, consultez [Guide pratique pour Ajouter de nouveaux éléments de projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="0edbf-123">For details, see [How to: Add New Project Items](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span></span> <span data-ttu-id="0edbf-124">Nommez le nouveau fichier source une base « DebugControl ».</span><span class="sxs-lookup"><span data-stu-id="0edbf-124">Give the new source file a base name of "DebugControl".</span></span>

3. <span data-ttu-id="0edbf-125">À l’aide de la **l’Explorateur de solutions**, supprimer le contrôle du projet par défaut en supprimant le fichier de code avec un nom de base «`UserControl1`».</span><span class="sxs-lookup"><span data-stu-id="0edbf-125">Using the **Solution Explorer**, delete the project's default control by deleting the code file with a base name of "`UserControl1`".</span></span> <span data-ttu-id="0edbf-126">Pour plus d’informations, consultez [Guide pratique pour Supprimer, suppression et exclure des éléments](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="0edbf-126">For details, see [How to: Remove, Delete, and Exclude Items](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span></span>

4. <span data-ttu-id="0edbf-127">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="0edbf-127">Build the solution.</span></span>

## <a name="checkpoint"></a><span data-ttu-id="0edbf-128">Point de contrôle</span><span class="sxs-lookup"><span data-stu-id="0edbf-128">Checkpoint</span></span>

<span data-ttu-id="0edbf-129">À ce stade, vous serez en mesure de voir votre contrôle personnalisé dans le **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="0edbf-129">At this point, you will be able to see your custom control in the **Toolbox**.</span></span>

<span data-ttu-id="0edbf-130">Pour vérifier votre progression, rechercher le nouvel onglet appelé **Composants DebugControlLibrary** et cliquez sur pour le sélectionner.</span><span class="sxs-lookup"><span data-stu-id="0edbf-130">To check your progress, find the new tab called **DebugControlLibrary Components** and click to select it.</span></span> <span data-ttu-id="0edbf-131">Quand il s’ouvre, vous verrez votre contrôle répertorié comme **DebugControl** avec l’icône par défaut en regard de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="0edbf-131">When it opens, you will see your control listed as **DebugControl** with the default icon beside it.</span></span>

## <a name="add-a-property-to-your-custom-control"></a><span data-ttu-id="0edbf-132">Ajouter une propriété à votre contrôle personnalisé</span><span class="sxs-lookup"><span data-stu-id="0edbf-132">Add a property to your custom control</span></span>

<span data-ttu-id="0edbf-133">Pour montrer que le code de votre contrôle personnalisé s’exécute au moment du design, vous ajoutez une propriété et définissez un point d’arrêt dans le code qui implémente la propriété.</span><span class="sxs-lookup"><span data-stu-id="0edbf-133">To demonstrate that your custom control's code is running at design-time, you will add a property and set a breakpoint in the code that implements the property.</span></span>

1. <span data-ttu-id="0edbf-134">Ouvrez **DebugControl** dans le **éditeur de Code**.</span><span class="sxs-lookup"><span data-stu-id="0edbf-134">Open **DebugControl** in the **Code Editor**.</span></span> <span data-ttu-id="0edbf-135">Ajoutez le code suivant à la définition de classe :</span><span class="sxs-lookup"><span data-stu-id="0edbf-135">Add the following code to the class definition:</span></span>

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

2. <span data-ttu-id="0edbf-136">Générez la solution.</span><span class="sxs-lookup"><span data-stu-id="0edbf-136">Build the solution.</span></span>

## <a name="add-your-custom-control-to-the-host-form"></a><span data-ttu-id="0edbf-137">Ajouter votre contrôle personnalisé au formulaire hôte</span><span class="sxs-lookup"><span data-stu-id="0edbf-137">Add your custom control to the host form</span></span>

<span data-ttu-id="0edbf-138">Pour déboguer le comportement au moment du design de votre contrôle personnalisé, vous devez placer une instance de la classe de contrôle personnalisé sur un formulaire hôte.</span><span class="sxs-lookup"><span data-stu-id="0edbf-138">To debug the design-time behavior of your custom control, you will place an instance of the custom control class on a host form.</span></span>

1. <span data-ttu-id="0edbf-139">Dans le projet « DebuggingExample », ouvrez Form1 dans le **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="0edbf-139">In the "DebuggingExample" project, open Form1 in the **Windows Forms Designer**.</span></span>

2. <span data-ttu-id="0edbf-140">Dans le **boîte à outils**, ouvrez le **Composants DebugControlLibrary** onglet et faites glisser un **DebugControl** instance vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="0edbf-140">In the **Toolbox**, open the **DebugControlLibrary Components** tab and drag a **DebugControl** instance onto the form.</span></span>

3. <span data-ttu-id="0edbf-141">Rechercher la `DemoString` propriété personnalisée dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0edbf-141">Find the `DemoString` custom property in the **Properties** window.</span></span> <span data-ttu-id="0edbf-142">Notez que vous pouvez modifier sa valeur comme vous le feriez pour toute autre propriété.</span><span class="sxs-lookup"><span data-stu-id="0edbf-142">Note that you can change its value as you would any other property.</span></span> <span data-ttu-id="0edbf-143">Notez également que lorsque la `DemoString` propriété est sélectionnée, la chaîne de la propriété description s’affiche en bas de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0edbf-143">Also note that when the `DemoString` property is selected, the property's description string appears at the bottom of the **Properties** window.</span></span>

## <a name="set-up-the-project-for-design-time-debugging"></a><span data-ttu-id="0edbf-144">Configurer le projet pour le débogage au moment du design</span><span class="sxs-lookup"><span data-stu-id="0edbf-144">Set up the project for design-time debugging</span></span>

<span data-ttu-id="0edbf-145">Pour déboguer le comportement au moment du design de votre contrôle personnalisé, vous allez déboguer une instance distincte de Visual Studio qui exécute le code de votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edbf-145">To debug your custom control's design-time behavior, you will debug a separate instance of Visual Studio that is running your custom control's code.</span></span>

1. <span data-ttu-id="0edbf-146">Avec le bouton droit sur le **DebugControlLibrary** de projet dans le **l’Explorateur de solutions** et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="0edbf-146">Right-click on the **DebugControlLibrary** project in the **Solution Explorer** and select **Properties**.</span></span>

2. <span data-ttu-id="0edbf-147">Dans le **DebugControlLibrary** feuille de propriétés, sélectionnez le **déboguer** onglet.</span><span class="sxs-lookup"><span data-stu-id="0edbf-147">In the **DebugControlLibrary** property sheet, select the **Debug** tab.</span></span>

     <span data-ttu-id="0edbf-148">Dans le **Action de démarrage** section, sélectionnez **démarrer le programme externe**.</span><span class="sxs-lookup"><span data-stu-id="0edbf-148">In the **Start Action** section, select **Start external program**.</span></span> <span data-ttu-id="0edbf-149">Vous serez le débogage d’une instance distincte de Visual Studio, cliquez sur le bouton de sélection (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) pour le rechercher l’IDE Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0edbf-149">You will be debugging a separate instance of Visual Studio, so click the ellipsis (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button to browse for the Visual Studio IDE.</span></span> <span data-ttu-id="0edbf-150">Le nom du fichier exécutable est **devenv.exe**, et si vous avez installé à l’emplacement par défaut, son chemin d’accès est %programfiles%\Microsoft Visual Studio 9.0\Common7\IDE\devenv.exe.</span><span class="sxs-lookup"><span data-stu-id="0edbf-150">The name of the executable file is **devenv.exe**, and if you installed to the default location, its path is %programfiles%\Microsoft Visual Studio 9.0\Common7\IDE\devenv.exe.</span></span>

3. <span data-ttu-id="0edbf-151">Cliquez sur **OK** pour fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0edbf-151">Click **OK** to close the dialog box.</span></span>

4. <span data-ttu-id="0edbf-152">Avec le bouton droit le **DebugControlLibrary** de projet et sélectionnez **définir comme projet de démarrage** pour activer cette configuration de débogage.</span><span class="sxs-lookup"><span data-stu-id="0edbf-152">Right-click the **DebugControlLibrary** project and select **Set as StartUp Project** to enable this debugging configuration.</span></span>

## <a name="debug-your-custom-control-at-design-time"></a><span data-ttu-id="0edbf-153">Déboguer votre contrôle personnalisé au moment du design</span><span class="sxs-lookup"><span data-stu-id="0edbf-153">Debug your custom control at design time</span></span>

<span data-ttu-id="0edbf-154">Vous êtes maintenant prêt à déboguer votre contrôle personnalisé en cours d’exécution en mode Création.</span><span class="sxs-lookup"><span data-stu-id="0edbf-154">Now you are ready to debug your custom control as it runs in design mode.</span></span> <span data-ttu-id="0edbf-155">Lorsque vous démarrez la session de débogage, une nouvelle instance de Visual Studio sera créée, et vous allez l’utiliser pour charger la solution « DebuggingExample ».</span><span class="sxs-lookup"><span data-stu-id="0edbf-155">When you start the debugging session, a new instance of Visual Studio will be created, and you will use it to load the "DebuggingExample" solution.</span></span> <span data-ttu-id="0edbf-156">Lorsque vous ouvrez Form1 dans le **Concepteur Forms**, une instance de votre contrôle personnalisé est créée et commence à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0edbf-156">When you open Form1 in the **Forms Designer**, an instance of your custom control will be created and will start running.</span></span>

1. <span data-ttu-id="0edbf-157">Ouvrir le **DebugControl** fichier source dans le **éditeur de Code** et placer un point d’arrêt sur la `Set` l’accesseur de la `DemoString` propriété.</span><span class="sxs-lookup"><span data-stu-id="0edbf-157">Open the **DebugControl** source file in the **Code Editor** and place a breakpoint on the `Set` accessor of the `DemoString` property.</span></span>

2. <span data-ttu-id="0edbf-158">Appuyez sur F5 pour démarrer la session de débogage.</span><span class="sxs-lookup"><span data-stu-id="0edbf-158">Press F5 to start the debugging session.</span></span> <span data-ttu-id="0edbf-159">Notez qu’une nouvelle instance de Visual Studio est créée.</span><span class="sxs-lookup"><span data-stu-id="0edbf-159">Note that a new instance of Visual Studio is created.</span></span> <span data-ttu-id="0edbf-160">Vous pouvez faire la distinction entre les instances de deux manières :</span><span class="sxs-lookup"><span data-stu-id="0edbf-160">You can distinguish between the instances in two ways:</span></span>

    - <span data-ttu-id="0edbf-161">L’instance de débogage a le mot **en cours d’exécution** dans sa barre de titre</span><span class="sxs-lookup"><span data-stu-id="0edbf-161">The debugging instance has the word **Running** in its title bar</span></span>

    - <span data-ttu-id="0edbf-162">L’instance de débogage a le **Démarrer** bouton sur son **déboguer** barre d’outils désactivé</span><span class="sxs-lookup"><span data-stu-id="0edbf-162">The debugging instance has the **Start** button on its **Debug** toolbar disabled</span></span>

     <span data-ttu-id="0edbf-163">Votre point d’arrêt est défini dans l’instance de débogage.</span><span class="sxs-lookup"><span data-stu-id="0edbf-163">Your breakpoint is set in the debugging instance.</span></span>

3. <span data-ttu-id="0edbf-164">Dans la nouvelle instance de Visual Studio, ouvrez la solution « DebuggingExample ».</span><span class="sxs-lookup"><span data-stu-id="0edbf-164">In the new instance of Visual Studio, open the "DebuggingExample" solution.</span></span> <span data-ttu-id="0edbf-165">Vous pouvez facilement trouver la solution en sélectionnant **projets récents** à partir de la **fichier** menu.</span><span class="sxs-lookup"><span data-stu-id="0edbf-165">You can easily find the solution by selecting **Recent Projects** from the **File** menu.</span></span> <span data-ttu-id="0edbf-166">Le fichier de solution « DebuggingExample.sln » apparaît comme étant le dernier fichier utilisé.</span><span class="sxs-lookup"><span data-stu-id="0edbf-166">The "DebuggingExample.sln" solution file will be listed as the most recently used file.</span></span>

4. <span data-ttu-id="0edbf-167">Ouvrez Form1 dans le **Concepteur Forms** et sélectionnez le **DebugControl** contrôle.</span><span class="sxs-lookup"><span data-stu-id="0edbf-167">Open Form1 in the **Forms Designer** and select the **DebugControl** control.</span></span>

5. <span data-ttu-id="0edbf-168">Modifiez la valeur de la propriété `DemoString` .</span><span class="sxs-lookup"><span data-stu-id="0edbf-168">Change the value of the `DemoString` property.</span></span> <span data-ttu-id="0edbf-169">Notez que lorsque vous validez la modification, l’instance de débogage de Visual Studio acquiert le focus et l’exécution s’arrête au point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="0edbf-169">Note that when you commit the change, the debugging instance of Visual Studio acquires focus and execution stops at your breakpoint.</span></span> <span data-ttu-id="0edbf-170">Vous pouvez pas dans l’accesseur de propriété comme votre serait tout autre code.</span><span class="sxs-lookup"><span data-stu-id="0edbf-170">You can single-step through the property accessor just as your would any other code.</span></span>

6. <span data-ttu-id="0edbf-171">Lorsque vous avez terminé de votre session de débogage, vous pouvez quitter en fermant l’instance hébergée de Visual Studio ou en cliquant sur le **arrêter le débogage** bouton dans l’instance de débogage.</span><span class="sxs-lookup"><span data-stu-id="0edbf-171">When you are finished with your debugging session, you can exit by dismissing the hosted instance of Visual Studio or by clicking the **Stop Debugging** button in the debugging instance.</span></span>

## <a name="next-steps"></a><span data-ttu-id="0edbf-172">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="0edbf-172">Next steps</span></span>

<span data-ttu-id="0edbf-173">Maintenant que vous pouvez déboguer vos contrôles personnalisés au moment du design, il existe de nombreuses possibilités pour le développement d’interaction de votre contrôle avec l’IDE Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0edbf-173">Now that you can debug your custom controls at design time, there are many possibilities for expanding your control's interaction with the Visual Studio IDE.</span></span>

- <span data-ttu-id="0edbf-174">Vous pouvez utiliser la <xref:System.ComponentModel.Component.DesignMode%2A> propriété de la <xref:System.ComponentModel.Component> classe pour écrire du code qui s’exécutera seulement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="0edbf-174">You can use the <xref:System.ComponentModel.Component.DesignMode%2A> property of the <xref:System.ComponentModel.Component> class to write code that will only execute at design time.</span></span> <span data-ttu-id="0edbf-175">Pour plus d'informations, consultez <xref:System.ComponentModel.Component.DesignMode%2A>.</span><span class="sxs-lookup"><span data-stu-id="0edbf-175">For details, see <xref:System.ComponentModel.Component.DesignMode%2A>.</span></span>

- <span data-ttu-id="0edbf-176">Il existe plusieurs attributs que vous pouvez appliquer aux propriétés de votre contrôle pour manipuler l’interaction de votre contrôle personnalisé avec le concepteur.</span><span class="sxs-lookup"><span data-stu-id="0edbf-176">There are several attributes you can apply to your control's properties to manipulate your custom control's interaction with the designer.</span></span> <span data-ttu-id="0edbf-177">Vous pouvez trouver ces attributs dans le <xref:System.ComponentModel?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0edbf-177">You can find these attributes in the <xref:System.ComponentModel?displayProperty=nameWithType> namespace.</span></span>

- <span data-ttu-id="0edbf-178">Vous pouvez écrire un concepteur personnalisé pour votre contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0edbf-178">You can write a custom designer for your custom control.</span></span> <span data-ttu-id="0edbf-179">Cela vous donne un contrôle complet sur l’expérience de conception à l’aide de l’infrastructure du concepteur extensible exposée par Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0edbf-179">This gives you complete control over the design experience using the extensible designer infrastructure exposed by Visual Studio.</span></span> <span data-ttu-id="0edbf-180">Pour plus d’informations, consultez [procédure pas à pas : Création d’un Windows Forms de contrôle qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md).</span><span class="sxs-lookup"><span data-stu-id="0edbf-180">For details, see [Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features](creating-a-wf-control-design-time-features.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0edbf-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0edbf-181">See also</span></span>

- [<span data-ttu-id="0edbf-182">Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0edbf-182">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)
- <span data-ttu-id="0edbf-183">[Guide pratique pour Services d’accès au moment du Design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171822(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="0edbf-183">[How to: Access Design-Time Services](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171822(v=vs.120))</span></span>
- <span data-ttu-id="0edbf-184">[Guide pratique pour Prise en charge d’accès au moment du Design dans les Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171827(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="0edbf-184">[How to: Access Design-Time Support in Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171827(v=vs.120))</span></span>
