---
title: 'Procédure : ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- examples [Windows Forms], TreeView control
- TreeView control [Windows Forms], removing nodes
- tree nodes in TreeView control
- TreeView control [Windows Forms], adding nodes
ms.assetid: 35bf1750-045e-4ec5-97cb-b47b0dbdaa2c
ms.openlocfilehash: ca8b19e8019c170f1826660e951294b18a25e96d
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880618"
---
# <a name="how-to-add-and-remove-nodes-with-the-windows-forms-treeview-control-using-the-designer"></a>Procédure : ajouter et supprimer des nœuds avec le contrôle TreeView Windows Forms à l’aide du concepteur
Étant donné que les Windows Forms <xref:System.Windows.Forms.TreeView> contrôle affiche les nœuds de façon hiérarchique, lors de l’ajout d’un nœud, vous devez faire attention à ce qui est son nœud parent.  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.TreeView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-or-remove-nodes-in-the-designer"></a>Pour ajouter ou supprimer des nœuds dans le Concepteur  
  
1. Sélectionnez le contrôle <xref:System.Windows.Forms.TreeView>.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur le **points de suspension** (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) situé en regard du <xref:System.Windows.Forms.TreeView.Nodes%2A> propriété .  
  
     Le **Éditeur TreeNode** s’affiche.  
  
3. Pour ajouter des nœuds, un nœud racine doit exister ; s’il n’existe pas, vous devez d’abord ajouter une racine en cliquant sur le **racine ajouter** bouton. Vous pouvez ensuite ajouter des nœuds enfants en sélectionnant la racine ou tout autre nœud, puis en cliquant sur le **ajouter un enfant** bouton.  
  
4. Pour supprimer des nœuds, sélectionnez le nœud à supprimer, puis cliquez sur le **supprimer** bouton.  
  
## <a name="see-also"></a>Voir aussi

- [TreeView, contrôle](treeview-control-windows-forms.md)
- [Vue d’ensemble du contrôle TreeView](treeview-control-overview-windows-forms.md)
- [Guide pratique pour Définir des icônes pour le contrôle TreeView Windows Forms](how-to-set-icons-for-the-windows-forms-treeview-control.md)
- [Guide pratique pour Effectuer une itération dans tous les nœuds d’un contrôle de TreeView Windows Forms](how-to-iterate-through-all-nodes-of-a-windows-forms-treeview-control.md)
- [Guide pratique pour Déterminer l’utilisateur a cliqué sur le nœud de TreeView](how-to-determine-which-treeview-node-was-clicked-windows-forms.md)
- [Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
