---
title: 'Procédure : Définir une table avec XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [WPF], defining tables
- documents [WPF], defining tables with XAML
- tables [WPF], defining with XAML
ms.assetid: 83f2dc58-437e-4cdc-b5dd-0019810c7a85
ms.openlocfilehash: 7398af6fddae56238e1af3ee4e726420c01ab7ea
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57376921"
---
# <a name="how-to-define-a-table-with-xaml"></a>Procédure : Définir une table avec XAML
L’exemple suivant montre comment définir un <xref:System.Windows.Documents.Table> à l’aide de [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].  L’exemple de table a quatre colonnes (représentées par <xref:System.Windows.Documents.TableColumn> éléments) et plusieurs lignes (représentées par <xref:System.Windows.Documents.TableRow> éléments) contenant des données ainsi que le titre, en-tête et informations de pied de page.  Lignes doivent être contenues dans un <xref:System.Windows.Documents.TableRowGroup> élément.  Chaque ligne dans la table est composée d’une ou plusieurs cellules (représentées par <xref:System.Windows.Documents.TableCell> éléments).  Contenu dans une cellule de tableau doit être contenu dans un <xref:System.Windows.Documents.Block> élément ; dans ce cas <xref:System.Windows.Documents.Paragraph> éléments sont utilisés.  La table héberge également un lien hypertexte (représenté par la <xref:System.Windows.Documents.Hyperlink> élément) dans la ligne de pied de page.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[TableSnippetsXAML#_TableXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippetsXAML/CS/Window1.xaml#_tablexaml)]  
  
 La figure suivante illustre le rendu de la table définie dans cet exemple.  
  
 ![Table affichée.](./media/tableeg.png "TableEG")
