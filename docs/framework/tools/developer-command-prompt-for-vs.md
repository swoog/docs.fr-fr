---
title: Invite de commandes développeur pour Visual Studio
ms.date: 08/14/2018
helpviewer_keywords:
- command prompt, Windows SDK
- Visual Studio command prompt
- command prompt, Visual Studio
- SDK command prompt
- tools [.NET Framework], setting environment variables
- environment variables, setting for tools
- developer command prompt
ms.assetid: 94fcf524-9045-4993-bfb2-e2d8bad44219
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6e648cdadb567919d320ea8a12d30b7be306e67a
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54221230"
---
# <a name="developer-command-prompt-for-visual-studio"></a><span data-ttu-id="e8bf1-102">Invite de commandes développeur pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bf1-102">Developer Command Prompt for Visual Studio</span></span>

<span data-ttu-id="e8bf1-103">L’invite de commandes développeur pour Visual Studio vous permet d’utiliser plus facilement les outils .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-103">The Developer Command Prompt for Visual Studio enables you to use .NET Framework tools more easily.</span></span> <span data-ttu-id="e8bf1-104">Il s’agit d’une invite de commandes qui définit automatiquement les variables d’environnement spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-104">It is a command prompt that automatically sets specific environment variables.</span></span>

> [!div class="button"]
> [<span data-ttu-id="e8bf1-105">Télécharger Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bf1-105">Download Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017)

## <a name="search-for-the-command-prompt-on-your-machine"></a><span data-ttu-id="e8bf1-106">Rechercher l’invite de commandes sur votre ordinateur</span><span class="sxs-lookup"><span data-stu-id="e8bf1-106">Search for the command prompt on your machine</span></span>

<span data-ttu-id="e8bf1-107">Vous pouvez avoir plusieurs invites de commandes, en fonction de la version de Visual Studio et des SDK que vous avez installés.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-107">You may have multiple command prompts, depending on the version of Visual Studio and any additional SDKs you've installed.</span></span> <span data-ttu-id="e8bf1-108">Par exemple, les versions 64 bits de Visual Studio fournissent à la fois des invites de commandes 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-108">For example, 64-bit versions of Visual Studio provide both 32-bit and 64-bit command prompts.</span></span> <span data-ttu-id="e8bf1-109">(Les versions 32 bits et 64 bits de la plupart des outils sont identiques ; toutefois, certains outils apportent des modifications propres aux environnements 32 bits et 64 bits.) Si les étapes suivantes ne fonctionnent pas, vous pouvez essayer de [rechercher manuellement les fichiers sur votre ordinateur](#manually-locate-the-files-on-your-machine) ou de [lancer l’invite de commandes à partir de Visual Studio](#run-the-command-prompt-from-inside-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="e8bf1-109">(The 32-bit and 64-bit versions of most tools are the same; however, a few tools make changes specific to 32-bit and 64-bit environments.) If the following steps don't work, you can try [Manually locate the files on your machine](#manually-locate-the-files-on-your-machine) or [Run the command prompt from inside Visual Studio](#run-the-command-prompt-from-inside-visual-studio).</span></span>

### <a name="in-windows-10"></a><span data-ttu-id="e8bf1-110">Dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="e8bf1-110">In Windows 10</span></span>

1. <span data-ttu-id="e8bf1-111">Dans la zone de recherche dans la barre des tâches, commencez à taper le nom de l’outil, tel que `dev` ou `developer command prompt`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-111">In the search box on the taskbar, start typing the name of the tool, such as `dev` or `developer command prompt`.</span></span> <span data-ttu-id="e8bf1-112">S’affiche alors une liste des applications installées qui correspondent à votre modèle de recherche.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-112">This brings up a list of installed apps that match your search pattern.</span></span> <span data-ttu-id="e8bf1-113">Si vous recherchez une autre invite de commandes, essayez d’entrer un autre terme de recherche, par exemple `prompt`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-113">If you're looking for a different command prompt, try entering a different search term such as `prompt`.</span></span>

2. <span data-ttu-id="e8bf1-114">Choisissez **Invite de commandes développeur pour Visual Studio** (ou l’invite de commandes que vous voulez utiliser).</span><span class="sxs-lookup"><span data-stu-id="e8bf1-114">Choose the **Developer Command Prompt for Visual Studio** (or the command prompt you want to use).</span></span>

### <a name="in-windows-81"></a><span data-ttu-id="e8bf1-115">Dans Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e8bf1-115">In Windows 8.1</span></span>

1. <span data-ttu-id="e8bf1-116">Accédez à l’écran **Démarrer**, par exemple en appuyant sur la touche du logo Windows ![Logo Windows](../get-started/media/windowskeyboardlogo.png "Windowskeyboardlogo") de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-116">Go to the **Start** screen, by pressing the Windows logo key ![Windows logo](../get-started/media/windowskeyboardlogo.png "Windowskeyboardlogo") on your keyboard for example.</span></span>

2. <span data-ttu-id="e8bf1-117">Dans l’écran **Démarrer**, appuyez sur **Ctrl**+**Tab** pour ouvrir la liste **Applications**, puis entrez `V`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-117">On the **Start** screen, press **Ctrl**+**Tab** to open the **Apps** list, and then enter `V`.</span></span> <span data-ttu-id="e8bf1-118">Cela entraîne l’affichage d’une liste qui inclut toutes les invites de commandes Visual Studio installées.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-118">This brings a list that includes all installed Visual Studio command prompts.</span></span>

3. <span data-ttu-id="e8bf1-119">Choisissez **Invite de commandes développeur** (ou l’invite de commandes que vous voulez utiliser).</span><span class="sxs-lookup"><span data-stu-id="e8bf1-119">Choose the **Developer Command Prompt** (or the command prompt you want to use).</span></span>

### <a name="in-windows-8"></a><span data-ttu-id="e8bf1-120">Dans Windows 8</span><span class="sxs-lookup"><span data-stu-id="e8bf1-120">In Windows 8</span></span>

1. <span data-ttu-id="e8bf1-121">Accédez à l’écran **Démarrer**, par exemple en appuyant sur la touche du logo Windows ![Logo Windows](../get-started/media/windowskeyboardlogo.png "Windowskeyboardlogo") de votre clavier.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-121">Go to the **Start** screen, by pressing the Windows logo key ![Windows logo](../get-started/media/windowskeyboardlogo.png "Windowskeyboardlogo") on your keyboard for example.</span></span>

2. <span data-ttu-id="e8bf1-122">Sur l’écran **Démarrer**, appuyez sur la touche du logo Windows ![Logo Windows](../get-started/media/windowskeyboardlogo.png "Windowskeyboardlogo") `+ Z`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-122">On the **Start** screen, press the Windows logo key ![Windows logo](../get-started/media/windowskeyboardlogo.png "Windowskeyboardlogo") `+ Z`.</span></span>

3. <span data-ttu-id="e8bf1-123">Choisissez l’icône **Vue Applications** en bas de l’écran, puis entrez `V`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-123">Choose the **Apps view** icon at the bottom of the screen and then enter `V`.</span></span> <span data-ttu-id="e8bf1-124">Cela entraîne l’affichage d’une liste qui inclut toutes les invites de commandes Visual Studio installées.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-124">This brings a list that includes all installed Visual Studio command prompts.</span></span>

4. <span data-ttu-id="e8bf1-125">Choisissez **Invite de commandes développeur** (ou l’invite de commandes que vous voulez utiliser).</span><span class="sxs-lookup"><span data-stu-id="e8bf1-125">Choose the **Developer Command Prompt** (or the command prompt you want to use).</span></span>

### <a name="in-windows-7"></a><span data-ttu-id="e8bf1-126">Dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8bf1-126">In Windows 7</span></span>

1. <span data-ttu-id="e8bf1-127">Sélectionnez **Démarrer**, développez **Tous les programmes**, puis développez **Microsoft Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-127">Choose **Start**, expand **All Programs**, and then expand **Microsoft Visual Studio**.</span></span>

2. <span data-ttu-id="e8bf1-128">En fonction de la version de Visual Studio que vous avez installée, choisissez **Visual Studio Tools**, **Invite de commandes Visual Studio** ou l’invite de commandes que vous voulez utiliser.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-128">Depending on the version of Visual Studio you've installed, choose  **Visual Studio Tools**, **Visual Studio Command Prompt**, or the command prompt you want to use.</span></span>

<span data-ttu-id="e8bf1-129">Si vous avez installé d’autres SDK, tels que le [SDK Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk), ou des [versions antérieures](https://developer.microsoft.com/windows/downloads/sdk-archive), vous pouvez voir des invites de commandes supplémentaires pour les architectures ARM, x86 ou x64.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-129">If you have other SDKs installed, such as the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) or [previous versions](https://developer.microsoft.com/windows/downloads/sdk-archive), you may see additional command prompts for ARM, x86, or x64 architectures.</span></span> <span data-ttu-id="e8bf1-130">Consultez la documentation relatives aux divers outils afin de déterminer la version de l'invite de commandes que vous devez utiliser.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-130">Check the documentation for the individual tools to determine which version of the command prompt you should use.</span></span>

## <a name="manually-locate-the-files-on-your-machine"></a><span data-ttu-id="e8bf1-131">Recherche manuelle des fichiers sur votre ordinateur</span><span class="sxs-lookup"><span data-stu-id="e8bf1-131">Manually locate the files on your machine</span></span>

<span data-ttu-id="e8bf1-132">En règle générale, les raccourcis des invites de commandes que vous avez installées sont placés dans le dossier **Menu Démarrer** de Visual Studio, par exemple dans C:\ProgramData\Microsoft\Windows\Menu Démarrer\Programmes\Visual Studio 2017\Visual Studio Tools.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-132">Usually, the shortcuts for the command prompts you have installed are placed at the **Start Menu** folder for Visual Studio, such as in C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Visual Studio 2017\Visual Studio Tools.</span></span> <span data-ttu-id="e8bf1-133">Mais si pour une raison quelconque la recherche de l’invite de commandes ne donne pas les résultats attendus, vous pouvez tenter de localiser manuellement le raccourci sur votre machine.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-133">But if for some reason, searching for the command prompt doesn't bring the expected results, you can try to manually locate the shortcut on your machine.</span></span> <span data-ttu-id="e8bf1-134">Essayez de rechercher le nom du fichier d’invite de commandes, par exemple *VsDevCmd.bat*, ou accédez au dossier Tools à l’emplacement C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools (le chemin varie en fonction de l’emplacement d’installation, de l’édition et de la version de Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="e8bf1-134">Try searching for the name of the command prompt file, such as *VsDevCmd.bat*, or go to the Tools folder such as C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools (path changes according to your Visual Studio version, edition, and installation location).</span></span>

## <a name="run-the-command-prompt-from-inside-visual-studio"></a><span data-ttu-id="e8bf1-135">Exécuter l’invite de commandes à partir de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e8bf1-135">Run the command prompt from inside Visual Studio</span></span>

<span data-ttu-id="e8bf1-136">Pour faciliter l’accès, vous pouvez ajouter l’invite de commandes développeur Visual Studio ou toute autre invite de commandes au menu **Outils** de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-136">For easier access, you can add the Visual Studio Developer Command Prompt, or any other command prompt, to the **Tools** menu in Visual Studio.</span></span> <span data-ttu-id="e8bf1-137">Pour cela, il vous suffit de l’ajouter à la liste des outils externes.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-137">To make the tool available, add it to the external tools list.</span></span> <span data-ttu-id="e8bf1-138">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e8bf1-138">Here are the steps:</span></span>

1. <span data-ttu-id="e8bf1-139">Ouvrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-139">Open Visual Studio.</span></span>

2. <span data-ttu-id="e8bf1-140">Sélectionnez le menu **Outils**, puis choisissez **Outils externes**.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-140">Select the **Tools** menu, and then choose **External Tools**.</span></span>

3. <span data-ttu-id="e8bf1-141">Dans la boîte de dialogue **Outils externes**, choisissez le bouton **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-141">On the **External Tools** dialog box, choose the **Add** button.</span></span> <span data-ttu-id="e8bf1-142">Une nouvelle entrée apparaît.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-142">A new entry appears.</span></span>

4. <span data-ttu-id="e8bf1-143">Entrez un **titre** pour votre nouvel élément de menu, par exemple `Command Prompt`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-143">Enter a **Title** for your new menu item such as `Command Prompt`.</span></span>

5. <span data-ttu-id="e8bf1-144">Dans le champ **Commande**, spécifiez le fichier à lancer, par exemple `%comspec%` ou `C:\Windows\System32\cmd.exe`.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-144">In the **Command** field, specify the file you want to launch, such as `%comspec%` or `C:\Windows\System32\cmd.exe`.</span></span>

6. <span data-ttu-id="e8bf1-145">Dans le champ **Arguments**, indiquez où trouver l’invite de commandes à utiliser en particulier, par exemple `/k "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\VsDevCmd.bat"` (cette commande lance l’invite de commandes développeur installée avec Visual Studio 2017 Enterprise).</span><span class="sxs-lookup"><span data-stu-id="e8bf1-145">In the **Arguments** field, specify where to find the specific command prompt you want to use such as `/k "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\VsDevCmd.bat"` (this command launches the Developer Command Prompt that is installed with Visual Studio 2017 Enterprise).</span></span> <span data-ttu-id="e8bf1-146">Changez cette valeur en fonction de l’emplacement d’installation, de l’édition et de la version de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-146">Change this value according to your Visual Studio version, edition, and installation location.</span></span>

7. <span data-ttu-id="e8bf1-147">Choisissez une valeur pour le champ **Répertoire Initial**, par exemple **Répertoire du projet**.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-147">Choose a value for the **Initial directory** field, such as **Project Directory**.</span></span>

8. <span data-ttu-id="e8bf1-148">Sélectionnez le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="e8bf1-148">Choose the **OK** button.</span></span>

   <span data-ttu-id="e8bf1-149">Le nouvel élément de menu est ajouté et vous pouvez accéder à l’invite de commandes à partir du menu **Outils**.</span><span class="sxs-lookup"><span data-stu-id="e8bf1-149">The new menu item is added, and you can access the command prompt from the **Tools** menu.</span></span>

   ![Élément de menu d’invite de commandes dans Visual Studio](media/command-prompt-vs-menu.png)

## <a name="see-also"></a><span data-ttu-id="e8bf1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8bf1-151">See also</span></span>

- [<span data-ttu-id="e8bf1-152">Outils</span><span class="sxs-lookup"><span data-stu-id="e8bf1-152">Tools</span></span>](../../../docs/framework/tools/index.md)
- [<span data-ttu-id="e8bf1-153">Gestion des outils externes</span><span class="sxs-lookup"><span data-stu-id="e8bf1-153">Managing External Tools</span></span>](/visualstudio/ide/managing-external-tools)
