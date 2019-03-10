---
title: 'Procédure : Utiliser une matrice de couleurs pour définir des valeurs Alpha dans des Images'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], using color matrices for semi-transparent
- transparency [Windows Forms], color matrices
- matrices [Windows Forms], alpha values
- bitmaps [Windows Forms], using color matrices for semi-transparent
ms.assetid: a27121e6-f7e9-4c09-84e2-f05aa9d2a1bb
ms.openlocfilehash: 9e102f51d00953d05ed1d217a345e32178676ffe
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716332"
---
# <a name="how-to-use-a-color-matrix-to-set-alpha-values-in-images"></a>Procédure : Utiliser une matrice de couleurs pour définir des valeurs Alpha dans des Images
Le <xref:System.Drawing.Bitmap> classe (qui hérite de la <xref:System.Drawing.Image> classe) et le <xref:System.Drawing.Imaging.ImageAttributes> classe fournit des fonctionnalités pour obtenir et définir des valeurs en pixels. Vous pouvez utiliser la <xref:System.Drawing.Imaging.ImageAttributes> classe pour modifier la valeur alpha de valeurs pour l’intégralité d’une image, ou vous pouvez appeler la <xref:System.Drawing.Bitmap.SetPixel%2A> méthode de la <xref:System.Drawing.Bitmap> classe pour modifier les valeurs de pixel individuelles.  
  
## <a name="example"></a>Exemple  
 Le <xref:System.Drawing.Imaging.ImageAttributes> classe comporte plusieurs propriétés que vous pouvez utiliser pour modifier les images pendant le rendu. Dans l’exemple suivant, un <xref:System.Drawing.Imaging.ImageAttributes> objet est utilisé pour définir toutes les valeurs alphabétiques à 80 % de leur nature. Pour cela, en initialisant une matrice de couleurs et en définissant la valeur alpha de mise à l’échelle de la valeur de la matrice à 0,8. L’adresse de la matrice des couleurs est passé à la <xref:System.Drawing.Imaging.ImageAttributes.SetColorMatrix%2A> méthode de la <xref:System.Drawing.Imaging.ImageAttributes> objet et le <xref:System.Drawing.Imaging.ImageAttributes> objet est passé à la <xref:System.Drawing.Graphics.DrawString%2A> méthode de la <xref:System.Drawing.Graphics> objet.  
  
 Pendant le rendu, les valeurs alphabétiques dans la bitmap sont converties à 80 % de leur nature. Cela entraîne une image qui est fusionnée avec l’arrière-plan. Comme le montre l’illustration suivante, l’image bitmap semble transparente ; Vous pouvez voir la ligne noire unie par son intermédiaire.  
  
 ![Fusion alpha utilisant une matrice](./media/image2.png "image2")  
  
 Où l’image est au-dessus de la partie blanche de l’arrière-plan, l’image a été fusionnée avec la couleur blanche. L’image où l’image dépasse la ligne noire, est fusionnée avec la couleur noire.  
  
 [!code-csharp[System.Drawing.AlphaBlending#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.AlphaBlending#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Fusion alpha de lignes et de remplissages](alpha-blending-lines-and-fills.md)
