---
title: 'Procédure : créer un dégradé de tracé'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- path gradients [Windows Forms], creating
- gradients [Windows Forms], creating path
- graphics paths [Windows Forms], creating gradient
ms.assetid: 1948e834-e104-481c-b71d-d8aa9e4d106e
ms.openlocfilehash: 31a8c68f382f81da2acac363bba6c8822e535770
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59186093"
---
# <a name="how-to-create-a-path-gradient"></a>Procédure : créer un dégradé de tracé
Le <xref:System.Drawing.Drawing2D.PathGradientBrush> classe vous permet de personnaliser la façon dont vous remplissez une forme avec des couleurs progressifs. Par exemple, vous pouvez spécifier une couleur pour le centre d’un chemin d’accès et un autre pour la limite d’un chemin d’accès. Vous pouvez également spécifier des couleurs distinctes pour chacun des points le long de la limite d’un chemin d’accès.  
  
> [!NOTE]
>  Dans [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], un chemin d’accès est une séquence de lignes et de courbes gérée par un <xref:System.Drawing.Drawing2D.GraphicsPath> objet. Pour plus d’informations sur [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] chemins d’accès, consultez [tracés graphiques dans GDI +](graphics-paths-in-gdi.md) et [génération et dessin de tracés](constructing-and-drawing-paths.md).  
  
### <a name="to-fill-an-ellipse-with-a-path-gradient"></a>Pour remplir une ellipse avec un dégradé de tracé  
  
-   L’exemple suivant remplit une ellipse avec un pinceau de dégradé de chemin d’accès. La couleur centrale est définie sur le bleu et la couleur de la limite est définie sur « cyan ». L’illustration suivante montre l’ellipse remplie.  
  
     ![Tracé en dégradé remplit une ellipse.](./media/how-to-create-a-path-gradient/gradient-path-filled-ellipse.png)  
  
     Par défaut, un pinceau de dégradé de chemin d’accès ne s’étend pas au-delà de la limite du chemin d’accès. Si vous utilisez le pinceau à dégradé pour remplir une illustration qui s’étend au-delà de la limite du chemin d’accès, il se peut que la zone de l’écran en dehors du tracé ne sera pas remplie.  
  
     L’illustration suivante montre que se passe-t-il si vous modifiez le <xref:System.Drawing.Graphics.FillEllipse%2A> appeler dans le code suivant à `e.Graphics.FillRectangle(pthGrBrush, 0, 10, 200, 40)`:  
  
     ![Tracé en dégradé étendu au-delà des limites du chemin d’accès.](./media/how-to-create-a-path-gradient/gradient-path-extended-beyond-boundary.png)  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#11)]
     [!code-vb[System.Drawing.UsingaGradientBrush#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#11)]  
  
     L’exemple de code précédent est conçu pour une utilisation avec Windows Forms et nécessite le <xref:System.Windows.Forms.PaintEventArgs> e, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
### <a name="to-specify-points-on-the-boundary"></a>Pour spécifier des points sur la limite  
  
-   L’exemple suivant construit un pinceau de dégradé de chemin d’accès à partir d’un chemin d’accès en étoile. Le code définit le <xref:System.Drawing.Drawing2D.PathGradientBrush.CenterColor%2A> propriété, qui définit la couleur au centre de gravité de l’étoile rouge. Le code affecte ensuite la <xref:System.Drawing.Drawing2D.PathGradientBrush.SurroundColors%2A> propriété pour spécifier différentes couleurs (stockées dans le `colors` tableau) des points dans le `points` tableau. La dernière instruction du code remplit le chemin d’accès en étoile avec le pinceau de dégradé de chemin d’accès.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#12)]
     [!code-vb[System.Drawing.UsingaGradientBrush#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#12)]  
  
-   L’exemple suivant dessine un dégradé de tracé sans un <xref:System.Drawing.Drawing2D.GraphicsPath> objet dans le code. Le particulier <xref:System.Drawing.Drawing2D.PathGradientBrush.%23ctor%2A> constructeur dans l’exemple reçoit un tableau de points, mais ne nécessite pas un <xref:System.Drawing.Drawing2D.GraphicsPath> objet. Notez également que le <xref:System.Drawing.Drawing2D.PathGradientBrush> est utilisé pour remplir un rectangle, pas un chemin d’accès. Le rectangle est supérieur à la trajectoire fermée utilisé pour définir la brosse, le rectangle n’est pas dessiné par le pinceau. L’illustration suivante montre le rectangle (ligne en pointillés) et la partie du rectangle peint par le pinceau de dégradé de chemin d’accès : 
  
     ![Partie dégradée peinte par le pinceau de dégradé de chemin d’accès.](./media/how-to-create-a-path-gradient/gradient-painted-path-gradient-brush.png)  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#13)]
     [!code-vb[System.Drawing.UsingaGradientBrush#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#13)]  
  
### <a name="to-customize-a-path-gradient"></a>Pour personnaliser un dégradé de tracé  
  
-   Pour personnaliser un pinceau de dégradé de chemin d’accès consiste à définir son <xref:System.Drawing.Drawing2D.PathGradientBrush.FocusScales%2A> propriété. Cette propriété spécifie un chemin d’accès interne qui se trouve dans le chemin d’accès principal. La couleur centrale s’affiche partout à l’intérieur de ce chemin d’accès interne et non uniquement au point central.  
  
     L’exemple suivant crée un pinceau de dégradé de chemin d’accès basé sur un chemin d’accès elliptique. Le code définit la couleur de contour bleu, définit la couleur centrale sur « cyan » et utilise ensuite le pinceau à dégradé pour remplir le tracé elliptique.  
  
     Ensuite, le code définit les échelles de focus du pinceau de dégradé de chemin d’accès. L’échelle de focus x est définie à 0.3, et l’échelle de focus y est définie sur 0,8. Le code appelle la <xref:System.Drawing.Graphics.TranslateTransform%2A> méthode d’un <xref:System.Drawing.Graphics> objet afin que le prochain appel à <xref:System.Drawing.Graphics.FillPath%2A> remplit une ellipse qui se trouve à droite de la première ellipse.  
  
     Pour voir l’effet des échelles de focus, imaginez une petite ellipse qui partage son centre de l’ellipse principale. La petite ellipse (interne) est l’ellipse principale évoluer horizontalement (autour de son centre) par un facteur de 0.3 et verticalement par un facteur de 0,8. Lorsque vous déplacez du contour de l’ellipse externe à la limite de l’ellipse interne, la couleur passe progressivement du bleu sur « cyan ». Lorsque vous déplacez du contour de l’ellipse interne au centre partagé, le reste de couleur cyan.  
  
     L'illustration suivante montre la sortie du code suivant. L’ellipse sur la gauche est aqua uniquement au point central. Les points de suspension à droite est aqua partout dans le chemin d’accès interne.  
  
 ![Effet de dégradé d’échelles de focus](./media/how-to-create-a-path-gradient/focus-scales-aqua-inner-outer-ellipse.png)  
  
 [!code-csharp[System.Drawing.UsingaGradientBrush#14](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.UsingaGradientBrush#14](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#14)]  
  
### <a name="to-customize-with-interpolation"></a>Pour personnaliser avec interpolation  
  
-   Une autre façon de personnaliser un pinceau de dégradé de chemin d’accès consiste à spécifier un tableau de couleurs d’interpolation et un tableau de positions d’interpolation.  
  
     L’exemple suivant crée un pinceau de dégradé de chemin d’accès basé sur un triangle. Le code définit le <xref:System.Drawing.Drawing2D.PathGradientBrush.InterpolationColors%2A> propriété du pinceau de dégradé de chemin d’accès pour spécifier un tableau de couleurs d’interpolation (vert foncé, cyan, bleu) et un tableau de positions d’interpolation (0, 0,25, 1). Lorsque vous déplacez du contour du triangle vers le point central, la couleur passe progressivement du vert foncé au cyan, puis du cyan au bleu. Le passage du vert foncé au cyan se produit à 25 pour cent de la distance du vert foncé au bleu.  
  
     L’illustration suivante montre le triangle rempli avec le pinceau de dégradé de chemin d’accès personnalisé.  
  
     ![Triangle rempli avec un pinceau de dégradé de chemin d’accès personnalisé.](./media/how-to-create-a-path-gradient/gradient-brush-filled-triangle.png)  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#15](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#15)]
     [!code-vb[System.Drawing.UsingaGradientBrush#15](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#15)]  
  
### <a name="to-set-the-center-point"></a>Pour définir le point central  
  
-   Par défaut, le point central d’un pinceau de dégradé de chemin d’accès est au centre de gravité du chemin d’accès utilisé pour construire le pinceau. Vous pouvez modifier l’emplacement du point central en définissant le <xref:System.Drawing.Drawing2D.PathGradientBrush.CenterPoint%2A> propriété de la <xref:System.Drawing.Drawing2D.PathGradientBrush> classe.  
  
     L’exemple suivant crée un pinceau de dégradé de chemin d’accès basé sur une ellipse. Le centre de l’ellipse est à (70, 35), mais le point central du pinceau de dégradé de chemin d’accès est défini sur (120, 40).  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#16](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#16)]
     [!code-vb[System.Drawing.UsingaGradientBrush#16](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#16)]  
  
     L’illustration suivante montre l’ellipse remplie et le point central du pinceau de dégradé de chemin d’accès :  
  
     ![Tracé en dégradé avec rempli ellipse et le point central.](./media/how-to-create-a-path-gradient/gradient-path-filled-ellipse-center-point.png)  
  
-   Vous pouvez définir le point central d’un pinceau de dégradé de chemin d’accès à un emplacement en dehors du tracé qui a été utilisé pour construire le pinceau. L’exemple suivant remplace l’appel pour définir le <xref:System.Drawing.Drawing2D.PathGradientBrush.CenterPoint%2A> propriété dans le code précédent.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#17](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#17)]
     [!code-vb[System.Drawing.UsingaGradientBrush#17](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#17)]  
  
     L’illustration suivante montre la sortie avec cette modification :  
  
     ![Tracé en dégradé avec point central en dehors du tracé.](./media/how-to-create-a-path-gradient/gradient-path-center-point-outside.png)  
  
     Dans l’illustration précédente, les points à l’extrême droite de l’ellipse ne sont pas bleu pur (même s’ils sont très proches). Les couleurs de dégradé sont positionnés comme si le remplissage atteint le point (145, 35) où la couleur serait un bleu pur (0, 0, 255). Mais le remplissage n’atteint jamais (145, 35), car un pinceau à dégradé peint uniquement à l’intérieur de son chemin d’accès.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Les exemples précédents sont conçus pour une utilisation avec Windows Forms, et ils nécessitent <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d'un pinceau à dégradé pour remplir des formes](using-a-gradient-brush-to-fill-shapes.md)
