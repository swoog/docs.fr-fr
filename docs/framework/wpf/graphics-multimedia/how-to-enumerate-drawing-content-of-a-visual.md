---
title: 'Procédure : Énumérer le contenu de dessin d’un visuel'
ms.date: 03/30/2017
helpviewer_keywords:
- retrieving the DrawingGroup value of a Visual [WPF]
- enumerating the contents of a Visual [WPF]
ms.assetid: 2974ddb3-2997-4713-8fd2-e93d549c58a8
ms.openlocfilehash: 4f0afc1075fe66c7f154fcef3cd883709db55316
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108002"
---
# <a name="how-to-enumerate-drawing-content-of-a-visual"></a><span data-ttu-id="8e4b2-102">Procédure : Énumérer le contenu de dessin d’un visuel</span><span class="sxs-lookup"><span data-stu-id="8e4b2-102">How to: Enumerate Drawing Content of a Visual</span></span>
<span data-ttu-id="8e4b2-103">Le <xref:System.Windows.Media.Drawing> objet fournissent un modèle d’objet pour énumérer le contenu d’un <xref:System.Windows.Media.Visual>.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-103">The <xref:System.Windows.Media.Drawing> object provide an object model for enumerating the contents of a <xref:System.Windows.Media.Visual>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8e4b2-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8e4b2-104">Example</span></span>  
 <span data-ttu-id="8e4b2-105">L’exemple suivant utilise le <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> méthode pour récupérer le <xref:System.Windows.Media.DrawingGroup> valeur d’un <xref:System.Windows.Media.Visual> et l’énumérer.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-105">The following example uses the <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> method to retrieve the <xref:System.Windows.Media.DrawingGroup> value of a <xref:System.Windows.Media.Visual> and enumerate it.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8e4b2-106">Lorsque vous énumérez le contenu de l’élément visuel, vous récupérez <xref:System.Windows.Media.Drawing> objets et pas la représentation sous-jacente des données rendues comme une liste d’instructions de graphismes vectoriels.</span><span class="sxs-lookup"><span data-stu-id="8e4b2-106">When you are enumerating the contents of the visual, you are retrieving <xref:System.Windows.Media.Drawing> objects, and not the underlying representation of the render data as a vector graphics instruction list.</span></span> <span data-ttu-id="8e4b2-107">Pour plus d’informations, consultez [Vue d’ensemble du rendu graphique WPF](wpf-graphics-rendering-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e4b2-107">For more information, see [WPF Graphics Rendering Overview](wpf-graphics-rendering-overview.md).</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMRetrieveDrawings](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/EnumerateDrawingsExample.xaml.cs#graphicsmmretrievedrawings)]  
  
## <a name="see-also"></a><span data-ttu-id="8e4b2-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e4b2-108">See also</span></span>

- <xref:System.Windows.Media.Drawing>
- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.VisualTreeHelper>
- [<span data-ttu-id="8e4b2-109">Vue d'ensemble des objets Drawing</span><span class="sxs-lookup"><span data-stu-id="8e4b2-109">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
- [<span data-ttu-id="8e4b2-110">Vue d'ensemble du rendu graphique de WPF</span><span class="sxs-lookup"><span data-stu-id="8e4b2-110">WPF Graphics Rendering Overview</span></span>](wpf-graphics-rendering-overview.md)
