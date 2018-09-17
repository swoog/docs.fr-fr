---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 07/31/2018
ms.openlocfilehash: 2c82dda2d93225edb360316637e22964135cd5e4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512553"
---
# <a name="dotnet-new"></a><span data-ttu-id="ff938-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="ff938-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="ff938-104">Name</span><span class="sxs-lookup"><span data-stu-id="ff938-104">Name</span></span>

<span data-ttu-id="ff938-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff938-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="ff938-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ff938-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ff938-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ff938-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ff938-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ff938-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ff938-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ff938-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="ff938-110">Description</span><span class="sxs-lookup"><span data-stu-id="ff938-110">Description</span></span>

<span data-ttu-id="ff938-111">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="ff938-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="ff938-112">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="ff938-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="ff938-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="ff938-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="ff938-114">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="ff938-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="ff938-115">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="ff938-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="ff938-116">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="ff938-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ff938-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ff938-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="ff938-118">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="ff938-118">The command contains a default list of templates.</span></span> <span data-ttu-id="ff938-119">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff938-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="ff938-120">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.1.300.</span><span class="sxs-lookup"><span data-stu-id="ff938-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="ff938-121">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="ff938-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="ff938-122">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-122">Template description</span></span>                          | <span data-ttu-id="ff938-123">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-123">Template name</span></span>   | <span data-ttu-id="ff938-124">Langages</span><span class="sxs-lookup"><span data-stu-id="ff938-124">Languages</span></span>     |
|----------------------------------------------|-----------------|---------------|
| <span data-ttu-id="ff938-125">Application console</span><span class="sxs-lookup"><span data-stu-id="ff938-125">Console application</span></span>                          | `console`       | <span data-ttu-id="ff938-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-127">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="ff938-127">Class library</span></span>                                | `classlib`      | <span data-ttu-id="ff938-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-129">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="ff938-129">Unit test project</span></span>                            | `mstest`        | <span data-ttu-id="ff938-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-131">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="ff938-131">xUnit test project</span></span>                           | `xunit`         | <span data-ttu-id="ff938-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-133">Page Razor</span><span class="sxs-lookup"><span data-stu-id="ff938-133">Razor page</span></span>                                   | `page`          | <span data-ttu-id="ff938-134">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-134">[C#]</span></span>          |
| <span data-ttu-id="ff938-135">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="ff938-135">MVC ViewImports</span></span>                              | `viewimports`   | <span data-ttu-id="ff938-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-136">[C#]</span></span>          |
| <span data-ttu-id="ff938-137">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="ff938-137">MVC ViewStart</span></span>                                | `viewstart`     | <span data-ttu-id="ff938-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-138">[C#]</span></span>          |
| <span data-ttu-id="ff938-139">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="ff938-139">ASP.NET Core empty</span></span>                           | `web`           | <span data-ttu-id="ff938-140">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-140">[C#], F#</span></span>      |
| <span data-ttu-id="ff938-141">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="ff938-141">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`           | <span data-ttu-id="ff938-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-142">[C#], F#</span></span>      |
| <span data-ttu-id="ff938-143">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ff938-143">ASP.NET Core Web App</span></span>                         | `razor`         | <span data-ttu-id="ff938-144">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-144">[C#]</span></span>          |
| <span data-ttu-id="ff938-145">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="ff938-145">ASP.NET Core with Angular</span></span>                    | `angular`       | <span data-ttu-id="ff938-146">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-146">[C#]</span></span>          |
| <span data-ttu-id="ff938-147">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="ff938-147">ASP.NET Core with React.js</span></span>                   | `react`         | <span data-ttu-id="ff938-148">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-148">[C#]</span></span>          |
| <span data-ttu-id="ff938-149">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="ff938-149">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`    | <span data-ttu-id="ff938-150">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-150">[C#]</span></span>          |
| <span data-ttu-id="ff938-151">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ff938-151">ASP.NET Core Web API</span></span>                         | `webapi`        | <span data-ttu-id="ff938-152">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-152">[C#], F#</span></span>      |
| <span data-ttu-id="ff938-153">Bibliothèque de classes Razor</span><span class="sxs-lookup"><span data-stu-id="ff938-153">Razor class library</span></span>                          | `razorclasslib` | <span data-ttu-id="ff938-154">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-154">[C#]</span></span>          |
| <span data-ttu-id="ff938-155">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="ff938-155">global.json file</span></span>                             | `globaljson`    |               |
| <span data-ttu-id="ff938-156">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="ff938-156">NuGet config</span></span>                                 | `nugetconfig`   |               |
| <span data-ttu-id="ff938-157">config web</span><span class="sxs-lookup"><span data-stu-id="ff938-157">Web config</span></span>                                   | `webconfig`     |               |
| <span data-ttu-id="ff938-158">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="ff938-158">Solution file</span></span>                                | `sln`           |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ff938-159">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ff938-159">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="ff938-160">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="ff938-160">The command contains a default list of templates.</span></span> <span data-ttu-id="ff938-161">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff938-161">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="ff938-162">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="ff938-162">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="ff938-163">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="ff938-163">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="ff938-164">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-164">Template description</span></span>                          | <span data-ttu-id="ff938-165">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-165">Template name</span></span> | <span data-ttu-id="ff938-166">Langages</span><span class="sxs-lookup"><span data-stu-id="ff938-166">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="ff938-167">Application console</span><span class="sxs-lookup"><span data-stu-id="ff938-167">Console application</span></span>                          | `console`     | <span data-ttu-id="ff938-168">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-168">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-169">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="ff938-169">Class library</span></span>                                | `classlib`    | <span data-ttu-id="ff938-170">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-170">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-171">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="ff938-171">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="ff938-172">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-172">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-173">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="ff938-173">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="ff938-174">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="ff938-174">[C#], F#, VB</span></span>  |
| <span data-ttu-id="ff938-175">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="ff938-175">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="ff938-176">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-176">[C#], F#</span></span>      |
| <span data-ttu-id="ff938-177">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="ff938-177">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="ff938-178">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-178">[C#], F#</span></span>      |
| <span data-ttu-id="ff938-179">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ff938-179">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="ff938-180">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-180">[C#]</span></span>          |
| <span data-ttu-id="ff938-181">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="ff938-181">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="ff938-182">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-182">[C#]</span></span>          |
| <span data-ttu-id="ff938-183">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="ff938-183">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="ff938-184">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-184">[C#]</span></span>          |
| <span data-ttu-id="ff938-185">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="ff938-185">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="ff938-186">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-186">[C#]</span></span>          |
| <span data-ttu-id="ff938-187">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ff938-187">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="ff938-188">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-188">[C#], F#</span></span>      |
| <span data-ttu-id="ff938-189">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="ff938-189">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="ff938-190">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="ff938-190">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="ff938-191">config web</span><span class="sxs-lookup"><span data-stu-id="ff938-191">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="ff938-192">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="ff938-192">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="ff938-193">Page Razor</span><span class="sxs-lookup"><span data-stu-id="ff938-193">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="ff938-194">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="ff938-194">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="ff938-195">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="ff938-195">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ff938-196">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ff938-196">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="ff938-197">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="ff938-197">The command contains a default list of templates.</span></span> <span data-ttu-id="ff938-198">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff938-198">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="ff938-199">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="ff938-199">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="ff938-200">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="ff938-200">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="ff938-201">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-201">Template description</span></span>  | <span data-ttu-id="ff938-202">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-202">Template name</span></span> | <span data-ttu-id="ff938-203">Langages</span><span class="sxs-lookup"><span data-stu-id="ff938-203">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="ff938-204">Application console</span><span class="sxs-lookup"><span data-stu-id="ff938-204">Console application</span></span>  | `console`     | <span data-ttu-id="ff938-205">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-205">[C#], F#</span></span>  |
| <span data-ttu-id="ff938-206">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="ff938-206">Class library</span></span>        | `classlib`    | <span data-ttu-id="ff938-207">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-207">[C#], F#</span></span>  |
| <span data-ttu-id="ff938-208">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="ff938-208">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="ff938-209">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-209">[C#], F#</span></span>  |
| <span data-ttu-id="ff938-210">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="ff938-210">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="ff938-211">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-211">[C#], F#</span></span>  |
| <span data-ttu-id="ff938-212">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="ff938-212">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="ff938-213">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-213">[C#]</span></span>      |
| <span data-ttu-id="ff938-214">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ff938-214">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="ff938-215">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="ff938-215">[C#], F#</span></span>  |
| <span data-ttu-id="ff938-216">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="ff938-216">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="ff938-217">[C#]</span><span class="sxs-lookup"><span data-stu-id="ff938-217">[C#]</span></span>      |
| <span data-ttu-id="ff938-218">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="ff938-218">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="ff938-219">config web</span><span class="sxs-lookup"><span data-stu-id="ff938-219">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="ff938-220">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="ff938-220">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="ff938-221">Options</span><span class="sxs-lookup"><span data-stu-id="ff938-221">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ff938-222">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ff938-222">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="ff938-223">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="ff938-223">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="ff938-224">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-224">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="ff938-225">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="ff938-225">Prints out help for the command.</span></span> <span data-ttu-id="ff938-226">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="ff938-226">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="ff938-227">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="ff938-227">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="ff938-228">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="ff938-228">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="ff938-229">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="ff938-229">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="ff938-230">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="ff938-230">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="ff938-231">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="ff938-231">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="ff938-232">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff938-232">Lists templates containing the specified name.</span></span> <span data-ttu-id="ff938-233">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="ff938-233">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="ff938-234">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-234">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="ff938-235">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="ff938-235">The language of the template to create.</span></span> <span data-ttu-id="ff938-236">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="ff938-236">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="ff938-237">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="ff938-237">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="ff938-238">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="ff938-238">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="ff938-239">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="ff938-239">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="ff938-240">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="ff938-240">The name for the created output.</span></span> <span data-ttu-id="ff938-241">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff938-241">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="ff938-242">Spécifie une source NuGet à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff938-242">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="ff938-243">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="ff938-243">Location to place the generated output.</span></span> <span data-ttu-id="ff938-244">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="ff938-244">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="ff938-245">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff938-245">Filters templates based on available types.</span></span> <span data-ttu-id="ff938-246">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="ff938-246">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="ff938-247">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="ff938-247">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="ff938-248">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="ff938-248">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="ff938-249">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="ff938-249">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="ff938-250">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="ff938-250">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ff938-251">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ff938-251">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="ff938-252">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="ff938-252">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="ff938-253">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-253">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="ff938-254">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="ff938-254">Prints out help for the command.</span></span> <span data-ttu-id="ff938-255">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="ff938-255">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="ff938-256">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="ff938-256">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="ff938-257">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="ff938-257">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="ff938-258">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="ff938-258">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="ff938-259">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="ff938-259">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="ff938-260">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="ff938-260">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="ff938-261">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff938-261">Lists templates containing the specified name.</span></span> <span data-ttu-id="ff938-262">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="ff938-262">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="ff938-263">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-263">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="ff938-264">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="ff938-264">The language of the template to create.</span></span> <span data-ttu-id="ff938-265">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="ff938-265">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="ff938-266">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="ff938-266">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="ff938-267">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="ff938-267">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="ff938-268">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="ff938-268">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="ff938-269">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="ff938-269">The name for the created output.</span></span> <span data-ttu-id="ff938-270">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff938-270">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="ff938-271">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="ff938-271">Location to place the generated output.</span></span> <span data-ttu-id="ff938-272">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="ff938-272">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="ff938-273">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff938-273">Filters templates based on available types.</span></span> <span data-ttu-id="ff938-274">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="ff938-274">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="ff938-275">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="ff938-275">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="ff938-276">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="ff938-276">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="ff938-277">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="ff938-277">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="ff938-278">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="ff938-278">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ff938-279">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ff938-279">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="ff938-280">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="ff938-280">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="ff938-281">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="ff938-281">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="ff938-282">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-282">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="ff938-283">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="ff938-283">Prints out help for the command.</span></span> <span data-ttu-id="ff938-284">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="ff938-284">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="ff938-285">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff938-285">Lists templates containing the specified name.</span></span> <span data-ttu-id="ff938-286">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="ff938-286">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="ff938-287">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-287">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="ff938-288">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="ff938-288">The language of the template to create.</span></span> <span data-ttu-id="ff938-289">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="ff938-289">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="ff938-290">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="ff938-290">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="ff938-291">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="ff938-291">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="ff938-292">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="ff938-292">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="ff938-293">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="ff938-293">The name for the created output.</span></span> <span data-ttu-id="ff938-294">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff938-294">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="ff938-295">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="ff938-295">Location to place the generated output.</span></span> <span data-ttu-id="ff938-296">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="ff938-296">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="ff938-297">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="ff938-297">Template options</span></span>

<span data-ttu-id="ff938-298">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="ff938-298">Each project template may have additional options available.</span></span> <span data-ttu-id="ff938-299">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="ff938-299">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="ff938-300">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ff938-300">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="ff938-301">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="ff938-301">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="ff938-302">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-302">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-303">**classlib**</span><span class="sxs-lookup"><span data-stu-id="ff938-303">**classlib**</span></span>

<span data-ttu-id="ff938-304">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="ff938-304">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="ff938-305">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="ff938-305">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="ff938-306">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="ff938-306">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="ff938-307">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-307">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-308">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="ff938-308">**mstest, xunit**</span></span>

<span data-ttu-id="ff938-309">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="ff938-309">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="ff938-310">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-310">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-311">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="ff938-311">**globaljson**</span></span>

<span data-ttu-id="ff938-312">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="ff938-312">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="ff938-313">**web**</span><span class="sxs-lookup"><span data-stu-id="ff938-313">**web**</span></span>

<span data-ttu-id="ff938-314">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-314">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="ff938-315">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-315">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-316">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ff938-316">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="ff938-317">Cette option s’applique uniquement si `IndividualAuth` ou `OrganizationalAuth` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="ff938-317">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="ff938-318">**webapi**</span><span class="sxs-lookup"><span data-stu-id="ff938-318">**webapi**</span></span>

<span data-ttu-id="ff938-319">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff938-319">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="ff938-320">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="ff938-320">The possible values are:</span></span>

- <span data-ttu-id="ff938-321">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="ff938-321">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="ff938-322">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ff938-322">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="ff938-323">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="ff938-323">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="ff938-324">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="ff938-324">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="ff938-325">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-325">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="ff938-326">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-326">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-327">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-327">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="ff938-328">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-328">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="ff938-329">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-329">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-330">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-330">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="ff938-331">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-331">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-332">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-332">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="ff938-333">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-333">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="ff938-334">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-334">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-335">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="ff938-335">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="ff938-336">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ff938-336">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="ff938-337">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-337">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-338">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="ff938-338">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="ff938-339">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-339">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="ff938-340">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-340">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-341">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="ff938-341">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="ff938-342">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="ff938-342">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="ff938-343">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-343">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="ff938-344">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-344">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="ff938-345">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="ff938-345">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="ff938-346">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-346">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-347">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-347">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-348">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ff938-348">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="ff938-349">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="ff938-349">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="ff938-350">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="ff938-350">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="ff938-351">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="ff938-351">**mvc, razor**</span></span>

<span data-ttu-id="ff938-352">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff938-352">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="ff938-353">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="ff938-353">The possible values are:</span></span>

- <span data-ttu-id="ff938-354">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="ff938-354">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="ff938-355">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="ff938-355">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="ff938-356">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ff938-356">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="ff938-357">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="ff938-357">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="ff938-358">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="ff938-358">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="ff938-359">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="ff938-359">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="ff938-360">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-360">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="ff938-361">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-361">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-362">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-362">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="ff938-363">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-363">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="ff938-364">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-364">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-365">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-365">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="ff938-366">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-366">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-367">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-367">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="ff938-368">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-369">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-369">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="ff938-370">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-370">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="ff938-371">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-371">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="ff938-372">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-372">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="ff938-373">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-373">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="ff938-374">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="ff938-374">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="ff938-375">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ff938-375">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="ff938-376">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-376">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-377">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="ff938-377">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="ff938-378">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-378">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="ff938-379">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-379">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-380">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="ff938-380">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="ff938-381">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="ff938-381">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="ff938-382">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-382">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-383">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="ff938-383">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="ff938-384">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="ff938-384">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="ff938-385">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-385">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="ff938-386">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-386">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="ff938-387">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-387">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="ff938-388">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="ff938-388">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="ff938-389">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-389">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-390">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-390">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-391">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ff938-391">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="ff938-392">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="ff938-392">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="ff938-393">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="ff938-393">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="ff938-394">**page**</span><span class="sxs-lookup"><span data-stu-id="ff938-394">**page**</span></span>

<span data-ttu-id="ff938-395">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-395">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="ff938-396">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="ff938-396">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="ff938-397">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="ff938-397">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="ff938-398">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="ff938-398">**viewimports**</span></span>

<span data-ttu-id="ff938-399">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-399">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="ff938-400">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="ff938-400">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="ff938-401">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="ff938-401">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="ff938-402">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="ff938-402">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="ff938-403">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-403">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-404">**classlib**</span><span class="sxs-lookup"><span data-stu-id="ff938-404">**classlib**</span></span>

<span data-ttu-id="ff938-405">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="ff938-405">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="ff938-406">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="ff938-406">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="ff938-407">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="ff938-407">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="ff938-408">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-408">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-409">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="ff938-409">**mstest, xunit**</span></span>

<span data-ttu-id="ff938-410">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="ff938-410">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="ff938-411">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-411">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-412">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="ff938-412">**globaljson**</span></span>

<span data-ttu-id="ff938-413">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="ff938-413">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="ff938-414">**web**</span><span class="sxs-lookup"><span data-stu-id="ff938-414">**web**</span></span>

<span data-ttu-id="ff938-415">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="ff938-415">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="ff938-416">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-416">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-417">**webapi**</span><span class="sxs-lookup"><span data-stu-id="ff938-417">**webapi**</span></span>

<span data-ttu-id="ff938-418">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff938-418">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="ff938-419">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="ff938-419">The possible values are:</span></span>

- <span data-ttu-id="ff938-420">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="ff938-420">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="ff938-421">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ff938-421">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="ff938-422">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="ff938-422">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="ff938-423">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="ff938-423">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="ff938-424">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-424">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="ff938-425">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-425">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-426">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-426">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="ff938-427">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-427">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="ff938-428">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-428">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-429">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-429">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="ff938-430">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-430">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-431">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-431">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="ff938-432">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-432">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="ff938-433">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-433">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-434">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="ff938-434">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="ff938-435">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ff938-435">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="ff938-436">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-436">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-437">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="ff938-437">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="ff938-438">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-438">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="ff938-439">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-439">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-440">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="ff938-440">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="ff938-441">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="ff938-441">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="ff938-442">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-442">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="ff938-443">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="ff938-443">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="ff938-444">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="ff938-444">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="ff938-445">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-445">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-446">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-446">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-447">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="ff938-447">**mvc, razor**</span></span>

<span data-ttu-id="ff938-448">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff938-448">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="ff938-449">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="ff938-449">The possible values are:</span></span>

- <span data-ttu-id="ff938-450">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="ff938-450">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="ff938-451">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="ff938-451">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="ff938-452">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="ff938-452">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="ff938-453">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="ff938-453">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="ff938-454">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="ff938-454">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="ff938-455">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="ff938-455">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="ff938-456">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-456">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="ff938-457">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-457">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-458">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-458">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="ff938-459">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-459">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="ff938-460">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-460">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-461">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-461">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="ff938-462">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-462">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-463">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-463">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="ff938-464">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-465">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-465">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="ff938-466">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-466">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="ff938-467">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="ff938-467">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="ff938-468">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-468">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="ff938-469">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-469">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="ff938-470">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="ff938-470">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="ff938-471">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="ff938-471">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="ff938-472">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-472">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-473">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="ff938-473">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="ff938-474">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="ff938-474">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="ff938-475">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-475">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="ff938-476">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="ff938-476">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="ff938-477">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="ff938-477">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="ff938-478">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-478">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="ff938-479">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="ff938-479">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="ff938-480">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="ff938-480">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="ff938-481">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="ff938-481">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="ff938-482">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="ff938-482">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="ff938-483">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-483">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="ff938-484">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="ff938-484">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="ff938-485">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="ff938-485">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="ff938-486">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="ff938-486">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="ff938-487">**page**</span><span class="sxs-lookup"><span data-stu-id="ff938-487">**page**</span></span>

<span data-ttu-id="ff938-488">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-488">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="ff938-489">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="ff938-489">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="ff938-490">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="ff938-490">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="ff938-491">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="ff938-491">**viewimports**</span></span>

<span data-ttu-id="ff938-492">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="ff938-492">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="ff938-493">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="ff938-493">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="ff938-494">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="ff938-494">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="ff938-495">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="ff938-495">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="ff938-496">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="ff938-496">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="ff938-497">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="ff938-497">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="ff938-498">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="ff938-498">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="ff938-499">**classlib**</span><span class="sxs-lookup"><span data-stu-id="ff938-499">**classlib**</span></span>

<span data-ttu-id="ff938-500">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="ff938-500">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="ff938-501">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="ff938-501">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="ff938-502">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="ff938-502">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="ff938-503">**mvc**</span><span class="sxs-lookup"><span data-stu-id="ff938-503">**mvc**</span></span>

<span data-ttu-id="ff938-504">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="ff938-504">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="ff938-505">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="ff938-505">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="ff938-506">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="ff938-506">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="ff938-507">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ff938-507">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="ff938-508">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="ff938-508">Values: `None` or `Individual`.</span></span> <span data-ttu-id="ff938-509">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="ff938-509">The default value is `None`.</span></span>

<span data-ttu-id="ff938-510">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="ff938-510">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="ff938-511">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="ff938-511">Values: `true` or `false`.</span></span> <span data-ttu-id="ff938-512">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="ff938-512">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="ff938-513">Exemples</span><span class="sxs-lookup"><span data-stu-id="ff938-513">Examples</span></span>

<span data-ttu-id="ff938-514">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="ff938-514">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="ff938-515">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="ff938-515">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="ff938-516">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification :</span><span class="sxs-lookup"><span data-stu-id="ff938-516">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="ff938-517">Créez une application xUnit :</span><span class="sxs-lookup"><span data-stu-id="ff938-517">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="ff938-518">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="ff938-518">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="ff938-519">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="ff938-519">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="ff938-520">Créez un fichier *global.json* dans le répertoire actif en définissant la version du SDK sur 2.0.0 (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="ff938-520">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="ff938-521">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff938-521">See also</span></span>

* [<span data-ttu-id="ff938-522">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="ff938-522">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="ff938-523">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="ff938-523">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="ff938-524">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="ff938-524">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="ff938-525">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="ff938-525">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
