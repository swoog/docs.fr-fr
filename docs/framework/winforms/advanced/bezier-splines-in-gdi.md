---
title: B&#233;Bézier cardinales dans GDI +
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Bezier splines
- splines [Windows Forms], Bezier
- GDI+, Bezier splines
ms.assetid: 5774ce1e-87d4-4bc7-88c4-4862052781b8
ms.openlocfilehash: 440c532aeb4492711fc533023606cb49c661d989
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54537611"
---
# <a name="b233zier-splines-in-gdi"></a>B&#233;Bézier cardinales dans GDI +
Une spline de Bézier est une courbe spécifiée par quatre points : deux points de terminaison (p1 et p2) et deux points de contrôle (c1 et c2). La courbe commence en p1 et p2 se termine. La courbe ne passe pas par les points de contrôle, mais les points de contrôle agissent comme des aimants qui la courbe dans certaines directions et influencent la courbure de la courbe. L’illustration suivante montre une courbe de Bézier, ainsi que ses points de terminaison et les points de contrôle.  
  
 ![Splines de Bézier](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art11a.gif "Aboutgdip02_art11a")  
  
 La courbe commence à p1 et se déplace vers le point de contrôle c1. La tangente de la courbe en p1 est la ligne dessinée de p1 à c1. La tangente en p2 est la ligne dessinée de c2 à p2.  
  
## <a name="drawing-bzier-splines"></a>Dessiner des Splines de Bézier  
 Pour dessiner une spline de Bézier, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> classe et un <xref:System.Drawing.Pen>. L’instance de la <xref:System.Drawing.Graphics> classe fournit le <xref:System.Drawing.Graphics.DrawBezier%2A> (méthode) et le <xref:System.Drawing.Pen> stocke les attributs, tels que la largeur et la couleur, de la ligne utilisée pour représenter la courbe. Le <xref:System.Drawing.Pen> est passé en tant qu’arguments à la <xref:System.Drawing.Graphics.DrawBezier%2A> (méthode). Les autres arguments passés à la <xref:System.Drawing.Graphics.DrawBezier%2A> méthode sont les points de terminaison et les points de contrôle. L’exemple suivant dessine une spline de Bézier avec le point de départ (0, 0), contrôler les points (40, 20) et (80, 150) et se terminant par le point (100, 10) :  
  
 [!code-csharp[LinesCurvesAndShapes#71](../../../../samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#71)]
 [!code-vb[LinesCurvesAndShapes#71](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#71)]  
  
 L’illustration suivante montre la courbe, les points de contrôle et deux lignes tangents.  
  
 ![Splines de Bézier](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art12.gif "Aboutgdip02_art12")  
  
 Splines de Bézier ont été initialement développés par Pierre Bézier pour la conception de l’industrie automobile. Ils ont fait leurs preuves pour être utile dans de nombreux types de conception assistée par ordinateur et sont également utilisées pour définir les contours des polices. Splines de Bézier peuvent produire une grande variété de formes, certains d'entre eux sont affichés dans l’illustration suivante.  
  
 ![Paths](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art13.gif "Aboutgdip02_art13")  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [Lignes, courbes et formes](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)
- [Génération et dessin de courbes](../../../../docs/framework/winforms/advanced/constructing-and-drawing-curves.md)
- [Guide pratique pour Créer des objets graphiques pour le dessin](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md)
- [Guide pratique pour Créer un stylet](../../../../docs/framework/winforms/advanced/how-to-create-a-pen.md)
