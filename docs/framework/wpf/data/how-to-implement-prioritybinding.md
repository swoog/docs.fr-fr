---
title: 'Procédure : Implémenter PriorityBinding'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], PriorityBinding class
ms.assetid: d63b65ab-b3e9-4322-9aa8-1450f8d89532
ms.openlocfilehash: aaf2caff1e2684e08c7eb65125536f1070203d70
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62020853"
---
# <a name="how-to-implement-prioritybinding"></a>Procédure : Implémenter PriorityBinding
<xref:System.Windows.Data.PriorityBinding> dans [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] fonctionne en spécifiant une liste de liaisons. La liste des liaisons est classée de priorité la plus élevée à la priorité la plus basse. Si la liaison de priorité la plus élevée retourne une valeur avec succès lorsqu’il est traité puis il n’est jamais nécessaire de traiter les autres liaisons dans la liste. Il peut arriver que la liaison de priorité la plus élevée prend beaucoup de temps à évaluer, la priorité la plus élevée suivante qui retourne une valeur avec succès est utilisée jusqu'à ce qu’une liaison d’une priorité plus élevée retourne une valeur avec succès.  
  
## <a name="example"></a>Exemple  
 Pour illustrer comment <xref:System.Windows.Data.PriorityBinding> fonctionne, le `AsyncDataSource` objet a été créé avec les trois propriétés suivantes : `FastDP`, `SlowerDP`, et `SlowestDP`.  
  
 L’accesseur get de `FastDP` retourne la valeur de la `_fastDP` membre de données.  
  
 L’accesseur get de `SlowerDP` attend trois secondes avant de retourner la valeur de la `_slowerDP` membre de données.  
  
 L’accesseur get de `SlowestDP` attend cinq secondes avant de retourner la valeur de la `_slowestDP` membre de données.  
  
> [!NOTE]
>  L’exemple est uniquement fourni à des fins de démonstration. Le [!INCLUDE[TLA#tla_net](../../../../includes/tlasharptla-net-md.md)] est recommandé de définir de propriétés qui sont beaucoup plus lent qu’un ensemble de champs serait. Pour plus d’informations, consultez [en choisissant entre les propriétés et méthodes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/ms229054(v=vs.100)).  
  
 [!code-csharp[PriorityBinding#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PriorityBinding/CSharp/Window1.xaml.cs#1)]
 [!code-vb[PriorityBinding#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PriorityBinding/VisualBasic/AsyncDataSource.vb#1)]  
  
 Le <xref:System.Windows.Controls.TextBlock.Text%2A> propriété est liée à la méthode ci-dessus `AsyncDS` à l’aide de <xref:System.Windows.Data.PriorityBinding>:  
  
 [!code-xaml[PriorityBinding#2](~/samples/snippets/csharp/VS_Snippets_Wpf/PriorityBinding/CSharp/Window1.xaml#2)]  
  
 Lorsque le moteur de liaison traite les <xref:System.Windows.Data.Binding> objets, il commence par la première <xref:System.Windows.Data.Binding>, qui est lié à la `SlowestDP` propriété. Lorsque cela <xref:System.Windows.Data.Binding> est traité, il ne retourne pas de valeur avec succès, car il est en veille pendant 5 secondes, par conséquent, la prochaine <xref:System.Windows.Data.Binding> élément est traité. La prochaine <xref:System.Windows.Data.Binding> ne retourne pas de valeur avec succès, car il est en état de veille pour 3 secondes. Le moteur de liaison se place ensuite sur la prochaine <xref:System.Windows.Data.Binding> élément, qui est lié à la `FastDP` propriété. Cela <xref:System.Windows.Data.Binding> retourne la valeur « Fast Value ». Le <xref:System.Windows.Controls.TextBlock> affiche désormais la valeur « Fast Value ».  
  
 Après 3 secondes, le `SlowerDP` propriété retourne la valeur « Valeur plus lent ». Le <xref:System.Windows.Controls.TextBlock> puis affiche la valeur « Valeur plus lent ».  
  
 Après 5 secondes, le `SlowestDP` propriété retourne la valeur « Slowest Value ». Cette liaison a la priorité la plus élevée, car elle est répertoriée en premier. Le <xref:System.Windows.Controls.TextBlock> affiche désormais la valeur « Slowest Value ».  
  
 Consultez <xref:System.Windows.Data.PriorityBinding> pour plus d’informations sur ce qui est considéré comme valeur de retournée avec succès à partir d’une liaison.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Data.Binding.IsAsync%2A?displayProperty=nameWithType>
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
