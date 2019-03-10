---
title: Fusion alpha de lignes et de remplissages
ms.date: 03/30/2017
helpviewer_keywords:
- lines [Windows Forms], adding transparency
- examples [Windows Forms], alpha blending
- alpha blending [Windows Forms], using with lines
- alpha blending
- lines [Windows Forms], alpha blending
- fills [Windows Forms], alpha blending
- alpha blending [Windows Forms], using with fills
- shapes [Windows Forms], adding transparency
ms.assetid: 5440f48c-3ac9-44c3-b170-c1c110bdbab8
ms.openlocfilehash: 7a8286fb741effaf668b87e90da04f79d1490de2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57715995"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="143b6-102">Fusion alpha de lignes et de remplissages</span><span class="sxs-lookup"><span data-stu-id="143b6-102">Alpha Blending Lines and Fills</span></span>
<span data-ttu-id="143b6-103">Dans [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], une couleur est une valeur 32 bits avec 8 bits pour alpha, rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="143b6-103">In [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="143b6-104">La valeur alpha indique la transparence de la couleur, l’étendue à laquelle la couleur est fusionnée avec la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="143b6-104">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="143b6-105">Plage de valeurs alpha comprise entre 0 et 255, où 0 représente une couleur entièrement transparente, et 255 représente une couleur entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="143b6-105">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>  
  
 <span data-ttu-id="143b6-106">Fusion alpha est un pixel par pixel de fusion de données de couleur source et d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="143b6-106">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="143b6-107">Chacun des trois composants (rouge, vert, bleu) d’une couleur de la source donnée est fusionnée avec le composant correspondant de la couleur d’arrière-plan selon la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="143b6-107">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>  
  
 <span data-ttu-id="143b6-108">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span><span class="sxs-lookup"><span data-stu-id="143b6-108">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>  
  
 <span data-ttu-id="143b6-109">Par exemple, supposons que le composant rouge de la couleur de la source est 150 et la composante rouge de la couleur d’arrière-plan est 100.</span><span class="sxs-lookup"><span data-stu-id="143b6-109">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="143b6-110">Si la valeur alpha est de 200, le composant rouge de la couleur résultante est calculé comme suit :</span><span class="sxs-lookup"><span data-stu-id="143b6-110">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>  
  
 <span data-ttu-id="143b6-111">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="143b6-111">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="143b6-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="143b6-112">In This Section</span></span>  
 [<span data-ttu-id="143b6-113">Guide pratique pour Dessiner des lignes opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="143b6-113">How to: Draw Opaque and Semitransparent Lines</span></span>](how-to-draw-opaque-and-semitransparent-lines.md)  
 <span data-ttu-id="143b6-114">Montre comment dessiner des lignes à contrôle alpha.</span><span class="sxs-lookup"><span data-stu-id="143b6-114">Shows how to draw alpha-blended lines.</span></span>  
  
 [<span data-ttu-id="143b6-115">Guide pratique pour Dessiner avec des pinceaux opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="143b6-115">How to: Draw with Opaque and Semitransparent Brushes</span></span>](how-to-draw-with-opaque-and-semitransparent-brushes.md)  
 <span data-ttu-id="143b6-116">Explique comment la fusion alpha avec des pinceaux.</span><span class="sxs-lookup"><span data-stu-id="143b6-116">Explains how to alpha-blend with brushes.</span></span>  
  
 [<span data-ttu-id="143b6-117">Guide pratique pour Utiliser le Mode de composition pour commander la fusion Alpha</span><span class="sxs-lookup"><span data-stu-id="143b6-117">How to: Use Compositing Mode to Control Alpha Blending</span></span>](how-to-use-compositing-mode-to-control-alpha-blending.md)  
 <span data-ttu-id="143b6-118">Décrit comment contrôler la fusion alpha utilisant <xref:System.Drawing.Drawing2D.CompositingMode>.</span><span class="sxs-lookup"><span data-stu-id="143b6-118">Describes how to control alpha blending using <xref:System.Drawing.Drawing2D.CompositingMode>.</span></span>  
  
 [<span data-ttu-id="143b6-119">Guide pratique pour Utiliser une matrice de couleurs pour définir des valeurs Alpha dans des Images</span><span class="sxs-lookup"><span data-stu-id="143b6-119">How to: Use a Color Matrix to Set Alpha Values in Images</span></span>](how-to-use-a-color-matrix-to-set-alpha-values-in-images.md)  
 <span data-ttu-id="143b6-120">Explique comment utiliser un <xref:System.Drawing.Imaging.ColorMatrix> objet fusion alpha.</span><span class="sxs-lookup"><span data-stu-id="143b6-120">Explains how to use a <xref:System.Drawing.Imaging.ColorMatrix> object to control alpha blending.</span></span>
