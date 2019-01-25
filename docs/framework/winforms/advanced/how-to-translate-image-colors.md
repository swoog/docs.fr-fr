---
title: 'Procédure : Traduire les couleurs d’Image'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], changing colors
- images [Windows Forms], changing colors
- image colors [Windows Forms]
ms.assetid: 2106fb9a-4d60-4dcf-9220-9f189a6c4d19
ms.openlocfilehash: 7a3ed1f3f6b3e89c8df160b7e753839e20acd877
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549757"
---
# <a name="how-to-translate-image-colors"></a>Procédure : Traduire les couleurs d’Image
Une traduction ajoute une valeur à une ou plusieurs des quatre composantes de couleur. Les entrées de matrice de couleurs qui représentent les traductions sont présentées dans le tableau suivant.  
  
|Composant à traduire|Entrée de la matrice|  
|--------------------------------|------------------|  
|Rouge|[4][0]|  
|Vert|[4][1]|  
|Bleu|[4][2]|  
|Alpha|[4][3]|  
  
## <a name="example"></a>Exemple  
 L’exemple suivant construit un <xref:System.Drawing.Image> objet à partir du fichier ColorBars.bmp. Le code ajoute ensuite 0,75 au composant rouge de chaque pixel dans l’image. L’image d’origine est dessinée en même temps que l’image transformée.  
  
 L’illustration suivante montre l’image d’origine sur la gauche et l’image transformée sur la droite.  
  
 ![Traduire les couleurs](../../../../docs/framework/winforms/advanced/media/colortrans2.png "colortrans2")  
  
 Le tableau suivant répertorie les vecteurs de couleur pour les quatre barres avant et après la traduction rouge. Notez que la valeur maximale pour un composant de couleur est 1, le composant rouge de la deuxième ligne ne change pas. (De même, la valeur minimale d’un composant de couleur est 0.)  
  
|D'origine|Langue cible|  
|--------------|----------------|  
|Noir (0, 0, 0, 1)|(0.75, 0, 0, 1)|  
|Rouge (1, 0, 0, 1)|(1, 0, 0, 1)|  
|Vert (0, 1, 0, 1)|(0.75, 1, 0, 1)|  
|Bleu (0, 0, 1, 1)|(0.75, 0, 1, 1)|  
  
 [!code-csharp[System.Drawing.RecoloringImages#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.RecoloringImages#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements. Remplacez `ColorBars.bmp` avec un nom de fichier d’image et le chemin d’accès valides sur votre système.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Graphiques et dessins dans Windows Forms](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
- [Recoloriage des images](../../../../docs/framework/winforms/advanced/recoloring-images.md)
