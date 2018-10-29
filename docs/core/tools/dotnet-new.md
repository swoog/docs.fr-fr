---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 10/24/2018
ms.openlocfilehash: 56d76f1dd54097f9cf20129d74057235290c273c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188198"
---
# <a name="dotnet-new"></a><span data-ttu-id="fbbde-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="fbbde-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="fbbde-104">Name</span><span class="sxs-lookup"><span data-stu-id="fbbde-104">Name</span></span>

<span data-ttu-id="fbbde-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="fbbde-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="fbbde-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="fbbde-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fbbde-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fbbde-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fbbde-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fbbde-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fbbde-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fbbde-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="fbbde-110">Description</span><span class="sxs-lookup"><span data-stu-id="fbbde-110">Description</span></span>

<span data-ttu-id="fbbde-111">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="fbbde-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="fbbde-112">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fbbde-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="fbbde-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="fbbde-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="fbbde-114">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="fbbde-115">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="fbbde-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="fbbde-116">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="fbbde-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fbbde-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fbbde-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="fbbde-118">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-118">The command contains a default list of templates.</span></span> <span data-ttu-id="fbbde-119">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="fbbde-120">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.1.300.</span><span class="sxs-lookup"><span data-stu-id="fbbde-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="fbbde-121">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="fbbde-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="fbbde-122">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-122">Template description</span></span>                          | <span data-ttu-id="fbbde-123">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-123">Template name</span></span>    | <span data-ttu-id="fbbde-124">Langages</span><span class="sxs-lookup"><span data-stu-id="fbbde-124">Languages</span></span>     |
|----------------------------------------------|------------------|---------------|
| <span data-ttu-id="fbbde-125">Application console</span><span class="sxs-lookup"><span data-stu-id="fbbde-125">Console application</span></span>                          | `console`        | <span data-ttu-id="fbbde-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-127">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="fbbde-127">Class library</span></span>                                | `classlib`       | <span data-ttu-id="fbbde-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-129">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="fbbde-129">Unit test project</span></span>                            | `mstest`         | <span data-ttu-id="fbbde-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-131">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="fbbde-131">xUnit test project</span></span>                           | `xunit`          | <span data-ttu-id="fbbde-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-133">Page Razor</span><span class="sxs-lookup"><span data-stu-id="fbbde-133">Razor page</span></span>                                   | `page`           | <span data-ttu-id="fbbde-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-134">[C#]</span></span>          |
| <span data-ttu-id="fbbde-135">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="fbbde-135">MVC ViewImports</span></span>                              | `viewimports`    | <span data-ttu-id="fbbde-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-136">[C#]</span></span>          |
| <span data-ttu-id="fbbde-137">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="fbbde-137">MVC ViewStart</span></span>                                | `viewstart`      | <span data-ttu-id="fbbde-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-138">[C#]</span></span>          |
| <span data-ttu-id="fbbde-139">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="fbbde-139">ASP.NET Core empty</span></span>                           | `web`            | <span data-ttu-id="fbbde-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-140">[C#], F#</span></span>      |
| <span data-ttu-id="fbbde-141">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="fbbde-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`            | <span data-ttu-id="fbbde-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-142">[C#], F#</span></span>      |
| <span data-ttu-id="fbbde-143">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="fbbde-143">ASP.NET Core Web App</span></span>                         | <span data-ttu-id="fbbde-144">`razor`, `webapp`</span><span class="sxs-lookup"><span data-stu-id="fbbde-144">`razor`, `webapp`</span></span>| <span data-ttu-id="fbbde-145">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-145">[C#]</span></span>          |
| <span data-ttu-id="fbbde-146">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="fbbde-146">ASP.NET Core with Angular</span></span>                    | `angular`        | <span data-ttu-id="fbbde-147">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-147">[C#]</span></span>          |
| <span data-ttu-id="fbbde-148">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="fbbde-148">ASP.NET Core with React.js</span></span>                   | `react`          | <span data-ttu-id="fbbde-149">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-149">[C#]</span></span>          |
| <span data-ttu-id="fbbde-150">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="fbbde-150">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`     | <span data-ttu-id="fbbde-151">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-151">[C#]</span></span>          |
| <span data-ttu-id="fbbde-152">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="fbbde-152">ASP.NET Core Web API</span></span>                         | `webapi`         | <span data-ttu-id="fbbde-153">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-153">[C#], F#</span></span>      |
| <span data-ttu-id="fbbde-154">Bibliothèque de classes Razor</span><span class="sxs-lookup"><span data-stu-id="fbbde-154">Razor class library</span></span>                          | `razorclasslib`  | <span data-ttu-id="fbbde-155">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-155">[C#]</span></span>          |
| <span data-ttu-id="fbbde-156">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="fbbde-156">global.json file</span></span>                             | `globaljson`     |               |
| <span data-ttu-id="fbbde-157">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="fbbde-157">NuGet config</span></span>                                 | `nugetconfig`    |               |
| <span data-ttu-id="fbbde-158">config web</span><span class="sxs-lookup"><span data-stu-id="fbbde-158">Web config</span></span>                                   | `webconfig`      |               |
| <span data-ttu-id="fbbde-159">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="fbbde-159">Solution file</span></span>                                | `sln`            |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fbbde-160">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fbbde-160">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="fbbde-161">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-161">The command contains a default list of templates.</span></span> <span data-ttu-id="fbbde-162">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-162">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="fbbde-163">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="fbbde-163">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="fbbde-164">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="fbbde-164">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="fbbde-165">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-165">Template description</span></span>                          | <span data-ttu-id="fbbde-166">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-166">Template name</span></span> | <span data-ttu-id="fbbde-167">Langages</span><span class="sxs-lookup"><span data-stu-id="fbbde-167">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="fbbde-168">Application console</span><span class="sxs-lookup"><span data-stu-id="fbbde-168">Console application</span></span>                          | `console`     | <span data-ttu-id="fbbde-169">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-169">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-170">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="fbbde-170">Class library</span></span>                                | `classlib`    | <span data-ttu-id="fbbde-171">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-171">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-172">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="fbbde-172">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="fbbde-173">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-173">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-174">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="fbbde-174">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="fbbde-175">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="fbbde-175">[C#], F#, VB</span></span>  |
| <span data-ttu-id="fbbde-176">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="fbbde-176">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="fbbde-177">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-177">[C#], F#</span></span>      |
| <span data-ttu-id="fbbde-178">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="fbbde-178">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="fbbde-179">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-179">[C#], F#</span></span>      |
| <span data-ttu-id="fbbde-180">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="fbbde-180">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="fbbde-181">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-181">[C#]</span></span>          |
| <span data-ttu-id="fbbde-182">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="fbbde-182">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="fbbde-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-183">[C#]</span></span>          |
| <span data-ttu-id="fbbde-184">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="fbbde-184">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="fbbde-185">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-185">[C#]</span></span>          |
| <span data-ttu-id="fbbde-186">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="fbbde-186">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="fbbde-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-187">[C#]</span></span>          |
| <span data-ttu-id="fbbde-188">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="fbbde-188">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="fbbde-189">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-189">[C#], F#</span></span>      |
| <span data-ttu-id="fbbde-190">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="fbbde-190">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="fbbde-191">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="fbbde-191">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="fbbde-192">config web</span><span class="sxs-lookup"><span data-stu-id="fbbde-192">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="fbbde-193">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="fbbde-193">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="fbbde-194">Page Razor</span><span class="sxs-lookup"><span data-stu-id="fbbde-194">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="fbbde-195">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="fbbde-195">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="fbbde-196">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="fbbde-196">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fbbde-197">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fbbde-197">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="fbbde-198">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-198">The command contains a default list of templates.</span></span> <span data-ttu-id="fbbde-199">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-199">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="fbbde-200">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="fbbde-200">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="fbbde-201">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="fbbde-201">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="fbbde-202">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-202">Template description</span></span>  | <span data-ttu-id="fbbde-203">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-203">Template name</span></span> | <span data-ttu-id="fbbde-204">Langages</span><span class="sxs-lookup"><span data-stu-id="fbbde-204">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="fbbde-205">Application console</span><span class="sxs-lookup"><span data-stu-id="fbbde-205">Console application</span></span>  | `console`     | <span data-ttu-id="fbbde-206">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-206">[C#], F#</span></span>  |
| <span data-ttu-id="fbbde-207">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="fbbde-207">Class library</span></span>        | `classlib`    | <span data-ttu-id="fbbde-208">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-208">[C#], F#</span></span>  |
| <span data-ttu-id="fbbde-209">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="fbbde-209">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="fbbde-210">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-210">[C#], F#</span></span>  |
| <span data-ttu-id="fbbde-211">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="fbbde-211">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="fbbde-212">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-212">[C#], F#</span></span>  |
| <span data-ttu-id="fbbde-213">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="fbbde-213">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="fbbde-214">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-214">[C#]</span></span>      |
| <span data-ttu-id="fbbde-215">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="fbbde-215">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="fbbde-216">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="fbbde-216">[C#], F#</span></span>  |
| <span data-ttu-id="fbbde-217">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="fbbde-217">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="fbbde-218">[C#]</span><span class="sxs-lookup"><span data-stu-id="fbbde-218">[C#]</span></span>      |
| <span data-ttu-id="fbbde-219">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="fbbde-219">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="fbbde-220">config web</span><span class="sxs-lookup"><span data-stu-id="fbbde-220">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="fbbde-221">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="fbbde-221">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="fbbde-222">Options</span><span class="sxs-lookup"><span data-stu-id="fbbde-222">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fbbde-223">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fbbde-223">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="fbbde-224">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="fbbde-224">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="fbbde-225">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-225">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="fbbde-226">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="fbbde-226">Prints out help for the command.</span></span> <span data-ttu-id="fbbde-227">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-227">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="fbbde-228">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="fbbde-228">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="fbbde-229">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-229">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="fbbde-230">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="fbbde-230">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="fbbde-231">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="fbbde-231">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="fbbde-232">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fbbde-232">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="fbbde-233">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="fbbde-233">Lists templates containing the specified name.</span></span> <span data-ttu-id="fbbde-234">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-234">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="fbbde-235">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-235">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="fbbde-236">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="fbbde-236">The language of the template to create.</span></span> <span data-ttu-id="fbbde-237">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="fbbde-237">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="fbbde-238">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-238">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="fbbde-239">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="fbbde-239">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="fbbde-240">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-240">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="fbbde-241">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-241">The name for the created output.</span></span> <span data-ttu-id="fbbde-242">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbbde-242">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="fbbde-243">Spécifie une source NuGet à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="fbbde-243">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="fbbde-244">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-244">Location to place the generated output.</span></span> <span data-ttu-id="fbbde-245">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="fbbde-245">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="fbbde-246">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-246">Filters templates based on available types.</span></span> <span data-ttu-id="fbbde-247">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="fbbde-247">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="fbbde-248">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="fbbde-248">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="fbbde-249">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-249">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="fbbde-250">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="fbbde-250">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="fbbde-251">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="fbbde-251">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fbbde-252">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fbbde-252">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="fbbde-253">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="fbbde-253">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="fbbde-254">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-254">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="fbbde-255">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="fbbde-255">Prints out help for the command.</span></span> <span data-ttu-id="fbbde-256">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-256">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="fbbde-257">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="fbbde-257">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="fbbde-258">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-258">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="fbbde-259">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="fbbde-259">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="fbbde-260">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="fbbde-260">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="fbbde-261">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fbbde-261">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="fbbde-262">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="fbbde-262">Lists templates containing the specified name.</span></span> <span data-ttu-id="fbbde-263">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-263">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="fbbde-264">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-264">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="fbbde-265">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="fbbde-265">The language of the template to create.</span></span> <span data-ttu-id="fbbde-266">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="fbbde-266">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="fbbde-267">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-267">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="fbbde-268">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="fbbde-268">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="fbbde-269">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-269">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="fbbde-270">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-270">The name for the created output.</span></span> <span data-ttu-id="fbbde-271">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbbde-271">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="fbbde-272">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-272">Location to place the generated output.</span></span> <span data-ttu-id="fbbde-273">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="fbbde-273">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="fbbde-274">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-274">Filters templates based on available types.</span></span> <span data-ttu-id="fbbde-275">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="fbbde-275">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="fbbde-276">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="fbbde-276">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="fbbde-277">Pour désinstaller un modèle à l’aide de `PATH` source, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-277">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="fbbde-278">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="fbbde-278">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="fbbde-279">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="fbbde-279">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="fbbde-280">Si vous ne parvenez pas à déterminer l’argument `PATH` ou `NUGET_ID` nécessaire pour désinstaller un modèle, l’exécution de `dotnet new --uninstall` sans argument répertorie tous les modèles installés et l’argument requis pour les désinstaller.</span><span class="sxs-lookup"><span data-stu-id="fbbde-280">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fbbde-281">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fbbde-281">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="fbbde-282">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="fbbde-282">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="fbbde-283">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-283">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="fbbde-284">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-284">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="fbbde-285">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="fbbde-285">Prints out help for the command.</span></span> <span data-ttu-id="fbbde-286">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-286">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="fbbde-287">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="fbbde-287">Lists templates containing the specified name.</span></span> <span data-ttu-id="fbbde-288">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-288">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="fbbde-289">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-289">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="fbbde-290">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="fbbde-290">The language of the template to create.</span></span> <span data-ttu-id="fbbde-291">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="fbbde-291">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="fbbde-292">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-292">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="fbbde-293">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="fbbde-293">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="fbbde-294">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-294">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="fbbde-295">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-295">The name for the created output.</span></span> <span data-ttu-id="fbbde-296">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="fbbde-296">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="fbbde-297">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-297">Location to place the generated output.</span></span> <span data-ttu-id="fbbde-298">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="fbbde-298">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="fbbde-299">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="fbbde-299">Template options</span></span>

<span data-ttu-id="fbbde-300">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="fbbde-300">Each project template may have additional options available.</span></span> <span data-ttu-id="fbbde-301">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="fbbde-301">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="fbbde-302">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="fbbde-302">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="fbbde-303">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="fbbde-303">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="fbbde-304">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-304">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-305">**classlib**</span><span class="sxs-lookup"><span data-stu-id="fbbde-305">**classlib**</span></span>

<span data-ttu-id="fbbde-306">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="fbbde-306">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fbbde-307">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="fbbde-307">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="fbbde-308">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-308">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="fbbde-309">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-309">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-310">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="fbbde-310">**mstest, xunit**</span></span>

<span data-ttu-id="fbbde-311">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="fbbde-311">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="fbbde-312">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-312">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-313">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="fbbde-313">**globaljson**</span></span>

<span data-ttu-id="fbbde-314">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="fbbde-314">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="fbbde-315">**web**</span><span class="sxs-lookup"><span data-stu-id="fbbde-315">**web**</span></span>

<span data-ttu-id="fbbde-316">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-316">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="fbbde-317">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-317">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-318">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbbde-318">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="fbbde-319">Cette option s’applique uniquement si `IndividualAuth` ou `OrganizationalAuth` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="fbbde-319">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="fbbde-320">**webapi**</span><span class="sxs-lookup"><span data-stu-id="fbbde-320">**webapi**</span></span>

<span data-ttu-id="fbbde-321">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbbde-321">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fbbde-322">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="fbbde-322">The possible values are:</span></span>

- <span data-ttu-id="fbbde-323">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="fbbde-323">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fbbde-324">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbbde-324">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fbbde-325">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-325">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fbbde-326">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="fbbde-326">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fbbde-327">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-327">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fbbde-328">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-328">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-329">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-329">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fbbde-330">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-330">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fbbde-331">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-331">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-332">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-332">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fbbde-333">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-333">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-334">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-334">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fbbde-335">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-335">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fbbde-336">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-336">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-337">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-337">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fbbde-338">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-338">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fbbde-339">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-339">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-340">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-340">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fbbde-341">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-341">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fbbde-342">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-342">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-343">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-343">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fbbde-344">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-344">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fbbde-345">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-345">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fbbde-346">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-346">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="fbbde-347">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="fbbde-347">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fbbde-348">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-348">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-349">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-349">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-350">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbbde-350">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="fbbde-351">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-351">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="fbbde-352">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="fbbde-352">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="fbbde-353">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="fbbde-353">**mvc, razor**</span></span>

<span data-ttu-id="fbbde-354">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbbde-354">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fbbde-355">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="fbbde-355">The possible values are:</span></span>

- <span data-ttu-id="fbbde-356">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="fbbde-356">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fbbde-357">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="fbbde-357">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="fbbde-358">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbbde-358">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fbbde-359">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-359">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fbbde-360">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="fbbde-360">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="fbbde-361">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="fbbde-361">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fbbde-362">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-362">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fbbde-363">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-363">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-364">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-364">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fbbde-365">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-365">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fbbde-366">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-366">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-367">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-367">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="fbbde-368">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-369">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-369">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="fbbde-370">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-370">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-371">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-371">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fbbde-372">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-372">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="fbbde-373">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-373">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fbbde-374">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-374">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fbbde-375">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-375">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="fbbde-376">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-376">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fbbde-377">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-377">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fbbde-378">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-378">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-379">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-379">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fbbde-380">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-380">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fbbde-381">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-381">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-382">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-382">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fbbde-383">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="fbbde-383">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="fbbde-384">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-384">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-385">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-385">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="fbbde-386">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-386">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fbbde-387">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-387">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fbbde-388">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-388">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="fbbde-389">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-389">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="fbbde-390">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="fbbde-390">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fbbde-391">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-391">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-392">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-392">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-393">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fbbde-393">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="fbbde-394">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-394">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="fbbde-395">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="fbbde-395">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="fbbde-396">**page**</span><span class="sxs-lookup"><span data-stu-id="fbbde-396">**page**</span></span>

<span data-ttu-id="fbbde-397">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-397">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fbbde-398">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-398">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="fbbde-399">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="fbbde-399">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="fbbde-400">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="fbbde-400">**viewimports**</span></span>

<span data-ttu-id="fbbde-401">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-401">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fbbde-402">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-402">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="fbbde-403">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="fbbde-403">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="fbbde-404">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="fbbde-404">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="fbbde-405">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-405">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-406">**classlib**</span><span class="sxs-lookup"><span data-stu-id="fbbde-406">**classlib**</span></span>

<span data-ttu-id="fbbde-407">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="fbbde-407">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fbbde-408">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="fbbde-408">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="fbbde-409">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-409">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="fbbde-410">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-410">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-411">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="fbbde-411">**mstest, xunit**</span></span>

<span data-ttu-id="fbbde-412">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="fbbde-412">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="fbbde-413">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-413">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-414">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="fbbde-414">**globaljson**</span></span>

<span data-ttu-id="fbbde-415">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="fbbde-415">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="fbbde-416">**web**</span><span class="sxs-lookup"><span data-stu-id="fbbde-416">**web**</span></span>

<span data-ttu-id="fbbde-417">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-417">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="fbbde-418">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-418">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-419">**webapi**</span><span class="sxs-lookup"><span data-stu-id="fbbde-419">**webapi**</span></span>

<span data-ttu-id="fbbde-420">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbbde-420">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fbbde-421">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="fbbde-421">The possible values are:</span></span>

- <span data-ttu-id="fbbde-422">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="fbbde-422">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fbbde-423">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbbde-423">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fbbde-424">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-424">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fbbde-425">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="fbbde-425">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fbbde-426">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-426">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fbbde-427">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-427">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-428">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-428">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fbbde-429">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-429">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fbbde-430">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-430">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-431">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-431">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fbbde-432">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-432">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-433">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-433">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fbbde-434">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-434">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fbbde-435">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-435">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-436">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-436">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fbbde-437">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-437">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fbbde-438">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-438">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-439">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-439">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fbbde-440">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-440">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fbbde-441">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-441">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-442">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-442">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fbbde-443">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-443">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fbbde-444">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-444">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fbbde-445">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-445">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="fbbde-446">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="fbbde-446">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fbbde-447">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-447">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-448">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-448">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-449">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="fbbde-449">**mvc, razor**</span></span>

<span data-ttu-id="fbbde-450">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbbde-450">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="fbbde-451">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="fbbde-451">The possible values are:</span></span>

- <span data-ttu-id="fbbde-452">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="fbbde-452">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="fbbde-453">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="fbbde-453">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="fbbde-454">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="fbbde-454">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="fbbde-455">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="fbbde-455">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="fbbde-456">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="fbbde-456">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="fbbde-457">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="fbbde-457">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="fbbde-458">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-458">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="fbbde-459">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-459">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-460">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-460">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="fbbde-461">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-461">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="fbbde-462">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-462">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-463">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-463">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="fbbde-464">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-465">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-465">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="fbbde-466">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-466">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-467">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-467">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="fbbde-468">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-468">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="fbbde-469">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-469">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="fbbde-470">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-470">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="fbbde-471">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-471">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="fbbde-472">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-472">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="fbbde-473">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-473">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="fbbde-474">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-474">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-475">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-475">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="fbbde-476">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="fbbde-476">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="fbbde-477">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-477">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="fbbde-478">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-478">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="fbbde-479">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="fbbde-479">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="fbbde-480">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-480">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="fbbde-481">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-481">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="fbbde-482">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="fbbde-482">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="fbbde-483">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-483">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="fbbde-484">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="fbbde-484">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="fbbde-485">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-485">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="fbbde-486">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="fbbde-486">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="fbbde-487">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-487">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="fbbde-488">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="fbbde-488">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="fbbde-489">**page**</span><span class="sxs-lookup"><span data-stu-id="fbbde-489">**page**</span></span>

<span data-ttu-id="fbbde-490">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-490">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fbbde-491">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-491">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="fbbde-492">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="fbbde-492">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="fbbde-493">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="fbbde-493">**viewimports**</span></span>

<span data-ttu-id="fbbde-494">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="fbbde-494">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="fbbde-495">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-495">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="fbbde-496">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="fbbde-496">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="fbbde-497">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="fbbde-497">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="fbbde-498">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="fbbde-498">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fbbde-499">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-499">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="fbbde-500">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-500">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="fbbde-501">**classlib**</span><span class="sxs-lookup"><span data-stu-id="fbbde-501">**classlib**</span></span>

<span data-ttu-id="fbbde-502">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="fbbde-502">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fbbde-503">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-503">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="fbbde-504">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-504">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="fbbde-505">**mvc**</span><span class="sxs-lookup"><span data-stu-id="fbbde-505">**mvc**</span></span>

<span data-ttu-id="fbbde-506">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="fbbde-506">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="fbbde-507">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-507">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="fbbde-508">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-508">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="fbbde-509">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fbbde-509">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="fbbde-510">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-510">Values: `None` or `Individual`.</span></span> <span data-ttu-id="fbbde-511">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-511">The default value is `None`.</span></span>

<span data-ttu-id="fbbde-512">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="fbbde-512">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="fbbde-513">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-513">Values: `true` or `false`.</span></span> <span data-ttu-id="fbbde-514">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="fbbde-514">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="fbbde-515">Exemples</span><span class="sxs-lookup"><span data-stu-id="fbbde-515">Examples</span></span>

<span data-ttu-id="fbbde-516">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="fbbde-516">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="fbbde-517">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="fbbde-517">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="fbbde-518">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification :</span><span class="sxs-lookup"><span data-stu-id="fbbde-518">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="fbbde-519">Créez une application xUnit :</span><span class="sxs-lookup"><span data-stu-id="fbbde-519">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="fbbde-520">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="fbbde-520">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="fbbde-521">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="fbbde-521">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="fbbde-522">Créez un fichier *global.json* dans le répertoire actif en définissant la version du SDK sur 2.0.0 (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="fbbde-522">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="fbbde-523">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbbde-523">See also</span></span>

* [<span data-ttu-id="fbbde-524">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="fbbde-524">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="fbbde-525">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="fbbde-525">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="fbbde-526">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="fbbde-526">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="fbbde-527">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="fbbde-527">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
