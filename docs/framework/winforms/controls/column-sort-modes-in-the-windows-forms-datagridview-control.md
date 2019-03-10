---
title: Modes de tri des colonnes du contrôle DataGridView Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], sort modes
- DataGridView control [Windows Forms], sort mode
ms.assetid: 43715887-2df9-4da7-bcf1-b9c7c842b2bf
ms.openlocfilehash: 935251c783bbe74903cee6afd5e14eed4483d69d
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57717854"
---
# <a name="column-sort-modes-in-the-windows-forms-datagridview-control"></a>Modes de tri des colonnes du contrôle DataGridView Windows Forms
<xref:System.Windows.Forms.DataGridView> colonnes ont trois modes de tri. Le mode de tri pour chaque colonne est spécifié via le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> propriété de la colonne, qui peut être définie à une des opérations suivantes <xref:System.Windows.Forms.DataGridViewColumnSortMode> valeurs d’énumération.  
  
|Valeur`DataGridViewColumnSortMode` |Description|  
|----------------------------------------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewColumnSortMode.Automatic>|Par défaut pour les colonnes de zone de texte. À moins que les en-têtes de colonne sont utilisés pour la sélection, en cliquant sur l’en-tête de colonne automatiquement trie le <xref:System.Windows.Forms.DataGridView> par cette colonne et afficher un glyphe qui indique l’ordre de tri.|  
|<xref:System.Windows.Forms.DataGridViewColumnSortMode.NotSortable>|Par défaut pour les colonnes de la zone de texte non –. Vous pouvez trier cette colonne par programme. Toutefois, il n’est pas conçu pour le tri, donc aucun espace n’est réservé pour le glyphe de tri.|  
|<xref:System.Windows.Forms.DataGridViewColumnSortMode.Programmatic>|Vous pouvez trier cette colonne par programmation, et l’espace est réservé pour le glyphe de tri.|  
  
 Vous pouvez souhaiter modifier le mode de tri pour une colonne par défaut est <xref:System.Windows.Forms.DataGridViewColumnSortMode.NotSortable> si elle contient des valeurs qui peuvent être triées. Par exemple, si vous avez une colonne de base de données contenant des nombres qui représentent des États d’élément, vous pouvez afficher ces nombres comme icônes correspondantes en liant une colonne d’image à la colonne de base de données. Vous pouvez ensuite modifier les valeurs de cellules numériques en valeurs d’affichage image dans un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.CellFormatting?displayProperty=nameWithType> événement. Dans ce cas, en définissant le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> propriété <xref:System.Windows.Forms.DataGridViewColumnSortMode.Automatic> permettra à vos utilisateurs trier la colonne. Le tri automatique permettra à vos utilisateurs pour regrouper des éléments qui ont le même état, même si les États correspondant aux numéros n’ont pas une séquence naturelle. Colonnes de la case à cocher sont un autre exemple où le tri automatique est utile pour regrouper des éléments dans le même état.  
  
 Vous pouvez trier une <xref:System.Windows.Forms.DataGridView> par programme en fonction des valeurs dans n’importe quelle colonne ou de plusieurs colonnes, quel que soit le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> paramètres. Tri par programmation est utile lorsque vous souhaitez fournir votre propre interface utilisateur (IU) pour le tri, ou lorsque vous souhaitez implémenter le tri personnalisé. En fournissant votre propre interface utilisateur de tri est utile, par exemple, lorsque vous définissez le <xref:System.Windows.Forms.DataGridView> en mode de sélection pour activer la sélection d’en-tête de colonne. Dans ce cas, bien que les en-têtes de colonne ne peut pas être utilisés pour le tri, voulez-vous les en-têtes pour afficher le glyphe de tri approprié, afin que vous puissiez attribuer le <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> propriété <xref:System.Windows.Forms.DataGridViewColumnSortMode.Programmatic>.  
  
 Les colonnes en mode de tri par programme n’affichent pas automatiquement un glyphe de tri. Pour ces colonnes, vous devez afficher le glyphe vous-même en définissant le <xref:System.Windows.Forms.DataGridViewColumnHeaderCell.SortGlyphDirection%2A?displayProperty=nameWithType> propriété. Cela est nécessaire si vous voulez une flexibilité de tri personnalisé. Par exemple, si vous triez le <xref:System.Windows.Forms.DataGridView> par plusieurs colonnes, vous pouvez souhaiter afficher plusieurs glyphes de tri ou aucun glyphe de tri.  
  
 Bien que vous pouvez trier par programme un <xref:System.Windows.Forms.DataGridView> par n’importe quelle colonne, certaines colonnes, tels que des colonnes de bouton, ne peuvent pas contenir les valeurs qui peuvent être triées. Pour ces colonnes, une <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> paramètre la propriété <xref:System.Windows.Forms.DataGridViewColumnSortMode.NotSortable> indique qu’il ne sera jamais utilisé pour le tri, il est donc pas nécessaire de réserver l’espace dans l’en-tête pour le glyphe de tri.  
  
 Quand un <xref:System.Windows.Forms.DataGridView> est triée, vous pouvez déterminer la colonne de tri et l’ordre de tri en vérifiant les valeurs de la <xref:System.Windows.Forms.DataGridView.SortedColumn%2A> et <xref:System.Windows.Forms.DataGridView.SortOrder%2A> propriétés. Ces valeurs ne sont pas significatifs après une opération de tri personnalisée. Pour plus d’informations sur le tri personnalisé, consultez la section tri personnalisé plus loin dans cette rubrique.  
  
 Quand un <xref:System.Windows.Forms.DataGridView> contrôle contenant des colonnes dépendantes et indépendantes est trié, les valeurs dans les colonnes indépendantes ne peut pas être gérés automatiquement. Pour conserver ces valeurs, vous devez implémenter le mode virtuel en définissant le <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété `true` et la gestion de la <xref:System.Windows.Forms.DataGridView.CellValueNeeded> et <xref:System.Windows.Forms.DataGridView.CellValuePushed> événements. Pour plus d'informations, voir [Procédure : Implémenter le Mode virtuel dans les Windows Forms DataGridView Control](how-to-implement-virtual-mode-in-the-windows-forms-datagridview-control.md). Tri par colonnes indépendantes en mode dépendant n’est pas pris en charge.  
  
## <a name="programmatic-sorting"></a>Tri par programmation  
 Vous pouvez trier une <xref:System.Windows.Forms.DataGridView> par programmation en appelant son <xref:System.Windows.Forms.DataGridView.Sort%2A> (méthode).  
  
 Le `Sort(DataGridViewColumn,ListSortDirection)` surcharge de la <xref:System.Windows.Forms.DataGridView.Sort%2A> méthode prend un <xref:System.Windows.Forms.DataGridViewColumn> et un <xref:System.ComponentModel.ListSortDirection> valeur d’énumération en tant que paramètres. Cette surcharge est utile lors du tri des colonnes avec des valeurs qui peuvent être triées, mais que vous ne souhaitez pas configurer pour le tri automatique. Lorsque vous appelez cette surcharge et passer dans une colonne avec un <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A> valeur de propriété de <xref:System.Windows.Forms.DataGridViewColumnSortMode.Automatic?displayProperty=nameWithType>, le <xref:System.Windows.Forms.DataGridView.SortedColumn%2A> et <xref:System.Windows.Forms.DataGridView.SortOrder%2A> propriétés sont définies automatiquement et le glyphe de tri approprié apparaît dans l’en-tête de colonne.  
  
> [!NOTE]
>  Lorsque le <xref:System.Windows.Forms.DataGridView> contrôle est lié à une source de données externe en définissant le <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété, le `Sort(DataGridViewColumn,ListSortDirection)` surcharge de méthode ne fonctionne pas pour les colonnes indépendantes. En outre, lorsque le <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> propriété est `true`, vous pouvez appeler cette surcharge uniquement pour les colonnes dépendantes. Pour déterminer si une colonne est liée aux données, vérifiez le <xref:System.Windows.Forms.DataGridViewColumn.IsDataBound%2A> valeur de propriété. Tri des colonnes indépendantes en mode dépendant n’est pas pris en charge.  
  
## <a name="custom-sorting"></a>Tri personnalisé  
 Vous pouvez personnaliser <xref:System.Windows.Forms.DataGridView> à l’aide de la `Sort(IComparer)` surcharge de la <xref:System.Windows.Forms.DataGridView.Sort%2A> méthode ou en gérant le <xref:System.Windows.Forms.DataGridView.SortCompare> événement.  
  
 Le `Sort(IComparer)` surcharge de méthode prend une instance d’une classe qui implémente le <xref:System.Collections.IComparer> interface en tant que paramètre. Cette surcharge est utile lorsque vous souhaitez fournir un tri personnalisé ; par exemple, lorsque les valeurs dans une colonne n’ont pas un ordre de tri naturel ou lorsque l’ordre de tri naturel est inapproprié. Dans ce cas, vous ne pouvez pas utiliser le tri automatique, mais vous pouvez cependant souhaiter vos utilisateurs à trier en cliquant sur les en-têtes de colonne. Vous pouvez appeler cette surcharge dans un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.ColumnHeaderMouseClick> événements si vous n’utilisez pas les en-têtes de colonne pour la sélection.  
  
> [!NOTE]
>  Le `Sort(IComparer)` surcharge de méthode fonctionne uniquement lorsque le <xref:System.Windows.Forms.DataGridView> contrôle n’est pas lié à une source de données externe et le <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> valeur de propriété est `false`. Pour personnaliser le tri pour les colonnes liées à une source de données externe, vous devez utiliser les opérations de tri fournies par la source de données. En mode virtuel, vous devez fournir vos propres opérations de tri pour les colonnes indépendantes.  
  
 Pour utiliser le `Sort(IComparer)` surcharge de méthode, vous devez créer votre propre classe qui implémente le <xref:System.Collections.IComparer> interface. Cette interface nécessite que votre classe implémente la <xref:System.Collections.IComparer.Compare%2A?displayProperty=nameWithType> méthode, à laquelle le <xref:System.Windows.Forms.DataGridView> passe <xref:System.Windows.Forms.DataGridViewRow> objets comme entrée quand le `Sort(IComparer)` surcharge de méthode est appelée. Avec cela, vous pouvez calculer l’ordre correct des lignes en fonction des valeurs dans n’importe quelle colonne.  
  
 Le `Sort(IComparer)` surcharge de méthode ne définit pas le <xref:System.Windows.Forms.DataGridView.SortedColumn%2A> et <xref:System.Windows.Forms.DataGridView.SortOrder%2A> propriétés, vous devez donc toujours définir le <xref:System.Windows.Forms.DataGridViewColumnHeaderCell.SortGlyphDirection%2A?displayProperty=nameWithType> propriété à afficher le glyphe de tri.  
  
 Comme alternative à la `Sort(IComparer)` surcharge de méthode, vous pouvez fournir un tri personnalisé en implémentant un gestionnaire pour le <xref:System.Windows.Forms.DataGridView.SortCompare> événement. Cet événement se produit lorsque les utilisateurs cliquent sur les en-têtes de colonnes configurés pour le tri automatique ou lorsque vous appelez le `Sort(DataGridViewColumn,ListSortDirection)` surcharge de la <xref:System.Windows.Forms.DataGridView.Sort%2A> (méthode). L’événement se produit pour chaque paire de lignes dans le contrôle, ce qui vous permet de calculer leur ordre correct.  
  
> [!NOTE]
>  Le <xref:System.Windows.Forms.DataGridView.SortCompare> événement ne se produit pas lorsque le <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriété est définie ou lorsque la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> valeur de propriété est `true`.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.Sort%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.SortedColumn%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridView.SortOrder%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumn.SortMode%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.DataGridViewColumnHeaderCell.SortGlyphDirection%2A?displayProperty=nameWithType>
- [Tri des données dans le contrôle DataGridView Windows Forms](sorting-data-in-the-windows-forms-datagridview-control.md)
- [Guide pratique pour Définir les Modes de tri des colonnes dans le contrôle de DataGridView Windows Forms](set-the-sort-modes-for-columns-wf-datagridview-control.md)
- [Guide pratique pour Personnaliser le tri dans le contrôle DataGridView Windows Forms](how-to-customize-sorting-in-the-windows-forms-datagridview-control.md)
