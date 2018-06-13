---
title: Utilisation de transformations pour mettre à l'échelle des couleurs
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- transformations [Windows Forms], for scaling colors
- colors [Windows Forms], scaling
ms.assetid: df23c887-7fd6-4b15-ad94-e30b5bd4b849
ms.openlocfilehash: 6cfe90cef42086672990c45c99961db3d29c3ff3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33525965"
---
# <a name="using-transformations-to-scale-colors"></a>Utilisation de transformations pour mettre à l'échelle des couleurs
Une transformation d’échelle multiplie une ou plusieurs des quatre composantes de couleur par un nombre. Les entrées de matrice de couleurs qui représentent la mise à l’échelle sont présentées dans le tableau suivant.  
  
|Composant à l’échelle|Entrée de la matrice|  
|----------------------------|------------------|  
|Rouge|[0][0]|  
|Vert|[1][1]|  
|Bleu|[2][2]|  
|Alpha|[3][3]|  
  
## <a name="scaling-one-color"></a>Mise à l’échelle d’une couleur  
 L’exemple suivant construit une <xref:System.Drawing.Image> objet à partir du fichier ColorBars2.bmp. Ensuite, le code ajuste la composante bleue de chaque pixel dans l’image selon un facteur de 2. L’image d’origine est dessinée en même temps que l’image transformée.  
  
 [!code-csharp[System.Drawing.RecoloringImages#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.RecoloringImages#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#41)]  
  
 L’illustration suivante montre l’image d’origine sur la gauche et l’image à l’échelle sur la droite.  
  
 ![Mettre à l’échelle de couleurs](../../../../docs/framework/winforms/advanced/media/colortrans3.png "colortrans3")  
  
 Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la mise à l’échelle bleu. Notez que la composante bleue de la quatrième barre de couleurs est passée de 0,8 à 0,6. C’est parce que [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] conserve uniquement la partie fractionnaire du résultat. Par exemple, (2)(0.8) = 1,6 et la partie fractionnaire de 1,6 est 0,6. En conservant uniquement la partie fractionnaire garantit que le résultat est toujours dans l’intervalle [0, 1].  
  
|D'origine|Mise à l’échelle|  
|--------------|------------|  
|(0.4, 0.4, 0.4, 1)|(0.4, 0.4, 0.8, 1)|  
|(0.4, 0.2, 0.2, 1)|(0.4, 0.2, 0.4, 1)|  
|(0.2, 0.4, 0.2, 1)|(0.2, 0.4, 0.4, 1)|  
|(0.4, 0.4, 0.8, 1)|(0.4, 0.4, 0.6, 1)|  
  
## <a name="scaling-multiple-colors"></a>Mise à l’échelle de plusieurs couleurs  
 L’exemple suivant construit une <xref:System.Drawing.Image> objet à partir du fichier ColorBars2.bmp. Ensuite, le code ajuste les composants rouges, verts et bleus de chaque pixel de l’image. Les composants rouges sont réduites de 25 pour cent, les composants verts à l’échelle vers le bas 35 % et les composants bleus sont réduites de 50 pour cent.  
  
 [!code-csharp[System.Drawing.RecoloringImages#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#42)]
 [!code-vb[System.Drawing.RecoloringImages#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#42)]  
  
 L’illustration suivante montre l’image d’origine sur la gauche et l’image à l’échelle sur la droite.  
  
 ![Mettre à l’échelle de couleurs](../../../../docs/framework/winforms/advanced/media/colortrans4.png "colortrans4")  
  
 Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après le redimensionnement rouge, vert et bleu.  
  
|D'origine|Mise à l’échelle|  
|--------------|------------|  
|(0.6, 0.6, 0.6, 1)|(0.45, 0.39, 0.3, 1)|  
|(0, 1, 1, 1)|(0, 0.65, 0.5, 1)|  
|(1, 1, 0, 1)|(0.75, 0.65, 0, 1)|  
|(1, 0, 1, 1)|(0.75, 0, 0.5, 1)|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Drawing.Imaging.ColorMatrix>  
 <xref:System.Drawing.Imaging.ImageAttributes>  
 [Graphiques et dessins dans Windows Forms](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)  
 [Recoloriage des images](../../../../docs/framework/winforms/advanced/recoloring-images.md)
