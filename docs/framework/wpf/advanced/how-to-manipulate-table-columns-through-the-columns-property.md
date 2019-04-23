---
title: 'Procédure : Manipuler les colonnes d’un tableau avec la propriété Columns'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- documents [WPF], manipulating table columns
- properties [WPF], Columns [WPF], manipulating table columns
- tables [WPF], manipulating columns
- Columns property [WPF]
ms.assetid: 3f8884f4-7e1f-456b-be06-fbd3cf469bf3
ms.openlocfilehash: d379d1a98bff614ff9e16cdd340bb69644988743
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078419"
---
# <a name="how-to-manipulate-a-tables-columns-through-the-columns-property"></a>Procédure : Manipuler les colonnes d’un tableau avec la propriété Columns
Cet exemple montre quelques-unes des opérations plus courantes qui peuvent être effectuées sur les colonnes d’un tableau avec la <xref:System.Windows.Documents.Table.Columns%2A> propriété.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une nouvelle table, puis utilise le <xref:System.Windows.Documents.TableColumnCollection.Add%2A> méthode pour ajouter des colonnes à la table <xref:System.Windows.Documents.Table.Columns%2A> collection.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Add](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_add)]
 [!code-vb[TableSnippets2#_Table_Columns_Add](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_add)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant insère une nouvelle <xref:System.Windows.Documents.TableColumn>.  La nouvelle colonne est insérée à la position d’index 0, rendant la première nouvelle colonne dans la table.  
  
> [!NOTE]
>  Le <xref:System.Windows.Documents.TableColumnCollection> collection utilise l’indexation standard de base zéro.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Insert](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_insert)]
 [!code-vb[TableSnippets2#_Table_Columns_Insert](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_insert)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant accède à quelques propriétés arbitraires sur les colonnes dans le <xref:System.Windows.Documents.TableColumnCollection> collection, qui fait référence à des colonnes particulières par index.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Manip](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_manip)]
 [!code-vb[TableSnippets2#_Table_Columns_Manip](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_manip)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant obtient le nombre de colonnes actuellement hébergées par la table.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Count](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_count)]
 [!code-vb[TableSnippets2#_Table_Columns_Count](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_count)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant supprime une colonne particulière par référence.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_DelRef](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_delref)]
 [!code-vb[TableSnippets2#_Table_Columns_DelRef](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_delref)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant supprime une colonne particulière par index.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_DelIndex](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_delindex)]
 [!code-vb[TableSnippets2#_Table_Columns_DelIndex](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_delindex)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant supprime toutes les colonnes de la collection de colonnes de la table.  
  
 [!code-csharp[TableSnippets2#_Table_Columns_Clear](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippets2/CSharp/Window1.xaml.cs#_table_columns_clear)]
 [!code-vb[TableSnippets2#_Table_Columns_Clear](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TableSnippets2/visualbasic/window1.xaml.vb#_table_columns_clear)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de Table](table-overview.md)
- [Définir une table avec XAML](how-to-define-a-table-with-xaml.md)
- [Générer une table par programmation](how-to-build-a-table-programmatically.md)
- [Manipuler les groupes de lignes d’un tableau avec la propriété RowGroups](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
- [Manipuler un FlowDocument avec la propriété Blocks](how-to-manipulate-a-flowdocument-through-the-blocks-property.md)
- [Manipuler les groupes de lignes d’un tableau avec la propriété RowGroups](how-to-manipulate-table-row-groups-through-the-rowgroups-property.md)
