---
title: 'Procédure : Définir une table avec XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [WPF], defining tables
- documents [WPF], defining tables with XAML
- tables [WPF], defining with XAML
ms.assetid: 83f2dc58-437e-4cdc-b5dd-0019810c7a85
ms.openlocfilehash: 011f612527f0c9e89ec05643edbb95b2d908488c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61776585"
---
# <a name="how-to-define-a-table-with-xaml"></a><span data-ttu-id="82b81-102">Procédure : Définir une table avec XAML</span><span class="sxs-lookup"><span data-stu-id="82b81-102">How to: Define a Table with XAML</span></span>
<span data-ttu-id="82b81-103">L’exemple suivant montre comment définir un <xref:System.Windows.Documents.Table> à l’aide de [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="82b81-103">The following example demonstrates how to define a <xref:System.Windows.Documents.Table> using [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span>  <span data-ttu-id="82b81-104">L’exemple de table a quatre colonnes (représentées par <xref:System.Windows.Documents.TableColumn> éléments) et plusieurs lignes (représentées par <xref:System.Windows.Documents.TableRow> éléments) contenant des données ainsi que le titre, en-tête et informations de pied de page.</span><span class="sxs-lookup"><span data-stu-id="82b81-104">The example table has four columns (represented by <xref:System.Windows.Documents.TableColumn> elements) and several rows (represented by <xref:System.Windows.Documents.TableRow> elements) containing data as well as title, header, and footer information.</span></span>  <span data-ttu-id="82b81-105">Lignes doivent être contenues dans un <xref:System.Windows.Documents.TableRowGroup> élément.</span><span class="sxs-lookup"><span data-stu-id="82b81-105">Rows must be contained in a <xref:System.Windows.Documents.TableRowGroup> element.</span></span>  <span data-ttu-id="82b81-106">Chaque ligne dans la table est composée d’une ou plusieurs cellules (représentées par <xref:System.Windows.Documents.TableCell> éléments).</span><span class="sxs-lookup"><span data-stu-id="82b81-106">Each row in the table is comprised of one or more cells (represented by <xref:System.Windows.Documents.TableCell> elements).</span></span>  <span data-ttu-id="82b81-107">Contenu dans une cellule de tableau doit être contenu dans un <xref:System.Windows.Documents.Block> élément ; dans ce cas <xref:System.Windows.Documents.Paragraph> éléments sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="82b81-107">Content in a table cell must be contained in a <xref:System.Windows.Documents.Block> element; in this case <xref:System.Windows.Documents.Paragraph> elements are used.</span></span>  <span data-ttu-id="82b81-108">La table héberge également un lien hypertexte (représenté par la <xref:System.Windows.Documents.Hyperlink> élément) dans la ligne de pied de page.</span><span class="sxs-lookup"><span data-stu-id="82b81-108">The table also hosts a hyperlink (represented by the <xref:System.Windows.Documents.Hyperlink> element) in the footer row.</span></span>  
  
## <a name="example"></a><span data-ttu-id="82b81-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="82b81-109">Example</span></span>  
 [!code-xaml[TableSnippetsXAML#_TableXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippetsXAML/CS/Window1.xaml#_tablexaml)]  
  
 <span data-ttu-id="82b81-110">La figure suivante montre le rendu de la table définie dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="82b81-110">The following figure shows how the table defined in this example renders:</span></span>  
  
 ![Capture d’écran d’une table définie avec XAML.](./media/how-to-define-a-table-with-xaml/planetary-information-xaml-table.png)
