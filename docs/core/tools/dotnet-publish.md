---
title: Commande dotnet publish - Interface CLI .NET Core
description: La commande dotnet publish publie votre projet .NET Core dans un répertoire.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: 38224aa8472f99df107e523667e18892384a20b0
ms.sourcegitcommit: f6343b070f3c66877338a05c8bfb0be9985255e2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2018
ms.locfileid: "39220670"
---
# <a name="dotnet-publish"></a><span data-ttu-id="768df-103">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="768df-103">dotnet publish</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="768df-104">Name</span><span class="sxs-lookup"><span data-stu-id="768df-104">Name</span></span>

<span data-ttu-id="768df-105">`dotnet publish` - Empaquette l’application et ses dépendances dans un dossier en vue d’un déploiement sur un système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="768df-105">`dotnet publish` - Packs the application and its dependencies into a folder for deployment to a hosting system.</span></span>

## <a name="synopsis"></a><span data-ttu-id="768df-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="768df-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="768df-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="768df-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet publish [<PROJECT>] [-c|--configuration] [-f|--framework] [--force] [--manifest] [--no-build] [--no-dependencies]
    [--no-restore] [-o|--output] [-r|--runtime] [--self-contained] [-v|--verbosity] [--version-suffix]
dotnet publish [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="768df-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="768df-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet publish [<PROJECT>] [-c|--configuration] [-f|--framework] [--force] [--manifest] [--no-dependencies]
    [--no-restore] [-o|--output] [-r|--runtime] [--self-contained] [-v|--verbosity] [--version-suffix]
dotnet publish [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="768df-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="768df-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet publish [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
    [--version-suffix]
dotnet publish [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="768df-110">Description</span><span class="sxs-lookup"><span data-stu-id="768df-110">Description</span></span>

<span data-ttu-id="768df-111">`dotnet publish` compile l’application, parcourt ses dépendances spécifiées dans le fichier projet et publie l’ensemble de fichiers obtenus dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="768df-111">`dotnet publish` compiles the application, reads through its dependencies specified in the project file, and publishes the resulting set of files to a directory.</span></span> <span data-ttu-id="768df-112">La sortie inclut les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="768df-112">The output includes the following assets:</span></span>

* <span data-ttu-id="768df-113">Le code de langage intermédiaire (IL) dans un assembly avec l’extension *dll*.</span><span class="sxs-lookup"><span data-stu-id="768df-113">Intermediate Language (IL) code in an assembly with a *dll* extension.</span></span>
* <span data-ttu-id="768df-114">Le fichier *.deps.json* qui inclut toutes les dépendances du projet.</span><span class="sxs-lookup"><span data-stu-id="768df-114">*.deps.json* file that includes all of the dependencies of the project.</span></span>
* <span data-ttu-id="768df-115">Le fichier *.runtime.config.json* qui spécifie le runtime partagé attendu par l’application, ainsi que d’autres options de configuration pour le runtime (par exemple, le type de garbage collection).</span><span class="sxs-lookup"><span data-stu-id="768df-115">*.runtime.config.json* file that specifies the shared runtime that the application expects, as well as other configuration options for the runtime (for example, garbage collection type).</span></span>
* <span data-ttu-id="768df-116">Les dépendances de l’application, qui sont copiées à partir du cache NuGet dans le dossier de sortie.</span><span class="sxs-lookup"><span data-stu-id="768df-116">The application's dependencies, which are copied from the NuGet cache into the output folder.</span></span>

<span data-ttu-id="768df-117">La sortie de la commande `dotnet publish` est prête pour le déploiement sur un système d’hébergement (par exemple, un serveur, PC, Mac, ordinateur portable) à des fins d’exécution.</span><span class="sxs-lookup"><span data-stu-id="768df-117">The `dotnet publish` command's output is ready for deployment to a hosting system (for example, a server, PC, Mac, laptop) for execution.</span></span> <span data-ttu-id="768df-118">Il s’agit de la seule façon officiellement prise en charge pour préparer l’application au déploiement.</span><span class="sxs-lookup"><span data-stu-id="768df-118">It's the only officially supported way to prepare the application for deployment.</span></span> <span data-ttu-id="768df-119">En fonction du type de déploiement que spécifie le projet, le runtime .NET Core partagé peut ou non être installé sur le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="768df-119">Depending on the type of deployment that the project specifies, the hosting system may or may not have the .NET Core shared runtime installed on it.</span></span> <span data-ttu-id="768df-120">Pour plus d’informations, consultez la page [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="768df-120">For more information, see [.NET Core Application Deployment](../deploying/index.md).</span></span> <span data-ttu-id="768df-121">Pour connaître la structure des répertoires d’une application publiée, consultez la page [Structure de répertoires](/aspnet/core/hosting/directory-structure).</span><span class="sxs-lookup"><span data-stu-id="768df-121">For the directory structure of a published application, see [Directory structure](/aspnet/core/hosting/directory-structure).</span></span>

[!INCLUDE[dotnet restore note + options](~/includes/dotnet-restore-note-options.md)]

## <a name="arguments"></a><span data-ttu-id="768df-122">Arguments</span><span class="sxs-lookup"><span data-stu-id="768df-122">Arguments</span></span>

`PROJECT`

<span data-ttu-id="768df-123">Projet à publier.</span><span class="sxs-lookup"><span data-stu-id="768df-123">The project to publish.</span></span> <span data-ttu-id="768df-124">Si aucune valeur n’est spécifiée, le répertoire actif est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="768df-124">If not specified, it defaults to the current directory.</span></span>

## <a name="options"></a><span data-ttu-id="768df-125">Options</span><span class="sxs-lookup"><span data-stu-id="768df-125">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="768df-126">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="768df-126">.NET Core 2.1</span></span>](#tab/netcore21)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="768df-127">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="768df-127">Defines the build configuration.</span></span> <span data-ttu-id="768df-128">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="768df-128">The default value is `Debug`.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="768df-129">Publie l’application pour le [framework cible](../../standard/frameworks.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="768df-129">Publishes the application for the specified [target framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="768df-130">Le framework cible doit être spécifié dans le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="768df-130">You must specify the target framework in the project file.</span></span>

`--force`

<span data-ttu-id="768df-131">Force la résolution de toutes les dépendances même si la dernière restauration a réussi.</span><span class="sxs-lookup"><span data-stu-id="768df-131">Forces all dependencies to be resolved even if the last restore was successful.</span></span> <span data-ttu-id="768df-132">Définir cet indicateur revient à supprimer le fichier *project.assets.json*.</span><span class="sxs-lookup"><span data-stu-id="768df-132">Specifying this flag is the same as deleting the *project.assets.json* file.</span></span>

`-h|--help`

<span data-ttu-id="768df-133">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-133">Prints out a short help for the command.</span></span>

`--manifest <PATH_TO_MANIFEST_FILE>`

<span data-ttu-id="768df-134">Spécifie un ou plusieurs [manifestes cibles](../deploying/runtime-store.md) à utiliser pour épurer l’ensemble des packages publiés avec l’application.</span><span class="sxs-lookup"><span data-stu-id="768df-134">Specifies one or several [target manifests](../deploying/runtime-store.md) to use to trim the set of packages published with the app.</span></span> <span data-ttu-id="768df-135">Le fichier manifeste fait partie de la sortie de la [commande `dotnet store`](dotnet-store.md).</span><span class="sxs-lookup"><span data-stu-id="768df-135">The manifest file is part of the output of the [`dotnet store` command](dotnet-store.md).</span></span> <span data-ttu-id="768df-136">Pour spécifier plusieurs manifestes, ajoutez une option `--manifest` pour chaque manifeste.</span><span class="sxs-lookup"><span data-stu-id="768df-136">To specify multiple manifests, add a `--manifest` option for each manifest.</span></span> <span data-ttu-id="768df-137">Cette option est disponible à partir du SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="768df-137">This option is available starting with .NET Core 2.0 SDK.</span></span>

`--no-build`

<span data-ttu-id="768df-138">Ne génère pas le projet avant la publication.</span><span class="sxs-lookup"><span data-stu-id="768df-138">Doesn't build the project before publishing.</span></span> <span data-ttu-id="768df-139">L’indicateur `--no-restore` est également défini implicitement.</span><span class="sxs-lookup"><span data-stu-id="768df-139">It also implicit sets the `--no-restore` flag.</span></span>

`--no-dependencies`

<span data-ttu-id="768df-140">Ignore les références entre projets et restaure uniquement le projet racine.</span><span class="sxs-lookup"><span data-stu-id="768df-140">Ignores project-to-project references and only restores the root project.</span></span>

`--no-restore`

<span data-ttu-id="768df-141">N’effectue pas de restauration implicite à l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-141">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="768df-142">Spécifie le chemin d’accès du répertoire de sortie.</span><span class="sxs-lookup"><span data-stu-id="768df-142">Specifies the path for the output directory.</span></span> <span data-ttu-id="768df-143">Si aucune valeur n’est spécifiée, il s’agit par défaut de *./bin/[configuration]/[framework]/publish/* pour un déploiement dépendant du framework ou de *./bin/[configuration]/[framework]/[runtime]/publish/* pour un déploiement autonome.</span><span class="sxs-lookup"><span data-stu-id="768df-143">If not specified, it defaults to *./bin/[configuration]/[framework]/publish/* for a framework-dependent deployment or *./bin/[configuration]/[framework]/[runtime]/publish/* for a self-contained deployment.</span></span>
<span data-ttu-id="768df-144">Si le chemin est relatif, le répertoire de sortie généré est relatif à l’emplacement du fichier projet, et non au répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="768df-144">If the path is relative, the output directory generated is relative to the project file location, not to the current working directory.</span></span>

`--self-contained`

<span data-ttu-id="768df-145">Publie le runtime .NET Core avec votre application ; ainsi, vous n’avez pas besoin d’installer le runtime sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="768df-145">Publishes the .NET Core runtime with your application so the runtime doesn't need to be installed on the target machine.</span></span> <span data-ttu-id="768df-146">Si un identificateur de runtime est spécifié, sa valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="768df-146">If a runtime identifier is specified, its default value is `true`.</span></span> <span data-ttu-id="768df-147">Pour plus d’informations sur les différents types de déploiement, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="768df-147">For more information about the different deployment types, see [.NET Core application deployment](../deploying/index.md).</span></span>

`-r|--runtime <RUNTIME_IDENTIFIER>`

<span data-ttu-id="768df-148">Publie l’application pour un runtime donné.</span><span class="sxs-lookup"><span data-stu-id="768df-148">Publishes the application for a given runtime.</span></span> <span data-ttu-id="768df-149">Cette option est utilisée pour créer un [déploiement autonome (SCD)](../deploying/index.md#self-contained-deployments-scd).</span><span class="sxs-lookup"><span data-stu-id="768df-149">This is used when creating a [self-contained deployment (SCD)](../deploying/index.md#self-contained-deployments-scd).</span></span> <span data-ttu-id="768df-150">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="768df-150">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span> <span data-ttu-id="768df-151">Par défaut, vous publiez un [déploiement dépendant du framework (FDD)](../deploying/index.md#framework-dependent-deployments-fdd).</span><span class="sxs-lookup"><span data-stu-id="768df-151">Default is to publish a [framework-dependent deployment (FDD)](../deploying/index.md#framework-dependent-deployments-fdd).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="768df-152">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-152">Sets the verbosity level of the command.</span></span> <span data-ttu-id="768df-153">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="768df-153">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version-suffix <VERSION_SUFFIX>`

<span data-ttu-id="768df-154">Définit le suffixe de version qui remplace l’astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="768df-154">Defines the version suffix to replace the asterisk (`*`) in the version field of the project file.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="768df-155">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="768df-155">.NET Core 2.0</span></span>](#tab/netcore20)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="768df-156">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="768df-156">Defines the build configuration.</span></span> <span data-ttu-id="768df-157">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="768df-157">The default value is `Debug`.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="768df-158">Publie l’application pour le [framework cible](../../standard/frameworks.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="768df-158">Publishes the application for the specified [target framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="768df-159">Le framework cible doit être spécifié dans le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="768df-159">You must specify the target framework in the project file.</span></span>

`--force`

<span data-ttu-id="768df-160">Force la résolution de toutes les dépendances même si la dernière restauration a réussi.</span><span class="sxs-lookup"><span data-stu-id="768df-160">Forces all dependencies to be resolved even if the last restore was successful.</span></span> <span data-ttu-id="768df-161">Définir cet indicateur revient à supprimer le fichier *project.assets.json*.</span><span class="sxs-lookup"><span data-stu-id="768df-161">Specifying this flag is the same as deleting the *project.assets.json* file.</span></span>

`-h|--help`

<span data-ttu-id="768df-162">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-162">Prints out a short help for the command.</span></span>

`--manifest <PATH_TO_MANIFEST_FILE>`

<span data-ttu-id="768df-163">Spécifie un ou plusieurs [manifestes cibles](../deploying/runtime-store.md) à utiliser pour épurer l’ensemble des packages publiés avec l’application.</span><span class="sxs-lookup"><span data-stu-id="768df-163">Specifies one or several [target manifests](../deploying/runtime-store.md) to use to trim the set of packages published with the app.</span></span> <span data-ttu-id="768df-164">Le fichier manifeste fait partie de la sortie de la [commande `dotnet store`](dotnet-store.md).</span><span class="sxs-lookup"><span data-stu-id="768df-164">The manifest file is part of the output of the [`dotnet store` command](dotnet-store.md).</span></span> <span data-ttu-id="768df-165">Pour spécifier plusieurs manifestes, ajoutez une option `--manifest` pour chaque manifeste.</span><span class="sxs-lookup"><span data-stu-id="768df-165">To specify multiple manifests, add a `--manifest` option for each manifest.</span></span> <span data-ttu-id="768df-166">Cette option est disponible à partir du SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="768df-166">This option is available starting with .NET Core 2.0 SDK.</span></span>

`--no-dependencies`

<span data-ttu-id="768df-167">Ignore les références entre projets et restaure uniquement le projet racine.</span><span class="sxs-lookup"><span data-stu-id="768df-167">Ignores project-to-project references and only restores the root project.</span></span>

`--no-restore`

<span data-ttu-id="768df-168">N’effectue pas de restauration implicite à l’exécution de la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-168">Doesn't execute an implicit restore when running the command.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="768df-169">Spécifie le chemin d’accès du répertoire de sortie.</span><span class="sxs-lookup"><span data-stu-id="768df-169">Specifies the path for the output directory.</span></span> <span data-ttu-id="768df-170">Si aucune valeur n’est spécifiée, il s’agit par défaut de *./bin/[configuration]/[framework]/publish/* pour un déploiement dépendant du framework ou de *./bin/[configuration]/[framework]/[runtime]/publish/* pour un déploiement autonome.</span><span class="sxs-lookup"><span data-stu-id="768df-170">If not specified, it defaults to *./bin/[configuration]/[framework]/publish/* for a framework-dependent deployment or *./bin/[configuration]/[framework]/[runtime]/publish/* for a self-contained deployment.</span></span>
<span data-ttu-id="768df-171">Si le chemin est relatif, le répertoire de sortie généré est relatif à l’emplacement du fichier projet, et non au répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="768df-171">If the path is relative, the output directory generated is relative to the project file location, not to the current working directory.</span></span>

`--self-contained`

<span data-ttu-id="768df-172">Publie le runtime .NET Core avec votre application ; ainsi, vous n’avez pas besoin d’installer le runtime sur l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="768df-172">Publishes the .NET Core runtime with your application so the runtime doesn't need to be installed on the target machine.</span></span> <span data-ttu-id="768df-173">Si un identificateur de runtime est spécifié, sa valeur par défaut est `true`.</span><span class="sxs-lookup"><span data-stu-id="768df-173">If a runtime identifier is specified, its default value is `true`.</span></span> <span data-ttu-id="768df-174">Pour plus d’informations sur les différents types de déploiement, consultez [Déploiement d’applications .NET Core](../deploying/index.md).</span><span class="sxs-lookup"><span data-stu-id="768df-174">For more information about the different deployment types, see [.NET Core application deployment](../deploying/index.md).</span></span>

`-r|--runtime <RUNTIME_IDENTIFIER>`

<span data-ttu-id="768df-175">Publie l’application pour un runtime donné.</span><span class="sxs-lookup"><span data-stu-id="768df-175">Publishes the application for a given runtime.</span></span> <span data-ttu-id="768df-176">Cette option est utilisée pour créer un [déploiement autonome (SCD)](../deploying/index.md#self-contained-deployments-scd).</span><span class="sxs-lookup"><span data-stu-id="768df-176">This is used when creating a [self-contained deployment (SCD)](../deploying/index.md#self-contained-deployments-scd).</span></span> <span data-ttu-id="768df-177">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="768df-177">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span> <span data-ttu-id="768df-178">Par défaut, vous publiez un [déploiement dépendant du framework (FDD)](../deploying/index.md#framework-dependent-deployments-fdd).</span><span class="sxs-lookup"><span data-stu-id="768df-178">Default is to publish a [framework-dependent deployment (FDD)](../deploying/index.md#framework-dependent-deployments-fdd).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="768df-179">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-179">Sets the verbosity level of the command.</span></span> <span data-ttu-id="768df-180">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="768df-180">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version-suffix <VERSION_SUFFIX>`

<span data-ttu-id="768df-181">Définit le suffixe de version qui remplace l’astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="768df-181">Defines the version suffix to replace the asterisk (`*`) in the version field of the project file.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="768df-182">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="768df-182">.NET Core 1.x</span></span>](#tab/netcore1x)

`-c|--configuration {Debug|Release}`

<span data-ttu-id="768df-183">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="768df-183">Defines the build configuration.</span></span> <span data-ttu-id="768df-184">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="768df-184">The default value is `Debug`.</span></span>

`-f|--framework <FRAMEWORK>`

<span data-ttu-id="768df-185">Publie l’application pour le [framework cible](../../standard/frameworks.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="768df-185">Publishes the application for the specified [target framework](../../standard/frameworks.md).</span></span> <span data-ttu-id="768df-186">Le framework cible doit être spécifié dans le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="768df-186">You must specify the target framework in the project file.</span></span>

`-h|--help`

<span data-ttu-id="768df-187">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-187">Prints out a short help for the command.</span></span>

`--manifest <PATH_TO_MANIFEST_FILE>`

<span data-ttu-id="768df-188">Spécifie un ou plusieurs [manifestes cibles](../deploying/runtime-store.md) à utiliser pour épurer l’ensemble des packages publiés avec l’application.</span><span class="sxs-lookup"><span data-stu-id="768df-188">Specifies one or several [target manifests](../deploying/runtime-store.md) to use to trim the set of packages published with the app.</span></span> <span data-ttu-id="768df-189">Le fichier manifeste fait partie de la sortie de la [commande `dotnet store`](dotnet-store.md).</span><span class="sxs-lookup"><span data-stu-id="768df-189">The manifest file is part of the output of the [`dotnet store` command](dotnet-store.md).</span></span> <span data-ttu-id="768df-190">Pour spécifier plusieurs manifestes, ajoutez une option `--manifest` pour chaque manifeste.</span><span class="sxs-lookup"><span data-stu-id="768df-190">To specify multiple manifests, add a `--manifest` option for each manifest.</span></span> <span data-ttu-id="768df-191">Cette option est disponible à partir du SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="768df-191">This option is available starting with .NET Core 2.0 SDK.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="768df-192">Spécifie le chemin d’accès du répertoire de sortie.</span><span class="sxs-lookup"><span data-stu-id="768df-192">Specifies the path for the output directory.</span></span> <span data-ttu-id="768df-193">Si aucune valeur n’est spécifiée, il s’agit par défaut de *./bin/[configuration]/[framework]/publish/* pour un déploiement dépendant du framework ou de *./bin/[configuration]/[framework]/[runtime]/publish/* pour un déploiement autonome.</span><span class="sxs-lookup"><span data-stu-id="768df-193">If not specified, it defaults to *./bin/[configuration]/[framework]/publish/* for a framework-dependent deployment or *./bin/[configuration]/[framework]/[runtime]/publish/* for a self-contained deployment.</span></span>
<span data-ttu-id="768df-194">Si le chemin est relatif, le répertoire de sortie généré est relatif à l’emplacement du fichier projet, et non au répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="768df-194">If the path is relative, the output directory generated is relative to the project file location, not to the current working directory.</span></span>

`-r|--runtime <RUNTIME_IDENTIFIER>`

<span data-ttu-id="768df-195">Publie l’application pour un runtime donné.</span><span class="sxs-lookup"><span data-stu-id="768df-195">Publishes the application for a given runtime.</span></span> <span data-ttu-id="768df-196">Cette option est utilisée pour créer un [déploiement autonome (SCD)](../deploying/index.md#self-contained-deployments-scd).</span><span class="sxs-lookup"><span data-stu-id="768df-196">This is used when creating a [self-contained deployment (SCD)](../deploying/index.md#self-contained-deployments-scd).</span></span> <span data-ttu-id="768df-197">Pour connaître les identificateurs de runtime, consultez le [catalogue des identificateurs de runtime](../rid-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="768df-197">For a list of Runtime Identifiers (RIDs), see the [RID catalog](../rid-catalog.md).</span></span> <span data-ttu-id="768df-198">Par défaut, vous publiez un [déploiement dépendant du framework (FDD)](../deploying/index.md#framework-dependent-deployments-fdd).</span><span class="sxs-lookup"><span data-stu-id="768df-198">Default is to publish a [framework-dependent deployment (FDD)](../deploying/index.md#framework-dependent-deployments-fdd).</span></span>

`-v|--verbosity <LEVEL>`

<span data-ttu-id="768df-199">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="768df-199">Sets the verbosity level of the command.</span></span> <span data-ttu-id="768df-200">Les valeurs autorisées sont `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]` et `diag[nostic]`.</span><span class="sxs-lookup"><span data-stu-id="768df-200">Allowed values are `q[uiet]`, `m[inimal]`, `n[ormal]`, `d[etailed]`, and `diag[nostic]`.</span></span>

`--version-suffix <VERSION_SUFFIX>`

<span data-ttu-id="768df-201">Définit le suffixe de version qui remplace l’astérisque (`*`) dans le champ de version du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="768df-201">Defines the version suffix to replace the asterisk (`*`) in the version field of the project file.</span></span>

---

## <a name="examples"></a><span data-ttu-id="768df-202">Exemples</span><span class="sxs-lookup"><span data-stu-id="768df-202">Examples</span></span>

<span data-ttu-id="768df-203">Publier le projet dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="768df-203">Publish the project in the current directory:</span></span>

`dotnet publish`

<span data-ttu-id="768df-204">Publier l’application à l’aide du fichier projet spécifié :</span><span class="sxs-lookup"><span data-stu-id="768df-204">Publish the application using the specified project file:</span></span>

`dotnet publish ~/projects/app1/app1.csproj`

<span data-ttu-id="768df-205">Publier le projet dans le répertoire actif à l’aide du framework `netcoreapp1.1` :</span><span class="sxs-lookup"><span data-stu-id="768df-205">Publish the project in the current directory using the `netcoreapp1.1` framework:</span></span>

`dotnet publish --framework netcoreapp1.1`

<span data-ttu-id="768df-206">Publier l’application actuelle à l’aide du framework `netcoreapp1.1` et du runtime pour `OS X 10.10` (vous devez lister cet identificateur de runtime dans le fichier projet) :</span><span class="sxs-lookup"><span data-stu-id="768df-206">Publish the current application using the `netcoreapp1.1` framework and the runtime for `OS X 10.10` (you must list this RID in the project file).</span></span>

`dotnet publish --framework netcoreapp1.1 --runtime osx.10.11-x64`

<span data-ttu-id="768df-207">Publier l’application actuelle, mais ne pas restaurer les références de projet à projet (P2P), seulement le projet racine durant l’opération de restauration (SDK .NET Core 2.0 et ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="768df-207">Publish the current application but don't restore project-to-project (P2P) references, just the root project during the restore operation (.NET Core SDK 2.0 and later versions):</span></span>

`dotnet publish --no-dependencies`

## <a name="see-also"></a><span data-ttu-id="768df-208">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="768df-208">See also</span></span>

* [<span data-ttu-id="768df-209">Frameworks cibles</span><span class="sxs-lookup"><span data-stu-id="768df-209">Target frameworks</span></span>](../../standard/frameworks.md)
* [<span data-ttu-id="768df-210">Catalogue d’identificateurs de runtime (RID)</span><span class="sxs-lookup"><span data-stu-id="768df-210">Runtime IDentifier (RID) catalog</span></span>](../rid-catalog.md)
