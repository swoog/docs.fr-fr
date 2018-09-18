---
title: Commande dotnet - Interface CLI .NET Core
description: Découvrez la commande dotnet (le pilote générique des outils .NET Core CLI) et comment l’utiliser.
author: mairaw
ms.author: mairaw
ms.date: 06/04/2018
ms.openlocfilehash: 53e8f8bab1cbaabaa7926aa68197c18843b0b637
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45615571"
---
# <a name="dotnet-command"></a><span data-ttu-id="bcdb5-103">Commande dotnet</span><span class="sxs-lookup"><span data-stu-id="bcdb5-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="bcdb5-104">Name</span><span class="sxs-lookup"><span data-stu-id="bcdb5-104">Name</span></span>

<span data-ttu-id="bcdb5-105">`dotnet` - Outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="bcdb5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bcdb5-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bcdb5-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bcdb5-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bcdb5-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bcdb5-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bcdb5-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bcdb5-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="bcdb5-110">Description</span><span class="sxs-lookup"><span data-stu-id="bcdb5-110">Description</span></span>

<span data-ttu-id="bcdb5-111">`dotnet` est un outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="bcdb5-112">Il expose les commandes qui permettent d’effectuer des tâches spécifiques, par exemple [`dotnet build`](dotnet-build.md) et [`dotnet run`](dotnet-run.md).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="bcdb5-113">Chaque commande définit ses propres arguments.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-113">Each command defines its own arguments.</span></span> <span data-ttu-id="bcdb5-114">Tapez `--help` après chaque commande pour accéder à une brève documentation d’aide.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="bcdb5-115">Vous pouvez utiliser `dotnet` pour exécuter des applications en spécifiant une DLL d’application, par exemple `dotnet myapp.dll`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="bcdb5-116">Pour plus d’informations sur les options de déploiement, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="bcdb5-117">Options</span><span class="sxs-lookup"><span data-stu-id="bcdb5-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bcdb5-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bcdb5-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="bcdb5-119">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="bcdb5-120">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="bcdb5-121">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="bcdb5-122">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="bcdb5-123">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="bcdb5-124">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="bcdb5-125">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="bcdb5-126">Affiche les runtimes .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="bcdb5-127">Affiche les kits de développement logiciel .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="bcdb5-128">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-128">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="bcdb5-129">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-129">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="bcdb5-130">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-130">Sets the verbosity level of the command.</span></span> <span data-ttu-id="bcdb5-131">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-131">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="bcdb5-132">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-132">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="bcdb5-133">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-133">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bcdb5-134">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bcdb5-134">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="bcdb5-135">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-135">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="bcdb5-136">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-136">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="bcdb5-137">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-137">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="bcdb5-138">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-138">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="bcdb5-139">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-139">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="bcdb5-140">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-140">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="bcdb5-141">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-141">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="bcdb5-142">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-142">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="bcdb5-143">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-143">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="bcdb5-144">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="bcdb5-145">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="bcdb5-146">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-146">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="bcdb5-147">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-147">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bcdb5-148">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bcdb5-148">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="bcdb5-149">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-149">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="bcdb5-150">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-150">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="bcdb5-151">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-151">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="bcdb5-152">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-152">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="bcdb5-153">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-153">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="bcdb5-154">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-154">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="bcdb5-155">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-155">Sets the verbosity level of the command.</span></span> <span data-ttu-id="bcdb5-156">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-156">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="bcdb5-157">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-157">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="bcdb5-158">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-158">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="bcdb5-159">Commandes dotnet</span><span class="sxs-lookup"><span data-stu-id="bcdb5-159">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="bcdb5-160">Général</span><span class="sxs-lookup"><span data-stu-id="bcdb5-160">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bcdb5-161">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bcdb5-161">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="bcdb5-162">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-162">Command</span></span>                                       | <span data-ttu-id="bcdb5-163">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-163">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="bcdb5-164">dotnet build</span><span class="sxs-lookup"><span data-stu-id="bcdb5-164">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="bcdb5-165">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-165">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="bcdb5-166">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="bcdb5-166">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="bcdb5-167">Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-167">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="bcdb5-168">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="bcdb5-168">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="bcdb5-169">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-169">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="bcdb5-170">dotnet help</span><span class="sxs-lookup"><span data-stu-id="bcdb5-170">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="bcdb5-171">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-171">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="bcdb5-172">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="bcdb5-172">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="bcdb5-173">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-173">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="bcdb5-174">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="bcdb5-174">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="bcdb5-175">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-175">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="bcdb5-176">dotnet new</span><span class="sxs-lookup"><span data-stu-id="bcdb5-176">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="bcdb5-177">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-177">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="bcdb5-178">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="bcdb5-178">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="bcdb5-179">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-179">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="bcdb5-180">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="bcdb5-180">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="bcdb5-181">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-181">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="bcdb5-182">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="bcdb5-182">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="bcdb5-183">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-183">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="bcdb5-184">dotnet run</span><span class="sxs-lookup"><span data-stu-id="bcdb5-184">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="bcdb5-185">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-185">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="bcdb5-186">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="bcdb5-186">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="bcdb5-187">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-187">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="bcdb5-188">dotnet store</span><span class="sxs-lookup"><span data-stu-id="bcdb5-188">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="bcdb5-189">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-189">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="bcdb5-190">dotnet test</span><span class="sxs-lookup"><span data-stu-id="bcdb5-190">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="bcdb5-191">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-191">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bcdb5-192">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bcdb5-192">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="bcdb5-193">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-193">Command</span></span>                             | <span data-ttu-id="bcdb5-194">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-194">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="bcdb5-195">dotnet build</span><span class="sxs-lookup"><span data-stu-id="bcdb5-195">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="bcdb5-196">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-196">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="bcdb5-197">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="bcdb5-197">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="bcdb5-198">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-198">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="bcdb5-199">dotnet help</span><span class="sxs-lookup"><span data-stu-id="bcdb5-199">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="bcdb5-200">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-200">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="bcdb5-201">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="bcdb5-201">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="bcdb5-202">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-202">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="bcdb5-203">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="bcdb5-203">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="bcdb5-204">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-204">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="bcdb5-205">dotnet new</span><span class="sxs-lookup"><span data-stu-id="bcdb5-205">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="bcdb5-206">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-206">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="bcdb5-207">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="bcdb5-207">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="bcdb5-208">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-208">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="bcdb5-209">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="bcdb5-209">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="bcdb5-210">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-210">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="bcdb5-211">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="bcdb5-211">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="bcdb5-212">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-212">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="bcdb5-213">dotnet run</span><span class="sxs-lookup"><span data-stu-id="bcdb5-213">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="bcdb5-214">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-214">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="bcdb5-215">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="bcdb5-215">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="bcdb5-216">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-216">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="bcdb5-217">dotnet store</span><span class="sxs-lookup"><span data-stu-id="bcdb5-217">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="bcdb5-218">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-218">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="bcdb5-219">dotnet test</span><span class="sxs-lookup"><span data-stu-id="bcdb5-219">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="bcdb5-220">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-220">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bcdb5-221">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bcdb5-221">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="bcdb5-222">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-222">Command</span></span>                             | <span data-ttu-id="bcdb5-223">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-223">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="bcdb5-224">dotnet build</span><span class="sxs-lookup"><span data-stu-id="bcdb5-224">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="bcdb5-225">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-225">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="bcdb5-226">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="bcdb5-226">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="bcdb5-227">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-227">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="bcdb5-228">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="bcdb5-228">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="bcdb5-229">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-229">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="bcdb5-230">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="bcdb5-230">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="bcdb5-231">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-231">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="bcdb5-232">dotnet new</span><span class="sxs-lookup"><span data-stu-id="bcdb5-232">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="bcdb5-233">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-233">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="bcdb5-234">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="bcdb5-234">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="bcdb5-235">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-235">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="bcdb5-236">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="bcdb5-236">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="bcdb5-237">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-237">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="bcdb5-238">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="bcdb5-238">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="bcdb5-239">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-239">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="bcdb5-240">dotnet run</span><span class="sxs-lookup"><span data-stu-id="bcdb5-240">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="bcdb5-241">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-241">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="bcdb5-242">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="bcdb5-242">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="bcdb5-243">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-243">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="bcdb5-244">dotnet test</span><span class="sxs-lookup"><span data-stu-id="bcdb5-244">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="bcdb5-245">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-245">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="bcdb5-246">Références de projets</span><span class="sxs-lookup"><span data-stu-id="bcdb5-246">Project references</span></span>

<span data-ttu-id="bcdb5-247">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-247">Command</span></span> | <span data-ttu-id="bcdb5-248">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-248">Function</span></span>
--- | ---
[<span data-ttu-id="bcdb5-249">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="bcdb5-249">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="bcdb5-250">Ajoute une référence au projet.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-250">Adds a project reference.</span></span>
[<span data-ttu-id="bcdb5-251">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="bcdb5-251">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="bcdb5-252">Liste les références du projet.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-252">Lists project references.</span></span>
[<span data-ttu-id="bcdb5-253">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="bcdb5-253">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="bcdb5-254">Supprime une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-254">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="bcdb5-255">Packages NuGet</span><span class="sxs-lookup"><span data-stu-id="bcdb5-255">NuGet packages</span></span>

<span data-ttu-id="bcdb5-256">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-256">Command</span></span> | <span data-ttu-id="bcdb5-257">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-257">Function</span></span>
--- | ---
[<span data-ttu-id="bcdb5-258">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="bcdb5-258">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="bcdb5-259">Ajoute un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-259">Adds a NuGet package.</span></span>
[<span data-ttu-id="bcdb5-260">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="bcdb5-260">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="bcdb5-261">Supprime un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-261">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="bcdb5-262">Commandes NuGet</span><span class="sxs-lookup"><span data-stu-id="bcdb5-262">NuGet commands</span></span>

<span data-ttu-id="bcdb5-263">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-263">Command</span></span> | <span data-ttu-id="bcdb5-264">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-264">Function</span></span>
--- | ---
[<span data-ttu-id="bcdb5-265">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="bcdb5-265">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="bcdb5-266">Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-266">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="bcdb5-267">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="bcdb5-267">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="bcdb5-268">Efface ou liste les ressources NuGet locales telles que le cache de requête HTTP, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-268">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="bcdb5-269">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="bcdb5-269">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="bcdb5-270">Effectue une transmission de type push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-270">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="bcdb5-271">Outils et commandes globaux</span><span class="sxs-lookup"><span data-stu-id="bcdb5-271">Global Tools commands</span></span>

<span data-ttu-id="bcdb5-272">Les [outils globaux .NET Core](global-tools.md) sont disponibles à partir de .NET Core SDK 2.1.300 :</span><span class="sxs-lookup"><span data-stu-id="bcdb5-272">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="bcdb5-273">Commande</span><span class="sxs-lookup"><span data-stu-id="bcdb5-273">Command</span></span> | <span data-ttu-id="bcdb5-274">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-274">Function</span></span>
--- | ---
[<span data-ttu-id="bcdb5-275">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="bcdb5-275">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="bcdb5-276">Installe un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-276">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="bcdb5-277">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="bcdb5-277">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="bcdb5-278">Répertorie tous les outils globaux actuellement installés dans le répertoire par défaut de votre machine ou à l’emplacement du chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-278">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="bcdb5-279">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="bcdb5-279">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="bcdb5-280">Désinstalle un outil global de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-280">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="bcdb5-281">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="bcdb5-281">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="bcdb5-282">Met à jour un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-282">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="bcdb5-283">Outils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="bcdb5-283">Additional tools</span></span>

<span data-ttu-id="bcdb5-284">À partir de .NET Core SDK 2.1.300, un certain nombre d’outils qui étaient disponibles uniquement par projet à l’aide de `DotnetCliToolReference` sont désormais disponibles dans le cadre du Kit de développement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-284">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="bcdb5-285">Ces outils sont répertoriés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="bcdb5-285">These tools are listed in the following table:</span></span>

| <span data-ttu-id="bcdb5-286">Outil</span><span class="sxs-lookup"><span data-stu-id="bcdb5-286">Tool</span></span>                                              | <span data-ttu-id="bcdb5-287">Fonction</span><span class="sxs-lookup"><span data-stu-id="bcdb5-287">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="bcdb5-288">dev-certs</span><span class="sxs-lookup"><span data-stu-id="bcdb5-288">dev-certs</span></span>                                         | <span data-ttu-id="bcdb5-289">Crée et gère les certificats de développement.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-289">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="bcdb5-290">ef</span><span class="sxs-lookup"><span data-stu-id="bcdb5-290">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="bcdb5-291">Outils en ligne de commande Entity Framework Core.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-291">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="bcdb5-292">sql-cache</span><span class="sxs-lookup"><span data-stu-id="bcdb5-292">sql-cache</span></span>                                         | <span data-ttu-id="bcdb5-293">Outils en ligne de commande du cache SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-293">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="bcdb5-294">user-secrets</span><span class="sxs-lookup"><span data-stu-id="bcdb5-294">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="bcdb5-295">Gère les secrets de développement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-295">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="bcdb5-296">watch</span><span class="sxs-lookup"><span data-stu-id="bcdb5-296">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="bcdb5-297">Démarre un observateur de fichier qui exécute une commande à chaque modification de fichier.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-297">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="bcdb5-298">Pour plus d’informations sur chaque outil, tapez `dotnet <tool-name> --help`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-298">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="bcdb5-299">Exemples</span><span class="sxs-lookup"><span data-stu-id="bcdb5-299">Examples</span></span>

<span data-ttu-id="bcdb5-300">Crée une application console .NET Core :</span><span class="sxs-lookup"><span data-stu-id="bcdb5-300">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="bcdb5-301">Restaurez les dépendances d’une application donnée :</span><span class="sxs-lookup"><span data-stu-id="bcdb5-301">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="bcdb5-302">Générez un projet et ses dépendances dans un répertoire donné :</span><span class="sxs-lookup"><span data-stu-id="bcdb5-302">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="bcdb5-303">Exécutez une DLL d’application, par exemple `myapp.dll` :</span><span class="sxs-lookup"><span data-stu-id="bcdb5-303">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="bcdb5-304">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="bcdb5-304">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bcdb5-305">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bcdb5-305">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="bcdb5-306">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-306">The primary package cache.</span></span> <span data-ttu-id="bcdb5-307">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-307">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="bcdb5-308">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-308">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="bcdb5-309">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-309">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="bcdb5-310">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-310">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="bcdb5-311">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-311">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="bcdb5-312">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-312">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="bcdb5-313">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-313">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="bcdb5-314">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-314">If not set, it defaults to `true`.</span></span> <span data-ttu-id="bcdb5-315">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-315">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="bcdb5-316">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-316">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="bcdb5-317">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-317">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="bcdb5-318">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-318">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bcdb5-319">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bcdb5-319">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="bcdb5-320">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-320">The primary package cache.</span></span> <span data-ttu-id="bcdb5-321">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-321">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="bcdb5-322">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-322">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="bcdb5-323">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-323">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="bcdb5-324">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-324">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="bcdb5-325">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-325">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="bcdb5-326">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-326">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="bcdb5-327">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-327">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="bcdb5-328">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-328">If not set, it defaults to `true`.</span></span> <span data-ttu-id="bcdb5-329">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-329">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="bcdb5-330">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-330">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bcdb5-331">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bcdb5-331">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="bcdb5-332">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-332">The primary package cache.</span></span> <span data-ttu-id="bcdb5-333">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-333">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="bcdb5-334">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-334">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="bcdb5-335">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-335">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="bcdb5-336">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-336">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="bcdb5-337">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="bcdb5-337">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="bcdb5-338">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="bcdb5-338">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
