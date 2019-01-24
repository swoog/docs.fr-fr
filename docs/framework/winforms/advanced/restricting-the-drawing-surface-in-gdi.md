---
title: Restriction de la surface de dessin dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, clipping
- clipping [Windows Forms], using GDI+
- GDI+, restricting drawing surface
ms.assetid: 8b5f71d9-d2f0-4540-9c41-740f90fd4c26
ms.openlocfilehash: 3784c833098a5585c5cdc38014d5a9542daf39f2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54583393"
---
# <a name="restricting-the-drawing-surface-in-gdi"></a><span data-ttu-id="04d26-102">Restriction de la surface de dessin dans GDI+</span><span class="sxs-lookup"><span data-stu-id="04d26-102">Restricting the Drawing Surface in GDI+</span></span>
<span data-ttu-id="04d26-103">Le découpage consiste à restreindre le dessin à un rectangle ou une région.</span><span class="sxs-lookup"><span data-stu-id="04d26-103">Clipping involves restricting drawing to a certain rectangle or region.</span></span> <span data-ttu-id="04d26-104">L’illustration suivante montre la chaîne « Hello » attachée à une région en forme de cœur.</span><span class="sxs-lookup"><span data-stu-id="04d26-104">The following illustration shows the string "Hello" clipped to a heart-shaped region.</span></span>  
  
 <span data-ttu-id="04d26-105">![Surface de dessin restreinte](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art30.gif "AboutGdip02_Art30")</span><span class="sxs-lookup"><span data-stu-id="04d26-105">![Restricted Drawing Surface](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art30.gif "AboutGdip02_Art30")</span></span>  
  
## <a name="clipping-with-regions"></a><span data-ttu-id="04d26-106">Découpage avec des régions</span><span class="sxs-lookup"><span data-stu-id="04d26-106">Clipping with Regions</span></span>  
 <span data-ttu-id="04d26-107">Régions peuvent être construites à partir de chemins d’accès et les chemins peuvent contenir des contours des chaînes, vous pouvez donc utiliser texte avec contour pour le découpage.</span><span class="sxs-lookup"><span data-stu-id="04d26-107">Regions can be constructed from paths, and paths can contain the outlines of strings, so you can use outlined text for clipping.</span></span> <span data-ttu-id="04d26-108">L’illustration suivante montre un ensemble de points de suspension concentriques découpé à l’intérieur d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="04d26-108">The following illustration shows a set of concentric ellipses clipped to the interior of a string of text.</span></span>  
  
 <span data-ttu-id="04d26-109">![Surface de dessin restreinte](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art31.gif "AboutGdip02_Art31")</span><span class="sxs-lookup"><span data-stu-id="04d26-109">![Restricted Drawing Surface](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art31.gif "AboutGdip02_Art31")</span></span>  
  
 <span data-ttu-id="04d26-110">Pour dessiner avec un découpage, créez un <xref:System.Drawing.Graphics> de l’objet, définissez son <xref:System.Drawing.Graphics.Clip%2A> propriété, puis appelez les méthodes de dessin de même <xref:System.Drawing.Graphics> objet :</span><span class="sxs-lookup"><span data-stu-id="04d26-110">To draw with clipping, create a <xref:System.Drawing.Graphics> object, set its <xref:System.Drawing.Graphics.Clip%2A> property, and then call the drawing methods of that same <xref:System.Drawing.Graphics> object:</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#91](../../../../samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#91)]
 [!code-vb[LinesCurvesAndShapes#91](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#91)]  
  
## <a name="see-also"></a><span data-ttu-id="04d26-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04d26-111">See also</span></span>
- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Region?displayProperty=nameWithType>
- [<span data-ttu-id="04d26-112">Lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="04d26-112">Lines, Curves, and Shapes</span></span>](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)
- [<span data-ttu-id="04d26-113">Utilisation de régions</span><span class="sxs-lookup"><span data-stu-id="04d26-113">Using Regions</span></span>](../../../../docs/framework/winforms/advanced/using-regions.md)
