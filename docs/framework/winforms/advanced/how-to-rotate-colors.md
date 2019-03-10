---
title: 'Procédure : Rotation des couleurs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], rotating
- examples [Windows Forms], rotating colors
ms.assetid: e2e4c300-159c-4f4a-9b56-103b0f7cbc05
ms.openlocfilehash: cb3824d8a5a5674b83124301dbfbd5a3ba60effa
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57720616"
---
# <a name="how-to-rotate-colors"></a>Procédure : Rotation des couleurs
Rotation dans un espace de couleurs à quatre dimensions est difficile à visualiser. Nous pouvons facilitent la visualisation, choisissez de conserver un seul des composants de couleur fixe. Supposons que nous mettre d’accord conserver le composant alpha fixé à 1 (totalement opaque). Vous pouvez ensuite visualiser un espace de couleurs à trois dimensions avec des axes rouges, vert et bleus, comme indiqué dans l’illustration suivante.  
  
 ![Recoloriage](./media/recoloring03.gif "recoloring03")  
  
 Une couleur peut être considérée comme un point dans l’espace 3D. Par exemple, le point (1, 0, 0) dans l’espace représente la couleur rouge, et le point (0, 1, 0) dans l’espace représente la couleur verte.  
  
 L’illustration suivante montre ce que cela signifie pour faire pivoter la couleur (1, 0, 0) via un angle de 60 degrés dans le plan rouge-vert. Rotation d’un plan parallèle au plan rouge-vert peut être considérée comme une rotation sur l’axe bleu.  
  
 ![Recoloriage](./media/recoloring04.gif "recoloring04")  
  
 L’illustration suivante montre comment initialiser une matrice de couleurs pour effectuer des rotations sur chacun des trois axes de coordonnées (rouge, vert, bleu).  
  
 ![Recoloring](./media/recoloring05.gif "recoloring05")  
  
## <a name="example"></a>Exemple  
 L’exemple suivant prend une image qui est une couleur (1, 0, 0.6) et applique une rotation de 60 degrés autour de l’axe bleu. L’angle de rotation est balayé pour passer d’un plan parallèle au plan rouge-vert.  
  
 L’illustration suivante montre l’image d’origine sur la gauche et l’image pivoté de couleur sur la droite.  
  
 ![Faire pivoter des couleurs](./media/colortrans5.png "colortrans5")  
  
 L’illustration suivante montre une visualisation de la rotation de couleurs effectuée dans le code suivant.  
  
 ![Recoloriage](./media/recoloring06.gif "recoloring06")  
  
 [!code-csharp[System.Drawing.RotateColors#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RotateColors/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.RotateColors#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RotateColors/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>. Remplacez `RotationInput.bmp` avec un nom de fichier d’image et le chemin d’accès valide sur votre système.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Graphiques et dessins dans Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Recoloriage des images](recoloring-images.md)
