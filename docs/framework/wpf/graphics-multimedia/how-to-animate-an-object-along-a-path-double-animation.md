---
title: 'Procédure : Animer un objet sur un tracé (animation double)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (double animation)
- double animation [WPF]
ms.assetid: 5a3c4a99-f303-42ad-a52a-e4794bb1798e
ms.openlocfilehash: a57b21e3f05f90e756c46c167bb419b5bc9068f4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600409"
---
# <a name="how-to-animate-an-object-along-a-path-double-animation"></a>Procédure : Animer un objet sur un tracé (animation double)
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> classe pour déplacer un objet sur un tracé défini par un <xref:System.Windows.Media.PathGeometry>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise deux <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objets pour déplacer un rectangle sur un tracé géométrique :  
  
-   La première <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime le <xref:System.Windows.Media.TranslateTransform.X%2A> de la <xref:System.Windows.Media.TranslateTransform> appliqué au rectangle. Le rectangle se déplace alors horizontalement sur le tracé.  
  
-   La seconde <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime le <xref:System.Windows.Media.TranslateTransform.Y%2A> de la <xref:System.Windows.Media.TranslateTransform> appliqué au rectangle. Le rectangle se déplace alors verticalement sur le tracé.  
  
 [!code-xaml[PathAnimationGallery_snippet#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/doubleanimationusingpathexample.xaml#doubleanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/DoubleAnimationUsingPathExample.cs#doubleanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#DoubleAnimationUsingPathWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/DoubleAnimationUsingPathExample.vb#doubleanimationusingpathwholepage)]  
  
 Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).  
  
 Une autre façon de déplacer un objet à l’aide d’un tracé géométrique consiste à utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> objet. Pour obtenir un exemple, consultez [animer un objet sur un tracé (Animation de matrice)](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-an-object-along-a-path-matrix-animation.md).  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Guides pratiques relatifs aux animations de tracés](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)
