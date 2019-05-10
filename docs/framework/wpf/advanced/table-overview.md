---
title: Vue d'ensemble de Table
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flow content elements [WPF], Table
- documents [WPF], tables
- tables [WPF]
ms.assetid: 5e1105f4-8fc4-473a-ba55-88c8e71386e6
ms.openlocfilehash: 01ab11d8e3c1d2c84514770816ca9c9eab0835b6
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64649189"
---
# <a name="table-overview"></a>Vue d'ensemble de Table
<xref:System.Windows.Documents.Table> est un élément de niveau bloc qui prend en charge sous forme de grille de présentation du contenu de document dynamique. La flexibilité de cet élément est très utile, mais rend plus difficiles sa compréhension et son utilisation.  
  
 Cette rubrique contient les sections suivantes.  
  
- [Principes de base de l’élément Table](#table_basics)  
  
- [Différences entre l’élément Table et l’élément Grid](#table_vs_Grid)  
  
- [Structure de base de l’élément Table](#basic_table_structure)  
  
- [Imbrication des tables](#table_containment)  
  
- [Regroupements de lignes](#row_groupings)  
  
- [Priorité du rendu en arrière-plan](#rendering_precedence)  
  
- [Étendue des lignes et des colonnes](#spanning_rows_or_columns)  
  
- [Génération d’une table avec du code](#building_a_table_with_code)  
  
- [Rubriques connexes] 
  
<a name="table_basics"></a>   
## <a name="table-basics"></a>Principes de base de l’élément Table  
  
<a name="table_vs_Grid"></a>   
### <a name="how-is-table-different-then-grid"></a>Différences entre l’élément Table et l’élément Grid  
 <xref:System.Windows.Documents.Table> et <xref:System.Windows.Controls.Grid> partagent des fonctionnalités communes, mais chacun est idéale pour différents scénarios. Un <xref:System.Windows.Documents.Table> est conçu pour être utilisé dans du contenu dynamique (voir [vue d’ensemble du Document de flux](flow-document-overview.md) pour plus d’informations sur le contenu dynamique). Les éléments Grid sont mieux adaptés à une utilisation dans des formulaires (autrement dit, partout, sauf dans du contenu dynamique). Au sein d’un <xref:System.Windows.Documents.FlowDocument>, <xref:System.Windows.Documents.Table> les comportements de contenu tels que la pagination, Redisposition et lors de la sélection de contenu de flux prend en charge un <xref:System.Windows.Controls.Grid> pas. Un <xref:System.Windows.Controls.Grid> quant à eux, est mieux utilisées en dehors d’un <xref:System.Windows.Documents.FlowDocument> pour de nombreuses raisons, y compris <xref:System.Windows.Controls.Grid> ajoute des éléments basés sur un index de ligne et de colonne, <xref:System.Windows.Documents.Table> pas. Le <xref:System.Windows.Controls.Grid> élément autorise la superposition de contenu enfant, et plusieurs éléments d’exister dans une même « cellule ». <xref:System.Windows.Documents.Table> ne prend pas en charge la superposition. Éléments enfants d’un <xref:System.Windows.Controls.Grid> peuvent être positionnés par rapport à la zone de leurs limites de « cellule ». <xref:System.Windows.Documents.Table> ne prend pas en charge cette fonctionnalité. Enfin, un <xref:System.Windows.Controls.Grid> requiert moins de ressources, puis un <xref:System.Windows.Documents.Table> par conséquent, envisagez d’utiliser un <xref:System.Windows.Controls.Grid> pour améliorer les performances.  
  
<a name="basic_table_structure"></a>   
### <a name="basic-table-structure"></a>Structure de base de l’élément Table  
 <xref:System.Windows.Documents.Table> Fournit une présentation sous forme de grille composée de colonnes (représentées par <xref:System.Windows.Documents.TableColumn> éléments) et des lignes (représentées par <xref:System.Windows.Documents.TableRow> éléments). <xref:System.Windows.Documents.TableColumn> éléments n’hébergent pas de contenu ; ils définissent simplement les colonnes et les caractéristiques des colonnes. <xref:System.Windows.Documents.TableRow> les éléments doivent être hébergés dans un <xref:System.Windows.Documents.TableRowGroup> élément, qui définit un regroupement de lignes pour la table. <xref:System.Windows.Documents.TableCell> éléments qui contiennent le contenu devant être présenté dans la table, doivent être hébergés dans un <xref:System.Windows.Documents.TableRow> élément. <xref:System.Windows.Documents.TableCell> peut uniquement contenir des éléments qui dérivent de <xref:System.Windows.Documents.Block>.  Les éléments enfants valides pour un <xref:System.Windows.Documents.TableCell> inclure.  
  
- <xref:System.Windows.Documents.BlockUIContainer>  
  
- <xref:System.Windows.Documents.List>  
  
- <xref:System.Windows.Documents.Paragraph>  
  
- <xref:System.Windows.Documents.Section>  
  
- <xref:System.Windows.Documents.Table>  
  
> [!NOTE]
>  <xref:System.Windows.Documents.TableCell> éléments ne peuvent pas héberger directement le contenu de texte. Pour plus d’informations sur les règles de relation contenant-contenu de flux tels que les éléments de contenu <xref:System.Windows.Documents.TableCell>, consultez [vue d’ensemble du Document de flux](flow-document-overview.md).  
  
> [!NOTE]
>  <xref:System.Windows.Documents.Table> est similaire à la <xref:System.Windows.Controls.Grid> élément mais comprend davantage de fonctions et, par conséquent, requiert une charge importante de ressources.  
  
 L’exemple suivant définit une table 2 x 3 simple avec [!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)].  
  
 [!code-xaml[TableSnippets2#_Table_BasicLayout](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_basiclayout)]  
  
 La figure suivante montre le rendu de cet exemple.  
  
 ![Capture d’écran montre le rendu d’une table de base.](./media/table-overview/basic-table-render-example.png)  
  
<a name="table_containment"></a>   
### <a name="table-containment"></a>Imbrication des tables  
 <xref:System.Windows.Documents.Table> dérive le <xref:System.Windows.Documents.Block> élément et respecte les règles communes applicables <xref:System.Windows.Documents.Block> éléments de niveau.  Un <xref:System.Windows.Documents.Table> élément peut être contenu par chacun des éléments suivants :  
  
- <xref:System.Windows.Documents.FlowDocument>  
  
- <xref:System.Windows.Documents.TableCell>  
  
- <xref:System.Windows.Controls.ListBoxItem>  
  
- <xref:System.Windows.Controls.ListViewItem>  
  
- <xref:System.Windows.Documents.Section>  
  
- <xref:System.Windows.Documents.Floater>  
  
- <xref:System.Windows.Documents.Figure>  
  
<a name="row_groupings"></a>   
### <a name="row-groupings"></a>Regroupements de lignes  
 Le <xref:System.Windows.Documents.TableRowGroup> élément permet de regrouper arbitrairement des lignes dans une table ; chaque ligne dans une table doit appartenir à un regroupement de lignes.  Les lignes qui sont regroupées ont souvent un but commun et il est donc possible d’appliquer un style à l’ensemble du regroupement.  Il est courant, pour les regroupements de lignes, de séparer les lignes spéciales, telles que les titres, les en-têtes et les pieds de page, du contenu principal de la table.  
  
 L’exemple suivant utilise [!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)] pour définir une table avec des lignes d’en-tête et de pied de page stylisées.  
  
 [!code-xaml[TableSnippets2#_Table_RowGroups](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_rowgroups)]  
  
 La figure suivante montre le rendu de cet exemple.  
  
 ![Capture d’écran : Groupes de lignes de table](./media/table-rowgroups.png "Table_RowGroups")  
  
<a name="rendering_precedence"></a>   
### <a name="background-rendering-precedence"></a>Priorité du rendu en arrière-plan  
 Les éléments de la table sont affichés dans l’ordre suivant (dans l’ordre de plan, du plus bas au plus haut). Cet ordre ne peut pas être modifié. Par exemple, il n’existe pas de propriété « Ordre de plan » que vous pourriez utiliser pour remplacer l’ordre établi.  
  
1. <xref:System.Windows.Documents.Table>  
  
2. <xref:System.Windows.Documents.TableColumn>  
  
3. <xref:System.Windows.Documents.TableRowGroup>  
  
4. <xref:System.Windows.Documents.TableRow>  
  
5. <xref:System.Windows.Documents.TableCell>  
  
 Prenons l’exemple suivant, qui définit des couleurs d’arrière-plan dans une table pour chacun de ces éléments.  
  
 [!code-xaml[TableSnippets2#_Table_ZOrder](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_zorder)]  
  
 La figure suivante montre comment s’affiche cet exemple (seules les couleurs d’arrière-plan sont affichées).  
  
 ![Capture d’écran : Table z&#45;ordre](./media/table-zorder.png "Table_ZOrder")  
  
<a name="spanning_rows_or_columns"></a>   
### <a name="spanning-rows-or-columns"></a>Étendue des lignes et des colonnes  
 Cellules de tableau peuvent être configurées pour couvrir plusieurs lignes ou colonnes à l’aide de la <xref:System.Windows.Documents.TableCell.RowSpan%2A> ou <xref:System.Windows.Documents.TableCell.ColumnSpan%2A> des attributs, respectivement.  
  
 Prenons l’exemple suivant, dans lequel une cellule s’étend sur trois colonnes.  
  
 [!code-xaml[TableSnippets2#_Table_ColumnSpan](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml#_table_columnspan)]  
  
 La figure suivante montre le rendu de cet exemple.  
  
 ![Capture d’écran : Cellule s’étendant sur toutes les colonnes de trois](./media/table-columnspan.png "Table_ColumnSpan")  
  
<a name="building_a_table_with_code"></a>   
## <a name="building-a-table-with-code"></a>Génération d’une table avec du code  
 Les exemples suivants montrent comment créer par programmation un <xref:System.Windows.Documents.Table> et le remplir avec le contenu. Le contenu de la table est réparti en cinq lignes (représentées par <xref:System.Windows.Documents.TableRow> objets contenus dans un <xref:System.Windows.Documents.Table.RowGroups%2A> objet) et six colonnes (représentées par <xref:System.Windows.Documents.TableColumn> objets). Les lignes sont utilisées pour différentes présentations, par exemple une ligne de titre prévue pour intituler l’ensemble de la table, une ligne d’en-tête pour décrire les colonnes de données d’une table ou une ligne de pied de page avec des informations de synthèse.  Notez que les lignes de titre, d’en-tête et de pied de page ne sont pas inhérentes à la table. Il s’agit simplement de lignes présentant des caractéristiques différentes. Cellules de tableau contiennent le contenu réel, ce qui peut être composé de texte, images ou presque n’importe quel autre [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] élément.  
  
 Tout d’abord, un <xref:System.Windows.Documents.FlowDocument> est créé pour héberger le <xref:System.Windows.Documents.Table>, ainsi qu’un nouveau <xref:System.Windows.Documents.Table> est créé et ajouté au contenu de la <xref:System.Windows.Documents.FlowDocument>.  
  
 [!code-csharp[TableSnippets#_TableCreate](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tablecreate)]
 [!code-vb[TableSnippets#_TableCreate](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tablecreate)]  
  
 Ensuite, six <xref:System.Windows.Documents.TableColumn> objets sont créés et ajoutés à la table <xref:System.Windows.Documents.Table.Columns%2A> collection avec une mise en forme.  
  
> [!NOTE]
>  Notez que la table <xref:System.Windows.Documents.Table.Columns%2A> collection utilise l’indexation standard de base zéro.  
  
 [!code-csharp[TableSnippets#_TableCreateColumns](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tablecreatecolumns)]
 [!code-vb[TableSnippets#_TableCreateColumns](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tablecreatecolumns)]  
  
 Ensuite, une ligne de titre est créée, puis ajoutée à la table avec une mise en forme.  La ligne de titre contient une seule cellule qui s’étend sur les six colonnes de la table.  
  
 [!code-csharp[TableSnippets#_TableAddTitleRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddtitlerow)]
 [!code-vb[TableSnippets#_TableAddTitleRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddtitlerow)]  
  
 Ensuite, une ligne d’en-tête est créée, puis ajoutée à la table, et les cellules de la ligne d’en-tête sont créées, puis remplies avec le contenu.  
  
 [!code-csharp[TableSnippets#_TableAddHeaderRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddheaderrow)]
 [!code-vb[TableSnippets#_TableAddHeaderRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddheaderrow)]  
  
 Ensuite, une ligne de données est créée, puis ajoutée à la table, et les cellules de cette ligne sont créées, puis remplies avec le contenu.  La génération de cette ligne est similaire à la création de la ligne d’en-tête. Cependant, la mise en forme appliquée est légèrement différente.  
  
 [!code-csharp[TableSnippets#_TableAddDataRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableadddatarow)]
 [!code-vb[TableSnippets#_TableAddDataRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableadddatarow)]  
  
 Enfin, une ligne de pied de page est créée, ajoutée, puis mise en forme.  Tout comme la ligne de titre, le pied de page contient une seule cellule qui s’étend sur les six colonnes de la table.  
  
 [!code-csharp[TableSnippets#_TableAddFooterRow](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets/CSharp/Table.cs#_tableaddfooterrow)]
 [!code-vb[TableSnippets#_TableAddFooterRow](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets/VisualBasic/Table.vb#_tableaddfooterrow)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des documents dynamiques](flow-document-overview.md)
- [Définir une table avec XAML](how-to-define-a-table-with-xaml.md)
- [Documents dans WPF](documents-in-wpf.md)
- [Utiliser les éléments de contenu de flux](how-to-use-flow-content-elements.md)
