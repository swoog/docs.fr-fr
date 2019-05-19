---
title: 'Procédure pas à pas : Sérialisation des collections de types standard avec DesignerSerializationVisibilityAttribute'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- serialization [Windows Forms], collections
- standard types [Windows Forms], collections
- collections [Windows Forms], serializing
- collections [Windows Forms], standard types
ms.assetid: 020c9df4-fdc5-4dae-815a-963ecae5668c
ms.openlocfilehash: 1f1412f03f912c0142b08d5ad8581e421252cfb3
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65882357"
---
# <a name="walkthrough-serializing-collections-of-standard-types-with-the-designerserializationvisibilityattribute"></a><span data-ttu-id="ca612-102">Procédure pas à pas : Sérialisation des collections de types standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="ca612-102">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>

<span data-ttu-id="ca612-103">Vos contrôles personnalisés parfois expose une collection en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="ca612-103">Your custom controls will sometimes expose a collection as a property.</span></span> <span data-ttu-id="ca612-104">Cette procédure pas à pas montre comment utiliser le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> classe pour contrôler la façon dont une collection est sérialisée au moment du design.</span><span class="sxs-lookup"><span data-stu-id="ca612-104">This walkthrough demonstrates how to use the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> class to control how a collection is serialized at design time.</span></span> <span data-ttu-id="ca612-105">Appliquer le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> valeur à votre propriété de collection garantit que la propriété sera sérialisée.</span><span class="sxs-lookup"><span data-stu-id="ca612-105">Applying the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> value to your collection property ensures that the property will be serialized.</span></span>

<span data-ttu-id="ca612-106">Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Sérialiser des Collections de Types Standard avec DesignerSerializationVisibilityAttribute](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171833(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="ca612-106">To copy the code in this topic as a single listing, see [How to: Serialize Collections of Standard Types with the DesignerSerializationVisibilityAttribute](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171833(v=vs.120)).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ca612-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="ca612-107">Prerequisites</span></span>

<span data-ttu-id="ca612-108">Cette procédure pas à pas nécessite Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ca612-108">You need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-a-control-with-a-serializable-collection"></a><span data-ttu-id="ca612-109">Créer un contrôle avec une collection sérialisable</span><span class="sxs-lookup"><span data-stu-id="ca612-109">Create a control with a serializable collection</span></span>

<span data-ttu-id="ca612-110">La première étape consiste à créer un contrôle qui a une collection sérialisable en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="ca612-110">The first step is to create a control that has a serializable collection as a property.</span></span> <span data-ttu-id="ca612-111">Vous pouvez modifier le contenu de cette collection à l’aide de la **éditeur de collections**, auquel vous pouvez accéder à partir de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ca612-111">You can edit the contents of this collection using the **Collection Editor**, which you can access from the **Properties** window.</span></span>

1. <span data-ttu-id="ca612-112">Dans Visual Studio, créez un projet de bibliothèque de contrôles Windows appelé `SerializationDemoControlLib`.</span><span class="sxs-lookup"><span data-stu-id="ca612-112">In Visual Studio, create a Windows Control Library project called `SerializationDemoControlLib`.</span></span> <span data-ttu-id="ca612-113">Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="ca612-113">For more information, see [Windows Control Library Template](https://docs.microsoft.com/previous-versions/kxczf775(v=vs.100)).</span></span>

2. <span data-ttu-id="ca612-114">Renommer `UserControl1` à `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-114">Rename `UserControl1` to `SerializationDemoControl`.</span></span> <span data-ttu-id="ca612-115">Pour plus d’informations, consultez [renommer un symbole de code (refactorisation)](/visualstudio/ide/reference/rename).</span><span class="sxs-lookup"><span data-stu-id="ca612-115">For more information, see [Rename a code symbol refactoring](/visualstudio/ide/reference/rename).</span></span>

3. <span data-ttu-id="ca612-116">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Padding.All%2A?displayProperty=nameWithType> propriété `10`.</span><span class="sxs-lookup"><span data-stu-id="ca612-116">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Padding.All%2A?displayProperty=nameWithType> property to `10`.</span></span>

4. <span data-ttu-id="ca612-117">Place un <xref:System.Windows.Forms.TextBox> dans contrôler le `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-117">Place a <xref:System.Windows.Forms.TextBox> control in the `SerializationDemoControl`.</span></span>

5. <span data-ttu-id="ca612-118">Sélectionnez le contrôle <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="ca612-118">Select the <xref:System.Windows.Forms.TextBox> control.</span></span> <span data-ttu-id="ca612-119">Dans le **propriétés** fenêtre, définissez les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca612-119">In the **Properties** window, set the following properties.</span></span>

    |<span data-ttu-id="ca612-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="ca612-120">Property</span></span>|<span data-ttu-id="ca612-121">Remplacer par</span><span class="sxs-lookup"><span data-stu-id="ca612-121">Change to</span></span>|
    |--------------|---------------|
    |<span data-ttu-id="ca612-122">**Multiline**</span><span class="sxs-lookup"><span data-stu-id="ca612-122">**Multiline**</span></span>|`true`|
    |<span data-ttu-id="ca612-123">**Dock**</span><span class="sxs-lookup"><span data-stu-id="ca612-123">**Dock**</span></span>|<xref:System.Windows.Forms.DockStyle.Fill>|
    |<span data-ttu-id="ca612-124">**ScrollBars**</span><span class="sxs-lookup"><span data-stu-id="ca612-124">**ScrollBars**</span></span>|<xref:System.Windows.Forms.ScrollBars.Vertical>|
    |<span data-ttu-id="ca612-125">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="ca612-125">**ReadOnly**</span></span>|`true`|

6. <span data-ttu-id="ca612-126">Dans le **éditeur de Code**, déclarez un champ de tableau de chaîne nommé `stringsValue` dans `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-126">In the **Code Editor**, declare a string array field named `stringsValue` in `SerializationDemoControl`.</span></span>

     [!code-cpp[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/cpp/form1.cpp#4)]
     [!code-csharp[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/CS/form1.cs#4)]
     [!code-vb[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/VB/form1.vb#4)]

7. <span data-ttu-id="ca612-127">Définir le `Strings` propriété sur le `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-127">Define the `Strings` property on the `SerializationDemoControl`.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ca612-128">Le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> valeur est utilisée pour permettre la sérialisation de la collection.</span><span class="sxs-lookup"><span data-stu-id="ca612-128">The <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> value is used to enable serialization of the collection.</span></span>

   [!code-cpp[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/cpp/form1.cpp#5)]
   [!code-csharp[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/CS/form1.cs#5)]
   [!code-vb[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/VB/form1.vb#5)]

8. <span data-ttu-id="ca612-129">Appuyez sur **F5** pour générer le projet et exécuter votre contrôle dans le **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="ca612-129">Press **F5** to build the project and run your control in the **UserControl Test Container**.</span></span>

9. <span data-ttu-id="ca612-130">Rechercher la `Strings` propriété dans le <xref:System.Windows.Forms.PropertyGrid> de la **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="ca612-130">Find the `Strings` property in the <xref:System.Windows.Forms.PropertyGrid> of the **UserControl Test Container**.</span></span> <span data-ttu-id="ca612-131">Cliquez sur le `Strings` propriété, puis cliquez sur le bouton de sélection (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) pour ouvrir la **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="ca612-131">Click the `Strings` property, then click the ellipsis (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button to open the **String Collection Editor**.</span></span>

10. <span data-ttu-id="ca612-132">Entrez plusieurs chaînes dans le **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="ca612-132">Enter several strings in the **String Collection Editor**.</span></span> <span data-ttu-id="ca612-133">Séparez-les en appuyant sur la **entrée** clé à la fin de chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="ca612-133">Separate them by pressing the **Enter** key at the end of each string.</span></span> <span data-ttu-id="ca612-134">Cliquez sur **OK** lorsque vous avez terminé d’entrer des chaînes.</span><span class="sxs-lookup"><span data-stu-id="ca612-134">Click **OK** when you are finished entering strings.</span></span>

   > [!NOTE]
   > <span data-ttu-id="ca612-135">Les chaînes que vous avez tapé s’affichent dans le <xref:System.Windows.Forms.TextBox> de la `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-135">The strings you typed appear in the <xref:System.Windows.Forms.TextBox> of the `SerializationDemoControl`.</span></span>

## <a name="serializing-a-collection-property"></a><span data-ttu-id="ca612-136">Sérialisation d’une propriété de Collection</span><span class="sxs-lookup"><span data-stu-id="ca612-136">Serializing a Collection Property</span></span>

<span data-ttu-id="ca612-137">Pour tester le comportement de sérialisation de votre contrôle, vous placer sur un formulaire et modifier le contenu de la collection avec le **éditeur de collections**.</span><span class="sxs-lookup"><span data-stu-id="ca612-137">To test the serialization behavior of your control, you will place it on a form and change the contents of the collection with the **Collection Editor**.</span></span> <span data-ttu-id="ca612-138">Vous pouvez voir l’état de collection sérialisée en examinant un fichier de concepteur spécial dans lequel le **Windows Forms Designer** émet du code.</span><span class="sxs-lookup"><span data-stu-id="ca612-138">You can see the serialized collection state by looking at a special designer file into which the **Windows Forms Designer** emits code.</span></span>

### <a name="to-serialize-a-collection"></a><span data-ttu-id="ca612-139">Pour sérialiser une collection</span><span class="sxs-lookup"><span data-stu-id="ca612-139">To serialize a collection</span></span>

1. <span data-ttu-id="ca612-140">Ajouter un projet d’Application de Windows à la solution.</span><span class="sxs-lookup"><span data-stu-id="ca612-140">Add a Windows Application project to the solution.</span></span> <span data-ttu-id="ca612-141">Attribuez un nom au projet `SerializationDemoControlTest`.</span><span class="sxs-lookup"><span data-stu-id="ca612-141">Name the project `SerializationDemoControlTest`.</span></span>

2. <span data-ttu-id="ca612-142">Dans le **boîte à outils**, recherchez l’onglet nommé **Composants SerializationDemoControlLib**.</span><span class="sxs-lookup"><span data-stu-id="ca612-142">In the **Toolbox**, find the tab named **SerializationDemoControlLib Components**.</span></span> <span data-ttu-id="ca612-143">Dans cet onglet, vous trouverez le `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-143">In this tab, you will find the `SerializationDemoControl`.</span></span> <span data-ttu-id="ca612-144">Pour plus d’informations, consultez [Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés](walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span><span class="sxs-lookup"><span data-stu-id="ca612-144">For more information, see [Walkthrough: Automatically Populating the Toolbox with Custom Components](walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span></span>

3. <span data-ttu-id="ca612-145">Place un `SerializationDemoControl` sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="ca612-145">Place a `SerializationDemoControl` on your form.</span></span>

4. <span data-ttu-id="ca612-146">Rechercher la `Strings` propriété dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ca612-146">Find the `Strings` property in the **Properties** window.</span></span> <span data-ttu-id="ca612-147">Cliquez sur le `Strings` propriété, puis cliquez sur le bouton de sélection (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) pour ouvrir la **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="ca612-147">Click the `Strings` property, then click the ellipsis (![The Ellipsis button (...) in the Properties window of Visual Studio.](./media/visual-studio-ellipsis-button.png)) button to open the **String Collection Editor**.</span></span>

5. <span data-ttu-id="ca612-148">Entrez plusieurs chaînes dans le **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="ca612-148">Type several strings in the **String Collection Editor**.</span></span> <span data-ttu-id="ca612-149">Séparez-les en appuyant sur la touche entrée à la fin de chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="ca612-149">Separate them by pressing the ENTER key at the end of each string.</span></span> <span data-ttu-id="ca612-150">Cliquez sur **OK** lorsque vous avez terminé d’entrer des chaînes.</span><span class="sxs-lookup"><span data-stu-id="ca612-150">Click **OK** when you are finished entering strings.</span></span>

> [!NOTE]
> <span data-ttu-id="ca612-151">Les chaînes que vous avez tapé s’affichent dans le <xref:System.Windows.Forms.TextBox> de la `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="ca612-151">The strings you typed appear in the <xref:System.Windows.Forms.TextBox> of the `SerializationDemoControl`.</span></span>

1. <span data-ttu-id="ca612-152">Dans l’**Explorateur de solutions**, cliquez sur le bouton **Afficher tous les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="ca612-152">In **Solution Explorer**, click the **Show All Files** button.</span></span>

2. <span data-ttu-id="ca612-153">Ouvrez le **Form1** nœud.</span><span class="sxs-lookup"><span data-stu-id="ca612-153">Open the **Form1** node.</span></span> <span data-ttu-id="ca612-154">En dessous, il est un fichier appelé **Form1.Designer.cs** ou **Form1.Designer.vb**.</span><span class="sxs-lookup"><span data-stu-id="ca612-154">Beneath it is a file called **Form1.Designer.cs** or **Form1.Designer.vb**.</span></span> <span data-ttu-id="ca612-155">C’est le fichier dans lequel le **Windows Forms Designer** émet le code qui représente l’état au moment du design de votre formulaire et ses contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="ca612-155">This is the file into which the **Windows Forms Designer** emits code representing the design-time state of your form and its child controls.</span></span> <span data-ttu-id="ca612-156">Ouvrez ce fichier dans **l’éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="ca612-156">Open this file in the **Code Editor**.</span></span>

3. <span data-ttu-id="ca612-157">Ouvrez la région appelée **code généré par le Concepteur de formulaire Windows** et recherchez la section intitulée **serializationDemoControl1**.</span><span class="sxs-lookup"><span data-stu-id="ca612-157">Open the region called **Windows Form Designer generated code** and find the section labeled **serializationDemoControl1**.</span></span> <span data-ttu-id="ca612-158">Sous cette étiquette est le code qui représente l’état sérialisé de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="ca612-158">Beneath this label is the code representing the serialized state of your control.</span></span> <span data-ttu-id="ca612-159">Les chaînes que vous avez tapé à l’étape 5 s’affichent dans une assignation à la `Strings` propriété.</span><span class="sxs-lookup"><span data-stu-id="ca612-159">The strings you typed in step 5 appear in an assignment to the `Strings` property.</span></span> <span data-ttu-id="ca612-160">Les exemples de code suivant en c# et Visual Basic, afficher le code similaire à ce que vous verrez si vous avez tapé les chaînes « rouge », « orange » et « jaune ».</span><span class="sxs-lookup"><span data-stu-id="ca612-160">The following code examples in C# and Visual Basic, show code similar to what you will see if you typed the strings "red", "orange", and "yellow".</span></span>

    ```csharp
    this.serializationDemoControl1.Strings = new string[] {
            "red",
            "orange",
            "yellow"};
    ```

    ```vb
    Me.serializationDemoControl1.Strings = New String() {"red", "orange", "yellow"}
    ```

4. <span data-ttu-id="ca612-161">Dans le **éditeur de Code**, modifiez la valeur de la <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> sur le `Strings` propriété <xref:System.ComponentModel.DesignerSerializationVisibility.Hidden>.</span><span class="sxs-lookup"><span data-stu-id="ca612-161">In the **Code Editor**, change the value of the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> on the `Strings` property to <xref:System.ComponentModel.DesignerSerializationVisibility.Hidden>.</span></span>

    ```csharp
    [DesignerSerializationVisibility(DesignerSerializationVisibility.Hidden)]
    ```

    ```vb
    <DesignerSerializationVisibility(DesignerSerializationVisibility.Hidden)> _
    ```

5. <span data-ttu-id="ca612-162">Régénérez la solution et répétez les étapes 3 et 4.</span><span class="sxs-lookup"><span data-stu-id="ca612-162">Rebuild the solution and repeat steps 3 and 4.</span></span>

> [!NOTE]
> <span data-ttu-id="ca612-163">Dans ce cas, le **Windows Forms Designer** n’émet aucune assignation à la `Strings` propriété.</span><span class="sxs-lookup"><span data-stu-id="ca612-163">In this case, the **Windows Forms Designer** emits no assignment to the `Strings` property.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ca612-164">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ca612-164">Next Steps</span></span>

<span data-ttu-id="ca612-165">Une fois que vous savez comment sérialiser une collection de types standards, intégrez vos contrôles personnalisés plus profondément dans l’environnement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="ca612-165">Once you know how to serialize a collection of standard types, consider integrating your custom controls more deeply into the design-time environment.</span></span> <span data-ttu-id="ca612-166">Les rubriques suivantes décrivent comment améliorer l’intégration au moment du design de vos contrôles personnalisés :</span><span class="sxs-lookup"><span data-stu-id="ca612-166">The following topics describe how to enhance the design-time integration of your custom controls:</span></span>

- <span data-ttu-id="ca612-167">[Architecture de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/c5z9s1h4(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="ca612-167">[Design-Time Architecture](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/c5z9s1h4(v=vs.120))</span></span>

- [<span data-ttu-id="ca612-168">Attributs dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca612-168">Attributes in Windows Forms Controls</span></span>](attributes-in-windows-forms-controls.md)

- <span data-ttu-id="ca612-169">[Vue d’ensemble de la sérialisation du Concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171834(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="ca612-169">[Designer Serialization Overview](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171834(v=vs.120))</span></span>

- [<span data-ttu-id="ca612-170">Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ca612-170">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](creating-a-wf-control-design-time-features.md)

## <a name="see-also"></a><span data-ttu-id="ca612-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca612-171">See also</span></span>

- <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute>
- <span data-ttu-id="ca612-172">[Vue d’ensemble de la sérialisation du Concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171834(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="ca612-172">[Designer Serialization Overview](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171834(v=vs.120))</span></span>
- <span data-ttu-id="ca612-173">[Guide pratique pour Sérialiser des Collections de Types Standard avec DesignerSerializationVisibilityAttribute](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171833(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="ca612-173">[How to: Serialize Collections of Standard Types with the DesignerSerializationVisibilityAttribute](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171833(v=vs.120))</span></span>
- [<span data-ttu-id="ca612-174">Procédure pas à pas : Remplissage automatique de la boîte à outils avec des composants personnalisés</span><span class="sxs-lookup"><span data-stu-id="ca612-174">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
