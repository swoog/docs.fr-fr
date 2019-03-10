---
title: 'Procédure : Ajouter des colonnes au contrôle ListView Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView control [Windows Forms], adding column headers
- columns [Windows Forms], adding to ListView controls
- list views [Windows Forms], adding columns
ms.assetid: 79174274-12ee-4a5d-80db-6ec02976d010
ms.openlocfilehash: 4937c31da5dd54cb96090c573e7bdba7a0c7d834
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57718959"
---
# <a name="how-to-add-columns-to-the-windows-forms-listview-control"></a>Procédure : Ajouter des colonnes au contrôle ListView Windows Forms
Dans la vue Détails, le <xref:System.Windows.Forms.ListView> contrôle peut afficher plusieurs colonnes pour chaque élément de liste. Vous pouvez utiliser les colonnes à afficher à l’utilisateur plusieurs types d’informations sur chaque élément de liste. Par exemple, une liste de fichiers peut afficher le nom de fichier, type de fichier, taille et date de que dernière modification du fichier. Pour plus d’informations sur le remplissage des colonnes après leur création, consultez [Comment : Afficher des sous-éléments en colonnes avec les Windows Forms ListView contrôle](how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md).  
  
### <a name="to-add-columns-programmatically"></a>Pour ajouter des colonnes par programmation  
  
1.  Définir le contrôle <xref:System.Windows.Forms.ListView.View%2A> propriété <xref:System.Windows.Forms.View.Details>.  
  
2.  Utilisez le <xref:System.Windows.Forms.ListView.ColumnHeaderCollection.Add%2A> méthode de la vue liste <xref:System.Windows.Forms.ListView.Columns%2A> propriété.  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#31)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.ListView>
- [Contrôle ListView](listview-control-windows-forms.md)
- [Vue d’ensemble du contrôle ListView](listview-control-overview-windows-forms.md)
