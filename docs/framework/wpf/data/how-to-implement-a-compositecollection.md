---
title: 'Procédure : Implémenter une classe CompositeCollection'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
ms.openlocfilehash: 2021ed83a8f2a6896631fa69d5dd55a74cad8a8d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691864"
---
# <a name="how-to-implement-a-compositecollection"></a><span data-ttu-id="ec93b-102">Procédure : Implémenter une classe CompositeCollection</span><span class="sxs-lookup"><span data-stu-id="ec93b-102">How to: Implement a CompositeCollection</span></span>
## <a name="example"></a><span data-ttu-id="ec93b-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec93b-103">Example</span></span>  
 <span data-ttu-id="ec93b-104">L’exemple suivant montre comment afficher plusieurs collections et éléments comme une liste à l’aide la <xref:System.Windows.Data.CompositeCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="ec93b-104">The following example shows how to display multiple collections and items as one list using the <xref:System.Windows.Data.CompositeCollection> class.</span></span> <span data-ttu-id="ec93b-105">Dans cet exemple, `GreekGods` est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de `GreekGod` des objets personnalisés.</span><span class="sxs-lookup"><span data-stu-id="ec93b-105">In this example, `GreekGods` is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of `GreekGod` custom objects.</span></span> <span data-ttu-id="ec93b-106">Modèles de données sont définies afin que `GreekGod` objets et `GreekHero` objets apparaissent avec un OR et une couleur de premier plan cyan, respectivement.</span><span class="sxs-lookup"><span data-stu-id="ec93b-106">Data templates are defined so that `GreekGod` objects and `GreekHero` objects appear with a gold and a cyan foreground color respectively.</span></span>  
  
 [!code-xaml[CompositeCollections#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="ec93b-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec93b-107">See also</span></span>
- <xref:System.Windows.Data.CollectionContainer>
- <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>
- <xref:System.Windows.Data.XmlDataProvider>
- <xref:System.Windows.DataTemplate>
- [<span data-ttu-id="ec93b-108">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="ec93b-108">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [<span data-ttu-id="ec93b-109">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="ec93b-109">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
