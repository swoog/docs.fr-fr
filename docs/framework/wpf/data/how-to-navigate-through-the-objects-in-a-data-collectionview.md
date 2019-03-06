---
title: "Procédure : Naviguer dans les objets d'un CollectionView de données"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CollectionView [WPF], navigating through objects
- data binding [WPF], navigating through objects in data CollectionView
- navigating through objects in data CollectionView [WPF]
ms.assetid: fcd37590-bce1-4ac9-8b74-3b96c7458b8a
ms.openlocfilehash: 9272a2f635a62abdac2746f2c8cce515812706f6
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57355777"
---
# <a name="how-to-navigate-through-the-objects-in-a-data-collectionview"></a><span data-ttu-id="06462-102">Procédure : Naviguer dans les objets d'un CollectionView de données</span><span class="sxs-lookup"><span data-stu-id="06462-102">How to: Navigate Through the Objects in a Data CollectionView</span></span>
<span data-ttu-id="06462-103">Les vues permettent à la même collection de données de différentes façons, en fonction de tri, de filtrage ou de regroupement.</span><span class="sxs-lookup"><span data-stu-id="06462-103">Views allow the same data collection to be viewed in different ways, depending on sorting, filtering, or grouping.</span></span> <span data-ttu-id="06462-104">Affichages également un concept de pointeur d’enregistrement actuel et permettent le déplacement du pointeur.</span><span class="sxs-lookup"><span data-stu-id="06462-104">Views also provide a current record pointer concept and enable moving the pointer.</span></span> <span data-ttu-id="06462-105">Cet exemple montre comment obtenir l’objet en cours ainsi que pour naviguer dans les objets dans une collection de données à l’aide de la fonctionnalité fournie dans la <xref:System.Windows.Data.CollectionView> classe.</span><span class="sxs-lookup"><span data-stu-id="06462-105">This example shows how to get the current object as well as navigate through the objects in a data collection using the functionality provided in the <xref:System.Windows.Data.CollectionView> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="06462-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="06462-106">Example</span></span>  
 <span data-ttu-id="06462-107">Dans cet exemple, `myCollectionView` est un <xref:System.Windows.Data.CollectionView> objet qui est une vue sur une collection liée.</span><span class="sxs-lookup"><span data-stu-id="06462-107">In this example, `myCollectionView` is a <xref:System.Windows.Data.CollectionView> object that is a view over a bound collection.</span></span>  
  
 <span data-ttu-id="06462-108">Dans l’exemple suivant, `OnButton` est un gestionnaire d’événements pour le `Previous` et `Next` boutons dans une application, qui sont des boutons qui permettent à l’utilisateur de naviguer dans la collection de données.</span><span class="sxs-lookup"><span data-stu-id="06462-108">In the following example, `OnButton` is an event handler for the `Previous` and `Next` buttons in an application, which are buttons that allow the user to navigate the data collection.</span></span> <span data-ttu-id="06462-109">Notez que le <xref:System.Windows.Data.CollectionView.IsCurrentBeforeFirst%2A> et <xref:System.Windows.Data.CollectionView.IsCurrentAfterLast%2A> propriétés indiquent si le pointeur d’enregistrement actif est arrivé au début et la fin de la liste respectivement donc qui <xref:System.Windows.Data.CollectionView.MoveCurrentToFirst%2A> et <xref:System.Windows.Data.CollectionView.MoveCurrentToLast%2A> peuvent être appelés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="06462-109">Note that the <xref:System.Windows.Data.CollectionView.IsCurrentBeforeFirst%2A> and <xref:System.Windows.Data.CollectionView.IsCurrentAfterLast%2A> properties report whether the current record pointer has come to the beginning and the end of the list respectively so that <xref:System.Windows.Data.CollectionView.MoveCurrentToFirst%2A> and <xref:System.Windows.Data.CollectionView.MoveCurrentToLast%2A> can be called as appropriately.</span></span>  
  
 <span data-ttu-id="06462-110">Le <xref:System.Windows.Data.CollectionView.CurrentItem%2A> propriété de la vue est castée en un `Order` pour retourner l’élément actuel de la commande dans la collection.</span><span class="sxs-lookup"><span data-stu-id="06462-110">The <xref:System.Windows.Data.CollectionView.CurrentItem%2A> property of the view is cast as an `Order` to return the current order item in the collection.</span></span>  
  
 [!code-csharp[CollectionView#OnButton](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#onbutton)]
 [!code-vb[CollectionView#OnButton](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#onbutton)]  
  
## <a name="see-also"></a><span data-ttu-id="06462-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06462-111">See also</span></span>
- [<span data-ttu-id="06462-112">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="06462-112">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="06462-113">Trier des données dans une vue</span><span class="sxs-lookup"><span data-stu-id="06462-113">Sort Data in a View</span></span>](how-to-sort-data-in-a-view.md)
- [<span data-ttu-id="06462-114">Filtrer les données d’une vue</span><span class="sxs-lookup"><span data-stu-id="06462-114">Filter Data in a View</span></span>](how-to-filter-data-in-a-view.md)
- [<span data-ttu-id="06462-115">Trier et grouper des données à l'aide d'une vue en XAML</span><span class="sxs-lookup"><span data-stu-id="06462-115">Sort and Group Data Using a View in XAML</span></span>](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [<span data-ttu-id="06462-116">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="06462-116">How-to Topics</span></span>](data-binding-how-to-topics.md)
