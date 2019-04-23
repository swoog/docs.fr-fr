---
title: 'Procédure : Modifier l’alignement horizontal d’une colonne dans un ListView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], horizontal alignment [WPF]
ms.assetid: b9573e44-9dad-4d14-939c-7859ca372758
ms.openlocfilehash: 528a711c1cf7992bb32c0aa4d6e81d71744c9f80
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59102659"
---
# <a name="how-to-change-the-horizontal-alignment-of-a-column-in-a-listview"></a>Procédure : Modifier l’alignement horizontal d’une colonne dans un ListView
Par défaut, le contenu de chaque colonne dans un <xref:System.Windows.Controls.ListViewItem> est alignée à gauche. Vous pouvez modifier l’alignement de chaque colonne en fournissant un <xref:System.Windows.DataTemplate> et en définissant le <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> propriété sur l’élément dans le <xref:System.Windows.DataTemplate>. Cette rubrique montre comment un <xref:System.Windows.Controls.ListView> aligne son contenu par défaut et comment modifier l’alignement d’une colonne dans un <xref:System.Windows.Controls.ListView>.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, les données dans le `Title` et `ISBN` colonnes est alignée à gauche.  
  
 [!code-xaml[ListViewHowTos#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#1)]  
[!code-xaml[ListViewHowTos#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#2)]  
  
 Pour modifier l’alignement de la `ISBN` colonne, vous devez spécifier que le <xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A> propriété de chaque <xref:System.Windows.Controls.ListViewItem> est <xref:System.Windows.HorizontalAlignment.Stretch>, de sorte que les éléments dans chaque <xref:System.Windows.Controls.ListViewItem> peut couvrir ou être positionnés sur toute la largeur de chaque colonne. Étant donné que le <xref:System.Windows.Controls.ListView> est lié à une source de données, vous devez créer un style qui définit le <xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A>. Ensuite, vous devez utiliser un <xref:System.Windows.DataTemplate> pour afficher le contenu au lieu d’utiliser le <xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A> propriété. Pour afficher le `ISBN` de chaque modèle, le <xref:System.Windows.DataTemplate> peut uniquement contenir une <xref:System.Windows.Controls.TextBlock> qui a son <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> propriété définie sur <xref:System.Windows.HorizontalAlignment.Right>.  
  
 L’exemple suivant définit le style et <xref:System.Windows.DataTemplate> nécessaire pour rendre le `ISBN` colonne alignée à droite et les modifications le <xref:System.Windows.Controls.GridViewColumn> pour référencer le <xref:System.Windows.DataTemplate>.  
  
 [!code-xaml[ListViewHowTos#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#3)]  
[!code-xaml[ListViewHowTos#4](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#4)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](../data/data-binding-overview.md)
- [Vue d’ensemble des modèles de données](../data/data-templating-overview.md)
- [Effectuer une liaison à des données XML à l’aide d’un XMLDataProvider et de requêtes XPath](../data/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [Vue d’ensemble de ListView](listview-overview.md)
