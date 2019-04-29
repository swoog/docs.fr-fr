---
title: 'Procédure : Faire pivoter un objet à l’aide d’un tracé géométrique'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
ms.assetid: cb31ca4d-f05a-4c6b-9a18-4b6faaf38d45
ms.openlocfilehash: 3e35169da7297ec62e0114ab21f4ba81c0a656ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651244"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path"></a>Procédure : Faire pivoter un objet à l’aide d’un tracé géométrique
Cet exemple montre comment faire tourner (pivoter) un objet sur un tracé géométrique défini par un <xref:System.Windows.Media.PathGeometry> objet.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise trois <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> objets pour déplacer un rectangle sur un tracé géométrique.  
  
- La première <xref:System.Windows.Media.Animation.DoubleAnimationUsingPath> anime un <xref:System.Windows.Media.RotateTransform> qui est appliqué au rectangle. L’animation génère des valeurs d’angle. Le rectangle tourne (pivote) ainsi sur les contours du tracé.  
  
- Les deux autres objets animent les <xref:System.Windows.Media.TranslateTransform.X%2A> et <xref:System.Windows.Media.TranslateTransform.Y%2A> valeurs d’un <xref:System.Windows.Media.TranslateTransform> qui est appliqué au rectangle. Le rectangle se déplace alors horizontalement et verticalement sur le tracé.  
  
 [!code-xaml[PathAnimationGallery_snippet#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/rotateanimationusingpathexample.xaml#rotateanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/RotateAnimationUsingPathExample.cs#rotateanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#RotateAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/RotateAnimationUsingPathExample.vb#rotateanimationusingpathwholepage)]  
  
 Une autre façon de faire pivoter un objet à l’aide d’un tracé géométrique consiste à utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> de l’objet et définissez son <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété `true`. Pour plus d’informations et un exemple, consultez [faire pivoter un objet à l’aide d’un tracé géométrique (Animation de matrice)](how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation.md).  
  
 Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’animation](animation-overview.md)
- [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028)
- [Guides pratiques relatifs aux animations de tracés](path-animation-how-to-topics.md)
