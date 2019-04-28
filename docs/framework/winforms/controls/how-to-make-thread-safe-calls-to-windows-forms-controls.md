---
title: 'Procédure : Effectuer des appels thread-safe aux contrôles Windows Forms'
ms.date: 02/19/2019
dev_langs:
- csharp
- vb
f1_keywords:
- EHInvalidOperation.WinForms.IllegalCrossThreadCall
helpviewer_keywords:
- thread safety [Windows Forms], calling controls [Windows Forms]
- calling controls [Windows Forms], thread safety [Windows Forms]
- CheckForIllegalCrossThreadCalls property [Windows Forms]
- Windows Forms controls [Windows Forms], multithreading
- BackgroundWorker class [Windows Forms], examples
- threading [Windows Forms], cross-thread calls
- controls [Windows Forms], multithreading
ms.assetid: 138f38b6-1099-4fd5-910c-390b41cbad35
ms.openlocfilehash: 3211df1f0e585780039471b80b5b913613ad9bbd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61913794"
---
# <a name="how-to-make-thread-safe-calls-to-windows-forms-controls"></a>Procédure : Effectuer des appels thread-safe aux contrôles Windows Forms

Le traitement multithread peut améliorer les performances des applications Windows Forms, mais l’accès à des contrôles Windows Forms n’est pas thread-safe. Le traitement multithread peut exposer votre code à des bogues très sérieux et complexes. Deux ou plusieurs threads manipuler un contrôle peuvent forcer le contrôle dans un état incohérent et conduire à des conditions de concurrence, blocages et se fige ou se bloque. Si vous implémentez le multithreading dans votre application, veillez à appeler les contrôles inter-threads de manière thread-safe. Pour plus d’informations, consultez [meilleures pratiques pour le threading managé](../../../standard/threading/managed-threading-best-practices.md). 

Il existe deux façons d’appeler en toute sécurité un contrôle Windows Forms à partir d’un thread qui n’a pas de créer ce contrôle. Vous pouvez utiliser la <xref:System.Windows.Forms.Control.Invoke%2A?displayProperty=fullName> méthode à appeler un délégué créé dans le thread principal, qui à son tour appelle le contrôle. Ou, vous pouvez implémenter un <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>, qui utilise un modèle événementiel de séparer le travail effectué dans le thread d’arrière-plan à partir de la création de rapports sur les résultats. 

## <a name="unsafe-cross-thread-calls"></a>Appels inter-threads non sécurisés

Il est risqué d’appeler un contrôle directement à partir d’un thread qui n’a pas de le créer. L’extrait de code suivant illustre un appel unsafe à la <xref:System.Windows.Forms.TextBox?displayProperty=nameWithType> contrôle. Le `Button1_Click` Gestionnaire d’événements crée un nouveau `WriteTextUnsafe` thread, qui définit le thread principal <xref:System.Windows.Forms.TextBox.Text%2A?displayProperty=nameWithType> propriété directement. 

```csharp
private void Button1_Click(object sender, EventArgs e)
{
    thread2 = new Thread(new ThreadStart(WriteTextUnsafe));
    thread2.Start();
}
private void WriteTextUnsafe()
{
    textBox1.Text = "This text was set unsafely.";
}
```

```vb
Private Sub Button1_Click(ByVal sender As Object, e As EventArgs) Handles Button1.Click
    Thread2 = New Thread(New ThreadStart(AddressOf WriteTextUnsafe))
    Thread2.Start()
End Sub

Private Sub WriteTextUnsafe()
    TextBox1.Text = "This text was set unsafely."
End Sub
```

Le débogueur Visual Studio détecte ces appels de threads unsafe en déclenchant une <xref:System.InvalidOperationException> avec le message, **opération inter-threads non valide. Contrôle » « accessible à partir d’un thread autre que le thread de création.** Le <xref:System.InvalidOperationException> toujours se produit pour les appels inter-threads non sécurisés pendant le débogage de Visual Studio et peut se produire lors de l’exécution de l’application. Vous devez corriger le problème, mais vous pouvez désactiver l’exception en définissant le <xref:System.Windows.Forms.Control.CheckForIllegalCrossThreadCalls%2A?displayProperty=nameWithType> propriété `false`.

## <a name="safe-cross-thread-calls"></a>Appels inter-thread-safe 

Les exemples de code suivants montrent deux façons d’appeler en toute sécurité un contrôle Windows Forms à partir d’un thread qui n’a pas créez-le : 
1. Le <xref:System.Windows.Forms.Control.Invoke%2A?displayProperty=fullName> (méthode), qui appelle un délégué à partir du thread principal pour appeler le contrôle. 
2. Un <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType> composant, qui offre un modèle piloté par les événements. 

Dans les deux exemples, l’en veille à la thread d’arrière-plan pendant une seconde simuler en cours de développement dans ce thread. 

Vous pouvez générer et exécuter ces exemples en tant qu’applications .NET Framework à partir de la C# ou ligne de commande de Visual Basic. Pour plus d’informations, consultez [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md) ou [construire à partir de la ligne de commande (Visual Basic)](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md). 

À compter de .NET Core 3.0, vous pouvez également générer et exécuter les exemples comme des applications .NET Core de Windows à partir d’un dossier qui a un .NET Core Windows Forms  *\<nom du dossier > .csproj* fichier projet. 

## <a name="example-use-the-invoke-method-with-a-delegate"></a>Exemple : Utilisez la méthode Invoke avec un délégué

L’exemple suivant illustre un modèle pour garantir des appels thread-safe à un contrôle Windows Forms. Elle interroge le <xref:System.Windows.Forms.Control.InvokeRequired%2A?displayProperty=fullName> propriété, qui compare le contrôle de création d’ID de thread à l’ID de thread appelant. Si les ID de thread sont identiques, il appelle le contrôle directement. Si l’ID de thread sont différents, il appelle le <xref:System.Windows.Forms.Control.Invoke%2A?displayProperty=nameWithType> méthode avec un délégué à partir du thread principal, ce qui rend l’appel réel au contrôle.

Le `SafeCallDelegate` Active paramètre la <xref:System.Windows.Forms.TextBox> du contrôle <xref:System.Windows.Forms.TextBox.Text%2A> propriété. Le `WriteTextSafe` requêtes de la méthode <xref:System.Windows.Forms.Control.InvokeRequired%2A>. Si <xref:System.Windows.Forms.Control.InvokeRequired%2A> retourne `true`, `WriteTextSafe` transmet le `SafeCallDelegate` à la <xref:System.Windows.Forms.Control.Invoke%2A> méthode pour effectuer l’appel réel au contrôle. Si <xref:System.Windows.Forms.Control.InvokeRequired%2A> retourne `false`, `WriteTextSafe` définit le <xref:System.Windows.Forms.TextBox.Text%2A?displayProperty=nameWithType> directement. Le `Button1_Click` Gestionnaire d’événements crée le nouveau thread et exécute le `WriteTextSafe` (méthode). 

 [!code-csharp[ThreadSafeCalls#1](~/samples/snippets/winforms/thread-safe/example1/cs/Form1.cs)]
 [!code-vb[ThreadSafeCalls#1](~/samples/snippets/winforms/thread-safe/example1/vb/Form1.vb)]  

## <a name="example-use-a-backgroundworker-event-handler"></a>Exemple : Utiliser un gestionnaire d’événements de BackgroundWorker

Un moyen simple pour implémenter le multithreading est avec le <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType> composant, qui utilise un modèle événementiel. Le thread d’arrière-plan s’exécute le <xref:System.ComponentModel.BackgroundWorker.DoWork?displayProperty=nameWithType> événement, qui n’interagit pas avec le thread principal. Le thread principal s’exécute le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged?displayProperty=nameWithType> et <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted?displayProperty=nameWithType> des gestionnaires d’événements, qui peuvent appeler les contrôles du thread principal.

Pour effectuer un appel thread-safe à l’aide de <xref:System.ComponentModel.BackgroundWorker>, créez une méthode dans le thread d’arrière-plan pour effectuer le travail, puis liez-le à le <xref:System.ComponentModel.BackgroundWorker.DoWork> événement. Créer une autre méthode dans le thread principal pour signaler les résultats du travail en arrière-plan, puis liez-le à le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> ou <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> événement. Pour démarrer le thread d’arrière-plan, appelez <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A?displayProperty=nameWithType>. 

L’exemple utilise le <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Gestionnaire d’événements pour définir le <xref:System.Windows.Forms.TextBox> du contrôle <xref:System.Windows.Forms.TextBox.Text%2A> propriété. Pour obtenir un exemple utilisant le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événement, consultez <xref:System.ComponentModel.BackgroundWorker>. 

 [!code-csharp[ThreadSafeCalls#2](~/samples/snippets/winforms/thread-safe/example2/cs/Form1.cs)]
 [!code-vb[ThreadSafeCalls#2](~/samples/snippets/winforms/thread-safe/example2/vb/Form1.vb)]  

## <a name="see-also"></a>Voir aussi

- <xref:System.ComponentModel.BackgroundWorker>
- [Guide pratique pour Exécuter une opération en arrière-plan](how-to-run-an-operation-in-the-background.md)
- [Guide pratique pour Implémenter un formulaire qui utilise une opération d’arrière-plan](how-to-implement-a-form-that-uses-a-background-operation.md)
- [Développer des contrôles Windows Forms personnalisés avec le .NET Framework](developing-custom-windows-forms-controls.md)
