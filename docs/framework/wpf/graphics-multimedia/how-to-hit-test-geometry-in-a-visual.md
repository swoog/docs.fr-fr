---
title: 'Procédure : Effectuer un test de positionnement avec Geometry dans un Visual'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], on visual objects comprising Geometry objects [WPF]
- visual objects [WPF], hit tests on
- Geometry objects [WPF], visual objects comprising
ms.assetid: 8bf2643f-d7f9-4cb4-9ea6-5b893c23200d
ms.openlocfilehash: 87b626e575d889447ef061d1ed62ef28efe5dfeb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947340"
---
# <a name="how-to-hit-test-geometry-in-a-visual"></a><span data-ttu-id="063b1-102">Procédure : Effectuer un test de positionnement avec Geometry dans un Visual</span><span class="sxs-lookup"><span data-stu-id="063b1-102">How to: Hit Test Geometry in a Visual</span></span>
<span data-ttu-id="063b1-103">Cet exemple montre comment effectuer un test de positionnement sur un objet visuel composé d’un ou plusieurs <xref:System.Windows.Media.Geometry> objets.</span><span class="sxs-lookup"><span data-stu-id="063b1-103">This example shows how to perform a hit test on a visual object that is composed of one or more <xref:System.Windows.Media.Geometry> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="063b1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="063b1-104">Example</span></span>  
 <span data-ttu-id="063b1-105">L’exemple suivant montre comment récupérer le <xref:System.Windows.Media.DrawingGroup> à partir d’un objet visuel qui utilise le <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="063b1-105">The following example shows how to retrieve the <xref:System.Windows.Media.DrawingGroup> from a visual object that uses the <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> method.</span></span> <span data-ttu-id="063b1-106">Un test de positionnement est ensuite effectué sur le contenu rendu de chaque dessin dans le <xref:System.Windows.Media.DrawingGroup> pour déterminer la géométrie atteinte.</span><span class="sxs-lookup"><span data-stu-id="063b1-106">A hit test is then performed on the rendered content of each drawing in the <xref:System.Windows.Media.DrawingGroup> to determine which geometry was hit.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="063b1-107">Dans la plupart des cas, vous utiliseriez le <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> méthode pour déterminer si un point croise le contenu rendu d’un objet visuel.</span><span class="sxs-lookup"><span data-stu-id="063b1-107">In most cases, you would use the <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> method to determine whether a point intersects any of the rendered content of a visual.</span></span>  
  
 [!code-csharp[VisualsOverview#VisualsOverviewSnippet4](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsOverview/CSharp/Window1.xaml.cs#visualsoverviewsnippet4)]
 [!code-vb[VisualsOverview#VisualsOverviewSnippet4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsOverview/visualbasic/window1.xaml.vb#visualsoverviewsnippet4)]  
  
 <span data-ttu-id="063b1-108">Le <xref:System.Windows.Media.Geometry.FillContains%2A> méthode est une méthode surchargée qui vous permet de test de positionnement en utilisant un <xref:System.Windows.Point> ou <xref:System.Windows.Media.Geometry>.</span><span class="sxs-lookup"><span data-stu-id="063b1-108">The <xref:System.Windows.Media.Geometry.FillContains%2A> method is an overloaded method that allows you to hit test by using a specified <xref:System.Windows.Point> or <xref:System.Windows.Media.Geometry>.</span></span> <span data-ttu-id="063b1-109">Si une géométrie est barrée, le trait peut s’étendre en dehors des limites du remplissage.</span><span class="sxs-lookup"><span data-stu-id="063b1-109">If a geometry is stroked, the stroke can extend outside the fill bounds.</span></span> <span data-ttu-id="063b1-110">Dans ce cas, vous souhaitez appeler <xref:System.Windows.Media.Geometry.StrokeContains%2A> outre <xref:System.Windows.Media.Geometry.FillContains%2A>.</span><span class="sxs-lookup"><span data-stu-id="063b1-110">In which case, you may want to call <xref:System.Windows.Media.Geometry.StrokeContains%2A> in addition to <xref:System.Windows.Media.Geometry.FillContains%2A>.</span></span>  
  
 <span data-ttu-id="063b1-111">Vous pouvez également fournir un <xref:System.Windows.Media.ToleranceType> qui est utilisé dans le cadre de la mise à plat de Bézier.</span><span class="sxs-lookup"><span data-stu-id="063b1-111">You can also provide a <xref:System.Windows.Media.ToleranceType> that is used for the purposes of Bezier flattening.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="063b1-112">Cet exemple ne prend pas en compte les transformations ou les découpages qui peuvent être appliqués à la géométrie.</span><span class="sxs-lookup"><span data-stu-id="063b1-112">This sample does not take into account any transforms or clipping that may be applied to the geometry.</span></span> <span data-ttu-id="063b1-113">En outre, cet exemple ne fonctionnera pas avec un contrôle sur lequel est appliqué un style, car aucun dessin ne lui est directement associé.</span><span class="sxs-lookup"><span data-stu-id="063b1-113">In addition, this sample will not work with a styled control, since it does not have any drawings directly associated with it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="063b1-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="063b1-114">See also</span></span>

- [<span data-ttu-id="063b1-115">Test de positionnement dans la couche visuelle</span><span class="sxs-lookup"><span data-stu-id="063b1-115">Hit Testing in the Visual Layer</span></span>](hit-testing-in-the-visual-layer.md)
- [<span data-ttu-id="063b1-116">Effectuer un test de positionnement avec Geometry comme paramètre</span><span class="sxs-lookup"><span data-stu-id="063b1-116">Hit Test Using Geometry as a Parameter</span></span>](how-to-hit-test-using-geometry-as-a-parameter.md)
