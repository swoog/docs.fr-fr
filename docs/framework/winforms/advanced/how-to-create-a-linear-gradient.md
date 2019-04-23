---
title: 'Procédure : créer un pinceau dégradé linéaire'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- linear gradients [Windows Forms], creating
- gradients [Windows Forms], creating linear
- colors [Windows Forms], creating linear gradients
- gradients
ms.assetid: 6c88e1cc-1217-4399-ac12-cb37592b9f01
ms.openlocfilehash: 540b6d422be5d5c0898f019592a755258145d14d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59125019"
---
# <a name="how-to-create-a-linear-gradient"></a>Procédure : créer un pinceau dégradé linéaire
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] Fournit des dégradés linéaires horizontales, verticales et diagonales. Par défaut, la couleur d’un dégradé linéaire Modifie uniformément. Toutefois, vous pouvez personnaliser un dégradé linéaire de sorte que la couleur change de façon non uniforme.  
  
 L’exemple suivant remplit une ligne, une ellipse et un rectangle avec un pinceau de dégradé linéaire horizontal.  
  
 Le <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructeur reçoit quatre arguments : deux points et deux couleurs. Le premier point (0, 10) est associé à la première couleur (rouge), et le deuxième point (200, 10) est associé à la deuxième couleur (bleu). Comme vous pouvez l’imaginer, la ligne dessinée de (0, 10) à (200, 10) passe progressivement du rouge au bleu.  
  
 Les 10 s dans les points (50, 10) et (200, 10) ne sont pas importants. L’important est que les deux points ont la même coordonnée deuxième, la ligne qui relie les est horizontale. L’ellipse et rectangle également changer progressivement du rouge au bleu puisque la coordonnée horizontale va de 0 à 200.  
  
 L’illustration suivante montre la ligne, l’ellipse et le rectangle. Notez que le dégradé de couleur se répète à mesure que la coordonnée horizontale augmente au-delà de 200.  
  
 ![Dégradé linéaire](./media/cslineargradient1.png "cslineargradient1")  
  
### <a name="to-use-horizontal-linear-gradients"></a>Pour utiliser des dégradés linéaires horizontales  
  
-   Transmettre l’opaque rouge et le bleu opaque en tant que l’argument troisième et quatrième, respectivement.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#21)]
     [!code-vb[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#21)]  
  
 Dans l’exemple précédent, les composants de couleur changent linéairement lorsque vous passez de la coordonnée horizontale de 0 à une coordonnée horizontale de 200. Par exemple, un point dont la première coordonnée se trouve à mi-chemin entre 0 et 200 aura un composant bleu qui se trouve à mi-chemin entre 0 et 255.  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] vous permet d’ajuster la façon dont une couleur varie d’un bord d’un dégradé à l’autre. Supposons que vous souhaitez créer un pinceau de dégradé qui passe du noir au rouge conformément au tableau suivant.  
  
|Coordonnée horizontale|Composants RVB|  
|---------------------------|--------------------|  
|0|(0, 0, 0)|  
|40|(128, 0, 0)|  
|200|(255, 0, 0)|  
  
 Notez que le composant rouge est à moitié intensité lorsque la coordonnée horizontale est seulement 20 pour cent de la façon de 0 à 200.  
  
 L’exemple suivant définit la <xref:System.Drawing.Drawing2D.LinearGradientBrush.Blend%2A> propriété d’un <xref:System.Drawing.Drawing2D.LinearGradientBrush> objet à associer trois intensité relative à trois positions relatives. Comme dans le tableau précédent, une intensité relative de 0,5 est associée à une position relative de 0,2. Le code remplit une ellipse et un rectangle avec le pinceau de dégradé.  
  
 L’illustration suivante montre l’ellipse qui en résulte et un rectangle.  
  
 ![Dégradé linéaire](./media/cslineargradient2.png "cslineargradient2")  
  
### <a name="to-customize-linear-gradients"></a>Pour personnaliser des dégradés linéaires  
  
-   Transmettre la rouge à noir et opaque opaque en tant que l’argument troisième et quatrième, respectivement.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#22)]
     [!code-vb[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#22)]  
  
 Les dégradés dans les exemples précédents ont été horizontales ; Autrement dit, la couleur passe progressivement à mesure que vous déplacez le long de n’importe quelle ligne horizontale. Vous pouvez également définir des dégradés verticaux et en diagonale.  
  
 L’exemple suivant passe les points (0, 0) et (200, 100) à un <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructeur. Associé à la couleur bleue (0, 0), et est associée à la couleur verte (200, 100). Le pinceau de dégradé linéaire remplit une ligne (largeur du stylet 10) et une ellipse.  
  
 L’illustration suivante montre la ligne et l’ellipse. Notez que la couleur de l’ellipse change progressivement à mesure que vous déplacez le long d’une ligne qui est parallèle à la ligne passant par (0, 0) et (200, 100).  
  
 ![Dégradé linéaire](./media/cslineargradient3.png "cslineargradient3")  
  
### <a name="to-create-diagonal-linear-gradients"></a>Pour créer des dégradés linéaires en diagonale  
  
-   Transmettre l’opaque bleu et le vert opaque en tant que l’argument troisième et quatrième, respectivement.  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#23)]
     [!code-vb[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#23)]  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d'un pinceau à dégradé pour remplir des formes](using-a-gradient-brush-to-fill-shapes.md)
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
