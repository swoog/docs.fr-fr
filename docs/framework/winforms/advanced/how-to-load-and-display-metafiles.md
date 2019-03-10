---
title: 'Procédure : Charge et affichage métafichiers'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- examples [Windows Forms], metafiles
- metafiles [Windows Forms], displaying
ms.assetid: 60af1714-f148-4d85-a739-0557965ffa73
ms.openlocfilehash: 121f285a95d0169db79bdc302d80dba03b3b40c2
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57720041"
---
# <a name="how-to-load-and-display-metafiles"></a>Procédure : Charge et affichage métafichiers
Le <xref:System.Drawing.Imaging.Metafile> (classe), qui hérite de la <xref:System.Drawing.Image> class, fournit des méthodes pour l’enregistrement, d’affichage et examen d’images vectorielles.  
  
## <a name="example"></a>Exemple  
 Pour afficher une image vectorielle (métafichier) sur l’écran, vous devez un <xref:System.Drawing.Imaging.Metafile> objet et un <xref:System.Drawing.Graphics> objet. Passez le nom d’un fichier (ou un flux de données) à un <xref:System.Drawing.Imaging.Metafile> constructeur. Après avoir créé un <xref:System.Drawing.Imaging.Metafile> d’objet, qui passez <xref:System.Drawing.Imaging.Metafile> de l’objet à la <xref:System.Drawing.Graphics.DrawImage%2A> méthode d’un <xref:System.Drawing.Graphics> objet.  
  
 L’exemple crée un <xref:System.Drawing.Imaging.Metafile> objet à partir d’un fichier EMF (métafichier amélioré), puis dessine l’image avec son coin supérieur gauche à (60, 10).  
  
 L’illustration suivante montre le métafichier dessiné à l’emplacement spécifié.  
  
 ![Position de l’image](./media/imageposition2.png "imageposition2")  
  
 [!code-csharp[System.Drawing.WorkingWithImages#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.WorkingWithImages#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 L'exemple précédent est conçu pour une utilisation avec Windows Forms et nécessite <xref:System.Windows.Forms.PaintEventArgs> `e`, qui est un paramètre du gestionnaire d'événements <xref:System.Windows.Forms.Control.Paint>.  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation des images, bitmaps, icônes et métafichiers](working-with-images-bitmaps-icons-and-metafiles.md)
