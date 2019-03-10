---
title: 'Procédure : Lire un son système à partir d’un formulaire Windows'
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
ms.openlocfilehash: b2ac6c4f2e3334a9b4c5ff4d2a6e31b6b9bf3673
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57711221"
---
# <a name="how-to-play-a-system-sound-from-a-windows-form"></a><span data-ttu-id="fa5bc-102">Procédure : Lire un son système à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="fa5bc-102">How to: Play a System Sound from a Windows Form</span></span>
<span data-ttu-id="fa5bc-103">L’exemple de code suivant émet le son système `Exclamation` à l’exécution.</span><span class="sxs-lookup"><span data-stu-id="fa5bc-103">The following code example plays the `Exclamation` system sound at run time.</span></span> <span data-ttu-id="fa5bc-104">Pour plus d’informations sur les sons système, consultez <xref:System.Media.SystemSounds>.</span><span class="sxs-lookup"><span data-stu-id="fa5bc-104">For more information about system sounds, see <xref:System.Media.SystemSounds>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fa5bc-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="fa5bc-105">Example</span></span>  
  
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
  
## <a name="compiling-the-code"></a><span data-ttu-id="fa5bc-106">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="fa5bc-106">Compiling the Code</span></span>  
 <span data-ttu-id="fa5bc-107">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="fa5bc-107">This example requires:</span></span>  
  
-   <span data-ttu-id="fa5bc-108">une référence à l'espace de noms <xref:System.Media?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="fa5bc-108">A reference to the <xref:System.Media?displayProperty=nameWithType> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa5bc-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa5bc-109">See also</span></span>
- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
- [<span data-ttu-id="fa5bc-110">Guide pratique pour Émettre un signal sonore à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="fa5bc-110">How to: Play a Beep from a Windows Form</span></span>](how-to-play-a-beep-from-a-windows-form.md)
- [<span data-ttu-id="fa5bc-111">Guide pratique pour Un signal sonore à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="fa5bc-111">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
