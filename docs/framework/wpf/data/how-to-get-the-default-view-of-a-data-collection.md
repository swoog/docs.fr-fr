---
title: 'Procédure : Obtenir la vue par défaut d’une collection de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data collections [WPF], creating views of
- data binding [WPF], creating views of data collections
ms.assetid: b641e96c-c2f6-42ea-9c5d-bac81176ad65
ms.openlocfilehash: 746331e69ee1e5eee795a0e35202f4889b72c53f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931508"
---
# <a name="how-to-get-the-default-view-of-a-data-collection"></a>Procédure : Obtenir la vue par défaut d’une collection de données
Les vues permettent à la même collection de données de différentes façons, en fonction de tri, filtrage ou des critères de regroupement. Chaque collection a un affichage par défaut partagé, qui est utilisé comme source de liaison réelle lorsqu’une liaison spécifie une collection comme source. Cet exemple montre comment obtenir la vue par défaut d’une collection.  
  
## <a name="example"></a>Exemple  
 Pour créer la vue, vous avez besoin d’une référence d’objet à la collection. Cet objet de données peut être obtenu en faisant référence à votre propre objet code-behind, en obtenant le contexte de données, en obtenant une propriété de la source de données, ou en obtenant une propriété de la liaison. Cet exemple montre comment obtenir le <xref:System.Windows.FrameworkElement.DataContext%2A> d’un objet de données et l’utiliser pour obtenir directement la collection par défaut afficher pour cette collection.  
  
 [!code-csharp[CollectionView#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#2)]
 [!code-vb[CollectionView#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#2)]  
  
 Dans cet exemple, l’élément racine est un <xref:System.Windows.Controls.StackPanel>. Le <xref:System.Windows.FrameworkElement.DataContext%2A> a la valeur *myDataSource*, qui fait référence à un fournisseur de données est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de *ordre* objets.  
  
 [!code-xaml[CollectionView#CollectionViewDataContext](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml#collectionviewdatacontext)]  
  
 Ou bien, vous pouvez instancier et lier à votre propre vue de collection en utilisant la <xref:System.Windows.Data.CollectionViewSource> classe. Cette vue de collection est partagée uniquement par les contrôles liés directement. Pour obtenir un exemple, consultez la section Comment créer une vue dans le [vue d’ensemble de la liaison de données](data-binding-overview.md).  
  
 Pour obtenir des exemples des fonctionnalités fournies par une vue de collection, consultez [trier des données dans une vue](how-to-sort-data-in-a-view.md), [filtrer des données dans une vue](how-to-filter-data-in-a-view.md), et [naviguer dans les objets d’un CollectionView de données](how-to-navigate-through-the-objects-in-a-data-collectionview.md).  
  
## <a name="see-also"></a>Voir aussi

- [Trier et grouper des données à l'aide d'une vue en XAML](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
