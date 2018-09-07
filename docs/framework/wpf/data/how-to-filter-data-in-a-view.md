---
title: "Comment : filtrer les données d'une vue"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [WPF], filtering data
- filtering data in views [WPF]
- data binding [WPF], filtering data in views
ms.assetid: c76e8606-4cc4-45a8-9110-e2ec66dc6afd
ms.openlocfilehash: b972da093fc50563c5db93e61aeb8421f9bf20b2
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44087639"
---
# <a name="how-to-filter-data-in-a-view"></a>Comment : filtrer les données d'une vue
Cet exemple montre comment filtrer des données dans une vue.  
  
## <a name="example"></a>Exemple  
 Pour créer un filtre, définissez une méthode qui fournit la logique de filtrage. La méthode est utilisée comme un rappel et accepte un paramètre de type `object`. La méthode suivante retourne tous les `Order` objets avec le `filled` propriété définie sur « Non », filtre le reste des objets.  
  
 [!code-csharp[SortFilter#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#2)]
 [!code-vb[SortFilter#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#2)]  
  
 Vous pouvez ensuite appliquer le filtre, comme indiqué dans l’exemple suivant. Dans cet exemple, `myCollectionView` est un <xref:System.Windows.Data.ListCollectionView> objet.  
  
 [!code-csharp[SortFilter#Filter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#filter)]
 [!code-vb[SortFilter#Filter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#filter)]  
  
 Pour annuler le filtrage, vous pouvez définir le <xref:System.Windows.Data.CollectionView.Filter%2A> propriété `null`:  
  
 [!code-csharp[SortFilter#Unfilter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#unfilter)]
 [!code-vb[SortFilter#Unfilter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#unfilter)]  
  
 Pour plus d’informations sur la façon de créer ou d’obtenir une vue, consultez [obtenir la vue par défaut d’une Collection de données](../../../../docs/framework/wpf/data/how-to-get-the-default-view-of-a-data-collection.md). Pour obtenir un exemple complet, consultez [de tri et filtrage des éléments dans une vue, exemple](https://go.microsoft.com/fwlink/?LinkID=160040).  
  
 Si votre objet de vue provient d’un <xref:System.Windows.Data.CollectionViewSource> de l’objet, vous appliquez la logique de filtrage en définissant un gestionnaire d’événements pour le <xref:System.Windows.Data.CollectionViewSource.Filter> événement. Dans l’exemple suivant, `listingDataView` est une instance de <xref:System.Windows.Data.CollectionViewSource>.  
  
 [!code-csharp[DataBindingLab#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#10)]
 [!code-vb[DataBindingLab#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#10)]  
  
 L’exemple suivant montre l’implémentation de l’exemple `ShowOnlyBargainsFilter` Gestionnaire d’événements de filtre. Ce gestionnaire d’événements utilise la <xref:System.Windows.Data.FilterEventArgs.Accepted%2A> propriété pour filtrer les `AuctionItem` objets qui ont un `CurrentPrice` de 25 $ ou plus.  
  
 [!code-csharp[DataBindingLab#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#5)]
 [!code-vb[DataBindingLab#5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#5)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Data.CollectionView.CanFilter%2A>  
 <xref:System.Windows.Data.BindingListCollectionView.CustomFilter%2A>  
 [Vue d’ensemble de la liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [Trier des données dans une vue](../../../../docs/framework/wpf/data/how-to-sort-data-in-a-view.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
