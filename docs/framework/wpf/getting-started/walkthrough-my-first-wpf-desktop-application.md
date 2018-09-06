---
title: Créer une application WPF dans Visual Studio
ms.date: 04/12/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting started [WPF], WPF
- WPF [WPF], getting started
ms.assetid: b96bed40-8946-4285-8fe4-88045ab854ed
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a8f806a1f1f7840f21e82d77d1b639b9318259e7
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43885179"
---
# <a name="walkthrough-my-first-wpf-desktop-application"></a>Procédure pas à pas : ma première application de bureau WPF

Cet article vous montre comment développer une application Windows Presentation Foundation (WPF) simple qui inclut les éléments qui sont communes à la plupart des applications WPF : balisage de d’Extensible Application Markup Language (XAML), code-behind, définitions d’application, contrôles, disposition, liaison de données et styles.

Cette procédure pas à pas comprend les étapes suivantes :

- XAML permet de concevoir l’apparence de l’interface utilisateur de l’application (IU).

- Écrire du code pour générer le comportement de l’application.

- Créer une définition d’application pour gérer l’application.

- Ajouter des contrôles et créer la disposition pour composer l’interface utilisateur de l’application.

- Créer des styles pour une apparence cohérente tout au long de l’interface utilisateur d’une application.

- Lier l’interface utilisateur aux données pour remplir l’interface utilisateur à partir des données et de conserver les données et l’interface utilisateur synchronisé.

À la fin de la procédure pas à pas, vous aurez créé une application Windows qui permet aux utilisateurs d’afficher les notes de frais pour certaines personnes autonome. L’application est composée de plusieurs pages WPF sont hébergées dans une fenêtre de style navigateur.

> [!TIP]
> L’exemple de code qui est utilisé pour générer cette procédure pas à pas est disponible pour Visual Basic et c# dans [Introduction to Building WPF Applications](https://go.microsoft.com/fwlink/?LinkID=160008).

## <a name="prerequisites"></a>Prérequis

- Visual Studio 2012 ou version ultérieure

Pour plus d’informations sur l’installation de la dernière version de Visual Studio, consultez [installer Visual Studio](/visualstudio/install/install-visual-studio).

## <a name="create-the-application-project"></a>Créer le projet d’application

La première étape consiste à créer l’infrastructure d’application, qui inclut une définition d’application, deux pages et une image.

1. Créer un nouveau projet d’Application WPF en Visual Basic ou Visual c# nommé **`ExpenseIt`**:

   1. Ouvrez Visual Studio et sélectionnez **fichier** > **New** > **projet**.

      Le **nouveau projet** boîte de dialogue s’ouvre.

   2. Sous le **installé** catégorie, développez le **Visual C#** ou **Visual Basic** nœud, puis sélectionnez **bureau classique Windows**.

   3. Sélectionnez le **application WPF (.NET Framework)** modèle. Entrez le nom **`ExpenseIt`** , puis sélectionnez **OK**.

      ![Boîte de dialogue Nouveau projet avec une application WPF sélectionnée](media/new-project-dialog.png)

      Visual Studio crée le projet et ouvre le concepteur pour la fenêtre d’application par défaut nommé **MainWindow.xaml**.

   > [!NOTE]
   > Cette procédure pas à pas utilise le <xref:System.Windows.Controls.DataGrid> contrôle qui est disponible dans le .NET Framework 4 et versions ultérieures. Être sûr que votre projet cible le .NET Framework 4 ou version ultérieure. Pour plus d’informations, consultez [Guide pratique pour cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).

2. Ouvrez *Application.xaml* (Visual Basic) ou *App.xaml* (c#).

    Ce fichier XAML définit une application WPF et les ressources de l’application. Vous utilisez également ce fichier pour spécifier l’interface utilisateur qui s’affiche automatiquement quand l’application démarre ; Dans ce cas, *MainWindow.xaml*.

    Votre XAML doit ressembler à ceci en Visual Basic :

    [!code-xaml[ExpenseIt#1_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/Application.xaml#1_a)]

    Ou à cela en C# :

    [!code-xaml[ExpenseIt#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/App.xaml#1)]

3. Ouvrez *MainWindow.xaml*.

    Ce fichier XAML est la fenêtre principale de votre application et affiche le contenu créé dans les pages. Le <xref:System.Windows.Window> classe définit les propriétés d’une fenêtre, telles que son titre, taille ou icône et gère les événements, tels que la fermeture ou le masquage.

4. Modifier le <xref:System.Windows.Window> élément à un <xref:System.Windows.Navigation.NavigationWindow>, comme illustré dans le XAML suivant :

   ```xaml
   <NavigationWindow x:Class="ExpenseIt.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        ...
   </NavigationWindow>
   ```

   Cette application accède à un contenu différent en fonction de l’entrée utilisateur. C’est pourquoi les principaux <xref:System.Windows.Window> doit être changé en un <xref:System.Windows.Navigation.NavigationWindow>. <xref:System.Windows.Navigation.NavigationWindow> hérite de toutes les propriétés de <xref:System.Windows.Window>. Le <xref:System.Windows.Navigation.NavigationWindow> élément dans le fichier XAML crée une instance de la <xref:System.Windows.Navigation.NavigationWindow> classe. Pour plus d’informations, consultez [vue d’ensemble de la Navigation](../../../../docs/framework/wpf/app-development/navigation-overview.md).

5. Modifiez les propriétés suivantes sur le <xref:System.Windows.Navigation.NavigationWindow> élément :

    - Définir le <xref:System.Windows.Window.Title%2A> propriété à «`ExpenseIt`».

    - Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété 500 pixels.

    - Définir le <xref:System.Windows.FrameworkElement.Height%2A> propriété sur 350 pixels.

    - Supprimer le <xref:System.Windows.Controls.Grid> éléments entre le <xref:System.Windows.Navigation.NavigationWindow> balises.

    Votre XAML doit ressembler à ceci en Visual Basic :

    [!code-xaml[ExpenseIt#2_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt/MainWindow.xaml#2_a)]

    Ou à cela en C# :

    [!code-xaml[ExpenseIt#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml#2)]

6. Ouvrez *MainWindow.xaml.vb* ou *MainWindow.xaml.cs*.

    Ce fichier est un fichier code-behind qui contient le code pour gérer les événements déclarés dans *MainWindow.xaml*. Ce fichier contient une classe partielle pour la fenêtre définie en XAML.

7. Si vous utilisez c#, modifiez le `MainWindow` classe à dériver de <xref:System.Windows.Navigation.NavigationWindow>. (En Visual Basic, cela se produit automatiquement lorsque vous modifiez la fenêtre en XAML.)

   Votre code doit ressembler à ceci :

   [!code-csharp[ExpenseIt#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml.cs#3)]
   [!code-vb[ExpenseIt#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml.vb#3)]

   > [!TIP]
   > Vous pouvez activer/désactiver le langage de code de l’exemple de code entre c# et Visual Basic dans le **langage** déroulante sur le coin supérieur droit de cet article.

## <a name="add-files-to-the-application"></a>Ajouter des fichiers à l’application

Dans cette section, vous allez ajouter deux pages et une image à l’application.

1. Ajouter une nouvelle page WPF au projet et nommez-le *`ExpenseItHome.xaml`*:

   1. Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.

   1. Dans le **ajouter un nouvel élément** boîte de dialogue, le **Page (WPF)** modèle est déjà sélectionné. Entrez le nom **`ExpenseItHome`**, puis sélectionnez **ajouter**.

    Cette page est la première page qui s’affiche lorsque l’application est lancée. Il affiche une liste de personnes, pour afficher une note de frais.

2. Ouvrez *`ExpenseItHome.xaml`*.

3. Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - Home`».

    Votre XAML doit ressembler à ceci en Visual Basic :

    [!code-xaml[ExpenseIt#6_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml#6_a)]

    Ou à cela en C# :

    [!code-xaml[ExpenseIt#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml#6)]

4. Ouvrez *MainWindow.xaml*.

5. Définir le <xref:System.Windows.Navigation.NavigationWindow.Source%2A> propriété sur le <xref:System.Windows.Navigation.NavigationWindow> à «`ExpenseItHome.xaml`».

    Cela définit *`ExpenseItHome.xaml`* être la première page ouverte au démarrage de l’application. Votre XAML doit ressembler à ceci en Visual Basic :

    [!code-xaml[ExpenseIt#7_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml#7_a)]

    Ou à cela en C# :

    [!code-xaml[ExpenseIt#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/MainWindow.xaml#7)]

   > [!TIP]
   > Vous pouvez également définir le **Source** propriété dans le **divers** catégorie de la **propriétés** fenêtre.
   >
   > ![Propriété de source dans la fenêtre Propriétés](media/properties-source.png)

6. Ajoutez une autre nouvelle page WPF au projet et nommez-le *ExpenseReportPage.xaml*::

   1. Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.

   1. Dans le **ajouter un nouvel élément** boîte de dialogue, le **Page (WPF)** modèle est déjà sélectionné. Entrez le nom **ExpenseReportPage**, puis sélectionnez **ajouter**.

    Cette page affiche la note de frais pour la personne sélectionnée sur le **`ExpenseItHome`** page.

7. Ouvrez *ExpenseReportPage.xaml*.

8. Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - View Expense`».

    Votre XAML doit ressembler à ceci en Visual Basic :

    [!code-xaml[ExpenseIt#4_A](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml#4_a)]

    Ou à cela en C# :

    [!code-xaml[ExpenseIt#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml#4)]

9. Ouvrez *ExpenseItHome.xaml.vb* et *ExpenseReportPage.xaml.vb*, ou *ExpenseItHome.xaml.cs* et *ExpenseReportPage.xaml.cs*.

    Lorsque vous créez un nouveau fichier de Page, Visual Studio crée automatiquement un *code-behind* fichier. Ces fichiers code-behind gèrent la logique pour répondre à une saisie de l’utilisateur.

    Votre code doit ressembler à ceci pour **`ExpenseItHome`**:

    [!code-csharp[ExpenseIt#2_5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml.cs#2_5)]
    [!code-vb[ExpenseIt#2_5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml.vb#2_5)]

    Et comme suit pour **ExpenseReportPage**:

    [!code-csharp[ExpenseIt#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml.cs#5)]
    [!code-vb[ExpenseIt#5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml.vb#5)]

10. Ajouter une image nommée *watermark.png* au projet. Vous pouvez créer votre propre image, copiez le fichier à partir de l’exemple de code ou obtenez-le [ici](https://github.com/dotnet/docs/blob/master/docs/framework/wpf/getting-started/media/watermark.png).

   1. Avec le bouton droit sur le nœud du projet et sélectionnez **ajouter** > **élément existant**, ou appuyez sur **MAJ**+**Alt** + **A**.

   2. Dans le **ajouter un élément existant** boîte de dialogue, accédez au fichier image que vous souhaitez utiliser, puis sélectionnez **ajouter**.

## <a name="build-and-run-the-application"></a>Générez et exécutez l'application.

1. Pour générer et exécuter l’application, appuyez sur **F5** ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu.

    L’illustration suivante montre l’application avec le <xref:System.Windows.Navigation.NavigationWindow> boutons :

    ![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure1.png)

2. Fermez l’application pour revenir à Visual Studio.

## <a name="create-the-layout"></a>Créer la disposition

Mise en page offre un moyen ordonné de placer des éléments d’interface utilisateur et gère également la taille et la position de ces éléments lors du redimensionnée d’une interface utilisateur. En règle générale, vous allez créer une disposition avec l’un des contrôles de disposition suivants :

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.DockPanel>
- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.VirtualizingStackPanel>
- <xref:System.Windows.Controls.WrapPanel>

Chacun de ces contrôles de disposition prend en charge un type spécial de disposition pour ses éléments enfants. `ExpenseIt` pages peuvent être redimensionnés, et chaque page comporte des éléments organisés horizontalement et verticalement en même temps que d’autres éléments. Par conséquent, le <xref:System.Windows.Controls.Grid> est l’élément de disposition idéal pour l’application.

> [!TIP]
> Pour plus d’informations sur <xref:System.Windows.Controls.Panel> éléments, consultez [vue d’ensemble de panneaux](../../../../docs/framework/wpf/controls/panels-overview.md). Pour plus d’informations sur la disposition, consultez [disposition](../../../../docs/framework/wpf/advanced/layout.md).

Dans la section, vous créez une seule colonne de table avec trois lignes et une marge de 10 pixels en ajoutant des définitions de colonne et de ligne à la <xref:System.Windows.Controls.Grid> dans *`ExpenseItHome.xaml`*.

1. Ouvrez *`ExpenseItHome.xaml`*.

2. Définir le <xref:System.Windows.FrameworkElement.Margin%2A> propriété sur le <xref:System.Windows.Controls.Grid> élément valeur « 10,0,10,10 » qui correspond aux marges gauche, haut, droite et bas :

   ```xaml
   <Grid Margin="10,0,10,10">
   ```

   > [!TIP]
   > Vous pouvez également définir le **marge** des valeurs dans le **propriétés** fenêtre, sous le **disposition** catégorie :
   >
   > ![Valeurs de marge dans la fenêtre Propriétés](media/properties-margin.png)

3. Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises pour créer les définitions de ligne et de colonne :

    [!code-xaml[ExpenseIt#8](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#8)]

    Le <xref:System.Windows.Controls.RowDefinition.Height%2A> de deux lignes est définie sur <xref:System.Windows.GridLength.Auto%2A>, ce qui signifie que les lignes sont dimensionnés de base sur le contenu dans les lignes. La valeur par défaut <xref:System.Windows.Controls.RowDefinition.Height%2A> est <xref:System.Windows.GridUnitType.Star> dimensionnement, ce qui signifie que la hauteur de ligne est une proportion pondérée de l’espace disponible. Par exemple, si deux lignes ont une <xref:System.Windows.Controls.RowDefinition.Height%2A> de « * », ils ont chacun une hauteur qui représente la moitié de l’espace disponible.

    Votre <xref:System.Windows.Controls.Grid> doit maintenant ressembler au XAML suivant :

    [!code-xaml[ExpenseIt#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#9)]

## <a name="add-controls"></a>Ajouter des contrôles

Dans cette section, vous allez mettre à jour l’interface utilisateur pour afficher la liste des personnes avec lesquelles un utilisateur peut sélectionner pour afficher la note de frais pour la page d’accueil. Les contrôles sont des objets d’interface utilisateur qui permettent aux utilisateurs d’interagir avec votre application. Pour plus d’informations, consultez [Contrôles](../../../../docs/framework/wpf/controls/index.md).

Pour créer cette interface utilisateur, vous allez ajouter les éléments suivants à *`ExpenseItHome.xaml`*:

- <xref:System.Windows.Controls.ListBox> (pour la liste de personnes).
- <xref:System.Windows.Controls.Label> (pour l’en-tête de liste).
- <xref:System.Windows.Controls.Button> (sur lequel cliquer pour afficher la note de frais pour la personne qui est sélectionnée dans la liste).

Chaque contrôle est placé dans une ligne de la <xref:System.Windows.Controls.Grid> en définissant le <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> propriété jointe. Pour plus d’informations sur les propriétés jointes, consultez [vue d’ensemble des propriétés jointes](../../../../docs/framework/wpf/advanced/attached-properties-overview.md).

1. Ouvrez *`ExpenseItHome.xaml`*.

2. Ajoutez le XAML suivant quelque part entre le <xref:System.Windows.Controls.Grid> balises :

   [!code-xaml[ExpenseIt#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt4/ExpenseItHome.xaml#10)]

   > [!TIP]
   > Vous pouvez également créer les contrôles en les faisant glisser à partir de la **boîte à outils** fenêtre sur la fenêtre de conception, puis en définissant leurs propriétés le **propriétés** fenêtre.

3. Générez et exécutez l’application.

L’illustration suivante montre les contrôles que vous venez de créer :

![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure2.png)

## <a name="add-an-image-and-a-title"></a>Ajouter une image et un titre

Dans cette section, vous allez mettre à jour l’interface utilisateur de la page d’accueil avec une image et un titre de page.

1. Ouvrez *`ExpenseItHome.xaml`*.

2. Ajouter une autre colonne à la <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> fixe <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de 230 pixels :

    [!code-xaml[ExpenseIt#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#11)]

3. Ajouter une autre ligne à la <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, pour un total de quatre lignes :

    [!code-xaml[ExpenseIt#11b](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#11b)]

4. Déplacer les contrôles vers la deuxième colonne en définissant le <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> propriété sur 1 dans chacun des trois contrôles (bordure, ListBox et bouton).

5. Déplacez chaque contrôle d’une ligne, vers le bas en incrémentant son <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> valeur par 1.

   Le XAML pour les trois contrôles ressemble maintenant à ceci :

    [!code-xaml[ExpenseIt#12](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#12)]

6. Définir le <xref:System.Windows.Controls.Panel.Background%2A> de la <xref:System.Windows.Controls.Grid> pour être le *watermark.png* fichier image, en ajoutant le XAML suivant quelque part entre le `<Grid>` et `</Grid>` balises :

    [!code-xaml[ExpenseIt#14](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#14)]

7. Avant du <xref:System.Windows.Controls.Border> élément, ajoutez un <xref:System.Windows.Controls.Label> avec le contenu « View Expense Report ». Il s’agit du titre de la page.

    [!code-xaml[ExpenseIt#13](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#13)]

8. Générez et exécutez l’application.

L’illustration suivante montre les résultats de ce que vous venez d’ajouter :

![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure3.png)

## <a name="add-code-to-handle-events"></a>Ajoutez du code pour gérer les événements

1. Ouvrez *`ExpenseItHome.xaml`*.

2. Ajouter un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements à la <xref:System.Windows.Controls.Button> élément. Pour plus d’informations, consultez [Comment : créer un gestionnaire d’événements simple](https://msdn.microsoft.com/library/b1456e07-9dec-4354-99cf-18666b64f480).

    [!code-xaml[ExpenseIt#15](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml#15)]

3. Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.

4. Ajoutez le code suivant à la `ExpenseItHome` classe pour ajouter un bouton Gestionnaire d’événements click. Le Gestionnaire d’événements ouvre le **ExpenseReportPage** page.

    [!code-csharp[ExpenseIt#16](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml.cs#16)]
    [!code-vb[ExpenseIt#16](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt6/ExpenseItHome.xaml.vb#16)]

## <a name="create-the-ui-for-expensereportpage"></a>Créer l’interface utilisateur pour ExpenseReportPage

*ExpenseReportPage.xaml* affiche la note de frais de la personne qui est sélectionnée sur la **`ExpenseItHome`** page. Dans cette section, vous allez créer l’interface utilisateur pour **ExpenseReportPage**. Vous également ajouter d’arrière-plan et les couleurs aux divers éléments d’interface utilisateur de remplissage.

1. Ouvrez *ExpenseReportPage.xaml*.

2. Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises :

    [!code-xaml[ExpenseIt#17](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseReportPage.xaml#17)]

    Cette interface utilisateur est similaire à *`ExpenseItHome.xaml`*, sauf que les données du rapport s’affiche dans un <xref:System.Windows.Controls.DataGrid>.

3. Générez et exécutez l’application.

    > [!NOTE]
    > Si vous obtenez une erreur le <xref:System.Windows.Controls.DataGrid> est introuvable ou n’existe pas, vérifiez que votre projet cible le .NET Framework 4 ou version ultérieur. Pour plus d’informations, consultez [Guide pratique pour cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).

4. Sélectionnez le **vue** bouton.

    La page de note de frais s’affiche. Notez également que le bouton de navigation arrière est activé.

L’illustration suivante montre les éléments d’interface utilisateur ajoutés à *ExpenseReportPage.xaml*.

![Capture d’écran : exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure4.png)

## <a name="style-controls"></a>Style aux contrôles

L’apparence des différents éléments est souvent le même pour tous les éléments du même type dans une interface utilisateur. Utilise l’interface utilisateur [styles](../../../../docs/framework/wpf/controls/styling-and-templating.md) pour pouvoir réutiliser l’apparence des différents éléments. La réutilisation des styles permet de simplifier la gestion et la création de XAML. Cette section remplace par des styles les attributs d’élément qui ont été définis lors des étapes précédentes.

1. Ouvrez *Application.xaml* ou *App.xaml*.

2. Ajoutez le XAML suivant entre les <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> balises :

    [!code-xaml[ExpenseIt#18](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/App.xaml#18)]

    Ce code XAML ajoute les styles suivants :

    - `headerTextStyle`: pour mettre en forme le titre de la page <xref:System.Windows.Controls.Label>.

    - `labelStyle`: pour mettre en forme les contrôles <xref:System.Windows.Controls.Label> .

    - `columnHeaderStyle`: pour mettre en forme <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.

    - `listHeaderStyle`: pour mettre en forme les contrôles <xref:System.Windows.Controls.Border> de l’en-tête de liste.

    - `listHeaderTextStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Label>.

    - `buttonStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Button> sur `ExpenseItHome.xaml`.

    Notez que les styles sont des ressources et des enfants de le <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> élément de propriété. À cet emplacement, les styles sont appliqués à tous les éléments d’une application. Pour obtenir un exemple d’utilisation des ressources dans une application .NET Framework, consultez [utiliser les ressources Application](../../../../docs/framework/wpf/advanced/how-to-use-application-resources.md).

3. Ouvrez *`ExpenseItHome.xaml`*.

4. Remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :

    [!code-xaml[ExpenseIt#19](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseItHome.xaml#19)]

    Les propriétés qui définissent l’apparence de chaque contrôle, comme <xref:System.Windows.VerticalAlignment> et <xref:System.Windows.Media.FontFamily> , sont supprimées et remplacées lors de l’application de styles. Par exemple, le `headerTextStyle` est appliqué à la « View Expense Report » <xref:System.Windows.Controls.Label>.

5. Ouvrez *ExpenseReportPage.xaml*.

6. Remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :

    [!code-xaml[ExpenseIt#20](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseReportPage.xaml#20)]

    Des styles sont ajoutés aux éléments <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Border> .

## <a name="bind-data-to-a-control"></a>Lier des données à un contrôle

Dans cette section, vous allez créer les données XML qui sont liées à différents contrôles.

1. Ouvrez *`ExpenseItHome.xaml`*.

2. Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez le XAML suivant pour créer un <xref:System.Windows.Data.XmlDataProvider> qui contient les données pour chaque personne :

    [!code-xaml[ExpenseIt#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#21)]
    [!code-xaml[ExpenseIt#23](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#23)]
    [!code-xaml[ExpenseIt#22](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#22)]

    Les données sont créées en tant qu’un <xref:System.Windows.Controls.Grid> ressource. Les données sont normalement chargées en tant que fichier, mais pour des raisons pratiques, elles sont ajoutées inline.

3. Dans le `<Grid.Resources>` élément, ajoutez le code suivant <xref:System.Windows.DataTemplate>, qui définit comment afficher les données dans le <xref:System.Windows.Controls.ListBox>:

    [!code-xaml[ExpenseIt#21](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#21)]
    [!code-xaml[ExpenseIt#24](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#24)]
    [!code-xaml[ExpenseIt#22](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#22)]

    Pour plus d’informations sur les modèles de données, consultez [vue d’ensemble de création de modèles de données](../../../../docs/framework/wpf/data/data-templating-overview.md).

4. Remplacer la <xref:System.Windows.Controls.ListBox> avec le XAML suivant :

    [!code-xaml[ExpenseIt#25](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#25)]

    Ce XAML lie le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox> à la source de données et applique le modèle de données en tant que le <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.

## <a name="connect-data-to-controls"></a>Connectez des données aux contrôles

Ensuite, vous ajouterez du code pour récupérer le nom qui est sélectionné sur la **`ExpenseItHome`** page et le passer au constructeur de **ExpenseReportPage**. **ExpenseReportPage** définit son contexte de données avec l’élément passé, ce qui est définie par les contrôles dans *ExpenseReportPage.xaml* lier à.

1. Ouvrez *ExpenseReportPage.xaml.vb* ou *ExpenseReportPage.xaml.cs*.

2. Ajoutez un constructeur qui prend un objet de façon à pouvoir transmettre les données de note de frais de la personne sélectionnée.

    [!code-csharp[ExpenseIt#26](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseReportPage.xaml.cs#26)]
    [!code-vb[ExpenseIt#26](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseReportPage.xaml.vb#26)]

3. Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.

4. Modifier le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements pour appeler le nouveau constructeur en passant les données de rapport de frais de la personne sélectionnée.

    [!code-csharp[ExpenseIt#27](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml.cs#27)]
    [!code-vb[ExpenseIt#27](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseItHome.xaml.vb#27)]

## <a name="style-data-with-data-templates"></a>Données de style avec les modèles de données

Dans cette section, vous allez mettre à jour l’interface utilisateur pour chaque élément dans les listes liées aux données à l’aide de modèles de données.

1. Ouvrez *ExpenseReportPage.xaml*.

2. Lier le contenu de la « Name » et « Department » <xref:System.Windows.Controls.Label> éléments pour les données appropriées de propriété source. Pour plus d’informations sur la liaison de données, consultez [vue d’ensemble de liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md).

    [!code-xaml[ExpenseIt#31](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#31)]

3. Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez les modèles de données suivants, qui définissent comment afficher les données de rapport de frais :

    [!code-xaml[ExpenseIt#30](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#30)]

4. Remplacez le <xref:System.Windows.Controls.DataGridTextColumn> éléments avec <xref:System.Windows.Controls.DataGridTemplateColumn> sous le <xref:System.Windows.Controls.DataGrid> élément et appliquer les modèles.

    [!code-xaml[ExpenseIt#32](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#32)]

5. Générez et exécutez l’application.

6. Sélectionnez une personne, puis le **vue** bouton.

L’illustration suivante montre les deux pages de le `ExpenseIt` application avec des contrôles, styles, la disposition, liaison de données et modèles de données appliqués :

![Captures d’écran, exemple ExpenseIt](../../../../docs/framework/wpf/getting-started/media/gettingstartedfigure5.png)

> [!NOTE]
> Cet exemple montre une fonctionnalité spécifique de WPF et ne respecte pas toutes les meilleures pratiques pour les éléments tels que la sécurité, la localisation et d’accessibilité. Pour une couverture complète de WPF et les .NET Framework application meilleures pratiques de développement, consultez les rubriques suivantes :
>
> - [Accessibilité](../../../../docs/framework/ui-automation/accessibility-best-practices.md)
>
> - [Sécurité](../../../../docs/framework/wpf/security-wpf.md)
>
> - [Globalisation et localisation pour WPF](../../../../docs/framework/wpf/advanced/wpf-globalization-and-localization-overview.md)
>
> - [Performances WPF](../../../../docs/framework/wpf/advanced/optimizing-wpf-application-performance.md)

## <a name="next-steps"></a>Étapes suivantes

Dans cette procédure pas à pas, vous avez appris un certain nombre de techniques pour la création d’une interface utilisateur à l’aide de Windows Presentation Foundation (WPF). Vous devez maintenant avoir une compréhension élémentaire des blocs de construction d’une application .NET Framework de liaison de données. Pour plus d’informations sur les modèles d’architecture et de programmation WPF, consultez les rubriques suivantes :

- [Architecture de WPF](../../../../docs/framework/wpf/advanced/wpf-architecture.md)
- [Vue d’ensemble du langage XAML (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
- [Vue d’ensemble des propriétés de dépendance](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md)
- [Disposition](../../../../docs/framework/wpf/advanced/layout.md)

Pour plus d’informations sur la création d’applications, consultez les rubriques suivantes :

- [Développement d’applications](../../../../docs/framework/wpf/app-development/index.md)
- [Contrôles](../../../../docs/framework/wpf/controls/index.md)
- [Vue d’ensemble de la liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [Graphiques et multimédia](../../../../docs/framework/wpf/graphics-multimedia/index.md)
- [Documents dans WPF](../../../../docs/framework/wpf/advanced/documents-in-wpf.md)

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des panneaux](../../../../docs/framework/wpf/controls/panels-overview.md)
- [Vue d’ensemble de création de modèles de données](../../../../docs/framework/wpf/data/data-templating-overview.md)
- [Créer une application WPF](../../../../docs/framework/wpf/app-development/building-a-wpf-application-wpf.md)
- [Styles et modèles](../../../../docs/framework/wpf/controls/styles-and-templates.md)
