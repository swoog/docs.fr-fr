---
title: 'Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView control [Windows Forms], populating
- ListView control [Windows Forms], adding list items
ms.assetid: 217611ee-fd11-4d39-9a54-a37c3e781be1
ms.openlocfilehash: 37e793104eb29c21e67b975a7caa372cc817e57f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59143882"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control-using-the-designer"></a>Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms à l’aide du concepteur
Le processus d’ajout d’un élément à un formulaire Windows <xref:System.Windows.Forms.ListView> contrôle se compose principalement de la spécification de l’élément et lui assigner des propriétés. Ajouter ou supprimer des éléments de liste peut être effectuée à tout moment.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.ListView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-or-remove-items-using-the-designer"></a>Pour ajouter ou supprimer des éléments à l’aide du Concepteur  
  
1.  Sélectionnez le contrôle <xref:System.Windows.Forms.ListView>.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur le **points de suspension** (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) situé en regard le <xref:System.Windows.Forms.ListView.Items%2A> propriété.  
  
     Le **éditeur de collections ListViewItem** s’affiche.  
  
3.  Pour ajouter un élément, cliquez sur le **ajouter** bouton. Vous pouvez ensuite définir les propriétés du nouvel élément, tel que le <xref:System.Windows.Forms.ListView.Text%2A> et <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> propriétés.  
  
4.  Pour supprimer un élément, sélectionnez-le et cliquez sur le **supprimer** bouton.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Procédure : ajouter des colonnes au contrôle ListView Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [Procédure : afficher des sous-éléments dans des colonnes avec le contrôle ListView Windows Forms](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)
- [Procédure : afficher des icônes pour le contrôle ListView Windows Forms](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [Procédure : ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [Procédure : regrouper des éléments dans un contrôle ListView Windows Forms](how-to-group-items-in-a-windows-forms-listview-control.md)
