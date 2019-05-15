---
title: 'Procédure : émettre un son en boucle dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sound loops
- SoundPlayer class [Windows Forms], play looping
- sounds [Windows Forms], looping
- playing sounds [Windows Forms], looping
ms.assetid: ea95dd46-10a3-46c0-8263-4b205f00df7f
ms.openlocfilehash: e14d9de2326234b86c1f24b227e86f822fbfdb71
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592357"
---
# <a name="how-to-loop-a-sound-playing-on-a-windows-form"></a><span data-ttu-id="4ebe6-102">Procédure : émettre un son en boucle dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="4ebe6-102">How to: Loop a Sound Playing on a Windows Form</span></span>
<span data-ttu-id="4ebe6-103">L'exemple de code suivant joue un son de manière répétitive.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-103">The following code example plays a sound repeatedly.</span></span> <span data-ttu-id="4ebe6-104">Quand le code du gestionnaire d'événements `stopPlayingButton_Click` est exécuté, le son s'arrête.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-104">When the code in the `stopPlayingButton_Click` event handler runs, any sound currently playing stops.</span></span> <span data-ttu-id="4ebe6-105">Si aucun son n'est joué, rien ne se produit.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-105">If no sound is playing, nothing happens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4ebe6-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4ebe6-106">Example</span></span>  
 [!code-csharp[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4ebe6-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="4ebe6-107">Compiling the Code</span></span>  
 <span data-ttu-id="4ebe6-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="4ebe6-108">This example requires:</span></span>  
  
- <span data-ttu-id="4ebe6-109">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="4ebe6-109">References to the System and System.Windows.Forms assemblies.</span></span>  
  
- <span data-ttu-id="4ebe6-110">que vous remplaciez le nom de fichier `"c:\Windows\Media\chimes.wav"` par un nom de fichier valide.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-110">That you replace the file name `"c:\Windows\Media\chimes.wav"` with a valid file name.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="4ebe6-111">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="4ebe6-111">Robust Programming</span></span>  
 <span data-ttu-id="4ebe6-112">Les opérations de fichiers doivent être placées dans des blocs de gestion des exceptions appropriés.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-112">File operations should be enclosed within appropriate exception-handling blocks.</span></span>  
  
 <span data-ttu-id="4ebe6-113">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-113">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="4ebe6-114">Le chemin d'accès est mal formé.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-114">The path name is malformed.</span></span> <span data-ttu-id="4ebe6-115">Par exemple, il contient des caractères qui ne sont pas valides ou est constitué uniquement d'espaces blancs (classe <xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="4ebe6-115">For example, it contains characters that are not valid or it is only white space (<xref:System.ArgumentException> class).</span></span>  
  
- <span data-ttu-id="4ebe6-116">Le chemin d'accès est en lecture seule (classe <xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="4ebe6-116">The path is read-only (<xref:System.IO.IOException> class).</span></span>  
  
- <span data-ttu-id="4ebe6-117">Le nom du chemin d'accès est `Nothing` (classe <xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="4ebe6-117">The path name is `Nothing` (<xref:System.ArgumentNullException> class).</span></span>  
  
- <span data-ttu-id="4ebe6-118">Le nom du chemin d'accès est trop long (classe <xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="4ebe6-118">The path name is too long (<xref:System.IO.PathTooLongException> class).</span></span>  
  
- <span data-ttu-id="4ebe6-119">Le chemin d'accès n'est pas valide (classe <xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="4ebe6-119">The path is invalid (<xref:System.IO.DirectoryNotFoundException> class).</span></span>  
  
- <span data-ttu-id="4ebe6-120">Le chemin d’accès n’est constitué que d’un signe deux-points « : » (classe <xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="4ebe6-120">The path is only a colon ":" (<xref:System.NotSupportedException> class).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="4ebe6-121">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4ebe6-121">.NET Framework Security</span></span>  
 <span data-ttu-id="4ebe6-122">Ne vous basez pas sur le nom d'un fichier pour en déterminer le contenu.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-122">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="4ebe6-123">Par exemple, le fichier Form1.vb peut ne pas être un fichier source Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-123">For example, the file Form1.vb may not be a Visual Basic source file.</span></span> <span data-ttu-id="4ebe6-124">Vérifiez toutes les entrées avant d'utiliser les données dans votre application.</span><span class="sxs-lookup"><span data-stu-id="4ebe6-124">Verify all inputs before using the data in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ebe6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ebe6-125">See also</span></span>

- <xref:System.Media.SoundPlayer.PlayLooping%2A>
- [<span data-ttu-id="4ebe6-126">Guide pratique pour Un signal sonore à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="4ebe6-126">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
- [<span data-ttu-id="4ebe6-127">Vue d’ensemble de la classe SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="4ebe6-127">SoundPlayer Class Overview</span></span>](soundplayer-class-overview.md)
