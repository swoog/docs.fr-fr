---
title: 'Procédure : Créer une réflexion'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- creating reflections [WPF]
- brushes [WPF], creating reflections
- reflections [WPF], creating
ms.assetid: 4f017e16-ab80-43c7-98df-03b6bddbb203
ms.openlocfilehash: 61b597cd36fcf0d60f215d9b5403f3b42b21dec4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59105259"
---
# <a name="how-to-create-a-reflection"></a><span data-ttu-id="2cea4-102">Procédure : Créer une réflexion</span><span class="sxs-lookup"><span data-stu-id="2cea4-102">How to: Create a Reflection</span></span>
<span data-ttu-id="2cea4-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.VisualBrush> pour créer une réflexion.</span><span class="sxs-lookup"><span data-stu-id="2cea4-103">This example shows how to use a <xref:System.Windows.Media.VisualBrush> to create a reflection.</span></span> <span data-ttu-id="2cea4-104">Étant donné qu’un <xref:System.Windows.Media.VisualBrush> peut afficher un visuel existant, vous pouvez utiliser cette fonctionnalité pour produire des effets visuels intéressants, tels que des réflexions et des agrandissements.</span><span class="sxs-lookup"><span data-stu-id="2cea4-104">Because a <xref:System.Windows.Media.VisualBrush> can display an existing visual, you can use this capability to produce interesting visual effects, such as reflections and magnification.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2cea4-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="2cea4-105">Example</span></span>  
 <span data-ttu-id="2cea4-106">L’exemple suivant utilise un <xref:System.Windows.Media.VisualBrush> pour créer une réflexion d’un <xref:System.Windows.Controls.Border> qui contient plusieurs éléments.</span><span class="sxs-lookup"><span data-stu-id="2cea4-106">The following example uses a <xref:System.Windows.Media.VisualBrush> to create a reflection of a <xref:System.Windows.Controls.Border> that contains several elements.</span></span> <span data-ttu-id="2cea4-107">L’illustration suivante montre la sortie que l’exemple génère.</span><span class="sxs-lookup"><span data-stu-id="2cea4-107">The following illustration shows the output that this example produces.</span></span>  
  
 <span data-ttu-id="2cea4-108">![Un reflétées objet visuel](./media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")</span><span class="sxs-lookup"><span data-stu-id="2cea4-108">![A reflected Visual object](./media/graphicsmm-visualbrush-reflection-small.jpg "graphicsmm_visualbrush_reflection_small")</span></span>  
<span data-ttu-id="2cea4-109">Objet Visual réfléchi</span><span class="sxs-lookup"><span data-stu-id="2cea4-109">A reflected Visual object</span></span>  
  
 [!code-csharp[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/visualbrush_markup_snip/CSharp/ReflectionExample.cs#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-vb[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/visualbrush_markup_snip/visualbasic/reflectionexample.vb#graphicsmmvisualbrushreflectionexamplewholepage)]
 [!code-xaml[visualbrush_markup_snip#GraphicsMMVisualBrushReflectionExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/visualbrush_markup_snip/XAML/ReflectionExample.xaml#graphicsmmvisualbrushreflectionexamplewholepage)]  
  
 <span data-ttu-id="2cea4-110">Pour l’exemple complet, qui inclut des exemples qui montrent comment agrandir des parties de l’écran et comment créer des réflexions, consultez [VisualBrush, exemple](https://go.microsoft.com/fwlink/?LinkID=160049).</span><span class="sxs-lookup"><span data-stu-id="2cea4-110">For the complete sample, which includes examples that show how to magnify parts of the screen and how to create reflections, see [VisualBrush Sample](https://go.microsoft.com/fwlink/?LinkID=160049).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2cea4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cea4-111">See also</span></span>

- <xref:System.Windows.Media.VisualBrush>
- [<span data-ttu-id="2cea4-112">Peinture avec des objets d'image, de dessin et visuels</span><span class="sxs-lookup"><span data-stu-id="2cea4-112">Painting with Images, Drawings, and Visuals</span></span>](painting-with-images-drawings-and-visuals.md)
