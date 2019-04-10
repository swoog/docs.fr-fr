---
title: 'Procédure : créer une interface de style Explorateur Windows dans un formulaire Windows'
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Explorer [Windows Forms], creating with Windows Forms
- SplitContainer control [Windows Forms], Explorer-style interface
- forms [Windows Forms], Windows Explorer type
ms.assetid: 9a3d5f4f-5dda-4350-9ad5-57ce5976dc47
ms.openlocfilehash: dd70feaba29e29748ac56729632fa359582a6914
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59327371"
---
# <a name="how-to-create-a-windows-explorerstyle-interface-on-a-windows-form"></a>Procédure : créer une interface de style Explorateur Windows dans un formulaire Windows
L’Explorateur Windows est un choix d’interface utilisateur commune pour les applications en raison de son caractère familier.  
  
 L’Explorateur Windows est, fondamentalement, un <xref:System.Windows.Forms.TreeView> contrôle et un <xref:System.Windows.Forms.ListView> contrôle sur des panneaux séparés. Les panneaux sont rendus redimensionnables par un séparateur. Cette disposition de contrôles est très efficace pour afficher et parcourir des informations.  
  
 Les étapes suivantes montrent comment disposer les contrôles dans un formulaire de type Explorateur Windows. Ils ne plus afficher comment ajouter la fonctionnalité d’exploration des fichiers de l’application de l’Explorateur Windows.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-a-windows-explorer-style-windows-form"></a>Pour créer un formulaire Windows de style Explorateur Windows  
  
1. Créer un nouveau projet d’Application de Windows (**fichier** > **New** > **projet** > **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).  
  
2. À partir de la **boîte à outils**:  
  
    1.  Faites glisser un <xref:System.Windows.Forms.SplitContainer> contrôle vers votre formulaire.  
  
    2.  Faites glisser un <xref:System.Windows.Forms.TreeView> contrôler en **SplitterPanel1** (le panneau de la <xref:System.Windows.Forms.SplitContainer> contrôle marqué **Panel1**).  
  
    3.  Faites glisser un <xref:System.Windows.Forms.ListView> contrôler en **SplitterPanel2** (le panneau de la <xref:System.Windows.Forms.SplitContainer> contrôle marqué **Panel2**).  
  
3. Sélectionnez tous les trois contrôles en appuyant sur la touche CTRL enfoncée et en cliquant dessus à son tour. Lorsque vous sélectionnez le <xref:System.Windows.Forms.SplitContainer> contrôler, cliquez sur la barre de fractionnement, plutôt que les panneaux.  
  
    > [!NOTE]
    >  N’utilisez pas le **sélectionner tout** commande sur le **modifier** menu. Si vous procédez ainsi, la propriété nécessaire à l’étape suivante n’apparaîtra pas dans le **propriétés** fenêtre.  
  
4. Dans la fenêtre **Propriétés** , définissez la propriété <xref:System.Windows.Forms.SplitContainer.Dock%2A> sur <xref:System.Windows.Forms.DockStyle.Fill>.  
  
5. Appuyez sur F5 pour exécuter l'application.  
  
     Le formulaire affiche une interface utilisateur de deux parties, similaire à celle de l’Explorateur Windows.  
  
    > [!NOTE]
    >  Lorsque vous faites glisser le séparateur, les panneaux se redimensionnent.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.SplitContainer>
- [Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms](how-to-create-a-multipane-user-interface-with-windows-forms.md)
- [Procédure : définir le comportement de redimensionnement et de positionnement dans une fenêtre fractionnée](how-to-define-resize-and-positioning-behavior-in-a-split-window.md)
- [Procédure : fractionner une fenêtre horizontalement](how-to-split-a-window-horizontally.md)
- [SplitContainer, contrôle](splitcontainer-control-windows-forms.md)
