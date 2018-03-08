---
title: Configuration requise pour .NET Core sur Windows
description: "Découvrez les dépendances nécessaires sur votre machine Windows pour développer et exécuter des applications .NET Core."
author: JRAlexander
ms.author: johalex
ms.date: 02/28/2018
ms.topic: article
ms.prod: .net-core
ms.workload:
- dotnetcore
ms.openlocfilehash: e64ecb807fd377458a9998ebbdfe2f6f15b115bb
ms.sourcegitcommit: ba765893e3efcece67d99fd6d5ce0074b050d1d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2018
---
# <a name="prerequisites-for-net-core-on-windows"></a><span data-ttu-id="d843d-103">Configuration requise pour .NET Core sur Windows</span><span class="sxs-lookup"><span data-stu-id="d843d-103">Prerequisites for .NET Core on Windows</span></span>

<span data-ttu-id="d843d-104">Cet article montre les dépendances nécessaires pour développer des applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="d843d-104">This article shows the dependencies needed to develop .NET Core applications on Windows.</span></span> <span data-ttu-id="d843d-105">Les versions de système d’exploitation et les dépendances prises en charge ci-après s’appliquent aux trois façons de développer des applications .NET Core sur Windows :</span><span class="sxs-lookup"><span data-stu-id="d843d-105">The supported OS versions and dependencies that follow apply to the three ways of developing .NET Core apps on Windows:</span></span>

* [<span data-ttu-id="d843d-106">Ligne de commande</span><span class="sxs-lookup"><span data-stu-id="d843d-106">Command line</span></span>](tutorials/using-with-xplat-cli.md)
* [<span data-ttu-id="d843d-107">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="d843d-107">Visual Studio 2017</span></span>](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)
* [<span data-ttu-id="d843d-108">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="d843d-108">Visual Studio Code</span></span>](https://code.visualstudio.com/)

## <a name="net-core-supported-windows-versions"></a><span data-ttu-id="d843d-109">Versions Windows prises en charge par .NET Core</span><span class="sxs-lookup"><span data-stu-id="d843d-109">.NET Core supported Windows versions</span></span>

<span data-ttu-id="d843d-110">.NET Core est pris en charge par les versions suivantes de :</span><span class="sxs-lookup"><span data-stu-id="d843d-110">.NET Core is supported on the following versions of:</span></span>

* <span data-ttu-id="d843d-111">Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="d843d-111">Windows 7 SP1</span></span>
* <span data-ttu-id="d843d-112">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d843d-112">Windows 8.1</span></span>
* <span data-ttu-id="d843d-113">Mise à jour anniversaire Windows 10 (version 1607) ou ultérieur</span><span class="sxs-lookup"><span data-stu-id="d843d-113">Windows 10 Anniversary Update (version 1607) or later versions</span></span>
* <span data-ttu-id="d843d-114">Windows Server 2008 R2 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="d843d-114">Windows Server 2008 R2 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="d843d-115">Windows Server 2012 SP1 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="d843d-115">Windows Server 2012 SP1 (Full Server or Server Core)</span></span>
* <span data-ttu-id="d843d-116">Windows Server 2012 R2 (version complète ou Server Core)</span><span class="sxs-lookup"><span data-stu-id="d843d-116">Windows Server 2012 R2 (Full Server or Server Core)</span></span>
* <span data-ttu-id="d843d-117">Windows Server 2016 (version complète, Server Core ou Nano Server)</span><span class="sxs-lookup"><span data-stu-id="d843d-117">Windows Server 2016 (Full Server, Server Core, or Nano Server)</span></span>

<span data-ttu-id="d843d-118">Consultez [.NET Core 2.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 2.x.</span><span class="sxs-lookup"><span data-stu-id="d843d-118">See [.NET Core 2.x - Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) for the complete list of .NET Core 2.x supported operating systems.</span></span>

<span data-ttu-id="d843d-119">Consultez [.NET Core 1.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="d843d-119">See [.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) for the complete list of .NET Core 1.x supported operating systems.</span></span>

## <a name="net-core-dependencies"></a><span data-ttu-id="d843d-120">Dépendances .NET Core</span><span class="sxs-lookup"><span data-stu-id="d843d-120">.NET Core dependencies</span></span>

<span data-ttu-id="d843d-121">.NET Core 1.1 et ses versions antérieures nécessitent le package redistribuable Visual C++ lors de l’exécution sur des versions de Windows antérieures à Windows 10 et Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d843d-121">.NET Core 1.1 and earlier versions require the Visual C++ Redistributable when running on Windows versions earlier than Windows 10 and Windows Server 2016.</span></span> <span data-ttu-id="d843d-122">Cette dépendance est installée automatiquement par le programme d’installation de .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d843d-122">This dependency is automatically installed by the .NET Core installer.</span></span>

<span data-ttu-id="d843d-123">Vous devez installer [Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) manuellement quand :</span><span class="sxs-lookup"><span data-stu-id="d843d-123">[Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) must be manually installed when:</span></span>

* <span data-ttu-id="d843d-124">vous installez .NET Core avec le [script du programme d’installation](./tools/dotnet-install-script.md) ;</span><span class="sxs-lookup"><span data-stu-id="d843d-124">Installing .NET Core with the [installer script](./tools/dotnet-install-script.md).</span></span>
* <span data-ttu-id="d843d-125">vous déployez une application .NET Core autonome.</span><span class="sxs-lookup"><span data-stu-id="d843d-125">Deploying a self-contained .NET Core application.</span></span>
* <span data-ttu-id="d843d-126">Génération du produit à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="d843d-126">Building the product from source.</span></span>
* <span data-ttu-id="d843d-127">Installation de .NET Core via un fichier *.zip*.</span><span class="sxs-lookup"><span data-stu-id="d843d-127">Installing .NET Core via a *.zip* file.</span></span> <span data-ttu-id="d843d-128">Ceci peut inclure des serveurs de builds/CI/CD.</span><span class="sxs-lookup"><span data-stu-id="d843d-128">This can include build/CI/CD servers.</span></span>

> [!NOTE]
> <span data-ttu-id="d843d-129">*Pour les machines Windows 7 et Windows Server 2008 seulement :* vérifiez que votre installation Windows est à jour et que le correctif logiciel [KB2533623](https://support.microsoft.com/help/2533623) y est installé via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="d843d-129">*For Windows 7 and Windows Server 2008 machines only:* Make sure that your Windows installation is up-to-date and includes hotfix [KB2533623](https://support.microsoft.com/help/2533623) installed through Windows Update.</span></span>

## <a name="prerequisites-with-visual-studio-2017"></a><span data-ttu-id="d843d-130">Prérequis pour Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="d843d-130">Prerequisites with Visual Studio 2017</span></span>

<span data-ttu-id="d843d-131">Vous pouvez utiliser l’éditeur de votre choix pour développer des applications .NET Core à l’aide du Kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d843d-131">You can use any editor to develop .NET Core applications using the .NET Core SDK.</span></span> <span data-ttu-id="d843d-132">[Visual Studio 2017](#visual-studio-2017) fournit un environnement de développement intégré pour les applications .NET Core sur Windows.</span><span class="sxs-lookup"><span data-stu-id="d843d-132">[Visual Studio 2017](#visual-studio-2017) provides an integrated development environment for .NET Core apps on Windows.</span></span>

<span data-ttu-id="d843d-133">Vous trouverez plus d’informations sur les modifications apportées à Visual Studio 2017 dans les [notes de publication](/visualstudio/releasenotes/vs2017-relnotes).</span><span class="sxs-lookup"><span data-stu-id="d843d-133">You can read more about the changes in Visual Studio 2017 in the [release notes](/visualstudio/releasenotes/vs2017-relnotes).</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="d843d-134">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="d843d-134">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="d843d-135">Pour développer des applications .NET Core 2.x dans Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="d843d-135">To develop .NET Core 2.x apps in Visual Studio 2017:</span></span>

 1. <span data-ttu-id="d843d-136">[Téléchargez et installez Visual Studio 2017 version 15.3.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="d843d-136">[Download and install Visual Studio 2017 version 15.3.0 or higher](/visualstudio/install/install-visual-studio) with the **.NET Core cross-platform development** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-3-workloads.jpg)

<span data-ttu-id="d843d-138">Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, Visual Studio 2017 utilise .NET Core 1.x par défaut.</span><span class="sxs-lookup"><span data-stu-id="d843d-138">After the **.NET Core cross-platform development** toolset is installed, Visual Studio 2017 uses .NET Core 1.x by default.</span></span> <span data-ttu-id="d843d-139">Installez le SDK .NET Core 2.x pour obtenir la prise en charge de .NET Core 2.x dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="d843d-139">Install the .NET Core 2.x SDK to get .NET Core 2.x support in Visual Studio 2017.</span></span>

 2. <span data-ttu-id="d843d-140">Installez le [SDK .NET Core 2.x](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="d843d-140">Install the [.NET Core 2.x SDK](https://www.microsoft.com/net/download/core).</span></span>
 3. <span data-ttu-id="d843d-141">Reciblez les projets .NET Core 1.x existants ou nouveaux sur .NET Core 2.x en suivant les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d843d-141">Retarget existing or new .NET Core 1.x projects to .NET Core 2.x using the following instructions:</span></span>
    * <span data-ttu-id="d843d-142">Dans le menu **Projet**, choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d843d-142">On the **Project** menu, Choose **Properties**.</span></span>
    * <span data-ttu-id="d843d-143">Dans le menu de sélection **framework cible**, choisissez **.NET Core 2.0**.</span><span class="sxs-lookup"><span data-stu-id="d843d-143">In the **Target framework** selection menu, set the value to **.NET Core 2.0**.</span></span>

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

<span data-ttu-id="d843d-145">Une fois installé le SDK .NET Core 2.x, Visual Studio 2017 l’utilise par défaut et prend en charge les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d843d-145">Once the .NET Core 2.x SDK is installed, Visual Studio 2017 uses the .NET Core SDK 2.x by default, and supports the following actions:</span></span>

* <span data-ttu-id="d843d-146">Ouvrir, générer et exécuter les projets .NET Core 1.x existants.</span><span class="sxs-lookup"><span data-stu-id="d843d-146">Open, build, and run existing .NET Core 1.x projects.</span></span>
* <span data-ttu-id="d843d-147">Recibler les projets .NET Core 1.x vers .NET Core 2.x, les générer et les exécuter.</span><span class="sxs-lookup"><span data-stu-id="d843d-147">Retarget .NET Core 1.x projects to .NET Core 2.x, build, and run.</span></span>
* <span data-ttu-id="d843d-148">Créer des projets .NET Core 2.x.</span><span class="sxs-lookup"><span data-stu-id="d843d-148">Create new .NET Core 2.x projects.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="d843d-149">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="d843d-149">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="d843d-150">Pur développer des applications .NET Core 1.x dans Visual Studio, [téléchargez et installez Visual Studio 2017 RTM (version 15.0.26228.4) ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).</span><span class="sxs-lookup"><span data-stu-id="d843d-150">To develop .NET Core 1.x apps in Visual Studio, [download and install Visual Studio 2017 RTM (version 15.0.26228.4) or higher](/visualstudio/install/install-visual-studio) with the **".NET Core cross-platform development"** workload (in the **Other Toolsets** section) selected.</span></span>

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs_workloads.jpg)

> [!IMPORTANT]
> <span data-ttu-id="d843d-152">Bien que vous puissiez utiliser Visual Studio 2015 pour le développement .NET Core 1.x, nous vous le déconseillons pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="d843d-152">It's possible to use Visual Studio 2015 for .NET Core 1.x development, but it's not recommended for the following reasons:</span></span>
  > * <span data-ttu-id="d843d-153">Les outils .NET Core sont une préversion, qui n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d843d-153">The .NET Core tooling is a preview version, which is not supported.</span></span>
  > * <span data-ttu-id="d843d-154">Les projets sont basés sur project.json, configuration qui est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="d843d-154">The projects are project.json-based, which is deprecated.</span></span>
>
> <span data-ttu-id="d843d-155">Pour plus d’informations sur les changements de format de projet, consultez la page [Vue d’ensemble des modifications](./tools/cli-msbuild-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="d843d-155">For more information about the project format changes, see [High-level overview of changes](./tools/cli-msbuild-architecture.md).</span></span>
---

> [!TIP]
> <span data-ttu-id="d843d-156">Pour vérifier votre version de Visual Studio 2017 :</span><span class="sxs-lookup"><span data-stu-id="d843d-156">To verify your Visual Studio 2017 version:</span></span>
>
> * <span data-ttu-id="d843d-157">Dans le menu **Aide**, choisissez **À propos de Microsoft Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="d843d-157">On the **Help** menu, choose **About Microsoft Visual Studio**.</span></span>
> * <span data-ttu-id="d843d-158">Dans la boîte de dialogue **À propos de Microsoft Visual Studio**, vérifiez le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="d843d-158">In the **About Microsoft Visual Studio** dialog, verify the version number.</span></span>
>   * <span data-ttu-id="d843d-159">Pour les applications .NET Core 2.x, Visual Studio 2017 version 15.3 (26730.01) ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d843d-159">For .NET Core 2.x apps, Visual Studio 2017 version 15.3 (26730.01) or higher.</span></span>
>   * <span data-ttu-id="d843d-160">Pour les applications .NET Core 1.x, Visual Studio 2017 version 15.0 (26228.04) ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d843d-160">For .NET Core 1.x apps, Visual Studio 2017 version 15.0 (26228.04) or higher.</span></span>
