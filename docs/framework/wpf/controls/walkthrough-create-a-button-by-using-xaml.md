---
title: 'Procédure pas à pas : Créer un bouton avec XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [WPF]
ms.assetid: 138c41c4-1759-4bbf-8d77-77031a06a8a0
ms.openlocfilehash: c092ad49f40257467245a07a6e4b9849822e1835
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59076560"
---
# <a name="walkthrough-create-a-button-by-using-xaml"></a><span data-ttu-id="54e9f-102">Procédure pas à pas : Créer un bouton avec XAML</span><span class="sxs-lookup"><span data-stu-id="54e9f-102">Walkthrough: Create a Button by Using XAML</span></span>
<span data-ttu-id="54e9f-103">L’objectif de cette procédure pas à pas est d’apprendre à créer un bouton animé pour une utilisation dans une application Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="54e9f-103">The objective of this walkthrough is to learn how to create an animated button for use in a Windows Presentation Foundation (WPF) application.</span></span> <span data-ttu-id="54e9f-104">Cette procédure pas à pas utilise des styles et un modèle pour créer une ressource de bouton personnalisé qui permet la réutilisation du code et la séparation de la logique de bouton de la déclaration de bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-104">This walkthrough uses styles and a template to create a customized button resource that allows reuse of code and separation of button logic from the button declaration.</span></span> <span data-ttu-id="54e9f-105">Cette procédure pas à pas est écrite entièrement en [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="54e9f-105">This walkthrough is written entirely in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="54e9f-106">Cette procédure pas à pas vous guide tout au long des étapes de création de l’application en tapant ou copiant et collant [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] dans Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="54e9f-106">This walkthrough guides you through the steps for creating the application by typing or copying and pasting [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] into Microsoft Visual Studio.</span></span> <span data-ttu-id="54e9f-107">Si vous préférez apprendre à utiliser un outil de conception (Microsoft Expression Blend) pour créer la même application, consultez [créer un bouton à l’aide de Microsoft Expression Blend](walkthrough-create-a-button-by-using-microsoft-expression-blend.md).</span><span class="sxs-lookup"><span data-stu-id="54e9f-107">If you would prefer to learn how to use a design tool (Microsoft Expression Blend) to create the same application, see [Create a Button by Using Microsoft Expression Blend](walkthrough-create-a-button-by-using-microsoft-expression-blend.md).</span></span>  
  
 <span data-ttu-id="54e9f-108">La figure suivante montre les boutons terminés.</span><span class="sxs-lookup"><span data-stu-id="54e9f-108">The following figure shows the finished buttons.</span></span>  
  
 <span data-ttu-id="54e9f-109">![Boutons personnalisés qui ont été créés à l’aide de XAML](./media/custom-button-animatedbutton-5.gif "custom_button_AnimatedButton_5")</span><span class="sxs-lookup"><span data-stu-id="54e9f-109">![Custom buttons that were created by using XAML](./media/custom-button-animatedbutton-5.gif "custom_button_AnimatedButton_5")</span></span>  
  
## <a name="create-basic-buttons"></a><span data-ttu-id="54e9f-110">Créer des boutons de base</span><span class="sxs-lookup"><span data-stu-id="54e9f-110">Create Basic Buttons</span></span>  
 <span data-ttu-id="54e9f-111">Nous allons commencer en créant un nouveau projet et en ajoutant quelques boutons à la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="54e9f-111">Let's start by creating a new project and adding a few buttons to the window.</span></span>  
  
#### <a name="to-create-a-new-wpf-project-and-add-buttons-to-the-window"></a><span data-ttu-id="54e9f-112">Pour créer un projet WPF et ajouter des boutons à la fenêtre</span><span class="sxs-lookup"><span data-stu-id="54e9f-112">To create a new WPF project and add buttons to the window</span></span>  
  
1.  <span data-ttu-id="54e9f-113">Démarrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="54e9f-113">Start Visual Studio.</span></span>  
  
2.  <span data-ttu-id="54e9f-114">**Créez un projet WPF :** Dans le menu **Fichier** , pointez sur **Nouveau**, puis cliquez sur **Projet**.</span><span class="sxs-lookup"><span data-stu-id="54e9f-114">**Create a new WPF project:** On the **File** menu, point to **New**, and then click **Project**.</span></span> <span data-ttu-id="54e9f-115">Rechercher la **Application Windows (WPF)** modèle et nommez le projet « BoutonAnimé ».</span><span class="sxs-lookup"><span data-stu-id="54e9f-115">Find the **Windows Application (WPF)** template and name the project "AnimatedButton".</span></span> <span data-ttu-id="54e9f-116">Cela créera la structure pour l’application.</span><span class="sxs-lookup"><span data-stu-id="54e9f-116">This will create the skeleton for the application.</span></span>  
  
3.  <span data-ttu-id="54e9f-117">**Ajouter des boutons de base par défaut :** Tous les fichiers que vous avez besoin pour cette procédure pas à pas sont fournies par le modèle.</span><span class="sxs-lookup"><span data-stu-id="54e9f-117">**Add basic default buttons:** All the files you need for this walkthrough are provided by the template.</span></span> <span data-ttu-id="54e9f-118">Ouvrez le fichier Window1.xaml en double-cliquant dessus dans l’Explorateur de solutions.</span><span class="sxs-lookup"><span data-stu-id="54e9f-118">Open the Window1.xaml file by double clicking it in Solution Explorer.</span></span> <span data-ttu-id="54e9f-119">Par défaut, il existe un <xref:System.Windows.Controls.Grid> élément dans Window1.xaml.</span><span class="sxs-lookup"><span data-stu-id="54e9f-119">By default, there is a <xref:System.Windows.Controls.Grid> element in Window1.xaml.</span></span> <span data-ttu-id="54e9f-120">Supprimer le <xref:System.Windows.Controls.Grid> élément et ajouter quelques boutons à la [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] page en tapant ou copiant et collant le code en surbrillance suivant dans Window1.xaml :</span><span class="sxs-lookup"><span data-stu-id="54e9f-120">Remove the <xref:System.Windows.Controls.Grid> element and add a few buttons to the [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] page by typing or copy and pasting the following highlighted code to Window1.xaml:</span></span>  
  
    ```xaml  
    <Window x:Class="AnimatedButton.Window1"  
      xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
      xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
      Title="AnimatedButton" Height="300" Width="300"   
      Background="Black">
      <!-- Buttons arranged vertically inside a StackPanel. -->
      <StackPanel HorizontalAlignment="Left">
          <Button>Button 1</Button>
          <Button>Button 2</Button>
          <Button>Button 3</Button>
      </StackPanel>  
    </Window>  
    ```  
  
     <span data-ttu-id="54e9f-121">Appuyez sur F5 pour exécuter l’application. Vous devriez voir un ensemble de boutons qui ressemble à la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="54e9f-121">Press F5 to run the application; you should see a set of buttons that looks like the following figure.</span></span>  
  
     <span data-ttu-id="54e9f-122">![Trois boutons de base](./media/custom-button-animatedbutton-1.gif "custom_button_AnimatedButton_1")</span><span class="sxs-lookup"><span data-stu-id="54e9f-122">![Three basic buttons](./media/custom-button-animatedbutton-1.gif "custom_button_AnimatedButton_1")</span></span>  
  
     <span data-ttu-id="54e9f-123">Maintenant que vous avez créé les boutons de base, vous avez terminé de travailler dans le fichier Window1.xaml.</span><span class="sxs-lookup"><span data-stu-id="54e9f-123">Now that you have created the basic buttons, you are finished working in the Window1.xaml file.</span></span> <span data-ttu-id="54e9f-124">Le reste de la procédure pas à pas se concentre sur le fichier app.xaml, en définissant des styles et un modèle pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="54e9f-124">The rest of the walkthrough focuses on the app.xaml file, defining styles and a template for the buttons.</span></span>  
  
## <a name="set-basic-properties"></a><span data-ttu-id="54e9f-125">Définir les propriétés de base</span><span class="sxs-lookup"><span data-stu-id="54e9f-125">Set Basic Properties</span></span>  
 <span data-ttu-id="54e9f-126">Ensuite, nous allons définir certaines propriétés sur ces boutons pour contrôler l’apparence du bouton et la disposition.</span><span class="sxs-lookup"><span data-stu-id="54e9f-126">Next, let's set some properties on these buttons to control the button appearance and layout.</span></span> <span data-ttu-id="54e9f-127">Au lieu de définir des propriétés sur les boutons individuellement, vous allez utiliser des ressources pour définir les propriétés d’un bouton pour l’application entière.</span><span class="sxs-lookup"><span data-stu-id="54e9f-127">Rather than setting properties on the buttons individually, you will use resources to define button properties for the entire application.</span></span> <span data-ttu-id="54e9f-128">Ressources d’application sont conceptuellement semblables à externe [!INCLUDE[TLA#tla_css](../../../../includes/tlasharptla-css-md.md)] pour les pages Web ; Cependant, les ressources sont beaucoup plus puissantes que [!INCLUDE[TLA#tla_css](../../../../includes/tlasharptla-css-md.md)], comme vous le verrez par la fin de cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="54e9f-128">Application resources are conceptually similar to external [!INCLUDE[TLA#tla_css](../../../../includes/tlasharptla-css-md.md)] for Web pages; however, resources are much more powerful than [!INCLUDE[TLA#tla_css](../../../../includes/tlasharptla-css-md.md)], as you will see by the end of this walkthrough.</span></span> <span data-ttu-id="54e9f-129">Pour en savoir plus sur les ressources, consultez [XAML ressources](../advanced/xaml-resources.md).</span><span class="sxs-lookup"><span data-stu-id="54e9f-129">To learn more about resources, see [XAML Resources](../advanced/xaml-resources.md).</span></span>  
  
#### <a name="to-use-styles-to-set-basic-properties-on-the-buttons"></a><span data-ttu-id="54e9f-130">Pour utiliser des styles pour définir les propriétés de base sur les boutons</span><span class="sxs-lookup"><span data-stu-id="54e9f-130">To use styles to set basic properties on the buttons</span></span>  
  
1.  <span data-ttu-id="54e9f-131">**Définir un bloc Application.Resources :** Ouvrez app.xaml et ajoutez le balisage en surbrillance suivant si elle n’est pas déjà :</span><span class="sxs-lookup"><span data-stu-id="54e9f-131">**Define an Application.Resources block:** Open app.xaml and add the following highlighted markup if it is not already there:</span></span>  
  
    ```xaml  
    <Application x:Class="AnimatedButton.App"  
      xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"  
      xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"  
      StartupUri="Window1.xaml"  
      >  
      <Application.Resources>
        <!-- Resources for the entire application can be defined here. -->
      </Application.Resources>  
    </Application>  
    ```  
  
     <span data-ttu-id="54e9f-132">Étendue de la ressource est déterminée par où vous définissez la ressource.</span><span class="sxs-lookup"><span data-stu-id="54e9f-132">Resource scope is determined by where you define the resource.</span></span> <span data-ttu-id="54e9f-133">Définition des ressources dans `Application.Resources` du fichier App.XAML fichier permet à la ressource à utiliser à partir de n’importe où dans l’application.</span><span class="sxs-lookup"><span data-stu-id="54e9f-133">Defining resources in `Application.Resources` in the app.xaml file enables the resource to be used from anywhere in the application.</span></span> <span data-ttu-id="54e9f-134">Pour en savoir plus sur la définition de la portée de vos ressources, consultez [XAML ressources](../advanced/xaml-resources.md).</span><span class="sxs-lookup"><span data-stu-id="54e9f-134">To learn more about defining the scope of your resources, see [XAML Resources](../advanced/xaml-resources.md).</span></span>  
  
2.  <span data-ttu-id="54e9f-135">**Créer un style et définir des valeurs de propriété de base avec celui-ci :** Ajoutez le balisage suivant à la `Application.Resources` bloc.</span><span class="sxs-lookup"><span data-stu-id="54e9f-135">**Create a style and define basic property values with it:** Add the following markup to the `Application.Resources` block.</span></span> <span data-ttu-id="54e9f-136">Ce balisage crée un <xref:System.Windows.Style> qui s’applique à tous les boutons dans le paramètre d’application, le <xref:System.Windows.FrameworkElement.Width%2A> des boutons à 90 et le <xref:System.Windows.FrameworkElement.Margin%2A> à 10 :</span><span class="sxs-lookup"><span data-stu-id="54e9f-136">This markup creates a <xref:System.Windows.Style> that applies to all buttons in the application, setting the <xref:System.Windows.FrameworkElement.Width%2A> of the buttons to 90 and the <xref:System.Windows.FrameworkElement.Margin%2A> to 10:</span></span>  
  
    ```xaml  
    <Application.Resources>  
      <Style TargetType="Button">
        <Setter Property="Width" Value="90" />
        <Setter Property="Margin" Value="10" />
      </Style>  
    </Application.Resources>  
    ```  
  
     <span data-ttu-id="54e9f-137">Le <xref:System.Windows.Style.TargetType%2A> propriété spécifie que le style s’applique à tous les objets de type <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-137">The <xref:System.Windows.Style.TargetType%2A> property specifies that the style applies to all objects of type <xref:System.Windows.Controls.Button>.</span></span> <span data-ttu-id="54e9f-138">Chaque <xref:System.Windows.Setter> définit une valeur de propriété différente pour le <xref:System.Windows.Style>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-138">Each <xref:System.Windows.Setter> sets a different property value for the <xref:System.Windows.Style>.</span></span> <span data-ttu-id="54e9f-139">Par conséquent, à ce stade chaque bouton dans l’application a une largeur de 90 et une marge de 10.</span><span class="sxs-lookup"><span data-stu-id="54e9f-139">Therefore, at this point every button in the application has a width of 90 and a margin of 10.</span></span>  <span data-ttu-id="54e9f-140">Si vous appuyez sur F5 pour exécuter l’application, vous voyez la fenêtre suivante.</span><span class="sxs-lookup"><span data-stu-id="54e9f-140">If you press F5 to run the application, you see the following window.</span></span>  
  
     <span data-ttu-id="54e9f-141">![Boutons avec une largeur de 90 et une marge de 10](./media/custom-button-animatedbutton-2.gif "custom_button_AnimatedButton_2")</span><span class="sxs-lookup"><span data-stu-id="54e9f-141">![Buttons with a width of 90 and a margin of 10](./media/custom-button-animatedbutton-2.gif "custom_button_AnimatedButton_2")</span></span>  
  
     <span data-ttu-id="54e9f-142">Il est beaucoup plus, que vous pouvez effectuer avec des styles, incluant diverses méthodes permettant d’affiner quels objets sont ciblés, en spécifiant les valeurs de propriété complexes et même à l’aide de styles en tant qu’entrée pour d’autres styles.</span><span class="sxs-lookup"><span data-stu-id="54e9f-142">There is much more you can do with styles, including a variety of ways to fine-tune what objects are targeted, specifying complex property values, and even using styles as input for other styles.</span></span> <span data-ttu-id="54e9f-143">Pour plus d’informations, consultez [Application d’un style et création de modèles](styling-and-templating.md).</span><span class="sxs-lookup"><span data-stu-id="54e9f-143">For more information, see [Styling and Templating](styling-and-templating.md).</span></span>  
  
3.  <span data-ttu-id="54e9f-144">**Définissez une valeur de propriété de style à une ressource :** Ressources activer un moyen simple de réutiliser des objets couramment définis et les valeurs.</span><span class="sxs-lookup"><span data-stu-id="54e9f-144">**Set a style property value to a resource:** Resources enable a simple way to reuse commonly defined objects and values.</span></span> <span data-ttu-id="54e9f-145">Il est particulièrement utile définir des valeurs complexes à l’aide de ressources pour rendre votre code plus modulaire.</span><span class="sxs-lookup"><span data-stu-id="54e9f-145">It is especially useful to define complex values using resources to make your code more modular.</span></span> <span data-ttu-id="54e9f-146">Ajoutez le balisage en surbrillance suivant à app.xaml.</span><span class="sxs-lookup"><span data-stu-id="54e9f-146">Add the following highlighted markup to app.xaml.</span></span>  
  
    ```xaml  
    <Application.Resources>  
      <LinearGradientBrush x:Key="GrayBlueGradientBrush" StartPoint="0,0" EndPoint="1,1">
        <GradientStop Color="DarkGray" Offset="0" />
        <GradientStop Color="#CCCCFF" Offset="0.5" />
        <GradientStop Color="DarkGray" Offset="1" />
      </LinearGradientBrush>  
      <Style TargetType="{x:Type Button}">  
        <Setter Property="Background" Value="{StaticResource GrayBlueGradientBrush}" />  
        <Setter Property="Width" Value="80" />  
        <Setter Property="Margin" Value="10" />  
      </Style>  
    </Application.Resources>  
    ```  
  
     <span data-ttu-id="54e9f-147">Directement sous le `Application.Resources` bloc, vous avez créé une ressource appelée « GrayBlueGradientBrush ».</span><span class="sxs-lookup"><span data-stu-id="54e9f-147">Directly under the `Application.Resources` block, you created a resource called "GrayBlueGradientBrush".</span></span> <span data-ttu-id="54e9f-148">Cette ressource définit un dégradé horizontal.</span><span class="sxs-lookup"><span data-stu-id="54e9f-148">This resource defines a horizontal gradient.</span></span> <span data-ttu-id="54e9f-149">Cette ressource peut être utilisée comme une valeur de propriété à partir de n’importe où dans l’application, y compris à l’intérieur de l’accesseur Set de style bouton pour le <xref:System.Windows.Controls.Control.Background%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="54e9f-149">This resource can be used as a property value from anywhere in the application, including inside the button style setter for the <xref:System.Windows.Controls.Control.Background%2A> property.</span></span> <span data-ttu-id="54e9f-150">Maintenant, tous les boutons ont une <xref:System.Windows.Controls.Control.Background%2A> valeur de propriété de ce dégradé.</span><span class="sxs-lookup"><span data-stu-id="54e9f-150">Now, all the buttons have a <xref:System.Windows.Controls.Control.Background%2A> property value of this gradient.</span></span>  
  
     <span data-ttu-id="54e9f-151">Appuyez sur F5 pour exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="54e9f-151">Press F5 to run the application.</span></span> <span data-ttu-id="54e9f-152">Il doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="54e9f-152">It should look like the following.</span></span>  
  
     <span data-ttu-id="54e9f-153">![Boutons avec un arrière-plan dégradé](./media/custom-button-animatedbutton-3.gif "custom_button_AnimatedButton_3")</span><span class="sxs-lookup"><span data-stu-id="54e9f-153">![Buttons with a gradient background](./media/custom-button-animatedbutton-3.gif "custom_button_AnimatedButton_3")</span></span>  
  
## <a name="create-a-template-that-defines-the-look-of-the-button"></a><span data-ttu-id="54e9f-154">Créer un modèle qui définit l’apparence du bouton</span><span class="sxs-lookup"><span data-stu-id="54e9f-154">Create a Template That Defines the Look of the Button</span></span>  
 <span data-ttu-id="54e9f-155">Dans cette section, vous créez un modèle qui personnalise l’apparence (présentation) du bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-155">In this section, you create a template that customizes the appearance (presentation) of the button.</span></span> <span data-ttu-id="54e9f-156">La présentation du bouton est composée de plusieurs objets, y compris des rectangles et autres composants à accorder au bouton un aspect unique.</span><span class="sxs-lookup"><span data-stu-id="54e9f-156">The button presentation is made up of several objects including rectangles and other components to give the button a unique look.</span></span>  
  
 <span data-ttu-id="54e9f-157">Jusqu’ici, le contrôle de l’aspect de boutons dans l’application a été restreint à la modification des propriétés du bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-157">So far, the control of how buttons look in the application has been confined to changing properties of the button.</span></span> <span data-ttu-id="54e9f-158">Que se passe-t-il si vous souhaitez apporter des modifications plus radicales à l’apparence du bouton ?</span><span class="sxs-lookup"><span data-stu-id="54e9f-158">What if you want to make more radical changes to the button's appearance?</span></span> <span data-ttu-id="54e9f-159">Les modèles permettent un contrôle puissant sur la présentation d’un objet.</span><span class="sxs-lookup"><span data-stu-id="54e9f-159">Templates enable powerful control over the presentation of an object.</span></span> <span data-ttu-id="54e9f-160">Étant donné que les modèles peuvent être utilisés dans les styles, vous pouvez appliquer un modèle à tous les objets que le style s’applique à (dans cette procédure pas à pas, le bouton).</span><span class="sxs-lookup"><span data-stu-id="54e9f-160">Because templates can be used within styles, you can apply a template to all objects that the style applies to (in this walkthrough, the button).</span></span>  
  
#### <a name="to-use-the-template-to-define-the-look-of-the-button"></a><span data-ttu-id="54e9f-161">Pour utiliser le modèle pour définir l’apparence du bouton</span><span class="sxs-lookup"><span data-stu-id="54e9f-161">To use the template to define the look of the button</span></span>  
  
1.  <span data-ttu-id="54e9f-162">**Définir le modèle :** Étant donné que les contrôles tels que <xref:System.Windows.Controls.Button> ont un <xref:System.Windows.Controls.Control.Template%2A> propriété, vous pouvez définir la valeur de propriété de modèle comme les autres valeurs de propriété que nous avons défini dans un <xref:System.Windows.Style> à l’aide un <xref:System.Windows.Setter>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-162">**Set up the template:** Because controls like <xref:System.Windows.Controls.Button> have a <xref:System.Windows.Controls.Control.Template%2A> property, you can define the template property value just like the other property values we have set in a <xref:System.Windows.Style> using a <xref:System.Windows.Setter>.</span></span> <span data-ttu-id="54e9f-163">Ajoutez le balisage en surbrillance suivant à votre style de bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-163">Add the following highlighted markup to your button style.</span></span>  
  
    ```xaml
    <Application.Resources>  
      <LinearGradientBrush x:Key="GrayBlueGradientBrush"   
        StartPoint="0,0" EndPoint="1,1">  
        <GradientStop Color="DarkGray" Offset="0" />  
        <GradientStop Color="#CCCCFF" Offset="0.5" />  
        <GradientStop Color="DarkGray" Offset="1" />  
      </LinearGradientBrush>  
      <Style TargetType="{x:Type Button}">  
        <Setter Property="Background" Value="{StaticResource GrayBlueGradientBrush}" />  
        <Setter Property="Width" Value="80" />  
        <Setter Property="Margin" Value="10" />  
        <Setter Property="Template">
          <Setter.Value>
            <!-- The button template is defined here. -->
          </Setter.Value>
        </Setter>  
      </Style>  
    </Application.Resources>  
    ```  
  
2.  <span data-ttu-id="54e9f-164">**Modifier la présentation de bouton :** À ce stade, vous devez définir le modèle.</span><span class="sxs-lookup"><span data-stu-id="54e9f-164">**Alter button presentation:** At this point, you need to define the template.</span></span> <span data-ttu-id="54e9f-165">Ajoutez le balisage en surbrillance suivant.</span><span class="sxs-lookup"><span data-stu-id="54e9f-165">Add the following highlighted markup.</span></span> <span data-ttu-id="54e9f-166">Ce balisage spécifie deux <xref:System.Windows.Shapes.Rectangle> éléments avec des bords arrondis, suivi d’un <xref:System.Windows.Controls.DockPanel>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-166">This markup specifies two <xref:System.Windows.Shapes.Rectangle> elements with rounded edges, followed by a <xref:System.Windows.Controls.DockPanel>.</span></span> <span data-ttu-id="54e9f-167">Le <xref:System.Windows.Controls.DockPanel> est utilisé pour héberger le <xref:System.Windows.Controls.ContentPresenter> du bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-167">The <xref:System.Windows.Controls.DockPanel> is used to host the <xref:System.Windows.Controls.ContentPresenter> of the button.</span></span> <span data-ttu-id="54e9f-168">Un <xref:System.Windows.Controls.ContentPresenter> affiche le contenu du bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-168">A <xref:System.Windows.Controls.ContentPresenter> displays the content of the button.</span></span> <span data-ttu-id="54e9f-169">Dans cette procédure pas à pas, le contenu est texte (« Bouton 1 », « Bouton 2 », « Bouton 3 »).</span><span class="sxs-lookup"><span data-stu-id="54e9f-169">In this walkthrough, the content is text ("Button 1", "Button 2", "Button 3").</span></span> <span data-ttu-id="54e9f-170">Tous les composants de modèle (les rectangles et les <xref:System.Windows.Controls.DockPanel>) sont disposés à l’intérieur d’un <xref:System.Windows.Controls.Grid>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-170">All of the template components (the rectangles and the <xref:System.Windows.Controls.DockPanel>) are laid out inside of a <xref:System.Windows.Controls.Grid>.</span></span>  
  
    ```xaml  
    <Setter.Value>  
      <ControlTemplate TargetType="Button">
        <Grid Width="{TemplateBinding Width}" Height="{TemplateBinding Height}" ClipToBounds="True">
          <!-- Outer Rectangle with rounded corners. -->
          <Rectangle x:Name="outerRectangle" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" Stroke="{TemplateBinding Background}" RadiusX="20" RadiusY="20" StrokeThickness="5" Fill="Transparent" />
          <!-- Inner Rectangle with rounded corners. -->
          <Rectangle x:Name="innerRectangle" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" Stroke="Transparent" StrokeThickness="20" Fill="{TemplateBinding Background}" RadiusX="20" RadiusY="20" />
          <!-- Present Content (text) of the button. -->
          <DockPanel Name="myContentPresenterDockPanel">
            <ContentPresenter x:Name="myContentPresenter" Margin="20" Content="{TemplateBinding  Content}" TextBlock.Foreground="Black" />
          </DockPanel>
        </Grid>
      </ControlTemplate>  
    </Setter.Value>  
    ```  
  
     <span data-ttu-id="54e9f-171">Appuyez sur F5 pour exécuter l'application.</span><span class="sxs-lookup"><span data-stu-id="54e9f-171">Press F5 to run the application.</span></span> <span data-ttu-id="54e9f-172">Il doit ressembler à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="54e9f-172">It should look like the following.</span></span>  
  
     <span data-ttu-id="54e9f-173">![](./media/custom-button-animatedbutton-4.gif "custom_button_AnimatedButton_4")</span><span class="sxs-lookup"><span data-stu-id="54e9f-173">![](./media/custom-button-animatedbutton-4.gif "custom_button_AnimatedButton_4")</span></span>  
  
3.  <span data-ttu-id="54e9f-174">**Ajouter un effet verre au modèle :** Ensuite, vous allez ajouter le verre.</span><span class="sxs-lookup"><span data-stu-id="54e9f-174">**Add a glasseffect to the template:** Next you will add the glass.</span></span> <span data-ttu-id="54e9f-175">Tout d’abord, vous créez quelques ressources qui créent un effet de dégradé de transparence.</span><span class="sxs-lookup"><span data-stu-id="54e9f-175">First you create some resources that create a glass gradient effect.</span></span> <span data-ttu-id="54e9f-176">Ajoutez ces ressources dégradés n’importe où dans le `Application.Resources` bloc :</span><span class="sxs-lookup"><span data-stu-id="54e9f-176">Add these gradient resources anywhere within the `Application.Resources` block:</span></span>  
  
    ```xaml  
    <Application.Resources>  
      <GradientStopCollection x:Key="MyGlassGradientStopsResource">
        <GradientStop Color="WhiteSmoke" Offset="0.2" />     
        <GradientStop Color="Transparent" Offset="0.4" />    
        <GradientStop Color="WhiteSmoke" Offset="0.5" />     
        <GradientStop Color="Transparent" Offset="0.75" />     
        <GradientStop Color="WhiteSmoke" Offset="0.9" />     
        <GradientStop Color="Transparent" Offset="1" />   
      </GradientStopCollection>   
      <LinearGradientBrush x:Key="MyGlassBrushResource"    
        StartPoint="0,0" EndPoint="1,1" Opacity="0.75"
        GradientStops="{StaticResource MyGlassGradientStopsResource}" />  
    <!-- Styles and other resources below here. -->  
    ```  
  
     <span data-ttu-id="54e9f-177">Ces ressources sont utilisées en tant que le <xref:System.Windows.Shapes.Shape.Fill%2A> pour un rectangle que nous insérons dans le <xref:System.Windows.Controls.Grid> du modèle de bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-177">These resources are used as the <xref:System.Windows.Shapes.Shape.Fill%2A> for a rectangle that we insert into the <xref:System.Windows.Controls.Grid> of the button template.</span></span> <span data-ttu-id="54e9f-178">Ajoutez le balisage en surbrillance suivant au modèle.</span><span class="sxs-lookup"><span data-stu-id="54e9f-178">Add the following highlighted markup to the template.</span></span>  
  
    ```xaml
    <Setter.Value>  
      <ControlTemplate TargetType="{x:Type Button}">  
        <Grid Width="{TemplateBinding Width}" Height="{TemplateBinding Height}"  
          ClipToBounds="True">  
  
        <!-- Outer Rectangle with rounded corners. -->  
        <Rectangle x:Name="outerRectangle" HorizontalAlignment="Stretch"   
          VerticalAlignment="Stretch" Stroke="{TemplateBinding Background}"   
          RadiusX="20" RadiusY="20" StrokeThickness="5" Fill="Transparent" />  
  
        <!-- Inner Rectangle with rounded corners. -->  
        <Rectangle x:Name="innerRectangle" HorizontalAlignment="Stretch"   
          VerticalAlignment="Stretch" Stroke="Transparent" StrokeThickness="20"   
          Fill="{TemplateBinding Background}" RadiusX="20" RadiusY="20" />  
  
        <!-- Glass Rectangle -->     
        <Rectangle x:Name="glassCube" HorizontalAlignment="Stretch"       
          VerticalAlignment="Stretch"       
          StrokeThickness="2" RadiusX="10" RadiusY="10" Opacity="0"       
          Fill="{StaticResource MyGlassBrushResource}"       
          RenderTransformOrigin="0.5,0.5">
          <Rectangle.Stroke>         
            <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
              <LinearGradientBrush.GradientStops>
                <GradientStop Offset="0.0" Color="LightBlue" />
                <GradientStop Offset="1.0" Color="Gray" />
              </LinearGradientBrush.GradientStops>
            </LinearGradientBrush>       
          </Rectangle.Stroke>       
          <!-- These transforms have no effect as they are declared here.
          The reason the transforms are included is to be targets
          for animation (see later). -->       
          <Rectangle.RenderTransform>
            <TransformGroup>
              <ScaleTransform />
              <RotateTransform />
            </TransformGroup>
          </Rectangle.RenderTransform>
          <!-- A BevelBitmapEffect is applied to give the button a "Beveled" look. -->
          <Rectangle.BitmapEffect>
            <BevelBitmapEffect />
          </Rectangle.BitmapEffect>
        </Rectangle>  
  
        <!-- Present Text of the button. -->  
        <DockPanel Name="myContentPresenterDockPanel">  
          <ContentPresenter x:Name="myContentPresenter" Margin="20"   
            Content="{TemplateBinding  Content}" TextBlock.Foreground="Black" />  
        </DockPanel>  
      </Grid>  
    </ControlTemplate>  
    </Setter.Value>  
    ```  
  
     <span data-ttu-id="54e9f-179">Notez que le <xref:System.Windows.UIElement.Opacity%2A> du rectangle avec le `x:Name` propriété de « glassCube » est 0, donc lorsque vous exécutez l’exemple, vous ne voyez pas la superposition en haut du rectangle de verre.</span><span class="sxs-lookup"><span data-stu-id="54e9f-179">Notice that the <xref:System.Windows.UIElement.Opacity%2A> of the rectangle with the `x:Name` property of "glassCube" is 0, so when you run the sample, you do not see the glass rectangle overlaid on top.</span></span> <span data-ttu-id="54e9f-180">Il s’agit, car nous ajouterons ultérieurement des déclencheurs du modèle pour quand l’utilisateur interagit avec le bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-180">This is because we will later add triggers to the template for when the user interacts with the button.</span></span> <span data-ttu-id="54e9f-181">Toutefois, vous pouvez voir à quoi ressemble le bouton en modifiant la <xref:System.Windows.UIElement.Opacity%2A> valeur à 1 et à l’application en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="54e9f-181">However, you can see what the button looks like now by changing the <xref:System.Windows.UIElement.Opacity%2A> value to 1 and running the application.</span></span> <span data-ttu-id="54e9f-182">Voir l'illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="54e9f-182">See the following figure.</span></span> <span data-ttu-id="54e9f-183">Avant de passer à l’étape suivante, modifiez le <xref:System.Windows.UIElement.Opacity%2A> à 0.</span><span class="sxs-lookup"><span data-stu-id="54e9f-183">Before proceeding to the next step, change the <xref:System.Windows.UIElement.Opacity%2A> back to 0.</span></span>  
  
     <span data-ttu-id="54e9f-184">![Boutons personnalisés qui ont été créés à l’aide de XAML](./media/custom-button-animatedbutton-5.gif "custom_button_AnimatedButton_5")</span><span class="sxs-lookup"><span data-stu-id="54e9f-184">![Custom buttons that were created by using XAML](./media/custom-button-animatedbutton-5.gif "custom_button_AnimatedButton_5")</span></span>  
  
## <a name="create-button-interactivity"></a><span data-ttu-id="54e9f-185">Créer l’interactivité de bouton</span><span class="sxs-lookup"><span data-stu-id="54e9f-185">Create Button Interactivity</span></span>  
 <span data-ttu-id="54e9f-186">Dans cette section, vous allez créer des déclencheurs de propriété et des déclencheurs d’événements pour modifier les valeurs de propriété et exécuter des animations en réponse aux actions utilisateur telles que le déplacement du pointeur de la souris sur le bouton et en cliquant sur.</span><span class="sxs-lookup"><span data-stu-id="54e9f-186">In this section, you will create property triggers and event triggers to change property values and run animations in response to user actions such as moving the mouse pointer over the button and clicking.</span></span>  
  
 <span data-ttu-id="54e9f-187">Un moyen simple pour ajouter une interactivité (pointage avec la souris, éloignement de la souris, cliquez sur et ainsi de suite) consiste à définir des déclencheurs dans votre modèle ou style.</span><span class="sxs-lookup"><span data-stu-id="54e9f-187">An easy way to add interactivity (mouse-over, mouse-leave, click, and so on) is to define triggers within your template or style.</span></span> <span data-ttu-id="54e9f-188">Pour créer un <xref:System.Windows.Trigger>, vous définissez une propriété « condition » telles que : Le bouton <xref:System.Windows.UIElement.IsMouseOver%2A> valeur de propriété est égale à `true`.</span><span class="sxs-lookup"><span data-stu-id="54e9f-188">To create a <xref:System.Windows.Trigger>, you define a property "condition" such as: The button <xref:System.Windows.UIElement.IsMouseOver%2A> property value is equal to `true`.</span></span> <span data-ttu-id="54e9f-189">Vous définissez alors des accesseurs Set (actions) qui ont lieu lorsque la condition de déclenchement est remplie.</span><span class="sxs-lookup"><span data-stu-id="54e9f-189">You then define setters (actions) that take place when the trigger condition is true.</span></span>  
  
#### <a name="to-create-button-interactivity"></a><span data-ttu-id="54e9f-190">Pour créer l’interactivité de bouton</span><span class="sxs-lookup"><span data-stu-id="54e9f-190">To create button interactivity</span></span>  
  
1.  <span data-ttu-id="54e9f-191">**Ajouter des déclencheurs de modèle :** Ajoutez le balisage en surbrillance à votre modèle.</span><span class="sxs-lookup"><span data-stu-id="54e9f-191">**Add template triggers:** Add the highlighted markup to your template.</span></span>  
  
    ```xaml
    <Setter.Value>  
      <ControlTemplate TargetType="{x:Type Button}">  
        <Grid Width="{TemplateBinding Width}"   
          Height="{TemplateBinding Height}" ClipToBounds="True">  
  
          <!-- Outer Rectangle with rounded corners. -->  
          <Rectangle x:Name="outerRectangle" HorizontalAlignment="Stretch"   
          VerticalAlignment="Stretch" Stroke="{TemplateBinding Background}"   
          RadiusX="20" RadiusY="20" StrokeThickness="5" Fill="Transparent" />  
  
          <!-- Inner Rectangle with rounded corners. -->  
          <Rectangle x:Name="innerRectangle" HorizontalAlignment="Stretch"   
            VerticalAlignment="Stretch" Stroke="Transparent"   
            StrokeThickness="20"   
            Fill="{TemplateBinding Background}" RadiusX="20" RadiusY="20"   
          />  
  
          <!-- Glass Rectangle -->  
          <Rectangle x:Name="glassCube" HorizontalAlignment="Stretch"  
            VerticalAlignment="Stretch"  
            StrokeThickness="2" RadiusX="10" RadiusY="10" Opacity="0"  
            Fill="{StaticResource MyGlassBrushResource}"  
            RenderTransformOrigin="0.5,0.5">  
            <Rectangle.Stroke>  
              <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">  
                <LinearGradientBrush.GradientStops>  
                  <GradientStop Offset="0.0" Color="LightBlue" />  
                  <GradientStop Offset="1.0" Color="Gray" />  
                </LinearGradientBrush.GradientStops>  
              </LinearGradientBrush>  
            </Rectangle.Stroke>  
  
            <!-- These transforms have no effect as they   
                 are declared here.   
                 The reason the transforms are included is to be targets   
                 for animation (see later). -->  
            <Rectangle.RenderTransform>  
              <TransformGroup>  
                <ScaleTransform />  
                <RotateTransform />  
              </TransformGroup>  
            </Rectangle.RenderTransform>  
  
              <!-- A BevelBitmapEffect is applied to give the button a   
                   "Beveled" look. -->  
            <Rectangle.BitmapEffect>  
              <BevelBitmapEffect />  
            </Rectangle.BitmapEffect>  
          </Rectangle>  
  
          <!-- Present Text of the button. -->  
          <DockPanel Name="myContentPresenterDockPanel">  
            <ContentPresenter x:Name="myContentPresenter" Margin="20"   
              Content="{TemplateBinding  Content}" TextBlock.Foreground="Black" />  
          </DockPanel>  
        </Grid>  
  
        <ControlTemplate.Triggers>       <!-- Set action triggers for the buttons and define            what the button does in response to those triggers. -->     </ControlTemplate.Triggers>  
      </ControlTemplate>  
    </Setter.Value>  
    ```  
  
2.  <span data-ttu-id="54e9f-192">**Ajouter des déclencheurs de propriété :** Ajoutez le balisage en surbrillance à la `ControlTemplate.Triggers` bloc :</span><span class="sxs-lookup"><span data-stu-id="54e9f-192">**Add property triggers:** Add the highlighted markup to the `ControlTemplate.Triggers` block:</span></span>  
  
    ```xaml
    <ControlTemplate.Triggers>  
  
      <!-- Set properties when mouse pointer is over the button. -->   <Trigger Property="IsMouseOver" Value="True">     <!-- Below are three property settings that occur when the           condition is met (user mouses over button).  -->     <!-- Change the color of the outer rectangle when user           mouses over it. -->     <Setter Property ="Rectangle.Stroke" TargetName="outerRectangle"       Value="{DynamicResource {x:Static SystemColors.HighlightBrushKey}}" />     <!-- Sets the glass opacity to 1, therefore, the           glass "appears" when user mouses over it. -->     <Setter Property="Rectangle.Opacity" Value="1" TargetName="glassCube" />     <!-- Makes the text slightly blurry as though you           were looking at it through blurry glass. -->     <Setter Property="ContentPresenter.BitmapEffect"        TargetName="myContentPresenter">       <Setter.Value>         <BlurBitmapEffect Radius="1" />       </Setter.Value>     </Setter>   </Trigger>  
  
    <ControlTemplate.Triggers/>  
    ```  
  
     <span data-ttu-id="54e9f-193">Appuyez sur F5 pour exécuter l’application et de voir l’effet lorsque vous exécutez le pointeur de la souris sur les boutons.</span><span class="sxs-lookup"><span data-stu-id="54e9f-193">Press F5 to run the application and see the effect as you run the mouse pointer over the buttons.</span></span>  
  
3.  <span data-ttu-id="54e9f-194">**Ajouter un déclencheur de focus :** Ensuite, nous allons ajouter quelques méthodes setter similaire pour gérer les cas où le bouton a le focus (par exemple, une fois que l’utilisateur clique dessus).</span><span class="sxs-lookup"><span data-stu-id="54e9f-194">**Add a focus trigger:** Next, we'll add some similar setters to handle the case when the button has focus (for example, after the user clicks it).</span></span>  
  
    ```xaml  
    <ControlTemplate.Triggers>  
  
      <!-- Set properties when mouse pointer is over the button. -->  
      <Trigger Property="IsMouseOver" Value="True">  
  
        <!-- Below are three property settings that occur when the   
             condition is met (user mouses over button).  -->  
        <!-- Change the color of the outer rectangle when user          mouses over it. -->  
        <Setter Property ="Rectangle.Stroke" TargetName="outerRectangle"  
          Value="{DynamicResource {x:Static SystemColors.HighlightBrushKey}}" />  
  
        <!-- Sets the glass opacity to 1, therefore, the          glass "appears" when user mouses over it. -->  
        <Setter Property="Rectangle.Opacity" Value="1"       TargetName="glassCube" />  
  
        <!-- Makes the text slightly blurry as though you were          looking at it through blurry glass. -->  
        <Setter Property="ContentPresenter.BitmapEffect"       TargetName="myContentPresenter">  
          <Setter.Value>  
            <BlurBitmapEffect Radius="1" />  
          </Setter.Value>  
        </Setter>  
      </Trigger>  
      <!-- Set properties when button has focus. -->   <Trigger Property="IsFocused" Value="true">     <Setter Property="Rectangle.Opacity" Value="1"       TargetName="glassCube" />     <Setter Property="Rectangle.Stroke" TargetName="outerRectangle"       Value="{DynamicResource {x:Static SystemColors.HighlightBrushKey}}" />     <Setter Property="Rectangle.Opacity" Value="1" TargetName="glassCube" />   </Trigger>  
  
    </ControlTemplate.Triggers>  
    ```  
  
     <span data-ttu-id="54e9f-195">Appuyez sur F5 pour exécuter l’application et cliquez sur l’un des boutons.</span><span class="sxs-lookup"><span data-stu-id="54e9f-195">Press F5 to run the application and click on one of the buttons.</span></span> <span data-ttu-id="54e9f-196">Notez que le bouton reste en surbrillance une fois que vous cliquez dessus, car il a encore le focus.</span><span class="sxs-lookup"><span data-stu-id="54e9f-196">Notice that the button stays highlighted after you click it because it still has focus.</span></span> <span data-ttu-id="54e9f-197">Si vous cliquez sur un autre bouton, le nouveau bouton Obtient le focus, tandis que le dernier le perd.</span><span class="sxs-lookup"><span data-stu-id="54e9f-197">If you click another button, the new button gains focus while the last one loses it.</span></span>  
  
4.  <span data-ttu-id="54e9f-198">**Ajouter des animations pour** <xref:System.Windows.UIElement.MouseEnter> **et** <xref:System.Windows.UIElement.MouseLeave> **:** Ensuite, nous ajouter certaines animations aux déclencheurs.</span><span class="sxs-lookup"><span data-stu-id="54e9f-198">**Add animations for**  <xref:System.Windows.UIElement.MouseEnter> **and** <xref:System.Windows.UIElement.MouseLeave> **:** Next we add some animations to the triggers.</span></span> <span data-ttu-id="54e9f-199">Ajoutez le balisage suivant n’importe où à l’intérieur de la `ControlTemplate.Triggers` bloc.</span><span class="sxs-lookup"><span data-stu-id="54e9f-199">Add the following markup anywhere inside of the `ControlTemplate.Triggers` block.</span></span>  
  
    ```xaml
    <!-- Animations that start when mouse enters and leaves button. -->  
    <EventTrigger RoutedEvent="Mouse.MouseEnter">  
      <EventTrigger.Actions>  
        <BeginStoryboard Name="mouseEnterBeginStoryboard">  
          <Storyboard>  
          <!-- This animation makes the glass rectangle shrink in the X direction. -->  
            <DoubleAnimation Storyboard.TargetName="glassCube"   
              Storyboard.TargetProperty=  
              "(Rectangle.RenderTransform).(TransformGroup.Children)[0].(ScaleTransform.ScaleX)"  
              By="-0.1" Duration="0:0:0.5" />  
            <!-- This animation makes the glass rectangle shrink in the Y direction. -->  
            <DoubleAnimation  
            Storyboard.TargetName="glassCube"   
              Storyboard.TargetProperty=  
              "(Rectangle.RenderTransform).(TransformGroup.Children)[0].(ScaleTransform.ScaleY)"   
              By="-0.1" Duration="0:0:0.5" />  
          </Storyboard>  
        </BeginStoryboard>  
      </EventTrigger.Actions>  
    </EventTrigger>  
    <EventTrigger RoutedEvent="Mouse.MouseLeave">  
      <EventTrigger.Actions>  
        <!-- Stopping the storyboard sets all animated properties back to default. -->  
        <StopStoryboard BeginStoryboardName="mouseEnterBeginStoryboard" />  
      </EventTrigger.Actions>  
    </EventTrigger>  
    ```  
  
     <span data-ttu-id="54e9f-200">Le rectangle transparent est réduite lorsque le pointeur de la souris se déplace sur le bouton et revient à sa taille normale lorsque le pointeur quitte.</span><span class="sxs-lookup"><span data-stu-id="54e9f-200">The glass rectangle shrinks when the mouse pointer moves over the button and returns back to normal size when the pointer leaves.</span></span>  
  
     <span data-ttu-id="54e9f-201">Il existe deux animations qui sont déclenchées lorsque le pointeur passe sur le bouton (<xref:System.Windows.UIElement.MouseEnter> événement est déclenché).</span><span class="sxs-lookup"><span data-stu-id="54e9f-201">There are two animations that are triggered when the pointer goes over the button (<xref:System.Windows.UIElement.MouseEnter> event is raised).</span></span> <span data-ttu-id="54e9f-202">Ces animations réduisent le rectangle de verre sur l’axe des X et Y.</span><span class="sxs-lookup"><span data-stu-id="54e9f-202">These animations shrink the glass rectangle along the X and Y axis.</span></span> <span data-ttu-id="54e9f-203">Notez les propriétés sur le <xref:System.Windows.Media.Animation.DoubleAnimation> éléments — <xref:System.Windows.Media.Animation.Timeline.Duration%2A> et <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-203">Notice the properties on the <xref:System.Windows.Media.Animation.DoubleAnimation> elements — <xref:System.Windows.Media.Animation.Timeline.Duration%2A> and <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A>.</span></span> <span data-ttu-id="54e9f-204">Le <xref:System.Windows.Media.Animation.Timeline.Duration%2A> Spécifie que l’animation se produit pendant une demi-seconde, et <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> Spécifie que le verre se réduit de 10 %.</span><span class="sxs-lookup"><span data-stu-id="54e9f-204">The <xref:System.Windows.Media.Animation.Timeline.Duration%2A> specifies that the animation occurs over half a second, and <xref:System.Windows.Media.Animation.DoubleAnimation.By%2A> specifies that the glass shrinks by 10%.</span></span>  
  
     <span data-ttu-id="54e9f-205">Le second déclencheur d’événement (<xref:System.Windows.UIElement.MouseLeave>) arrête simplement le premier.</span><span class="sxs-lookup"><span data-stu-id="54e9f-205">The second event trigger (<xref:System.Windows.UIElement.MouseLeave>) simply stops the first one.</span></span> <span data-ttu-id="54e9f-206">Lorsque vous arrêtez un <xref:System.Windows.Media.Animation.Storyboard>, toutes les propriétés animées retournent leurs valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="54e9f-206">When you stop a <xref:System.Windows.Media.Animation.Storyboard>, all the animated properties return to their default values.</span></span> <span data-ttu-id="54e9f-207">Par conséquent, lorsque l’utilisateur déplace le pointeur hors du bouton, le bouton revient à la façon dont il avait avant le pointeur de la souris est déplacé sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-207">Therefore, when the user moves the pointer off the button, the button goes back to the way it was before the mouse pointer moved over the button.</span></span> <span data-ttu-id="54e9f-208">Pour plus d’informations sur les animations, consultez [vue d’ensemble de l’Animation](../graphics-multimedia/animation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="54e9f-208">For more information about animations, see [Animation Overview](../graphics-multimedia/animation-overview.md).</span></span>  
  
5.  <span data-ttu-id="54e9f-209">**Ajouter une animation lorsque le bouton est cliqué :** L’étape finale consiste à ajouter un déclencheur pour lorsque l’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="54e9f-209">**Add an animation for when the button is clicked:** The final step is to add a trigger for when the user clicks the button.</span></span> <span data-ttu-id="54e9f-210">Ajoutez le balisage suivant n’importe où à l’intérieur de la `ControlTemplate.Triggers` bloc :</span><span class="sxs-lookup"><span data-stu-id="54e9f-210">Add the following markup anywhere inside of the `ControlTemplate.Triggers` block:</span></span>  
  
    ```xaml
    <!-- Animation fires when button is clicked, causing glass to spin.  -->  
    <EventTrigger RoutedEvent="Button.Click">  
      <EventTrigger.Actions>  
        <BeginStoryboard>  
          <Storyboard>  
            <DoubleAnimation Storyboard.TargetName="glassCube"   
              Storyboard.TargetProperty=  
              "(Rectangle.RenderTransform).(TransformGroup.Children)[1].(RotateTransform.Angle)"   
              By="360" Duration="0:0:0.5" />  
          </Storyboard>  
        </BeginStoryboard>  
      </EventTrigger.Actions>  
    </EventTrigger>  
    ```  
  
     <span data-ttu-id="54e9f-211">Appuyez sur F5 pour exécuter l’application, puis cliquez sur un des boutons.</span><span class="sxs-lookup"><span data-stu-id="54e9f-211">Press F5 to run the application, and click one of the buttons.</span></span> <span data-ttu-id="54e9f-212">Lorsque vous cliquez sur un bouton, le rectangle de verre tourne.</span><span class="sxs-lookup"><span data-stu-id="54e9f-212">When you click a button, the glass rectangle spins around.</span></span>  
  
## <a name="summary"></a><span data-ttu-id="54e9f-213">Récapitulatif</span><span class="sxs-lookup"><span data-stu-id="54e9f-213">Summary</span></span>  
 <span data-ttu-id="54e9f-214">Dans cette procédure pas à pas, vous avez effectué les exercices suivants :</span><span class="sxs-lookup"><span data-stu-id="54e9f-214">In this walkthrough, you performed the following exercises:</span></span>  
  
-   <span data-ttu-id="54e9f-215">Ciblé un <xref:System.Windows.Style> à un type d’objet (<xref:System.Windows.Controls.Button>).</span><span class="sxs-lookup"><span data-stu-id="54e9f-215">Targeted a <xref:System.Windows.Style> to an object type (<xref:System.Windows.Controls.Button>).</span></span>  
  
-   <span data-ttu-id="54e9f-216">Contrôlé des propriétés de base des boutons dans l’ensemble de l’application à l’aide de la <xref:System.Windows.Style>.</span><span class="sxs-lookup"><span data-stu-id="54e9f-216">Controlled basic properties of the buttons in the entire application using the <xref:System.Windows.Style>.</span></span>  
  
-   <span data-ttu-id="54e9f-217">Créé des ressources telles que des dégradés à utiliser pour les valeurs de propriété de la <xref:System.Windows.Style> setters.</span><span class="sxs-lookup"><span data-stu-id="54e9f-217">Created resources like gradients to use for property values of the <xref:System.Windows.Style> setters.</span></span>  
  
-   <span data-ttu-id="54e9f-218">Personnalisé l’apparence des boutons dans l’application entière en appliquant un modèle pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="54e9f-218">Customized the look of buttons in the entire application by applying a template to the buttons.</span></span>  
  
-   <span data-ttu-id="54e9f-219">Personnaliser le comportement pour les boutons en réponse aux actions de l’utilisateur (tel que <xref:System.Windows.UIElement.MouseEnter>, <xref:System.Windows.UIElement.MouseLeave>, et <xref:System.Windows.Controls.Primitives.ButtonBase.Click>) incluant des effets d’animation.</span><span class="sxs-lookup"><span data-stu-id="54e9f-219">Customized behavior for the buttons in response to user actions (such as <xref:System.Windows.UIElement.MouseEnter>, <xref:System.Windows.UIElement.MouseLeave>, and <xref:System.Windows.Controls.Primitives.ButtonBase.Click>) that included animation effects.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54e9f-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54e9f-220">See also</span></span>

- [<span data-ttu-id="54e9f-221">Créer un bouton à l’aide de Microsoft Expression Blend</span><span class="sxs-lookup"><span data-stu-id="54e9f-221">Create a Button by Using Microsoft Expression Blend</span></span>](walkthrough-create-a-button-by-using-microsoft-expression-blend.md)
- [<span data-ttu-id="54e9f-222">Application d'un style et création de modèles</span><span class="sxs-lookup"><span data-stu-id="54e9f-222">Styling and Templating</span></span>](styling-and-templating.md)
- [<span data-ttu-id="54e9f-223">Vue d'ensemble de l'animation</span><span class="sxs-lookup"><span data-stu-id="54e9f-223">Animation Overview</span></span>](../graphics-multimedia/animation-overview.md)
- [<span data-ttu-id="54e9f-224">Vue d'ensemble de la peinture avec des couleurs unies ou des dégradés</span><span class="sxs-lookup"><span data-stu-id="54e9f-224">Painting with Solid Colors and Gradients Overview</span></span>](../graphics-multimedia/painting-with-solid-colors-and-gradients-overview.md)
- [<span data-ttu-id="54e9f-225">Vue d'ensemble des effets bitmap</span><span class="sxs-lookup"><span data-stu-id="54e9f-225">Bitmap Effects Overview</span></span>](../graphics-multimedia/bitmap-effects-overview.md)
