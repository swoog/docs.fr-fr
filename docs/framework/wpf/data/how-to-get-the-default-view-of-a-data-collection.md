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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59222105"
---
# <a name="how-to-get-the-default-view-of-a-data-collection"></a><span data-ttu-id="0573b-102">Procédure : Obtenir la vue par défaut d’une collection de données</span><span class="sxs-lookup"><span data-stu-id="0573b-102">How to: Get the Default View of a Data Collection</span></span>
<span data-ttu-id="0573b-103">Les vues permettent à la même collection de données de différentes façons, en fonction de tri, filtrage ou des critères de regroupement.</span><span class="sxs-lookup"><span data-stu-id="0573b-103">Views allow the same data collection to be viewed in different ways, depending on sorting, filtering, or grouping criteria.</span></span> <span data-ttu-id="0573b-104">Chaque collection a un affichage par défaut partagé, qui est utilisé comme source de liaison réelle lorsqu’une liaison spécifie une collection comme source.</span><span class="sxs-lookup"><span data-stu-id="0573b-104">Every collection has one shared default view, which is used as the actual binding source when a binding specifies a collection as its source.</span></span> <span data-ttu-id="0573b-105">Cet exemple montre comment obtenir la vue par défaut d’une collection.</span><span class="sxs-lookup"><span data-stu-id="0573b-105">This example shows how to get the default view of a collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0573b-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="0573b-106">Example</span></span>  
 <span data-ttu-id="0573b-107">Pour créer la vue, vous avez besoin d’une référence d’objet à la collection.</span><span class="sxs-lookup"><span data-stu-id="0573b-107">To create the view, you need an object reference to the collection.</span></span> <span data-ttu-id="0573b-108">Cet objet de données peut être obtenu en faisant référence à votre propre objet code-behind, en obtenant le contexte de données, en obtenant une propriété de la source de données, ou en obtenant une propriété de la liaison.</span><span class="sxs-lookup"><span data-stu-id="0573b-108">This data object can be obtained by referencing your own code-behind object, by getting the data context, by getting a property of the data source, or by getting a property of the binding.</span></span> <span data-ttu-id="0573b-109">Cet exemple montre comment obtenir le <xref:System.Windows.FrameworkElement.DataContext%2A> d’un objet de données et l’utiliser pour obtenir directement la collection par défaut afficher pour cette collection.</span><span class="sxs-lookup"><span data-stu-id="0573b-109">This example shows how to get the <xref:System.Windows.FrameworkElement.DataContext%2A> of a data object and use it to directly obtain the default collection view for this collection.</span></span>  
  
 [!code-csharp[CollectionView#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#2)]
 [!code-vb[CollectionView#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#2)]  
  
 <span data-ttu-id="0573b-110">Dans cet exemple, l’élément racine est un <xref:System.Windows.Controls.StackPanel>.</span><span class="sxs-lookup"><span data-stu-id="0573b-110">In this example, the root element is a <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="0573b-111">Le <xref:System.Windows.FrameworkElement.DataContext%2A> a la valeur *myDataSource*, qui fait référence à un fournisseur de données est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de *ordre* objets.</span><span class="sxs-lookup"><span data-stu-id="0573b-111">The <xref:System.Windows.FrameworkElement.DataContext%2A> is set to *myDataSource*, which refers to a data provider that is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of *Order* objects.</span></span>  
  
 [!code-xaml[CollectionView#CollectionViewDataContext](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml#collectionviewdatacontext)]  
  
 <span data-ttu-id="0573b-112">Ou bien, vous pouvez instancier et lier à votre propre vue de collection en utilisant la <xref:System.Windows.Data.CollectionViewSource> classe.</span><span class="sxs-lookup"><span data-stu-id="0573b-112">Alternatively, you can instantiate and bind to your own collection view using the <xref:System.Windows.Data.CollectionViewSource> class.</span></span> <span data-ttu-id="0573b-113">Cette vue de collection est partagée uniquement par les contrôles liés directement.</span><span class="sxs-lookup"><span data-stu-id="0573b-113">This collection view is only shared by controls that bind to it directly.</span></span> <span data-ttu-id="0573b-114">Pour obtenir un exemple, consultez la section Comment créer une vue dans le [vue d’ensemble de la liaison de données](data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0573b-114">For an example, see the How to Create a View section in the [Data Binding Overview](data-binding-overview.md).</span></span>  
  
 <span data-ttu-id="0573b-115">Pour obtenir des exemples des fonctionnalités fournies par une vue de collection, consultez [trier des données dans une vue](how-to-sort-data-in-a-view.md), [filtrer des données dans une vue](how-to-filter-data-in-a-view.md), et [naviguer dans les objets d’un CollectionView de données](how-to-navigate-through-the-objects-in-a-data-collectionview.md).</span><span class="sxs-lookup"><span data-stu-id="0573b-115">For examples of the functionality provided by a collection view, see [Sort Data in a View](how-to-sort-data-in-a-view.md), [Filter Data in a View](how-to-filter-data-in-a-view.md), and [Navigate Through the Objects in a Data CollectionView](how-to-navigate-through-the-objects-in-a-data-collectionview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0573b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0573b-116">See also</span></span>

- [<span data-ttu-id="0573b-117">Trier et grouper des données à l'aide d'une vue en XAML</span><span class="sxs-lookup"><span data-stu-id="0573b-117">Sort and Group Data Using a View in XAML</span></span>](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [<span data-ttu-id="0573b-118">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="0573b-118">How-to Topics</span></span>](data-binding-how-to-topics.md)
