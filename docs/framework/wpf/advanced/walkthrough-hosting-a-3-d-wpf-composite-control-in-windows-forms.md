---
title: 'Procédure pas à pas : Hébergement d’un contrôle Composite 3-d WPF dans les Windows Forms'
ms.date: 08/18/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosting WPF content in Windows Forms [WPF]
- composite controls [WPF], hosting WPF in
ms.assetid: 486369a9-606a-4a3b-b086-a06f2119c7b0
ms.openlocfilehash: b1bd003c6a408e7455bb5c45e1f34a740fce67d1
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57367438"
---
# <a name="walkthrough-hosting-a-3-d-wpf-composite-control-in-windows-forms"></a>Procédure pas à pas : Hébergement d’un contrôle Composite 3-d WPF dans les Windows Forms

Cette procédure pas à pas montre comment vous pouvez créer un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] composite contrôler et l’héberger dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles et formulaires à l’aide de la <xref:System.Windows.Forms.Integration.ElementHost> contrôle.

Dans cette procédure pas à pas, vous allez implémenter un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> qui contient deux contrôles enfants. Le <xref:System.Windows.Controls.UserControl> affiche un cône tridimensionnel (3D). Le rendu d’objets 3D est beaucoup plus facile avec le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] qu’avec [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]. Par conséquent, il est judicieux pour héberger un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl> classe pour créer des graphiques 3D dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)].

Cette procédure pas à pas décrit notamment les tâches suivantes :

-   Création de la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.

-   Création du projet hôte Windows Forms.

-   Hébergement du [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Controls.UserControl>.

## <a name="prerequisites"></a>Prérequis

Pour exécuter cette procédure pas à pas, vous devez disposer des composants suivants :

-   Visual Studio 2017

<a name="To_Create_the_UserControl"></a>
## <a name="create-the-usercontrol"></a>Créer le UserControl

1.  Créer un **bibliothèque de contrôles utilisateur WPF** projet nommé `HostingWpfUserControlInWf`.

2.  Ouvrez UserControl1.xaml dans le [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].

3.  Remplacez le code généré par le code suivant :

     [!code-xaml[HostingWpfUserControlInWf#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HostingWpfUserControlInWf/CSharp/HostingWpfUserControlInWf/ConeControl.xaml#1)]

     Ce code définit un <xref:System.Windows.Controls.UserControl?displayProperty=nameWithType> qui contient deux contrôles enfants. Le premier contrôle enfant est un <xref:System.Windows.Controls.Label?displayProperty=nameWithType> contrôle ; le second est un <xref:System.Windows.Controls.Viewport3D> contrôle qui affiche un cône 3D.

<a name="To_Create_the_Windows_Forms_Host_Project"></a>
## <a name="create-the-host-project"></a>Créer le projet hôte

1.  Ajouter un **application WPF (.NET Framework)** projet nommé `WpfUserControlHost` à la solution. Pour plus d’informations, consultez [Procédure pas à pas : Ma première application de bureau WPF](../getting-started/walkthrough-my-first-wpf-desktop-application.md).

2.  Dans **l’Explorateur de solutions**, ajoutez une référence à l’assembly WindowsFormsIntegration, nommé WindowsFormsIntegration.dll.

3.  Ajouter des références à ce qui suit [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] assemblys :

    -   PresentationCore

    -   PresentationFramework

    -   WindowsBase

4.  Ajoutez au projet une référence à `HostingWpfUserControlInWf`.

5.  Dans l’Explorateur de solutions, définissez le `WpfUserControlHost` projet comme projet de démarrage.

<a name="To_Host_the_Windows_Presentation_Foundation"></a>
## <a name="host-the-usercontrol"></a>Héberger le contrôle utilisateur

1.  Dans le Concepteur de formulaires Windows, ouvrez Form1.

2.  Dans la fenêtre Propriétés, cliquez sur **événements**, puis double-cliquez sur le <xref:System.Windows.Forms.Form.Load> événement pour créer un gestionnaire d’événements.

     Ouvre l’éditeur de Code nouvellement généré `Form1_Load` Gestionnaire d’événements.

3.  Remplacez le code dans Form1.cs par le code suivant.

     Le `Form1_Load` Gestionnaire d’événements crée une instance de `UserControl1` et ajoute ses le <xref:System.Windows.Forms.Integration.ElementHost> collection de contrôles enfants du contrôle. Le <xref:System.Windows.Forms.Integration.ElementHost> contrôle est ajouté à la collection du formulaire des contrôles enfants.

     [!code-csharp[HostingWpfUserControlInWf#10](~/samples/snippets/csharp/VS_Snippets_Wpf/HostingWpfUserControlInWf/CSharp/WpfUserControlHost/Form1.cs#10)]
     [!code-vb[HostingWpfUserControlInWf#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HostingWpfUserControlInWf/VisualBasic/WpfUserControlHost/Form1.vb#10)]

4.  Appuyez sur **F5** pour générer et exécuter l’application.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)
- [Procédure pas à pas : Hébergement d’un contrôle Composite WPF dans les Windows Forms](walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
- [Procédure pas à pas : Hébergement d’un contrôle Composite de formulaires Windows dans WPF](walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)
- [Hébergement d’un contrôle Composite WPF dans Windows Forms, exemple](https://go.microsoft.com/fwlink/?LinkID=160001)