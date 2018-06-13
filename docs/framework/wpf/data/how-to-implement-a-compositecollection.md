---
title: 'Comment : implémenter une classe CompositeCollection'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
ms.openlocfilehash: f8af8d806b8c889be11533392ee3c831399e9ab7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33556115"
---
# <a name="how-to-implement-a-compositecollection"></a><span data-ttu-id="00b81-102">Comment : implémenter une classe CompositeCollection</span><span class="sxs-lookup"><span data-stu-id="00b81-102">How to: Implement a CompositeCollection</span></span>
## <a name="example"></a><span data-ttu-id="00b81-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="00b81-103">Example</span></span>  
 <span data-ttu-id="00b81-104">L’exemple suivant montre comment afficher plusieurs collections et éléments comme une liste à l’aide la <xref:System.Windows.Data.CompositeCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="00b81-104">The following example shows how to display multiple collections and items as one list using the <xref:System.Windows.Data.CompositeCollection> class.</span></span> <span data-ttu-id="00b81-105">Dans cet exemple, `GreekGods` est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de `GreekGod` des objets personnalisés.</span><span class="sxs-lookup"><span data-stu-id="00b81-105">In this example, `GreekGods` is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of `GreekGod` custom objects.</span></span> <span data-ttu-id="00b81-106">Modèles de données sont définies afin que `GreekGod` objets et `GreekHero` objets s’affichent avec un OR et une couleur d’arrière-plan cyan, respectivement.</span><span class="sxs-lookup"><span data-stu-id="00b81-106">Data templates are defined so that `GreekGod` objects and `GreekHero` objects appear with a gold and a cyan foreground color respectively.</span></span>  
  
 [!code-xaml[CompositeCollections#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="00b81-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00b81-107">See Also</span></span>  
 <xref:System.Windows.Data.CollectionContainer>  
 <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>  
 <xref:System.Windows.Data.XmlDataProvider>  
 <xref:System.Windows.DataTemplate>  
 [<span data-ttu-id="00b81-108">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="00b81-108">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [<span data-ttu-id="00b81-109">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="00b81-109">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
