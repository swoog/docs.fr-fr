---
title: 'Procédure : Appliquer un GuidelineSet à un dessin'
ms.date: 03/30/2017
helpviewer_keywords:
- GuidelineSet property [WPF], applying to drawings
- graphics [WPF], GuidelineSet property
ms.assetid: 45f3e0b4-8820-45a7-b865-b8ea5b17b0c8
ms.openlocfilehash: 4bd2ee349f2c1855a9af6b4c00f2630cd50a9108
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54493376"
---
# <a name="how-to-apply-a-guidelineset-to-a-drawing"></a><span data-ttu-id="50cee-102">Procédure : Appliquer un GuidelineSet à un dessin</span><span class="sxs-lookup"><span data-stu-id="50cee-102">How to: Apply a GuidelineSet to a Drawing</span></span>
<span data-ttu-id="50cee-103">Cet exemple montre comment appliquer un <xref:System.Windows.Media.GuidelineSet> à un <xref:System.Windows.Media.DrawingGroup>.</span><span class="sxs-lookup"><span data-stu-id="50cee-103">This example shows how to apply a <xref:System.Windows.Media.GuidelineSet> to a <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
 <span data-ttu-id="50cee-104">Le <xref:System.Windows.Media.DrawingGroup> classe est le seul type de <xref:System.Windows.Media.Drawing> qui a un <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="50cee-104">The <xref:System.Windows.Media.DrawingGroup> class is the only type of <xref:System.Windows.Media.Drawing> that has a <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> property.</span></span> <span data-ttu-id="50cee-105">Pour appliquer un <xref:System.Windows.Media.GuidelineSet> à un autre type de <xref:System.Windows.Media.Drawing>, ajoutez-le à un <xref:System.Windows.Media.DrawingGroup> , puis appliquez le <xref:System.Windows.Media.GuidelineSet> à votre <xref:System.Windows.Media.DrawingGroup>.</span><span class="sxs-lookup"><span data-stu-id="50cee-105">To apply a <xref:System.Windows.Media.GuidelineSet> to another type of <xref:System.Windows.Media.Drawing>, add it to a <xref:System.Windows.Media.DrawingGroup> and then apply the <xref:System.Windows.Media.GuidelineSet> to your <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="50cee-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="50cee-106">Example</span></span>  
 <span data-ttu-id="50cee-107">L’exemple suivant crée deux <xref:System.Windows.Media.DrawingGroup> les objets qui sont presque identiques ; la seule différence est : le second <xref:System.Windows.Media.DrawingGroup> a un <xref:System.Windows.Media.GuidelineSet> et n’est pas le cas de la première.</span><span class="sxs-lookup"><span data-stu-id="50cee-107">The following example creates two <xref:System.Windows.Media.DrawingGroup> objects that are almost identical; the only difference is: the second <xref:System.Windows.Media.DrawingGroup> has a <xref:System.Windows.Media.GuidelineSet> and the first does not.</span></span>  
  
 <span data-ttu-id="50cee-108">L’illustration suivante montre la sortie de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="50cee-108">The following illustration shows the output from the example.</span></span> <span data-ttu-id="50cee-109">Étant donné que la différence de rendu entre les deux <xref:System.Windows.Media.DrawingGroup> objets étant très subtile, certaines parties des dessins sont agrandies.</span><span class="sxs-lookup"><span data-stu-id="50cee-109">Because the rendering difference between the two <xref:System.Windows.Media.DrawingGroup> objects is so subtle, portions of the drawings are enlarged.</span></span>  
  
 <span data-ttu-id="50cee-110">![DrawingGroup avec et sans GuidelineSet](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-drawinggroup-guidelineset.png "graphicsmm_drawinggroup_guidelineset")</span><span class="sxs-lookup"><span data-stu-id="50cee-110">![A DrawingGroup with and without a GuidelineSet](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-drawinggroup-guidelineset.png "graphicsmm_drawinggroup_guidelineset")</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupGuidelineSetExample.cs#graphicsmmdrawinggroupguidelinesetexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupGuidelineSetExample.xaml#graphicsmmdrawinggroupguidelinesetexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="50cee-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50cee-111">See also</span></span>
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.GuidelineSet>
- [<span data-ttu-id="50cee-112">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="50cee-112">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)
