---
title: 'Procédure pas à pas : exécution d’une opération en arrière-plan'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- background tasks
- forms [Windows Forms], multithreading
- forms [Windows Forms], background operations
- background threads
- BackgroundWorker class [Windows Forms], examples
- threading [Windows Forms], background operations
- background operations
ms.assetid: 1b9a4e0a-f134-48ff-a1be-c461446a31ba
ms.openlocfilehash: 6c705c6d6ff9bbd233bbddc3a73acf8aca13a547
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211522"
---
# <a name="walkthrough-running-an-operation-in-the-background"></a><span data-ttu-id="92b41-102">Procédure pas à pas : exécution d’une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="92b41-102">Walkthrough: Running an Operation in the Background</span></span>

<span data-ttu-id="92b41-103">Si vous avez une opération qui prendra un certain temps et que vous ne souhaitez pas causer de retards dans votre interface utilisateur, vous pouvez utiliser la classe <xref:System.ComponentModel.BackgroundWorker> pour exécuter l'opération sur un autre thread.</span><span class="sxs-lookup"><span data-stu-id="92b41-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>

<span data-ttu-id="92b41-104">Pour obtenir une liste complète du code utilisé dans cet exemple, consultez [Comment : exécuter une opération en arrière-plan](how-to-run-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="92b41-104">For a complete listing of the code used in this example, see [How to: Run an Operation in the Background](how-to-run-an-operation-in-the-background.md).</span></span>

## <a name="run-an-operation-in-the-background"></a><span data-ttu-id="92b41-105">Exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="92b41-105">Run an operation in the background</span></span>

1. <span data-ttu-id="92b41-106">Avec votre formulaire actif dans le Concepteur de formulaires Windows dans Visual Studio, faites glisser deux <xref:System.Windows.Forms.Button> des contrôles de la **boîte à outils** le formulaire, puis définissez le `Name` et <xref:System.Windows.Forms.Control.Text%2A> propriétés des boutons en fonction de la tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="92b41-106">With your form active in the Windows Forms Designer in Visual Studio, drag two <xref:System.Windows.Forms.Button> controls from the **Toolbox** to the form, and then set the `Name` and <xref:System.Windows.Forms.Control.Text%2A> properties of the buttons according to the following table.</span></span>

    |<span data-ttu-id="92b41-107">Bouton</span><span class="sxs-lookup"><span data-stu-id="92b41-107">Button</span></span>|<span data-ttu-id="92b41-108">Nom</span><span class="sxs-lookup"><span data-stu-id="92b41-108">Name</span></span>|<span data-ttu-id="92b41-109">Texte</span><span class="sxs-lookup"><span data-stu-id="92b41-109">Text</span></span>|
    |------------|----------|----------|
    |`button1`|`startBtn`|<span data-ttu-id="92b41-110">**Démarrer**</span><span class="sxs-lookup"><span data-stu-id="92b41-110">**Start**</span></span>|
    |`button2`|`cancelBtn`|<span data-ttu-id="92b41-111">**Annuler**</span><span class="sxs-lookup"><span data-stu-id="92b41-111">**Cancel**</span></span>|

2. <span data-ttu-id="92b41-112">Ouvrir le **boîte à outils**, cliquez sur le **composants** onglet, puis faites glisser le <xref:System.ComponentModel.BackgroundWorker> composant vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="92b41-112">Open the **Toolbox**, click the **Components** tab, and then drag the <xref:System.ComponentModel.BackgroundWorker> component onto your form.</span></span>

     <span data-ttu-id="92b41-113">Le `backgroundWorker1` composant apparaît dans le **barre d’état du composant**.</span><span class="sxs-lookup"><span data-stu-id="92b41-113">The `backgroundWorker1` component appears in the **Component Tray**.</span></span>

3. <span data-ttu-id="92b41-114">Dans la fenêtre **Propriétés** , définissez la propriété <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> sur `true`.</span><span class="sxs-lookup"><span data-stu-id="92b41-114">In the **Properties** window, set the <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> property to `true`.</span></span>

4. <span data-ttu-id="92b41-115">Dans le **propriétés** fenêtre, cliquez sur le **événements** bouton, puis double-cliquez sur le <xref:System.ComponentModel.BackgroundWorker.DoWork> et <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> événements pour créer des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="92b41-115">In the **Properties** window, click on the **Events** button, and then double-click the <xref:System.ComponentModel.BackgroundWorker.DoWork> and <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> events to create event handlers.</span></span>

5. <span data-ttu-id="92b41-116">Insérez votre code du temps dans le <xref:System.ComponentModel.BackgroundWorker.DoWork> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92b41-116">Insert your time-consuming code into the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span>

6. <span data-ttu-id="92b41-117">Extraire tous les paramètres requis par l’opération à partir de la <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> propriété de le <xref:System.ComponentModel.DoWorkEventArgs> paramètre.</span><span class="sxs-lookup"><span data-stu-id="92b41-117">Extract any parameters required by the operation from the <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> property of the <xref:System.ComponentModel.DoWorkEventArgs> parameter.</span></span>

7. <span data-ttu-id="92b41-118">Assignez le résultat du calcul à la <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> propriété de la <xref:System.ComponentModel.DoWorkEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="92b41-118">Assign the result of the computation to the <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> property of the <xref:System.ComponentModel.DoWorkEventArgs>.</span></span>

     <span data-ttu-id="92b41-119">Il s’agit de va être disponible pour le <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92b41-119">This is will be available to the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#2)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#2)]

8. <span data-ttu-id="92b41-120">Insérer du code pour récupérer le résultat de votre opération dans le <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92b41-120">Insert code for retrieving the result of your operation in the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#3)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#3)]

9. <span data-ttu-id="92b41-121">Implémentez la méthode `TimeConsumingOperation`.</span><span class="sxs-lookup"><span data-stu-id="92b41-121">Implement the `TimeConsumingOperation` method.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#4)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#4)]

10. <span data-ttu-id="92b41-122">Dans le Concepteur Windows Forms, double-cliquez sur `startButton` pour créer le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92b41-122">In the Windows Forms Designer, double-click `startButton` to create the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>

11. <span data-ttu-id="92b41-123">Appelez le <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> méthode dans le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour `startButton`.</span><span class="sxs-lookup"><span data-stu-id="92b41-123">Call the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method in the <xref:System.Windows.Forms.Control.Click> event handler for `startButton`.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#5)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#5)]

12. <span data-ttu-id="92b41-124">Dans le Concepteur Windows Forms, double-cliquez sur `cancelButton` pour créer le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="92b41-124">In the Windows Forms Designer, double-click `cancelButton` to create the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>

13. <span data-ttu-id="92b41-125">Appelez le <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> méthode dans le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour `cancelButton`.</span><span class="sxs-lookup"><span data-stu-id="92b41-125">Call the <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> method in the <xref:System.Windows.Forms.Control.Click> event handler for `cancelButton`.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#6)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#6)]

14. <span data-ttu-id="92b41-126">En haut du fichier, importez les espaces de noms System.ComponentModel et System.Threading.</span><span class="sxs-lookup"><span data-stu-id="92b41-126">At the top of the file, import the System.ComponentModel and System.Threading namespaces.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#7)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#7)]

15. <span data-ttu-id="92b41-127">Appuyez sur **F6** pour générer la solution, puis appuyez sur **Ctrl**+**F5** pour exécuter l’application en dehors du débogueur.</span><span class="sxs-lookup"><span data-stu-id="92b41-127">Press **F6** to build the solution, and then press **Ctrl**+**F5** to run the application outside the debugger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92b41-128">Si vous appuyez sur **F5** pour exécuter l’application sous le débogueur, l’exception levée dans le `TimeConsumingOperation` méthode est interceptée et affichée par le débogueur.</span><span class="sxs-lookup"><span data-stu-id="92b41-128">If you press **F5** to run the application under the debugger, the exception raised in the `TimeConsumingOperation` method is caught and displayed by the debugger.</span></span> <span data-ttu-id="92b41-129">Lorsque vous exécutez l’application en dehors du débogueur, le <xref:System.ComponentModel.BackgroundWorker> gère l’exception et met en cache dans le <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> propriété de la <xref:System.ComponentModel.RunWorkerCompletedEventArgs>.</span><span class="sxs-lookup"><span data-stu-id="92b41-129">When you run the application outside the debugger, the <xref:System.ComponentModel.BackgroundWorker> handles the exception and caches it in the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> property of the <xref:System.ComponentModel.RunWorkerCompletedEventArgs>.</span></span>

16. <span data-ttu-id="92b41-130">Cliquez sur le **Démarrer** bouton pour exécuter une opération asynchrone, puis cliquez sur le **Annuler** bouton pour arrêter une opération asynchrone en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="92b41-130">Click the **Start** button to run an asynchronous operation, and then click the **Cancel** button to stop a running asynchronous operation.</span></span>

     <span data-ttu-id="92b41-131">Le résultat de chaque opération est affiché dans un <xref:System.Windows.Forms.MessageBox>.</span><span class="sxs-lookup"><span data-stu-id="92b41-131">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>

## <a name="next-steps"></a><span data-ttu-id="92b41-132">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="92b41-132">Next steps</span></span>

- <span data-ttu-id="92b41-133">Implémenter un formulaire qui signale la progression au fur et une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="92b41-133">Implement a form that reports progress as an asynchronous operation proceeds.</span></span> <span data-ttu-id="92b41-134">Pour plus d'informations, voir [Procédure : Implémenter un formulaire qui utilise une opération d’arrière-plan](how-to-implement-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="92b41-134">For more information, see [How to: Implement a Form That Uses a Background Operation](how-to-implement-a-form-that-uses-a-background-operation.md).</span></span>

- <span data-ttu-id="92b41-135">Implémentez une classe qui prend en charge le modèle asynchrone pour les composants.</span><span class="sxs-lookup"><span data-stu-id="92b41-135">Implement a class that supports the Asynchronous Pattern for Components.</span></span> <span data-ttu-id="92b41-136">Pour plus d’informations, consultez [implémenter le modèle asynchrone basé sur événement](../../../standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern.md).</span><span class="sxs-lookup"><span data-stu-id="92b41-136">For more information, see [Implementing the Event-based Asynchronous Pattern](../../../standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="92b41-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92b41-137">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="92b41-138">Guide pratique pour implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="92b41-138">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
- [<span data-ttu-id="92b41-139">Guide pratique pour exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="92b41-139">How to: Run an Operation in the Background</span></span>](how-to-run-an-operation-in-the-background.md)
- [<span data-ttu-id="92b41-140">Composant BackgroundWorker</span><span class="sxs-lookup"><span data-stu-id="92b41-140">BackgroundWorker Component</span></span>](backgroundworker-component.md)
