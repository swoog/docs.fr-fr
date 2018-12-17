---
title: Nouveautés de .NET Core 3.0
description: Découvrez les nouvelles fonctionnalités de .NET Core 3.0.
dev_langs:
- csharp
- vb
author: thraka
ms.author: adegeo
ms.date: 12/04/2018
ms.openlocfilehash: 3ca833031eb8bb0f43a334f833f2e0075842d57d
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53156667"
---
# <a name="whats-new-in-net-core-30-preview-1"></a><span data-ttu-id="a5022-103">Nouveautés de .NET Core 3.0 (préversion 1)</span><span class="sxs-lookup"><span data-stu-id="a5022-103">What's new in .NET Core 3.0 (Preview 1)</span></span>

<span data-ttu-id="a5022-104">Cet article décrit les nouveautés de .NET Core 3.0 (préversion 1).</span><span class="sxs-lookup"><span data-stu-id="a5022-104">This article describes what is new in .NET Core 3.0 (preview 1).</span></span> <span data-ttu-id="a5022-105">Une des principales améliorations est la prise en charge des applications de bureau Windows (Windows uniquement).</span><span class="sxs-lookup"><span data-stu-id="a5022-105">One of the biggest enhancements is support for Windows desktop applications (Windows only).</span></span> <span data-ttu-id="a5022-106">En utilisant un composant .NET Core 3.0 appelé Bureau Windows, vous pouvez porter vos applications Windows Forms Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="a5022-106">By utilizing a .NET Core 3.0 component called Windows Desktop, you can port your Windows Forms Windows Presentation Foundation (WPF) applications.</span></span> <span data-ttu-id="a5022-107">Pour être clair, le composant Bureau Windows est uniquement pris en charge sous Windows.</span><span class="sxs-lookup"><span data-stu-id="a5022-107">To be clear, the Windows Desktop component is only supported on Windows.</span></span> <span data-ttu-id="a5022-108">Pour plus d'informations, consultez la section [Bureau Windows](#windows-desktop) ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a5022-108">For more information, see the section [Windows desktop](#windows-desktop) below.</span></span>

<span data-ttu-id="a5022-109">.NET Core 3.0 prend en charge C# 8.0.</span><span class="sxs-lookup"><span data-stu-id="a5022-109">.NET Core 3.0 adds support for C# 8.0.</span></span>

<span data-ttu-id="a5022-110">[Téléchargez et commencez à utiliser .NET Core 3 Préversion 1](https://aka.ms/netcore3download) dès maintenant sous Windows, Mac et Linux.</span><span class="sxs-lookup"><span data-stu-id="a5022-110">[Download and get started with .NET Core 3 Preview 1](https://aka.ms/netcore3download) right now on Windows, Mac and Linux.</span></span> <span data-ttu-id="a5022-111">Vous pouvez consulter les détails complets de la version dans les [notes de publication de .NET Core 3 Préversion 1](https://aka.ms/netcore3releasenotes).</span><span class="sxs-lookup"><span data-stu-id="a5022-111">You can see complete details of the release in the [.NET Core 3 Preview 1 release notes](https://aka.ms/netcore3releasenotes).</span></span>

<span data-ttu-id="a5022-112">Pour plus d’informations, consultez l’[annonce de .NET Core 3.0 Préversion 1](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/).</span><span class="sxs-lookup"><span data-stu-id="a5022-112">For more information, see the [.NET Core 3.0 Preview 1 announcement](https://blogs.msdn.microsoft.com/dotnet/2018/12/04/announcing-net-core-3-preview-1-and-open-sourcing-windows-desktop-frameworks/).</span></span>

## <a name="net-standard-21"></a><span data-ttu-id="a5022-113">.NET Standard 2.1</span><span class="sxs-lookup"><span data-stu-id="a5022-113">.NET Standard 2.1</span></span>

<span data-ttu-id="a5022-114">.NET Core 3.0 implémente également .NET Standard 2.1.</span><span class="sxs-lookup"><span data-stu-id="a5022-114">.NET Core 3.0 implements .NET Standard 2.1.</span></span>

## <a name="default-executables"></a><span data-ttu-id="a5022-115">Exécutables par défaut</span><span class="sxs-lookup"><span data-stu-id="a5022-115">Default executables</span></span>

<span data-ttu-id="a5022-116">.NET Core permet désormais de générer des exécutables par défaut.</span><span class="sxs-lookup"><span data-stu-id="a5022-116">.NET Core will now build executables by default.</span></span> <span data-ttu-id="a5022-117">Il s’agit d’une nouvelle fonctionnalité pour les applications qui utilisent une version .NET Core installée de façon globale.</span><span class="sxs-lookup"><span data-stu-id="a5022-117">This is new for applications that use a globally installed version of .NET Core.</span></span> <span data-ttu-id="a5022-118">Jusqu'à présent, seuls les [déploiements autonomes](../deploying/index.md#self-contained-deployments-scd) avaient des exécutables.</span><span class="sxs-lookup"><span data-stu-id="a5022-118">Until now, only [self-contained deployments](../deploying/index.md#self-contained-deployments-scd) had executables.</span></span>

<span data-ttu-id="a5022-119">Lors de l’étape `dotnet build` ou `dotnet publish`, un exécutable est créé s’il correspond à l’environnement et à la plateforme du Kit de développement que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="a5022-119">During `dotnet build` or `dotnet publish`, an executable is created provided that matches the environment and platform of the SDK you are using.</span></span> <span data-ttu-id="a5022-120">Vous pouvez obtenir le même résultat avec ces exécutables, comme vous le feriez avec d’autres exécutables natifs comme :</span><span class="sxs-lookup"><span data-stu-id="a5022-120">You can expect the same things with these executables as you would other native executables, such as:</span></span>

* <span data-ttu-id="a5022-121">Vous pouvez double-cliquer sur l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="a5022-121">You can double-click on the executable.</span></span>
* <span data-ttu-id="a5022-122">Vous pouvez lancer l’application directement à partir d’une invite de commandes, par exemple `myapp.exe` sous Windows, et `./myapp` sous Linux et macOS.</span><span class="sxs-lookup"><span data-stu-id="a5022-122">You can launch the application from a command prompt directly, such as `myapp.exe` on Windows, and `./myapp` on Linux and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="a5022-123">La spécification d’un runtime avec des arguments `dotnet publish -r` ou `dotnet build -r` pour d’autres environnements de runtime n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a5022-123">Specifying a specific runtime with `dotnet publish -r` or `dotnet build -r` arguments for other runtime environments isn't supported.</span></span>

## <a name="build-copies-dependencies"></a><span data-ttu-id="a5022-124">Dépendances de copies de build</span><span class="sxs-lookup"><span data-stu-id="a5022-124">Build copies dependencies</span></span>

<span data-ttu-id="a5022-125">`dotnet build` copie maintenant les dépendances NuGet pour votre application à partir du cache NuGet vers le dossier de sortie de build.</span><span class="sxs-lookup"><span data-stu-id="a5022-125">`dotnet build` now copies NuGet dependencies for your application from the NuGet cache to the build output folder.</span></span> <span data-ttu-id="a5022-126">Auparavant, les dépendances étaient copiées uniquement dans le cadre de `dotnet publish`.</span><span class="sxs-lookup"><span data-stu-id="a5022-126">Previously, dependencies were only copied as part of `dotnet publish`.</span></span> 

<span data-ttu-id="a5022-127">Certaines opérations, par exemple la liaison et la publication d’une page de type Razor, nécessiteront toujours une publication.</span><span class="sxs-lookup"><span data-stu-id="a5022-127">There are some operations, like linking and razor page publishing that will still require publishing.</span></span>


## <a name="local-dotnet-tools"></a><span data-ttu-id="a5022-128">Outils dotnet locaux</span><span class="sxs-lookup"><span data-stu-id="a5022-128">Local dotnet tools</span></span>

<span data-ttu-id="a5022-129">Alors que .NET Core 2.1 prenant en charge des outils globaux, .NET Core 3.0 dispose maintenant d’outils locaux.</span><span class="sxs-lookup"><span data-stu-id="a5022-129">While .NET Core 2.1 supported global tools, .NET Core 3.0 now has local tools.</span></span> <span data-ttu-id="a5022-130">Les outils locaux sont similaires aux outils globales mais ils sont associés à un emplacement particulier sur le disque.</span><span class="sxs-lookup"><span data-stu-id="a5022-130">Local tools are similar to global tools but are associated with a particular location on disk.</span></span> <span data-ttu-id="a5022-131">Cela permet une utilisation par projet et par référentiel.</span><span class="sxs-lookup"><span data-stu-id="a5022-131">This enables per-project and per-repository tooling.</span></span> <span data-ttu-id="a5022-132">Un outil installé localement n’est pas disponible de façon globale.</span><span class="sxs-lookup"><span data-stu-id="a5022-132">Any tool installed locally isn't available globally.</span></span>

<span data-ttu-id="a5022-133">Les outils locaux s’appuient sur un nom de fichier manifeste `dotnet-tools.json` dans votre répertoire actuel.</span><span class="sxs-lookup"><span data-stu-id="a5022-133">Local tools rely on a manifest file name `dotnet-tools.json` in your current directory.</span></span> <span data-ttu-id="a5022-134">Ce fichier manifeste définit les outils qui doivent être disponibles.</span><span class="sxs-lookup"><span data-stu-id="a5022-134">This manifest file defines the tools to be available.</span></span> <span data-ttu-id="a5022-135">En créant ce fichier manifeste à la racine de votre référentiel, vous garantissez que toute personne qui clone votre code pourra restaurer et utiliser les outils nécessaires pour fonctionner correctement avec votre code.</span><span class="sxs-lookup"><span data-stu-id="a5022-135">By creating this manifest file at the root of your repository, you ensure anyone cloning your code can restore and use the tools that are needed to successfully work with your code.</span></span>

<span data-ttu-id="a5022-136">Lorsque le fichier manifeste des outils locaux est disponible, utilisez la commande suivante pour automatiquement télécharger et installer localement ces outils :</span><span class="sxs-lookup"><span data-stu-id="a5022-136">When the local tools manifest file is available, use the following command to automatically download and install those tools locally:</span></span>

```console
dotnet tool restore
```

<span data-ttu-id="a5022-137">Exécutez l’outil local avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5022-137">Run a local tool with the following command:</span></span>

```console
dotnet tool run <tool-command-name>
```

<span data-ttu-id="a5022-138">Lorsqu’un outil local est appelé, dotnet recherche un manifeste dans la structure de répertoire.</span><span class="sxs-lookup"><span data-stu-id="a5022-138">When a local tool is called, dotnet searches for a manifest up the directory structure.</span></span> <span data-ttu-id="a5022-139">Si le fichier manifeste d’un outil est trouvé, la commande recherche l’outil demandé.</span><span class="sxs-lookup"><span data-stu-id="a5022-139">When a tool manifest file is found, it is searched for the requested tool.</span></span> <span data-ttu-id="a5022-140">Si elle trouve l’outil, elle inclut les informations nécessaires pour trouver l’outil à l’emplacement des packages globaux NuGet.</span><span class="sxs-lookup"><span data-stu-id="a5022-140">If the tool is found, it includes the information needed to find the tool in the NuGet global packages location.</span></span> 

<span data-ttu-id="a5022-141">Si l’outil se trouve dans le manifeste mais pas dans le cache, l’utilisateur reçoit une erreur.</span><span class="sxs-lookup"><span data-stu-id="a5022-141">If the tool is found in the manifest, but not the cache, the user receives an error.</span></span> <span data-ttu-id="a5022-142">Le message sera amélioré après la préversion 1 pour demander à l’utilisateur d’exécuter `dotnet tool restore`.</span><span class="sxs-lookup"><span data-stu-id="a5022-142">The message will be improved after Preview 1 to request the user run `dotnet tool restore`.</span></span>

<span data-ttu-id="a5022-143">Pour ajouter des outils locaux à un répertoire, vous devez d’abord créer le fichier manifeste de l’outil.</span><span class="sxs-lookup"><span data-stu-id="a5022-143">To add local tools to a directory, you need to first create the tool manifest file.</span></span> <span data-ttu-id="a5022-144">Après la préversion 1, nous proposerons un mécanisme pour la création des fichiers manifeste, notamment un nouveau modèle dotnet.</span><span class="sxs-lookup"><span data-stu-id="a5022-144">After Preview 1, we will offer a mechanism for creating tool manifest files, such as a dotnet new template.</span></span> <span data-ttu-id="a5022-145">Pour la préversion 1, vous devez créer le fichier `dotnet-tools.json` avec le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="a5022-145">For Preview 1 you must create the file named `dotnet-tools.json` with the following contents:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {}
}
```

<span data-ttu-id="a5022-146">Une fois le manifeste créé, vous pouvez ajouter des outils locaux à l’aide de la commande :</span><span class="sxs-lookup"><span data-stu-id="a5022-146">Once the manifest is created, you can add local tools to it using:</span></span>

```console
dotnet tool install <toolPackageId>
```

<span data-ttu-id="a5022-147">Cette commande installe la dernière version de l’outil, sauf si une autre version est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a5022-147">This command installs the latest version of the tool, unless another version is specified.</span></span>  <span data-ttu-id="a5022-148">Même si la version la plus récente a été automatiquement choisie, la version de l’outil est inscrite dans le fichier manifeste de l’outil pour permettre la restauration ou l’exécution de la version correcte de l’outil.</span><span class="sxs-lookup"><span data-stu-id="a5022-148">Even if the latest version was automatically chosen, the version of the tool is written into the tool manifest file to allow the correct version of the tool to be restored or run.</span></span>

<span data-ttu-id="a5022-149">Le fichier manifeste de l’outil est conçu pour permettre des modifications manuelles et ainsi mettre à jour la version requise pour une utilisation avec le référentiel.</span><span class="sxs-lookup"><span data-stu-id="a5022-149">The tool manifest file is designed to allow hand editing – which you might do to update the required version for working with the repository.</span></span>

<span data-ttu-id="a5022-150">Voici un exemple de fichier `dotnet-tools.json` :</span><span class="sxs-lookup"><span data-stu-id="a5022-150">Here is an example `dotnet-tools.json` file:</span></span>

```json
{
  "version": 1,
  "isRoot": true,
  "tools": {
    "dotnetsay": {
      "version": "2.1.4",
      "commands": [
        "dotnetsay"
      ]
    },
    "t-rex": {
      "version": "1.0.103",
      "commands": [
        "t-rex"
      ]
    }
  }
}
```

<span data-ttu-id="a5022-151">Pour supprimer un outil du fichier manifeste, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="a5022-151">To remove a tool from the tool manifest file, run the following command:</span></span>

```console
dotnet tool uninstall <toolPackageId>
```

<span data-ttu-id="a5022-152">Pour les outils locaux et globaux, une version compatible du runtime est requise.</span><span class="sxs-lookup"><span data-stu-id="a5022-152">For both global and local tools, a compatible version of the runtime is required.</span></span> <span data-ttu-id="a5022-153">De nombreux outils actuellement sur NuGet.org ciblent le runtime .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="a5022-153">Many tools currently on NuGet.org target .NET Core Runtime 2.1.</span></span> <span data-ttu-id="a5022-154">Pour installer ces outils de façon locale ou globale, vous devez toujours installer le [runtime NET Core 2.1](https://dotnet.microsoft.com/download/dotnet-core/2.1).</span><span class="sxs-lookup"><span data-stu-id="a5022-154">To install those globally or locally, you would still need to install the [NET Core 2.1 Runtime](https://dotnet.microsoft.com/download/dotnet-core/2.1).</span></span>

<span data-ttu-id="a5022-155">Pour plus d’informations, consultez [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288).</span><span class="sxs-lookup"><span data-stu-id="a5022-155">For more information, see [Local Tools Early Preview Documentation](https://github.com/dotnet/cli/issues/10288).</span></span>

## <a name="windows-desktop"></a><span data-ttu-id="a5022-156">Bureau Windows</span><span class="sxs-lookup"><span data-stu-id="a5022-156">Windows desktop</span></span>

<span data-ttu-id="a5022-157">À compter de .NET Core 3.0 Préversion 1, vous pouvez créer des applications de bureau Windows à l’aide des outils WPF et Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="a5022-157">Starting with .NET Core 3.0 Preview 1, you can build Windows desktop applications using WPF and Windows Forms.</span></span> <span data-ttu-id="a5022-158">Ces infrastructures prennent également en charge l’utilisation de contrôles modernes et le style Fluent à partir de la bibliothèque XAML de l’interface utilisateur Windows (WinUI) via des [îles XAML](/windows/uwp/xaml-platform/xaml-host-controls).</span><span class="sxs-lookup"><span data-stu-id="a5022-158">These frameworks also support using modern controls and Fluent styling from the Windows UI XAML Library (WinUI) via [XAML islands](/windows/uwp/xaml-platform/xaml-host-controls).</span></span>

<span data-ttu-id="a5022-159">Le composant Bureau Windows fait partie du SDK .NET Core 3.0 Windows.</span><span class="sxs-lookup"><span data-stu-id="a5022-159">The Windows Desktop component is part of the Windows .NET Core 3.0 SDK.</span></span>

<span data-ttu-id="a5022-160">Vous pouvez créer une nouvelle application WPF ou Windows Forms à l’aide des commandes `dotnet` suivantes :</span><span class="sxs-lookup"><span data-stu-id="a5022-160">You can create a new WPF or Windows Forms app with the following `dotnet` commands:</span></span>

```console
dotnet new wpf
dotnet new winforms
```

<span data-ttu-id="a5022-161">Vous pouvez également ouvrir, lancer et déboguer des projets .NET Core 3.0 WPF et Windows Forms dans Visual Studio 2019 Préversion 1.</span><span class="sxs-lookup"><span data-stu-id="a5022-161">You can also open, launch, and debug .NET Core 3.0 WPF and Windows Forms projects in Visual Studio 2019 Preview 1.</span></span> <span data-ttu-id="a5022-162">Il est actuellement possible d’ouvrir ces projets dans 15.9 de 2017 Visual Studio, mais ce n’est pas un scénario pris en charge (et vous devez [activer les préversions](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)).</span><span class="sxs-lookup"><span data-stu-id="a5022-162">It's currently possible to open these projects in Visual Studio 2017 15.9, however, it isn't a supported scenario (and you need to [enable previews](https://blogs.msdn.microsoft.com/dotnet/2018/11/13/net-core-tooling-update-for-visual-studio-2017-version-15-9/)).</span></span>

<span data-ttu-id="a5022-163">Les nouveaux projets sont identiques aux projets .NET Core existants, avec quelques ajouts.</span><span class="sxs-lookup"><span data-stu-id="a5022-163">The new projects are the same as existing .NET Core projects, with a couple additions.</span></span> <span data-ttu-id="a5022-164">Voici une comparaison entre le projet de console .NET Core de base et un projet Windows Forms et WPF de base.</span><span class="sxs-lookup"><span data-stu-id="a5022-164">Here is the comparison of the basic .NET Core console project and a basic Windows Forms and WPF project.</span></span>

<span data-ttu-id="a5022-165">Dans un projet de console .NET Core, le projet utilise le SDK `Microsoft.NET.Sdk` et déclare une dépendance sur .NET Core 3.0 via l’infrastructure cible `netcoreapp3.0`.</span><span class="sxs-lookup"><span data-stu-id="a5022-165">In a .NET Core console project, the project uses the `Microsoft.NET.Sdk` SDK and declares a dependency on .NET Core 3.0 via the `netcoreapp3.0` target framework.</span></span> <span data-ttu-id="a5022-166">Pour créer une application Bureau Windows, utilisez le SDK `Microsoft.NET.Sdk.WindowsDesktop` et choisissez l’infrastructure d’interface utilisateur à utiliser :</span><span class="sxs-lookup"><span data-stu-id="a5022-166">To create a Windows Desktop app, use the `Microsoft.NET.Sdk.WindowsDesktop` SDK and choose which UI framework to use:</span></span>

```diff
-<Project Sdk="Microsoft.NET.Sdk">
+<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
+   <UseWPF>true</UseWPF>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="a5022-167">Pour choisir Windows Forms plutôt que WPF, définissez `UseWindowsForms` au lieu de `UseWPF` :</span><span class="sxs-lookup"><span data-stu-id="a5022-167">To choose Windows Forms over WPF, set `UseWindowsForms` instead of `UseWPF`:</span></span>

```diff
<Project Sdk="Microsoft.NET.Sdk.WindowsDesktop">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>netcoreapp3.0</TargetFramework>
-   <UseWPF>true</UseWPF>
+   <UseWindowsForms>true</UseWindowsForms>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="a5022-168">`UseWPF` et `UseWindowsForms` peuvent être définies sur `true` si l’application utilise les deux infrastructures, par exemple lorsqu’une boîte de dialogue Windows Forms héberge un contrôle WPF.</span><span class="sxs-lookup"><span data-stu-id="a5022-168">Both `UseWPF` and `UseWindowsForms` can be set to `true` if the app uses both frameworks, for example when a Windows Forms dialog is hosting a WPF control.</span></span>

<span data-ttu-id="a5022-169">Partagez vos commentaires sur les référentiels [dotnet/winforms](https://github.com/dotnet/winforms/issues), [dotnet/wpf](https://github.com/dotnet/wpf/issues) et [dotnet/core](https://github.com/dotnet/core/issues).</span><span class="sxs-lookup"><span data-stu-id="a5022-169">Please share your feedback on the [dotnet/winforms](https://github.com/dotnet/winforms/issues),  [dotnet/wpf](https://github.com/dotnet/wpf/issues) and [dotnet/core](https://github.com/dotnet/core/issues) repos.</span></span>

## <a name="fast-built-in-json-support"></a><span data-ttu-id="a5022-170">Prise en charge JSON intégrée rapide</span><span class="sxs-lookup"><span data-stu-id="a5022-170">Fast built-in JSON support</span></span>

<span data-ttu-id="a5022-171">`System.Text.Json.Utf8JsonReader` est un lecteur hautes performances et à faible allocation de type forward-only pour le texte JSON codé au format UTF-8 et lu à partir de `ReadOnlySpan<byte>`.</span><span class="sxs-lookup"><span data-stu-id="a5022-171">`System.Text.Json.Utf8JsonReader` is a high-performance, low allocation, forward-only reader for UTF-8 encoded JSON text, read from a `ReadOnlySpan<byte>`.</span></span> <span data-ttu-id="a5022-172">`Utf8JsonReader` est un type fondamental de bas niveau, permettant de générer des analyseurs et des désérialiseurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a5022-172">The `Utf8JsonReader` is a foundational, low-level type, that can be leveraged to build custom parsers and deserializers.</span></span> <span data-ttu-id="a5022-173">La lecture d’une charge utile JSON à l’aide du nouveau `Utf8JsonReader` est 2 fois plus rapide qu’avec le lecteur proposé par [Json.NET](https://www.newtonsoft.com/json).</span><span class="sxs-lookup"><span data-stu-id="a5022-173">Reading through a JSON payload using the new `Utf8JsonReader` is 2x faster than using the reader from [Json.NET](https://www.newtonsoft.com/json).</span></span> <span data-ttu-id="a5022-174">Ce lecteur n’alloue aucune ressource tant que vous n’avez pas besoin d’actualiser des jetons JSON sous forme de chaînes (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="a5022-174">It does not allocate until you need to actualize JSON tokens as (UTF-16) strings.</span></span>

<span data-ttu-id="a5022-175">Cette nouvelle API inclura les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="a5022-175">This new API will include the following components:</span></span>

* <span data-ttu-id="a5022-176">Préversion 1 : lecteur JSON (accès séquentiel)</span><span class="sxs-lookup"><span data-stu-id="a5022-176">In Preview 1: JSON reader (sequential access)</span></span>
* <span data-ttu-id="a5022-177">Prochainement : enregistreur JSON, DOM (accès aléatoire), sérialiseur poco, désérialiseur poco</span><span class="sxs-lookup"><span data-stu-id="a5022-177">Coming next: JSON writer, DOM (random access), poco serializer, poco deserializer</span></span>

<span data-ttu-id="a5022-178">Voici la boucle de lecteur de base pour le `Utf8JsonReader`, utilisable comme point de départ :</span><span class="sxs-lookup"><span data-stu-id="a5022-178">Here is the basic reader loop for the `Utf8JsonReader` that can be used as a starting point:</span></span>

```csharp
using System.Text.Json;

public static void Utf8JsonReaderLoop(ReadOnlySpan<byte> dataUtf8)
{
    var json = new Utf8JsonReader(dataUtf8, isFinalBlock: true, state: default);

    while (json.Read())
    {
        JsonTokenType tokenType = json.TokenType;
        ReadOnlySpan<byte> valueSpan = json.ValueSpan;
        switch (tokenType)
        {
            case JsonTokenType.StartObject:
            case JsonTokenType.EndObject:
                break;
            case JsonTokenType.StartArray:
            case JsonTokenType.EndArray:
                break;
            case JsonTokenType.PropertyName:
                break;
            case JsonTokenType.String:
                string valueString = json.GetStringValue();
                break;
            case JsonTokenType.Number:
                if (!json.TryGetInt32Value(out int valueInteger))
                {
                    throw new FormatException();
                }
                break;
            case JsonTokenType.True:
            case JsonTokenType.False:
                bool valueBool = json.GetBooleanValue();
                break;
            case JsonTokenType.Null:
                break;
            default:
                throw new ArgumentException();
        }
    }

    dataUtf8 = dataUtf8.Slice((int)json.BytesConsumed);
    JsonReaderState state = json.CurrentState;
}
```

<span data-ttu-id="a5022-179">L’écosystème .NET s’appuyaient sur [Json.NET](https://www.newtonsoft.com/json) et d’autres bibliothèques JSON populaires, qui restent des solutions efficaces.</span><span class="sxs-lookup"><span data-stu-id="a5022-179">The .NET ecosystem has relied on [Json.NET](https://www.newtonsoft.com/json) and other popular JSON libraries, which continue to be good choices.</span></span> <span data-ttu-id="a5022-180">JSON.NET utilise des chaînes .NET comme type de données de base, au format UTF-16.</span><span class="sxs-lookup"><span data-stu-id="a5022-180">JSON.NET uses .NET strings as its base datatype, which are UTF-16 under the hood.</span></span> 

<span data-ttu-id="a5022-181">Dans .NET Core 2.1 et 3.0, nous avons ajouté de nouvelles API permettant d’écrire des API JSON (notamment `Utf8JsonReader`) qui nécessitent beaucoup moins de mémoire, s’appuient sur l’utilisation de `Span<T>` et de chaînes UTF-8, et répondent mieux aux besoins des applications à débit élevé comme Kestrel ou le serveur web ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="a5022-181">In .NET Core 2.1 and 3.0, we added new APIs that makes it possible to write JSON APIs (such as `Utf8JsonReader`) that require much less memory, based on using `Span<T>` and UTF-8 strings, and better serve the needs of high-throughput applications like Kestrel, ASP.NET Core web server.</span></span>

## <a name="ranges-and-indices"></a><span data-ttu-id="a5022-182">Plages et index</span><span class="sxs-lookup"><span data-stu-id="a5022-182">Ranges and indices</span></span>

<span data-ttu-id="a5022-183">Le nouveau type `Index` peut être utilisé pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="a5022-183">The new `Index` type can be used for indexing.</span></span> <span data-ttu-id="a5022-184">Vous pouvez en créer un à partir d’un `int` qui compte à partir du début, ou avec un opérateur (C#) `^` préfixé qui compte à partir de la fin :</span><span class="sxs-lookup"><span data-stu-id="a5022-184">You can create one from an `int` that counts from the beginning, or with a prefix `^` operator (C#) that counts from the end:</span></span>

```csharp
Index i1 = 3;  // number 3 from beginning
Index i2 = ^4; // number 4 from end
int[] a = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
Console.WriteLine($"{a[i1]}, {a[i2]}"); // "3, 6"
```

<span data-ttu-id="a5022-185">Il existe également un type `Range`, composé de deux `Index` valeurs, une pour le début et une pour la fin, et qui peut être écrit avec une expression de plage (C#) `x..y`.</span><span class="sxs-lookup"><span data-stu-id="a5022-185">There is also a `Range` type, which consists of two `Index` values, one for the start and one for the end, and can be written with a `x..y` range expression (C#).</span></span> <span data-ttu-id="a5022-186">Vous pouvez indexer ensuite avec un `Range` afin de produire une tranche :</span><span class="sxs-lookup"><span data-stu-id="a5022-186">You can then index with a `Range` in order to produce a slice:</span></span>

```csharp
var slice = a[i1..i2]; // { 3, 4, 5 }
```

> [!NOTE]
> <span data-ttu-id="a5022-187">Seul [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) prend en charge la syntaxe pour `Range` et `Index`.</span><span class="sxs-lookup"><span data-stu-id="a5022-187">Only [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) supports syntax for `Range` and `Index`.</span></span>

## <a name="async-streams"></a><span data-ttu-id="a5022-188">Flux asynchrones</span><span class="sxs-lookup"><span data-stu-id="a5022-188">Async streams</span></span>

<span data-ttu-id="a5022-189">Le type `IAsyncEnumerable<T>` est une nouvelle version asynchrone de `IEnumerable<T>`.</span><span class="sxs-lookup"><span data-stu-id="a5022-189">The `IAsyncEnumerable<T>` type is a new asynchronous version of `IEnumerable<T>`.</span></span> <span data-ttu-id="a5022-190">Le langage vous permet d’appliquer une opération `await foreach` sur ces objets pour consommer leurs éléments, et une opération `yield return` pour produire les éléments.</span><span class="sxs-lookup"><span data-stu-id="a5022-190">The language lets you `await foreach` over these to consume their elements, and `yield return` to them to produce elements.</span></span>

<span data-ttu-id="a5022-191">L’exemple suivant montre la production et la consommation de flux de données asynchrones.</span><span class="sxs-lookup"><span data-stu-id="a5022-191">The following example demonstrates both production and consumption of async streams.</span></span> <span data-ttu-id="a5022-192">L’instruction `foreach` est asynchrone et utilise elle-même `yield return` afin de produire un flux asynchrone pour les appelants.</span><span class="sxs-lookup"><span data-stu-id="a5022-192">The `foreach` statement is async and itself uses `yield return` to produce an async stream for callers.</span></span> <span data-ttu-id="a5022-193">Ce modèle (qui utilise `yield return`) est le modèle recommandé pour produire des flux de données asynchrones.</span><span class="sxs-lookup"><span data-stu-id="a5022-193">This pattern (using `yield return`) is the recommended model for producing async streams.</span></span>

```csharp
async IAsyncEnumerable<int> GetBigResultsAsync()
{
    await foreach (var result in GetResultsAsync())
    {
        if (result > 20) yield return result; 
    }
}
```

> [!WARNING]
> <span data-ttu-id="a5022-194">.NET core 3.0 Préversion 1 contient actuellement un bogue au niveau de `await foreach`.</span><span class="sxs-lookup"><span data-stu-id="a5022-194">.NET Core 3.0 Preview 1 currently has a bug with `await foreach`.</span></span> <span data-ttu-id="a5022-195">Utilisez plutôt `GetEnumerator` et `MoveNext` pour traiter les éléments.</span><span class="sxs-lookup"><span data-stu-id="a5022-195">Instead, use `GetEnumerator` and `MoveNext` to process elements.</span></span> <span data-ttu-id="a5022-196">Pour plus d'informations, consultez [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268).</span><span class="sxs-lookup"><span data-stu-id="a5022-196">For more information, see [roslyn/#31268](https://github.com/dotnet/roslyn/issues/31268).</span></span>

<span data-ttu-id="a5022-197">Outre la possibilité d’effectuer une opération `await foreach`, vous pouvez également créer des itérateurs asynchrones, par exemple un itérateur qui retourne un objet `IAsyncEnumerable/IAsyncEnumerator` auquel vous pouvez à la fois appliquer des opérations `await` et `yield`.</span><span class="sxs-lookup"><span data-stu-id="a5022-197">In addition to being able to `await foreach`, you can also create async iterators, for example, an iterator that returns an `IAsyncEnumerable/IAsyncEnumerator` that you can both `await` and `yield` in.</span></span> <span data-ttu-id="a5022-198">Pour les objets qui doivent être supprimés, vous pouvez utiliser `IAsyncDisposable`, qui implémentent différents types BCL, notamment `Stream` et `Timer`.</span><span class="sxs-lookup"><span data-stu-id="a5022-198">For objects that need to be disposed, you can use `IAsyncDisposable`, which various BCL types implement, such as `Stream` and `Timer`.</span></span>

> [!NOTE]
> <span data-ttu-id="a5022-199">Seul [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) prend en charge la syntaxe `await foreach`</span><span class="sxs-lookup"><span data-stu-id="a5022-199">Only [C# 8.0](https://blogs.msdn.microsoft.com/dotnet/2018/11/12/building-c-8-0/) supports `await foreach` syntax.</span></span>

## <a name="type-sequencereader"></a><span data-ttu-id="a5022-200">Type : SequenceReader</span><span class="sxs-lookup"><span data-stu-id="a5022-200">Type: SequenceReader</span></span>

<span data-ttu-id="a5022-201">Dans .NET Core 3.0, `System.Buffers.SequenceReader` a été ajouté et peut servir de lecteur pour `ReadOnlySequence<T>`.</span><span class="sxs-lookup"><span data-stu-id="a5022-201">In .NET Core 3.0, `System.Buffers.SequenceReader` has been added which can be used as a reader for `ReadOnlySequence<T>`.</span></span> <span data-ttu-id="a5022-202">Cela permet une analyse facile, hautes performances et à faible allocation des données `System.IO.Pipelines`, capable de couvrir plusieurs mémoires tampon de stockage.</span><span class="sxs-lookup"><span data-stu-id="a5022-202">This allows easy, high performance, low allocation parsing of `System.IO.Pipelines` data that can cross multiple backing buffers.</span></span> 

<span data-ttu-id="a5022-203">L’exemple suivant segmente une entrée `Sequence` en plusieurs lignes délimitées `CR/LF` valides :</span><span class="sxs-lookup"><span data-stu-id="a5022-203">The following example breaks an input `Sequence` into valid `CR/LF` delimited lines:</span></span>

```csharp
private static ReadOnlySpan<byte> CRLF => new byte[] { (byte)'\r', (byte)'\n' };

public static void ReadLines(ReadOnlySequence<byte> sequence)
{
    SequenceReader<byte> reader = new SequenceReader<byte>(sequence);

    while (!reader.End)
    {
        if (!reader.TryReadToAny(out ReadOnlySpan<byte> line, CRLF, advancePastDelimiter:false))
        {
            // Couldn't find another delimiter
            // ...
        }

        if (!reader.IsNext(CRLF, advancePast: true))
        {
            // Not a good CR/LF pair
            // ...
        }

        // line is valid, process
        ProcessLine(line);
    }
}
```

## <a name="type-metadataloadcontext"></a><span data-ttu-id="a5022-204">Type : MetadataLoadContext</span><span class="sxs-lookup"><span data-stu-id="a5022-204">Type: MetadataLoadContext</span></span>

<span data-ttu-id="a5022-205">Le type `MetadataLoadContext` a été ajouté et permet la lecture des métadonnées de l'assembly sans affecter le domaine d’application de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="a5022-205">The `MetadataLoadContext` type has been added that enables reading assembly metadata without affecting the caller’s application domain.</span></span> <span data-ttu-id="a5022-206">Les assemblys sont lus comme des données, y compris ceux générés pour des architectures et plateformes différentes de l’environnement d’exécution actuel.</span><span class="sxs-lookup"><span data-stu-id="a5022-206">Assemblies are read as data, including assemblies built for different architectures and platforms than the current runtime environment.</span></span> <span data-ttu-id="a5022-207">`MetadataLoadContext` se superpose à <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, qui est uniquement disponible dans .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a5022-207">`MetadataLoadContext` overlaps with the <xref:System.Reflection.Assembly.ReflectionOnlyLoad*>, which is only available in the .NET Framework.</span></span>

<span data-ttu-id="a5022-208">`MetdataLoadContext` est disponible dans le [package System.Reflection.MetadataLoadContext](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext).</span><span class="sxs-lookup"><span data-stu-id="a5022-208">`MetdataLoadContext` is available in the [System.Reflection.MetadataLoadContext package](https://www.nuget.org/packages/System.Reflection.MetadataLoadContext).</span></span> <span data-ttu-id="a5022-209">Il s’agit d’un package .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="a5022-209">It is a .NET Standard 2.0 package.</span></span>

<span data-ttu-id="a5022-210">`MetadataLoadContext` expose les API semblables au type <xref:System.Runtime.Loader.AssemblyLoadContext>, mais il n’est pas basé sur ce type.</span><span class="sxs-lookup"><span data-stu-id="a5022-210">The `MetadataLoadContext` exposes APIs similar to the <xref:System.Runtime.Loader.AssemblyLoadContext> type, but is not based on that type.</span></span> <span data-ttu-id="a5022-211">Tout comme <xref:System.Runtime.Loader.AssemblyLoadContext>, `MetadataLoadContext` permet le chargement d’assemblys dans un univers de chargement d’assemblys isolé.</span><span class="sxs-lookup"><span data-stu-id="a5022-211">Much like <xref:System.Runtime.Loader.AssemblyLoadContext>, the `MetadataLoadContext` enables loading assemblies within an isolated assembly loading universe.</span></span> <span data-ttu-id="a5022-212">Les API `MetdataLoadContext` retournent des objets <xref:System.Reflection.Assembly>, permettant l’utilisation des API de réflexion courantes.</span><span class="sxs-lookup"><span data-stu-id="a5022-212">`MetdataLoadContext` APIs return <xref:System.Reflection.Assembly> objects, enabling the use of familiar reflection APIs.</span></span> <span data-ttu-id="a5022-213">Les API orientées exécution, par exemple [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), ne sont pas autorisées et renverront une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="a5022-213">Execution-oriented APIs, such as [MethodBase.Invoke](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/src/System/Reflection/TypeLoading/Methods/RoMethod.cs#L127), are not allowed and will throw InvalidOperationException.</span></span>

<span data-ttu-id="a5022-214">L’exemple suivant montre comment rechercher des types concrets dans un assembly qui implémente une interface donnée :</span><span class="sxs-lookup"><span data-stu-id="a5022-214">The following sample demonstrates how to find concrete types in an assembly that implements a given interface:</span></span>

```csharp
var paths = new string[] {@"C:\myapp\mscorlib.dll", @"C:\myapp\myapp.dll"};
var resolver = new PathAssemblyResolver(paths);
using (var lc = new MetadataLoadContext(resolver))
{
    Assembly a = lc.LoadFromAssemblyName("myapp");
    Type myInterface = a.GetType("MyApp.IPluginInterface");
    foreach (Type t in a.GetTypes())
    {
        if (t.IsClass && myInterface.IsAssignableFrom(t))
            Console.WriteLine($"Class {t.FullName} implements IPluginInterface");
    }
}
```

<span data-ttu-id="a5022-215">Les scénarios pour `MetadataLoadContext` incluent des fonctionnalités et des outils au moment de la conception, ainsi que des fonctionnalités de runtime qui doivent inspecter un ensemble d’assemblys en tant que données et dont l’intégralité des verrous appliqués aux fichiers et à la mémoire doivent être supprimés une l’inspection terminée.</span><span class="sxs-lookup"><span data-stu-id="a5022-215">Scenarios for `MetadataLoadContext` include design-time features, build-time tooling, and runtime light-up features that need to inspect a set of assemblies as data and have all file locks and memory freed after inspection is performed.</span></span>

<span data-ttu-id="a5022-216">`MetadataLoadContext` contient une classe de résolution passée à son constructeur.</span><span class="sxs-lookup"><span data-stu-id="a5022-216">The `MetadataLoadContext` has a resolver class passed to its constructor.</span></span> <span data-ttu-id="a5022-217">La tâche du programme de résolution consiste à charger un `Assembly` en fonction de son `AssemblyName`.</span><span class="sxs-lookup"><span data-stu-id="a5022-217">The resolver's job is to load an `Assembly` given its `AssemblyName`.</span></span> <span data-ttu-id="a5022-218">La classe de résolution est dérivée de la classe abstraite `MetadataAssemblyResolver`.</span><span class="sxs-lookup"><span data-stu-id="a5022-218">The resolver class derives from the abstract `MetadataAssemblyResolver` class.</span></span> <span data-ttu-id="a5022-219">Une implémentation du programme de résolution pour des scénarios basés sur le chemin d’accès est fournie avec `PathAssemblyResolver`.</span><span class="sxs-lookup"><span data-stu-id="a5022-219">An implementation of the resolver for path-based scenarios is provided with `PathAssemblyResolver`.</span></span>

<span data-ttu-id="a5022-220">Les [tests MetadataLoadContext](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) illustrent de nombreux cas d’usage.</span><span class="sxs-lookup"><span data-stu-id="a5022-220">The [MetadataLoadContext tests](https://github.com/dotnet/corefx/tree/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests) demonstrate many use cases.</span></span> <span data-ttu-id="a5022-221">Les [tests Assembly](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) constituent un bon point de départ.</span><span class="sxs-lookup"><span data-stu-id="a5022-221">The [Assembly tests](https://github.com/dotnet/corefx/blob/master/src/System.Reflection.MetadataLoadContext/tests/src/Tests/Assembly/AssemblyTests.cs) are a good place to start.</span></span>

## <a name="tls-13--openssl-111-on-linux"></a><span data-ttu-id="a5022-222">TLS 1.3 et OpenSSL 1.1.1 sous Linux</span><span class="sxs-lookup"><span data-stu-id="a5022-222">TLS 1.3 & OpenSSL 1.1.1 on Linux</span></span>

<span data-ttu-id="a5022-223">.NET Core tire désormais parti de la [prise en charge de TLS 1.3 dans OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), si disponible dans un environnement donné.</span><span class="sxs-lookup"><span data-stu-id="a5022-223">.NET Core will now take advantage of [TLS 1.3 support in OpenSSL 1.1.1](https://www.openssl.org/blog/blog/2018/09/11/release111/), when it is available in a given environment.</span></span> <span data-ttu-id="a5022-224">Selon l’[équipe OpenSSL](https://www.openssl.org/blog/blog/2018/09/11/release111/), TLS 1.3 présentent plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="a5022-224">There are multiple benefits of TLS 1.3, per the [OpenSSL team](https://www.openssl.org/blog/blog/2018/09/11/release111/):</span></span>

* <span data-ttu-id="a5022-225">Délais de connexion améliorés grâce à une réduction du nombre d’allers-retours requis entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="a5022-225">Improved connection times due to a reduction in the number of round trips required between the client and server.</span></span>

* <span data-ttu-id="a5022-226">Sécurité améliorée grâce à la suppression de différents algorithmes de chiffrement obsolètes et non sécurisés et à un chiffrement plus complet de la négociation de connexion.</span><span class="sxs-lookup"><span data-stu-id="a5022-226">Improved security due to the removal of various obsolete and insecure cryptographic algorithms and encryption of more of the connection handshake.</span></span>

<span data-ttu-id="a5022-227">.NET Core 3.0 Préversion 1 est capable d’utiliser **OpenSSL 1.1.1**, **OpenSSL 1.1.0** ou **OpenSSL 1.0.2** (soit la meilleure version trouvée, sur un système Linux).</span><span class="sxs-lookup"><span data-stu-id="a5022-227">.NET Core 3.0 Preview 1 is capable of utilizing **OpenSSL 1.1.1**, **OpenSSL 1.1.0**, or **OpenSSL 1.0.2** (whatever the best version found is, on a Linux system).</span></span>  <span data-ttu-id="a5022-228">Si **OpenSSL 1.1.1** est disponible, les types SslStream et HttpClient utiliseront **TLS 1.3** avec `SslProtocols.None` (protocoles système par défaut), en supposant que le client et le serveur prennent en charge **TLS 1.3**.</span><span class="sxs-lookup"><span data-stu-id="a5022-228">When **OpenSSL 1.1.1** is available the SslStream and HttpClient types will use **TLS 1.3** when using `SslProtocols.None` (system default protocols), assuming both the client and server support **TLS 1.3**.</span></span>

<span data-ttu-id="a5022-229">L’exemple suivant montre comment .NET Core 3.0 Préversion 1 sous Ubuntu 18.10 se connecte à <https://www.cloudflare.com> :</span><span class="sxs-lookup"><span data-stu-id="a5022-229">The following sample demonstrates .NET Core 3.0 Preview 1 on Ubuntu 18.10 connecting to <https://www.cloudflare.com>:</span></span>

```csharp
using System;
using System.Net.Security;
using System.Net.Sockets;
using System.Threading.Tasks;

namespace tlstest
{
    class Program
    {
        static async Task Main()
        {
            using (TcpClient tcpClient = new TcpClient())
            {
                string targetHost = "www.cloudflare.com";

                await tcpClient.ConnectAsync(targetHost, 443);

                using (SslStream sslStream = new SslStream(tcpClient.GetStream()))
                {
                    await sslStream.AuthenticateAsClientAsync(targetHost);
                    await Console.Out.WriteLineAsync($"Connected to {targetHost} with {sslStream.SslProtocol}");
                }
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/tlstest$ dotnet run
Connected to www.cloudflare.com with Tls13
user@comp-ubuntu1810:~/tlstest$ openssl version
OpenSSL 1.1.1  11 Sep 2018
```

>[!IMPORTANT]
><span data-ttu-id="a5022-230">Windows et macOS ne prennent pas encore en charge **TLS 1.3**.</span><span class="sxs-lookup"><span data-stu-id="a5022-230">Windows and macOS do not yet support **TLS 1.3**.</span></span> <span data-ttu-id="a5022-231">.NET Core 3.0 prendra en charge **TLS 1.3** sur ces systèmes d’exploitation dès que de la prise en charge sera disponible.</span><span class="sxs-lookup"><span data-stu-id="a5022-231">.NET Core 3.0 will support **TLS 1.3** on these operating systems when support becomes available.</span></span>

## <a name="cryptography"></a><span data-ttu-id="a5022-232">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="a5022-232">Cryptography</span></span>

<span data-ttu-id="a5022-233">La prise en charge a été ajoutée pour les chiffrements **AES-GCM** et **AES-CCM**, avec une implémentation via `System.Security.Cryptography.AesGcm` et `System.Security.Cryptography.AesCcm`.</span><span class="sxs-lookup"><span data-stu-id="a5022-233">Support has been added for **AES-GCM** and **AES-CCM** ciphers, implemented via `System.Security.Cryptography.AesGcm` and `System.Security.Cryptography.AesCcm`.</span></span> <span data-ttu-id="a5022-234">Ces algorithmes sont de type [Authenticated Encryption with Association Data (AEAD)](https://en.wikipedia.org/wiki/Authenticated_encryption), et les premiers algorithmes Authenticated Encryption (AE) ont été ajoutés à .NET Core.</span><span class="sxs-lookup"><span data-stu-id="a5022-234">These algorithms are both [Authenticated Encryption with Association Data (AEAD) algorithms](https://en.wikipedia.org/wiki/Authenticated_encryption), and the first Authenticated Encryption (AE) algorithms added to .NET Core.</span></span>

<span data-ttu-id="a5022-235">Le code suivant montre l’utilisation du chiffrement **AesGcm** pour chiffrer et déchiffrer des données aléatoires.</span><span class="sxs-lookup"><span data-stu-id="a5022-235">The following code demonstrates using **AesGcm** cipher to encrypt and decrypt random data.</span></span>

<span data-ttu-id="a5022-236">Le code pour **AesCcm** sera presque identique (seuls les noms des variables de classe seraient différents).</span><span class="sxs-lookup"><span data-stu-id="a5022-236">The code for **AesCcm** would look almost identical (only the class variable names would be different).</span></span>

```csharp
// key should be: pre-known, derived, or transported via another channel, such as RSA encryption
byte[] key = new byte[16];
RandomNumberGenerator.Fill(key);

byte[] nonce = new byte[12];
RandomNumberGenerator.Fill(nonce);

// normally this would be your data
byte[] dataToEncrypt = new byte[1234];
byte[] associatedData = new byte[333];
RandomNumberGenerator.Fill(dataToEncrypt);
RandomNumberGenerator.Fill(associatedData);

// these will be filled during the encryption
byte[] tag = new byte[16];
byte[] ciphertext = new byte[dataToEncrypt.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Encrypt(nonce, dataToEncrypt, ciphertext, tag, associatedData);
}

// tag, nonce, ciphertext, associatedData should be sent to the other part

byte[] decryptedData = new byte[ciphertext.Length];

using (AesGcm aesGcm = new AesGcm(key))
{
    aesGcm.Decrypt(nonce, ciphertext, tag, decryptedData, associatedData);
}

// do something with the data
// this should always print that data is the same
Console.WriteLine($"AES-GCM: Decrypted data is{(dataToEncrypt.SequenceEqual(decryptedData) ? "the same as" : "different than")} original data.");
```

## <a name="cryptographic-key-importexport"></a><span data-ttu-id="a5022-237">Importation/exportation d’une clé de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a5022-237">Cryptographic Key Import/Export</span></span>

<span data-ttu-id="a5022-238">.NET Core 3.0 Préversion 1 prend en charge l’importation et l’exportation de clés publiques et privées asymétriques aux formats standard, sans avoir à utiliser un certificat X.509.</span><span class="sxs-lookup"><span data-stu-id="a5022-238">.NET Core 3.0 Preview 1 supports the import and export of asymmetric public and private keys from standard formats, without needing to use an X.509 certificate.</span></span>

<span data-ttu-id="a5022-239">Tous les types de clés (RSA, DSA, ECDsa, ECDiffieHellman) prennent en charge le format **X.509 SubjectPublicKeyInfo** pour les clés publiques, et les formats **PKCS #8 PrivateKeyInfo** et **PKCS #8 EncryptedPrivateKeyInfo** pour les clés privées.</span><span class="sxs-lookup"><span data-stu-id="a5022-239">All key types (RSA, DSA, ECDsa, ECDiffieHellman) support the **X.509 SubjectPublicKeyInfo** format for public keys, and the **PKCS#8 PrivateKeyInfo** and **PKCS#8 EncryptedPrivateKeyInfo** formats for private keys.</span></span> <span data-ttu-id="a5022-240">Le chiffrement RSA prend également en charge **PKCS #1 RSAPublicKey** et **PKCS #1 RSAPrivateKey**.</span><span class="sxs-lookup"><span data-stu-id="a5022-240">RSA additionally supports **PKCS#1 RSAPublicKey** and **PKCS#1 RSAPrivateKey**.</span></span> <span data-ttu-id="a5022-241">Les méthodes d’exportation produisent toutes des données binaires encodées au format DER, tout comme les méthodes d’importation.</span><span class="sxs-lookup"><span data-stu-id="a5022-241">The export methods all produce DER-encoded binary data, and the import methods expect the same.</span></span> <span data-ttu-id="a5022-242">Si une clé est stockée au format PEM compatible avec le texte, l’appelant devra décoder le contenu au format base64 avant d’appeler une méthode d’importation.</span><span class="sxs-lookup"><span data-stu-id="a5022-242">If a key is stored in the text-friendly PEM format, the caller will need to base64-decode the content before calling an import method.</span></span>

```csharp
using System;
using System.IO;
using System.Security.Cryptography;

namespace rsakeyprint
{
    class Program
    {
        static void Main(string[] args)
        {
            using (RSA rsa = RSA.Create())
            {
                byte[] keyBytes = File.ReadAllBytes(args[0]);
                rsa.ImportRSAPrivateKey(keyBytes, out int bytesRead);
 
                Console.WriteLine($"Read {bytesRead} bytes, {keyBytes.Length-bytesRead} extra byte(s) in file.");
                RSAParameters rsaParameters = rsa.ExportParameters(true);
                Console.WriteLine(BitConverter.ToString(rsaParameters.D));
            }
        }
    }
}
```

```console
user@comp-ubuntu1810:~/rsakeyprint$ echo Making a small key to save on screen space.
Making a small key to save on screen space.
user@comp-ubuntu1810:~/rsakeyprint$ openssl genrsa 768 | openssl rsa -outform der -out rsa.key
Generating RSA private key, 768 bit long modulus (2 primes)
..+++++++
........+++++++
e is 65537 (0x010001)
writing RSA key
user@comp-ubuntu1810:~/rsakeyprint$ dotnet run rsa.key
Read 461 bytes, 0 extra byte(s) in file.
0F-D0-82-34-F8-13-38-4A-7F-C7-52-4A-F6-93-F8-FB-6D-98-7A-6A-04-3B-BC-35-8C-7D-AC-A5-A3-6E-AD-C1-66-30-81-2C-2A-DE-DA-60-03-6A-2C-D9-76-15-7F-61-97-57-
79-E1-6E-45-62-C3-83-04-97-CB-32-EF-C5-17-5F-99-60-92-AE-B6-34-6F-30-06-03-AC-BF-15-24-43-84-EB-83-60-EF-4D-3B-BD-D9-5D-56-26-F0-51-CE-F1
user@comp-ubuntu1810:~/rsakeyprint$ openssl rsa -in rsa.key -inform der -text -noout | grep -A7 private
privateExponent:
    0f:d0:82:34:f8:13:38:4a:7f:c7:52:4a:f6:93:f8:
    fb:6d:98:7a:6a:04:3b:bc:35:8c:7d:ac:a5:a3:6e:
    ad:c1:66:30:81:2c:2a:de:da:60:03:6a:2c:d9:76:
    15:7f:61:97:57:79:e1:6e:45:62:c3:83:04:97:cb:
    32:ef:c5:17:5f:99:60:92:ae:b6:34:6f:30:06:03:
    ac:bf:15:24:43:84:eb:83:60:ef:4d:3b:bd:d9:5d:
    56:26:f0:51:ce:f1
```

<span data-ttu-id="a5022-243">Les fichiers PKCS #8 peuvent être inspectés avec la classe `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo`.</span><span class="sxs-lookup"><span data-stu-id="a5022-243">PKCS#8 files can be inspected with the `System.Security.Cryptography.Pkcs.Pkcs8PrivateKeyInfo` class.</span></span>

<span data-ttu-id="a5022-244">Les fichiers PFX/PKCS#12 peuvent être inspectés et manipulés avec `System.Security.Cryptography.Pkcs.Pkcs12Info` et `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="a5022-244">PFX/PKCS#12 files can be inspected and manipulated with `System.Security.Cryptography.Pkcs.Pkcs12Info` and `System.Security.Cryptography.Pkcs.Pkcs12Builder`, respectively.</span></span>

## <a name="serialport-for-linux"></a><span data-ttu-id="a5022-245">SerialPort pour Linux</span><span class="sxs-lookup"><span data-stu-id="a5022-245">SerialPort for Linux</span></span>

<span data-ttu-id="a5022-246">.NET Core 3.0 prend désormais en charge <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> sous Linux.</span><span class="sxs-lookup"><span data-stu-id="a5022-246">.NET Core 3.0 now supports <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType> on Linux.</span></span>

<span data-ttu-id="a5022-247">Auparavant, .NET Core était uniquement pris en charge grâce au type `SerialPort` sous Windows.</span><span class="sxs-lookup"><span data-stu-id="a5022-247">Previously, .NET Core only supported using the `SerialPort` type on Windows.</span></span>

## <a name="more-bcl-improvements"></a><span data-ttu-id="a5022-248">Plusieurs améliorations BCL</span><span class="sxs-lookup"><span data-stu-id="a5022-248">More BCL Improvements</span></span>

<span data-ttu-id="a5022-249">Les types `Span<T>`, `Memory<T>` et autres types associés qui avaient été introduits dans .NET Core 2.1 ont été optimisées dans .NET Core 3.0.</span><span class="sxs-lookup"><span data-stu-id="a5022-249">The `Span<T>`, `Memory<T>`, and related types that were introduced in .NET Core 2.1, have been optimized in .NET Core 3.0.</span></span> <span data-ttu-id="a5022-250">Les opérations courantes comme la construction de type span, le découpage, l’analyse et la mise en forme sont maintenant plus performantes.</span><span class="sxs-lookup"><span data-stu-id="a5022-250">Common operations such as span construction, slicing, parsing, and formatting now perform better.</span></span> 

<span data-ttu-id="a5022-251">En outre, les types comme `String` ont bénéficié d’améliorations en arrière-plan pour les rendre plus efficaces lorsqu’ils sont utilisés comme des clés avec `Dictionary<TKey, TValue>` et d’autres collections.</span><span class="sxs-lookup"><span data-stu-id="a5022-251">Additionally, types like `String` have seen under-the-cover improvements to make them more efficient when used as keys with `Dictionary<TKey, TValue>` and other collections.</span></span> <span data-ttu-id="a5022-252">Aucune modification de code n’est nécessaire pour tirer parti de ces améliorations.</span><span class="sxs-lookup"><span data-stu-id="a5022-252">No code changes are required to benefit from these improvements.</span></span>

<span data-ttu-id="a5022-253">Les améliorations suivantes sont également des nouveautés dans .NET Core 3 Préversion 1 :</span><span class="sxs-lookup"><span data-stu-id="a5022-253">The following improvements are also new in .NET Core 3 Preview 1:</span></span>

* <span data-ttu-id="a5022-254">Prise en charge de Brotli intégrée à HttpClient</span><span class="sxs-lookup"><span data-stu-id="a5022-254">Brotli support built in to HttpClient</span></span>
* <span data-ttu-id="a5022-255">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span><span class="sxs-lookup"><span data-stu-id="a5022-255">ThreadPool.UnsafeQueueWorkItem(IThreadPoolWorkItem)</span></span>
* <span data-ttu-id="a5022-256">Unsafe.Unbox</span><span class="sxs-lookup"><span data-stu-id="a5022-256">Unsafe.Unbox</span></span>
* <span data-ttu-id="a5022-257">CancellationToken.Unregister</span><span class="sxs-lookup"><span data-stu-id="a5022-257">CancellationToken.Unregister</span></span>
* <span data-ttu-id="a5022-258">Opérateurs arithmétiques complexes</span><span class="sxs-lookup"><span data-stu-id="a5022-258">Complex arithmetic operators</span></span>
* <span data-ttu-id="a5022-259">API de socket pour TCP keep alive</span><span class="sxs-lookup"><span data-stu-id="a5022-259">Socket APIs for TCP keep alive</span></span>
* <span data-ttu-id="a5022-260">StringBuilder.GetChunks</span><span class="sxs-lookup"><span data-stu-id="a5022-260">StringBuilder.GetChunks</span></span>
* <span data-ttu-id="a5022-261">Analyse IPEndPoint</span><span class="sxs-lookup"><span data-stu-id="a5022-261">IPEndPoint parsing</span></span>
* <span data-ttu-id="a5022-262">RandomNumberGenerator.GetInt32</span><span class="sxs-lookup"><span data-stu-id="a5022-262">RandomNumberGenerator.GetInt32</span></span>

## <a name="tiered-compilation"></a><span data-ttu-id="a5022-263">Compilation hiérarchisée</span><span class="sxs-lookup"><span data-stu-id="a5022-263">Tiered compilation</span></span>

<span data-ttu-id="a5022-264">La [compilation hiérarchisée](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/) est activée par défaut avec .NET Core 3.0.</span><span class="sxs-lookup"><span data-stu-id="a5022-264">[Tiered compilation](https://blogs.msdn.microsoft.com/dotnet/2018/08/02/tiered-compilation-preview-in-net-core-2-1/) is on by default with .NET Core 3.0.</span></span> <span data-ttu-id="a5022-265">Cette fonctionnalité permet au runtime d’utiliser de manière plus adaptative le compilateur juste-à-temps (Just-In-Time ou JIT) pour obtenir de meilleures performances, à la fois au démarrage et pour optimiser le débit.</span><span class="sxs-lookup"><span data-stu-id="a5022-265">It is a feature that enables the runtime to more adaptively use the Just-In-Time (JIT) compiler to get better performance, both at startup and to maximize throughput.</span></span>

<span data-ttu-id="a5022-266">Cette fonctionnalité avait été ajoutée en option dans [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) et était activée par défaut dans [.NET Core 2.2 Préversion 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/).</span><span class="sxs-lookup"><span data-stu-id="a5022-266">This feature was added as an opt-in feature in [.NET Core 2.1](https://blogs.msdn.microsoft.com/dotnet/2018/05/30/announcing-net-core-2-1/) and then was enabled by default in [.NET Core 2.2 Preview 2](https://blogs.msdn.microsoft.com/dotnet/2018/09/12/announcing-net-core-2-2-preview-2/).</span></span> <span data-ttu-id="a5022-267">Elle est ensuite redevenue une option dans la version .NET Core 2.2.</span><span class="sxs-lookup"><span data-stu-id="a5022-267">Subsequently, it has been reverted back to opt in with the .NET Core 2.2 release.</span></span>

## <a name="arm64-linux-support"></a><span data-ttu-id="a5022-268">Support ARM64 Linux</span><span class="sxs-lookup"><span data-stu-id="a5022-268">ARM64 Linux support</span></span>

<span data-ttu-id="a5022-269">Nous ajoutons la prise en charge de ARM64 sous Linux dans cette version.</span><span class="sxs-lookup"><span data-stu-id="a5022-269">We are adding support for ARM64 for Linux this release.</span></span> <span data-ttu-id="a5022-270">Pour le contexte, nous avons ajouté la prise en charge d’ARM32 sous Linux avec .NET Core 2.1, et sous Windows avec .NET Core 2.2.</span><span class="sxs-lookup"><span data-stu-id="a5022-270">For context, we added support for ARM32 for Linux with .NET Core 2.1 and Windows with .NET Core 2.2.</span></span> <span data-ttu-id="a5022-271">Actuellement, ARM64 est principallement utilisé dans des scénarios IoT.</span><span class="sxs-lookup"><span data-stu-id="a5022-271">The primary use case for ARM64 is currently with IoT scenarios.</span></span>

<span data-ttu-id="a5022-272">Des [images Docker Alpine, Debian et Ubuntu sont disponibles avec .NET Core pour ARM64](https://hub.docker.com/r/microsoft/dotnet/).</span><span class="sxs-lookup"><span data-stu-id="a5022-272">Alpine, Debian and Ubuntu [Docker images are available for .NET Core for ARM64](https://hub.docker.com/r/microsoft/dotnet/).</span></span>

<span data-ttu-id="a5022-273">Consultez [État de .NET Core ARM64](https://github.com/dotnet/announcements/issues/82) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a5022-273">Please check [.NET Core ARM64 Status](https://github.com/dotnet/announcements/issues/82) for more information.</span></span>

>[!NOTE]
> <span data-ttu-id="a5022-274">La prise en charge d’**ARM64** sous Windows n’est pas encore disponible.</span><span class="sxs-lookup"><span data-stu-id="a5022-274">**ARM64** Windows support isn't yet available.</span></span>
