---
title: 'Procédure : Rogner et mettre à l’échelle des Images'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: 95343ad2c7bc6a83bc4d935f33712ab910d658ff
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57705816"
---
# <a name="how-to-crop-and-scale-images"></a>Procédure : Rogner et mettre à l’échelle des Images
Le <xref:System.Drawing.Graphics> classe fournit plusieurs <xref:System.Drawing.Graphics.DrawImage%2A> méthodes, dont certaines ont des paramètres de rectangle source et destination que vous pouvez utiliser pour rogner et mettre à l’échelle des images.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir du fichier de disque Apple.gif. Le code dessine l’image entière dans sa taille d’origine. Le code appelle ensuite la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet sur lequel dessiner une partie de l’image dans un rectangle de destination est supérieur à l’image d’origine.  
  
 Le <xref:System.Drawing.Graphics.DrawImage%2A> méthode détermine la partie de la pomme à dessiner en examinant le rectangle source, qui est spécifié par le troisième, quatrième, cinquième et sixième arguments. Dans ce cas, la pomme est rognée à 75 % de sa largeur et 75 pour cent de sa hauteur.  
  
 Le <xref:System.Drawing.Graphics.DrawImage%2A> méthode détermine où dessiner la pomme rognée et la taille pour rendre la pomme rognée en examinant le rectangle de destination, qui est spécifié par le deuxième argument. Dans ce cas, le rectangle de destination est 30 pour cent plus large et 30 pour cent plus haut que l’image d’origine.  
  
 L’illustration suivante montre la pomme d’origine et la mise à l’échelle, rognage d’apple.  
  
 ![Rogner et mettre à l’échelle](./media/cscropscale1.png "csCropScale1")  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>. Veillez à remplacer `Apple.gif` avec un nom de fichier d’image et le chemin d’accès valides sur votre système.  
  
## <a name="see-also"></a>Voir aussi
- [Images, bitmaps et métafichiers](images-bitmaps-and-metafiles.md)
- [Utilisation des images, bitmaps, icônes et métafichiers](working-with-images-bitmaps-icons-and-metafiles.md)
