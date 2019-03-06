---
title: 'Procédure : Utiliser le modèle maître/détail avec des données hiérarchiques'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: 11429b9e-058d-4084-bfb6-2cf209c8ddf7
ms.openlocfilehash: 41f02013feb1405e5640afa73b954dc84921c924
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57351479"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-data"></a>Procédure : Utiliser le modèle maître/détail avec des données hiérarchiques
Cet exemple montre comment implémenter le scénario maître / détail.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, `LeagueList` est une collection de `Leagues`. Chaque `League` a un `Name` et une collection de `Divisions`et chaque `Division` a un nom et une collection de `Teams`. Chaque `Team` a un nom d’équipe.  
  
 [!code-xaml[MasterDetail#HowTo1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto1)]  
[!code-xaml[MasterDetail#HowTo2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MasterDetail/VisualBasic/Page1.xaml#howto2)]  
  
 Voici une capture d’écran de l’exemple. Le `Divisions` <xref:System.Windows.Controls.ListBox> effectue automatiquement le suivi des sélections dans le `Leagues` <xref:System.Windows.Controls.ListBox> et afficher les données correspondantes. Le `Teams` <xref:System.Windows.Controls.ListBox> effectue le suivi des sélections dans les deux autres <xref:System.Windows.Controls.ListBox> contrôles.  
  
 ![Master&#45;exemple pour detail](./media/databindingmasterdetailsample.png "DataBindingMasterDetailSample")  
  
 Les deux choses à noter dans cet exemple sont :  
  
1.  Les trois <xref:System.Windows.Controls.ListBox> lient des contrôles à la même source. Vous définissez le <xref:System.Windows.Data.Binding.Path%2A> propriété de la liaison pour spécifier le niveau de données que vous souhaitez le <xref:System.Windows.Controls.ListBox> à afficher.  
  
2.  Vous devez définir le <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> propriété `true` sur la <xref:System.Windows.Controls.ListBox> contrôles dont la sélection que vous effectuez le suivi. Définition de cette propriété garantit que l’élément sélectionné est toujours défini en tant que le <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>. Ou bien, si le <xref:System.Windows.Controls.ListBox> obtient ses données à partir d’un <xref:System.Windows.Data.CollectionViewSource>, il synchronise automatiquement sélection et la devise.  
  
 La technique est légèrement différente lorsque vous utilisez [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] données. Pour obtenir un exemple, consultez [utiliser le modèle maître / détail avec des données XML hiérarchiques](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.HierarchicalDataTemplate>
- [Effectuer une liaison à une collection et afficher des informations basées sur la sélection](how-to-bind-to-a-collection-and-display-information-based-on-selection.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Vue d’ensemble des modèles de données](data-templating-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
