---
title: Créer une application WPF dans Visual Studio
ms.date: 03/20/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- getting started [WPF], WPF
- WPF [WPF], getting started
ms.assetid: b96bed40-8946-4285-8fe4-88045ab854ed
author: mairaw
ms.author: mairaw
ms.custom: vs-dotnet
ms.openlocfilehash: 9d0abd18b2242ab21e8a915caac1ff9e3216acd0
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64617275"
---
# <a name="walkthrough-my-first-wpf-desktop-application"></a>Procédure pas à pas : Ma première application de bureau WPF

Cet article vous explique comment développer une application de bureau Windows Presentation Foundation (WPF) qui inclut les éléments qui sont communes à la plupart des applications WPF : Extensible Application Markup Language (XAML) balisage, code-behind, définitions d’application, contrôles, disposition, liaison de données et styles. Pour développer l’application, vous allez utiliser Visual Studio. 

Cette procédure pas à pas comprend les étapes suivantes :

- XAML permet de concevoir l’apparence de l’interface utilisateur de l’application (IU).

- Écrire du code pour générer le comportement de l’application.

- Créer une définition d’application pour gérer l’application.

- Ajouter des contrôles et créer la disposition pour composer l’interface utilisateur de l’application.

- Créer des styles pour une apparence cohérente tout au long de l’interface utilisateur de l’application.

- Lier l’interface utilisateur à des données, pour remplir l’interface utilisateur à partir des données et de conserver les données et l’interface utilisateur synchronisé.

À la fin de la procédure pas à pas, vous aurez créé une application Windows qui permet aux utilisateurs d’afficher les notes de frais pour certaines personnes autonome. L’application est composée de plusieurs pages WPF sont hébergées dans une fenêtre de style navigateur.

> [!TIP]
> L’exemple de code qui est utilisé pour générer cette procédure pas à pas est disponible pour les deux Visual Basic et C# à [Code d’exemple de procédure pas à pas WPF application](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/WalkthroughFirstWPFApp).
>
> Vous pouvez activer/désactiver le langage de code de l’exemple de code entre C# et Visual Basic à l’aide de la **\< />** déroulante sur le coin supérieur droit de cet article.

## <a name="prerequisites"></a>Prérequis

- Visual Studio 2017 ou version ultérieure

   Pour plus d’informations sur l’installation de la dernière version de Visual Studio, consultez [installer Visual Studio](/visualstudio/install/install-visual-studio). Cet article utilise Visual Studio 2019.

## <a name="create-the-application-project"></a>Créer le projet d’application

La première étape consiste à créer l’infrastructure d’application, qui inclut une définition d’application, deux pages et une image.

1. Créer un nouveau projet d’Application WPF en Visual Basic ou Visual c# nommé **`ExpenseIt`**:

   1. Ouvrez Visual Studio et sélectionnez **fichier** > **New** > **projet**.

      Le **créer un nouveau projet** boîte de dialogue s’ouvre.

      ![Créer une boîte de dialogue Nouveau projet](./media/gettingstartedfigure0a.png)

   2. Dans le **langage** liste déroulante, sélectionnez **C#** ou **Visual Basic**.

   3. Sélectionnez le **application WPF (.NET Framework)** modèle, puis sélectionnez **suivant**. 
    
   4. Sélectionnez **créer un nouveau projet**.

      Le **configurer un nouveau projet** boîte de dialogue s’ouvre.

      ![Configurer une boîte de dialogue Nouveau projet](./media/gettingstartedfigure0c.png)

   5. Entrez le nom du projet **`ExpenseIt`** , puis sélectionnez **créer**.

      Visual Studio crée le projet et ouvre le concepteur pour la fenêtre d’application par défaut nommé **MainWindow.xaml**.

2. Ouvrez *Application.xaml* (Visual Basic) ou *App.xaml* (c#).

    Ce fichier XAML définit une application WPF et les ressources de l’application. Vous utilisez également ce fichier pour spécifier l’interface utilisateur, dans ce cas *MainWindow.xaml*, qui s’affiche automatiquement lorsque l’application démarre.

    Votre XAML doit ressembler à ce qui suit dans Visual Basic :

    [!code-xaml[ExpenseIt#1_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/Application.xaml#1_a)]

    Et comme le suivant dans C#:

    [!code-xaml[ExpenseIt#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/App.xaml#1)]

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

   Cette application accède à un contenu différent en fonction de l’entrée utilisateur. C’est pourquoi les principaux <xref:System.Windows.Window> doit être changé en un <xref:System.Windows.Navigation.NavigationWindow>. <xref:System.Windows.Navigation.NavigationWindow> hérite de toutes les propriétés de <xref:System.Windows.Window>. Le <xref:System.Windows.Navigation.NavigationWindow> élément dans le fichier XAML crée une instance de la <xref:System.Windows.Navigation.NavigationWindow> classe. Pour plus d’informations, consultez [vue d’ensemble de la Navigation](../app-development/navigation-overview.md).

5. Supprimer le <xref:System.Windows.Controls.Grid> éléments entre le <xref:System.Windows.Navigation.NavigationWindow> balises.

6. Modifiez les propriétés suivantes dans le code XAML pour le <xref:System.Windows.Navigation.NavigationWindow> élément :

    - Définir le <xref:System.Windows.Window.Title%2A> propriété à «`ExpenseIt`».

    - Définir le <xref:System.Windows.FrameworkElement.Height%2A> propriété sur 350 pixels.

    - Définir le <xref:System.Windows.FrameworkElement.Width%2A> propriété 500 pixels.

    Votre XAML doit ressembler à ce qui suit pour Visual Basic :

    [!code-xaml[ExpenseIt#2_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt/MainWindow.xaml#2_a)]

    Et comme suit pour C#:

    [!code-xaml[ExpenseIt#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/MainWindow.xaml#2)]

7. Ouvrez *MainWindow.xaml.vb* ou *MainWindow.xaml.cs*.

    Ce fichier est un fichier code-behind qui contient le code pour gérer les événements déclarés dans *MainWindow.xaml*. Ce fichier contient une classe partielle pour la fenêtre définie en XAML.

8. Si vous utilisez C#, modifiez le `MainWindow` classe à dériver de <xref:System.Windows.Navigation.NavigationWindow>. (En Visual Basic, cela se produit automatiquement lorsque vous modifiez la fenêtre en XAML.) Votre C# code doit maintenant ressembler à ceci :

   [!code-csharp[ExpenseIt#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/MainWindow.xaml.cs?highlight=21)]

## <a name="add-files-to-the-application"></a>Ajouter des fichiers à l’application

Dans cette section, vous allez ajouter deux pages et une image à l’application.

1. Ajoutez une nouvelle page au projet et nommez-le *`ExpenseItHome.xaml`*:

   1. Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.

   1. Dans le **ajouter un nouvel élément** boîte de dialogue, le **Page (WPF)** modèle est déjà sélectionné. Entrez le nom **`ExpenseItHome`**, puis sélectionnez **ajouter**.

    Cette page est la première page qui s’affiche lorsque l’application est lancée. Il affiche une liste de personnes, pour afficher une note de frais.

1. Ouvrez *`ExpenseItHome.xaml`*.

1. Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - Home`».

1. Définir le `DesignHeight` et `DesignWidth` valeurs d’élément de 300 pixels.

    Le XAML apparaît maintenant comme suit pour Visual Basic :

    [!code-xaml[ExpenseIt#6_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml#6_a)]

    Et comme suit pour C#:

    [!code-xaml[ExpenseIt#6](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml#6)]

1. Ouvrez *MainWindow.xaml*.

1. Ajouter un <xref:System.Windows.Navigation.NavigationWindow.Source%2A> propriété le <xref:System.Windows.Navigation.NavigationWindow> élément et affectez-lui la valeur «`ExpenseItHome.xaml`».

    Cela définit *`ExpenseItHome.xaml`* être la première page ouverte au démarrage de l’application. 

    Exemple XAML dans Visual Basic :

    [!code-xaml[ExpenseIt#7_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/MainWindow.xaml#7_a)]

    Et en C# :

    [!code-xaml[ExpenseIt#7](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/MainWindow.xaml#7)]

   > [!TIP]
   > Vous pouvez également définir le **Source** propriété dans le **divers** catégorie de la **propriétés** fenêtre.
   >
   > ![Propriété de source dans la fenêtre Propriétés](./media/properties-source.png)

1. Ajoutez une autre nouvelle page WPF au projet et nommez-le *ExpenseReportPage.xaml*::

   1. Dans **l’Explorateur de solutions**, avec le bouton droit sur le **`ExpenseIt`** nœud de projet et choisissez **ajouter** > **Page**.

   1. Dans le **ajouter un nouvel élément** boîte de dialogue, sélectionnez le **Page (WPF)** modèle. Entrez le nom **ExpenseReportPage**, puis sélectionnez **ajouter**.

    Cette page affiche la note de frais pour la personne sélectionnée sur le **`ExpenseItHome`** page.

1. Ouvrez *ExpenseReportPage.xaml*.

1. Définir le <xref:System.Windows.Controls.Page.Title%2A> à «`ExpenseIt - View Expense`».

1. Définir le `DesignHeight` et `DesignWidth` valeurs d’élément de 300 pixels.

    *ExpenseReportPage.xaml* se présente maintenant comme suit dans Visual Basic :

    [!code-xaml[ExpenseIt#4_A](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml#4_a)]

    Et comme le suivant dans C#:

    [!code-xaml[ExpenseIt#4](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml#4)]

1. Ouvrez *ExpenseItHome.xaml.vb* et *ExpenseReportPage.xaml.vb*, ou *ExpenseItHome.xaml.cs* et *ExpenseReportPage.xaml.cs*.

    Lorsque vous créez un nouveau fichier de Page, Visual Studio crée automatiquement ses *code-behind* fichier. Ces fichiers code-behind gèrent la logique pour répondre à une saisie de l’utilisateur.

    Votre code doit ressembler à ce qui suit pour **`ExpenseItHome`**:

    [!code-csharp[ExpenseIt#2_5](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt2/ExpenseItHome.xaml.cs#2_5)]

    [!code-vb[ExpenseIt#2_5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseItHome.xaml.vb#2_5)]

    Et comme suit pour **ExpenseReportPage**:

    [!code-csharp[ExpenseIt#5](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt/ExpenseReportPage.xaml.cs#5)]

    [!code-vb[ExpenseIt#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt1_A/ExpenseReportPage.xaml.vb#5)]

1. Ajouter une image nommée *watermark.png* au projet. Vous pouvez créer votre propre image, copiez le fichier à partir de l’exemple de code ou obtenez-le [ici](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/WalkthroughFirstWPFApp).

    1. Avec le bouton droit sur le nœud du projet et sélectionnez **ajouter** > **élément existant**, ou appuyez sur **MAJ**+**Alt** + **A**.

    2. Dans le **ajouter un élément existant** boîte de dialogue, définissez le filtre de fichier soit **tous les fichiers** ou **fichiers Image**, accédez au fichier image que vous souhaitez utiliser, puis sélectionnez **ajouter** .

## <a name="build-and-run-the-application"></a>Générez et exécutez l'application.

1. Pour générer et exécuter l’application, appuyez sur **F5** ou sélectionnez **démarrer le débogage** à partir de la **déboguer** menu.

    L’illustration suivante montre l’application avec le <xref:System.Windows.Navigation.NavigationWindow> boutons :

    ![Capture d’écran : exemple ExpenseIt](./media/gettingstartedfigure1.png)

2. Fermez l’application pour revenir à Visual Studio.

## <a name="create-the-layout"></a>Créer la disposition

Mise en page offre un moyen ordonné de placer des éléments d’interface utilisateur et gère également la taille et la position de ces éléments lors du redimensionnée d’une interface utilisateur. En règle générale, vous allez créer une disposition avec l’un des contrôles de disposition suivants :

- <xref:System.Windows.Controls.Canvas> -Définit une zone dans laquelle vous pouvez explicitement positionner des éléments enfants à l’aide des coordonnées relatives à la zone du canevas.
- <xref:System.Windows.Controls.DockPanel> -Définit une zone où vous pouvez organiser les éléments enfants horizontalement ou verticalement, par rapport aux autres.
- <xref:System.Windows.Controls.Grid> -Définit une grille flexible composée de colonnes et de lignes.
- <xref:System.Windows.Controls.StackPanel> -Organise les éléments enfants sur une seule ligne qui peut être orientée horizontalement ou verticalement.
- <xref:System.Windows.Controls.VirtualizingStackPanel> -Organise et virtualise un contenu sur une seule ligne est orienté horizontalement ou verticalement.
- <xref:System.Windows.Controls.WrapPanel> -Éléments enfants de positions dans un ordre séquentiel de gauche à droite, en faisant passer le contenu à la ligne suivante à la périphérie de la zone conteneur. Classement continue ensuite séquentiellement de haut en bas ou de droite à gauche, selon la valeur de la propriété Orientation.

Chacun de ces contrôles de disposition prend en charge un type particulier de disposition pour ses éléments enfants. `ExpenseIt` pages peuvent être redimensionnés, et chaque page comporte des éléments organisés horizontalement et verticalement en même temps que d’autres éléments. Dans cet exemple, le <xref:System.Windows.Controls.Grid> est utilisé comme élément de disposition de l’application.

> [!TIP]
> Pour plus d’informations sur <xref:System.Windows.Controls.Panel> éléments, consultez [vue d’ensemble de panneaux](../controls/panels-overview.md). Pour plus d’informations sur la disposition, consultez [disposition](../advanced/layout.md).

Dans cette section, vous créez une seule colonne de table avec trois lignes et une marge de 10 pixels en ajoutant des définitions de colonne et de ligne à la <xref:System.Windows.Controls.Grid> dans *`ExpenseItHome.xaml`*.

1. Dans *`ExpenseItHome.xaml`*, définissez le <xref:System.Windows.FrameworkElement.Margin%2A> propriété sur le <xref:System.Windows.Controls.Grid> élément valeur « 10,0,10,10 » qui correspond aux marges gauche, haut, droite et bas :

   ```xaml
   <Grid Margin="10,0,10,10">
   ```

   > [!TIP]
   > Vous pouvez également définir le **marge** des valeurs dans le **propriétés** fenêtre, sous le **disposition** catégorie :
   >
   > ![Valeurs de marge dans la fenêtre Propriétés](./media/properties-margin.png)

2. Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises pour créer les définitions de ligne et de colonne :

    [!code-xaml[ExpenseIt#8](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#8)]

    Le <xref:System.Windows.Controls.RowDefinition.Height%2A> de deux lignes est définie sur <xref:System.Windows.GridLength.Auto%2A>, ce qui signifie que les lignes sont dimensionnés en fonction du contenu dans les lignes. La valeur par défaut <xref:System.Windows.Controls.RowDefinition.Height%2A> est <xref:System.Windows.GridUnitType.Star> dimensionnement, ce qui signifie que la hauteur de ligne est une proportion pondérée de l’espace disponible. Par exemple, si deux lignes ont une <xref:System.Windows.Controls.RowDefinition.Height%2A> de « * », ils ont chacun une hauteur qui représente la moitié de l’espace disponible.

    Votre <xref:System.Windows.Controls.Grid> doit maintenant contenir le XAML suivant :

    [!code-xaml[ExpenseIt#9](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt3/ExpenseItHome.xaml#9)]

## <a name="add-controls"></a>Ajouter des contrôles

Dans cette section, vous allez mettre à jour l’interface utilisateur pour afficher une liste de personnes, où vous sélectionnez une personne pour afficher l’état de leurs dépenses de la page d’accueil. Les contrôles sont des objets d’interface utilisateur qui permettent aux utilisateurs d’interagir avec votre application. Pour plus d’informations, consultez [Contrôles](../controls/index.md).

Pour créer cette interface utilisateur, vous allez ajouter les éléments suivants à *`ExpenseItHome.xaml`*:

- Un <xref:System.Windows.Controls.ListBox> (pour la liste de personnes).
- Un <xref:System.Windows.Controls.Label> (pour l’en-tête de liste).
- Un <xref:System.Windows.Controls.Button> (sur lequel cliquer pour afficher la note de frais pour la personne qui est sélectionnée dans la liste).

Chaque contrôle est placé dans une ligne de la <xref:System.Windows.Controls.Grid> en définissant le <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> propriété jointe. Pour plus d’informations sur les propriétés jointes, consultez [vue d’ensemble des propriétés jointes](../advanced/attached-properties-overview.md).

1. Dans *`ExpenseItHome.xaml`*, ajoutez le XAML suivant quelque part entre le <xref:System.Windows.Controls.Grid> balises :

   [!code-xaml[ExpenseIt#10](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt4/ExpenseItHome.xaml#10)]

   > [!TIP]
   > Vous pouvez également créer les contrôles en les faisant glisser à partir de la **boîte à outils** fenêtre sur la fenêtre de conception, puis en définissant leurs propriétés le **propriétés** fenêtre.

2. Générez et exécutez l’application.

    L’illustration suivante montre les contrôles que vous avez créé :

    ![Capture d’écran : exemple ExpenseIt](./media/gettingstartedfigure2.png)

3. Fermez l’application pour revenir à Visual Studio.

## <a name="add-an-image-and-a-title"></a>Ajouter une image et un titre

Dans cette section, vous allez mettre à jour l’interface utilisateur de la page d’accueil avec une image et un titre de page.

1. Dans *`ExpenseItHome.xaml`*, ajoutez une autre colonne à la <xref:System.Windows.Controls.Grid.ColumnDefinitions%2A> fixe <xref:System.Windows.Controls.ColumnDefinition.Width%2A> de 230 pixels :

    [!code-xaml[ExpenseIt#11](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseItHome.xaml?highlight=52-55)]

2. Ajouter une autre ligne à la <xref:System.Windows.Controls.Grid.RowDefinitions%2A>, pour un total de quatre lignes :

    [!code-xaml[ExpenseIt#11b](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseItHome.xaml?highlight=57-62)]

3. Déplacer les contrôles vers la deuxième colonne en définissant le <xref:System.Windows.Controls.Grid.Column%2A?displayProperty=nameWithType> propriété sur 1 dans chacun des trois contrôles (bordure, ListBox et bouton).

4. Déplacez chaque contrôle d’une ligne vers le bas en incrémentant son <xref:System.Windows.Controls.Grid.Row%2A?displayProperty=nameWithType> valeur de 1 pour chacun des trois contrôles (bordure, ListBox et bouton) et pour l’élément Border.

   Le XAML pour les trois contrôles se présente désormais comme suit :

    [!code-xaml[ExpenseIt#12](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#12)]

5. Définir le <xref:System.Windows.Controls.Panel.Background%2A?displayProperty=nameWithType> propriété le *watermark.png* fichier image, en ajoutant le XAML suivant n’importe où entre le `<Grid>` et `</Grid>` balises :

    [!code-xaml[ExpenseIt#14](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#14)]

6. Avant du <xref:System.Windows.Controls.Border> élément, ajoutez un <xref:System.Windows.Controls.Label> avec le contenu « View Expense Report ». Cette étiquette est le titre de la page.

    [!code-xaml[ExpenseIt#13](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt5/ExpenseItHome.xaml#13)]

7. Générez et exécutez l’application.

L’illustration suivante montre les résultats de ce que vous venez d’ajouter :

![Capture d’écran : exemple ExpenseIt](./media/gettingstartedfigure3.png)

## <a name="add-code-to-handle-events"></a>Ajoutez du code pour gérer les événements

1. Dans *`ExpenseItHome.xaml`*, ajoutez un <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements à la <xref:System.Windows.Controls.Button> élément. Pour plus d'informations, voir [Procédure : Créez un gestionnaire d’événements simple](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb675300(v=vs.100)).

    [!code-xaml[ExpenseIt#15](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml#15)]

2. Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.

3. Ajoutez le code suivant à la `ExpenseItHome` classe pour ajouter un bouton Gestionnaire d’événements click. Le Gestionnaire d’événements ouvre le **ExpenseReportPage** page.

    [!code-csharp[ExpenseIt#16](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseItHome.xaml.cs#16)]
    [!code-vb[ExpenseIt#16](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt6/ExpenseItHome.xaml.vb#16)]

## <a name="create-the-ui-for-expensereportpage"></a>Créer l’interface utilisateur pour ExpenseReportPage

*ExpenseReportPage.xaml* affiche la note de frais de la personne qui est sélectionnée sur la **`ExpenseItHome`** page. Dans cette section, vous allez créer l’interface utilisateur pour **ExpenseReportPage**. Vous également ajouter d’arrière-plan et les couleurs aux divers éléments d’interface utilisateur de remplissage.

1. Ouvrez *ExpenseReportPage.xaml*.

2. Ajoutez le XAML suivant entre les <xref:System.Windows.Controls.Grid> balises :

    [!code-xaml[ExpenseIt#17](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt6/ExpenseReportPage.xaml#17)]

    Cette interface utilisateur est similaire à *`ExpenseItHome.xaml`*, sauf que les données du rapport s’affiche dans un <xref:System.Windows.Controls.DataGrid>.

3. Générez et exécutez l’application.

4. Sélectionnez le **vue** bouton.

    La page de note de frais s’affiche. Notez également que le bouton de navigation arrière est activé.

L’illustration suivante montre les éléments d’interface utilisateur ajoutés à *ExpenseReportPage.xaml*.

![Capture d’écran : exemple ExpenseIt](./media/gettingstartedfigure4.png)

## <a name="style-controls"></a>Style aux contrôles

L’apparence des différents éléments est souvent le même pour tous les éléments du même type dans une interface utilisateur. Utilise l’interface utilisateur [styles](../controls/styling-and-templating.md) pour pouvoir réutiliser l’apparence des différents éléments. La réutilisation des styles permet de simplifier la gestion et la création de XAML. Cette section remplace par des styles les attributs d’élément qui ont été définis lors des étapes précédentes.

1. Ouvrez *Application.xaml* ou *App.xaml*.

2. Ajoutez le XAML suivant entre les <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> balises :

    [!code-xaml[ExpenseIt#18](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/App.xaml#18)]

    Ce code XAML ajoute les styles suivants :

    - `headerTextStyle`: Pour mettre en forme le titre de la page <xref:System.Windows.Controls.Label>.

    - `labelStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Label> contrôles.

    - `columnHeaderStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Primitives.DataGridColumnHeader>.

    - `listHeaderStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Border> contrôles.

    - `listHeaderTextStyle`: Pour mettre en forme l’en-tête de liste <xref:System.Windows.Controls.Label>.

    - `buttonStyle`: Pour mettre en forme le <xref:System.Windows.Controls.Button> sur `ExpenseItHome.xaml`.

    Notez que les styles sont des ressources et des enfants de le <xref:System.Windows.Application.Resources%2A?displayProperty=nameWithType> élément de propriété. À cet emplacement, les styles sont appliqués à tous les éléments d’une application. Pour obtenir un exemple d’utilisation des ressources dans une application .NET, consultez [utiliser les ressources Application](../advanced/how-to-use-application-resources.md).

3. Dans *`ExpenseItHome.xaml`*, remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :

    [!code-xaml[ExpenseIt#19](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseItHome.xaml#19)]

    Les propriétés qui définissent l’apparence de chaque contrôle, comme <xref:System.Windows.VerticalAlignment> et <xref:System.Windows.Media.FontFamily> , sont supprimées et remplacées lors de l’application de styles. Par exemple, le `headerTextStyle` est appliqué à la « View Expense Report » <xref:System.Windows.Controls.Label>.

4. Ouvrez *ExpenseReportPage.xaml*.

5. Remplacez tout le contenu entre le <xref:System.Windows.Controls.Grid> éléments avec le XAML suivant :

    [!code-xaml[ExpenseIt#20](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt7/ExpenseReportPage.xaml#20)]

    Ce XAML ajoute les styles pour le <xref:System.Windows.Controls.Label> et <xref:System.Windows.Controls.Border> éléments.

6. Générez et exécutez l’application. L’apparence de la fenêtre est le même que précédemment.

    ![Capture d’écran : exemple ExpenseIt](./media/gettingstartedfigure4.png)

7. Fermez l’application pour revenir à Visual Studio.

## <a name="bind-data-to-a-control"></a>Lier des données à un contrôle

Dans cette section, vous allez créer les données XML qui sont liées à différents contrôles.

1. Dans *`ExpenseItHome.xaml`*, après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez le XAML suivant pour créer un <xref:System.Windows.Data.XmlDataProvider> qui contient les données pour chaque personne :

    [!code-xaml[ExpenseIt#23](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml?range=13,16-40,49)]

    Les données sont créées en tant qu’un <xref:System.Windows.Controls.Grid> ressource. Normalement, ces données seraient chargées en tant que fichier, mais par souci de simplicité, les données sont ajoutées inline.

2. Dans le `<Grid.Resources>` élément, ajoutez le code suivant `<xref:System.Windows.DataTemplate>` élément, qui définit comment afficher les données dans le <xref:System.Windows.Controls.ListBox>, après le `<XmlDataProvider>` élément :

    [!code-xaml[ExpenseIt#24](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml?range=13,43-46,49)]

    Pour plus d’informations sur les modèles de données, consultez [vue d’ensemble de création de modèles de données](../data/data-templating-overview.md).

3. Remplacer la <xref:System.Windows.Controls.ListBox> avec le XAML suivant :

    [!code-xaml[ExpenseIt#25](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml#25)]

    Ce XAML lie le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox> à la source de données et applique le modèle de données en tant que le <xref:System.Windows.Controls.ItemsControl.ItemTemplate%2A>.

## <a name="connect-data-to-controls"></a>Connectez des données aux contrôles

Ensuite, vous ajouterez du code pour récupérer le nom qui est sélectionné sur la **`ExpenseItHome`** page et le passer au constructeur de **ExpenseReportPage**. **ExpenseReportPage** définit son contexte de données avec l’élément passé, ce qui est définie par les contrôles dans *ExpenseReportPage.xaml* lier à.

1. Ouvrez *ExpenseReportPage.xaml.vb* ou *ExpenseReportPage.xaml.cs*.

2. Ajoutez un constructeur qui prend un objet de façon à pouvoir transmettre les données de note de frais de la personne sélectionnée.

    [!code-csharp[ExpenseIt#26](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseReportPage.xaml.cs#26)]
    [!code-vb[ExpenseIt#26](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseReportPage.xaml.vb#26)]

3. Ouvrez *`ExpenseItHome.xaml.vb`* ou *`ExpenseItHome.xaml.cs`*.

4. Modifier le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Gestionnaire d’événements pour appeler le nouveau constructeur en passant les données de rapport de frais de la personne sélectionnée.

    [!code-csharp[ExpenseIt#27](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt8/ExpenseItHome.xaml.cs#27)]
    [!code-vb[ExpenseIt#27](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpenseIt/VB/ExpenseIt8/ExpenseItHome.xaml.vb#27)]

## <a name="style-data-with-data-templates"></a>Données de style avec les modèles de données

Dans cette section, vous allez mettre à jour l’interface utilisateur pour chaque élément dans les listes liées aux données à l’aide de modèles de données.

1. Ouvrez *ExpenseReportPage.xaml*.

2. Lier le contenu de la « Name » et « Department » <xref:System.Windows.Controls.Label> éléments pour les données appropriées de propriété source. Pour plus d’informations sur la liaison de données, consultez [vue d’ensemble de liaison de données](../data/data-binding-overview.md).

    [!code-xaml[ExpenseIt#31](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#31)]

3. Après l’ouverture <xref:System.Windows.Controls.Grid> élément, ajoutez les modèles de données suivants, qui définissent comment afficher les données de rapport de frais :

    [!code-xaml[ExpenseIt#30](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#30)]

4. Remplacez le <xref:System.Windows.Controls.DataGridTextColumn> éléments avec <xref:System.Windows.Controls.DataGridTemplateColumn> sous le <xref:System.Windows.Controls.DataGrid> élément et appliquer les modèles.

    [!code-xaml[ExpenseIt#32](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpenseIt/CSharp/ExpenseIt9/ExpenseReportPage.xaml#32)]

5. Générez et exécutez l’application.

6. Sélectionnez une personne, puis le **vue** bouton.

L’illustration suivante montre les deux pages de le `ExpenseIt` application avec des contrôles, styles, la disposition, liaison de données et modèles de données appliqués :

![Captures d'écran : exemple ExpenseIt](./media/gettingstartedfigure5.png)

> [!NOTE]
> Cet exemple montre une fonctionnalité spécifique de WPF et ne respecte pas toutes les meilleures pratiques pour les éléments tels que la sécurité, la localisation et d’accessibilité. Pour une couverture complète de WPF et les .NET application meilleures pratiques de développement, consultez les rubriques suivantes :
>
> - [Accessibilité](../../ui-automation/accessibility-best-practices.md)
>
> - [Sécurité](../security-wpf.md)
>
> - [Globalisation et localisation pour WPF](../advanced/wpf-globalization-and-localization-overview.md)
>
> - [Performances WPF](../advanced/optimizing-wpf-application-performance.md)

## <a name="next-steps"></a>Étapes suivantes

Dans cette procédure pas à pas, vous avez appris un certain nombre de techniques pour la création d’une interface utilisateur à l’aide de Windows Presentation Foundation (WPF). Vous devez maintenant avoir une compréhension élémentaire des blocs de construction d’une application de .NET lié aux données. Pour plus d’informations sur les modèles d’architecture et de programmation WPF, consultez les rubriques suivantes :

- [Architecture de WPF](../advanced/wpf-architecture.md)
- [Vue d’ensemble du langage XAML (WPF)](../advanced/xaml-overview-wpf.md)
- [Vue d’ensemble des propriétés de dépendance](../advanced/dependency-properties-overview.md)
- [Disposition](../advanced/layout.md)

Pour plus d’informations sur la création d’applications, consultez les rubriques suivantes :

- [Développement d’applications](../app-development/index.md)
- [Contrôles](../controls/index.md)
- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Graphiques et multimédia](../graphics-multimedia/index.md)
- [Documents dans WPF](../advanced/documents-in-wpf.md)

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des panneaux](../controls/panels-overview.md)
- [Vue d’ensemble de création de modèles de données](../data/data-templating-overview.md)
- [Créer une application WPF](../app-development/building-a-wpf-application-wpf.md)
- [Styles et modèles](../controls/styles-and-templates.md)
