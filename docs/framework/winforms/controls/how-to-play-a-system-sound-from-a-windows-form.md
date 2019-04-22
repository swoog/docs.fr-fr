---
title: 'Procédure : émettre un signal sonore système à partir d’un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], playing for system events
- playing sounds [Windows Forms], Windows Forms
- system sounds [Windows Forms], playing from Windows Forms
- playing sounds [Windows Forms], system
- SoundPlayer class [Windows Forms], system sounds
- sounds [Windows Forms], playing
- examples [Windows Forms], sounds
ms.assetid: afb206ff-4824-4804-a8d4-185bf5ad8e7c
ms.openlocfilehash: d85d8cd40ff2b32cb3f2a79cf9a8221964f186c0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59153229"
---
# <a name="how-to-play-a-system-sound-from-a-windows-form"></a>Procédure : émettre un signal sonore système à partir d’un formulaire Windows
L’exemple de code suivant émet le son système `Exclamation` à l’exécution. Pour plus d’informations sur les sons système, consultez <xref:System.Media.SystemSounds>.  
  
## <a name="example"></a>Exemple  
  
```vb  
Public Sub PlayExclamation()  
    SystemSounds.Exclamation.Play()  
End Sub  
```  
  
```csharp  
public void playExclamation()  
{  
    SystemSounds.Exclamation.Play();  
}  
```  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une référence à l'espace de noms <xref:System.Media?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
- [Guide pratique pour Émettre un signal sonore à partir d’un formulaire Windows](how-to-play-a-beep-from-a-windows-form.md)
- [Guide pratique pour Un signal sonore à partir d’un formulaire Windows](how-to-play-a-sound-from-a-windows-form.md)
