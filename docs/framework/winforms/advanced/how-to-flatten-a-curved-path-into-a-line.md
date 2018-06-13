---
title: 'Comment : aplanir un tracé courbé en une ligne'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], flattening curves into lines
- curves [Windows Forms], flattening
- GraphicsPath object
- paths [Windows Forms], flattening
- drawing [Windows Forms], flattening curves
ms.assetid: e654b8de-25f4-4735-9208-42e4514a589c
ms.openlocfilehash: a3a8467dc5906a88911672316bb0f2ed3607d3a4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33521201"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a><span data-ttu-id="1c217-102">Comment : aplanir un tracé courbé en une ligne</span><span class="sxs-lookup"><span data-stu-id="1c217-102">How to: Flatten a Curved Path into a Line</span></span>
<span data-ttu-id="1c217-103">A <xref:System.Drawing.Drawing2D.GraphicsPath> objet stocke une séquence de lignes et de splines de Bézier.</span><span class="sxs-lookup"><span data-stu-id="1c217-103">A <xref:System.Drawing.Drawing2D.GraphicsPath> object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="1c217-104">Vous pouvez ajouter plusieurs types de courbes (ellipses, arcs, splines cardinales) à un chemin d’accès, mais chaque courbe est converti en une spline de Bézier avant d’être stockée dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="1c217-104">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="1c217-105">La mise à plat d’un chemin d’accès consiste à convertir chaque spline de Bézier dans le chemin d’accès à une séquence de lignes droites.</span><span class="sxs-lookup"><span data-stu-id="1c217-105">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span> <span data-ttu-id="1c217-106">L’illustration suivante montre un chemin d’accès avant et après la mise à plat.</span><span class="sxs-lookup"><span data-stu-id="1c217-106">The following illustration shows a path before and after flattening.</span></span>  
  
 <span data-ttu-id="1c217-107">![Lignes droites et courbes](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")</span><span class="sxs-lookup"><span data-stu-id="1c217-107">![Straight Lines and Curves](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")</span></span>  
  
### <a name="to-flatten-a-path"></a><span data-ttu-id="1c217-108">Pour aplatir un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="1c217-108">To Flatten a Path</span></span>  
  
-   <span data-ttu-id="1c217-109">Appelez le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode d’un <xref:System.Drawing.Drawing2D.GraphicsPath> objet.</span><span class="sxs-lookup"><span data-stu-id="1c217-109">call the <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> method of a <xref:System.Drawing.Drawing2D.GraphicsPath> object.</span></span> <span data-ttu-id="1c217-110">Le <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> méthode reçoit un argument d’aplatissement qui spécifie la distance maximale entre le tracé aplati et le chemin d’accès d’origine.</span><span class="sxs-lookup"><span data-stu-id="1c217-110">The <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c217-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c217-111">See Also</span></span>  
 <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>  
 [<span data-ttu-id="1c217-112">Lignes, courbes et formes</span><span class="sxs-lookup"><span data-stu-id="1c217-112">Lines, Curves, and Shapes</span></span>](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)  
 [<span data-ttu-id="1c217-113">Génération et dessin de tracés</span><span class="sxs-lookup"><span data-stu-id="1c217-113">Constructing and Drawing Paths</span></span>](../../../../docs/framework/winforms/advanced/constructing-and-drawing-paths.md)
