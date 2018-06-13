---
title: 'Comment : définir une table avec XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [WPF], defining tables
- documents [WPF], defining tables with XAML
- tables [WPF], defining with XAML
ms.assetid: 83f2dc58-437e-4cdc-b5dd-0019810c7a85
ms.openlocfilehash: 2a35a27567d962fc125cb3c408ccab95afa222af
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33543099"
---
# <a name="how-to-define-a-table-with-xaml"></a>Comment : définir une table avec XAML
L’exemple suivant montre comment définir un <xref:System.Windows.Documents.Table> à l’aide de [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].  L’exemple de tableau a quatre colonnes (représentées par <xref:System.Windows.Documents.TableColumn> éléments) et plusieurs lignes (représenté par <xref:System.Windows.Documents.TableRow> éléments) contenant des données ainsi que le titre, en-tête et les informations de pied de page.  Lignes doivent être contenues dans un <xref:System.Windows.Documents.TableRowGroup> élément.  Chaque ligne dans la table est composée d’une ou plusieurs cellules (représentées par <xref:System.Windows.Documents.TableCell> éléments).  Le contenu dans une cellule de tableau doit être contenu dans un <xref:System.Windows.Documents.Block> élément ; dans ce cas <xref:System.Windows.Documents.Paragraph> les éléments sont utilisés.  Le tableau héberge également un lien hypertexte (représenté par la <xref:System.Windows.Documents.Hyperlink> élément) dans la ligne de pied de page.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[TableSnippetsXAML#_TableXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TableSnippetsXAML/CS/Window1.xaml#_tablexaml)]  
  
 La figure suivante illustre le rendu de la table définie dans cet exemple.  
  
 ![Table affichée.](../../../../docs/framework/wpf/advanced/media/tableeg.png "TableEG")
