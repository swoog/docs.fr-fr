---
title: 'Procédure : Implémenter une classe CompositeCollection'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
ms.openlocfilehash: 71d55a23711b116a91386a537d5572e8506d4c6b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372670"
---
# <a name="how-to-implement-a-compositecollection"></a>Procédure : Implémenter une classe CompositeCollection
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment afficher plusieurs collections et éléments comme une liste à l’aide la <xref:System.Windows.Data.CompositeCollection> classe. Dans cet exemple, `GreekGods` est un <xref:System.Collections.ObjectModel.ObservableCollection%601> de `GreekGod` des objets personnalisés. Modèles de données sont définies afin que `GreekGod` objets et `GreekHero` objets apparaissent avec un OR et une couleur de premier plan cyan, respectivement.  
  
 [!code-xaml[CompositeCollections#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Data.CollectionContainer>
- <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>
- <xref:System.Windows.Data.XmlDataProvider>
- <xref:System.Windows.DataTemplate>
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
