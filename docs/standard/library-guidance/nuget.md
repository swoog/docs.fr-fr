---
title: Bibliothèques NuGet et .NET
description: Meilleures pratiques recommandées pour l’empaquetage avec NuGet pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: d0ea462a7f52dd9a6b2f14be9ed5770160bf66b1
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374490"
---
# <a name="nuget"></a><span data-ttu-id="a410f-103">NuGet</span><span class="sxs-lookup"><span data-stu-id="a410f-103">NuGet</span></span>

<span data-ttu-id="a410f-104">NuGet est un gestionnaire de package pour l’écosystème .NET et est passé, les développeurs principal découvrir et d’obtenir les bibliothèques .NET open source.</span><span class="sxs-lookup"><span data-stu-id="a410f-104">NuGet is a package manager for the .NET ecosystem and is the primary way developers discover and acquire .NET open-source libraries.</span></span> <span data-ttu-id="a410f-105">[NuGet.org](https://www.nuget.org/), un service gratuit fourni par Microsoft pour l’hébergement de packages NuGet, est l’hôte principal pour les packages NuGet publiques, mais vous pouvez publier dans les services de NuGet personnalisés tels que [MyGet](https://www.myget.org/) et [les artefacts Azure ](https://azure.microsoft.com/services/devops/artifacts/).</span><span class="sxs-lookup"><span data-stu-id="a410f-105">[NuGet.org](https://www.nuget.org/), a free service provided by Microsoft for hosting NuGet packages, is the primary host for public NuGet packages, but you can publish to custom NuGet services like [MyGet](https://www.myget.org/) and [Azure Artifacts](https://azure.microsoft.com/services/devops/artifacts/).</span></span>

<span data-ttu-id="a410f-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span><span class="sxs-lookup"><span data-stu-id="a410f-106">![NuGet](./media/nuget/nuget-logo.png "NuGet")</span></span>

## <a name="create-a-nuget-package"></a><span data-ttu-id="a410f-107">Créer un package NuGet</span><span class="sxs-lookup"><span data-stu-id="a410f-107">Create a NuGet package</span></span>

<span data-ttu-id="a410f-108">Un package NuGet (`*.nupkg`) est un fichier zip qui contient les assemblys .NET et les métadonnées associées.</span><span class="sxs-lookup"><span data-stu-id="a410f-108">A NuGet package (`*.nupkg`) is a zip file that contains .NET assemblies and associated metadata.</span></span>

<span data-ttu-id="a410f-109">Il existe deux façons de créer un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="a410f-109">There are two main ways to create a NuGet package.</span></span> <span data-ttu-id="a410f-110">La plus récente et recommandée consiste à créer un package à partir d’un projet de SDK-style (fichier de projet dont le contenu commence par `<Project Sdk="Microsoft.NET.Sdk">`).</span><span class="sxs-lookup"><span data-stu-id="a410f-110">The newer and recommended way is to create a package from a SDK-style project (project file whose content starts with `<Project Sdk="Microsoft.NET.Sdk">`).</span></span> <span data-ttu-id="a410f-111">Assemblys et cibles sont automatiquement ajoutés au package et restant des métadonnées est ajoutée au fichier MSBuild, comme le numéro de version et de nom de package.</span><span class="sxs-lookup"><span data-stu-id="a410f-111">Assemblies and targets are automatically added to the package and remaining metadata is added to the MSBuild file, like package name and version number.</span></span> <span data-ttu-id="a410f-112">Compilation avec le [ `dotnet pack` ](../../core/tools/dotnet-pack.md) commande sorties un `*.nupkg` fichier au lieu des assemblys.</span><span class="sxs-lookup"><span data-stu-id="a410f-112">Compiling with the [`dotnet pack`](../../core/tools/dotnet-pack.md) command outputs a `*.nupkg` file instead of assemblies.</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFramework>netstandard2.0</TargetFramework>
    <AssemblyName>Contoso.Api</AssemblyName>
    <PackageVersion>1.1.0</PackageVersion>
    <Authors>John Doe</Authors>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="a410f-113">L’ancienne méthode de création d’un package NuGet est avec un `*.nuspec` fichier et le `nuget.exe` outil de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a410f-113">The older way of creating a NuGet package is with a `*.nuspec` file and the `nuget.exe` command-line tool.</span></span> <span data-ttu-id="a410f-114">Un fichier nuspec vous donne un contrôle, mais vous devez spécifier soigneusement les assemblys et les cibles à inclure dans le package NuGet final.</span><span class="sxs-lookup"><span data-stu-id="a410f-114">A nuspec file gives you great control but you must carefully specify what assemblies and targets to include in the final NuGet package.</span></span> <span data-ttu-id="a410f-115">Il est facile de commettre une erreur ou pour une personne d’oublier de mettre à jour le fichier nuspec lors des modifications.</span><span class="sxs-lookup"><span data-stu-id="a410f-115">It's easy to make a mistake or for someone to forget to update the nuspec when making changes.</span></span> <span data-ttu-id="a410f-116">L’avantage d’un fichier nuspec est de vous permet de créer des packages NuGet pour les infrastructures qui ne gèrent pas encore un fichier de projet de style SDK.</span><span class="sxs-lookup"><span data-stu-id="a410f-116">The advantage of a nuspec is you can use it create NuGet packages for frameworks that don't yet support an SDK-style project file.</span></span>

<span data-ttu-id="a410f-117">**ENVISAGEZ de ✔️** à l’aide d’un fichier de projet de style SDK pour créer le package NuGet.</span><span class="sxs-lookup"><span data-stu-id="a410f-117">**✔️ CONSIDER** using an SDK-style project file to create the NuGet package.</span></span>

<span data-ttu-id="a410f-118">**ENVISAGEZ de ✔️** configuration SourceLink afin d’ajouter les métadonnées de contrôle de code source à vos assemblys et le package NuGet.</span><span class="sxs-lookup"><span data-stu-id="a410f-118">**✔️ CONSIDER** setting up SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

## <a name="package-dependencies"></a><span data-ttu-id="a410f-119">Dépendances de package</span><span class="sxs-lookup"><span data-stu-id="a410f-119">Package dependencies</span></span>

<span data-ttu-id="a410f-120">Dépendances de package NuGet sont traitées en détail dans le [dépendances](./dependencies.md) article.</span><span class="sxs-lookup"><span data-stu-id="a410f-120">NuGet package dependencies are covered in detail in the [Dependencies](./dependencies.md) article.</span></span>

## <a name="important-nuget-package-metadata"></a><span data-ttu-id="a410f-121">Métadonnées de package NuGet importantes</span><span class="sxs-lookup"><span data-stu-id="a410f-121">Important NuGet package metadata</span></span>

<span data-ttu-id="a410f-122">Un package NuGet prend en charge plusieurs [propriétés de métadonnées](/nuget/reference/nuspec).</span><span class="sxs-lookup"><span data-stu-id="a410f-122">A NuGet package supports many [metadata properties](/nuget/reference/nuspec).</span></span> <span data-ttu-id="a410f-123">Le tableau suivant contient les métadonnées de base que chaque projet open source doit fournir :</span><span class="sxs-lookup"><span data-stu-id="a410f-123">The following table contains the core metadata that every open-source project should provide:</span></span>

| <span data-ttu-id="a410f-124">Nom de la propriété MSBuild</span><span class="sxs-lookup"><span data-stu-id="a410f-124">MSBuild Property name</span></span>              | <span data-ttu-id="a410f-125">Nom de fichier NuSpec</span><span class="sxs-lookup"><span data-stu-id="a410f-125">Nuspec name</span></span>              | <span data-ttu-id="a410f-126">Description</span><span class="sxs-lookup"><span data-stu-id="a410f-126">Description</span></span>  |
| ---------------------------------- | ------------------------ | ------------ |
| `PackageId`                        | `id`                       | <span data-ttu-id="a410f-127">L’identificateur du package.</span><span class="sxs-lookup"><span data-stu-id="a410f-127">The package identifier.</span></span> <span data-ttu-id="a410f-128">Un préfixe de l’identificateur peut être réservé s’il répond à la [critères](/nuget/reference/id-prefix-reservation).</span><span class="sxs-lookup"><span data-stu-id="a410f-128">A prefix from the identifier can be reserved if it meets the [criteria](/nuget/reference/id-prefix-reservation).</span></span> |
| `PackageVersion`                   | `version`                  | <span data-ttu-id="a410f-129">Version du package NuGet.</span><span class="sxs-lookup"><span data-stu-id="a410f-129">NuGet package version.</span></span> <span data-ttu-id="a410f-130">Pour plus d’informations, consultez [version du package NuGet](./versioning.md#nuget-package-version).</span><span class="sxs-lookup"><span data-stu-id="a410f-130">For more information, see [NuGet package version](./versioning.md#nuget-package-version).</span></span>             |
| `Title`                            | `title`                    | <span data-ttu-id="a410f-131">Un titre convivial du package.</span><span class="sxs-lookup"><span data-stu-id="a410f-131">A human-friendly title of the package.</span></span> <span data-ttu-id="a410f-132">Les valeurs par défaut pour le `PackageId`.</span><span class="sxs-lookup"><span data-stu-id="a410f-132">It defaults to the `PackageId`.</span></span>             |
| `Description`                      | `description`              | <span data-ttu-id="a410f-133">Longue description du package affiché dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a410f-133">A long description of the package displayed in UI.</span></span>             |
| `Authors`                          | `authors`                  | <span data-ttu-id="a410f-134">Liste séparée par des virgules des auteurs de packages, correspondent aux noms de profil sur nuget.org.</span><span class="sxs-lookup"><span data-stu-id="a410f-134">A comma-separated list of package authors, matching the profile names on nuget.org.</span></span>             |
| `PackageTags`                      | `tags`                     | <span data-ttu-id="a410f-135">Une liste délimitée de balises et les mots clés qui décrivent le package.</span><span class="sxs-lookup"><span data-stu-id="a410f-135">A space-delimited list of tags and keywords that describe the package.</span></span> <span data-ttu-id="a410f-136">Les balises sont utilisées lors de la recherche pour les packages.</span><span class="sxs-lookup"><span data-stu-id="a410f-136">Tags are used when searching for packages.</span></span>             |
| `PackageIconUrl`                   | `iconUrl`                  | <span data-ttu-id="a410f-137">URL d’une image à utiliser comme icône pour le package.</span><span class="sxs-lookup"><span data-stu-id="a410f-137">A URL for an image to use as the icon for the package.</span></span> <span data-ttu-id="a410f-138">URL doit être HTTPS et l’image doit être de 64 x 64 et un arrière-plan transparent.</span><span class="sxs-lookup"><span data-stu-id="a410f-138">URL should be HTTPS and the image should be 64x64 and have a transparent background.</span></span>             |
| `PackageProjectUrl`                | `projectUrl`               | <span data-ttu-id="a410f-139">Une URL pour le dépôt source ou de la page d’accueil du projet.</span><span class="sxs-lookup"><span data-stu-id="a410f-139">A URL for the project homepage or source repository.</span></span>             |
| `PackageLicenseUrl`                | `licenseUrl`               | <span data-ttu-id="a410f-140">Une URL à la licence de projet.</span><span class="sxs-lookup"><span data-stu-id="a410f-140">A URL to the project license.</span></span> <span data-ttu-id="a410f-141">Peut être l’URL vers le `LICENSE` fichier dans le contrôle de code source.</span><span class="sxs-lookup"><span data-stu-id="a410f-141">Can be the URL to the `LICENSE` file in source control.</span></span>             |

<span data-ttu-id="a410f-142">**ENVISAGEZ de ✔️** choisir un nom de package NuGet avec un préfixe qui répond à la réservation du préfixe de NuGet [critères](/nuget/reference/id-prefix-reservation).</span><span class="sxs-lookup"><span data-stu-id="a410f-142">**✔️ CONSIDER** choosing a NuGet package name with a prefix that meets NuGet's prefix reservation [criteria](/nuget/reference/id-prefix-reservation).</span></span>

<span data-ttu-id="a410f-143">**✔️ Envisagez** à l’aide de la `LICENSE` fichier dans le contrôle de code source en tant que le `LicenseUrl`.</span><span class="sxs-lookup"><span data-stu-id="a410f-143">**✔️ CONSIDER** using the `LICENSE` file in source control as the `LicenseUrl`.</span></span> <span data-ttu-id="a410f-144">Par exemple, [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md).</span><span class="sxs-lookup"><span data-stu-id="a410f-144">For example, [LICENSE.md](https://github.com/JamesNK/Newtonsoft.Json/blob/c4af75c8e91ca0d75aa6c335e8c106780c4f7712/LICENSE.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a410f-145">Un projet sans une licence par défaut est [copyright exclusif](https://choosealicense.com/no-permission/), ce qui empêche d’autres personnes à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a410f-145">A project without a license defaults to [exclusive copyright](https://choosealicense.com/no-permission/), making it impossible for other people to use.</span></span>

<span data-ttu-id="a410f-146">**FAIRE ✔️** utiliser une href HTTPS à l’icône de votre package.</span><span class="sxs-lookup"><span data-stu-id="a410f-146">**✔️ DO** use an HTTPS href to your package icon.</span></span>

> <span data-ttu-id="a410f-147">Exécutent des sites comme NuGet.org avec le protocole HTTPS est activé et afficher une image non-HTTPS créera un avertissement de contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="a410f-147">Sites like NuGet.org run with HTTPS enabled and displaying a non-HTTPS image will create a mixed content warning.</span></span>

<span data-ttu-id="a410f-148">**FAIRE ✔️** utiliser une image d’icône de package qui est de 64 x 64 et a un arrière-plan transparent pour optimiser l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a410f-148">**✔️ DO** use a package icon image that is 64x64 and has a transparent background for best viewing results.</span></span>

## <a name="pre-release-packages"></a><span data-ttu-id="a410f-149">Packages de préversion</span><span class="sxs-lookup"><span data-stu-id="a410f-149">Pre-release packages</span></span>

<span data-ttu-id="a410f-150">Les packages NuGet avec un suffixe de version sont considérés comme [préliminaires](/nuget/create-packages/prerelease-packages).</span><span class="sxs-lookup"><span data-stu-id="a410f-150">NuGet packages with a version suffix are considered [pre-release](/nuget/create-packages/prerelease-packages).</span></span> <span data-ttu-id="a410f-151">Par défaut, le Gestionnaire de Package NuGet UI affiche les versions stables, sauf si un utilisateur choisit de pré-version de packages, ce qui rend les packages de la version préliminaire idéal pour les tests utilisateur limité.</span><span class="sxs-lookup"><span data-stu-id="a410f-151">By default, the NuGet Package Manager UI shows stable releases unless a user opts-in to pre-release packages, making pre-release packages ideal for limited user testing.</span></span>

```xml
<PackageVersion>1.0.1-beta1</PackageVersion>
```

> [!NOTE]
> <span data-ttu-id="a410f-152">Un package stable ne peut pas dépendre d’un package de version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="a410f-152">A stable package cannot depend on a pre-release package.</span></span> <span data-ttu-id="a410f-153">Vous devez mettre votre propre package préliminaires ou dépendent d’une version stable antérieure.</span><span class="sxs-lookup"><span data-stu-id="a410f-153">You must either make your own package pre-release or depend on an older stable version.</span></span>

<span data-ttu-id="a410f-154">![Dépendance de package de version préliminaire de NuGet](./media/nuget/nuget-prerelease-package.png "dépendance de package de version préliminaire de NuGet")</span><span class="sxs-lookup"><span data-stu-id="a410f-154">![NuGet pre-release package dependency](./media/nuget/nuget-prerelease-package.png "NuGet pre-release package dependency")</span></span>

<span data-ttu-id="a410f-155">**FAIRE ✔️** publier un package de version préliminaire lors de tests, l’aperçu ou de l’expérimentation.</span><span class="sxs-lookup"><span data-stu-id="a410f-155">**✔️ DO** publish a pre-release package when testing, previewing, or experimenting.</span></span>

<span data-ttu-id="a410f-156">**FAIRE ✔️** publier un package stable lorsque son prêt pour que d’autres packages stables y faire référence.</span><span class="sxs-lookup"><span data-stu-id="a410f-156">**✔️ DO** publish a stable package when its ready so other stable packages can reference it.</span></span>

## <a name="symbol-packages"></a><span data-ttu-id="a410f-157">Packages de symboles</span><span class="sxs-lookup"><span data-stu-id="a410f-157">Symbol packages</span></span>

<span data-ttu-id="a410f-158">NuGet prend en charge [génération d’un package de symboles distincts](/nuget/create-packages/symbol-packages) contenant de déboguer les fichiers PDB en même temps que le package principal contenant les assemblys .NET.</span><span class="sxs-lookup"><span data-stu-id="a410f-158">NuGet supports [generating a separate symbol package](/nuget/create-packages/symbol-packages) containing debug PDB files alongside the main package containing .NET assemblies.</span></span> <span data-ttu-id="a410f-159">L’idée de packages de symboles est qu’ils sont hébergés sur un serveur de symboles et sont téléchargés uniquement par un outil tel que Visual Studio à la demande.</span><span class="sxs-lookup"><span data-stu-id="a410f-159">The idea of symbol packages is they're hosted on a symbol server and are only downloaded by a tool like Visual Studio on demand.</span></span>

<span data-ttu-id="a410f-160">Actuellement l’hôte publique principale pour les symboles - [SymbolSource](http://www.symbolsource.org/) -ne prend pas en charge les fichiers PDB portables créés par le Kit de développement logiciel-style projets et packages de symboles ne sont pas utiles.</span><span class="sxs-lookup"><span data-stu-id="a410f-160">Currently the main public host for symbols - [SymbolSource](http://www.symbolsource.org/) - doesn't support the portable PDBs created by SDK-style projects and symbol packages aren't useful.</span></span>

<span data-ttu-id="a410f-161">**ENVISAGEZ de ✔️** l’incorporation de fichiers PDB dans le package NuGet principal.</span><span class="sxs-lookup"><span data-stu-id="a410f-161">**✔️ CONSIDER** embedding PDBs in the main NuGet package.</span></span>

<span data-ttu-id="a410f-162">**Évitez de ❌** création d’un package de symboles contenant les fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="a410f-162">**❌ AVOID** creating a symbols package containing PDBs.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="a410f-163">[Précédent](./strong-naming.md)
[Suivant](./dependencies.md)</span><span class="sxs-lookup"><span data-stu-id="a410f-163">[Previous](./strong-naming.md)
[Next](./dependencies.md)</span></span>
