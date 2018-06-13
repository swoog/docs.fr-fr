---
title: Utilisation d'un stylet pour dessiner des lignes et des formes
ms.date: 03/30/2017
helpviewer_keywords:
- pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- drawing
ms.assetid: 8a7542ab-3e9e-443f-8405-2d6053528e20
ms.openlocfilehash: 667a5b13c5e8cb5d9a693d6f8512b254f130d606
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524340"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="73de7-102">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="73de7-102">Using a Pen to Draw Lines and Shapes</span></span>
<span data-ttu-id="73de7-103">Utilisez [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] `Pen` objets pour dessiner des segments de ligne, des courbes et des contours des formes.</span><span class="sxs-lookup"><span data-stu-id="73de7-103">Use [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] `Pen` objects to draw line segments, curves, and the outlines of shapes.</span></span> <span data-ttu-id="73de7-104">Dans cette section, *ligne* fait référence à un de ces éléments, sauf si spécifié pour n'indiquer qu’un segment de ligne.</span><span class="sxs-lookup"><span data-stu-id="73de7-104">In this section, *line* refers to any of these, unless specified to mean only a line segment.</span></span> <span data-ttu-id="73de7-105">Définir les propriétés d’un stylet pour contrôler la couleur, largeur, l’alignement et le style des lignes dessinées avec ce stylet.</span><span class="sxs-lookup"><span data-stu-id="73de7-105">Set the properties of a pen to control the color, width, alignment, and style of lines drawn with that pen.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="73de7-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="73de7-106">In This Section</span></span>  
 [<span data-ttu-id="73de7-107">Guide pratique pour utiliser un stylet pour dessiner des lignes</span><span class="sxs-lookup"><span data-stu-id="73de7-107">How to: Use a Pen to Draw Lines</span></span>](../../../../docs/framework/winforms/advanced/how-to-use-a-pen-to-draw-lines.md)  
 <span data-ttu-id="73de7-108">Explique comment dessiner des lignes.</span><span class="sxs-lookup"><span data-stu-id="73de7-108">Explains how to draw lines.</span></span>  
  
 [<span data-ttu-id="73de7-109">Guide pratique pour utiliser un stylet pour dessiner des rectangles</span><span class="sxs-lookup"><span data-stu-id="73de7-109">How to: Use a Pen to Draw Rectangles</span></span>](../../../../docs/framework/winforms/advanced/how-to-use-a-pen-to-draw-rectangles.md)  
 <span data-ttu-id="73de7-110">Décrit comment dessiner des rectangles.</span><span class="sxs-lookup"><span data-stu-id="73de7-110">Describes how to draw rectangles.</span></span>  
  
 [<span data-ttu-id="73de7-111">Guide pratique pour définir la largeur et l'alignement du stylet</span><span class="sxs-lookup"><span data-stu-id="73de7-111">How to: Set Pen Width and Alignment</span></span>](../../../../docs/framework/winforms/advanced/how-to-set-pen-width-and-alignment.md)  
 <span data-ttu-id="73de7-112">Explique comment modifier la largeur et l’alignement d’un `Pen` objet.</span><span class="sxs-lookup"><span data-stu-id="73de7-112">Explains how to change the width and alignment of a `Pen` object.</span></span>  
  
 [<span data-ttu-id="73de7-113">Guide pratique pour dessiner une ligne avec des embouts de ligne</span><span class="sxs-lookup"><span data-stu-id="73de7-113">How to: Draw a Line with Line Caps</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-a-line-with-line-caps.md)  
 <span data-ttu-id="73de7-114">Décrit comment ajouter des majuscules lorsque vous dessinez une ligne.</span><span class="sxs-lookup"><span data-stu-id="73de7-114">Describes how to add end caps when drawing a line.</span></span>  
  
 [<span data-ttu-id="73de7-115">Guide pratique pour joindre des lignes</span><span class="sxs-lookup"><span data-stu-id="73de7-115">How to: Join Lines</span></span>](../../../../docs/framework/winforms/advanced/how-to-join-lines.md)  
 <span data-ttu-id="73de7-116">Montre comment joindre deux lignes.</span><span class="sxs-lookup"><span data-stu-id="73de7-116">Shows how to join two lines.</span></span>  
  
 [<span data-ttu-id="73de7-117">Guide pratique pour dessiner une ligne en pointillés personnalisée</span><span class="sxs-lookup"><span data-stu-id="73de7-117">How to: Draw a Custom Dashed Line</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-a-custom-dashed-line.md)  
 <span data-ttu-id="73de7-118">Décrit comment dessiner une ligne en pointillés.</span><span class="sxs-lookup"><span data-stu-id="73de7-118">Describes how to draw a dashed line.</span></span>  
  
 [<span data-ttu-id="73de7-119">Guide pratique pour dessiner une ligne remplie d'une texture</span><span class="sxs-lookup"><span data-stu-id="73de7-119">How to: Draw a Line Filled with a Texture</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-a-line-filled-with-a-texture.md)  
 <span data-ttu-id="73de7-120">Explique comment dessiner une ligne remplie de texture.</span><span class="sxs-lookup"><span data-stu-id="73de7-120">Explains how to draw a texture-filled line.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="73de7-121">Référence</span><span class="sxs-lookup"><span data-stu-id="73de7-121">Reference</span></span>  
 <xref:System.Drawing.Pen>  
 <span data-ttu-id="73de7-122">Décrit cette classe et fournit des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="73de7-122">Describes this class and has links to all its members.</span></span>
