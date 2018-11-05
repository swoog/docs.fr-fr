---
title: Dépendances et bibliothèques .NET
description: Meilleures pratiques suggérées pour la gestion des dépendances NuGet dans les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: c5df30c606e77c9ef44387233b0072ab890f612f
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2018
ms.locfileid: "49400525"
---
# <a name="dependencies"></a><span data-ttu-id="c415c-103">Dépendances</span><span class="sxs-lookup"><span data-stu-id="c415c-103">Dependencies</span></span>

<span data-ttu-id="c415c-104">Le principal moyen d’ajouter des dépendances à une bibliothèque .NET est de référencer des packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="c415c-104">The primary way of adding dependencies to a .NET library is referencing NuGet packages.</span></span> <span data-ttu-id="c415c-105">Les références de packages NuGet vous permettent de réutiliser rapidement des fonctionnalités déjà écrites et d’en tirer parti , mais elles sont une source courante de friction pour les développeurs .NET.</span><span class="sxs-lookup"><span data-stu-id="c415c-105">NuGet package references allow you to quickly reuse and leverage already written functionality, but they're a common source of friction for .NET developers.</span></span> <span data-ttu-id="c415c-106">La gestion correcte des dépendances est importante pour empêcher des modifications dans d’autres bibliothèques .NET d’arrêter votre bibliothèque .NET et vice versa !</span><span class="sxs-lookup"><span data-stu-id="c415c-106">Correctly managing dependencies is important to prevent changes in other .NET libraries from breaking your .NET library, and vice versa!</span></span>

## <a name="diamond-dependencies"></a><span data-ttu-id="c415c-107">Dépendances en losange</span><span class="sxs-lookup"><span data-stu-id="c415c-107">Diamond dependencies</span></span>

<span data-ttu-id="c415c-108">Il est courant qu’un projet .NET ait plusieurs versions d’un package dans son arborescence des dépendances.</span><span class="sxs-lookup"><span data-stu-id="c415c-108">It's a common situation for a .NET project to have multiple versions of a package in its dependency tree.</span></span> <span data-ttu-id="c415c-109">Par exemple, une application dépend de deux packages NuGet dont chacun dépend de différentes versions du même package.</span><span class="sxs-lookup"><span data-stu-id="c415c-109">For example, an app depends on two NuGet packages, each of which depends on different versions of the same package.</span></span> <span data-ttu-id="c415c-110">Il y a désormais une dépendance en losange dans le graphique de dépendance de l’application.</span><span class="sxs-lookup"><span data-stu-id="c415c-110">A diamond dependency now exists in the app's dependency graph.</span></span>

<span data-ttu-id="c415c-111">![Dépendance en losange](./media/dependencies/diamond-dependency.png "Dépendance en losange")</span><span class="sxs-lookup"><span data-stu-id="c415c-111">![Diamond dependency](./media/dependencies/diamond-dependency.png "Diamond dependency")</span></span>

<span data-ttu-id="c415c-112">Lors du build, NuGet analyse tous les packages dont dépend un projet, y compris les dépendances de dépendances.</span><span class="sxs-lookup"><span data-stu-id="c415c-112">At build time, NuGet analyzes all the packages that a project depends on, including the dependencies of dependencies.</span></span> <span data-ttu-id="c415c-113">Lorsque plusieurs versions d’un package sont détectées, les règles sont évaluées pour en choisir une.</span><span class="sxs-lookup"><span data-stu-id="c415c-113">When multiple versions of a package are detected, rules are evaluated to pick one.</span></span> <span data-ttu-id="c415c-114">L’unification des packages est nécessaire, car l’exécution côte à côte des versions d’un assembly dans la même application est problématique dans .NET.</span><span class="sxs-lookup"><span data-stu-id="c415c-114">Unifying packages is necessary because running side-by-side versions of an assembly in the same application is problematic in .NET.</span></span>

<span data-ttu-id="c415c-115">La plupart des dépendances en losange sont facilement résolues ; toutefois, elles peuvent créer des problèmes dans certaines circonstances :</span><span class="sxs-lookup"><span data-stu-id="c415c-115">Most diamond dependencies are easily resolved; however, they can create issues in certain circumstances:</span></span>

1. <span data-ttu-id="c415c-116">**Les conflits de références de packages NuGet** empêchent la résolution d’une version pendant la restauration du package.</span><span class="sxs-lookup"><span data-stu-id="c415c-116">**Conflicting NuGet package references** prevent a version from being resolved during package restore.</span></span>
2. <span data-ttu-id="c415c-117">**Des modifications importantes entre les versions** provoquent des bogues et des exceptions lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c415c-117">**Breaking changes between the versions** cause bugs and exceptions at runtime.</span></span>
3. <span data-ttu-id="c415c-118">**Un nom fort est attribué à l’assembly de package**, la version d’assembly est modifiée et l’application exécutée sur .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c415c-118">**The package assembly is strong named**, the assembly version changed, and the app is running on the .NET Framework.</span></span> <span data-ttu-id="c415c-119">Des redirection des liaisons d'assembly sont requises.</span><span class="sxs-lookup"><span data-stu-id="c415c-119">Assembly binding redirects are required.</span></span>

<span data-ttu-id="c415c-120">Il n’est pas possible de savoir quels packages seront utilisées en même temps que le vôtre.</span><span class="sxs-lookup"><span data-stu-id="c415c-120">It's not possible to know what packages will be used alongside your own.</span></span> <span data-ttu-id="c415c-121">Un bon moyen de réduire la probabilité d’une dépendance en losange avec arrêt de votre bibliothèque consiste à limiter le nombre de packages dont vous dépendez.</span><span class="sxs-lookup"><span data-stu-id="c415c-121">A good way to reduce the likelihood of a diamond dependency breaking your library is to minimize the number of packages you depend on.</span></span>

<span data-ttu-id="c415c-122">**PASSEZ ✔️** en revue votre bibliothèque .NET pour détecter les dépendances inutiles.</span><span class="sxs-lookup"><span data-stu-id="c415c-122">**✔️ DO** review your .NET library for unnecessary dependencies.</span></span>

## <a name="nuget-dependency-version-ranges"></a><span data-ttu-id="c415c-123">Plages de versions de dépendances de NuGet</span><span class="sxs-lookup"><span data-stu-id="c415c-123">NuGet dependency version ranges</span></span>

<span data-ttu-id="c415c-124">Une référence de package spécifie la plage de packages valides autorisés.</span><span class="sxs-lookup"><span data-stu-id="c415c-124">A package reference specifies the range of valid packages it allows.</span></span> <span data-ttu-id="c415c-125">Généralement, la version de référence de package dans le fichier projet est la version minimale et il n’y a pas de maximum.</span><span class="sxs-lookup"><span data-stu-id="c415c-125">Typically, the package reference version in the project file is the minimum version and there's no maximum.</span></span>

```xml
<!-- Accepts any version 1.0 and above. -->
<PackageReference Include="ExamplePackage" Version="1.0" />
```

<span data-ttu-id="c415c-126">Les règles que NuGet utilise lors de la résolution des dépendances sont [complexes](/nuget/consume-packages/dependency-resolution), mais il recherche toujours la version la plus ancienne applicable.</span><span class="sxs-lookup"><span data-stu-id="c415c-126">The rules that NuGet uses when resolving dependencies are [complex](/nuget/consume-packages/dependency-resolution), but NuGet always looks for the lowest applicable version.</span></span> <span data-ttu-id="c415c-127">NuGet préfère la version la plus ancienne applicable à la plus récente disponible, car la plus ancienne aura moins de problèmes de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="c415c-127">NuGet prefers the lowest applicable version over using the highest available because the lowest will have the least compatibility issues.</span></span>

<span data-ttu-id="c415c-128">En raison de la règle de la version la plus ancienne applicable de NuGet, il n’est pas nécessaire de placer une version supérieure ou une plage exacte sur les références de package pour éviter d’obtenir la dernière version.</span><span class="sxs-lookup"><span data-stu-id="c415c-128">Because of NuGet's lowest applicable version rule, it isn't necessary to place an upper version or exact range on package references to avoid getting the latest version.</span></span> <span data-ttu-id="c415c-129">NuGet essaie déjà de trouver de la version la plus ancienne et la plus compatible pour vous.</span><span class="sxs-lookup"><span data-stu-id="c415c-129">NuGet already tries to find the lowest, most compatible version for you.</span></span>

```xml
<!-- Accepts 1.0 up to 1.x, but not 2.0 and higher. -->
<PackageReference Include="ExamplePackage" Version="[1.0,2.0)" />

<!-- Accepts exactly 1.0. -->
<PackageReference Include="ExamplePackage" Version="[1.0]" />
```

<span data-ttu-id="c415c-130">Des limites de versions supérieures entraîneront l’échec de NuGet en cas de conflit.</span><span class="sxs-lookup"><span data-stu-id="c415c-130">Upper version limits will cause NuGet to fail if there's a conflict.</span></span> <span data-ttu-id="c415c-131">Par exemple, une bibliothèque accepte exactement 1.0, tandis qu’une autre bibliothèque requiert 2.0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c415c-131">For example, one library accepts exactly 1.0 while another library requires 2.0 or above.</span></span> <span data-ttu-id="c415c-132">Alors que les modifications importantes peuvent avoir été introduites dans la version 2.0, une dépendance de version stricte ou supérieure d’une limite garantit une erreur.</span><span class="sxs-lookup"><span data-stu-id="c415c-132">While breaking changes may have been introduced in version 2.0, a strict or upper limit version dependency guarantees an error.</span></span>

<span data-ttu-id="c415c-133">![Conflit de dépendance en losange](./media/dependencies/diamond-dependency-conflict.png "Conflit de dépendance en losange")</span><span class="sxs-lookup"><span data-stu-id="c415c-133">![Diamond dependency conflict](./media/dependencies/diamond-dependency-conflict.png "Diamond dependency conflict")</span></span>

<span data-ttu-id="c415c-134">**❌ PAS** de références de packages NuGet sans version minimale.</span><span class="sxs-lookup"><span data-stu-id="c415c-134">**❌ DO NOT** have NuGet package references with no minimum version.</span></span>

<span data-ttu-id="c415c-135">**❌ ÉVITER** les références de package NuGet qui exigent une version précise.</span><span class="sxs-lookup"><span data-stu-id="c415c-135">**❌ AVOID** NuGet package references that demand an exact version.</span></span>

<span data-ttu-id="c415c-136">**❌ ÉVITER** LES références de package NuGet avec une limite supérieure de version.</span><span class="sxs-lookup"><span data-stu-id="c415c-136">**❌ AVOID** NuGet package references with a version upper limit.</span></span>

## <a name="nuget-shared-source-packages"></a><span data-ttu-id="c415c-137">Packages NuGet à code source partagé</span><span class="sxs-lookup"><span data-stu-id="c415c-137">NuGet shared source packages</span></span>

<span data-ttu-id="c415c-138">Une manière de réduire les dépendances externes de packages NuGet externes consiste à référencer les packages à code source partagé.</span><span class="sxs-lookup"><span data-stu-id="c415c-138">One way to reduce external NuGet package dependencies is to reference shared source packages.</span></span> <span data-ttu-id="c415c-139">Un package à code source partagé contient des [fichiers de code source](/nuget/reference/nuspec#including-content-files) qui sont inclus dans un projet référencé.</span><span class="sxs-lookup"><span data-stu-id="c415c-139">A shared source package contains [source code files](/nuget/reference/nuspec#including-content-files) that are included in a project when referenced.</span></span> <span data-ttu-id="c415c-140">Comme vous incluez uniquement des fichiers de code source compilés avec le reste de votre projet, il n’y a aucune dépendance externe ni risque de conflit.</span><span class="sxs-lookup"><span data-stu-id="c415c-140">Because you're just including source code files that are compiled with the rest of your project, there's no external dependency and chance of conflict.</span></span>

<span data-ttu-id="c415c-141">Les packages à code source partagée sont l’idéal pour inclure de petits éléments de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c415c-141">Shared source packages are great for including small pieces of functionality.</span></span> <span data-ttu-id="c415c-142">Par exemple, un package à source partagée de méthodes d’assistance pour les appels HTTP.</span><span class="sxs-lookup"><span data-stu-id="c415c-142">For example, a shared source package of helper methods for making HTTP calls.</span></span>

<span data-ttu-id="c415c-143">![Package à code source partagé](./media/dependencies/shared-source-package.png "Package à code source partagé")</span><span class="sxs-lookup"><span data-stu-id="c415c-143">![Shared source package](./media/dependencies/shared-source-package.png "Shared source package")</span></span>

```xml
<PackageReference Include="Microsoft.Extensions.Buffers.Testing.Sources" PrivateAssets="All" Version="1.0" />
```

<span data-ttu-id="c415c-144">![Projet à code source partagé](./media/dependencies/shared-source-project.png "Projet à code source partagé")</span><span class="sxs-lookup"><span data-stu-id="c415c-144">![Shared source project](./media/dependencies/shared-source-project.png "Shared source project")</span></span>

<span data-ttu-id="c415c-145">Les packages à code source partagé ont certaines limitations.</span><span class="sxs-lookup"><span data-stu-id="c415c-145">Shared source packages have some limitations.</span></span> <span data-ttu-id="c415c-146">Ils ne peuvent être référencés que par `PackageReference`, ce qui exclut les projets `packages.config` plus anciens.</span><span class="sxs-lookup"><span data-stu-id="c415c-146">They can only be referenced by `PackageReference`, so older `packages.config` projects are excluded.</span></span> <span data-ttu-id="c415c-147">Par ailleurs, les packages à code source partagé ne peuvent être utilisés que par des projets ayant le même type de langage.</span><span class="sxs-lookup"><span data-stu-id="c415c-147">Also shared source packages are only usable by projects with the same language type.</span></span> <span data-ttu-id="c415c-148">En raison de ces limitations, les packages à code source partagé sont très bien adaptés au partage d’une fonctionnalité au sein d’un projet open source.</span><span class="sxs-lookup"><span data-stu-id="c415c-148">Because of these limitations shared source packages are best used to share functionality within an open-source project.</span></span>

<span data-ttu-id="c415c-149">**✔️ ENVISAGER** de référencer des packages à code source partagé pour de petits éléments internes de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c415c-149">**✔️ CONSIDER** referencing shared source packages for small, internal pieces of functionality.</span></span>

<span data-ttu-id="c415c-150">**✔️ ENVISAGER** de faire de votre package un package à code source partagé pour de petits éléments internes de fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="c415c-150">**✔️ CONSIDER** making your package a shared source package if it provides small, internal pieces of functionality.</span></span>

<span data-ttu-id="c415c-151">**✔️ RÉFÉRENCER** des packages à code source partagé avec `PrivateAssets="All"`.</span><span class="sxs-lookup"><span data-stu-id="c415c-151">**✔️ DO** reference shared source packages with `PrivateAssets="All"`.</span></span>

> <span data-ttu-id="c415c-152">Ce paramètre indique à NuGet que le package ne doit être utilisée que lors du développement et ne doit pas être exposé en tant que dépendance publique.</span><span class="sxs-lookup"><span data-stu-id="c415c-152">This setting tells NuGet the package is only to be used at development time and shouldn't be exposed as a public dependency.</span></span>

<span data-ttu-id="c415c-153">**❌ PAS** de packages de type à code source partagé dans votre API publique.</span><span class="sxs-lookup"><span data-stu-id="c415c-153">**❌ DO NOT** have shared source package types in your public API.</span></span>

> <span data-ttu-id="c415c-154">Les types à code source partagé sont compilés dans l’assembly de référencement et ne peuvent pas être échangés au-delà des limites de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="c415c-154">Shared source types are compiled into the referencing assembly and can't be exchanged across assembly boundaries.</span></span> <span data-ttu-id="c415c-155">Par exemple, un type de `IRepository` à code source partagé dans un projet est un type distinct du même `IRepository` à code source partagé dans un autre projet.</span><span class="sxs-lookup"><span data-stu-id="c415c-155">For example, a shared-source `IRepository` type in one project is a separate type from the same shared-source `IRepository` in another project.</span></span> <span data-ttu-id="c415c-156">Les types de packages à code source partagé doivent avoir une visibilité `internal`.</span><span class="sxs-lookup"><span data-stu-id="c415c-156">Types in shared source packages should have an `internal` visibility.</span></span>

<span data-ttu-id="c415c-157">**❌ NE PAS** publier de packages à code source partagé sur nuget.org.</span><span class="sxs-lookup"><span data-stu-id="c415c-157">**❌ DO NOT** publish shared source packages to nuget.org.</span></span>

> <span data-ttu-id="c415c-158">Les packages à code source partagé contiennent du code source et ne peuvent être utilisés que par des projets ayant le même type de langage.</span><span class="sxs-lookup"><span data-stu-id="c415c-158">Shared source packages contain source code and can only be used by projects with the same language type.</span></span> <span data-ttu-id="c415c-159">Par exemple, un package à code source partagé C# ne peut pas être utilisé par une application F#.</span><span class="sxs-lookup"><span data-stu-id="c415c-159">For example, a C# shared source package cannot be used by an F# application.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="c415c-160">[Précédent](./nuget.md)
[Suivant](./sourcelink.md)</span><span class="sxs-lookup"><span data-stu-id="c415c-160">[Previous](./nuget.md)
[Next](./sourcelink.md)</span></span>
