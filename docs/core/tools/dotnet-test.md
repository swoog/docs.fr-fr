---
title: Commande dotnet test - Interface CLI .NET Core
description: La commande dotnet test est utilisée pour exécuter des tests unitaires dans un projet donné.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: e80ba874ec8d0fbc49858719dc3b9b6e02254c78
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2018
ms.locfileid: "46696454"
---
# <a name="dotnet-test"></a><span data-ttu-id="298c4-103">dotnet test</span><span class="sxs-lookup"><span data-stu-id="298c4-103">dotnet test</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="298c4-104">Name</span><span class="sxs-lookup"><span data-stu-id="298c4-104">Name</span></span>

<span data-ttu-id="298c4-105">`dotnet test` - Pilote de test .NET utilisée pour exécuter des tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="298c4-105">`dotnet test` - .NET test driver used to execute unit tests.</span></span>

## <a name="synopsis"></a><span data-ttu-id="298c4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="298c4-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="298c4-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="298c4-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [--blame] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="298c4-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="298c4-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [--collect] [-d|--diag] [-f|--framework] [--filter]
    [-l|--logger] [--no-build] [--no-restore] [-o|--output] [-r|--results-directory] [-s|--settings] [-t|--list-tests] [-v|--verbosity]
dotnet test [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="298c4-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="298c4-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet test [<PROJECT>] [-a|--test-adapter-path] [-c|--configuration] [-d|--diag] [-f|--framework] [--filter] [-l|--logger] [--no-build] [-o|--output] [-s|--settings] [-t|--list-tests]  [-v|--verbosity]
dotnet test [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="298c4-110">Description</span><span class="sxs-lookup"><span data-stu-id="298c4-110">Description</span></span>

<span data-ttu-id="298c4-111">La commande `dotnet test` est utilisée pour exécuter des tests unitaires dans un projet donné.</span><span class="sxs-lookup"><span data-stu-id="298c4-111">The `dotnet test` command is used to execute unit tests in a given project.</span></span> <span data-ttu-id="298c4-112">La commande `dotnet test` lance l’application console Test Runner spécifiée pour un projet.</span><span class="sxs-lookup"><span data-stu-id="298c4-112">The `dotnet test` command launches the test runner console application specified for a project.</span></span> <span data-ttu-id="298c4-113">Test Runner exécute les tests définis pour un framework de tests unitaires (par exemple, MSTest, NUnit ou xUnit) et signale la réussite ou l’échec de chaque test.</span><span class="sxs-lookup"><span data-stu-id="298c4-113">The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test.</span></span> <span data-ttu-id="298c4-114">Si tous les tests réussissent, l’exécuteur de tests retourne 0 en tant que code de sortie. Sinon, si un test échoue, il retourne 1.</span><span class="sxs-lookup"><span data-stu-id="298c4-114">If all tests are successful, the test runner returns 0 as an exit code; otherwise if any test fails, it returns 1.</span></span> <span data-ttu-id="298c4-115">Test Runner et la bibliothèque de tests unitaires sont empaquetés sous forme de packages NuGet et sont restaurés comme des dépendances ordinaires du projet.</span><span class="sxs-lookup"><span data-stu-id="298c4-115">The test runner and the unit test library are packaged as NuGet packages and are restored as ordinary dependencies for the project.</span></span>

<span data-ttu-id="298c4-116">Les projets de test spécifient l’application Test Runner à l’aide d’un élément `<PackageReference>` ordinaire, comme indiqué dans l’exemple de fichier projet suivant :</span><span class="sxs-lookup"><span data-stu-id="298c4-116">Test projects specify the test runner using an ordinary `<PackageReference>` element, as seen in the following sample project file:</span></span>

[!code-xml[XUnit Basic Template](../../../samples/snippets/csharp/xunit-test/xunit-test.csproj)]

## <a name="arguments"></a><span data-ttu-id="298c4-117">Arguments</span><span class="sxs-lookup"><span data-stu-id="298c4-117">Arguments</span></span>

`PROJECT`

<span data-ttu-id="298c4-118">Chemin du projet de test.</span><span class="sxs-lookup"><span data-stu-id="298c4-118">Path to the test project.</span></span> <span data-ttu-id="298c4-119">Si aucune valeur n’est spécifiée, le répertoire actif est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="298c4-119">If not specified, it defaults to current directory.</span></span>

## <a name="options"></a><span data-ttu-id="298c4-120">Options</span><span class="sxs-lookup"><span data-stu-id="298c4-120">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="298c4-121">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="298c4-121">.NET Core 2.1</span></span>](#tab/netcore21)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="298c4-122">Utilise les adaptateurs de tests personnalisés à partir du chemin spécifié dans la série de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-122">Use the custom test adapters from the specified path in the test run.</span></span>

`--blame`

<span data-ttu-id="298c4-123">Exécute les tests en mode responsable.</span><span class="sxs-lookup"><span data-stu-id="298c4-123">Runs the tests in blame mode.</span></span> <span data-ttu-id="298c4-124">Cette option s’avère utile pour isoler les tests responsables du plantage de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="298c4-124">This option is helpful in isolating the problematic tests causing test host to crash.</span></span> <span data-ttu-id="298c4-125">Elle crée un fichier de sortie dans le répertoire actif nommé *Sequence.xml* qui capture l’ordre d’exécution des tests avant le plantage.</span><span class="sxs-lookup"><span data-stu-id="298c4-125">It creates an output file in the current directory as *Sequence.xml* that captures the order of tests execution before the crash.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="298c4-126">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="298c4-126">Defines the build configuration.</span></span> <span data-ttu-id="298c4-127">La valeur par défaut est `Debug`, mais la configuration de votre projet peut remplacer ce paramètre du kit SDK par défaut.</span><span class="sxs-lookup"><span data-stu-id="298c4-127">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="298c4-128">Active le collecteur de données pour la série de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-128">Enables data collector for the test run.</span></span> <span data-ttu-id="298c4-129">Pour plus d’informations, consultez [Monitor and analyze test run](https://aka.ms/vstest-collect) (Surveiller et analyser la série de tests).</span><span class="sxs-lookup"><span data-stu-id="298c4-129">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="298c4-130">Active le mode de diagnostic pour la plateforme de test et écrit des messages de diagnostic dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="298c4-130">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="298c4-131">Recherche des binaires de test pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="298c4-131">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="298c4-132">Filtre les tests dans le projet actuel à l’aide de l’expression donnée.</span><span class="sxs-lookup"><span data-stu-id="298c4-132">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="298c4-133">Pour plus de détails, consultez la section [Détails de l’option de filtre](#filter-option-details).</span><span class="sxs-lookup"><span data-stu-id="298c4-133">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="298c4-134">Pour plus d’informations et des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="298c4-134">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="298c4-135">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-135">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="298c4-136">Spécifie un enregistreur d’événements pour les résultats de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-136">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="298c4-137">Ne génère pas le projet de test avant son exécution.</span><span class="sxs-lookup"><span data-stu-id="298c4-137">Doesn't build the test project before running it.</span></span> <span data-ttu-id="298c4-138">L’indicateur `--no-restore` est également défini implicitement.</span><span class="sxs-lookup"><span data-stu-id="298c4-138">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="298c4-139">N’effectue pas de restauration implicite à l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-139">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="298c4-140">Répertoire dans lequel rechercher les binaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="298c4-140">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="298c4-141">Répertoire où les résultats de test doivent être placés.</span><span class="sxs-lookup"><span data-stu-id="298c4-141">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="298c4-142">Si le répertoire spécifié n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="298c4-142">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="298c4-143">Paramètres à utiliser durant l’exécution des tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-143">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="298c4-144">Répertorie tous les tests découverts dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="298c4-144">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="298c4-145">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-145">Sets the verbosity level of the command.</span></span> <span data-ttu-id="298c4-146">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="298c4-146">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="298c4-147">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="298c4-147">.NET Core 2.0</span></span>](#tab/netcore20)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="298c4-148">Utilise les adaptateurs de tests personnalisés à partir du chemin spécifié dans la série de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-148">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="298c4-149">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="298c4-149">Defines the build configuration.</span></span> <span data-ttu-id="298c4-150">La valeur par défaut est `Debug`, mais la configuration de votre projet peut remplacer ce paramètre du kit SDK par défaut.</span><span class="sxs-lookup"><span data-stu-id="298c4-150">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`--collect <DATA_COLLECTOR_FRIENDLY_NAME>`

<span data-ttu-id="298c4-151">Active le collecteur de données pour la série de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-151">Enables data collector for the test run.</span></span> <span data-ttu-id="298c4-152">Pour plus d’informations, consultez [Monitor and analyze test run](https://aka.ms/vstest-collect) (Surveiller et analyser la série de tests).</span><span class="sxs-lookup"><span data-stu-id="298c4-152">For more information, see [Monitor and analyze test run](https://aka.ms/vstest-collect).</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="298c4-153">Active le mode de diagnostic pour la plateforme de test et écrit des messages de diagnostic dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="298c4-153">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="298c4-154">Recherche des binaires de test pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="298c4-154">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="298c4-155">Filtre les tests dans le projet actuel à l’aide de l’expression donnée.</span><span class="sxs-lookup"><span data-stu-id="298c4-155">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="298c4-156">Pour plus de détails, consultez la section [Détails de l’option de filtre](#filter-option-details).</span><span class="sxs-lookup"><span data-stu-id="298c4-156">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="298c4-157">Pour plus d’informations et des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="298c4-157">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="298c4-158">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-158">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="298c4-159">Spécifie un enregistreur d’événements pour les résultats de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-159">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="298c4-160">Ne génère pas le projet de test avant son exécution.</span><span class="sxs-lookup"><span data-stu-id="298c4-160">Doesn't build the test project before running it.</span></span> <span data-ttu-id="298c4-161">L’indicateur `--no-restore` est également défini implicitement.</span><span class="sxs-lookup"><span data-stu-id="298c4-161">It also implicit sets the `--no-restore` flag.</span></span>

`--no-restore`

<span data-ttu-id="298c4-162">N’effectue pas de restauration implicite à l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-162">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="298c4-163">Répertoire dans lequel rechercher les binaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="298c4-163">Directory in which to find the binaries to run.</span></span>

`-r|--results-directory <PATH>`

<span data-ttu-id="298c4-164">Répertoire où les résultats de test doivent être placés.</span><span class="sxs-lookup"><span data-stu-id="298c4-164">The directory where the test results are going to be placed.</span></span> <span data-ttu-id="298c4-165">Si le répertoire spécifié n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="298c4-165">If the specified directory doesn't exist, it's created.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="298c4-166">Paramètres à utiliser durant l’exécution des tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-166">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="298c4-167">Répertorie tous les tests découverts dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="298c4-167">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="298c4-168">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-168">Sets the verbosity level of the command.</span></span> <span data-ttu-id="298c4-169">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="298c4-169">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="298c4-170">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="298c4-170">.NET Core 1.x</span></span>](#tab/netcore1x)

`-a|--test-adapter-path <PATH_TO_ADAPTER>`

<span data-ttu-id="298c4-171">Utilise les adaptateurs de tests personnalisés à partir du chemin spécifié dans la série de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-171">Use the custom test adapters from the specified path in the test run.</span></span>

`-c|--configuration {Debug|Release}`

<span data-ttu-id="298c4-172">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="298c4-172">Defines the build configuration.</span></span> <span data-ttu-id="298c4-173">La valeur par défaut est `Debug`, mais la configuration de votre projet peut remplacer ce paramètre du kit SDK par défaut.</span><span class="sxs-lookup"><span data-stu-id="298c4-173">The default value is `Debug`, but your project's configuration could override this default SDK setting.</span></span>

`-d|--diag <PATH_TO_DIAGNOSTICS_FILE>`

<span data-ttu-id="298c4-174">Active le mode de diagnostic pour la plateforme de test et écrit des messages de diagnostic dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="298c4-174">Enables diagnostic mode for the test platform and write diagnostic messages to the specified file.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="298c4-175">Recherche des binaires de test pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="298c4-175">Looks for test binaries for a specific [framework](../../standard/frameworks.md).</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="298c4-176">Filtre les tests dans le projet actuel à l’aide de l’expression donnée.</span><span class="sxs-lookup"><span data-stu-id="298c4-176">Filters out tests in the current project using the given expression.</span></span> <span data-ttu-id="298c4-177">Pour plus de détails, consultez la section [Détails de l’option de filtre](#filter-option-details).</span><span class="sxs-lookup"><span data-stu-id="298c4-177">For more information, see the [Filter option details](#filter-option-details) section.</span></span> <span data-ttu-id="298c4-178">Pour plus d’informations et des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="298c4-178">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

`-h|--help`

<span data-ttu-id="298c4-179">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-179">Prints out a short help for the command.</span></span>

`-l|--logger <LoggerUri/FriendlyName>`

<span data-ttu-id="298c4-180">Spécifie un enregistreur d’événements pour les résultats de tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-180">Specifies a logger for test results.</span></span>

`--no-build`

<span data-ttu-id="298c4-181">Ne génère pas le projet de test avant son exécution.</span><span class="sxs-lookup"><span data-stu-id="298c4-181">Doesn't build the test project before running it.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="298c4-182">Répertoire dans lequel rechercher les binaires à exécuter.</span><span class="sxs-lookup"><span data-stu-id="298c4-182">Directory in which to find the binaries to run.</span></span>

`-s|--settings <SETTINGS_FILE>`

<span data-ttu-id="298c4-183">Paramètres à utiliser durant l’exécution des tests.</span><span class="sxs-lookup"><span data-stu-id="298c4-183">Settings to use when running tests.</span></span>

`-t|--list-tests`

<span data-ttu-id="298c4-184">Répertorie tous les tests découverts dans le projet actuel.</span><span class="sxs-lookup"><span data-stu-id="298c4-184">List all of the discovered tests in the current project.</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="298c4-185">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="298c4-185">Sets the verbosity level of the command.</span></span> <span data-ttu-id="298c4-186">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="298c4-186">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="298c4-187">Exemples</span><span class="sxs-lookup"><span data-stu-id="298c4-187">Examples</span></span>

<span data-ttu-id="298c4-188">Exécutez les tests du projet dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="298c4-188">Run the tests in the project in the current directory:</span></span>

`dotnet test`

<span data-ttu-id="298c4-189">Exécuter les tests dans le projet `test1` :</span><span class="sxs-lookup"><span data-stu-id="298c4-189">Run the tests in the `test1` project:</span></span>

`dotnet test ~/projects/test1/test1.csproj`

<span data-ttu-id="298c4-190">Exécutez les tests du projet dans le répertoire actif et générez un fichier de résultats des tests au format trx :</span><span class="sxs-lookup"><span data-stu-id="298c4-190">Run the tests in the project in the current directory and generate a test results file in the trx format:</span></span>

`dotnet test --logger:trx`

## <a name="filter-option-details"></a><span data-ttu-id="298c4-191">Détails de l’option de filtre</span><span class="sxs-lookup"><span data-stu-id="298c4-191">Filter option details</span></span>

`--filter <EXPRESSION>`

<span data-ttu-id="298c4-192">`<Expression>` est au format `<property><operator><value>[|&<Expression>]`.</span><span class="sxs-lookup"><span data-stu-id="298c4-192">`<Expression>` has the format `<property><operator><value>[|&<Expression>]`.</span></span>

<span data-ttu-id="298c4-193">`<property>` est un attribut de `Test Case`.</span><span class="sxs-lookup"><span data-stu-id="298c4-193">`<property>` is an attribute of the `Test Case`.</span></span> <span data-ttu-id="298c4-194">Les propriétés suivantes sont prises en charge par les principales infrastructures de tests unitaires :</span><span class="sxs-lookup"><span data-stu-id="298c4-194">The following are the properties supported by popular unit test frameworks:</span></span>

| <span data-ttu-id="298c4-195">Infrastructure de test</span><span class="sxs-lookup"><span data-stu-id="298c4-195">Test Framework</span></span> | <span data-ttu-id="298c4-196">Propriétés prises en charge</span><span class="sxs-lookup"><span data-stu-id="298c4-196">Supported properties</span></span>                                                                                      |
| -------------- | --------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="298c4-197">MSTest</span><span class="sxs-lookup"><span data-stu-id="298c4-197">MSTest</span></span>         | <ul><li><span data-ttu-id="298c4-198">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="298c4-198">FullyQualifiedName</span></span></li><li><span data-ttu-id="298c4-199">Name</span><span class="sxs-lookup"><span data-stu-id="298c4-199">Name</span></span></li><li><span data-ttu-id="298c4-200">ClassName</span><span class="sxs-lookup"><span data-stu-id="298c4-200">ClassName</span></span></li><li><span data-ttu-id="298c4-201">Priorité</span><span class="sxs-lookup"><span data-stu-id="298c4-201">Priority</span></span></li><li><span data-ttu-id="298c4-202">TestCategory</span><span class="sxs-lookup"><span data-stu-id="298c4-202">TestCategory</span></span></li></ul> |
| <span data-ttu-id="298c4-203">xUnit</span><span class="sxs-lookup"><span data-stu-id="298c4-203">xUnit</span></span>          | <ul><li><span data-ttu-id="298c4-204">FullyQualifiedName</span><span class="sxs-lookup"><span data-stu-id="298c4-204">FullyQualifiedName</span></span></li><li><span data-ttu-id="298c4-205">DisplayName</span><span class="sxs-lookup"><span data-stu-id="298c4-205">DisplayName</span></span></li><li><span data-ttu-id="298c4-206">Caractéristiques</span><span class="sxs-lookup"><span data-stu-id="298c4-206">Traits</span></span></li></ul>                                   |

<span data-ttu-id="298c4-207">La section `<operator>` décrit la relation entre la propriété et la valeur :</span><span class="sxs-lookup"><span data-stu-id="298c4-207">The `<operator>` describes the relationship between the property and the value:</span></span>

| <span data-ttu-id="298c4-208">Opérateur</span><span class="sxs-lookup"><span data-stu-id="298c4-208">Operator</span></span> | <span data-ttu-id="298c4-209">Fonction</span><span class="sxs-lookup"><span data-stu-id="298c4-209">Function</span></span>        |
| :------: | --------------- |
| `=`      | <span data-ttu-id="298c4-210">Correspondance exacte</span><span class="sxs-lookup"><span data-stu-id="298c4-210">Exact match</span></span>     |
| `!=`     | <span data-ttu-id="298c4-211">Pas de correspondance exacte</span><span class="sxs-lookup"><span data-stu-id="298c4-211">Not exact match</span></span> |
| `~`      | <span data-ttu-id="298c4-212">Contient</span><span class="sxs-lookup"><span data-stu-id="298c4-212">Contains</span></span>        |

<span data-ttu-id="298c4-213">`<value>` est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="298c4-213">`<value>` is a string.</span></span> <span data-ttu-id="298c4-214">Toutes les recherches respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="298c4-214">All the lookups are case insensitive.</span></span>

<span data-ttu-id="298c4-215">Une expression sans `<operator>` est automatiquement considérée comme `contains` sur la propriété `FullyQualifiedName` (par exemple, `dotnet test --filter xyz` est identique à `dotnet test --filter FullyQualifiedName~xyz`).</span><span class="sxs-lookup"><span data-stu-id="298c4-215">An expression without an `<operator>` is automatically considered as a `contains` on `FullyQualifiedName` property (for example, `dotnet test --filter xyz` is same as `dotnet test --filter FullyQualifiedName~xyz`).</span></span>

<span data-ttu-id="298c4-216">Les expressions peuvent être associées à des opérateurs conditionnels :</span><span class="sxs-lookup"><span data-stu-id="298c4-216">Expressions can be joined with conditional operators:</span></span>

| <span data-ttu-id="298c4-217">Opérateur</span><span class="sxs-lookup"><span data-stu-id="298c4-217">Operator</span></span>            | <span data-ttu-id="298c4-218">Fonction</span><span class="sxs-lookup"><span data-stu-id="298c4-218">Function</span></span> |
| ------------------- | -------- |
| <code>&#124;</code> | <span data-ttu-id="298c4-219">OU</span><span class="sxs-lookup"><span data-stu-id="298c4-219">OR</span></span>       |
| `&`                 | <span data-ttu-id="298c4-220">AND</span><span class="sxs-lookup"><span data-stu-id="298c4-220">AND</span></span>      |

<span data-ttu-id="298c4-221">Vous pouvez mettre des expressions entre parenthèses quand vous utilisez des opérateurs conditionnels (par exemple, `(Name~TestMethod1) | (Name~TestMethod2)`).</span><span class="sxs-lookup"><span data-stu-id="298c4-221">You can enclose expressions in parenthesis when using conditional operators (for example, `(Name~TestMethod1) | (Name~TestMethod2)`).</span></span>

<span data-ttu-id="298c4-222">Pour plus d’informations et des exemples sur la façon d’utiliser le filtrage de test unitaire sélectif, consultez [Exécution de tests unitaires sélectifs](../testing/selective-unit-tests.md).</span><span class="sxs-lookup"><span data-stu-id="298c4-222">For more information and examples on how to use selective unit test filtering, see [Running selective unit tests](../testing/selective-unit-tests.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="298c4-223">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="298c4-223">See also</span></span>

* [<span data-ttu-id="298c4-224">Frameworks et cibles</span><span class="sxs-lookup"><span data-stu-id="298c4-224">Frameworks and Targets</span></span>](../../standard/frameworks.md)  
* [<span data-ttu-id="298c4-225">Catalogue d’identificateurs de runtime (RID) .NET Core</span><span class="sxs-lookup"><span data-stu-id="298c4-225">.NET Core Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
