---
title: Guide pratique pour charger un son de façon asynchrone dans un Windows Form
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- SoundPlayer class [Windows Forms], loading sounds asynchronously
- sounds [Windows Forms], loading on separate threads
- threading [Windows Forms], sounds
ms.assetid: 3b6a9296-1d5e-4d52-a4ba-94366d6fe302
ms.openlocfilehash: 9ebede03a3a9d2cc6db1cda2537bcaf30afcb2d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33533567"
---
# <a name="how-to-load-a-sound-asynchronously-within-a-windows-form"></a><span data-ttu-id="0c1c1-102">Guide pratique pour charger un son de façon asynchrone dans un Windows Form</span><span class="sxs-lookup"><span data-stu-id="0c1c1-102">How to: Load a Sound Asynchronously within a Windows Form</span></span>
<span data-ttu-id="0c1c1-103">L'exemple de code suivant charge un son de façon asynchrone à partir d'une URL et le lit sur un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-103">The following code example asynchronously loads a sound from an URL and then plays it on a new thread.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c1c1-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0c1c1-104">Example</span></span>  
 [!code-csharp[System.Media.SoundPlayer.LoadAsync#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.LoadAsync#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.LoadAsync/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0c1c1-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="0c1c1-105">Compiling the Code</span></span>  
 <span data-ttu-id="0c1c1-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="0c1c1-106">This example requires:</span></span>  
  
-   <span data-ttu-id="0c1c1-107">des références aux assemblys System et System.Windows.Forms ;</span><span class="sxs-lookup"><span data-stu-id="0c1c1-107">References to the System and System.Windows.Forms assemblies.</span></span>  
  
-   <span data-ttu-id="0c1c1-108">que vous remplaciez le nom de fichier `"http://www.tailspintoys.com/sounds/stop.wav"` par un nom de fichier valide.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-108">That you replace the file name `"http://www.tailspintoys.com/sounds/stop.wav"` with a valid file name.</span></span>  
  
 <span data-ttu-id="0c1c1-109">Pour plus d’informations sur la création de cet exemple à partir de la ligne de commande pour Visual Basic ou Visual c#, consultez [génération à partir de la ligne de commande](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) ou [de ligne de commande avec csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-109">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="0c1c1-110">Vous pouvez également générer cet exemple dans Visual Studio en collant le code dans un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="0c1c1-111">Consultez également la page [Comment : compiler et exécuter un exemple complet de code Windows Forms à l’aide de Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="0c1c1-112">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="0c1c1-112">Robust Programming</span></span>  
 <span data-ttu-id="0c1c1-113">Les opérations de fichiers doivent être placées dans des blocs de gestion des exceptions appropriés.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-113">File operations should be enclosed within appropriate exception-handling blocks.</span></span>  
  
 <span data-ttu-id="0c1c1-114">Les conditions ci-dessous peuvent générer une exception.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-114">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="0c1c1-115">Le chemin d'accès est mal formé.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-115">The path name is malformed.</span></span> <span data-ttu-id="0c1c1-116">Par exemple, il contient des caractères qui ne sont pas valides ou est constitué uniquement d'espaces blancs (classe <xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-116">For example, it contains characters that are not valid or is only white space (<xref:System.ArgumentException> class).</span></span>  
  
-   <span data-ttu-id="0c1c1-117">Le chemin d'accès est en lecture seule (classe <xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-117">The path is read-only (<xref:System.IO.IOException> class).</span></span>  
  
-   <span data-ttu-id="0c1c1-118">Le nom du chemin d'accès est `Nothing` (classe <xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-118">The path name is `Nothing` (<xref:System.ArgumentNullException> class).</span></span>  
  
-   <span data-ttu-id="0c1c1-119">Le nom de chemin d'accès est trop long (classe <xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-119">The path name is too long (<xref:System.IO.PathTooLongException> class).</span></span>  
  
-   <span data-ttu-id="0c1c1-120">Le chemin d'accès n'est pas valide (classe <xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-120">The path is not valid (<xref:System.IO.DirectoryNotFoundException> class).</span></span>  
  
-   <span data-ttu-id="0c1c1-121">Le chemin d'accès n'est constitué que d'un signe deux-points (":") (classe <xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="0c1c1-121">The path is only a colon ":" (<xref:System.NotSupportedException> class).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="0c1c1-122">Sécurité .NET Framework</span><span class="sxs-lookup"><span data-stu-id="0c1c1-122">.NET Framework Security</span></span>  
 <span data-ttu-id="0c1c1-123">Ne vous basez pas sur le nom d'un fichier pour en déterminer le contenu.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-123">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="0c1c1-124">Par exemple, le fichier `Form1.vb` peut ne pas être un fichier source Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-124">For example, the file `Form1.vb` may not be a Visual Basic source file.</span></span> <span data-ttu-id="0c1c1-125">Vérifiez toutes les entrées avant d'utiliser les données dans votre application.</span><span class="sxs-lookup"><span data-stu-id="0c1c1-125">Verify all inputs before using the data in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c1c1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c1c1-126">See Also</span></span>  
 <xref:System.Media.SoundPlayer.LoadAsync%2A>  
 <xref:System.Media.SoundPlayer.LoadCompleted>  
 <xref:System.Media.SoundPlayer.Play%2A>  
 [<span data-ttu-id="0c1c1-127">Guide pratique pour lire un son à partir d’un Windows Form</span><span class="sxs-lookup"><span data-stu-id="0c1c1-127">How to: Play a Sound from a Windows Form</span></span>](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
