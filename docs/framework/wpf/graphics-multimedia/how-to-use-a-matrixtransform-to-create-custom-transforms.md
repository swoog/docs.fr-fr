---
title: 'Procédure : Utiliser la classe MatrixTransform pour créer des transformations personnalisées'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], custom Transforms
ms.assetid: 919381ca-989f-47cf-86b4-1094060236e4
ms.openlocfilehash: aeccb961db539d4cc6dea75fb487fba06e59d6de
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61769258"
---
# <a name="how-to-use-a-matrixtransform-to-create-custom-transforms"></a>Procédure : Utiliser la classe MatrixTransform pour créer des transformations personnalisées
Cet exemple montre comment utiliser un <xref:System.Windows.Media.MatrixTransform> pour translater (déplacer) la position, étirer et incliner d’un <xref:System.Windows.Controls.Button>.  
  
> [!NOTE]
>  Utilisez le <xref:System.Windows.Media.MatrixTransform> classe pour créer des transformations personnalisées qui ne sont pas fournies par le <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, ou <xref:System.Windows.Media.TranslateTransform> classes.  
  
## <a name="example"></a>Exemple  
 [!code-xaml[Transforms_snip#MatrixTransform](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MatrixTransformExample.xaml#matrixtransform)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Media.MatrixTransform>
- <xref:System.Windows.Media.Transform>
- [Vue d’ensemble des transformations](transforms-overview.md)
- [Rubriques de guide pratique](transformations-how-to-topics.md)
- [Vue d’ensemble des formes et dessins de base dans WPF](shapes-and-basic-drawing-in-wpf-overview.md)
