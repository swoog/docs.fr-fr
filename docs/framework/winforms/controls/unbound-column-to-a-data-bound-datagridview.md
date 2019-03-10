---
title: 'Procédure : Ajouter une colonne indépendante à un contrôle de DataGridView lié aux données Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- columns [Windows Forms], unbound data
- data grids [Windows Forms], adding unbound columns
- DataGridView control [Windows Forms], unbound data
ms.assetid: f7bdc4d8-ba8e-421b-ad62-82d936f01372
ms.openlocfilehash: d7f96aa8d11cee9427a9e51f8e79fc55adc79355
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711994"
---
# <a name="how-to-add-an-unbound-column-to-a-data-bound-windows-forms-datagridview-control"></a>Procédure : Ajouter une colonne indépendante à un contrôle de DataGridView lié aux données Windows Forms
Les données que vous affichez dans le contrôle <xref:System.Windows.Forms.DataGridView> proviennent normalement d'une source de données quelconque. Vous pouvez toutefois vouloir afficher une colonne de données qui ne provienne pas de la source de données. Ce type de colonne est appelé colonne indépendante. Les colonnes indépendantes peuvent prendre de nombreuses formes. Souvent, elles sont utilisées pour fournir un accès aux détails d'une ligne de données.  
  
 L’exemple de code suivant montre comment créer une colonne indépendante de **détails** boutons à afficher une table enfant sont liés à une ligne particulière dans une table parente lorsque vous implémentez un scénario maître/détail. Pour répondre aux clics de bouton, implémentez un gestionnaire d'événements <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType> qui affiche un formulaire contenant la table enfant.  
  
 Cette tâche est prise en charge dans Visual Studio.  Voir également [Guide pratique pour Ajouter et supprimer des colonnes dans les Windows Forms DataGridView Control à l’aide du concepteur](add-and-remove-columns-in-the-datagrid-using-the-designer.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#010](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#010)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#010](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#010)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- [Affichage des données dans le contrôle DataGridView Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)
- [Modes d’affichage des données dans le contrôle DataGridView Windows Forms](data-display-modes-in-the-windows-forms-datagridview-control.md)
