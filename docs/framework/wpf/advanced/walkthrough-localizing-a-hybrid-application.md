---
title: "Procédure pas à pas : localisation d'une application hybride"
ms.date: 08/18/2018
helpviewer_keywords:
- localization [WPF interoperability]
- hybrid applications [WPF interoperability]
ms.assetid: fbc0c54e-930a-4c13-8e9c-27b83665010a
ms.openlocfilehash: 60e33f9f3ab767a6fd1d5489721fd2a82950155e
ms.sourcegitcommit: bd4fa78f5a46133efdead1bc692a9aa2811d7868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "42754445"
---
# <a name="walkthrough-localizing-a-hybrid-application"></a>Procédure pas à pas : localisation d'une application hybride

Cette procédure pas à pas vous indique comment localiser [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] éléments dans un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]-application hybride.

Cette procédure pas à pas décrit notamment les tâches suivantes :

-   Création de la [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] projet hôte.

-   Ajout de contenu localisable

-   Activation de la localisation

-   Assignation d’identificateurs de ressource

-   Utilisation de l’outil LocBaml pour produire un assembly satellite

Pour l’intégralité du code des tâches illustrées dans cette procédure pas à pas, consultez [localisation d’un exemple d’Application hybride](http://go.microsoft.com/fwlink/?LinkID=160015).

Quand vous aurez terminé, vous disposerez d’une application hybride localisée.

## <a name="prerequisites"></a>Prérequis

Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :

-   Visual Studio 2017

## <a name="creating-the-windows-forms-host-project"></a>Création du projet hôte Windows Forms

La première étape consiste à créer le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] application projet et ajoutez un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] élément avec le contenu que vous localiserez.

### <a name="to-create-the-host-project"></a>Pour créer le projet hôte

1.  Créer un **application WPF** projet nommé `LocalizingWpfInWf`. Pour plus d’informations, consultez [Comment : créer un projet d’application Windows](http://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa).

2.  Ajouter un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> élément appelé `SimpleControl` au projet.

3.  Utilisez le <xref:System.Windows.Forms.Integration.ElementHost> contrôle se place un `SimpleControl` élément sur le formulaire. Pour plus d’informations, consultez [procédure pas à pas : hébergement d’un contrôle Composite 3D de WPF dans les Windows Forms](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-3-d-wpf-composite-control-in-windows-forms.md).

## <a name="adding-localizable-content"></a>Ajout de contenu localisable

Ensuite, vous allez ajouter un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle label et définissez le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] du contenu d’élément comme une chaîne localisable.

### <a name="to-add-localizable-content"></a>Pour ajouter du contenu localisable

1.  Dans **l’Explorateur de solutions**, double-cliquez sur **SimpleControl.xaml** pour l’ouvrir dans le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].

2.  Définissez le contenu de la <xref:System.Windows.Controls.Button> contrôler avec le code suivant.

     [!code-xaml[LocalizingWpfInWf#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizingWpfInWf/CSharp/SimpleControl0.xaml#10)]

3.  Dans **l’Explorateur de solutions**, double-cliquez sur **Form1** pour l’ouvrir dans le Concepteur de formulaires Windows.

4.  Ouvrez le **boîte à outils** et double-cliquez sur **étiquette** pour ajouter un contrôle d’étiquette au formulaire. Affectez à sa propriété <xref:System.Windows.Forms.Control.Text%2A> la valeur `"Hello"`.

5.  Appuyez sur **F5** pour générer et exécuter l’application.

     Les deux le `SimpleControl` élément et le contrôle d’étiquette affichent le texte **« Hello »**.

## <a name="enabling-localization"></a>Activation de la localisation

Le Concepteur Windows Forms comprend des paramètres permettant d’activer la localisation dans un assembly satellite.

### <a name="to-enable-localization"></a>Pour activer la localisation

1.  Dans **l’Explorateur de solutions**, double-cliquez sur **Form1.cs** pour l’ouvrir dans le Concepteur de formulaires Windows.

2.  Dans le **propriétés** fenêtre, définissez la valeur de la forme **Localizable** propriété `true`.

3.  Dans le **propriétés** fenêtre, définissez la valeur de la **langage** propriété **Espagnol (Espagne)**.

4.  Dans le Concepteur Windows Forms, sélectionnez le contrôle d’étiquette.

5.  Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Control.Text%2A> propriété `"Hola"`.

     Un nouveau fichier de ressources nommé Form1.es-ES.resx est ajouté au projet.

6.  Dans **l’Explorateur de solutions**, avec le bouton droit **Form1.cs** et cliquez sur **afficher le Code** pour l’ouvrir dans l’éditeur de Code.

7.  Copiez le code suivant dans le `Form1` constructeur, avant l’appel à `InitializeComponent`.

     [!code-csharp[LocalizingWpfInWf#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizingWpfInWf/CSharp/Form1.cs#2)]

8.  Dans **l’Explorateur de solutions**, avec le bouton droit **LocalizingWpfInWf** et cliquez sur **décharger le projet**.

     Le nom du projet est étiqueté **(non disponible)**.

9. Avec le bouton droit **LocalizingWpfInWf**, puis cliquez sur **Modifier LocalizingWpfInWf.csproj**.

     Le fichier projet s’ouvre dans l’éditeur de code.

10. Copiez la ligne suivante dans la première `PropertyGroup` dans le fichier projet.

    ```xml
    <UICulture>en-US</UICulture>
    ```

11. Enregistrez, puis fermez le fichier projet.

12. Dans **l’Explorateur de solutions**, avec le bouton droit **LocalizingWpfInWf** et cliquez sur **recharger le projet**.

## <a name="assigning-resource-identifiers"></a>Assignation d’identificateurs de ressource

Vous pouvez mapper votre contenu localisable à des assemblys de ressources en utilisant des identificateurs de ressource. L’application MsBuild.exe assigne automatiquement des identificateurs de ressource lorsque vous spécifiez la `updateuid` option.

### <a name="to-assign-resource-identifiers"></a>Pour assigner des identificateurs de ressource

1.  Dans le Menu Démarrer, ouvrez l’invite de commandes Visual Studio.

2.  Utilisez la commande suivante pour assigner des identificateurs de ressource à votre contenu localisable.

    ```
    msbuild /t:updateuid LocalizingWpfInWf.csproj
    ```

3.  Dans **l’Explorateur de solutions**, double-cliquez sur **SimpleControl.xaml** pour l’ouvrir dans l’éditeur de Code. Vous verrez que le `msbuild` commande a ajouté le `Uid` à tous les éléments d’attribut. Cela facilite la localisation par l’assignation des identificateurs de ressource.

     [!code-xaml[LocalizingWpfInWf#20](../../../../samples/snippets/csharp/VS_Snippets_Wpf/LocalizingWpfInWf/CSharp/SimpleControl.xaml#20)]

4.  Appuyez sur **F6** pour générer la solution.

## <a name="using-locbaml-to-produce-a-satellite-assembly"></a>Utilisation de LocBaml pour produire un assembly satellite

Votre contenu localisé est stocké dans une ressource uniquement *assembly satellite*. Utilisez l’outil de ligne de commande LocBaml.exe pour produire un assembly localisé pour votre [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contenu.

### <a name="to-produce-a-satellite-assembly"></a>Pour produire un assembly satellite

1.  Copiez LocBaml.exe dans le dossier obj\Debug de votre projet. Pour plus d’informations, consultez [localiser une Application](../../../../docs/framework/wpf/advanced/how-to-localize-an-application.md).

2.  Dans la fenêtre d’invite de commandes, utilisez la commande suivante pour extraire les chaînes de ressources dans un fichier temporaire.

    ```
    LocBaml /parse LocalizingWpfInWf.g.en-US.resources /out:temp.csv
    ```

3.  Ouvrez le fichier temp.csv avec Visual Studio ou un autre éditeur de texte. Remplacez la chaîne `"Hello"` avec sa traduction en espagnol, `"Hola"`.

4.  Enregistrez le fichier temp.csv.

5.  Utilisez la commande suivante pour générer le fichier de ressources localisé.

    ```
    LocBaml /generate /trans:temp.csv LocalizingWpfInWf.g.en-US.resources /out:. /cul:es-ES
    ```

     Le fichier LocalizingWpfInWf.g.es-ES.resources est créé dans le dossier obj\Debug.

6.  Utilisez la commande suivante pour générer l’assembly satellite localisé.

    ```
    Al.exe /out:LocalizingWpfInWf.resources.dll /culture:es-ES /embed:LocalizingWpfInWf.Form1.es-ES.resources /embed:LocalizingWpfInWf.g.es-ES.resources
    ```

     Le fichier LocalizingWpfInWf.resources.dll est créé dans le dossier obj\Debug.

7.  Copiez le fichier LocalizingWpfInWf.resources.dll dans le dossier du projet bin\Debug\es-ES. Remplacez le fichier existant.

8.  Exécutez LocalizingWpfInWf.exe, qui se trouve dans le dossier bin\Debug de votre projet. Ne regénérez pas l’application, car cela aura pour effet de remplacer l’assembly satellite.

     L’application affiche les chaînes localisées au lieu des chaînes en anglais.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Localiser une application](../../../../docs/framework/wpf/advanced/how-to-localize-an-application.md)
- [Procédure pas à pas : Localisation de Windows Forms](http://msdn.microsoft.com/library/9a96220d-a19b-4de0-9f48-01e5d82679e5)
- [Concepteur WPF](http://msdn.microsoft.com/library/c6c65214-8411-4e16-b254-163ed4099c26)