---
title: 'Procédure : Arrondir les angles d’un RectangleGeometry'
ms.date: 03/30/2017
helpviewer_keywords:
- corners [WPF], rounding
- RectangleGeometry class [WPF], rounding corners
- graphics [WPF], rounding corners of RectangleGeometry objects [WPF]
- rounding corners of RectangleGeometry objects [WPF]
ms.assetid: 926644bc-1357-4c0b-ac81-694bd090ae87
ms.openlocfilehash: eb2f173bedb903e12b2795264c684524cfa09825
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59089131"
---
# <a name="how-to-round-the-corners-of-a-rectanglegeometry"></a><span data-ttu-id="aaa7b-102">Procédure : Arrondir les angles d’un RectangleGeometry</span><span class="sxs-lookup"><span data-stu-id="aaa7b-102">How to: Round the Corners of a RectangleGeometry</span></span>
<span data-ttu-id="aaa7b-103">Pour arrondir les angles d’un <xref:System.Windows.Media.RectangleGeometry>, définissez son <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> propriétés à une valeur supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="aaa7b-103">To round the corners of a <xref:System.Windows.Media.RectangleGeometry>, set its <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> properties to a value greater than zero.</span></span> <span data-ttu-id="aaa7b-104">Plus les valeurs, plus angles du rectangle.</span><span class="sxs-lookup"><span data-stu-id="aaa7b-104">The larger the values, the rounder the rectangle's corners.</span></span>  
  
## <a name="example"></a><span data-ttu-id="aaa7b-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="aaa7b-105">Example</span></span>  
 <span data-ttu-id="aaa7b-106">L’exemple suivant montre plusieurs <xref:System.Windows.Media.RectangleGeometry> objets différents avec <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> paramètres.</span><span class="sxs-lookup"><span data-stu-id="aaa7b-106">The following example shows several <xref:System.Windows.Media.RectangleGeometry> objects with different <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> settings.</span></span> <span data-ttu-id="aaa7b-107">Le <xref:System.Windows.Media.RectangleGeometry> les objets sont affichés à l’aide de <xref:System.Windows.Shapes.Path> éléments.</span><span class="sxs-lookup"><span data-stu-id="aaa7b-107">The <xref:System.Windows.Media.RectangleGeometry> objects are displayed using <xref:System.Windows.Shapes.Path> elements.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRoundedRectangleGeometryExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/RectangleGeometryRoundedCornerExample.xaml#graphicsmmroundedrectanglegeometryexamplewholepage)]  
  
 <span data-ttu-id="aaa7b-108">![Rectangles avec différents RadiusX&#47;paramètres RadiusY](./media/graphicsmm-rounded.png "graphicsmm_rounded")</span><span class="sxs-lookup"><span data-stu-id="aaa7b-108">![Rectangles with different RadiusX&#47;RadiusY settings](./media/graphicsmm-rounded.png "graphicsmm_rounded")</span></span>  
<span data-ttu-id="aaa7b-109">Rectangles aux angles arrondis</span><span class="sxs-lookup"><span data-stu-id="aaa7b-109">Rectangles with Rounded Corners</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aaa7b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaa7b-110">See also</span></span>

- [<span data-ttu-id="aaa7b-111">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="aaa7b-111">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="aaa7b-112">Créer une forme composite</span><span class="sxs-lookup"><span data-stu-id="aaa7b-112">Create a Composite Shape</span></span>](how-to-create-a-composite-shape.md)
- [<span data-ttu-id="aaa7b-113">Créer une forme à l’aide d’un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="aaa7b-113">Create a Shape by Using a PathGeometry</span></span>](how-to-create-a-shape-by-using-a-pathgeometry.md)
