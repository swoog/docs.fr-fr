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
# <a name="how-to-play-a-sound-embedded-in-a-resource-from-a-windows-form"></a><span data-ttu-id="6e6e8-102">Guide pratique pour émettre un son incorporé dans une ressource à partir d'un Windows Form</span><span class="sxs-lookup"><span data-stu-id="6e6e8-102">How to: Play a Sound Embedded in a Resource from a Windows Form</span></span>
<span data-ttu-id="6e6e8-103">Vous pouvez utiliser la <xref:System.Media.SoundPlayer> classe pour lire un son à partir d’une ressource incorporée.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-103">You can use the <xref:System.Media.SoundPlayer> class to play a sound from an embedded resource.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6e6e8-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6e6e8-104">Example</span></span>  
 [!code-csharp[System.Windows.Forms.Sound#10](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Sound/CS/soundtestform.cs#10)]
 [!code-vb[System.Windows.Forms.Sound#10](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Sound/VB/soundtestform.vb#10)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6e6e8-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="6e6e8-105">Compiling the Code</span></span>  
 <span data-ttu-id="6e6e8-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="6e6e8-106">This example requires:</span></span>  
  
 <span data-ttu-id="6e6e8-107">L’importation du <xref:System.Media?displayProperty=nameWithType> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-107">Importing the <xref:System.Media?displayProperty=nameWithType> namespace.</span></span>  
  
 <span data-ttu-id="6e6e8-108">L’inclusion du fichier audio en tant que ressource incorporée dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-108">Including the sound file as an embedded resource in your project.</span></span>  
  
 <span data-ttu-id="6e6e8-109">Le remplacement de « \<AssemblyName » par le nom de l’assembly dans lequel le fichier audio est incorporé.</span><span class="sxs-lookup"><span data-stu-id="6e6e8-109">Replacing "\<AssemblyName>" with the name of the assembly in which the sound file is embedded.</span></span> <span data-ttu-id="6e6e8-110">N’incluez pas le suffixe « .dll ».</span><span class="sxs-lookup"><span data-stu-id="6e6e8-110">Do not include the ".dll" suffix.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e6e8-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e6e8-111">See Also</span></span>  
 <xref:System.Media.SoundPlayer>  
 [<span data-ttu-id="6e6e8-112">Guide pratique pour lire un son à partir d’un Windows Form</span><span class="sxs-lookup"><span data-stu-id="6e6e8-112">How to: Play a Sound from a Windows Form</span></span>](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)  
 [<span data-ttu-id="6e6e8-113">Guide pratique pour mettre en boucle l’émission d’un son dans un Windows Form</span><span class="sxs-lookup"><span data-stu-id="6e6e8-113">How to: Loop a Sound Playing on a Windows Form</span></span>](../../../../docs/framework/winforms/controls/how-to-loop-a-sound-playing-on-a-windows-form.md)
