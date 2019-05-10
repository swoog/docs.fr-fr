---
title: 'Procédure pas à pas : organiser le contenu WPF dans Windows Forms au moment du design'
ms.date: 03/30/2017
helpviewer_keywords:
- WPF user control [Windows Forms], hosting in a layout panel
- WPF content [Windows Forms], arranging at design time
- Windows Forms, arranging WPF content at design time
- WPF content [Windows Forms], hosting in Windows Forms
- Windows Forms, anchoring and docking WPF content
- interoperability [WPF]
ms.assetid: 5efb1c53-1484-43d6-aa8a-f4861b99bb8a
ms.openlocfilehash: a8f690438136450cb12dbcf5e17ddfcca617457e
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211445"
---
# <a name="walkthrough-arrange-wpf-content-on-windows-forms-at-design-time"></a>Procédure pas à pas : Organiser le contenu WPF sur les Windows Forms au moment du design

Cette procédure pas à pas montre comment utiliser les fonctionnalités de disposition Windows Forms, telles que l'ancrage et les lignes d'alignement, pour disposer les contrôles WPF (Windows Presentation Foundation).

Lors de cette procédure pas à pas, vous allez exécuter les tâches suivantes :

- créer le projet ;

- créer le contrôle WPF ;

- héberger des contrôles WPF dans un panneau de disposition ;

- utiliser des lignes d'alignement pour aligner des contrôles WPF ;

- ancrer des contrôles WPF.

## <a name="prerequisites"></a>Prérequis

Cette procédure pas à pas nécessite Visual Studio.

## <a name="create-the-project"></a>Créer le projet

Ouvrez Visual Studio et créez un nouveau projet d’Application de Windows Forms dans Visual Basic ou Visual C# nommé `ArrangeElementHost`.

> [!NOTE]
> Lors de l'hébergement de contenu WPF, seuls les projets Visual Basic et C# sont pris en charge.

## <a name="create-the-wpf-control"></a>Créer le contrôle WPF

Après avoir ajouté un contrôle WPF au projet, vous pouvez le disposer sur le formulaire.

1. Ajoutez un nouveau <xref:System.Windows.Controls.UserControl> WPF au projet. Utilisez le nom par défaut pour le type de contrôle, `UserControl1.xaml`. Pour plus d’informations, consultez [Procédure pas à pas : Création de contenu WPF dans les Windows Forms au moment du Design](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).

2. En mode Design, assurez-vous que `UserControl1` est sélectionné. Pour plus d'informations, voir [Procédure : Sélectionner et déplacer des éléments sur l’aire de conception](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/bb514527(v=vs.100)).

3. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.FrameworkElement.Width%2A> et <xref:System.Windows.FrameworkElement.Height%2A> propriétés à `200`.

4. Affectez à la propriété <xref:System.Windows.Controls.Control.Background%2A> la valeur `Blue`.

5. Générez le projet.

## <a name="hosting-wpf-controls-in-a-layout-panel"></a>Hébergement de contrôles WPF dans un panneau de disposition
 Vous pouvez utiliser des contrôles WPF dans des panneaux de disposition de la même façon que vous utilisez d'autres contrôles Windows Forms.

#### <a name="to-host-wpf-controls-in-a-layout-panel"></a>Pour héberger des contrôles WPF dans un panneau de disposition

1. Ouvrez `Form1` dans le Concepteur Windows Forms.

2. Dans le **boîte à outils**, faites glisser un <xref:System.Windows.Forms.TableLayoutPanel> contrôle vers le formulaire.

3. Sur le <xref:System.Windows.Forms.TableLayoutPanel> panneau des balises actives du contrôle, sélectionnez **supprimer la dernière ligne**.

4. Augmentez la largeur et la hauteur du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.

5. Dans le **boîte à outils**, double-cliquez sur `UserControl1` pour créer une instance de `UserControl1` dans la première cellule de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.

     L'instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost1`.

6. Dans le **boîte à outils**, double-cliquez sur `UserControl1` pour créer une autre instance dans la deuxième cellule de la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.

7. Dans le **structure du Document** fenêtre, sélectionnez `tableLayoutPanel1`. Pour plus d’informations, consultez [fenêtre Structure du Document](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/46xf4h0w(v=vs.100)#using-the-document-outline-window-for-silverlight-and-wpf).

8. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Control.Padding%2A> propriété `10, 10, 10, 10`.

     Les deux contrôles <xref:System.Windows.Forms.Integration.ElementHost> sont redimensionnés pour s'adapter à la nouvelle disposition.

## <a name="using-snaplines-to-align-wpf-controls"></a>Utilisation de lignes d'alignement pour aligner des contrôles WPF
 Les lignes d'alignement permettent d'aligner facilement les contrôles sur un formulaire. Vous pouvez aussi utiliser des lignes d'alignement pour aligner vos contrôles WPF. Pour plus d’informations, consultez [Procédure pas à pas : Organisation des contrôles dans les Windows Forms à l’aide des lignes d’alignement](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).

#### <a name="to-use-snaplines-to-align-wpf-controls"></a>Pour utiliser des lignes d'alignement pour aligner des contrôles WPF

1. À partir de la **boîte à outils**, faites glisser une instance de `UserControl1` vers le formulaire et placez-le dans l’espace sous le <xref:System.Windows.Forms.TableLayoutPanel> contrôle.

     L'instance de `UserControl1` est hébergée dans un nouveau contrôle <xref:System.Windows.Forms.Integration.ElementHost> nommé `elementHost3`.

2. À l'aide des lignes d'alignement, alignez le bord gauche de `elementHost3` avec le bord gauche du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.

3. À l'aide des lignes d'alignement, affectez à `elementHost3` la même largeur que celle du contrôle <xref:System.Windows.Forms.TableLayoutPanel>.

4. Déplacez `elementHost3` vers le contrôle <xref:System.Windows.Forms.TableLayoutPanel> jusqu'à ce qu'une ligne d'alignement centrale apparaisse entre les contrôles.

5. Dans le **propriétés** fenêtre, définissez la valeur de la propriété de marge à `20, 20, 20, 20`.

6. Déplacez le `elementHost3` hors du contrôle <xref:System.Windows.Forms.TableLayoutPanel> jusqu'à ce que la ligne d'alignement centrale réapparaisse. La ligne d'alignement centrale indique maintenant une marge de 20.

7. Déplacez `elementHost3` vers la droite jusqu'à ce que son bord gauche soit aligné avec le bord gauche de `elementHost1`.

8. Modifiez la largeur de `elementHost3` jusqu'à ce que son bord droit soit aligné avec le bord droit de `elementHost2`.

## <a name="anchoring-and-docking-wpf-controls"></a>Ancrage de contrôles WPF
 Un contrôle WPF hébergé sur un formulaire a le même comportement d'ancrage que d'autres contrôles Windows Forms.

#### <a name="to-anchor-and-dock-wpf-controls"></a>Pour ancrer des contrôles WPF

1. Sélectionnez `elementHost1`.

2. Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.Control.Anchor%2A> propriété **Top, Bottom, Left, Right**.

3. Agrandissez le contrôle <xref:System.Windows.Forms.TableLayoutPanel>.

     Le contrôle `elementHost1` est redimensionné pour remplir la cellule.

4. Sélectionnez `elementHost2`.

5. Dans le **propriétés** fenêtre, définissez la valeur de la <xref:System.Windows.Forms.Control.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill>.

     Le contrôle `elementHost2` est redimensionné pour remplir la cellule.

6. Sélectionnez le contrôle <xref:System.Windows.Forms.TableLayoutPanel>.

7. Affectez à sa propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Top>.

8. Sélectionnez `elementHost3`.

9. Affectez à sa propriété <xref:System.Windows.Forms.Control.Dock%2A> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.

     Le contrôle `elementHost3` est redimensionné pour remplir l'espace restant sur le formulaire.

10. Redimensionnez le formulaire.

     Les trois contrôles <xref:System.Windows.Forms.Integration.ElementHost> sont redimensionnés correctement.

     Pour plus d'informations, voir [Procédure : Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Guide pratique pour Ancrer et arrimer des contrôles enfants dans un contrôle TableLayoutPanel](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [Guide pratique pour Aligner un contrôle sur les bords des formulaires au moment du Design](../controls/how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)
- [Procédure pas à pas : Organisation des contrôles dans les formulaires de Windows à l’aide des lignes d’alignement](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [Migration et interopérabilité](../../wpf/advanced/migration-and-interoperability.md)
- [Utilisation de contrôles WPF](using-wpf-controls.md)
- [Concevoir en XAML dans Visual Studio](/visualstudio/designers/designing-xaml-in-visual-studio)
