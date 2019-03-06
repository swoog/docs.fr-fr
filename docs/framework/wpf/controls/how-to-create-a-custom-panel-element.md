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
ms.openlocfilehash: 2e778adfb79a64c8f248992aee92de9471906129
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57368699"
---
# <a name="how-to-create-a-custom-panel-element"></a><span data-ttu-id="174a1-102">Procédure : Créer un élément Panel personnalisé</span><span class="sxs-lookup"><span data-stu-id="174a1-102">How to: Create a Custom Panel Element</span></span>
## <a name="example"></a><span data-ttu-id="174a1-103">Exemple</span><span class="sxs-lookup"><span data-stu-id="174a1-103">Example</span></span>  
 <span data-ttu-id="174a1-104">Cet exemple montre comment substituer le comportement de disposition par défaut de la <xref:System.Windows.Controls.Panel> élément et créer des éléments de disposition personnalisés qui sont dérivés de <xref:System.Windows.Controls.Panel>.</span><span class="sxs-lookup"><span data-stu-id="174a1-104">This example shows how to override the default layout behavior of the <xref:System.Windows.Controls.Panel> element and create custom layout elements that are derived from <xref:System.Windows.Controls.Panel>.</span></span>  
  
 <span data-ttu-id="174a1-105">L’exemple définit un personnalisé simple <xref:System.Windows.Controls.Panel> élément appelé `PlotPanel`, qui positionne les éléments enfants en fonction de deux codées en dur coordonnées x et y-.</span><span class="sxs-lookup"><span data-stu-id="174a1-105">The example defines a simple custom <xref:System.Windows.Controls.Panel> element called `PlotPanel`, which positions child elements according to two hard-coded x- and y-coordinates.</span></span> <span data-ttu-id="174a1-106">Dans cet exemple, `x` et `y` sont toutes deux définies sur `50`; par conséquent, tous les éléments enfants sont positionnés à cet emplacement sur le x et y axes.</span><span class="sxs-lookup"><span data-stu-id="174a1-106">In this example, `x` and `y` are both set to `50`; therefore, all child elements are positioned at that location on the x and y axes.</span></span>  
  
 <span data-ttu-id="174a1-107">Pour implémenter <xref:System.Windows.Controls.Panel> comportements, l’exemple utilise le <xref:System.Windows.FrameworkElement.MeasureOverride%2A> et <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> méthodes.</span><span class="sxs-lookup"><span data-stu-id="174a1-107">To implement custom <xref:System.Windows.Controls.Panel> behaviors, the example uses the <xref:System.Windows.FrameworkElement.MeasureOverride%2A> and <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> methods.</span></span> <span data-ttu-id="174a1-108">Chaque méthode retourne le <xref:System.Windows.Size> données qui sont nécessaires pour positionner et restituer les éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="174a1-108">Each method returns the <xref:System.Windows.Size> data that is necessary to position and render child elements.</span></span>  
  
 [!code-cpp[PlotPanel#1](~/samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="174a1-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="174a1-109">See also</span></span>
- <xref:System.Windows.Controls.Panel>
- [<span data-ttu-id="174a1-110">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="174a1-110">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="174a1-111">Créer un exemple de panneau d’agencement de contenu personnalisé</span><span class="sxs-lookup"><span data-stu-id="174a1-111">Create a Custom Content-Wrapping Panel Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=159979)
