---
title: 'Procédure : Effectuer une liaison à une collection et afficher des informations basées sur la sélection'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data collections [WPF], selecting data for views
- data binding [WPF], creating views of data collections
- data binding [WPF], selecting data for views
- data binding [WPF], binding to collections
ms.assetid: 952a7d76-dd29-49e5-86f5-32c4530e70eb
ms.openlocfilehash: bb7d4c89e63982a3052857dcb50d04d36d9517dd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59314388"
---
# <a name="how-to-bind-to-a-collection-and-display-information-based-on-selection"></a>Procédure : Effectuer une liaison à une collection et afficher des informations basées sur la sélection
Dans un scénario maître / détail simple, vous avez lié aux données <xref:System.Windows.Controls.ItemsControl> comme un <xref:System.Windows.Controls.ListBox>. En fonction de sélection de l’utilisateur, afficher plus d’informations sur l’élément sélectionné. Cet exemple montre comment implémenter ce scénario.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, `People` est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de `Person` classes. Cela `Person` classe contient trois propriétés : `FirstName`, `LastName`, et `HomeTown`, tous du type `string`.  
  
 [!code-xaml[CollectionBinding#Source](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#source)]  
[!code-xaml[CollectionBinding#UI](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#ui)]  
  
 Le <xref:System.Windows.Controls.ContentControl> utilise les éléments suivants <xref:System.Windows.DataTemplate> qui définit comment les informations d’un `Person` est présenté :  
  
 [!code-xaml[CollectionBinding#DetailTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#detailtemplate)]  
  
 Voici une capture d’écran de ce que l’exemple se produit. Le <xref:System.Windows.Controls.ContentControl> présente les autres propriétés de la personne sélectionnée.  
  
 ![Liaison à une collection](./media/databinding-collectionbindingsample.png "DataBinding_CollectionBindingSample")  
  
 Les deux choses à noter dans cet exemple sont :  
  
1. Le <xref:System.Windows.Controls.ListBox> et <xref:System.Windows.Controls.ContentControl> lier à la même source. Le <xref:System.Windows.Data.Binding.Path%2A> propriétés des deux liaisons ne sont pas spécifiées, car les deux contrôles sont une liaison à l’objet d’ensemble de la collection.  
  
2. Vous devez définir le <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> propriété `true` pour ce faire. Définition de cette propriété garantit que l’élément sélectionné est toujours défini en tant que le <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>. Ou bien, si le <xref:System.Windows.Controls.ListBox> obtient ses données à partir d’un <xref:System.Windows.Data.CollectionViewSource>, il synchronise automatiquement sélection et la devise.  
  
 Notez que le `Person` substitue le `ToString` méthode la façon suivante. Par défaut, le <xref:System.Windows.Controls.ListBox> appels `ToString` et affiche une représentation sous forme de chaîne de chaque objet dans la collection liée. C’est pourquoi chaque `Person` apparaît sous la forme d’un prénom dans le <xref:System.Windows.Controls.ListBox>.  
  
 [!code-csharp[CollectionBinding#ToString](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Data.cs#tostring)]
 [!code-vb[CollectionBinding#ToString](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionBinding/VisualBasic/Person.vb#tostring)]  
  
## <a name="see-also"></a>Voir aussi

- [Utiliser le modèle maître/détail avec des données hiérarchiques](how-to-use-the-master-detail-pattern-with-hierarchical-data.md)
- [Utiliser le modèle maître/détail avec des données XML hiérarchiques](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Vue d’ensemble des modèles de données](data-templating-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
