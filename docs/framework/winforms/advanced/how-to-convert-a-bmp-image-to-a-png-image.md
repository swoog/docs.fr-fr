---
title: 'Procédure : Convertir une image BMP en une image PNG'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BMP images [Windows Forms], converting to PNG
- image formats [Windows Forms], converting between
ms.assetid: 9d4a692d-73ac-4ce3-9e05-9ec321e8fbd6
ms.openlocfilehash: f8636bea120aee86c795b4196415145a484e5772
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57724997"
---
# <a name="how-to-convert-a-bmp-image-to-a-png-image"></a>Procédure : Convertir une image BMP en une image PNG
Il peut arriver que vous souhaitiez effectuer une conversion d'un format de fichier image vers un autre. Vous pouvez facilement effectuer cette conversion en appelant la méthode <xref:System.Drawing.Image.Save%2A> de la classe <xref:System.Drawing.Image> et en spécifiant le <xref:System.Drawing.Imaging.ImageFormat> pour le format de fichier image souhaité.  
  
## <a name="example"></a>Exemple  
 L'exemple suivant charge une image BMP à partir d'un type et enregistre l'image au format PNG.  
  
 [!code-csharp[UsingImageEncodersDecoders#4](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#4)]
 [!code-vb[UsingImageEncodersDecoders#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une application Windows Forms ;  
  
-   une référence à l'espace de noms `System.Drawing.Imaging`.  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Répertorier les encodeurs installés](how-to-list-installed-encoders.md)
- [Utilisation d’encodeurs et de décodeurs d’images dans GDI+ managé](using-image-encoders-and-decoders-in-managed-gdi.md)
- [Types de bitmaps](types-of-bitmaps.md)
