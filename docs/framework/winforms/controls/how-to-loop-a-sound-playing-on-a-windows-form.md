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
ms.openlocfilehash: a74acbbbcb5646a35de54a6000a0feae30f145a5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59188511"
---
# <a name="how-to-loop-a-sound-playing-on-a-windows-form"></a><span data-ttu-id="4c64d-102">Procédure : émettre un son en boucle dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="4c64d-102">How to: Loop a Sound Playing on a Windows Form</span></span>
<span data-ttu-id="4c64d-103">L'exemple de code suivant joue un son de manière répétitive.</span><span class="sxs-lookup"><span data-stu-id="4c64d-103">The following code example plays a sound repeatedly.</span></span> <span data-ttu-id="4c64d-104">Quand le code du gestionnaire d'événements `stopPlayingButton_Click` est exécuté, le son s'arrête.</span><span class="sxs-lookup"><span data-stu-id="4c64d-104">When the code in the `stopPlayingButton_Click` event handler runs, any sound currently playing stops.</span></span> <span data-ttu-id="4c64d-105">Si aucun son n'est joué, rien ne se produit.</span><span class="sxs-lookup"><span data-stu-id="4c64d-105">If no sound is playing, nothing happens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4c64d-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="4c64d-106">Example</span></span>  
 [!code-csharp[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4c64d-107">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="4c64d-107">Compiling the Code</span></span>  
 <span data-ttu-id="4c64d-108">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="4c64d-108">This example requires:</span></span>  
  
-   <span data-ttu-id="4c64d-109">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="4c64d-109">References to the System and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="4c64d-110">que vous remplaciez le nom de fichier `"c:\Windows\Media\chimes.wav"` par un nom de fichier valide.</span><span class="sxs-lookup"><span data-stu-id="4c64d-110">That you replace the file name `"c:\Windows\Media\chimes.wav"` with a valid file name.</span></span>  
  
 <span data-ttu-id="4c64d-111">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="4c64d-111">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](../../../visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](../../../csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="4c64d-112">Vous pouvez également créer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="4c64d-112">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="4c64d-113">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="4c64d-113">Robust Programming</span></span>  
 <span data-ttu-id="4c64d-114">Les opérations de fichiers doivent être placées dans des blocs de gestion des exceptions appropriés.</span><span class="sxs-lookup"><span data-stu-id="4c64d-114">File operations should be enclosed within appropriate exception-handling blocks.</span></span>  
  
 <span data-ttu-id="4c64d-115">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="4c64d-115">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="4c64d-116">Le chemin d'accès est mal formé.</span><span class="sxs-lookup"><span data-stu-id="4c64d-116">The path name is malformed.</span></span> <span data-ttu-id="4c64d-117">Par exemple, il contient des caractères qui ne sont pas valides ou est constitué uniquement d'espaces blancs (classe <xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="4c64d-117">For example, it contains characters that are not valid or it is only white space (<xref:System.ArgumentException> class).</span></span>  
  
-   <span data-ttu-id="4c64d-118">Le chemin d'accès est en lecture seule (classe <xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="4c64d-118">The path is read-only (<xref:System.IO.IOException> class).</span></span>  
  
-   <span data-ttu-id="4c64d-119">Le nom du chemin d'accès est `Nothing` (classe <xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="4c64d-119">The path name is `Nothing` (<xref:System.ArgumentNullException> class).</span></span>  
  
-   <span data-ttu-id="4c64d-120">Le nom du chemin d'accès est trop long (classe <xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="4c64d-120">The path name is too long (<xref:System.IO.PathTooLongException> class).</span></span>  
  
-   <span data-ttu-id="4c64d-121">Le chemin d'accès n'est pas valide (classe <xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="4c64d-121">The path is invalid (<xref:System.IO.DirectoryNotFoundException> class).</span></span>  
  
-   <span data-ttu-id="4c64d-122">Le chemin d’accès n’est constitué que d’un signe deux-points « : » (classe <xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="4c64d-122">The path is only a colon ":" (<xref:System.NotSupportedException> class).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="4c64d-123">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4c64d-123">.NET Framework Security</span></span>  
 <span data-ttu-id="4c64d-124">Ne vous basez pas sur le nom d'un fichier pour en déterminer le contenu.</span><span class="sxs-lookup"><span data-stu-id="4c64d-124">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="4c64d-125">Par exemple, le fichier Form1.vb peut ne pas être un fichier source Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4c64d-125">For example, the file Form1.vb may not be a Visual Basic source file.</span></span> <span data-ttu-id="4c64d-126">Vérifiez toutes les entrées avant d'utiliser les données dans votre application.</span><span class="sxs-lookup"><span data-stu-id="4c64d-126">Verify all inputs before using the data in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c64d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c64d-127">See also</span></span>

- <xref:System.Media.SoundPlayer.PlayLooping%2A>
- [<span data-ttu-id="4c64d-128">Guide pratique pour Un signal sonore à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="4c64d-128">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
- [<span data-ttu-id="4c64d-129">Vue d’ensemble de la classe SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="4c64d-129">SoundPlayer Class Overview</span></span>](soundplayer-class-overview.md)
