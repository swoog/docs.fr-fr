---
title: Commande dotnet - Interface CLI .NET Core
description: Découvrez la commande dotnet (le pilote générique des outils .NET Core CLI) et comment l’utiliser.
author: mairaw
ms.author: mairaw
ms.date: 03/20/2018
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: 2d22124cb613152df402046541650f3262e7e202
ms.sourcegitcommit: 6f967c86dde55472440f0c8669b0e910ee3c53ba
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2018
---
# <a name="dotnet-command"></a><span data-ttu-id="7e466-103">Commande dotnet</span><span class="sxs-lookup"><span data-stu-id="7e466-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="7e466-104">Name</span><span class="sxs-lookup"><span data-stu-id="7e466-104">Name</span></span>

<span data-ttu-id="7e466-105">`dotnet` - Pilote général pour l’exécution des commandes de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-105">`dotnet` - General driver for running the command-line commands.</span></span>

## <a name="synopsis"></a><span data-ttu-id="7e466-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7e466-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="7e466-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="7e466-107">.NET Core 2.x</span></span>](#tab/netcore2x)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e466-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e466-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="7e466-109">Description</span><span class="sxs-lookup"><span data-stu-id="7e466-109">Description</span></span>

<span data-ttu-id="7e466-110">`dotnet` est un pilote générique pour la chaîne d’outils de l’interface de ligne de commande (CLI).</span><span class="sxs-lookup"><span data-stu-id="7e466-110">`dotnet` is a generic driver for the Command Line Interface (CLI) toolchain.</span></span> <span data-ttu-id="7e466-111">Appelé seul, il fournit des instructions d’utilisation succinctes.</span><span class="sxs-lookup"><span data-stu-id="7e466-111">Invoked on its own, it provides brief usage instructions.</span></span>

<span data-ttu-id="7e466-112">Chaque fonctionnalité est implémentée comme une commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-112">Each specific feature is implemented as a command.</span></span> <span data-ttu-id="7e466-113">Pour utiliser la fonctionnalité, la commande est spécifiée après `dotnet`, comme dans [`dotnet build`](dotnet-build.md).</span><span class="sxs-lookup"><span data-stu-id="7e466-113">In order to use the feature, the command is specified after `dotnet`, such as [`dotnet build`](dotnet-build.md).</span></span> <span data-ttu-id="7e466-114">Tous les arguments qui suivent la commande sont ses arguments propres.</span><span class="sxs-lookup"><span data-stu-id="7e466-114">All of the arguments following the command are its own arguments.</span></span>

<span data-ttu-id="7e466-115">Le seul cas où la commande `dotnet` est utilisée seule est l’exécution d’applications [dépendantes du framework](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="7e466-115">The only time `dotnet` is used as a command on its own is to run [framework-dependent apps](../deploying/index.md).</span></span> <span data-ttu-id="7e466-116">Spécifiez une DLL d’application après le verbe `dotnet` pour exécuter l’application (par exemple, `dotnet myapp.dll`).</span><span class="sxs-lookup"><span data-stu-id="7e466-116">Specify an application DLL after the `dotnet` verb to execute the application (for example, `dotnet myapp.dll`).</span></span>

## <a name="options"></a><span data-ttu-id="7e466-117">Options</span><span class="sxs-lookup"><span data-stu-id="7e466-117">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="7e466-118">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="7e466-118">.NET Core 2.x</span></span>](#tab/netcore2x)

`--additional-deps <PATH>`

<span data-ttu-id="7e466-119">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="7e466-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="7e466-120">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="7e466-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="7e466-121">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="7e466-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="7e466-122">Version du runtime .NET Core installé à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="7e466-122">Version of the installed .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="7e466-123">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-123">Prints out a short help for the command.</span></span> <span data-ttu-id="7e466-124">Si vous l’utilisez avec `dotnet`, elle affiche également la liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="7e466-124">If using with `dotnet`, it also prints a list of the available commands.</span></span>

`--info`

<span data-ttu-id="7e466-125">Affiche des informations détaillées sur l’environnement et les outils CLI, telles que le système d’exploitation actuel, le SHA de validation de la version, etc.</span><span class="sxs-lookup"><span data-stu-id="7e466-125">Prints out detailed information about the CLI tooling and the environment, such as the current operating system, commit SHA for the version, and other information.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="7e466-126">Effectue une restauration par progression en l’absence de framework candidat partagé.</span><span class="sxs-lookup"><span data-stu-id="7e466-126">Rolls forward on no candidate shared framework.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="7e466-127">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-127">Sets the verbosity level of the command.</span></span> <span data-ttu-id="7e466-128">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="7e466-128">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="7e466-129">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="7e466-129">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="7e466-130">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7e466-130">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e466-131">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e466-131">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="7e466-132">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="7e466-132">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="7e466-133">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="7e466-133">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="7e466-134">Version du runtime .NET Core installé à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="7e466-134">Version of the installed .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="7e466-135">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-135">Prints out a short help for the command.</span></span> <span data-ttu-id="7e466-136">Si vous l’utilisez avec `dotnet`, elle affiche également la liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="7e466-136">If using with `dotnet`, it also prints a list of the available commands.</span></span>

`--info`

<span data-ttu-id="7e466-137">Affiche des informations détaillées sur l’environnement et les outils CLI, telles que le système d’exploitation actuel, le SHA de validation de la version, etc.</span><span class="sxs-lookup"><span data-stu-id="7e466-137">Prints out detailed information about the CLI tooling and the environment, such as the current operating system, commit SHA for the version, and other information.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="7e466-138">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-138">Sets the verbosity level of the command.</span></span> <span data-ttu-id="7e466-139">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="7e466-139">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="7e466-140">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="7e466-140">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="7e466-141">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="7e466-141">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="7e466-142">Commandes dotnet</span><span class="sxs-lookup"><span data-stu-id="7e466-142">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="7e466-143">Général</span><span class="sxs-lookup"><span data-stu-id="7e466-143">General</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="7e466-144">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="7e466-144">.NET Core 2.x</span></span>](#tab/netcore2x)

| <span data-ttu-id="7e466-145">Commande</span><span class="sxs-lookup"><span data-stu-id="7e466-145">Command</span></span>                             | <span data-ttu-id="7e466-146">Fonction</span><span class="sxs-lookup"><span data-stu-id="7e466-146">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="7e466-147">dotnet build</span><span class="sxs-lookup"><span data-stu-id="7e466-147">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="7e466-148">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7e466-148">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="7e466-149">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="7e466-149">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="7e466-150">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="7e466-150">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="7e466-151">dotnet help</span><span class="sxs-lookup"><span data-stu-id="7e466-151">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="7e466-152">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="7e466-152">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="7e466-153">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="7e466-153">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="7e466-154">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="7e466-154">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="7e466-155">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="7e466-155">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="7e466-156">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="7e466-156">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="7e466-157">dotnet new</span><span class="sxs-lookup"><span data-stu-id="7e466-157">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="7e466-158">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="7e466-158">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="7e466-159">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="7e466-159">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="7e466-160">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="7e466-160">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="7e466-161">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="7e466-161">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="7e466-162">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="7e466-162">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="7e466-163">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="7e466-163">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="7e466-164">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="7e466-164">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="7e466-165">dotnet run</span><span class="sxs-lookup"><span data-stu-id="7e466-165">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="7e466-166">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="7e466-166">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="7e466-167">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="7e466-167">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="7e466-168">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="7e466-168">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="7e466-169">dotnet store</span><span class="sxs-lookup"><span data-stu-id="7e466-169">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="7e466-170">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="7e466-170">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="7e466-171">dotnet test</span><span class="sxs-lookup"><span data-stu-id="7e466-171">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="7e466-172">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="7e466-172">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e466-173">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e466-173">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="7e466-174">Commande</span><span class="sxs-lookup"><span data-stu-id="7e466-174">Command</span></span>                             | <span data-ttu-id="7e466-175">Fonction</span><span class="sxs-lookup"><span data-stu-id="7e466-175">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="7e466-176">dotnet build</span><span class="sxs-lookup"><span data-stu-id="7e466-176">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="7e466-177">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7e466-177">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="7e466-178">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="7e466-178">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="7e466-179">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="7e466-179">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="7e466-180">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="7e466-180">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="7e466-181">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="7e466-181">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="7e466-182">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="7e466-182">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="7e466-183">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="7e466-183">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="7e466-184">dotnet new</span><span class="sxs-lookup"><span data-stu-id="7e466-184">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="7e466-185">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="7e466-185">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="7e466-186">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="7e466-186">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="7e466-187">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="7e466-187">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="7e466-188">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="7e466-188">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="7e466-189">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="7e466-189">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="7e466-190">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="7e466-190">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="7e466-191">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="7e466-191">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="7e466-192">dotnet run</span><span class="sxs-lookup"><span data-stu-id="7e466-192">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="7e466-193">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="7e466-193">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="7e466-194">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="7e466-194">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="7e466-195">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="7e466-195">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="7e466-196">dotnet test</span><span class="sxs-lookup"><span data-stu-id="7e466-196">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="7e466-197">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="7e466-197">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="7e466-198">Références de projets</span><span class="sxs-lookup"><span data-stu-id="7e466-198">Project references</span></span>

<span data-ttu-id="7e466-199">Commande</span><span class="sxs-lookup"><span data-stu-id="7e466-199">Command</span></span> | <span data-ttu-id="7e466-200">Fonction</span><span class="sxs-lookup"><span data-stu-id="7e466-200">Function</span></span>
--- | ---
[<span data-ttu-id="7e466-201">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="7e466-201">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="7e466-202">Ajoute une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="7e466-202">Add a project reference.</span></span>
[<span data-ttu-id="7e466-203">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="7e466-203">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="7e466-204">Liste les références du projet.</span><span class="sxs-lookup"><span data-stu-id="7e466-204">List project references.</span></span>
[<span data-ttu-id="7e466-205">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="7e466-205">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="7e466-206">Supprime une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="7e466-206">Remove a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="7e466-207">Packages NuGet</span><span class="sxs-lookup"><span data-stu-id="7e466-207">NuGet packages</span></span>

<span data-ttu-id="7e466-208">Commande</span><span class="sxs-lookup"><span data-stu-id="7e466-208">Command</span></span> | <span data-ttu-id="7e466-209">Fonction</span><span class="sxs-lookup"><span data-stu-id="7e466-209">Function</span></span>
--- | ---
[<span data-ttu-id="7e466-210">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="7e466-210">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="7e466-211">Ajoute un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="7e466-211">Add a NuGet package.</span></span>
[<span data-ttu-id="7e466-212">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="7e466-212">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="7e466-213">Supprime un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="7e466-213">Remove a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="7e466-214">Commandes NuGet</span><span class="sxs-lookup"><span data-stu-id="7e466-214">NuGet commands</span></span>

<span data-ttu-id="7e466-215">Commande</span><span class="sxs-lookup"><span data-stu-id="7e466-215">Command</span></span> | <span data-ttu-id="7e466-216">Fonction</span><span class="sxs-lookup"><span data-stu-id="7e466-216">Function</span></span>
--- | ---
[<span data-ttu-id="7e466-217">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="7e466-217">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="7e466-218">Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="7e466-218">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="7e466-219">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="7e466-219">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="7e466-220">Efface ou liste les ressources NuGet locales telles que le cache de requête HTTP, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7e466-220">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="7e466-221">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="7e466-221">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="7e466-222">Effectue une transmission de type push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="7e466-222">Pushes a package to the server and publishes it.</span></span>

## <a name="examples"></a><span data-ttu-id="7e466-223">Exemples</span><span class="sxs-lookup"><span data-stu-id="7e466-223">Examples</span></span>

<span data-ttu-id="7e466-224">Initialisez un exemple d’application console .NET Core qui peut être compilé et exécuté :</span><span class="sxs-lookup"><span data-stu-id="7e466-224">Initialize a sample .NET Core console application that can be compiled and run:</span></span>

`dotnet new console`

<span data-ttu-id="7e466-225">Restaurez les dépendances d’une application donnée :</span><span class="sxs-lookup"><span data-stu-id="7e466-225">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="7e466-226">Générez un projet et ses dépendances dans un répertoire donné :</span><span class="sxs-lookup"><span data-stu-id="7e466-226">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="7e466-227">Exécuter une application dépendante du framework nommée `myapp.dll` :</span><span class="sxs-lookup"><span data-stu-id="7e466-227">Run a framework-dependent app named `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="7e466-228">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="7e466-228">Environment variables</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="7e466-229">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="7e466-229">.NET Core 2.x</span></span>](#tab/netcore2x)

`DOTNET_PACKAGES`

<span data-ttu-id="7e466-230">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="7e466-230">The primary package cache.</span></span> <span data-ttu-id="7e466-231">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="7e466-231">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="7e466-232">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7e466-232">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="7e466-233">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7e466-233">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="7e466-234">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `1`, `yes` ou `false`) ; définie sur `true` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="7e466-234">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted); otherwise, set to `false` to opt-in to the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="7e466-235">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="7e466-235">If not set, the defaults is `false`, and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="7e466-236">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="7e466-236">Specifies whether .NET Core runtime, shared framework or SDK are resolved from the global location.</span></span> <span data-ttu-id="7e466-237">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="7e466-237">If not set, it defaults to `true`.</span></span> <span data-ttu-id="7e466-238">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="7e466-238">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="7e466-239">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="7e466-239">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="7e466-240">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="7e466-240">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="7e466-241">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="7e466-241">The primary package cache.</span></span> <span data-ttu-id="7e466-242">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="7e466-242">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="7e466-243">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="7e466-243">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="7e466-244">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7e466-244">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="7e466-245">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `1`, `yes` ou `false`) ; définie sur `true` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="7e466-245">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted); otherwise, set to `false` to opt-in to the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="7e466-246">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="7e466-246">If not set, the defaults is `false`, and the telemetry feature is active.</span></span>

---
