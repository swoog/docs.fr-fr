---
title: Sélection de la version de .NET Core
description: Découvrez comment .NET Core recherche et choisit les versions du runtime pour votre programme.
author: billwagner
ms.author: wiwagn
ms.date: 06/27/2018
ms.openlocfilehash: d1b885ebbade4736d5f592d1dc1d4ba25a321a16
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37874468"
---
# <a name="net-core-version-selection"></a><span data-ttu-id="cd02e-103">Sélection de la version de .NET Core</span><span class="sxs-lookup"><span data-stu-id="cd02e-103">.NET Core version selection</span></span>

[!INCLUDE [topic-appliesto-net-core-2plus](../../../includes/topic-appliesto-net-core-2plus.md)]

<span data-ttu-id="cd02e-104">Cet article explique les stratégies utilisées par les outils .NET Core, le kit SDK et le runtime pour sélectionner les versions.</span><span class="sxs-lookup"><span data-stu-id="cd02e-104">This article explains the policies used by the .NET Core tools, SDK, and runtime for selecting versions.</span></span> <span data-ttu-id="cd02e-105">Ces stratégies concilient l’exécution des applications avec les versions spécifiées et la facilité de mise à niveau des machines des développeurs et des utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="cd02e-105">These policies provide a balance between running applications using the specified versions and enabling ease of upgrading both developer and end user machines.</span></span> <span data-ttu-id="cd02e-106">Voici les objectifs visés par ces stratégies :</span><span class="sxs-lookup"><span data-stu-id="cd02e-106">These policies perform the following:</span></span>

- <span data-ttu-id="cd02e-107">Déploiement facile et efficace de .NET Core, notamment des mises à jour de sécurité et de fiabilité.</span><span class="sxs-lookup"><span data-stu-id="cd02e-107">Easy and efficient deployment of .NET Core, including security and reliability updates.</span></span>
- <span data-ttu-id="cd02e-108">Utilisation des outils et des commandes les plus récents, indépendamment du runtime cible.</span><span class="sxs-lookup"><span data-stu-id="cd02e-108">Use the latest tools and commands independent of target runtime.</span></span>

<span data-ttu-id="cd02e-109">La sélection de version s’opère dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="cd02e-109">Version selection occurs:</span></span>

- <span data-ttu-id="cd02e-110">Quand vous exécutez une commande du kit SDK, [celui-ci utilise la dernière version installée](#the-sdk-uses-the-latest-installed-version).</span><span class="sxs-lookup"><span data-stu-id="cd02e-110">When you run an SDK command, [the sdk uses the latest installed version](#the-sdk-uses-the-latest-installed-version).</span></span>
- <span data-ttu-id="cd02e-111">Quand vous générez un assembly, [les monikers de framework cible définissent les API au moment de la génération](#target-framework-monikers-define-build-time-apis).</span><span class="sxs-lookup"><span data-stu-id="cd02e-111">When you build an assembly, [target framework monikers define build time APIs](#target-framework-monikers-define-build-time-apis).</span></span>
- <span data-ttu-id="cd02e-112">Quand vous exécutez une application .NET Core, [les applications dépendantes de la version cible de .Net Framework font l’objet d’une restauration par progression](#framework-dependent-apps-roll-forward).</span><span class="sxs-lookup"><span data-stu-id="cd02e-112">When you run a .NET Core application, [target framework dependent apps roll forward](#framework-dependent-apps-roll-forward).</span></span>
- <span data-ttu-id="cd02e-113">Quand vous publiez une application autonome, [les déploiements autonomes incluent le runtime sélectionné](#self-contained-deployments-include-the-selected-runtime).</span><span class="sxs-lookup"><span data-stu-id="cd02e-113">When you publish a self-contained application, [self-contained deployments include the selected runtime](#self-contained-deployments-include-the-selected-runtime).</span></span>

<span data-ttu-id="cd02e-114">Le reste de ce document examine ces quatre scénarios.</span><span class="sxs-lookup"><span data-stu-id="cd02e-114">The rest of this document examines those four scenarios.</span></span>

## <a name="the-sdk-uses-the-latest-installed-version"></a><span data-ttu-id="cd02e-115">Le kit SDK utilise la dernière version installée</span><span class="sxs-lookup"><span data-stu-id="cd02e-115">The SDK uses the latest installed version</span></span>

<span data-ttu-id="cd02e-116">Les commandes du kit SDK incluent `dotnet new`, `dotnet build` et `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="cd02e-116">SDK commands include `dotnet new`, `dotnet build` or `dotnet run`.</span></span> <span data-ttu-id="cd02e-117">L’interface CLI `dotnet` doit choisir une version du kit SDK pour n’importe quelle commande.</span><span class="sxs-lookup"><span data-stu-id="cd02e-117">The `dotnet` CLI must choose an SDK version for any command.</span></span> <span data-ttu-id="cd02e-118">Par défaut, l’interface CLI .NET Core utilise le dernier kit SDK installé sur la machine.</span><span class="sxs-lookup"><span data-stu-id="cd02e-118">The .NET Core CLI uses the latest SDK installed on the machine by default.</span></span> <span data-ttu-id="cd02e-119">S’il est installé, le kit SDK .NET Core v2.1.301 est utilisé, même si le projet sur lequel vous travaillez cible .NET Core Runtime 2.0.</span><span class="sxs-lookup"><span data-stu-id="cd02e-119">You'll use the .NET Core SDK v2.1.301 when it's installed, even if the project you are working with targets the .NET Core Runtime 2.0.</span></span> <span data-ttu-id="cd02e-120">Cela vaut aussi bien pour les préversions que pour les versions publiées.</span><span class="sxs-lookup"><span data-stu-id="cd02e-120">Note that this is true for preview versions as well as released versions.</span></span> <span data-ttu-id="cd02e-121">Vous pouvez tirer parti des fonctionnalités et des améliorations du dernier kit SDK tout en ciblant des versions antérieures du runtime .NET Core.</span><span class="sxs-lookup"><span data-stu-id="cd02e-121">You can take advantage of the latest SDK features and improvements while targeting earlier .NET Core runtime versions.</span></span> <span data-ttu-id="cd02e-122">Vous pouvez cibler plusieurs versions du runtime de .NET Core dans différents projets en utilisant les mêmes outils du kit SDK pour tous les projets.</span><span class="sxs-lookup"><span data-stu-id="cd02e-122">You can target multiple runtime versions of .NET Core on different projects, using the same SDK tools for all projects.</span></span>

<span data-ttu-id="cd02e-123">À de rares occasions, vous pouvez être amené à utiliser une version antérieure du kit SDK.</span><span class="sxs-lookup"><span data-stu-id="cd02e-123">On rare occasions, you may need to use an earlier version of the SDK.</span></span> <span data-ttu-id="cd02e-124">Vous devez dans ce cas spécifier cette version dans un [ fichier *global.json*](../tools/global-json.md).</span><span class="sxs-lookup"><span data-stu-id="cd02e-124">You specify that version in a [*global.json* file](../tools/global-json.md).</span></span> <span data-ttu-id="cd02e-125">La stratégie « utiliser la dernière version » signifie que vous utilisez uniquement *global.json* pour spécifier une version du kit SDK .NET Core antérieure à la dernière version installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-125">The "use latest" policy means you only use *global.json* to specify a .NET Core SDK version earlier than the latest installed version.</span></span>

<span data-ttu-id="cd02e-126">*global.json* peut être placé n’importe où dans la hiérarchie des fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd02e-126">*global.json* can be placed anywhere in the file hierarchy.</span></span> <span data-ttu-id="cd02e-127">L’interface CLI effectue une recherche vers le haut dans le répertoire du projet et s’arrête au premier fichier *global.json* trouvé.</span><span class="sxs-lookup"><span data-stu-id="cd02e-127">The CLI searches upward from the project directory for the first *global.json* it finds.</span></span> <span data-ttu-id="cd02e-128">Vous pouvez contrôler les projets auxquels un fichier *global.json* donné s’applique par son emplacement dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="cd02e-128">You control which projects a given *global.json* applies to by its place in the file system.</span></span> <span data-ttu-id="cd02e-129">L’interface CLI .NET recherche un fichier *global.json* de manière itérative en parcourant le chemin de bas en haut dans le répertoire de travail actif.</span><span class="sxs-lookup"><span data-stu-id="cd02e-129">The .NET CLI searches for a *global.json* file iteratively navigating the path upward from the current working directory.</span></span> <span data-ttu-id="cd02e-130">Le premier fichier *global.json* trouvé spécifie la version utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-130">The first *global.json* file found specifies the version used.</span></span> <span data-ttu-id="cd02e-131">Si cette version est installée, elle est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-131">If that version is installed, that version is used.</span></span> <span data-ttu-id="cd02e-132">Si le kit SDK spécifié dans le fichier *global.json* est introuvable, l’interface CLI .NET restaure par progression le dernier kit SDK installé.</span><span class="sxs-lookup"><span data-stu-id="cd02e-132">If the SDK specified in the *global.json* is not found, the .NET CLI rolls forward to the latest SDK installed.</span></span> <span data-ttu-id="cd02e-133">Cela correspond au comportement par défaut, quand aucun fichier *global.json* n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="cd02e-133">This is the same as the default behavior, when no *global.json* file is found.</span></span>

<span data-ttu-id="cd02e-134">L’exemple suivant présente la syntaxe du fichier *global.json* :</span><span class="sxs-lookup"><span data-stu-id="cd02e-134">The following example shows the *global.json* syntax:</span></span>

``` json
{
  "sdk": {
    "version": "2.0.0"
  }
}
```

<span data-ttu-id="cd02e-135">Le processus de sélection d’une version du kit SDK est le suivant :</span><span class="sxs-lookup"><span data-stu-id="cd02e-135">The process for selecting an SDK version is:</span></span>

1. <span data-ttu-id="cd02e-136">`dotnet` recherche un fichier *global.json* en remontant de manière itérative le chemin dans le répertoire de travail actif.</span><span class="sxs-lookup"><span data-stu-id="cd02e-136">`dotnet` searches for a *global.json* file iteratively reverse-navigating the path upward from the current working directory.</span></span>
1. <span data-ttu-id="cd02e-137">`dotnet` utilise le kit SDK spécifié dans le premier fichier *global.json* trouvé.</span><span class="sxs-lookup"><span data-stu-id="cd02e-137">`dotnet` uses the SDK specified in the first *global.json* found.</span></span>
1. <span data-ttu-id="cd02e-138">`dotnet` utilise la dernière version du kit SDK installé si aucun fichier *global.json* n’est trouvé.</span><span class="sxs-lookup"><span data-stu-id="cd02e-138">`dotnet` uses the latest installed SDK if no *global.json* is found.</span></span>

<span data-ttu-id="cd02e-139">Pour plus d’informations sur la sélection d’une version du kit SDK, consultez la section [Règles de correspondance](../tools/global-json.md) de la rubrique relative à *global.json*.</span><span class="sxs-lookup"><span data-stu-id="cd02e-139">You can learn more about selecting an SDK version in the [matching rules](../tools/global-json.md) section of the topic on *global.json*.</span></span>

## <a name="target-framework-monikers-define-build-time-apis"></a><span data-ttu-id="cd02e-140">Les monikers de framework cible définissent les API au moment de la génération</span><span class="sxs-lookup"><span data-stu-id="cd02e-140">Target Framework Monikers define build time APIs</span></span>

<span data-ttu-id="cd02e-141">Vous générez votre projet par rapport aux API définies dans un **moniker de framework cible** (TFM).</span><span class="sxs-lookup"><span data-stu-id="cd02e-141">You build your project against APIs defined in a **Target Framework Moniker** (TFM).</span></span> <span data-ttu-id="cd02e-142">Vous devez spécifier la [version cible de .Net Framework](../../standard/frameworks.md) dans le fichier projet.</span><span class="sxs-lookup"><span data-stu-id="cd02e-142">You specify the [target framework](../../standard/frameworks.md) in the project file.</span></span> <span data-ttu-id="cd02e-143">Définissez l’élément `TargetFramework` dans votre fichier projet comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="cd02e-143">Set the `TargetFramework` element in your project file as shown in the following example:</span></span>

``` xml
<TargetFramework>netcoreapp2.0</TargetFramework>
```

<span data-ttu-id="cd02e-144">Vous pouvez générer votre projet par rapport à plusieurs TFM.</span><span class="sxs-lookup"><span data-stu-id="cd02e-144">You may build your project against multiple TFMs.</span></span> <span data-ttu-id="cd02e-145">S’il est plus courant de définir plusieurs versions cibles de .Net Framework pour les bibliothèques, cela est également possible dans le cas des applications.</span><span class="sxs-lookup"><span data-stu-id="cd02e-145">Setting multiple target frameworks is more common for libraries but can be done with applications as well.</span></span> <span data-ttu-id="cd02e-146">Pour cela, vous devez spécifier une propriété `TargetFrameworks` (pluriel de `TargetFramework`).</span><span class="sxs-lookup"><span data-stu-id="cd02e-146">You specify a `TargetFrameworks` property (plural of `TargetFramework`).</span></span> <span data-ttu-id="cd02e-147">Les versions cibles de .Net Framework sont séparées par un point-virgule, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="cd02e-147">The target frameworks are semicolon-delimited as shown in the following example:</span></span>

``` xml
<TargetFrameworks>netcoreapp2.0;net47</TargetFrameworks>
```

<span data-ttu-id="cd02e-148">Un kit SDK donné prend en charge un ensemble fixe de versions de .Net Framework, plafonné à la version cible de .Net Framework du runtime qu’il intègre.</span><span class="sxs-lookup"><span data-stu-id="cd02e-148">A given SDK supports a fixed set of frameworks, capped to the target framework of the runtime it ships with.</span></span> <span data-ttu-id="cd02e-149">Par exemple, le kit SDK .NET Core 2.0 comprend le runtime .NET Core 2.0, qui est une implémentation de la version cible de .Net Framework `netcoreapp2.0`.</span><span class="sxs-lookup"><span data-stu-id="cd02e-149">For example, the .NET Core 2.0 SDK includes the .NET Core 2.0 runtime, which is an implementation of the `netcoreapp2.0` target framework.</span></span> <span data-ttu-id="cd02e-150">Le kit SDK .NET Core 2.0 prend en charge `netcoreapp1.0`, `netcoreapp1.1`, et `netcoreapp2.0`, mais pas `netcoreapp2.1` (ou version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="cd02e-150">The .NET Core 2.0 SDK supports `netcoreapp1.0`, `netcoreapp1.1`, and `netcoreapp2.0` but not `netcoreapp2.1` (or higher).</span></span> <span data-ttu-id="cd02e-151">L’installation du kit SDK .NET Core 2.1 vise à générer pour `netcoreapp2.1`.</span><span class="sxs-lookup"><span data-stu-id="cd02e-151">You install the .NET Core 2.1 SDK to build for `netcoreapp2.1`.</span></span>

<span data-ttu-id="cd02e-152">Les versions cibles de .Net Framework Standard sont également plafonnées à la version cible de .Net Framework du runtime intégré au kit SDK.</span><span class="sxs-lookup"><span data-stu-id="cd02e-152">.NET Standard target frameworks are also capped to the target framework of the runtime the SDK ships with.</span></span> <span data-ttu-id="cd02e-153">Le kit SDK .NET Core 2.0 est plafonné à `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="cd02e-153">The .NET Core 2.0 SDK is capped to `netstandard2.0`.</span></span>

## <a name="framework-dependent-apps-roll-forward"></a><span data-ttu-id="cd02e-154">Les applications dépendantes du framework font l’objet d’une restauration par progression</span><span class="sxs-lookup"><span data-stu-id="cd02e-154">Framework-dependent apps roll forward</span></span>

<span data-ttu-id="cd02e-155">Une application s’exécute à partir de la source avec [`dotnet run`](../tools/dotnet-run.md).</span><span class="sxs-lookup"><span data-stu-id="cd02e-155">You run an application from source with [`dotnet run`](../tools/dotnet-run.md).</span></span> <span data-ttu-id="cd02e-156">`dotnet run` permet à la fois de générer et d’exécuter une application.</span><span class="sxs-lookup"><span data-stu-id="cd02e-156">`dotnet run` both builds and runs an application.</span></span> <span data-ttu-id="cd02e-157">L’exécutable `dotnet` est l’**hôte** de l’application dans les environnements de développement.</span><span class="sxs-lookup"><span data-stu-id="cd02e-157">The `dotnet` executable is the **host** for the application in development environments.</span></span>

<span data-ttu-id="cd02e-158">L’hôte choisit la dernière version de correctif installée sur la machine.</span><span class="sxs-lookup"><span data-stu-id="cd02e-158">The host chooses the latest patch version installed on the machine.</span></span> <span data-ttu-id="cd02e-159">Par exemple, si vous avez spécifié `netcoreapp2.0` dans votre fichier projet et que `2.0.4` est le dernier runtime .NET installé, le runtime `2.0.4` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cd02e-159">For example, if you specified `netcoreapp2.0` in your project file, and `2.0.4` is the latest .NET runtime installed, the `2.0.4` runtime is used.</span></span>

<span data-ttu-id="cd02e-160">Si aucune version acceptable de `2.0.*` n’est trouvée, une nouvelle version `2.*` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-160">If no acceptable `2.0.*` version is found, a new `2.*` version is used.</span></span> <span data-ttu-id="cd02e-161">Par exemple, si vous avez spécifié `netcoreapp2.0` et que seule la version `2.1.0` est installée, l’application s’exécute en utilisant le runtime `2.1.0`.</span><span class="sxs-lookup"><span data-stu-id="cd02e-161">For example, if you specified `netcoreapp2.0` and only `2.1.0` is installed, the application runs using the `2.1.0` runtime.</span></span> <span data-ttu-id="cd02e-162">Ce comportement est appelé « restauration par progression d’une version mineure ».</span><span class="sxs-lookup"><span data-stu-id="cd02e-162">This behavior is referred to as "minor version roll-forward."</span></span> <span data-ttu-id="cd02e-163">Les versions antérieures ne sont pas non plus prises en considération.</span><span class="sxs-lookup"><span data-stu-id="cd02e-163">Lower versions also won't be considered.</span></span> <span data-ttu-id="cd02e-164">Quand aucun runtime acceptable n’est installé, l’application ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="cd02e-164">When no acceptable runtime is installed, the application won't run.</span></span>

<span data-ttu-id="cd02e-165">Voici quelques exemples d’utilisation pour illustrer le comportement :</span><span class="sxs-lookup"><span data-stu-id="cd02e-165">A few usage examples demonstrate the behavior:</span></span>

- <span data-ttu-id="cd02e-166">La version 2.0.4 est requise.</span><span class="sxs-lookup"><span data-stu-id="cd02e-166">2.0.4 is required.</span></span> <span data-ttu-id="cd02e-167">La version 2.0.5 est la version de correctif installée la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-167">2.0.5 is the highest patch version installed.</span></span> <span data-ttu-id="cd02e-168">La version 2.0.5 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-168">2.0.5 is used.</span></span>
- <span data-ttu-id="cd02e-169">La version 2.0.4 est requise.</span><span class="sxs-lookup"><span data-stu-id="cd02e-169">2.0.4 is required.</span></span> <span data-ttu-id="cd02e-170">Aucune version 2.0.\* n’est installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-170">No 2.0.\* versions are installed.</span></span> <span data-ttu-id="cd02e-171">La version 1.1.1 correspond à la version de runtime installée la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-171">1.1.1 is the highest runtime installed.</span></span> <span data-ttu-id="cd02e-172">Un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cd02e-172">An error message is displayed.</span></span>
- <span data-ttu-id="cd02e-173">La version 2.0.4 est requise.</span><span class="sxs-lookup"><span data-stu-id="cd02e-173">2.0.4 is required.</span></span> <span data-ttu-id="cd02e-174">La version 2.0.0 correspond à la version installée la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-174">2.0.0 is the highest version installed.</span></span> <span data-ttu-id="cd02e-175">Un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cd02e-175">An error message is displayed.</span></span>
- <span data-ttu-id="cd02e-176">La version 2.0.4 est requise.</span><span class="sxs-lookup"><span data-stu-id="cd02e-176">2.0.4 is required.</span></span> <span data-ttu-id="cd02e-177">Aucune version 2.0.\* n’est installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-177">No 2.0.\* versions are installed.</span></span> <span data-ttu-id="cd02e-178">La version 2.2.2 correspond à la version de runtime 2.x installée la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-178">2.2.2 is the highest 2.x runtime version installed.</span></span> <span data-ttu-id="cd02e-179">La version 2.2.2 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-179">2.2.2 is used.</span></span>
- <span data-ttu-id="cd02e-180">La version 2.0.4 est requise.</span><span class="sxs-lookup"><span data-stu-id="cd02e-180">2.0.4 is required.</span></span> <span data-ttu-id="cd02e-181">Aucune version 2.x n’est installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-181">No 2.x versions are installed.</span></span> <span data-ttu-id="cd02e-182">La version 3.0.0 (version non disponible actuellement) est installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-182">3.0.0 (not a currently available version) is installed.</span></span> <span data-ttu-id="cd02e-183">Un message d’erreur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cd02e-183">An error message is displayed.</span></span>

<span data-ttu-id="cd02e-184">La restauration par progression de la version mineure présente un effet secondaire qui peut toucher les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="cd02e-184">Minor version roll-forward has one side-effect that may affect end users.</span></span> <span data-ttu-id="cd02e-185">Penchons-nous sur le scénario suivant :</span><span class="sxs-lookup"><span data-stu-id="cd02e-185">Consider the following scenario:</span></span>

- <span data-ttu-id="cd02e-186">La version 2.0.4 est requise.</span><span class="sxs-lookup"><span data-stu-id="cd02e-186">2.0.4 is required.</span></span> <span data-ttu-id="cd02e-187">Aucune version 2.0.\* n’est installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-187">No 2.0.\* versions are installed.</span></span> <span data-ttu-id="cd02e-188">La version 2.2.2 est installée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-188">2.2.2 is installed.</span></span> <span data-ttu-id="cd02e-189">La version 2.2.2 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-189">2.2.2 is used.</span></span>
- <span data-ttu-id="cd02e-190">La version 2.0.5 est installée ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="cd02e-190">2.0.5 is later installed.</span></span> <span data-ttu-id="cd02e-191">La version 2.0.5 sera utilisée pour les lancements suivants de l’application, et non la version 2.2.2.</span><span class="sxs-lookup"><span data-stu-id="cd02e-191">2.0.5 will be used for subsequent application launches, not 2.2.2.</span></span> <span data-ttu-id="cd02e-192">Le dernier correctif de la version mineure requise est préféré à une version mineure supérieure.</span><span class="sxs-lookup"><span data-stu-id="cd02e-192">The latest patch of the required minor version is preferred over a higher minor version.</span></span>
- <span data-ttu-id="cd02e-193">Il est possible que les versions 2.0.5 et 2.2.2 se comportent différemment, en particulier dans certains scénarios comme la sérialisation de données binaires.</span><span class="sxs-lookup"><span data-stu-id="cd02e-193">It's possible that 2.0.5 and 2.2.2 behave differently, particularly for scenarios like serializing binary data.</span></span>

## <a name="self-contained-deployments-include-the-selected-runtime"></a><span data-ttu-id="cd02e-194">Les déploiements autonomes incluent le runtime sélectionné</span><span class="sxs-lookup"><span data-stu-id="cd02e-194">Self-contained deployments include the selected runtime</span></span>

<span data-ttu-id="cd02e-195">Vous pouvez publier une application en tant que [**distribution autonome**](../deploying/index.md#self-contained-deployments-scd).</span><span class="sxs-lookup"><span data-stu-id="cd02e-195">You can publish an application as a [**self-contained distribution**](../deploying/index.md#self-contained-deployments-scd).</span></span> <span data-ttu-id="cd02e-196">Cette approche regroupe le runtime et les bibliothèques .NET Core avec votre application.</span><span class="sxs-lookup"><span data-stu-id="cd02e-196">This approach bundles the .NET Core runtime and libraries with your application.</span></span> <span data-ttu-id="cd02e-197">Les déploiements autonomes ne dépendent pas des environnements d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cd02e-197">Self-contained deployments don't have a dependency on runtime environments.</span></span> <span data-ttu-id="cd02e-198">La sélection de la version du runtime se produit au moment de la publication, et non au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="cd02e-198">Runtime version selection occurs at publishing time, not run time.</span></span>

<span data-ttu-id="cd02e-199">Le processus de publication sélectionne la dernière version de correctif de la famille de runtime donnée.</span><span class="sxs-lookup"><span data-stu-id="cd02e-199">The publishing process selects the latest patch version of the given runtime family.</span></span> <span data-ttu-id="cd02e-200">Par exemple, `dotnet publish` sélectionne .NET Core 2.0.4 s’il s’agit de la dernière version de correctif de la famille du runtime .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="cd02e-200">For example, `dotnet publish` will select .NET Core 2.0.4 if it is the latest patch version in the .NET Core 2.0 runtime family.</span></span> <span data-ttu-id="cd02e-201">La version cible de .Net Framework (y compris les derniers correctifs de sécurité installés) est empaquetée avec l’application.</span><span class="sxs-lookup"><span data-stu-id="cd02e-201">The target framework (including the latest installed security patches) is packaged with the application.</span></span>

<span data-ttu-id="cd02e-202">Si la version minimale spécifiée pour une application n’est pas satisfaire, il s’agit d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="cd02e-202">It's an error if the minimum version specified for an application isn't satisfied.</span></span> <span data-ttu-id="cd02e-203">`dotnet publish` se lie à la dernière version de correctif de runtime (au sein d’une famille de version principale.secondaire donnée).</span><span class="sxs-lookup"><span data-stu-id="cd02e-203">`dotnet publish` binds to the latest runtime patch version (within a given major.minor version family).</span></span> <span data-ttu-id="cd02e-204">`dotnet publish` ne prend pas en charge la sémantique de restauration par progression de `dotnet run`.</span><span class="sxs-lookup"><span data-stu-id="cd02e-204">`dotnet publish` doesn't support the roll-forward semantics of `dotnet run`.</span></span> <span data-ttu-id="cd02e-205">Pour plus d’informations sur les correctifs et les déploiements autonomes, consultez l’article relatif à la [sélection de correctif de runtime](../deploying/runtime-patch-selection.md) dans le déploiement d’applications .NET Core.</span><span class="sxs-lookup"><span data-stu-id="cd02e-205">For more information about patches and self-contained deployments, see the article on [runtime patch selection](../deploying/runtime-patch-selection.md) in deploying .NET Core applications.</span></span>

<span data-ttu-id="cd02e-206">Les déploiements autonomes peuvent nécessiter une version de correctif spécifique.</span><span class="sxs-lookup"><span data-stu-id="cd02e-206">Self-contained deployments may require a specific patch version.</span></span> <span data-ttu-id="cd02e-207">Vous pouvez remplacer la version de correctif de runtime minimale (par une version supérieure ou inférieure) dans le fichier projet, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="cd02e-207">You can override the minimum runtime patch version (to higher or lower versions) in the project file, as shown in the following example:</span></span>

``` xml
<RuntimeFrameworkVersion>2.0.4</RuntimeFrameworkVersion>
```

<span data-ttu-id="cd02e-208">L’élément `RuntimeFrameworkVersion` remplace la stratégie de version par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd02e-208">The `RuntimeFrameworkVersion` element  overrides the default version policy.</span></span> <span data-ttu-id="cd02e-209">Pour les déploiements autonomes, `RuntimeFrameworkVersion` spécifie la version *exacte* du framework du runtime.</span><span class="sxs-lookup"><span data-stu-id="cd02e-209">For self-contained deployments, the `RuntimeFrameworkVersion` specifies the *exact* runtime framework version.</span></span> <span data-ttu-id="cd02e-210">Pour les applications dépendantes du framework, `RuntimeFrameworkVersion` spécifie la version *minimale* requise du framework du runtime.</span><span class="sxs-lookup"><span data-stu-id="cd02e-210">For framework dependent applications, the `RuntimeFrameworkVersion` specifies the *minimum* required runtime framework version.</span></span>