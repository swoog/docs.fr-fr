---
title: 'Procédure : Émettre un signal sonore à partir d’un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], beep
- Windows Forms, sounds
- sounds [Windows Forms], playing
- forms [Windows Forms], sounds
- examples [Windows Forms], sounds
ms.assetid: 7ea5cded-4888-4f35-8f28-5cab1a55c973
ms.openlocfilehash: b847f2f759667eed5dfb6f9168a5c2fc50909cc3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54544508"
---
# <a name="how-to-play-a-beep-from-a-windows-form"></a>Procédure : Émettre un signal sonore à partir d’un formulaire Windows
Cet exemple émet un signal sonore à l’exécution.  
  
## <a name="example"></a>Exemple  
  
```vb  
Public Sub OnePing()  
    Beep()  
End Sub  
```  
  
```csharp  
public void onePing()  
{  
    SystemSounds.Beep.Play();  
}  
```  
  
> [!NOTE]
>  Le son exécuté dans le C# exemple de code est déterminé par le <xref:System.Media.SystemSounds.Beep%2A> paramètre de son système. Pour plus d'informations, consultez <xref:System.Media.SystemSounds>.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Pour C#, cet exemple requiert une référence à la <xref:System.Media?displayProperty=nameWithType> espace de noms.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Interaction.Beep%2A>
- <xref:System.Media.SoundPlayer>
- [Guide pratique pour Lire un son système à partir d’un formulaire Windows](../../../../docs/framework/winforms/controls/how-to-play-a-system-sound-from-a-windows-form.md)
- [Guide pratique pour Un signal sonore à partir d’un formulaire Windows](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
