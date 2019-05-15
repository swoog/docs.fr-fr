---
title: 'Procédure : télécharger un fichier en arrière-plan'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BackgroundWorker component
- background tasks
- Asynchronous Pattern
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9b7bc5ae-051c-4904-9720-18f6667388bd
ms.openlocfilehash: ed7d5593a29726412f5ea75812cf5a6d800ee77a
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591707"
---
# <a name="how-to-download-a-file-in-the-background"></a><span data-ttu-id="c4244-102">Procédure : télécharger un fichier en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="c4244-102">How to: Download a File in the Background</span></span>
<span data-ttu-id="c4244-103">Le téléchargement de fichier est une tâche courante et il est souvent utile d’exécuter cette opération potentiellement longue sur un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="c4244-103">Downloading a file is a common task, and it is often useful to run this potentially time-consuming operation on a separate thread.</span></span> <span data-ttu-id="c4244-104">Utilisez le composant <xref:System.ComponentModel.BackgroundWorker> pour accomplir cette tâche avec très peu de code.</span><span class="sxs-lookup"><span data-stu-id="c4244-104">Use the <xref:System.ComponentModel.BackgroundWorker> component to accomplish this task with very little code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c4244-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4244-105">Example</span></span>  
 <span data-ttu-id="c4244-106">L'exemple de code suivant montre comment utiliser un composant <xref:System.ComponentModel.BackgroundWorker> pour charger un fichier XML à partir d'une URL.</span><span class="sxs-lookup"><span data-stu-id="c4244-106">The following code example demonstrates how to use a <xref:System.ComponentModel.BackgroundWorker> component to load an XML file from a URL.</span></span> <span data-ttu-id="c4244-107">Lorsque l’utilisateur clique sur le **télécharger** bouton, le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements appelle la <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> méthode d’un <xref:System.ComponentModel.BackgroundWorker> composant pour démarrer l’opération de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="c4244-107">When the user clicks the **Download** button, the <xref:System.Windows.Forms.Control.Click> event handler calls the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method of a <xref:System.ComponentModel.BackgroundWorker> component to start the download operation.</span></span> <span data-ttu-id="c4244-108">Le bouton est désactivé pendant toute la durée du téléchargement, puis il est réactivé une fois le téléchargement terminé.</span><span class="sxs-lookup"><span data-stu-id="c4244-108">The button is disabled for the duration of the download, and then enabled when the download is complete.</span></span> <span data-ttu-id="c4244-109">Un <xref:System.Windows.Forms.MessageBox> affiche le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="c4244-109">A <xref:System.Windows.Forms.MessageBox> displays the contents of the file.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#1)]  
  
 <span data-ttu-id="c4244-110">**Téléchargement du fichier**</span><span class="sxs-lookup"><span data-stu-id="c4244-110">**Downloading the file**</span></span>  
  
 <span data-ttu-id="c4244-111">Le fichier est téléchargé sur le thread de travail du composant <xref:System.ComponentModel.BackgroundWorker>, qui exécute le gestionnaire d'événements <xref:System.ComponentModel.BackgroundWorker.DoWork>.</span><span class="sxs-lookup"><span data-stu-id="c4244-111">The file is downloaded on the <xref:System.ComponentModel.BackgroundWorker> component's worker thread, which runs the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span> <span data-ttu-id="c4244-112">Ce thread démarre quand votre code appelle la méthode <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>.</span><span class="sxs-lookup"><span data-stu-id="c4244-112">This thread starts when your code calls the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#3)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#3)]  
  
 <span data-ttu-id="c4244-113">**Attente de la fin d’un BackgroundWorker**</span><span class="sxs-lookup"><span data-stu-id="c4244-113">**Waiting for a BackgroundWorker to finish**</span></span>  
  
 <span data-ttu-id="c4244-114">Le gestionnaire d’événements `downloadButton_Click` illustre comment attendre qu’un composant <xref:System.ComponentModel.BackgroundWorker> ait terminé sa tâche asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c4244-114">The `downloadButton_Click` event handler demonstrates how to wait for a <xref:System.ComponentModel.BackgroundWorker> component to finish its asynchronous task.</span></span>  
  
 <span data-ttu-id="c4244-115">Si vous souhaitez seulement que l'application réponde aux événements et que vous ne souhaitez pas effectuer de travail dans le thread principal en attendant que le thread d'arrière-plan se termine, quittez simplement le gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="c4244-115">If you only want the application to respond to events and do not want to do any work in the main thread while you wait for the background thread to complete, just exit the handler.</span></span>  
  
 <span data-ttu-id="c4244-116">Si vous souhaitez continuer à travailler dans le thread principal, utilisez la propriété <xref:System.ComponentModel.BackgroundWorker.IsBusy%2A> pour déterminer si le thread <xref:System.ComponentModel.BackgroundWorker> est toujours en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="c4244-116">If you want to continue doing work in the main thread, use the <xref:System.ComponentModel.BackgroundWorker.IsBusy%2A> property to determine whether the <xref:System.ComponentModel.BackgroundWorker> thread is still running.</span></span> <span data-ttu-id="c4244-117">Dans l'exemple, une barre de progression est mise à jour pendant le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="c4244-117">In the example, a progress bar is updated while the download is processing.</span></span> <span data-ttu-id="c4244-118">Veillez à appeler la méthode <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType> pour que l'interface utilisateur reste réactive.</span><span class="sxs-lookup"><span data-stu-id="c4244-118">Be sure to call the <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType> method to keep the UI responsive.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#2)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#2)]  
  
 <span data-ttu-id="c4244-119">**Affichage du résultat**</span><span class="sxs-lookup"><span data-stu-id="c4244-119">**Displaying the result**</span></span>  
  
 <span data-ttu-id="c4244-120">La méthode `backgroundWorker1_RunWorkerCompleted` gère l'événement <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> et est appelée quand l'opération d'arrière-plan est terminée.</span><span class="sxs-lookup"><span data-stu-id="c4244-120">The `backgroundWorker1_RunWorkerCompleted` method handles the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event and is called when the background operation is completed.</span></span> <span data-ttu-id="c4244-121">Cette méthode vérifie d'abord la propriété <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c4244-121">This method first checks the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="c4244-122">Si <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> est `null`, cette méthode affiche le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="c4244-122">If <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> is `null`, then this method displays the contents of the file.</span></span> <span data-ttu-id="c4244-123">Elle active ensuite le bouton de téléchargement, qui a été désactivé quand le téléchargement a commencé, et elle réinitialise la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="c4244-123">It then enables the download button, which was disabled when the download began, and it resets the progress bar.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#4)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c4244-124">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="c4244-124">Compiling the Code</span></span>  
 <span data-ttu-id="c4244-125">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="c4244-125">This example requires:</span></span>  
  
- <span data-ttu-id="c4244-126">Références aux assemblys System.Drawing, System.Windows.Forms et System.Xml.</span><span class="sxs-lookup"><span data-stu-id="c4244-126">References to the System.Drawing, System.Windows.Forms, and System.Xml assemblies.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="c4244-127">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="c4244-127">Robust Programming</span></span>  
 <span data-ttu-id="c4244-128">Vérifiez toujours la propriété <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> dans votre gestionnaire d'événements <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> avant d'accéder à la propriété <xref:System.ComponentModel.RunWorkerCompletedEventArgs.Result%2A?displayProperty=nameWithType> ou à tout autre objet qui peut avoir été affecté par le gestionnaire d'événements <xref:System.ComponentModel.BackgroundWorker.DoWork>.</span><span class="sxs-lookup"><span data-stu-id="c4244-128">Always check the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> property in your <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler before attempting to access the <xref:System.ComponentModel.RunWorkerCompletedEventArgs.Result%2A?displayProperty=nameWithType> property or any other object that may have been affected by the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4244-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4244-129">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- [<span data-ttu-id="c4244-130">Guide pratique pour exécuter une opération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="c4244-130">How to: Run an Operation in the Background</span></span>](how-to-run-an-operation-in-the-background.md)
- [<span data-ttu-id="c4244-131">Guide pratique pour implémenter un formulaire qui utilise une opération d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="c4244-131">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
