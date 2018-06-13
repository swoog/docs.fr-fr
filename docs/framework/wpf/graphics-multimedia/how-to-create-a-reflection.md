---
title: 'Comment : créer une réflexion'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- creating reflections [WPF]
- brushes [WPF], creating reflections
- reflections [WPF], creating
ms.assetid: 4f017e16-ab80-43c7-98df-03b6bddbb203
ms.openlocfilehash: c791dbbe02faaba790c650d482db092702730fa6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33560574"
---
# <a name="how-to-create-a-reflection"></a><span data-ttu-id="a1023-102">Comment : créer une réflexion</span><span class="sxs-lookup"><span data-stu-id="a1023-102">How to: Create a Reflection</span></span>
<span data-ttu-id="a1023-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.VisualBrush> pour créer une réflexion.</span><span class="sxs-lookup"><span data-stu-id="a1023-103">This example shows how to use a <xref:System.Windows.Media.VisualBrush> to create a reflection.</span></span> <span data-ttu-id="a1023-104">Car un <xref:System.Windows.Media.VisualBrush> peut afficher un effet visuel existant, vous pouvez utiliser cette fonctionnalité pour produire des effets visuels intéressants, tels que des réflexions et le facteur de zoom.</span><span class="sxs-lookup"><span data-stu-id="a1023-104">Because a <xref:System.Windows.Media.VisualBrush> can display an existing visual, you can use this capability to produce interesting visual effects, such as reflections and magnification.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a1023-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a1023-105">Example</span></span>  
 <span data-ttu-id="a1023-106">L’exemple suivant utilise un <xref:System.Windows.Media.VisualBrush> pour créer une réflexion d’un <xref:System.Windows.Controls.Border> qui contient plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="a1023-106">The following example uses a <xref:System.Windows.Media.VisualBrush> to create a reflection of a <xref:System.Windows.Controls.Border> that contains several elements.</span></span> <span data-ttu-id="a1023-107">L’illustration suivante montre la sortie que l’exemple génère.</span><span class="sxs-lookup"><span data-stu-id="a1023-107">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="a1023-108">![A reflétées objet visuel](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")</span><span class="sxs-lookup"><span data-stu-id="a1023-108">![A reflected Visual object](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")</span></span>  
<span data-ttu-id="a1023-109">Objet Visual réfléchi</span><span class="sxs-lookup"><span data-stu-id="a1023-109">A reflected Visual object</span></span>  
  
 [!code-csharp[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/ReflectionExample.cs#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-vb[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/reflectionexample.vb#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-xaml[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/ReflectionExample.xaml#graphicsmmvisualbrushreflectionexamplewholepage)]  
  
 <span data-ttu-id="a1023-110">Pour l’exemple complet, qui inclut des exemples qui montrent comment agrandir des parties de l’écran et créer des réflexions, consultez [VisualBrush, exemple](http://go.microsoft.com/fwlink/?LinkID=160049).</span><span class="sxs-lookup"><span data-stu-id="a1023-110">For the complete sample, which includes examples that show how to magnify parts of the screen and how to create reflections, see [VisualBrush Sample](http://go.microsoft.com/fwlink/?LinkID=160049).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1023-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1023-111">See Also</span></span>  
 <xref:System.Windows.Media.VisualBrush>  
 [<span data-ttu-id="a1023-112">Peinture avec des images, des dessins et des objets visuels</span><span class="sxs-lookup"><span data-stu-id="a1023-112">Painting with Images, Drawings, and Visuals</span></span>](../../../../docs/framework/wpf/graphics-multimedia/painting-with-images-drawings-and-visuals.md)
