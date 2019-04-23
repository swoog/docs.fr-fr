---
title: Commande dotnet
description: Découvrez la commande dotnet (le pilote générique des outils .NET Core CLI) et comment l’utiliser.
ms.date: 06/04/2018
ms.openlocfilehash: 5278adf44d12e428cdeacf1d475377ce9155c314
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59613003"
---
# <a name="dotnet-command"></a><span data-ttu-id="ba624-103">Commande dotnet</span><span class="sxs-lookup"><span data-stu-id="ba624-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="ba624-104">Name</span><span class="sxs-lookup"><span data-stu-id="ba624-104">Name</span></span>

<span data-ttu-id="ba624-105">`dotnet` - Outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="ba624-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="ba624-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ba624-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ba624-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ba624-107">.NET Core 2.1</span></span>](#tab/netcore21)

```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ba624-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ba624-108">.NET Core 2.0</span></span>](#tab/netcore20)

```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ba624-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ba624-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```

---

## <a name="description"></a><span data-ttu-id="ba624-110">Description</span><span class="sxs-lookup"><span data-stu-id="ba624-110">Description</span></span>

<span data-ttu-id="ba624-111">`dotnet` est un outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="ba624-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="ba624-112">Il expose les commandes qui permettent d’effectuer des tâches spécifiques, par exemple [`dotnet build`](dotnet-build.md) et [`dotnet run`](dotnet-run.md).</span><span class="sxs-lookup"><span data-stu-id="ba624-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="ba624-113">Chaque commande définit ses propres arguments.</span><span class="sxs-lookup"><span data-stu-id="ba624-113">Each command defines its own arguments.</span></span> <span data-ttu-id="ba624-114">Tapez `--help` après chaque commande pour accéder à une brève documentation d’aide.</span><span class="sxs-lookup"><span data-stu-id="ba624-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="ba624-115">Vous pouvez utiliser `dotnet` pour exécuter des applications en spécifiant une DLL d’application, par exemple `dotnet myapp.dll`.</span><span class="sxs-lookup"><span data-stu-id="ba624-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="ba624-116">Pour plus d’informations sur les options de déploiement, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="ba624-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="ba624-117">Options</span><span class="sxs-lookup"><span data-stu-id="ba624-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ba624-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ba624-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="ba624-119">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ba624-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="ba624-120">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="ba624-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="ba624-121">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="ba624-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="ba624-122">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="ba624-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="ba624-123">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="ba624-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="ba624-124">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba624-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="ba624-125">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="ba624-126">Affiche les runtimes .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="ba624-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="ba624-127">Affiche les kits de développement logiciel .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="ba624-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx <N>`

<span data-ttu-id="ba624-128">Définit le comportement quand le framework partagé requis n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ba624-128">Defines behavior when the required shared framework is not available.</span></span> <span data-ttu-id="ba624-129">`N` peut être :</span><span class="sxs-lookup"><span data-stu-id="ba624-129">`N` can be:</span></span>
* <span data-ttu-id="ba624-130">`0` : désactiver l’extrapolation même pour les versions mineures.</span><span class="sxs-lookup"><span data-stu-id="ba624-130">`0` - Disable even minor version roll forward.</span></span>
* <span data-ttu-id="ba624-131">`1` : extrapoler la version mineure, mais pas la version majeure.</span><span class="sxs-lookup"><span data-stu-id="ba624-131">`1` - Roll forward on minor version, but not on major version.</span></span> <span data-ttu-id="ba624-132">Il s'agit du comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba624-132">This is the default behavior.</span></span>
* <span data-ttu-id="ba624-133">`2` : extrapoler les versions majeures et mineures.</span><span class="sxs-lookup"><span data-stu-id="ba624-133">`2` - Roll forward on minor and major versions.</span></span>

 <span data-ttu-id="ba624-134">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="ba624-134">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="ba624-135">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="ba624-135">Sets the verbosity level of the command.</span></span> <span data-ttu-id="ba624-136">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="ba624-136">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="ba624-137">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="ba624-137">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="ba624-138">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ba624-138">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ba624-139">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ba624-139">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="ba624-140">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ba624-140">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="ba624-141">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="ba624-141">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="ba624-142">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="ba624-142">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="ba624-143">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="ba624-143">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="ba624-144">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="ba624-144">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="ba624-145">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba624-145">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="ba624-146">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-146">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="ba624-147">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="ba624-147">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="ba624-148">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="ba624-148">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="ba624-149">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="ba624-149">Sets the verbosity level of the command.</span></span> <span data-ttu-id="ba624-150">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="ba624-150">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="ba624-151">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="ba624-151">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="ba624-152">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ba624-152">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ba624-153">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ba624-153">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="ba624-154">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="ba624-154">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="ba624-155">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="ba624-155">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="ba624-156">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="ba624-156">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="ba624-157">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="ba624-157">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="ba624-158">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="ba624-158">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="ba624-159">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-159">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="ba624-160">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="ba624-160">Sets the verbosity level of the command.</span></span> <span data-ttu-id="ba624-161">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="ba624-161">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="ba624-162">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="ba624-162">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="ba624-163">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ba624-163">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="ba624-164">Commandes dotnet</span><span class="sxs-lookup"><span data-stu-id="ba624-164">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="ba624-165">Général</span><span class="sxs-lookup"><span data-stu-id="ba624-165">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ba624-166">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ba624-166">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="ba624-167">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-167">Command</span></span>                                       | <span data-ttu-id="ba624-168">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-168">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="ba624-169">dotnet build</span><span class="sxs-lookup"><span data-stu-id="ba624-169">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="ba624-170">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-170">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="ba624-171">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="ba624-171">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="ba624-172">Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="ba624-172">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="ba624-173">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="ba624-173">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="ba624-174">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="ba624-174">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="ba624-175">dotnet help</span><span class="sxs-lookup"><span data-stu-id="ba624-175">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="ba624-176">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="ba624-176">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="ba624-177">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="ba624-177">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="ba624-178">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="ba624-178">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="ba624-179">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="ba624-179">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="ba624-180">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="ba624-180">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="ba624-181">dotnet new</span><span class="sxs-lookup"><span data-stu-id="ba624-181">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="ba624-182">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="ba624-182">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="ba624-183">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="ba624-183">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="ba624-184">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="ba624-184">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="ba624-185">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="ba624-185">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="ba624-186">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="ba624-186">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="ba624-187">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="ba624-187">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="ba624-188">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="ba624-188">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="ba624-189">dotnet run</span><span class="sxs-lookup"><span data-stu-id="ba624-189">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="ba624-190">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ba624-190">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="ba624-191">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="ba624-191">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="ba624-192">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="ba624-192">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="ba624-193">dotnet store</span><span class="sxs-lookup"><span data-stu-id="ba624-193">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="ba624-194">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="ba624-194">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="ba624-195">dotnet test</span><span class="sxs-lookup"><span data-stu-id="ba624-195">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="ba624-196">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="ba624-196">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ba624-197">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ba624-197">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="ba624-198">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-198">Command</span></span>                             | <span data-ttu-id="ba624-199">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-199">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="ba624-200">dotnet build</span><span class="sxs-lookup"><span data-stu-id="ba624-200">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="ba624-201">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-201">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="ba624-202">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="ba624-202">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="ba624-203">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="ba624-203">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="ba624-204">dotnet help</span><span class="sxs-lookup"><span data-stu-id="ba624-204">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="ba624-205">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="ba624-205">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="ba624-206">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="ba624-206">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="ba624-207">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="ba624-207">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="ba624-208">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="ba624-208">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="ba624-209">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="ba624-209">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="ba624-210">dotnet new</span><span class="sxs-lookup"><span data-stu-id="ba624-210">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="ba624-211">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="ba624-211">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="ba624-212">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="ba624-212">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="ba624-213">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="ba624-213">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="ba624-214">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="ba624-214">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="ba624-215">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="ba624-215">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="ba624-216">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="ba624-216">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="ba624-217">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="ba624-217">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="ba624-218">dotnet run</span><span class="sxs-lookup"><span data-stu-id="ba624-218">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="ba624-219">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ba624-219">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="ba624-220">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="ba624-220">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="ba624-221">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="ba624-221">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="ba624-222">dotnet store</span><span class="sxs-lookup"><span data-stu-id="ba624-222">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="ba624-223">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="ba624-223">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="ba624-224">dotnet test</span><span class="sxs-lookup"><span data-stu-id="ba624-224">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="ba624-225">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="ba624-225">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ba624-226">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ba624-226">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="ba624-227">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-227">Command</span></span>                             | <span data-ttu-id="ba624-228">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-228">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="ba624-229">dotnet build</span><span class="sxs-lookup"><span data-stu-id="ba624-229">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="ba624-230">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-230">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="ba624-231">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="ba624-231">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="ba624-232">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="ba624-232">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="ba624-233">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="ba624-233">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="ba624-234">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="ba624-234">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="ba624-235">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="ba624-235">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="ba624-236">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="ba624-236">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="ba624-237">dotnet new</span><span class="sxs-lookup"><span data-stu-id="ba624-237">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="ba624-238">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="ba624-238">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="ba624-239">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="ba624-239">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="ba624-240">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="ba624-240">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="ba624-241">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="ba624-241">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="ba624-242">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="ba624-242">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="ba624-243">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="ba624-243">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="ba624-244">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="ba624-244">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="ba624-245">dotnet run</span><span class="sxs-lookup"><span data-stu-id="ba624-245">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="ba624-246">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ba624-246">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="ba624-247">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="ba624-247">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="ba624-248">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="ba624-248">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="ba624-249">dotnet test</span><span class="sxs-lookup"><span data-stu-id="ba624-249">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="ba624-250">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="ba624-250">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="ba624-251">Références de projets</span><span class="sxs-lookup"><span data-stu-id="ba624-251">Project references</span></span>

<span data-ttu-id="ba624-252">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-252">Command</span></span> | <span data-ttu-id="ba624-253">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-253">Function</span></span>
--- | ---
[<span data-ttu-id="ba624-254">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="ba624-254">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="ba624-255">Ajoute une référence au projet.</span><span class="sxs-lookup"><span data-stu-id="ba624-255">Adds a project reference.</span></span>
[<span data-ttu-id="ba624-256">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="ba624-256">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="ba624-257">Liste les références du projet.</span><span class="sxs-lookup"><span data-stu-id="ba624-257">Lists project references.</span></span>
[<span data-ttu-id="ba624-258">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="ba624-258">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="ba624-259">Supprime une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="ba624-259">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="ba624-260">Packages NuGet</span><span class="sxs-lookup"><span data-stu-id="ba624-260">NuGet packages</span></span>

<span data-ttu-id="ba624-261">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-261">Command</span></span> | <span data-ttu-id="ba624-262">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-262">Function</span></span>
--- | ---
[<span data-ttu-id="ba624-263">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="ba624-263">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="ba624-264">Ajoute un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="ba624-264">Adds a NuGet package.</span></span>
[<span data-ttu-id="ba624-265">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="ba624-265">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="ba624-266">Supprime un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="ba624-266">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="ba624-267">Commandes NuGet</span><span class="sxs-lookup"><span data-stu-id="ba624-267">NuGet commands</span></span>

<span data-ttu-id="ba624-268">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-268">Command</span></span> | <span data-ttu-id="ba624-269">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-269">Function</span></span>
--- | ---
[<span data-ttu-id="ba624-270">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="ba624-270">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="ba624-271">Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="ba624-271">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="ba624-272">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="ba624-272">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="ba624-273">Efface ou liste les ressources NuGet locales telles que le cache de requête HTTP, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ba624-273">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="ba624-274">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="ba624-274">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="ba624-275">Effectue une transmission de type push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="ba624-275">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="ba624-276">Outils et commandes globaux</span><span class="sxs-lookup"><span data-stu-id="ba624-276">Global Tools commands</span></span>

<span data-ttu-id="ba624-277">Les [outils globaux .NET Core](global-tools.md) sont disponibles à partir de .NET Core SDK 2.1.300 :</span><span class="sxs-lookup"><span data-stu-id="ba624-277">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="ba624-278">Commande</span><span class="sxs-lookup"><span data-stu-id="ba624-278">Command</span></span> | <span data-ttu-id="ba624-279">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-279">Function</span></span>
--- | ---
[<span data-ttu-id="ba624-280">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="ba624-280">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="ba624-281">Installe un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ba624-281">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="ba624-282">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="ba624-282">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="ba624-283">Répertorie tous les outils globaux actuellement installés dans le répertoire par défaut de votre machine ou à l’emplacement du chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="ba624-283">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="ba624-284">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="ba624-284">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="ba624-285">Désinstalle un outil global de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ba624-285">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="ba624-286">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="ba624-286">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="ba624-287">Met à jour un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ba624-287">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="ba624-288">Outils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ba624-288">Additional tools</span></span>

<span data-ttu-id="ba624-289">À partir de .NET Core SDK 2.1.300, un certain nombre d’outils qui étaient disponibles uniquement par projet à l’aide de `DotnetCliToolReference` sont désormais disponibles dans le cadre du Kit de développement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-289">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="ba624-290">Ces outils sont répertoriés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="ba624-290">These tools are listed in the following table:</span></span>

| <span data-ttu-id="ba624-291">Outil</span><span class="sxs-lookup"><span data-stu-id="ba624-291">Tool</span></span>                                              | <span data-ttu-id="ba624-292">Fonction</span><span class="sxs-lookup"><span data-stu-id="ba624-292">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="ba624-293">dev-certs</span><span class="sxs-lookup"><span data-stu-id="ba624-293">dev-certs</span></span>                                         | <span data-ttu-id="ba624-294">Crée et gère les certificats de développement.</span><span class="sxs-lookup"><span data-stu-id="ba624-294">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="ba624-295">ef</span><span class="sxs-lookup"><span data-stu-id="ba624-295">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="ba624-296">Outils en ligne de commande Entity Framework Core.</span><span class="sxs-lookup"><span data-stu-id="ba624-296">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="ba624-297">sql-cache</span><span class="sxs-lookup"><span data-stu-id="ba624-297">sql-cache</span></span>                                         | <span data-ttu-id="ba624-298">Outils en ligne de commande du cache SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ba624-298">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="ba624-299">user-secrets</span><span class="sxs-lookup"><span data-stu-id="ba624-299">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="ba624-300">Gère les secrets de développement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba624-300">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="ba624-301">watch</span><span class="sxs-lookup"><span data-stu-id="ba624-301">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="ba624-302">Démarre un observateur de fichier qui exécute une commande à chaque modification de fichier.</span><span class="sxs-lookup"><span data-stu-id="ba624-302">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="ba624-303">Pour plus d’informations sur chaque outil, tapez `dotnet <tool-name> --help`.</span><span class="sxs-lookup"><span data-stu-id="ba624-303">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="ba624-304">Exemples</span><span class="sxs-lookup"><span data-stu-id="ba624-304">Examples</span></span>

<span data-ttu-id="ba624-305">Crée une application console .NET Core :</span><span class="sxs-lookup"><span data-stu-id="ba624-305">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="ba624-306">Restaurez les dépendances d’une application donnée :</span><span class="sxs-lookup"><span data-stu-id="ba624-306">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="ba624-307">Générez un projet et ses dépendances dans un répertoire donné :</span><span class="sxs-lookup"><span data-stu-id="ba624-307">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="ba624-308">Exécutez une DLL d’application, par exemple `myapp.dll` :</span><span class="sxs-lookup"><span data-stu-id="ba624-308">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="ba624-309">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="ba624-309">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ba624-310">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ba624-310">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="ba624-311">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="ba624-311">The primary package cache.</span></span> <span data-ttu-id="ba624-312">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="ba624-312">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="ba624-313">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba624-313">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="ba624-314">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ba624-314">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="ba624-315">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="ba624-315">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="ba624-316">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="ba624-316">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="ba624-317">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="ba624-317">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="ba624-318">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="ba624-318">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="ba624-319">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="ba624-319">If not set, it defaults to `true`.</span></span> <span data-ttu-id="ba624-320">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="ba624-320">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="ba624-321">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="ba624-321">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="ba624-322">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="ba624-322">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="ba624-323">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="ba624-323">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ba624-324">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ba624-324">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="ba624-325">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="ba624-325">The primary package cache.</span></span> <span data-ttu-id="ba624-326">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="ba624-326">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="ba624-327">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba624-327">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="ba624-328">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ba624-328">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="ba624-329">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="ba624-329">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="ba624-330">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="ba624-330">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="ba624-331">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="ba624-331">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="ba624-332">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="ba624-332">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="ba624-333">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="ba624-333">If not set, it defaults to `true`.</span></span> <span data-ttu-id="ba624-334">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="ba624-334">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="ba624-335">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="ba624-335">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ba624-336">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ba624-336">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="ba624-337">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="ba624-337">The primary package cache.</span></span> <span data-ttu-id="ba624-338">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="ba624-338">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="ba624-339">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ba624-339">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="ba624-340">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ba624-340">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="ba624-341">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="ba624-341">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="ba624-342">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="ba624-342">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="ba624-343">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="ba624-343">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
