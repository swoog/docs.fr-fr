---
title: Splines cardinales dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- splines [Windows Forms], cardinal
- GDI+, cardinal splines
- cardinal splines
ms.assetid: 09b3797a-6294-422d-9adf-a5a0a7695c0c
ms.openlocfilehash: f7d04f59e2424b71eb5bd0015f9496e6e67edbfa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54589530"
---
# <a name="cardinal-splines-in-gdi"></a>Splines cardinales dans GDI+
Une spline cardinale est une séquence de courbes reliées entre elles pour former une courbe plus grande. La fonction spline est spécifiée par un tableau de points et un paramètre de tension. Une spline cardinale traverse sans heurts de chaque point dans le tableau ; Il existe des angles aigus et aucune modification soudain dans la précision de la courbe. L’illustration suivante montre un ensemble de points et une spline cardinale qui passe par chaque point dans le jeu.  
  
 ![Spline cardinale](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art09.gif "Aboutgdip02_art09")  
  
## <a name="physical-and-mathematical-splines"></a>Splines physiques et mathématiques  
 Une spline physique est un élément dynamique de bois ou d’autres documents flexibles. Avant l’arrivée des splines mathématiques, concepteurs utilisés splines physiques pour dessiner des courbes. Un concepteur voulez-vous placer la spline sur une feuille de papier et ancrez-la à un ensemble donné de points. Le concepteur peut ensuite créer une courbe en dessinant le long de la fonction spline avec un stylet ou un crayon. Un ensemble donné de points peut produire des courbes, en fonction des propriétés de la spline physique différentes. Par exemple, une courbe avec une forte résistance à pliage produirait une courbe autre qu’une spline extrêmement flexible.  
  
 Les formules de splines mathématiques sont basées sur les propriétés de baguettes flexibles, par conséquent, les courbes produites par des splines mathématiques sont similaires aux courbes générés une fois par splines physiques. Comme splines physiques de la tension différents produira différentes courbes via un ensemble donné de points, des splines mathématiques avec différentes valeurs pour le paramètre tension produira différentes courbes via un ensemble donné de points. L’illustration suivante montre quatre splines cardinales passant par le même ensemble de points. La tension est indiquée pour chaque spline. La valeur 0 correspond à une tension physique infinie qui force la courbe à prendre le plus court (ligne droite) entre les points. La valeur 1 correspond à aucune tension physique, ce qui permet la spline à prendre le chemin d’accès de courbure minimum. Avec les valeurs de tension supérieures à 1, la courbe se comporte comme un ressort, envoyé à prendre le chemin le plus long.  
  
 ![Splines cardinales](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art10.gif "Aboutgdip02_art10")  
  
 Les quatre splines de l’illustration précédente partagent la même ligne de tangente au point de départ. La tangente est la ligne dessinée à partir du point de départ au point suivant le long de la courbe. De même, la tangente partagée sur le point de fin est la ligne dessinée à partir du point de fin pour le point précédent sur la courbe.  
  
 Pour dessiner une spline cardinale, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> (classe), un <xref:System.Drawing.Pen>et un tableau de <xref:System.Drawing.Point> objets de l’instance de la <xref:System.Drawing.Graphics> classe fournit le <xref:System.Drawing.Graphics.DrawCurve%2A> (méthode), qui dessine la spline, et le <xref:System.Drawing.Pen> stocke les attributs de la fonction spline, telles que la largeur de ligne et la couleur. Le tableau de <xref:System.Drawing.Point> objets stocke les points de la courbe doit passer. L’exemple de code suivant montre comment dessiner une spline cardinale qui passe par les points dans `myPointArray`. Le troisième paramètre est la tension.  
  
 [!code-csharp[LinesCurvesAndShapes#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#31)]
 [!code-vb[LinesCurvesAndShapes#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#31)]  
  
## <a name="see-also"></a>Voir aussi
- [Lignes, courbes et formes](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)
- [Génération et dessin de courbes](../../../../docs/framework/winforms/advanced/constructing-and-drawing-curves.md)
