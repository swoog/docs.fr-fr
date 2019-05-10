---
title: 'Procédure pas à pas : démonstration de l’héritage visuel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- form inheritance [Windows Forms], walkthroughs
- visual inheritance
- inheritance [Windows Forms], walkthroughs
- walkthroughs [Windows Forms], visual inheritance
- Windows Forms, inheritance
ms.assetid: 01966086-3142-450e-8210-3fd4cb33f591
ms.openlocfilehash: a5e2a8b0bf982ff112d7930e331456fa69485dfc
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64665906"
---
# <a name="walkthrough-demonstrating-visual-inheritance"></a><span data-ttu-id="adaed-102">Procédure pas à pas : démonstration de l’héritage visuel</span><span class="sxs-lookup"><span data-stu-id="adaed-102">Walkthrough: Demonstrating Visual Inheritance</span></span>
<span data-ttu-id="adaed-103">L'héritage visuel vous permet de visualiser les contrôles sur le formulaire de base et d'ajouter de nouveaux contrôles.</span><span class="sxs-lookup"><span data-stu-id="adaed-103">Visual inheritance enables you to see the controls on the base form and to add new controls.</span></span> <span data-ttu-id="adaed-104">Dans cette procédure pas à pas, vous allez créer un formulaire de base et le compiler dans une bibliothèque de classes.</span><span class="sxs-lookup"><span data-stu-id="adaed-104">In this walkthrough you will create a base form and compile it into a class library.</span></span> <span data-ttu-id="adaed-105">Vous importerez cette bibliothèque de classes dans un autre projet et créerez un formulaire qui hérite du formulaire de base.</span><span class="sxs-lookup"><span data-stu-id="adaed-105">You will import this class library into another project and create a new form that inherits from the base form.</span></span> <span data-ttu-id="adaed-106">Pendant cette procédure pas à pas, vous allez apprendre à :</span><span class="sxs-lookup"><span data-stu-id="adaed-106">During this walkthrough, you will learn how to:</span></span>  
  
- <span data-ttu-id="adaed-107">créer un projet de bibliothèque de classes contenant un formulaire de base ;</span><span class="sxs-lookup"><span data-stu-id="adaed-107">Create a class library project containing a base form.</span></span>  
  
- <span data-ttu-id="adaed-108">ajouter un bouton avec des propriétés modifiables par les classes dérivées du formulaire de base ;</span><span class="sxs-lookup"><span data-stu-id="adaed-108">Add a button with properties that derived classes of the base form can modify.</span></span>  
  
- <span data-ttu-id="adaed-109">ajouter un bouton qui ne peut pas être modifié par les héritiers du formulaire de base ;</span><span class="sxs-lookup"><span data-stu-id="adaed-109">Add a button that cannot be modified by inheritors of the base form.</span></span>  
  
- <span data-ttu-id="adaed-110">créer un projet contenant un formulaire qui hérite de `BaseForm`.</span><span class="sxs-lookup"><span data-stu-id="adaed-110">Create a project containing a form that inherits from `BaseForm`.</span></span>  
  
 <span data-ttu-id="adaed-111">Pour finir, cette procédure pas à pas vous montrera la différence entre les contrôles privés et protégés dans un formulaire hérité.</span><span class="sxs-lookup"><span data-stu-id="adaed-111">Ultimately, this walkthrough will demonstrate the difference between private and protected controls on an inherited form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="adaed-112">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="adaed-112">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="adaed-113">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="adaed-113">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="adaed-114">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="adaed-114">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="adaed-115">Les contrôles ne prennent pas tous en charge l'héritage visuel à partir d'un formulaire de base.</span><span class="sxs-lookup"><span data-stu-id="adaed-115">Not all controls support visual inheritance from a base form.</span></span> <span data-ttu-id="adaed-116">Les contrôles suivants ne prennent pas en charge le scénario décrit dans cette procédure pas à pas :</span><span class="sxs-lookup"><span data-stu-id="adaed-116">The following controls do not support the scenario described in this walkthrough:</span></span>  
>   
>  <xref:System.Windows.Forms.WebBrowser>  
>   
>  <xref:System.Windows.Forms.ToolStrip>  
>   
>  <xref:System.Windows.Forms.ToolStripPanel>  
>   
>  <xref:System.Windows.Forms.TableLayoutPanel>  
>   
>  <xref:System.Windows.Forms.FlowLayoutPanel>  
>   
>  <xref:System.Windows.Forms.DataGridView>  
>   
>  <span data-ttu-id="adaed-117">Ces contrôles dans le formulaire hérité sont toujours en lecture seule, quels que soient les modificateurs que vous utilisez (`private`, `protected` ou `public`).</span><span class="sxs-lookup"><span data-stu-id="adaed-117">These controls in the inherited form are always read-only regardless of the modifiers you use (`private`, `protected`, or `public`).</span></span>  
  
## <a name="scenario-steps"></a><span data-ttu-id="adaed-118">Étapes du scénario</span><span class="sxs-lookup"><span data-stu-id="adaed-118">Scenario Steps</span></span>  
 <span data-ttu-id="adaed-119">La première étape consiste à créer le formulaire de base.</span><span class="sxs-lookup"><span data-stu-id="adaed-119">The first step is to create the base form.</span></span>  
  
#### <a name="to-create-a-class-library-project-containing-a-base-form"></a><span data-ttu-id="adaed-120">Pour créer un projet de bibliothèque de classes contenant un formulaire de base</span><span class="sxs-lookup"><span data-stu-id="adaed-120">To create a class library project containing a base form</span></span>  
  
1. <span data-ttu-id="adaed-121">À partir de la **fichier** menu, choisissez **New**, puis **projet** pour ouvrir le **nouveau projet** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="adaed-121">From the **File** menu, choose **New**, and then **Project** to open the **New Project** dialog box.</span></span>  
  
2. <span data-ttu-id="adaed-122">Créer une application Windows Forms nommée `BaseFormLibrary`.</span><span class="sxs-lookup"><span data-stu-id="adaed-122">Create a Windows Forms application named `BaseFormLibrary`.</span></span>  
  
3. <span data-ttu-id="adaed-123">Pour créer une bibliothèque de classes au lieu d’une application Windows Forms standard, dans **l’Explorateur de solutions**, avec le bouton droit le **BaseFormLibrary** nœud de projet, puis sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="adaed-123">To create a class library instead of a standard Windows Forms application, in **Solution Explorer**, right-click the **BaseFormLibrary** project node and then select **Properties**.</span></span>  
  
4. <span data-ttu-id="adaed-124">Dans les propriétés du projet, modifiez le **type de sortie** de **Windows Application** à **bibliothèque de classes**.</span><span class="sxs-lookup"><span data-stu-id="adaed-124">In the properties for the project, change the **Output type** from **Windows Application** to **Class Library**.</span></span>  
  
5. <span data-ttu-id="adaed-125">À partir de la **fichier** menu, choisissez **Enregistrer tout** pour enregistrer le projet et les fichiers à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="adaed-125">From the **File** menu, choose **Save All** to save the project and files to the default location.</span></span>  
  
 <span data-ttu-id="adaed-126">Les deux procédures suivantes ajoutent des boutons au formulaire de base.</span><span class="sxs-lookup"><span data-stu-id="adaed-126">The next two procedures add buttons to the base form.</span></span> <span data-ttu-id="adaed-127">Pour illustrer l'héritage visuel, donnez aux boutons différents niveaux d'accès en définissant leurs propriétés `Modifiers`.</span><span class="sxs-lookup"><span data-stu-id="adaed-127">To demonstrate visual inheritance, you will give the buttons different access levels by setting their `Modifiers` properties.</span></span>  
  
#### <a name="to-add-a-button-that-inheritors-of-the-base-form-can-modify"></a><span data-ttu-id="adaed-128">Pour ajouter un bouton modifiable par les héritiers du formulaire de base</span><span class="sxs-lookup"><span data-stu-id="adaed-128">To add a button that inheritors of the base form can modify</span></span>  
  
1. <span data-ttu-id="adaed-129">Ouvrez **Form1** dans le concepteur.</span><span class="sxs-lookup"><span data-stu-id="adaed-129">Open **Form1** in the designer.</span></span>  
  
2. <span data-ttu-id="adaed-130">Sur le **tous les Windows Forms** onglet de la **boîte à outils**, double-cliquez sur **bouton** pour ajouter un bouton au formulaire.</span><span class="sxs-lookup"><span data-stu-id="adaed-130">On the **All Windows Forms** tab of the **Toolbox**, double-click **Button** to add a button to the form.</span></span> <span data-ttu-id="adaed-131">Utilisez la souris pour positionner et redimensionner le bouton.</span><span class="sxs-lookup"><span data-stu-id="adaed-131">Use the mouse to position and resize the button.</span></span>  
  
3. <span data-ttu-id="adaed-132">Dans la fenêtre Propriétés, définissez les propriétés suivantes du bouton :</span><span class="sxs-lookup"><span data-stu-id="adaed-132">In the Properties window, set the following properties of the button:</span></span>  
  
    - <span data-ttu-id="adaed-133">Définir le **texte** propriété **Say Hello**.</span><span class="sxs-lookup"><span data-stu-id="adaed-133">Set the **Text** property to **Say Hello**.</span></span>  
  
    - <span data-ttu-id="adaed-134">Définir le **(nom)** propriété **btnProtected**.</span><span class="sxs-lookup"><span data-stu-id="adaed-134">Set the **(Name)** property to **btnProtected**.</span></span>  
  
    - <span data-ttu-id="adaed-135">Définir le **modificateurs** propriété **protégé**.</span><span class="sxs-lookup"><span data-stu-id="adaed-135">Set the **Modifiers** property to **Protected**.</span></span> <span data-ttu-id="adaed-136">Cela rend possible pour les formulaires qui héritent de **Form1** pour modifier les propriétés de **btnProtected**.</span><span class="sxs-lookup"><span data-stu-id="adaed-136">This makes it possible for forms that inherit from **Form1** to modify the properties of **btnProtected**.</span></span>  
  
4. <span data-ttu-id="adaed-137">Double-cliquez sur le **Say Hello** pour ajouter un gestionnaire d’événements pour le **cliquez sur** événement.</span><span class="sxs-lookup"><span data-stu-id="adaed-137">Double-click the **Say Hello** button to add an event handler for the **Click** event.</span></span>  
  
5. <span data-ttu-id="adaed-138">Ajoutez la ligne de code suivante au gestionnaire d'événements :</span><span class="sxs-lookup"><span data-stu-id="adaed-138">Add the following line of code to the event handler:</span></span>  
  
    ```vb  
    MessageBox.Show("Hello, World!")  
    ```  
  
    ```csharp  
    MessageBox.Show("Hello, World!");  
    ```  
  
#### <a name="to-add-a-button-that-cannot-be-modified-by-inheritors-of-the-base-form"></a><span data-ttu-id="adaed-139">Pour ajouter un bouton qui ne peut pas être modifié par les héritiers du formulaire de base</span><span class="sxs-lookup"><span data-stu-id="adaed-139">To add a button that cannot be modified by inheritors of the base form</span></span>  
  
1. <span data-ttu-id="adaed-140">Passez en mode design en cliquant sur le **Form1.vb [Design], Form1.cs [Design] ou Form1.jsl [Design]** onglet au-dessus de l’éditeur de code, ou en appuyant sur F7.</span><span class="sxs-lookup"><span data-stu-id="adaed-140">Switch to design view by clicking the **Form1.vb [Design], Form1.cs [Design], or Form1.jsl [Design]** tab above the code editor, or by pressing F7.</span></span>  
  
2. <span data-ttu-id="adaed-141">Ajoutez un deuxième bouton et définissez ses propriétés comme suit :</span><span class="sxs-lookup"><span data-stu-id="adaed-141">Add a second button and set its properties as follows:</span></span>  
  
    - <span data-ttu-id="adaed-142">Définir le **texte** propriété **Say Goodbye**.</span><span class="sxs-lookup"><span data-stu-id="adaed-142">Set the **Text** property to **Say Goodbye**.</span></span>  
  
    - <span data-ttu-id="adaed-143">Définir le **(nom)** propriété **btnPrivate**.</span><span class="sxs-lookup"><span data-stu-id="adaed-143">Set the **(Name)** property to **btnPrivate**.</span></span>  
  
    - <span data-ttu-id="adaed-144">Définir le **modificateurs** propriété **privé**.</span><span class="sxs-lookup"><span data-stu-id="adaed-144">Set the **Modifiers** property to **Private**.</span></span> <span data-ttu-id="adaed-145">Cela empêche les formulaires qui héritent **Form1** pour modifier les propriétés de **btnPrivate**.</span><span class="sxs-lookup"><span data-stu-id="adaed-145">This makes it impossible for forms that inherit from **Form1** to modify the properties of **btnPrivate**.</span></span>  
  
3. <span data-ttu-id="adaed-146">Double-cliquez sur le **Say Goodbye** pour ajouter un gestionnaire d’événements pour le **cliquez sur** événement.</span><span class="sxs-lookup"><span data-stu-id="adaed-146">Double-click the **Say Goodbye** button to add an event handler for the **Click** event.</span></span> <span data-ttu-id="adaed-147">Placez la ligne de code suivante dans la procédure d'événement :</span><span class="sxs-lookup"><span data-stu-id="adaed-147">Place the following line of code in the event procedure:</span></span>  
  
    ```vb  
    MessageBox.Show("Goodbye!")  
    ```  
  
    ```csharp  
    MessageBox.Show("Goodbye!");  
    ```  
  
4. <span data-ttu-id="adaed-148">À partir de la **Build** menu, choisissez **générer une bibliothèque BaseForm** pour générer la bibliothèque de classes.</span><span class="sxs-lookup"><span data-stu-id="adaed-148">From the **Build** menu, choose **Build BaseForm Library** to build the class library.</span></span>  
  
     <span data-ttu-id="adaed-149">Une fois la bibliothèque générée, vous pouvez créer un projet qui hérite du formulaire que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="adaed-149">Once the library is built, you can create a new project that inherits from the form you just created.</span></span>  
  
#### <a name="to-create-a-project-containing-a-form-that-inherits-from-the-base-form"></a><span data-ttu-id="adaed-150">Pour créer un projet contenant un formulaire qui hérite du formulaire de base</span><span class="sxs-lookup"><span data-stu-id="adaed-150">To create a project containing a form that inherits from the base form</span></span>  
  
1. <span data-ttu-id="adaed-151">À partir de la **fichier** menu, choisissez **ajouter** , puis **nouveau projet** pour ouvrir le **ajouter un nouveau projet** boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="adaed-151">From the **File** menu, choose **Add** and then **New Project** to open the **Add New Project** dialog box.</span></span>  
  
2. <span data-ttu-id="adaed-152">Créer une application Windows Forms nommée `InheritanceTest`.</span><span class="sxs-lookup"><span data-stu-id="adaed-152">Create a Windows Forms application named `InheritanceTest`.</span></span>  
  
#### <a name="to-add-an-inherited-form"></a><span data-ttu-id="adaed-153">Pour ajouter un formulaire hérité</span><span class="sxs-lookup"><span data-stu-id="adaed-153">To add an inherited form</span></span>  
  
1. <span data-ttu-id="adaed-154">Dans **l’Explorateur de solutions**, avec le bouton droit le **InheritanceTest** projet, sélectionnez **ajouter**, puis sélectionnez **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="adaed-154">In **Solution Explorer**, right-click the **InheritanceTest** project, select **Add**, and then select **New Item**.</span></span>  
  
2. <span data-ttu-id="adaed-155">Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez le **Windows Forms** catégorie (si vous avez une liste de catégories), puis sélectionnez le **formulaire hérité** modèle.</span><span class="sxs-lookup"><span data-stu-id="adaed-155">In the **Add New Item** dialog box, select the **Windows Forms** category (if you have a list of categories) and then select the **Inherited Form** template.</span></span>  
  
3. <span data-ttu-id="adaed-156">Laissez le nom par défaut `Form2` puis cliquez sur **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="adaed-156">Leave the default name of `Form2` and then click **Add**.</span></span>  
  
4. <span data-ttu-id="adaed-157">Dans le **sélecteur d’héritage** boîte de dialogue, sélectionnez **Form1** à partir de la **BaseFormLibrary** projet en tant que le formulaire hériter et cliquez sur **OK** .</span><span class="sxs-lookup"><span data-stu-id="adaed-157">In the **Inheritance Picker** dialog box, select **Form1** from the **BaseFormLibrary** project as the form to inherit from and click **OK**.</span></span>  
  
     <span data-ttu-id="adaed-158">Cette opération crée un formulaire dans le **InheritanceTest** projet qui dérive du formulaire dans **BaseFormLibrary**.</span><span class="sxs-lookup"><span data-stu-id="adaed-158">This creates a form in the **InheritanceTest** project that derives from the form in **BaseFormLibrary**.</span></span>  
  
5. <span data-ttu-id="adaed-159">Ouvrez le formulaire hérité (**Form2**) dans le concepteur en double-cliquant dessus, s’il n’est pas déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="adaed-159">Open the inherited form (**Form2**) in the designer by double-clicking it, if it is not already open.</span></span>  
  
     <span data-ttu-id="adaed-160">Dans le concepteur, les boutons hérités possèdent un symbole)</span><span class="sxs-lookup"><span data-stu-id="adaed-160">In the designer, the inherited buttons have a symbol (</span></span>![Capture d’écran du symbole de l’héritage de Visual Basic.](./media/walkthrough-demonstrating-visual-inheritance/visual-basic-inheritance-glyph.gif)<span data-ttu-id="adaed-162">) dans le coin supérieur, indiquant qu’ils sont hérités.</span><span class="sxs-lookup"><span data-stu-id="adaed-162">) in their upper corner, indicating they are inherited.</span></span>  
  
6. <span data-ttu-id="adaed-163">Sélectionnez le **Say Hello** bouton et observez les poignées de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="adaed-163">Select the **Say Hello** button and observe the resize handles.</span></span> <span data-ttu-id="adaed-164">Ce bouton étant protégé, les héritiers peuvent le déplacer, le redimensionner, changer sa légende et apporter d'autres modifications.</span><span class="sxs-lookup"><span data-stu-id="adaed-164">Because this button is protected, the inheritors can move it, resize it, change its caption, and make other modifications.</span></span>  
  
7. <span data-ttu-id="adaed-165">Sélectionnez privé **Say Goodbye** bouton et notez qu’il n’a pas de poignées de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="adaed-165">Select the private **Say Goodbye** button, and notice that it does not have resize handles.</span></span> <span data-ttu-id="adaed-166">En outre, dans le **propriétés** fenêtre, les propriétés de ce bouton sont estompées pour indiquer qu’ils ne sont pas modifiables.</span><span class="sxs-lookup"><span data-stu-id="adaed-166">Additionally, in the **Properties** window, the properties of this button are grayed to indicate they cannot be modified.</span></span>  
  
8. <span data-ttu-id="adaed-167">Si vous utilisez Visual c# :</span><span class="sxs-lookup"><span data-stu-id="adaed-167">If you are using Visual C#:</span></span>  
  
    1. <span data-ttu-id="adaed-168">Dans **l’Explorateur de solutions**, avec le bouton droit **Form1** dans le **InheritanceTest** de projet, puis choisissez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="adaed-168">In **Solution Explorer**, right-click **Form1** in the **InheritanceTest** project and then choose **Delete**.</span></span> <span data-ttu-id="adaed-169">Dans la boîte de message qui s’affiche, cliquez sur **OK** pour confirmer la suppression.</span><span class="sxs-lookup"><span data-stu-id="adaed-169">In the message box that appears, click **OK** to confirm the deletion.</span></span>  
  
    2. <span data-ttu-id="adaed-170">Ouvrez le fichier Program.cs et remplacez la ligne `Application.Run(new Form1());` par `Application.Run(new Form2());`.</span><span class="sxs-lookup"><span data-stu-id="adaed-170">Open the Program.cs file and change the line `Application.Run(new Form1());` to `Application.Run(new Form2());`.</span></span>  
  
9. <span data-ttu-id="adaed-171">Dans **l’Explorateur de solutions**, avec le bouton droit le **InheritanceTest** de projet et sélectionnez **définir comme projet de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="adaed-171">In **Solution Explorer**, right-click the **InheritanceTest** project and select **Set As Startup Project**.</span></span>  
  
10. <span data-ttu-id="adaed-172">Dans **l’Explorateur de solutions**, avec le bouton droit le **InheritanceTest** de projet et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="adaed-172">In **Solution Explorer**, right-click the **InheritanceTest** project and select **Properties**.</span></span>  
  
11. <span data-ttu-id="adaed-173">Dans le **InheritanceTest** pages de propriétés, définissez la **objet de démarrage** soit le formulaire hérité (**Form2**).</span><span class="sxs-lookup"><span data-stu-id="adaed-173">In the **InheritanceTest** property pages, set the **Startup object** to be the inherited form (**Form2**).</span></span>  
  
12. <span data-ttu-id="adaed-174">Appuyez sur F5 pour exécuter l'application et observez le comportement du formulaire hérité.</span><span class="sxs-lookup"><span data-stu-id="adaed-174">Press F5 to run the application, and observe the behavior of the inherited form.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="adaed-175">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="adaed-175">Next Steps</span></span>  
 <span data-ttu-id="adaed-176">L'héritage pour les contrôles utilisateur fonctionne de la même façon.</span><span class="sxs-lookup"><span data-stu-id="adaed-176">Inheritance for user controls works in much the same way.</span></span> <span data-ttu-id="adaed-177">Ouvrez un nouveau projet de bibliothèque de classes et ajoutez un contrôle utilisateur.</span><span class="sxs-lookup"><span data-stu-id="adaed-177">Open a new class library project and add a user control.</span></span> <span data-ttu-id="adaed-178">Placez les contrôles constituants dessus et compilez le projet.</span><span class="sxs-lookup"><span data-stu-id="adaed-178">Place constituent controls on it and compile the project.</span></span> <span data-ttu-id="adaed-179">Ouvrez un autre projet de bibliothèque de classes et ajoutez une référence à la bibliothèque de classes compilée.</span><span class="sxs-lookup"><span data-stu-id="adaed-179">Open another new class library project and add a reference to the compiled class library.</span></span> <span data-ttu-id="adaed-180">Essayez également d’ajouter un contrôle hérité (via le **ajouter de nouveaux éléments** boîte de dialogue) au projet et à l’aide de la **sélecteur d’héritage**.</span><span class="sxs-lookup"><span data-stu-id="adaed-180">Also, try adding an inherited control (through the **Add New Items** dialog box) to the project and using the **Inheritance Picker**.</span></span> <span data-ttu-id="adaed-181">Ajoutez un contrôle utilisateur et modifiez le `Inherits` (`:` en Visual c#) instruction.</span><span class="sxs-lookup"><span data-stu-id="adaed-181">Add a user control, and change the `Inherits` (`:` in Visual C#) statement.</span></span> <span data-ttu-id="adaed-182">Pour plus d'informations, voir [Procédure : Hériter des Windows Forms](how-to-inherit-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="adaed-182">For more information, see [How to: Inherit Windows Forms](how-to-inherit-windows-forms.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="adaed-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adaed-183">See also</span></span>

- [<span data-ttu-id="adaed-184">Guide pratique pour Hériter des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="adaed-184">How to: Inherit Windows Forms</span></span>](how-to-inherit-windows-forms.md)
- [<span data-ttu-id="adaed-185">Héritage visuel des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="adaed-185">Windows Forms Visual Inheritance</span></span>](windows-forms-visual-inheritance.md)
- [<span data-ttu-id="adaed-186">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="adaed-186">Windows Forms</span></span>](../index.md)
