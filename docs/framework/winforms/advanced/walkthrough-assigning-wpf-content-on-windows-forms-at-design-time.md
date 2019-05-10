---
title: 'Procédure pas à pas : Attribution de contenu WPF dans Windows Forms au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- WPF content [Windows Forms], assigning at design time
- ElementHost control [Windows Forms], assigning WPF content at design time
- interoperability [WPF]
- Windows Forms, content assignments
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: b3e9ef93-7e0f-4a2f-8f1e-3437609a1eb7
ms.openlocfilehash: 09427bfc836f40ca9c7aa76f4904bfe7083bf8dc
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211235"
---
# <a name="walkthrough-assign-wpf-content-on-windows-forms-at-design-time"></a>Procédure pas à pas : Assigner un contenu WPF dans les Windows Forms au moment du design

Cette procédure pas à pas montre comment sélectionner les types de contrôle WPF (Windows Presentation Foundation) que vous souhaitez afficher sur votre formulaire. Vous pouvez sélectionner tout type de contrôle WPF inclus dans votre projet.

Lors de cette procédure pas à pas, vous allez exécuter les tâches suivantes :

- créer le projet ;

- créer les types de contrôles WPF ;

- sélectionner les contrôles WPF.

## <a name="prerequisites"></a>Prérequis

Cette procédure pas à pas nécessite Visual Studio.

## <a name="create-the-project"></a>Créer le projet

Ouvrez Visual Studio et créez un nouveau projet d’Application de Windows Forms dans Visual Basic ou Visual C# nommé `SelectingWpfContent`.

> [!NOTE]
> Lors de l'hébergement de contenu WPF, seuls les projets Visual Basic et C# sont pris en charge.

## <a name="create-the-wpf-control-types"></a>Créer des types de contrôles WPF

Après avoir ajouté des types de contrôles WPF au projet, vous pouvez les héberger dans différents contrôles <xref:System.Windows.Forms.Integration.ElementHost>.

## <a name="create-wpf-control-types"></a>Créer des types de contrôles WPF

1. Ajoutez un nouveau projet <xref:System.Windows.Controls.UserControl> WPF à la solution. Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`. Pour plus d’informations, consultez [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).

2. En mode Design, assurez-vous que `UserControl1` est sélectionné. Pour plus d'informations, voir [Procédure : Sélectionner et déplacer des éléments sur l’aire de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).

3. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à `200`.

4. Ajouter un <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> le contrôle à la <xref:System.Windows.Controls.UserControl> et définissez la valeur de la <xref:System.Windows.Controls.TextBox.Text%2A> propriété **le contenu hébergé**.

5. Ajoutez un deuxième <xref:System.Windows.Controls.UserControl> WPF au projet. Utilisez le nom par défaut pour le type de contrôle, `UserControl2.xaml`.

6. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à `200`.

7. Ajouter un <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> le contrôle à la <xref:System.Windows.Controls.UserControl> et définissez la valeur de la <xref:System.Windows.Controls.TextBox.Text%2A> propriété **contenu hébergé 2**.

 **Remarque** en général, vous devez héberger le contenu WPF plus sophistiqué. Le contrôle <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> est utilisé ici uniquement à titre d'illustration.

1. Générez le projet.

## <a name="select-wpf-controls"></a>Sélectionner les contrôles WPF

Vous pouvez assigner du contenu WPF différent à un contrôle <xref:System.Windows.Forms.Integration.ElementHost> qui héberge déjà du contenu.

1. Ouvrez `Form1` dans le Concepteur Windows Forms.

2. Dans le **boîte à outils**, double-cliquez sur `UserControl1` pour créer une instance de `UserControl1` sur le formulaire.

     Une instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.

3. Dans le panneau des balises actives pour `elementHost1`, ouvrez le **sélectionner le contenu hébergé** liste déroulante.

4. Sélectionnez **UserControl2** dans la zone de liste déroulante.

     Le contrôle `elementHost1` héberge maintenant une instance du type `UserControl2`.

5. Dans le **propriétés** fenêtre, vérifiez que le <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> propriété est définie sur **UserControl2**.

6. À partir de la **boîte à outils**, dans le **interopérabilité WPF** de groupe, faites glisser un <xref:System.Windows.Forms.Integration.ElementHost> contrôle vers le formulaire.

     Le nom par défaut du nouveau contrôle est `elementHost2`.

7. Dans le panneau des balises actives pour `elementHost2`, ouvrez le **sélectionner le contenu hébergé** liste déroulante.

8. Sélectionnez **UserControl1** dans la liste déroulante.

9. Le contrôle `elementHost2` héberge maintenant une instance du type `UserControl1`.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Migration et interopérabilité](../../wpf/advanced/migration-and-interoperability.md)
- [Utilisation de contrôles WPF](using-wpf-controls.md)
- [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)
