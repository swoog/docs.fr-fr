---
title: 'Procédure : émettre un signal sonore incorporé dans une ressource à partir d’un formulaire Windows'
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
ms.openlocfilehash: 49235f9cb035c5a09c26b427f855fc00e818fe1c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59078575"
---
# <a name="how-to-play-a-sound-embedded-in-a-resource-from-a-windows-form"></a><span data-ttu-id="29605-102">Procédure : émettre un signal sonore incorporé dans une ressource à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="29605-102">How to: Play a Sound Embedded in a Resource from a Windows Form</span></span>
<span data-ttu-id="29605-103">Vous pouvez utiliser la <xref:System.Media.SoundPlayer> classe pour lire un son à partir d’une ressource incorporée.</span><span class="sxs-lookup"><span data-stu-id="29605-103">You can use the <xref:System.Media.SoundPlayer> class to play a sound from an embedded resource.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29605-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="29605-104">Example</span></span>  
 [!code-csharp[System.Windows.Forms.Sound#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Sound/CS/soundtestform.cs#10)]
 [!code-vb[System.Windows.Forms.Sound#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Sound/VB/soundtestform.vb#10)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="29605-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="29605-105">Compiling the Code</span></span>  
 <span data-ttu-id="29605-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="29605-106">This example requires:</span></span>  
  
 <span data-ttu-id="29605-107">L’importation du <xref:System.Media?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="29605-107">Importing the <xref:System.Media?displayProperty=nameWithType> namespace.</span></span>  
  
 <span data-ttu-id="29605-108">L’inclusion du fichier audio en tant que ressource incorporée dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="29605-108">Including the sound file as an embedded resource in your project.</span></span>  
  
 <span data-ttu-id="29605-109">Le remplacement de « \<AssemblyName » par le nom de l’assembly dans lequel le fichier audio est incorporé.</span><span class="sxs-lookup"><span data-stu-id="29605-109">Replacing "\<AssemblyName>" with the name of the assembly in which the sound file is embedded.</span></span> <span data-ttu-id="29605-110">N’incluez pas le suffixe « .dll ».</span><span class="sxs-lookup"><span data-stu-id="29605-110">Do not include the ".dll" suffix.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29605-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29605-111">See also</span></span>

- <xref:System.Media.SoundPlayer>
- [<span data-ttu-id="29605-112">Guide pratique pour Un signal sonore à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="29605-112">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
- [<span data-ttu-id="29605-113">Guide pratique pour Lecture d’un formulaire Windows d’un son en boucle</span><span class="sxs-lookup"><span data-stu-id="29605-113">How to: Loop a Sound Playing on a Windows Form</span></span>](how-to-loop-a-sound-playing-on-a-windows-form.md)
