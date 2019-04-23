---
title: 'Procédure pas à pas : mise à jour des informations de barre d’état au moment de l’exécution'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- status bars [Windows Forms], updating at run time
- status bars [Windows Forms], refreshing panels
- StatusBar control [Windows Forms], refreshing panels
- panels [Windows Forms], refreshing status bar
ms.assetid: cc2abb06-c082-49f7-a5a3-2fd1bbcb58d1
ms.openlocfilehash: 7beae9bb886c7c79d4d97375887bfecb0c2a40c1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59333312"
---
# <a name="walkthrough-updating-status-bar-information-at-run-time"></a>Procédure pas à pas : mise à jour des informations de barre d’état au moment de l’exécution
> [!IMPORTANT]
>  Le <xref:System.Windows.Forms.StatusStrip> et <xref:System.Windows.Forms.ToolStripStatusLabel> contrôles remplacent et ajoutent des fonctionnalités à la <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôle ; Toutefois, le <xref:System.Windows.Forms.StatusBar> et <xref:System.Windows.Forms.StatusBarPanel> contrôles ont été conservés pour la compatibilité descendante et une utilisation ultérieure, si vous Choisissez.  
  
 Il arrive souvent qu’un programme vous demande de mettre à jour dynamiquement le contenu des panneaux de la barre d’état au moment de l’exécution en cas de modification de l’état de l’application ou de toute autre interaction utilisateur. Il s’agit d’un moyen couramment utilisé pour indiquer aux utilisateurs que des touches telles que Verr. maj, Verr. num ou Arrêt défil sont activées, ou pour fournir la date ou une horloge pour référence.  
  
 Dans l’exemple suivant, vous allez utiliser une instance de la <xref:System.Windows.Forms.StatusBarPanel> classe pour héberger une horloge.  
  
### <a name="to-get-the-status-bar-ready-for-updating"></a>Pour préparer la mise à jour de la barre d’état  
  
1. Créez un nouveau Windows Form.  
  
2. Ajoutez un contrôle <xref:System.Windows.Forms.StatusBar> à votre formulaire. Pour plus d’informations, consultez [Guide pratique pour Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
3. Ajoutez un panneau de barre d’état à votre <xref:System.Windows.Forms.StatusBar> contrôle. Pour plus d’informations, consultez [Guide pratique pour Ajouter des panneaux à un contrôle StatusBar](how-to-add-panels-to-a-statusbar-control.md).  
  
4. Pour le <xref:System.Windows.Forms.StatusBar> contrôle que vous avez ajouté à votre formulaire, définissez la <xref:System.Windows.Forms.StatusBar.ShowPanels%2A> propriété `true`.  
  
5. Ajouter un formulaire Windows <xref:System.Windows.Forms.Timer> composant au formulaire.  
  
    > [!NOTE]
    >  Les formulaires Windows <xref:System.Windows.Forms.Timer?displayProperty=nameWithType> composant est conçu pour un environnement Windows Forms. Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).  
  
6. Affectez à la propriété <xref:System.Windows.Forms.Timer.Enabled%2A> la valeur `true`.  
  
7. Définir le <xref:System.Windows.Forms.Timer.Interval%2A> propriété de la <xref:System.Windows.Forms.Timer> à 30000.  
  
    > [!NOTE]
    >  Le <xref:System.Windows.Forms.Timer.Interval%2A> propriété de la <xref:System.Windows.Forms.Timer> composant est défini sur 30 secondes (30 000 millisecondes) pour garantir qu’une heure précise de l’heure affichée.  
  
### <a name="to-implement-the-timer-to-update-the-status-bar"></a>Pour implémenter la minuterie afin de mettre à jour la barre d’état  
  
1. Insérez le code suivant dans le Gestionnaire d’événements de la <xref:System.Windows.Forms.Timer> composant à mettre à jour le panneau de la <xref:System.Windows.Forms.StatusBar> contrôle.  
  
    ```vb  
    Private Sub Timer1_Tick(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Timer1.Tick  
       StatusBar1.Panels(0).Text = Now.ToShortTimeString  
    End Sub  
    ```  
  
    ```csharp  
    private void timer1_Tick(object sender, System.EventArgs e)  
    {  
       statusBar1.Panels[0].Text = DateTime.Now.ToShortTimeString();  
    }  
    ```  
  
    ```cpp  
    private:  
      System::Void timer1_Tick(System::Object ^ sender,  
        System::EventArgs ^ e)  
      {  
        statusBar1->Panels[0]->Text =  
          DateTime::Now.ToShortTimeString();  
      }  
    ```  
  
     À ce stade, vous êtes prêt à exécuter l’application et à voir apparaître l’horloge dans le panneau de la barre d’état.  
  
### <a name="to-test-the-application"></a>Pour tester l'application  
  
1. Déboguez l’application et appuyez sur la touche F5 pour l’exécuter. Pour plus d’informations sur le débogage, consultez l’article [Débogage dans Visual Studio](/visualstudio/debugger/debugging-in-visual-studio).  
  
    > [!NOTE]
    >  L’horloge apparaîtra dans la barre d’état au bout de 30 secondes environ. Cela permet d’obtenir l’heure la plus précise possible. À l’inverse, pour que l’horloge s’affiche plus vite, vous pouvez réduire la valeur de la <xref:System.Windows.Forms.Timer.Interval%2A> propriété définie à l’étape 7 de la procédure précédente.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Guide pratique pour Ajouter des panneaux à un contrôle StatusBar](how-to-add-panels-to-a-statusbar-control.md)
- [Guide pratique pour Déterminer l’utilisateur a cliqué sur le panneau du contrôle StatusBar Windows Forms](determine-which-panel-wf-statusbar-control-was-clicked.md)
- [Vue d’ensemble du contrôle StatusBar](statusbar-control-overview-windows-forms.md)
