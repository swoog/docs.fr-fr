---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 07/31/2018
ms.openlocfilehash: 396c4ddf09854fa4582226bdb1422f8c929e459b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2018
ms.locfileid: "47208631"
---
# <a name="dotnet-new"></a><span data-ttu-id="a0a89-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="a0a89-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="a0a89-104">Name</span><span class="sxs-lookup"><span data-stu-id="a0a89-104">Name</span></span>

<span data-ttu-id="a0a89-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0a89-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="a0a89-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a0a89-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="a0a89-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a0a89-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="a0a89-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a0a89-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a0a89-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a0a89-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="a0a89-110">Description</span><span class="sxs-lookup"><span data-stu-id="a0a89-110">Description</span></span>

<span data-ttu-id="a0a89-111">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="a0a89-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="a0a89-112">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="a0a89-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="a0a89-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="a0a89-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="a0a89-114">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="a0a89-115">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="a0a89-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="a0a89-116">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="a0a89-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="a0a89-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a0a89-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="a0a89-118">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-118">The command contains a default list of templates.</span></span> <span data-ttu-id="a0a89-119">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="a0a89-120">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.1.300.</span><span class="sxs-lookup"><span data-stu-id="a0a89-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="a0a89-121">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="a0a89-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="a0a89-122">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-122">Template description</span></span>                          | <span data-ttu-id="a0a89-123">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-123">Template name</span></span>   | <span data-ttu-id="a0a89-124">Langages</span><span class="sxs-lookup"><span data-stu-id="a0a89-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="a0a89-125">Application console</span><span class="sxs-lookup"><span data-stu-id="a0a89-125">Console application</span></span>                          | `console`       | <span data-ttu-id="a0a89-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-127">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="a0a89-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="a0a89-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-129">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="a0a89-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="a0a89-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-131">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="a0a89-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="a0a89-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-133">Page Razor</span><span class="sxs-lookup"><span data-stu-id="a0a89-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="a0a89-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-134">[C#]</span></span>          |
| <span data-ttu-id="a0a89-135">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="a0a89-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="a0a89-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-136">[C#]</span></span>          |
| <span data-ttu-id="a0a89-137">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="a0a89-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="a0a89-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-138">[C#]</span></span>          |
| <span data-ttu-id="a0a89-139">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="a0a89-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="a0a89-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-140">[C#], F#</span></span>      |
| <span data-ttu-id="a0a89-141">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="a0a89-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="a0a89-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-142">[C#], F#</span></span>      |
| <span data-ttu-id="a0a89-143">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a0a89-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="a0a89-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-144">[C#]</span></span>          |
| <span data-ttu-id="a0a89-145">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="a0a89-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="a0a89-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-146">[C#]</span></span>          |
| <span data-ttu-id="a0a89-147">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="a0a89-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="a0a89-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-148">[C#]</span></span>          |
| <span data-ttu-id="a0a89-149">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="a0a89-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="a0a89-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-150">[C#]</span></span>          |
| <span data-ttu-id="a0a89-151">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a0a89-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="a0a89-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-152">[C#], F#</span></span>      |
| <span data-ttu-id="a0a89-153">Bibliothèque de classes Razor</span><span class="sxs-lookup"><span data-stu-id="a0a89-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="a0a89-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-154">[C#]</span></span>          |
| <span data-ttu-id="a0a89-155">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="a0a89-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="a0a89-156">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="a0a89-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="a0a89-157">config web</span><span class="sxs-lookup"><span data-stu-id="a0a89-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="a0a89-158">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="a0a89-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="a0a89-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a0a89-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="a0a89-160">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-160">The command contains a default list of templates.</span></span> <span data-ttu-id="a0a89-161">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="a0a89-162">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="a0a89-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="a0a89-163">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="a0a89-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="a0a89-164">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-164">Template description</span></span>                          | <span data-ttu-id="a0a89-165">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-165">Template name</span></span> | <span data-ttu-id="a0a89-166">Langages</span><span class="sxs-lookup"><span data-stu-id="a0a89-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="a0a89-167">Application console</span><span class="sxs-lookup"><span data-stu-id="a0a89-167">Console application</span></span>                          | `console`     | <span data-ttu-id="a0a89-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-169">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="a0a89-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="a0a89-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-171">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="a0a89-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="a0a89-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-173">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="a0a89-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="a0a89-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="a0a89-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="a0a89-175">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="a0a89-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="a0a89-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-176">[C#], F#</span></span>      |
| <span data-ttu-id="a0a89-177">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="a0a89-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="a0a89-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-178">[C#], F#</span></span>      |
| <span data-ttu-id="a0a89-179">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a0a89-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="a0a89-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-180">[C#]</span></span>          |
| <span data-ttu-id="a0a89-181">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="a0a89-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="a0a89-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-182">[C#]</span></span>          |
| <span data-ttu-id="a0a89-183">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="a0a89-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="a0a89-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-184">[C#]</span></span>          |
| <span data-ttu-id="a0a89-185">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="a0a89-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="a0a89-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-186">[C#]</span></span>          |
| <span data-ttu-id="a0a89-187">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a0a89-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="a0a89-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-188">[C#], F#</span></span>      |
| <span data-ttu-id="a0a89-189">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="a0a89-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="a0a89-190">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="a0a89-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="a0a89-191">config web</span><span class="sxs-lookup"><span data-stu-id="a0a89-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="a0a89-192">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="a0a89-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="a0a89-193">Page Razor</span><span class="sxs-lookup"><span data-stu-id="a0a89-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="a0a89-194">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="a0a89-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="a0a89-195">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="a0a89-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a0a89-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a0a89-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="a0a89-197">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-197">The command contains a default list of templates.</span></span> <span data-ttu-id="a0a89-198">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="a0a89-199">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="a0a89-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="a0a89-200">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="a0a89-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="a0a89-201">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-201">Template description</span></span>  | <span data-ttu-id="a0a89-202">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-202">Template name</span></span> | <span data-ttu-id="a0a89-203">Langages</span><span class="sxs-lookup"><span data-stu-id="a0a89-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="a0a89-204">Application console</span><span class="sxs-lookup"><span data-stu-id="a0a89-204">Console application</span></span>  | `console`     | <span data-ttu-id="a0a89-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-205">[C#], F#</span></span>  |
| <span data-ttu-id="a0a89-206">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="a0a89-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="a0a89-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-207">[C#], F#</span></span>  |
| <span data-ttu-id="a0a89-208">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="a0a89-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="a0a89-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-209">[C#], F#</span></span>  |
| <span data-ttu-id="a0a89-210">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="a0a89-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="a0a89-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-211">[C#], F#</span></span>  |
| <span data-ttu-id="a0a89-212">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="a0a89-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="a0a89-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-213">[C#]</span></span>      |
| <span data-ttu-id="a0a89-214">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a0a89-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="a0a89-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="a0a89-215">[C#], F#</span></span>  |
| <span data-ttu-id="a0a89-216">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a0a89-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="a0a89-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="a0a89-217">[C#]</span></span>      |
| <span data-ttu-id="a0a89-218">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="a0a89-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="a0a89-219">config web</span><span class="sxs-lookup"><span data-stu-id="a0a89-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="a0a89-220">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="a0a89-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="a0a89-221">Options</span><span class="sxs-lookup"><span data-stu-id="a0a89-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="a0a89-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a0a89-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="a0a89-223">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="a0a89-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="a0a89-224">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="a0a89-225">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a0a89-225">Prints out help for the command.</span></span> <span data-ttu-id="a0a89-226">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="a0a89-227">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="a0a89-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="a0a89-228">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="a0a89-229">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="a0a89-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="a0a89-230">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="a0a89-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="a0a89-231">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="a0a89-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="a0a89-232">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0a89-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="a0a89-233">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="a0a89-234">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="a0a89-235">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="a0a89-235">The language of the template to create.</span></span> <span data-ttu-id="a0a89-236">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="a0a89-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="a0a89-237">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a89-238">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="a0a89-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="a0a89-239">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="a0a89-240">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-240">The name for the created output.</span></span> <span data-ttu-id="a0a89-241">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0a89-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="a0a89-242">Spécifie une source NuGet à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="a0a89-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="a0a89-243">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-243">Location to place the generated output.</span></span> <span data-ttu-id="a0a89-244">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="a0a89-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="a0a89-245">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-245">Filters templates based on available types.</span></span> <span data-ttu-id="a0a89-246">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="a0a89-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="a0a89-247">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="a0a89-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a89-248">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="a0a89-249">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="a0a89-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="a0a89-250">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="a0a89-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="a0a89-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a0a89-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="a0a89-252">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="a0a89-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="a0a89-253">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="a0a89-254">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a0a89-254">Prints out help for the command.</span></span> <span data-ttu-id="a0a89-255">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="a0a89-256">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="a0a89-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="a0a89-257">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="a0a89-258">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="a0a89-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="a0a89-259">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="a0a89-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="a0a89-260">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="a0a89-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="a0a89-261">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0a89-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="a0a89-262">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="a0a89-263">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="a0a89-264">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="a0a89-264">The language of the template to create.</span></span> <span data-ttu-id="a0a89-265">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="a0a89-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="a0a89-266">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a89-267">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="a0a89-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="a0a89-268">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="a0a89-269">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-269">The name for the created output.</span></span> <span data-ttu-id="a0a89-270">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0a89-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="a0a89-271">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-271">Location to place the generated output.</span></span> <span data-ttu-id="a0a89-272">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="a0a89-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="a0a89-273">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-273">Filters templates based on available types.</span></span> <span data-ttu-id="a0a89-274">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="a0a89-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="a0a89-275">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="a0a89-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a89-276">Pour désinstaller un modèle à l’aide de `PATH` source, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-276">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="a0a89-277">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="a0a89-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="a0a89-278">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="a0a89-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="a0a89-279">Si vous ne parvenez pas à déterminer l’argument `PATH` ou `NUGET_ID` nécessaire pour désinstaller un modèle, l’exécution de `dotnet new --uninstall` sans argument répertorie tous les modèles installés et l’argument requis pour les désinstaller.</span><span class="sxs-lookup"><span data-stu-id="a0a89-279">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a0a89-280">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a0a89-280">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="a0a89-281">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="a0a89-281">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="a0a89-282">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-282">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="a0a89-283">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-283">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="a0a89-284">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="a0a89-284">Prints out help for the command.</span></span> <span data-ttu-id="a0a89-285">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-285">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="a0a89-286">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0a89-286">Lists templates containing the specified name.</span></span> <span data-ttu-id="a0a89-287">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-287">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="a0a89-288">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-288">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="a0a89-289">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="a0a89-289">The language of the template to create.</span></span> <span data-ttu-id="a0a89-290">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="a0a89-290">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="a0a89-291">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-291">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="a0a89-292">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="a0a89-292">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="a0a89-293">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-293">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="a0a89-294">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-294">The name for the created output.</span></span> <span data-ttu-id="a0a89-295">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a0a89-295">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="a0a89-296">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-296">Location to place the generated output.</span></span> <span data-ttu-id="a0a89-297">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="a0a89-297">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="a0a89-298">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="a0a89-298">Template options</span></span>

<span data-ttu-id="a0a89-299">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="a0a89-299">Each project template may have additional options available.</span></span> <span data-ttu-id="a0a89-300">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="a0a89-300">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="a0a89-301">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="a0a89-301">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="a0a89-302">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="a0a89-302">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="a0a89-303">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-303">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-304">**classlib**</span><span class="sxs-lookup"><span data-stu-id="a0a89-304">**classlib**</span></span>

<span data-ttu-id="a0a89-305">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a0a89-305">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a0a89-306">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="a0a89-306">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="a0a89-307">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-307">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="a0a89-308">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-308">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-309">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="a0a89-309">**mstest, xunit**</span></span>

<span data-ttu-id="a0a89-310">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a0a89-310">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="a0a89-311">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-311">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-312">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="a0a89-312">**globaljson**</span></span>

<span data-ttu-id="a0a89-313">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="a0a89-313">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="a0a89-314">**web**</span><span class="sxs-lookup"><span data-stu-id="a0a89-314">**web**</span></span>

<span data-ttu-id="a0a89-315">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-315">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="a0a89-316">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-316">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-317">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a0a89-317">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="a0a89-318">Cette option s’applique uniquement si `IndividualAuth` ou `OrganizationalAuth` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="a0a89-318">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="a0a89-319">**webapi**</span><span class="sxs-lookup"><span data-stu-id="a0a89-319">**webapi**</span></span>

<span data-ttu-id="a0a89-320">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0a89-320">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="a0a89-321">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="a0a89-321">The possible values are:</span></span>

- <span data-ttu-id="a0a89-322">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a0a89-322">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="a0a89-323">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a0a89-323">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="a0a89-324">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-324">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="a0a89-325">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a89-325">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="a0a89-326">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-326">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="a0a89-327">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-327">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-328">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-328">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="a0a89-329">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-329">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="a0a89-330">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-330">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-331">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-331">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="a0a89-332">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-332">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-333">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-333">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="a0a89-334">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-334">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="a0a89-335">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-335">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-336">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-336">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="a0a89-337">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-337">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="a0a89-338">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-338">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-339">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-339">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="a0a89-340">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-340">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="a0a89-341">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-341">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-342">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-342">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="a0a89-343">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-343">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="a0a89-344">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-344">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="a0a89-345">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-345">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="a0a89-346">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a0a89-346">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="a0a89-347">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-347">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-348">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-348">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-349">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a0a89-349">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="a0a89-350">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-350">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="a0a89-351">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="a0a89-351">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="a0a89-352">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="a0a89-352">**mvc, razor**</span></span>

<span data-ttu-id="a0a89-353">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0a89-353">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="a0a89-354">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="a0a89-354">The possible values are:</span></span>

- <span data-ttu-id="a0a89-355">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a0a89-355">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="a0a89-356">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="a0a89-356">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="a0a89-357">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a0a89-357">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="a0a89-358">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-358">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="a0a89-359">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="a0a89-359">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="a0a89-360">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a89-360">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="a0a89-361">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-361">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="a0a89-362">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-362">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-363">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-363">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="a0a89-364">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-364">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="a0a89-365">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-365">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-366">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-366">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="a0a89-367">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-367">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-368">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-368">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="a0a89-369">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-369">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-370">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-370">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="a0a89-371">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-371">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="a0a89-372">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-372">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="a0a89-373">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-373">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="a0a89-374">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-374">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="a0a89-375">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-375">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="a0a89-376">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-376">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="a0a89-377">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-377">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-378">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-378">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="a0a89-379">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-379">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="a0a89-380">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-380">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-381">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-381">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="a0a89-382">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="a0a89-382">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="a0a89-383">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-383">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-384">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-384">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="a0a89-385">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-385">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="a0a89-386">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-386">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="a0a89-387">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-387">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="a0a89-388">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-388">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="a0a89-389">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a0a89-389">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="a0a89-390">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-390">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-391">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-391">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-392">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a0a89-392">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="a0a89-393">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-393">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="a0a89-394">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="a0a89-394">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="a0a89-395">**page**</span><span class="sxs-lookup"><span data-stu-id="a0a89-395">**page**</span></span>

<span data-ttu-id="a0a89-396">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-396">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="a0a89-397">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-397">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="a0a89-398">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="a0a89-398">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="a0a89-399">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="a0a89-399">**viewimports**</span></span>

<span data-ttu-id="a0a89-400">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-400">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="a0a89-401">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-401">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="a0a89-402">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="a0a89-402">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="a0a89-403">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="a0a89-403">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="a0a89-404">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-404">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-405">**classlib**</span><span class="sxs-lookup"><span data-stu-id="a0a89-405">**classlib**</span></span>

<span data-ttu-id="a0a89-406">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a0a89-406">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a0a89-407">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="a0a89-407">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="a0a89-408">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-408">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="a0a89-409">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-409">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-410">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="a0a89-410">**mstest, xunit**</span></span>

<span data-ttu-id="a0a89-411">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a0a89-411">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="a0a89-412">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-412">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-413">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="a0a89-413">**globaljson**</span></span>

<span data-ttu-id="a0a89-414">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="a0a89-414">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="a0a89-415">**web**</span><span class="sxs-lookup"><span data-stu-id="a0a89-415">**web**</span></span>

<span data-ttu-id="a0a89-416">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-416">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="a0a89-417">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-417">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-418">**webapi**</span><span class="sxs-lookup"><span data-stu-id="a0a89-418">**webapi**</span></span>

<span data-ttu-id="a0a89-419">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0a89-419">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="a0a89-420">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="a0a89-420">The possible values are:</span></span>

- <span data-ttu-id="a0a89-421">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a0a89-421">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="a0a89-422">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a0a89-422">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="a0a89-423">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-423">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="a0a89-424">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a89-424">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="a0a89-425">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-425">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="a0a89-426">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-426">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-427">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-427">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="a0a89-428">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-428">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="a0a89-429">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-429">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-430">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-430">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="a0a89-431">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-431">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-432">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-432">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="a0a89-433">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-433">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="a0a89-434">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-434">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-435">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-435">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="a0a89-436">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-436">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="a0a89-437">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-437">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-438">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-438">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="a0a89-439">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-439">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="a0a89-440">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-440">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-441">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-441">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="a0a89-442">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-442">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="a0a89-443">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-443">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="a0a89-444">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-444">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="a0a89-445">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a0a89-445">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="a0a89-446">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-446">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-447">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-447">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-448">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="a0a89-448">**mvc, razor**</span></span>

<span data-ttu-id="a0a89-449">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0a89-449">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="a0a89-450">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="a0a89-450">The possible values are:</span></span>

- <span data-ttu-id="a0a89-451">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="a0a89-451">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="a0a89-452">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="a0a89-452">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="a0a89-453">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a0a89-453">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="a0a89-454">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="a0a89-454">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="a0a89-455">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="a0a89-455">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="a0a89-456">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="a0a89-456">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="a0a89-457">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-457">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="a0a89-458">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-458">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-459">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-459">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="a0a89-460">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-460">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="a0a89-461">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-461">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-462">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-462">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="a0a89-463">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-463">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-464">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-464">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="a0a89-465">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-465">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-466">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-466">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="a0a89-467">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-467">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="a0a89-468">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-468">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="a0a89-469">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-469">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="a0a89-470">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-470">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="a0a89-471">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-471">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="a0a89-472">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-472">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="a0a89-473">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-473">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-474">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-474">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="a0a89-475">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="a0a89-475">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="a0a89-476">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-476">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="a0a89-477">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-477">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="a0a89-478">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="a0a89-478">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="a0a89-479">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-479">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="a0a89-480">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-480">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="a0a89-481">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="a0a89-481">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="a0a89-482">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-482">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="a0a89-483">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="a0a89-483">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="a0a89-484">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-484">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="a0a89-485">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a0a89-485">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="a0a89-486">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-486">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="a0a89-487">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="a0a89-487">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="a0a89-488">**page**</span><span class="sxs-lookup"><span data-stu-id="a0a89-488">**page**</span></span>

<span data-ttu-id="a0a89-489">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-489">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="a0a89-490">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-490">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="a0a89-491">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="a0a89-491">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="a0a89-492">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="a0a89-492">**viewimports**</span></span>

<span data-ttu-id="a0a89-493">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="a0a89-493">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="a0a89-494">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-494">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="a0a89-495">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a0a89-495">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="a0a89-496">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="a0a89-496">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="a0a89-497">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a0a89-497">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a0a89-498">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-498">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="a0a89-499">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-499">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="a0a89-500">**classlib**</span><span class="sxs-lookup"><span data-stu-id="a0a89-500">**classlib**</span></span>

<span data-ttu-id="a0a89-501">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a0a89-501">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a0a89-502">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-502">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="a0a89-503">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-503">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="a0a89-504">**mvc**</span><span class="sxs-lookup"><span data-stu-id="a0a89-504">**mvc**</span></span>

<span data-ttu-id="a0a89-505">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="a0a89-505">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="a0a89-506">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-506">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="a0a89-507">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-507">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="a0a89-508">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="a0a89-508">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="a0a89-509">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-509">Values: `None` or `Individual`.</span></span> <span data-ttu-id="a0a89-510">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-510">The default value is `None`.</span></span>

<span data-ttu-id="a0a89-511">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="a0a89-511">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="a0a89-512">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-512">Values: `true` or `false`.</span></span> <span data-ttu-id="a0a89-513">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="a0a89-513">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="a0a89-514">Exemples</span><span class="sxs-lookup"><span data-stu-id="a0a89-514">Examples</span></span>

<span data-ttu-id="a0a89-515">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="a0a89-515">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="a0a89-516">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="a0a89-516">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="a0a89-517">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification :</span><span class="sxs-lookup"><span data-stu-id="a0a89-517">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="a0a89-518">Créez une application xUnit :</span><span class="sxs-lookup"><span data-stu-id="a0a89-518">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="a0a89-519">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="a0a89-519">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="a0a89-520">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="a0a89-520">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="a0a89-521">Créez un fichier *global.json* dans le répertoire actif en définissant la version du SDK sur 2.0.0 (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="a0a89-521">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="a0a89-522">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0a89-522">See also</span></span>

* [<span data-ttu-id="a0a89-523">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="a0a89-523">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="a0a89-524">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="a0a89-524">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="a0a89-525">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="a0a89-525">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="a0a89-526">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="a0a89-526">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
