---
title: 'Procédure : Trier et grouper des données à l’aide d’une vue en XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], grouping data in views in XAML
- XAML [WPF], sorting data in views
- grouping data in views in XAML [WPF]
- data binding [WPF], sorting data in views in XAML
- sorting data in views in XAML [WPF]
- XAML [WPF], grouping data in views
- views [WPF], sorting data
- views [WPF], grouping data
ms.assetid: 145c8c3f-dbdd-4d0d-816f-90b35eba7eda
ms.openlocfilehash: ca4439b574264ebebfda745f0765f750099bc95f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62020736"
---
# <a name="how-to-sort-and-group-data-using-a-view-in-xaml"></a><span data-ttu-id="62ca7-102">Procédure : Trier et grouper des données à l’aide d’une vue en XAML</span><span class="sxs-lookup"><span data-stu-id="62ca7-102">How to: Sort and Group Data Using a View in XAML</span></span>
<span data-ttu-id="62ca7-103">Cet exemple montre comment créer une vue d’une collection de données dans [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="62ca7-103">This example shows how to create a view of a data collection in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)].</span></span> <span data-ttu-id="62ca7-104">Les vues permettent pour les fonctionnalités de regroupement, le tri, filtrage et la notion d’un élément en cours.</span><span class="sxs-lookup"><span data-stu-id="62ca7-104">Views allow for the functionalities of grouping, sorting, filtering, and the notion of a current item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="62ca7-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="62ca7-105">Example</span></span>  
 <span data-ttu-id="62ca7-106">Dans l’exemple suivant, la ressource statique nommée *place* est défini comme une collection de *Place* objets, dans lequel chaque *Place* objet se compose d’un nom de ville et le état.</span><span class="sxs-lookup"><span data-stu-id="62ca7-106">In the following example, the static resource named *places* is defined as a collection of *Place* objects, in which each *Place* object is consisted of a city name and the state.</span></span> <span data-ttu-id="62ca7-107">Le préfixe *src* est mappé à l’espace de noms dans lequel la source de données *emplacements* est défini.</span><span class="sxs-lookup"><span data-stu-id="62ca7-107">The prefix *src* is mapped to the namespace where the data source *Places* is defined.</span></span> <span data-ttu-id="62ca7-108">Le préfixe *scm* est mappé à `"clr-namespace:System.ComponentModel;assembly=WindowsBase"` et *dat* mappe à `"clr-namespace:System.Windows.Data;assembly=PresentationFramework"`.</span><span class="sxs-lookup"><span data-stu-id="62ca7-108">The prefix *scm* maps to `"clr-namespace:System.ComponentModel;assembly=WindowsBase"` and *dat* maps to `"clr-namespace:System.Windows.Data;assembly=PresentationFramework"`.</span></span>  
  
 <span data-ttu-id="62ca7-109">L’exemple suivant crée une vue de la collecte de données qui est triée par nom de ville et regroupée par l’état.</span><span class="sxs-lookup"><span data-stu-id="62ca7-109">The following example creates a view of the data collection that is sorted by the city name and grouped by the state.</span></span>  
  
 [!code-xaml[CollectionViewSource#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#1)]  
  
 <span data-ttu-id="62ca7-110">La vue peut ensuite être une source de liaison, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="62ca7-110">The view can then be a binding source, as in the following example:</span></span>  
  
 [!code-xaml[CollectionViewSource#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#2)]  
  
 <span data-ttu-id="62ca7-111">Pour les liaisons à des données XML définies dans un <xref:System.Windows.Data.XmlDataProvider> ressource, faites précéder le nom XML avec un symbole @.</span><span class="sxs-lookup"><span data-stu-id="62ca7-111">For bindings to XML data defined in an <xref:System.Windows.Data.XmlDataProvider> resource, precede the XML name with an @ symbol.</span></span>  
  
 [!code-xaml[CollectionViewSource#XDPChunk](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#xdpchunk)]  
  
 [!code-xaml[CollectionViewSource#Attribute](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#attribute)]  
  
## <a name="see-also"></a><span data-ttu-id="62ca7-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62ca7-112">See also</span></span>

- <xref:System.Windows.Data.CollectionViewSource>
- [<span data-ttu-id="62ca7-113">Obtenir la vue par défaut d'une collection de données</span><span class="sxs-lookup"><span data-stu-id="62ca7-113">Get the Default View of a Data Collection</span></span>](how-to-get-the-default-view-of-a-data-collection.md)
- [<span data-ttu-id="62ca7-114">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="62ca7-114">Data Binding Overview</span></span>](data-binding-overview.md)
- [<span data-ttu-id="62ca7-115">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="62ca7-115">How-to Topics</span></span>](data-binding-how-to-topics.md)
