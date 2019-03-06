---
title: "Procédure : Créer une image bitmap à partir d'un Visual"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: 429aacc99d8ead5a18e9be7602b19a74773b419a
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57362862"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a><span data-ttu-id="9540e-102">Procédure : Créer une image bitmap à partir d'un Visual</span><span class="sxs-lookup"><span data-stu-id="9540e-102">How to: Create a Bitmap from a Visual</span></span>
<span data-ttu-id="9540e-103">Cet exemple montre comment vous pouvez créer une image bitmap à partir d’un <xref:System.Windows.Media.Visual>.</span><span class="sxs-lookup"><span data-stu-id="9540e-103">This example shows how you can create a bitmap from a <xref:System.Windows.Media.Visual>.</span></span> <span data-ttu-id="9540e-104">Un <xref:System.Windows.Media.DrawingVisual> est rendue avec <xref:System.Windows.Media.FormattedText>.</span><span class="sxs-lookup"><span data-stu-id="9540e-104">A <xref:System.Windows.Media.DrawingVisual> is rendered with <xref:System.Windows.Media.FormattedText>.</span></span> <span data-ttu-id="9540e-105">Le <xref:System.Windows.Media.Visual> est ensuite rendu dans le <xref:System.Windows.Media.Imaging.RenderTargetBitmap> création d’une bitmap d’un texte donné.</span><span class="sxs-lookup"><span data-stu-id="9540e-105">The <xref:System.Windows.Media.Visual> is then rendered to the <xref:System.Windows.Media.Imaging.RenderTargetBitmap> creating a bitmap of the given text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9540e-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="9540e-106">Example</span></span>  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a><span data-ttu-id="9540e-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9540e-107">See also</span></span>
- <xref:System.Windows.Media.DrawingContext>
- [<span data-ttu-id="9540e-108">Vue d’ensemble de la création d’images</span><span class="sxs-lookup"><span data-stu-id="9540e-108">Imaging Overview</span></span>](imaging-overview.md)
- [<span data-ttu-id="9540e-109">Vue d’ensemble des objets de dessin</span><span class="sxs-lookup"><span data-stu-id="9540e-109">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="9540e-110">Utilisation d’objets DrawingVisual</span><span class="sxs-lookup"><span data-stu-id="9540e-110">Using DrawingVisual Objects</span></span>](using-drawingvisual-objects.md)
