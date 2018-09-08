---
title: "Comment : faire pivoter un objet à l'aide d'un tracé géométrique (animation de matrice)"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- geometric paths [WPF], rotating objects by
- rotating objects by geometric paths [WPF]
- matrix animation [WPF]
ms.assetid: 877dc9aa-6bdc-4beb-8772-3efaec32c0f0
ms.openlocfilehash: 3a35f6dda05cfe65811de16d76b288c8fbd618a7
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44133608"
---
# <a name="how-to-rotate-an-object-by-using-a-geometric-path-matrix-animation"></a>Comment : faire pivoter un objet à l'aide d'un tracé géométrique (animation de matrice)
Cet exemple montre comment utiliser un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> et un <xref:System.Windows.Media.MatrixTransform> à faire tourner (pivoter) un objet le long d’un tracé géométrique défini par un <xref:System.Windows.Media.PathGeometry> objet.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> objet à animer le <xref:System.Windows.Media.MatrixTransform.Matrix%2A> propriété d’un <xref:System.Windows.Media.MatrixTransform>. Le <xref:System.Windows.Media.MatrixTransform> est appliqué à un bouton et oblige ce dernier à déplacer sur un tracé courbé. Étant donné que le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> propriété est définie sur `true`, le rectangle pivote le long de la tangente du chemin d’accès.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathdoesrotatewithtangentexample.xaml#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathDoesRotateWithTangentExample.cs#matrixanimationusingpathdoesrotatewithtangentwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathDoesRotateWithTangentWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathDoesRotateWithTangentExample.vb#matrixanimationusingpathdoesrotatewithtangentwholepage)]  
  
 Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028).  
  
 La version du code de l’exemple précédent utilisé un <xref:System.Windows.Media.Animation.Storyboard> pour animer la <xref:System.Windows.Media.EllipseGeometry>, bien qu’une seule animation ait été appliquée. Appliquer une seule animation à une propriété dans le code d’un moyen plus simple consiste à utiliser le <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> (méthode). Si vous voulez voir un exemple, consultez l’article [Comment : animer une propriété sans utiliser de storyboard](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-without-using-a-storyboard.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble de l’animation](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [Guides pratiques relatifs aux animations de tracés](../../../../docs/framework/wpf/graphics-multimedia/path-animation-how-to-topics.md)  
 [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028)
