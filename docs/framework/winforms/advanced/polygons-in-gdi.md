---
title: Polygones dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- polygons
- drawing [Windows Forms], polygons
- GDI+, polygons
ms.assetid: a72213d2-d69a-4c2b-a75c-be7b20390c13
ms.openlocfilehash: 2b1e3d387e4d056d9187c54dcef560544206c370
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132624"
---
# <a name="polygons-in-gdi"></a>Polygones dans GDI+
Un polygone est une forme fermée avec trois ou quatre côtés. Par exemple, un triangle est un polygone à trois côtés, un rectangle est un polygone avec les quatre côtés et un pentagone est un polygone à cinq côtés. L’illustration suivante montre plusieurs polygones.  
  
 ![Polygons](./media/aboutgdip02-art07.gif "Aboutgdip02_art07")  
  
## <a name="drawing-a-polygon"></a>Dessin d’un polygone  
 Pour dessiner un polygone, vous devez un <xref:System.Drawing.Graphics> objet, un <xref:System.Drawing.Pen> objet et un tableau de <xref:System.Drawing.Point> (ou <xref:System.Drawing.PointF>) objets. Le <xref:System.Drawing.Graphics> objet fournit le <xref:System.Drawing.Graphics.DrawPolygon%2A> (méthode). Le <xref:System.Drawing.Pen> objet stocke les attributs, tels que la largeur et la couleur, de la ligne utilisée pour restituer le polygone et le tableau de <xref:System.Drawing.Point> objets stocke les points à relier par des lignes droites. Le <xref:System.Drawing.Pen> objet et le tableau de <xref:System.Drawing.Point> objets sont passés comme arguments pour le <xref:System.Drawing.Graphics.DrawPolygon%2A> (méthode). L’exemple suivant dessine un polygone à trois côtés. Notez qu’il n’y a uniquement trois points dans `myPointArray`: (0, 0), (50, 30) et (30, 60). Le <xref:System.Drawing.Graphics.DrawPolygon%2A> méthode ferme automatiquement le polygone en dessinant une ligne à partir de (30, 60) par le point de départ (0, 0).  
  
 [!code-csharp[LinesCurvesAndShapes#111](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#111)]
 [!code-vb[LinesCurvesAndShapes#111](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#111)]  
  
 L’illustration suivante montre le polygone.  
  
 ![Polygon](./media/aboutgdip02-art08.gif "Aboutgdip02_art08")  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [Lignes, courbes et formes](lines-curves-and-shapes.md)
- [Guide pratique pour Créer un stylet](how-to-create-a-pen.md)
