---
title: 'Procédure : Créer une scène 3D'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- scenes [WPF], 3-D
- 3-D scenes
ms.assetid: adb4a598-71a2-4dd5-b677-ea3fc11b78b2
ms.openlocfilehash: 8c9aec78bdda4f9f122b6dbefe0956ba649adf22
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57370746"
---
# <a name="how-to-create-a-3-d-scene"></a>Procédure : Créer une scène 3D
Cet exemple montre comment créer un objet 3D qui ressemble à une feuille de papier ayant subi une rotation. Un <xref:System.Windows.Controls.Viewport3D> , ainsi que les composants suivants sont utilisés pour créer cette scène 3D simple :  
  
-   Un appareil photo est créé en utilisant un <xref:System.Windows.Media.Media3D.PerspectiveCamera>. L’appareil photo spécifie quelle partie de la scène 3D est visible.  
  
-   Un maillage est créé pour spécifier la forme d’un objet 3D (feuille de papier) à l’aide de la <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D>.  
  
-   Un matériau est spécifié doit être affiché sur la surface de l’objet (dégradé linéaire dans cet exemple) en utilisant le <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D>.  
  
-   Une lumière est créée pour briller sur l’objet en utilisant <xref:System.Windows.Media.Media3D.DirectionalLight>.  
  
## <a name="example"></a>Exemple  
 Le code ci-dessous montre comment créer une scène 3D dans XAML.  
  
 [!code-xaml[3DGallery_snip#Basic3DShapeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/Basic3DShapeExample.xaml#basic3dshapeexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 Le code ci-dessous montre comment créer la même scène 3D en code procédural.  
  
 [!code-csharp[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Basic3DShapeExample.cs#basic3dshapecodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/basic3dshapeexample.vb#basic3dshapecodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
