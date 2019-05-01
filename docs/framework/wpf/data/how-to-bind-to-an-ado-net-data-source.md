---
title: 'Procédure : Effectuer une liaison à une source de données ADO.NET'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], binding to ADO.NET data sources
- ADO.NET data sources [WPF], binding to
- binding [WPF], to ADO.NET data sources
ms.assetid: a70c6d7b-7b38-4fdf-b655-4804db7c8315
ms.openlocfilehash: 08933e67c2cc4b7ccfb6ae0c9dfde34f40e4e5f5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62021040"
---
# <a name="how-to-bind-to-an-adonet-data-source"></a>Procédure : Effectuer une liaison à une source de données ADO.NET

Cet exemple montre comment lier un [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] <xref:System.Windows.Controls.ListBox> le contrôle à un [!INCLUDE[TLA#tla_adonet](../../../../includes/tlasharptla-adonet-md.md)] `DataSet`.

## <a name="example"></a>Exemple

Dans cet exemple, un objet `OleDbConnection` est utilisé pour se connecter à la source de données qui est un fichier `Access MDB` spécifié dans la chaîne de connexion. Une fois la connexion établie, un objet `OleDbDataAdapter` est créé. L’objet `OleDbDataAdapter` exécute une instruction select [!INCLUDE[TLA#tla_sql](../../../../includes/tlasharptla-sql-md.md)] pour extraire le recordset de la base de données. Les résultats de la commande [!INCLUDE[TLA2#tla_sql](../../../../includes/tla2sharptla-sql-md.md)] sont stockés dans une `DataTable` du `DataSet` en appelant la méthode `Fill` de l’`OleDbDataAdapter`. Dans cet exemple, la `DataTable` est nommée `BookTable`. L’exemple définit ensuite la <xref:System.Windows.FrameworkElement.DataContext%2A> propriété de la <xref:System.Windows.Controls.ListBox> à la `DataSet` objet.

[!code-csharp[ADODataSet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml.cs#1)]
[!code-vb[ADODataSet#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ADODataSet/VisualBasic/Window1.xaml.vb#1)]

Vous pouvez ensuite lier le <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> propriété de la <xref:System.Windows.Controls.ListBox> à `BookTable` de la `DataSet`:

[!code-xaml[ADODataSet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml#2)]

`BookItemTemplate` est le <xref:System.Windows.DataTemplate> qui définit comment les données s’affichent :

[!code-xaml[ADODataSet#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml#3)]

`IntColorConverter` convertit un `int` en une couleur. Avec l’utilisation de ce convertisseur, le <xref:System.Windows.Controls.TextBlock.Background%2A> couleur du troisième <xref:System.Windows.Controls.TextBlock> apparaît en vert si la valeur de `NumPages` est inférieure à 350 et rouge dans le cas contraire. L’implémentation du convertisseur n’est pas décrite ici.

## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Data.BindingListCollectionView>
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
