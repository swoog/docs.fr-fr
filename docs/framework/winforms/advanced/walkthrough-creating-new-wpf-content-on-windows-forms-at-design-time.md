---
title: 'Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design'
ms.date: 08/18/2018
helpviewer_keywords:
- interoperability [Windows Forms], WPF and Windows Forms
- WPF content [Windows Forms], hosting in Windows Forms
- hosting WPF content in Windows Forms
- ElementHost control
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: 2e92d8e8-f0e4-4df7-9f07-2acf35cd798c
ms.openlocfilehash: ed48db399ba47f0e6be96f7bca33d3892b19e433
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707909"
---
# <a name="walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time"></a>Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design

Cette rubrique montre comment créer un contrôle Windows Presentation Foundation (WPF) pour une utilisation dans vos applications Windows Forms.

Au cours de cette procédure pas à pas, vous allez exécuter les tâches suivantes :

- créer le projet ;

- créer un projet WPF ;

- ajouter le nouveau contrôle WPF à un Windows Form. Le contrôle WPF est hébergé dans un contrôle <xref:System.Windows.Forms.Integration.ElementHost>.

## <a name="prerequisites"></a>Prérequis

Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :

- Visual Studio 2017

## <a name="creating-the-project"></a>Création du projet

La première étape consiste à créer le projet Windows Forms. Ouvrez Visual Studio et créez un nouveau **Windows Forms App (.NET Framework)** projet dans Visual Basic ou Visual c# nommé `HostingWpf`.

> [!NOTE]
> Lors de l'hébergement de contenu WPF, seuls les projets Visual Basic et C# sont pris en charge.

## <a name="creating-a-new-wpf-control"></a>Création d'un contrôle WPF

La création d'un contrôle WPF et son ajout à votre projet sont des tâches aussi simples que l'ajout de tout autre élément à votre projet. Le Concepteur de formulaires Windows fonctionne avec un type particulier de contrôle nommé *contrôle composite*, ou *contrôle utilisateur*. Pour plus d'informations sur les contrôles utilisateur WPF, consultez <xref:System.Windows.Controls.UserControl>.

> [!NOTE]
> Le type <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> pour WPF est distinct du type de contrôle utilisateur fourni par Windows Forms, également nommé <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>.

### <a name="to-create-a-new-wpf-control"></a>Pour créer un contrôle WPF

1. Dans **l’Explorateur de solutions**, ajoutez un nouveau **bibliothèque de contrôles utilisateur WPF (.NET Framework)** projet à la solution. Utilisez le nom par défaut pour la bibliothèque de contrôles, `WpfControlLibrary1`. Le nom du contrôle par défaut est `UserControl1.xaml`.

     Ajout du nouveau contrôle a les effets suivants :

    - Le fichier UserControl1.xaml est ajouté.

    - Le fichier UserControl1.xaml.cs ou UserControl1.xaml.vb est ajouté. Ce fichier contient le code-behind pour les gestionnaires d'événements et autre implémentation.

    - Les références aux assemblys WPF sont ajoutées.

    - Le fichier UserControl1.xaml s'ouvre dans le [!INCLUDE[wpfdesigner_current_long](../../../../includes/wpfdesigner-current-long-md.md)].

2. En mode Design, assurez-vous que `UserControl1` est sélectionné. Pour plus d'informations, voir [Procédure : Sélectionner et déplacer des éléments sur l’aire de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).

3. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à **200**.

4. À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> contrôle sur l’aire de conception.

5. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Controls.TextBox.Text%2A> propriété **le contenu hébergé**.

    > [!NOTE]
    > En général, vous devez héberger du contenu WPF plus sophistiqué. Le contrôle <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> est utilisé ici uniquement à titre d'illustration.

6. Générez le projet.

## <a name="adding-a-wpf-control-to-a-windows-form"></a>Ajout d'un contrôle WPF à un Windows Form

Votre nouveau contrôle WPF est prêt à être utilisé sur le formulaire. Windows Forms utilise le <xref:System.Windows.Forms.Integration.ElementHost> contrôle pour héberger le contenu WPF.

### <a name="to-add-a-wpf-control-to-a-windows-form"></a>Pour ajouter un contrôle WPF à un Windows Form

1. Ouvrez `Form1` dans le Concepteur Windows Forms.

2. Dans le **boîte à outils**, recherchez l’onglet **contrôles utilisateur WPF WPFUserControlLibrary**.

3. Faites glisser une instance de `UserControl1` sur le formulaire.

    - Un contrôle <xref:System.Windows.Forms.Integration.ElementHost> est créé automatiquement sur le formulaire pour héberger le contrôle WPF.

    - Le <xref:System.Windows.Forms.Integration.ElementHost> contrôle est nommé `elementHost1` et dans le **propriétés** fenêtre, vous pouvez voir son <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> propriété est définie sur **UserControl1**.

    - des références aux assemblys WPF sont ajoutées au projet.

    - Le contrôle `elementHost1` a un panneau de Smart Tags qui affiche les options d’hébergement disponibles.

4. Dans le **tâches ElementHost** panneau des balises actives, sélectionnez **ancrer dans le conteneur parent**.

5. Appuyez sur **F5** pour générer et exécuter l’application.

## <a name="next-steps"></a>Étapes suivantes

Windows Forms et WPF sont des technologies différentes, mais elles sont conçues pour interagir étroitement. Pour fournir l’apparence et le comportement dans vos applications plus riches, essayez ce qui suit :

- Hébergez un contrôle Windows Forms dans une page WPF. Pour plus d’informations, consultez [Procédure pas à pas : Hébergement d’un Windows contrôle Forms dans WPF](../../wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md).

- Appliquez des styles visuels Windows Forms à votre contenu WPF. Pour plus d'informations, voir [Procédure : Activer des Styles visuels dans une Application hybride](../../wpf/advanced/how-to-enable-visual-styles-in-a-hybrid-application.md).

- Modifiez le style de votre contenu WPF. Pour plus d’informations, consultez [Procédure pas à pas : Contenu WPF de style](walkthrough-styling-wpf-content.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Migration et interopérabilité](../../wpf/advanced/migration-and-interoperability.md)
- [Utilisation de contrôles WPF](using-wpf-controls.md)
- [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)
