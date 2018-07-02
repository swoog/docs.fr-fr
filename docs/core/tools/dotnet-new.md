---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 06/12/2018
ms.openlocfilehash: f0ef91361dfbc2c2ba5532fbd607786289e98c69
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36207766"
---
# <a name="dotnet-new"></a><span data-ttu-id="207e3-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="207e3-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="207e3-104">Name</span><span class="sxs-lookup"><span data-stu-id="207e3-104">Name</span></span>

<span data-ttu-id="207e3-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="207e3-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="207e3-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="207e3-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="207e3-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="207e3-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="207e3-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="207e3-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="207e3-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="207e3-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="207e3-110">Description</span><span class="sxs-lookup"><span data-stu-id="207e3-110">Description</span></span>

<span data-ttu-id="207e3-111">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="207e3-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="207e3-112">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="207e3-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="207e3-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="207e3-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="207e3-114">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="207e3-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="207e3-115">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="207e3-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="207e3-116">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="207e3-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="207e3-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="207e3-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="207e3-118">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="207e3-118">The command contains a default list of templates.</span></span> <span data-ttu-id="207e3-119">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="207e3-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="207e3-120">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.1.300.</span><span class="sxs-lookup"><span data-stu-id="207e3-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="207e3-121">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="207e3-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="207e3-122">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-122">Template description</span></span>                          | <span data-ttu-id="207e3-123">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-123">Template name</span></span>   | <span data-ttu-id="207e3-124">Langages</span><span class="sxs-lookup"><span data-stu-id="207e3-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="207e3-125">Application console</span><span class="sxs-lookup"><span data-stu-id="207e3-125">Console application</span></span>                          | `console`       | <span data-ttu-id="207e3-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-127">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="207e3-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="207e3-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-129">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="207e3-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="207e3-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-131">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="207e3-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="207e3-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-133">Page Razor</span><span class="sxs-lookup"><span data-stu-id="207e3-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="207e3-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-134">[C#]</span></span>          |
| <span data-ttu-id="207e3-135">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="207e3-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="207e3-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-136">[C#]</span></span>          |
| <span data-ttu-id="207e3-137">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="207e3-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="207e3-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-138">[C#]</span></span>          |
| <span data-ttu-id="207e3-139">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="207e3-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="207e3-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-140">[C#], F#</span></span>      |
| <span data-ttu-id="207e3-141">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="207e3-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="207e3-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-142">[C#], F#</span></span>      |
| <span data-ttu-id="207e3-143">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="207e3-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="207e3-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-144">[C#]</span></span>          |
| <span data-ttu-id="207e3-145">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="207e3-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="207e3-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-146">[C#]</span></span>          |
| <span data-ttu-id="207e3-147">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="207e3-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="207e3-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-148">[C#]</span></span>          |
| <span data-ttu-id="207e3-149">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="207e3-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="207e3-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-150">[C#]</span></span>          |
| <span data-ttu-id="207e3-151">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="207e3-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="207e3-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-152">[C#], F#</span></span>      |
| <span data-ttu-id="207e3-153">Bibliothèque de classes Razor</span><span class="sxs-lookup"><span data-stu-id="207e3-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="207e3-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-154">[C#]</span></span>          |
| <span data-ttu-id="207e3-155">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="207e3-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="207e3-156">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="207e3-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="207e3-157">config web</span><span class="sxs-lookup"><span data-stu-id="207e3-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="207e3-158">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="207e3-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="207e3-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="207e3-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="207e3-160">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="207e3-160">The command contains a default list of templates.</span></span> <span data-ttu-id="207e3-161">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="207e3-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="207e3-162">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="207e3-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="207e3-163">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="207e3-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="207e3-164">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-164">Template description</span></span>                          | <span data-ttu-id="207e3-165">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-165">Template name</span></span> | <span data-ttu-id="207e3-166">Langages</span><span class="sxs-lookup"><span data-stu-id="207e3-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="207e3-167">Application console</span><span class="sxs-lookup"><span data-stu-id="207e3-167">Console application</span></span>                          | `console`     | <span data-ttu-id="207e3-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-169">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="207e3-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="207e3-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-171">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="207e3-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="207e3-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-173">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="207e3-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="207e3-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="207e3-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="207e3-175">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="207e3-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="207e3-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-176">[C#], F#</span></span>      |
| <span data-ttu-id="207e3-177">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="207e3-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="207e3-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-178">[C#], F#</span></span>      |
| <span data-ttu-id="207e3-179">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="207e3-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="207e3-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-180">[C#]</span></span>          |
| <span data-ttu-id="207e3-181">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="207e3-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="207e3-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-182">[C#]</span></span>          |
| <span data-ttu-id="207e3-183">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="207e3-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="207e3-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-184">[C#]</span></span>          |
| <span data-ttu-id="207e3-185">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="207e3-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="207e3-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-186">[C#]</span></span>          |
| <span data-ttu-id="207e3-187">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="207e3-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="207e3-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-188">[C#], F#</span></span>      |
| <span data-ttu-id="207e3-189">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="207e3-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="207e3-190">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="207e3-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="207e3-191">config web</span><span class="sxs-lookup"><span data-stu-id="207e3-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="207e3-192">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="207e3-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="207e3-193">Page Razor</span><span class="sxs-lookup"><span data-stu-id="207e3-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="207e3-194">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="207e3-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="207e3-195">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="207e3-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="207e3-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="207e3-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="207e3-197">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="207e3-197">The command contains a default list of templates.</span></span> <span data-ttu-id="207e3-198">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="207e3-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="207e3-199">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="207e3-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="207e3-200">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="207e3-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="207e3-201">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-201">Template description</span></span>  | <span data-ttu-id="207e3-202">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-202">Template name</span></span> | <span data-ttu-id="207e3-203">Langages</span><span class="sxs-lookup"><span data-stu-id="207e3-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="207e3-204">Application console</span><span class="sxs-lookup"><span data-stu-id="207e3-204">Console application</span></span>  | `console`     | <span data-ttu-id="207e3-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-205">[C#], F#</span></span>  |
| <span data-ttu-id="207e3-206">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="207e3-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="207e3-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-207">[C#], F#</span></span>  |
| <span data-ttu-id="207e3-208">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="207e3-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="207e3-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-209">[C#], F#</span></span>  |
| <span data-ttu-id="207e3-210">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="207e3-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="207e3-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-211">[C#], F#</span></span>  |
| <span data-ttu-id="207e3-212">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="207e3-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="207e3-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-213">[C#]</span></span>      |
| <span data-ttu-id="207e3-214">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="207e3-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="207e3-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="207e3-215">[C#], F#</span></span>  |
| <span data-ttu-id="207e3-216">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="207e3-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="207e3-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="207e3-217">[C#]</span></span>      |
| <span data-ttu-id="207e3-218">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="207e3-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="207e3-219">config web</span><span class="sxs-lookup"><span data-stu-id="207e3-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="207e3-220">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="207e3-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="207e3-221">Options</span><span class="sxs-lookup"><span data-stu-id="207e3-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="207e3-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="207e3-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="207e3-223">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="207e3-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="207e3-224">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="207e3-225">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="207e3-225">Prints out help for the command.</span></span> <span data-ttu-id="207e3-226">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="207e3-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="207e3-227">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="207e3-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="207e3-228">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="207e3-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="207e3-229">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="207e3-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="207e3-230">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="207e3-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="207e3-231">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="207e3-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="207e3-232">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="207e3-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="207e3-233">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="207e3-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="207e3-234">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="207e3-235">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="207e3-235">The language of the template to create.</span></span> <span data-ttu-id="207e3-236">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="207e3-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="207e3-237">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="207e3-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="207e3-238">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="207e3-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="207e3-239">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="207e3-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="207e3-240">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="207e3-240">The name for the created output.</span></span> <span data-ttu-id="207e3-241">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="207e3-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="207e3-242">Spécifie une source NuGet à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="207e3-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="207e3-243">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-243">Location to place the generated output.</span></span> <span data-ttu-id="207e3-244">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="207e3-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="207e3-245">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="207e3-245">Filters templates based on available types.</span></span> <span data-ttu-id="207e3-246">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="207e3-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="207e3-247">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="207e3-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="207e3-248">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="207e3-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="207e3-249">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="207e3-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="207e3-250">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="207e3-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="207e3-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="207e3-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="207e3-252">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="207e3-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="207e3-253">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="207e3-254">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="207e3-254">Prints out help for the command.</span></span> <span data-ttu-id="207e3-255">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="207e3-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="207e3-256">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="207e3-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="207e3-257">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="207e3-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="207e3-258">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="207e3-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="207e3-259">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="207e3-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="207e3-260">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="207e3-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="207e3-261">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="207e3-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="207e3-262">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="207e3-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="207e3-263">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="207e3-264">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="207e3-264">The language of the template to create.</span></span> <span data-ttu-id="207e3-265">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="207e3-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="207e3-266">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="207e3-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="207e3-267">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="207e3-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="207e3-268">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="207e3-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="207e3-269">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="207e3-269">The name for the created output.</span></span> <span data-ttu-id="207e3-270">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="207e3-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="207e3-271">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-271">Location to place the generated output.</span></span> <span data-ttu-id="207e3-272">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="207e3-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="207e3-273">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="207e3-273">Filters templates based on available types.</span></span> <span data-ttu-id="207e3-274">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="207e3-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="207e3-275">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="207e3-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="207e3-276">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="207e3-276">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="207e3-277">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="207e3-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="207e3-278">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="207e3-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="207e3-279">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="207e3-279">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="207e3-280">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="207e3-280">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="207e3-281">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="207e3-281">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="207e3-282">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-282">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="207e3-283">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="207e3-283">Prints out help for the command.</span></span> <span data-ttu-id="207e3-284">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="207e3-284">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="207e3-285">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="207e3-285">Lists templates containing the specified name.</span></span> <span data-ttu-id="207e3-286">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="207e3-286">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="207e3-287">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-287">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="207e3-288">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="207e3-288">The language of the template to create.</span></span> <span data-ttu-id="207e3-289">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="207e3-289">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="207e3-290">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="207e3-290">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="207e3-291">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="207e3-291">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="207e3-292">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="207e3-292">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="207e3-293">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="207e3-293">The name for the created output.</span></span> <span data-ttu-id="207e3-294">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="207e3-294">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="207e3-295">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-295">Location to place the generated output.</span></span> <span data-ttu-id="207e3-296">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="207e3-296">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="207e3-297">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="207e3-297">Template options</span></span>

<span data-ttu-id="207e3-298">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="207e3-298">Each project template may have additional options available.</span></span> <span data-ttu-id="207e3-299">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="207e3-299">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="207e3-300">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="207e3-300">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="207e3-301">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="207e3-301">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="207e3-302">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-302">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-303">**classlib**</span><span class="sxs-lookup"><span data-stu-id="207e3-303">**classlib**</span></span>

<span data-ttu-id="207e3-304">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="207e3-304">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="207e3-305">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="207e3-305">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="207e3-306">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="207e3-306">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="207e3-307">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-307">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-308">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="207e3-308">**mstest, xunit**</span></span>

<span data-ttu-id="207e3-309">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="207e3-309">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="207e3-310">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-310">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-311">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="207e3-311">**globaljson**</span></span>

<span data-ttu-id="207e3-312">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="207e3-312">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="207e3-313">**web**</span><span class="sxs-lookup"><span data-stu-id="207e3-313">**web**</span></span>

<span data-ttu-id="207e3-314">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-314">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="207e3-315">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-315">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-316">**webapi**</span><span class="sxs-lookup"><span data-stu-id="207e3-316">**webapi**</span></span>

<span data-ttu-id="207e3-317">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="207e3-317">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="207e3-318">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="207e3-318">The possible values are:</span></span>

- <span data-ttu-id="207e3-319">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="207e3-319">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="207e3-320">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="207e3-320">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="207e3-321">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="207e3-321">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="207e3-322">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="207e3-322">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="207e3-323">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-323">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="207e3-324">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-324">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-325">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-325">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="207e3-326">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-326">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="207e3-327">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-327">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-328">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-328">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="207e3-329">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-329">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-330">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-330">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="207e3-331">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-331">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="207e3-332">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-332">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-333">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="207e3-333">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="207e3-334">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="207e3-334">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="207e3-335">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-335">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-336">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="207e3-336">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="207e3-337">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-337">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="207e3-338">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-338">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-339">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="207e3-339">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="207e3-340">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="207e3-340">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="207e3-341">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-341">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="207e3-342">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-342">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="207e3-343">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="207e3-343">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="207e3-344">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-344">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-345">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-345">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-346">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="207e3-346">**mvc, razor**</span></span>

<span data-ttu-id="207e3-347">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="207e3-347">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="207e3-348">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="207e3-348">The possible values are:</span></span>

- <span data-ttu-id="207e3-349">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="207e3-349">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="207e3-350">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="207e3-350">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="207e3-351">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="207e3-351">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="207e3-352">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="207e3-352">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="207e3-353">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="207e3-353">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="207e3-354">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="207e3-354">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="207e3-355">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-355">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="207e3-356">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-356">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-357">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-357">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="207e3-358">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-358">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="207e3-359">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-359">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-360">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-360">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="207e3-361">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-361">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-362">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-362">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="207e3-363">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-363">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-364">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-364">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="207e3-365">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-365">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="207e3-366">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-366">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="207e3-367">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-367">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="207e3-368">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-368">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="207e3-369">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="207e3-369">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="207e3-370">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="207e3-370">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="207e3-371">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-371">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-372">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="207e3-372">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="207e3-373">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-373">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="207e3-374">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-374">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-375">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="207e3-375">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="207e3-376">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="207e3-376">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="207e3-377">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-377">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-378">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="207e3-378">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="207e3-379">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="207e3-379">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="207e3-380">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-380">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="207e3-381">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-381">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="207e3-382">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-382">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="207e3-383">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="207e3-383">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="207e3-384">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-384">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-385">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-385">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-386">**page**</span><span class="sxs-lookup"><span data-stu-id="207e3-386">**page**</span></span>

<span data-ttu-id="207e3-387">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="207e3-387">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="207e3-388">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="207e3-388">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="207e3-389">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="207e3-389">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="207e3-390">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="207e3-390">**viewimports**</span></span>

<span data-ttu-id="207e3-391">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="207e3-391">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="207e3-392">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="207e3-392">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="207e3-393">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="207e3-393">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="207e3-394">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="207e3-394">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="207e3-395">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-395">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-396">**classlib**</span><span class="sxs-lookup"><span data-stu-id="207e3-396">**classlib**</span></span>

<span data-ttu-id="207e3-397">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="207e3-397">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="207e3-398">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="207e3-398">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="207e3-399">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="207e3-399">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="207e3-400">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-400">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-401">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="207e3-401">**mstest, xunit**</span></span>

<span data-ttu-id="207e3-402">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="207e3-402">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="207e3-403">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-403">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-404">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="207e3-404">**globaljson**</span></span>

<span data-ttu-id="207e3-405">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="207e3-405">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="207e3-406">**web**</span><span class="sxs-lookup"><span data-stu-id="207e3-406">**web**</span></span>

<span data-ttu-id="207e3-407">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-407">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="207e3-408">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-408">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-409">**webapi**</span><span class="sxs-lookup"><span data-stu-id="207e3-409">**webapi**</span></span>

<span data-ttu-id="207e3-410">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="207e3-410">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="207e3-411">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="207e3-411">The possible values are:</span></span>

- <span data-ttu-id="207e3-412">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="207e3-412">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="207e3-413">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="207e3-413">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="207e3-414">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="207e3-414">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="207e3-415">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="207e3-415">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="207e3-416">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-416">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="207e3-417">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-417">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-418">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-418">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="207e3-419">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-419">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="207e3-420">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-420">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-421">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-421">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="207e3-422">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-422">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-423">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-423">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="207e3-424">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-424">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="207e3-425">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-425">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-426">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="207e3-426">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="207e3-427">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="207e3-427">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="207e3-428">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-428">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-429">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="207e3-429">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="207e3-430">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-430">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="207e3-431">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-431">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-432">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="207e3-432">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="207e3-433">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="207e3-433">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="207e3-434">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-434">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="207e3-435">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-435">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="207e3-436">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="207e3-436">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="207e3-437">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-437">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-438">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-438">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-439">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="207e3-439">**mvc, razor**</span></span>

<span data-ttu-id="207e3-440">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="207e3-440">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="207e3-441">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="207e3-441">The possible values are:</span></span>

- <span data-ttu-id="207e3-442">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="207e3-442">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="207e3-443">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="207e3-443">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="207e3-444">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="207e3-444">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="207e3-445">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="207e3-445">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="207e3-446">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="207e3-446">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="207e3-447">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="207e3-447">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="207e3-448">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-448">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="207e3-449">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-449">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-450">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-450">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="207e3-451">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-451">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="207e3-452">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-452">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-453">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-453">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="207e3-454">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-454">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-455">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-455">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="207e3-456">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-456">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-457">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-457">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="207e3-458">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-458">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="207e3-459">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="207e3-459">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="207e3-460">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-460">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="207e3-461">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-461">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="207e3-462">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="207e3-462">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="207e3-463">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="207e3-463">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="207e3-464">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-464">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-465">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="207e3-465">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="207e3-466">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="207e3-466">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="207e3-467">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-467">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="207e3-468">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="207e3-468">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="207e3-469">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="207e3-469">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="207e3-470">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-470">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="207e3-471">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="207e3-471">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="207e3-472">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="207e3-472">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="207e3-473">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="207e3-473">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="207e3-474">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="207e3-474">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="207e3-475">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-475">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="207e3-476">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="207e3-476">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="207e3-477">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="207e3-477">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="207e3-478">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="207e3-478">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="207e3-479">**page**</span><span class="sxs-lookup"><span data-stu-id="207e3-479">**page**</span></span>

<span data-ttu-id="207e3-480">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="207e3-480">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="207e3-481">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="207e3-481">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="207e3-482">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="207e3-482">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="207e3-483">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="207e3-483">**viewimports**</span></span>

<span data-ttu-id="207e3-484">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="207e3-484">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="207e3-485">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="207e3-485">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="207e3-486">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="207e3-486">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="207e3-487">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="207e3-487">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="207e3-488">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="207e3-488">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="207e3-489">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="207e3-489">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="207e3-490">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="207e3-490">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="207e3-491">**classlib**</span><span class="sxs-lookup"><span data-stu-id="207e3-491">**classlib**</span></span>

<span data-ttu-id="207e3-492">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="207e3-492">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="207e3-493">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="207e3-493">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="207e3-494">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="207e3-494">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="207e3-495">**mvc**</span><span class="sxs-lookup"><span data-stu-id="207e3-495">**mvc**</span></span>

<span data-ttu-id="207e3-496">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="207e3-496">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="207e3-497">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="207e3-497">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="207e3-498">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="207e3-498">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="207e3-499">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="207e3-499">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="207e3-500">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="207e3-500">Values: `None` or `Individual`.</span></span> <span data-ttu-id="207e3-501">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="207e3-501">The default value is `None`.</span></span>

<span data-ttu-id="207e3-502">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="207e3-502">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="207e3-503">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="207e3-503">Values: `true` or `false`.</span></span> <span data-ttu-id="207e3-504">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="207e3-504">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="207e3-505">Exemples</span><span class="sxs-lookup"><span data-stu-id="207e3-505">Examples</span></span>

<span data-ttu-id="207e3-506">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="207e3-506">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="207e3-507">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="207e3-507">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="207e3-508">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification :</span><span class="sxs-lookup"><span data-stu-id="207e3-508">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="207e3-509">Créez une application xUnit :</span><span class="sxs-lookup"><span data-stu-id="207e3-509">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="207e3-510">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="207e3-510">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="207e3-511">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="207e3-511">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="207e3-512">Créez un fichier *global.json* dans le répertoire actif en définissant la version du SDK sur 2.0.0 (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="207e3-512">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="207e3-513">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="207e3-513">See also</span></span>

[<span data-ttu-id="207e3-514">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="207e3-514">Custom templates for dotnet new</span></span>](custom-templates.md)  
[<span data-ttu-id="207e3-515">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="207e3-515">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
[<span data-ttu-id="207e3-516">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="207e3-516">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
[<span data-ttu-id="207e3-517">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="207e3-517">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
