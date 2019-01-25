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
ms.openlocfilehash: e877545f93fb57b636fd2e1559f52b4ad70a0b4e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722762"
---
# <a name="how-to-add-an-unbound-column-to-a-data-bound-windows-forms-datagridview-control"></a>Procédure : Ajouter une colonne indépendante à un contrôle de DataGridView lié aux données Windows Forms
Les données que vous affichez dans le contrôle <xref:System.Windows.Forms.DataGridView> proviennent normalement d'une source de données quelconque. Vous pouvez toutefois vouloir afficher une colonne de données qui ne provienne pas de la source de données. Ce type de colonne est appelé colonne indépendante. Les colonnes indépendantes peuvent prendre de nombreuses formes. Souvent, elles sont utilisées pour fournir un accès aux détails d'une ligne de données.  
  
 L’exemple de code suivant montre comment créer une colonne indépendante de **détails** boutons à afficher une table enfant sont liés à une ligne particulière dans une table parente lorsque vous implémentez un scénario maître/détail. Pour répondre aux clics de bouton, implémentez un gestionnaire d'événements <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType> qui affiche un formulaire contenant la table enfant.  
  
 Cette tâche est prise en charge dans Visual Studio.  Voir également [Guide pratique pour Ajouter et supprimer des colonnes dans le contrôle de DataGridView Windows Forms à l’aide du Concepteur](https://msdn.microsoft.com/library/dyyesckz\(v=vs.110\))  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#010](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#010)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#010](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#010)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   un contrôle <xref:System.Windows.Forms.DataGridView> nommé `dataGridView1` ;  
  
-   des références aux assemblys <xref:System?displayProperty=nameWithType> et <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- [Affichage des données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)
- [Modes d’affichage des données dans le contrôle DataGridView Windows Forms](../../../../docs/framework/winforms/controls/data-display-modes-in-the-windows-forms-datagridview-control.md)
