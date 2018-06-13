---
title: 'Impossible de créer l’assembly : &lt;message d’erreur&gt;'
ms.date: 07/20/2015
f1_keywords:
- vbc30145
- bc30145
helpviewer_keywords:
- BC30145
ms.assetid: 2e7eb2b9-eda6-4bdb-95cc-72c7f0be7528
ms.openlocfilehash: 8f497069088ad30a3be58d02caa0a32f7f1b21b7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33595171"
---
# <a name="unable-to-emit-assembly-lterror-messagegt"></a><span data-ttu-id="1f500-102">Impossible de créer l’assembly : &lt;message d’erreur&gt;</span><span class="sxs-lookup"><span data-stu-id="1f500-102">Unable to emit assembly: &lt;error message&gt;</span></span>
<span data-ttu-id="1f500-103">Le compilateur Visual Basic appelle Assembly Linker (Al.exe, également appelé Alink) pour générer un assembly avec un manifeste, avec l’éditeur de liens signale une erreur lors de l’étape d’émission de création de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="1f500-103">The Visual Basic compiler calls the Assembly Linker (Al.exe, also known as Alink) to generate an assembly with a manifest, with the linker reporting an error in the emission stage of creating the assembly.</span></span>  
  
 <span data-ttu-id="1f500-104">**ID d’erreur :** BC30145</span><span class="sxs-lookup"><span data-stu-id="1f500-104">**Error ID:** BC30145</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="1f500-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="1f500-105">To correct this error</span></span>  
  
1.  <span data-ttu-id="1f500-106">Examinez le message d’erreur entre guillemets et consultez la rubrique [Al.exe](../../../framework/tools/al-exe-assembly-linker.md).</span><span class="sxs-lookup"><span data-stu-id="1f500-106">Examine the quoted error message and consult the topic [Al.exe](../../../framework/tools/al-exe-assembly-linker.md).</span></span> <span data-ttu-id="1f500-107">Pour obtenir davantage d’explications et de conseils.</span><span class="sxs-lookup"><span data-stu-id="1f500-107">for further explanation and advice.</span></span>  
  
2.  <span data-ttu-id="1f500-108">Essayez de signer l’assembly manuellement, soit à l’aide de la [Al.exe](../../../framework/tools/al-exe-assembly-linker.md) ou le [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md).</span><span class="sxs-lookup"><span data-stu-id="1f500-108">Try signing the assembly manually, using either the [Al.exe](../../../framework/tools/al-exe-assembly-linker.md) or the [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md).</span></span>  
  
3.  <span data-ttu-id="1f500-109">Si l'erreur persiste, rassemblez des informations sur ses circonstances et avertissez les services de support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f500-109">If the error persists, gather information about the circumstances and notify Microsoft Product Support Services.</span></span>  
  
### <a name="to-sign-the-assembly-manually"></a><span data-ttu-id="1f500-110">Pour signer manuellement l'assembly</span><span class="sxs-lookup"><span data-stu-id="1f500-110">To sign the assembly manually</span></span>  
  
1.  <span data-ttu-id="1f500-111">Utilisez le [Sn.exe (outil Strong Name)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)) pour créer un fichier de paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="1f500-111">Use the [Sn.exe (Strong Name Tool)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)) to create a public/private key pair file.</span></span>  
  
     <span data-ttu-id="1f500-112">Ce fichier porte l’extension .snk.</span><span class="sxs-lookup"><span data-stu-id="1f500-112">This file has a .snk extension.</span></span>  
  
2.  <span data-ttu-id="1f500-113">Supprimez la référence COM qui génère l'erreur de votre projet.</span><span class="sxs-lookup"><span data-stu-id="1f500-113">Delete the COM reference that is generating the error from your project.</span></span>  
  
3.  <span data-ttu-id="1f500-114">À partir des fenêtres **Démarrer** menu, pointez sur **programmes**, pointez sur **Microsoft Visual Studio 2008**, pointez sur **Visual Studio Tools**, et puis cliquez sur **invite de commandes de Visual Studio 2008**.</span><span class="sxs-lookup"><span data-stu-id="1f500-114">From the Windows **Start** menu, point to **Programs**, point to **Microsoft Visual Studio 2008**, point to **Visual Studio Tools**, and then click **Visual Studio 2008 Command Prompt**.</span></span>  
  
4.  <span data-ttu-id="1f500-115">Accédez au répertoire dans lequel vous voulez placer le wrapper d'assembly.</span><span class="sxs-lookup"><span data-stu-id="1f500-115">Move to the directory where you want to place your assembly wrapper.</span></span>  
  
5.  <span data-ttu-id="1f500-116">Tapez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1f500-116">Type the following code.</span></span>  
  
    ```  
    tlbimp <path to COM reference file> /out:<output assembly name> /keyfile:<path to .snk file>  
    ```  
  
     <span data-ttu-id="1f500-117">Voici un exemple du code que vous pouvez entrer.</span><span class="sxs-lookup"><span data-stu-id="1f500-117">An example of the code you might enter would be the following.</span></span>  
  
    ```  
    tlbimp c:\windows\system32\msi.dll /out:Interop.WindowsInstaller.dll /keyfile:"c:\documents and settings\mykey.snk"  
    ```  
  
     <span data-ttu-id="1f500-118">Utilisez des guillemets doubles (") si un chemin ou un fichier contient des espaces.</span><span class="sxs-lookup"><span data-stu-id="1f500-118">Use double quotation marks (") if a path or file contains spaces.</span></span>  
  
6.  <span data-ttu-id="1f500-119">Dans Visual Studio, ajoutez une référence d’Assembly .NET au fichier que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="1f500-119">In Visual Studio, add a .NET Assembly reference to the file you just created.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1f500-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f500-120">See Also</span></span>  
 
 <span data-ttu-id="1f500-121">[Al.exe](../../../framework/tools/al-exe-assembly-linker.md).</span><span class="sxs-lookup"><span data-stu-id="1f500-121">[Al.exe](../../../framework/tools/al-exe-assembly-linker.md).</span></span>  
 <span data-ttu-id="1f500-122">[Sn.exe (outil Strong Name)] [Sn.exe (outil Strong Name)](../../../framework/tools/sn-exe-strong-name-tool.md))</span><span class="sxs-lookup"><span data-stu-id="1f500-122">[Sn.exe (Strong Name Tool)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md))</span></span>  
 [<span data-ttu-id="1f500-123">Guide pratique pour créer une paire de clés publique/privée</span><span class="sxs-lookup"><span data-stu-id="1f500-123">How to: Create a Public-Private Key Pair</span></span>](../../../framework/app-domains/how-to-create-a-public-private-key-pair.md)  
 [<span data-ttu-id="1f500-124">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="1f500-124">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)
