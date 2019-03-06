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
# <a name="how-to-round-the-corners-of-a-rectanglegeometry"></a>Procédure : Arrondir les angles d'un RectangleGeometry
Pour arrondir les angles d’un <xref:System.Windows.Media.RectangleGeometry>, définissez son <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> propriétés à une valeur supérieure à zéro. Plus les valeurs, plus angles du rectangle.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre plusieurs <xref:System.Windows.Media.RectangleGeometry> objets différents avec <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> et <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> paramètres. Le <xref:System.Windows.Media.RectangleGeometry> les objets sont affichés à l’aide de <xref:System.Windows.Shapes.Path> éléments.  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRoundedRectangleGeometryExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/RectangleGeometryRoundedCornerExample.xaml#graphicsmmroundedrectanglegeometryexamplewholepage)]  
  
 ![Rectangles avec différents RadiusX&#47;paramètres RadiusY](./media/graphicsmm-rounded.png "graphicsmm_rounded")  
Rectangles aux angles arrondis  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de Geometry](geometry-overview.md)
- [Créer une forme composite](how-to-create-a-composite-shape.md)
- [Créer une forme à l’aide d’un PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md)
