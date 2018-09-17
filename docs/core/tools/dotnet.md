---
title: Commande dotnet - Interface CLI .NET Core
description: Découvrez la commande dotnet (le pilote générique des outils .NET Core CLI) et comment l’utiliser.
author: mairaw
ms.author: mairaw
ms.date: 06/04/2018
ms.openlocfilehash: 53e8f8bab1cbaabaa7926aa68197c18843b0b637
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44079814"
---
# <a name="dotnet-command"></a><span data-ttu-id="30db3-103">Commande dotnet</span><span class="sxs-lookup"><span data-stu-id="30db3-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="30db3-104">Name</span><span class="sxs-lookup"><span data-stu-id="30db3-104">Name</span></span>

<span data-ttu-id="30db3-105">`dotnet` - Outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="30db3-105">`dotnet` - A tool for managing .NET source code and binaries.</span></span>

## <a name="synopsis"></a><span data-ttu-id="30db3-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="30db3-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="30db3-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="30db3-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="30db3-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="30db3-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="30db3-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="30db3-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="30db3-110">Description</span><span class="sxs-lookup"><span data-stu-id="30db3-110">Description</span></span>

<span data-ttu-id="30db3-111">`dotnet` est un outil de gestion du code source et des ressources binaires .NET.</span><span class="sxs-lookup"><span data-stu-id="30db3-111">`dotnet` is a tool for managing .NET source code and binaries.</span></span> <span data-ttu-id="30db3-112">Il expose les commandes qui permettent d’effectuer des tâches spécifiques, par exemple [`dotnet build`](dotnet-build.md) et [`dotnet run`](dotnet-run.md).</span><span class="sxs-lookup"><span data-stu-id="30db3-112">It exposes commands that perform specific tasks, such as [`dotnet build`](dotnet-build.md) and [`dotnet run`](dotnet-run.md).</span></span> <span data-ttu-id="30db3-113">Chaque commande définit ses propres arguments.</span><span class="sxs-lookup"><span data-stu-id="30db3-113">Each command defines its own arguments.</span></span> <span data-ttu-id="30db3-114">Tapez `--help` après chaque commande pour accéder à une brève documentation d’aide.</span><span class="sxs-lookup"><span data-stu-id="30db3-114">Type `--help` after each command to access brief help documentation.</span></span>

<span data-ttu-id="30db3-115">Vous pouvez utiliser `dotnet` pour exécuter des applications en spécifiant une DLL d’application, par exemple `dotnet myapp.dll`.</span><span class="sxs-lookup"><span data-stu-id="30db3-115">`dotnet` can be used to run applications, by specifying an application DLL, such as `dotnet myapp.dll`.</span></span> <span data-ttu-id="30db3-116">Pour plus d’informations sur les options de déploiement, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="30db3-116">See [.NET Core application deployment](../deploying/index.md) for to learn about deployment options.</span></span>

## <a name="options"></a><span data-ttu-id="30db3-117">Options</span><span class="sxs-lookup"><span data-stu-id="30db3-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="30db3-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="30db3-118">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="30db3-119">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="30db3-119">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="30db3-120">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="30db3-120">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="30db3-121">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="30db3-121">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="30db3-122">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="30db3-122">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="30db3-123">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="30db3-123">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="30db3-124">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="30db3-124">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="30db3-125">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-125">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--list-runtimes`

<span data-ttu-id="30db3-126">Affiche les runtimes .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="30db3-126">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="30db3-127">Affiche les kits de développement logiciel .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="30db3-127">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="30db3-128">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="30db3-128">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="30db3-129">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="30db3-129">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="30db3-130">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="30db3-130">Sets the verbosity level of the command.</span></span> <span data-ttu-id="30db3-131">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="30db3-131">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="30db3-132">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="30db3-132">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="30db3-133">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="30db3-133">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="30db3-134">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="30db3-134">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="30db3-135">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="30db3-135">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="30db3-136">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="30db3-136">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="30db3-137">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="30db3-137">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="30db3-138">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="30db3-138">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="30db3-139">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="30db3-139">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="30db3-140">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="30db3-140">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="30db3-141">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-141">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="30db3-142">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="30db3-142">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="30db3-143">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="30db3-143">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="30db3-144">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="30db3-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="30db3-145">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="30db3-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="30db3-146">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="30db3-146">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="30db3-147">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="30db3-147">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="30db3-148">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="30db3-148">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="30db3-149">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="30db3-149">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="30db3-150">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="30db3-150">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="30db3-151">Version du runtime .NET Core à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="30db3-151">Version of the .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="30db3-152">Affiche la documentation relative à une commande donnée, par exemple `dotnet build --help`.</span><span class="sxs-lookup"><span data-stu-id="30db3-152">Prints out documentation for a given command, such as `dotnet build --help`.</span></span> <span data-ttu-id="30db3-153">`dotnet --help` affiche une liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="30db3-153">`dotnet --help` prints a list of available commands.</span></span>

`--info`

<span data-ttu-id="30db3-154">Affiche des informations détaillées sur une installation .NET Core et l’environnement de la machine, par exemple le système d’exploitation actuel, ainsi que le SHA de validation de la version du .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-154">Prints out detailed information about a .NET Core installation and the machine environment, such as the current operating system, and commit SHA of the .NET Core version.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="30db3-155">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="30db3-155">Sets the verbosity level of the command.</span></span> <span data-ttu-id="30db3-156">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="30db3-156">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="30db3-157">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="30db3-157">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="30db3-158">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="30db3-158">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="30db3-159">Commandes dotnet</span><span class="sxs-lookup"><span data-stu-id="30db3-159">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="30db3-160">Général</span><span class="sxs-lookup"><span data-stu-id="30db3-160">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="30db3-161">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="30db3-161">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="30db3-162">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-162">Command</span></span>                                       | <span data-ttu-id="30db3-163">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-163">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="30db3-164">dotnet build</span><span class="sxs-lookup"><span data-stu-id="30db3-164">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="30db3-165">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-165">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="30db3-166">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="30db3-166">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="30db3-167">Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="30db3-167">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="30db3-168">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="30db3-168">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="30db3-169">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="30db3-169">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="30db3-170">dotnet help</span><span class="sxs-lookup"><span data-stu-id="30db3-170">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="30db3-171">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="30db3-171">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="30db3-172">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="30db3-172">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="30db3-173">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="30db3-173">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="30db3-174">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="30db3-174">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="30db3-175">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="30db3-175">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="30db3-176">dotnet new</span><span class="sxs-lookup"><span data-stu-id="30db3-176">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="30db3-177">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="30db3-177">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="30db3-178">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="30db3-178">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="30db3-179">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="30db3-179">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="30db3-180">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="30db3-180">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="30db3-181">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="30db3-181">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="30db3-182">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="30db3-182">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="30db3-183">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="30db3-183">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="30db3-184">dotnet run</span><span class="sxs-lookup"><span data-stu-id="30db3-184">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="30db3-185">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="30db3-185">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="30db3-186">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="30db3-186">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="30db3-187">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="30db3-187">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="30db3-188">dotnet store</span><span class="sxs-lookup"><span data-stu-id="30db3-188">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="30db3-189">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="30db3-189">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="30db3-190">dotnet test</span><span class="sxs-lookup"><span data-stu-id="30db3-190">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="30db3-191">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="30db3-191">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="30db3-192">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="30db3-192">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="30db3-193">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-193">Command</span></span>                             | <span data-ttu-id="30db3-194">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-194">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="30db3-195">dotnet build</span><span class="sxs-lookup"><span data-stu-id="30db3-195">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="30db3-196">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-196">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="30db3-197">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="30db3-197">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="30db3-198">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="30db3-198">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="30db3-199">dotnet help</span><span class="sxs-lookup"><span data-stu-id="30db3-199">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="30db3-200">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="30db3-200">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="30db3-201">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="30db3-201">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="30db3-202">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="30db3-202">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="30db3-203">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="30db3-203">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="30db3-204">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="30db3-204">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="30db3-205">dotnet new</span><span class="sxs-lookup"><span data-stu-id="30db3-205">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="30db3-206">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="30db3-206">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="30db3-207">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="30db3-207">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="30db3-208">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="30db3-208">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="30db3-209">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="30db3-209">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="30db3-210">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="30db3-210">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="30db3-211">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="30db3-211">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="30db3-212">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="30db3-212">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="30db3-213">dotnet run</span><span class="sxs-lookup"><span data-stu-id="30db3-213">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="30db3-214">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="30db3-214">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="30db3-215">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="30db3-215">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="30db3-216">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="30db3-216">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="30db3-217">dotnet store</span><span class="sxs-lookup"><span data-stu-id="30db3-217">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="30db3-218">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="30db3-218">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="30db3-219">dotnet test</span><span class="sxs-lookup"><span data-stu-id="30db3-219">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="30db3-220">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="30db3-220">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="30db3-221">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="30db3-221">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="30db3-222">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-222">Command</span></span>                             | <span data-ttu-id="30db3-223">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-223">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="30db3-224">dotnet build</span><span class="sxs-lookup"><span data-stu-id="30db3-224">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="30db3-225">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-225">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="30db3-226">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="30db3-226">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="30db3-227">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="30db3-227">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="30db3-228">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="30db3-228">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="30db3-229">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="30db3-229">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="30db3-230">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="30db3-230">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="30db3-231">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="30db3-231">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="30db3-232">dotnet new</span><span class="sxs-lookup"><span data-stu-id="30db3-232">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="30db3-233">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="30db3-233">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="30db3-234">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="30db3-234">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="30db3-235">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="30db3-235">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="30db3-236">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="30db3-236">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="30db3-237">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="30db3-237">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="30db3-238">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="30db3-238">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="30db3-239">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="30db3-239">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="30db3-240">dotnet run</span><span class="sxs-lookup"><span data-stu-id="30db3-240">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="30db3-241">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="30db3-241">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="30db3-242">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="30db3-242">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="30db3-243">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="30db3-243">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="30db3-244">dotnet test</span><span class="sxs-lookup"><span data-stu-id="30db3-244">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="30db3-245">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="30db3-245">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="30db3-246">Références de projets</span><span class="sxs-lookup"><span data-stu-id="30db3-246">Project references</span></span>

<span data-ttu-id="30db3-247">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-247">Command</span></span> | <span data-ttu-id="30db3-248">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-248">Function</span></span>
--- | ---
[<span data-ttu-id="30db3-249">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="30db3-249">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="30db3-250">Ajoute une référence au projet.</span><span class="sxs-lookup"><span data-stu-id="30db3-250">Adds a project reference.</span></span>
[<span data-ttu-id="30db3-251">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="30db3-251">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="30db3-252">Liste les références du projet.</span><span class="sxs-lookup"><span data-stu-id="30db3-252">Lists project references.</span></span>
[<span data-ttu-id="30db3-253">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="30db3-253">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="30db3-254">Supprime une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="30db3-254">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="30db3-255">Packages NuGet</span><span class="sxs-lookup"><span data-stu-id="30db3-255">NuGet packages</span></span>

<span data-ttu-id="30db3-256">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-256">Command</span></span> | <span data-ttu-id="30db3-257">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-257">Function</span></span>
--- | ---
[<span data-ttu-id="30db3-258">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="30db3-258">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="30db3-259">Ajoute un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="30db3-259">Adds a NuGet package.</span></span>
[<span data-ttu-id="30db3-260">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="30db3-260">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="30db3-261">Supprime un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="30db3-261">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="30db3-262">Commandes NuGet</span><span class="sxs-lookup"><span data-stu-id="30db3-262">NuGet commands</span></span>

<span data-ttu-id="30db3-263">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-263">Command</span></span> | <span data-ttu-id="30db3-264">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-264">Function</span></span>
--- | ---
[<span data-ttu-id="30db3-265">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="30db3-265">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="30db3-266">Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="30db3-266">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="30db3-267">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="30db3-267">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="30db3-268">Efface ou liste les ressources NuGet locales telles que le cache de requête HTTP, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30db3-268">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="30db3-269">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="30db3-269">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="30db3-270">Effectue une transmission de type push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="30db3-270">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="30db3-271">Outils et commandes globaux</span><span class="sxs-lookup"><span data-stu-id="30db3-271">Global Tools commands</span></span>

<span data-ttu-id="30db3-272">Les [outils globaux .NET Core](global-tools.md) sont disponibles à partir de .NET Core SDK 2.1.300 :</span><span class="sxs-lookup"><span data-stu-id="30db3-272">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="30db3-273">Commande</span><span class="sxs-lookup"><span data-stu-id="30db3-273">Command</span></span> | <span data-ttu-id="30db3-274">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-274">Function</span></span>
--- | ---
[<span data-ttu-id="30db3-275">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="30db3-275">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="30db3-276">Installe un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30db3-276">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="30db3-277">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="30db3-277">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="30db3-278">Répertorie tous les outils globaux actuellement installés dans le répertoire par défaut de votre machine ou à l’emplacement du chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="30db3-278">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="30db3-279">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="30db3-279">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="30db3-280">Désinstalle un outil global de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30db3-280">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="30db3-281">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="30db3-281">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="30db3-282">Met à jour un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="30db3-282">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="30db3-283">Outils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="30db3-283">Additional tools</span></span>

<span data-ttu-id="30db3-284">À partir de .NET Core SDK 2.1.300, un certain nombre d’outils qui étaient disponibles uniquement par projet à l’aide de `DotnetCliToolReference` sont désormais disponibles dans le cadre du Kit de développement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-284">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="30db3-285">Ces outils sont répertoriés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="30db3-285">These tools are listed in the following table:</span></span>

| <span data-ttu-id="30db3-286">Outil</span><span class="sxs-lookup"><span data-stu-id="30db3-286">Tool</span></span>                                              | <span data-ttu-id="30db3-287">Fonction</span><span class="sxs-lookup"><span data-stu-id="30db3-287">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="30db3-288">dev-certs</span><span class="sxs-lookup"><span data-stu-id="30db3-288">dev-certs</span></span>                                         | <span data-ttu-id="30db3-289">Crée et gère les certificats de développement.</span><span class="sxs-lookup"><span data-stu-id="30db3-289">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="30db3-290">ef</span><span class="sxs-lookup"><span data-stu-id="30db3-290">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="30db3-291">Outils en ligne de commande Entity Framework Core.</span><span class="sxs-lookup"><span data-stu-id="30db3-291">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="30db3-292">sql-cache</span><span class="sxs-lookup"><span data-stu-id="30db3-292">sql-cache</span></span>                                         | <span data-ttu-id="30db3-293">Outils en ligne de commande du cache SQL Server.</span><span class="sxs-lookup"><span data-stu-id="30db3-293">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="30db3-294">user-secrets</span><span class="sxs-lookup"><span data-stu-id="30db3-294">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="30db3-295">Gère les secrets de développement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="30db3-295">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="30db3-296">watch</span><span class="sxs-lookup"><span data-stu-id="30db3-296">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="30db3-297">Démarre un observateur de fichier qui exécute une commande à chaque modification de fichier.</span><span class="sxs-lookup"><span data-stu-id="30db3-297">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="30db3-298">Pour plus d’informations sur chaque outil, tapez `dotnet <tool-name> --help`.</span><span class="sxs-lookup"><span data-stu-id="30db3-298">For more information about each tool, type `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="30db3-299">Exemples</span><span class="sxs-lookup"><span data-stu-id="30db3-299">Examples</span></span>

<span data-ttu-id="30db3-300">Crée une application console .NET Core :</span><span class="sxs-lookup"><span data-stu-id="30db3-300">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="30db3-301">Restaurez les dépendances d’une application donnée :</span><span class="sxs-lookup"><span data-stu-id="30db3-301">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="30db3-302">Générez un projet et ses dépendances dans un répertoire donné :</span><span class="sxs-lookup"><span data-stu-id="30db3-302">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="30db3-303">Exécutez une DLL d’application, par exemple `myapp.dll` :</span><span class="sxs-lookup"><span data-stu-id="30db3-303">Run an application DLL, such as `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="30db3-304">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="30db3-304">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="30db3-305">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="30db3-305">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="30db3-306">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="30db3-306">The primary package cache.</span></span> <span data-ttu-id="30db3-307">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="30db3-307">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="30db3-308">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="30db3-308">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="30db3-309">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30db3-309">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="30db3-310">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="30db3-310">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="30db3-311">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="30db3-311">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="30db3-312">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="30db3-312">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="30db3-313">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="30db3-313">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="30db3-314">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="30db3-314">If not set, it defaults to `true`.</span></span> <span data-ttu-id="30db3-315">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="30db3-315">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="30db3-316">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="30db3-316">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="30db3-317">Désactive la restauration par progression d’une version mineure, si la valeur est `0`.</span><span class="sxs-lookup"><span data-stu-id="30db3-317">Disables minor version roll forward, if set to `0`.</span></span> <span data-ttu-id="30db3-318">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="30db3-318">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="30db3-319">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="30db3-319">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="30db3-320">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="30db3-320">The primary package cache.</span></span> <span data-ttu-id="30db3-321">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="30db3-321">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="30db3-322">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="30db3-322">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="30db3-323">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30db3-323">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="30db3-324">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="30db3-324">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="30db3-325">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="30db3-325">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="30db3-326">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="30db3-326">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="30db3-327">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="30db3-327">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="30db3-328">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="30db3-328">If not set, it defaults to `true`.</span></span> <span data-ttu-id="30db3-329">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="30db3-329">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="30db3-330">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="30db3-330">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="30db3-331">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="30db3-331">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="30db3-332">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="30db3-332">The primary package cache.</span></span> <span data-ttu-id="30db3-333">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="30db3-333">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="30db3-334">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="30db3-334">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="30db3-335">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30db3-335">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="30db3-336">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="30db3-336">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="30db3-337">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="30db3-337">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="30db3-338">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="30db3-338">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
