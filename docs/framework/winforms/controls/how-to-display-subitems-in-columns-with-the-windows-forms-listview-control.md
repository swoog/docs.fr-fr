---
title: 'Procédure : afficher des sous-éléments dans des colonnes avec le contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- list items
- Details view
- ListView control [Windows Forms], adding ListSubItems
- subitems
ms.assetid: e465f044-cde7-4fd9-a687-788a73a0f554
ms.openlocfilehash: defa8aa736927c9076eb2410d6d914a8f7550d03
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59183714"
---
# <a name="how-to-display-subitems-in-columns-with-the-windows-forms-listview-control"></a>Procédure : afficher des sous-éléments dans des colonnes avec le contrôle ListView Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.ListView> contrôle peut afficher un texte supplémentaire ou des sous-éléments pour chaque élément dans la vue Détails. La première colonne affiche le texte de l’élément, par exemple un numéro d’employé. La deuxième, troisième et les colonnes suivantes affichent le premier, deuxième, et les sous-éléments suivants.  
  
### <a name="to-add-subitems-to-a-list-item"></a>Pour ajouter des sous-éléments à un élément de liste  
  
1.  Ajoutez toutes les colonnes nécessités. Étant donné que la première colonne affiche l’élément <xref:System.Windows.Forms.ListView.Text%2A> propriété, vous avez besoin d’une colonne de plus qu’il sont a de sous-éléments. Pour plus d’informations sur l’ajout de colonnes, consultez [Comment : Ajouter des colonnes pour les Windows Forms ListView contrôle](how-to-add-columns-to-the-windows-forms-listview-control.md).  
  
2.  Appelez le <xref:System.Windows.Forms.ListViewItem.ListViewSubItemCollection.Add%2A> méthode de la collection retournée par la <xref:System.Windows.Forms.ListViewItem.SubItems%2A> propriété d’un élément. L’exemple de code ci-dessous définit le nom de l’employé et le service pour un élément de liste.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#61)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#61)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
- [Procédure : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms](how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)
- [Procédure : ajouter des colonnes au contrôle ListView Windows Forms](how-to-add-columns-to-the-windows-forms-listview-control.md)
- [Procédure : afficher des icônes pour le contrôle ListView Windows Forms](how-to-display-icons-for-the-windows-forms-listview-control.md)
- [Procédure : ajouter des informations personnalisées à un contrôle TreeView ou ListView (Windows Forms)](add-custom-information-to-a-treeview-or-listview-control-wf.md)
