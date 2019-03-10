---
title: Génération et dessin de courbes
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [Windows Forms], curves
- examples [Windows Forms], drawing curves
- curves [Windows Forms], drawing
ms.assetid: 76e92623-4130-4644-b867-faca58bdb3a2
ms.openlocfilehash: 92e7b1e8b4ce37db633b5dafe212a252b854d1af
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57702709"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="7ff9d-102">Génération et dessin de courbes</span><span class="sxs-lookup"><span data-stu-id="7ff9d-102">Constructing and Drawing Curves</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] <span data-ttu-id="7ff9d-103">prend en charge plusieurs types de courbes : splines de Bézier, des splines cardinales, des arcs et des points de suspension.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-103">supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="7ff9d-104">Une ellipse est définie par son rectangle englobant ; un arc est une partie d’une ellipse définie par un angle de départ et un angle de balayage.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-104">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="7ff9d-105">Une spline cardinale est définie par un tableau de points et un paramètre de tension, la courbe passe sans heurts par chaque point dans le tableau, et le paramètre tension influence la courbure de la courbe.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-105">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="7ff9d-106">Une spline de Bézier définie par deux points de terminaison et deux points de contrôle que la courbe ne passe pas par les points de contrôle, mais les points de contrôle influencent la direction et de pliage comme la courbe passe à partir d’un point de terminaison à l’autre.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-106">A Bézier spline is defined by two endpoints and two control points  the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one endpoint to the other.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7ff9d-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="7ff9d-107">In This Section</span></span>  
 [<span data-ttu-id="7ff9d-108">Guide pratique pour Dessiner des splines cardinales</span><span class="sxs-lookup"><span data-stu-id="7ff9d-108">How to: Draw Cardinal Splines</span></span>](how-to-draw-cardinal-splines.md)  
 <span data-ttu-id="7ff9d-109">Décrit des splines cardinales et comment les dessiner.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-109">Describes cardinal splines and how to draw them.</span></span>  
  
 [<span data-ttu-id="7ff9d-110">Guide pratique pour Dessiner une Spline de Bézier unique</span><span class="sxs-lookup"><span data-stu-id="7ff9d-110">How to: Draw a Single Bézier Spline</span></span>](how-to-draw-a-single-bezier-spline.md)  
 <span data-ttu-id="7ff9d-111">Décrit une spline de Bézier et comment dessiner un.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-111">Describes a Bézier spline and how to draw one.</span></span>  
  
 [<span data-ttu-id="7ff9d-112">Guide pratique pour Dessiner une séquence de Splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="7ff9d-112">How to: Draw a Sequence of Bézier Splines</span></span>](how-to-draw-a-sequence-of-bezier-splines.md)  
 <span data-ttu-id="7ff9d-113">Explique comment dessiner plusieurs splines de Bézier dans la séquence.</span><span class="sxs-lookup"><span data-stu-id="7ff9d-113">Explains how to draw several Bézier splines in sequence.</span></span>
