---
title: Guide pratique pour émettre un son incorporé dans une ressource à partir d'un Windows Form
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], playing from resources
- resources [Windows Forms], playing sounds
- playing sounds [Windows Forms], from resources
- SoundPlayer class [Windows Forms], playing sounds from resources
ms.assetid: 7d148bb6-8a1e-47d7-a08d-35828d2e688f
ms.openlocfilehash: c9dc8499e2d12ed17f9b409a805148d08da894fc
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33532133"
---
# <a name="how-to-play-a-sound-embedded-in-a-resource-from-a-windows-form"></a>Guide pratique pour émettre un son incorporé dans une ressource à partir d'un Windows Form
Vous pouvez utiliser la <xref:System.Media.SoundPlayer> classe pour lire un son à partir d’une ressource incorporée.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[System.Windows.Forms.Sound#10](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Sound/CS/soundtestform.cs#10)]
 [!code-vb[System.Windows.Forms.Sound#10](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Sound/VB/soundtestform.vb#10)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
 L’importation du <xref:System.Media?displayProperty=nameWithType> espace de noms.  
  
 L’inclusion du fichier audio en tant que ressource incorporée dans votre projet.  
  
 Le remplacement de « \<AssemblyName » par le nom de l’assembly dans lequel le fichier audio est incorporé. N’incluez pas le suffixe « .dll ».  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Media.SoundPlayer>  
 [Guide pratique pour lire un son à partir d’un Windows Form](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)  
 [Guide pratique pour mettre en boucle l’émission d’un son dans un Windows Form](../../../../docs/framework/winforms/controls/how-to-loop-a-sound-playing-on-a-windows-form.md)
