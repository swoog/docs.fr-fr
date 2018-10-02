---
title: 'Comment : appliquer plusieurs transformations à un objet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- grouping Transform objects [WPF]
- Transform objects [WPF], grouping
- graphics [WPF], grouping Transform objects
- TransformGroup [WPF]
ms.assetid: 98cd1921-12bc-4bf5-8193-529228fb7402
ms.openlocfilehash: 0700a7ae3f18f745b0d479ace3acbf2d7fbd9722
ms.sourcegitcommit: daa8788af67ac2d1cecd24f9f3409babb2f978c9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47861989"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a><span data-ttu-id="cde1c-102">Comment : appliquer plusieurs transformations à un objet</span><span class="sxs-lookup"><span data-stu-id="cde1c-102">How to: Apply Multiple Transforms to an Object</span></span>
<span data-ttu-id="cde1c-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.TransformGroup> au groupe de deux ou plusieurs <xref:System.Windows.Media.Transform> des objets dans un composite unique <xref:System.Windows.Media.Transform>.</span><span class="sxs-lookup"><span data-stu-id="cde1c-103">This example shows how to use a <xref:System.Windows.Media.TransformGroup> to group two or more <xref:System.Windows.Media.Transform> objects into a single composite <xref:System.Windows.Media.Transform>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cde1c-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="cde1c-104">Example</span></span>  
 <span data-ttu-id="cde1c-105">L’exemple suivant utilise un <xref:System.Windows.Media.TransformGroup> pour appliquer un <xref:System.Windows.Media.ScaleTransform> et un <xref:System.Windows.Media.RotateTransform> à un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="cde1c-105">The following example uses a <xref:System.Windows.Media.TransformGroup> to apply a <xref:System.Windows.Media.ScaleTransform> and a <xref:System.Windows.Media.RotateTransform> to a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[Transforms_snip#MultipleTransformExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MultipleTransformExample.xaml#multipletransformexamplewholepage)]  
  
 [!code-csharp[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/MultipleTransformsExample.cs#multipletransformscodeexamplewholepage)]
 [!code-vb[Transforms_Procedural_snip#MultipleTransformsCodeExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/MultipleTransformsExample.vb#multipletransformscodeexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="cde1c-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cde1c-106">See Also</span></span>  
 <xref:System.Windows.UIElement.RenderTransform%2A>  
 <xref:System.Windows.Media.TransformGroup>  
 [<span data-ttu-id="cde1c-107">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="cde1c-107">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)  
 [<span data-ttu-id="cde1c-108">Exemple de transformations 2D</span><span class="sxs-lookup"><span data-stu-id="cde1c-108">2-D Transforms Sample</span></span>](https://go.microsoft.com/fwlink/?LinkID=158252)
