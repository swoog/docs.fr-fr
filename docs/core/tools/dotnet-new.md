---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 05/29/2018
ms.openlocfilehash: ae24c4145cc67ca863c07e4d22af8a1c2c2dd732
ms.sourcegitcommit: 3540f614fc94f77ca4ab58df66db2d0f4d52dfee
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2018
ms.locfileid: "34570461"
---
# <a name="dotnet-new"></a><span data-ttu-id="bc9f0-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="bc9f0-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="bc9f0-104">Name</span><span class="sxs-lookup"><span data-stu-id="bc9f0-104">Name</span></span>

<span data-ttu-id="bc9f0-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="bc9f0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bc9f0-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bc9f0-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bc9f0-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bc9f0-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bc9f0-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bc9f0-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bc9f0-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="bc9f0-110">Description</span><span class="sxs-lookup"><span data-stu-id="bc9f0-110">Description</span></span>

<span data-ttu-id="bc9f0-111">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="bc9f0-112">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="bc9f0-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="bc9f0-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="bc9f0-114">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="bc9f0-115">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="bc9f0-116">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bc9f0-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bc9f0-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="bc9f0-118">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-118">The command contains a default list of templates.</span></span> <span data-ttu-id="bc9f0-119">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="bc9f0-120">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.1.300.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="bc9f0-121">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="bc9f0-122">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-122">Template description</span></span>                          | <span data-ttu-id="bc9f0-123">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-123">Template name</span></span>   | <span data-ttu-id="bc9f0-124">Langages</span><span class="sxs-lookup"><span data-stu-id="bc9f0-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="bc9f0-125">Application console</span><span class="sxs-lookup"><span data-stu-id="bc9f0-125">Console application</span></span>                          | `console`       | <span data-ttu-id="bc9f0-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-127">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="bc9f0-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="bc9f0-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-129">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="bc9f0-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="bc9f0-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-131">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="bc9f0-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="bc9f0-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-133">Page Razor</span><span class="sxs-lookup"><span data-stu-id="bc9f0-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="bc9f0-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-134">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-135">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="bc9f0-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="bc9f0-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-136">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-137">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="bc9f0-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="bc9f0-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-138">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-139">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="bc9f0-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="bc9f0-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-140">[C#], F#</span></span>      |
| <span data-ttu-id="bc9f0-141">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="bc9f0-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="bc9f0-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-142">[C#], F#</span></span>      |
| <span data-ttu-id="bc9f0-143">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="bc9f0-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="bc9f0-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-144">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-145">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="bc9f0-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="bc9f0-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-146">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-147">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="bc9f0-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="bc9f0-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-148">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-149">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="bc9f0-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="bc9f0-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-150">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-151">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="bc9f0-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="bc9f0-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-152">[C#], F#</span></span>      |
| <span data-ttu-id="bc9f0-153">Bibliothèque de classes Razor</span><span class="sxs-lookup"><span data-stu-id="bc9f0-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="bc9f0-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-154">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-155">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="bc9f0-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="bc9f0-156">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="bc9f0-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="bc9f0-157">config web</span><span class="sxs-lookup"><span data-stu-id="bc9f0-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="bc9f0-158">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="bc9f0-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bc9f0-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bc9f0-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="bc9f0-160">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-160">The command contains a default list of templates.</span></span> <span data-ttu-id="bc9f0-161">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="bc9f0-162">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="bc9f0-163">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="bc9f0-164">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-164">Template description</span></span>                          | <span data-ttu-id="bc9f0-165">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-165">Template name</span></span> | <span data-ttu-id="bc9f0-166">Langages</span><span class="sxs-lookup"><span data-stu-id="bc9f0-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="bc9f0-167">Application console</span><span class="sxs-lookup"><span data-stu-id="bc9f0-167">Console application</span></span>                          | `console`     | <span data-ttu-id="bc9f0-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-169">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="bc9f0-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="bc9f0-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-171">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="bc9f0-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="bc9f0-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-173">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="bc9f0-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="bc9f0-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="bc9f0-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="bc9f0-175">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="bc9f0-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="bc9f0-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-176">[C#], F#</span></span>      |
| <span data-ttu-id="bc9f0-177">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="bc9f0-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="bc9f0-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-178">[C#], F#</span></span>      |
| <span data-ttu-id="bc9f0-179">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="bc9f0-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="bc9f0-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-180">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-181">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="bc9f0-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="bc9f0-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-182">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-183">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="bc9f0-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="bc9f0-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-184">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-185">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="bc9f0-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="bc9f0-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-186">[C#]</span></span>          |
| <span data-ttu-id="bc9f0-187">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="bc9f0-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="bc9f0-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-188">[C#], F#</span></span>      |
| <span data-ttu-id="bc9f0-189">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="bc9f0-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="bc9f0-190">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="bc9f0-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="bc9f0-191">config web</span><span class="sxs-lookup"><span data-stu-id="bc9f0-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="bc9f0-192">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="bc9f0-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="bc9f0-193">Page Razor</span><span class="sxs-lookup"><span data-stu-id="bc9f0-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="bc9f0-194">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="bc9f0-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="bc9f0-195">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="bc9f0-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bc9f0-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bc9f0-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="bc9f0-197">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-197">The command contains a default list of templates.</span></span> <span data-ttu-id="bc9f0-198">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="bc9f0-199">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="bc9f0-200">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="bc9f0-201">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-201">Template description</span></span>  | <span data-ttu-id="bc9f0-202">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-202">Template name</span></span> | <span data-ttu-id="bc9f0-203">Langages</span><span class="sxs-lookup"><span data-stu-id="bc9f0-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="bc9f0-204">Application console</span><span class="sxs-lookup"><span data-stu-id="bc9f0-204">Console application</span></span>  | `console`     | <span data-ttu-id="bc9f0-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-205">[C#], F#</span></span>  |
| <span data-ttu-id="bc9f0-206">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="bc9f0-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="bc9f0-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-207">[C#], F#</span></span>  |
| <span data-ttu-id="bc9f0-208">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="bc9f0-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="bc9f0-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-209">[C#], F#</span></span>  |
| <span data-ttu-id="bc9f0-210">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="bc9f0-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="bc9f0-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-211">[C#], F#</span></span>  |
| <span data-ttu-id="bc9f0-212">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="bc9f0-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="bc9f0-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-213">[C#]</span></span>      |
| <span data-ttu-id="bc9f0-214">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="bc9f0-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="bc9f0-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="bc9f0-215">[C#], F#</span></span>  |
| <span data-ttu-id="bc9f0-216">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="bc9f0-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="bc9f0-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="bc9f0-217">[C#]</span></span>      |
| <span data-ttu-id="bc9f0-218">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="bc9f0-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="bc9f0-219">config web</span><span class="sxs-lookup"><span data-stu-id="bc9f0-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="bc9f0-220">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="bc9f0-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="bc9f0-221">Options</span><span class="sxs-lookup"><span data-stu-id="bc9f0-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bc9f0-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bc9f0-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="bc9f0-223">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="bc9f0-224">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="bc9f0-225">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-225">Prints out help for the command.</span></span> <span data-ttu-id="bc9f0-226">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="bc9f0-227">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="bc9f0-228">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="bc9f0-229">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="bc9f0-230">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="bc9f0-231">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="bc9f0-232">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="bc9f0-233">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="bc9f0-234">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="bc9f0-235">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-235">The language of the template to create.</span></span> <span data-ttu-id="bc9f0-236">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="bc9f0-237">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-237">Not valid for some templates.</span></span>

    > [!NOTE]
    > Some shells interpret `#` as a special character. In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="bc9f0-238">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-238">The name for the created output.</span></span> <span data-ttu-id="bc9f0-239">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-239">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="bc9f0-240">Spécifie une source NuGet à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-240">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="bc9f0-241">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-241">Location to place the generated output.</span></span> <span data-ttu-id="bc9f0-242">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-242">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="bc9f0-243">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-243">Filters templates based on available types.</span></span> <span data-ttu-id="bc9f0-244">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="bc9f0-244">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="bc9f0-245">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-245">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="bc9f0-246">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-246">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="bc9f0-247">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-247">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="bc9f0-248">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-248">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bc9f0-249">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bc9f0-249">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="bc9f0-250">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-250">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="bc9f0-251">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-251">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="bc9f0-252">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-252">Prints out help for the command.</span></span> <span data-ttu-id="bc9f0-253">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-253">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="bc9f0-254">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-254">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="bc9f0-255">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-255">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="bc9f0-256">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-256">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="bc9f0-257">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-257">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="bc9f0-258">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-258">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="bc9f0-259">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-259">Lists templates containing the specified name.</span></span> <span data-ttu-id="bc9f0-260">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-260">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="bc9f0-261">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-261">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="bc9f0-262">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-262">The language of the template to create.</span></span> <span data-ttu-id="bc9f0-263">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-263">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="bc9f0-264">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-264">Not valid for some templates.</span></span>

    > [!NOTE]
    > Some shells interpret `#` as a special character. In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="bc9f0-265">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-265">The name for the created output.</span></span> <span data-ttu-id="bc9f0-266">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-266">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="bc9f0-267">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-267">Location to place the generated output.</span></span> <span data-ttu-id="bc9f0-268">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-268">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="bc9f0-269">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-269">Filters templates based on available types.</span></span> <span data-ttu-id="bc9f0-270">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="bc9f0-270">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="bc9f0-271">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-271">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="bc9f0-272">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-272">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="bc9f0-273">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-273">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="bc9f0-274">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-274">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bc9f0-275">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bc9f0-275">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="bc9f0-276">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-276">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="bc9f0-277">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-277">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="bc9f0-278">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-278">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="bc9f0-279">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-279">Prints out help for the command.</span></span> <span data-ttu-id="bc9f0-280">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-280">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="bc9f0-281">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-281">Lists templates containing the specified name.</span></span> <span data-ttu-id="bc9f0-282">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-282">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="bc9f0-283">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-283">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="bc9f0-284">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-284">The language of the template to create.</span></span> <span data-ttu-id="bc9f0-285">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-285">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="bc9f0-286">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-286">Not valid for some templates.</span></span>

    > [!NOTE]
    > Some shells interpret `#` as a special character. In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="bc9f0-287">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-287">The name for the created output.</span></span> <span data-ttu-id="bc9f0-288">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-288">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="bc9f0-289">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-289">Location to place the generated output.</span></span> <span data-ttu-id="bc9f0-290">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-290">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="bc9f0-291">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="bc9f0-291">Template options</span></span>

<span data-ttu-id="bc9f0-292">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-292">Each project template may have additional options available.</span></span> <span data-ttu-id="bc9f0-293">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-293">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="bc9f0-294">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="bc9f0-294">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="bc9f0-295">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-295">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="bc9f0-296">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-296">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-297">**classlib**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-297">**classlib**</span></span>

<span data-ttu-id="bc9f0-298">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-298">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="bc9f0-299">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-299">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="bc9f0-300">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-300">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="bc9f0-301">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-301">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-302">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-302">**mstest, xunit**</span></span>

<span data-ttu-id="bc9f0-303">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-303">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="bc9f0-304">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-304">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-305">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-305">**globaljson**</span></span>

<span data-ttu-id="bc9f0-306">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-306">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="bc9f0-307">**web**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-307">**web**</span></span>

<span data-ttu-id="bc9f0-308">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-308">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="bc9f0-309">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-309">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-310">**webapi**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-310">**webapi**</span></span>

<span data-ttu-id="bc9f0-311">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-311">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="bc9f0-312">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-312">The possible values are:</span></span>

- <span data-ttu-id="bc9f0-313">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-313">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="bc9f0-314">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-314">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="bc9f0-315">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-315">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="bc9f0-316">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-316">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="bc9f0-317">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-317">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="bc9f0-318">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-318">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-319">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-319">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="bc9f0-320">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-320">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="bc9f0-321">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-321">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-322">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-322">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="bc9f0-323">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-323">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-324">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-324">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="bc9f0-325">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-325">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="bc9f0-326">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-326">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-327">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-327">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="bc9f0-328">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-328">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="bc9f0-329">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-329">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-330">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-330">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="bc9f0-331">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-331">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="bc9f0-332">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-332">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-333">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-333">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="bc9f0-334">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-334">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="bc9f0-335">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-335">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="bc9f0-336">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-336">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="bc9f0-337">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-337">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="bc9f0-338">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-338">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-339">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-339">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-340">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-340">**mvc, razor**</span></span>

<span data-ttu-id="bc9f0-341">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-341">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="bc9f0-342">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-342">The possible values are:</span></span>

- <span data-ttu-id="bc9f0-343">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-343">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="bc9f0-344">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-344">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="bc9f0-345">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-345">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="bc9f0-346">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-346">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="bc9f0-347">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-347">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="bc9f0-348">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-348">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="bc9f0-349">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-349">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="bc9f0-350">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-350">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-351">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-351">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="bc9f0-352">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-352">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="bc9f0-353">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-353">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-354">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-354">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="bc9f0-355">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-355">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-356">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-356">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="bc9f0-357">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-357">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-358">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-358">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="bc9f0-359">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-359">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="bc9f0-360">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-360">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="bc9f0-361">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-361">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="bc9f0-362">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-362">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="bc9f0-363">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-363">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="bc9f0-364">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-364">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="bc9f0-365">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-365">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-366">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-366">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="bc9f0-367">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-367">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="bc9f0-368">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-368">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-369">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-369">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="bc9f0-370">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-370">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="bc9f0-371">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-371">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-372">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-372">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="bc9f0-373">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-373">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="bc9f0-374">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-374">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="bc9f0-375">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-375">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="bc9f0-376">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-376">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="bc9f0-377">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-377">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="bc9f0-378">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-378">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-379">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-379">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-380">**page**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-380">**page**</span></span>

<span data-ttu-id="bc9f0-381">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-381">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="bc9f0-382">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-382">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="bc9f0-383">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-383">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="bc9f0-384">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-384">**viewimports**</span></span>

<span data-ttu-id="bc9f0-385">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-385">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="bc9f0-386">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-386">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="bc9f0-387">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="bc9f0-387">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="bc9f0-388">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-388">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="bc9f0-389">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-389">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-390">**classlib**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-390">**classlib**</span></span>

<span data-ttu-id="bc9f0-391">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-391">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="bc9f0-392">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-392">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="bc9f0-393">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-393">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="bc9f0-394">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-394">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-395">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-395">**mstest, xunit**</span></span>

<span data-ttu-id="bc9f0-396">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-396">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="bc9f0-397">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-397">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-398">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-398">**globaljson**</span></span>

<span data-ttu-id="bc9f0-399">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-399">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="bc9f0-400">**web**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-400">**web**</span></span>

<span data-ttu-id="bc9f0-401">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-401">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="bc9f0-402">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-402">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-403">**webapi**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-403">**webapi**</span></span>

<span data-ttu-id="bc9f0-404">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-404">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="bc9f0-405">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-405">The possible values are:</span></span>

- <span data-ttu-id="bc9f0-406">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-406">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="bc9f0-407">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-407">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="bc9f0-408">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-408">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="bc9f0-409">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-409">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="bc9f0-410">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-410">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="bc9f0-411">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-411">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-412">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-412">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="bc9f0-413">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-413">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="bc9f0-414">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-414">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-415">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-415">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="bc9f0-416">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-416">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-417">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-417">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="bc9f0-418">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-418">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="bc9f0-419">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-419">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-420">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-420">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="bc9f0-421">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-421">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="bc9f0-422">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-422">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-423">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-423">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="bc9f0-424">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-424">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="bc9f0-425">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-425">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-426">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-426">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="bc9f0-427">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-427">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="bc9f0-428">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-428">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="bc9f0-429">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-429">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="bc9f0-430">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-430">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="bc9f0-431">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-431">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-432">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-432">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-433">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-433">**mvc, razor**</span></span>

<span data-ttu-id="bc9f0-434">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-434">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="bc9f0-435">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-435">The possible values are:</span></span>

- <span data-ttu-id="bc9f0-436">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="bc9f0-436">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="bc9f0-437">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-437">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="bc9f0-438">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-438">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="bc9f0-439">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-439">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="bc9f0-440">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-440">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="bc9f0-441">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-441">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="bc9f0-442">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-442">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="bc9f0-443">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-443">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-444">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-444">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="bc9f0-445">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-445">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="bc9f0-446">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-446">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-447">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-447">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="bc9f0-448">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-448">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-449">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-449">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="bc9f0-450">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-450">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-451">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-451">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="bc9f0-452">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-452">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="bc9f0-453">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-453">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="bc9f0-454">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-454">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="bc9f0-455">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-455">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="bc9f0-456">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-456">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="bc9f0-457">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-457">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="bc9f0-458">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-458">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-459">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-459">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="bc9f0-460">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-460">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="bc9f0-461">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-461">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="bc9f0-462">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-462">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="bc9f0-463">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-463">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="bc9f0-464">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-464">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="bc9f0-465">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-465">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="bc9f0-466">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-466">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="bc9f0-467">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-467">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="bc9f0-468">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-468">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="bc9f0-469">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-469">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="bc9f0-470">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-470">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="bc9f0-471">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-471">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="bc9f0-472">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-472">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="bc9f0-473">**page**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-473">**page**</span></span>

<span data-ttu-id="bc9f0-474">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-474">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="bc9f0-475">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-475">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="bc9f0-476">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-476">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="bc9f0-477">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-477">**viewimports**</span></span>

<span data-ttu-id="bc9f0-478">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-478">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="bc9f0-479">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-479">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="bc9f0-480">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="bc9f0-480">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="bc9f0-481">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-481">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="bc9f0-482">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-482">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="bc9f0-483">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-483">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="bc9f0-484">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-484">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="bc9f0-485">**classlib**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-485">**classlib**</span></span>

<span data-ttu-id="bc9f0-486">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-486">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="bc9f0-487">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-487">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="bc9f0-488">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-488">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="bc9f0-489">**mvc**</span><span class="sxs-lookup"><span data-stu-id="bc9f0-489">**mvc**</span></span>

<span data-ttu-id="bc9f0-490">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-490">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="bc9f0-491">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-491">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="bc9f0-492">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-492">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="bc9f0-493">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-493">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="bc9f0-494">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-494">Values: `None` or `Individual`.</span></span> <span data-ttu-id="bc9f0-495">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-495">The default value is `None`.</span></span>

<span data-ttu-id="bc9f0-496">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-496">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="bc9f0-497">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-497">Values: `true` or `false`.</span></span> <span data-ttu-id="bc9f0-498">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="bc9f0-498">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="bc9f0-499">Exemples</span><span class="sxs-lookup"><span data-stu-id="bc9f0-499">Examples</span></span>

<span data-ttu-id="bc9f0-500">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-500">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="bc9f0-501">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-501">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="bc9f0-502">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification ciblant .NET Core 2.0 :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-502">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication targeting .NET Core 2.0:</span></span>

`dotnet new mvc -au None -f netcoreapp2.0`

<span data-ttu-id="bc9f0-503">Créez une application xUnit ciblant .NET Core 2.0 :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-503">Create a new xUnit application targeting .NET Core 2.0:</span></span>

`dotnet new xunit --framework netcoreapp2.0`

<span data-ttu-id="bc9f0-504">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-504">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="bc9f0-505">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-505">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="bc9f0-506">Créez un fichier *global.json* dans le répertoire actif en définissant la version du SDK sur 2.0.0 (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="bc9f0-506">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="bc9f0-507">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc9f0-507">See also</span></span>

[<span data-ttu-id="bc9f0-508">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="bc9f0-508">Custom templates for dotnet new</span></span>](custom-templates.md)  
[<span data-ttu-id="bc9f0-509">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="bc9f0-509">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
[<span data-ttu-id="bc9f0-510">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="bc9f0-510">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
[<span data-ttu-id="bc9f0-511">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="bc9f0-511">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)