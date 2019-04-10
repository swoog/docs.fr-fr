---
title: 'Procédure : ajouter, charger, enregistrer et annuler des boutons dans le contrôle BindingNavigator de Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], manipulating
- BindingNavigator control [Windows Forms], adding buttons
ms.assetid: faa33042-186e-4bb2-8798-17ceb987ec62
ms.openlocfilehash: 4d5cc91ca8bf71b2d5893f591652d777041e1a4d
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59304777"
---
# <a name="how-to-add-load-save-and-cancel-buttons-to-the-windows-forms-bindingnavigator-control"></a>Procédure : ajouter, charger, enregistrer et annuler des boutons dans le contrôle BindingNavigator de Windows Forms
Le <xref:System.Windows.Forms.BindingNavigator> contrôle est à usage spécial <xref:System.Windows.Forms.ToolStrip> contrôle qui est destiné à la navigation et la manipulation des contrôles liés aux données sur votre formulaire.  
  
 S’agissant d’un <xref:System.Windows.Forms.ToolStrip> contrôle, le <xref:System.Windows.Forms.BindingNavigator> composant peut être facilement modifié pour inclure des commandes supplémentaires ou alternatives pour l’utilisateur.  
  
 Dans la procédure suivante, un <xref:System.Windows.Forms.TextBox> contrôle est lié aux données et le <xref:System.Windows.Forms.ToolStrip> contrôle qui est ajouté au formulaire est modifié pour inclure la charge, enregistrer et les boutons d’annulation.  
  
### <a name="to-add-load-save-and-cancel-buttons-to-the-bindingnavigator-component"></a>Pour ajouter la charge, enregistrer et annuler des boutons au composant BindingNavigator  
  
1. Ajoutez un contrôle <xref:System.Windows.Forms.TextBox> à votre formulaire.  
  
2. Lier à un <xref:System.Windows.Forms.BindingSource>, qui est lié à une source de données. Pour cet exemple, le <xref:System.Windows.Forms.BindingSource> est lié à une base de données.  
  
3. Une fois que l’adaptateur de jeu de données et de table sont générées, faites glisser un <xref:System.Windows.Forms.BindingNavigator> contrôle au formulaire.  
  
4. Définir le <xref:System.Windows.Forms.BindingNavigator> du contrôle <xref:System.Windows.Forms.BindingNavigator.BindingSource%2A> propriété le <xref:System.Windows.Forms.BindingSource> sur le formulaire qui est lié aux contrôles.  
  
5. Sélectionnez le contrôle <xref:System.Windows.Forms.BindingNavigator>.  
  
6. Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) afin que la **tâches BindingNavigator** boîte de dialogue s’affiche et sélectionnez **modifier des éléments**.  
  
     Le **éditeur de collections Items** s’affiche.  
  
7. Dans le **éditeur de collections Items**, procédez comme suit :  
  
    1.  Ajouter un <xref:System.Windows.Forms.ToolStripSeparator> et trois <xref:System.Windows.Forms.ToolStripButton> éléments en sélectionnant le type approprié de <xref:System.Windows.Forms.ToolStripItem> et en cliquant sur le **ajouter** bouton.  
  
    2.  Définir le <xref:System.Windows.Forms.ToolStripItem.Name%2A> propriété des boutons pour **LoadButton**, **SaveButton**, et **CancelButton**, respectivement.  
  
    3.  Définir le <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriété des boutons pour **charge**, **enregistrer**, et **Annuler**.  
  
    4.  Définir le <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> propriété pour chacun des boutons pour **texte**. Vous pouvez également définir cette propriété **Image** ou **ImageAndText**et définir l’image à afficher dans le <xref:System.Windows.Forms.ToolStripItem.Image%2A> propriété.  
  
    5.  Cliquez sur **OK** pour fermer la boîte de dialogue. Les boutons sont ajoutés à la <xref:System.Windows.Forms.ToolStrip>.  
  
8. Avec le bouton droit de la forme et choisissez **afficher le Code**.  
  
9. Dans l’éditeur de Code, recherchez la ligne de code qui charge les données dans l’adaptateur de table. Ce code a été généré lorsque vous configurez la liaison de données à l’étape 2. Le code doit être similaire à ce qui suit : `TableAdapterName.Fill(DataSetName.TableName)`. Il figurera très probablement se trouver dans le formulaire <xref:System.Windows.Forms.Form.Load> événement.  
  
10. Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événements de la **charge** <xref:System.Windows.Forms.ToolStripButton> créé précédemment et de déplacer ce code de chargement des données dedans.  
  
     Votre code doit maintenant ressembler à ce qui suit :  
  
    ```vb  
    Private Sub LoadButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles LoadButton.Click  
        TableAdapterName.Fill(DataSetName.TableName)  
    End Sub  
    ```  
  
    ```csharp  
    private void LoadButton_Click(System.Object sender,   
        System.EventArgs e)  
    {  
        TableAdapterName.Fill(DataSetName.TableName);  
    }  
    ```  
  
11. Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événements de la **enregistrer** <xref:System.Windows.Forms.ToolStripButton> vous avez créé précédemment et écrire du code pour mettre à jour les données dans la table, le contrôle est lié à.  
  
    ```vb  
    Private Sub SaveButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles SaveButton.Click  
        TableAdapterName.Update(DataSetName.TableName)  
    End Sub  
    ```  
  
    ```csharp  
    private void SaveButton_Click(System.Object sender,   
        System.EventArgs e)  
    {  
        TableAdapterName.Update(DataSetName.TableName);  
    }  
    ```  
  
    > [!NOTE]
    > Dans certains cas, le <xref:System.Windows.Forms.BindingNavigator> composant aura déjà un **enregistrer** bouton, mais aucun code n’aura été généré par le Concepteur de formulaires Windows. Dans ce cas, vous pouvez placer le code précédent dans le <xref:System.Windows.Forms.ToolStripItem.Click> Gestionnaire d’événements pour ce bouton, au lieu de créer un bouton entièrement nouveau sur le <xref:System.Windows.Forms.ToolStrip>. Toutefois, le bouton est désactivé par défaut, vous devez donc définir la <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> propriété du bouton sur `true` pour que le bouton fonctionne correctement.
  
12. Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événements de la **Annuler** <xref:System.Windows.Forms.ToolStripButton> créé précédemment et d’écrire du code pour annuler les modifications apportées à l’enregistrement de données qui s’affiche.  
  
    ```vb  
    Private Sub CancelButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles CancelButton.Click  
        BindingSourceName.CancelEdit()  
    End Sub  
    ```  
  
    ```csharp  
    private void CancelButton_Click(System.Object sender, System.EventArgs e)  
    {  
        BindingSourceName.CancelEdit();  
    }  
    ```  
  
    > [!NOTE]
    >  Le <xref:System.Windows.Forms.BindingSource.CancelEdit%2A> méthode porte sur la ligne de données. Enregistrer les modifications apportées pendant l’affichage de cet enregistrement individuel avant de naviguer jusqu'à l’enregistrement suivant.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.ToolStrip>
- [BindingNavigator, contrôle](bindingnavigator-control-windows-forms.md)
- [Vue d'ensemble du composant BindingSource](bindingsource-component-overview.md)
