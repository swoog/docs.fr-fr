---
title: Configuration requise pour .NET Core sur Windows
description: Découvrez les dépendances nécessaires sur votre machine Windows pour développer et exécuter des applications .NET Core.
author: JRAlexander
ms.author: johalex
ms.date: 04/24/2018
ms.openlocfilehash: 7c6f39f004ebc39ca714ce419a38d842fcf8f0cb
ms.sourcegitcommit: ff1d40507b3eb6e2185478e37c66c66be6de46f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/11/2018
---
# <a name="prerequisites-for-net-core-on-windows"></a><span data-ttu-id="4d9d8-103">Configuration requise pour .NET Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="4d9d8-103">Prerequisites for .NET Core on Windows</span></span>

<span data-ttu-id="4d9d8-104">Cet article montre les dépendances nécessaires pour développer des applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-104">This article shows the dependencies needed to develop .NET Core applications on Windows.</span></span> <span data-ttu-id="4d9d8-105">Les versions de système d’exploitation et les dépendances prises en charge ci-après s’appliquent aux trois façons de développer des applications .NET Core sur Windows :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-105">The supported OS versions and dependencies that follow apply to the three ways of developing .NET Core apps on Windows:</span></span>

* [<span data-ttu-id="4d9d8-106">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="4d9d8-106">Command line</span></span>](tutorials/using-with-xplat-cli.md)
* [<span data-ttu-id="4d9d8-107">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="4d9d8-107">Visual Studio 2017</span></span>](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)
* [<span data-ttu-id="4d9d8-108">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="4d9d8-108">Visual Studio Code</span></span>](https://code.visualstudio.com/)

## <a name="net-core-supported-windows-versions"></a><span data-ttu-id="4d9d8-109">Versions Windows prises en charge par .NET Core</span><span class="sxs-lookup"><span data-stu-id="4d9d8-109">.NET Core supported Windows versions</span></span>

<span data-ttu-id="4d9d8-110">.NET Core est pris en charge par les versions suivantes de :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-110">.NET Core is supported on the following versions of:</span></span>

* <span data-ttu-id="4d9d8-111">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="4d9d8-111">Windows 7 SP1</span></span>
* <span data-ttu-id="4d9d8-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4d9d8-112">Windows 8.1</span></span>
* <span data-ttu-id="4d9d8-113">Mise à jour anniversaire Windows 10 (version 1607) ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="4d9d8-113">Windows 10 Anniversary Update (version 1607) or later versions</span></span>
* <span data-ttu-id="4d9d8-114">Windows Server 2008 R2 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="4d9d8-114">Windows Server 2008 R2 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="4d9d8-115">Windows Server 2012 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="4d9d8-115">Windows Server 2012 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="4d9d8-116">Windows Server 2012 R2 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="4d9d8-116">Windows Server 2012 R2 (Full Server or Server Core)</span></span>
* <span data-ttu-id="4d9d8-117">Windows Server 2016 (version complète, Server Core ou Nano Server)</span><span class="sxs-lookup"><span data-stu-id="4d9d8-117">Windows Server 2016 (Full Server, Server Core, or Nano Server)</span></span>

<span data-ttu-id="4d9d8-118">Consultez [.NET Core 2.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 2.x.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-118">See [.NET Core 2.x - Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) for the complete list of .NET Core 2.x supported operating systems.</span></span>

<span data-ttu-id="4d9d8-119">Consultez [.NET Core 1.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-119">See [.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) for the complete list of .NET Core 1.x supported operating systems.</span></span>

## <a name="net-core-dependencies"></a><span data-ttu-id="4d9d8-120">Dépendances .NET Core</span><span class="sxs-lookup"><span data-stu-id="4d9d8-120">.NET Core dependencies</span></span>

<span data-ttu-id="4d9d8-121">.NET Core 1.1 et ses versions antérieures nécessitent le package redistribuable Visual C++ lors de l’exécution sur des versions de Windows antérieures à Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-121">.NET Core 1.1 and earlier versions require the Visual C++ Redistributable when running on Windows versions earlier than Windows 10 and Windows Server 2016.</span></span> <span data-ttu-id="4d9d8-122">Cette dépendance est installée automatiquement par le programme d’installation de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-122">This dependency is automatically installed by the .NET Core installer.</span></span>

<span data-ttu-id="4d9d8-123">Vous devez installer [Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) manuellement quand :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-123">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) must be manually installed when:</span></span>

* <span data-ttu-id="4d9d8-124">vous installez .NET Core avec le [script du programme d’installation](./tools/dotnet-install-script.md) ;</span><span class="sxs-lookup"><span data-stu-id="4d9d8-124">Installing .NET Core with the [installer script](./tools/dotnet-install-script.md).</span></span>
* <span data-ttu-id="4d9d8-125">vous déployez une application .NET Core autonome.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-125">Deploying a self-contained .NET Core application.</span></span>
* <span data-ttu-id="4d9d8-126">Génération du produit à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-126">Building the product from source.</span></span>
* <span data-ttu-id="4d9d8-127">Installation de .NET Core via un fichier *.zip*.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-127">Installing .NET Core via a *.zip* file.</span></span> <span data-ttu-id="4d9d8-128">Ceci peut inclure des serveurs de builds/CI/CD.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-128">This can include build/CI/CD servers.</span></span>

> [!NOTE]
> <span data-ttu-id="4d9d8-129">*Pour Windows 8.1 et versions antérieures, ou Windows Server 2012 R2 et versions antérieures :* vérifiez que votre installation de Windows est à jour et qu’elle comprend le correctif [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows) (que vous pouvez installer par le biais de Windows Update).</span><span class="sxs-lookup"><span data-stu-id="4d9d8-129">*For Windows 8.1 and earlier versions, or Windows Server 2012 R2 and earlier versions:* Make sure that your Windows installation is up-to-date and includes [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows) which can be installed through Windows Update.</span></span> <span data-ttu-id="4d9d8-130">Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur comme celle-ci : `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span><span class="sxs-lookup"><span data-stu-id="4d9d8-130">If you don't have this update installed, you'll see an error when you launch a .NET Core application like the following: `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span></span>

## <a name="prerequisites-with-visual-studio-2017"></a><span data-ttu-id="4d9d8-131">Prérequis pour Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="4d9d8-131">Prerequisites with Visual Studio 2017</span></span>

<span data-ttu-id="4d9d8-132">Vous pouvez utiliser l’éditeur de votre choix pour développer des applications .NET Core à l’aide du Kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-132">You can use any editor to develop .NET Core applications using the .NET Core SDK.</span></span> <span data-ttu-id="4d9d8-133">[Visual Studio 2017](#visual-studio-2017) fournit un environnement de développement intégré pour les applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-133">[Visual Studio 2017](#visual-studio-2017) provides an integrated development environment for .NET Core apps on Windows.</span></span>

<span data-ttu-id="4d9d8-134">Vous trouverez plus d’informations sur les modifications apportées à Visual Studio 2017 dans les [notes de publication](/visualstudio/releasenotes/vs2017-relnotes).</span><span class="sxs-lookup"><span data-stu-id="4d9d8-134">You can read more about the changes in Visual Studio 2017 in the [release notes](/visualstudio/releasenotes/vs2017-relnotes).</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="4d9d8-135">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="4d9d8-135">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="4d9d8-136">Pour développer des applications .NET Core 2.x dans Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-136">To develop .NET Core 2.x apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="4d9d8-137">[Téléchargez et installez Visual Studio 2017 version 15.3.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="4d9d8-137">[Download and install Visual Studio 2017 version 15.3.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-3-workloads.jpg)

<span data-ttu-id="4d9d8-139">Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, Visual Studio 2017 utilise .NET Core 1.x par défaut.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-139">After the **.NET Core cross-platform development** toolset is installed, Visual Studio 2017 uses .NET Core 1.x by default.</span></span> <span data-ttu-id="4d9d8-140">Installez le SDK .NET Core 2.x pour obtenir la prise en charge de .NET Core 2.x dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-140">Install the .NET Core 2.x SDK to get .NET Core 2.x support in Visual Studio 2017.</span></span>

 2. <span data-ttu-id="4d9d8-141">Installez le [SDK .NET Core 2.x](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="4d9d8-141">Install the [.NET Core 2.x SDK](https://www.microsoft.com/net/download/core).</span></span>
 3. <span data-ttu-id="4d9d8-142">Reciblez les projets .NET Core 1.x existants ou nouveaux sur .NET Core 2.x en suivant les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-142">Retarget existing or new .NET Core 1.x projects to .NET Core 2.x using the following instructions:</span></span>
    * <span data-ttu-id="4d9d8-143">Dans le menu **Projet**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-143">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="4d9d8-144">Dans le menu de sélection **framework cible**, choisissez **.NET Core 2.0**.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-144">In the **Target framework** selection menu, set the value to **.NET Core 2.0**.</span></span>

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="4d9d8-146">Une fois installé le SDK .NET Core 2.x, Visual Studio 2017 l’utilise par défaut et prend en charge les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-146">Once the .NET Core 2.x SDK is installed, Visual Studio 2017 uses the .NET Core SDK 2.x by default, and supports the following actions:</span></span>

* <span data-ttu-id="4d9d8-147">Ouvrir, générer et exécuter les projets .NET Core 1.x existants.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-147">Open, build, and run existing .NET Core 1.x projects.</span></span>
* <span data-ttu-id="4d9d8-148">Recibler les projets .NET Core 1.x vers .NET Core 2.x, les générer et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-148">Retarget .NET Core 1.x projects to .NET Core 2.x, build, and run.</span></span>
* <span data-ttu-id="4d9d8-149">Créer des projets .NET Core 2.x.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-149">Create new .NET Core 2.x projects.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4d9d8-150">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4d9d8-150">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="4d9d8-151">Pur développer des applications .NET Core 1.x dans Visual Studio, [téléchargez et installez Visual Studio 2017 RTM (version 15.0.26228.4) ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="4d9d8-151">To develop .NET Core 1.x apps in Visual Studio, [download and install Visual Studio 2017 RTM (version 15.0.26228.4) or higher](/visualstudio/install/install-visual-studio) with the **".NET Core cross-platform development"** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs_workloads.jpg)

> [!IMPORTANT]
> <span data-ttu-id="4d9d8-153">Bien que vous puissiez utiliser Visual Studio 2015 pour le développement .NET Core 1.x, nous vous le déconseillons pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-153">It's possible to use Visual Studio 2015 for .NET Core 1.x development, but it's not recommended for the following reasons:</span></span>
  > * <span data-ttu-id="4d9d8-154">Les outils .NET Core sont une préversion, qui n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-154">The .NET Core tooling is a preview version, which is not supported.</span></span>
  > * <span data-ttu-id="4d9d8-155">Les projets sont basés sur project.json, configuration qui est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-155">The projects are project.json-based, which is deprecated.</span></span>
>
> <span data-ttu-id="4d9d8-156">Pour plus d’informations sur les changements de format de projet, consultez la page [Vue d’ensemble des modifications](./tools/cli-msbuild-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="4d9d8-156">For more information about the project format changes, see [High-level overview of changes](./tools/cli-msbuild-architecture.md).</span></span>
---

> [!TIP]
> <span data-ttu-id="4d9d8-157">Pour vérifier votre version de Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="4d9d8-157">To verify your Visual Studio 2017 version:</span></span>
>
> * <span data-ttu-id="4d9d8-158">Dans le menu **Aide**, choisissez **À propos de Microsoft Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-158">On the **Help** menu, choose **About Microsoft Visual Studio**.</span></span>
> * <span data-ttu-id="4d9d8-159">Dans la boîte de dialogue **À propos de Microsoft Visual Studio**, vérifiez le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-159">In the **About Microsoft Visual Studio** dialog, verify the version number.</span></span>
>   * <span data-ttu-id="4d9d8-160">Pour les applications .NET Core 2.1 Preview 1, Visual Studio 2017 version 15.6 Preview 6 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-160">For .NET Core 2.1 Preview 1 apps, Visual Studio 2017 version 15.6 Preview 6 or higher.</span></span>
>   * <span data-ttu-id="4d9d8-161">Pour les applications .NET Core 2.0, Visual Studio 2017 version 15.3 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-161">For .NET Core 2.0 apps, Visual Studio 2017 version 15.3 or higher.</span></span>
>   * <span data-ttu-id="4d9d8-162">Pour les applications .NET Core 1.x, Visual Studio 2017 version 15.0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4d9d8-162">For .NET Core 1.x apps, Visual Studio 2017 version 15.0 or higher.</span></span>
