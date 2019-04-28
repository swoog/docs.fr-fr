---
title: 'Procédure : Créer une scène 3D'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- scenes [WPF], 3-D
- 3-D scenes
ms.assetid: adb4a598-71a2-4dd5-b677-ea3fc11b78b2
ms.openlocfilehash: 8e176cb437055787da86d56770dd71323134fa33
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61910180"
---
# <a name="how-to-create-a-3-d-scene"></a>Procédure : Créer une scène 3D
Cet exemple montre comment créer un objet 3D qui ressemble à une feuille de papier ayant subi une rotation. Un <xref:System.Windows.Controls.Viewport3D> , ainsi que les composants suivants sont utilisés pour créer cette scène 3D simple :  
  
- Un appareil photo est créé en utilisant un <xref:System.Windows.Media.Media3D.PerspectiveCamera>. L’appareil photo spécifie quelle partie de la scène 3D est visible.  
  
- Un maillage est créé pour spécifier la forme d’un objet 3D (feuille de papier) à l’aide de la <xref:System.Windows.Media.Media3D.GeometryModel3D.Geometry%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D>.  
  
- Un matériau est spécifié doit être affiché sur la surface de l’objet (dégradé linéaire dans cet exemple) en utilisant le <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> propriété du <xref:System.Windows.Media.Media3D.GeometryModel3D>.  
  
- Une lumière est créée pour briller sur l’objet en utilisant <xref:System.Windows.Media.Media3D.DirectionalLight>.  
  
## <a name="example"></a>Exemple  
 Le code ci-dessous montre comment créer une scène 3D dans XAML.  
  
 [!code-xaml[3DGallery_snip#Basic3DShapeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/Basic3DShapeExample.xaml#basic3dshapeexamplewholepage)]  
  
## <a name="example"></a>Exemple  
 Le code ci-dessous montre comment créer la même scène 3D en code procédural.  
  
 [!code-csharp[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Basic3DShapeExample.cs#basic3dshapecodeexamplewholepage)]
 [!code-vb[3DGallery_procedural_snip#Basic3DShapeCodeExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/3DGallery_procedural_snip/visualbasic/basic3dshapeexample.vb#basic3dshapecodeexamplewholepage)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des graphiques 3D](3-d-graphics-overview.md)
