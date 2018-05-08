---
title: 'Comment : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], populating
- list views [Windows Forms], adding list items
- ListView control [Windows Forms], adding list items
ms.assetid: 1b35a80a-edd8-495f-a807-a28c4aae52c6
ms.openlocfilehash: 83ef2e108695988bbb0329d9f01e1317d9308f18
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control"></a>Comment : ajouter et supprimer des éléments avec le contrôle ListView Windows Forms
Le processus d’ajout d’un élément à un Windows Forms <xref:System.Windows.Forms.ListView> contrôle se compose principalement de la spécification de l’élément et lui assigner des propriétés. Ajouter ou supprimer des éléments de liste peut être effectuée à tout moment.  
  
### <a name="to-add-items-programmatically"></a>Pour ajouter par programmation des éléments  
  
1.  Utilisez le <xref:System.Windows.Forms.ListView.ListViewItemCollection.Add%2A> méthode de la <xref:System.Windows.Forms.ListView.Items%2A> propriété.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#11)]  
  
### <a name="to-remove-items-programmatically"></a>Pour supprimer des éléments par programme  
  
1.  Utilisez le <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> ou <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> méthode de la <xref:System.Windows.Forms.ListView.Items%2A> propriété. Le <xref:System.Windows.Forms.ListView.ListViewItemCollection.RemoveAt%2A> méthode supprime un élément unique ; le <xref:System.Windows.Forms.ListView.ListViewItemCollection.Clear%2A> méthode supprime tous les éléments de la liste.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.ListView>  
 [Contrôle ListView](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)  
 [Vue d’ensemble du contrôle ListView](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)
