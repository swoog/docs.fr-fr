---
title: 'Procédure : afficher des icônes pour le contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], displaying icons
- icons [Windows Forms], displaying for ListView controls
- lists [Windows Forms], displaying icons
- ImageList component [Windows Forms], with ListView control
- list views [Windows Forms], displaying icons
ms.assetid: 9d577542-8595-429b-99e5-078770ec9d35
ms.openlocfilehash: e01035a356c0293959676cd5907d2234bbf79f16
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59151383"
---
# <a name="how-to-display-icons-for-the-windows-forms-listview-control"></a>Procédure : afficher des icônes pour le contrôle ListView Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.ListView> contrôle peut afficher des icônes à partir de trois listes d’images. Les vues de liste, les détails et SmallIcon affichent des images à partir de la liste d’images spécifié dans le <xref:System.Windows.Forms.ListView.SmallImageList%2A> propriété. La vue LargeIcon affiche des images à partir de la liste d’images spécifié dans le <xref:System.Windows.Forms.ListView.LargeImageList%2A> propriété. Un affichage de liste peut également afficher un ensemble supplémentaire d’icônes, défini le <xref:System.Windows.Forms.ListView.StateImageList%2A> propriété, en regard des petites ou grandes icônes. Pour plus d’informations sur les listes d’images, consultez [composant ImageList](imagelist-component-windows-forms.md) et [Comment : Ajouter ou supprimer des Images avec les Windows Forms composant ImageList](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).  
  
### <a name="to-display-images-in-a-list-view"></a>Pour afficher des images dans une vue liste  
  
1.  Définissez la propriété appropriée :<xref:System.Windows.Forms.ListView.SmallImageList%2A>, <xref:System.Windows.Forms.ListView.LargeImageList%2A>, ou <xref:System.Windows.Forms.ListView.StateImageList%2A>— à l’objet existant <xref:System.Windows.Forms.ImageList> composant que vous souhaitez utiliser.  
  
     Ces propriétés peuvent être définies dans le concepteur avec la fenêtre Propriétés ou dans le code.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#41)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#41)]  
  
2.  Définir le <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> ou <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> propriété pour chaque élément de liste qui a une icône associée.  
  
     Ces propriétés peuvent être définies dans le code ou dans le **éditeur de collections ListViewItem**. Pour ouvrir le **éditeur de collections ListViewItem**, cliquez sur le bouton de sélection (![d’écran de VisualStudioEllipsesButton](../media/vbellipsesbutton.png "vbEllipsesButton")) en regard de la <xref:System.Windows.Forms.ListView.Items%2A>propriété sur le **propriétés** fenêtre.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#42)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#42)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Procédure : ajouter des colonnes au contrôle ListView Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [Procédure : ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [ImageList, composant](imagelist-component-windows-forms.md)
