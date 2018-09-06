---
title: 'Procédure pas à pas : sérialisation des collections de types standard avec DesignerSerializationVisibilityAttribute'
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
ms.openlocfilehash: 54859b3065e8e9bb9680d8b6bf7946b393f73b9f
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43788079"
---
# <a name="walkthrough-serializing-collections-of-standard-types-with-the-designerserializationvisibilityattribute"></a><span data-ttu-id="d0af1-102">Procédure pas à pas : sérialisation des collections de types standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="d0af1-102">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>
<span data-ttu-id="d0af1-103">Vos contrôles personnalisés parfois expose une collection en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="d0af1-103">Your custom controls will sometimes expose a collection as a property.</span></span> <span data-ttu-id="d0af1-104">Cette procédure pas à pas montre comment utiliser le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> classe pour contrôler la façon dont une collection est sérialisée au moment du design.</span><span class="sxs-lookup"><span data-stu-id="d0af1-104">This walkthrough demonstrates how to use the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> class to control how a collection is serialized at design time.</span></span> <span data-ttu-id="d0af1-105">Appliquer le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> valeur à votre propriété de collection garantit que la propriété sera sérialisée.</span><span class="sxs-lookup"><span data-stu-id="d0af1-105">Applying the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> value to your collection property ensures that the property will be serialized.</span></span>  
  
 <span data-ttu-id="d0af1-106">Pour copier le code dans cette rubrique sous forme de liste unique, consultez [Comment : sérialiser des Collections de Types Standard avec DesignerSerializationVisibilityAttribute](https://msdn.microsoft.com/library/7829fcdd-8205-405f-8231-a1282a9835c9).</span><span class="sxs-lookup"><span data-stu-id="d0af1-106">To copy the code in this topic as a single listing, see [How to: Serialize Collections of Standard Types with the DesignerSerializationVisibilityAttribute](https://msdn.microsoft.com/library/7829fcdd-8205-405f-8231-a1282a9835c9).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0af1-107">Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée.</span><span class="sxs-lookup"><span data-stu-id="d0af1-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="d0af1-108">Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** .</span><span class="sxs-lookup"><span data-stu-id="d0af1-108">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="d0af1-109">Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="d0af1-109">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="d0af1-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="d0af1-110">Prerequisites</span></span>  
 <span data-ttu-id="d0af1-111">Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d0af1-111">In order to complete this walkthrough, you will need:</span></span>  
  
-   <span data-ttu-id="d0af1-112">Autorisations suffisantes pour pouvoir créer et exécuter des projets d’application Windows Forms sur l’ordinateur où Visual Studio est installé.</span><span class="sxs-lookup"><span data-stu-id="d0af1-112">Sufficient permissions to be able to create and run Windows Forms application projects on the computer where Visual Studio is installed.</span></span>  
  
## <a name="creating-a-control-that-has-a-serializable-collection"></a><span data-ttu-id="d0af1-113">Création d’un contrôle qui a une Collection sérialisable</span><span class="sxs-lookup"><span data-stu-id="d0af1-113">Creating a Control That Has a Serializable Collection</span></span>  
 <span data-ttu-id="d0af1-114">La première étape consiste à créer un contrôle qui a une collection sérialisable en tant que propriété.</span><span class="sxs-lookup"><span data-stu-id="d0af1-114">The first step is to create a control that has a serializable collection as a property.</span></span> <span data-ttu-id="d0af1-115">Vous pouvez modifier le contenu de cette collection à l’aide de la **éditeur de collections**, auquel vous pouvez accéder à partir de la **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d0af1-115">You can edit the contents of this collection using the **Collection Editor**, which you can access from the **Properties** window.</span></span>  
  
#### <a name="to-create-a-control-with-a-serializable-collection"></a><span data-ttu-id="d0af1-116">Pour créer un contrôle avec une collection sérialisable</span><span class="sxs-lookup"><span data-stu-id="d0af1-116">To create a control with a serializable collection</span></span>  
  
1.  <span data-ttu-id="d0af1-117">Créez un projet de bibliothèque de contrôles Windows appelé `SerializationDemoControlLib`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-117">Create a Windows Control Library project called `SerializationDemoControlLib`.</span></span> <span data-ttu-id="d0af1-118">Pour plus d’informations, consultez [modèle de bibliothèque de contrôles Windows](https://msdn.microsoft.com/library/722f4e2d-1310-4ed5-8f33-593337ab66b4).</span><span class="sxs-lookup"><span data-stu-id="d0af1-118">For more information, see [Windows Control Library Template](https://msdn.microsoft.com/library/722f4e2d-1310-4ed5-8f33-593337ab66b4).</span></span>  
  
2.  <span data-ttu-id="d0af1-119">Renommer `UserControl1` à `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-119">Rename `UserControl1` to `SerializationDemoControl`.</span></span> <span data-ttu-id="d0af1-120">Pour plus d’informations, consultez [Comment : renommer des identificateurs](https://msdn.microsoft.com/library/2430f732-2b70-4516-8cf6-a7bb71cc9724).</span><span class="sxs-lookup"><span data-stu-id="d0af1-120">For more information, see [How to: Rename Identifiers](https://msdn.microsoft.com/library/2430f732-2b70-4516-8cf6-a7bb71cc9724).</span></span>  
  
3.  <span data-ttu-id="d0af1-121">Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Padding.All%2A?displayProperty=nameWithType> propriété `10`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-121">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Padding.All%2A?displayProperty=nameWithType> property to `10`.</span></span>  
  
4.  <span data-ttu-id="d0af1-122">Place un <xref:System.Windows.Forms.TextBox> dans contrôler le `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-122">Place a <xref:System.Windows.Forms.TextBox> control in the `SerializationDemoControl`.</span></span>  
  
5.  <span data-ttu-id="d0af1-123">Sélectionnez le contrôle <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="d0af1-123">Select the <xref:System.Windows.Forms.TextBox> control.</span></span> <span data-ttu-id="d0af1-124">Dans le **propriétés** fenêtre, définissez les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d0af1-124">In the **Properties** window, set the following properties.</span></span>  
  
    |<span data-ttu-id="d0af1-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="d0af1-125">Property</span></span>|<span data-ttu-id="d0af1-126">Remplacer par</span><span class="sxs-lookup"><span data-stu-id="d0af1-126">Change to</span></span>|  
    |--------------|---------------|  
    |<span data-ttu-id="d0af1-127">**Multiline**</span><span class="sxs-lookup"><span data-stu-id="d0af1-127">**Multiline**</span></span>|`true`|  
    |<span data-ttu-id="d0af1-128">**Dock**</span><span class="sxs-lookup"><span data-stu-id="d0af1-128">**Dock**</span></span>|<xref:System.Windows.Forms.DockStyle.Fill>|  
    |<span data-ttu-id="d0af1-129">**Barres de défilement**</span><span class="sxs-lookup"><span data-stu-id="d0af1-129">**ScrollBars**</span></span>|<xref:System.Windows.Forms.ScrollBars.Vertical>|  
    |<span data-ttu-id="d0af1-130">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="d0af1-130">**ReadOnly**</span></span>|`true`|  
  
6.  <span data-ttu-id="d0af1-131">Dans le **éditeur de Code**, déclarez un champ de tableau de chaîne nommé `stringsValue` dans `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-131">In the **Code Editor**, declare a string array field named `stringsValue` in `SerializationDemoControl`.</span></span>  
  
     [!code-cpp[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/cpp/form1.cpp#4)]
     [!code-csharp[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/CS/form1.cs#4)]
     [!code-vb[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/VB/form1.vb#4)]  
  
7.  <span data-ttu-id="d0af1-132">Définir le `Strings` propriété sur le `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-132">Define the `Strings` property on the `SerializationDemoControl`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0af1-133">Le <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> valeur est utilisée pour permettre la sérialisation de la collection.</span><span class="sxs-lookup"><span data-stu-id="d0af1-133">The <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> value is used to enable serialization of the collection.</span></span>  
  
 [!code-cpp[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/cpp/form1.cpp#5)]
 [!code-csharp[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/CS/form1.cs#5)]
 [!code-vb[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/VB/form1.vb#5)]  
  
1.  <span data-ttu-id="d0af1-134">Appuyez sur F5 pour générer le projet et exécuter votre contrôle dans le **Conteneur de test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-134">Press F5 to build the project and run your control in the **UserControl Test Container**.</span></span>  
  
2.  <span data-ttu-id="d0af1-135">Rechercher la `Strings` propriété dans le <xref:System.Windows.Forms.PropertyGrid> de la **conteneur de Test UserControl**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-135">Find the `Strings` property in the <xref:System.Windows.Forms.PropertyGrid> of the **UserControl Test Container**.</span></span> <span data-ttu-id="d0af1-136">Cliquez sur le `Strings` propriété, puis cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) pour ouvrir le **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-136">Click the `Strings` property, then click the ellipsis (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) button to open the **String Collection Editor**.</span></span>  
  
3.  <span data-ttu-id="d0af1-137">Entrez plusieurs chaînes dans le **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-137">Enter several strings in the **String Collection Editor**.</span></span> <span data-ttu-id="d0af1-138">Séparez-les en appuyant sur la touche entrée à la fin de chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="d0af1-138">Separate them by pressing the ENTER key at the end of each string.</span></span> <span data-ttu-id="d0af1-139">Cliquez sur **OK** lorsque vous avez terminé d’entrer des chaînes.</span><span class="sxs-lookup"><span data-stu-id="d0af1-139">Click **OK** when you are finished entering strings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0af1-140">Les chaînes que vous avez tapé s’affichent dans le <xref:System.Windows.Forms.TextBox> de la `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-140">The strings you typed appear in the <xref:System.Windows.Forms.TextBox> of the `SerializationDemoControl`.</span></span>  
  
## <a name="serializing-a-collection-property"></a><span data-ttu-id="d0af1-141">Sérialisation d’une propriété de Collection</span><span class="sxs-lookup"><span data-stu-id="d0af1-141">Serializing a Collection Property</span></span>  
 <span data-ttu-id="d0af1-142">Pour tester le comportement de sérialisation de votre contrôle, vous placer sur un formulaire et modifier le contenu de la collection avec le **éditeur de collections**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-142">To test the serialization behavior of your control, you will place it on a form and change the contents of the collection with the **Collection Editor**.</span></span> <span data-ttu-id="d0af1-143">Vous pouvez voir l’état de collection sérialisée en examinant un fichier de concepteur spécial dans lequel le **Windows Forms Designer** émet du code.</span><span class="sxs-lookup"><span data-stu-id="d0af1-143">You can see the serialized collection state by looking at a special designer file, into which the **Windows Forms Designer** emits code.</span></span>  
  
#### <a name="to-serialize-a-collection"></a><span data-ttu-id="d0af1-144">Pour sérialiser une collection</span><span class="sxs-lookup"><span data-stu-id="d0af1-144">To serialize a collection</span></span>  
  
1.  <span data-ttu-id="d0af1-145">Ajouter un projet d’Application de Windows à la solution.</span><span class="sxs-lookup"><span data-stu-id="d0af1-145">Add a Windows Application project to the solution.</span></span> <span data-ttu-id="d0af1-146">Attribuez un nom au projet `SerializationDemoControlTest`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-146">Name the project `SerializationDemoControlTest`.</span></span>  
  
2.  <span data-ttu-id="d0af1-147">Dans le **boîte à outils**, recherchez l’onglet nommé **Composants SerializationDemoControlLib**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-147">In the **Toolbox**, find the tab named **SerializationDemoControlLib Components**.</span></span> <span data-ttu-id="d0af1-148">Dans cet onglet, vous trouverez le `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-148">In this tab, you will find the `SerializationDemoControl`.</span></span> <span data-ttu-id="d0af1-149">Pour plus d’informations, consultez l’article [Procédure pas à pas : remplissage automatique de la boîte à outils avec des composants personnalisés](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span><span class="sxs-lookup"><span data-stu-id="d0af1-149">For more information, see [Walkthrough: Automatically Populating the Toolbox with Custom Components](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span></span>  
  
3.  <span data-ttu-id="d0af1-150">Place un `SerializationDemoControl` sur votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="d0af1-150">Place a `SerializationDemoControl` on your form.</span></span>  
  
4.  <span data-ttu-id="d0af1-151">Rechercher la `Strings` propriété dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d0af1-151">Find the `Strings` property in the **Properties** window.</span></span> <span data-ttu-id="d0af1-152">Cliquez sur le `Strings` propriété, puis cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) pour ouvrir le **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-152">Click the `Strings` property, then click the ellipsis (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) button to open the **String Collection Editor**.</span></span>  
  
5.  <span data-ttu-id="d0af1-153">Entrez plusieurs chaînes dans le **éditeur de collections String**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-153">Type several strings in the **String Collection Editor**.</span></span> <span data-ttu-id="d0af1-154">Séparez-les en appuyant sur la touche entrée à la fin de chaque chaîne.</span><span class="sxs-lookup"><span data-stu-id="d0af1-154">Separate them by pressing the ENTER key at the end of each string.</span></span> <span data-ttu-id="d0af1-155">Cliquez sur **OK** lorsque vous avez terminé d’entrer des chaînes.</span><span class="sxs-lookup"><span data-stu-id="d0af1-155">Click **OK** when you are finished entering strings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0af1-156">Les chaînes que vous avez tapé s’affichent dans le <xref:System.Windows.Forms.TextBox> de la `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="d0af1-156">The strings you typed appear in the <xref:System.Windows.Forms.TextBox> of the `SerializationDemoControl`.</span></span>  
  
1.  <span data-ttu-id="d0af1-157">Dans l’**Explorateur de solutions**, cliquez sur le bouton **Afficher tous les fichiers**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-157">In **Solution Explorer**, click the **Show All Files** button.</span></span>  
  
2.  <span data-ttu-id="d0af1-158">Ouvrez le **Form1** nœud.</span><span class="sxs-lookup"><span data-stu-id="d0af1-158">Open the **Form1** node.</span></span> <span data-ttu-id="d0af1-159">En dessous, il est un fichier appelé **Form1.Designer.cs** ou **Form1.Designer.vb**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-159">Beneath it is a file called **Form1.Designer.cs** or **Form1.Designer.vb**.</span></span> <span data-ttu-id="d0af1-160">C’est le fichier dans lequel le **Windows Forms Designer** émet le code qui représente l’état au moment du design de votre formulaire et ses contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="d0af1-160">This is the file into which the **Windows Forms Designer** emits code representing the design-time state of your form and its child controls.</span></span> <span data-ttu-id="d0af1-161">Ouvrez ce fichier dans **l’éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-161">Open this file in the **Code Editor**.</span></span>  
  
3.  <span data-ttu-id="d0af1-162">Ouvrez la région appelée **code généré par le Concepteur de formulaire Windows** et recherchez la section intitulée **serializationDemoControl1**.</span><span class="sxs-lookup"><span data-stu-id="d0af1-162">Open the region called **Windows Form Designer generated code** and find the section labeled **serializationDemoControl1**.</span></span> <span data-ttu-id="d0af1-163">Sous cette étiquette est le code qui représente l’état sérialisé de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="d0af1-163">Beneath this label is the code representing the serialized state of your control.</span></span> <span data-ttu-id="d0af1-164">Les chaînes que vous avez tapé à l’étape 5 s’affichent dans une assignation à la `Strings` propriété.</span><span class="sxs-lookup"><span data-stu-id="d0af1-164">The strings you typed in step 5 appear in an assignment to the `Strings` property.</span></span> <span data-ttu-id="d0af1-165">Les exemples de code suivant en c# et Visual Basic, afficher le code similaire à ce que vous verrez si vous avez tapé les chaînes « rouge », « orange » et « jaune ».</span><span class="sxs-lookup"><span data-stu-id="d0af1-165">The following code examples in C# and Visual Basic, show code similar to what you will see if you typed the strings "red", "orange", and "yellow".</span></span>  
  
    ```csharp  
    this.serializationDemoControl1.Strings = new string[] {  
            "red",  
            "orange",  
            "yellow"};  
    ```  
    
    ```vb  
    Me.serializationDemoControl1.Strings = New String() {"red", "orange", "yellow"}  
    ```
  
4.  <span data-ttu-id="d0af1-166">Dans le **éditeur de Code**, modifiez la valeur de la <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> sur le `Strings` propriété <xref:System.ComponentModel.DesignerSerializationVisibility.Hidden>.</span><span class="sxs-lookup"><span data-stu-id="d0af1-166">In the **Code Editor**, change the value of the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> on the `Strings` property to <xref:System.ComponentModel.DesignerSerializationVisibility.Hidden>.</span></span>  
  
    ```csharp  
    [DesignerSerializationVisibility(DesignerSerializationVisibility.Hidden)]  
    ```  
    ```vb  
    <DesignerSerializationVisibility(DesignerSerializationVisibility.Hidden)> _  
    ```  
  
5. <span data-ttu-id="d0af1-167">Régénérez la solution et répétez les étapes 3 et 4.</span><span class="sxs-lookup"><span data-stu-id="d0af1-167">Rebuild the solution and repeat steps 3 and 4.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d0af1-168">Dans ce cas, le **Windows Forms Designer** n’émet aucune assignation à la `Strings` propriété.</span><span class="sxs-lookup"><span data-stu-id="d0af1-168">In this case, the **Windows Forms Designer** emits no assignment to the `Strings` property.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="d0af1-169">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d0af1-169">Next Steps</span></span>  
 <span data-ttu-id="d0af1-170">Une fois que vous savez comment sérialiser une collection de types standards, intégrez vos contrôles personnalisés plus profondément dans l’environnement au moment du design.</span><span class="sxs-lookup"><span data-stu-id="d0af1-170">Once you know how to serialize a collection of standard types, consider integrating your custom controls more deeply into the design-time environment.</span></span> <span data-ttu-id="d0af1-171">Les rubriques suivantes décrivent comment améliorer l’intégration au moment du design de vos contrôles personnalisés :</span><span class="sxs-lookup"><span data-stu-id="d0af1-171">The following topics describe how to enhance the design-time integration of your custom controls:</span></span>  
  
-   [<span data-ttu-id="d0af1-172">Architecture de conception</span><span class="sxs-lookup"><span data-stu-id="d0af1-172">Design-Time Architecture</span></span>](https://msdn.microsoft.com/library/4881917b-628f-4689-b872-472e4f8a4e3a)  
  
-   [<span data-ttu-id="d0af1-173">Attributs dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d0af1-173">Attributes in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/attributes-in-windows-forms-controls.md)  
  
-   [<span data-ttu-id="d0af1-174">Vue d’ensemble de la sérialisation du Concepteur</span><span class="sxs-lookup"><span data-stu-id="d0af1-174">Designer Serialization Overview</span></span>](https://msdn.microsoft.com/library/c342635a-aa5f-4281-915b-b013738af15a)  
  
-   [<span data-ttu-id="d0af1-175">Procédure pas à pas : création d’un contrôle Windows Forms qui tire parti des fonctionnalités au moment du design de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d0af1-175">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](../../../../docs/framework/winforms/controls/creating-a-wf-control-design-time-features.md)  
  
## <a name="see-also"></a><span data-ttu-id="d0af1-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0af1-176">See Also</span></span>  
 <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute>  
 [<span data-ttu-id="d0af1-177">Vue d’ensemble de la sérialisation du Concepteur</span><span class="sxs-lookup"><span data-stu-id="d0af1-177">Designer Serialization Overview</span></span>](https://msdn.microsoft.com/library/c342635a-aa5f-4281-915b-b013738af15a)  
 [<span data-ttu-id="d0af1-178">Comment : sérialiser des Collections de Types Standard avec DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="d0af1-178">How to: Serialize Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](https://msdn.microsoft.com/library/7829fcdd-8205-405f-8231-a1282a9835c9)  
 [<span data-ttu-id="d0af1-179">Procédure pas à pas : remplissage automatique de la boîte à outils avec des composants personnalisés</span><span class="sxs-lookup"><span data-stu-id="d0af1-179">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
