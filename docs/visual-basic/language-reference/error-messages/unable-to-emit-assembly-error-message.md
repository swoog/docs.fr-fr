---
title: "Impossible de créer l'assembly : <error message>"
ms.date: 08/14/2018
f1_keywords:
- vbc30145
- bc30145
helpviewer_keywords:
- BC30145
ms.assetid: 2e7eb2b9-eda6-4bdb-95cc-72c7f0be7528
ms.openlocfilehash: 404a8255adcdc414a40b40395ada1c90c1078325
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42754084"
---
# <a name="unable-to-emit-assembly-error-message"></a><span data-ttu-id="95315-102">Impossible de créer l’assembly : \<message d’erreur ></span><span class="sxs-lookup"><span data-stu-id="95315-102">Unable to emit assembly: \<error message></span></span>

<span data-ttu-id="95315-103">Le compilateur Visual Basic appelle l’utilitaire Assembly Linker (*Al.exe*, également appelé Alink) pour générer un assembly avec un manifeste et l’éditeur de liens signale une erreur dans la phase d’émission de création de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="95315-103">The Visual Basic compiler calls the Assembly Linker (*Al.exe*, also known as Alink) to generate an assembly with a manifest, and the linker reports an error in the emission stage of creating the assembly.</span></span>

<span data-ttu-id="95315-104">**ID d’erreur :** BC30145</span><span class="sxs-lookup"><span data-stu-id="95315-104">**Error ID:** BC30145</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="95315-105">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="95315-105">To correct this error</span></span>

1. <span data-ttu-id="95315-106">Examinez le message d’erreur cité et consultez la rubrique [Al.exe](../../../framework/tools/al-exe-assembly-linker.md) pour obtenir davantage d’explications et de conseils.</span><span class="sxs-lookup"><span data-stu-id="95315-106">Examine the quoted error message and consult the topic [Al.exe](../../../framework/tools/al-exe-assembly-linker.md) for further explanation and advice.</span></span>

2. <span data-ttu-id="95315-107">Essayez de signer l’assembly manuellement, à l’aide la [Al.exe](../../../framework/tools/al-exe-assembly-linker.md) ou [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md).</span><span class="sxs-lookup"><span data-stu-id="95315-107">Try signing the assembly manually, using either the [Al.exe](../../../framework/tools/al-exe-assembly-linker.md) or the [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md).</span></span>

3. <span data-ttu-id="95315-108">Si l'erreur persiste, rassemblez des informations sur ses circonstances et avertissez les services de support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="95315-108">If the error persists, gather information about the circumstances and notify Microsoft Product Support Services.</span></span>

### <a name="to-sign-the-assembly-manually"></a><span data-ttu-id="95315-109">Pour signer manuellement l'assembly</span><span class="sxs-lookup"><span data-stu-id="95315-109">To sign the assembly manually</span></span>

1. <span data-ttu-id="95315-110">Utiliser le [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)) pour créer un fichier de paire de clés publique/privée.</span><span class="sxs-lookup"><span data-stu-id="95315-110">Use the [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md)) to create a public/private key pair file.</span></span>

   <span data-ttu-id="95315-111">Ce fichier a une *.snk* extension.</span><span class="sxs-lookup"><span data-stu-id="95315-111">This file has an *.snk* extension.</span></span>

2. <span data-ttu-id="95315-112">Supprimez la référence COM qui génère l'erreur de votre projet.</span><span class="sxs-lookup"><span data-stu-id="95315-112">Delete the COM reference that is generating the error from your project.</span></span>

3. <span data-ttu-id="95315-113">Ouvrez le [invite de commandes développeur pour Visual Studio](../../../framework/tools/developer-command-prompt-for-vs.md).</span><span class="sxs-lookup"><span data-stu-id="95315-113">Open the [Developer Command Prompt for Visual Studio](../../../framework/tools/developer-command-prompt-for-vs.md).</span></span>

   <span data-ttu-id="95315-114">Dans Windows 10, entrez **invite de commandes développeur** dans la zone de recherche sur la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="95315-114">In Windows 10, enter **Developer command prompt** into the search box on the task bar.</span></span> <span data-ttu-id="95315-115">Ensuite, sélectionnez **invite de commandes développeur pour VS 2017** à partir de la liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="95315-115">Then, select **Developer Command Prompt for VS 2017** from the results list.</span></span>

4. <span data-ttu-id="95315-116">Accédez au répertoire dans le répertoire où vous souhaitez placer le wrapper d’assembly.</span><span class="sxs-lookup"><span data-stu-id="95315-116">Change the directory to the directory where you want to place your assembly wrapper.</span></span>

5. <span data-ttu-id="95315-117">Entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="95315-117">Enter the following command:</span></span>

    ```cmd
    tlbimp <path to COM reference file> /out:<output assembly name> /keyfile:<path to .snk file>
    ```

   <span data-ttu-id="95315-118">Est un exemple de la commande réelle, que vous pouvez entrer :</span><span class="sxs-lookup"><span data-stu-id="95315-118">An example of the actual command you might enter is:</span></span>

    ```cmd
    tlbimp c:\windows\system32\msi.dll /out:Interop.WindowsInstaller.dll /keyfile:"c:\documents and settings\mykey.snk"
    ```

   > [!TIP]
   > <span data-ttu-id="95315-119">Utilisez des guillemets si un fichier ou un chemin d’accès contient des espaces.</span><span class="sxs-lookup"><span data-stu-id="95315-119">Use double quotation marks if a path or file contains spaces.</span></span>

6. <span data-ttu-id="95315-120">Dans Visual Studio, ajoutez une référence d’Assembly .NET au fichier que vous venez de créer.</span><span class="sxs-lookup"><span data-stu-id="95315-120">In Visual Studio, add a .NET Assembly reference to the file you just created.</span></span>

## <a name="see-also"></a><span data-ttu-id="95315-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95315-121">See also</span></span>

- <span data-ttu-id="95315-122">[Al.exe](../../../framework/tools/al-exe-assembly-linker.md).</span><span class="sxs-lookup"><span data-stu-id="95315-122">[Al.exe](../../../framework/tools/al-exe-assembly-linker.md).</span></span>
- <span data-ttu-id="95315-123">[Sn.exe (Strong Name Tool)] [Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md))</span><span class="sxs-lookup"><span data-stu-id="95315-123">[Sn.exe (Strong Name Tool)][Sn.exe (Strong Name Tool)](../../../framework/tools/sn-exe-strong-name-tool.md))</span></span>
- [<span data-ttu-id="95315-124">Guide pratique pour créer une paire de clés publique/privée</span><span class="sxs-lookup"><span data-stu-id="95315-124">How to: Create a Public-Private Key Pair</span></span>](../../../framework/app-domains/how-to-create-a-public-private-key-pair.md)
- [<span data-ttu-id="95315-125">Nous contacter</span><span class="sxs-lookup"><span data-stu-id="95315-125">Talk to Us</span></span>](/visualstudio/ide/talk-to-us)