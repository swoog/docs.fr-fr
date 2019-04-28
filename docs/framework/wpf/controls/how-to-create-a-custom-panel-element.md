---
title: 'Procédure : Créer un élément Panel personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Panel control [WPF]
- custom Panel elements [WPF]
ms.assetid: e0df4f1e-8c07-4e86-89a3-e22acfffdc2a
ms.openlocfilehash: d4fc9d76ada9f27bd52619280b323691af9382c2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910960"
---
# <a name="how-to-create-a-custom-panel-element"></a>Procédure : Créer un élément Panel personnalisé
## <a name="example"></a>Exemple  
 Cet exemple montre comment substituer le comportement de disposition par défaut de la <xref:System.Windows.Controls.Panel> élément et créer des éléments de disposition personnalisés qui sont dérivés de <xref:System.Windows.Controls.Panel>.  
  
 L’exemple définit un personnalisé simple <xref:System.Windows.Controls.Panel> élément appelé `PlotPanel`, qui positionne les éléments enfants en fonction de deux codées en dur coordonnées x et y-. Dans cet exemple, `x` et `y` sont toutes deux définies sur `50`; par conséquent, tous les éléments enfants sont positionnés à cet emplacement sur le x et y axes.  
  
 Pour implémenter <xref:System.Windows.Controls.Panel> comportements, l’exemple utilise le <xref:System.Windows.FrameworkElement.MeasureOverride%2A> et <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> méthodes. Chaque méthode retourne le <xref:System.Windows.Size> données qui sont nécessaires pour positionner et restituer les éléments enfants.  
  
 [!code-cpp[PlotPanel#1](~/samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Controls.Panel>
- [Vue d’ensemble de Panel](panels-overview.md)
- [Créer un exemple de panneau d’agencement de contenu personnalisé](https://go.microsoft.com/fwlink/?LinkID=159979)
