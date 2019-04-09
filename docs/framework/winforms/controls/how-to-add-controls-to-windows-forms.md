---
title: 'Procédure : ajouter des contrôles à des Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, adding to form
- controls [Windows Forms], adding
ms.assetid: 2af86001-9d62-4154-87fb-66db2c3cd9fd
ms.openlocfilehash: 72b5931a79284a93a4e0fdf3cb2cc3b03157f5f7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59106481"
---
# <a name="how-to-add-controls-to-windows-forms"></a>Procédure : ajouter des contrôles à des Windows Forms
La plupart des formulaires sont conçus en ajoutant des contrôles à la surface du formulaire pour définir une interface utilisateur (IU). Un *contrôle* est un composant d’un formulaire utilisé pour afficher des informations ou accepter l’entrée d’utilisateur. Pour plus d’informations sur les contrôles, consultez [des contrôles Windows Forms](index.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-draw-a-control-on-a-form"></a>Pour dessiner un contrôle sur un formulaire  
  
1.  Ouvrez le formulaire. Pour plus d'informations, voir [Procédure : Afficher des Windows Forms dans le concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).  
  
2.  Dans le **boîte à outils**, cliquez sur le contrôle que vous souhaitez ajouter à votre formulaire.  
  
3.  Dans le formulaire, cliquez sur l’emplacement du coin supérieur gauche du contrôle à localiser et faites glisser vers l’emplacement de l’angle inférieur droit du contrôle à localiser.  
  
     Le contrôle est ajouté au formulaire avec la taille et l’emplacement spécifié.  
  
    > [!NOTE]
    >  Chaque contrôle a une taille par défaut définie. Vous pouvez ajouter un contrôle à votre formulaire dans la taille du contrôle par défaut en le faisant glisser à partir de la **boîte à outils** au formulaire.  
  
### <a name="to-drag-a-control-to-a-form"></a>Pour faire glisser un contrôle à un formulaire  
  
1.  Ouvrez le formulaire. Pour plus d'informations, voir [Procédure : Afficher des Windows Forms dans le concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).  
  
2.  Dans le **boîte à outils**, cliquez sur le contrôle souhaité et faites-le glisser vers votre formulaire.  
  
     Le contrôle est ajouté au formulaire à l’emplacement spécifié dans sa taille par défaut.  
  
    > [!NOTE]
    >  Vous pouvez double-cliquer sur un contrôle dans le **boîte à outils** pour l’ajouter à l’angle supérieur gauche du formulaire dans sa taille par défaut.  
  
     Vous pouvez également ajouter dynamiquement des contrôles à un formulaire au moment de l’exécution. Dans l’exemple de code suivant, un <xref:System.Windows.Forms.TextBox> contrôle sera ajouté au formulaire quand un <xref:System.Windows.Forms.Button> clic sur le contrôle.  
  
    > [!NOTE]
    >  La procédure suivante requiert l’existence d’un formulaire avec un **bouton** contrôle, `Button1`déjà placé dessus.  
  
### <a name="to-add-a-control-to-a-form-programmatically"></a>Pour ajouter un contrôle à un formulaire par programmation  
  
1.  Dans la méthode qui gère le bouton `Click` événement au sein de la classe de votre formulaire, insertion code similaire à ce qui suit pour ajouter une référence à votre variable de contrôle, définissez le contrôle `Location`et ajouter le contrôle.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       Dim MyText As New TextBox()  
       MyText.Location = New Point(25, 25)  
       Me.Controls.Add(MyText)  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)   
    {  
       TextBox myText = new TextBox();  
       myText.Location = new Point(25,25);  
       this.Controls.Add (myText);  
    }  
    ```  
  
    ```cpp  
    private:  
      System::Void button1_Click(System::Object ^  sender,  
        System::EventArgs ^  e)  
      {  
        TextBox ^ myText = gcnew TextBox();  
        myText->Location = Point(25,25);  
        this->Controls->Add(myText);  
      }  
    ```  
  
    > [!NOTE]
    >  Vous pouvez également ajouter le code pour initialiser d’autres propriétés du contrôle.  
  
    > [!IMPORTANT]
    >  Vous pouvez exposer votre ordinateur local à un risque de sécurité via le réseau en référençant un malveillant `UserControl`. Il s’agit uniquement d’un problème dans le cas d’une personne malveillante, création d’un contrôle personnalisé causer des dommages, que vous suivi par inadvertance l’ajout à votre projet.  
  
## <a name="see-also"></a>Voir aussi

- [contrôles Windows Forms](index.md)
- [Disposition des contrôles dans les Windows Forms](arranging-controls-on-windows-forms.md)
- [Procédure : redimensionner des contrôles dans des Windows Forms](how-to-resize-controls-on-windows-forms.md)
- [Procédure : définir le texte affiché par un contrôle Windows Forms](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [Contrôles à utiliser dans les Windows Forms](controls-to-use-on-windows-forms.md)
