---
title: 'Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- debugging [Visual Studio], walkthroughs
- custom controls [Windows Forms], walkthroughs
- visual editors
- debugging [Visual Studio], Windows Forms
- custom controls [Windows Forms], debugging
- designers
- controls [Windows Forms], debugging
- walkthroughs [Windows Forms], debugging
- design-time debugging
ms.assetid: 1fd83ccd-3798-42fc-85a3-6cba99467387
ms.openlocfilehash: db6266f30c4fb62364f3c40a75a4a11ef853c1cb
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59325356"
---
# <a name="walkthrough-debugging-custom-windows-forms-controls-at-design-time"></a>Procédure pas à pas : débogage des contrôles Windows Forms personnalisés au moment du design
Lorsque vous créez un contrôle personnalisé, vous trouverez souvent il nécessaires pour déboguer son comportement au moment du design. Cela est particulièrement vrai si vous créez un concepteur personnalisé pour votre contrôle personnalisé. Pour plus d’informations, consultez [procédure pas à pas : Création d’un Windows Forms de contrôle qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md).  
  
 Vous pouvez déboguer vos contrôles personnalisés à l’aide de Visual Studio, simplement comme pour toutes les autres classes .NET Framework. La différence est que vous devez déboguer une instance distincte de Visual Studio qui exécute le code de votre contrôle personnalisé  
  
 Cette procédure pas à pas décrit notamment les tâches suivantes :  
  
-   Création d’un projet Windows Forms pour héberger votre contrôle personnalisé  
  
-   Création d’un projet de bibliothèque de contrôle  
  
-   Ajout d’une propriété à votre contrôle personnalisé  
  
-   Ajout de votre contrôle personnalisé au formulaire hôte  
  
-   Configuration du projet pour le débogage au moment du design  
  
-   Débogage de votre contrôle personnalisé au moment du design  
  
 Lorsque vous avez terminé, vous devez comprendre les tâches nécessaires pour déboguer le comportement au moment du design d’un contrôle personnalisé.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
## <a name="creating-the-project"></a>Création du projet  
 La première étape consiste à créer le projet d’application. Vous utiliserez ce projet pour générer l’application qui héberge le contrôle personnalisé.  
  
#### <a name="to-create-the-project"></a>Pour créer le projet  
  
-   Créer un projet d’Application de Windows appelé « DebuggingExample » (**fichier** > **New** > **projet**  >  **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).  
  
## <a name="creating-a-control-library-project"></a>Création d’un projet de bibliothèque de contrôle  
 L’étape suivante consiste à créer le projet de bibliothèque de contrôle et de configurer le contrôle personnalisé.  
  
#### <a name="to-create-the-control-library-project"></a>Pour créer le projet de bibliothèque de contrôle  
  
1. Ajouter un **bibliothèque de contrôles Windows** projet à la solution.  
  
2. Ajouter un nouveau **UserControl** élément au projet DebugControlLibrary. Pour plus d’informations, consultez [Guide pratique pour Ajouter de nouveaux éléments de projet](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)). Nommez le nouveau fichier source une base « DebugControl ».  
  
3. À l’aide de la **l’Explorateur de solutions**, supprimer le contrôle du projet par défaut en supprimant le fichier de code avec un nom de base «`UserControl1`». Pour plus d’informations, consultez [Guide pratique pour Supprimer, suppression et exclure des éléments](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).  
  
4. Générez la solution.  
  
## <a name="checkpoint"></a>Point de contrôle  
 À ce stade, vous serez en mesure de voir votre contrôle personnalisé dans le **boîte à outils**.  
  
#### <a name="to-check-your-progress"></a>Pour vérifier votre progression  
  
-   Recherchez le nouvel onglet appelé **Composants DebugControlLibrary** et cliquez sur pour le sélectionner. Quand il s’ouvre, vous verrez votre contrôle répertorié comme **DebugControl** avec l’icône par défaut en regard de celle-ci.  
  
## <a name="adding-a-property-to-your-custom-control"></a>Ajout d’une propriété à votre contrôle personnalisé  
 Pour montrer que le code de votre contrôle personnalisé s’exécute au moment du design, vous ajoutez une propriété et définissez un point d’arrêt dans le code qui implémente la propriété.  
  
#### <a name="to-add-a-property-to-your-custom-control"></a>Pour ajouter une propriété à votre contrôle personnalisé  
  
1. Ouvrez **DebugControl** dans le **éditeur de Code**. Ajoutez le code suivant à la définition de classe :  
  
    ```vb  
    Private demoStringValue As String = Nothing  
    <BrowsableAttribute(true)>  
    Public Property DemoString() As String  
  
        Get  
            Return Me.demoStringValue  
        End Get  
  
        Set(ByVal value As String)  
            Me.demoStringValue = value  
        End Set  
  
    End Property  
    ```  
  
    ```csharp  
    private string demoStringValue = null;  
    [Browsable(true)]  
    public string DemoString  
    {  
        get  
        {  
            return this.demoStringValue;  
        }  
        set  
        {  
            demoStringValue = value;  
        }  
    }  
    ```  
  
2. Générez la solution.  
  
## <a name="adding-your-custom-control-to-the-host-form"></a>Ajout de votre contrôle personnalisé au formulaire hôte  
 Pour déboguer le comportement au moment du design de votre contrôle personnalisé, vous devez placer une instance de la classe de contrôle personnalisé sur un formulaire hôte.  
  
#### <a name="to-add-your-custom-control-to-the-host-form"></a>Pour ajouter votre contrôle personnalisé au formulaire hôte  
  
1. Dans le projet « DebuggingExample », ouvrez Form1 dans le **Windows Forms Designer**.  
  
2. Dans le **boîte à outils**, ouvrez le **Composants DebugControlLibrary** onglet et faites glisser un **DebugControl** instance vers le formulaire.  
  
3. Rechercher la `DemoString` propriété personnalisée dans le **propriétés** fenêtre. Notez que vous pouvez modifier sa valeur comme vous le feriez pour toute autre propriété. Notez également que lorsque la `DemoString` propriété est sélectionnée, la chaîne de la propriété description s’affiche en bas de la **propriétés** fenêtre.  
  
## <a name="setting-up-the-project-for-design-time-debugging"></a>Configuration du projet pour le débogage au moment du Design  
 Pour déboguer le comportement au moment du design de votre contrôle personnalisé, vous allez déboguer une instance distincte de Visual Studio qui exécute le code de votre contrôle personnalisé.  
  
#### <a name="to-set-up-the-project-for-design-time-debugging"></a>Pour configurer le projet pour le débogage au moment du design  
  
1. Avec le bouton droit sur le **DebugControlLibrary** de projet dans le **l’Explorateur de solutions** et sélectionnez **propriétés**.  
  
2. Dans le **DebugControlLibrary** feuille de propriétés, sélectionnez le **déboguer** onglet.  
  
     Dans le **Action de démarrage** section, sélectionnez **démarrer le programme externe**. Vous serez le débogage d’une instance distincte de Visual Studio, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) pour le rechercher l’IDE Visual Studio. Le nom du fichier exécutable est **devenv.exe**, et si vous avez installé à l’emplacement par défaut, son chemin d’accès est %programfiles%\Microsoft Visual Studio 9.0\Common7\IDE\devenv.exe.  
  
3. Cliquez sur **OK** pour fermer la boîte de dialogue.  
  
4. Avec le bouton droit le **DebugControlLibrary** de projet et sélectionnez **définir comme projet de démarrage** pour activer cette configuration de débogage.  
  
## <a name="debugging-your-custom-control-at-design-time"></a>Débogage de votre contrôle personnalisé au moment du Design  
 Vous êtes maintenant prêt à déboguer votre contrôle personnalisé en cours d’exécution en mode Création. Lorsque vous démarrez la session de débogage, une nouvelle instance de Visual Studio sera créée, et vous allez l’utiliser pour charger la solution « DebuggingExample ». Lorsque vous ouvrez Form1 dans le **Concepteur Forms**, une instance de votre contrôle personnalisé est créée et commence à s’exécuter.  
  
#### <a name="to-debug-your-custom-control-at-design-time"></a>Pour déboguer votre contrôle personnalisé au moment du design  
  
1. Ouvrir le **DebugControl** fichier source dans le **éditeur de Code** et placer un point d’arrêt sur la `Set` l’accesseur de la `DemoString` propriété.  
  
2. Appuyez sur F5 pour démarrer la session de débogage. Notez qu’une nouvelle instance de Visual Studio est créée. Vous pouvez faire la distinction entre les instances de deux manières :  
  
    -   L’instance de débogage a le mot **en cours d’exécution** dans sa barre de titre  
  
    -   L’instance de débogage a le **Démarrer** bouton sur son **déboguer** barre d’outils désactivé  
  
     Votre point d’arrêt est défini dans l’instance de débogage.  
  
3. Dans la nouvelle instance de Visual Studio, ouvrez la solution « DebuggingExample ». Vous pouvez facilement trouver la solution en sélectionnant **projets récents** à partir de la **fichier** menu. Le fichier de solution « DebuggingExample.sln » apparaît comme étant le dernier fichier utilisé.  
  
4. Ouvrez Form1 dans le **Concepteur Forms** et sélectionnez le **DebugControl** contrôle.  
  
5. Modifiez la valeur de la propriété `DemoString` . Notez que lorsque vous validez la modification, l’instance de débogage de Visual Studio acquiert le focus et l’exécution s’arrête au point d’arrêt. Vous pouvez pas dans l’accesseur de propriété comme votre serait tout autre code.  
  
6. Lorsque vous avez terminé de votre session de débogage, vous pouvez quitter en fermant l’instance hébergée de Visual Studio ou en cliquant sur le **arrêter le débogage** bouton dans l’instance de débogage.  
  
## <a name="next-steps"></a>Étapes suivantes  
 Maintenant que vous pouvez déboguer vos contrôles personnalisés au moment du design, il existe de nombreuses possibilités pour le développement d’interaction de votre contrôle avec l’IDE Visual Studio.  
  
-   Vous pouvez utiliser la <xref:System.ComponentModel.Component.DesignMode%2A> propriété de la <xref:System.ComponentModel.Component> classe pour écrire du code qui s’exécutera seulement au moment du design. Pour plus d'informations, consultez <xref:System.ComponentModel.Component.DesignMode%2A>.  
  
-   Il existe plusieurs attributs que vous pouvez appliquer aux propriétés de votre contrôle pour manipuler l’interaction de votre contrôle personnalisé avec le concepteur. Vous pouvez trouver ces attributs dans le <xref:System.ComponentModel?displayProperty=nameWithType> espace de noms.  
  
-   Vous pouvez écrire un concepteur personnalisé pour votre contrôle personnalisé. Cela vous donne un contrôle complet sur l’expérience de conception à l’aide de l’infrastructure du concepteur extensible exposée par Visual Studio. Pour plus d’informations, consultez [procédure pas à pas : Création d’un Windows Forms de contrôle qui tire parti des fonctionnalités au moment du Design de Visual Studio](creating-a-wf-control-design-time-features.md).  
  
## <a name="see-also"></a>Voir aussi

- [Procédure pas à pas : création d’un contrôle Windows Forms qui tire parti des fonctionnalités au moment du design de Visual Studio](creating-a-wf-control-design-time-features.md)
- [Procédure : Services d’accès au moment du Design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171822(v=vs.120))
- [Procédure : Prise en charge d’accès au moment du Design dans les Windows Forms](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171827(v=vs.120))
