---
title: Organiser des projets pour .NET Framework et .NET Core
description: Aide destinée aux propriétaires de projet qui souhaitent compiler leur solution côte à côte pour le .NET Framework et .NET Core.
author: conniey
ms.author: mairaw
ms.date: 04/06/2017
ms.custom: seodec18
ms.openlocfilehash: cfb3670bda887792389c7cee3f65397e649304d5
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53146925"
---
# <a name="organize-your-project-to-support-both-net-framework-and-net-core"></a><span data-ttu-id="9d301-103">Organiser votre projet pour prendre en charge à la fois le .NET Framework et .NET Core</span><span class="sxs-lookup"><span data-stu-id="9d301-103">Organize your project to support both .NET Framework and .NET Core</span></span>

<span data-ttu-id="9d301-104">Découvrez comment créer une solution qui se compile parallèlement pour .NET Framework et .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9d301-104">Learn how to create a solution that compiles for both .NET Framework and .NET Core side-by-side.</span></span> <span data-ttu-id="9d301-105">Découvrez plusieurs options pour organiser les projets de façon à vous aider à atteindre cet objectif.</span><span class="sxs-lookup"><span data-stu-id="9d301-105">See several options to organize projects to help you achieve this goal.</span></span> <span data-ttu-id="9d301-106">Voici quelques scénarios classiques à prendre en compte quand vous devez décider comment configurer la disposition de votre projet avec .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9d301-106">Here are some typical scenarios to consider when you're deciding how to setup your project layout with .NET Core.</span></span> <span data-ttu-id="9d301-107">La liste peut ne pas couvrir tout ce que vous souhaitez : établissez vos priorités en fonction des besoins de votre projet.</span><span class="sxs-lookup"><span data-stu-id="9d301-107">The list may not cover everything you want; prioritize based on your project's needs.</span></span>

* <span data-ttu-id="9d301-108">[**Combiner des projets existants et des projets .NET Core en projets uniques**][option-csproj]</span><span class="sxs-lookup"><span data-stu-id="9d301-108">[**Combine existing projects and .NET Core projects into single projects**][option-csproj]</span></span>

  <span data-ttu-id="9d301-109">*En voici les avantages :*</span><span class="sxs-lookup"><span data-stu-id="9d301-109">*What this is good for:*</span></span>
  * <span data-ttu-id="9d301-110">Simplification de votre processus de génération : compilation d’un seul projet au lieu de plusieurs, chacun ciblant une version du .NET Framework ou une plateforme différente.</span><span class="sxs-lookup"><span data-stu-id="9d301-110">Simplifying your build process by compiling a single project rather than compiling multiple projects, each targeting a different .NET Framework version or platform.</span></span>
  * <span data-ttu-id="9d301-111">Simplification de la gestion des fichiers sources pour les projets multiciblés car vous devez gérez un seul fichier projet.</span><span class="sxs-lookup"><span data-stu-id="9d301-111">Simplifying source file management for multi-targeted projects because you must manage a single project file.</span></span> <span data-ttu-id="9d301-112">Lors de l’ajout/suppression de fichiers sources, les alternatives vous obligent à synchroniser manuellement ces fichiers avec vos autres projets.</span><span class="sxs-lookup"><span data-stu-id="9d301-112">When adding/removing source files, the alternatives require you to manually sync these with your other projects.</span></span>
  * <span data-ttu-id="9d301-113">Génération facile d’un package NuGet à consommer.</span><span class="sxs-lookup"><span data-stu-id="9d301-113">Easily generating a NuGet package for consumption.</span></span>
  * <span data-ttu-id="9d301-114">Vous permet d’écrire du code pour une version spécifique du .NET Framework dans vos bibliothèques via l’utilisation de directives de compilation.</span><span class="sxs-lookup"><span data-stu-id="9d301-114">Allows you to write code for a specific .NET Framework version in your libraries through the use of compiler directives.</span></span>

  <span data-ttu-id="9d301-115">*Scénarios non pris en charge :*</span><span class="sxs-lookup"><span data-stu-id="9d301-115">*Unsupported scenarios:*</span></span>
  * <span data-ttu-id="9d301-116">Demander aux développeurs d’utiliser Visual Studio 2017 pour ouvrir des projets existants.</span><span class="sxs-lookup"><span data-stu-id="9d301-116">Requires developers to use Visual Studio 2017 to open existing projects.</span></span> <span data-ttu-id="9d301-117">Pour prendre en charge les versions antérieures de Visual Studio, [conserver vos fichiers projet dans des dossiers différents](#support-vs) est une meilleure option.</span><span class="sxs-lookup"><span data-stu-id="9d301-117">To support older versions of Visual Studio, [keeping your project files in different folders](#support-vs) is a better option.</span></span>

* <a name="support-vs"></a><span data-ttu-id="9d301-118">[**Séparer les projets existants des nouveaux projets .NET Core**][option-csproj-folder]</span><span class="sxs-lookup"><span data-stu-id="9d301-118">[**Keep existing projects and new .NET Core projects separate**][option-csproj-folder]</span></span>

  <span data-ttu-id="9d301-119">*En voici les avantages :*</span><span class="sxs-lookup"><span data-stu-id="9d301-119">*What this is good for:*</span></span>
  * <span data-ttu-id="9d301-120">Continuation de la prise en charge du développement de projets existants sans devoir mettre à niveau pour les développeurs/contributeurs qui n’ont pas Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="9d301-120">Continuing to support development on existing projects without having to upgrade for developers/contributors who may not have Visual Studio 2017.</span></span>
  * <span data-ttu-id="9d301-121">Réduction du risque de création de bogues dans des projets existants car aucune évolution du code n’est nécessaire dans ces projets.</span><span class="sxs-lookup"><span data-stu-id="9d301-121">Decreasing the possibility of creating new bugs in existing projects because no code churn is required in those projects.</span></span>

## <a name="example"></a><span data-ttu-id="9d301-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="9d301-122">Example</span></span>

<span data-ttu-id="9d301-123">Considérez le dépôt ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9d301-123">Consider the repository below:</span></span>

<span data-ttu-id="9d301-124">![Projet existant][example-initial-project]</span><span class="sxs-lookup"><span data-stu-id="9d301-124">![Existing project][example-initial-project]</span></span>

<span data-ttu-id="9d301-125">[**Code source**][example-initial-project-code]</span><span class="sxs-lookup"><span data-stu-id="9d301-125">[**Source Code**][example-initial-project-code]</span></span>

<span data-ttu-id="9d301-126">La section suivante décrit plusieurs méthodes pour ajouter la prise en charge de .NET Core pour ce dépôt en fonction des contraintes et de la complexité des projets existants.</span><span class="sxs-lookup"><span data-stu-id="9d301-126">The following describes several ways to add support for .NET Core for this repository depending on the constraints and complexity of the existing projects.</span></span>

## <a name="replace-existing-projects-with-a-multi-targeted-net-core-project"></a><span data-ttu-id="9d301-127">Remplacer les projets existants par un projet .NET Core multiciblé</span><span class="sxs-lookup"><span data-stu-id="9d301-127">Replace existing projects with a multi-targeted .NET Core project</span></span>

<span data-ttu-id="9d301-128">Réorganisez le dépôt de sorte que tous les fichiers *\*.csproj* existants soient supprimés et qu’un seul fichier *\*.csproj* ciblant plusieurs frameworks soit créé.</span><span class="sxs-lookup"><span data-stu-id="9d301-128">Reorganize the repository so that any existing *\*.csproj* files are removed and a single *\*.csproj* file is created that targets multiple frameworks.</span></span> <span data-ttu-id="9d301-129">Il s’agit d’une option intéressante car un même projet peut être compilé pour différents frameworks.</span><span class="sxs-lookup"><span data-stu-id="9d301-129">This is a great option because a single project is able to compile for different frameworks.</span></span> <span data-ttu-id="9d301-130">Elle permet également de gérer différentes options de compilation et dépendances par framework ciblé.</span><span class="sxs-lookup"><span data-stu-id="9d301-130">It also has the power to handle different compilation options and dependencies per targeted framework.</span></span>

<span data-ttu-id="9d301-131">![Créer un csproj ciblant plusieurs frameworks][example-csproj]</span><span class="sxs-lookup"><span data-stu-id="9d301-131">![Create an csproj that targets multiple frameworks][example-csproj]</span></span>

<span data-ttu-id="9d301-132">[**Code source**][example-csproj-code]</span><span class="sxs-lookup"><span data-stu-id="9d301-132">[**Source Code**][example-csproj-code]</span></span>

<span data-ttu-id="9d301-133">Les modifications à noter sont :</span><span class="sxs-lookup"><span data-stu-id="9d301-133">Changes to note are:</span></span>

* <span data-ttu-id="9d301-134">Remplacement de *packages.config* et de *\*.csproj* par un nouveau [.csproj *\*.NET Core*][example-csproj-netcore].</span><span class="sxs-lookup"><span data-stu-id="9d301-134">Replacement of *packages.config* and *\*.csproj* with a new [.NET Core *\*.csproj*][example-csproj-netcore].</span></span> <span data-ttu-id="9d301-135">Les packages NuGet sont spécifiés avec `<PackageReference> ItemGroup`.</span><span class="sxs-lookup"><span data-stu-id="9d301-135">NuGet packages are specified with `<PackageReference> ItemGroup`.</span></span>

## <a name="keep-existing-projects-and-create-a-net-core-project"></a><span data-ttu-id="9d301-136">Conserver les projets existants et créer un projet .NET Core</span><span class="sxs-lookup"><span data-stu-id="9d301-136">Keep existing projects and create a .NET Core project</span></span>

<span data-ttu-id="9d301-137">Si des projets existants ciblent des frameworks plus anciens, vous pouvez laisser ces projets inchangés et utiliser un projet .NET Core pour cibler les futurs frameworks.</span><span class="sxs-lookup"><span data-stu-id="9d301-137">If there are existing projects that target older frameworks, you may want to leave these projects untouched and use a .NET Core project to target future frameworks.</span></span>

<span data-ttu-id="9d301-138">![Projet .NET Core avec un projet existant dans un dossier différent][example-csproj-different-folder]</span><span class="sxs-lookup"><span data-stu-id="9d301-138">![.NET Core project with existing project in different folder][example-csproj-different-folder]</span></span>

<span data-ttu-id="9d301-139">[**Code source**][example-csproj-different-code]</span><span class="sxs-lookup"><span data-stu-id="9d301-139">[**Source Code**][example-csproj-different-code]</span></span>

<span data-ttu-id="9d301-140">Les modifications à noter sont :</span><span class="sxs-lookup"><span data-stu-id="9d301-140">Changes to note are:</span></span>

* <span data-ttu-id="9d301-141">Le projet .NET Core et les projets existants sont conservés dans des dossiers distincts.</span><span class="sxs-lookup"><span data-stu-id="9d301-141">The .NET Core and existing projects are kept in separate folders.</span></span>
  * <span data-ttu-id="9d301-142">Le fait de conserver les projets dans des dossiers distincts vous évite de devoir installer Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="9d301-142">Keeping projects in separate folders avoids forcing you to have Visual Studio 2017.</span></span> <span data-ttu-id="9d301-143">Vous pouvez créer une solution distincte qui ouvre seulement les anciens projets.</span><span class="sxs-lookup"><span data-stu-id="9d301-143">You can create a separate solution that only opens the old projects.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d301-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d301-144">See Also</span></span>

* <span data-ttu-id="9d301-145">Consultez la [documentation relative au portage vers .NET Core][porting-doc] pour obtenir de l’aide sur la migration vers .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9d301-145">Please see the [.NET Core porting documentation][porting-doc] for more guidance on migrating to .NET Core.</span></span>

[porting-doc]: index.md
[example-initial-project]: media/project-structure/project.png "Projet existant"
[example-initial-project-code]: https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library/

[example-csproj]: media/project-structure/project.csproj.png "Créer un csproj ciblant plusieurs frameworks"
[example-csproj-code]: https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/
[example-csproj-netcore]: https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj/src/Car/Car.csproj

[example-csproj-different-folder]: media/project-structure/project.csproj.different.png "Projet .NET Core avec une bibliothèque de classes portable dans un dossier différent"
[example-csproj-different-code]: https://github.com/dotnet/samples/tree/master/framework/libraries/migrate-library-csproj-keep-existing/

[option-csproj]: #replace-existing-projects-with-a-multi-targeted-net-core-project
[option-csproj-folder]: #keep-existing-projects-and-create-a-net-core-project
