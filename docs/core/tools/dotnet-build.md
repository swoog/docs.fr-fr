---
title: Commande dotnet build - Interface CLI .NET Core
description: La commande dotnet build permet de générer un projet et l’ensemble de ses dépendances.
author: mairaw
ms.author: mairaw
ms.date: 05/25/2018
ms.openlocfilehash: 6b0b7bc11b560d8632b38f1dfa4e7eb3ce6c54d2
ms.sourcegitcommit: 60645077dc4b62178403145f8ef691b13ffec28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2018
ms.locfileid: "37961455"
---
# <a name="dotnet-build"></a><span data-ttu-id="29a06-103">dotnet-build</span><span class="sxs-lookup"><span data-stu-id="29a06-103">dotnet-build</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="29a06-104">Name</span><span class="sxs-lookup"><span data-stu-id="29a06-104">Name</span></span>

<span data-ttu-id="29a06-105">`dotnet build` : Génère un projet et l’ensemble de ses dépendances.</span><span class="sxs-lookup"><span data-stu-id="29a06-105">`dotnet build` - Builds a project and all of its dependencies.</span></span>

## <a name="synopsis"></a><span data-ttu-id="29a06-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="29a06-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="29a06-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="29a06-107">.NET Core 2.x</span></span>](#tab/netcore2x)
```
dotnet build [<PROJECT>] [-c|--configuration] [-f|--framework] [--force] [--no-dependencies] [--no-incremental]
    [--no-restore] [-o|--output] [-r|--runtime] [-v|--verbosity] [--version-suffix]
dotnet build [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="29a06-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="29a06-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet build [<PROJECT>] [-c|--configuration] [-f|--framework] [--no-dependencies] [--no-incremental] [-o|--output]
    [-r|--runtime] [-v|--verbosity] [--version-suffix]
dotnet build [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="29a06-109">Description</span><span class="sxs-lookup"><span data-stu-id="29a06-109">Description</span></span>

<span data-ttu-id="29a06-110">La commande `dotnet build` génère le projet et ses dépendances dans un ensemble de fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="29a06-110">The `dotnet build` command builds the project and its dependencies into a set of binaries.</span></span> <span data-ttu-id="29a06-111">Les fichiers binaires incluent le code du projet dans des fichiers en langage intermédiaire (IL) avec une extension *.dll* et les fichiers de symboles utilisés pour le débogage avec une extension *.pdb*.</span><span class="sxs-lookup"><span data-stu-id="29a06-111">The binaries include the project's code in Intermediate Language (IL) files with a *.dll* extension and symbol files used for debugging with a *.pdb* extension.</span></span> <span data-ttu-id="29a06-112">Un fichier JSON de dépendances (*\*.deps.json*) est généré. Il répertorie les dépendances de l’application.</span><span class="sxs-lookup"><span data-stu-id="29a06-112">A dependencies JSON file (*\*.deps.json*) is produced that lists the dependencies of the application.</span></span> <span data-ttu-id="29a06-113">Un fichier *\*.runtimeconfig.json* est généré. Il spécifie le runtime partagé et sa version pour l’application.</span><span class="sxs-lookup"><span data-stu-id="29a06-113">A *\*.runtimeconfig.json* file is produced, which specifies the shared runtime and its version for the application.</span></span>

<span data-ttu-id="29a06-114">Si le projet a des dépendances tierces, comme des bibliothèques NuGet, elles sont résolues à partir du cache NuGet et ne sont pas disponibles avec la sortie générée du projet.</span><span class="sxs-lookup"><span data-stu-id="29a06-114">If the project has third-party dependencies, such as libraries from NuGet, they're resolved from the NuGet cache and aren't available with the project's built output.</span></span> <span data-ttu-id="29a06-115">Par conséquent, le produit de `dotnet build` ne peut pas être transféré en l’état vers un autre ordinateur pour exécution.</span><span class="sxs-lookup"><span data-stu-id="29a06-115">With that in mind, the product of `dotnet build` isn't ready to be transferred to another machine to run.</span></span> <span data-ttu-id="29a06-116">Ce comportement contraste avec celui du .NET Framework dans lequel la génération d’un projet exécutable (une application) produit une sortie exécutable sur n’importe quel ordinateur où le .NET Framework est installé.</span><span class="sxs-lookup"><span data-stu-id="29a06-116">This is in contrast to the behavior of the .NET Framework in which building an executable project (an application) produces output that's runnable on any machine where the .NET Framework is installed.</span></span> <span data-ttu-id="29a06-117">Pour obtenir un résultat similaire dans .NET Core, vous devez utiliser la commande [dotnet publish](dotnet-publish.md).</span><span class="sxs-lookup"><span data-stu-id="29a06-117">To have a similar experience with .NET Core, you need to use the [dotnet publish](dotnet-publish.md) command.</span></span> <span data-ttu-id="29a06-118">Pour plus d’informations, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="29a06-118">For more information, see [.NET Core Application Deployment](../deploying/index.md).</span></span>

<span data-ttu-id="29a06-119">La génération requiert le fichier *project.assets.json* qui répertorie les dépendances de votre application.</span><span class="sxs-lookup"><span data-stu-id="29a06-119">Building requires the *project.assets.json* file, which lists the dependencies of your application.</span></span> <span data-ttu-id="29a06-120">Le fichier est créé quand la commande [`dotnet restore`](dotnet-restore.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="29a06-120">The file is created when [`dotnet restore`](dotnet-restore.md) is executed.</span></span> <span data-ttu-id="29a06-121">Si le fichier de ressources est absent, les outils ne peuvent pas résoudre les assemblys de référence, ce qui entraîne des erreurs.</span><span class="sxs-lookup"><span data-stu-id="29a06-121">Without the assets file in place, the tooling cannot resolve reference assemblies, which results in errors.</span></span> <span data-ttu-id="29a06-122">Avec le SDK .NET Core 1.x, vous deviez explicitement exécuter `dotnet restore` avant d’exécuter `dotnet build`.</span><span class="sxs-lookup"><span data-stu-id="29a06-122">With .NET Core 1.x SDK, you needed to explicitly run the `dotnet restore` before running `dotnet build`.</span></span> <span data-ttu-id="29a06-123">À compter du SDK .NET Core 2.0, `dotnet restore` s’exécute implicitement quand vous exécutez `dotnet build`.</span><span class="sxs-lookup"><span data-stu-id="29a06-123">Starting with .NET Core 2.0 SDK, `dotnet restore` runs implicitly when you run `dotnet build`.</span></span> <span data-ttu-id="29a06-124">Si vous souhaitez désactiver la restauration implicite au moment d’exécuter la commande de génération, vous pouvez passer l’option `--no-restore`.</span><span class="sxs-lookup"><span data-stu-id="29a06-124">If you want to disable implicit restore when running the build command, you can pass the `--no-restore` option.</span></span>

[!INCLUDE[dotnet restore note + options](~/includes/dotnet-restore-note-options.md)]

<span data-ttu-id="29a06-125">La commande `dotnet build` utilise MSBuild pour générer le projet. Elle prend donc en charge les builds parallèles et les builds incrémentielles.</span><span class="sxs-lookup"><span data-stu-id="29a06-125">`dotnet build` uses MSBuild to build the project, so it supports both parallel and incremental builds.</span></span> <span data-ttu-id="29a06-126">Pour plus d’informations, consultez l’article [Incremental Builds (Générations incrémentielles)](/visualstudio/msbuild/incremental-builds) .</span><span class="sxs-lookup"><span data-stu-id="29a06-126">For more information, see [Incremental Builds](/visualstudio/msbuild/incremental-builds).</span></span>

<span data-ttu-id="29a06-127">En plus de ses options, la commande `dotnet build` accepte des options MSBuild, comme `/p` pour définir des propriétés ou `/l` pour définir un enregistreur d’événements.</span><span class="sxs-lookup"><span data-stu-id="29a06-127">In addition to its options, the `dotnet build` command accepts MSBuild options, such as `/p` for setting properties or `/l` to define a logger.</span></span> <span data-ttu-id="29a06-128">Pour plus d’informations sur ces options, consultez [Informations de référence sur la ligne de commande MSBuild](/visualstudio/msbuild/msbuild-command-line-reference).</span><span class="sxs-lookup"><span data-stu-id="29a06-128">For more information about these options, see the [MSBuild Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference).</span></span>

<span data-ttu-id="29a06-129">La possibilité d’exécuter le projet ou non est déterminée par la propriété `<OutputType>` dans le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="29a06-129">Whether the project is executable or not is determined by the `<OutputType>` property in the project file.</span></span> <span data-ttu-id="29a06-130">L’exemple suivant illustre un projet qui génère du code exécutable :</span><span class="sxs-lookup"><span data-stu-id="29a06-130">The following example shows a project that produces executable code:</span></span>

```xml
<PropertyGroup>
  <OutputType>Exe</OutputType>
</PropertyGroup>
```

<span data-ttu-id="29a06-131">Pour générer une bibliothèque, omettez la propriété `<OutputType>`.</span><span class="sxs-lookup"><span data-stu-id="29a06-131">In order to produce a library, omit the `<OutputType>` property.</span></span> <span data-ttu-id="29a06-132">La principale différence dans la sortie générée est que la DLL de langage intermédiaire pour une bibliothèque ne contient pas de points d’entrée et ne peut pas être exécutée.</span><span class="sxs-lookup"><span data-stu-id="29a06-132">The main difference in built output is that the IL DLL for a library doesn't contain entry points and can't be executed.</span></span>

## <a name="arguments"></a><span data-ttu-id="29a06-133">Arguments</span><span class="sxs-lookup"><span data-stu-id="29a06-133">Arguments</span></span>

`PROJECT`

<span data-ttu-id="29a06-134">Fichier projet à générer.</span><span class="sxs-lookup"><span data-stu-id="29a06-134">The project file to build.</span></span> <span data-ttu-id="29a06-135">Si vous ne spécifiez pas de fichier projet, MSBuild recherche dans le répertoire de travail actuel un fichier avec une extension se terminant par *proj* et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="29a06-135">If a project file is not specified, MSBuild searches the current working directory for a file that has a file extension that ends in *proj* and uses that file.</span></span>

## <a name="options"></a><span data-ttu-id="29a06-136">Options</span><span class="sxs-lookup"><span data-stu-id="29a06-136">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="29a06-137">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="29a06-137">.NET Core 2.x</span></span>](#tab/netcore2x)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="29a06-138">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="29a06-138">Defines the build configuration.</span></span> <span data-ttu-id="29a06-139">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="29a06-139">The default value is `Debug`.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="29a06-140">Compile pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="29a06-140">Compiles for a specific [framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="29a06-141">Le framework doit être défini dans le [fichier projet](csproj.md).</span><span class="sxs-lookup"><span data-stu-id="29a06-141">The framework must be defined in the [project file](csproj.md).</span></span>

`--force`

<span data-ttu-id="29a06-142">Force la résolution de toutes les dépendances même si la dernière restauration a réussi.</span><span class="sxs-lookup"><span data-stu-id="29a06-142">Forces all dependencies to be resolved even if the last restore was successful.</span></span> <span data-ttu-id="29a06-143">Définir cet indicateur revient à supprimer le fichier *project.assets.json*.</span><span class="sxs-lookup"><span data-stu-id="29a06-143">Specifying this flag is the same as deleting the *project.assets.json* file.</span></span>

`-h|--help`

<span data-ttu-id="29a06-144">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="29a06-144">Prints out a short help for the command.</span></span>

`--no-dependencies`

<span data-ttu-id="29a06-145">Ignore les références entre projets (P2P) et génère uniquement le projet racine spécifié.</span><span class="sxs-lookup"><span data-stu-id="29a06-145">Ignores project-to-project (P2P) references and only builds the specified root project.</span></span>

`--no-incremental`

<span data-ttu-id="29a06-146">Marque la build comme unsafe pour la génération incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="29a06-146">Marks the build as unsafe for incremental build.</span></span> <span data-ttu-id="29a06-147">Cet indicateur désactive la compilation incrémentielle et force une regénération du graphique de dépendance du projet.</span><span class="sxs-lookup"><span data-stu-id="29a06-147">This flag turns off incremental compilation and forces a clean rebuild of the project's dependency graph.</span></span>

`--no-restore`

<span data-ttu-id="29a06-148">N’exécute pas de restauration implicite pendant la génération.</span><span class="sxs-lookup"><span data-stu-id="29a06-148">Doesn't execute an implicit restore during build.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="29a06-149">Répertoire dans lequel placer les fichiers binaires générés.</span><span class="sxs-lookup"><span data-stu-id="29a06-149">Directory in which to place the built binaries.</span></span> <span data-ttu-id="29a06-150">Vous devez également définir `--framework` lorsque vous spécifiez cette option.</span><span class="sxs-lookup"><span data-stu-id="29a06-150">You also need to define `--framework` when you specify this option.</span></span>

`-r|--runtime <RUNTIME_IDENTIFIER>`

<span data-ttu-id="29a06-151">Spécifie le runtime cible.</span><span class="sxs-lookup"><span data-stu-id="29a06-151">Specifies the target runtime.</span></span> <span data-ttu-id="29a06-152">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="29a06-152">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="29a06-153">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="29a06-153">Sets the verbosity level of the command.</span></span> <span data-ttu-id="29a06-154">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="29a06-154">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version-suffix <VERSION_SUFFIX>`

<span data-ttu-id="29a06-155">Définit le suffixe de version pour un astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="29a06-155">Defines the version suffix for an asterisk (`*`) in the version field of the project file.</span></span> <span data-ttu-id="29a06-156">Le format respecte les instructions de version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="29a06-156">The format follows NuGet's version guidelines.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="29a06-157">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="29a06-157">.NET Core 1.x</span></span>](#tab/netcore1x)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="29a06-158">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="29a06-158">Defines the build configuration.</span></span> <span data-ttu-id="29a06-159">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="29a06-159">The default value is `Debug`.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="29a06-160">Compile pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="29a06-160">Compiles for a specific [framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="29a06-161">Le framework doit être défini dans le [fichier projet](csproj.md).</span><span class="sxs-lookup"><span data-stu-id="29a06-161">The framework must be defined in the [project file](csproj.md).</span></span>

`-h|--help`

<span data-ttu-id="29a06-162">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="29a06-162">Prints out a short help for the command.</span></span>

`--no-dependencies`

<span data-ttu-id="29a06-163">Ignore les références entre projets (P2P) et génère uniquement le projet racine spécifié.</span><span class="sxs-lookup"><span data-stu-id="29a06-163">Ignores project-to-project (P2P) references and only builds the specified root project.</span></span>

`--no-incremental`

<span data-ttu-id="29a06-164">Marque la build comme unsafe pour la génération incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="29a06-164">Marks the build as unsafe for incremental build.</span></span> <span data-ttu-id="29a06-165">Cet indicateur désactive la compilation incrémentielle et force une regénération du graphique de dépendance du projet.</span><span class="sxs-lookup"><span data-stu-id="29a06-165">This flag turns off incremental compilation and forces a clean rebuild of the project's dependency graph.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="29a06-166">Répertoire dans lequel placer les fichiers binaires générés.</span><span class="sxs-lookup"><span data-stu-id="29a06-166">Directory in which to place the built binaries.</span></span> <span data-ttu-id="29a06-167">Vous devez également définir `--framework` lorsque vous spécifiez cette option.</span><span class="sxs-lookup"><span data-stu-id="29a06-167">You also need to define `--framework` when you specify this option.</span></span>

`-r|--runtime <RUNTIME_IDENTIFIER>`

<span data-ttu-id="29a06-168">Spécifie le runtime cible.</span><span class="sxs-lookup"><span data-stu-id="29a06-168">Specifies the target runtime.</span></span> <span data-ttu-id="29a06-169">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="29a06-169">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="29a06-170">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="29a06-170">Sets the verbosity level of the command.</span></span> <span data-ttu-id="29a06-171">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="29a06-171">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version-suffix <VERSION_SUFFIX>`

<span data-ttu-id="29a06-172">Définit le suffixe de version pour un astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="29a06-172">Defines the version suffix for an asterisk (`*`) in the version field of the project file.</span></span> <span data-ttu-id="29a06-173">Le format respecte les instructions de version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="29a06-173">The format follows NuGet's version guidelines.</span></span>

---

## <a name="examples"></a><span data-ttu-id="29a06-174">Exemples</span><span class="sxs-lookup"><span data-stu-id="29a06-174">Examples</span></span>

<span data-ttu-id="29a06-175">Générer un projet et ses dépendances :</span><span class="sxs-lookup"><span data-stu-id="29a06-175">Build a project and its dependencies:</span></span>

`dotnet build`

<span data-ttu-id="29a06-176">Générer un projet et ses dépendances à l’aide de la configuration Release :</span><span class="sxs-lookup"><span data-stu-id="29a06-176">Build a project and its dependencies using Release configuration:</span></span>

`dotnet build --configuration Release`

<span data-ttu-id="29a06-177">Générer un projet et ses dépendances pour un runtime spécifique (dans cet exemple, Ubuntu 16.04) :</span><span class="sxs-lookup"><span data-stu-id="29a06-177">Build a project and its dependencies for a specific runtime (in this example, Ubuntu 16.04):</span></span>

`dotnet build --runtime ubuntu.16.04-x64`

<span data-ttu-id="29a06-178">Générer le projet et utiliser la source de package NuGet spécifiée pendant l’opération de restauration (SDK .NET Core 2.0 et versions ultérieures) :</span><span class="sxs-lookup"><span data-stu-id="29a06-178">Build the project and use the specified NuGet package source during the restore operation (.NET Core SDK 2.0 and later versions):</span></span>

`dotnet build --source c:\packages\mypackages`