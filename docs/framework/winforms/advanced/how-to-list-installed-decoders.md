---
title: 'Procédure : lister les décodeurs installés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image decoders [Windows Forms], listing
ms.assetid: 11417191-8c95-40ca-8024-779e61706fb6
ms.openlocfilehash: c92b8010def2f77f859ee0bd9cdb1ed51dd15f27
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079409"
---
# <a name="how-to-list-installed-decoders"></a>Procédure : lister les décodeurs installés
Voulez-vous répertorier les décodeurs d’images disponibles sur un ordinateur, pour déterminer si votre application peut lire un format de fichier d’image particulier. Le <xref:System.Drawing.Imaging.ImageCodecInfo> classe fournit le <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> des méthodes statiques afin que vous pouvez déterminer quelle image décodeurs disponibles. <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageDecoders%2A> Retourne un tableau de <xref:System.Drawing.Imaging.ImageCodecInfo> objets.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant génère la liste des décodeurs installés et leurs valeurs de propriété.  
  
 [!code-csharp[UsingImageEncodersDecoders#2](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#2)]
 [!code-vb[UsingImageEncodersDecoders#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#2)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une application Windows Forms ;  
  
-   Un <xref:System.Windows.Forms.PaintEventArgs>, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi

- [Procédure : lister les encodeurs installés](how-to-list-installed-encoders.md)
- [Utilisation d'encodeurs et de décodeurs d'images dans GDI+ managé](using-image-encoders-and-decoders-in-managed-gdi.md)
