---
title: 'Procédure : Télécharger un fichier en arrière-plan'
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
ms.openlocfilehash: e31008bcc9580c582effa3f0131a07aa4541db6f
ms.sourcegitcommit: af0a22a4eb11bbcd33baec49150d551955b50a16
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56260996"
---
# <a name="how-to-download-a-file-in-the-background"></a>Procédure : Télécharger un fichier en arrière-plan
Le téléchargement de fichier est une tâche courante et il est souvent utile d’exécuter cette opération potentiellement longue sur un thread séparé. Utilisez le composant <xref:System.ComponentModel.BackgroundWorker> pour accomplir cette tâche avec très peu de code.  
  
## <a name="example"></a>Exemple  
 L'exemple de code suivant montre comment utiliser un composant <xref:System.ComponentModel.BackgroundWorker> pour charger un fichier XML à partir d'une URL. Lorsque l’utilisateur clique sur le **télécharger** bouton, le <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements appelle la <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> méthode d’un <xref:System.ComponentModel.BackgroundWorker> composant pour démarrer l’opération de téléchargement. Le bouton est désactivé pendant toute la durée du téléchargement, puis il est réactivé une fois le téléchargement terminé. Un <xref:System.Windows.Forms.MessageBox> affiche le contenu du fichier.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#1)]  
  
 **Téléchargement du fichier**  
  
 Le fichier est téléchargé sur le thread de travail du composant <xref:System.ComponentModel.BackgroundWorker>, qui exécute le gestionnaire d'événements <xref:System.ComponentModel.BackgroundWorker.DoWork>. Ce thread démarre quand votre code appelle la méthode <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#3](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#3)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#3](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#3)]  
  
 **Attente de la fin d’un BackgroundWorker**  
  
 Le gestionnaire d’événements `downloadButton_Click` illustre comment attendre qu’un composant <xref:System.ComponentModel.BackgroundWorker> ait terminé sa tâche asynchrone.  
  
 Si vous souhaitez seulement que l'application réponde aux événements et que vous ne souhaitez pas effectuer de travail dans le thread principal en attendant que le thread d'arrière-plan se termine, quittez simplement le gestionnaire.  
  
 Si vous souhaitez continuer à travailler dans le thread principal, utilisez la propriété <xref:System.ComponentModel.BackgroundWorker.IsBusy%2A> pour déterminer si le thread <xref:System.ComponentModel.BackgroundWorker> est toujours en cours d'exécution. Dans l'exemple, une barre de progression est mise à jour pendant le téléchargement. Veillez à appeler la méthode <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType> pour que l'interface utilisateur reste réactive.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#2)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#2)]  
  
 **Affichage du résultat**  
  
 La méthode `backgroundWorker1_RunWorkerCompleted` gère l'événement <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> et est appelée quand l'opération d'arrière-plan est terminée. Cette méthode vérifie d'abord la propriété <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType>. Si <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> est `null`, cette méthode affiche le contenu du fichier. Elle active ensuite le bouton de téléchargement, qui a été désactivé quand le téléchargement a commencé, et elle réinitialise la barre de progression.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#4](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#4)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#4](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   Références aux assemblys System.Drawing, System.Windows.Forms et System.Xml.  
  
 Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Vérifiez toujours la propriété <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> dans votre gestionnaire d'événements <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> avant d'accéder à la propriété <xref:System.ComponentModel.RunWorkerCompletedEventArgs.Result%2A?displayProperty=nameWithType> ou à tout autre objet qui peut avoir été affecté par le gestionnaire d'événements <xref:System.ComponentModel.BackgroundWorker.DoWork>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.ComponentModel.BackgroundWorker>
- [Guide pratique pour exécuter une opération en arrière-plan](../../../../docs/framework/winforms/controls/how-to-run-an-operation-in-the-background.md)
- [Guide pratique pour implémenter un formulaire qui utilise une opération d’arrière-plan](../../../../docs/framework/winforms/controls/how-to-implement-a-form-that-uses-a-background-operation.md)
