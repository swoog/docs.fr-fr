---
title: 'Procédure : Animer un objet sur un tracé (animation de matrice)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], objects along paths (matrix animation)
- matrix animation [WPF]
ms.assetid: 7000e697-1414-468c-b915-cf66062fc49e
ms.openlocfilehash: ab15126680b7d8c6936246a7dae2f67c7541233b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61651439"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation"></a>Procédure : Animer un objet sur un tracé (animation de matrice)
Cet exemple montre comment utiliser le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> classe pour animer un objet sur un tracé défini par un <xref:System.Windows.Media.PathGeometry>.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant anime un objet sur un tracé de la manière suivante :  
  
- Applique un <xref:System.Windows.Media.MatrixTransform> à l’objet afin de le déplacer.  
  
- Définit le chemin d’accès en utilisant un <xref:System.Windows.Media.PathGeometry>.  
  
- Crée un <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> et l’utilise pour animer la <xref:System.Windows.Media.Matrix> propriété de la <xref:System.Windows.Media.MatrixTransform>. Le <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> prend le <xref:System.Windows.Media.PathGeometry> et l’utilise pour générer <xref:System.Windows.Media.Matrix> valeurs.  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexample.xaml#matrixanimationusingpathwholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExample.cs#matrixanimationusingpathwholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExample.vb#matrixanimationusingpathwholepage)]  
  
 Pour obtenir un exemple complet, consultez [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028). Pour plus d’informations sur les tracés géométriques, consultez le [vue d’ensemble de Geometry](geometry-overview.md).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble de l’animation](animation-overview.md)
- [Animation de tracés, exemple](https://go.microsoft.com/fwlink/?LinkID=160028)
- [Guides pratiques relatifs aux animations de tracés](path-animation-how-to-topics.md)
