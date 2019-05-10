---
title: 'Procédure : lister les encodeurs installés'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image codecs [Windows Forms], listing
- image encoders [Windows Forms], listing
ms.assetid: 49e8e4e9-7a67-42d9-86bf-08821cdc282e
ms.openlocfilehash: 2634dd96b3aa5edcecde092919eb328b7f3dadc3
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64626840"
---
# <a name="how-to-list-installed-encoders"></a>Procédure : lister les encodeurs installés
Voulez-vous répertorier les encodeurs d’images disponibles sur un ordinateur, pour déterminer si votre application peut enregistrer dans un format de fichier d’image particulier. Le <xref:System.Drawing.Imaging.ImageCodecInfo> classe fournit le <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> des méthodes statiques afin que vous puissiez déterminer quelle image les encodeurs sont disponibles. <xref:System.Drawing.Imaging.ImageCodecInfo.GetImageEncoders%2A> Retourne un tableau de <xref:System.Drawing.Imaging.ImageCodecInfo> objets.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant génère la liste des encodeurs installés et leurs valeurs de propriété.  
  
 [!code-csharp[UsingImageEncodersDecoders#1](~/samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#1)]
 [!code-vb[UsingImageEncodersDecoders#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
- une application Windows Forms ;  
  
- Un <xref:System.Windows.Forms.PaintEventArgs>, qui est un paramètre de <xref:System.Windows.Forms.PaintEventHandler>.  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Répertorier les décodeurs installés](how-to-list-installed-decoders.md)
- [Utilisation d’encodeurs et de décodeurs d’images dans GDI+ managé](using-image-encoders-and-decoders-in-managed-gdi.md)
