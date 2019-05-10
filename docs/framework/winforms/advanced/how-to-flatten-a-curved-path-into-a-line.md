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
ms.openlocfilehash: d59a802618ddd5080c651e822ed4c09641f7f170
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645367"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a>Procédure : aplatir un tracé courbe en ligne
Un <xref:System.Drawing.Drawing2D.GraphicsPath> objet stocke une séquence de lignes et de splines de Bézier. Vous pouvez ajouter plusieurs types de courbes (ellipses, arcs, splines cardinales) à un chemin d’accès, mais chaque courbe est converti en une spline de Bézier avant d’être stockée dans le chemin d’accès. Mise à plat d’un chemin d’accès consiste à convertir chaque spline de Bézier dans le chemin d’accès à une séquence de lignes droites. L’illustration suivante montre un chemin d’accès avant et après la mise à plat.  
  
 ![Lignes droites et courbes](./media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")  
  
### <a name="to-flatten-a-path"></a>Pour aplanir un tracé  
  
- Appelez le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode d’un <xref:System.Drawing.Drawing2D.GraphicsPath> objet. Le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode reçoit un argument d’aplatissement qui spécifie la distance maximale entre la trajectoire aplatie et le chemin d’accès d’origine.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- [Lignes, courbes et formes](lines-curves-and-shapes.md)
- [Génération et dessin de tracés](constructing-and-drawing-paths.md)
