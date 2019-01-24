---
title: Définition de Classes (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- execution [Visual Basic], ending
- objects [Visual Basic], initializing
- Initialize event [Visual Basic]
- files [Visual Basic], closing
- programs [Visual Basic], quitting
- code, exiting
- objects [Visual Basic], creating
- program termination
- classes [Visual Basic], walkthroughs
- class modules, walkthroughs
- Terminate event [Visual Basic]
- execution [Visual Basic], stopping
ms.assetid: 07018828-2d49-4cf5-a44b-19fb15d9efea
ms.openlocfilehash: c41d3b2c8d905395f1249b15709da8dbdf5d4632
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640431"
---
# <a name="walkthrough-defining-classes-visual-basic"></a><span data-ttu-id="70950-102">Procédure pas à pas : Définition de Classes (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="70950-102">Walkthrough: Defining Classes (Visual Basic)</span></span>

<span data-ttu-id="70950-103">Cette procédure pas à pas montre comment définir des classes que vous pouvez ensuite utiliser pour créer des objets.</span><span class="sxs-lookup"><span data-stu-id="70950-103">This walkthrough demonstrates how to define classes, which you can then use to create objects.</span></span> <span data-ttu-id="70950-104">Il vous montre comment ajouter des propriétés et méthodes à la nouvelle classe et vous montre comment initialiser un objet.</span><span class="sxs-lookup"><span data-stu-id="70950-104">It also shows you how to add properties and methods to the new class, and demonstrates how to initialize an object.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
## <a name="to-define-a-class"></a><span data-ttu-id="70950-105">Pour définir une classe</span><span class="sxs-lookup"><span data-stu-id="70950-105">To define a class</span></span>
  
1.  <span data-ttu-id="70950-106">Créez un projet en cliquant sur **nouveau projet** sur le **fichier** menu.</span><span class="sxs-lookup"><span data-stu-id="70950-106">Create a project by clicking **New Project** on the **File** menu.</span></span> <span data-ttu-id="70950-107">La boîte de dialogue **Nouveau projet** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="70950-107">The **New Project** dialog box appears.</span></span>  
  
2.  <span data-ttu-id="70950-108">Sélectionnez les applications Windows à partir de la liste des modèles de projet Visual Basic pour afficher le nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="70950-108">Select Windows Application from the list of Visual Basic project templates to display the new project.</span></span>  
  
3.  <span data-ttu-id="70950-109">Ajoutez une nouvelle classe au projet en cliquant sur **ajouter une classe** sur le **projet** menu.</span><span class="sxs-lookup"><span data-stu-id="70950-109">Add a new class to the project by clicking **Add Class** on the **Project** menu.</span></span> <span data-ttu-id="70950-110">La boîte de dialogue **Ajouter un nouvel élément** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="70950-110">The **Add New Item** dialog box appears.</span></span>  
  
4.  <span data-ttu-id="70950-111">Sélectionnez le **classe** modèle.</span><span class="sxs-lookup"><span data-stu-id="70950-111">Select the **Class** template.</span></span>  
  
5.  <span data-ttu-id="70950-112">Nommez la nouvelle classe `UserNameInfo.vb`, puis cliquez sur **ajouter** pour afficher le code pour la nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="70950-112">Name the new class `UserNameInfo.vb`, and then click **Add** to display the code for the new class.</span></span>  
  
     [!code-vb[VbVbalrOOP#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#5)]
  
    > [!NOTE]
    >  <span data-ttu-id="70950-113">Vous pouvez utiliser Visual Basic **éditeur de Code** pour ajouter une classe à votre formulaire de démarrage en tapant le `Class` mot clé suivie du nom de la nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="70950-113">You can use the Visual Basic **Code Editor** to add a class to your startup form by typing the `Class` keyword followed by the name of the new class.</span></span> <span data-ttu-id="70950-114">Le **éditeur de Code** fournit un correspondant `End Class` instruction pour vous.</span><span class="sxs-lookup"><span data-stu-id="70950-114">The **Code Editor** provides a corresponding `End Class` statement for you.</span></span>  
  
6.  <span data-ttu-id="70950-115">Définir un champ privé pour la classe en ajoutant le code suivant entre les `Class` et `End Class` instructions :</span><span class="sxs-lookup"><span data-stu-id="70950-115">Define a private field for the class by adding the following code between the `Class` and `End Class` statements:</span></span>  
  
     [!code-vb[VbVbalrOOP#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#7)]
  
     <span data-ttu-id="70950-116">Déclaration du champ en tant que `Private` signifie qu’il peut être utilisé uniquement dans la classe.</span><span class="sxs-lookup"><span data-stu-id="70950-116">Declaring the field as `Private` means it can be used only within the class.</span></span> <span data-ttu-id="70950-117">Vous pouvez rendre les champs disponibles à partir de l’extérieur d’une classe à l’aide des modificateurs d’accès comme `Public` qui fournissent un accès plus.</span><span class="sxs-lookup"><span data-stu-id="70950-117">You can make fields available from outside a class by using access modifiers such as `Public` that provide more access.</span></span> <span data-ttu-id="70950-118">Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="70950-118">For more information, see [Access levels in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
7.  <span data-ttu-id="70950-119">Définir une propriété pour la classe en ajoutant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="70950-119">Define a property for the class by adding the following code:</span></span>  
  
     [!code-vb[VbVbalrOOP#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#8)]
  
8.  <span data-ttu-id="70950-120">Définissez une méthode pour la classe en ajoutant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="70950-120">Define a method for the class by adding the following code:</span></span>  
  
     [!code-vb[VbVbalrOOP#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#9)]
  
9. <span data-ttu-id="70950-121">Définir un constructeur paramétrable pour la nouvelle classe en ajoutant une procédure nommée `Sub New`:</span><span class="sxs-lookup"><span data-stu-id="70950-121">Define a parameterized constructor for the new class by adding a procedure named `Sub New`:</span></span>  
  
     [!code-vb[VbVbalrOOP#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#10)]
  
     <span data-ttu-id="70950-122">Le `Sub New` est appelé automatiquement lorsqu’un objet basé sur cette classe est créé.</span><span class="sxs-lookup"><span data-stu-id="70950-122">The `Sub New` constructor is called automatically when an object based on this class is created.</span></span> <span data-ttu-id="70950-123">Ce constructeur définit la valeur du champ qui contient le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="70950-123">This constructor sets the value of the field that holds the user name.</span></span>  
  
## <a name="to-create-a-button-to-test-the-class"></a><span data-ttu-id="70950-124">Pour créer un bouton pour tester la classe</span><span class="sxs-lookup"><span data-stu-id="70950-124">To create a button to test the class</span></span>
  
1.  <span data-ttu-id="70950-125">Modifiez le formulaire de démarrage en mode design en cliquant sur son nom dans **l’Explorateur de solutions** , puis en cliquant sur **Concepteur de vues**.</span><span class="sxs-lookup"><span data-stu-id="70950-125">Change the startup form to design mode by right-clicking its name in **Solution Explorer** and then clicking **View Designer**.</span></span> <span data-ttu-id="70950-126">Par défaut, le formulaire de démarrage pour les projets d’Application de Windows est nommé Form1.vb.</span><span class="sxs-lookup"><span data-stu-id="70950-126">By default, the startup form for Windows Application projects is named Form1.vb.</span></span> <span data-ttu-id="70950-127">Le formulaire principal s’affiche alors.</span><span class="sxs-lookup"><span data-stu-id="70950-127">The main form will then appear.</span></span>  
  
2.  <span data-ttu-id="70950-128">Ajoutez un bouton au formulaire principal et double-cliquez dessus pour afficher le code pour le `Button1_Click` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="70950-128">Add a button to the main form and double-click it to display the code for the `Button1_Click` event handler.</span></span> <span data-ttu-id="70950-129">Ajoutez le code suivant pour appeler la procédure de test :</span><span class="sxs-lookup"><span data-stu-id="70950-129">Add the following code to call the test procedure:</span></span>  
  
     [!code-vb[VbVbalrOOP#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#12)]
  
## <a name="to-run-your-application"></a><span data-ttu-id="70950-130">Pour exécuter votre application</span><span class="sxs-lookup"><span data-stu-id="70950-130">To run your application</span></span>
  
1.  <span data-ttu-id="70950-131">Exécutez votre application en appuyant sur F5.</span><span class="sxs-lookup"><span data-stu-id="70950-131">Run your application by pressing F5.</span></span> <span data-ttu-id="70950-132">Cliquez sur le bouton sur le formulaire pour appeler la procédure de test.</span><span class="sxs-lookup"><span data-stu-id="70950-132">Click the button on the form to call the test procedure.</span></span> <span data-ttu-id="70950-133">Il affiche un message indiquant que l’original `UserName` est « MOORE, BOBBY », car la procédure appelée le `Capitalize` méthode de l’objet.</span><span class="sxs-lookup"><span data-stu-id="70950-133">It displays a message stating that the original `UserName` is "MOORE, BOBBY", because the procedure called the `Capitalize` method of the object.</span></span>  
  
2.  <span data-ttu-id="70950-134">Cliquez sur **OK** pour fermer la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="70950-134">Click **OK** to dismiss the message box.</span></span> <span data-ttu-id="70950-135">Le `Button1 Click` procédure modifie la valeur de la `UserName` propriété et affiche un message indiquant que la nouvelle valeur de `UserName` est « Worden, Joe ».</span><span class="sxs-lookup"><span data-stu-id="70950-135">The `Button1 Click` procedure changes the value of the `UserName` property and displays a message stating that the new value of `UserName` is "Worden, Joe".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70950-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70950-136">See also</span></span>

- [<span data-ttu-id="70950-137">Programmation orientée objet (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="70950-137">Object-Oriented Programming (Visual Basic)</span></span>](../../concepts/object-oriented-programming.md)
- [<span data-ttu-id="70950-138">Objets et classes</span><span class="sxs-lookup"><span data-stu-id="70950-138">Objects and Classes</span></span>](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
