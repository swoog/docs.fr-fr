---
title: 'Procédure : ajouter des colonnes au contrôle ListView Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView control [Windows Forms], adding column headers
- columns [Windows Forms], adding to ListView controls
ms.assetid: 5b1a8b4d-587e-479a-95c1-f9b90884f13a
ms.openlocfilehash: 9ddff31e4d66ffef2600a1246b35c0a66154c341
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59190417"
---
# <a name="how-to-add-columns-to-the-windows-forms-listview-control-using-the-designer"></a>Procédure : ajouter des colonnes au contrôle ListView Windows Forms à l’aide du concepteur
Les formulaires Windows <xref:System.Windows.Forms.ListView> contrôle peut afficher plusieurs colonnes pour chaque liste d’éléments dans le **détails** vue. Vous pouvez utiliser les colonnes pour afficher plusieurs types d’informations sur chaque élément de liste. Par exemple, une liste de fichiers peut afficher le nom de fichier, type de fichier, taille et date de que dernière modification du fichier. Pour plus d’informations sur le remplissage des colonnes une fois qu’ils sont créés, consultez [Comment : Afficher des sous-éléments en colonnes avec les Windows Forms ListView contrôle](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md).  
  
 La procédure suivante nécessite un **Windows Application** projet avec un formulaire contenant un <xref:System.Windows.Forms.ListView> contrôle. Pour plus d’informations sur la configuration d’un tel projet, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Les boîtes de dialogue et les commandes de menu qui s'affichent peuvent être différentes de celles qui sont décrites dans l'aide, en fonction de vos paramètres actifs ou de l'édition utilisée. Pour modifier vos paramètres, choisissez **Importation et exportation de paramètres** dans le menu **Outils** . Pour plus d’informations, consultez [Personnaliser l’IDE Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-columns-in-the-designer"></a>Pour ajouter des colonnes dans le Concepteur  
  
1.  Dans le **propriétés** fenêtre, définissez le contrôle <xref:System.Windows.Forms.ListView.View%2A> propriété <xref:System.Windows.Forms.View.Details>.  
  
2.  Dans le **propriétés** fenêtre, cliquez sur le **points de suspension** bouton (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) à côté le <xref:System.Windows.Forms.ListView.Columns%2A> propriété.  
  
     Le **éditeur de collections ColumnHeader** s’affiche.  
  
3.  Utilisez le **ajouter** pour ajouter de nouvelles colonnes. Vous pouvez ensuite sélectionner l’en-tête de colonne et définir son texte (la légende de la colonne), alignement du texte et la largeur.  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Procédure : afficher des sous-éléments dans des colonnes avec le contrôle ListView Windows Forms](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)
- [Procédure : afficher des icônes pour le contrôle ListView Windows Forms](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [Procédure : ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
