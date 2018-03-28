---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 03/21/2018
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: 2cbd42195d0ec713d2ccb4af823075ece950ceff
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2018
---
# <a name="dotnet-new"></a><span data-ttu-id="a2271-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="a2271-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="a2271-104">Name</span><span class="sxs-lookup"><span data-stu-id="a2271-104">Name</span></span>

<span data-ttu-id="a2271-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a2271-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="a2271-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a2271-106">Synopsis</span></span>

# <a name="net-core-20tabnetcore2x"></a>[<span data-ttu-id="a2271-107">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a2271-107">.NET Core 2.0</span></span>](#tab/netcore2x)
```
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a2271-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a2271-108">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="a2271-109">Description</span><span class="sxs-lookup"><span data-stu-id="a2271-109">Description</span></span>

<span data-ttu-id="a2271-110">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="a2271-110">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span> 

<span data-ttu-id="a2271-111">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a2271-111">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="a2271-112">Arguments</span><span class="sxs-lookup"><span data-stu-id="a2271-112">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="a2271-113">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="a2271-113">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="a2271-114">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="a2271-114">Each template might have specific options you can pass.</span></span> <span data-ttu-id="a2271-115">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="a2271-115">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-20tabnetcore2x"></a>[<span data-ttu-id="a2271-116">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a2271-116">.NET Core 2.0</span></span>](#tab/netcore2x)

<span data-ttu-id="a2271-117">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="a2271-117">The command contains a default list of templates.</span></span> <span data-ttu-id="a2271-118">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a2271-118">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="a2271-119">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="a2271-119">The following table shows the templates that come pre-installed with the .NET Core 2.0 SDK.</span></span> <span data-ttu-id="a2271-120">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="a2271-120">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="a2271-121">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="a2271-121">Template description</span></span>                          | <span data-ttu-id="a2271-122">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="a2271-122">Template name</span></span> | <span data-ttu-id="a2271-123">Langages</span><span class="sxs-lookup"><span data-stu-id="a2271-123">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="a2271-124">Application console</span><span class="sxs-lookup"><span data-stu-id="a2271-124">Console application</span></span>                          | `console`     | <span data-ttu-id="a2271-125">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a2271-125">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a2271-126">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="a2271-126">Class library</span></span>                                | `classlib`    | <span data-ttu-id="a2271-127">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a2271-127">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a2271-128">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="a2271-128">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="a2271-129">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a2271-129">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a2271-130">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="a2271-130">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="a2271-131">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a2271-131">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a2271-132">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="a2271-132">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="a2271-133">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-133">[C#], F#</span></span>      |
| <span data-ttu-id="a2271-134">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="a2271-134">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="a2271-135">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-135">[C#], F#</span></span>      |
| <span data-ttu-id="a2271-136">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a2271-136">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="a2271-137">[C#]</span><span class="sxs-lookup"><span data-stu-id="a2271-137">[C#]</span></span>          |
| <span data-ttu-id="a2271-138">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="a2271-138">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="a2271-139">[C#]</span><span class="sxs-lookup"><span data-stu-id="a2271-139">[C#]</span></span>          |
| <span data-ttu-id="a2271-140">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="a2271-140">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="a2271-141">[C#]</span><span class="sxs-lookup"><span data-stu-id="a2271-141">[C#]</span></span>          |
| <span data-ttu-id="a2271-142">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="a2271-142">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="a2271-143">[C#]</span><span class="sxs-lookup"><span data-stu-id="a2271-143">[C#]</span></span>          |
| <span data-ttu-id="a2271-144">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a2271-144">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="a2271-145">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-145">[C#], F#</span></span>      |
| <span data-ttu-id="a2271-146">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="a2271-146">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="a2271-147">Config NuGet</span><span class="sxs-lookup"><span data-stu-id="a2271-147">Nuget config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="a2271-148">config web</span><span class="sxs-lookup"><span data-stu-id="a2271-148">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="a2271-149">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="a2271-149">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="a2271-150">Page Razor</span><span class="sxs-lookup"><span data-stu-id="a2271-150">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="a2271-151">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="a2271-151">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="a2271-152">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="a2271-152">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a2271-153">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a2271-153">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="a2271-154">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="a2271-154">The command contains a default list of templates.</span></span> <span data-ttu-id="a2271-155">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a2271-155">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="a2271-156">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="a2271-156">The following table shows the templates that come pre-installed with the .NET Core 1.x SDK.</span></span> <span data-ttu-id="a2271-157">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="a2271-157">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="a2271-158">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="a2271-158">Template description</span></span>  | <span data-ttu-id="a2271-159">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="a2271-159">Template name</span></span> | <span data-ttu-id="a2271-160">Langages</span><span class="sxs-lookup"><span data-stu-id="a2271-160">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="a2271-161">Application console</span><span class="sxs-lookup"><span data-stu-id="a2271-161">Console application</span></span>  | `console`     | <span data-ttu-id="a2271-162">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-162">[C#], F#</span></span>  |
| <span data-ttu-id="a2271-163">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="a2271-163">Class library</span></span>        | `classlib`    | <span data-ttu-id="a2271-164">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-164">[C#], F#</span></span>  |
| <span data-ttu-id="a2271-165">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="a2271-165">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="a2271-166">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-166">[C#], F#</span></span>  |
| <span data-ttu-id="a2271-167">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="a2271-167">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="a2271-168">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-168">[C#], F#</span></span>  |
| <span data-ttu-id="a2271-169">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="a2271-169">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="a2271-170">[C#]</span><span class="sxs-lookup"><span data-stu-id="a2271-170">[C#]</span></span>      |
| <span data-ttu-id="a2271-171">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a2271-171">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="a2271-172">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a2271-172">[C#], F#</span></span>  |
| <span data-ttu-id="a2271-173">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a2271-173">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="a2271-174">[C#]</span><span class="sxs-lookup"><span data-stu-id="a2271-174">[C#]</span></span>      |
| <span data-ttu-id="a2271-175">Config NuGet</span><span class="sxs-lookup"><span data-stu-id="a2271-175">Nuget config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="a2271-176">config web</span><span class="sxs-lookup"><span data-stu-id="a2271-176">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="a2271-177">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="a2271-177">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="a2271-178">Options</span><span class="sxs-lookup"><span data-stu-id="a2271-178">Options</span></span>

# <a name="net-core-20tabnetcore2x"></a>[<span data-ttu-id="a2271-179">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a2271-179">.NET Core 2.0</span></span>](#tab/netcore2x)

`--force`

<span data-ttu-id="a2271-180">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="a2271-180">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="a2271-181">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-181">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="a2271-182">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a2271-182">Prints out help for the command.</span></span> <span data-ttu-id="a2271-183">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="a2271-183">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="a2271-184">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="a2271-184">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="a2271-185">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="a2271-185">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="a2271-186">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="a2271-186">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="a2271-187">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="a2271-187">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="a2271-188">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="a2271-188">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="a2271-189">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="a2271-189">Lists templates containing the specified name.</span></span> <span data-ttu-id="a2271-190">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="a2271-190">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="a2271-191">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-191">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="a2271-192">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="a2271-192">The language of the template to create.</span></span> <span data-ttu-id="a2271-193">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="a2271-193">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="a2271-194">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="a2271-194">Not valid for some templates.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="a2271-195">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="a2271-195">The name for the created output.</span></span> <span data-ttu-id="a2271-196">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a2271-196">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="a2271-197">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="a2271-197">Location to place the generated output.</span></span> <span data-ttu-id="a2271-198">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="a2271-198">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="a2271-199">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="a2271-199">Filters templates based on available types.</span></span> <span data-ttu-id="a2271-200">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="a2271-200">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="a2271-201">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="a2271-201">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="a2271-202">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="a2271-202">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="a2271-203">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="a2271-203">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="a2271-204">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="a2271-204">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a2271-205">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a2271-205">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="a2271-206">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="a2271-206">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="a2271-207">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="a2271-207">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="a2271-208">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-208">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="a2271-209">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a2271-209">Prints out help for the command.</span></span> <span data-ttu-id="a2271-210">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="a2271-210">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="a2271-211">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="a2271-211">Lists templates containing the specified name.</span></span> <span data-ttu-id="a2271-212">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="a2271-212">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="a2271-213">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-213">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="a2271-214">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="a2271-214">The language of the template to create.</span></span> <span data-ttu-id="a2271-215">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="a2271-215">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="a2271-216">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="a2271-216">Not valid for some templates.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="a2271-217">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="a2271-217">The name for the created output.</span></span> <span data-ttu-id="a2271-218">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a2271-218">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="a2271-219">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="a2271-219">Location to place the generated output.</span></span> <span data-ttu-id="a2271-220">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="a2271-220">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="a2271-221">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="a2271-221">Template options</span></span>

<span data-ttu-id="a2271-222">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="a2271-222">Each project template may have additional options available.</span></span> <span data-ttu-id="a2271-223">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="a2271-223">The core templates have the following additional options:</span></span>

# <a name="net-core-20tabnetcore2x"></a>[<span data-ttu-id="a2271-224">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a2271-224">.NET Core 2.0</span></span>](#tab/netcore2x)

<span data-ttu-id="a2271-225">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="a2271-225">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="a2271-226">`--no-restore` : n’effectue pas de restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-226">`--no-restore` - Doesn't perform an implicit restore during project creation.</span></span>

<span data-ttu-id="a2271-227">**classlib**</span><span class="sxs-lookup"><span data-stu-id="a2271-227">**classlib**</span></span>

<span data-ttu-id="a2271-228">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a2271-228">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a2271-229">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="a2271-229">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="a2271-230">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="a2271-230">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="a2271-231">`--no-restore` : n’effectue pas de restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-231">`--no-restore` - Doesn't perform an implicit restore during project creation.</span></span>

<span data-ttu-id="a2271-232">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="a2271-232">**mstest, xunit**</span></span>

<span data-ttu-id="a2271-233">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a2271-233">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="a2271-234">`--no-restore` : n’effectue pas de restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-234">`--no-restore` - Doesn't perform an implicit restore during project creation.</span></span>

<span data-ttu-id="a2271-235">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="a2271-235">**globaljson**</span></span>

<span data-ttu-id="a2271-236">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="a2271-236">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="a2271-237">**web**</span><span class="sxs-lookup"><span data-stu-id="a2271-237">**web**</span></span>

<span data-ttu-id="a2271-238">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="a2271-238">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="a2271-239">`--no-restore` : n’effectue pas de restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-239">`--no-restore` - Doesn't perform an implicit restore during project creation.</span></span>

<span data-ttu-id="a2271-240">**webapi**</span><span class="sxs-lookup"><span data-stu-id="a2271-240">**webapi**</span></span>

<span data-ttu-id="a2271-241">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a2271-241">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="a2271-242">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="a2271-242">The possible values are:</span></span>

- <span data-ttu-id="a2271-243">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a2271-243">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="a2271-244">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a2271-244">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="a2271-245">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="a2271-245">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="a2271-246">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="a2271-246">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="a2271-247">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2271-247">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="a2271-248">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-248">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="a2271-249">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="a2271-249">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="a2271-250">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-250">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="a2271-251">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-251">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a2271-252">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2271-252">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="a2271-253">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-253">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a2271-254">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="a2271-254">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="a2271-255">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-255">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="a2271-256">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-256">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="a2271-257">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="a2271-257">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="a2271-258">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a2271-258">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="a2271-259">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-259">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a2271-260">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="a2271-260">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="a2271-261">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2271-261">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="a2271-262">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-262">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a2271-263">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="a2271-263">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="a2271-264">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a2271-264">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="a2271-265">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-265">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="a2271-266">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="a2271-266">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="a2271-267">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a2271-267">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="a2271-268">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-268">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a2271-269">`--no-restore` : n’effectue pas de restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-269">`--no-restore` - Doesn't perform an implicit restore during project creation.</span></span>

<span data-ttu-id="a2271-270">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="a2271-270">**mvc, razor**</span></span>

<span data-ttu-id="a2271-271">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a2271-271">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="a2271-272">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="a2271-272">The possible values are:</span></span>

- <span data-ttu-id="a2271-273">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a2271-273">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="a2271-274">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="a2271-274">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="a2271-275">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a2271-275">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="a2271-276">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="a2271-276">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="a2271-277">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="a2271-277">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="a2271-278">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="a2271-278">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="a2271-279">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2271-279">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="a2271-280">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-280">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="a2271-281">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="a2271-281">The default value is `https://login.microsoftonline.com/tfp/` .</span></span>

<span data-ttu-id="a2271-282">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-282">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="a2271-283">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-283">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a2271-284">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-284">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="a2271-285">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-285">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a2271-286">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-286">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="a2271-287">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-287">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a2271-288">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2271-288">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="a2271-289">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-289">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="a2271-290">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="a2271-290">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="a2271-291">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-291">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="a2271-292">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-292">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="a2271-293">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="a2271-293">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="a2271-294">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a2271-294">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="a2271-295">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-295">Use with `SingleOrg` or `IndividualB2C` authentication..</span></span> <span data-ttu-id="a2271-296">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="a2271-296">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="a2271-297">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2271-297">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="a2271-298">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-298">Use with `SingleOrg` authentication..</span></span> <span data-ttu-id="a2271-299">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="a2271-299">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="a2271-300">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="a2271-300">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="a2271-301">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-301">Use with `SingleOrg` or `IndividualB2C` authentication..</span></span> <span data-ttu-id="a2271-302">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="a2271-302">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="a2271-303">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a2271-303">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="a2271-304">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a2271-304">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="a2271-305">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="a2271-305">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="a2271-306">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-306">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="a2271-307">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a2271-307">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="a2271-308">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a2271-308">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a2271-309">`--no-restore` : n’effectue pas de restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a2271-309">`--no-restore` - Doesn't perform an implicit restore during project creation.</span></span>

<span data-ttu-id="a2271-310">**page**</span><span class="sxs-lookup"><span data-stu-id="a2271-310">**page**</span></span>

<span data-ttu-id="a2271-311">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="a2271-311">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="a2271-312">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="a2271-312">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="a2271-313">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="a2271-313">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="a2271-314">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="a2271-314">**viewimports**</span></span>

<span data-ttu-id="a2271-315">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="a2271-315">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="a2271-316">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="a2271-316">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a2271-317">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a2271-317">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="a2271-318">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="a2271-318">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="a2271-319">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a2271-319">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a2271-320">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="a2271-320">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="a2271-321">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="a2271-321">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="a2271-322">**classlib**</span><span class="sxs-lookup"><span data-stu-id="a2271-322">**classlib**</span></span>

<span data-ttu-id="a2271-323">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a2271-323">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a2271-324">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="a2271-324">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="a2271-325">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="a2271-325">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="a2271-326">**mvc**</span><span class="sxs-lookup"><span data-stu-id="a2271-326">**mvc**</span></span>

<span data-ttu-id="a2271-327">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a2271-327">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a2271-328">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="a2271-328">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="a2271-329">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="a2271-329">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="a2271-330">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a2271-330">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="a2271-331">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="a2271-331">Values: `None` or `Individual`.</span></span> <span data-ttu-id="a2271-332">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="a2271-332">The default value is `None`.</span></span>

<span data-ttu-id="a2271-333">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a2271-333">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="a2271-334">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="a2271-334">Values: `true` or `false`.</span></span> <span data-ttu-id="a2271-335">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="a2271-335">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="a2271-336">Exemples</span><span class="sxs-lookup"><span data-stu-id="a2271-336">Examples</span></span>

<span data-ttu-id="a2271-337">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="a2271-337">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang f#`

<span data-ttu-id="a2271-338">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="a2271-338">Create a .NET Standard class library project in the specified directory (available only with .NET Core 2.0 SDK or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="a2271-339">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification ciblant .NET Core 2.0 :</span><span class="sxs-lookup"><span data-stu-id="a2271-339">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication targeting .NET Core 2.0:</span></span>

`dotnet new mvc -au None -f netcoreapp2.0`

<span data-ttu-id="a2271-340">Créez une application xUnit ciblant .NET Core 2.0 :</span><span class="sxs-lookup"><span data-stu-id="a2271-340">Create a new xUnit application targeting .NET Core 2.0:</span></span>

`dotnet new xunit --framework netcoreapp2.0`

<span data-ttu-id="a2271-341">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="a2271-341">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="a2271-342">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="a2271-342">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

## <a name="see-also"></a><span data-ttu-id="a2271-343">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2271-343">See also</span></span>

[<span data-ttu-id="a2271-344">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="a2271-344">Custom templates for dotnet new</span></span>](custom-templates.md)  
[<span data-ttu-id="a2271-345">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="a2271-345">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
[<span data-ttu-id="a2271-346">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="a2271-346">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
[<span data-ttu-id="a2271-347">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="a2271-347">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
