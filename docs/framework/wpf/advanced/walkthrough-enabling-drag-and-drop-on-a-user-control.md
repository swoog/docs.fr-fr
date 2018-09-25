---
title: 'Procédure pas à pas : activation de la fonction glisser-déplacer sur un contrôle utilisateur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- walkthrough [WPF], drag-and-drop
- drag-and-drop [WPF], walkthrough
ms.assetid: cc844419-1a77-4906-95d9-060d79107fc7
ms.openlocfilehash: 7ca4987da8422c00e3fc34ff4605ddd13e4091b6
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47087643"
---
# <a name="walkthrough-enabling-drag-and-drop-on-a-user-control"></a>Procédure pas à pas : activation de la fonction glisser-déplacer sur un contrôle utilisateur

Cette procédure pas à pas montre comment créer un contrôle utilisateur personnalisé qui peut participer à un transfert de données par glisser-déplacer dans [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].

Dans cette procédure pas à pas, vous allez créer un WPF personnalisé <xref:System.Windows.Controls.UserControl> qui représente une forme de cercle. Vous implémentez la fonctionnalité sur le contrôle pour activer le transfert de données par glisser-déplacer. Par exemple, si vous faites glisser un contrôle de cercle sur un autre, les données de couleur de remplissage sont copiées du cercle source vers la cible. Si vous faites glisser un contrôle de cercle pour un <xref:System.Windows.Controls.TextBox>, la représentation sous forme de chaîne de la couleur de remplissage est copiée dans le <xref:System.Windows.Controls.TextBox>. Vous allez également créer une petite application qui contient deux contrôles de panneau et un <xref:System.Windows.Controls.TextBox> pour tester la fonctionnalité de glisser-déplacer. Vous écrivez du code qui permet aux panneaux de traiter les données de cercle déplacées, ce qui vous permet de déplacer ou copier des cercles de la collection d’enfants d’un panneau à l’autre.

Cette procédure pas à pas décrit les tâches suivantes :

-   Créer un contrôle utilisateur personnalisé.

-   Permettre au contrôle utilisateur d’être une source de glissement.

-   Permettre au contrôle utilisateur d’être une cible de déplacement.

-   Permettre à un panneau de recevoir des données déplacées à partir du contrôle utilisateur.

## <a name="prerequisites"></a>Prérequis

Vous avez besoin de Visual Studio pour effectuer cette procédure pas à pas.

## <a name="create-the-application-project"></a>Créer le projet d’Application
 Dans cette section, vous allez créer l’infrastructure d’application, qui inclut une page principale avec deux panneaux et un <xref:System.Windows.Controls.TextBox>.

1.  Créez un projet d’application WPF en Visual Basic ou Visual C# nommé `DragDropExample`. Pour plus d'informations, consultez [Guide pratique pour créer un projet d'application WPF](https://msdn.microsoft.com/library/1f6aea7a-33e1-4d3f-8555-1daa42e95d82).

2.  Ouvrez MainWindow.xaml.

3.  Ajoutez le balisage suivant entre les balises <xref:System.Windows.Controls.Grid> balises.

     Ce balisage crée l’interface utilisateur pour l’application de test.

     [!code-xaml[DragDropWalkthrough#PanelsStep1XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/SnippetWindow.xaml#panelsstep1xaml)]

## <a name="add-a-new-user-control-to-the-project"></a>Ajouter un nouveau contrôle utilisateur au projet
 Dans cette section, vous ajoutez un nouveau contrôle utilisateur au projet.

1.  Dans le menu Projet, sélectionnez **Ajouter un contrôle utilisateur**.

2.  Dans le **ajouter un nouvel élément** boîte de dialogue zone, remplacez le nom par `Circle.xaml`, puis cliquez sur **ajouter**.

     Circle.XAML et son code-behind sont ajoutés au projet.

3.  Ouvrez Circle.xaml.

     Ce fichier doit contenir les éléments d’interface utilisateur du contrôle utilisateur.

4.  Ajoutez le balisage suivant à la racine <xref:System.Windows.Controls.Grid> pour créer un contrôle utilisateur simple qui est un cercle bleu comme interface utilisateur.

     [!code-xaml[DragDropWalkthrough#EllipseXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml#ellipsexaml)]

5.  Ouvrez Circle.xaml.cs ou Circle.xaml.vb.

6.  En C#, ajoutez le code suivant après le constructeur par défaut pour créer un constructeur de copie. En Visual Basic, ajoutez le code suivant pour créer un constructeur par défaut et un constructeur de copie.

     Pour que le contrôle utilisateur puisse être copié, vous ajoutez une méthode de constructeur de copie dans le fichier code-behind. Dans le contrôle utilisateur de cercle simplifié, vous copiez uniquement les valeurs de remplissage et de taille du contrôle utilisateur.

     [!code-csharp[DragDropWalkthrough#CopyCtor](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#copyctor)]
     [!code-vb[DragDropWalkthrough#CopyCtor](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#copyctor)]

## <a name="add-the-user-control-to-the-main-window"></a>Ajoutez le contrôle utilisateur à la fenêtre principale

1.  Ouvrez MainWindow.xaml.

2.  Ajoutez le XAML suivant à l’ouverture <xref:System.Windows.Window> balise pour créer une référence d’espace de noms XML à l’application actuelle.

    ```
    xmlns:local="clr-namespace:DragDropExample"
    ```

3.  Dans la première <xref:System.Windows.Controls.StackPanel>, ajoutez le XAML suivant pour créer deux instances du contrôle de l’utilisateur de cercle dans le premier panneau.

     [!code-xaml[DragDropWalkthrough#CirclesXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/SnippetWindow.xaml#circlesxaml)]

     Le code XAML complet pour le panneau ressemble à ce qui suit.

     [!code-xaml[DragDropWalkthrough#PanelsStep2XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/SnippetWindow.xaml#panelsstep2xaml)]

## <a name="implement-drag-source-events-in-the-user-control"></a>Implémenter des événements de Source de glissement dans le contrôle utilisateur
 Dans cette section, vous allez substituer les <xref:System.Windows.UIElement.OnMouseMove%2A> (méthode) et lance l’opération de glisser-déplacer.

 Si une opération de glissement est démarrée (un bouton de la souris est enfoncé et la souris est déplacée), vous empaqueter les données à transférer dans un <xref:System.Windows.DataObject>. Dans cet exemple, le contrôle de cercle empaquette trois éléments de données : une représentation sous forme de chaîne de sa couleur de remplissage, une double représentation de sa hauteur et une copie de lui-même.

### <a name="to-initiate-a-drag-and-drop-operation"></a>Pour lancer une opération de glisser-déplacer

1.  Ouvrez Circle.xaml.cs ou Circle.xaml.vb.

2.  Ajoutez le code suivant <xref:System.Windows.UIElement.OnMouseMove%2A> override pour fournir la gestion de classe pour le <xref:System.Windows.UIElement.MouseMove> événement.

     [!code-csharp[DragDropWalkthrough#OnMouseMove](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#onmousemove)]
     [!code-vb[DragDropWalkthrough#OnMouseMove](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#onmousemove)]

     Cela <xref:System.Windows.UIElement.OnMouseMove%2A> remplacement effectue les tâches suivantes :

    -   Vérifie si le bouton gauche de la souris est enfoncé quand la souris se déplace.

    -   Empaquette les données de cercle dans un <xref:System.Windows.DataObject>. Dans cet exemple, le contrôle de cercle empaquette trois éléments de données : une représentation sous forme de chaîne de sa couleur de remplissage, une double représentation de sa hauteur et une copie de lui-même.

    -   Appelle la méthode statique <xref:System.Windows.DragDrop.DoDragDrop%2A?displayProperty=nameWithType> méthode pour lancer l’opération de glisser-déplacer. Vous passez les trois paramètres suivants pour le <xref:System.Windows.DragDrop.DoDragDrop%2A> méthode :

        -   `dragSource` : Référence à ce contrôle.

        -   `data` – Les <xref:System.Windows.DataObject> créé dans le code précédent.

        -   `allowedEffects` – Les opérations de glisser-déplacer autorisées qui sont <xref:System.Windows.DragDropEffects.Copy> ou <xref:System.Windows.DragDropEffects.Move>.

3.  Appuyez sur **F5** pour générer et exécuter l’application.

4.  Cliquez sur un des contrôles de cercle et faites-le glisser sur les panneaux, l’autre cercle et le <xref:System.Windows.Controls.TextBox>. Lorsque vous faites glisser sur le <xref:System.Windows.Controls.TextBox>, le curseur se transforme pour indiquer un déplacement.

5.  Tout en faisant glisser un cercle sur le <xref:System.Windows.Controls.TextBox>, appuyez sur la **Ctrl** clé. Notez que le curseur change pour indiquer une copie.

6.  Faites glisser et déposez un cercle sur le <xref:System.Windows.Controls.TextBox>. La représentation sous forme de chaîne de la couleur de remplissage du cercle est ajoutée à la <xref:System.Windows.Controls.TextBox>.

     ![Représentation sous forme de chaîne de la couleur de remplissage du cercle](../../../../docs/framework/wpf/advanced/media/dragdrop-colorstring.png "DragDrop_ColorString")

Par défaut, le curseur change pendant une opération de glisser-déplacer pour indiquer l’effet du déplacement des données. Vous pouvez personnaliser les commentaires donnés à l’utilisateur en gérant la <xref:System.Windows.UIElement.GiveFeedback> événement et en définissant un autre curseur.

## <a name="give-feedback-to-the-user"></a>Envoyer des commentaires à l’utilisateur

1.  Ouvrez Circle.xaml.cs ou Circle.xaml.vb.

2.  Ajoutez le code suivant <xref:System.Windows.UIElement.OnGiveFeedback%2A> override pour fournir la gestion de classe pour le <xref:System.Windows.UIElement.GiveFeedback> événement.

     [!code-csharp[DragDropWalkthrough#OnGiveFeedback](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#ongivefeedback)]
     [!code-vb[DragDropWalkthrough#OnGiveFeedback](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#ongivefeedback)]

     Cela <xref:System.Windows.UIElement.OnGiveFeedback%2A> remplacement effectue les tâches suivantes :

    -   Vérifie la <xref:System.Windows.GiveFeedbackEventArgs.Effects%2A> valeurs qui sont définies dans la cible de dépôt <xref:System.Windows.UIElement.DragOver> Gestionnaire d’événements.

    -   Définit un curseur personnalisé basé sur le <xref:System.Windows.GiveFeedbackEventArgs.Effects%2A> valeur. Le curseur a pour objectif de fournir des commentaires visuels à l’utilisateur sur l’effet du déplacement des données.

3.  Appuyez sur **F5** pour générer et exécuter l’application.

4.  Faites glisser un du cercle le contrôle sur les panneaux, l’autre cercle et le <xref:System.Windows.Controls.TextBox>. Notez que les curseurs sont maintenant les curseurs personnalisés que vous avez spécifié dans le <xref:System.Windows.UIElement.OnGiveFeedback%2A> remplacer.

     ![Glisser-déplacer avec des curseurs personnalisés](../../../../docs/framework/wpf/advanced/media/dragdrop-customcursor.png "DragDrop_CustomCursor")

5.  Sélectionnez le texte `green` à partir de la <xref:System.Windows.Controls.TextBox>.

6.  Faites glisser le texte `green` sur un contrôle de cercle. Notez que les curseurs par défaut sont affichés pour indiquer les effets de l’opération de glisser-déplacer. Le curseur de commentaire est toujours défini par la source de glissement.

## <a name="implement-drop-target-events-in-the-user-control"></a>Implémenter des événements de cible de déplacement dans le contrôle utilisateur
 Dans cette section, vous indiquez que le contrôle utilisateur est une cible de déplacement, vous substituez les méthodes qui permettent au contrôle utilisateur d’être une cible de déplacement et vous traitez les données qui sont déplacées sur celui-ci.

### <a name="to-enable-the-user-control-to-be-a-drop-target"></a>Pour permettre au contrôle utilisateur d’être une cible de déplacement

1.  Ouvrez Circle.xaml.

2.  Dans l’ouverture <xref:System.Windows.Controls.UserControl> , ajoutez le <xref:System.Windows.UIElement.AllowDrop%2A> propriété et affectez-lui la valeur `true`.

     [!code-xaml[DragDropWalkthrough#UCTagXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml#uctagxaml)]

Le <xref:System.Windows.UIElement.OnDrop%2A> méthode est appelée lorsque le <xref:System.Windows.UIElement.AllowDrop%2A> propriété est définie sur `true` et données à partir de la source de glissement sont déplacées sur le contrôle utilisateur de cercle. Dans cette méthode, vous traitez les données qui ont été déplacées et appliquez les données au cercle.

### <a name="to-process-the-dropped-data"></a>Pour traiter les données déplacées

1.  Ouvrez Circle.xaml.cs ou Circle.xaml.vb.

2.  Ajoutez le code suivant <xref:System.Windows.UIElement.OnDrop%2A> override pour fournir la gestion de classe pour le <xref:System.Windows.UIElement.Drop> événement.

     [!code-csharp[DragDropWalkthrough#OnDrop](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#ondrop)]
     [!code-vb[DragDropWalkthrough#OnDrop](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#ondrop)]

     Cela <xref:System.Windows.UIElement.OnDrop%2A> remplacement effectue les tâches suivantes :

    -   Utilise le <xref:System.Windows.DataObject.GetDataPresent%2A> méthode permettant de vérifier si les données glissées contiennent un objet string.

    -   Utilise le <xref:System.Windows.DataObject.GetData%2A> méthode pour extraire les données de chaîne si elle est présente.

    -   Utilise un <xref:System.Windows.Media.BrushConverter> pour essayer de convertir la chaîne à un <xref:System.Windows.Media.Brush>.

    -   Si la conversion réussite, applique le pinceau pour le <xref:System.Windows.Shapes.Shape.Fill%2A> de la <xref:System.Windows.Shapes.Ellipse> qui fournit l’interface utilisateur du contrôle de cercle.

    -   Marque le <xref:System.Windows.UIElement.Drop> événement comme géré. Vous devez marquer l’événement de déplacement comme étant géré pour que les autres éléments qui reçoivent cet événement sachent que le contrôle utilisateur de cercle l’a géré.

3.  Appuyez sur **F5** pour générer et exécuter l’application.

4.  Sélectionnez le texte `green` dans le <xref:System.Windows.Controls.TextBox>.

5.  Faites glisser le texte vers un contrôle de cercle et déplacez-le. Le cercle passe du bleu au vert.

     ![Convertir une chaîne en pinceau](../../../../docs/framework/wpf/advanced/media/dragdrop-dropgreentext.png "DragDrop_DropGreenText")

6.  Tapez le texte `green` dans le <xref:System.Windows.Controls.TextBox>.

7.  Sélectionnez le texte `gre` dans le <xref:System.Windows.Controls.TextBox>.

8.  Faites le glisser vers un contrôle de cercle et déplacez-le. Notez que le curseur change pour indiquer que le déplacement est autorisé, mais la couleur du cercle ne change pas, car `gre` n’est pas une couleur valide.

9. Faites glisser le contrôle de cercle vert et déplacez-le sur le contrôle de cercle bleu. Le cercle passe du bleu au vert. Notez que le curseur affiché varie selon que le <xref:System.Windows.Controls.TextBox> ou le cercle est la source du glissement.

Définition de la <xref:System.Windows.UIElement.AllowDrop%2A> propriété `true` et traitement des données déplacées est tout ce qui est nécessaire pour un élément peut être une cible de dépôt. Toutefois, pour fournir une meilleure expérience utilisateur, vous devez également gérer les <xref:System.Windows.UIElement.DragEnter>, <xref:System.Windows.UIElement.DragLeave>, et <xref:System.Windows.UIElement.DragOver> événements. Dans ces événements, vous pouvez effectuer des vérifications et fournir des commentaires supplémentaires à l’utilisateur avant de déplacer les données.

Quand les données sont glissées sur le contrôle utilisateur de cercle, le contrôle doit notifier la source de glissement si elle peut ou non traiter les données en cours de glissement. Si le contrôle ne sait pas comment traiter les données, il doit refuser le déplacement. Pour ce faire, vous gérerez les <xref:System.Windows.UIElement.DragOver> .PreviewKeyDown et définir le <xref:System.Windows.DragEventArgs.Effects%2A> propriété.

### <a name="to-verify-that-the-data-drop-is-allowed"></a>Pour vérifier que le déplacement de données est autorisé

1.  Ouvrez Circle.xaml.cs ou Circle.xaml.vb.

2.  Ajoutez le code suivant <xref:System.Windows.UIElement.OnDragOver%2A> override pour fournir la gestion de classe pour le <xref:System.Windows.UIElement.DragOver> événement.

     [!code-csharp[DragDropWalkthrough#OnDragOver](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#ondragover)]
     [!code-vb[DragDropWalkthrough#OnDragOver](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#ondragover)]

     Cela <xref:System.Windows.UIElement.OnDragOver%2A> remplacement effectue les tâches suivantes :

    -   Affecte la valeur <xref:System.Windows.DragEventArgs.Effects%2A> à la propriété <xref:System.Windows.DragDropEffects.None>.

    -   Exécute les mêmes vérifications que celles effectuées dans le <xref:System.Windows.UIElement.OnDrop%2A> méthode pour déterminer si le contrôle utilisateur de cercle peut traiter les données glissées.

    -   Si le contrôle utilisateur peut traiter les données, définit les <xref:System.Windows.DragEventArgs.Effects%2A> propriété <xref:System.Windows.DragDropEffects.Copy> ou <xref:System.Windows.DragDropEffects.Move>.

3.  Appuyez sur **F5** pour générer et exécuter l’application.

4.  Sélectionnez le texte `gre` dans le <xref:System.Windows.Controls.TextBox>.

5.  Faites glisser le texte vers un contrôle de cercle. Notez que le curseur change à présent pour indiquer que le déplacement n’est pas autorisé, car `gre` n’est pas une couleur valide.

 Vous pouvez améliorer l’expérience utilisateur en appliquant un aperçu de l’opération de déplacement. Pour le contrôle utilisateur de cercle, vous remplacerez la <xref:System.Windows.UIElement.OnDragEnter%2A> et <xref:System.Windows.UIElement.OnDragLeave%2A> méthodes. Lorsque les données sont glissées sur le contrôle, l’arrière-plan actuel <xref:System.Windows.Shapes.Shape.Fill%2A> est enregistré dans une variable d’espace réservé. La chaîne est ensuite convertie en pinceau et appliquée à la <xref:System.Windows.Shapes.Ellipse> qui fournit le cercle l’interface utilisateur. Si les données sont glissées en dehors du cercle sans être déplacées, la version d’origine <xref:System.Windows.Shapes.Shape.Fill%2A> valeur est réappliquée au cercle.

### <a name="to-preview-the-effects-of-the-drag-and-drop-operation"></a>Pour afficher un aperçu du résultat de l’opération de glisser-déplacer

1.  Ouvrez Circle.xaml.cs ou Circle.xaml.vb.

2.  Dans la classe de cercle, déclarez une privée <xref:System.Windows.Media.Brush> variable nommée `_previousFill` et initialisez-la à `null`.

     [!code-csharp[DragDropWalkthrough#Brush](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#brush)]
     [!code-vb[DragDropWalkthrough#Brush](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#brush)]

3.  Ajoutez le code suivant <xref:System.Windows.UIElement.OnDragEnter%2A> override pour fournir la gestion de classe pour le <xref:System.Windows.UIElement.DragEnter> événement.

     [!code-csharp[DragDropWalkthrough#OnDragEnter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#ondragenter)]
     [!code-vb[DragDropWalkthrough#OnDragEnter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#ondragenter)]

     Cela <xref:System.Windows.UIElement.OnDragEnter%2A> remplacement effectue les tâches suivantes :

    -   Enregistre le <xref:System.Windows.Shapes.Shape.Fill%2A> propriété de la <xref:System.Windows.Shapes.Ellipse> dans le `_previousFill` variable.

    -   Exécute les mêmes vérifications que celles effectuées dans le <xref:System.Windows.UIElement.OnDrop%2A> méthode pour déterminer si les données peuvent être converties à un <xref:System.Windows.Media.Brush>.

    -   Si les données sont converties à valide <xref:System.Windows.Media.Brush>, s’applique à la <xref:System.Windows.Shapes.Shape.Fill%2A> de la <xref:System.Windows.Shapes.Ellipse>.

4.  Ajoutez le code suivant <xref:System.Windows.UIElement.OnDragLeave%2A> override pour fournir la gestion de classe pour le <xref:System.Windows.UIElement.DragLeave> événement.

     [!code-csharp[DragDropWalkthrough#OnDragLeave](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/Circle.xaml.cs#ondragleave)]
     [!code-vb[DragDropWalkthrough#OnDragLeave](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/Circle.xaml.vb#ondragleave)]

     Cela <xref:System.Windows.UIElement.OnDragLeave%2A> remplacement effectue les tâches suivantes :

    -   S’applique le <xref:System.Windows.Media.Brush> enregistré dans le `_previousFill` à la variable le <xref:System.Windows.Shapes.Shape.Fill%2A> de la <xref:System.Windows.Shapes.Ellipse> qui fournit l’interface utilisateur du contrôle d’utilisateur de cercle.

5.  Appuyez sur **F5** pour générer et exécuter l’application.

6.  Sélectionnez le texte `green` dans le <xref:System.Windows.Controls.TextBox>.

7.  Faites glisser le texte sur un contrôle de cercle sans le déplacer. Le cercle passe du bleu au vert.

     ![Prévisualiser les effets d’une opération de glisser-déplacer](../../../../docs/framework/wpf/advanced/media/dragdrop-previeweffects.png "DragDrop_PreviewEffects")

8.  Faites glisser le texte en dehors du contrôle de cercle. Le cercle passe du vert au bleu.

## <a name="enable-a-panel-to-receive-dropped-data"></a>Activer un panneau de recevoir des données déplacées

Dans cette section, vous permettez aux panneaux qui hébergent les contrôles utilisateur de cercle d’agir en tant que cibles de dépôt pour les données de cercle glissées. Vous implémentez le code qui vous permet de déplacer un cercle à partir d’un panneau à un autre, ou pour effectuer une copie d’un contrôle de cercle en maintenant enfoncée la **Ctrl** enfoncée tout en faisant glisser et déplacer d’un cercle.

1.  Ouvrez MainWindow.xaml.

2.  Comme indiqué dans le XAML suivant, dans chacun de la <xref:System.Windows.Controls.StackPanel> contrôles, ajoutez des gestionnaires pour les <xref:System.Windows.UIElement.DragOver> et <xref:System.Windows.UIElement.Drop> événements. Nom de la <xref:System.Windows.UIElement.DragOver> Gestionnaire d’événements, `panel_DragOver`et nommez le <xref:System.Windows.UIElement.Drop> Gestionnaire d’événements, `panel_Drop`.

     [!code-xaml[DragDropWalkthrough#PanelsXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/MainWindow.xaml#panelsxaml)]

3.  Ouvrez MainWindows.xaml.cs ou MainWindow.xaml.vb.

4.  Ajoutez le code suivant pour le <xref:System.Windows.UIElement.DragOver> Gestionnaire d’événements.

     [!code-csharp[DragDropWalkthrough#PanelDragOver](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/MainWindow.xaml.cs#paneldragover)]
     [!code-vb[DragDropWalkthrough#PanelDragOver](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/MainWindow.xaml.vb#paneldragover)]

     Cela <xref:System.Windows.UIElement.DragOver> Gestionnaire d’événements effectue les tâches suivantes :

    -   Vérifie que les données glissées contiennent les données « Object » qui a été empaquetées dans le <xref:System.Windows.DataObject> par le contrôle utilisateur de cercle et passées dans l’appel à <xref:System.Windows.DragDrop.DoDragDrop%2A>.

    -   Si les données « Object » sont présent, vérifie si le **Ctrl** touche est enfoncée.

    -   Si le **Ctrl** touche est enfoncée, définit le <xref:System.Windows.DragEventArgs.Effects%2A> propriété <xref:System.Windows.DragDropEffects.Copy>. Sinon, définissez le <xref:System.Windows.DragEventArgs.Effects%2A> propriété <xref:System.Windows.DragDropEffects.Move>.

5.  Ajoutez le code suivant pour le <xref:System.Windows.UIElement.Drop> Gestionnaire d’événements.

     [!code-csharp[DragDropWalkthrough#PanelDrop](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDropWalkthrough/CS/MainWindow.xaml.cs#paneldrop)]
     [!code-vb[DragDropWalkthrough#PanelDrop](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDropWalkthrough/VB/MainWindow.xaml.vb#paneldrop)]

     Cela <xref:System.Windows.UIElement.Drop> Gestionnaire d’événements effectue les tâches suivantes :

    -   Vérifie si le <xref:System.Windows.UIElement.Drop> événement a déjà été géré. Par exemple, si un cercle est déplacé sur un autre cercle qui gère la <xref:System.Windows.UIElement.Drop> événement, vous ne souhaitez pas que le panneau qui contient le contrôle de cercle gère aussi.

    -   Si le <xref:System.Windows.UIElement.Drop> événement n'est pas géré, vérifie si le **Ctrl** touche est enfoncée.

    -   Si le **Ctrl** touche est enfoncée quand le <xref:System.Windows.UIElement.Drop> se produit, effectue une copie du cercle, contrôle et ajoutez-la à la <xref:System.Windows.Controls.Panel.Children%2A> collection de la <xref:System.Windows.Controls.StackPanel>.

    -   Si le **Ctrl** touche n’est pas enfoncée, déplace le cercle à partir de la <xref:System.Windows.Controls.Panel.Children%2A> collection de son panneau parent vers le <xref:System.Windows.Controls.Panel.Children%2A> collection du panneau qui il a été supprimé.

    -   Définit le <xref:System.Windows.DragEventArgs.Effects%2A> propriété pour notifier le <xref:System.Windows.DragDrop.DoDragDrop%2A> méthode si une opération de déplacement ou de copie a été effectuée.

6.  Appuyez sur **F5** pour générer et exécuter l’application.

7.  Sélectionnez le texte `green` à partir de la <xref:System.Windows.Controls.TextBox>.

8.  Faites glisser le texte sur un contrôle de cercle et déplacez-le.

9. Faites glisser un contrôle de cercle du panneau gauche vers le panneau droit et déplacez-le. Le cercle est supprimé de la <xref:System.Windows.Controls.Panel.Children%2A> collection du panneau gauche et ajouté à la collection d’enfants du panneau droit.

10. Faites glisser un contrôle de cercle du panneau il est contenu vers l’autre panneau et déposez-le tout en appuyant sur la **Ctrl** clé. Le cercle est copié et la copie est ajoutée à la <xref:System.Windows.Controls.Panel.Children%2A> collection du Panneau de réception.

     ![Glissement d'un cercle en maintenant la touche CTRL enfoncée](../../../../docs/framework/wpf/advanced/media/dragdrop-paneldrop.png "DragDrop_PanelDrop")

## <a name="see-also"></a>Voir aussi

- [Vue d'ensemble du glisser-déplacer](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)