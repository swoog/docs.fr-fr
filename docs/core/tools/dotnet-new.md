---
title: Commande dotnet new - Interface CLI .NET Core
description: La commande dotnet new crée des projets .NET Core basés sur le modèle spécifié.
author: mairaw
ms.author: mairaw
ms.date: 10/24/2018
ms.openlocfilehash: a8d486f569f31d68d5659ac6a80d615474ef2506
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53131480"
---
# <a name="dotnet-new"></a><span data-ttu-id="d28e4-103">dotnet new</span><span class="sxs-lookup"><span data-stu-id="d28e4-103">dotnet new</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="d28e4-104">Name</span><span class="sxs-lookup"><span data-stu-id="d28e4-104">Name</span></span>

<span data-ttu-id="d28e4-105">`dotnet new` : crée un projet, un fichier de configuration ou une solution en fonction du modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="d28e4-105">`dotnet new` - Creates a new project, configuration file, or solution based on the specified template.</span></span>

## <a name="synopsis"></a><span data-ttu-id="d28e4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d28e4-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="d28e4-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="d28e4-107">.NET Core 2.1</span></span>](#tab/netcore21)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [--nuget-source] [-o|--output]
    [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="d28e4-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="d28e4-108">.NET Core 2.0</span></span>](#tab/netcore20)

```console
dotnet new <TEMPLATE> [--force] [-i|--install] [-lang|--language] [-n|--name] [-o|--output] [-u|--uninstall] [Template options]
dotnet new <TEMPLATE> [-l|--list] [--type]
dotnet new [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="d28e4-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="d28e4-109">.NET Core 1.x</span></span>](#tab/netcore1x)

```console
dotnet new <TEMPLATE> [-lang|--language] [-n|--name] [-o|--output] [-all|--show-all] [-h|--help] [Template options]
dotnet new <TEMPLATE> [-l|--list]
dotnet new [-all|--show-all]
dotnet new [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="d28e4-110">Description</span><span class="sxs-lookup"><span data-stu-id="d28e4-110">Description</span></span>

<span data-ttu-id="d28e4-111">La commande `dotnet new` offre un moyen pratique d’initialiser un projet .NET Core valide.</span><span class="sxs-lookup"><span data-stu-id="d28e4-111">The `dotnet new` command provides a convenient way to initialize a valid .NET Core project.</span></span>

<span data-ttu-id="d28e4-112">La commande appelle le [moteur de modèles](https://github.com/dotnet/templating) pour créer les artefacts sur le disque en fonction du modèle et des options spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d28e4-112">The command calls the [template engine](https://github.com/dotnet/templating) to create the artifacts on disk based on the specified template and options.</span></span>

## <a name="arguments"></a><span data-ttu-id="d28e4-113">Arguments</span><span class="sxs-lookup"><span data-stu-id="d28e4-113">Arguments</span></span>

`TEMPLATE`

<span data-ttu-id="d28e4-114">Modèle à instancier quand la commande est appelée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-114">The template to instantiate when the command is invoked.</span></span> <span data-ttu-id="d28e4-115">Vous pouvez passer des options spécifiques pour chaque modèle.</span><span class="sxs-lookup"><span data-stu-id="d28e4-115">Each template might have specific options you can pass.</span></span> <span data-ttu-id="d28e4-116">Pour plus d'informations, consultez [Options de modèle](#template-options).</span><span class="sxs-lookup"><span data-stu-id="d28e4-116">For more information, see [Template options](#template-options).</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="d28e4-117">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="d28e4-117">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="d28e4-118">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-118">The command contains a default list of templates.</span></span> <span data-ttu-id="d28e4-119">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-119">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="d28e4-120">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.1.300.</span><span class="sxs-lookup"><span data-stu-id="d28e4-120">The following table shows the templates that come pre-installed with the .NET Core SDK 2.1.300.</span></span> <span data-ttu-id="d28e4-121">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="d28e4-121">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="d28e4-122">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-122">Template description</span></span>                          | <span data-ttu-id="d28e4-123">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-123">Template name</span></span>    | <span data-ttu-id="d28e4-124">Langages</span><span class="sxs-lookup"><span data-stu-id="d28e4-124">Languages</span></span>     |
|----------------------------------------------|------------------|---------------|
| <span data-ttu-id="d28e4-125">Application console</span><span class="sxs-lookup"><span data-stu-id="d28e4-125">Console application</span></span>                          | `console`        | <span data-ttu-id="d28e4-126">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-126">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-127">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="d28e4-127">Class library</span></span>                                | `classlib`       | <span data-ttu-id="d28e4-128">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-128">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-129">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="d28e4-129">Unit test project</span></span>                            | `mstest`         | <span data-ttu-id="d28e4-130">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-130">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-131">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="d28e4-131">xUnit test project</span></span>                           | `xunit`          | <span data-ttu-id="d28e4-132">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-132">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-133">Projet de test NUnit</span><span class="sxs-lookup"><span data-stu-id="d28e4-133">NUnit test project</span></span>                           | `nunit`          | <span data-ttu-id="d28e4-134">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-134">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-135">Page Razor</span><span class="sxs-lookup"><span data-stu-id="d28e4-135">Razor page</span></span>                                   | `page`           | <span data-ttu-id="d28e4-136">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-136">[C#]</span></span>          |
| <span data-ttu-id="d28e4-137">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="d28e4-137">MVC ViewImports</span></span>                              | `viewimports`    | <span data-ttu-id="d28e4-138">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-138">[C#]</span></span>          |
| <span data-ttu-id="d28e4-139">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="d28e4-139">MVC ViewStart</span></span>                                | `viewstart`      | <span data-ttu-id="d28e4-140">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-140">[C#]</span></span>          |
| <span data-ttu-id="d28e4-141">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="d28e4-141">ASP.NET Core empty</span></span>                           | `web`            | <span data-ttu-id="d28e4-142">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-142">[C#], F#</span></span>      |
| <span data-ttu-id="d28e4-143">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="d28e4-143">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`            | <span data-ttu-id="d28e4-144">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-144">[C#], F#</span></span>      |
| <span data-ttu-id="d28e4-145">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="d28e4-145">ASP.NET Core Web App</span></span>                         | <span data-ttu-id="d28e4-146">`razor`, `webapp`</span><span class="sxs-lookup"><span data-stu-id="d28e4-146">`razor`, `webapp`</span></span>| <span data-ttu-id="d28e4-147">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-147">[C#]</span></span>          |
| <span data-ttu-id="d28e4-148">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="d28e4-148">ASP.NET Core with Angular</span></span>                    | `angular`        | <span data-ttu-id="d28e4-149">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-149">[C#]</span></span>          |
| <span data-ttu-id="d28e4-150">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="d28e4-150">ASP.NET Core with React.js</span></span>                   | `react`          | <span data-ttu-id="d28e4-151">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-151">[C#]</span></span>          |
| <span data-ttu-id="d28e4-152">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="d28e4-152">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`     | <span data-ttu-id="d28e4-153">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-153">[C#]</span></span>          |
| <span data-ttu-id="d28e4-154">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="d28e4-154">ASP.NET Core Web API</span></span>                         | `webapi`         | <span data-ttu-id="d28e4-155">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-155">[C#], F#</span></span>      |
| <span data-ttu-id="d28e4-156">Bibliothèque de classes Razor</span><span class="sxs-lookup"><span data-stu-id="d28e4-156">Razor class library</span></span>                          | `razorclasslib`  | <span data-ttu-id="d28e4-157">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-157">[C#]</span></span>          |
| <span data-ttu-id="d28e4-158">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="d28e4-158">global.json file</span></span>                             | `globaljson`     |               |
| <span data-ttu-id="d28e4-159">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="d28e4-159">NuGet config</span></span>                                 | `nugetconfig`    |               |
| <span data-ttu-id="d28e4-160">config web</span><span class="sxs-lookup"><span data-stu-id="d28e4-160">Web config</span></span>                                   | `webconfig`      |               |
| <span data-ttu-id="d28e4-161">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="d28e4-161">Solution file</span></span>                                | `sln`            |               |

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="d28e4-162">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="d28e4-162">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="d28e4-163">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-163">The command contains a default list of templates.</span></span> <span data-ttu-id="d28e4-164">Utilisez `dotnet new -l` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-164">Use `dotnet new -l` to obtain a list of the available templates.</span></span> <span data-ttu-id="d28e4-165">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="d28e4-165">The following table shows the templates that come pre-installed with the .NET Core SDK 2.0.</span></span> <span data-ttu-id="d28e4-166">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="d28e4-166">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="d28e4-167">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-167">Template description</span></span>                          | <span data-ttu-id="d28e4-168">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-168">Template name</span></span> | <span data-ttu-id="d28e4-169">Langages</span><span class="sxs-lookup"><span data-stu-id="d28e4-169">Languages</span></span>     |
|----------------------------------------------|---------------|---------------|
| <span data-ttu-id="d28e4-170">Application console</span><span class="sxs-lookup"><span data-stu-id="d28e4-170">Console application</span></span>                          | `console`     | <span data-ttu-id="d28e4-171">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-171">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-172">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="d28e4-172">Class library</span></span>                                | `classlib`    | <span data-ttu-id="d28e4-173">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-173">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-174">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="d28e4-174">Unit test project</span></span>                            | `mstest`      | <span data-ttu-id="d28e4-175">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-175">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-176">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="d28e4-176">xUnit test project</span></span>                           | `xunit`       | <span data-ttu-id="d28e4-177">[C#], F#, VB</span><span class="sxs-lookup"><span data-stu-id="d28e4-177">[C#], F#, VB</span></span>  |
| <span data-ttu-id="d28e4-178">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="d28e4-178">ASP.NET Core empty</span></span>                           | `web`         | <span data-ttu-id="d28e4-179">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-179">[C#], F#</span></span>      |
| <span data-ttu-id="d28e4-180">Application web ASP.NET Core (Model-View-Controller)</span><span class="sxs-lookup"><span data-stu-id="d28e4-180">ASP.NET Core Web App (Model-View-Controller)</span></span> | `mvc`         | <span data-ttu-id="d28e4-181">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-181">[C#], F#</span></span>      |
| <span data-ttu-id="d28e4-182">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="d28e4-182">ASP.NET Core Web App</span></span>                         | `razor`       | <span data-ttu-id="d28e4-183">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-183">[C#]</span></span>          |
| <span data-ttu-id="d28e4-184">ASP.NET Core avec Angular</span><span class="sxs-lookup"><span data-stu-id="d28e4-184">ASP.NET Core with Angular</span></span>                    | `angular`     | <span data-ttu-id="d28e4-185">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-185">[C#]</span></span>          |
| <span data-ttu-id="d28e4-186">ASP.NET Core avec React.js</span><span class="sxs-lookup"><span data-stu-id="d28e4-186">ASP.NET Core with React.js</span></span>                   | `react`       | <span data-ttu-id="d28e4-187">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-187">[C#]</span></span>          |
| <span data-ttu-id="d28e4-188">ASP.NET Core avec React.js et Redux</span><span class="sxs-lookup"><span data-stu-id="d28e4-188">ASP.NET Core with React.js and Redux</span></span>         | `reactredux`  | <span data-ttu-id="d28e4-189">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-189">[C#]</span></span>          |
| <span data-ttu-id="d28e4-190">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="d28e4-190">ASP.NET Core Web API</span></span>                         | `webapi`      | <span data-ttu-id="d28e4-191">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-191">[C#], F#</span></span>      |
| <span data-ttu-id="d28e4-192">fichier global.json</span><span class="sxs-lookup"><span data-stu-id="d28e4-192">global.json file</span></span>                             | `globaljson`  |               |
| <span data-ttu-id="d28e4-193">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="d28e4-193">NuGet config</span></span>                                 | `nugetconfig` |               |
| <span data-ttu-id="d28e4-194">config web</span><span class="sxs-lookup"><span data-stu-id="d28e4-194">Web config</span></span>                                   | `webconfig`   |               |
| <span data-ttu-id="d28e4-195">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="d28e4-195">Solution file</span></span>                                | `sln`         |               |
| <span data-ttu-id="d28e4-196">Page Razor</span><span class="sxs-lookup"><span data-stu-id="d28e4-196">Razor page</span></span>                                   | `page`        |               |
| <span data-ttu-id="d28e4-197">ViewImports MVC</span><span class="sxs-lookup"><span data-stu-id="d28e4-197">MVC ViewImports</span></span>                              | `viewimports` |               |
| <span data-ttu-id="d28e4-198">ViewStart MVC</span><span class="sxs-lookup"><span data-stu-id="d28e4-198">MVC ViewStart</span></span>                                | `viewstart`   |               |

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="d28e4-199">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="d28e4-199">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="d28e4-200">La commande contient une liste par défaut de modèles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-200">The command contains a default list of templates.</span></span> <span data-ttu-id="d28e4-201">Utilisez `dotnet new -all` pour obtenir une liste des modèles disponibles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-201">Use `dotnet new -all` to obtain a list of the available templates.</span></span> <span data-ttu-id="d28e4-202">Le tableau suivant présente les modèles préinstallés avec le SDK .NET Core 1.x.</span><span class="sxs-lookup"><span data-stu-id="d28e4-202">The following table shows the templates that come pre-installed with the .NET Core SDK 1.x.</span></span> <span data-ttu-id="d28e4-203">Le langage par défaut pour le modèle est indiqué entre crochets.</span><span class="sxs-lookup"><span data-stu-id="d28e4-203">The default language for the template is shown inside the brackets.</span></span>

|<span data-ttu-id="d28e4-204">Description du modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-204">Template description</span></span>  | <span data-ttu-id="d28e4-205">Nom du modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-205">Template name</span></span> | <span data-ttu-id="d28e4-206">Langages</span><span class="sxs-lookup"><span data-stu-id="d28e4-206">Languages</span></span> |
|----------------------|---------------|-----------|
| <span data-ttu-id="d28e4-207">Application console</span><span class="sxs-lookup"><span data-stu-id="d28e4-207">Console application</span></span>  | `console`     | <span data-ttu-id="d28e4-208">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-208">[C#], F#</span></span>  |
| <span data-ttu-id="d28e4-209">Bibliothèque de classes</span><span class="sxs-lookup"><span data-stu-id="d28e4-209">Class library</span></span>        | `classlib`    | <span data-ttu-id="d28e4-210">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-210">[C#], F#</span></span>  |
| <span data-ttu-id="d28e4-211">Projet de test unitaire</span><span class="sxs-lookup"><span data-stu-id="d28e4-211">Unit test project</span></span>    | `mstest`      | <span data-ttu-id="d28e4-212">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-212">[C#], F#</span></span>  |
| <span data-ttu-id="d28e4-213">Projet de test xUnit</span><span class="sxs-lookup"><span data-stu-id="d28e4-213">xUnit test project</span></span>   | `xunit`       | <span data-ttu-id="d28e4-214">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-214">[C#], F#</span></span>  |
| <span data-ttu-id="d28e4-215">ASP.NET Core vide</span><span class="sxs-lookup"><span data-stu-id="d28e4-215">ASP.NET Core empty</span></span>   | `web`         | <span data-ttu-id="d28e4-216">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-216">[C#]</span></span>      |
| <span data-ttu-id="d28e4-217">Application web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="d28e4-217">ASP.NET Core Web App</span></span> | `mvc`         | <span data-ttu-id="d28e4-218">[C#], F#</span><span class="sxs-lookup"><span data-stu-id="d28e4-218">[C#], F#</span></span>  |
| <span data-ttu-id="d28e4-219">API web ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="d28e4-219">ASP.NET Core Web API</span></span> | `webapi`      | <span data-ttu-id="d28e4-220">[C#]</span><span class="sxs-lookup"><span data-stu-id="d28e4-220">[C#]</span></span>      |
| <span data-ttu-id="d28e4-221">Configuration NuGet</span><span class="sxs-lookup"><span data-stu-id="d28e4-221">NuGet config</span></span>         | `nugetconfig` |           |
| <span data-ttu-id="d28e4-222">config web</span><span class="sxs-lookup"><span data-stu-id="d28e4-222">Web config</span></span>           | `webconfig`   |           |
| <span data-ttu-id="d28e4-223">Fichier solution</span><span class="sxs-lookup"><span data-stu-id="d28e4-223">Solution file</span></span>        | `sln`         |           |

---

## <a name="options"></a><span data-ttu-id="d28e4-224">Options</span><span class="sxs-lookup"><span data-stu-id="d28e4-224">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="d28e4-225">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="d28e4-225">.NET Core 2.1</span></span>](#tab/netcore21)

`--force`

<span data-ttu-id="d28e4-226">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="d28e4-226">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="d28e4-227">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-227">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="d28e4-228">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="d28e4-228">Prints out help for the command.</span></span> <span data-ttu-id="d28e4-229">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-229">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="d28e4-230">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="d28e4-230">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="d28e4-231">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-231">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="d28e4-232">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="d28e4-232">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="d28e4-233">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="d28e4-233">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="d28e4-234">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-234">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="d28e4-235">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="d28e4-235">Lists templates containing the specified name.</span></span> <span data-ttu-id="d28e4-236">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-236">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="d28e4-237">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-237">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="d28e4-238">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="d28e4-238">The language of the template to create.</span></span> <span data-ttu-id="d28e4-239">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="d28e4-239">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="d28e4-240">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-240">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="d28e4-241">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="d28e4-241">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="d28e4-242">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-242">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="d28e4-243">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-243">The name for the created output.</span></span> <span data-ttu-id="d28e4-244">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d28e4-244">If no name is specified, the name of the current directory is used.</span></span>

`--nuget-source`

<span data-ttu-id="d28e4-245">Spécifie une source NuGet à utiliser pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="d28e4-245">Specifies a NuGet source to use during install.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="d28e4-246">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-246">Location to place the generated output.</span></span> <span data-ttu-id="d28e4-247">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="d28e4-247">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="d28e4-248">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-248">Filters templates based on available types.</span></span> <span data-ttu-id="d28e4-249">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="d28e4-249">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="d28e4-250">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="d28e4-250">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="d28e4-251">Pour désinstaller un modèle à l’aide de `PATH`, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-251">To uninstall a template using a `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="d28e4-252">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="d28e4-252">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span>
> <span data-ttu-id="d28e4-253">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="d28e4-253">Additionally, do not include a final terminating directory slash on your template path.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="d28e4-254">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="d28e4-254">.NET Core 2.0</span></span>](#tab/netcore20)

`--force`

<span data-ttu-id="d28e4-255">Force le contenu à être généré même s’il change les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="d28e4-255">Forces content to be generated even if it would change existing files.</span></span> <span data-ttu-id="d28e4-256">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-256">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="d28e4-257">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="d28e4-257">Prints out help for the command.</span></span> <span data-ttu-id="d28e4-258">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-258">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-i|--install <PATH|NUGET_ID>`

<span data-ttu-id="d28e4-259">Installe un pack source ou de modèle à partir du `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="d28e4-259">Installs a source or template pack from the `PATH` or `NUGET_ID` provided.</span></span> <span data-ttu-id="d28e4-260">Si vous souhaitez installer une préversion d’un package de modèle, vous devez spécifier la version au format `<package-name>::<package-version>`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-260">If you want to install a prerelease version of a template package, you need to specify the version in the format of `<package-name>::<package-version>`.</span></span> <span data-ttu-id="d28e4-261">Par défaut, `dotnet new` passe \* pour la version, qui représente la dernière version stable du package.</span><span class="sxs-lookup"><span data-stu-id="d28e4-261">By default, `dotnet new` passes \* for the version, which represents the last stable package version.</span></span> <span data-ttu-id="d28e4-262">Consultez un exemple dans la section [Exemples](#examples).</span><span class="sxs-lookup"><span data-stu-id="d28e4-262">See an example at the [Examples](#examples) section.</span></span>

<span data-ttu-id="d28e4-263">Pour plus d’informations sur la création de modèles personnalisés, consultez [Modèles personnalisés pour dotnet new](custom-templates.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-263">For information on creating custom templates, see [Custom templates for dotnet new](custom-templates.md).</span></span>

`-l|--list`

<span data-ttu-id="d28e4-264">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="d28e4-264">Lists templates containing the specified name.</span></span> <span data-ttu-id="d28e4-265">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-265">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="d28e4-266">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-266">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#|VB}`

<span data-ttu-id="d28e4-267">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="d28e4-267">The language of the template to create.</span></span> <span data-ttu-id="d28e4-268">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="d28e4-268">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="d28e4-269">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-269">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="d28e4-270">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="d28e4-270">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="d28e4-271">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-271">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="d28e4-272">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-272">The name for the created output.</span></span> <span data-ttu-id="d28e4-273">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d28e4-273">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="d28e4-274">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-274">Location to place the generated output.</span></span> <span data-ttu-id="d28e4-275">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="d28e4-275">The default is the current directory.</span></span>

`--type`

<span data-ttu-id="d28e4-276">Filtre les modèles en fonction des types disponibles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-276">Filters templates based on available types.</span></span> <span data-ttu-id="d28e4-277">Les valeurs prédéfinies sont « project », « item » ou « other ».</span><span class="sxs-lookup"><span data-stu-id="d28e4-277">Predefined values are "project", "item" or "other".</span></span>

`-u|--uninstall <PATH|NUGET_ID>`

<span data-ttu-id="d28e4-278">Désinstalle un pack source ou de modèle au `PATH` ou `NUGET_ID` fourni.</span><span class="sxs-lookup"><span data-stu-id="d28e4-278">Uninstalls a source or template pack at the `PATH` or `NUGET_ID` provided.</span></span>

> [!NOTE]
> <span data-ttu-id="d28e4-279">Pour désinstaller un modèle à l’aide de `PATH` source, vous devez qualifier le chemin d’accès avec un nom complet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-279">To uninstall a template using a source `PATH`, you need to fully qualify the path.</span></span> <span data-ttu-id="d28e4-280">Par exemple, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* fonctionne, mais *./GarciaSoftware.ConsoleTemplate.CSharp* à partir du dossier conteneur ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="d28e4-280">For example, *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp* will work, but *./GarciaSoftware.ConsoleTemplate.CSharp* from the containing folder will not.</span></span> <span data-ttu-id="d28e4-281">En outre, n’incluez pas de barre oblique finale après le répertoire dans votre chemin d’accès au modèle.</span><span class="sxs-lookup"><span data-stu-id="d28e4-281">Additionally, do not include a final terminating directory slash on your template path.</span></span>
> 
> <span data-ttu-id="d28e4-282">Si vous ne parvenez pas à déterminer l’argument `PATH` ou `NUGET_ID` nécessaire pour désinstaller un modèle, l’exécution de `dotnet new --uninstall` sans argument répertorie tous les modèles installés et l’argument requis pour les désinstaller.</span><span class="sxs-lookup"><span data-stu-id="d28e4-282">If you are unable to determine the `PATH` or `NUGET_ID` argument needed to uninstall a template, running `dotnet new --uninstall` without an argument will list all installed templates and the argument required to uninstall them.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="d28e4-283">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="d28e4-283">.NET Core 1.x</span></span>](#tab/netcore1x)

`-all|--show-all`

<span data-ttu-id="d28e4-284">Affiche tous les modèles pour un type de projet spécifique lors de l’exécution dans le contexte de la commande `dotnet new` seule.</span><span class="sxs-lookup"><span data-stu-id="d28e4-284">Shows all templates for a specific type of project when running in the context of the `dotnet new` command alone.</span></span> <span data-ttu-id="d28e4-285">Lors de l’exécution dans le contexte d’un modèle spécifique, comme `dotnet new web -all`, `-all` est interprété comme un indicateur de création forcée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-285">When running in the context of a specific template, such as `dotnet new web -all`, `-all` is interpreted as a force creation flag.</span></span> <span data-ttu-id="d28e4-286">Ceci est nécessaire quand le répertoire de sortie contient déjà un projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-286">This is required when the output directory already contains a project.</span></span>

`-h|--help`

<span data-ttu-id="d28e4-287">Affiche l’aide pour la commande.</span><span class="sxs-lookup"><span data-stu-id="d28e4-287">Prints out help for the command.</span></span> <span data-ttu-id="d28e4-288">Elle peut être appelée pour la commande `dotnet new` elle-même ou pour n’importe quel modèle, par exemple, `dotnet new mvc --help`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-288">It can be invoked for the `dotnet new` command itself or for any template, such as `dotnet new mvc --help`.</span></span>

`-l|--list`

<span data-ttu-id="d28e4-289">Liste les modèles contenant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="d28e4-289">Lists templates containing the specified name.</span></span> <span data-ttu-id="d28e4-290">Si elle est appelée pour la commande `dotnet new`, elle liste les modèles disponibles dans le répertoire donné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-290">If invoked for the `dotnet new` command, it lists the possible templates available for the given directory.</span></span> <span data-ttu-id="d28e4-291">Par exemple, si le répertoire contient déjà un projet, elle ne liste pas tous les modèles de projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-291">For example if the directory already contains a project, it doesn't list all project templates.</span></span>

`-lang|--language {C#|F#}`

<span data-ttu-id="d28e4-292">Langage du modèle à créer.</span><span class="sxs-lookup"><span data-stu-id="d28e4-292">The language of the template to create.</span></span> <span data-ttu-id="d28e4-293">Le langage accepté diffère selon le modèle (voir les valeurs par défaut dans la section [arguments](#arguments)).</span><span class="sxs-lookup"><span data-stu-id="d28e4-293">The language accepted varies by the template (see defaults in the [arguments](#arguments) section).</span></span> <span data-ttu-id="d28e4-294">Non valide pour certains modèles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-294">Not valid for some templates.</span></span>

> [!NOTE]
> <span data-ttu-id="d28e4-295">Certains interpréteurs interprètent la commande `#` comme un caractère spécial.</span><span class="sxs-lookup"><span data-stu-id="d28e4-295">Some shells interpret `#` as a special character.</span></span> <span data-ttu-id="d28e4-296">Dans ce cas, vous devez placer la valeur de paramètre de langage entre guillemets doubles, par exemple `dotnet new console -lang "F#"`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-296">In those cases, you need to enclose the language parameter value, such as `dotnet new console -lang "F#"`.</span></span>

`-n|--name <OUTPUT_NAME>`

<span data-ttu-id="d28e4-297">Le nom de la sortie créée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-297">The name for the created output.</span></span> <span data-ttu-id="d28e4-298">Si aucun nom n’est spécifié, le nom du répertoire actif est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d28e4-298">If no name is specified, the name of the current directory is used.</span></span>

`-o|--output <OUTPUT_DIRECTORY>`

<span data-ttu-id="d28e4-299">Emplacement où placer la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-299">Location to place the generated output.</span></span> <span data-ttu-id="d28e4-300">La valeur par défaut correspond au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="d28e4-300">The default is the current directory.</span></span>

---

## <a name="template-options"></a><span data-ttu-id="d28e4-301">Options de modèle</span><span class="sxs-lookup"><span data-stu-id="d28e4-301">Template options</span></span>

<span data-ttu-id="d28e4-302">Chaque modèle de projet peut présenter d’autres options disponibles.</span><span class="sxs-lookup"><span data-stu-id="d28e4-302">Each project template may have additional options available.</span></span> <span data-ttu-id="d28e4-303">Les modèles de base ont les options supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="d28e4-303">The core templates have the following additional options:</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="d28e4-304">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="d28e4-304">.NET Core 2.1</span></span>](#tab/netcore21)

<span data-ttu-id="d28e4-305">**console, angular, react, reactredux, razorclasslib**</span><span class="sxs-lookup"><span data-stu-id="d28e4-305">**console, angular, react, reactredux, razorclasslib**</span></span>

  <span data-ttu-id="d28e4-306">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-306">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-307">**classlib**</span><span class="sxs-lookup"><span data-stu-id="d28e4-307">**classlib**</span></span>

<span data-ttu-id="d28e4-308">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="d28e4-308">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="d28e4-309">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="d28e4-309">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="d28e4-310">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-310">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="d28e4-311">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-311">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-312">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="d28e4-312">**mstest, xunit**</span></span>

<span data-ttu-id="d28e4-313">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-313">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="d28e4-314">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-314">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-315">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="d28e4-315">**globaljson**</span></span>

<span data-ttu-id="d28e4-316">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="d28e4-316">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="d28e4-317">**web**</span><span class="sxs-lookup"><span data-stu-id="d28e4-317">**web**</span></span>

<span data-ttu-id="d28e4-318">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-318">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="d28e4-319">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-319">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-320">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d28e4-320">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="d28e4-321">Cette option s’applique uniquement si `IndividualAuth` ou `OrganizationalAuth` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="d28e4-321">This option only applies if `IndividualAuth` or `OrganizationalAuth` are not being used.</span></span>

<span data-ttu-id="d28e4-322">**webapi**</span><span class="sxs-lookup"><span data-stu-id="d28e4-322">**webapi**</span></span>

<span data-ttu-id="d28e4-323">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d28e4-323">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="d28e4-324">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="d28e4-324">The possible values are:</span></span>

- <span data-ttu-id="d28e4-325">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="d28e4-325">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="d28e4-326">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="d28e4-326">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="d28e4-327">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-327">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="d28e4-328">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="d28e4-328">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="d28e4-329">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-329">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="d28e4-330">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-330">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-331">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-331">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="d28e4-332">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-332">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="d28e4-333">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-333">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-334">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-334">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="d28e4-335">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-335">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-336">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-336">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="d28e4-337">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-337">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="d28e4-338">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-338">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-339">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-339">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="d28e4-340">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-340">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="d28e4-341">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-341">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-342">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-342">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="d28e4-343">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-343">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="d28e4-344">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-344">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-345">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-345">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="d28e4-346">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-346">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="d28e4-347">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-347">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="d28e4-348">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-348">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="d28e4-349">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="d28e4-349">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="d28e4-350">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-350">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-351">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-351">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-352">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d28e4-352">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="d28e4-353">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-353">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="d28e4-354">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="d28e4-354">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="d28e4-355">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="d28e4-355">**mvc, razor**</span></span>

<span data-ttu-id="d28e4-356">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d28e4-356">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="d28e4-357">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="d28e4-357">The possible values are:</span></span>

- <span data-ttu-id="d28e4-358">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="d28e4-358">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="d28e4-359">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="d28e4-359">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="d28e4-360">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="d28e4-360">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="d28e4-361">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-361">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="d28e4-362">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="d28e4-362">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="d28e4-363">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="d28e4-363">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="d28e4-364">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-364">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="d28e4-365">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-365">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-366">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-366">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="d28e4-367">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-367">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="d28e4-368">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-368">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-369">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-369">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="d28e4-370">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-370">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-371">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-371">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="d28e4-372">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-372">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-373">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-373">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="d28e4-374">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-374">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="d28e4-375">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-375">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="d28e4-376">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-376">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="d28e4-377">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-377">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="d28e4-378">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-378">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="d28e4-379">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-379">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="d28e4-380">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-380">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-381">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-381">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="d28e4-382">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-382">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="d28e4-383">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-383">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-384">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-384">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="d28e4-385">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="d28e4-385">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="d28e4-386">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-386">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-387">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-387">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="d28e4-388">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-388">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="d28e4-389">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-389">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="d28e4-390">`--exclude-launch-settings` - Exclure *launchSettings.json* du modèle généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-390">`--exclude-launch-settings` - Exclude *launchSettings.json* from the generated template.</span></span>

<span data-ttu-id="d28e4-391">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-391">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="d28e4-392">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="d28e4-392">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="d28e4-393">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-393">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-394">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-394">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-395">`--no-https` - Le projet ne nécessite pas le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d28e4-395">`--no-https` - Project doesn't require HTTPS.</span></span> <span data-ttu-id="d28e4-396">`app.UseHsts` et `app.UseHttpsRedirection` ne sont pas ajoutés à `Startup.Configure`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-396">`app.UseHsts` and `app.UseHttpsRedirection` aren't added to `Startup.Configure`.</span></span> <span data-ttu-id="d28e4-397">Cette option s’applique uniquement si `Individual`, `IndividualB2C`, `SingleOrg` ou `MultiOrg` ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="d28e4-397">This option only applies if `Individual`, `IndividualB2C`, `SingleOrg`, or `MultiOrg` aren't being used.</span></span>

<span data-ttu-id="d28e4-398">**page**</span><span class="sxs-lookup"><span data-stu-id="d28e4-398">**page**</span></span>

<span data-ttu-id="d28e4-399">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-399">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="d28e4-400">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-400">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="d28e4-401">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="d28e4-401">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="d28e4-402">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="d28e4-402">**viewimports**</span></span>

<span data-ttu-id="d28e4-403">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-403">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="d28e4-404">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-404">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="d28e4-405">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="d28e4-405">.NET Core 2.0</span></span>](#tab/netcore20)

<span data-ttu-id="d28e4-406">**console, angular, react, reactredux**</span><span class="sxs-lookup"><span data-stu-id="d28e4-406">**console, angular, react, reactredux**</span></span>

  <span data-ttu-id="d28e4-407">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-407">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-408">**classlib**</span><span class="sxs-lookup"><span data-stu-id="d28e4-408">**classlib**</span></span>

<span data-ttu-id="d28e4-409">`-f|--framework <FRAMEWORK>` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="d28e4-409">`-f|--framework <FRAMEWORK>` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="d28e4-410">Valeurs : `netcoreapp2.0` pour créer une bibliothèque de classes .NET Core ou `netstandard2.0` pour créer une bibliothèque de classes .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="d28e4-410">Values: `netcoreapp2.0` to create a .NET Core Class Library or `netstandard2.0` to create a .NET Standard Class Library.</span></span> <span data-ttu-id="d28e4-411">La valeur par défaut est `netstandard2.0`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-411">The default value is `netstandard2.0`.</span></span>

<span data-ttu-id="d28e4-412">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-412">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-413">**mstest, xunit**</span><span class="sxs-lookup"><span data-stu-id="d28e4-413">**mstest, xunit**</span></span>

<span data-ttu-id="d28e4-414">`-p|--enable-pack` : permet l’empaquetage pour le projet à l’aide de [dotnet pack](dotnet-pack.md).</span><span class="sxs-lookup"><span data-stu-id="d28e4-414">`-p|--enable-pack` - Enables packaging for the project using [dotnet pack](dotnet-pack.md).</span></span>

<span data-ttu-id="d28e4-415">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-415">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-416">**globaljson**</span><span class="sxs-lookup"><span data-stu-id="d28e4-416">**globaljson**</span></span>

<span data-ttu-id="d28e4-417">`--sdk-version <VERSION_NUMBER>` : spécifie la version du SDK .NET Core à utiliser dans le fichier *global.json*.</span><span class="sxs-lookup"><span data-stu-id="d28e4-417">`--sdk-version <VERSION_NUMBER>` - Specifies the version of the .NET Core SDK to use in the *global.json* file.</span></span>

<span data-ttu-id="d28e4-418">**web**</span><span class="sxs-lookup"><span data-stu-id="d28e4-418">**web**</span></span>

<span data-ttu-id="d28e4-419">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-419">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="d28e4-420">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-420">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-421">**webapi**</span><span class="sxs-lookup"><span data-stu-id="d28e4-421">**webapi**</span></span>

<span data-ttu-id="d28e4-422">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d28e4-422">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="d28e4-423">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="d28e4-423">The possible values are:</span></span>

- <span data-ttu-id="d28e4-424">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="d28e4-424">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="d28e4-425">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="d28e4-425">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="d28e4-426">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-426">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="d28e4-427">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="d28e4-427">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="d28e4-428">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-428">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="d28e4-429">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-429">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-430">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-430">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="d28e4-431">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-431">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="d28e4-432">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-432">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-433">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-433">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="d28e4-434">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-434">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-435">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-435">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="d28e4-436">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-436">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="d28e4-437">À utiliser avec l’authentification `IndividualB2C` ou `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-437">Use with `IndividualB2C` or `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-438">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-438">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="d28e4-439">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-439">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="d28e4-440">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-440">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-441">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-441">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="d28e4-442">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-442">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="d28e4-443">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-443">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-444">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-444">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="d28e4-445">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-445">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="d28e4-446">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-446">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="d28e4-447">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-447">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="d28e4-448">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="d28e4-448">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="d28e4-449">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-449">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-450">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-450">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-451">**mvc, razor**</span><span class="sxs-lookup"><span data-stu-id="d28e4-451">**mvc, razor**</span></span>

<span data-ttu-id="d28e4-452">`-au|--auth <AUTHENTICATION_TYPE>` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d28e4-452">`-au|--auth <AUTHENTICATION_TYPE>` - The type of authentication to use.</span></span> <span data-ttu-id="d28e4-453">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="d28e4-453">The possible values are:</span></span>

- <span data-ttu-id="d28e4-454">`None` : aucune authentification (configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="d28e4-454">`None` - No authentication (Default).</span></span>
- <span data-ttu-id="d28e4-455">`Individual` : authentification individuelle.</span><span class="sxs-lookup"><span data-stu-id="d28e4-455">`Individual` - Individual authentication.</span></span>
- <span data-ttu-id="d28e4-456">`IndividualB2C` : authentification individuelle avec Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="d28e4-456">`IndividualB2C` - Individual authentication with Azure AD B2C.</span></span>
- <span data-ttu-id="d28e4-457">`SingleOrg` : authentification d’organisation pour un seul abonné.</span><span class="sxs-lookup"><span data-stu-id="d28e4-457">`SingleOrg` - Organizational authentication for a single tenant.</span></span>
- <span data-ttu-id="d28e4-458">`MultiOrg` : authentification d’organisation pour plusieurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="d28e4-458">`MultiOrg` - Organizational authentication for multiple tenants.</span></span>
- <span data-ttu-id="d28e4-459">`Windows` : authentification Windows.</span><span class="sxs-lookup"><span data-stu-id="d28e4-459">`Windows` - Windows authentication.</span></span>

<span data-ttu-id="d28e4-460">`--aad-b2c-instance <INSTANCE>` : instance d’Azure Active Directory B2C à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-460">`--aad-b2c-instance <INSTANCE>` - The Azure Active Directory B2C instance to connect to.</span></span> <span data-ttu-id="d28e4-461">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-461">Use with `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-462">La valeur par défaut est `https://login.microsoftonline.com/tfp/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-462">The default value is `https://login.microsoftonline.com/tfp/`.</span></span>

<span data-ttu-id="d28e4-463">`-ssp|--susi-policy-id <ID>` : ID de la stratégie de connexion et d’inscription pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-463">`-ssp|--susi-policy-id <ID>` - The sign-in and sign-up policy ID for this project.</span></span> <span data-ttu-id="d28e4-464">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-464">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-465">`-rp|--reset-password-policy-id <ID>` : ID de stratégie de réinitialisation du mot de passe pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-465">`-rp|--reset-password-policy-id <ID>` - The reset password policy ID for this project.</span></span> <span data-ttu-id="d28e4-466">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-466">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-467">`-ep|--edit-profile-policy-id <ID>` : ID de stratégie de modification du profil pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-467">`-ep|--edit-profile-policy-id <ID>` - The edit profile policy ID for this project.</span></span> <span data-ttu-id="d28e4-468">À utiliser avec l’authentification `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-468">Use with `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-469">`--aad-instance <INSTANCE>` : instance d’Azure Active Directory à laquelle se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-469">`--aad-instance <INSTANCE>` - The Azure Active Directory instance to connect to.</span></span> <span data-ttu-id="d28e4-470">À utiliser avec l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-470">Use with `SingleOrg` or `MultiOrg` authentication.</span></span> <span data-ttu-id="d28e4-471">La valeur par défaut est `https://login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-471">The default value is `https://login.microsoftonline.com/`.</span></span>

<span data-ttu-id="d28e4-472">`--client-id <ID>` : ID client pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-472">`--client-id <ID>` - The Client ID for this project.</span></span> <span data-ttu-id="d28e4-473">À utiliser avec l’authentification `IndividualB2C`, `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-473">Use with `IndividualB2C`, `SingleOrg`, or `MultiOrg` authentication.</span></span> <span data-ttu-id="d28e4-474">La valeur par défaut est `11111111-1111-1111-11111111111111111`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-474">The default value is `11111111-1111-1111-11111111111111111`.</span></span>

<span data-ttu-id="d28e4-475">`--domain <DOMAIN>` : domaine de l’abonné d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-475">`--domain <DOMAIN>` - The domain for the directory tenant.</span></span> <span data-ttu-id="d28e4-476">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-476">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-477">La valeur par défaut est `qualified.domain.name`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-477">The default value is `qualified.domain.name`.</span></span>

<span data-ttu-id="d28e4-478">`--tenant-id <ID>` : ID d’abonné de l’annuaire auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="d28e4-478">`--tenant-id <ID>` - The TenantId ID of the directory to connect to.</span></span> <span data-ttu-id="d28e4-479">À utiliser avec l’authentification `SingleOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-479">Use with `SingleOrg` authentication.</span></span> <span data-ttu-id="d28e4-480">La valeur par défaut est `22222222-2222-2222-2222-222222222222`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-480">The default value is `22222222-2222-2222-2222-222222222222`.</span></span>

<span data-ttu-id="d28e4-481">`--callback-path <PATH>` : chemin de demande dans le chemin de base de l’application de l’URI de redirection.</span><span class="sxs-lookup"><span data-stu-id="d28e4-481">`--callback-path <PATH>` - The request path within the application's base path of the redirect URI.</span></span> <span data-ttu-id="d28e4-482">À utiliser avec l’authentification `SingleOrg` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-482">Use with `SingleOrg` or `IndividualB2C` authentication.</span></span> <span data-ttu-id="d28e4-483">La valeur par défaut est `/signin-oidc`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-483">The default value is `/signin-oidc`.</span></span>

<span data-ttu-id="d28e4-484">`-r|--org-read-access` : accorde à cette application un accès en lecture au répertoire.</span><span class="sxs-lookup"><span data-stu-id="d28e4-484">`-r|--org-read-access` - Allows this application read-access to the directory.</span></span> <span data-ttu-id="d28e4-485">S’applique uniquement à l’authentification `SingleOrg` ou `MultiOrg`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-485">Only applies to `SingleOrg` or `MultiOrg` authentication.</span></span>

<span data-ttu-id="d28e4-486">`--use-launch-settings` : inclut *launchSettings.json* dans la sortie de modèle générée.</span><span class="sxs-lookup"><span data-stu-id="d28e4-486">`--use-launch-settings` - Includes *launchSettings.json* in the generated template output.</span></span>

<span data-ttu-id="d28e4-487">`--use-browserlink` : inclut BrowserLink dans le projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-487">`--use-browserlink` - Includes BrowserLink in the project.</span></span>

<span data-ttu-id="d28e4-488">`-uld|--use-local-db` : spécifie que la base de données locale doit être utilisée à la place de SQLite.</span><span class="sxs-lookup"><span data-stu-id="d28e4-488">`-uld|--use-local-db` - Specifies LocalDB should be used instead of SQLite.</span></span> <span data-ttu-id="d28e4-489">S’applique uniquement à l’authentification `Individual` ou `IndividualB2C`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-489">Only applies to `Individual` or `IndividualB2C` authentication.</span></span>

<span data-ttu-id="d28e4-490">`--no-restore` - N’exécute aucune restauration implicite pendant la création du projet.</span><span class="sxs-lookup"><span data-stu-id="d28e4-490">`--no-restore` - Doesn't execute an implicit restore during project creation.</span></span>

<span data-ttu-id="d28e4-491">**page**</span><span class="sxs-lookup"><span data-stu-id="d28e4-491">**page**</span></span>

<span data-ttu-id="d28e4-492">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-492">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="d28e4-493">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-493">The default value is `MyApp.Namespace`.</span></span>

<span data-ttu-id="d28e4-494">`-np|--no-pagemodel` : crée la page sans modèle de page.</span><span class="sxs-lookup"><span data-stu-id="d28e4-494">`-np|--no-pagemodel` - Creates the page without a PageModel.</span></span>

<span data-ttu-id="d28e4-495">**viewimports**</span><span class="sxs-lookup"><span data-stu-id="d28e4-495">**viewimports**</span></span>

<span data-ttu-id="d28e4-496">`-na|--namespace <NAMESPACE_NAME>` : espace de noms pour le code généré.</span><span class="sxs-lookup"><span data-stu-id="d28e4-496">`-na|--namespace <NAMESPACE_NAME>`- Namespace for the generated code.</span></span> <span data-ttu-id="d28e4-497">La valeur par défaut est `MyApp.Namespace`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-497">The default value is `MyApp.Namespace`.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="d28e4-498">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="d28e4-498">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="d28e4-499">**console, xunit, mstest, web, webapi**</span><span class="sxs-lookup"><span data-stu-id="d28e4-499">**console, xunit, mstest, web, webapi**</span></span>

<span data-ttu-id="d28e4-500">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="d28e4-500">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="d28e4-501">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-501">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="d28e4-502">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-502">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="d28e4-503">**classlib**</span><span class="sxs-lookup"><span data-stu-id="d28e4-503">**classlib**</span></span>

<span data-ttu-id="d28e4-504">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="d28e4-504">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="d28e4-505">Valeurs : `netcoreapp1.0`, `netcoreapp1.1` ou `netstandard1.0` à `netstandard1.6`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-505">Values: `netcoreapp1.0`, `netcoreapp1.1`, or `netstandard1.0` to `netstandard1.6`.</span></span> <span data-ttu-id="d28e4-506">La valeur par défaut est `netstandard1.4`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-506">The default value is `netstandard1.4`.</span></span>

<span data-ttu-id="d28e4-507">**mvc**</span><span class="sxs-lookup"><span data-stu-id="d28e4-507">**mvc**</span></span>

<span data-ttu-id="d28e4-508">`-f|--framework` : spécifie le [framework](../../standard/frameworks.md) à cibler.</span><span class="sxs-lookup"><span data-stu-id="d28e4-508">`-f|--framework` - Specifies the [framework](../../standard/frameworks.md) to target.</span></span> <span data-ttu-id="d28e4-509">Valeurs : `netcoreapp1.0` ou `netcoreapp1.1`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-509">Values: `netcoreapp1.0` or `netcoreapp1.1`.</span></span> <span data-ttu-id="d28e4-510">La valeur par défaut est `netcoreapp1.0`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-510">The default value is `netcoreapp1.0`.</span></span>

<span data-ttu-id="d28e4-511">`-au|--auth` : type d’authentification à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d28e4-511">`-au|--auth` - The type of authentication to use.</span></span> <span data-ttu-id="d28e4-512">Valeurs : `None` ou `Individual`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-512">Values: `None` or `Individual`.</span></span> <span data-ttu-id="d28e4-513">La valeur par défaut est `None`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-513">The default value is `None`.</span></span>

<span data-ttu-id="d28e4-514">`-uld|--use-local-db` : spécifie s’il convient ou non d’utiliser LocalDB au lieu de SQLite.</span><span class="sxs-lookup"><span data-stu-id="d28e4-514">`-uld|--use-local-db` - Specifies whether or not to use LocalDB instead of SQLite.</span></span> <span data-ttu-id="d28e4-515">Valeurs : `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-515">Values: `true` or `false`.</span></span> <span data-ttu-id="d28e4-516">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="d28e4-516">The default value is `false`.</span></span>

---

## <a name="examples"></a><span data-ttu-id="d28e4-517">Exemples</span><span class="sxs-lookup"><span data-stu-id="d28e4-517">Examples</span></span>

<span data-ttu-id="d28e4-518">Créez un projet d’application console F# dans le répertoire actif :</span><span class="sxs-lookup"><span data-stu-id="d28e4-518">Create an F# console application project in the current directory:</span></span>

`dotnet new console -lang F#`

<span data-ttu-id="d28e4-519">Créez un projet de bibliothèque de classes .NET Standard dans le répertoire spécifié (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieur) :</span><span class="sxs-lookup"><span data-stu-id="d28e4-519">Create a .NET Standard class library project in the specified directory (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new classlib -lang VB -o MyLibrary`

<span data-ttu-id="d28e4-520">Créez un projet d’application ASP.NET Core C# MVC dans le répertoire actif sans authentification :</span><span class="sxs-lookup"><span data-stu-id="d28e4-520">Create a new ASP.NET Core C# MVC application project in the current directory with no authentication:</span></span>

`dotnet new mvc -au None`

<span data-ttu-id="d28e4-521">Créez une application xUnit :</span><span class="sxs-lookup"><span data-stu-id="d28e4-521">Create a new xUnit application:</span></span>

`dotnet new xunit`

<span data-ttu-id="d28e4-522">Répertoriez tous les modèles disponibles pour MVC :</span><span class="sxs-lookup"><span data-stu-id="d28e4-522">List all templates available for MVC:</span></span>

`dotnet new mvc -l`

<span data-ttu-id="d28e4-523">Installez la version 2.0 des modèles d’application monopage pour ASP.NET Core (option de commande disponible pour .NET Core  SDK 1.1 et versions ultérieures uniquement) :</span><span class="sxs-lookup"><span data-stu-id="d28e4-523">Install version 2.0 of the Single Page Application templates for ASP.NET Core (command option available for .NET Core SDK 1.1 and later versions only):</span></span>

`dotnet new -i Microsoft.DotNet.Web.Spa.ProjectTemplates::2.0.0`

<span data-ttu-id="d28e4-524">Créez un fichier *global.json* dans le répertoire actif en définissant la version du SDK sur 2.0.0 (disponible uniquement avec le SDK .NET Core 2.0 ou ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="d28e4-524">Create a *global.json* in the current directory setting the SDK version to 2.0.0 (available only with .NET Core SDK 2.0 or later versions):</span></span>

`dotnet new globaljson --sdk-version 2.0.0`

## <a name="see-also"></a><span data-ttu-id="d28e4-525">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d28e4-525">See also</span></span>

* [<span data-ttu-id="d28e4-526">Modèles personnalisés pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="d28e4-526">Custom templates for dotnet new</span></span>](custom-templates.md)  
* [<span data-ttu-id="d28e4-527">Créer un modèle personnalisé pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="d28e4-527">Create a custom template for dotnet new</span></span>](~/docs/core/tutorials/create-custom-template.md)  
* [<span data-ttu-id="d28e4-528">Dépôt GitHub dotnet/dotnet-template-samples</span><span class="sxs-lookup"><span data-stu-id="d28e4-528">dotnet/dotnet-template-samples GitHub repo</span></span>](https://github.com/dotnet/dotnet-template-samples)  
* [<span data-ttu-id="d28e4-529">Modèles disponibles pour dotnet new</span><span class="sxs-lookup"><span data-stu-id="d28e4-529">Available templates for dotnet new</span></span>](https://github.com/dotnet/templating/wiki/Available-templates-for-dotnet-new)
