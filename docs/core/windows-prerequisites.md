---
title: Configuration requise pour .NET Core sur Windows
description: Découvrez les dépendances nécessaires sur votre machine Windows pour développer et exécuter des applications .NET Core.
author: JRAlexander
ms.author: johalex
ms.date: 05/18/2018
ms.openlocfilehash: 3d172c83f0a79744afbaeeff52d7fea62d9b98b6
ms.sourcegitcommit: 895c7602386a6dfe7ca4facce3d965b27e5c6e87
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2018
ms.locfileid: "34311986"
---
# <a name="prerequisites-for-net-core-on-windows"></a><span data-ttu-id="a2adf-103">Configuration requise pour .NET Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="a2adf-103">Prerequisites for .NET Core on Windows</span></span>

<span data-ttu-id="a2adf-104">Cet article montre les dépendances nécessaires pour développer des applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="a2adf-104">This article shows the dependencies needed to develop .NET Core applications on Windows.</span></span> <span data-ttu-id="a2adf-105">Les versions de système d’exploitation et les dépendances prises en charge ci-après s’appliquent aux trois façons de développer des applications .NET Core sur Windows :</span><span class="sxs-lookup"><span data-stu-id="a2adf-105">The supported OS versions and dependencies that follow apply to the three ways of developing .NET Core apps on Windows:</span></span>

* [<span data-ttu-id="a2adf-106">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="a2adf-106">Command line</span></span>](tutorials/using-with-xplat-cli.md)
* [<span data-ttu-id="a2adf-107">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="a2adf-107">Visual Studio 2017</span></span>](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)
* [<span data-ttu-id="a2adf-108">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="a2adf-108">Visual Studio Code</span></span>](https://code.visualstudio.com/)

## <a name="net-core-supported-windows-versions"></a><span data-ttu-id="a2adf-109">Versions Windows prises en charge par .NET Core</span><span class="sxs-lookup"><span data-stu-id="a2adf-109">.NET Core supported Windows versions</span></span>

<span data-ttu-id="a2adf-110">.NET Core est pris en charge par les versions suivantes de :</span><span class="sxs-lookup"><span data-stu-id="a2adf-110">.NET Core is supported on the following versions of:</span></span>

* <span data-ttu-id="a2adf-111">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="a2adf-111">Windows 7 SP1</span></span>
* <span data-ttu-id="a2adf-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a2adf-112">Windows 8.1</span></span>
* <span data-ttu-id="a2adf-113">Mise à jour anniversaire Windows 10 (version 1607) ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="a2adf-113">Windows 10 Anniversary Update (version 1607) or later versions</span></span>
* <span data-ttu-id="a2adf-114">Windows Server 2008 R2 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="a2adf-114">Windows Server 2008 R2 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="a2adf-115">Windows Server 2012 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="a2adf-115">Windows Server 2012 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="a2adf-116">Windows Server 2012 R2 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="a2adf-116">Windows Server 2012 R2 (Full Server or Server Core)</span></span>
* <span data-ttu-id="a2adf-117">Windows Server 2016 ou versions ultérieures (version complète, Server Core ou Nano Server)</span><span class="sxs-lookup"><span data-stu-id="a2adf-117">Windows Server 2016 or later versions (Full Server, Server Core, or Nano Server)</span></span>

<span data-ttu-id="a2adf-118">Les articles suivants dressent la liste complète des systèmes d’exploitation .NET Core pris en charge par version :</span><span class="sxs-lookup"><span data-stu-id="a2adf-118">The following articles have a complete list of .NET Core supported operating systems per version:</span></span>

* [<span data-ttu-id="a2adf-119">.NET Core 2.1 - Versions de système d’exploitation prises en charge</span><span class="sxs-lookup"><span data-stu-id="a2adf-119">.NET Core 2.1 - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)
* [<span data-ttu-id="a2adf-120">.NET Core 2.0 - Versions de système d’exploitation prises en charge</span><span class="sxs-lookup"><span data-stu-id="a2adf-120">.NET Core 2.0 - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md)
* [<span data-ttu-id="a2adf-121">.NET Core 1.x - Versions de système d’exploitation prises en charge</span><span class="sxs-lookup"><span data-stu-id="a2adf-121">.NET Core 1.x - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)

## <a name="net-core-dependencies"></a><span data-ttu-id="a2adf-122">Dépendances .NET Core</span><span class="sxs-lookup"><span data-stu-id="a2adf-122">.NET Core dependencies</span></span>

<span data-ttu-id="a2adf-123">.NET Core 1.1 et ses versions antérieures nécessitent le package redistribuable Visual C++ lors de l’exécution sur des versions de Windows antérieures à Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="a2adf-123">.NET Core 1.1 and earlier versions require the Visual C++ Redistributable when running on Windows versions earlier than Windows 10 and Windows Server 2016.</span></span> <span data-ttu-id="a2adf-124">Cette dépendance est installée automatiquement par le programme d’installation de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="a2adf-124">This dependency is automatically installed by the .NET Core installer.</span></span>

<span data-ttu-id="a2adf-125">Vous devez installer [Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) manuellement quand :</span><span class="sxs-lookup"><span data-stu-id="a2adf-125">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) must be manually installed when:</span></span>

* <span data-ttu-id="a2adf-126">vous installez .NET Core avec le [script du programme d’installation](./tools/dotnet-install-script.md) ;</span><span class="sxs-lookup"><span data-stu-id="a2adf-126">Installing .NET Core with the [installer script](./tools/dotnet-install-script.md).</span></span>
* <span data-ttu-id="a2adf-127">vous déployez une application .NET Core autonome.</span><span class="sxs-lookup"><span data-stu-id="a2adf-127">Deploying a self-contained .NET Core application.</span></span>
* <span data-ttu-id="a2adf-128">Génération du produit à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="a2adf-128">Building the product from source.</span></span>
* <span data-ttu-id="a2adf-129">Installation de .NET Core via un fichier *.zip*.</span><span class="sxs-lookup"><span data-stu-id="a2adf-129">Installing .NET Core via a *.zip* file.</span></span> <span data-ttu-id="a2adf-130">Ceci peut inclure des serveurs de builds/CI/CD.</span><span class="sxs-lookup"><span data-stu-id="a2adf-130">This can include build/CI/CD servers.</span></span>

> [!NOTE]
> <span data-ttu-id="a2adf-131">**Pour Windows 8.1 et versions antérieures, ou Windows Server 2012 R2 et versions antérieures :**</span><span class="sxs-lookup"><span data-stu-id="a2adf-131">**For Windows 8.1 and earlier versions, or Windows Server 2012 R2 and earlier versions:**</span></span>
>
> <span data-ttu-id="a2adf-132">Vérifiez que votre installation Windows est à jour et comprend le correctif logiciel [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows), installable via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="a2adf-132">Make sure that your Windows installation is up-to-date and includes [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows), which can be installed through Windows Update.</span></span> <span data-ttu-id="a2adf-133">Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur semblable à celle-ci : `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span><span class="sxs-lookup"><span data-stu-id="a2adf-133">If you don't have this update installed, you'll see an error like the following when you launch a .NET Core application: `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span></span>
>
> <span data-ttu-id="a2adf-134">**Pour Windows 7 ou Windows Server 2008 R2 :**</span><span class="sxs-lookup"><span data-stu-id="a2adf-134">**For Windows 7 or Windows Server 2008 R2:**</span></span>
>
> <span data-ttu-id="a2adf-135">Outre KB2999226, vérifiez également que la mise à jour [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot) est installée.</span><span class="sxs-lookup"><span data-stu-id="a2adf-135">In addition to KB2999226, make sure you also have [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot) installed.</span></span> <span data-ttu-id="a2adf-136">Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur comme celle-ci : `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`.</span><span class="sxs-lookup"><span data-stu-id="a2adf-136">If you don't have this update installed, you'll see an error similar to the following when you launch a .NET Core application: `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`.</span></span>

## <a name="prerequisites-with-visual-studio-2017"></a><span data-ttu-id="a2adf-137">Prérequis pour Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="a2adf-137">Prerequisites with Visual Studio 2017</span></span>

<span data-ttu-id="a2adf-138">Vous pouvez utiliser l’éditeur de votre choix pour développer des applications .NET Core à l’aide du Kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="a2adf-138">You can use any editor to develop .NET Core applications using the .NET Core SDK.</span></span> <span data-ttu-id="a2adf-139">[Visual Studio 2017](#visual-studio-2017) fournit un environnement de développement intégré pour les applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="a2adf-139">[Visual Studio 2017](#visual-studio-2017) provides an integrated development environment for .NET Core apps on Windows.</span></span>

<span data-ttu-id="a2adf-140">Vous trouverez plus d’informations sur les modifications apportées à Visual Studio 2017 dans les [notes de publication](/visualstudio/releasenotes/vs2017-relnotes).</span><span class="sxs-lookup"><span data-stu-id="a2adf-140">You can read more about the changes in Visual Studio 2017 in the [release notes](/visualstudio/releasenotes/vs2017-relnotes).</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="a2adf-141">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="a2adf-141">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="a2adf-142">Pour développer des applications .NET Core 2.x dans Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="a2adf-142">To develop .NET Core 2.x apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="a2adf-143">[Téléchargez et installez Visual Studio 2017 version 15.3.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="a2adf-143">[Download and install Visual Studio 2017 version 15.3.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-3-workloads.jpg)

<span data-ttu-id="a2adf-145">Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, Visual Studio 2017 utilise .NET Core 1.x par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2adf-145">After the **.NET Core cross-platform development** toolset is installed, Visual Studio 2017 uses .NET Core 1.x by default.</span></span> <span data-ttu-id="a2adf-146">Installez le SDK .NET Core 2.x pour obtenir la prise en charge de .NET Core 2.x dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="a2adf-146">Install the .NET Core 2.x SDK to get .NET Core 2.x support in Visual Studio 2017.</span></span>

 2. <span data-ttu-id="a2adf-147">Installez le [SDK .NET Core 2.x](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="a2adf-147">Install the [.NET Core 2.x SDK](https://www.microsoft.com/net/download/core).</span></span>
 3. <span data-ttu-id="a2adf-148">Reciblez les projets .NET Core 1.x existants ou nouveaux sur .NET Core 2.x en suivant les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2adf-148">Retarget existing or new .NET Core 1.x projects to .NET Core 2.x using the following instructions:</span></span>
    * <span data-ttu-id="a2adf-149">Dans le menu **Projet**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a2adf-149">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="a2adf-150">Dans le menu de sélection **framework cible**, choisissez **.NET Core 2.0**.</span><span class="sxs-lookup"><span data-stu-id="a2adf-150">In the **Target framework** selection menu, set the value to **.NET Core 2.0**.</span></span>

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="a2adf-152">Une fois installé le SDK .NET Core 2.x, Visual Studio 2017 l’utilise par défaut et prend en charge les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2adf-152">Once the .NET Core 2.x SDK is installed, Visual Studio 2017 uses the .NET Core SDK 2.x by default, and supports the following actions:</span></span>

* <span data-ttu-id="a2adf-153">Ouvrir, générer et exécuter les projets .NET Core 1.x existants.</span><span class="sxs-lookup"><span data-stu-id="a2adf-153">Open, build, and run existing .NET Core 1.x projects.</span></span>
* <span data-ttu-id="a2adf-154">Recibler les projets .NET Core 1.x vers .NET Core 2.x, les générer et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="a2adf-154">Retarget .NET Core 1.x projects to .NET Core 2.x, build, and run.</span></span>
* <span data-ttu-id="a2adf-155">Créer des projets .NET Core 2.x.</span><span class="sxs-lookup"><span data-stu-id="a2adf-155">Create new .NET Core 2.x projects.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a2adf-156">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a2adf-156">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="a2adf-157">Pur développer des applications .NET Core 1.x dans Visual Studio, [téléchargez et installez Visual Studio 2017 RTM (version 15.0.26228.4) ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="a2adf-157">To develop .NET Core 1.x apps in Visual Studio, [download and install Visual Studio 2017 RTM (version 15.0.26228.4) or higher](/visualstudio/install/install-visual-studio) with the **".NET Core cross-platform development"** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs_workloads.jpg)

> [!IMPORTANT]
> <span data-ttu-id="a2adf-159">Bien que vous puissiez utiliser Visual Studio 2015 pour le développement .NET Core 1.x, nous vous le déconseillons pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2adf-159">It's possible to use Visual Studio 2015 for .NET Core 1.x development, but it's not recommended for the following reasons:</span></span>
  > * <span data-ttu-id="a2adf-160">Les outils .NET Core sont une préversion, qui n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a2adf-160">The .NET Core tooling is a preview version, which is not supported.</span></span>
  > * <span data-ttu-id="a2adf-161">Les projets sont basés sur project.json, configuration qui est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="a2adf-161">The projects are project.json-based, which is deprecated.</span></span>
>
> <span data-ttu-id="a2adf-162">Pour plus d’informations sur les changements de format de projet, consultez la page [Vue d’ensemble des modifications](./tools/cli-msbuild-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="a2adf-162">For more information about the project format changes, see [High-level overview of changes](./tools/cli-msbuild-architecture.md).</span></span>
---

> [!TIP]
> <span data-ttu-id="a2adf-163">Pour vérifier votre version de Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="a2adf-163">To verify your Visual Studio 2017 version:</span></span>
>
> * <span data-ttu-id="a2adf-164">Dans le menu **Aide**, choisissez **À propos de Microsoft Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="a2adf-164">On the **Help** menu, choose **About Microsoft Visual Studio**.</span></span>
> * <span data-ttu-id="a2adf-165">Dans la boîte de dialogue **À propos de Microsoft Visual Studio**, vérifiez le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="a2adf-165">In the **About Microsoft Visual Studio** dialog, verify the version number.</span></span>
>   * <span data-ttu-id="a2adf-166">Pour les applications .NET Core 2.1 RC, Visual Studio 2017 version 15.7 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a2adf-166">For .NET Core 2.1 RC apps, Visual Studio 2017 version 15.7 or higher.</span></span>
>   * <span data-ttu-id="a2adf-167">Pour les applications .NET Core 2.0, Visual Studio 2017 version 15.3 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a2adf-167">For .NET Core 2.0 apps, Visual Studio 2017 version 15.3 or higher.</span></span>
>   * <span data-ttu-id="a2adf-168">Pour les applications .NET Core 1.x, Visual Studio 2017 version 15.0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a2adf-168">For .NET Core 1.x apps, Visual Studio 2017 version 15.0 or higher.</span></span>
