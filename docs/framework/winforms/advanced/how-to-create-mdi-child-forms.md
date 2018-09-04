---
title: 'Comment : créer des formulaires MDI enfants'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- MDI [Windows Forms], creating forms
- child forms
ms.assetid: 164b69bb-2eca-4339-ada3-0679eb2c6dda
ms.openlocfilehash: bdfbe59ef779de242e32be11ca28c84f68437240
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43658923"
---
# <a name="how-to-create-mdi-child-forms"></a>Comment : créer des formulaires MDI enfants
Formulaires MDI enfants constituent un élément essentiel de [Applications d’Interface multidocument (MDI)](../../../../docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md), car ils représentent le centre d’intervention de l’utilisateur.  
  
 Dans la procédure suivante, vous allez créer un formulaire MDI enfant qui affiche un contrôle <xref:System.Windows.Forms.RichTextBox>, semblable à la plupart des applications de traitement de texte. La remplacement du contrôle <xref:System.Windows.Forms> par d'autres contrôles, tels que le contrôle <xref:System.Windows.Forms.DataGridView> ou une combinaison de contrôles, vous permet de créer des fenêtres MDI enfants (et, par extension, des applications MDI) avec diverses possibilités.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-mdi-child-forms"></a>Pour créer des formulaires MDI enfants  
  
1.  Créez un projet Windows Forms. Dans **les propriétés Windows** pour le formulaire, définissez son <xref:System.Windows.Forms.Form.IsMdiContainer%2A> propriété `true`et son `WindowsState` propriété `Maximized`.  
  
     Ainsi, vous désignez le formulaire comme le conteneur MDI des fenêtres enfants.  
  
2.  Faites glisser un contrôle <xref:System.Windows.Forms.MenuStrip> de la `Toolbox` vers le formulaire. Définissez ses `Text` propriété **fichier**.  
  
3.  Cliquez sur les points de suspension (...) à côté du **éléments** propriété, puis cliquez sur **ajouter** pour ajouter deux éléments de menu ToolStrip enfants outil. Définir le `Text` propriété de ces éléments **New** et **fenêtre**.  
  
4.  Dans **l’Explorateur de solutions**, cliquez sur le projet, pointez sur **ajouter**, puis sélectionnez **ajouter un nouvel élément**.  
  
5.  Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez **Windows Form** (en Visual Basic ou Visual c#) ou **Windows Forms Application (.NET)** (dans [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) à partir de la  **Modèles** volet. Dans le **nom** boîte, nommez le formulaire **Form2**. Cliquez sur le **Open** pour ajouter le formulaire au projet.  
  
    > [!NOTE]
    >  Le formulaire MDI enfant que vous avez créé lors de cette étape est un Windows Form standard. Il a donc une propriété <xref:System.Windows.Forms.Form.Opacity%2A>, ce qui vous permet de contrôler la transparence du formulaire. Cependant, la propriété <xref:System.Windows.Forms.Form.Opacity%2A> a été conçue pour les fenêtres de niveau supérieur. Ne l'utilisez pas avec des formulaires MDI enfants, car des problèmes de peinture peuvent survenir.  
  
     Ce formulaire sera le modèle pour vos formulaires MDI enfants.  
  
     Le **Windows Forms Designer** s’ouvre et affiche **Form2**.  
  
6.  À partir de la **boîte à outils**, faites glisser un **RichTextBox** contrôle au formulaire.  
  
7.  Dans le **propriétés** fenêtre, définissez le `Anchor` propriété **supérieure, gauche** et `Dock` propriété **remplir**.  
  
     Ainsi, le contrôle <xref:System.Windows.Forms.RichTextBox> remplit complètement la zone de formulaire MDI enfant, même quand le formulaire est redimensionné.  
  
8.  Double-cliquez sur le **New** élément de menu pour créer un <xref:System.Windows.Forms.Control.Click> Gestionnaire d’événements pour celle-ci.  
  
9. Insérez du code semblable à ce qui suit pour créer un nouveau formulaire MDI enfant lorsque l’utilisateur clique sur le **New** élément de menu.  
  
    > [!NOTE]
    >  Dans l'exemple suivant, le gestionnaire d'événements gère l'événement <xref:System.Windows.Forms.Control.Click> pour `MenuItem2`. N’oubliez pas que, selon les spécificités de l’architecture de votre application, votre **New** élément de menu ne peut pas être `MenuItem2`.  
  
    ```vb  
    Protected Sub MDIChildNew_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MenuItem2.Click  
       Dim NewMDIChild As New Form2()  
       'Set the Parent Form of the Child window.  
       NewMDIChild.MdiParent = Me  
       'Display the new form.  
       NewMDIChild.Show()  
    End Sub  
    ```  
  
    ```csharp  
    protected void MDIChildNew_Click(object sender, System.EventArgs e){  
       Form2 newMDIChild = new Form2();  
       // Set the Parent Form of the Child window.  
       newMDIChild.MdiParent = this;  
       // Display the new form.  
       newMDIChild.Show();  
    }  
    ```  
  
    ```cpp  
    private:  
       void menuItem2_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          Form2^ newMDIChild = gcnew Form2();  
          // Set the Parent Form of the Child window.  
          newMDIChild->MdiParent = this;  
          // Display the new form.  
          newMDIChild->Show();  
       }  
    ```  
  
     Dans [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)], ajoutez la directive `#include` suivante en haut de Form1.h :  
  
    ```cpp  
    #include "Form2.h"  
    ```  
  
10. Dans la liste déroulante en haut de la **propriétés** fenêtre, sélectionnez la barre de menus qui correspond à la **fichier** MenuStrip et définissez le <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> propriété dans la fenêtre <xref:System.Windows.Forms.ToolStripMenuItem>.  
  
     Cela permettra le **fenêtre** menu pour conserver une liste des fenêtres MDI enfants ouvertes avec une coche en regard de la fenêtre enfant active.  
  
11. Appuyez sur F5 pour exécuter l'application. En sélectionnant **New** à partir de la **fichier** menu, vous pouvez créer des formulaires MDI enfants dont la liste sont conservées dans le **fenêtre** élément de menu.  
  
    > [!NOTE]
    >  Quand un formulaire MDI enfant a un composant <xref:System.Windows.Forms.MainMenu> (avec, généralement, une structure d'éléments de menu) et qu'il est ouvert dans un formulaire MDI parent qui a un composant <xref:System.Windows.Forms.MainMenu> (avec, généralement, une structure d'éléments de menu), les éléments de menu fusionnent automatiquement si vous avez défini la propriété <xref:System.Windows.Forms.MenuItem.MergeType%2A> (et, éventuellement, la propriété <xref:System.Windows.Forms.MenuItem.MergeOrder%2A>). Affectez la valeur <xref:System.Windows.Forms.MenuMerge.MergeItems> à la propriété <xref:System.Windows.Forms.MenuItem.MergeType%2A> des deux composants <xref:System.Windows.Forms.MainMenu> et à tous les éléments de menu du formulaire enfant. Définissez aussi la propriété <xref:System.Windows.Forms.MenuItem.MergeOrder%2A> pour que les éléments de menu des deux menus apparaissent dans l'ordre souhaité. De plus, sachez que quand vous fermez un formulaire MDI parent, chaque formulaire MDI enfant déclenche un événement <xref:System.Windows.Forms.Form.Closing> avant que l'événement <xref:System.Windows.Forms.Form.Closing> pour le parent MDI soit déclenché. L'annulation de l'événement <xref:System.Windows.Forms.Form.Closing>  d'un enfant MDI n'empêchera pas le déclenchement de l'événement <xref:System.Windows.Forms.Form.Closing> du MDI parent. Toutefois, l'argument <xref:System.ComponentModel.CancelEventArgs> pour l'événement <xref:System.Windows.Forms.Form.Closing> du MDI parent prendra la valeur `true`. Vous pouvez forcer la fermeture du MDI parent et de tous les formulaires MDI enfants en affectant la valeur `false` à l'argument <xref:System.ComponentModel.CancelEventArgs>.  
  
## <a name="see-also"></a>Voir aussi  
 [Applications d’interface multidocument (MDI, Multiple Document Interface)](../../../../docs/framework/winforms/advanced/multiple-document-interface-mdi-applications.md)  
 [Guide pratique pour créer des formulaires MDI parents](../../../../docs/framework/winforms/advanced/how-to-create-mdi-parent-forms.md)  
 [Guide pratique pour déterminer l’enfant MDI actif](../../../../docs/framework/winforms/advanced/how-to-determine-the-active-mdi-child.md)  
 [Guide pratique pour envoyer des données à l’enfant MDI actif](../../../../docs/framework/winforms/advanced/how-to-send-data-to-the-active-mdi-child.md)  
 [Guide pratique pour réorganiser des formulaires MDI enfants](../../../../docs/framework/winforms/advanced/how-to-arrange-mdi-child-forms.md)
