---
title: 'Procédure pas à pas : utilisation du contrôle MaskedTextBox'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- input [Windows Forms], controlling to ensure validity
- MaskedTextBox control [Windows Forms], walkthroughs
- MaskedTextBox control [Windows Forms], validation
- user input [Windows Forms], controlling
- text [Windows Forms], controls for input
ms.assetid: df60565e-5447-4110-92a6-be1f6ff5faa3
ms.openlocfilehash: ca505b062be8c60c1dd9b08fead4855eb1eb4cd6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59103842"
---
# <a name="walkthrough-working-with-the-maskedtextbox-control"></a>Procédure pas à pas : utilisation du contrôle MaskedTextBox
Cette procédure pas à pas décrit notamment les tâches suivantes :  
  
-   L’initialisation du <xref:System.Windows.Forms.MaskedTextBox> contrôle  
  
-   À l’aide de la <xref:System.Windows.Forms.MaskedTextBox.MaskInputRejected> Gestionnaire d’événements pour avertir l’utilisateur lorsqu’un caractère n’est pas conforme au masque  
  
-   Affecter un type à la <xref:System.Windows.Forms.MaskedTextBox.ValidatingType%2A> propriété et à l’aide de la <xref:System.Windows.Forms.MaskedTextBox.TypeValidationCompleted> pour avertir l’utilisateur lorsque la valeur qu’il essaie de valider n’est pas valide pour le type de gestionnaire d’événements  
  
## <a name="creating-the-project-and-adding-a-control"></a>Création du projet et l’ajout d’un contrôle  
  
#### <a name="to-add-a-maskedtextbox-control-to-your-form"></a>Pour ajouter un contrôle MaskedTextBox à votre formulaire  
  
1.  Ouvrez le formulaire sur lequel vous souhaitez placer le <xref:System.Windows.Forms.MaskedTextBox> contrôle.  
  
2.  Faites glisser un <xref:System.Windows.Forms.MaskedTextBox> contrôle depuis la **boîte à outils** à votre formulaire.  
  
3.  Cliquez sur le contrôle et choisissez **propriétés**. Dans le **propriétés** fenêtre, sélectionnez le **masque** propriété et cliquez sur le **...**  (suspension) en regard du nom de propriété.  
  
4.  Dans le **masque d’entrée** boîte de dialogue, sélectionnez le **Date courte** masquer et cliquez sur **OK**.  
  
5.  Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.MaskedTextBox.BeepOnError%2A> propriété `true`. Cette propriété provoque un court signal sonore est déclenché chaque fois que l’utilisateur tente d’entrer un caractère qui ne respecte pas la définition de masque.  
  
 Pour obtenir un résumé des caractères qui prend en charge de la propriété Mask, consultez la section Notes de la <xref:System.Windows.Forms.MaskedTextBox.Mask%2A> propriété.  
  
## <a name="alert-the-user-to-input-errors"></a>Alerter l’utilisateur pour les erreurs d’entrée  
  
#### <a name="add-a-balloon-tip-for-rejected-mask-input"></a>Ajouter une info-bulle pour l’entrée de masque rejetés  
  
1.  Retour à la **boîte à outils** et ajoutez un <xref:System.Windows.Forms.ToolTip> à votre formulaire.  
  
2.  Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.MaskedTextBox.MaskInputRejected> événement qui déclenche le <xref:System.Windows.Forms.ToolTip> lorsque se produit une erreur d’entrée. L’info-bulle reste visible pendant cinq secondes, ou jusqu'à ce que l’utilisateur clique dessus.  
  
    ```csharp  
    public void Form1_Load(Object sender, EventArgs e)   
    {  
        ... // Other initialization code  
        maskedTextBox1.Mask = "00/00/0000";  
        maskedTextBox1.MaskInputRejected += new MaskInputRejectedEventHandler(maskedTextBox1_MaskInputRejected)  
    }  
  
    void maskedTextBox1_MaskInputRejected(object sender, MaskInputRejectedEventArgs e)  
    {  
        toolTip1.ToolTipTitle = "Invalid Input";  
        toolTip1.Show("We're sorry, but only digits (0-9) are allowed in dates.", maskedTextBox1, maskedTextBox1.Location, 5000);  
    }  
    ```  
  
    ```vb  
    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load  
        Me.ToolTip1.IsBalloon = True  
        Me.MaskedTextBox1.Mask = "00/00/0000"  
    End Sub  
  
    Private Sub MaskedTextBox1_MaskInputRejected(sender as Object, e as MaskInputRejectedEventArgs) Handles MaskedTextBox1.MaskInputRejected  
        ToolTip1.ToolTipTitle = "Invalid Input"  
        ToolTip1.Show("We're sorry, but only digits (0-9) are allowed in dates.", MaskedTextBox1, 5000)  
    End Sub  
    ```  
  
## <a name="alert-the-user-to-a-type-that-is-not-valid"></a>Avertir l’utilisateur à un Type qui n’est pas valide  
  
#### <a name="add-a-balloon-tip-for-invalid-data-types"></a>Ajouter une info-bulle pour les types de données non valides  
  
1.  Dans votre formulaire <xref:System.Windows.Forms.Form.Load> Gestionnaire d’événements, affecter un <xref:System.Type> objet représentant le <xref:System.DateTime> type à la <xref:System.Windows.Forms.MaskedTextBox> du contrôle <xref:System.Windows.Forms.MaskedTextBox.ValidatingType%2A> propriété :  
  
    ```csharp  
    private void Form1_Load(Object sender, EventArgs e)  
    {  
        // Other code  
        maskedTextBox1.ValidatingType = typeof(System.DateTime);  
        maskedTextBox1.TypeValidationCompleted += new TypeValidationEventHandler(maskedTextBox1_TypeValidationCompleted);  
    }  
    ```  
  
    ```vb  
    Private Sub Form1_Load(sender as Object, e as EventArgs)  
        // Other code  
        MaskedTextBox1.ValidatingType = GetType(System.DateTime)  
    End Sub  
    ```  
  
2.  Ajoutez un gestionnaire d'événements pour l'événement <xref:System.Windows.Forms.MaskedTextBox.TypeValidationCompleted> :  
  
    ```csharp  
    public void maskedTextBox1_TypeValidationCompleted(object sender, TypeValidationEventArgs e)  
    {  
        if (!e.IsValidInput)  
        {  
           toolTip1.ToolTipTitle = "Invalid Date Value";  
           toolTip1.Show("We're sorry, but the value you entered is not a valid date. Please change the value.", maskedTextBox1, 5000);  
           e.Cancel = true;  
        }  
    }  
    ```  
  
    ```vb  
    Public Sub MaskedTextBox1_TypeValidationCompleted(sender as Object, e as TypeValidationEventArgs)  
        If Not e.IsValidInput Then  
           ToolTip1.ToolTipTitle = "Invalid Date Value"  
           ToolTip1.Show("We're sorry, but the value you entered is not a valid date. Please change the value.", maskedTextBox1, 5000)  
           e.Cancel = True  
        End If  
    End Sub  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.MaskedTextBox>
- [MaskedTextBox, contrôle](maskedtextbox-control-windows-forms.md)
