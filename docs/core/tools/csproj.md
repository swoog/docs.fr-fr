---
title: Ajouts au format csproj pour .NET Core
description: Découvrir les différences entre les fichiers csproj existants et les fichiers csproj .NET Core
author: blackdwarf
ms.date: 09/22/2017
ms.openlocfilehash: 74cde39a0bbba65d252d64bcedb91c3949dcf6f2
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54222062"
---
# <a name="additions-to-the-csproj-format-for-net-core"></a><span data-ttu-id="af7fa-103">Ajouts au format csproj pour .NET Core</span><span class="sxs-lookup"><span data-stu-id="af7fa-103">Additions to the csproj format for .NET Core</span></span>

<span data-ttu-id="af7fa-104">Ce document décrit les modifications qui ont été ajoutées aux fichiers projet dans le cadre du passage de *project.json* à *csproj* et [MSBuild](https://github.com/Microsoft/MSBuild).</span><span class="sxs-lookup"><span data-stu-id="af7fa-104">This document outlines the changes that were added to the project files as part of the move from *project.json* to *csproj* and [MSBuild](https://github.com/Microsoft/MSBuild).</span></span> <span data-ttu-id="af7fa-105">Pour plus d’informations de référence ou syntaxiques générales sur les fichiers projet, consultez la documentation sur les [fichiers projet MSBuild](/visualstudio/msbuild/msbuild-project-file-schema-reference).</span><span class="sxs-lookup"><span data-stu-id="af7fa-105">For more information about general project file syntax and reference, see [the MSBuild project file](/visualstudio/msbuild/msbuild-project-file-schema-reference) documentation.</span></span>  

## <a name="implicit-package-references"></a><span data-ttu-id="af7fa-106">Références de package implicites</span><span class="sxs-lookup"><span data-stu-id="af7fa-106">Implicit package references</span></span>
<span data-ttu-id="af7fa-107">Les métapackages sont référencés implicitement en fonction du ou des frameworks cibles spécifiés dans la propriété `<TargetFramework>` ou `<TargetFrameworks>` de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-107">Metapackages are implicitly referenced based on the target framework(s) specified in the `<TargetFramework>` or `<TargetFrameworks>` property of your project file.</span></span> <span data-ttu-id="af7fa-108">`<TargetFrameworks>` est ignoré si `<TargetFramework>` est spécifié, indépendamment de l’ordre.</span><span class="sxs-lookup"><span data-stu-id="af7fa-108">`<TargetFrameworks>` is ignored if `<TargetFramework>` is specified, independent of order.</span></span>

```xml
 <PropertyGroup>
   <TargetFramework>netcoreapp2.1</TargetFramework>
 </PropertyGroup>
 ```
 
 ```xml
 <PropertyGroup>
   <TargetFrameworks>netcoreapp2.1;net462</TargetFrameworks>
 </PropertyGroup>
 ```

### <a name="recommendations"></a><span data-ttu-id="af7fa-109">Recommandations</span><span class="sxs-lookup"><span data-stu-id="af7fa-109">Recommendations</span></span>
<span data-ttu-id="af7fa-110">Comme les métapackages `Microsoft.NETCore.App` ou `NetStandard.Library` sont implicitement référencés, voici les bonnes pratiques que nous recommandons :</span><span class="sxs-lookup"><span data-stu-id="af7fa-110">Since `Microsoft.NETCore.App` or `NetStandard.Library` metapackages are implicitly referenced, the following are our recommended best practices:</span></span>

* <span data-ttu-id="af7fa-111">Quand vous ciblez .NET Core ou .NET Standard, n’incluez jamais de référence explicite aux métapackages `Microsoft.NETCore.App` ou `NetStandard.Library` via un élément `<PackageReference>` dans votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-111">When targeting .NET Core or .NET Standard, never have an explicit reference to the `Microsoft.NETCore.App` or `NetStandard.Library` metapackages via a `<PackageReference>` item in your project file.</span></span>
* <span data-ttu-id="af7fa-112">Si vous avez besoin d’une version spécifique du runtime quand vous ciblez .NET Core, vous devez utiliser la propriété `<RuntimeFrameworkVersion>` dans votre projet (par exemple, `1.0.4`) au lieu de référencer le métapackage.</span><span class="sxs-lookup"><span data-stu-id="af7fa-112">If you need a specific version of the runtime when targeting .NET Core, you should use the `<RuntimeFrameworkVersion>` property in your project (for example, `1.0.4`) instead of referencing the metapackage.</span></span>
    * <span data-ttu-id="af7fa-113">Cela peut se produire si vous utilisez des [déploiements autonomes](../deploying/index.md#self-contained-deployments-scd) et que vous devez utiliser une version de correctif spécifique du runtime 1.0.0 LTS, par exemple.</span><span class="sxs-lookup"><span data-stu-id="af7fa-113">This might happen if you are using [self-contained deployments](../deploying/index.md#self-contained-deployments-scd) and you need a specific patch version of 1.0.0 LTS runtime, for example.</span></span>
* <span data-ttu-id="af7fa-114">Si vous avez besoin d’une version spécifique du métapackage `NetStandard.Library` quand vous ciblez .NET Standard, vous pouvez utiliser la propriété `<NetStandardImplicitPackageVersion>` et définir la version dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="af7fa-114">If you need a specific version of the `NetStandard.Library` metapackage when targeting .NET Standard, you can use the `<NetStandardImplicitPackageVersion>` property and set the version you need.</span></span>
* <span data-ttu-id="af7fa-115">Vous ne devez pas ajouter ni mettre à jour explicitement les références au métapackage `Microsoft.NETCore.App` ou `NetStandard.Library` dans les projets .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="af7fa-115">Don't explicitly add or update references to either the `Microsoft.NETCore.App` or `NetStandard.Library` metapackage in .NET Framework projects.</span></span> <span data-ttu-id="af7fa-116">Si une version de `NetStandard.Library` est nécessaire lors de l’utilisation d’un package NuGet basé sur .NET Standard, NuGet installe automatiquement cette version.</span><span class="sxs-lookup"><span data-stu-id="af7fa-116">If any version of `NetStandard.Library` is needed when using a .NET Standard-based NuGet package, NuGet automatically installs that version.</span></span>

## <a name="default-compilation-includes-in-net-core-projects"></a><span data-ttu-id="af7fa-117">Inclusions de compilation par défaut dans les projets .NET Core</span><span class="sxs-lookup"><span data-stu-id="af7fa-117">Default compilation includes in .NET Core projects</span></span>
<span data-ttu-id="af7fa-118">Dans le cadre du passage au format *csproj* dans les dernières versions du SDK, nous avons déplacé les inclusions et exclusions par défaut pour les éléments de compilation et les ressources incorporées dans les fichiers de propriétés du SDK.</span><span class="sxs-lookup"><span data-stu-id="af7fa-118">With the move to the *csproj* format in the latest SDK versions, we've moved the default includes and excludes for compile items and embedded resources to the SDK properties files.</span></span> <span data-ttu-id="af7fa-119">Cela signifie que vous n’avez plus besoin de spécifier ces éléments dans votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-119">This means that you no longer need to specify these items in your project file.</span></span> 

<span data-ttu-id="af7fa-120">La principale raison de cette modification est de réduire l’encombrement de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-120">The main reason for doing this is to reduce the clutter in your project file.</span></span> <span data-ttu-id="af7fa-121">Les valeurs par défaut qui sont présentes dans le SDK doivent couvrir la plupart des cas d’utilisation courants, il est donc inutile de les répéter dans chaque projet que vous créez.</span><span class="sxs-lookup"><span data-stu-id="af7fa-121">The defaults that are present in the SDK should cover most common use cases, so there is no need to repeat them in every project that you create.</span></span> <span data-ttu-id="af7fa-122">Il en résulte des fichiers projet moins volumineux qui sont beaucoup plus faciles à comprendre et à modifier à la main, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af7fa-122">This leads to smaller project files that are much easier to understand as well as edit by hand, if needed.</span></span> 

<span data-ttu-id="af7fa-123">Le tableau suivant montre les éléments et les modèles [Glob](https://en.wikipedia.org/wiki/Glob_(programming)) inclus et exclus dans le SDK :</span><span class="sxs-lookup"><span data-stu-id="af7fa-123">The following table shows which element and which [globs](https://en.wikipedia.org/wiki/Glob_(programming)) are both included and excluded in the SDK:</span></span> 

| <span data-ttu-id="af7fa-124">Élément</span><span class="sxs-lookup"><span data-stu-id="af7fa-124">Element</span></span>           | <span data-ttu-id="af7fa-125">Inclure Glob</span><span class="sxs-lookup"><span data-stu-id="af7fa-125">Include glob</span></span>                              | <span data-ttu-id="af7fa-126">Exclure Glob</span><span class="sxs-lookup"><span data-stu-id="af7fa-126">Exclude glob</span></span>                                                  | <span data-ttu-id="af7fa-127">Supprimer Glob</span><span class="sxs-lookup"><span data-stu-id="af7fa-127">Remove glob</span></span>                |
|-------------------|-------------------------------------------|---------------------------------------------------------------|----------------------------|
| <span data-ttu-id="af7fa-128">Compile</span><span class="sxs-lookup"><span data-stu-id="af7fa-128">Compile</span></span>           | <span data-ttu-id="af7fa-129">\*\*/\*.cs (ou autres extensions de langage)</span><span class="sxs-lookup"><span data-stu-id="af7fa-129">\*\*/\*.cs (or other language extensions)</span></span> | <span data-ttu-id="af7fa-130">\*\*/\*.user ;  \*\*/\*.\*proj ;  \*\*/\*.sln ;  \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="af7fa-130">\*\*/\*.user;  \*\*/\*.\*proj;  \*\*/\*.sln;  \*\*/\*.vssscc</span></span>  | <span data-ttu-id="af7fa-131">N/A</span><span class="sxs-lookup"><span data-stu-id="af7fa-131">N/A</span></span>                        |
| <span data-ttu-id="af7fa-132">EmbeddedResource</span><span class="sxs-lookup"><span data-stu-id="af7fa-132">EmbeddedResource</span></span>  | <span data-ttu-id="af7fa-133">\*\*/\*.resx</span><span class="sxs-lookup"><span data-stu-id="af7fa-133">\*\*/\*.resx</span></span>                              | <span data-ttu-id="af7fa-134">\*\*/\*.user ; \*\*/\*.\*proj ; \*\*/\*.sln ; \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="af7fa-134">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span></span>     | <span data-ttu-id="af7fa-135">N/A</span><span class="sxs-lookup"><span data-stu-id="af7fa-135">N/A</span></span>                        |
| <span data-ttu-id="af7fa-136">Aucun.</span><span class="sxs-lookup"><span data-stu-id="af7fa-136">None</span></span>              | \*\*/\*                                   | <span data-ttu-id="af7fa-137">\*\*/\*.user ; \*\*/\*.\*proj ; \*\*/\*.sln ; \*\*/\*.vssscc</span><span class="sxs-lookup"><span data-stu-id="af7fa-137">\*\*/\*.user; \*\*/\*.\*proj; \*\*/\*.sln; \*\*/\*.vssscc</span></span>     | <span data-ttu-id="af7fa-138">- \*\*/\*.cs ; \*\*/\*.resx</span><span class="sxs-lookup"><span data-stu-id="af7fa-138">- \*\*/\*.cs; \*\*/\*.resx</span></span> |

<span data-ttu-id="af7fa-139">Si vous avez des modèles Glob dans votre projet et que vous essayez de le générer à l’aide du dernier SDK, vous obtenez l’erreur suivante :</span><span class="sxs-lookup"><span data-stu-id="af7fa-139">If you have globs in your project and you try to build it using the newest SDK, you'll get the following error:</span></span>

> <span data-ttu-id="af7fa-140">Des éléments de compilation en double ont été inclus.</span><span class="sxs-lookup"><span data-stu-id="af7fa-140">Duplicate Compile items were included.</span></span> <span data-ttu-id="af7fa-141">Le SDK .NET inclut des éléments de compilation de votre répertoire de projet par défaut.</span><span class="sxs-lookup"><span data-stu-id="af7fa-141">The .NET SDK includes Compile items from your project directory by default.</span></span> <span data-ttu-id="af7fa-142">Vous pouvez supprimer ces éléments de votre fichier projet ou définir la propriété 'EnableDefaultCompileItems' sur 'false' si vous voulez explicitement les inclure dans votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-142">You can either remove these items from your project file, or set the 'EnableDefaultCompileItems' property to 'false' if you want to explicitly include them in your project file.</span></span> 

<span data-ttu-id="af7fa-143">Pour contourner cette erreur, vous pouvez supprimer les éléments `Compile` explicites qui correspondent à ceux répertoriés dans le tableau précédent ou vous pouvez définir la propriété `<EnableDefaultCompileItems>` sur `false`, comme ceci :</span><span class="sxs-lookup"><span data-stu-id="af7fa-143">In order to get around this error, you can either remove the explicit `Compile` items that match the ones listed on the previous table, or you can set the `<EnableDefaultCompileItems>` property to `false`, like this:</span></span>

```xml
<PropertyGroup>
    <EnableDefaultCompileItems>false</EnableDefaultCompileItems>
</PropertyGroup>
```
<span data-ttu-id="af7fa-144">Le fait de définir cette propriété avec la valeur `false` désactive l’inclusion implicite, ce qui rétablit le comportement des SDK précédents dans lesquels vous deviez spécifier les globs par défaut dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-144">Setting this property to `false` will disable implicit inclusion, reverting to the behavior of previous SDKs where you had to specify the default globs in your project.</span></span>

<span data-ttu-id="af7fa-145">Ce changement ne modifie pas le mécanisme principal des autres inclusions.</span><span class="sxs-lookup"><span data-stu-id="af7fa-145">This change does not modify the main mechanics of other includes.</span></span> <span data-ttu-id="af7fa-146">Toutefois, si vous voulez, par exemple, spécifier certains fichiers à publier avec votre application, vous pouvez toujours utiliser les mécanismes connus dans *csproj* correspondants (par exemple, l’élément `<Content>`).</span><span class="sxs-lookup"><span data-stu-id="af7fa-146">However, if you wish to specify, for example, some files to get published with your app, you can still use the known mechanisms in *csproj* for that (for example, the `<Content>` element).</span></span>

<span data-ttu-id="af7fa-147">`<EnableDefaultCompileItems>` désactive uniquement les modèles Glob `Compile`, mais n’affecte pas les autres modèles Glob, comme le modèle Glob implicite `None`, qui s’applique également aux éléments \*.cs.</span><span class="sxs-lookup"><span data-stu-id="af7fa-147">`<EnableDefaultCompileItems>` only disables `Compile` globs but doesn't affect other globs, like the implicit `None` glob, which also applies to \*.cs items.</span></span> <span data-ttu-id="af7fa-148">Par conséquent, **l’Explorateur de solutions** continue d’afficher des éléments \*.cs dans le cadre du projet, inclus en tant qu’éléments `None`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-148">Because of that, **Solution Explorer** will continue show \*.cs items as part of the project, included as `None` items.</span></span> <span data-ttu-id="af7fa-149">De la même façon, vous pouvez utiliser `<EnableDefaultNoneItems>` pour désactiver le modèle Glob implicite `None`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-149">In a similar way, you can use `<EnableDefaultNoneItems>` to disable the implicit `None` glob.</span></span>

<span data-ttu-id="af7fa-150">Pour désactiver **tous les modèles Glob implicites**, vous pouvez affecter à la propriété `<EnableDefaultItems>` la valeur `false` comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="af7fa-150">To disable **all implicit globs**, you can set the `<EnableDefaultItems>` property to `false` as in the following example:</span></span>
```xml
<PropertyGroup>
    <EnableDefaultItems>false</EnableDefaultItems>
</PropertyGroup>
```

## <a name="how-to-see-the-whole-project-as-msbuild-sees-it"></a><span data-ttu-id="af7fa-151">Comment afficher la totalité du projet tel qu’il est perçu par MSBuild ?</span><span class="sxs-lookup"><span data-stu-id="af7fa-151">How to see the whole project as MSBuild sees it</span></span>

<span data-ttu-id="af7fa-152">Même si ces modifications csproj simplifient considérablement les fichiers projet, vous pouvez souhaiter voir le projet entièrement développé tel qu’il est perçu par MSBuild une fois le kit SDK et ses cibles inclus.</span><span class="sxs-lookup"><span data-stu-id="af7fa-152">While those csproj changes greatly simplify project files, you might want to see the fully expanded project as MSBuild sees it once the SDK and its targets are included.</span></span> <span data-ttu-id="af7fa-153">Prétraitez le projet avec [le commutateur `/pp`](/visualstudio/msbuild/msbuild-command-line-reference#preprocess) de la commande [`dotnet msbuild`](dotnet-msbuild.md), qui affiche les fichiers qui sont importés, leurs sources et leurs contributions à la build sans réellement générer le projet :</span><span class="sxs-lookup"><span data-stu-id="af7fa-153">Preprocess the project with [the `/pp` switch](/visualstudio/msbuild/msbuild-command-line-reference#preprocess) of the [`dotnet msbuild`](dotnet-msbuild.md) command, which shows which files are imported, their sources, and their contributions to the build without actually building the project:</span></span>

`dotnet msbuild -pp:fullproject.xml`

<span data-ttu-id="af7fa-154">Si le projet comporte plusieurs frameworks cibles, les résultats de la commande ne doivent se concentrer que sur un seul d'entre eux en le spécifiant en tant que propriété MSBuild :</span><span class="sxs-lookup"><span data-stu-id="af7fa-154">If the project has multiple target frameworks, the results of the command should be focused on only one of them by specifying it as an MSBuild property:</span></span>

`dotnet msbuild -p:TargetFramework=netcoreapp2.0 -pp:fullproject.xml`

## <a name="additions"></a><span data-ttu-id="af7fa-155">Ajouts</span><span class="sxs-lookup"><span data-stu-id="af7fa-155">Additions</span></span>

### <a name="sdk-attribute"></a><span data-ttu-id="af7fa-156">Attribut Sdk</span><span class="sxs-lookup"><span data-stu-id="af7fa-156">Sdk attribute</span></span> 
<span data-ttu-id="af7fa-157">L’élément `<Project>` racine du fichier *.csproj* a un nouvel attribut nommé `Sdk`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-157">The root `<Project>` element of the *.csproj* file has a new attribute called `Sdk`.</span></span> <span data-ttu-id="af7fa-158">`Sdk` spécifie le SDK à utiliser par le projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-158">`Sdk` specifies which SDK will be used by the project.</span></span> <span data-ttu-id="af7fa-159">Le SDK, comme le décrit le [document de superposition](cli-msbuild-architecture.md), est un ensemble de [tâches](/visualstudio/msbuild/msbuild-tasks) et de [cibles](/visualstudio/msbuild/msbuild-targets) MSBuild pouvant générer du code .NET Core.</span><span class="sxs-lookup"><span data-stu-id="af7fa-159">The SDK, as the [layering document](cli-msbuild-architecture.md) describes, is a set of MSBuild [tasks](/visualstudio/msbuild/msbuild-tasks) and [targets](/visualstudio/msbuild/msbuild-targets) that can build .NET Core code.</span></span> <span data-ttu-id="af7fa-160">Nous fournissons trois Kits SDK principaux dans les outils .NET Core :</span><span class="sxs-lookup"><span data-stu-id="af7fa-160">We ship three main SDKs with the .NET Core tools:</span></span>

1. <span data-ttu-id="af7fa-161">Le SDK .NET Core avec l’ID `Microsoft.NET.Sdk`</span><span class="sxs-lookup"><span data-stu-id="af7fa-161">The .NET Core SDK with the ID of `Microsoft.NET.Sdk`</span></span>
2. <span data-ttu-id="af7fa-162">Le SDK .NET Core avec l’ID `Microsoft.NET.Sdk.Web`</span><span class="sxs-lookup"><span data-stu-id="af7fa-162">The .NET Core web SDK with the ID of `Microsoft.NET.Sdk.Web`</span></span>
3. <span data-ttu-id="af7fa-163">Le Kit SDK de la bibliothèque de classes .NET Core Razor avec l’ID `Microsoft.NET.Sdk.Razor`</span><span class="sxs-lookup"><span data-stu-id="af7fa-163">The .NET Core Razor Class Library SDK with the ID of `Microsoft.NET.Sdk.Razor`</span></span>

<span data-ttu-id="af7fa-164">Vous devez définir l’attribut `Sdk` sur un de ces ID pour l’élément `<Project>` afin d’utiliser les outils .NET Core et générer votre code.</span><span class="sxs-lookup"><span data-stu-id="af7fa-164">You need to have the `Sdk` attribute set to one of those IDs on the `<Project>` element in order to use the .NET Core tools and build your code.</span></span> 

### <a name="packagereference"></a><span data-ttu-id="af7fa-165">PackageReference</span><span class="sxs-lookup"><span data-stu-id="af7fa-165">PackageReference</span></span>
<span data-ttu-id="af7fa-166">Un élément `<PackageReference>` spécifie une dépendance NuGet dans le projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-166">A `<PackageReference>` item element specifies a NuGet dependency in the project.</span></span> <span data-ttu-id="af7fa-167">L’attribut `Include` spécifie l’ID du package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-167">The `Include` attribute specifies the package ID.</span></span> 

```xml
<PackageReference Include="<package-id>" Version="" PrivateAssets="" IncludeAssets="" ExcludeAssets="" />
```

#### <a name="version"></a><span data-ttu-id="af7fa-168">Version</span><span class="sxs-lookup"><span data-stu-id="af7fa-168">Version</span></span>
<span data-ttu-id="af7fa-169">`Version` spécifie la version du package à restaurer.</span><span class="sxs-lookup"><span data-stu-id="af7fa-169">`Version` specifies the version of the package to restore.</span></span> <span data-ttu-id="af7fa-170">L’attribut respecte les règles du schéma de [contrôle de version de NuGet](/nuget/create-packages/dependency-versions#version-ranges).</span><span class="sxs-lookup"><span data-stu-id="af7fa-170">The attribute respects the rules of the [NuGet versioning](/nuget/create-packages/dependency-versions#version-ranges) scheme.</span></span> <span data-ttu-id="af7fa-171">Le comportement par défaut est une correspondance exacte entre les versions.</span><span class="sxs-lookup"><span data-stu-id="af7fa-171">The default behavior is an exact version match.</span></span> <span data-ttu-id="af7fa-172">Par exemple, la spécification `Version="1.2.3"` est équivalente à la notation `[1.2.3]` de NuGet pour la version du package 1.2.3 précisément.</span><span class="sxs-lookup"><span data-stu-id="af7fa-172">For example, specifying `Version="1.2.3"` is equivalent to NuGet notation `[1.2.3]` for the exact 1.2.3 version of the package.</span></span>

#### <a name="includeassets-excludeassets-and-privateassets"></a><span data-ttu-id="af7fa-173">IncludeAssets, ExcludeAssets et PrivateAssets</span><span class="sxs-lookup"><span data-stu-id="af7fa-173">IncludeAssets, ExcludeAssets and PrivateAssets</span></span>
<span data-ttu-id="af7fa-174">L’attribut `IncludeAssets` spécifie quelles ressources appartenant au package spécifié par `<PackageReference>` doivent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="af7fa-174">`IncludeAssets` attribute specifies which assets belonging to the package specified by `<PackageReference>` should be consumed.</span></span> 

<span data-ttu-id="af7fa-175">L’attribut `ExcludeAssets` spécifie quelles ressources appartenant au package spécifié par `<PackageReference>` ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="af7fa-175">`ExcludeAssets` attribute specifies which assets belonging to the package specified by `<PackageReference>` should not be consumed.</span></span>

<span data-ttu-id="af7fa-176">L’attribut `PrivateAssets` spécifie quelles ressources appartenant au package spécifié par `<PackageReference>` doivent être utilisées, mais sans être reprises dans le projet suivant.</span><span class="sxs-lookup"><span data-stu-id="af7fa-176">`PrivateAssets` attribute specifies which assets belonging to the package specified by `<PackageReference>` should be consumed but not flow to the next project.</span></span> 

> [!NOTE]
> <span data-ttu-id="af7fa-177">`PrivateAssets` est équivalent à l’élément *project.json*/*xproj* `SuppressParent`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-177">`PrivateAssets` is equivalent to the *project.json*/*xproj* `SuppressParent` element.</span></span>

<span data-ttu-id="af7fa-178">Ces attributs peuvent contenir un ou plusieurs des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="af7fa-178">These attributes can contain one or more of the following items:</span></span>

* <span data-ttu-id="af7fa-179">`Compile` : Le contenu du dossier lib est disponible pour la compilation.</span><span class="sxs-lookup"><span data-stu-id="af7fa-179">`Compile` – the contents of the lib folder are available to compile against.</span></span>
* <span data-ttu-id="af7fa-180">`Runtime` : Le contenu du dossier runtime est distribué.</span><span class="sxs-lookup"><span data-stu-id="af7fa-180">`Runtime` – the contents of the runtime folder are distributed.</span></span>
* <span data-ttu-id="af7fa-181">`ContentFiles` : Le contenu du dossier *contentfiles* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="af7fa-181">`ContentFiles` – the contents of the *contentfiles* folder are used.</span></span>
* <span data-ttu-id="af7fa-182">`Build` : Les propriétés/cibles du dossier de génération sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="af7fa-182">`Build` – the props/targets in the build folder are used.</span></span>
* <span data-ttu-id="af7fa-183">`Native` : Le contenu des ressources natives est copié dans le dossier de sortie de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="af7fa-183">`Native` – the contents from native assets are copied to the output folder for runtime.</span></span>
* <span data-ttu-id="af7fa-184">`Analyzers` : Les analyseurs sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="af7fa-184">`Analyzers` – the analyzers are used.</span></span>

<span data-ttu-id="af7fa-185">Sinon, l’attribut peut contenir :</span><span class="sxs-lookup"><span data-stu-id="af7fa-185">Alternatively, the attribute can contain:</span></span>

* <span data-ttu-id="af7fa-186">`None` : Aucune ressource n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="af7fa-186">`None` – none of the assets are used.</span></span>
* <span data-ttu-id="af7fa-187">`All` : Toutes les ressources sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="af7fa-187">`All` – all assets are used.</span></span>

### <a name="dotnetclitoolreference"></a><span data-ttu-id="af7fa-188">DotNetCliToolReference</span><span class="sxs-lookup"><span data-stu-id="af7fa-188">DotNetCliToolReference</span></span>
<span data-ttu-id="af7fa-189">Un élément `<DotNetCliToolReference>` spécifie l’outil CLI que l’utilisateur souhaite restaurer dans le contexte du projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-189">A `<DotNetCliToolReference>` item element specifies the CLI tool that the user wants to restore in the context of the project.</span></span> <span data-ttu-id="af7fa-190">Il constitue une alternative au nœud `tools` dans *project.json*.</span><span class="sxs-lookup"><span data-stu-id="af7fa-190">It's a replacement for the `tools` node in *project.json*.</span></span> 

```xml
<DotNetCliToolReference Include="<package-id>" Version="" />
```

#### <a name="version"></a><span data-ttu-id="af7fa-191">Version</span><span class="sxs-lookup"><span data-stu-id="af7fa-191">Version</span></span>
<span data-ttu-id="af7fa-192">`Version` spécifie la version du package à restaurer.</span><span class="sxs-lookup"><span data-stu-id="af7fa-192">`Version` specifies the version of the package to restore.</span></span> <span data-ttu-id="af7fa-193">L’attribut respecte les règles du schéma de [contrôle de version de NuGet](/nuget/create-packages/dependency-versions#version-ranges).</span><span class="sxs-lookup"><span data-stu-id="af7fa-193">The attribute respects the rules of the [NuGet versioning](/nuget/create-packages/dependency-versions#version-ranges) scheme.</span></span> <span data-ttu-id="af7fa-194">Le comportement par défaut est une correspondance exacte entre les versions.</span><span class="sxs-lookup"><span data-stu-id="af7fa-194">The default behavior is an exact version match.</span></span> <span data-ttu-id="af7fa-195">Par exemple, la spécification `Version="1.2.3"` est équivalente à la notation `[1.2.3]` de NuGet pour la version du package 1.2.3 précisément.</span><span class="sxs-lookup"><span data-stu-id="af7fa-195">For example, specifying `Version="1.2.3"` is equivalent to NuGet notation `[1.2.3]` for the exact 1.2.3 version of the package.</span></span>

### <a name="runtimeidentifiers"></a><span data-ttu-id="af7fa-196">RuntimeIdentifiers</span><span class="sxs-lookup"><span data-stu-id="af7fa-196">RuntimeIdentifiers</span></span>
<span data-ttu-id="af7fa-197">L’élément de propriété `<RuntimeIdentifiers>` vous permet de spécifier une liste délimitée par des points-virgules d’[identificateurs de runtime (RID)](../rid-catalog.md) pour le projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-197">The `<RuntimeIdentifiers>` property element lets you specify a semicolon-delimited list of [Runtime Identifiers (RIDs)](../rid-catalog.md) for the project.</span></span> <span data-ttu-id="af7fa-198">Les RID permettent de publier des déploiements autonomes.</span><span class="sxs-lookup"><span data-stu-id="af7fa-198">RIDs enable publishing self-contained deployments.</span></span> 

```xml
<RuntimeIdentifiers>win10-x64;osx.10.11-x64;ubuntu.16.04-x64</RuntimeIdentifiers>
```

### <a name="runtimeidentifier"></a><span data-ttu-id="af7fa-199">RuntimeIdentifier</span><span class="sxs-lookup"><span data-stu-id="af7fa-199">RuntimeIdentifier</span></span>
<span data-ttu-id="af7fa-200">L’élément de propriété `<RuntimeIdentifier>` vous permet de spécifier un seul [identificateur de runtime (RID)](../rid-catalog.md) pour le projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-200">The `<RuntimeIdentifier>` property element allows you to specify only one [Runtime Identifier (RID)](../rid-catalog.md) for the project.</span></span> <span data-ttu-id="af7fa-201">Le RID permet de publier un déploiement autonome.</span><span class="sxs-lookup"><span data-stu-id="af7fa-201">The RID enables publishing a self-contained deployment.</span></span>

```xml
<RuntimeIdentifier>ubuntu.16.04-x64</RuntimeIdentifier>
```

<span data-ttu-id="af7fa-202">Utilisez plutôt `<RuntimeIdentifiers>` (au pluriel) si vous devez publier pour plusieurs runtimes.</span><span class="sxs-lookup"><span data-stu-id="af7fa-202">Use `<RuntimeIdentifiers>` (plural) instead if you need to publish for multiple runtimes.</span></span> <span data-ttu-id="af7fa-203">`<RuntimeIdentifier>` peut fournir des builds plus rapides quand un seul runtime est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="af7fa-203">`<RuntimeIdentifier>` can provide faster builds when only a single runtime is required.</span></span>

### <a name="packagetargetfallback"></a><span data-ttu-id="af7fa-204">PackageTargetFallback</span><span class="sxs-lookup"><span data-stu-id="af7fa-204">PackageTargetFallback</span></span> 
<span data-ttu-id="af7fa-205">L’élément de propriété `<PackageTargetFallback>` vous permet de spécifier un jeu de cibles compatibles à utiliser lors de la restauration des packages.</span><span class="sxs-lookup"><span data-stu-id="af7fa-205">The `<PackageTargetFallback>` property element allows you to specify a set of compatible targets to be used when restoring packages.</span></span> <span data-ttu-id="af7fa-206">Il est conçu pour permettre aux packages qui utilisent le [moniker du framework cible](/nuget/schema/target-frameworks) dotnet de fonctionner avec les packages qui ne déclarent pas de moniker du framework cible dotnet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-206">It's designed to allow packages that use the dotnet [TxM (Target x Moniker)](/nuget/schema/target-frameworks) to operate with packages that don't declare a dotnet TxM.</span></span> <span data-ttu-id="af7fa-207">Si votre projet utilise le moniker du framework cible dotnet, tous les packages dont il dépend doivent également avoir un moniker du framework cible dotnet, sauf si vous ajoutez `<PackageTargetFallback>` à votre projet pour permettre aux plateformes autres que dotnet d’être compatibles avec dotnet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-207">If your project uses the dotnet TxM, then all the packages it depends on must also have a dotnet TxM, unless you add the `<PackageTargetFallback>` to your project in order to allow non-dotnet platforms to be compatible with dotnet.</span></span> 

<span data-ttu-id="af7fa-208">L’exemple suivant fournit les solutions de secours pour toutes les cibles dans votre projet :</span><span class="sxs-lookup"><span data-stu-id="af7fa-208">The following example provides the fallbacks for all targets in your project:</span></span> 

```xml
<PackageTargetFallback>
    $(PackageTargetFallback);portable-net45+win8+wpa81+wp8
</PackageTargetFallback >
```

<span data-ttu-id="af7fa-209">L’exemple suivant spécifie les solutions de secours uniquement pour la cible `netcoreapp2.1` :</span><span class="sxs-lookup"><span data-stu-id="af7fa-209">The following example specifies the fallbacks only for the `netcoreapp2.1` target:</span></span>

```xml
<PackageTargetFallback Condition="'$(TargetFramework)'=='netcoreapp2.1'">
    $(PackageTargetFallback);portable-net45+win8+wpa81+wp8
</PackageTargetFallback >
```

## <a name="nuget-metadata-properties"></a><span data-ttu-id="af7fa-210">Propriétés de métadonnées NuGet</span><span class="sxs-lookup"><span data-stu-id="af7fa-210">NuGet metadata properties</span></span>
<span data-ttu-id="af7fa-211">Avec le passage à MSBuild, nous avons transféré les métadonnées d’entrée utilisées lors de la compression d’un package NuGet des fichiers *project.json* vers les fichiers *csproj*.</span><span class="sxs-lookup"><span data-stu-id="af7fa-211">With the move to MSBuild, we have moved the input metadata that is used when packing a NuGet package from *project.json* to *.csproj* files.</span></span> <span data-ttu-id="af7fa-212">Les entrées sont des propriétés MSBuild qui doivent donc être placées dans un groupe `<PropertyGroup>`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-212">The inputs are MSBuild properties so they have to go within a `<PropertyGroup>` group.</span></span> <span data-ttu-id="af7fa-213">Voici la liste des propriétés qui sont utilisées comme entrées dans le processus de compression lors de l’utilisation de la commande `dotnet pack` ou de la cible MSBuild `Pack` qui fait partie du SDK.</span><span class="sxs-lookup"><span data-stu-id="af7fa-213">The following is the list of properties that are used as inputs to the packing process when using the `dotnet pack` command or the `Pack` MSBuild target that is part of the SDK.</span></span> 

### <a name="ispackable"></a><span data-ttu-id="af7fa-214">IsPackable</span><span class="sxs-lookup"><span data-stu-id="af7fa-214">IsPackable</span></span>
<span data-ttu-id="af7fa-215">Valeur booléenne qui spécifie si le projet peut être compressé.</span><span class="sxs-lookup"><span data-stu-id="af7fa-215">A Boolean value that specifies whether the project can be packed.</span></span> <span data-ttu-id="af7fa-216">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-216">The default value is `true`.</span></span> 

### <a name="packageversion"></a><span data-ttu-id="af7fa-217">PackageVersion</span><span class="sxs-lookup"><span data-stu-id="af7fa-217">PackageVersion</span></span>
<span data-ttu-id="af7fa-218">Spécifie la version du package obtenu.</span><span class="sxs-lookup"><span data-stu-id="af7fa-218">Specifies the version that the resulting package will have.</span></span> <span data-ttu-id="af7fa-219">Accepte toutes les formes de la chaîne de version NuGet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-219">Accepts all forms of NuGet version string.</span></span> <span data-ttu-id="af7fa-220">La valeur par défaut est la valeur de `$(Version)`, autrement dit, de la propriété `Version` dans le projet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-220">Default is the value of `$(Version)`, that is, of the property `Version` in the project.</span></span> 

### <a name="packageid"></a><span data-ttu-id="af7fa-221">PackageId</span><span class="sxs-lookup"><span data-stu-id="af7fa-221">PackageId</span></span>
<span data-ttu-id="af7fa-222">Spécifie le nom du package obtenu.</span><span class="sxs-lookup"><span data-stu-id="af7fa-222">Specifies the name for the resulting package.</span></span> <span data-ttu-id="af7fa-223">Si non spécifié, l’opération `pack` utilise par défaut le `AssemblyName` ou le nom du répertoire comme nom du package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-223">If not specified, the `pack` operation will default to using the `AssemblyName` or directory name as the name of the package.</span></span> 

### <a name="title"></a><span data-ttu-id="af7fa-224">Titre</span><span class="sxs-lookup"><span data-stu-id="af7fa-224">Title</span></span>
<span data-ttu-id="af7fa-225">Titre convivial du package, généralement utilisé dans les affichages de l’interface utilisateur comme sur nuget.org et dans le gestionnaire de package de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="af7fa-225">A human-friendly title of the package, typically used in UI displays as on nuget.org and the Package Manager in Visual Studio.</span></span> <span data-ttu-id="af7fa-226">Si non spécifié, l’ID de package est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="af7fa-226">If not specified, the package ID is used instead.</span></span>

### <a name="authors"></a><span data-ttu-id="af7fa-227">Auteurs</span><span class="sxs-lookup"><span data-stu-id="af7fa-227">Authors</span></span>
<span data-ttu-id="af7fa-228">Liste séparée par des points-virgules des auteurs de packages, qui correspondent aux noms de profil sur nuget.org. Ceux-ci sont affichés dans la galerie NuGet sur nuget.org et servent à croiser les références des packages de mêmes auteurs.</span><span class="sxs-lookup"><span data-stu-id="af7fa-228">A semicolon-separated list of packages authors, matching the profile names on nuget.org. These are displayed in the NuGet Gallery on nuget.org and are used to cross-reference packages by the same authors.</span></span>

### <a name="packagedescription"></a><span data-ttu-id="af7fa-229">PackageDescription</span><span class="sxs-lookup"><span data-stu-id="af7fa-229">PackageDescription</span></span>

<span data-ttu-id="af7fa-230">Description longue du package pour l’affichage de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="af7fa-230">A long description of the package for UI display.</span></span>

### <a name="description"></a><span data-ttu-id="af7fa-231">Description</span><span class="sxs-lookup"><span data-stu-id="af7fa-231">Description</span></span>
<span data-ttu-id="af7fa-232">Description longue de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="af7fa-232">A long description for the assembly.</span></span> <span data-ttu-id="af7fa-233">Si `PackageDescription` n’est pas spécifié, cette propriété est également utilisée comme description du package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-233">If `PackageDescription` is not specified then this property is also used as the description of the package.</span></span>

### <a name="copyright"></a><span data-ttu-id="af7fa-234">Copyright</span><span class="sxs-lookup"><span data-stu-id="af7fa-234">Copyright</span></span>
<span data-ttu-id="af7fa-235">Détails de copyright pour le package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-235">Copyright details for the package.</span></span>

### <a name="packagerequirelicenseacceptance"></a><span data-ttu-id="af7fa-236">PackageRequireLicenseAcceptance</span><span class="sxs-lookup"><span data-stu-id="af7fa-236">PackageRequireLicenseAcceptance</span></span>
<span data-ttu-id="af7fa-237">Valeur booléenne qui spécifie si le client doit inviter l’utilisateur à accepter la licence du package avant d’installer le package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-237">A Boolean value that specifies whether the client must prompt the consumer to accept the package license before installing the package.</span></span> <span data-ttu-id="af7fa-238">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-238">The default is `false`.</span></span>

### <a name="packagelicenseurl"></a><span data-ttu-id="af7fa-239">PackageLicenseUrl</span><span class="sxs-lookup"><span data-stu-id="af7fa-239">PackageLicenseUrl</span></span>
<span data-ttu-id="af7fa-240">URL vers la licence applicable au package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-240">An URL to the license that is applicable to the package.</span></span>

### <a name="packageprojecturl"></a><span data-ttu-id="af7fa-241">PackageProjectUrl</span><span class="sxs-lookup"><span data-stu-id="af7fa-241">PackageProjectUrl</span></span>
<span data-ttu-id="af7fa-242">URL de la page d’accueil du package, souvent affichée dans l’interface utilisateur ainsi que sur nuget.org.</span><span class="sxs-lookup"><span data-stu-id="af7fa-242">A URL for the package's home page, often shown in UI displays as well as nuget.org.</span></span>

### <a name="packageiconurl"></a><span data-ttu-id="af7fa-243">PackageIconUrl</span><span class="sxs-lookup"><span data-stu-id="af7fa-243">PackageIconUrl</span></span>
<span data-ttu-id="af7fa-244">URL d’une image 64 x 64 avec un arrière-plan transparent à utiliser comme icône pour le package dans l’affichage de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="af7fa-244">A URL for a 64x64 image with transparent background to use as the icon for the package in UI display.</span></span>

### <a name="packagereleasenotes"></a><span data-ttu-id="af7fa-245">PackageReleaseNotes</span><span class="sxs-lookup"><span data-stu-id="af7fa-245">PackageReleaseNotes</span></span>
<span data-ttu-id="af7fa-246">Notes de publication du package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-246">Release notes for the package.</span></span>

### <a name="packagetags"></a><span data-ttu-id="af7fa-247">PackageTags</span><span class="sxs-lookup"><span data-stu-id="af7fa-247">PackageTags</span></span>
<span data-ttu-id="af7fa-248">Liste de balises séparées par un point-virgule qui désigne le package.</span><span class="sxs-lookup"><span data-stu-id="af7fa-248">A semicolon-delimited list of tags that designates the package.</span></span>

### <a name="packageoutputpath"></a><span data-ttu-id="af7fa-249">PackageOutputPath</span><span class="sxs-lookup"><span data-stu-id="af7fa-249">PackageOutputPath</span></span>
<span data-ttu-id="af7fa-250">Détermine le chemin de sortie dans lequel le package compressé est déposé.</span><span class="sxs-lookup"><span data-stu-id="af7fa-250">Determines the output path in which the packed package will be dropped.</span></span> <span data-ttu-id="af7fa-251">La valeur par défaut est `$(OutputPath)`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-251">Default is `$(OutputPath)`.</span></span> 

### <a name="includesymbols"></a><span data-ttu-id="af7fa-252">IncludeSymbols</span><span class="sxs-lookup"><span data-stu-id="af7fa-252">IncludeSymbols</span></span>
<span data-ttu-id="af7fa-253">Cette valeur booléenne indique si le package doit créer un package de symboles supplémentaire quand le projet est compressé.</span><span class="sxs-lookup"><span data-stu-id="af7fa-253">This Boolean value indicates whether the package should create an additional symbols package when the project is packed.</span></span> <span data-ttu-id="af7fa-254">Ce package a une extension *.symbols.nupkg* et copie les fichiers PDB avec la DLL et d’autres fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="af7fa-254">This package will have a *.symbols.nupkg* extension and will copy the PDB files along with the DLL and other output files.</span></span>

### <a name="includesource"></a><span data-ttu-id="af7fa-255">IncludeSource</span><span class="sxs-lookup"><span data-stu-id="af7fa-255">IncludeSource</span></span>
<span data-ttu-id="af7fa-256">Cette valeur booléenne indique si le processus de compression doit créer un package source.</span><span class="sxs-lookup"><span data-stu-id="af7fa-256">This Boolean value indicates whether the pack process should create a source package.</span></span> <span data-ttu-id="af7fa-257">Le package source contient le code source de la bibliothèque ainsi que les fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="af7fa-257">The source package contains the library's source code as well as PDB files.</span></span> <span data-ttu-id="af7fa-258">Les fichiers sources sont placés dans le répertoire `src/ProjectName` dans le fichier de package obtenu.</span><span class="sxs-lookup"><span data-stu-id="af7fa-258">Source files are put under the `src/ProjectName` directory in the resulting package file.</span></span> 

### <a name="istool"></a><span data-ttu-id="af7fa-259">IsTool</span><span class="sxs-lookup"><span data-stu-id="af7fa-259">IsTool</span></span>
<span data-ttu-id="af7fa-260">Spécifie si tous les fichiers de sortie sont copiés dans le dossier *tools* au lieu du dossier *lib*.</span><span class="sxs-lookup"><span data-stu-id="af7fa-260">Specifies whether all output files are copied to the *tools* folder instead of the *lib* folder.</span></span> <span data-ttu-id="af7fa-261">Notez que cela est différent d’un `DotNetCliTool` qui est spécifié en définissant `PackageType` dans le fichier *.csproj*.</span><span class="sxs-lookup"><span data-stu-id="af7fa-261">Note that this is different from a `DotNetCliTool` which is specified by setting the `PackageType` in the *.csproj* file.</span></span>

### <a name="repositoryurl"></a><span data-ttu-id="af7fa-262">RepositoryUrl</span><span class="sxs-lookup"><span data-stu-id="af7fa-262">RepositoryUrl</span></span>
<span data-ttu-id="af7fa-263">Spécifie l’URL du dépôt où réside le code source du package et/ou à partir de laquelle il est généré.</span><span class="sxs-lookup"><span data-stu-id="af7fa-263">Specifies the URL for the repository where the source code for the package resides and/or from which it's being built.</span></span> 

### <a name="repositorytype"></a><span data-ttu-id="af7fa-264">RepositoryType</span><span class="sxs-lookup"><span data-stu-id="af7fa-264">RepositoryType</span></span>
<span data-ttu-id="af7fa-265">Spécifie le type de dépôt.</span><span class="sxs-lookup"><span data-stu-id="af7fa-265">Specifies the type of the repository.</span></span> <span data-ttu-id="af7fa-266">La valeur par défaut est « git ».</span><span class="sxs-lookup"><span data-stu-id="af7fa-266">Default is "git".</span></span> 

### <a name="nopackageanalysis"></a><span data-ttu-id="af7fa-267">NoPackageAnalysis</span><span class="sxs-lookup"><span data-stu-id="af7fa-267">NoPackageAnalysis</span></span>
<span data-ttu-id="af7fa-268">Spécifie que le pack ne doit pas exécuter d’analyse du package après sa génération.</span><span class="sxs-lookup"><span data-stu-id="af7fa-268">Specifies that pack should not run package analysis after building the package.</span></span>

### <a name="minclientversion"></a><span data-ttu-id="af7fa-269">MinClientVersion</span><span class="sxs-lookup"><span data-stu-id="af7fa-269">MinClientVersion</span></span>
<span data-ttu-id="af7fa-270">Spécifie la version minimale du client NuGet qui peut installer ce package, appliquée par nuget.exe et le gestionnaire de package Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="af7fa-270">Specifies the minimum version of the NuGet client that can install this package, enforced by nuget.exe and the Visual Studio Package Manager.</span></span>

### <a name="includebuildoutput"></a><span data-ttu-id="af7fa-271">IncludeBuildOutput</span><span class="sxs-lookup"><span data-stu-id="af7fa-271">IncludeBuildOutput</span></span>
<span data-ttu-id="af7fa-272">Ces valeurs booléennes spécifient si les assemblys de sortie de génération doivent être compressés dans le fichier *.nupkg* ou non.</span><span class="sxs-lookup"><span data-stu-id="af7fa-272">This Boolean values specifies whether the build output assemblies should be packed into the *.nupkg* file or not.</span></span>

### <a name="includecontentinpack"></a><span data-ttu-id="af7fa-273">IncludeContentInPack</span><span class="sxs-lookup"><span data-stu-id="af7fa-273">IncludeContentInPack</span></span>
<span data-ttu-id="af7fa-274">Cette valeur booléenne indique si tous les éléments qui ont un type `Content` sont automatiquement inclus dans le package obtenu.</span><span class="sxs-lookup"><span data-stu-id="af7fa-274">This Boolean value specifies whether any items that have a type of `Content` will be included in the resulting package automatically.</span></span> <span data-ttu-id="af7fa-275">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-275">The default is `true`.</span></span> 

### <a name="buildoutputtargetfolder"></a><span data-ttu-id="af7fa-276">BuildOutputTargetFolder</span><span class="sxs-lookup"><span data-stu-id="af7fa-276">BuildOutputTargetFolder</span></span>
<span data-ttu-id="af7fa-277">Spécifie le dossier où placer les assemblys de sortie.</span><span class="sxs-lookup"><span data-stu-id="af7fa-277">Specifies the folder where to place the output assemblies.</span></span> <span data-ttu-id="af7fa-278">Les assemblys de sortie (et les autres fichiers de sortie) sont copiés dans les dossiers de leur framework respectif.</span><span class="sxs-lookup"><span data-stu-id="af7fa-278">The output assemblies (and other output files) are copied into their respective framework folders.</span></span>

### <a name="contenttargetfolders"></a><span data-ttu-id="af7fa-279">ContentTargetFolders</span><span class="sxs-lookup"><span data-stu-id="af7fa-279">ContentTargetFolders</span></span>
<span data-ttu-id="af7fa-280">Cette propriété spécifie l’emplacement par défaut où placer tous les fichiers de contenu si `PackagePath` n’est pas spécifié pour eux.</span><span class="sxs-lookup"><span data-stu-id="af7fa-280">This property specifies the default location of where all the content files should go if `PackagePath` is not specified for them.</span></span> <span data-ttu-id="af7fa-281">La valeur par défaut est « content;contentFiles ».</span><span class="sxs-lookup"><span data-stu-id="af7fa-281">The default value is "content;contentFiles".</span></span>

### <a name="nuspecfile"></a><span data-ttu-id="af7fa-282">NuspecFile</span><span class="sxs-lookup"><span data-stu-id="af7fa-282">NuspecFile</span></span>
<span data-ttu-id="af7fa-283">Chemin relatif ou absolu du fichier *.nuspec* utilisé pour la compression.</span><span class="sxs-lookup"><span data-stu-id="af7fa-283">Relative or absolute path to the *.nuspec* file being used for packing.</span></span> 

> [!NOTE]
> <span data-ttu-id="af7fa-284">Si le fichier *.nuspec* est spécifié, il est utilisé **exclusivement** pour les informations de packaging et toutes les informations non utilisées dans les projets.</span><span class="sxs-lookup"><span data-stu-id="af7fa-284">If the *.nuspec* file is specified, it's used **exclusively** for packaging information and any information in the projects is not used.</span></span> 

### <a name="nuspecbasepath"></a><span data-ttu-id="af7fa-285">NuspecBasePath</span><span class="sxs-lookup"><span data-stu-id="af7fa-285">NuspecBasePath</span></span>
<span data-ttu-id="af7fa-286">Chemin de base pour le fichier *.nuspec*.</span><span class="sxs-lookup"><span data-stu-id="af7fa-286">Base path for the *.nuspec* file.</span></span>

### <a name="nuspecproperties"></a><span data-ttu-id="af7fa-287">NuspecProperties</span><span class="sxs-lookup"><span data-stu-id="af7fa-287">NuspecProperties</span></span>
<span data-ttu-id="af7fa-288">Liste de paires clé=valeur séparées par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="af7fa-288">Semicolon separated list of key=value pairs.</span></span>

## <a name="assemblyinfo-properties"></a><span data-ttu-id="af7fa-289">Propriétés AssemblyInfo</span><span class="sxs-lookup"><span data-stu-id="af7fa-289">AssemblyInfo properties</span></span>
<span data-ttu-id="af7fa-290">Les [attributs d’assembly](../../framework/app-domains/set-assembly-attributes.md) qui figurent généralement dans un fichier *AssemblyInfo* désormais générés automatiquement à partir des propriétés.</span><span class="sxs-lookup"><span data-stu-id="af7fa-290">[Assembly attributes](../../framework/app-domains/set-assembly-attributes.md) that were typically present in an *AssemblyInfo* file are now automatically generated from properties.</span></span>

### <a name="properties-per-attribute"></a><span data-ttu-id="af7fa-291">Propriétés par attribut</span><span class="sxs-lookup"><span data-stu-id="af7fa-291">Properties per attribute</span></span>

<span data-ttu-id="af7fa-292">Chaque attribut a une propriété qui contrôle son contenu et une autre pour désactiver sa génération, comme indiqué dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="af7fa-292">Each attribute has a property that control its content and another to disable its generation as shown in the following table:</span></span>

| <span data-ttu-id="af7fa-293">Attribut</span><span class="sxs-lookup"><span data-stu-id="af7fa-293">Attribute</span></span>                                                      | <span data-ttu-id="af7fa-294">Property</span><span class="sxs-lookup"><span data-stu-id="af7fa-294">Property</span></span>               | <span data-ttu-id="af7fa-295">Propriété permettant de désactiver</span><span class="sxs-lookup"><span data-stu-id="af7fa-295">Property to disable</span></span>                             |
|----------------------------------------------------------------|------------------------|-------------------------------------------------|
| <xref:System.Reflection.AssemblyCompanyAttribute>              | `Company`              | `GenerateAssemblyCompanyAttribute`              |
| <xref:System.Reflection.AssemblyConfigurationAttribute>        | `Configuration`        | `GenerateAssemblyConfigurationAttribute`        |
| <xref:System.Reflection.AssemblyCopyrightAttribute>            | `Copyright`            | `GenerateAssemblyCopyrightAttribute`            |
| <xref:System.Reflection.AssemblyDescriptionAttribute>          | `Description`          | `GenerateAssemblyDescriptionAttribute`          |
| <xref:System.Reflection.AssemblyFileVersionAttribute>          | `FileVersion`          | `GenerateAssemblyFileVersionAttribute`          |
| <xref:System.Reflection.AssemblyInformationalVersionAttribute> | `InformationalVersion` | `GenerateAssemblyInformationalVersionAttribute` |
| <xref:System.Reflection.AssemblyProductAttribute>              | `Product`              | `GenerateAssemblyProductAttribute`              |
| <xref:System.Reflection.AssemblyTitleAttribute>                | `AssemblyTitle`        | `GenerateAssemblyTitleAttribute`                |
| <xref:System.Reflection.AssemblyVersionAttribute>              | `AssemblyVersion`      | `GenerateAssemblyVersionAttribute`              |
| <xref:System.Resources.NeutralResourcesLanguageAttribute>      | `NeutralLanguage`      | `GenerateNeutralResourcesLanguageAttribute`     |

<span data-ttu-id="af7fa-296">Remarques :</span><span class="sxs-lookup"><span data-stu-id="af7fa-296">Notes:</span></span>

* <span data-ttu-id="af7fa-297">Le comportement par défaut de `AssemblyVersion` et `FileVersion` consiste à prendre la valeur de `$(Version)` sans suffixe.</span><span class="sxs-lookup"><span data-stu-id="af7fa-297">`AssemblyVersion` and `FileVersion` default is to take the value of `$(Version)` without suffix.</span></span> <span data-ttu-id="af7fa-298">Par exemple, si `$(Version)` est `1.2.3-beta.4`, alors la valeur serait `1.2.3`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-298">For example, if `$(Version)` is `1.2.3-beta.4`, then the value would be `1.2.3`.</span></span>
* <span data-ttu-id="af7fa-299">`InformationalVersion` utilise par défaut la valeur de `$(Version)`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-299">`InformationalVersion` defaults to the value of `$(Version)`.</span></span>
* <span data-ttu-id="af7fa-300">`$(SourceRevisionId)` est ajouté à `InformationalVersion` si la propriété est présente.</span><span class="sxs-lookup"><span data-stu-id="af7fa-300">`InformationalVersion` has `$(SourceRevisionId)` appended if the property is present.</span></span> <span data-ttu-id="af7fa-301">Cela peut être désactivé à l’aide de `IncludeSourceRevisionInInformationalVersion`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-301">It can be disabled using `IncludeSourceRevisionInInformationalVersion`.</span></span>
* <span data-ttu-id="af7fa-302">Les propriétés `Copyright` et `Description` sont également utilisées pour les métadonnées NuGet.</span><span class="sxs-lookup"><span data-stu-id="af7fa-302">`Copyright` and `Description` properties are also used for NuGet metadata.</span></span>
* <span data-ttu-id="af7fa-303">`Configuration` est partagé avec le processus de génération et défini par le biais du paramètre `--configuration` des commandes `dotnet`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-303">`Configuration` is shared with all the build process and set via the `--configuration` parameter of `dotnet` commands.</span></span>

### <a name="generateassemblyinfo"></a><span data-ttu-id="af7fa-304">GenerateAssemblyInfo</span><span class="sxs-lookup"><span data-stu-id="af7fa-304">GenerateAssemblyInfo</span></span> 
<span data-ttu-id="af7fa-305">Valeur booléenne qui active ou désactive la génération AssemblyInfo.</span><span class="sxs-lookup"><span data-stu-id="af7fa-305">A Boolean that enable or disable all the AssemblyInfo generation.</span></span> <span data-ttu-id="af7fa-306">La valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="af7fa-306">The default value is `true`.</span></span> 

### <a name="generatedassemblyinfofile"></a><span data-ttu-id="af7fa-307">GeneratedAssemblyInfoFile</span><span class="sxs-lookup"><span data-stu-id="af7fa-307">GeneratedAssemblyInfoFile</span></span> 
<span data-ttu-id="af7fa-308">Chemin d’accès du fichier d’informations sur l’assembly généré.</span><span class="sxs-lookup"><span data-stu-id="af7fa-308">The path of the generated assembly info file.</span></span> <span data-ttu-id="af7fa-309">Utilise par défaut un fichier dans le répertoire `$(IntermediateOutputPath)` (obj).</span><span class="sxs-lookup"><span data-stu-id="af7fa-309">Default to a file in the `$(IntermediateOutputPath)` (obj) directory.</span></span>
