---
title: 'Procédure : charger un son de façon asynchrone dans un formulaire Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SoundPlayer class [Windows Forms], loading sounds asynchronously
- sounds [Windows Forms], loading on separate threads
- threading [Windows Forms], sounds
ms.assetid: 3b6a9296-1d5e-4d52-a4ba-94366d6fe302
ms.openlocfilehash: 5f533d82fcca07a2b64bdbbfb160a7b2a23ce540
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592379"
---
# <a name="how-to-load-a-sound-asynchronously-within-a-windows-form"></a><span data-ttu-id="fad5d-102">Procédure : charger un son de façon asynchrone dans un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="fad5d-102">How to: Load a Sound Asynchronously within a Windows Form</span></span>
<span data-ttu-id="fad5d-103">L'exemple de code suivant charge un son de façon asynchrone à partir d'une URL et le lit sur un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="fad5d-103">The following code example asynchronously loads a sound from an URL and then plays it on a new thread.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fad5d-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="fad5d-104">Example</span></span>  
 [!code-csharp[System.Media.SoundPlayer.LoadAsync#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.LoadAsync#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fad5d-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="fad5d-105">Compiling the Code</span></span>  
 <span data-ttu-id="fad5d-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="fad5d-106">This example requires:</span></span>  
  
- <span data-ttu-id="fad5d-107">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="fad5d-107">References to the System and System.Windows.Forms assemblies.</span></span>  
  
- <span data-ttu-id="fad5d-108">que vous remplaciez le nom de fichier `"http://www.tailspintoys.com/sounds/stop.wav"` par un nom de fichier valide.</span><span class="sxs-lookup"><span data-stu-id="fad5d-108">That you replace the file name `"http://www.tailspintoys.com/sounds/stop.wav"` with a valid file name.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="fad5d-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="fad5d-109">Robust Programming</span></span>  
 <span data-ttu-id="fad5d-110">Les opérations de fichiers doivent être placées dans des blocs de gestion des exceptions appropriés.</span><span class="sxs-lookup"><span data-stu-id="fad5d-110">File operations should be enclosed within appropriate exception-handling blocks.</span></span>  
  
 <span data-ttu-id="fad5d-111">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="fad5d-111">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="fad5d-112">Le chemin d'accès est mal formé.</span><span class="sxs-lookup"><span data-stu-id="fad5d-112">The path name is malformed.</span></span> <span data-ttu-id="fad5d-113">Par exemple, il contient des caractères qui ne sont pas valides ou est constitué uniquement d'espaces blancs (classe <xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="fad5d-113">For example, it contains characters that are not valid or is only white space (<xref:System.ArgumentException> class).</span></span>  
  
- <span data-ttu-id="fad5d-114">Le chemin d'accès est en lecture seule (classe <xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="fad5d-114">The path is read-only (<xref:System.IO.IOException> class).</span></span>  
  
- <span data-ttu-id="fad5d-115">Le nom du chemin d'accès est `Nothing` (classe <xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="fad5d-115">The path name is `Nothing` (<xref:System.ArgumentNullException> class).</span></span>  
  
- <span data-ttu-id="fad5d-116">Le nom de chemin d'accès est trop long (classe <xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="fad5d-116">The path name is too long (<xref:System.IO.PathTooLongException> class).</span></span>  
  
- <span data-ttu-id="fad5d-117">Le chemin d'accès n'est pas valide (classe <xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="fad5d-117">The path is not valid (<xref:System.IO.DirectoryNotFoundException> class).</span></span>  
  
- <span data-ttu-id="fad5d-118">Le chemin d’accès n’est constitué que d’un signe deux-points « : » (classe <xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="fad5d-118">The path is only a colon ":" (<xref:System.NotSupportedException> class).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="fad5d-119">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="fad5d-119">.NET Framework Security</span></span>  
 <span data-ttu-id="fad5d-120">Ne vous basez pas sur le nom d'un fichier pour en déterminer le contenu.</span><span class="sxs-lookup"><span data-stu-id="fad5d-120">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="fad5d-121">Par exemple, le fichier `Form1.vb` peut ne pas être un fichier source Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fad5d-121">For example, the file `Form1.vb` may not be a Visual Basic source file.</span></span> <span data-ttu-id="fad5d-122">Vérifiez toutes les entrées avant d'utiliser les données dans votre application.</span><span class="sxs-lookup"><span data-stu-id="fad5d-122">Verify all inputs before using the data in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fad5d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fad5d-123">See also</span></span>

- <xref:System.Media.SoundPlayer.LoadAsync%2A>
- <xref:System.Media.SoundPlayer.LoadCompleted>
- <xref:System.Media.SoundPlayer.Play%2A>
- [<span data-ttu-id="fad5d-124">Guide pratique pour Un signal sonore à partir d’un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="fad5d-124">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
