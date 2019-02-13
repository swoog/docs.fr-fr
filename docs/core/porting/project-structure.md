---
title: Organiser des projets pour .NET Framework et .NET Core
description: Aide destinée aux propriétaires de projet qui souhaitent compiler leur solution côte à côte pour le .NET Framework et .NET Core.
author: conniey
ms.date: 12/07/2018
ms.custom: seodec18
ms.openlocfilehash: 57bb766f1d91c502a508b6362dc642310009c8c4
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904021"
---
# <a name="organize-your-project-to-support-both-net-framework-and-net-core"></a><span data-ttu-id="7e136-103">Organiser votre projet pour prendre en charge à la fois le .NET Framework et .NET Core</span><span class="sxs-lookup"><span data-stu-id="7e136-103">Organize your project to support both .NET Framework and .NET Core</span></span>

<span data-ttu-id="7e136-104">Découvrez comment créer une solution qui se compile parallèlement pour .NET Framework et .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7e136-104">Learn how to create a solution that compiles for both .NET Framework and .NET Core side-by-side.</span></span> <span data-ttu-id="7e136-105">Découvrez plusieurs options pour organiser les projets de façon à vous aider à atteindre cet objectif.</span><span class="sxs-lookup"><span data-stu-id="7e136-105">See several options to organize projects to help you achieve this goal.</span></span> <span data-ttu-id="7e136-106">Voici quelques scénarios classiques à prendre en compte quand vous devez décider comment configurer la disposition de votre projet avec .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7e136-106">Here are some typical scenarios to consider when you're deciding how to setup your project layout with .NET Core.</span></span> <span data-ttu-id="7e136-107">La liste peut ne pas couvrir tout ce que vous souhaitez : établissez vos priorités en fonction des besoins de votre projet.</span><span class="sxs-lookup"><span data-stu-id="7e136-107">The list may not cover everything you want; prioritize based on your project's needs.</span></span>

* [<span data-ttu-id="7e136-108">**Combiner des projets existants et des projets .NET Core pour en faire des projets uniques**</span><span class="sxs-lookup"><span data-stu-id="7e136-108">**Combine existing projects and .NET Core projects into single projects**</span></span>](#replace-existing-projects-with-a-multi-targeted-net-core-project)

  <span data-ttu-id="7e136-109">*En voici les avantages :*</span><span class="sxs-lookup"><span data-stu-id="7e136-109">*What this is good for:*</span></span>
  * <span data-ttu-id="7e136-110">Simplification de votre processus de génération : compilation d’un seul projet au lieu de plusieurs, chacun ciblant une version du .NET Framework ou une plateforme différente.</span><span class="sxs-lookup"><span data-stu-id="7e136-110">Simplifying your build process by compiling a single project rather than compiling multiple projects, each targeting a different .NET Framework version or platform.</span></span>
  * <span data-ttu-id="7e136-111">Simplification de la gestion des fichiers sources pour les projets multiciblés car vous devez gérez un seul fichier projet.</span><span class="sxs-lookup"><span data-stu-id="7e136-111">Simplifying source file management for multi-targeted projects because you must manage a single project file.</span></span> <span data-ttu-id="7e136-112">Lors de l’ajout/suppression de fichiers sources, les alternatives vous obligent à synchroniser manuellement ces fichiers avec vos autres projets.</span><span class="sxs-lookup"><span data-stu-id="7e136-112">When adding/removing source files, the alternatives require you to manually sync these with your other projects.</span></span>
  * <span data-ttu-id="7e136-113">Génération facile d’un package NuGet à consommer.</span><span class="sxs-lookup"><span data-stu-id="7e136-113">Easily generating a NuGet package for consumption.</span></span>
  * <span data-ttu-id="7e136-114">Vous permet d’écrire du code pour une version spécifique du .NET Framework dans vos bibliothèques via l’utilisation de directives de compilation.</span><span class="sxs-lookup"><span data-stu-id="7e136-114">Allows you to write code for a specific .NET Framework version in your libraries through the use of compiler directives.</span></span>

  <span data-ttu-id="7e136-115">*Scénarios non pris en charge :*</span><span class="sxs-lookup"><span data-stu-id="7e136-115">*Unsupported scenarios:*</span></span>
  * <span data-ttu-id="7e136-116">Demander aux développeurs d’utiliser Visual Studio 2017 pour ouvrir des projets existants.</span><span class="sxs-lookup"><span data-stu-id="7e136-116">Requires developers to use Visual Studio 2017 to open existing projects.</span></span> <span data-ttu-id="7e136-117">Pour prendre en charge les versions antérieures de Visual Studio, [conserver vos fichiers projet dans des dossiers différents](#support-vs) est une meilleure option.</span><span class="sxs-lookup"><span data-stu-id="7e136-117">To support older versions of Visual Studio, [keeping your project files in different folders](#support-vs) is a better option.</span></span>

* <a name="support-vs"></a><span data-ttu-id="7e136-118">[**Séparer les projets existants des nouveaux projets .NET Core**](#keep-existing-projects-and-create-a-net-core-project)</span><span class="sxs-lookup"><span data-stu-id="7e136-118">[**Keep existing projects and new .NET Core projects separate**](#keep-existing-projects-and-create-a-net-core-project)</span></span>

  <span data-ttu-id="7e136-119">*En voici les avantages :*</span><span class="sxs-lookup"><span data-stu-id="7e136-119">*What this is good for:*</span></span>
  * <span data-ttu-id="7e136-120">Continuation de la prise en charge du développement de projets existants sans devoir mettre à niveau pour les développeurs/contributeurs qui n’ont pas Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="7e136-120">Continuing to support development on existing projects without having to upgrade for developers/contributors who may not have Visual Studio 2017.</span></span>
  * <span data-ttu-id="7e136-121">Réduction du risque de création de bogues dans des projets existants car aucune évolution du code n’est nécessaire dans ces projets.</span><span class="sxs-lookup"><span data-stu-id="7e136-121">Decreasing the possibility of creating new bugs in existing projects because no code churn is required in those projects.</span></span>

## <a name="example"></a><span data-ttu-id="7e136-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="7e136-122">Example</span></span>

<span data-ttu-id="7e136-123">Considérez le dépôt ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7e136-123">Consider the repository below:</span></span>

![Projet existant](media/project-structure/project.png)

[<span data-ttu-id="7e136-125">**Code source**</span><span class="sxs-lookup"><span data-stu-id="7e136-125">**Source Code**</span></span>](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library/)

<span data-ttu-id="7e136-126">La section suivante décrit plusieurs méthodes pour ajouter la prise en charge de .NET Core pour ce dépôt en fonction des contraintes et de la complexité des projets existants.</span><span class="sxs-lookup"><span data-stu-id="7e136-126">The following describes several ways to add support for .NET Core for this repository depending on the constraints and complexity of the existing projects.</span></span>

## <a name="replace-existing-projects-with-a-multi-targeted-net-core-project"></a><span data-ttu-id="7e136-127">Remplacer les projets existants par un projet .NET Core multiciblé</span><span class="sxs-lookup"><span data-stu-id="7e136-127">Replace existing projects with a multi-targeted .NET Core project</span></span>

<span data-ttu-id="7e136-128">Réorganisez le dépôt de sorte que tous les fichiers *\*.csproj* existants soient supprimés et qu’un seul fichier *\*.csproj* ciblant plusieurs frameworks soit créé.</span><span class="sxs-lookup"><span data-stu-id="7e136-128">Reorganize the repository so that any existing *\*.csproj* files are removed and a single *\*.csproj* file is created that targets multiple frameworks.</span></span> <span data-ttu-id="7e136-129">Il s’agit d’une option intéressante car un même projet peut être compilé pour différents frameworks.</span><span class="sxs-lookup"><span data-stu-id="7e136-129">This is a great option because a single project is able to compile for different frameworks.</span></span> <span data-ttu-id="7e136-130">Elle permet également de gérer différentes options de compilation et dépendances par framework ciblé.</span><span class="sxs-lookup"><span data-stu-id="7e136-130">It also has the power to handle different compilation options and dependencies per targeted framework.</span></span>

![Créer un csproj qui cible plusieurs frameworks](media/project-structure/project.csproj.png)

[<span data-ttu-id="7e136-132">**Code source**</span><span class="sxs-lookup"><span data-stu-id="7e136-132">**Source Code**</span></span>](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/)

<span data-ttu-id="7e136-133">Les modifications à noter sont :</span><span class="sxs-lookup"><span data-stu-id="7e136-133">Changes to note are:</span></span>

* <span data-ttu-id="7e136-134">Remplacement de *packages.config* et de *\*.csproj* par un nouveau [.csproj *\*.NET Core*](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/src/Car/Car.csproj).</span><span class="sxs-lookup"><span data-stu-id="7e136-134">Replacement of *packages.config* and *\*.csproj* with a new [.NET Core *\*.csproj*](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/src/Car/Car.csproj).</span></span> <span data-ttu-id="7e136-135">Les packages NuGet sont spécifiés avec `<PackageReference> ItemGroup`.</span><span class="sxs-lookup"><span data-stu-id="7e136-135">NuGet packages are specified with `<PackageReference> ItemGroup`.</span></span>

## <a name="keep-existing-projects-and-create-a-net-core-project"></a><span data-ttu-id="7e136-136">Conserver les projets existants et créer un projet .NET Core</span><span class="sxs-lookup"><span data-stu-id="7e136-136">Keep existing projects and create a .NET Core project</span></span>

<span data-ttu-id="7e136-137">Si des projets existants ciblent des frameworks plus anciens, vous pouvez laisser ces projets inchangés et utiliser un projet .NET Core pour cibler les futurs frameworks.</span><span class="sxs-lookup"><span data-stu-id="7e136-137">If there are existing projects that target older frameworks, you may want to leave these projects untouched and use a .NET Core project to target future frameworks.</span></span>

![Projet .NET Core avec un projet existant dans un dossier différent](media/project-structure/project.csproj.different.png)

[<span data-ttu-id="7e136-139">**Code source**</span><span class="sxs-lookup"><span data-stu-id="7e136-139">**Source Code**</span></span>](https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj-keep-existing/)

<span data-ttu-id="7e136-140">Les modifications à noter sont :</span><span class="sxs-lookup"><span data-stu-id="7e136-140">Changes to note are:</span></span>

* <span data-ttu-id="7e136-141">Le projet .NET Core et les projets existants sont conservés dans des dossiers distincts.</span><span class="sxs-lookup"><span data-stu-id="7e136-141">The .NET Core and existing projects are kept in separate folders.</span></span>
  * <span data-ttu-id="7e136-142">Le fait de conserver les projets dans des dossiers distincts vous évite de devoir installer Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="7e136-142">Keeping projects in separate folders avoids forcing you to have Visual Studio 2017.</span></span> <span data-ttu-id="7e136-143">Vous pouvez créer une solution distincte qui ouvre seulement les anciens projets.</span><span class="sxs-lookup"><span data-stu-id="7e136-143">You can create a separate solution that only opens the old projects.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e136-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e136-144">See also</span></span>

<span data-ttu-id="7e136-145">Consultez la [documentation relative au portage vers .NET Core](index.md) pour obtenir des informations supplémentaires sur la migration vers .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7e136-145">Please see the [.NET Core porting documentation](index.md) for more guidance on migrating to .NET Core.</span></span>
