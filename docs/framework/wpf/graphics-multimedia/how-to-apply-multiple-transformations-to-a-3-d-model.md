---
title: 'Procédure : Appliquer plusieurs transformations à un modèle 3D'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 3-D models [WPF], applying multiple transformations to
ms.assetid: cb72245a-5560-4c96-9f58-593c66296992
ms.openlocfilehash: d18b9bc78e011796f9d9e6d535f3dc949bd5a0f8
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57352462"
---
# <a name="how-to-apply-multiple-transformations-to-a-3-d-model"></a>Procédure : Appliquer plusieurs transformations à un modèle 3D
Cet exemple montre comment utiliser un <xref:System.Windows.Media.Media3D.RotateTransform3D> et un <xref:System.Windows.Media.Media3D.ScaleTransform3D> pour faire pivoter et de modifier l’échelle d’un modèle 3D. Le code ci-dessous montre comment appliquer ces transformations à la <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> propriété d’un <xref:System.Windows.Media.Media3D.GeometryModel3D> dans XAML.  
  
 [!code-xaml[3DGallery_snip#Multiple3DTransformationsExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/MultipleTransformationsExample.xaml#multiple3dtransformationsexampleinline1)]  
  
 En code :  
  
 [!code-csharp[3DGallery_procedural_snip#Multiple3DTransformationsCodeExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/MultipleTransformationsExample.cs#multiple3dtransformationscodeexampleinline1)]
 [!code-vb[3DGallery_procedural_snip#Multiple3DTransformationsCodeExampleInline1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/multipletransformationsexample.vb#multiple3dtransformationscodeexampleinline1)]  
  
## <a name="example"></a>Exemple  
 Le code suivant montre l’exemple entier dans XAML.  
  
 [!code-xaml[3DGallery_snip#Multiple3DTransformationsExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/MultipleTransformationsExample.xaml#multiple3dtransformationsexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 Voici l’exemple complet dans le code.  
  
 [!code-csharp[3DGallery_procedural_snip#Multiple3DTransformationsCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/MultipleTransformationsExample.cs#multiple3dtransformationscodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#Multiple3DTransformationsCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/multipletransformationsexample.vb#multiple3dtransformationscodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Transformer l’échelle d’un modèle 3D](how-to-transform-the-scale-of-a-3-d-model.md)
