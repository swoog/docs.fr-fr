---
title: 'Procédure : disposer une forme en mosaïque avec une image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- texture brushes [Windows Forms], tiling images with
- images [Windows Forms], filling shapes with
- shapes [Windows Forms], tiling with images
- bitmaps [Windows Forms], filling shapes with
ms.assetid: 6d407891-6e5c-4495-a546-3da5604e9fb8
ms.openlocfilehash: ad7b8737a63028e533cadfa6db56b063eb943f22
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59221536"
---
# <a name="how-to-tile-a-shape-with-an-image"></a>Procédure : disposer une forme en mosaïque avec une image
Tout comme les vignettes peuvent être placés à côté des autres pour couvrir un étage, rectangulaires images peuvent être placés en regard de chacun des autres sur fill (mosaïque) une forme. Pour disposer en mosaïque à l’intérieur d’une forme, utilisez un pinceau de la texture. Lorsque vous construisez un <xref:System.Drawing.TextureBrush> de l’objet, un des arguments que vous passez au constructeur est un <xref:System.Drawing.Image> objet. Lorsque vous utilisez le pinceau de texture pour peindre l’intérieur d’une forme, la forme est remplie avec les copies répétées de cette image.  
  
 La propriété de mode de retour à la ligne de la <xref:System.Drawing.TextureBrush> objet détermine comment l’image est orienté comme il est répété dans une grille rectangulaire. Vous pouvez effectuer toutes les vignettes dans la grille ont la même orientation, ou vous pouvez rendre une image de retournement d’une position à l’autre. La rotation peut être horizontale, verticale ou les deux. Les exemples suivants illustrent une mosaïque avec différents types de rotation.  
  
### <a name="to-tile-an-image"></a>À la vignette d’une image  
  
-   Cet exemple utilise l’image 75 × 75 suivante à la vignette d’un rectangle 200 × 200.  
  
 ![Vignette 1](./media/tile1.gif "tile1")  
  
-   L’illustration suivante montre la façon dont le rectangle est affichée en mosaïque avec l’image. Notez que toutes les vignettes ont la même orientation ; Il n’existe aucun retournement.  
  
 ![Vignette 2](./media/tile2.gif "tile2")  
  
 [!code-csharp[System.Drawing.UsingABrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingABrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#31)]  
  
### <a name="to-flip-an-image-horizontally-while-tiling"></a>Pour faire pivoter une image horizontalement lors de la disposition en mosaïque  
  
-   Cet exemple utilise la même image 75 × 75 pour remplir un rectangle 200 × 200. Le mode habillage est défini pour retourner l’image horizontalement. L’illustration suivante montre la façon dont le rectangle est affichée en mosaïque avec l’image. Notez que lorsque vous déplacez à partir d’une vignette à l’autre dans une ligne donnée, l’image est retournée horizontalement.  
  
 ![Vignette 3](./media/tile3.gif "tile3")  
  
 [!code-csharp[System.Drawing.UsingABrush#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.UsingABrush#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#32)]  
  
### <a name="to-flip-an-image-vertically-while-tiling"></a>Pour faire pivoter une image verticalement lors de la disposition en mosaïque  
  
-   Cet exemple utilise la même image 75 × 75 pour remplir un rectangle 200 × 200. Le mode habillage est défini pour retourner l’image verticalement.  
  
     [!code-csharp[System.Drawing.UsingABrush#33](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#33)]
     [!code-vb[System.Drawing.UsingABrush#33](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#33)]  
  
### <a name="to-flip-an-image-horizontally-and-vertically-while-tiling"></a>Pour faire pivoter une image horizontalement et verticalement mosaïque  
  
-   Cet exemple utilise la même image 75 × 75 à la vignette d’un rectangle 200 × 200. Le mode habillage est défini pour retourner l’image horizontalement et verticalement. L’illustration suivante montre la façon dont le rectangle est affichée en mosaïque par l’image. Notez que lorsque vous déplacez à partir d’une vignette à l’autre dans une ligne donnée, l’image est retournée horizontalement, et lorsque vous passez d’une image à la suivante dans une colonne donnée, l’image est retournée verticalement.  
  
 ![Vignette 5](./media/tile5.gif "tile5")  
  
 [!code-csharp[System.Drawing.UsingABrush#34](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#34)]
 [!code-vb[System.Drawing.UsingABrush#34](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#34)]  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d'un pinceau pour remplir des formes](using-a-brush-to-fill-shapes.md)
