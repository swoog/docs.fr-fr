---
title: Vue d'ensemble du contrôle ToolBar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ToolBar
helpviewer_keywords:
- toolbars [Windows Forms], about toolbars
- ToolBar control [Windows Forms], about ToolBar controls
ms.assetid: d426b203-0216-4dbe-b834-1641e50a9c29
ms.openlocfilehash: 7b39c8e3dca88e968b43ba5ff14794e2e77247d1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59174809"
---
# <a name="toolbar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle ToolBar (Windows Forms)
> [!NOTE]
>  Le contrôle <xref:System.Windows.Forms.ToolStrip> remplace le contrôle <xref:System.Windows.Forms.ToolBar> et lui ajoute des fonctionnalités ; toutefois, le contrôle <xref:System.Windows.Forms.ToolBar> est conservé pour la compatibilité descendante et l'utilisation future si tel est votre choix.  
  
 Le contrôle Windows Forms <xref:System.Windows.Forms.ToolBar> est utilisé sur les formulaires comme barre de contrôle affichant une rangée de menus déroulants et de boutons bitmap qui activent des commandes. Ainsi, un clic sur un bouton de barre d’outils peut être équivalent à choisir une commande de menu. Vous pouvez configurer les boutons pour qu’ils apparaissent et se comportent comme des boutons de commande, des menus déroulants ou des séparateurs. En règle générale, une barre d'outils contient des boutons et des menus qui correspondent à des éléments dans la structure de menu de l'application et fournissent un accès rapide aux commandes et aux fonctions les plus fréquemment utilisées d'une application.  
  
## <a name="working-with-the-toolbar-control"></a>Utilisation du contrôle ToolBar  
 Un <xref:System.Windows.Forms.ToolBar> contrôle est généralement « fixé » en haut de sa fenêtre parente, mais il peut également être ancré à n’importe quel côté de la fenêtre. Une barre d’outils peut afficher des info-bulles quand l’utilisateur pointe avec la souris sur un bouton de barre d’outils. Une info-bulle est une petite fenêtre contextuelle qui décrit brièvement l’objectif du bouton ou du menu. Pour afficher des info-bulles, la <xref:System.Windows.Forms.ToolBar.ShowToolTips%2A> propriété doit être définie sur `true`.  
  
> [!NOTE]
>  Certaines applications comportent des contrôles très similaires à la barre d’outils, qui ont la possibilité de « flotter » au-dessus de la fenêtre de l’application et d’être repositionnés. Le contrôle Windows Forms ToolBar n’est pas en mesure d’effectuer ces actions.  
  
 Lorsque le <xref:System.Windows.Forms.ToolBar.Appearance%2A> propriété est définie sur <xref:System.Windows.Forms.ToolBarAppearance>, les boutons de barre d’outils apparaissent en relief et en trois dimensions. Vous pouvez définir le <xref:System.Windows.Forms.ToolBar.Appearance%2A> propriété de la barre d’outils pour <xref:System.Windows.Forms.ToolBarAppearance> pour donner à la barre d’outils et de ses boutons un aspect plat. Quand le pointeur de la souris est placé sur un bouton à deux dimensions, l’apparence du bouton passe à trois dimensions. Les boutons de barre d’outils peut être divisés en groupes logiques à l’aide de séparateurs. Un séparateur est un bouton de barre d’outils avec le <xref:System.Windows.Forms.ToolBarButton.Style%2A> propriété définie sur <xref:System.Windows.Forms.ToolBarButtonStyle>. Il apparaît comme un espace vide dans la barre d’outils. Quand la barre d’outils a une apparence à deux dimensions, les séparateurs de boutons apparaissent comme des lignes (et non pas des espaces) entre les boutons.  
  
 Le <xref:System.Windows.Forms.ToolBar> contrôle vous permet de créer des barres d’outils en ajoutant <xref:System.Windows.Forms.Button> des objets sur un <xref:System.Windows.Forms.ToolBar.Buttons%2A> collection. Vous pouvez utiliser l’éditeur de collections pour ajouter des boutons à un <xref:System.Windows.Forms.ToolBar> contrôle ; chaque <xref:System.Windows.Forms.Button> objet doit être texte ou une image, vous pouvez affecter à la fois. L’image est fournie par un composant [ImageList](imagelist-component-windows-forms.md) associé. Au moment de l’exécution, vous pouvez ajouter ou supprimer des boutons à partir de la <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection> à l’aide de la <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection.Add%2A> et <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection.Remove%2A> méthodes. Pour programmer les boutons d’une <xref:System.Windows.Forms.ToolBar>, ajouter du code pour le <xref:System.Windows.Forms.ToolBar.ButtonClick> événements de la <xref:System.Windows.Forms.ToolBar>, à l’aide la <xref:System.Windows.Forms.ToolBarButtonClickEventArgs.Button%2A> propriété de la <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> classe pour déterminer quel bouton l’utilisateur a cliqué.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.ToolBar>
- [ToolBar, contrôle](toolbar-control-windows-forms.md)
- [Guide pratique pour Ajouter des boutons à un contrôle de barre d’outils](how-to-add-buttons-to-a-toolbar-control.md)
- [Guide pratique pour Définir une icône pour un bouton de barre d’outils](how-to-define-an-icon-for-a-toolbar-button.md)
- [Guide pratique pour Déclencher des événements de Menu pour les boutons de barre d’outils](how-to-trigger-menu-events-for-toolbar-buttons.md)
