---
title: "Comment : utiliser les propriétés jointes d'une zone de dessin pour positionner des éléments enfants"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- attached properties [WPF Designer]
- Canvas control [WPF], attached properties
ms.assetid: 48f1d25d-3820-4107-a4cc-d6c1e5664a44
ms.openlocfilehash: 89327b834dfd71c0a7420eb42a598b98cdb5e9d8
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45668299"
---
# <a name="how-to-use-the-attached-properties-of-canvas-to-position-child-elements"></a><span data-ttu-id="beb52-102">Comment : utiliser les propriétés jointes d'une zone de dessin pour positionner des éléments enfants</span><span class="sxs-lookup"><span data-stu-id="beb52-102">How to: Use the Attached Properties of Canvas to Position Child Elements</span></span>
<span data-ttu-id="beb52-103">Cet exemple montre comment utiliser les propriétés jointes de <xref:System.Windows.Controls.Canvas> pour positionner des éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="beb52-103">This example shows how to use the attached properties of <xref:System.Windows.Controls.Canvas> to position child elements.</span></span>  
  
## <a name="example"></a><span data-ttu-id="beb52-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="beb52-104">Example</span></span>  
 <span data-ttu-id="beb52-105">L’exemple suivant ajoute quatre <xref:System.Windows.Controls.Button> éléments en tant qu’éléments enfants d’un parent <xref:System.Windows.Controls.Canvas>.</span><span class="sxs-lookup"><span data-stu-id="beb52-105">The following example adds four <xref:System.Windows.Controls.Button> elements as child elements of a parent <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="beb52-106">Chaque élément est représenté par un <xref:System.Windows.Controls.Canvas.Bottom%2A>, <xref:System.Windows.Controls.Canvas.Left%2A>, <xref:System.Windows.Controls.Canvas.Right%2A>, et <xref:System.Windows.Controls.Canvas.Top%2A>.</span><span class="sxs-lookup"><span data-stu-id="beb52-106">Each element is represented by a <xref:System.Windows.Controls.Canvas.Bottom%2A>, <xref:System.Windows.Controls.Canvas.Left%2A>, <xref:System.Windows.Controls.Canvas.Right%2A>, and <xref:System.Windows.Controls.Canvas.Top%2A>.</span></span>
<span data-ttu-id="beb52-107">Chaque <xref:System.Windows.Controls.Button> est positionné par rapport au parent <xref:System.Windows.Controls.Canvas> , en fonction de sa valeur de propriété assignée.</span><span class="sxs-lookup"><span data-stu-id="beb52-107">Each <xref:System.Windows.Controls.Button> is positioned relative to the parent <xref:System.Windows.Controls.Canvas> and according to its assigned property value.</span></span>  
  
 [!code-cpp[CanvasAttachedProperties#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/CanvasAttachedProperties/CPP/CanvasAttachedProps.cpp#1)]
 [!code-csharp[CanvasAttachedProperties#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasAttachedProperties/CSharp/CanvasAttachedProps.cs#1)]
 [!code-vb[CanvasAttachedProperties#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasAttachedProperties/VisualBasic/CanvasAttachedProps.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="beb52-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beb52-108">See Also</span></span>  
 <xref:System.Windows.Controls.Canvas>  
 <xref:System.Windows.Controls.Canvas.Bottom%2A>  
 <xref:System.Windows.Controls.Canvas.Left%2A>  
 <xref:System.Windows.Controls.Canvas.Right%2A>  
 <xref:System.Windows.Controls.Canvas.Top%2A>  
 <xref:System.Windows.Controls.Button>  
 [<span data-ttu-id="beb52-109">Vue d’ensemble de Panel</span><span class="sxs-lookup"><span data-stu-id="beb52-109">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [<span data-ttu-id="beb52-110">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="beb52-110">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/canvas-how-to-topics.md)  
 [<span data-ttu-id="beb52-111">Vue d'ensemble des propriétés jointes</span><span class="sxs-lookup"><span data-stu-id="beb52-111">Attached Properties Overview</span></span>](../../../../docs/framework/wpf/advanced/attached-properties-overview.md)
