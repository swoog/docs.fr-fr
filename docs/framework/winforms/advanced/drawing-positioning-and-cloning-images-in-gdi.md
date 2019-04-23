---
title: Dessin, positionnement et clonage d'images dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- raster images [Windows Forms]
- images [Windows Forms], positioning
- drawing [Windows Forms], images
- drawing [Windows Forms], raster images
- images [Windows Forms], cloning
- images [Windows Forms], drawing
- GDI+, drawing images
- GDI+, cloning images
- GDI+, positioning images
ms.assetid: 09f0c07a-19c0-43b4-90a2-862a10545ce8
ms.openlocfilehash: b5f98e7bdef9ff8ed0a4cd0e040cb92a31f30503
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59188446"
---
# <a name="drawing-positioning-and-cloning-images-in-gdi"></a>Dessin, positionnement et clonage d'images dans GDI+
Vous pouvez utiliser la <xref:System.Drawing.Bitmap> classe pour charger et afficher des images raster et vous pouvez utiliser la <xref:System.Drawing.Imaging.Metafile> classe pour charger et afficher des images vectorielles. Le <xref:System.Drawing.Bitmap> et <xref:System.Drawing.Imaging.Metafile> classes héritent de la <xref:System.Drawing.Image> classe. Pour afficher une image vectorielle, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> classe et un <xref:System.Drawing.Imaging.Metafile>. Pour afficher une image raster, vous avez besoin d’une instance de la <xref:System.Drawing.Graphics> classe et un <xref:System.Drawing.Bitmap>. L’instance de la <xref:System.Drawing.Graphics> classe fournit le <xref:System.Drawing.Graphics.DrawImage%2A> (méthode), qui reçoit le <xref:System.Drawing.Imaging.Metafile> ou <xref:System.Drawing.Bitmap> en tant qu’argument.  
  
## <a name="file-types-and-cloning"></a>Types de fichiers et de clonage  
 L’exemple de code suivant montre comment construire un <xref:System.Drawing.Bitmap> à partir du fichier Climber.jpg et affiche la bitmap. Point de destination pour le coin supérieur gauche de l’image, (10, 10), est spécifié dans les deuxième et troisième paramètres.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#11)]  
  
 L’illustration suivante montre l’image.  
  
 ![Exemple d’image](./media/aboutgdip03-art04.gif "AboutGdip03_Art04")  
  
 Vous pouvez construire <xref:System.Drawing.Bitmap> formats de fichier des objets à partir d’une variété de graphiques : BMP, GIF, JPEG, EXIF, PNG, TIFF et icône.  
  
 L’exemple de code suivant montre comment construire <xref:System.Drawing.Bitmap> objets parmi un éventail de types de fichiers, puis affiche les bitmaps.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#12)]  
  
 Le <xref:System.Drawing.Bitmap> classe fournit un <xref:System.Drawing.Bitmap.Clone%2A> méthode que vous pouvez utiliser pour effectuer une copie d’un existant <xref:System.Drawing.Bitmap>. Le <xref:System.Drawing.Bitmap.Clone%2A> méthode a un paramètre de rectangle source que vous pouvez utiliser pour spécifier la partie de l’image bitmap d’origine que vous souhaitez copier. L’exemple de code suivant montre comment créer un <xref:System.Drawing.Bitmap> en clonant la moitié supérieure du existant <xref:System.Drawing.Bitmap>. Ensuite, les deux images sont dessinées.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#13)]  
  
 L’illustration suivante montre les deux images.  
  
 ![Cropping](./media/aboutgdip03-art05.gif "AboutGdip03_Art05")  
  
## <a name="see-also"></a>Voir aussi

- [Images, bitmaps et métafichiers](images-bitmaps-and-metafiles.md)
- [Guide pratique pour Créer des objets graphiques pour le dessin](how-to-create-graphics-objects-for-drawing.md)
- [Utilisation des images, bitmaps, icônes et métafichiers](working-with-images-bitmaps-icons-and-metafiles.md)
