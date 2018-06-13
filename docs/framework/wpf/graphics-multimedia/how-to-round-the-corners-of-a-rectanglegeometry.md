---
title: "Comment : arrondir les angles d'un RectangleGeometry"
ms.date: 03/30/2017
helpviewer_keywords:
- corners [WPF], rounding
- RectangleGeometry class [WPF], rounding corners
- graphics [WPF], rounding corners of RectangleGeometry objects [WPF]
- rounding corners of RectangleGeometry objects [WPF]
ms.assetid: 926644bc-1357-4c0b-ac81-694bd090ae87
ms.openlocfilehash: e4f1d37e2c0f26967affff14ed6475fc8c0cb28c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33561639"
---
# <a name="how-to-round-the-corners-of-a-rectanglegeometry"></a><span data-ttu-id="ccfa4-102">Comment : arrondir les angles d'un RectangleGeometry</span><span class="sxs-lookup"><span data-stu-id="ccfa4-102">How to: Round the Corners of a RectangleGeometry</span></span>
<span data-ttu-id="ccfa4-103">Pour arrondir les angles d’un <xref:System.Windows.Media.RectangleGeometry>, définissez son <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> propriétés à une valeur supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="ccfa4-103">To round the corners of a <xref:System.Windows.Media.RectangleGeometry>, set its <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> properties to a value greater than zero.</span></span> <span data-ttu-id="ccfa4-104">Plus les valeurs, plus angles du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ccfa4-104">The larger the values, the rounder the rectangle's corners.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ccfa4-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="ccfa4-105">Example</span></span>  
 <span data-ttu-id="ccfa4-106">L’exemple suivant montre plusieurs <xref:System.Windows.Media.RectangleGeometry> objets avec différentes <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> paramètres.</span><span class="sxs-lookup"><span data-stu-id="ccfa4-106">The following example shows several <xref:System.Windows.Media.RectangleGeometry> objects with different <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> settings.</span></span> <span data-ttu-id="ccfa4-107">Le <xref:System.Windows.Media.RectangleGeometry> les objets sont affichés à l’aide de <xref:System.Windows.Shapes.Path> éléments.</span><span class="sxs-lookup"><span data-stu-id="ccfa4-107">The <xref:System.Windows.Media.RectangleGeometry> objects are displayed using <xref:System.Windows.Shapes.Path> elements.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRoundedRectangleGeometryExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/RectangleGeometryRoundedCornerExample.xaml#graphicsmmroundedrectanglegeometryexamplewholepage)]  
  
 <span data-ttu-id="ccfa4-108">![Rectangles avec différents paramètres RadiusX&#47;paramètres RadiusY](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-rounded.png "graphicsmm_rounded")</span><span class="sxs-lookup"><span data-stu-id="ccfa4-108">![Rectangles with different RadiusX&#47;RadiusY settings](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-rounded.png "graphicsmm_rounded")</span></span>  
<span data-ttu-id="ccfa4-109">Rectangles à angles arrondis</span><span class="sxs-lookup"><span data-stu-id="ccfa4-109">Rectangles with Rounded Corners</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccfa4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccfa4-110">See Also</span></span>  
 [<span data-ttu-id="ccfa4-111">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="ccfa4-111">Geometry Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)  
 [<span data-ttu-id="ccfa4-112">Créer une forme composite</span><span class="sxs-lookup"><span data-stu-id="ccfa4-112">Create a Composite Shape</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-composite-shape.md)  
 [<span data-ttu-id="ccfa4-113">Créer une forme à l’aide d’un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="ccfa4-113">Create a Shape by Using a PathGeometry</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md)
