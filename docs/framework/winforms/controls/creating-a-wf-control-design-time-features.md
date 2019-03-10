---
title: 'Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms controls, creating
- design-time functionality [Windows Forms], Windows Forms
- DocumentDesigner class [Windows Forms]
- walkthroughs [Windows Forms], controls
ms.assetid: 6f487c59-cb38-4afa-ad2e-95edacb1d626
ms.openlocfilehash: 70cd08a9d7d03cec4e946d2acb806dbecfe774f7
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57724620"
---
# <a name="walkthrough-creating-a-windows-forms-control-that-takes-advantage-of-visual-studio-design-time-features"></a>Procédure pas à pas : Création d’un contrôle de formulaire Windows qui tire parti des fonctionnalités au moment du Design de Visual Studio

L’expérience au moment du design pour un contrôle personnalisé peut être améliorée en créant un concepteur personnalisé associé.

Cette procédure pas à pas illustre comment créer un concepteur personnalisé pour un contrôle personnalisé. Vous allez implémenter un `MarqueeControl` type et une classe de concepteur associée, appelé `MarqueeControlRootDesigner`.

Le `MarqueeControl` type implémente un affichage semblable à un texte défilant de théâtre, avec des lumières animées et du texte clignotant.

Le concepteur pour ce contrôle interagit avec l’environnement de conception pour fournir une expérience au moment du design personnalisée. Avec le concepteur personnalisé, vous pouvez assembler un personnalisé `MarqueeControl` implémentation avec des lumières animées et du texte clignotant selon plusieurs combinaisons. Vous pouvez utiliser le contrôle assemblé sur un formulaire comme tout autre contrôle Windows Forms.

Cette procédure pas à pas décrit notamment les tâches suivantes :

- Création du projet

- Création d’un projet de bibliothèque de contrôle

- Référencer le projet de contrôle personnalisé

- Définition d’un contrôle personnalisé et son concepteur personnalisé

- Création d’une Instance de votre contrôle personnalisé

- Configuration du projet pour le débogage au moment du Design

- Implémentation de votre contrôle personnalisé

- Création d’un contrôle enfant pour votre contrôle personnalisé

- Créer le contrôle enfant MarqueeBorder

- Création d’un concepteur personnalisé pour les clichés instantanés et les propriétés de filtre

- Gestion des modifications de composant

- Ajout de verbes de concepteur à votre concepteur personnalisé

- Création d’un UITypeEditor personnalisé

- Test de votre contrôle personnalisé dans le Concepteur

Lorsque vous avez terminé, votre contrôle personnalisé se présente comme suit :

![Possible de MarqueeControl](./media/demomarqueecontrol.gif "DemoMarqueeControl")

Pour l’intégralité du code, consultez [Comment : Créer un contrôle Windows Forms tire parti des fonctionnalités de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120)).

> [!NOTE]
> Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).

## <a name="prerequisites"></a>Prérequis

Pour exécuter cette procédure pas à pas, vous avez besoin des éléments suivants :

- Autorisations suffisantes pour pouvoir créer et exécuter des projets d’application Windows Forms sur l’ordinateur où Visual Studio est installé.

## <a name="creating-the-project"></a>Création du projet

La première étape consiste à créer le projet d’application. Vous utiliserez ce projet pour générer l’application qui héberge le contrôle personnalisé.

### <a name="to-create-the-project"></a>Pour créer le projet

- Créez un projet Windows Forms Application appelé « MarqueeControlTest » (**fichier** > **New** > **projet**  >   **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).

## <a name="creating-a-control-library-project"></a>Création d’un projet de bibliothèque de contrôle

L’étape suivante consiste à créer le projet de bibliothèque de contrôles. Vous allez créer un nouveau contrôle personnalisé et son concepteur personnalisé correspondant.

### <a name="to-create-the-control-library-project"></a>Pour créer le projet de bibliothèque de contrôle

1. Ajouter un projet de bibliothèque de contrôles Windows Forms à la solution. Nommez le projet « MarqueeControlLibrary ».

2. À l’aide de **l’Explorateur de solutions**, supprimer le contrôle du projet par défaut en supprimant le fichier source nommé « UserControl1.cs » ou « UserControl1.vb », en fonction de la langue de votre choix. Pour plus d'informations, voir [Procédure : Supprimer, suppression et exclure des éléments](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).

3. Ajouter un nouveau <xref:System.Windows.Forms.UserControl> d’élément à la `MarqueeControlLibrary` projet. Nommez le nouveau fichier source une base de « MarqueeControl. »

4. À l’aide de **l’Explorateur de solutions**, créez un dossier dans le `MarqueeControlLibrary` projet. Pour plus d'informations, voir [Procédure : Ajouter de nouveaux éléments de projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)). Nommez le nouveau dossier « Conception ».

5. Cliquez sur le **conception** dossier et ajoutez une nouvelle classe. Nommez le fichier source une base de « MarqueeControlRootDesigner. »

6. Vous devez utiliser des types de l’assembly System.Design, ajoutez cette référence à la `MarqueeControlLibrary` projet.

    > [!NOTE]
    > Pour utiliser l’assembly System.Design, votre projet doit cibler la version complète du .NET Framework, pas le .NET Framework Client Profile. Pour modifier le framework cible, consultez [Comment : Cibler une version du .NET Framework](/visualstudio/ide/how-to-target-a-version-of-the-dotnet-framework).

## <a name="referencing-the-custom-control-project"></a>Référencer le projet de contrôle personnalisé

Vous utiliserez le `MarqueeControlTest` projet pour tester le contrôle personnalisé. Le projet de test auront connaissance du contrôle personnalisé lorsque vous ajoutez une référence de projet pour le `MarqueeControlLibrary` assembly.

### <a name="to-reference-the-custom-control-project"></a>Pour référencer le projet de contrôle personnalisé

- Dans le `MarqueeControlTest` de projet, ajoutez une référence de projet pour le `MarqueeControlLibrary` assembly. Veillez à utiliser le **projets** onglet dans le **ajouter une référence** boîte de dialogue au lieu de référencer le `MarqueeControlLibrary` assembly directement.

## <a name="defining-a-custom-control-and-its-custom-designer"></a>Définition d’un contrôle personnalisé et son concepteur personnalisé
 Votre contrôle personnalisé doivent dériver de la <xref:System.Windows.Forms.UserControl> classe. Cela permet à votre contrôle de contenir d’autres contrôles, et il donne à votre contrôle un grand nombre de fonctionnalités par défaut.

 Votre contrôle personnalisé aura un concepteur personnalisé associé. Cela vous permet de créer une expérience de conception unique spécifiquement adaptée à votre contrôle personnalisé.

 Vous associez le contrôle à son concepteur à l’aide de la <xref:System.ComponentModel.DesignerAttribute> classe. Étant donné que vous développez l’ensemble du comportement au moment du design de votre contrôle personnalisé, le concepteur personnalisé implémentera le <xref:System.ComponentModel.Design.IRootDesigner> interface.

### <a name="to-define-a-custom-control-and-its-custom-designer"></a>Pour définir un contrôle personnalisé et son concepteur personnalisé

1. Ouvrez le `MarqueeControl` fichier source dans le **éditeur de Code**. En haut du fichier, importez les espaces de noms suivants :

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#220](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrol.cs#220)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#220](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrol.vb#220)]

2. Ajouter le <xref:System.ComponentModel.DesignerAttribute> à la `MarqueeControl` déclaration de classe. Cela associe le contrôle personnalisé à son concepteur.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#240](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrol.cs#240)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#240](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrol.vb#240)]

3. Ouvrez le `MarqueeControlRootDesigner` fichier source dans le **éditeur de Code**. En haut du fichier, importez les espaces de noms suivants :

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#520](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#520)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#520](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#520)]

4. Modifiez la déclaration de `MarqueeControlRootDesigner` d’hériter de la <xref:System.Windows.Forms.Design.DocumentDesigner> classe. Appliquer le <xref:System.ComponentModel.ToolboxItemFilterAttribute> pour spécifier l’interaction du concepteur avec le **boîte à outils**.

     **Remarque** la définition de la `MarqueeControlRootDesigner` classe a été placée dans un espace de noms appelé « MarqueeControlLibrary.Design ». Cette déclaration place le concepteur dans un espace de noms spécial réservé pour les types liés à la conception.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#530](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#530)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#530](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#530)]

5. Définissez le constructeur pour la `MarqueeControlRootDesigner` classe. Insérer un <xref:System.Diagnostics.Trace.WriteLine%2A> instruction dans le corps du constructeur. Cela sera utile pour le débogage.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#540](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#540)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#540](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#540)]

## <a name="creating-an-instance-of-your-custom-control"></a>Création d’une Instance de votre contrôle personnalisé
 Pour observer le comportement personnalisé au moment du design de votre contrôle, vous placerez une instance de votre contrôle sur le formulaire dans `MarqueeControlTest` projet.

### <a name="to-create-an-instance-of-your-custom-control"></a>Pour créer une instance de votre contrôle personnalisé

1. Ajouter un nouveau <xref:System.Windows.Forms.UserControl> d’élément à la `MarqueeControlTest` projet. Nommez le nouveau fichier source une base de « DemoMarqueeControl. »

2. Ouvrez le `DemoMarqueeControl` de fichiers dans le **éditeur de Code**. En haut du fichier, importez le `MarqueeControlLibrary` espace de noms :

```vb
Imports MarqueeControlLibrary
```

```csharp
using MarqueeControlLibrary;
```

1. Modifiez la déclaration de `DemoMarqueeControl` d’hériter de la `MarqueeControl` classe.

2. Générez le projet.

3. Ouvrez `Form1` dans le Concepteur Windows Forms.

4. Rechercher la **Composants MarqueeControlTest** onglet dans le **boîte à outils** et ouvrez-le. Faites glisser un `DemoMarqueeControl` à partir de la **boîte à outils** vers votre formulaire.

5. Générez le projet.

## <a name="setting-up-the-project-for-design-time-debugging"></a>Configuration du projet pour le débogage au moment du Design

Lorsque vous développez une expérience de conception personnalisée, il sera nécessaire déboguer vos composants et contrôles. Il existe un moyen simple de configurer votre projet pour autoriser le débogage au moment du design. Pour plus d’informations, consultez [Procédure pas à pas : Débogage personnalisés Windows Forms des contrôles au moment du Design](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md).

### <a name="to-set-up-the-project-for-design-time-debugging"></a>Pour configurer le projet pour le débogage au moment du design

1. Cliquez sur le `MarqueeControlLibrary` de projet et sélectionnez **propriétés**.

2. Dans la boîte de dialogue « Pages de propriétés MarqueeControlLibrary », sélectionnez le **déboguer** page.

3. Dans le **Action de démarrage** section, sélectionnez **démarrer le programme externe**. Vous serez le débogage d’une instance distincte de Visual Studio, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) pour le rechercher l’IDE Visual Studio. Le nom du fichier exécutable est devenv.exe, et si vous avez installé à l’emplacement par défaut, son chemin d’accès est %programfiles%\Microsoft Visual Studio 9.0\Common7\IDE\devenv.exe.

4. Cliquez sur OK pour fermer la boîte de dialogue.

5. Cliquez sur le `MarqueeControlLibrary` de projet et sélectionnez « Définir comme projet de démarrage » pour activer cette configuration de débogage.

## <a name="checkpoint"></a>Point de contrôle

Vous êtes maintenant prêt à déboguer le comportement au moment du design de votre contrôle personnalisé. Une fois que vous avez déterminé que l’environnement de débogage est correctement configuré, vous allez tester l’association entre le contrôle personnalisé et le concepteur personnalisé.

### <a name="to-test-the-debugging-environment-and-the-designer-association"></a>Pour tester l’environnement de débogage et l’association de concepteur

1. Ouvrez le `MarqueeControlRootDesigner` fichier source dans le **éditeur de Code** et placer un point d’arrêt sur la <xref:System.Diagnostics.Trace.WriteLine%2A> instruction.

2. Appuyez sur F5 pour démarrer la session de débogage. Notez qu’une nouvelle instance de Visual Studio est créée.

3. Dans la nouvelle instance de Visual Studio, ouvrez la solution « MarqueeControlTest ». Vous pouvez facilement trouver la solution en sélectionnant **projets récents** à partir de la **fichier** menu. Le fichier de solution « MarqueeControlTest.sln » apparaît comme étant le dernier fichier utilisé.

4. Ouvrez le `DemoMarqueeControl` dans le concepteur. Notez que l’instance de débogage de Visual Studio acquiert le focus et l’exécution s’arrête au point d’arrêt. Appuyez sur F5 pour continuer la session de débogage.

À ce stade, tout est en place pour vous permettre de développer et déboguer votre contrôle personnalisé et son concepteur personnalisé associé. Le reste de cette procédure pas à pas se concentre sur les détails de l’implémentation des fonctionnalités du contrôle et le concepteur.

## <a name="implementing-your-custom-control"></a>Implémentation de votre contrôle personnalisé

Le `MarqueeControl` est un <xref:System.Windows.Forms.UserControl> avec un peu de personnalisation. Il expose deux méthodes : `Start`, qui démarre l’animation de texte défilant, et `Stop`, ce qui arrête l’animation. Étant donné que le `MarqueeControl` contient des contrôles enfants qui implémentent le `IMarqueeWidget` interface, `Start` et `Stop` énumérer chaque contrôle enfant et l’appel de la `StartMarquee` et `StopMarquee` méthodes, respectivement, sur chaque contrôle enfant qui implémente `IMarqueeWidget`.

L’apparence de la `MarqueeBorder` et `MarqueeText` contrôles est dépendante de la disposition, afin `MarqueeControl` remplace le <xref:System.Windows.Forms.Control.OnLayout%2A> méthode et appelle <xref:System.Windows.Forms.Control.PerformLayout%2A> sur les contrôles enfants de ce type.

Ceci est l’étendue de la `MarqueeControl` personnalisations. Les fonctionnalités d’exécution sont implémentées par le `MarqueeBorder` et `MarqueeText` contrôles et les fonctionnalités au moment du design sont implémentées par le `MarqueeBorderDesigner` et `MarqueeControlRootDesigner` classes.

### <a name="to-implement-your-custom-control"></a>Pour implémenter votre contrôle personnalisé

1. Ouvrez le `MarqueeControl` fichier source dans le **éditeur de Code**. Implémentez le `Start` et `Stop` méthodes.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#260](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrol.cs#260)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#260](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrol.vb#260)]

2. Remplacez la méthode <xref:System.Windows.Forms.Control.OnLayout%2A> .

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#270](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrol.cs#270)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#270](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrol.vb#270)]

## <a name="creating-a-child-control-for-your-custom-control"></a>Création d’un contrôle enfant pour votre contrôle personnalisé

Le `MarqueeControl` hébergera les deux types de contrôle enfant : le `MarqueeBorder` contrôle et le `MarqueeText` contrôle.

- `MarqueeBorder`: Ce contrôle est peint une bordure de « lumières » autour de ses bords. Les lumières flash en séquence, afin qu’ils semblent se déplacent autour de la bordure. La vitesse à laquelle l’éclairage flash est contrôlée par une propriété appelée `UpdatePeriod`. Plusieurs autres propriétés personnalisées déterminent les autres aspects de l’apparence du contrôle. Deux méthodes, appelées `StartMarquee` et `StopMarquee`, contrôler quand l’animation démarre et s’arrête.

- `MarqueeText`: Ce contrôle est peint une chaîne clignotante. Comme le `MarqueeBorder` contrôle, la vitesse à laquelle le texte clignote est contrôlée par le `UpdatePeriod` propriété. Le `MarqueeText` contrôle a également la `StartMarquee` et `StopMarquee` méthodes en commun avec la `MarqueeBorder` contrôle.

Au moment du design, le `MarqueeControlRootDesigner` permet à ces deux types de contrôle à ajouter à un `MarqueeControl` dans n’importe quelle combinaison.

Fonctionnalités communes des deux contrôles sont incluses dans une interface appelée `IMarqueeWidget`. Cela permet la `MarqueeControl` pour découvrir tous les contrôles enfants connexes au texte défilant et de leur traitement spécial.

Pour implémenter la fonctionnalité d’animation périodique, vous allez utiliser <xref:System.ComponentModel.BackgroundWorker> objets à partir de la <xref:System.ComponentModel?displayProperty=nameWithType> espace de noms. Vous pouvez utiliser <xref:System.Windows.Forms.Timer> objets, mais lorsque plusieurs `IMarqueeWidget` objets sont présents, le thread d’interface utilisateur unique peut être incapable de suivre l’animation.

### <a name="to-create-a-child-control-for-your-custom-control"></a>Pour créer un contrôle enfant pour votre contrôle personnalisé

1. Ajouter un nouvel élément de classe pour le `MarqueeControlLibrary` projet. Nommez le nouveau fichier source une base « IMarqueeWidget. »

2. Ouvrez le `IMarqueeWidget` fichier source dans le **éditeur de Code** et modifiez la déclaration de `class` à `interface`:

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/imarqueewidget.cs#2)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/imarqueewidget.vb#2)]

3. Ajoutez le code suivant à la `IMarqueeWidget` interface à exposer deux méthodes et une propriété qui manipulent l’animation de texte défilant :

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/imarqueewidget.cs#3)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/imarqueewidget.vb#3)]

4. Ajouter un nouveau **contrôle personnalisé** d’élément à la `MarqueeControlLibrary` projet. Nommez le nouveau fichier source une base de « MarqueeText. »

5. Faites glisser un <xref:System.ComponentModel.BackgroundWorker> composant à partir de la **boîte à outils** sur votre `MarqueeText` contrôle. Ce composant permettra la `MarqueeText` contrôle se mettre à jour en mode asynchrone.

6. Dans la fenêtre Propriétés, définissez la <xref:System.ComponentModel.BackgroundWorker> du composant `WorkerReportsProgress` et <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> propriétés à `true`. Ces paramètres permettent la <xref:System.ComponentModel.BackgroundWorker> composant déclencher périodiquement la <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événement et d’annuler les mises à jour asynchrones. Pour plus d’informations, consultez [composant BackgroundWorker](backgroundworker-component.md).

7. Ouvrez le `MarqueeText` fichier source dans le **éditeur de Code**. En haut du fichier, importez les espaces de noms suivants :

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#120](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#120)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#120](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#120)]

8. Modifiez la déclaration de `MarqueeText` d’hériter de <xref:System.Windows.Forms.Label> et pour implémenter le `IMarqueeWidget` interface :

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#130](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#130)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#130](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#130)]

9. Déclarez les variables d’instance qui correspondent aux propriétés exposées et les initialiser dans le constructeur. Le `isLit` champ détermine si le texte doit être peint dans la couleur indiquée par le `LightColor` propriété.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#140](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#140)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#140](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#140)]

10. Implémentez l'interface `IMarqueeWidget`.

    Le `StartMarquee` et `StopMarquee` méthodes appellent le <xref:System.ComponentModel.BackgroundWorker> du composant <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> et <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> méthodes pour démarrer et arrêter l’animation.

    Le <xref:System.ComponentModel.CategoryAttribute.Category%2A> et <xref:System.ComponentModel.BrowsableAttribute.Browsable%2A> attributs sont appliqués à la `UpdatePeriod` propriété afin qu’il apparaisse dans une section personnalisée de la fenêtre Propriétés appelée « Sélection ».

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#150](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#150)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#150](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#150)]

11. Implémentez les accesseurs de propriété. Vous exposerez deux propriétés aux clients : `LightColor` et `DarkColor`. Le <xref:System.ComponentModel.CategoryAttribute.Category%2A> et <xref:System.ComponentModel.BrowsableAttribute.Browsable%2A> attributs sont appliqués à ces propriétés, par conséquent, les propriétés apparaissent dans une section personnalisée de la fenêtre Propriétés appelée « Sélection ».

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#160](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#160)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#160](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#160)]

12. Implémentez les gestionnaires pour le <xref:System.ComponentModel.BackgroundWorker> du composant <xref:System.ComponentModel.BackgroundWorker.DoWork> et <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événements.

    Le <xref:System.ComponentModel.BackgroundWorker.DoWork> se met en veille du Gestionnaire d’événements pour le nombre de millisecondes spécifié par `UpdatePeriod` puis déclenche le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événement, jusqu'à ce que votre code s’arrête l’animation en appelant <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A>.

    Le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> Gestionnaire d’événements Active ou désactive le texte entre son état clair et sombre pour donner l’apparence d’un clignotement.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#180](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#180)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#180](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#180)]

13. Remplacer le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode pour activer l’animation.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#170](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueetext.cs#170)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#170](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueetext.vb#170)]

14. Appuyez sur F6 pour générer la solution.

## <a name="create-the-marqueeborder-child-control"></a>Créer le contrôle enfant MarqueeBorder

Le `MarqueeBorder` contrôle est légèrement plus sophistiqué que le `MarqueeText` contrôle. Il a plus de propriétés et l’animation dans le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode est plus complexe. En principe, il est assez semblable à la `MarqueeText` contrôle.

Étant donné que le `MarqueeBorder` contrôle peut avoir des contrôles enfants, il doit être conscient de <xref:System.Windows.Forms.Control.Layout> événements.

### <a name="to-create-the-marqueeborder-control"></a>Pour créer le contrôle MarqueeBorder

1. Ajouter un nouveau **contrôle personnalisé** d’élément à la `MarqueeControlLibrary` projet. Nommez le nouveau fichier source une base de « MarqueeBorder. »

2. Faites glisser un <xref:System.ComponentModel.BackgroundWorker> composant à partir de la **boîte à outils** sur votre `MarqueeBorder` contrôle. Ce composant permettra la `MarqueeBorder` contrôle se mettre à jour en mode asynchrone.

3. Dans la fenêtre Propriétés, définissez la <xref:System.ComponentModel.BackgroundWorker> du composant `WorkerReportsProgress` et <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> propriétés à `true`. Ces paramètres permettent la <xref:System.ComponentModel.BackgroundWorker> composant déclencher périodiquement la <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événement et d’annuler les mises à jour asynchrones. Pour plus d’informations, consultez [composant BackgroundWorker](backgroundworker-component.md).

4. Dans la fenêtre Propriétés, cliquez sur le bouton événements. Joindre des gestionnaires pour les <xref:System.ComponentModel.BackgroundWorker.DoWork> et <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événements.

5. Ouvrez le `MarqueeBorder` fichier source dans le **éditeur de Code**. En haut du fichier, importez les espaces de noms suivants :

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#20)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#20)]

6. Modifiez la déclaration de `MarqueeBorder` d’hériter de <xref:System.Windows.Forms.Panel> et pour implémenter le `IMarqueeWidget` interface.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#30)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#30)]

7. Déclarez deux énumérations pour gérer le `MarqueeBorder` état du contrôle : `MarqueeSpinDirection`, qui détermine la direction dans laquelle les lumières « tournent » autour de la bordure et `MarqueeLightShape`, qui détermine la forme des lumières (carrées ou circulaires). Placez ces déclarations avant la `MarqueeBorder` déclaration de classe.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#97](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#97)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#97](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#97)]

8. Déclarez les variables d’instance qui correspondent aux propriétés exposées et les initialiser dans le constructeur.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#40)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#40)]

9. Implémentez l'interface `IMarqueeWidget`.

    Le `StartMarquee` et `StopMarquee` méthodes appellent le <xref:System.ComponentModel.BackgroundWorker> du composant <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> et <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> méthodes pour démarrer et arrêter l’animation.

    Étant donné que le `MarqueeBorder` contrôle peut contenir des contrôles enfants, le `StartMarquee` méthode énumère tous les contrôles enfants et les appels `StartMarquee` sur ceux qui implémentent `IMarqueeWidget`. Le `StopMarquee` méthode a une implémentation semblable.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#50](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#50)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#50](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#50)]

10. Implémentez les accesseurs de propriété. Le `MarqueeBorder` contrôle a plusieurs propriétés pour contrôler son apparence.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#60)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#60)]

11. Implémentez les gestionnaires pour le <xref:System.ComponentModel.BackgroundWorker> du composant <xref:System.ComponentModel.BackgroundWorker.DoWork> et <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événements.

    Le <xref:System.ComponentModel.BackgroundWorker.DoWork> se met en veille du Gestionnaire d’événements pour le nombre de millisecondes spécifié par `UpdatePeriod` puis déclenche le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> événement, jusqu'à ce que votre code s’arrête l’animation en appelant <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A>.

    Le <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> Gestionnaire d’événements incrémente la position de la lumière « base », à partir de laquelle l’état clair/sombre des autres lumières est déterminé, et appelle le <xref:System.Windows.Forms.Control.Refresh%2A> méthode pour que le contrôle à se redessiner.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#90](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#90)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#90](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#90)]

12. Implémenter les méthodes d’assistance, `IsLit` et `DrawLight`.

    Le `IsLit` méthode détermine la couleur d’une lumière à une position donnée. Les lumières sont « allumés » sont dessinées dans la couleur indiquée par le `LightColor` propriété et celles qui sont « foncé » sont dessinées dans la couleur indiquée par le `DarkColor` propriété.

    Le `DrawLight` méthode dessine une lumière à l’aide de la couleur appropriée, la forme et la position.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#80](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#80)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#80](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#80)]

13. Remplacer le <xref:System.Windows.Forms.Control.OnLayout%2A> et <xref:System.Windows.Forms.Control.OnPaint%2A> méthodes.

    Le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode dessine les lumières le long des bords de la `MarqueeBorder` contrôle.

    Étant donné que le <xref:System.Windows.Forms.Control.OnPaint%2A> méthode varie selon les dimensions de la `MarqueeBorder` contrôle, vous devez l’appeler chaque fois que la disposition change. Pour ce faire, substituez <xref:System.Windows.Forms.Control.OnLayout%2A> et appelez <xref:System.Windows.Forms.Control.Refresh%2A>.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#70](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#70)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#70](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#70)]

## <a name="creating-a-custom-designer-to-shadow-and-filter-properties"></a>Création d’un concepteur personnalisé pour les clichés instantanés et les propriétés de filtre

Le `MarqueeControlRootDesigner` classe fournit l’implémentation pour le concepteur racine. En plus de ce concepteur, qui fonctionne sur le `MarqueeControl`, vous devez un concepteur personnalisé qui est associé spécifiquement le `MarqueeBorder` contrôle. Ce concepteur fournit un comportement personnalisé qui est approprié dans le contexte du concepteur racine personnalisé.

Plus précisément, le `MarqueeBorderDesigner` sera « masquer » et filtrer certaines propriétés sur le `MarqueeBorder` contrôle, en modifiant leur interaction avec l’environnement de conception.

L’interception d’appels à l’accesseur de propriété d’un composant est appelé « occultation ». Il permet à un concepteur effectuer le suivi de la valeur définie par l’utilisateur et éventuellement passer cette valeur au composant en cours de conception.

Pour cet exemple, le <xref:System.Windows.Forms.Control.Visible%2A> et <xref:System.Windows.Forms.Control.Enabled%2A> propriétés seront occultées par le `MarqueeBorderDesigner`, ce qui empêche l’utilisateur d’apporter la `MarqueeBorder` contrôle invisible ou désactivée au moment du design.

Les concepteurs peuvent également ajouter ou supprimer des propriétés. Pour cet exemple, le <xref:System.Windows.Forms.Control.Padding%2A> propriété sera supprimée au moment du design, car le `MarqueeBorder` contrôle définit par programme le remplissage selon la taille des lumières spécifiées par la `LightSize` propriété.

La classe de base pour `MarqueeBorderDesigner` est <xref:System.ComponentModel.Design.ComponentDesigner>, qui a des méthodes qui peuvent modifier les attributs, les propriétés et les événements exposés par un contrôle au moment du design :

- <xref:System.ComponentModel.Design.ComponentDesigner.PreFilterProperties%2A>

- <xref:System.ComponentModel.Design.ComponentDesigner.PostFilterProperties%2A>

- <xref:System.ComponentModel.Design.ComponentDesigner.PreFilterAttributes%2A>

- <xref:System.ComponentModel.Design.ComponentDesigner.PostFilterAttributes%2A>

- <xref:System.ComponentModel.Design.ComponentDesigner.PreFilterEvents%2A>

- <xref:System.ComponentModel.Design.ComponentDesigner.PostFilterEvents%2A>

Lorsque vous modifiez l’interface publique d’un composant à l’aide de ces méthodes, vous devez suivre ces règles :

- Ajouter ou supprimer des éléments dans le `PreFilter` méthodes uniquement

- Modifier des éléments existants dans le `PostFilter` méthodes uniquement

- Appeler l’implémentation de base tout d’abord dans le `PreFilter` méthodes

- Appeler l’implémentation de base dernière dans le `PostFilter` méthodes

Adhérant à ces règles permet de s’assurer que tous les concepteurs dans l’environnement au moment du design ont une vue cohérente de tous les composants en cours de conception.

Le <xref:System.ComponentModel.Design.ComponentDesigner> classe fournit un dictionnaire pour gérer les valeurs des propriétés occultées, ce qui vous évite d’avoir à créer des variables d’instance spécifique.

### <a name="to-create-a-custom-designer-to-shadow-and-filter-properties"></a>Pour créer un concepteur personnalisé pour les propriétés de filtre et les clichés instantanés

1. Cliquez sur le **conception** dossier et ajoutez une nouvelle classe. Nommez le fichier source une base de « MarqueeBorderDesigner. »

2. Ouvrez le `MarqueeBorderDesigner` fichier source dans le **éditeur de Code**. En haut du fichier, importez les espaces de noms suivants :

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#420](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborderdesigner.cs#420)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#420](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborderdesigner.vb#420)]

3. Modifiez la déclaration de `MarqueeBorderDesigner` d’hériter de <xref:System.Windows.Forms.Design.ParentControlDesigner>.

    Étant donné que le `MarqueeBorder` contrôle peut contenir des contrôles enfants, `MarqueeBorderDesigner` hérite <xref:System.Windows.Forms.Design.ParentControlDesigner>, qui gère l’interaction parent-enfant.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#430](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborderdesigner.cs#430)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#430](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborderdesigner.vb#430)]

4. Substituer l’implémentation de base de <xref:System.ComponentModel.Design.ComponentDesigner.PreFilterProperties%2A>.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#450](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborderdesigner.cs#450)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#450](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborderdesigner.vb#450)]

5. Implémentez les propriétés <xref:System.Windows.Forms.Control.Enabled%2A> et <xref:System.Windows.Forms.Control.Visible%2A>. Ces implémentations occultent les propriétés du contrôle.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#440](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborderdesigner.cs#440)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#440](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborderdesigner.vb#440)]

## <a name="handling-component-changes"></a>Gestion des modifications de composant
 Le `MarqueeControlRootDesigner` classe fournit l’expérience au moment du design personnalisé pour votre `MarqueeControl` instances. La plupart des fonctionnalités au moment du design est héritée de la <xref:System.Windows.Forms.Design.DocumentDesigner> classe ; votre code est implémenter deux personnalisations spécifiques : gestion des modifications de composant et l’ajout de verbes de concepteur.

 En tant que les utilisateurs à concevoir leurs `MarqueeControl` instances, votre concepteur racine suit les modifications apportées à la `MarqueeControl` et ses contrôles enfants. L’environnement au moment du design offre un service commode, <xref:System.ComponentModel.Design.IComponentChangeService>, pour le suivi des modifications à l’état du composant.

 Vous acquérez une référence à ce service en interrogeant l’environnement avec la <xref:System.ComponentModel.Design.ComponentDesigner.GetService%2A> (méthode). Si la requête est réussie, votre concepteur peut joindre un gestionnaire pour le <xref:System.ComponentModel.Design.IComponentChangeService.ComponentChanged> événements et effectuer toutes les tâches qui sont nécessaires pour maintenir un état cohérent au moment du design.

 Dans le cas de la `MarqueeControlRootDesigner` (classe), vous appellerez la <xref:System.Windows.Forms.Control.Refresh%2A> méthode sur chaque `IMarqueeWidget` objet contenu dans le `MarqueeControl`. Cela entraîne le `IMarqueeWidget` objet à se redessiner correctement lorsque les propriétés telles que son parent <xref:System.Windows.Forms.Control.Size%2A> sont modifiés.

### <a name="to-handle-component-changes"></a>Pour gérer les changements de composant

1. Ouvrez le `MarqueeControlRootDesigner` fichier source dans le **éditeur de Code** et remplacer le <xref:System.Windows.Forms.Design.DocumentDesigner.Initialize%2A> (méthode). Appeler l’implémentation de base de <xref:System.Windows.Forms.Design.DocumentDesigner.Initialize%2A> et de requête pour le <xref:System.ComponentModel.Design.IComponentChangeService>.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#580](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#580)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#580](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#580)]

2. Implémentez le <xref:System.ComponentModel.Design.IComponentChangeService.OnComponentChanged%2A> Gestionnaire d’événements. Type du composant d’émission, de test et s’il s’agit une `IMarqueeWidget`, appeler ses <xref:System.Windows.Forms.Control.Refresh%2A> (méthode).

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#560](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#560)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#560](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#560)]

## <a name="adding-designer-verbs-to-your-custom-designer"></a>Ajout de verbes de concepteur à votre concepteur personnalisé

Un verbe de concepteur est une commande de menu liée à un gestionnaire d’événements. Verbes de concepteur sont ajoutés au menu contextuel d’un composant au moment du design. Pour plus d'informations, consultez <xref:System.ComponentModel.Design.DesignerVerb>.

Vous allez ajouter deux verbes de concepteur à vos concepteurs : **Exécuter Test** et **arrêter le Test**. Ces verbes vous permettra d’afficher le comportement au moment de l’exécution de la `MarqueeControl` au moment du design. Ces verbes seront ajoutés à la `MarqueeControlRootDesigner`.

Lorsque **exécuter le Test** est appelé, le Gestionnaire d’événements de verbe appellera le `StartMarquee` méthode sur le `MarqueeControl`. Lorsque **arrêter le Test** est appelé, le Gestionnaire d’événements de verbe appellera le `StopMarquee` méthode sur le `MarqueeControl`. L’implémentation de la `StartMarquee` et `StopMarquee` méthodes appellent ces méthodes sur les contrôles contenus qui implémentent `IMarqueeWidget`les `IMarqueeWidget` contrôles participeront également dans le test.

### <a name="to-add-designer-verbs-to-your-custom-designers"></a>Pour ajouter des verbes de concepteur à vos concepteurs personnalisés

1. Dans le `MarqueeControlRootDesigner` de classe, l’ajout de gestionnaires d’événements nommé `OnVerbRunTest` et `OnVerbStopTest`.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#570](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#570)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#570](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#570)]

2. Se connecter à ces gestionnaires d’événements à leurs verbes de concepteur correspondantes. `MarqueeControlRootDesigner` hérite une <xref:System.ComponentModel.Design.DesignerVerbCollection> à partir de sa classe de base. Vous allez créer deux nouveaux <xref:System.ComponentModel.Design.DesignerVerb> objets et les ajouter à cette collection dans le <xref:System.Windows.Forms.Design.DocumentDesigner.Initialize%2A> (méthode).

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#590](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueecontrolrootdesigner.cs#590)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#590](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueecontrolrootdesigner.vb#590)]

## <a name="creating-a-custom-uitypeeditor"></a>Création d’un UITypeEditor personnalisé

Lorsque vous créez une expérience au moment du design personnalisée pour les utilisateurs, il est souvent préférable de créer une interaction personnalisée avec la fenêtre Propriétés. Vous pouvez y parvenir en créant un <xref:System.Drawing.Design.UITypeEditor>. Pour plus d'informations, voir [Procédure : Créer un éditeur de Type d’interface utilisateur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/fd3kt7d5(v=vs.120)).

Le `MarqueeBorder` contrôle expose plusieurs propriétés dans la fenêtre Propriétés. Deux de ces propriétés, `MarqueeSpinDirection` et `MarqueeLightShape` sont représentés par des énumérations. Pour illustrer l’utilisation d’un éditeur de type d’interface utilisateur, le `MarqueeLightShape` propriété aura associé à un <xref:System.Drawing.Design.UITypeEditor> classe.

### <a name="to-create-a-custom-ui-type-editor"></a>Pour créer un type d’interface utilisateur personnalisé éditeur

1. Ouvrez le `MarqueeBorder` fichier source dans le **éditeur de Code**.

2. Dans la définition de la `MarqueeBorder` classe, déclarez une classe appelée `LightShapeEditor` qui dérive de <xref:System.Drawing.Design.UITypeEditor>.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#96](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#96)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#96](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#96)]

3. Déclarez un <xref:System.Windows.Forms.Design.IWindowsFormsEditorService> variable d’instance appelée `editorService`.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#92](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#92)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#92](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#92)]

4. Remplacez la méthode <xref:System.Drawing.Design.UITypeEditor.GetEditStyle%2A> . Cette implémentation retourne <xref:System.Drawing.Design.UITypeEditorEditStyle.DropDown>, ce qui indique à l’environnement de design comment afficher le `LightShapeEditor`.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#93](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#93)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#93](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#93)]

5. Remplacez la méthode <xref:System.Drawing.Design.UITypeEditor.EditValue%2A> . Cette implémentation interroge l’environnement de conception pour un <xref:System.Windows.Forms.Design.IWindowsFormsEditorService> objet. Si la réussite, il crée un `LightShapeSelectionControl`. Le <xref:System.Windows.Forms.Design.IWindowsFormsEditorService.DropDownControl%2A> méthode est appelée pour démarrer le `LightShapeEditor`. La valeur de retour de cet appel est retournée à l’environnement de conception.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#94](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/marqueeborder.cs#94)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#94](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/marqueeborder.vb#94)]

## <a name="creating-a-view-control-for-your-custom-uitypeeditor"></a>Création d’un contrôle d’affichage pour votre UITypeEditor personnalisé

1. Le `MarqueeLightShape` propriété prend en charge deux types de formes légères : `Square` et `Circle`. Vous allez créer un contrôle personnalisé utilisé aux seules fins afficher graphiquement ces valeurs dans la fenêtre Propriétés. Ce contrôle personnalisé sera être utilisé par votre <xref:System.Drawing.Design.UITypeEditor> pour interagir avec la fenêtre Propriétés.

### <a name="to-create-a-view-control-for-your-custom-ui-type-editor"></a>Pour créer un contrôle d’affichage pour votre interface utilisateur personnalisée à l’éditeur de type

1. Ajouter un nouveau <xref:System.Windows.Forms.UserControl> d’élément à la `MarqueeControlLibrary` projet. Nommez le nouveau fichier source une base de « LightShapeSelectionControl. »

2. Faites glisser deux <xref:System.Windows.Forms.Panel> des contrôles de la **boîte à outils** sur le `LightShapeSelectionControl`. Nommez-les `squarePanel` et `circlePanel`. Disposez-les côte à côte. Définir le <xref:System.Windows.Forms.Control.Size%2A> propriété des deux <xref:System.Windows.Forms.Panel> de contrôles à (60, 60). Définir le <xref:System.Windows.Forms.Control.Location%2A> propriété de la `squarePanel` le contrôle à (8, 10). Définir le <xref:System.Windows.Forms.Control.Location%2A> propriété de la `circlePanel` le contrôle à (80, 10). Enfin, définissez la <xref:System.Windows.Forms.Control.Size%2A> propriété de la `LightShapeSelectionControl` à (150, 80).

3. Ouvrez le `LightShapeSelectionControl` fichier source dans le **éditeur de Code**. En haut du fichier, importez le <xref:System.Windows.Forms.Design?displayProperty=nameWithType> espace de noms :

```vb
Imports System.Windows.Forms.Design
```

```csharp
using System.Windows.Forms.Design;
```

1. Implémentez <xref:System.Windows.Forms.Control.Click> gestionnaires d’événements pour le `squarePanel` et `circlePanel` contrôles. Ces méthodes appellent <xref:System.Windows.Forms.Design.IWindowsFormsEditorService.CloseDropDown%2A> à la fin personnalisé <xref:System.Drawing.Design.UITypeEditor> session d’édition.

    [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#390](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/lightshapeselectioncontrol.cs#390)]
    [!code-vb[System.Windows.Forms.Design.DocumentDesigner#390](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/lightshapeselectioncontrol.vb#390)]

2. Déclarez un <xref:System.Windows.Forms.Design.IWindowsFormsEditorService> variable d’instance appelée `editorService`.

```vb
Private editorService As IWindowsFormsEditorService
```

```csharp
private IWindowsFormsEditorService editorService;
```

1. Déclarez un `MarqueeLightShape` variable d’instance appelée `lightShapeValue`.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#330](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/lightshapeselectioncontrol.cs#330)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#330](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/lightshapeselectioncontrol.vb#330)]

2. Dans le `LightShapeSelectionControl` constructeur, attacher le <xref:System.Windows.Forms.Control.Click> gestionnaires d’événements pour le `squarePanel` et `circlePanel` contrôles <xref:System.Windows.Forms.Control.Click> événements. Définissez également une surcharge de constructeur qui affecte le `MarqueeLightShape` valeur de l’environnement de conception vers le `lightShapeValue` champ.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#340](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/lightshapeselectioncontrol.cs#340)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#340](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/lightshapeselectioncontrol.vb#340)]

3. Dans le <xref:System.ComponentModel.Component.Dispose%2A> (méthode), détacher le <xref:System.Windows.Forms.Control.Click> gestionnaires d’événements.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#350](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/lightshapeselectioncontrol.cs#350)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#350](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/lightshapeselectioncontrol.vb#350)]

4. Dans l’**Explorateur de solutions**, cliquez sur le bouton **Afficher tous les fichiers**. Ouvrez le fichier LightShapeSelectionControl.Designer.cs ou LightShapeSelectionControl.Designer.vb et supprimez la définition par défaut de la <xref:System.ComponentModel.Component.Dispose%2A> (méthode).

5. Implémentez la propriété `LightShape`.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#360](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/lightshapeselectioncontrol.cs#360)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#360](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/lightshapeselectioncontrol.vb#360)]

6. Remplacez la méthode <xref:System.Windows.Forms.Control.OnPaint%2A> . Cette implémentation dessinera un carré rempli et un cercle. Elle sera également en surbrillance la valeur sélectionnée en dessinant une bordure autour d’une forme ou l’autre.

     [!code-csharp[System.Windows.Forms.Design.DocumentDesigner#380](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/CS/lightshapeselectioncontrol.cs#380)]
     [!code-vb[System.Windows.Forms.Design.DocumentDesigner#380](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Design.DocumentDesigner/VB/lightshapeselectioncontrol.vb#380)]

## <a name="testing-your-custom-control-in-the-designer"></a>Test de votre contrôle personnalisé dans le Concepteur

À ce stade, vous pouvez générer le `MarqueeControlLibrary` projet. Tester votre implémentation en créant un contrôle qui hérite de la `MarqueeControl` classe et l’utiliser sur un formulaire.

### <a name="to-create-a-custom-marqueecontrol-implementation"></a>Pour créer une implémentation personnalisée de MarqueeControl

1. Ouvrez `DemoMarqueeControl` dans le Concepteur Windows Forms. Cette opération crée une instance de la `DemoMarqueeControl` type et l’affiche dans une instance de la `MarqueeControlRootDesigner` type.

2. Dans le **boîte à outils**, ouvrez le **composants MarqueeControlLibrary** onglet. Vous verrez la `MarqueeBorder` et `MarqueeText` contrôles disponibles pour la sélection.

3. Faites glisser une instance de la `MarqueeBorder` contrôler sur le `DemoMarqueeControl` aire de conception. Ancrez ce `MarqueeBorder` vers le contrôle parent.

4. Faites glisser une instance de la `MarqueeText` contrôler sur le `DemoMarqueeControl` aire de conception.

5. Générez la solution.

6. Avec le bouton droit le `DemoMarqueeControl` et dans le menu contextuel, sélectionnez le **exécuter le Test** option pour démarrer l’animation. Cliquez sur **arrêter le Test** pour arrêter l’animation.

7. Ouvrez **Form1** en mode Création.

8. Placez deux <xref:System.Windows.Forms.Button> contrôles du formulaire. Nommez-les `startButton` et `stopButton`et modifier le <xref:System.Windows.Forms.Control.Text%2A> valeurs de propriété à **Démarrer** et **arrêter**, respectivement.

9. Implémentez <xref:System.Windows.Forms.Control.Click> gestionnaires d’événements pour les deux <xref:System.Windows.Forms.Button> contrôles.

10. Dans le **boîte à outils**, ouvrez le **Composants MarqueeControlTest** onglet. Vous verrez le `DemoMarqueeControl` disponibles pour la sélection.

11. Faites glisser une instance de `DemoMarqueeControl` sur le **Form1** aire de conception.

12. Dans le <xref:System.Windows.Forms.Control.Click> appeler des gestionnaires d’événements, le `Start` et `Stop` méthodes sur le `DemoMarqueeControl`.

```vb
Private Sub startButton_Click(sender As Object, e As System.EventArgs)
    Me.demoMarqueeControl1.Start()
End Sub 'startButton_Click

Private Sub stopButton_Click(sender As Object, e As System.EventArgs)
Me.demoMarqueeControl1.Stop()
End Sub 'stopButton_Click
```

```csharp
private void startButton_Click(object sender, System.EventArgs e)
{
    this.demoMarqueeControl1.Start();
}

private void stopButton_Click(object sender, System.EventArgs e)
{
    this.demoMarqueeControl1.Stop();
}
```

1. Définir le `MarqueeControlTest` projet comme projet de démarrage et l’exécuter. Vous verrez le formulaire contenant votre `DemoMarqueeControl`. Cliquez sur le **Démarrer** bouton pour démarrer l’animation. Vous devez voir le texte clignote et les lumières se déplacent autour de la bordure.

## <a name="next-steps"></a>Étapes suivantes

Le `MarqueeControlLibrary` illustre une implémentation simple de contrôles personnalisés et des concepteurs associés. Vous pouvez rendre cet exemple plus sophistiquées de plusieurs façons :

- Modifier les valeurs de propriété pour la `DemoMarqueeControl` dans le concepteur. Ajouter d’autres `MarqueBorder` contrôle et de les ancrer dans leurs instances parentes pour créer un effet imbriqué. Essayez d’utiliser des paramètres différents pour le `UpdatePeriod` et les propriétés liées à la lumière.

- Créez vos propres implémentations de `IMarqueeWidget`. Vous pouvez, par exemple, créer une clignotant « enseigne » ou un signe animé avec plusieurs images.

- Personnaliser davantage l’expérience au moment du design. Vous pouvez essayer plus de propriétés que l’occultation <xref:System.Windows.Forms.Control.Enabled%2A> et <xref:System.Windows.Forms.Control.Visible%2A>, et vous pouvez ajouter de nouvelles propriétés. Ajoutez de nouveaux verbes de concepteur pour simplifier les tâches courantes comme l’ancrage de contrôles enfants.

- Licence le `MarqueeControl`. Pour plus d'informations, voir [Procédure : Licence des composants et contrôles](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/fe8b1eh9(v=vs.120)).

- Contrôler la façon dont vos contrôles sont sérialisés et comment le code est généré pour eux. Pour plus d’informations, consultez [Compilation et génération de Code Source dynamique](../../reflection-and-codedom/dynamic-source-code-generation-and-compilation.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.UserControl>
- <xref:System.Windows.Forms.Design.ParentControlDesigner>
- <xref:System.Windows.Forms.Design.DocumentDesigner>
- <xref:System.ComponentModel.Design.IRootDesigner>
- <xref:System.ComponentModel.Design.DesignerVerb>
- <xref:System.Drawing.Design.UITypeEditor>
- <xref:System.ComponentModel.BackgroundWorker>
- [Guide pratique pour Créer un contrôle Windows Forms tire parti des fonctionnalités de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))
- [Extension de la prise en charge au moment du design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))
- [Concepteurs personnalisés](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/h51z5c0x(v=vs.120))
