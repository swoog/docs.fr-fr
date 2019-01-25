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
ms.openlocfilehash: 549f4e7af1a9aa623c7f8ff12b528f771a8ff806
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54504772"
---
# <a name="how-to-bind-to-a-collection-and-display-information-based-on-selection"></a><span data-ttu-id="8de99-102">Procédure : Effectuer une liaison à une collection et afficher des informations basées sur la sélection</span><span class="sxs-lookup"><span data-stu-id="8de99-102">How to: Bind to a Collection and Display Information Based on Selection</span></span>
<span data-ttu-id="8de99-103">Dans un scénario maître / détail simple, vous avez lié aux données <xref:System.Windows.Controls.ItemsControl> comme un <xref:System.Windows.Controls.ListBox>.</span><span class="sxs-lookup"><span data-stu-id="8de99-103">In a simple master-detail scenario, you have a data-bound <xref:System.Windows.Controls.ItemsControl> such as a <xref:System.Windows.Controls.ListBox>.</span></span> <span data-ttu-id="8de99-104">En fonction de sélection de l’utilisateur, afficher plus d’informations sur l’élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="8de99-104">Based on user selection, you display more information about the selected item.</span></span> <span data-ttu-id="8de99-105">Cet exemple montre comment implémenter ce scénario.</span><span class="sxs-lookup"><span data-stu-id="8de99-105">This example shows how to implement this scenario.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8de99-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="8de99-106">Example</span></span>  
 <span data-ttu-id="8de99-107">Dans cet exemple, `People` est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de `Person` classes.</span><span class="sxs-lookup"><span data-stu-id="8de99-107">In this example, `People` is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of `Person` classes.</span></span> <span data-ttu-id="8de99-108">Cela `Person` classe contient trois propriétés : `FirstName`, `LastName`, et `HomeTown`, tous du type `string`.</span><span class="sxs-lookup"><span data-stu-id="8de99-108">This `Person` class contains three properties: `FirstName`, `LastName`, and `HomeTown`, all of type `string`.</span></span>  
  
 [!code-xaml[CollectionBinding#Source](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#source)]  
[!code-xaml[CollectionBinding#UI](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#ui)]  
  
 <span data-ttu-id="8de99-109">Le <xref:System.Windows.Controls.ContentControl> utilise les éléments suivants <xref:System.Windows.DataTemplate> qui définit comment les informations d’un `Person` est présenté :</span><span class="sxs-lookup"><span data-stu-id="8de99-109">The <xref:System.Windows.Controls.ContentControl> uses the following <xref:System.Windows.DataTemplate> that defines how the information of a `Person` is presented:</span></span>  
  
 [!code-xaml[CollectionBinding#DetailTemplate](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#detailtemplate)]  
  
 <span data-ttu-id="8de99-110">Voici une capture d’écran de ce que l’exemple se produit.</span><span class="sxs-lookup"><span data-stu-id="8de99-110">The following is a screenshot of what the example produces.</span></span> <span data-ttu-id="8de99-111">Le <xref:System.Windows.Controls.ContentControl> présente les autres propriétés de la personne sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8de99-111">The <xref:System.Windows.Controls.ContentControl> shows the other properties of the person selected.</span></span>  
  
 <span data-ttu-id="8de99-112">![Liaison à une collection](../../../../docs/framework/wpf/data/media/databinding-collectionbindingsample.png "DataBinding_CollectionBindingSample")</span><span class="sxs-lookup"><span data-stu-id="8de99-112">![Binding to a collection](../../../../docs/framework/wpf/data/media/databinding-collectionbindingsample.png "DataBinding_CollectionBindingSample")</span></span>  
  
 <span data-ttu-id="8de99-113">Les deux choses à noter dans cet exemple sont :</span><span class="sxs-lookup"><span data-stu-id="8de99-113">The two things to notice in this example are:</span></span>  
  
1.  <span data-ttu-id="8de99-114">Le <xref:System.Windows.Controls.ListBox> et <xref:System.Windows.Controls.ContentControl> lier à la même source.</span><span class="sxs-lookup"><span data-stu-id="8de99-114">The <xref:System.Windows.Controls.ListBox> and the <xref:System.Windows.Controls.ContentControl> bind to the same source.</span></span> <span data-ttu-id="8de99-115">Le <xref:System.Windows.Data.Binding.Path%2A> propriétés des deux liaisons ne sont pas spécifiées, car les deux contrôles sont une liaison à l’objet d’ensemble de la collection.</span><span class="sxs-lookup"><span data-stu-id="8de99-115">The <xref:System.Windows.Data.Binding.Path%2A> properties of both bindings are not specified because both controls are binding to the entire collection object.</span></span>  
  
2.  <span data-ttu-id="8de99-116">Vous devez définir le <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> propriété `true` pour ce faire.</span><span class="sxs-lookup"><span data-stu-id="8de99-116">You must set the <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> property to `true` for this to work.</span></span> <span data-ttu-id="8de99-117">Définition de cette propriété garantit que l’élément sélectionné est toujours défini en tant que le <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>.</span><span class="sxs-lookup"><span data-stu-id="8de99-117">Setting this property ensures that the selected item is always set as the <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>.</span></span> <span data-ttu-id="8de99-118">Ou bien, si le <xref:System.Windows.Controls.ListBox> obtient ses données à partir d’un <xref:System.Windows.Data.CollectionViewSource>, il synchronise automatiquement sélection et la devise.</span><span class="sxs-lookup"><span data-stu-id="8de99-118">Alternatively, if the <xref:System.Windows.Controls.ListBox> gets it data from a <xref:System.Windows.Data.CollectionViewSource>, it synchronizes selection and currency automatically.</span></span>  
  
 <span data-ttu-id="8de99-119">Notez que le `Person` substitue le `ToString` méthode la façon suivante.</span><span class="sxs-lookup"><span data-stu-id="8de99-119">Note that the `Person` class overrides the `ToString` method the following way.</span></span> <span data-ttu-id="8de99-120">Par défaut, le <xref:System.Windows.Controls.ListBox> appels `ToString` et affiche une représentation sous forme de chaîne de chaque objet dans la collection liée.</span><span class="sxs-lookup"><span data-stu-id="8de99-120">By default, the <xref:System.Windows.Controls.ListBox> calls `ToString` and displays a string representation of each object in the bound collection.</span></span> <span data-ttu-id="8de99-121">C’est pourquoi chaque `Person` apparaît sous la forme d’un prénom dans le <xref:System.Windows.Controls.ListBox>.</span><span class="sxs-lookup"><span data-stu-id="8de99-121">That is why each `Person` appears as a first name in the <xref:System.Windows.Controls.ListBox>.</span></span>  
  
 [!code-csharp[CollectionBinding#ToString](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Data.cs#tostring)]
 [!code-vb[CollectionBinding#ToString](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionBinding/VisualBasic/Person.vb#tostring)]  
  
## <a name="see-also"></a><span data-ttu-id="8de99-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de99-122">See also</span></span>
- [<span data-ttu-id="8de99-123">Utiliser le modèle maître/détail avec des données hiérarchiques</span><span class="sxs-lookup"><span data-stu-id="8de99-123">Use the Master-Detail Pattern with Hierarchical Data</span></span>](../../../../docs/framework/wpf/data/how-to-use-the-master-detail-pattern-with-hierarchical-data.md)
- [<span data-ttu-id="8de99-124">Utiliser le modèle maître/détail avec des données XML hiérarchiques</span><span class="sxs-lookup"><span data-stu-id="8de99-124">Use the Master-Detail Pattern with Hierarchical XML Data</span></span>](../../../../docs/framework/wpf/data/how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md)
- [<span data-ttu-id="8de99-125">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="8de99-125">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="8de99-126">Vue d’ensemble des modèles de données</span><span class="sxs-lookup"><span data-stu-id="8de99-126">Data Templating Overview</span></span>](../../../../docs/framework/wpf/data/data-templating-overview.md)
- [<span data-ttu-id="8de99-127">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="8de99-127">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
