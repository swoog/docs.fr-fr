---
title: 'Procédure : Utiliser une Table de remappage des couleurs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- color tables [Windows Forms], remapping colors with
- custom colors [Windows Forms], creating with color remap table
- color remap tables [Windows Forms], using
ms.assetid: 977df1ce-8665-42d4-9fb1-ef7f0ff63419
ms.openlocfilehash: 06a25179a3afc004029972bbf7d4d5691d42b25b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54683909"
---
# <a name="how-to-use-a-color-remap-table"></a>Procédure : Utiliser une Table de remappage des couleurs
Remappage est le processus de conversion des couleurs dans une image en fonction d’une table de remappage des couleurs. La table de remappage des couleurs est un tableau de <xref:System.Drawing.Imaging.ColorMap> objets. Chaque <xref:System.Drawing.Imaging.ColorMap> objet dans le tableau a une <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> propriété et un <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> propriété.  
  
 Lorsque [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] Dessine une image, chaque pixel de l’image est comparé au tableau des anciennes couleurs. Si de la couleur d’un pixel correspond à une ancienne couleur, sa couleur est remplacée par la nouvelle couleur correspondante. Les couleurs sont modifiées uniquement pour le rendu, les valeurs de couleur de l’image elle-même (stockées dans un <xref:System.Drawing.Image> ou <xref:System.Drawing.Bitmap> objet) ne sont pas modifiés.  
  
 Pour dessiner une image remappée, initialiser un tableau de <xref:System.Drawing.Imaging.ColorMap> objets. Passer ce tableau à la <xref:System.Drawing.Imaging.ImageAttributes.SetRemapTable%2A> méthode d’un <xref:System.Drawing.Imaging.ImageAttributes> de l’objet, puis passer la <xref:System.Drawing.Imaging.ImageAttributes> de l’objet à la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un <xref:System.Drawing.Image> objet à partir du fichier RemapInput.bmp. Le code crée une table de remappage des couleurs qui se compose d’un seul <xref:System.Drawing.Imaging.ColorMap> objet. Le <xref:System.Drawing.Imaging.ColorMap.OldColor%2A> propriété de la `ColorRemap` objet est rouge et le <xref:System.Drawing.Imaging.ColorMap.NewColor%2A> propriété est bleu. L’image est dessinée une fois sans le remappage et une autre fois avec le remappage. Le processus de remappage modifie tous les pixels rouge au bleu.  
  
 L’illustration suivante montre l’image d’origine sur la gauche et l’image remappée sur la droite.  
  
 ![Color ReMap](../../../../docs/framework/winforms/advanced/media/colortrans7.png "colortrans7")  
  
 [!code-csharp[System.Drawing.RecoloringImages#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.RecoloringImages#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L’exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre de la <xref:System.Windows.Forms.Control.Paint> Gestionnaire d’événements.  
  
## <a name="see-also"></a>Voir aussi
- [Recoloriage des images](../../../../docs/framework/winforms/advanced/recoloring-images.md)
- [Images, bitmaps et métafichiers](../../../../docs/framework/winforms/advanced/images-bitmaps-and-metafiles.md)
