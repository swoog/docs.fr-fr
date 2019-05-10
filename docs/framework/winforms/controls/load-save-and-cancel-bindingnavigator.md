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
ms.openlocfilehash: f190bfa29af480fa104f30b21b1af517c413b838
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211575"
---
# <a name="how-to-add-load-save-and-cancel-buttons-to-the-windows-forms-bindingnavigator-control"></a><span data-ttu-id="c2c42-102">Procédure : ajouter, charger, enregistrer et annuler des boutons dans le contrôle BindingNavigator de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c2c42-102">How to: Add Load, Save, and Cancel Buttons to the Windows Forms BindingNavigator Control</span></span>

<span data-ttu-id="c2c42-103">Le <xref:System.Windows.Forms.BindingNavigator> contrôle est à usage spécial <xref:System.Windows.Forms.ToolStrip> contrôle qui est destiné à la navigation et la manipulation des contrôles liés aux données sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="c2c42-103">The <xref:System.Windows.Forms.BindingNavigator> control is a special-purpose <xref:System.Windows.Forms.ToolStrip> control that is intended for navigating and manipulating controls on your form that are bound to data.</span></span>

<span data-ttu-id="c2c42-104">S’agissant d’un <xref:System.Windows.Forms.ToolStrip> contrôle, le <xref:System.Windows.Forms.BindingNavigator> composant peut être facilement modifié pour inclure des commandes supplémentaires ou alternatives pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2c42-104">Because it is a <xref:System.Windows.Forms.ToolStrip> control, the <xref:System.Windows.Forms.BindingNavigator> component can be easily modified to include additional or alternative commands for the user.</span></span>

<span data-ttu-id="c2c42-105">Dans la procédure suivante, un <xref:System.Windows.Forms.TextBox> contrôle est lié aux données et le <xref:System.Windows.Forms.ToolStrip> contrôle qui est ajouté au formulaire est modifié pour inclure la charge, enregistrer et les boutons d’annulation.</span><span class="sxs-lookup"><span data-stu-id="c2c42-105">In the following procedure, a <xref:System.Windows.Forms.TextBox> control is bound to data, and the <xref:System.Windows.Forms.ToolStrip> control that is added to the form is modified to include load, save, and cancel buttons.</span></span>

## <a name="add-load-save-and-cancel-buttons-to-the-bindingnavigator-component"></a><span data-ttu-id="c2c42-106">Ajouter charger, enregistrer et annuler des boutons au composant BindingNavigator</span><span class="sxs-lookup"><span data-stu-id="c2c42-106">Add load, save, and cancel buttons to the BindingNavigator component</span></span>

1. <span data-ttu-id="c2c42-107">Dans Visual Studio, ajoutez un <xref:System.Windows.Forms.TextBox> à votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="c2c42-107">In Visual Studio, add a <xref:System.Windows.Forms.TextBox> control to your form.</span></span>

2. <span data-ttu-id="c2c42-108">Lier à un <xref:System.Windows.Forms.BindingSource>, qui est lié à une source de données.</span><span class="sxs-lookup"><span data-stu-id="c2c42-108">Bind it to a <xref:System.Windows.Forms.BindingSource>, which is bound to a data source.</span></span> <span data-ttu-id="c2c42-109">Pour cet exemple, le <xref:System.Windows.Forms.BindingSource> est lié à une base de données.</span><span class="sxs-lookup"><span data-stu-id="c2c42-109">For this example, the <xref:System.Windows.Forms.BindingSource> is bound to a database.</span></span>

3. <span data-ttu-id="c2c42-110">Une fois que l’adaptateur de jeu de données et de table sont générées, faites glisser un <xref:System.Windows.Forms.BindingNavigator> contrôle au formulaire.</span><span class="sxs-lookup"><span data-stu-id="c2c42-110">After the dataset and table adapter are generated, drag a <xref:System.Windows.Forms.BindingNavigator> control to the form.</span></span>

4. <span data-ttu-id="c2c42-111">Définir le <xref:System.Windows.Forms.BindingNavigator> du contrôle <xref:System.Windows.Forms.BindingNavigator.BindingSource%2A> propriété le <xref:System.Windows.Forms.BindingSource> sur le formulaire qui est lié aux contrôles.</span><span class="sxs-lookup"><span data-stu-id="c2c42-111">Set the <xref:System.Windows.Forms.BindingNavigator> control's <xref:System.Windows.Forms.BindingNavigator.BindingSource%2A> property to the <xref:System.Windows.Forms.BindingSource> on the form that is bound to the controls.</span></span>

5. <span data-ttu-id="c2c42-112">Sélectionnez le contrôle <xref:System.Windows.Forms.BindingNavigator>.</span><span class="sxs-lookup"><span data-stu-id="c2c42-112">Select the <xref:System.Windows.Forms.BindingNavigator> control.</span></span>

6. <span data-ttu-id="c2c42-113">Cliquez sur le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) afin que la **tâches BindingNavigator** boîte de dialogue s’affiche et sélectionnez **modifier des éléments**.</span><span class="sxs-lookup"><span data-stu-id="c2c42-113">Click the smart tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) so the **BindingNavigator Tasks** dialog appears and select **Edit Items**.</span></span>

     <span data-ttu-id="c2c42-114">Le **éditeur de collections Items** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c2c42-114">The **Items Collection Editor** appears.</span></span>

7. <span data-ttu-id="c2c42-115">Dans le **éditeur de collections Items**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c2c42-115">In the **Items Collection Editor**, complete the following:</span></span>

    1. <span data-ttu-id="c2c42-116">Ajouter un <xref:System.Windows.Forms.ToolStripSeparator> et trois <xref:System.Windows.Forms.ToolStripButton> éléments en sélectionnant le type approprié de <xref:System.Windows.Forms.ToolStripItem> et en cliquant sur le **ajouter** bouton.</span><span class="sxs-lookup"><span data-stu-id="c2c42-116">Add a <xref:System.Windows.Forms.ToolStripSeparator> and three <xref:System.Windows.Forms.ToolStripButton> items by selecting the appropriate type of <xref:System.Windows.Forms.ToolStripItem> and clicking the **Add** button.</span></span>

    2. <span data-ttu-id="c2c42-117">Définir le <xref:System.Windows.Forms.ToolStripItem.Name%2A> propriété des boutons pour **LoadButton**, **SaveButton**, et **CancelButton**, respectivement.</span><span class="sxs-lookup"><span data-stu-id="c2c42-117">Set the <xref:System.Windows.Forms.ToolStripItem.Name%2A> property of the buttons to **LoadButton**, **SaveButton**, and **CancelButton**, respectively.</span></span>

    3. <span data-ttu-id="c2c42-118">Définir le <xref:System.Windows.Forms.ToolStripItem.Text%2A> propriété des boutons pour **charge**, **enregistrer**, et **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="c2c42-118">Set the <xref:System.Windows.Forms.ToolStripItem.Text%2A> property of the buttons to **Load**, **Save**, and **Cancel**.</span></span>

    4. <span data-ttu-id="c2c42-119">Définir le <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> propriété pour chacun des boutons pour **texte**.</span><span class="sxs-lookup"><span data-stu-id="c2c42-119">Set the <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> property for each of the buttons to **Text**.</span></span> <span data-ttu-id="c2c42-120">Vous pouvez également définir cette propriété **Image** ou **ImageAndText**et définir l’image à afficher dans le <xref:System.Windows.Forms.ToolStripItem.Image%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="c2c42-120">Alternatively, you can set this property to **Image** or **ImageAndText**, and set the image to be displayed in the <xref:System.Windows.Forms.ToolStripItem.Image%2A> property.</span></span>

    5. <span data-ttu-id="c2c42-121">Cliquez sur **OK** pour fermer la boîte de dialogue. Les boutons sont ajoutés à la <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="c2c42-121">Click **OK** to close the dialog box.The buttons are added to the <xref:System.Windows.Forms.ToolStrip>.</span></span>

8. <span data-ttu-id="c2c42-122">Avec le bouton droit de la forme et choisissez **afficher le Code**.</span><span class="sxs-lookup"><span data-stu-id="c2c42-122">Right-click the form and choose **View Code**.</span></span>

9. <span data-ttu-id="c2c42-123">Dans l’éditeur de Code, recherchez la ligne de code qui charge les données dans l’adaptateur de table.</span><span class="sxs-lookup"><span data-stu-id="c2c42-123">In the Code Editor, find the line of code that loads data into the table adapter.</span></span> <span data-ttu-id="c2c42-124">Ce code a été généré lorsque vous configurez la liaison de données à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c2c42-124">This code was generated when you set up the data binding in step 2.</span></span> <span data-ttu-id="c2c42-125">Le code doit être similaire à ce qui suit : `TableAdapterName.Fill(DataSetName.TableName)`.</span><span class="sxs-lookup"><span data-stu-id="c2c42-125">The code should be similar to the following: `TableAdapterName.Fill(DataSetName.TableName)`.</span></span> <span data-ttu-id="c2c42-126">Il figurera très probablement se trouver dans le formulaire <xref:System.Windows.Forms.Form.Load> événement.</span><span class="sxs-lookup"><span data-stu-id="c2c42-126">It will most likely be in the form's <xref:System.Windows.Forms.Form.Load> event.</span></span>

10. <span data-ttu-id="c2c42-127">Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événements de la **charge** <xref:System.Windows.Forms.ToolStripButton> créé précédemment et de déplacer ce code de chargement des données dedans.</span><span class="sxs-lookup"><span data-stu-id="c2c42-127">Create an event handler for the <xref:System.Windows.Forms.ToolStripItem.Click> event of the **Load** <xref:System.Windows.Forms.ToolStripButton> you created earlier and move this data-loading code into it.</span></span>

     <span data-ttu-id="c2c42-128">Votre code doit maintenant ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c2c42-128">Your code should now look similar to the following:</span></span>

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

11. <span data-ttu-id="c2c42-129">Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événements de la **enregistrer** <xref:System.Windows.Forms.ToolStripButton> vous avez créé précédemment et écrire du code pour mettre à jour les données dans la table, le contrôle est lié à.</span><span class="sxs-lookup"><span data-stu-id="c2c42-129">Create an event handler for the <xref:System.Windows.Forms.ToolStripItem.Click> event of the **Save**<xref:System.Windows.Forms.ToolStripButton> you created earlier and write code to update the data within the table the control is bound to.</span></span>

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
    > <span data-ttu-id="c2c42-130">Dans certains cas, le <xref:System.Windows.Forms.BindingNavigator> composant a déjà un **enregistrer** bouton, mais aucun code n’a été généré par le Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="c2c42-130">In some cases, the <xref:System.Windows.Forms.BindingNavigator> component already has a **Save** button, but no code has been generated by the Windows Forms Designer.</span></span> <span data-ttu-id="c2c42-131">Dans ce cas, vous pouvez placer le code précédent dans le <xref:System.Windows.Forms.ToolStripItem.Click> Gestionnaire d’événements pour ce bouton, au lieu de créer un bouton entièrement nouveau sur le <xref:System.Windows.Forms.ToolStrip>.</span><span class="sxs-lookup"><span data-stu-id="c2c42-131">In this case, you can place the preceding code in the <xref:System.Windows.Forms.ToolStripItem.Click> event handler for that button, rather than creating an entirely new button on the <xref:System.Windows.Forms.ToolStrip>.</span></span> <span data-ttu-id="c2c42-132">Toutefois, le bouton est désactivé par défaut, vous devez donc définir la <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> propriété du bouton sur `true` pour que le bouton fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="c2c42-132">However, the button is disabled by default, so you must set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property of the button to `true` to have the button function correctly.</span></span>

12. <span data-ttu-id="c2c42-133">Créer un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripItem.Click> événements de la **Annuler** <xref:System.Windows.Forms.ToolStripButton> créé précédemment et d’écrire du code pour annuler les modifications apportées à l’enregistrement de données qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="c2c42-133">Create an event handler for the <xref:System.Windows.Forms.ToolStripItem.Click> event of the **Cancel** <xref:System.Windows.Forms.ToolStripButton> you created earlier and write code to cancel any changes to the data record that is displayed.</span></span>

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
    > <span data-ttu-id="c2c42-134">Le <xref:System.Windows.Forms.BindingSource.CancelEdit%2A> méthode porte sur la ligne de données.</span><span class="sxs-lookup"><span data-stu-id="c2c42-134">The <xref:System.Windows.Forms.BindingSource.CancelEdit%2A> method is scoped to the row of data.</span></span> <span data-ttu-id="c2c42-135">Enregistrer les modifications apportées pendant l’affichage de cet enregistrement individuel avant de naviguer jusqu'à l’enregistrement suivant.</span><span class="sxs-lookup"><span data-stu-id="c2c42-135">Save any changes you make while viewing that individual record before navigating to the next record.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2c42-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2c42-136">See also</span></span>

- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.ToolStrip>
- [<span data-ttu-id="c2c42-137">BindingNavigator, contrôle</span><span class="sxs-lookup"><span data-stu-id="c2c42-137">BindingNavigator Control</span></span>](bindingnavigator-control-windows-forms.md)
- [<span data-ttu-id="c2c42-138">Vue d'ensemble du composant BindingSource</span><span class="sxs-lookup"><span data-stu-id="c2c42-138">BindingSource Component Overview</span></span>](bindingsource-component-overview.md)
