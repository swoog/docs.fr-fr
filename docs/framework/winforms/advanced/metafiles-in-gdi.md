---
title: Métafichiers dans GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], metafiles
- GDI+, metafiles
- metafiles
ms.assetid: 51da872c-c783-440f-8bf6-1e580a966c31
ms.openlocfilehash: f46c24b699aa49db2bc4b8467ce96a125602acec
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645746"
---
# <a name="metafiles-in-gdi"></a>Métafichiers dans GDI+
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] Fournit la <xref:System.Drawing.Imaging.Metafile> classe afin que vous pouvez enregistrer et afficher des métafichiers. Un métafichier, également appelé image vectorielle, est une image qui est stockée comme une séquence de commandes et les paramètres de dessin. Les commandes et les paramètres enregistrement dans un <xref:System.Drawing.Imaging.Metafile> objet peut être stocké en mémoire ou enregistré dans un fichier ou le flux.  
  
## <a name="metafile-formats"></a>Formats de métafichier  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] peut afficher des métafichiers qui ont été stockés dans les formats suivants :  
  
- Métafichier Windows (WMF)  
  
- métafichier amélioré (EMF)  
  
- EMF+  
  
 [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] peut enregistrer des métafichiers aux formats EMF et EMF +, mais pas dans le format WMF.  
  
 EMF + est une extension d’EMF qui permet [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] enregistrements doivent être stockés. Il existe deux variantes du format EMF + : EMF + uniquement et double EMF +. Métafichiers EMF + Only contiennent uniquement [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] enregistrements. Ces métafichiers peuvent être affichés par [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] mais pas par [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)]. Les métafichiers EMF + Dual contiennent [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] et [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] enregistrements. Chaque [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] enregistrements dans une double EMF + métafichier est associée à un autre [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)] enregistrement. Ces métafichiers peuvent être affichés par [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] ou par [!INCLUDE[ndptecgdi](../../../../includes/ndptecgdi-md.md)].  
  
 L’exemple suivant affiche un métafichier précédemment enregistré en tant que fichier. Le métafichier est affiché avec son coin supérieur gauche à (100, 100).  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#21)]  
  
## <a name="see-also"></a>Voir aussi

- [Images, bitmaps et métafichiers](images-bitmaps-and-metafiles.md)
