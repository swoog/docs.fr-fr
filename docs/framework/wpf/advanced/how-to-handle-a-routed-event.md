---
title: 'Comment : gérer un événement routé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- routed events [WPF], handling
- bubbling events [WPF]
ms.assetid: 157787b4-f469-4047-8777-5b034145f32e
ms.openlocfilehash: 80b3be439498c0dc448322d1e7daf30202a470dc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-handle-a-routed-event"></a>Comment : gérer un événement routé
Cet exemple illustre le fonctionnement des événements de propagation et indique comment écrire un gestionnaire permettant de traiter les données des événements routés.  
  
## <a name="example"></a>Exemple  
 Dans [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)], les éléments sont organisés dans une structure d’arborescence d’éléments. L’élément parent peut participer à la gestion des événements déclenchés initialement par les éléments enfants dans l’arborescence d’éléments. Ceci est possible grâce au routage d’événement.  
  
 En règle générale, les événements routés respectent l’une des deux stratégies de routage : propagation ou tunneling. Cet exemple se concentre sur l’événement de propagation et utilise le <xref:System.Windows.Controls.Primitives.ButtonBase.Click?displayProperty=nameWithType> événement pour montrer le fonctionnement du routage.  
  
 L’exemple suivant crée deux <xref:System.Windows.Controls.Button> contrôle et utilise [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] syntaxe pour attacher un gestionnaire d’événements à un élément parent commun, qui est dans cet exemple d’attribut <xref:System.Windows.Controls.StackPanel>. Au lieu d’attacher un gestionnaire d’événements pour chaque <xref:System.Windows.Controls.Button> élément enfant, l’exemple utilise la syntaxe d’attribut pour attacher le Gestionnaire d’événements pour le <xref:System.Windows.Controls.StackPanel> élément parent. Ce modèle de gestion des événements indique comment utiliser le routage d’événement afin de réduire le nombre d’éléments attachés à un gestionnaire. Tous les événements de propagation pour chaque <xref:System.Windows.Controls.Button> passent par l’élément parent.  
  
 Notez que sur le parent <xref:System.Windows.Controls.StackPanel> élément, le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> nom de l’événement spécifié comme l’attribut est partiellement qualifié en nommant le <xref:System.Windows.Controls.Button> classe. Le <xref:System.Windows.Controls.Button> classe est un <xref:System.Windows.Controls.Primitives.ButtonBase> classe dérivée qui a le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement dans la liste de membres. Cette technique de qualification partielle permettant d’attacher un gestionnaire d’événements est nécessaire si l’événement géré n’existe pas dans la liste de membres de l’élément auquel le gestionnaire d’événements routés est attaché.  
  
 [!code-xaml[RoutedEventHandle#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventHandle/CSharp/default.xaml#xaml)]  
  
 L’exemple suivant gère le <xref:System.Windows.Controls.Primitives.ButtonBase.Click> événement.  L’exemple signale l’élément qui gère l’événement, ainsi que l’élément qui déclenche l’événement. Le gestionnaire d’événements est exécuté quand l’utilisateur clique sur l’un des boutons.  
  
 [!code-csharp[RoutedEventHandle#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventHandle/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventHandle#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventHandle/VisualBasic/MainWindow.xaml.vb#handler)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.RoutedEvent>  
 [Vue d’ensemble des entrées](../../../../docs/framework/wpf/advanced/input-overview.md)  
 [Vue d’ensemble des événements routés](../../../../docs/framework/wpf/advanced/routed-events-overview.md)  
 [Rubriques de guide pratique](../../../../docs/framework/wpf/advanced/events-how-to-topics.md)  
 [Syntaxe XAML en détail](../../../../docs/framework/wpf/advanced/xaml-syntax-in-detail.md)
