---
title: Commande dotnet - Interface CLI .NET Core
description: Découvrez la commande dotnet (le pilote générique des outils .NET Core CLI) et comment l’utiliser.
author: mairaw
ms.author: mairaw
ms.date: 06/04/2018
ms.openlocfilehash: 788dc746705f9328683019ab3ad9836204a1ea63
ms.sourcegitcommit: fc70fcb9c789b6a4aefcdace46f3643fd076450f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34805657"
---
# <a name="dotnet-command"></a><span data-ttu-id="706b0-103">Commande dotnet</span><span class="sxs-lookup"><span data-stu-id="706b0-103">dotnet command</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="706b0-104">Name</span><span class="sxs-lookup"><span data-stu-id="706b0-104">Name</span></span>

<span data-ttu-id="706b0-105">`dotnet` - Pilote général pour l’exécution des commandes de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-105">`dotnet` - General driver for running the command-line commands.</span></span>

## <a name="synopsis"></a><span data-ttu-id="706b0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="706b0-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="706b0-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="706b0-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [--list-runtimes] [--list-sdks] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="706b0-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="706b0-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet [command] [arguments] [--additional-deps] [--additionalprobingpath] [-d|--diagnostics]
    [--fx-version] [-h|--help] [--info] [--roll-forward-on-no-candidate-fx] [-v|--verbosity] [--version]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="706b0-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="706b0-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet [command] [arguments] [--additionalprobingpath] [-d|--diagnostics] [--fx-version]
    [-h|--help] [--info] [-v|--verbosity] [--version]
```
---

## <a name="description"></a><span data-ttu-id="706b0-110">Description</span><span class="sxs-lookup"><span data-stu-id="706b0-110">Description</span></span>

<span data-ttu-id="706b0-111">`dotnet` est un pilote générique pour la chaîne d’outils de l’interface de ligne de commande (CLI).</span><span class="sxs-lookup"><span data-stu-id="706b0-111">`dotnet` is a generic driver for the Command Line Interface (CLI) toolchain.</span></span> <span data-ttu-id="706b0-112">Appelé seul, il fournit des instructions d’utilisation succinctes.</span><span class="sxs-lookup"><span data-stu-id="706b0-112">Invoked on its own, it provides brief usage instructions.</span></span>

<span data-ttu-id="706b0-113">Chaque fonctionnalité est implémentée comme une commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-113">Each specific feature is implemented as a command.</span></span> <span data-ttu-id="706b0-114">Pour utiliser la fonctionnalité, la commande est spécifiée après `dotnet`, comme dans [`dotnet build`](dotnet-build.md).</span><span class="sxs-lookup"><span data-stu-id="706b0-114">To use the feature, the command is specified after `dotnet`, such as [`dotnet build`](dotnet-build.md).</span></span> <span data-ttu-id="706b0-115">Tous les arguments qui suivent la commande sont ses arguments propres.</span><span class="sxs-lookup"><span data-stu-id="706b0-115">All of the arguments following the command are its own arguments.</span></span>

<span data-ttu-id="706b0-116">Le seul cas où la commande `dotnet` est utilisée seule est l’exécution d’applications [dépendantes du framework](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="706b0-116">The only time `dotnet` is used as a command on its own is to run [framework-dependent apps](../deploying/index.md).</span></span> <span data-ttu-id="706b0-117">Spécifiez une DLL d’application après le verbe `dotnet` pour exécuter l’application (par exemple, `dotnet myapp.dll`).</span><span class="sxs-lookup"><span data-stu-id="706b0-117">Specify an application DLL after the `dotnet` verb to execute the application (for example, `dotnet myapp.dll`).</span></span>

## <a name="options"></a><span data-ttu-id="706b0-118">Options</span><span class="sxs-lookup"><span data-stu-id="706b0-118">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="706b0-119">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="706b0-119">.NET Core 2.1</span></span>](#tab/netcore21)

`--additional-deps <PATH>`

<span data-ttu-id="706b0-120">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="706b0-120">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="706b0-121">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="706b0-121">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="706b0-122">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="706b0-122">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="706b0-123">Version du runtime .NET Core installé à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="706b0-123">Version of the installed .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="706b0-124">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-124">Prints out a short help for the command.</span></span> <span data-ttu-id="706b0-125">Si vous l’utilisez avec `dotnet`, elle affiche également la liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="706b0-125">If using with `dotnet`, it also prints a list of the available commands.</span></span>

`--info`

<span data-ttu-id="706b0-126">Affiche des informations détaillées sur l’environnement et les outils CLI, telles que le système d’exploitation actuel, le SHA de validation de la version, etc.</span><span class="sxs-lookup"><span data-stu-id="706b0-126">Prints out detailed information about the CLI tooling and the environment, such as the current operating system, commit SHA for the version, and other information.</span></span>

`--list-runtimes`

<span data-ttu-id="706b0-127">Affiche les runtimes .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="706b0-127">Displays the installed .NET Core runtimes.</span></span>

`--list-sdks`

<span data-ttu-id="706b0-128">Affiche les kits de développement logiciel .NET Core installés.</span><span class="sxs-lookup"><span data-stu-id="706b0-128">Displays the installed .NET Core SDKs.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="706b0-129">Effectue une restauration par progression en l’absence de framework candidat partagé.</span><span class="sxs-lookup"><span data-stu-id="706b0-129">Rolls forward on no candidate shared framework.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="706b0-130">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-130">Sets the verbosity level of the command.</span></span> <span data-ttu-id="706b0-131">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="706b0-131">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="706b0-132">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="706b0-132">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="706b0-133">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="706b0-133">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="706b0-134">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="706b0-134">.NET Core 2.0</span></span>](#tab/netcore20)

`--additional-deps <PATH>`

<span data-ttu-id="706b0-135">Chemin du fichier *deps.json* supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="706b0-135">Path to additional *deps.json* file.</span></span>

`--additionalprobingpath <PATH>`

<span data-ttu-id="706b0-136">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="706b0-136">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="706b0-137">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="706b0-137">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="706b0-138">Version du runtime .NET Core installé à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="706b0-138">Version of the installed .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="706b0-139">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-139">Prints out a short help for the command.</span></span> <span data-ttu-id="706b0-140">Si vous l’utilisez avec `dotnet`, elle affiche également la liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="706b0-140">If using with `dotnet`, it also prints a list of the available commands.</span></span>

`--info`

<span data-ttu-id="706b0-141">Affiche des informations détaillées sur l’environnement et les outils CLI, telles que le système d’exploitation actuel, le SHA de validation de la version, etc.</span><span class="sxs-lookup"><span data-stu-id="706b0-141">Prints out detailed information about the CLI tooling and the environment, such as the current operating system, commit SHA for the version, and other information.</span></span>

`--roll-forward-on-no-candidate-fx`

 <span data-ttu-id="706b0-142">Effectue une restauration par progression en l’absence de framework candidat partagé.</span><span class="sxs-lookup"><span data-stu-id="706b0-142">Rolls forward on no candidate shared framework.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="706b0-143">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-143">Sets the verbosity level of the command.</span></span> <span data-ttu-id="706b0-144">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="706b0-144">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="706b0-145">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="706b0-145">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="706b0-146">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="706b0-146">Prints out the version of the .NET Core SDK in use.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="706b0-147">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="706b0-147">.NET Core 1.x</span></span>](#tab/netcore1x)

`--additionalprobingpath <PATH>`

<span data-ttu-id="706b0-148">Chemin d’accès contenant la stratégie de sondage et les assemblys à sonder.</span><span class="sxs-lookup"><span data-stu-id="706b0-148">Path containing probing policy and assemblies to probe.</span></span>

`-d|--diagnostics`

<span data-ttu-id="706b0-149">Active la sortie de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="706b0-149">Enables diagnostic output.</span></span>

`--fx-version <VERSION>`

<span data-ttu-id="706b0-150">Version du runtime .NET Core installé à utiliser pour exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="706b0-150">Version of the installed .NET Core runtime to use to run the application.</span></span>

`-h|--help`

<span data-ttu-id="706b0-151">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-151">Prints out a short help for the command.</span></span> <span data-ttu-id="706b0-152">Si vous l’utilisez avec `dotnet`, elle affiche également la liste des commandes disponibles.</span><span class="sxs-lookup"><span data-stu-id="706b0-152">If using with `dotnet`, it also prints a list of the available commands.</span></span>

`--info`

<span data-ttu-id="706b0-153">Affiche des informations détaillées sur l’environnement et les outils CLI, telles que le système d’exploitation actuel, le SHA de validation de la version, etc.</span><span class="sxs-lookup"><span data-stu-id="706b0-153">Prints out detailed information about the CLI tooling and the environment, such as the current operating system, commit SHA for the version, and other information.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="706b0-154">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-154">Sets the verbosity level of the command.</span></span> <span data-ttu-id="706b0-155">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="706b0-155">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span> <span data-ttu-id="706b0-156">Non pris en charge dans toutes les commandes ; consultez la page de commande spécifique pour déterminer si cette option est disponible.</span><span class="sxs-lookup"><span data-stu-id="706b0-156">Not supported in every command; see specific command page to determine if this option is available.</span></span>

`--version`

<span data-ttu-id="706b0-157">Affiche la version du SDK .NET Core en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="706b0-157">Prints out the version of the .NET Core SDK in use.</span></span>

---

## <a name="dotnet-commands"></a><span data-ttu-id="706b0-158">Commandes dotnet</span><span class="sxs-lookup"><span data-stu-id="706b0-158">dotnet commands</span></span>

### <a name="general"></a><span data-ttu-id="706b0-159">Général</span><span class="sxs-lookup"><span data-stu-id="706b0-159">General</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="706b0-160">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="706b0-160">.NET Core 2.1</span></span>](#tab/netcore21)

| <span data-ttu-id="706b0-161">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-161">Command</span></span>                                       | <span data-ttu-id="706b0-162">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-162">Function</span></span>                                                            |
| --------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="706b0-163">dotnet build</span><span class="sxs-lookup"><span data-stu-id="706b0-163">dotnet build</span></span>](dotnet-build.md)               | <span data-ttu-id="706b0-164">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="706b0-164">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="706b0-165">dotnet build-server</span><span class="sxs-lookup"><span data-stu-id="706b0-165">dotnet build-server</span></span>](dotnet-build-server.md) | <span data-ttu-id="706b0-166">Interagit avec les serveurs démarrés par une build.</span><span class="sxs-lookup"><span data-stu-id="706b0-166">Interacts with servers started by a build.</span></span>                          |
| [<span data-ttu-id="706b0-167">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="706b0-167">dotnet clean</span></span>](dotnet-clean.md)               | <span data-ttu-id="706b0-168">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="706b0-168">Clean build outputs.</span></span>                                                |
| [<span data-ttu-id="706b0-169">dotnet help</span><span class="sxs-lookup"><span data-stu-id="706b0-169">dotnet help</span></span>](dotnet-help.md)                 | <span data-ttu-id="706b0-170">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-170">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="706b0-171">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="706b0-171">dotnet migrate</span></span>](dotnet-migrate.md)           | <span data-ttu-id="706b0-172">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="706b0-172">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="706b0-173">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="706b0-173">dotnet msbuild</span></span>](dotnet-msbuild.md)           | <span data-ttu-id="706b0-174">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="706b0-174">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="706b0-175">dotnet new</span><span class="sxs-lookup"><span data-stu-id="706b0-175">dotnet new</span></span>](dotnet-new.md)                   | <span data-ttu-id="706b0-176">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="706b0-176">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="706b0-177">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="706b0-177">dotnet pack</span></span>](dotnet-pack.md)                 | <span data-ttu-id="706b0-178">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="706b0-178">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="706b0-179">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="706b0-179">dotnet publish</span></span>](dotnet-publish.md)           | <span data-ttu-id="706b0-180">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="706b0-180">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="706b0-181">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="706b0-181">dotnet restore</span></span>](dotnet-restore.md)           | <span data-ttu-id="706b0-182">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="706b0-182">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="706b0-183">dotnet run</span><span class="sxs-lookup"><span data-stu-id="706b0-183">dotnet run</span></span>](dotnet-run.md)                   | <span data-ttu-id="706b0-184">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="706b0-184">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="706b0-185">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="706b0-185">dotnet sln</span></span>](dotnet-sln.md)                   | <span data-ttu-id="706b0-186">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="706b0-186">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="706b0-187">dotnet store</span><span class="sxs-lookup"><span data-stu-id="706b0-187">dotnet store</span></span>](dotnet-store.md)               | <span data-ttu-id="706b0-188">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="706b0-188">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="706b0-189">dotnet test</span><span class="sxs-lookup"><span data-stu-id="706b0-189">dotnet test</span></span>](dotnet-test.md)                 | <span data-ttu-id="706b0-190">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="706b0-190">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="706b0-191">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="706b0-191">.NET Core 2.0</span></span>](#tab/netcore20)

| <span data-ttu-id="706b0-192">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-192">Command</span></span>                             | <span data-ttu-id="706b0-193">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-193">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="706b0-194">dotnet build</span><span class="sxs-lookup"><span data-stu-id="706b0-194">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="706b0-195">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="706b0-195">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="706b0-196">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="706b0-196">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="706b0-197">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="706b0-197">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="706b0-198">dotnet help</span><span class="sxs-lookup"><span data-stu-id="706b0-198">dotnet help</span></span>](dotnet-help.md)       | <span data-ttu-id="706b0-199">Affiche plus de documentation détaillée en ligne pour la commande.</span><span class="sxs-lookup"><span data-stu-id="706b0-199">Shows more detailed documentation online for the command.</span></span>           |
| [<span data-ttu-id="706b0-200">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="706b0-200">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="706b0-201">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="706b0-201">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="706b0-202">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="706b0-202">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="706b0-203">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="706b0-203">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="706b0-204">dotnet new</span><span class="sxs-lookup"><span data-stu-id="706b0-204">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="706b0-205">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="706b0-205">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="706b0-206">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="706b0-206">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="706b0-207">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="706b0-207">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="706b0-208">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="706b0-208">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="706b0-209">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="706b0-209">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="706b0-210">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="706b0-210">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="706b0-211">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="706b0-211">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="706b0-212">dotnet run</span><span class="sxs-lookup"><span data-stu-id="706b0-212">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="706b0-213">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="706b0-213">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="706b0-214">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="706b0-214">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="706b0-215">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="706b0-215">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="706b0-216">dotnet store</span><span class="sxs-lookup"><span data-stu-id="706b0-216">dotnet store</span></span>](dotnet-store.md)     | <span data-ttu-id="706b0-217">Stocke les assemblys dans le magasin de packages de runtime.</span><span class="sxs-lookup"><span data-stu-id="706b0-217">Stores assemblies in the runtime package store.</span></span>                     |
| [<span data-ttu-id="706b0-218">dotnet test</span><span class="sxs-lookup"><span data-stu-id="706b0-218">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="706b0-219">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="706b0-219">Runs tests using a test runner.</span></span>                                     |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="706b0-220">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="706b0-220">.NET Core 1.x</span></span>](#tab/netcore1x)

| <span data-ttu-id="706b0-221">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-221">Command</span></span>                             | <span data-ttu-id="706b0-222">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-222">Function</span></span>                                                            |
| ----------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="706b0-223">dotnet build</span><span class="sxs-lookup"><span data-stu-id="706b0-223">dotnet build</span></span>](dotnet-build.md)     | <span data-ttu-id="706b0-224">Génère une application .NET Core.</span><span class="sxs-lookup"><span data-stu-id="706b0-224">Builds a .NET Core application.</span></span>                                     |
| [<span data-ttu-id="706b0-225">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="706b0-225">dotnet clean</span></span>](dotnet-clean.md)     | <span data-ttu-id="706b0-226">Nettoie les sorties de build.</span><span class="sxs-lookup"><span data-stu-id="706b0-226">Clean build outputs.</span></span>                                              |
| [<span data-ttu-id="706b0-227">dotnet migrate</span><span class="sxs-lookup"><span data-stu-id="706b0-227">dotnet migrate</span></span>](dotnet-migrate.md) | <span data-ttu-id="706b0-228">Migre un projet Preview 2 valide vers un projet SDK .NET Core 1.0.</span><span class="sxs-lookup"><span data-stu-id="706b0-228">Migrates a valid Preview 2 project to a .NET Core SDK 1.0 project.</span></span>  |
| [<span data-ttu-id="706b0-229">dotnet msbuild</span><span class="sxs-lookup"><span data-stu-id="706b0-229">dotnet msbuild</span></span>](dotnet-msbuild.md) | <span data-ttu-id="706b0-230">Fournit l’accès à la ligne de commande MSBuild.</span><span class="sxs-lookup"><span data-stu-id="706b0-230">Provides access to the MSBuild command line.</span></span>                        |
| [<span data-ttu-id="706b0-231">dotnet new</span><span class="sxs-lookup"><span data-stu-id="706b0-231">dotnet new</span></span>](dotnet-new.md)         | <span data-ttu-id="706b0-232">Initialise un projet C# ou F# pour un modèle donné.</span><span class="sxs-lookup"><span data-stu-id="706b0-232">Initializes a C# or F# project for a given template.</span></span>                |
| [<span data-ttu-id="706b0-233">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="706b0-233">dotnet pack</span></span>](dotnet-pack.md)       | <span data-ttu-id="706b0-234">Crée un package NuGet à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="706b0-234">Creates a NuGet package of your code.</span></span>                               |
| [<span data-ttu-id="706b0-235">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="706b0-235">dotnet publish</span></span>](dotnet-publish.md) | <span data-ttu-id="706b0-236">Publie une application .NET dépendante du framework ou autonome.</span><span class="sxs-lookup"><span data-stu-id="706b0-236">Publishes a .NET framework-dependent or self-contained application.</span></span> |
| [<span data-ttu-id="706b0-237">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="706b0-237">dotnet restore</span></span>](dotnet-restore.md) | <span data-ttu-id="706b0-238">Restaure les dépendances d’une application donnée.</span><span class="sxs-lookup"><span data-stu-id="706b0-238">Restores the dependencies for a given application.</span></span>                  |
| [<span data-ttu-id="706b0-239">dotnet run</span><span class="sxs-lookup"><span data-stu-id="706b0-239">dotnet run</span></span>](dotnet-run.md)         | <span data-ttu-id="706b0-240">Exécute l’application à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="706b0-240">Runs the application from source.</span></span>                                   |
| [<span data-ttu-id="706b0-241">dotnet sln</span><span class="sxs-lookup"><span data-stu-id="706b0-241">dotnet sln</span></span>](dotnet-sln.md)         | <span data-ttu-id="706b0-242">Options pour ajouter, supprimer et lister des projets dans un fichier solution.</span><span class="sxs-lookup"><span data-stu-id="706b0-242">Options to add, remove, and list projects in a solution file.</span></span>       |
| [<span data-ttu-id="706b0-243">dotnet test</span><span class="sxs-lookup"><span data-stu-id="706b0-243">dotnet test</span></span>](dotnet-test.md)       | <span data-ttu-id="706b0-244">Exécute des tests à l’aide d’un lanceur de tests.</span><span class="sxs-lookup"><span data-stu-id="706b0-244">Runs tests using a test runner.</span></span>                                     |

---

### <a name="project-references"></a><span data-ttu-id="706b0-245">Références de projets</span><span class="sxs-lookup"><span data-stu-id="706b0-245">Project references</span></span>

<span data-ttu-id="706b0-246">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-246">Command</span></span> | <span data-ttu-id="706b0-247">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-247">Function</span></span>
--- | ---
[<span data-ttu-id="706b0-248">dotnet add reference</span><span class="sxs-lookup"><span data-stu-id="706b0-248">dotnet add reference</span></span>](dotnet-add-reference.md) | <span data-ttu-id="706b0-249">Ajoute une référence au projet.</span><span class="sxs-lookup"><span data-stu-id="706b0-249">Adds a project reference.</span></span>
[<span data-ttu-id="706b0-250">dotnet list reference</span><span class="sxs-lookup"><span data-stu-id="706b0-250">dotnet list reference</span></span>](dotnet-list-reference.md) | <span data-ttu-id="706b0-251">Liste les références du projet.</span><span class="sxs-lookup"><span data-stu-id="706b0-251">Lists project references.</span></span>
[<span data-ttu-id="706b0-252">dotnet remove reference</span><span class="sxs-lookup"><span data-stu-id="706b0-252">dotnet remove reference</span></span>](dotnet-remove-reference.md) | <span data-ttu-id="706b0-253">Supprime une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="706b0-253">Removes a project reference.</span></span>

### <a name="nuget-packages"></a><span data-ttu-id="706b0-254">Packages NuGet</span><span class="sxs-lookup"><span data-stu-id="706b0-254">NuGet packages</span></span>

<span data-ttu-id="706b0-255">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-255">Command</span></span> | <span data-ttu-id="706b0-256">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-256">Function</span></span>
--- | ---
[<span data-ttu-id="706b0-257">dotnet add package</span><span class="sxs-lookup"><span data-stu-id="706b0-257">dotnet add package</span></span>](dotnet-add-package.md) | <span data-ttu-id="706b0-258">Ajoute un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="706b0-258">Adds a NuGet package.</span></span>
[<span data-ttu-id="706b0-259">dotnet remove package</span><span class="sxs-lookup"><span data-stu-id="706b0-259">dotnet remove package</span></span>](dotnet-remove-package.md) | <span data-ttu-id="706b0-260">Supprime un package NuGet.</span><span class="sxs-lookup"><span data-stu-id="706b0-260">Removes a NuGet package.</span></span>

### <a name="nuget-commands"></a><span data-ttu-id="706b0-261">Commandes NuGet</span><span class="sxs-lookup"><span data-stu-id="706b0-261">NuGet commands</span></span>

<span data-ttu-id="706b0-262">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-262">Command</span></span> | <span data-ttu-id="706b0-263">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-263">Function</span></span>
--- | ---
[<span data-ttu-id="706b0-264">dotnet nuget delete</span><span class="sxs-lookup"><span data-stu-id="706b0-264">dotnet nuget delete</span></span>](dotnet-nuget-delete.md) | <span data-ttu-id="706b0-265">Supprime ou retire un package du serveur.</span><span class="sxs-lookup"><span data-stu-id="706b0-265">Deletes or unlists a package from the server.</span></span>
[<span data-ttu-id="706b0-266">dotnet nuget locals</span><span class="sxs-lookup"><span data-stu-id="706b0-266">dotnet nuget locals</span></span>](dotnet-nuget-locals.md) | <span data-ttu-id="706b0-267">Efface ou liste les ressources NuGet locales telles que le cache de requête HTTP, le cache temporaire ou le dossier de packages globaux à l’échelle de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="706b0-267">Clears or lists local NuGet resources such as http-request cache, temporary cache, or machine-wide global packages folder.</span></span>
[<span data-ttu-id="706b0-268">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="706b0-268">dotnet nuget push</span></span>](dotnet-nuget-push.md) | <span data-ttu-id="706b0-269">Effectue une transmission de type push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="706b0-269">Pushes a package to the server and publishes it.</span></span>

### <a name="global-tools-commands"></a><span data-ttu-id="706b0-270">Outils et commandes globaux</span><span class="sxs-lookup"><span data-stu-id="706b0-270">Global Tools commands</span></span>

<span data-ttu-id="706b0-271">Les [outils globaux .NET Core](global-tools.md) sont disponibles à partir de .NET Core SDK 2.1.300 :</span><span class="sxs-lookup"><span data-stu-id="706b0-271">[.NET Core Global Tools](global-tools.md) are available starting with .NET Core SDK 2.1.300:</span></span>

<span data-ttu-id="706b0-272">Commande</span><span class="sxs-lookup"><span data-stu-id="706b0-272">Command</span></span> | <span data-ttu-id="706b0-273">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-273">Function</span></span>
--- | ---
[<span data-ttu-id="706b0-274">dotnet tool install</span><span class="sxs-lookup"><span data-stu-id="706b0-274">dotnet tool install</span></span>](dotnet-tool-install.md) | <span data-ttu-id="706b0-275">Installe un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="706b0-275">Installs a Global Tool on your machine.</span></span>
[<span data-ttu-id="706b0-276">dotnet tool list</span><span class="sxs-lookup"><span data-stu-id="706b0-276">dotnet tool list</span></span>](dotnet-tool-list.md) | <span data-ttu-id="706b0-277">Répertorie tous les outils globaux actuellement installés dans le répertoire par défaut de votre machine ou à l’emplacement du chemin spécifié.</span><span class="sxs-lookup"><span data-stu-id="706b0-277">Lists all Global Tools currently installed in the default directory on your machine or in the specified path.</span></span>
[<span data-ttu-id="706b0-278">dotnet tool uninstall</span><span class="sxs-lookup"><span data-stu-id="706b0-278">dotnet tool uninstall</span></span>](dotnet-tool-uninstall.md) | <span data-ttu-id="706b0-279">Désinstalle un outil global de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="706b0-279">Uninstalls a Global Tool from your machine.</span></span>
[<span data-ttu-id="706b0-280">dotnet tool update</span><span class="sxs-lookup"><span data-stu-id="706b0-280">dotnet tool update</span></span>](dotnet-tool-update.md) | <span data-ttu-id="706b0-281">Met à jour un outil global sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="706b0-281">Updates a Global Tool on your machine.</span></span>

### <a name="additional-tools"></a><span data-ttu-id="706b0-282">Outils supplémentaires</span><span class="sxs-lookup"><span data-stu-id="706b0-282">Additional tools</span></span>

<span data-ttu-id="706b0-283">À partir de .NET Core SDK 2.1.300, un certain nombre d’outils qui étaient disponibles uniquement par projet à l’aide de `DotnetCliToolReference` sont désormais disponibles dans le cadre du Kit de développement .NET Core.</span><span class="sxs-lookup"><span data-stu-id="706b0-283">Starting with .NET Core SDK 2.1.300, a number of tools that were available only on a per project basis using `DotnetCliToolReference` are now available as part of the .NET Core SDK.</span></span> <span data-ttu-id="706b0-284">Ces outils incluent :</span><span class="sxs-lookup"><span data-stu-id="706b0-284">These tools include:</span></span>

| <span data-ttu-id="706b0-285">Outil</span><span class="sxs-lookup"><span data-stu-id="706b0-285">Tool</span></span>                                              | <span data-ttu-id="706b0-286">Fonction</span><span class="sxs-lookup"><span data-stu-id="706b0-286">Function</span></span>                                                     |
| ------------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="706b0-287">dev-certs</span><span class="sxs-lookup"><span data-stu-id="706b0-287">dev-certs</span></span>                                         | <span data-ttu-id="706b0-288">Crée et gère les certificats de développement.</span><span class="sxs-lookup"><span data-stu-id="706b0-288">Creates and manages development certificates.</span></span>                |
| [<span data-ttu-id="706b0-289">ef</span><span class="sxs-lookup"><span data-stu-id="706b0-289">ef</span></span>](/ef/core/miscellaneous/cli/dotnet)           | <span data-ttu-id="706b0-290">Outils en ligne de commande Entity Framework Core.</span><span class="sxs-lookup"><span data-stu-id="706b0-290">Entity Framework Core command-line tools.</span></span>                    |
| <span data-ttu-id="706b0-291">sql-cache</span><span class="sxs-lookup"><span data-stu-id="706b0-291">sql-cache</span></span>                                         | <span data-ttu-id="706b0-292">Outils en ligne de commande du cache SQL Server.</span><span class="sxs-lookup"><span data-stu-id="706b0-292">SQL Server cache command-line tools.</span></span>                         |
| [<span data-ttu-id="706b0-293">user-secrets</span><span class="sxs-lookup"><span data-stu-id="706b0-293">user-secrets</span></span>](/aspnet/core/security/app-secrets) | <span data-ttu-id="706b0-294">Gère les secrets de développement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="706b0-294">Manages development user secrets.</span></span>                            |
| [<span data-ttu-id="706b0-295">watch</span><span class="sxs-lookup"><span data-stu-id="706b0-295">watch</span></span>](/aspnet/core/tutorials/dotnet-watch)      | <span data-ttu-id="706b0-296">Démarre un observateur de fichier qui exécute une commande à chaque modification de fichier.</span><span class="sxs-lookup"><span data-stu-id="706b0-296">Starts a file watcher that runs a command when files change.</span></span> |

<span data-ttu-id="706b0-297">Pour plus d'informations sur chaque outil, exécutez `dotnet <tool-name> --help`.</span><span class="sxs-lookup"><span data-stu-id="706b0-297">For more information about each tool, execute `dotnet <tool-name> --help`.</span></span>

## <a name="examples"></a><span data-ttu-id="706b0-298">Exemples</span><span class="sxs-lookup"><span data-stu-id="706b0-298">Examples</span></span>

<span data-ttu-id="706b0-299">Crée une application console .NET Core :</span><span class="sxs-lookup"><span data-stu-id="706b0-299">Creates a new .NET Core console application:</span></span>

`dotnet new console`

<span data-ttu-id="706b0-300">Restaurez les dépendances d’une application donnée :</span><span class="sxs-lookup"><span data-stu-id="706b0-300">Restore dependencies for a given application:</span></span>

`dotnet restore`

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

<span data-ttu-id="706b0-301">Générez un projet et ses dépendances dans un répertoire donné :</span><span class="sxs-lookup"><span data-stu-id="706b0-301">Build a project and its dependencies in a given directory:</span></span>

`dotnet build`

<span data-ttu-id="706b0-302">Exécuter une application dépendante du framework nommée `myapp.dll` :</span><span class="sxs-lookup"><span data-stu-id="706b0-302">Run a framework-dependent app named `myapp.dll`:</span></span>

`dotnet myapp.dll`

## <a name="environment-variables"></a><span data-ttu-id="706b0-303">Variables d’environnement</span><span class="sxs-lookup"><span data-stu-id="706b0-303">Environment variables</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="706b0-304">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="706b0-304">.NET Core 2.1</span></span>](#tab/netcore21)

`DOTNET_PACKAGES`

<span data-ttu-id="706b0-305">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="706b0-305">The primary package cache.</span></span> <span data-ttu-id="706b0-306">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="706b0-306">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="706b0-307">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="706b0-307">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="706b0-308">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="706b0-308">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="706b0-309">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="706b0-309">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="706b0-310">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="706b0-310">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="706b0-311">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="706b0-311">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="706b0-312">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="706b0-312">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="706b0-313">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="706b0-313">If not set, it defaults to `true`.</span></span> <span data-ttu-id="706b0-314">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="706b0-314">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="706b0-315">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="706b0-315">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

`DOTNET_ROLL_FORWARD_ON_NO_CANDIDATE_FX`

<span data-ttu-id="706b0-316">Désactive la restauration par progression d’une version mineure.</span><span class="sxs-lookup"><span data-stu-id="706b0-316">Disables minor version roll forward.</span></span> <span data-ttu-id="706b0-317">Pour plus d'informations, consultez [Restauration par progression](../whats-new/dotnet-core-2-1.md#roll-forward).</span><span class="sxs-lookup"><span data-stu-id="706b0-317">For more information, see [Roll forward](../whats-new/dotnet-core-2-1.md#roll-forward).</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="706b0-318">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="706b0-318">.NET Core 2.0</span></span>](#tab/netcore20)

`DOTNET_PACKAGES`

<span data-ttu-id="706b0-319">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="706b0-319">The primary package cache.</span></span> <span data-ttu-id="706b0-320">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="706b0-320">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="706b0-321">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="706b0-321">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="706b0-322">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="706b0-322">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="706b0-323">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="706b0-323">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="706b0-324">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="706b0-324">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="706b0-325">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="706b0-325">If not set, the default is `false` and the telemetry feature is active.</span></span>

`DOTNET_MULTILEVEL_LOOKUP`

<span data-ttu-id="706b0-326">Spécifie si le runtime .NET Core, le framework partagé ou le SDK sont résolus à partir de l’emplacement global.</span><span class="sxs-lookup"><span data-stu-id="706b0-326">Specifies whether .NET Core runtime, shared framework, or SDK are resolved from the global location.</span></span> <span data-ttu-id="706b0-327">Si elle n’est pas définie, la valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="706b0-327">If not set, it defaults to `true`.</span></span> <span data-ttu-id="706b0-328">Définie sur `false` pour ne pas résoudre depuis l’emplacement global et avoir des installations .NET Core (les valeurs `0` ou `false` sont acceptées).</span><span class="sxs-lookup"><span data-stu-id="706b0-328">Set to `false` to not resolve from the global location and have isolated .NET Core installations (values `0` or `false` are accepted).</span></span> <span data-ttu-id="706b0-329">Pour plus d’informations sur la recherche multiniveau, consultez [Recherche SharedFX multiniveau](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span><span class="sxs-lookup"><span data-stu-id="706b0-329">For more information about multi-level lookup, see [Multi-level SharedFX Lookup](https://github.com/dotnet/core-setup/blob/master/Documentation/design-docs/multilevel-sharedfx-lookup.md).</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="706b0-330">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="706b0-330">.NET Core 1.x</span></span>](#tab/netcore1x)

`DOTNET_PACKAGES`

<span data-ttu-id="706b0-331">Cache du package principal.</span><span class="sxs-lookup"><span data-stu-id="706b0-331">The primary package cache.</span></span> <span data-ttu-id="706b0-332">S’il n’est pas défini, les valeurs par défaut sont `$HOME/.nuget/packages` sous Unix et `%HOME%\NuGet\Packages` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="706b0-332">If not set, it defaults to `$HOME/.nuget/packages` on Unix or `%HOME%\NuGet\Packages` on Windows.</span></span>

`DOTNET_SERVICING`

<span data-ttu-id="706b0-333">Spécifie l’emplacement de l’index de service que doit utiliser l’hôte partagé lors du chargement de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="706b0-333">Specifies the location of the servicing index to use by the shared host when loading the runtime.</span></span>

`DOTNET_CLI_TELEMETRY_OPTOUT`

<span data-ttu-id="706b0-334">Spécifie si les données concernant l’utilisation des outils .NET Core doivent être collectées et envoyées à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="706b0-334">Specifies whether data about the .NET Core tools usage is collected and sent to Microsoft.</span></span> <span data-ttu-id="706b0-335">Définie sur `true` pour ne pas adhérer à la fonctionnalité de télémétrie (valeurs acceptées : `true`, `1` ou `yes`).</span><span class="sxs-lookup"><span data-stu-id="706b0-335">Set to `true` to opt-out of the telemetry feature (values `true`, `1`, or `yes` accepted).</span></span> <span data-ttu-id="706b0-336">Sinon, définie sur `false` pour adhérer aux fonctionnalités de télémétrie (valeurs acceptées : `false`, `0` ou `no`).</span><span class="sxs-lookup"><span data-stu-id="706b0-336">Otherwise, set to `false` to opt into the telemetry features (values `false`, `0`, or `no` accepted).</span></span> <span data-ttu-id="706b0-337">Si elle n’est pas définie, la valeur par défaut est `false`, et la fonctionnalité de télémétrie est active.</span><span class="sxs-lookup"><span data-stu-id="706b0-337">If not set, the default is `false` and the telemetry feature is active.</span></span>

---
