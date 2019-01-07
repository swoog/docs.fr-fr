---
title: Commande dotnet build
description: La commande dotnet build permet de générer un projet et l’ensemble de ses dépendances.
ms.date: 12/04/2018
ms.openlocfilehash: 1e5e05d51f98394b2b77e3a8fc645cf9712b0a0f
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169692"
---
# <a name="dotnet-build"></a><span data-ttu-id="4a8ec-103">dotnet build</span><span class="sxs-lookup"><span data-stu-id="4a8ec-103">dotnet build</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="4a8ec-104">Name</span><span class="sxs-lookup"><span data-stu-id="4a8ec-104">Name</span></span>

<span data-ttu-id="4a8ec-105">`dotnet build` : Génère un projet et l’ensemble de ses dépendances.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-105">`dotnet build` - Builds a project and all of its dependencies.</span></span>

## <a name="synopsis"></a><span data-ttu-id="4a8ec-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="4a8ec-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="4a8ec-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="4a8ec-107">.NET Core 2.x</span></span>](#tab/netcore2x)
```
dotnet build [<PROJECT>|<SOLUTION>] [-c|--configuration] [-f|--framework] [--force] [--no-dependencies] [--no-incremental]
    [--no-restore] [-o|--output] [-r|--runtime] [-v|--verbosity] [--version-suffix]

dotnet build [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4a8ec-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4a8ec-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet build [<PROJECT>|<SOLUTION>] [-c|--configuration] [-f|--framework] [--no-dependencies] [--no-incremental] [-o|--output]
    [-r|--runtime] [-v|--verbosity] [--version-suffix]

dotnet build [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="4a8ec-109">Description</span><span class="sxs-lookup"><span data-stu-id="4a8ec-109">Description</span></span>

<span data-ttu-id="4a8ec-110">La commande `dotnet build` génère le projet et ses dépendances dans un ensemble de fichiers binaires.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-110">The `dotnet build` command builds the project and its dependencies into a set of binaries.</span></span> <span data-ttu-id="4a8ec-111">Les fichiers binaires incluent le code du projet dans des fichiers en langage intermédiaire (IL) avec une extension *.dll* et les fichiers de symboles utilisés pour le débogage avec une extension *.pdb*.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-111">The binaries include the project's code in Intermediate Language (IL) files with a *.dll* extension and symbol files used for debugging with a *.pdb* extension.</span></span> <span data-ttu-id="4a8ec-112">Un fichier JSON de dépendances (*\*.deps.json*) est généré. Il répertorie les dépendances de l’application.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-112">A dependencies JSON file (*\*.deps.json*) is produced that lists the dependencies of the application.</span></span> <span data-ttu-id="4a8ec-113">Un fichier *\*.runtimeconfig.json* est généré. Il spécifie le runtime partagé et sa version pour l’application.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-113">A *\*.runtimeconfig.json* file is produced, which specifies the shared runtime and its version for the application.</span></span>

<span data-ttu-id="4a8ec-114">Si le projet a des dépendances tierces, comme des bibliothèques NuGet, elles sont résolues à partir du cache NuGet et ne sont pas disponibles avec la sortie générée du projet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-114">If the project has third-party dependencies, such as libraries from NuGet, they're resolved from the NuGet cache and aren't available with the project's built output.</span></span> <span data-ttu-id="4a8ec-115">Par conséquent, le produit de `dotnet build` ne peut pas être transféré en l’état vers un autre ordinateur pour exécution.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-115">With that in mind, the product of `dotnet build` isn't ready to be transferred to another machine to run.</span></span> <span data-ttu-id="4a8ec-116">Ce comportement contraste avec celui du .NET Framework dans lequel la génération d’un projet exécutable (une application) produit une sortie exécutable sur n’importe quel ordinateur où le .NET Framework est installé.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-116">This is in contrast to the behavior of the .NET Framework in which building an executable project (an application) produces output that's runnable on any machine where the .NET Framework is installed.</span></span> <span data-ttu-id="4a8ec-117">Pour obtenir un résultat similaire dans .NET Core, vous devez utiliser la commande [dotnet publish](dotnet-publish.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-117">To have a similar experience with .NET Core, you need to use the [dotnet publish](dotnet-publish.md) command.</span></span> <span data-ttu-id="4a8ec-118">Pour plus d’informations, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-118">For more information, see [.NET Core Application Deployment](../deploying/index.md).</span></span>

<span data-ttu-id="4a8ec-119">La génération requiert le fichier *project.assets.json* qui répertorie les dépendances de votre application.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-119">Building requires the *project.assets.json* file, which lists the dependencies of your application.</span></span> <span data-ttu-id="4a8ec-120">Le fichier est créé quand la commande [`dotnet restore`](dotnet-restore.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-120">The file is created when [`dotnet restore`](dotnet-restore.md) is executed.</span></span> <span data-ttu-id="4a8ec-121">Si le fichier de ressources est absent, les outils ne peuvent pas résoudre les assemblys de référence, ce qui entraîne des erreurs.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-121">Without the assets file in place, the tooling cannot resolve reference assemblies, which results in errors.</span></span> <span data-ttu-id="4a8ec-122">Avec le SDK .NET Core 1.x, vous deviez explicitement exécuter `dotnet restore` avant d’exécuter `dotnet build`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-122">With .NET Core 1.x SDK, you needed to explicitly run the `dotnet restore` before running `dotnet build`.</span></span> <span data-ttu-id="4a8ec-123">À compter du SDK .NET Core 2.0, `dotnet restore` s’exécute implicitement quand vous exécutez `dotnet build`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-123">Starting with .NET Core 2.0 SDK, `dotnet restore` runs implicitly when you run `dotnet build`.</span></span> <span data-ttu-id="4a8ec-124">Si vous souhaitez désactiver la restauration implicite au moment d’exécuter la commande de génération, vous pouvez passer l’option `--no-restore`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-124">If you want to disable implicit restore when running the build command, you can pass the `--no-restore` option.</span></span>

[!INCLUDE[dotnet restore note + options](~/includes/dotnet-restore-note-options.md)]

<span data-ttu-id="4a8ec-125">La possibilité d’exécuter le projet ou non est déterminée par la propriété `<OutputType>` dans le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-125">Whether the project is executable or not is determined by the `<OutputType>` property in the project file.</span></span> <span data-ttu-id="4a8ec-126">L’exemple suivant illustre un projet qui génère du code exécutable :</span><span class="sxs-lookup"><span data-stu-id="4a8ec-126">The following example shows a project that produces executable code:</span></span>

```xml
<PropertyGroup>
  <OutputType>Exe</OutputType>
</PropertyGroup>
```

<span data-ttu-id="4a8ec-127">Pour générer une bibliothèque, omettez la propriété `<OutputType>`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-127">In order to produce a library, omit the `<OutputType>` property.</span></span> <span data-ttu-id="4a8ec-128">La principale différence dans la sortie générée est que la DLL de langage intermédiaire pour une bibliothèque ne contient pas de points d’entrée et ne peut pas être exécutée.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-128">The main difference in built output is that the IL DLL for a library doesn't contain entry points and can't be executed.</span></span>

### <a name="msbuild"></a><span data-ttu-id="4a8ec-129">MSBuild</span><span class="sxs-lookup"><span data-stu-id="4a8ec-129">MSBuild</span></span>

<span data-ttu-id="4a8ec-130">La commande `dotnet build` utilise MSBuild pour générer le projet. Elle prend donc en charge les builds parallèles et les builds incrémentielles.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-130">`dotnet build` uses MSBuild to build the project, so it supports both parallel and incremental builds.</span></span> <span data-ttu-id="4a8ec-131">Pour plus d’informations, consultez l’article [Incremental Builds (Générations incrémentielles)](/visualstudio/msbuild/incremental-builds) .</span><span class="sxs-lookup"><span data-stu-id="4a8ec-131">For more information, see [Incremental Builds](/visualstudio/msbuild/incremental-builds).</span></span>

<span data-ttu-id="4a8ec-132">En plus de ses options, la commande `dotnet build` accepte des options MSBuild, comme `-p` pour définir des propriétés ou `-l` pour définir un enregistreur d’événements.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-132">In addition to its options, the `dotnet build` command accepts MSBuild options, such as `-p` for setting properties or `-l` to define a logger.</span></span> <span data-ttu-id="4a8ec-133">Pour plus d’informations sur ces options, consultez [Informations de référence sur la ligne de commande MSBuild](/visualstudio/msbuild/msbuild-command-line-reference).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-133">For more information about these options, see the [MSBuild Command-Line Reference](/visualstudio/msbuild/msbuild-command-line-reference).</span></span> <span data-ttu-id="4a8ec-134">Ou vous pouvez également utiliser la commande [dotnet msbuild](dotnet-msbuild.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-134">Or you can also use the [dotnet msbuild](dotnet-msbuild.md) command.</span></span>

<span data-ttu-id="4a8ec-135">L’exécution de `dotnet msbuild -restore -target:Build` équivaut à `dotnet build`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-135">Running `dotnet build` is equivalent to `dotnet msbuild -restore -target:Build`.</span></span>

## <a name="arguments"></a><span data-ttu-id="4a8ec-136">Arguments</span><span class="sxs-lookup"><span data-stu-id="4a8ec-136">Arguments</span></span>

`PROJECT | SOLUTION`

<span data-ttu-id="4a8ec-137">Le fichier projet ou solution à générer.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-137">The project or solution file to build.</span></span> <span data-ttu-id="4a8ec-138">Si vous ne spécifiez pas de fichier projet ou solution, MSBuild recherche dans le répertoire de travail actif un fichier dont l’extension se termine par *proj* ou *sln* et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-138">If a project or solution file is not specified, MSBuild searches the current working directory for a file that has a file extension that ends in either *proj* or *sln* and uses that file.</span></span>

## <a name="options"></a><span data-ttu-id="4a8ec-139">Options</span><span class="sxs-lookup"><span data-stu-id="4a8ec-139">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="4a8ec-140">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="4a8ec-140">.NET Core 2.x</span></span>](#tab/netcore2x)

* **`-c|--configuration {Debug|Release}`**

  <span data-ttu-id="4a8ec-141">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-141">Defines the build configuration.</span></span> <span data-ttu-id="4a8ec-142">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-142">The default value is `Debug`.</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="4a8ec-143">Compile pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-143">Compiles for a specific [framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="4a8ec-144">Le framework doit être défini dans le [fichier projet](csproj.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-144">The framework must be defined in the [project file](csproj.md).</span></span>

* **`--force`**

  <span data-ttu-id="4a8ec-145">Force la résolution de toutes les dépendances même si la dernière restauration a réussi.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-145">Forces all dependencies to be resolved even if the last restore was successful.</span></span> <span data-ttu-id="4a8ec-146">Définir cet indicateur revient à supprimer le fichier *project.assets.json*.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-146">Specifying this flag is the same as deleting the *project.assets.json* file.</span></span>

* **`-h|--help`**

  <span data-ttu-id="4a8ec-147">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-147">Prints out a short help for the command.</span></span>

* **`--no-dependencies`**

  <span data-ttu-id="4a8ec-148">Ignore les références entre projets (P2P) et génère uniquement le projet racine spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-148">Ignores project-to-project (P2P) references and only builds the specified root project.</span></span>

* **`--no-incremental`**

  <span data-ttu-id="4a8ec-149">Marque la build comme unsafe pour la génération incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-149">Marks the build as unsafe for incremental build.</span></span> <span data-ttu-id="4a8ec-150">Cet indicateur désactive la compilation incrémentielle et force une regénération du graphique de dépendance du projet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-150">This flag turns off incremental compilation and forces a clean rebuild of the project's dependency graph.</span></span>

* **`--no-restore`**

  <span data-ttu-id="4a8ec-151">N’exécute pas de restauration implicite pendant la génération.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-151">Doesn't execute an implicit restore during build.</span></span>

* **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="4a8ec-152">Répertoire dans lequel placer les fichiers binaires générés.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-152">Directory in which to place the built binaries.</span></span> <span data-ttu-id="4a8ec-153">Vous devez également définir `--framework` lorsque vous spécifiez cette option.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-153">You also need to define `--framework` when you specify this option.</span></span> <span data-ttu-id="4a8ec-154">S’il n’est pas spécifié, le chemin d'accès par défaut est `./bin/<configuration>/<framework>/`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-154">If not specified, the default path is `./bin/<configuration>/<framework>/`.</span></span>

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="4a8ec-155">Spécifie le runtime cible.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-155">Specifies the target runtime.</span></span> <span data-ttu-id="4a8ec-156">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-156">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span>

* **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="4a8ec-157">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-157">Sets the verbosity level of the command.</span></span> <span data-ttu-id="4a8ec-158">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-158">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

* **`--version-suffix <VERSION_SUFFIX>`**

  <span data-ttu-id="4a8ec-159">Définit le suffixe de version pour un astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-159">Defines the version suffix for an asterisk (`*`) in the version field of the project file.</span></span> <span data-ttu-id="4a8ec-160">Le format respecte les instructions de version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-160">The format follows NuGet's version guidelines.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="4a8ec-161">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="4a8ec-161">.NET Core 1.x</span></span>](#tab/netcore1x)

* **`-c|--configuration {Debug|Release}`**

  <span data-ttu-id="4a8ec-162">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-162">Defines the build configuration.</span></span> <span data-ttu-id="4a8ec-163">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-163">The default value is `Debug`.</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="4a8ec-164">Compile pour un [framework](../../standard/frameworks.md) spécifique.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-164">Compiles for a specific [framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="4a8ec-165">Le framework doit être défini dans le [fichier projet](csproj.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-165">The framework must be defined in the [project file](csproj.md).</span></span>

* **`-h|--help`**

  <span data-ttu-id="4a8ec-166">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-166">Prints out a short help for the command.</span></span>

* **`--no-dependencies`**

  <span data-ttu-id="4a8ec-167">Ignore les références entre projets (P2P) et génère uniquement le projet racine spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-167">Ignores project-to-project (P2P) references and only builds the specified root project.</span></span>

* **`--no-incremental`**

  <span data-ttu-id="4a8ec-168">Marque la build comme unsafe pour la génération incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-168">Marks the build as unsafe for incremental build.</span></span> <span data-ttu-id="4a8ec-169">Cet indicateur désactive la compilation incrémentielle et force une regénération du graphique de dépendance du projet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-169">This flag turns off incremental compilation and forces a clean rebuild of the project's dependency graph.</span></span>

* **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="4a8ec-170">Répertoire dans lequel placer les fichiers binaires générés.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-170">Directory in which to place the built binaries.</span></span> <span data-ttu-id="4a8ec-171">Vous devez également définir `--framework` lorsque vous spécifiez cette option.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-171">You also need to define `--framework` when you specify this option.</span></span>

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="4a8ec-172">Spécifie le runtime cible.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-172">Specifies the target runtime.</span></span> <span data-ttu-id="4a8ec-173">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="4a8ec-173">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span>

* **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="4a8ec-174">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-174">Sets the verbosity level of the command.</span></span> <span data-ttu-id="4a8ec-175">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-175">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

* **`--version-suffix <VERSION_SUFFIX>`**

  <span data-ttu-id="4a8ec-176">Définit le suffixe de version pour un astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-176">Defines the version suffix for an asterisk (`*`) in the version field of the project file.</span></span> <span data-ttu-id="4a8ec-177">Le format respecte les instructions de version de NuGet.</span><span class="sxs-lookup"><span data-stu-id="4a8ec-177">The format follows NuGet's version guidelines.</span></span>

---

## <a name="examples"></a><span data-ttu-id="4a8ec-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="4a8ec-178">Examples</span></span>

* <span data-ttu-id="4a8ec-179">Générer un projet et ses dépendances :</span><span class="sxs-lookup"><span data-stu-id="4a8ec-179">Build a project and its dependencies:</span></span>

  ```console
  dotnet build
  ```

* <span data-ttu-id="4a8ec-180">Générer un projet et ses dépendances à l’aide de la configuration Release :</span><span class="sxs-lookup"><span data-stu-id="4a8ec-180">Build a project and its dependencies using Release configuration:</span></span>

  ```console
  dotnet build --configuration Release
  ```

* <span data-ttu-id="4a8ec-181">Générer un projet et ses dépendances pour un runtime spécifique (dans cet exemple, Ubuntu 16.04) :</span><span class="sxs-lookup"><span data-stu-id="4a8ec-181">Build a project and its dependencies for a specific runtime (in this example, Ubuntu 16.04):</span></span>

  ```console
  dotnet build --runtime ubuntu.16.04-x64
  ```

* <span data-ttu-id="4a8ec-182">Générer le projet et utiliser la source de package NuGet spécifiée pendant l’opération de restauration (SDK .NET Core 2.0 et versions ultérieures) :</span><span class="sxs-lookup"><span data-stu-id="4a8ec-182">Build the project and use the specified NuGet package source during the restore operation (.NET Core 2.0 SDK and later versions):</span></span>

  ```console
  dotnet build --source c:\packages\mypackages
  ```

* <span data-ttu-id="4a8ec-183">Générer le projet et définir la version 1.2.3.4 comme paramètre de build :</span><span class="sxs-lookup"><span data-stu-id="4a8ec-183">Build the project and set 1.2.3.4 version as a build parameter:</span></span>

  ```console
  dotnet build -p:Version=1.2.3.4
  ```