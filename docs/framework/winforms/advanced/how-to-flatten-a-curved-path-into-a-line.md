---
title: 'Procédure : Aplanir un tracé courbé en une ligne'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], flattening curves into lines
- curves [Windows Forms], flattening
- GraphicsPath object
- paths [Windows Forms], flattening
- drawing [Windows Forms], flattening curves
ms.assetid: e654b8de-25f4-4735-9208-42e4514a589c
ms.openlocfilehash: aa47a655417cdf82d79fb222dc6ff6f6d8c3a947
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54601816"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a>Procédure : Aplanir un tracé courbé en une ligne
Un <xref:System.Drawing.Drawing2D.GraphicsPath> objet stocke une séquence de lignes et de splines de Bézier. Vous pouvez ajouter plusieurs types de courbes (ellipses, arcs, splines cardinales) à un chemin d’accès, mais chaque courbe est converti en une spline de Bézier avant d’être stockée dans le chemin d’accès. Mise à plat d’un chemin d’accès consiste à convertir chaque spline de Bézier dans le chemin d’accès à une séquence de lignes droites. L’illustration suivante montre un chemin d’accès avant et après la mise à plat.  
  
 ![Lignes droites et courbes](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")  
  
### <a name="to-flatten-a-path"></a>Pour aplanir un tracé  
  
-   Appelez le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode d’un <xref:System.Drawing.Drawing2D.GraphicsPath> objet. Le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode reçoit un argument d’aplatissement qui spécifie la distance maximale entre la trajectoire aplatie et le chemin d’accès d’origine.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- [Lignes, courbes et formes](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)
- [Génération et dessin de tracés](../../../../docs/framework/winforms/advanced/constructing-and-drawing-paths.md)
