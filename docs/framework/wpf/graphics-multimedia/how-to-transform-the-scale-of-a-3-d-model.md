---
title: 'Procédure : Transformer l’échelle d’un modèle 3D'
ms.date: 03/30/2017
helpviewer_keywords:
- scaling [WPF], 3-D objects
- 3-D objects [WPF], scaling
ms.assetid: f3fdfe33-f7dc-44b0-84a5-e43b89947f35
ms.openlocfilehash: 6d668de08201d819ce9f8752bedf6c388a6bc718
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165079"
---
# <a name="how-to-transform-the-scale-of-a-3-d-model"></a>Procédure : Transformer l’échelle d’un modèle 3D
Cet exemple montre comment mettre à l’échelle un objet 3D. Pour mettre à l’échelle un objet 3D, vous devez utiliser un <xref:System.Windows.Media.Media3D.ScaleTransform3D>. Le <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A>, <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A>, et <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleZ%2A> propriétés redimensionnent l’élément selon le facteur que vous spécifiez. Par exemple, un <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleX%2A> valeur de 1,5 étire un objet à 150 % de sa largeur d’origine. A <xref:System.Windows.Media.Media3D.ScaleTransform3D.ScaleY%2A> la valeur 0,5 diminue la hauteur d’un objet de 50 %. Le code ci-dessous montre à l’aide un <xref:System.Windows.Media.Media3D.ScaleTransform3D> en tant que la transformation pour un <xref:System.Windows.Media.Media3D.GeometryModel3D>.  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexampleinline1)]  
  
## <a name="example"></a>Exemple  
 Le code suivant montre l’exemple complet.  
  
 [!code-xaml[3DGallery_snip#ScaleTransform3DExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ScaleTransform3DExample.xaml#scaletransform3dexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Animer des translations 3D](how-to-animate-3-d-translations.md)
- [Créer une scène 3D](how-to-create-a-3-d-scene.md)
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
