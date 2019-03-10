---
title: Utilisation d'un stylet pour dessiner des lignes et des formes
ms.date: 03/30/2017
helpviewer_keywords:
- pens
- examples [Windows Forms], drawing lines and shapes
- examples [Windows Forms], pens
- drawing
ms.assetid: 8a7542ab-3e9e-443f-8405-2d6053528e20
ms.openlocfilehash: 3846c59712cec6003c35f336714041544dec94b3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716278"
---
# <a name="using-a-pen-to-draw-lines-and-shapes"></a><span data-ttu-id="39b7b-102">Utilisation d'un stylet pour dessiner des lignes et des formes</span><span class="sxs-lookup"><span data-stu-id="39b7b-102">Using a Pen to Draw Lines and Shapes</span></span>
<span data-ttu-id="39b7b-103">Utilisez [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] `Pen` objets pour dessiner des segments de ligne, des courbes et des contours des formes.</span><span class="sxs-lookup"><span data-stu-id="39b7b-103">Use [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] `Pen` objects to draw line segments, curves, and the outlines of shapes.</span></span> <span data-ttu-id="39b7b-104">Dans cette section, *ligne* fait référence à un de ces éléments, sauf indication contraire pour signifier uniquement un segment de ligne.</span><span class="sxs-lookup"><span data-stu-id="39b7b-104">In this section, *line* refers to any of these, unless specified to mean only a line segment.</span></span> <span data-ttu-id="39b7b-105">Définir les propriétés d’un stylet pour contrôler la couleur, la largeur, l’alignement et le style des lignes dessinées avec ce stylet.</span><span class="sxs-lookup"><span data-stu-id="39b7b-105">Set the properties of a pen to control the color, width, alignment, and style of lines drawn with that pen.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="39b7b-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="39b7b-106">In This Section</span></span>  
 [<span data-ttu-id="39b7b-107">Guide pratique pour Utiliser un stylet pour dessiner des lignes</span><span class="sxs-lookup"><span data-stu-id="39b7b-107">How to: Use a Pen to Draw Lines</span></span>](how-to-use-a-pen-to-draw-lines.md)  
 <span data-ttu-id="39b7b-108">Explique comment dessiner des lignes.</span><span class="sxs-lookup"><span data-stu-id="39b7b-108">Explains how to draw lines.</span></span>  
  
 [<span data-ttu-id="39b7b-109">Guide pratique pour Utiliser un stylet pour dessiner des Rectangles</span><span class="sxs-lookup"><span data-stu-id="39b7b-109">How to: Use a Pen to Draw Rectangles</span></span>](how-to-use-a-pen-to-draw-rectangles.md)  
 <span data-ttu-id="39b7b-110">Décrit comment dessiner des rectangles.</span><span class="sxs-lookup"><span data-stu-id="39b7b-110">Describes how to draw rectangles.</span></span>  
  
 [<span data-ttu-id="39b7b-111">Guide pratique pour Largeur du stylet ensemble et l’alignement</span><span class="sxs-lookup"><span data-stu-id="39b7b-111">How to: Set Pen Width and Alignment</span></span>](how-to-set-pen-width-and-alignment.md)  
 <span data-ttu-id="39b7b-112">Explique comment modifier la largeur et l’alignement d’un `Pen` objet.</span><span class="sxs-lookup"><span data-stu-id="39b7b-112">Explains how to change the width and alignment of a `Pen` object.</span></span>  
  
 [<span data-ttu-id="39b7b-113">Guide pratique pour Dessiner une ligne avec des embouts de ligne</span><span class="sxs-lookup"><span data-stu-id="39b7b-113">How to: Draw a Line with Line Caps</span></span>](how-to-draw-a-line-with-line-caps.md)  
 <span data-ttu-id="39b7b-114">Décrit comment ajouter des embouts lorsque vous dessinez une ligne.</span><span class="sxs-lookup"><span data-stu-id="39b7b-114">Describes how to add end caps when drawing a line.</span></span>  
  
 [<span data-ttu-id="39b7b-115">Guide pratique pour Joindre des lignes</span><span class="sxs-lookup"><span data-stu-id="39b7b-115">How to: Join Lines</span></span>](how-to-join-lines.md)  
 <span data-ttu-id="39b7b-116">Montre comment joindre deux lignes.</span><span class="sxs-lookup"><span data-stu-id="39b7b-116">Shows how to join two lines.</span></span>  
  
 [<span data-ttu-id="39b7b-117">Guide pratique pour Dessiner une ligne en pointillés personnalisée</span><span class="sxs-lookup"><span data-stu-id="39b7b-117">How to: Draw a Custom Dashed Line</span></span>](how-to-draw-a-custom-dashed-line.md)  
 <span data-ttu-id="39b7b-118">Décrit comment dessiner une ligne en pointillés.</span><span class="sxs-lookup"><span data-stu-id="39b7b-118">Describes how to draw a dashed line.</span></span>  
  
 [<span data-ttu-id="39b7b-119">Guide pratique pour Dessiner une ligne remplie d’une Texture</span><span class="sxs-lookup"><span data-stu-id="39b7b-119">How to: Draw a Line Filled with a Texture</span></span>](how-to-draw-a-line-filled-with-a-texture.md)  
 <span data-ttu-id="39b7b-120">Explique comment dessiner une ligne remplie de texture.</span><span class="sxs-lookup"><span data-stu-id="39b7b-120">Explains how to draw a texture-filled line.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="39b7b-121">Référence</span><span class="sxs-lookup"><span data-stu-id="39b7b-121">Reference</span></span>  
 <xref:System.Drawing.Pen>  
 <span data-ttu-id="39b7b-122">Décrit cette classe et fournit des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="39b7b-122">Describes this class and has links to all its members.</span></span>
