---
title: Commande dotnet
description: Découvrez la commande dotnet (le pilote générique des outils .NET Core CLI) et comment l’utiliser.
ms.date: 06/04/2018
ms.openlocfilehash: 53eb96ee6fe809b2e6e42eec4e7e9b5f7c5edf2a
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55066439"
---
# <a name="dotnet-command"></a><span data-ttu-id="48f10-103">Commande dotnet</span><span class="sxs-lookup"><span data-stu-id="48f10-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="48f10-104">Name</span><span class="sxs-lookup"><span data-stu-id="48f10-104">Name</span></span>

<span data-ttu-id="48f10-105">`dotnet` - Outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="48f10-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="48f10-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="48f10-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="48f10-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="48f10-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="48f10-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="48f10-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="48f10-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="48f10-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="48f10-110">Description</span><span class="sxs-lookup"><span data-stu-id="48f10-110">Description</span></span>

<span data-ttu-id="48f10-111">`dotnet` est un outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="48f10-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="48f10-112">Il expose les commandes qui permettent d’effectuer des tâches spécifiques, par exemple [`dotnet build`](dotnet-build.md) et [`dotnet run`](dotnet-run.md).</span><span class="sxs-lookup"><span data-stu-id="48f10-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="48f10-113">Chaque commande définit ses propres arguments.</span><span class="sxs-lookup"><span data-stu-id="48f10-113">Each command defines its own arguments.</span></span> <span data-ttu-id="48f10-114">Tapez `--help` après chaque commande pour accéder à une brève documentation d’aide.</span><span class="sxs-lookup"><span data-stu-id="48f10-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="48f10-115">Vous pouvez utiliser `dotnet` pour exécuter des applications en spécifiant une DLL d’application, par exemple `dotnet myapp.dll`.</span><span class="sxs-lookup"><span data-stu-id="48f10-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="48f10-116">Pour plus d’informations sur les options de déploiement, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="48f10-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="48f10-117">Options</span><span class="sxs-lookup"><span data-stu-id="48f10-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="48f10-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="48f10-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="48f10-119">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="48f10-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="48f10-120">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="48f10-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="48f10-121">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="48f10-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="48f10-122">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="48f10-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="48f10-123">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="48f10-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="48f10-124">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="48f10-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="48f10-125">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="48f10-126">Affiche les runtimes .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="48f10-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="48f10-127">Affiche les kits de développement logiciel .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="48f10-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx <N>`

<span data-ttu-id="48f10-128">Définit le comportement quand le framework partagé requis n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="48f10-128">Defines behavior when the required shared framework is not available.</span></span> <span data-ttu-id="48f10-129">`N` peut être :</span><span class="sxs-lookup"><span data-stu-id="48f10-129">`N` can be:</span></span>
 * <span data-ttu-id="48f10-130">`0` : désactiver l’extrapolation même pour les versions mineures.</span><span class="sxs-lookup"><span data-stu-id="48f10-130">`0` - Disable even minor version roll forward.</span></span>
 * <span data-ttu-id="48f10-131">`1` : extrapoler la version mineure, mais pas la version majeure.</span><span class="sxs-lookup"><span data-stu-id="48f10-131">`1` - Roll forward on minor version, but not on major version.</span></span> <span data-ttu-id="48f10-132">Il s'agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="48f10-132">This is the default behavior.</span></span>
 * <span data-ttu-id="48f10-133">`2` : extrapoler les versions majeures et mineures.</span><span class="sxs-lookup"><span data-stu-id="48f10-133">`2` - Roll forward on minor and major versions.</span></span>

 <span data-ttu-id="48f10-134">Pour plus d'informations, consultez [Extrapolation](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="48f10-134">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="48f10-135">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="48f10-135">Sets the verbosity level of the command.</span></span> <span data-ttu-id="48f10-136">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="48f10-136">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="48f10-137">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="48f10-137">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="48f10-138">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="48f10-138">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="48f10-139">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="48f10-139">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="48f10-140">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="48f10-140">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="48f10-141">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="48f10-141">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="48f10-142">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="48f10-142">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="48f10-143">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="48f10-143">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="48f10-144">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="48f10-144">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="48f10-145">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="48f10-145">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="48f10-146">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-146">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="48f10-147">Désactive l’extrapolation de version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="48f10-147">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="48f10-148">Pour plus d'informations, consultez [Extrapolation](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="48f10-148">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="48f10-149">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="48f10-149">Sets the verbosity level of the command.</span></span> <span data-ttu-id="48f10-150">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="48f10-150">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="48f10-151">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="48f10-151">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="48f10-152">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="48f10-152">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="48f10-153">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="48f10-153">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="48f10-154">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="48f10-154">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="48f10-155">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="48f10-155">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="48f10-156">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="48f10-156">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="48f10-157">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="48f10-157">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="48f10-158">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="48f10-158">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="48f10-159">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-159">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="48f10-160">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="48f10-160">Sets the verbosity level of the command.</span></span> <span data-ttu-id="48f10-161">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="48f10-161">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="48f10-162">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="48f10-162">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="48f10-163">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="48f10-163">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="48f10-164">Commandes dotnet</span><span class="sxs-lookup"><span data-stu-id="48f10-164">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="48f10-165">Général</span><span class="sxs-lookup"><span data-stu-id="48f10-165">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="48f10-166">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="48f10-166">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="48f10-167">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-167">Command</span></span>                                       | <span data-ttu-id="48f10-168">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-168">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="48f10-169">dotnet build</span><span class="sxs-lookup"><span data-stu-id="48f10-169">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="48f10-170">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-170">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="48f10-171">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="48f10-171">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="48f10-172">Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="48f10-172">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="48f10-173">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="48f10-173">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="48f10-174">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="48f10-174">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="48f10-175">dotnet help</span><span class="sxs-lookup"><span data-stu-id="48f10-175">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="48f10-176">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="48f10-176">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="48f10-177">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="48f10-177">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="48f10-178">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="48f10-178">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="48f10-179">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="48f10-179">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="48f10-180">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="48f10-180">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="48f10-181">dotnet new</span><span class="sxs-lookup"><span data-stu-id="48f10-181">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="48f10-182">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="48f10-182">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="48f10-183">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="48f10-183">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="48f10-184">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="48f10-184">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="48f10-185">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="48f10-185">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="48f10-186">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="48f10-186">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="48f10-187">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="48f10-187">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="48f10-188">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="48f10-188">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="48f10-189">dotnet run</span><span class="sxs-lookup"><span data-stu-id="48f10-189">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="48f10-190">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="48f10-190">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="48f10-191">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="48f10-191">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="48f10-192">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="48f10-192">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="48f10-193">dotnet store</span><span class="sxs-lookup"><span data-stu-id="48f10-193">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="48f10-194">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="48f10-194">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="48f10-195">dotnet test</span><span class="sxs-lookup"><span data-stu-id="48f10-195">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="48f10-196">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="48f10-196">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="48f10-197">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="48f10-197">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="48f10-198">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-198">Command</span></span>                             | <span data-ttu-id="48f10-199">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-199">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="48f10-200">dotnet build</span><span class="sxs-lookup"><span data-stu-id="48f10-200">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="48f10-201">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-201">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="48f10-202">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="48f10-202">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="48f10-203">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="48f10-203">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="48f10-204">dotnet help</span><span class="sxs-lookup"><span data-stu-id="48f10-204">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="48f10-205">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="48f10-205">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="48f10-206">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="48f10-206">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="48f10-207">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="48f10-207">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="48f10-208">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="48f10-208">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="48f10-209">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="48f10-209">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="48f10-210">dotnet new</span><span class="sxs-lookup"><span data-stu-id="48f10-210">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="48f10-211">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="48f10-211">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="48f10-212">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="48f10-212">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="48f10-213">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="48f10-213">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="48f10-214">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="48f10-214">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="48f10-215">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="48f10-215">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="48f10-216">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="48f10-216">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="48f10-217">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="48f10-217">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="48f10-218">dotnet run</span><span class="sxs-lookup"><span data-stu-id="48f10-218">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="48f10-219">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="48f10-219">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="48f10-220">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="48f10-220">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="48f10-221">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="48f10-221">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="48f10-222">dotnet store</span><span class="sxs-lookup"><span data-stu-id="48f10-222">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="48f10-223">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="48f10-223">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="48f10-224">dotnet test</span><span class="sxs-lookup"><span data-stu-id="48f10-224">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="48f10-225">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="48f10-225">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="48f10-226">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="48f10-226">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="48f10-227">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-227">Command</span></span>                             | <span data-ttu-id="48f10-228">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-228">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="48f10-229">dotnet build</span><span class="sxs-lookup"><span data-stu-id="48f10-229">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="48f10-230">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-230">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="48f10-231">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="48f10-231">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="48f10-232">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="48f10-232">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="48f10-233">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="48f10-233">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="48f10-234">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="48f10-234">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="48f10-235">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="48f10-235">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="48f10-236">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="48f10-236">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="48f10-237">dotnet new</span><span class="sxs-lookup"><span data-stu-id="48f10-237">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="48f10-238">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="48f10-238">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="48f10-239">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="48f10-239">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="48f10-240">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="48f10-240">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="48f10-241">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="48f10-241">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="48f10-242">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="48f10-242">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="48f10-243">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="48f10-243">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="48f10-244">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="48f10-244">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="48f10-245">dotnet run</span><span class="sxs-lookup"><span data-stu-id="48f10-245">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="48f10-246">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="48f10-246">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="48f10-247">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="48f10-247">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="48f10-248">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="48f10-248">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="48f10-249">dotnet test</span><span class="sxs-lookup"><span data-stu-id="48f10-249">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="48f10-250">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="48f10-250">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="48f10-251">Références de projets</span><span class="sxs-lookup"><span data-stu-id="48f10-251">Project references</span></span>

<span data-ttu-id="48f10-252">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-252">Command</span></span> | <span data-ttu-id="48f10-253">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-253">Function</span></span>
--- | ---
[<span data-ttu-id="48f10-254">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="48f10-254">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="48f10-255">Ajoute une référence au projet.</span><span class="sxs-lookup"><span data-stu-id="48f10-255">Adds a project reference.</span></span>
[<span data-ttu-id="48f10-256">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="48f10-256">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="48f10-257">Liste les références du projet.</span><span class="sxs-lookup"><span data-stu-id="48f10-257">Lists project references.</span></span>
[<span data-ttu-id="48f10-258">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="48f10-258">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="48f10-259">Supprime une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="48f10-259">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="48f10-260">Packages NuGet</span><span class="sxs-lookup"><span data-stu-id="48f10-260">NuGet packages</span></span>

<span data-ttu-id="48f10-261">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-261">Command</span></span> | <span data-ttu-id="48f10-262">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-262">Function</span></span>
--- | ---
[<span data-ttu-id="48f10-263">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="48f10-263">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="48f10-264">Ajoute un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="48f10-264">Adds a NuGet package.</span></span>
[<span data-ttu-id="48f10-265">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="48f10-265">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="48f10-266">Supprime un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="48f10-266">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="48f10-267">Commandes NuGet</span><span class="sxs-lookup"><span data-stu-id="48f10-267">NuGet commands</span></span>

<span data-ttu-id="48f10-268">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-268">Command</span></span> | <span data-ttu-id="48f10-269">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-269">Function</span></span>
--- | ---
[<span data-ttu-id="48f10-270">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="48f10-270">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="48f10-271">Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="48f10-271">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="48f10-272">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="48f10-272">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="48f10-273">Efface ou liste les ressources NuGet locales telles que le cache de requête HTTP, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="48f10-273">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="48f10-274">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="48f10-274">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="48f10-275">Effectue une transmission de type push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="48f10-275">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="48f10-276">Outils et commandes globaux</span><span class="sxs-lookup"><span data-stu-id="48f10-276">Global Tools commands</span></span>

<span data-ttu-id="48f10-277">Les [outils globaux .NET Core](global-tools.md) sont disponibles à partir de .NET Core SDK 2.1.300 :</span><span class="sxs-lookup"><span data-stu-id="48f10-277">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="48f10-278">Commande</span><span class="sxs-lookup"><span data-stu-id="48f10-278">Command</span></span> | <span data-ttu-id="48f10-279">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-279">Function</span></span>
--- | ---
[<span data-ttu-id="48f10-280">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="48f10-280">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="48f10-281">Installe un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="48f10-281">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="48f10-282">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="48f10-282">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="48f10-283">Répertorie tous les outils globaux actuellement installés dans le répertoire par défaut de votre machine ou à l’emplacement du chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="48f10-283">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="48f10-284">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="48f10-284">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="48f10-285">Désinstalle un outil global de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="48f10-285">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="48f10-286">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="48f10-286">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="48f10-287">Met à jour un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="48f10-287">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="48f10-288">Outils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="48f10-288">Additional tools</span></span>

<span data-ttu-id="48f10-289">À partir de .NET Core SDK 2.1.300, un certain nombre d’outils qui étaient disponibles uniquement par projet à l’aide de `DotnetCliToolReference` sont désormais disponibles dans le cadre du Kit de développement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-289">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="48f10-290">Ces outils sont répertoriés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="48f10-290">These tools are listed in the following table:</span></span>

| <span data-ttu-id="48f10-291">Outil</span><span class="sxs-lookup"><span data-stu-id="48f10-291">Tool</span></span>                                              | <span data-ttu-id="48f10-292">Fonction</span><span class="sxs-lookup"><span data-stu-id="48f10-292">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="48f10-293">dev-certs</span><span class="sxs-lookup"><span data-stu-id="48f10-293">dev-certs</span></span>                                         | <span data-ttu-id="48f10-294">Crée et gère les certificats de développement.</span><span class="sxs-lookup"><span data-stu-id="48f10-294">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="48f10-295">ef</span><span class="sxs-lookup"><span data-stu-id="48f10-295">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="48f10-296">Outils en ligne de commande Entity Framework Core.</span><span class="sxs-lookup"><span data-stu-id="48f10-296">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="48f10-297">sql-cache</span><span class="sxs-lookup"><span data-stu-id="48f10-297">sql-cache</span></span>                                         | <span data-ttu-id="48f10-298">Outils en ligne de commande du cache SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48f10-298">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="48f10-299">user-secrets</span><span class="sxs-lookup"><span data-stu-id="48f10-299">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="48f10-300">Gère les secrets de développement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48f10-300">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="48f10-301">watch</span><span class="sxs-lookup"><span data-stu-id="48f10-301">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="48f10-302">Démarre un observateur de fichier qui exécute une commande à chaque modification de fichier.</span><span class="sxs-lookup"><span data-stu-id="48f10-302">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="48f10-303">Pour plus d’informations sur chaque outil, tapez `dotnet <tool-name> --help`.</span><span class="sxs-lookup"><span data-stu-id="48f10-303">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="48f10-304">Exemples</span><span class="sxs-lookup"><span data-stu-id="48f10-304">Examples</span></span>

<span data-ttu-id="48f10-305">Crée une application console .NET Core :</span><span class="sxs-lookup"><span data-stu-id="48f10-305">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="48f10-306">Restaurez les dépendances d’une application donnée :</span><span class="sxs-lookup"><span data-stu-id="48f10-306">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="48f10-307">Générez un projet et ses dépendances dans un répertoire donné :</span><span class="sxs-lookup"><span data-stu-id="48f10-307">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="48f10-308">Exécutez une DLL d’application, par exemple `myapp.dll` :</span><span class="sxs-lookup"><span data-stu-id="48f10-308">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="48f10-309">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="48f10-309">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="48f10-310">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="48f10-310">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="48f10-311">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="48f10-311">The primary package cache.</span></span> <span data-ttu-id="48f10-312">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="48f10-312">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="48f10-313">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="48f10-313">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="48f10-314">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48f10-314">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="48f10-315">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="48f10-315">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="48f10-316">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="48f10-316">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="48f10-317">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="48f10-317">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="48f10-318">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="48f10-318">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="48f10-319">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="48f10-319">If not set, it defaults to `true`.</span></span> <span data-ttu-id="48f10-320">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="48f10-320">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="48f10-321">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="48f10-321">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="48f10-322">Désactive l’extrapolation de version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="48f10-322">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="48f10-323">Pour plus d'informations, consultez [Extrapolation](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="48f10-323">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="48f10-324">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="48f10-324">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="48f10-325">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="48f10-325">The primary package cache.</span></span> <span data-ttu-id="48f10-326">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="48f10-326">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="48f10-327">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="48f10-327">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="48f10-328">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48f10-328">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="48f10-329">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="48f10-329">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="48f10-330">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="48f10-330">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="48f10-331">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="48f10-331">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="48f10-332">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="48f10-332">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="48f10-333">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="48f10-333">If not set, it defaults to `true`.</span></span> <span data-ttu-id="48f10-334">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="48f10-334">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="48f10-335">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="48f10-335">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="48f10-336">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="48f10-336">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="48f10-337">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="48f10-337">The primary package cache.</span></span> <span data-ttu-id="48f10-338">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="48f10-338">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="48f10-339">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="48f10-339">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="48f10-340">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48f10-340">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="48f10-341">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="48f10-341">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="48f10-342">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="48f10-342">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="48f10-343">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="48f10-343">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
