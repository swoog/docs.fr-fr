---
title: "Procédure : Arrondir les angles d'un RectangleGeometry"
ms.date: 03/30/2017
helpviewer_keywords:
- corners [WPF], rounding
- RectangleGeometry class [WPF], rounding corners
- graphics [WPF], rounding corners of RectangleGeometry objects [WPF]
- rounding corners of RectangleGeometry objects [WPF]
ms.assetid: 926644bc-1357-4c0b-ac81-694bd090ae87
ms.openlocfilehash: f00d7a7cd6117318efb17645bbb9df279c97adff
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57378533"
---
# <a name="how-to-round-the-corners-of-a-rectanglegeometry"></a><span data-ttu-id="d39a4-102">Procédure : Arrondir les angles d'un RectangleGeometry</span><span class="sxs-lookup"><span data-stu-id="d39a4-102">How to: Round the Corners of a RectangleGeometry</span></span>
<span data-ttu-id="d39a4-103">Pour arrondir les angles d’un <xref:System.Windows.Media.RectangleGeometry>, définissez son <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> propriétés à une valeur supérieure à zéro.</span><span class="sxs-lookup"><span data-stu-id="d39a4-103">To round the corners of a <xref:System.Windows.Media.RectangleGeometry>, set its <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> properties to a value greater than zero.</span></span> <span data-ttu-id="d39a4-104">Plus les valeurs, plus angles du rectangle.</span><span class="sxs-lookup"><span data-stu-id="d39a4-104">The larger the values, the rounder the rectangle's corners.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d39a4-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="d39a4-105">Example</span></span>  
 <span data-ttu-id="d39a4-106">L’exemple suivant montre plusieurs <xref:System.Windows.Media.RectangleGeometry> objets différents avec <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> paramètres.</span><span class="sxs-lookup"><span data-stu-id="d39a4-106">The following example shows several <xref:System.Windows.Media.RectangleGeometry> objects with different <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> and <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> settings.</span></span> <span data-ttu-id="d39a4-107">Le <xref:System.Windows.Media.RectangleGeometry> les objets sont affichés à l’aide de <xref:System.Windows.Shapes.Path> éléments.</span><span class="sxs-lookup"><span data-stu-id="d39a4-107">The <xref:System.Windows.Media.RectangleGeometry> objects are displayed using <xref:System.Windows.Shapes.Path> elements.</span></span>  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRoundedRectangleGeometryExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/RectangleGeometryRoundedCornerExample.xaml#graphicsmmroundedrectanglegeometryexamplewholepage)]  
  
 <span data-ttu-id="d39a4-108">![Rectangles avec différents RadiusX&#47;paramètres RadiusY](./media/graphicsmm-rounded.png "graphicsmm_rounded")</span><span class="sxs-lookup"><span data-stu-id="d39a4-108">![Rectangles with different RadiusX&#47;RadiusY settings](./media/graphicsmm-rounded.png "graphicsmm_rounded")</span></span>  
<span data-ttu-id="d39a4-109">Rectangles aux angles arrondis</span><span class="sxs-lookup"><span data-stu-id="d39a4-109">Rectangles with Rounded Corners</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d39a4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d39a4-110">See also</span></span>
- [<span data-ttu-id="d39a4-111">Vue d’ensemble de Geometry</span><span class="sxs-lookup"><span data-stu-id="d39a4-111">Geometry Overview</span></span>](geometry-overview.md)
- [<span data-ttu-id="d39a4-112">Créer une forme composite</span><span class="sxs-lookup"><span data-stu-id="d39a4-112">Create a Composite Shape</span></span>](how-to-create-a-composite-shape.md)
- [<span data-ttu-id="d39a4-113">Créer une forme à l’aide d’un PathGeometry</span><span class="sxs-lookup"><span data-stu-id="d39a4-113">Create a Shape by Using a PathGeometry</span></span>](how-to-create-a-shape-by-using-a-pathgeometry.md)
