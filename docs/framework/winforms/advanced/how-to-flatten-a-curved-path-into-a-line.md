---
title: 'Procédure : aplatir un tracé courbe en ligne'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], flattening curves into lines
- curves [Windows Forms], flattening
- GraphicsPath object
- paths [Windows Forms], flattening
- drawing [Windows Forms], flattening curves
ms.assetid: e654b8de-25f4-4735-9208-42e4514a589c
ms.openlocfilehash: a151b4244e14d3704fd5fa1c55de92211981232f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59215155"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a>Procédure : aplatir un tracé courbe en ligne
Un <xref:System.Drawing.Drawing2D.GraphicsPath> objet stocke une séquence de lignes et de splines de Bézier. Vous pouvez ajouter plusieurs types de courbes (ellipses, arcs, splines cardinales) à un chemin d’accès, mais chaque courbe est converti en une spline de Bézier avant d’être stockée dans le chemin d’accès. Mise à plat d’un chemin d’accès consiste à convertir chaque spline de Bézier dans le chemin d’accès à une séquence de lignes droites. L’illustration suivante montre un chemin d’accès avant et après la mise à plat.  
  
 ![Lignes droites et courbes](./media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")  
  
### <a name="to-flatten-a-path"></a>Pour aplanir un tracé  
  
-   Appelez le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode d’un <xref:System.Drawing.Drawing2D.GraphicsPath> objet. Le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode reçoit un argument d’aplatissement qui spécifie la distance maximale entre la trajectoire aplatie et le chemin d’accès d’origine.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- [Lignes, courbes et formes](lines-curves-and-shapes.md)
- [Génération et dessin de tracés](constructing-and-drawing-paths.md)
