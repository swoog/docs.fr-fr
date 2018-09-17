---
title: Configuration requise pour .NET Core sur Windows
description: Découvrez les dépendances nécessaires sur votre machine Windows pour développer et exécuter des applications .NET Core.
author: mairaw
ms.author: mairaw
ms.date: 08/31/2018
ms.openlocfilehash: 477d303b50495070ba3a3540188deb274dd9f510
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44179492"
---
# <a name="prerequisites-for-net-core-on-windows"></a><span data-ttu-id="ce4ad-103">Configuration requise pour .NET Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="ce4ad-103">Prerequisites for .NET Core on Windows</span></span>

<span data-ttu-id="ce4ad-104">Cet article montre les dépendances nécessaires pour développer des applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-104">This article shows the dependencies needed to develop .NET Core applications on Windows.</span></span> <span data-ttu-id="ce4ad-105">Les versions de système d’exploitation et les dépendances prises en charge ci-après s’appliquent aux trois façons de développer des applications .NET Core sur Windows :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-105">The supported OS versions and dependencies that follow apply to the three ways of developing .NET Core apps on Windows:</span></span>

* [<span data-ttu-id="ce4ad-106">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="ce4ad-106">Command line</span></span>](tutorials/using-with-xplat-cli.md)
* [<span data-ttu-id="ce4ad-107">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="ce4ad-107">Visual Studio 2017</span></span>](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)
* [<span data-ttu-id="ce4ad-108">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ce4ad-108">Visual Studio Code</span></span>](https://code.visualstudio.com/)

## <a name="net-core-supported-windows-versions"></a><span data-ttu-id="ce4ad-109">Versions Windows prises en charge par .NET Core</span><span class="sxs-lookup"><span data-stu-id="ce4ad-109">.NET Core supported Windows versions</span></span>

<span data-ttu-id="ce4ad-110">.NET Core est pris en charge par les versions suivantes de :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-110">.NET Core is supported on the following versions of:</span></span>

* <span data-ttu-id="ce4ad-111">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="ce4ad-111">Windows 7 SP1</span></span>
* <span data-ttu-id="ce4ad-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ce4ad-112">Windows 8.1</span></span>
* <span data-ttu-id="ce4ad-113">Mise à jour anniversaire Windows 10 (version 1607) ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="ce4ad-113">Windows 10 Anniversary Update (version 1607) or later versions</span></span>
* <span data-ttu-id="ce4ad-114">Windows Server 2008 R2 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="ce4ad-114">Windows Server 2008 R2 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="ce4ad-115">Windows Server 2012 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="ce4ad-115">Windows Server 2012 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="ce4ad-116">Windows Server 2012 R2 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="ce4ad-116">Windows Server 2012 R2 (Full Server or Server Core)</span></span>
* <span data-ttu-id="ce4ad-117">Windows Server 2016 ou versions ultérieures (version complète, Server Core ou Nano Server)</span><span class="sxs-lookup"><span data-stu-id="ce4ad-117">Windows Server 2016 or later versions (Full Server, Server Core, or Nano Server)</span></span>

## <a name="net-core-supported-operating-systems"></a><span data-ttu-id="ce4ad-118">Systèmes d’exploitation pris en charge par .NET Core</span><span class="sxs-lookup"><span data-stu-id="ce4ad-118">.NET Core supported operating systems</span></span>

<span data-ttu-id="ce4ad-119">Les articles suivants dressent la liste complète des systèmes d’exploitation .NET Core pris en charge par version :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-119">The following articles have a complete list of .NET Core supported operating systems per version:</span></span>

* [<span data-ttu-id="ce4ad-120">.NET Core 2.1 - Versions de système d’exploitation prises en charge</span><span class="sxs-lookup"><span data-stu-id="ce4ad-120">.NET Core 2.1 - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)
* [<span data-ttu-id="ce4ad-121">.NET Core 2.0 - Versions de système d’exploitation prises en charge</span><span class="sxs-lookup"><span data-stu-id="ce4ad-121">.NET Core 2.0 - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md)
* [<span data-ttu-id="ce4ad-122">.NET Core 1.x - Versions de système d’exploitation prises en charge</span><span class="sxs-lookup"><span data-stu-id="ce4ad-122">.NET Core 1.x - Supported OS Versions</span></span>](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)

## <a name="net-core-dependencies"></a><span data-ttu-id="ce4ad-123">Dépendances .NET Core</span><span class="sxs-lookup"><span data-stu-id="ce4ad-123">.NET Core dependencies</span></span>

<span data-ttu-id="ce4ad-124">.NET Core 1.1 et ses versions antérieures nécessitent le package redistribuable Visual C++ lors de l’exécution sur des versions de Windows antérieures à Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-124">.NET Core 1.1 and earlier versions require the Visual C++ Redistributable when running on Windows versions earlier than Windows 10 and Windows Server 2016.</span></span> <span data-ttu-id="ce4ad-125">Cette dépendance est installée automatiquement par le programme d’installation de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-125">This dependency is automatically installed by the .NET Core installer.</span></span>

<span data-ttu-id="ce4ad-126">Vous devez installer [Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) manuellement quand :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-126">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) must be manually installed when:</span></span>

* <span data-ttu-id="ce4ad-127">vous installez .NET Core avec le [script du programme d’installation](./tools/dotnet-install-script.md) ;</span><span class="sxs-lookup"><span data-stu-id="ce4ad-127">Installing .NET Core with the [installer script](./tools/dotnet-install-script.md).</span></span>
* <span data-ttu-id="ce4ad-128">vous déployez une application .NET Core autonome.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-128">Deploying a self-contained .NET Core application.</span></span>
* <span data-ttu-id="ce4ad-129">Génération du produit à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-129">Building the product from source.</span></span>
* <span data-ttu-id="ce4ad-130">Installation de .NET Core via un fichier *.zip*.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-130">Installing .NET Core via a *.zip* file.</span></span> <span data-ttu-id="ce4ad-131">Ceci peut inclure des serveurs de builds/CI/CD.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-131">This can include build/CI/CD servers.</span></span>

> [!NOTE]
> <span data-ttu-id="ce4ad-132">**Pour Windows 8.1 et versions antérieures, ou Windows Server 2012 R2 et versions antérieures :**</span><span class="sxs-lookup"><span data-stu-id="ce4ad-132">**For Windows 8.1 and earlier versions, or Windows Server 2012 R2 and earlier versions:**</span></span>
>
> <span data-ttu-id="ce4ad-133">Vérifiez que votre installation Windows est à jour et comprend le correctif logiciel [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows), installable via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-133">Make sure that your Windows installation is up-to-date and includes [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows), which can be installed through Windows Update.</span></span> <span data-ttu-id="ce4ad-134">Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur semblable à celle-ci : `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span><span class="sxs-lookup"><span data-stu-id="ce4ad-134">If you don't have this update installed, you'll see an error like the following when you launch a .NET Core application: `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`</span></span>
>
> <span data-ttu-id="ce4ad-135">**Pour Windows 7 ou Windows Server 2008 R2 :**</span><span class="sxs-lookup"><span data-stu-id="ce4ad-135">**For Windows 7 or Windows Server 2008 R2:**</span></span>
>
> <span data-ttu-id="ce4ad-136">Outre KB2999226, vérifiez également que la mise à jour [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot) est installée.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-136">In addition to KB2999226, make sure you also have [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot) installed.</span></span> <span data-ttu-id="ce4ad-137">Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur comme celle-ci : `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-137">If you don't have this update installed, you'll see an error similar to the following when you launch a .NET Core application: `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`.</span></span>

## <a name="prerequisites-with-visual-studio-2017"></a><span data-ttu-id="ce4ad-138">Prérequis pour Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="ce4ad-138">Prerequisites with Visual Studio 2017</span></span>

<span data-ttu-id="ce4ad-139">Vous pouvez utiliser l’éditeur de votre choix pour développer des applications .NET Core à l’aide du Kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-139">You can use any editor to develop .NET Core applications using the .NET Core SDK.</span></span> <span data-ttu-id="ce4ad-140">[Visual Studio 2017](#visual-studio-2017) fournit un environnement de développement intégré pour les applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-140">[Visual Studio 2017](#visual-studio-2017) provides an integrated development environment for .NET Core apps on Windows.</span></span>

<span data-ttu-id="ce4ad-141">Vous trouverez plus d’informations sur les modifications apportées à Visual Studio 2017 dans les [notes de publication](/visualstudio/releasenotes/vs2017-relnotes).</span><span class="sxs-lookup"><span data-stu-id="ce4ad-141">You can read more about the changes in Visual Studio 2017 in the [release notes](/visualstudio/releasenotes/vs2017-relnotes).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ce4ad-142">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ce4ad-142">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="ce4ad-143">Pour développer des applications .NET Core 2.1 dans Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-143">To develop .NET Core 2.1 apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="ce4ad-144">[Téléchargez et installez Visual Studio 2017 version 15.7.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="ce4ad-144">[Download and install Visual Studio 2017 version 15.7.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-8-workloads.jpg)

<span data-ttu-id="ce4ad-146">Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, par défaut, Visual Studio 2017 15.7 utilise le SDK .NET Core 2.0, et Visual Studio 2017 15.8 utilise le SDK 2.1.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-146">After the **.NET Core cross-platform development** toolset is installed, by default, Visual Studio 2017 15.7 uses .NET Core 2.0 SDK and Visual Studio 2017 15.8 uses 2.1 SDK.</span></span>

 2. <span data-ttu-id="ce4ad-147">Si vous utilisez Visual Studio 2017 15.7, installez le [SDK .NET Core 2.1](https://www.microsoft.com/net/download/core) ou effectuez la mise à niveau vers Visual Studio 2017 15.8.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-147">If you're using Visual Studio 2017 15.7, install the [.NET Core 2.1 SDK](https://www.microsoft.com/net/download/core) or upgrade to Visual Studio 2017 15.8.</span></span>

 3. <span data-ttu-id="ce4ad-148">Reciblez vos projets .NET Core existants ou nouveaux vers .NET Core 2.1 en vous aidant des instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-148">Retarget existing or new .NET Core projects to .NET Core 2.1 using the following instructions:</span></span>
    * <span data-ttu-id="ce4ad-149">Dans le menu **Projet**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-149">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="ce4ad-150">Dans le menu de sélection du **framework cible**, choisissez **.NET Core 2.1**.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-150">In the **Target framework** selection menu, set the value to **.NET Core 2.1**.</span></span>

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="ce4ad-152">Une fois que vous avez configuré Visual Studio avec le SDK .NET Core 2.1, vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-152">Once you have Visual Studio configured with .NET Core 2.1 SDK, you can do the following actions:</span></span>

* <span data-ttu-id="ce4ad-153">Ouvrir, générer et exécuter les projets .NET Core 1.x et 2.x existants.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-153">Open, build, and run existing .NET Core 1.x and 2.x projects.</span></span>
* <span data-ttu-id="ce4ad-154">Recibler les projets .NET Core 1.x et 2.0 vers .NET Core 2.1, les générer et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-154">Retarget .NET Core 1.x and 2.0 projects to .NET Core 2.1, build, and run.</span></span>
* <span data-ttu-id="ce4ad-155">Créer des projets .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-155">Create new .NET Core 2.1 projects.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ce4ad-156">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ce4ad-156">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="ce4ad-157">Pour développer des applications .NET Core 2.0 dans Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-157">To develop .NET Core 2.0 apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="ce4ad-158">[Téléchargez et installez Visual Studio 2017 version 15.3.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="ce4ad-158">[Download and install Visual Studio 2017 version 15.3.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-3-workloads.jpg)

<span data-ttu-id="ce4ad-160">Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, Visual Studio 2017 utilise .NET Core 1.x par défaut.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-160">After the **.NET Core cross-platform development** toolset is installed, Visual Studio 2017 uses .NET Core 1.x by default.</span></span> <span data-ttu-id="ce4ad-161">Installez le SDK .NET Core 2.0 pour bénéficier de la prise en charge de .NET Core 2.0 dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-161">Install the .NET Core 2.0 SDK to get .NET Core 2.0 support in Visual Studio 2017.</span></span>

 2. <span data-ttu-id="ce4ad-162">Installez le [SDK .NET Core 2.0](https://www.microsoft.com/net/download/dotnet-core/2.0).</span><span class="sxs-lookup"><span data-stu-id="ce4ad-162">Install the [.NET Core 2.0 SDK](https://www.microsoft.com/net/download/dotnet-core/2.0).</span></span>
 3. <span data-ttu-id="ce4ad-163">Reciblez vos projets .NET Core 1.x existants ou nouveaux vers .NET Core 2.0 en vous aidant des instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-163">Retarget existing or new .NET Core 1.x projects to .NET Core 2.0 using the following instructions:</span></span>
    * <span data-ttu-id="ce4ad-164">Dans le menu **Projet**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-164">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="ce4ad-165">Dans le menu de sélection **framework cible**, choisissez **.NET Core 2.0**.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-165">In the **Target framework** selection menu, set the value to **.NET Core 2.0**.</span></span>

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="ce4ad-167">Une fois le SDK .NET Core 2.0 installé, Visual Studio 2017 l’utilise par défaut et prend en charge les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-167">Once the .NET Core 2.0 SDK is installed, Visual Studio 2017 uses the .NET Core SDK 2.0 by default, and supports the following actions:</span></span>

* <span data-ttu-id="ce4ad-168">Ouvrir, générer et exécuter les projets .NET Core 1.x existants.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-168">Open, build, and run existing .NET Core 1.x projects.</span></span>
* <span data-ttu-id="ce4ad-169">Recibler les projets .NET Core 1.x vers .NET Core 2.0, les générer et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-169">Retarget .NET Core 1.x projects to .NET Core 2.0, build, and run.</span></span>
* <span data-ttu-id="ce4ad-170">Créer des projets .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-170">Create new .NET Core 2.0 projects.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ce4ad-171">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ce4ad-171">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="ce4ad-172">Pur développer des applications .NET Core 1.x dans Visual Studio, [téléchargez et installez Visual Studio 2017](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="ce4ad-172">To develop .NET Core 1.x apps in Visual Studio, [download and install Visual Studio 2017](/visualstudio/install/install-visual-studio) with the **".NET Core cross-platform development"** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs_workloads.jpg)

> [!IMPORTANT]
> <span data-ttu-id="ce4ad-174">Bien que vous puissiez utiliser Visual Studio 2015 pour le développement .NET Core 1.x, nous vous le déconseillons pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-174">It's possible to use Visual Studio 2015 for .NET Core 1.x development, but it's not recommended for the following reasons:</span></span>
  > * <span data-ttu-id="ce4ad-175">Les outils .NET Core sont une préversion, qui n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-175">The .NET Core tooling is a preview version, which is not supported.</span></span>
  > * <span data-ttu-id="ce4ad-176">Les projets sont basés sur project.json, configuration qui est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-176">The projects are project.json-based, which is deprecated.</span></span>
>
> <span data-ttu-id="ce4ad-177">Pour plus d’informations sur les changements de format de projet, consultez la page [Vue d’ensemble des modifications](./tools/cli-msbuild-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="ce4ad-177">For more information about the project format changes, see [High-level overview of changes](./tools/cli-msbuild-architecture.md).</span></span>
---

<a name="vs-mapping"></a>

> [!TIP]
> <span data-ttu-id="ce4ad-178">Pour vérifier votre version de Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="ce4ad-178">To verify your Visual Studio 2017 version:</span></span>
>
> * <span data-ttu-id="ce4ad-179">Dans le menu **Aide**, choisissez **À propos de Microsoft Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-179">On the **Help** menu, choose **About Microsoft Visual Studio**.</span></span>
> * <span data-ttu-id="ce4ad-180">Dans la boîte de dialogue **À propos de Microsoft Visual Studio**, vérifiez le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-180">In the **About Microsoft Visual Studio** dialog, verify the version number.</span></span>
>   * <span data-ttu-id="ce4ad-181">Pour les applications .NET Core 2.2 Preview 1, Visual Studio 2017 version 15.9 (disponible en préversion) ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-181">For .NET Core 2.2 Preview 1 apps, Visual Studio 2017 version 15.9 (currently in Preview) or higher.</span></span>
>   * <span data-ttu-id="ce4ad-182">Pour les applications .NET Core 2.1, Visual Studio 2017 version 15.7 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-182">For .NET Core 2.1 apps, Visual Studio 2017 version 15.7 or higher.</span></span>
>   * <span data-ttu-id="ce4ad-183">Pour les applications .NET Core 2.0, Visual Studio 2017 version 15.3 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-183">For .NET Core 2.0 apps, Visual Studio 2017 version 15.3 or higher.</span></span>
>   * <span data-ttu-id="ce4ad-184">Pour les applications .NET Core 1.x, Visual Studio 2017 version 15.0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ce4ad-184">For .NET Core 1.x apps, Visual Studio 2017 version 15.0 or higher.</span></span>
