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
ms.openlocfilehash: 80a827a88ac92008c7fe2a642d1d4b59a18f89da
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880407"
---
# <a name="how-to-display-icons-for-the-windows-forms-listview-control"></a>Procédure : afficher des icônes pour le contrôle ListView Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.ListView> contrôle peut afficher des icônes à partir de trois listes d’images. Les vues de liste, les détails et SmallIcon affichent des images à partir de la liste d’images spécifié dans le <xref:System.Windows.Forms.ListView.SmallImageList%2A> propriété. La vue LargeIcon affiche des images à partir de la liste d’images spécifié dans le <xref:System.Windows.Forms.ListView.LargeImageList%2A> propriété. Un affichage de liste peut également afficher un ensemble supplémentaire d’icônes, défini le <xref:System.Windows.Forms.ListView.StateImageList%2A> propriété, en regard des petites ou grandes icônes. Pour plus d’informations sur les listes d’images, consultez [composant ImageList](imagelist-component-windows-forms.md) et [Comment : Ajouter ou supprimer des Images avec les Windows Forms composant ImageList](how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).  
  
### <a name="to-display-images-in-a-list-view"></a>Pour afficher des images dans une vue liste  
  
1. Définissez la propriété appropriée :<xref:System.Windows.Forms.ListView.SmallImageList%2A>, <xref:System.Windows.Forms.ListView.LargeImageList%2A>, ou <xref:System.Windows.Forms.ListView.StateImageList%2A>— à l’objet existant <xref:System.Windows.Forms.ImageList> composant que vous souhaitez utiliser.  
  
     Ces propriétés peuvent être définies dans le concepteur avec la fenêtre Propriétés ou dans le code.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#41)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#41)]  
  
2. Définir le <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> ou <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> propriété pour chaque élément de liste qui a une icône associée.  
  
     Ces propriétés peuvent être définies dans le code ou dans le **éditeur de collections ListViewItem**. Pour ouvrir le **éditeur de collections ListViewItem**, cliquez sur le bouton de sélection (![bouton les points de suspension (...) dans la fenêtre Propriétés de Visual Studio.](./media/visual-studio-ellipsis-button.png)) à côté du <xref:System.Windows.Forms.ListView.Items%2A> propriété sur le **Propriétés** fenêtre.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#42)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#42)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Guide pratique pour Ajouter et supprimer des éléments avec le contrôle ListView Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Guide pratique pour Ajouter des colonnes au contrôle ListView Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [Guide pratique pour Ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
- [ImageList, composant](imagelist-component-windows-forms.md)
