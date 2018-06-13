---
title: 'Comment : implémenter un moteur de présentation personnalisé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- layout engines [Windows Forms], custom
- TableLayoutPanel control [Windows Forms], layout engine
- layout engines [Windows Forms], implementing
- FlowLayoutPanel control [Windows Forms], layout engine
ms.assetid: f91aa91c-29f4-4089-95ca-5d48b774b00e
ms.openlocfilehash: 0444f0d03a36adf833c04167c6d7a3c302ab15dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33531295"
---
# <a name="how-to-implement-a-custom-layout-engine"></a><span data-ttu-id="59133-102">Comment : implémenter un moteur de présentation personnalisé</span><span class="sxs-lookup"><span data-stu-id="59133-102">How to: Implement a Custom Layout Engine</span></span>
<span data-ttu-id="59133-103">L’exemple de code suivant montre comment créer un moteur de disposition personnalisée qui effectue une disposition de flux simple.</span><span class="sxs-lookup"><span data-stu-id="59133-103">The following code example demonstrates how to create a custom layout engine that performs a simple flow layout.</span></span> <span data-ttu-id="59133-104">Il implémente un contrôle de panneau de configuration nommé `DemoFlowPanel`, qui remplace le <xref:System.Windows.Forms.Control.LayoutEngine%2A> propriété afin de fournir une instance de la `DemoFlowLayout` classe.</span><span class="sxs-lookup"><span data-stu-id="59133-104">It implements a panel control named `DemoFlowPanel`, which overrides the <xref:System.Windows.Forms.Control.LayoutEngine%2A> property to provide an instance of the `DemoFlowLayout` class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="59133-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="59133-105">Example</span></span>  
 [!code-cpp[System.Windows.Forms.Layout.LayoutEngine#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.Layout.LayoutEngine/cpp/DemoFlowLayout.cpp#1)]
 [!code-csharp[System.Windows.Forms.Layout.LayoutEngine#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Layout.LayoutEngine/CS/DemoFlowLayout.cs#1)]
 [!code-vb[System.Windows.Forms.Layout.LayoutEngine#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Layout.LayoutEngine/VB/DemoFlowLayout.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="59133-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59133-106">See Also</span></span>  
 <xref:System.Windows.Forms.Layout.LayoutEngine>  
 <xref:System.Windows.Forms.Control.LayoutEngine%2A?displayProperty=nameWithType>
