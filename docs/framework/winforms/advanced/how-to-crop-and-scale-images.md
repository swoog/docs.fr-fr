---
title: 'Procédure : rogner et mettre à l’échelle des images'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: 4257431881565f9160f45795111d374cc680dedd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937569"
---
# <a name="how-to-crop-and-scale-images"></a>Procédure : rogner et mettre à l’échelle des images
Le <xref:System.Drawing.Graphics> classe fournit plusieurs <xref:System.Drawing.Graphics.DrawImage%2A> méthodes, dont certaines ont des paramètres de rectangle source et destination que vous pouvez utiliser pour rogner et mettre à l’échelle des images.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir du fichier de disque Apple.gif. Le code dessine l’image entière dans sa taille d’origine. Le code appelle ensuite la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet sur lequel dessiner une partie de l’image dans un rectangle de destination est supérieur à l’image d’origine.  
  
 Le <xref:System.Drawing.Graphics.DrawImage%2A> méthode détermine la partie de la pomme à dessiner en examinant le rectangle source, qui est spécifié par le troisième, quatrième, cinquième et sixième arguments. Dans ce cas, la pomme est rognée à 75 % de sa largeur et 75 pour cent de sa hauteur.  
  
 Le <xref:System.Drawing.Graphics.DrawImage%2A> méthode détermine où dessiner la pomme rognée et la taille pour rendre la pomme rognée en examinant le rectangle de destination, qui est spécifié par le deuxième argument. Dans ce cas, le rectangle de destination est 30 pour cent plus large et 30 pour cent plus haut que l’image d’origine.  
  
 L’illustration suivante montre la pomme d’origine et la mise à l’échelle, rognage d’apple.  
  
 ![Capture d’écran d’une image d’origine et de la même image rognée.](./media/how-to-crop-and-scale-images/original-image-cropped-image.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements. Veillez à remplacer `Apple.gif` avec un nom de fichier d’image et le chemin d’accès valides sur votre système.  
  
## <a name="see-also"></a>Voir aussi

- [Images, bitmaps et métafichiers](images-bitmaps-and-metafiles.md)
- [Utilisation des images, bitmaps, icônes et métafichiers](working-with-images-bitmaps-icons-and-metafiles.md)
