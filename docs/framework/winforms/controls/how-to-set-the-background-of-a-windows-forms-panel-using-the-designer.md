---
title: 'Procédure : Définir l’arrière-plan d’un contrôle Panel Windows Forms à l’aide du Concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: db83cf54-3c69-4b08-ac6c-25b9b5abb1b0
ms.openlocfilehash: 73b09b9240f417dbe80546e89f2fdfb1e4e4a483
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711913"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel-using-the-designer"></a>Procédure : Définir l’arrière-plan d’un contrôle Panel Windows Forms à l’aide du Concepteur
Un formulaire Windows <xref:System.Windows.Forms.Panel> contrôle peut afficher une couleur d’arrière-plan et une image d’arrière-plan. Le <xref:System.Windows.Forms.Control.BackColor%2A> propriété définit la couleur d’arrière-plan pour les contrôles qui sont contenus dans le panneau de configuration, tels que des étiquettes et cases d’option. Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété n’est pas définie, le <xref:System.Windows.Forms.Control.BackColor%2A> sélectionnée remplit tout le panneau. Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété est définie, l’image est affichée derrière les contrôles qui sont contenus dans le panneau de configuration.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire qui contient un <xref:System.Windows.Forms.Panel> contrôle. Pour plus d’informations sur la façon de configurer un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-set-the-background-in-the-windows-forms-designer"></a>Pour définir l’arrière-plan dans le Concepteur de formulaires Windows  
  
1.  Sélectionnez le contrôle <xref:System.Windows.Forms.Panel>.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur la flèche située en regard du <xref:System.Windows.Forms.Control.BackColor%2A> propriété pour afficher une fenêtre avec trois onglets.  
  
3.  Sélectionnez le **personnalisé** onglet pour afficher une palette de couleurs.  
  
4.  Sélectionnez le **Web** ou **système** onglet pour afficher une liste de noms de couleurs prédéfinis, puis sélectionnez une couleur.  
  
5.  Dans le **propriétés** fenêtre, cliquez sur la flèche située en regard du <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété.  
  
6.  Dans le **Open** boîte de dialogue, sélectionnez le fichier que vous souhaitez afficher.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [Panel, contrôle](panel-control-windows-forms.md)
- [Vue d’ensemble du contrôle Panel](panel-control-overview-windows-forms.md)
- [Guide pratique pour Contrôles de groupe avec le contrôle de panneau Windows Forms à l’aide du Concepteur](group-controls-with-wf-panel-control-using-the-designer.md)
