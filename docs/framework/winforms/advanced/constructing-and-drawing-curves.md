---
title: Génération et dessin de courbes
ms.date: 03/30/2017
helpviewer_keywords:
- drawing [Windows Forms], curves
- examples [Windows Forms], drawing curves
- curves [Windows Forms], drawing
ms.assetid: 76e92623-4130-4644-b867-faca58bdb3a2
ms.openlocfilehash: d9a790060fdf0f0c2a739d99aba1b36cf0323f8b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33520615"
---
# <a name="constructing-and-drawing-curves"></a>Génération et dessin de courbes
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] prend en charge plusieurs types de courbes : ellipses, arcs, splines cardinales et splines de Bézier. Une ellipse définie par son rectangle englobant ; un arc est une partie d’une ellipse définie par un angle de départ et un angle de balayage. Une spline cardinale est définie par un tableau de points et un paramètre de tension — la courbe passe sans heurts sur chaque point dans le tableau et le paramètre tension influe sur la courbure de la courbe. Une spline de Bézier définie par deux points de terminaison et deux points de contrôle que la courbe ne passe pas par les points de contrôle, mais les points de contrôle influencent la direction et de pliage d’à partir d’un point de terminaison à l’autre.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour dessiner des splines cardinales](../../../../docs/framework/winforms/advanced/how-to-draw-cardinal-splines.md)  
 Décrit des splines cardinales et comment les dessiner.  
  
 [Guide pratique pour dessiner une spline de Bézier unique](../../../../docs/framework/winforms/advanced/how-to-draw-a-single-bezier-spline.md)  
 Décrit une spline de Bézier et comment dessiner une.  
  
 [Guide pratique pour dessiner une séquence de splines de Bézier](../../../../docs/framework/winforms/advanced/how-to-draw-a-sequence-of-bezier-splines.md)  
 Explique comment dessiner plusieurs splines de Bézier dans l’ordre.
