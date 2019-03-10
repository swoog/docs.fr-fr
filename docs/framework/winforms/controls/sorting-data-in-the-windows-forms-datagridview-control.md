---
title: Tri des données dans le contrôle Windows Forms DataGridView
ms.date: 02/13/2018
helpviewer_keywords:
- data [Windows Forms], sorting in grids
- data grids [Windows Forms], sorting data
- DataGridView control [Windows Forms], sorting data
ms.assetid: c1d4f24c-d961-4181-809d-5a5caa6122e4
ms.openlocfilehash: 606ffc7bd6136b775adaaaa79cf5042cf1e2dd70
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57724919"
---
# <a name="sorting-data-in-the-windows-forms-datagridview-control"></a>Tri des données dans le contrôle Windows Forms DataGridView

Par défaut, les utilisateurs peuvent trier les données dans un <xref:System.Windows.Forms.DataGridView> contrôle en cliquant sur l’en-tête d’une colonne de zone de texte (ou en appuyant sur F3 lorsqu’une cellule de zone de texte a le focus sur .NET Framework 4.7.2 et versions ultérieures). Vous pouvez modifier le <xref:System.Windows.Forms.DataGridViewColumn.SortMode> propriété des colonnes spécifiques pour permettre aux utilisateurs de trier par d’autres types de colonne lorsqu’il est judicieux de le faire. Vous pouvez également trier les données par programme en n’importe quelle colonne, ou en plusieurs colonnes.

## <a name="in-this-section"></a>Dans cette section

[Modes de tri des colonnes du contrôle DataGridView Windows Forms](column-sort-modes-in-the-windows-forms-datagridview-control.md)  
Décrit les options de tri des données dans le contrôle.

[Guide pratique pour Définir les Modes de tri des colonnes dans le contrôle de DataGridView Windows Forms](set-the-sort-modes-for-columns-wf-datagridview-control.md)  
Explique comment permettre aux utilisateurs de trier les colonnes qui ne sont pas pouvant être triées par défaut.

[Guide pratique pour Personnaliser le tri dans le contrôle DataGridView Windows Forms](how-to-customize-sorting-in-the-windows-forms-datagridview-control.md)  
Décrit comment trier les données par programme et comment personnaliser le tri à l’aide de la <xref:System.Windows.Forms.DataGridView.SortCompare?displayProperty=nameWithType> événement ou en implémentant le <xref:System.Collections.IComparer> interface.

## <a name="reference"></a>Référence

<xref:System.Windows.Forms.DataGridView>  
Fournit une documentation de référence pour le contrôle <xref:System.Windows.Forms.DataGridView>.  

<xref:System.Windows.Forms.DataGridView.Sort%2A?displayProperty=nameWithType>  
Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridView.Sort%2A> (méthode).

<xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType>  
Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> propriété.

<xref:System.Windows.Forms.DataGridViewColumnSortMode>  
Fournit la documentation de référence pour le <xref:System.Windows.Forms.DataGridViewColumnSortMode> énumération.

## <a name="see-also"></a>Voir aussi

- [DataGridView, contrôle](datagridview-control-windows-forms.md)
- [Types de colonnes dans le contrôle DataGridView Windows Forms](column-types-in-the-windows-forms-datagridview-control.md)
