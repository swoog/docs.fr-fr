---
title: 'Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- user interface [Windows Forms], multipane
- SplitContainer control [Windows Forms], using the designer
- multipane user interface
ms.assetid: c3f9294d-a26c-4198-9242-f237f55f7573
ms.openlocfilehash: 2b72d972d679a47213c0d5ed4270d2c623d713ca
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59082930"
---
# <a name="how-to-create-a-multipane-user-interface-with-windows-forms-using-the-designer"></a>Procédure : créer une interface utilisateur à plusieurs volets avec Windows Forms à l’aide du concepteur
Dans la procédure suivante, vous allez créer une interface utilisateur à plusieurs volets semblable à celle utilisée dans Microsoft Outlook, avec un **dossier** liste, un **Messages** volet et un **aperçu** volet. Cette disposition est obtenue principalement en ancrant les contrôles dans le formulaire.  
  
 Lorsque vous ancrez un contrôle, vous déterminez le bord du conteneur parent auquel un contrôle est attaché. Par conséquent, si vous définissez la <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Right>, le bord droit du contrôle sera ancré sur le bord droit de son contrôle parent. En outre, le bord du contrôle ancré est redimensionné pour correspondre à celle de son contrôle conteneur. Pour plus d’informations sur la façon dont <xref:System.Windows.Forms.SplitContainer.Dock%2A> fonctionne de la propriété, consultez [Comment : Ancrer des contrôles aux Windows Forms](how-to-dock-controls-on-windows-forms.md).  
  
 Cette procédure se concentre sur la disposition du <xref:System.Windows.Forms.SplitContainer> et d’autres contrôles sur le formulaire, et non sur l’ajout de fonctionnalités pour que l’application ressemble à Microsoft Outlook.  
  
 Pour créer cette interface utilisateur, vous placez tous les contrôles dans un <xref:System.Windows.Forms.SplitContainer> contrôle, qui contient un <xref:System.Windows.Forms.TreeView> contrôle dans le volet gauche. Le volet de droite de la <xref:System.Windows.Forms.SplitContainer> contrôle contient une seconde <xref:System.Windows.Forms.SplitContainer> contrôler avec un <xref:System.Windows.Forms.ListView> contrôle ci-dessus un <xref:System.Windows.Forms.RichTextBox> contrôle. Ces <xref:System.Windows.Forms.SplitContainer> les contrôles permettent un redimensionnement indépendant des autres contrôles sur le formulaire. Vous pouvez adapter les techniques de cette procédure pour les interfaces utilisateur personnalisées de métier de votre choix.  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-create-an-outlook-style-user-interface-at-design-time"></a>Pour créer une interface utilisateur de type Outlook au moment du design  
  
1.  Créer un nouveau projet d’Application de Windows (**fichier** > **New** > **projet** > **Visual C#** ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).  
  
2.  Faites glisser un <xref:System.Windows.Forms.SplitContainer> contrôle depuis la **boîte à outils** au formulaire. Dans la fenêtre **Propriétés** , définissez la propriété <xref:System.Windows.Forms.SplitContainer.Dock%2A> sur <xref:System.Windows.Forms.DockStyle.Fill>.  
  
3.  Faites glisser un <xref:System.Windows.Forms.TreeView> contrôler à partir de la **boîte à outils** vers le panneau gauche de la <xref:System.Windows.Forms.SplitContainer> contrôle. Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Left> en cliquant sur le panneau de gauche dans l’éditeur de valeur indiqué lorsque l’utilisateur clique sur la flèche vers le bas.  
  
4.  Faites glisser un autre <xref:System.Windows.Forms.SplitContainer> contrôle depuis la **boîte à outils**; placer dans le volet de droite de la <xref:System.Windows.Forms.SplitContainer> contrôle que vous avez ajouté à votre formulaire. Dans le **propriétés** fenêtre, définissez la <xref:System.Windows.Forms.SplitContainer.Dock%2A> propriété <xref:System.Windows.Forms.DockStyle.Fill> et <xref:System.Windows.Forms.SplitContainer.Orientation%2A> propriété <xref:System.Windows.Forms.Orientation.Horizontal>.  
  
5.  Faites glisser un <xref:System.Windows.Forms.ListView> contrôle depuis la **boîte à outils** vers le panneau supérieur du deuxième <xref:System.Windows.Forms.SplitContainer> contrôle que vous avez ajouté à votre formulaire. Affectez à la propriété <xref:System.Windows.Forms.SplitContainer.Dock%2A> du contrôle <xref:System.Windows.Forms.ListView> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.  
  
6.  Faites glisser un <xref:System.Windows.Forms.RichTextBox> contrôle depuis la **boîte à outils** vers le panneau inférieur du deuxième <xref:System.Windows.Forms.SplitContainer> contrôle. Affectez à la propriété <xref:System.Windows.Forms.SplitContainer.Dock%2A> du contrôle <xref:System.Windows.Forms.RichTextBox> la valeur <xref:System.Windows.Forms.DockStyle.Fill>.  
  
     À ce stade, si vous appuyez sur F5 pour exécuter l’application, le formulaire affiche une interface utilisateur en trois parties, semblable à celle de Microsoft Outlook.  
  
    > [!NOTE]
    >  Lorsque vous placez le pointeur de la souris sur un des séparateurs dans la <xref:System.Windows.Forms.SplitContainer> contrôles, vous pouvez modifier les dimensions internes.  
  
     À ce stade dans le développement d’applications, vous avez créé une interface utilisateur sophistiquée. L’étape suivante consiste à continuer la programmation de l’application elle-même, peut-être en connectant le <xref:System.Windows.Forms.TreeView> contrôle et <xref:System.Windows.Forms.ListView> contrôles à un certain type de source de données. Pour plus d’informations sur la connexion des contrôles aux données, consultez [une liaison de données et Windows Forms](../data-binding-and-windows-forms.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.SplitContainer>
- [SplitContainer, contrôle](splitcontainer-control-windows-forms.md)
