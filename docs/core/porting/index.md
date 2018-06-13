---
title: Portage vers .NET Core à partir du .NET Framework
description: Présentation du processus de portage et d’outils qui peuvent s’avérer utiles lors du portage d’un projet .NET Framework vers .NET Core.
author: cartermp
ms.author: mairaw
ms.date: 06/20/2016
ms.openlocfilehash: bf4f50ca915f21cdda6b99ae6bdf9e837eca3ae7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33210080"
---
# <a name="porting-to-net-core-from-net-framework"></a><span data-ttu-id="d663d-103">Portage vers .NET Core à partir du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="d663d-103">Porting to .NET Core from .NET Framework</span></span>

<span data-ttu-id="d663d-104">Si vous avez un code s’exécutant sur le .NET Framework, vous pouvez être intéressé par l’exécution de votre code sur .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="d663d-104">If you've got code running on the .NET Framework, you may be interested in running your code on .NET Core 1.0.</span></span>  <span data-ttu-id="d663d-105">Cet article contient une vue d’ensemble du processus de portage et une liste des outils que peuvent s’avérer utiles lors du portage vers .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d663d-105">This article covers an overview of the porting process and a list of the tools you may find helpful when porting to .NET Core.</span></span>

## <a name="overview-of-the-porting-process"></a><span data-ttu-id="d663d-106">Vue d’ensemble du processus de portage</span><span class="sxs-lookup"><span data-stu-id="d663d-106">Overview of the Porting Process</span></span>

<span data-ttu-id="d663d-107">Le processus recommandé pour le portage est constitué de la série d’étapes suivante.</span><span class="sxs-lookup"><span data-stu-id="d663d-107">The recommended process for porting follows the following series of steps.</span></span>  <span data-ttu-id="d663d-108">Chacune de ces parties du processus est traitée plus en détail dans d’autres articles.</span><span class="sxs-lookup"><span data-stu-id="d663d-108">Each of these parts of the process are covered in more detail in further articles.</span></span>

1. <span data-ttu-id="d663d-109">Identifiez et considérez vos dépendances tierces.</span><span class="sxs-lookup"><span data-stu-id="d663d-109">Identify and account for your third-party dependencies.</span></span>

   <span data-ttu-id="d663d-110">Ceci implique de comprendre ce que sont vos dépendances tierces, comment vous en dépendez, comment faire pour voir si elles s’exécutent aussi sur .NET Core, ainsi que les étapes à réaliser si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="d663d-110">This will involve understanding what your third-party dependencies are, how you depend on them, how to see if they also run on .NET Core, and steps you can take if they don't.</span></span>
   
2. <span data-ttu-id="d663d-111">Reciblez tous les projets que vous voulez porter pour cibler le .NET Framework 4.6.2.</span><span class="sxs-lookup"><span data-stu-id="d663d-111">Retarget all projects you wish to port to target .NET Framework 4.6.2.</span></span>

   <span data-ttu-id="d663d-112">Cela garantit que vous pouvez utiliser des API alternatives pour des cibles spécifiques au .NET Framework dans les cas où .NET Core ne peut pas prendre en charge une API particulière.</span><span class="sxs-lookup"><span data-stu-id="d663d-112">This ensures that you can use API alternatives for .NET Framework-specific targets in the cases where .NET Core can't support a particular API.</span></span>
   
3. <span data-ttu-id="d663d-113">Utilisez l’[outil API Portability Analyzer](https://github.com/Microsoft/dotnet-apiport/) pour analyser vos assemblys et développer un plan pour réaliser le portage en fonction de ses résultats.</span><span class="sxs-lookup"><span data-stu-id="d663d-113">Use the [API Portability Analyzer tool](https://github.com/Microsoft/dotnet-apiport/) to analyze your assemblies and develop a plan to port based on its results.</span></span>

   <span data-ttu-id="d663d-114">L’outil API Portability Analyzer analyse vos assemblys compilés et génère un rapport qui présente résumé de portabilité générale, et une analyse de chaque API que vous utilisez et qui n’est pas disponible sur .NET Core.</span><span class="sxs-lookup"><span data-stu-id="d663d-114">The API Portability Analyzer tool will analyze your compiled assemblies and generate a report which shows a high-level portability summary and a breakdown of each API you're using that isn't available on .NET Core.</span></span>  <span data-ttu-id="d663d-115">Vous pouvez utiliser ce rapport parallèlement à une analyse de votre code base pour développer un plan de la façon dont vous allez porter votre code.</span><span class="sxs-lookup"><span data-stu-id="d663d-115">You can use this report alongside an analysis of your codebase to develop a plan for how you'll port your code over.</span></span>
   
4. <span data-ttu-id="d663d-116">Porter le code de vos tests.</span><span class="sxs-lookup"><span data-stu-id="d663d-116">Port your tests code.</span></span>

   <span data-ttu-id="d663d-117">Le portage vers .NET Core représentant un grand changement pour votre code base, il est fortement recommandé de porter vos tests, pour pouvoir exécuter des tests au fil du portage du code.</span><span class="sxs-lookup"><span data-stu-id="d663d-117">Because porting to .NET Core is such a big change to your codebase, it's highly recommended to get your tests ported so that you can run tests as you port code over.</span></span>  <span data-ttu-id="d663d-118">MSTest, xUnit et NUnit prennent tous actuellement en charge .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="d663d-118">MSTest, xUnit, and NUnit all support .NET Core 1.0 today.</span></span>
   
6. <span data-ttu-id="d663d-119">Exécutez votre plan de portage !</span><span class="sxs-lookup"><span data-stu-id="d663d-119">Execute your plan for porting!</span></span>

## <a name="tools-to-help"></a><span data-ttu-id="d663d-120">Outils pour vous aider</span><span class="sxs-lookup"><span data-stu-id="d663d-120">Tools to help</span></span>

<span data-ttu-id="d663d-121">Voici une courte liste des outils qui peuvent vous être utiles :</span><span class="sxs-lookup"><span data-stu-id="d663d-121">Here's a short list of the tools you'll find helpful:</span></span>

* <span data-ttu-id="d663d-122">NuGet - [Client NuGet](https://dist.nuget.org/index.html) ou [Explorateur de package NuGet](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer), Gestionnaire de package de Microsoft pour les implémentations .NET.</span><span class="sxs-lookup"><span data-stu-id="d663d-122">NuGet - [Nuget Client](https://dist.nuget.org/index.html) or [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer), Microsoft's package manager for .NET implementations.</span></span>
* <span data-ttu-id="d663d-123">API Portability Analyzer - [Outil de ligne de commande](https://github.com/Microsoft/dotnet-apiport/releases) ou [Extension Visual Studio](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b), une chaîne d’outils qui permet de générer un rapport sur la portabilité de votre code entre le .NET Framework et .NET Core, avec une analyse des problèmes par assembly.</span><span class="sxs-lookup"><span data-stu-id="d663d-123">Api Portability Analyzer - [command line tool](https://github.com/Microsoft/dotnet-apiport/releases) or [Visual Studio Extension](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b), a toolchain that can generate a report of how portable your code is between .NET Framework and .NET Core, with an assembly-by-assembly breakdown of issues.</span></span>  <span data-ttu-id="d663d-124">Pour plus d’informations, consultez [Outils pour vous aider dans le processus](https://github.com/Microsoft/dotnet-apiport/blob/master/docs/HowTo/).</span><span class="sxs-lookup"><span data-stu-id="d663d-124">See [Tooling to help you on the process](https://github.com/Microsoft/dotnet-apiport/blob/master/docs/HowTo/) for more information.</span></span>
* <span data-ttu-id="d663d-125">Reverse Package Search - A [service web pratique](https://packagesearch.azurewebsites.net) qui vous permet de rechercher un type et de trouver des packages contenant ce type.</span><span class="sxs-lookup"><span data-stu-id="d663d-125">Reverse Package Search - A [useful web service](https://packagesearch.azurewebsites.net) that allows you to search for a type and find packages containing that type.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d663d-126">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d663d-126">Next steps</span></span>

[<span data-ttu-id="d663d-127">Analyse de vos dépendances tierces.</span><span class="sxs-lookup"><span data-stu-id="d663d-127">Analyzing your third-party dependencies.</span></span>](third-party-deps.md)
   
