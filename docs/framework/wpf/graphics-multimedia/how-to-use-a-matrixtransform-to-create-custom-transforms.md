---
title: 'Procédure : Utiliser la classe MatrixTransform pour créer des transformations personnalisées'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], custom Transforms
ms.assetid: 919381ca-989f-47cf-86b4-1094060236e4
ms.openlocfilehash: aeccb961db539d4cc6dea75fb487fba06e59d6de
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59182310"
---
# <a name="how-to-use-a-matrixtransform-to-create-custom-transforms"></a><span data-ttu-id="a6072-102">Procédure : Utiliser la classe MatrixTransform pour créer des transformations personnalisées</span><span class="sxs-lookup"><span data-stu-id="a6072-102">How to: Use a MatrixTransform to Create Custom Transforms</span></span>
<span data-ttu-id="a6072-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.MatrixTransform> pour translater (déplacer) la position, étirer et incliner d’un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="a6072-103">This example shows how to use a <xref:System.Windows.Media.MatrixTransform> to translate (move) the position, stretch, and skew of a <xref:System.Windows.Controls.Button>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a6072-104">Utilisez le <xref:System.Windows.Media.MatrixTransform> classe pour créer des transformations personnalisées qui ne sont pas fournies par le <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, ou <xref:System.Windows.Media.TranslateTransform> classes.</span><span class="sxs-lookup"><span data-stu-id="a6072-104">Use the <xref:System.Windows.Media.MatrixTransform> class to create custom transformations that are not provided by the <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, or <xref:System.Windows.Media.TranslateTransform> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a6072-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="a6072-105">Example</span></span>  
 [!code-xaml[Transforms_snip#MatrixTransform](~/samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MatrixTransformExample.xaml#matrixtransform)]  
  
## <a name="see-also"></a><span data-ttu-id="a6072-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6072-106">See also</span></span>

- <xref:System.Windows.Media.MatrixTransform>
- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="a6072-107">Vue d'ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="a6072-107">Transforms Overview</span></span>](transforms-overview.md)
- [<span data-ttu-id="a6072-108">Rubriques Comment</span><span class="sxs-lookup"><span data-stu-id="a6072-108">How-to Topics</span></span>](transformations-how-to-topics.md)
- [<span data-ttu-id="a6072-109">Vue d'ensemble des formes et dessins de base dans WPF</span><span class="sxs-lookup"><span data-stu-id="a6072-109">Shapes and Basic Drawing in WPF Overview</span></span>](shapes-and-basic-drawing-in-wpf-overview.md)
