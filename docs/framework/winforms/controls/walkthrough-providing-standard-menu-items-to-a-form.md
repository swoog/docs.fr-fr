---
title: 'Procédure pas à pas : fourniture d’éléments de menu standard à un formulaire'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- menu items [Windows Forms], standard
- toolbars [Windows Forms], walkthroughs
- StatusStrip control [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: dac37d98-589e-4d6d-9673-6437e8943122
ms.openlocfilehash: ebfacadfee3ea069359a72ea0402751e9e6280d7
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211498"
---
# <a name="walkthrough-providing-standard-menu-items-to-a-form"></a>Procédure pas à pas : fourniture d’éléments de menu standard à un formulaire

Vous pouvez fournir un menu standard pour vos formulaires avec le contrôle <xref:System.Windows.Forms.MenuStrip>.

Cette procédure pas à pas montre comment utiliser un <xref:System.Windows.Forms.MenuStrip> contrôle pour créer un menu standard. Le formulaire répond également lorsqu’un utilisateur sélectionne un élément de menu. Les tâches suivantes sont illustrées dans cette procédure pas à pas :

- Création d’un projet Windows Forms.

- Création d’un menu standard.

- Création d’un <xref:System.Windows.Forms.StatusStrip> contrôle.

- Gérer la sélection d’éléments de menu.

Lorsque vous avez terminé, vous disposerez d’un formulaire avec un menu standard qui affiche les sélections d’élément de menu dans un <xref:System.Windows.Forms.StatusStrip> contrôle.

Pour copier le code dans cette rubrique sous la forme d’une liste unique, consultez [Guide pratique pour Fournir des éléments de Menu Standard à un formulaire](how-to-provide-standard-menu-items-to-a-form.md).

## <a name="prerequisites"></a>Prérequis

Vous aurez besoin de Visual Studio pour effectuer cette procédure pas à pas.

## <a name="create-the-project"></a>Créer le projet

1. Dans Visual Studio, créez un projet d’application Windows appelé **StandardMenuForm** (**fichier** > **New** > **projet**   >  **Visual C#**  ou **Visual Basic** > **bureau classique**  >  **Windows Forms Application**).

2. Dans le Concepteur Windows Forms, sélectionnez le formulaire.

## <a name="create-a-standard-menu"></a>Créer un menu standard

Le Concepteur de formulaires Windows peut remplir automatiquement un <xref:System.Windows.Forms.MenuStrip> contrôle avec les éléments de menu standard.

1. À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.MenuStrip> contrôle vers votre formulaire.

2. Cliquez sur le <xref:System.Windows.Forms.MenuStrip> glyphe de balise active du contrôle (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) et sélectionnez **insérer des éléments Standard**.

     Le <xref:System.Windows.Forms.MenuStrip> contrôle soit rempli avec les éléments de menu standard.

3. Cliquez sur le **fichier** élément de menu pour afficher ses éléments de menu par défaut et les icônes correspondantes.

## <a name="create-a-statusstrip-control"></a>Créer un contrôle StatusStrip

Utilisez le <xref:System.Windows.Forms.StatusStrip> contrôle pour afficher l’état de vos applications Windows Forms. Dans l’exemple actuel, les éléments de menu sélectionnés par l’utilisateur sont affichés dans un <xref:System.Windows.Forms.StatusStrip> contrôle.

1. À partir de la **boîte à outils**, faites glisser un <xref:System.Windows.Forms.StatusStrip> contrôle vers votre formulaire.

     Le <xref:System.Windows.Forms.StatusStrip> contrôle s’ancre automatiquement vers le bas du formulaire.

2. Cliquez sur le <xref:System.Windows.Forms.StatusStrip> du contrôle bouton de liste déroulante et sélectionnez **StatusLabel** pour ajouter un <xref:System.Windows.Forms.ToolStripStatusLabel> le contrôle à la <xref:System.Windows.Forms.StatusStrip> contrôle.

## <a name="handle-item-selection"></a>Gérer la sélection d’éléments

Gérer le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement répondre quand l’utilisateur sélectionne un élément de menu.

1. Cliquez sur le **fichier** élément de menu que vous avez créé dans la création une section de Menu Standard.

2. Dans la fenêtre **Propriétés**, cliquez sur **Événements**.

3. Double-cliquez sur le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement.

     Le Concepteur de formulaires Windows génère un gestionnaire d’événements pour le <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> événement.

4. Insérez le code suivant dans le Gestionnaire d’événements.

     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#3)]

5. Insérer le `UpdateStatus` définition de méthode d’utilitaire dans le formulaire.

     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#2)]

## <a name="checkpoint--test-your-form"></a>Point de contrôle-tester votre formulaire

1. Appuyez sur **F5** pour compiler et exécuter votre formulaire.

2. Cliquez sur le **fichier** élément de menu pour ouvrir le menu.

3. Sur le **fichier** menu, cliquez sur un des éléments pour le sélectionner.

     Le <xref:System.Windows.Forms.StatusStrip> contrôle affiche l’élément sélectionné.

## <a name="next-steps"></a>Étapes suivantes

Dans cette procédure pas à pas, vous avez créé un formulaire avec un menu standard. Vous pouvez utiliser le <xref:System.Windows.Forms.ToolStrip> famille de contrôles à de nombreuses autres fins :

- Créer des menus contextuels pour vos contrôles avec <xref:System.Windows.Forms.ContextMenuStrip>. Pour plus d’informations, consultez [vue d’ensemble du composant ContextMenu](contextmenu-component-overview-windows-forms.md).

- Créer un formulaire d’interface (multidocument MDI) document avec l’ancrage <xref:System.Windows.Forms.ToolStrip> contrôles. Pour plus d’informations, consultez [Procédure pas à pas : Création d’un formulaire MDI avec la fusion de menus et des contrôles ToolStrip](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).

- Donnez à votre <xref:System.Windows.Forms.ToolStrip> contrôle un aspect professionnel. Pour plus d'informations, voir [Procédure : Définir le convertisseur ToolStrip pour une Application](how-to-set-the-toolstrip-renderer-for-an-application.md).

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [MenuStrip, contrôle](menustrip-control-windows-forms.md)
