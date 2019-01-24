---
title: 'Procédure : Lire un son incorporé dans une ressource à partir d’un formulaire Windows'
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
ms.openlocfilehash: 390f70acc99d8950a23ce514d90c79c3da765f2a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631332"
---
# <a name="how-to-play-a-sound-embedded-in-a-resource-from-a-windows-form"></a>Procédure : Lire un son incorporé dans une ressource à partir d’un formulaire Windows
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
- <xref:System.Media.SoundPlayer>
- [Guide pratique pour Un signal sonore à partir d’un formulaire Windows](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
- [Guide pratique pour Lecture d’un formulaire Windows d’un son en boucle](../../../../docs/framework/winforms/controls/how-to-loop-a-sound-playing-on-a-windows-form.md)
