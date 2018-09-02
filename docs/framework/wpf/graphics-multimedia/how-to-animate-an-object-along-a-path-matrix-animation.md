---
title: 'Comment : animer un objet sur un tracé (animation de matrice)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (matrix animation)
- matrix animation [WPF]
ms.assetid: 7000e697-1414-468c-b915-cf66062fc49e
ms.openlocfilehash: f88133a5e927a1a1f59b1aa02826d140c107d002
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43469984"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation"></a>Comment : animer un objet sur un tracé (animation de matrice)
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> classe pour animer un objet sur un tracé défini par un <xref:System.Windows.Media.PathGeometry>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant anime un objet sur un tracé de la manière suivante :  
  
-   Applique un <xref:System.Windows.Media.MatrixTransform> à l’objet afin de le déplacer.  
  
-   Définit le chemin d’accès en utilisant un <xref:System.Windows.Media.PathGeometry>.  
  
-   Crée un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> et l’utilise pour animer la <xref:System.Windows.Media.Matrix> propriété de la <xref:System.Windows.Media.MatrixTransform>. Le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> prend le <xref:System.Windows.Media.PathGeometry> et l’utilise pour générer <xref:System.Windows.Media.Matrix> valeurs.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexample.xaml#matrixanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExample.cs#matrixanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExample.vb#matrixanimationusingpathwholepage)]  
  
 Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028). Pour plus d’informations sur les tracés géométriques, consultez le [vue d’ensemble de Geometry](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028)  
 [Guides pratiques relatifs aux animations de tracés](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
