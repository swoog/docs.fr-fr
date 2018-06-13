---
title: 'Comment : créer un élément Panel personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Panel control [WPF]
- custom Panel elements [WPF]
ms.assetid: e0df4f1e-8c07-4e86-89a3-e22acfffdc2a
ms.openlocfilehash: 2d1581ef1d0130a6952becf36d668e6a198e1ee9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552398"
---
# <a name="how-to-create-a-custom-panel-element"></a>Comment : créer un élément Panel personnalisé
## <a name="example"></a>Exemple  
 Cet exemple montre comment substituer le comportement de mise en page par défaut de la <xref:System.Windows.Controls.Panel> élément et créer des éléments de disposition personnalisés qui sont dérivés de <xref:System.Windows.Controls.Panel>.  
  
 L’exemple définit un personnalisé simple <xref:System.Windows.Controls.Panel> élément appelé `PlotPanel`, ce qui positionne des éléments enfants en fonction de deux codées en dur coordonnées x et y-. Dans cet exemple, `x` et `y` sont toutes deux définies sur `50`; par conséquent, tous les éléments enfants sont positionnés à cet emplacement sur le x et y axes.  
  
 Pour implémenter des <xref:System.Windows.Controls.Panel> comportements, l’exemple utilise le <xref:System.Windows.FrameworkElement.MeasureOverride%2A> et <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> méthodes. Chaque méthode retourne les <xref:System.Windows.Size> données qui sont nécessaires pour positionner et restituer les éléments enfants.  
  
 [!code-cpp[PlotPanel#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Controls.Panel>  
 [Vue d’ensemble de Panel](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [Créer un exemple de panneau d’habillage du contenu personnalisé](http://go.microsoft.com/fwlink/?LinkID=159979)
