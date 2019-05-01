---
title: 'Procédure : faire pivoter, refléter et incliner des images'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], reflecting
- images [Windows Forms], rotating
- images [Windows Forms], skewing
ms.assetid: a3bf97eb-63ed-425a-ba07-dcc65efb567c
ms.openlocfilehash: 505028c491228ffdf9c11d0c71dcd5e1afdc5103
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967156"
---
# <a name="how-to-rotate-reflect-and-skew-images"></a>Procédure : faire pivoter, refléter et incliner des images
Vous pouvez faire pivoter, refléter et incliner une image en spécifiant des points de destination pour les angles supérieur gauche, supérieur droit et inférieur gauche de l’image d’origine. Les trois points de destination déterminent une transformation affine qui mappe l’image rectangulaire d’origine à un parallélogramme.  
  
## <a name="example"></a>Exemple  
 Par exemple, supposons que l’image d’origine est un rectangle avec le coin supérieur gauche à (0, 0), coin supérieur droit à (100, 0) et le coin inférieur gauche à (0, 50). Maintenant Supposons que vous mappiez ces trois points aux points de destination comme suit.  
  
|Point d’origine|Point de destination|  
|--------------------|-----------------------|  
|Haut-gauche (0, 0)|(200, 20)|  
|Angle supérieur droit (100, 0)|(110, 100)|  
|Inférieur gauche (0, 50)|(250, 30)|  
  
 L’illustration suivante montre l’image d’origine et l’image mappée au parallélogramme. L’image d’origine a été faussée, reflétée, rotation et traduite. L’axe des abscisses le long du bord supérieur de l’image d’origine sont mappé à la ligne qui s’exécute via (200, 20) et (110, 100). L’axe des y le long du bord gauche de l’image d’origine sont mappé à la ligne qui s’exécute via (200, 20) et (250, 30).  
  
 ![L’image d’origine et l’image mappée au parallélogramme.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-illustration.gif)  
  
 L’illustration suivante montre une transformation similaire appliquée à une image photographique :  
  
 ![L’image d’un climber et l’image mappée au parallélogramme.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-photo.png)  
  
 L’illustration suivante montre une transformation similaire appliquée à un métafichier :  
  
 ![Illustration de formes et de texte et qui mappé à un parallélogramme.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-metafile.png)  
  
 L’exemple suivant produit les images présentées dans la première illustration.  
  
 [!code-csharp[System.Drawing.WorkingWithImages#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.WorkingWithImages#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs>`e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>. Veillez à remplacer `Stripes.bmp` avec le chemin d’accès à une image qui est valide sur votre système.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation des images, bitmaps, icônes et métafichiers](working-with-images-bitmaps-icons-and-metafiles.md)
