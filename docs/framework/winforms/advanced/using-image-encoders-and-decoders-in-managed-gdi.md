---
title: Utilisation d'encodeurs et de décodeurs d'images dans GDI+ managé
ms.date: 03/30/2017
helpviewer_keywords:
- image encoders [Windows Forms], using
- image decoders [Windows Forms], using
ms.assetid: 0e838ea1-4e7e-4334-b882-ab25df607b8b
ms.openlocfilehash: e56bc20eb55d694d19b25d9e94e5c9d9e3952628
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64666443"
---
# <a name="using-image-encoders-and-decoders-in-managed-gdi"></a>Utilisation d'encodeurs et de décodeurs d'images dans GDI+ managé
Le <xref:System.Drawing> espace de noms fournit le <xref:System.Drawing.Image> et <xref:System.Drawing.Bitmap> classes pour stocker et manipuler des images. À l’aide d’encodeurs d’images dans [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], vous pouvez écrire des images de la mémoire sur le disque. À l’aide de décodeurs d’images dans [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], vous pouvez charger des images à partir du disque dans la mémoire. Un encodeur traduit les données dans un <xref:System.Drawing.Image> ou <xref:System.Drawing.Bitmap> objet dans un format de fichier de disque désigné. Un décodeur traduit les données dans un fichier de disque au format requis par le <xref:System.Drawing.Image> et <xref:System.Drawing.Bitmap> objets.  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] a intégré encodeurs et décodeurs qui prennent en charge les types de fichiers suivants :  
  
- BMP  
  
- GIF  
  
- JPEG  
  
- PNG  
  
- TIFF  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] contient également des décodeurs intégrés qui prennent en charge les types de fichiers suivants :  
  
- WMF  
  
- EMF  
  
- ICÔNE  
  
 Les rubriques suivantes traitent des encodeurs et décodeurs plus en détail :  
  
## <a name="in-this-section"></a>Dans cette section  
 [Guide pratique pour Répertorier les encodeurs installés](how-to-list-installed-encoders.md)  
 Décrit comment répertorier les encodeurs disponibles sur un ordinateur.  
  
 [Guide pratique pour Répertorier les décodeurs installés](how-to-list-installed-decoders.md)  
 Décrit comment répertorier les décodeurs disponibles sur un ordinateur.  
  
 [Guide pratique pour Déterminer les paramètres pris en charge par un encodeur](how-to-determine-the-parameters-supported-by-an-encoder.md)  
 Décrit comment répertorier les <xref:System.Drawing.Imaging.EncoderParameters> pris en charge par un encodeur.  
  
 [Guide pratique pour Convertir une image BMP en une image PNG](how-to-convert-a-bmp-image-to-a-png-image.md)  
 Décrit comment enregistrer une image dans un format d’image différent.  
  
 [Guide pratique pour Définir au niveau de Compression JPEG](how-to-set-jpeg-compression-level.md)  
 Décrit comment modifier le niveau de qualité d’une image.  
  
## <a name="reference"></a>Référence  
 <xref:System.Drawing.Image>  
  
 <xref:System.Drawing.Bitmap>  
  
 <xref:System.Drawing.Imaging.ImageCodecInfo>  
  
 <xref:System.Drawing.Imaging.EncoderParameter>  
  
 <xref:System.Drawing.Imaging.Encoder>  
  
## <a name="related-sections"></a>Rubriques connexes  
 [À propos du code managé GDI+](about-gdi-managed-code.md)  
  
 [Images, bitmaps et métafichiers](images-bitmaps-and-metafiles.md)
