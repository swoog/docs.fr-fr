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
ms.openlocfilehash: f58fa2d105492c6c72d3d6906c3c35f89130fe91
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33517684"
---
# <a name="alpha-blending-lines-and-fills"></a>Fusion alpha de lignes et de remplissages
Dans [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], une couleur est une valeur 32 bits avec 8 bits pour alpha, rouge, vert et bleu. La valeur alpha indique la transparence de la couleur, le degré auquel la couleur est fusionnée avec la couleur d’arrière-plan. Plage de valeurs alpha comprise entre 0 et 255, où 0 représente une couleur entièrement transparente, et 255 représente une couleur entièrement opaque.  
  
 Fusion alpha est un mélange de pixels par source et arrière-plan des données de couleur. Chacun des trois composants (rouge, vert, bleu) d’une couleur de la source de donnée est fusionnée avec le composant correspondant de la couleur d’arrière-plan en fonction de la formule suivante :  
  
 CouleurAffichage = CouleurSource × alpha / 255 + backgroundColor × (255 – alpha) / 255  
  
 Par exemple, supposons que la composante rouge de la couleur source est 150 et la composante rouge de la couleur d’arrière-plan est 100. Si la valeur alpha est de 200, il se peut que la composante rouge de la couleur résultante est calculée comme suit :  
  
 150 × 200 / 255 + 100 × (255 – 200) / 255 = 139  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour dessiner des lignes opaques et translucides](../../../../docs/framework/winforms/advanced/how-to-draw-opaque-and-semitransparent-lines.md)  
 Montre comment dessiner des lignes à contrôle alpha.  
  
 [Guide pratique pour dessiner avec des pinceaux opaques et translucides](../../../../docs/framework/winforms/advanced/how-to-draw-with-opaque-and-semitransparent-brushes.md)  
 Explique comment la fusion alpha avec des pinceaux.  
  
 [Guide pratique pour utiliser le mode de composition pour commander la fusion alpha](../../../../docs/framework/winforms/advanced/how-to-use-compositing-mode-to-control-alpha-blending.md)  
 Décrit comment contrôler la fusion alpha utilisant <xref:System.Drawing.Drawing2D.CompositingMode>.  
  
 [Guide pratique pour utiliser une matrice de couleurs pour définir des valeurs alpha dans des images](../../../../docs/framework/winforms/advanced/how-to-use-a-color-matrix-to-set-alpha-values-in-images.md)  
 Explique comment utiliser un <xref:System.Drawing.Imaging.ColorMatrix> objet fusion alpha.
