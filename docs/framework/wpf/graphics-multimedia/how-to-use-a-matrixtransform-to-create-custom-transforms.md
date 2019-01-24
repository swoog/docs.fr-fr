---
title: 'Procédure : Utiliser un MatrixTransform pour créer des transformations personnalisées'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [WPF], custom Transforms
ms.assetid: 919381ca-989f-47cf-86b4-1094060236e4
ms.openlocfilehash: 3b5a6fbedd30c859dffadad00c8faab74fc0773b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54628797"
---
# <a name="how-to-use-a-matrixtransform-to-create-custom-transforms"></a><span data-ttu-id="2e706-102">Procédure : Utiliser un MatrixTransform pour créer des transformations personnalisées</span><span class="sxs-lookup"><span data-stu-id="2e706-102">How to: Use a MatrixTransform to Create Custom Transforms</span></span>
<span data-ttu-id="2e706-103">Cet exemple montre comment utiliser un <xref:System.Windows.Media.MatrixTransform> pour translater (déplacer) la position, étirer et incliner d’un <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="2e706-103">This example shows how to use a <xref:System.Windows.Media.MatrixTransform> to translate (move) the position, stretch, and skew of a <xref:System.Windows.Controls.Button>.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2e706-104">Utilisez le <xref:System.Windows.Media.MatrixTransform> classe pour créer des transformations personnalisées qui ne sont pas fournies par le <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, ou <xref:System.Windows.Media.TranslateTransform> classes.</span><span class="sxs-lookup"><span data-stu-id="2e706-104">Use the <xref:System.Windows.Media.MatrixTransform> class to create custom transformations that are not provided by the <xref:System.Windows.Media.RotateTransform>, <xref:System.Windows.Media.SkewTransform>, <xref:System.Windows.Media.ScaleTransform>, or <xref:System.Windows.Media.TranslateTransform> classes.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2e706-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="2e706-105">Example</span></span>  
 [!code-xaml[Transforms_snip#MatrixTransform](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/MatrixTransformExample.xaml#matrixtransform)]  
  
## <a name="see-also"></a><span data-ttu-id="2e706-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e706-106">See also</span></span>
- <xref:System.Windows.Media.MatrixTransform>
- <xref:System.Windows.Media.Transform>
- [<span data-ttu-id="2e706-107">Vue d’ensemble des transformations</span><span class="sxs-lookup"><span data-stu-id="2e706-107">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [<span data-ttu-id="2e706-108">Rubriques de guide pratique</span><span class="sxs-lookup"><span data-stu-id="2e706-108">How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transformations-how-to-topics.md)
- [<span data-ttu-id="2e706-109">Vue d’ensemble des formes et dessins de base dans WPF</span><span class="sxs-lookup"><span data-stu-id="2e706-109">Shapes and Basic Drawing in WPF Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/shapes-and-basic-drawing-in-wpf-overview.md)
