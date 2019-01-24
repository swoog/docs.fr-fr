---
title: "Procédure : Filtrer les données d'une vue"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [WPF], filtering data
- filtering data in views [WPF]
- data binding [WPF], filtering data in views
ms.assetid: c76e8606-4cc4-45a8-9110-e2ec66dc6afd
ms.openlocfilehash: 33af517c086f8f89cc06a1de7a2979c5b1624109
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54689319"
---
# <a name="how-to-filter-data-in-a-view"></a><span data-ttu-id="831a3-102">Procédure : Filtrer les données d'une vue</span><span class="sxs-lookup"><span data-stu-id="831a3-102">How to: Filter Data in a View</span></span>
<span data-ttu-id="831a3-103">Cet exemple montre comment filtrer des données dans une vue.</span><span class="sxs-lookup"><span data-stu-id="831a3-103">This example shows how to filter data in a view.</span></span>  
  
## <a name="example"></a><span data-ttu-id="831a3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="831a3-104">Example</span></span>  
 <span data-ttu-id="831a3-105">Pour créer un filtre, définissez une méthode qui fournit la logique de filtrage.</span><span class="sxs-lookup"><span data-stu-id="831a3-105">To create a filter, define a method that provides the filtering logic.</span></span> <span data-ttu-id="831a3-106">La méthode est utilisée comme un rappel et accepte un paramètre de type `object`.</span><span class="sxs-lookup"><span data-stu-id="831a3-106">The method is used as a callback and accepts a parameter of type `object`.</span></span> <span data-ttu-id="831a3-107">La méthode suivante retourne tous les `Order` objets avec le `filled` propriété définie sur « Non », filtre le reste des objets.</span><span class="sxs-lookup"><span data-stu-id="831a3-107">The following method returns all the `Order` objects with the `filled` property set to "No", filtering out the rest of the objects.</span></span>  
  
 [!code-csharp[SortFilter#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#2)]
 [!code-vb[SortFilter#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#2)]  
  
 <span data-ttu-id="831a3-108">Vous pouvez ensuite appliquer le filtre, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="831a3-108">You can then apply the filter, as shown in the following example.</span></span> <span data-ttu-id="831a3-109">Dans cet exemple, `myCollectionView` est un <xref:System.Windows.Data.ListCollectionView> objet.</span><span class="sxs-lookup"><span data-stu-id="831a3-109">In this example, `myCollectionView` is a <xref:System.Windows.Data.ListCollectionView> object.</span></span>  
  
 [!code-csharp[SortFilter#Filter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#filter)]
 [!code-vb[SortFilter#Filter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#filter)]  
  
 <span data-ttu-id="831a3-110">Pour annuler le filtrage, vous pouvez définir le <xref:System.Windows.Data.CollectionView.Filter%2A> propriété `null`:</span><span class="sxs-lookup"><span data-stu-id="831a3-110">To undo filtering, you can set the <xref:System.Windows.Data.CollectionView.Filter%2A> property to `null`:</span></span>  
  
 [!code-csharp[SortFilter#Unfilter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#unfilter)]
 [!code-vb[SortFilter#Unfilter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#unfilter)]  
  
 <span data-ttu-id="831a3-111">Pour plus d’informations sur la façon de créer ou d’obtenir une vue, consultez [obtenir la vue par défaut d’une Collection de données](../../../../docs/framework/wpf/data/how-to-get-the-default-view-of-a-data-collection.md).</span><span class="sxs-lookup"><span data-stu-id="831a3-111">For information about how to create or obtain a view, see [Get the Default View of a Data Collection](../../../../docs/framework/wpf/data/how-to-get-the-default-view-of-a-data-collection.md).</span></span> <span data-ttu-id="831a3-112">Pour obtenir un exemple complet, consultez [de tri et filtrage des éléments dans une vue, exemple](https://go.microsoft.com/fwlink/?LinkID=160040).</span><span class="sxs-lookup"><span data-stu-id="831a3-112">For the complete example, see [Sorting and Filtering Items in a View Sample](https://go.microsoft.com/fwlink/?LinkID=160040).</span></span>  
  
 <span data-ttu-id="831a3-113">Si votre objet de vue provient d’un <xref:System.Windows.Data.CollectionViewSource> de l’objet, vous appliquez la logique de filtrage en définissant un gestionnaire d’événements pour le <xref:System.Windows.Data.CollectionViewSource.Filter> événement.</span><span class="sxs-lookup"><span data-stu-id="831a3-113">If your view object comes from a <xref:System.Windows.Data.CollectionViewSource> object, you apply filtering logic by setting an event handler for the <xref:System.Windows.Data.CollectionViewSource.Filter> event.</span></span> <span data-ttu-id="831a3-114">Dans l’exemple suivant, `listingDataView` est une instance de <xref:System.Windows.Data.CollectionViewSource>.</span><span class="sxs-lookup"><span data-stu-id="831a3-114">In the following example, `listingDataView` is an instance of <xref:System.Windows.Data.CollectionViewSource>.</span></span>  
  
 [!code-csharp[DataBindingLab#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#10)]
 [!code-vb[DataBindingLab#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#10)]  
  
 <span data-ttu-id="831a3-115">L’exemple suivant montre l’implémentation de l’exemple `ShowOnlyBargainsFilter` Gestionnaire d’événements de filtre.</span><span class="sxs-lookup"><span data-stu-id="831a3-115">The following shows the implementation of the example `ShowOnlyBargainsFilter` filter event handler.</span></span> <span data-ttu-id="831a3-116">Ce gestionnaire d’événements utilise la <xref:System.Windows.Data.FilterEventArgs.Accepted%2A> propriété pour filtrer les `AuctionItem` objets qui ont un `CurrentPrice` de 25 $ ou plus.</span><span class="sxs-lookup"><span data-stu-id="831a3-116">This event handler uses the <xref:System.Windows.Data.FilterEventArgs.Accepted%2A> property to filter out `AuctionItem` objects that have a `CurrentPrice` of $25 or greater.</span></span>  
  
 [!code-csharp[DataBindingLab#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#5)]
 [!code-vb[DataBindingLab#5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="831a3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="831a3-117">See also</span></span>
- <xref:System.Windows.Data.CollectionView.CanFilter%2A>
- <xref:System.Windows.Data.BindingListCollectionView.CustomFilter%2A>
- [<span data-ttu-id="831a3-118">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="831a3-118">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="831a3-119">Trier des données dans une vue</span><span class="sxs-lookup"><span data-stu-id="831a3-119">Sort Data in a View</span></span>](../../../../docs/framework/wpf/data/how-to-sort-data-in-a-view.md)
- [<span data-ttu-id="831a3-120">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="831a3-120">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
