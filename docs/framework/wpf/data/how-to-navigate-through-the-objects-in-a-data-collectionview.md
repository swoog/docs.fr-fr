---
title: 'Procédure : Naviguer dans les objets d’un CollectionView de données'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CollectionView [WPF], navigating through objects
- data binding [WPF], navigating through objects in data CollectionView
- navigating through objects in data CollectionView [WPF]
ms.assetid: fcd37590-bce1-4ac9-8b74-3b96c7458b8a
ms.openlocfilehash: 1507ab4db0c91b670d8bca754f6fd67d887c7041
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61931497"
---
# <a name="how-to-navigate-through-the-objects-in-a-data-collectionview"></a>Procédure : Naviguer dans les objets d’un CollectionView de données
Les vues permettent à la même collection de données de différentes façons, en fonction de tri, de filtrage ou de regroupement. Affichages également un concept de pointeur d’enregistrement actuel et permettent le déplacement du pointeur. Cet exemple montre comment obtenir l’objet en cours ainsi que pour naviguer dans les objets dans une collection de données à l’aide de la fonctionnalité fournie dans la <xref:System.Windows.Data.CollectionView> classe.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, `myCollectionView` est un <xref:System.Windows.Data.CollectionView> objet qui est une vue sur une collection liée.  
  
 Dans l’exemple suivant, `OnButton` est un gestionnaire d’événements pour le `Previous` et `Next` boutons dans une application, qui sont des boutons qui permettent à l’utilisateur de naviguer dans la collection de données. Notez que le <xref:System.Windows.Data.CollectionView.IsCurrentBeforeFirst%2A> et <xref:System.Windows.Data.CollectionView.IsCurrentAfterLast%2A> propriétés indiquent si le pointeur d’enregistrement actif est arrivé au début et la fin de la liste respectivement donc qui <xref:System.Windows.Data.CollectionView.MoveCurrentToFirst%2A> et <xref:System.Windows.Data.CollectionView.MoveCurrentToLast%2A> peuvent être appelés de manière appropriée.  
  
 Le <xref:System.Windows.Data.CollectionView.CurrentItem%2A> propriété de la vue est castée en un `Order` pour retourner l’élément actuel de la commande dans la collection.  
  
 [!code-csharp[CollectionView#OnButton](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#onbutton)]
 [!code-vb[CollectionView#OnButton](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#onbutton)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Trier des données dans une vue](how-to-sort-data-in-a-view.md)
- [Filtrer les données d’une vue](how-to-filter-data-in-a-view.md)
- [Trier et grouper des données à l'aide d'une vue en XAML](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
