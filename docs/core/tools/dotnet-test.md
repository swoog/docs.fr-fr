---
title: Commande dotnet test - Interface CLI .NET Core
description: La commande dotnet test est utilisée pour exécuter des tests unitaires dans un projet donné.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 8a10ac9175ee5fcf8649efbb07d8d382ac3afdc7
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34696268"
---
# <a name="dotnet-test"></a><span data-ttu-id="6488d-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="6488d-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="6488d-104">Name</span><span class="sxs-lookup"><span data-stu-id="6488d-104">Name</span></span>

<span data-ttu-id="6488d-105">`dotnet test` - Pilote de test .NET utilisée pour exécuter des tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="6488d-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="6488d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6488d-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="6488d-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6488d-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="6488d-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="6488d-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="6488d-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="6488d-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]
dotnet test [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="6488d-110">Description</span><span class="sxs-lookup"><span data-stu-id="6488d-110">Description</span></span>

<span data-ttu-id="6488d-111">La commande `dotnet test` est utilisée pour exécuter des tests unitaires dans un projet donné.</span><span class="sxs-lookup"><span data-stu-id="6488d-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="6488d-112">La commande `dotnet test` lance l’application console Test Runner spécifiée pour un projet.</span><span class="sxs-lookup"><span data-stu-id="6488d-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="6488d-113">Test Runner exécute les tests définis pour un framework de tests unitaires (par exemple, MSTest, NUnit ou xUnit) et signale la réussite ou l’échec de chaque test.</span><span class="sxs-lookup"><span data-stu-id="6488d-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="6488d-114">Test Runner et la bibliothèque de tests unitaires sont empaquetés sous forme de packages NuGet et sont restaurés comme des dépendances ordinaires du projet.</span><span class="sxs-lookup"><span data-stu-id="6488d-114">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="6488d-115">Les projets de test spécifient l’application Test Runner à l’aide d’un élément `<PackageReference>` ordinaire, comme indiqué dans l’exemple de fichier projet suivant :</span><span class="sxs-lookup"><span data-stu-id="6488d-115">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="6488d-116">Arguments</span><span class="sxs-lookup"><span data-stu-id="6488d-116">Arguments</span></span>

`PROJECT`

<span data-ttu-id="6488d-117">Chemin du projet de test.</span><span class="sxs-lookup"><span data-stu-id="6488d-117">Path to the test project.</span></span> <span data-ttu-id="6488d-118">Si aucune valeur n’est spécifiée, le répertoire actif est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="6488d-118">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="6488d-119">Options</span><span class="sxs-lookup"><span data-stu-id="6488d-119">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="6488d-120">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6488d-120">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="6488d-121">Utilise les adaptateurs de tests personnalisés à partir du chemin spécifié dans la série de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-121">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="6488d-122">Exécute les tests en mode responsable.</span><span class="sxs-lookup"><span data-stu-id="6488d-122">Runs the tests in blame mode.</span></span> <span data-ttu-id="6488d-123">Cette option s’avère utile pour isoler les tests responsables du plantage de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="6488d-123">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="6488d-124">Elle crée un fichier de sortie dans le répertoire actif nommé *Sequence.xml* qui capture l’ordre d’exécution des tests avant le plantage.</span><span class="sxs-lookup"><span data-stu-id="6488d-124">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="6488d-125">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="6488d-125">Defines the build configuration.</span></span> <span data-ttu-id="6488d-126">La valeur par défaut est `Debug`, mais la configuration de votre projet peut remplacer ce paramètre du kit SDK par défaut.</span><span class="sxs-lookup"><span data-stu-id="6488d-126">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="6488d-127">Active le collecteur de données pour la série de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-127">Enables data collector for the test run.</span></span> <span data-ttu-id="6488d-128">Pour plus d’informations, consultez [Monitor and analyze test run](https://aka.ms/vstest-collect) (Surveiller et analyser la série de tests).</span><span class="sxs-lookup"><span data-stu-id="6488d-128">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="6488d-129">Active le mode de diagnostic pour la plateforme de test et écrit des messages de diagnostic dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="6488d-129">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="6488d-130">Recherche des binaires de test pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="6488d-130">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="6488d-131">Filtre les tests dans le projet actuel à l’aide de l’expression donnée.</span><span class="sxs-lookup"><span data-stu-id="6488d-131">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="6488d-132">Pour plus de détails, consultez la section [Détails de l’option de filtre](#filter-option-details).</span><span class="sxs-lookup"><span data-stu-id="6488d-132">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="6488d-133">Pour plus d’informations et pour obtenir des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="6488d-133">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="6488d-134">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-134">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="6488d-135">Spécifie un enregistreur d’événements pour les résultats de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-135">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="6488d-136">Ne génère pas le projet de test avant son exécution.</span><span class="sxs-lookup"><span data-stu-id="6488d-136">Doesn't build the test project before running it.</span></span> <span data-ttu-id="6488d-137">L’indicateur `--no-restore` est également défini implicitement.</span><span class="sxs-lookup"><span data-stu-id="6488d-137">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="6488d-138">N’effectue pas de restauration implicite à l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-138">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="6488d-139">Répertoire dans lequel rechercher les binaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6488d-139">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="6488d-140">Répertoire où les résultats de test doivent être placés.</span><span class="sxs-lookup"><span data-stu-id="6488d-140">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="6488d-141">Si le répertoire spécifié n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="6488d-141">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="6488d-142">Paramètres à utiliser durant l’exécution des tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-142">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="6488d-143">Répertorie tous les tests découverts dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6488d-143">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="6488d-144">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-144">Sets the verbosity level of the command.</span></span> <span data-ttu-id="6488d-145">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="6488d-145">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="6488d-146">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="6488d-146">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="6488d-147">Utilise les adaptateurs de tests personnalisés à partir du chemin spécifié dans la série de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-147">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="6488d-148">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="6488d-148">Defines the build configuration.</span></span> <span data-ttu-id="6488d-149">La valeur par défaut est `Debug`, mais la configuration de votre projet peut remplacer ce paramètre du kit SDK par défaut.</span><span class="sxs-lookup"><span data-stu-id="6488d-149">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="6488d-150">Active le collecteur de données pour la série de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-150">Enables data collector for the test run.</span></span> <span data-ttu-id="6488d-151">Pour plus d’informations, consultez [Monitor and analyze test run](https://aka.ms/vstest-collect) (Surveiller et analyser la série de tests).</span><span class="sxs-lookup"><span data-stu-id="6488d-151">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="6488d-152">Active le mode de diagnostic pour la plateforme de test et écrit des messages de diagnostic dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="6488d-152">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="6488d-153">Recherche des binaires de test pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="6488d-153">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="6488d-154">Filtre les tests dans le projet actuel à l’aide de l’expression donnée.</span><span class="sxs-lookup"><span data-stu-id="6488d-154">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="6488d-155">Pour plus de détails, consultez la section [Détails de l’option de filtre](#filter-option-details).</span><span class="sxs-lookup"><span data-stu-id="6488d-155">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="6488d-156">Pour plus d’informations et pour obtenir des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="6488d-156">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="6488d-157">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-157">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="6488d-158">Spécifie un enregistreur d’événements pour les résultats de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-158">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="6488d-159">Ne génère pas le projet de test avant son exécution.</span><span class="sxs-lookup"><span data-stu-id="6488d-159">Doesn't build the test project before running it.</span></span> <span data-ttu-id="6488d-160">L’indicateur `--no-restore` est également défini implicitement.</span><span class="sxs-lookup"><span data-stu-id="6488d-160">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="6488d-161">N’effectue pas de restauration implicite à l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-161">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="6488d-162">Répertoire dans lequel rechercher les binaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6488d-162">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="6488d-163">Répertoire où les résultats de test doivent être placés.</span><span class="sxs-lookup"><span data-stu-id="6488d-163">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="6488d-164">Si le répertoire spécifié n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="6488d-164">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="6488d-165">Paramètres à utiliser durant l’exécution des tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-165">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="6488d-166">Répertorie tous les tests découverts dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6488d-166">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="6488d-167">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-167">Sets the verbosity level of the command.</span></span> <span data-ttu-id="6488d-168">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="6488d-168">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="6488d-169">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="6488d-169">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="6488d-170">Utilise les adaptateurs de tests personnalisés à partir du chemin spécifié dans la série de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-170">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="6488d-171">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="6488d-171">Defines the build configuration.</span></span> <span data-ttu-id="6488d-172">La valeur par défaut est `Debug`, mais la configuration de votre projet peut remplacer ce paramètre du kit SDK par défaut.</span><span class="sxs-lookup"><span data-stu-id="6488d-172">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="6488d-173">Active le mode de diagnostic pour la plateforme de test et écrit des messages de diagnostic dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="6488d-173">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="6488d-174">Recherche des binaires de test pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="6488d-174">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="6488d-175">Filtre les tests dans le projet actuel à l’aide de l’expression donnée.</span><span class="sxs-lookup"><span data-stu-id="6488d-175">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="6488d-176">Pour plus de détails, consultez la section [Détails de l’option de filtre](#filter-option-details).</span><span class="sxs-lookup"><span data-stu-id="6488d-176">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="6488d-177">Pour plus d’informations et des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="6488d-177">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="6488d-178">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-178">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="6488d-179">Spécifie un enregistreur d’événements pour les résultats de tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-179">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="6488d-180">Ne génère pas le projet de test avant son exécution.</span><span class="sxs-lookup"><span data-stu-id="6488d-180">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="6488d-181">Répertoire dans lequel rechercher les binaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6488d-181">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="6488d-182">Paramètres à utiliser durant l’exécution des tests.</span><span class="sxs-lookup"><span data-stu-id="6488d-182">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="6488d-183">Répertorie tous les tests découverts dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="6488d-183">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="6488d-184">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="6488d-184">Sets the verbosity level of the command.</span></span> <span data-ttu-id="6488d-185">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="6488d-185">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="6488d-186">Exemples</span><span class="sxs-lookup"><span data-stu-id="6488d-186">Examples</span></span>

<span data-ttu-id="6488d-187">Exécutez les tests du projet dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="6488d-187">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="6488d-188">Exécuter les tests dans le projet `test1` :</span><span class="sxs-lookup"><span data-stu-id="6488d-188">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

## <a name="filter-option-details"></a><span data-ttu-id="6488d-189">Détails de l’option de filtre</span><span class="sxs-lookup"><span data-stu-id="6488d-189">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="6488d-190">`<Expression>` est au format `<property><operator><value>[|&<Expression>]`.</span><span class="sxs-lookup"><span data-stu-id="6488d-190">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="6488d-191">`<property>` est un attribut de `Test Case`.</span><span class="sxs-lookup"><span data-stu-id="6488d-191">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="6488d-192">Les propriétés suivantes sont prises en charge par les principales infrastructures de tests unitaires :</span><span class="sxs-lookup"><span data-stu-id="6488d-192">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="6488d-193">Infrastructure de test</span><span class="sxs-lookup"><span data-stu-id="6488d-193">Test Framework</span></span> | <span data-ttu-id="6488d-194">Propriétés prises en charge</span><span class="sxs-lookup"><span data-stu-id="6488d-194">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="6488d-195">MSTest</span><span class="sxs-lookup"><span data-stu-id="6488d-195">MSTest</span></span>         | <ul><li><span data-ttu-id="6488d-196">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="6488d-196">FullyQualifiedName</span></span></li><li><span data-ttu-id="6488d-197">Name</span><span class="sxs-lookup"><span data-stu-id="6488d-197">Name</span></span></li><li><span data-ttu-id="6488d-198">ClassName</span><span class="sxs-lookup"><span data-stu-id="6488d-198">ClassName</span></span></li><li><span data-ttu-id="6488d-199">Priorité</span><span class="sxs-lookup"><span data-stu-id="6488d-199">Priority</span></span></li><li><span data-ttu-id="6488d-200">TestCategory</span><span class="sxs-lookup"><span data-stu-id="6488d-200">TestCategory</span></span></li></ul> |
| <span data-ttu-id="6488d-201">xUnit</span><span class="sxs-lookup"><span data-stu-id="6488d-201">xUnit</span></span>          | <ul><li><span data-ttu-id="6488d-202">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="6488d-202">FullyQualifiedName</span></span></li><li><span data-ttu-id="6488d-203">DisplayName</span><span class="sxs-lookup"><span data-stu-id="6488d-203">DisplayName</span></span></li><li><span data-ttu-id="6488d-204">Caractéristiques</span><span class="sxs-lookup"><span data-stu-id="6488d-204">Traits</span></span></li></ul>                                   |

<span data-ttu-id="6488d-205">La section `<operator>` décrit la relation entre la propriété et la valeur :</span><span class="sxs-lookup"><span data-stu-id="6488d-205">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="6488d-206">Opérateur</span><span class="sxs-lookup"><span data-stu-id="6488d-206">Operator</span></span> | <span data-ttu-id="6488d-207">Fonction</span><span class="sxs-lookup"><span data-stu-id="6488d-207">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="6488d-208">Correspondance exacte</span><span class="sxs-lookup"><span data-stu-id="6488d-208">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="6488d-209">Pas de correspondance exacte</span><span class="sxs-lookup"><span data-stu-id="6488d-209">Not exact match</span></span> |
| `~`      | <span data-ttu-id="6488d-210">Contient</span><span class="sxs-lookup"><span data-stu-id="6488d-210">Contains</span></span>        |

<span data-ttu-id="6488d-211">`<value>` est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="6488d-211">`<value>` is a string.</span></span> <span data-ttu-id="6488d-212">Toutes les recherches respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="6488d-212">All the lookups are case insensitive.</span></span>

<span data-ttu-id="6488d-213">Une expression sans `<operator>` est automatiquement considérée comme `contains` sur la propriété `FullyQualifiedName` (par exemple, `dotnet test --filter xyz` est identique à `dotnet test --filter FullyQualifiedName~xyz`).</span><span class="sxs-lookup"><span data-stu-id="6488d-213">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="6488d-214">Les expressions peuvent être associées à des opérateurs conditionnels :</span><span class="sxs-lookup"><span data-stu-id="6488d-214">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="6488d-215">Opérateur</span><span class="sxs-lookup"><span data-stu-id="6488d-215">Operator</span></span>            | <span data-ttu-id="6488d-216">Fonction</span><span class="sxs-lookup"><span data-stu-id="6488d-216">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="6488d-217">OU</span><span class="sxs-lookup"><span data-stu-id="6488d-217">OR</span></span>       |
| `&`                 | <span data-ttu-id="6488d-218">AND</span><span class="sxs-lookup"><span data-stu-id="6488d-218">AND</span></span>      |

<span data-ttu-id="6488d-219">Vous pouvez mettre des expressions entre parenthèses quand vous utilisez des opérateurs conditionnels (par exemple, `(Name~TestMethod1) | (Name~TestMethod2)`).</span><span class="sxs-lookup"><span data-stu-id="6488d-219">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="6488d-220">Pour plus d’informations et des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="6488d-220">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6488d-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6488d-221">See also</span></span>

[<span data-ttu-id="6488d-222">Frameworks et cibles</span><span class="sxs-lookup"><span data-stu-id="6488d-222">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
[<span data-ttu-id="6488d-223">Catalogue d’identificateurs de runtime (RID) .NET Core</span><span class="sxs-lookup"><span data-stu-id="6488d-223">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
