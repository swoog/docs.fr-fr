---
title: 'Comment : rechercher des éléments générés par DataTemplate'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- finding DataTemplate elements [WPF]
- DataTemplate [WPF]
ms.assetid: bfcd564e-5e9e-451e-8641-a9b5c3cfac90
ms.openlocfilehash: d46a408bc1b5fc512905aa5bf176b13bd1511865
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-find-datatemplate-generated-elements"></a>Comment : rechercher des éléments générés par DataTemplate
Cet exemple montre comment rechercher des éléments qui sont générés par un <xref:System.Windows.DataTemplate>.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, il existe un <xref:System.Windows.Controls.ListBox> qui est lié à certains [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] données :  
  
 [!code-xaml[FindGeneratedItems#LB](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#lb)]  
  
 Le <xref:System.Windows.Controls.ListBox> utilise les éléments suivants <xref:System.Windows.DataTemplate>:  
  
 [!code-xaml[FindGeneratedItems#DT](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#dt)]  
  
 Si vous souhaitez récupérer le <xref:System.Windows.Controls.TextBlock> élément généré par le <xref:System.Windows.DataTemplate> une certaine <xref:System.Windows.Controls.ListBoxItem>, vous devez obtenir le <xref:System.Windows.Controls.ListBoxItem>, rechercher le <xref:System.Windows.Controls.ContentPresenter> dans ce <xref:System.Windows.Controls.ListBoxItem>, puis appelez <xref:System.Windows.FrameworkTemplate.FindName%2A> sur la <xref:System.Windows.DataTemplate> qui est défini sur ce <xref:System.Windows.Controls.ContentPresenter>. L’exemple suivant montre comment effectuer ces étapes. À des fins de démonstration, cet exemple crée une boîte de message qui affiche le texte du contenu de la <xref:System.Windows.DataTemplate>-bloc de texte généré.  
  
 [!code-csharp[FindGeneratedItems#DTFindElement](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#dtfindelement)]
 [!code-vb[FindGeneratedItems#DTFindElement](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#dtfindelement)]  
  
 Voici l’implémentation de `FindVisualChild`, qui utilise le <xref:System.Windows.Media.VisualTreeHelper> méthodes :  
  
 [!code-csharp[FindGeneratedItems#FVC](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#fvc)]
 [!code-vb[FindGeneratedItems#FVC](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#fvc)]  
  
## <a name="see-also"></a>Voir aussi  
 [Guide pratique pour rechercher des éléments générés par ControlTemplate](../../../../docs/framework/wpf/controls/how-to-find-controltemplate-generated-elements.md)  
 [Vue d’ensemble de la liaison de données](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)  
 [Application d’un style et création de modèles](../../../../docs/framework/wpf/controls/styling-and-templating.md)  
 [Portées de nom XAML WPF](../../../../docs/framework/wpf/advanced/wpf-xaml-namescopes.md)  
 [Arborescences dans WPF](../../../../docs/framework/wpf/advanced/trees-in-wpf.md)
