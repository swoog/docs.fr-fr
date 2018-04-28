---
title: Développement de bibliothèques avec des outils multiplateformes
description: Découvrez comment créer des bibliothèques pour .NET à l’aide des outils de l’interface de ligne de commande .NET Core.
author: cartermp
ms.author: mairaw
ms.date: 05/01/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.workload:
- dotnetcore
ms.openlocfilehash: 6bdb5b11a54ce23c676d10ef6e440fa46ea12f72
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="developing-libraries-with-cross-platform-tools"></a><span data-ttu-id="4018c-103">Développement de bibliothèques avec des outils multiplateformes</span><span class="sxs-lookup"><span data-stu-id="4018c-103">Developing Libraries with Cross Platform Tools</span></span>

<span data-ttu-id="4018c-104">Cet article explique comment écrire des bibliothèques pour .NET à l’aide des outils CLI multiplateformes.</span><span class="sxs-lookup"><span data-stu-id="4018c-104">This article covers how to write libraries for .NET using cross-platform CLI tools.</span></span> <span data-ttu-id="4018c-105">L’interface CLI fournit une expérience efficace et de bas niveau qui fonctionne sur tous les systèmes d’exploitation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4018c-105">The CLI provides an efficient and low-level experience that works across any supported OS.</span></span> <span data-ttu-id="4018c-106">Vous pouvez toujours créer des bibliothèques avec Visual Studio, et si c’est ce que vous préférez, [consultez le guide Visual Studio](libraries-with-vs.md).</span><span class="sxs-lookup"><span data-stu-id="4018c-106">You can still build libraries with Visual Studio, and if that is your preferred experience [refer to the Visual Studio guide](libraries-with-vs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4018c-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="4018c-107">Prerequisites</span></span>

<span data-ttu-id="4018c-108">[Le SDK .NET Core et l’interface CLI](https://www.microsoft.com/net/core) doivent être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4018c-108">You need [the .NET Core SDK and CLI](https://www.microsoft.com/net/core) installed on your machine.</span></span>

<span data-ttu-id="4018c-109">Pour accéder aux sections de ce document concernant les versions du .NET Framework, vous devez installer le [.NET Framework](http://getdotnet.azurewebsites.net/) sur un ordinateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4018c-109">For the sections of this document dealing with .NET Framework versions, you need the [.NET Framework](http://getdotnet.azurewebsites.net/) installed on a Windows machine.</span></span>

<span data-ttu-id="4018c-110">De plus, si vous voulez prendre en charge des cibles .NET Framework antérieures, vous devez installer les packs de ciblage/développeur des versions antérieures du Framework à partir de la [page de plateformes cibles .NET](http://getdotnet.azurewebsites.net/target-dotnet-platforms.html).</span><span class="sxs-lookup"><span data-stu-id="4018c-110">Additionally, if you wish to support older .NET Framework targets, you need to install targeting/developer packs for older framework versions from the [.NET target platforms page](http://getdotnet.azurewebsites.net/target-dotnet-platforms.html).</span></span> <span data-ttu-id="4018c-111">Reportez-vous au tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="4018c-111">Refer to this table:</span></span>

| <span data-ttu-id="4018c-112">Version du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4018c-112">.NET Framework Version</span></span> | <span data-ttu-id="4018c-113">À télécharger</span><span class="sxs-lookup"><span data-stu-id="4018c-113">What to download</span></span>                                       |
| ---------------------- | ------------------------------------------------------ |
| <span data-ttu-id="4018c-114">4.6.1</span><span class="sxs-lookup"><span data-stu-id="4018c-114">4.6.1</span></span>                  | <span data-ttu-id="4018c-115">Pack de ciblage .NET Framework 4.6.1</span><span class="sxs-lookup"><span data-stu-id="4018c-115">.NET Framework 4.6.1 Targeting Pack</span></span>                    |
| <span data-ttu-id="4018c-116">4.6</span><span class="sxs-lookup"><span data-stu-id="4018c-116">4.6</span></span>                    | <span data-ttu-id="4018c-117">Pack de ciblage .NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="4018c-117">.NET Framework 4.6 Targeting Pack</span></span>                      |
| <span data-ttu-id="4018c-118">4.5.2</span><span class="sxs-lookup"><span data-stu-id="4018c-118">4.5.2</span></span>                  | <span data-ttu-id="4018c-119">Pack du développeur .NET Framework 4.5.2</span><span class="sxs-lookup"><span data-stu-id="4018c-119">.NET Framework 4.5.2 Developer Pack</span></span>                    |
| <span data-ttu-id="4018c-120">4.5.1</span><span class="sxs-lookup"><span data-stu-id="4018c-120">4.5.1</span></span>                  | <span data-ttu-id="4018c-121">Pack du développeur .NET Framework 4.5.1</span><span class="sxs-lookup"><span data-stu-id="4018c-121">.NET Framework 4.5.1 Developer Pack</span></span>                    |
| <span data-ttu-id="4018c-122">4.5</span><span class="sxs-lookup"><span data-stu-id="4018c-122">4.5</span></span>                    | <span data-ttu-id="4018c-123">SDK Windows pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="4018c-123">Windows Software Development Kit for Windows 8</span></span>         |
| <span data-ttu-id="4018c-124">4.0</span><span class="sxs-lookup"><span data-stu-id="4018c-124">4.0</span></span>                    | <span data-ttu-id="4018c-125">SDK pour Windows 7 et .NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="4018c-125">Windows SDK for Windows 7 and .NET Framework 4</span></span>         |
| <span data-ttu-id="4018c-126">2.0, 3.0 et 3.5</span><span class="sxs-lookup"><span data-stu-id="4018c-126">2.0, 3.0, and 3.5</span></span>      | <span data-ttu-id="4018c-127">Runtime .NET Framework 3.5 SP1 (ou version Windows 8+)</span><span class="sxs-lookup"><span data-stu-id="4018c-127">.NET Framework 3.5 SP1 Runtime (or Windows 8+ version)</span></span> |

## <a name="how-to-target-the-net-standard"></a><span data-ttu-id="4018c-128">Comment cibler .NET Standard</span><span class="sxs-lookup"><span data-stu-id="4018c-128">How to target the .NET Standard</span></span>

<span data-ttu-id="4018c-129">Si vous ne connaissez pas très bien .NET Standard, référez-vous à la page [.NET Standard](../../standard/net-standard.md) pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="4018c-129">If you're not quite familiar with the .NET Standard, refer to the [.NET Standard](../../standard/net-standard.md) to learn more.</span></span>

<span data-ttu-id="4018c-130">Voici un tableau qui associe les versions .NET Standard à diverses implémentations :</span><span class="sxs-lookup"><span data-stu-id="4018c-130">In that article, there is a table which maps .NET Standard versions to various implementations:</span></span>

[!INCLUDE [net-standard-table](~/includes/net-standard-table.md)]

<span data-ttu-id="4018c-131">Voici ce que signifie ce tableau dans le processus de création d’une bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="4018c-131">Here's what this table means for the purposes of creating a library:</span></span>

<span data-ttu-id="4018c-132">La version de .NET Standard que vous choisissez est un compromis entre l’accès aux API les plus récentes et la possibilité de cibler plus d’implémentations .NET et de versions .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="4018c-132">The version of the .NET Standard you pick will be a tradeoff between access to the newest APIs and the ability to target more .NET implementations and .NET Standard versions.</span></span> <span data-ttu-id="4018c-133">Vous contrôlez la plage de versions et de plateformes pouvant être ciblées en sélectionnant une version de `netstandardX.X` (où `X.X` est un numéro de version), puis en l’ajoutant à votre fichier projet (`.csproj` ou `.fsproj`).</span><span class="sxs-lookup"><span data-stu-id="4018c-133">You control the range of targetable platforms and versions by picking a version of `netstandardX.X` (Where `X.X` is a version number) and adding it to your project file (`.csproj` or `.fsproj`).</span></span>

<span data-ttu-id="4018c-134">Vous disposez de trois options principales quand vous ciblez .NET Standard, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4018c-134">You have three primary options when targeting the .NET Standard, depending on your needs.</span></span>

1. <span data-ttu-id="4018c-135">Vous pouvez utiliser la version par défaut de .NET Standard fournie par les modèles (`netstandard1.4`). Celle-ci vous donne accès à la plupart des API sur .NET Standard tout en étant compatible avec UWP, le .NET Framework  4.6.1 et le prochain .NET Standard 2.0.</span><span class="sxs-lookup"><span data-stu-id="4018c-135">You can use the default version of the .NET Standard supplied by templates - `netstandard1.4` - which gives you access to most APIs on .NET Standard while still being compatible with UWP, .NET Framework 4.6.1, and the forthcoming .NET Standard 2.0.</span></span>

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
      <PropertyGroup>
        <TargetFramework>netstandard1.4</TargetFramework>
      </PropertyGroup>
    </Project>
    ```

2. <span data-ttu-id="4018c-136">Vous pouvez utiliser une version inférieure ou supérieure de .NET Standard en modifiant la valeur dans le nœud `TargetFramework` de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="4018c-136">You can use a lower or higher version of the .NET Standard by modifying the value in the `TargetFramework` node of your project file.</span></span>
    
    <span data-ttu-id="4018c-137">Les versions .NET standard sont à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="4018c-137">.NET Standard versions are backward compatible.</span></span> <span data-ttu-id="4018c-138">Cela signifie que les bibliothèques `netstandard1.0` s’exécutent sur les plateformes `netstandard1.1` et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4018c-138">That means that `netstandard1.0` libraries run on `netstandard1.1` platforms and higher.</span></span> <span data-ttu-id="4018c-139">Toutefois, il n’existe pas de compatibilité ascendante : les plateformes .NET Standard antérieures ne peuvent pas référencer les plateformes ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4018c-139">However, there is no forward compatibility - lower .NET Standard platforms cannot reference higher ones.</span></span> <span data-ttu-id="4018c-140">Cela signifie que les bibliothèques `netstandard1.0` ne peuvent pas cibler des bibliothèques de référence ciblant `netstandard1.1` ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4018c-140">This means that `netstandard1.0` libraries cannot reference libraries targeting `netstandard1.1` or higher.</span></span> <span data-ttu-id="4018c-141">Sélectionnez la version Standard qui offre une bonne combinaison entre les API et la prise en charge de plateformes pour vos besoins.</span><span class="sxs-lookup"><span data-stu-id="4018c-141">Select the Standard version that has the right mix of APIs and platform support for your needs.</span></span> <span data-ttu-id="4018c-142">Nous vous recommandons d’utiliser `netstandard1.4` pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="4018c-142">We recommend `netstandard1.4` for now.</span></span>
    
3. <span data-ttu-id="4018c-143">Si vous voulez cibler les versions .NET Framework 4.0 ou antérieures, ou que vous voulez utiliser une API disponible dans le .NET Framework, mais pas dans .NET Standard (par exemple, `System.Drawing`), lisez les sections suivantes et découvrez comment réaliser un multiciblage.</span><span class="sxs-lookup"><span data-stu-id="4018c-143">If you want to target the .NET Framework versions 4.0 or below, or you wish to use an API available in the .NET Framework but not in the .NET Standard (for example, `System.Drawing`), read the following sections and learn how to multitarget.</span></span>

## <a name="how-to-target-the-net-framework"></a><span data-ttu-id="4018c-144">Comment cibler le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4018c-144">How to target the .NET Framework</span></span>

> [!NOTE]
> <span data-ttu-id="4018c-145">Les instructions suivantes supposent que le .NET Framework est installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4018c-145">These instructions assume you have the .NET Framework installed on your machine.</span></span> <span data-ttu-id="4018c-146">Reportez-vous aux [Prérequis](#prerequisites) pour installer les dépendances.</span><span class="sxs-lookup"><span data-stu-id="4018c-146">Refer to the [Prerequisites](#prerequisites) to get dependencies installed.</span></span>

<span data-ttu-id="4018c-147">N’oubliez pas que certaines des versions du .NET Framework utilisées ici ne sont plus prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4018c-147">Keep in mind that some of the .NET Framework versions used here are no longer in support.</span></span> <span data-ttu-id="4018c-148">Reportez-vous au [Forum aux questions sur la politique de support de Microsoft .NET Framework](https://support.microsoft.com/gp/framework_faq/en-us) concernant les versions non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4018c-148">Refer to the [.NET Framework Support Lifecycle Policy FAQ](https://support.microsoft.com/gp/framework_faq/en-us) about unsupported versions.</span></span>

<span data-ttu-id="4018c-149">Si vous voulez atteindre le nombre maximal de développeurs et de projets, utilisez le .NET Framework 4.0 comme cible de base de référence.</span><span class="sxs-lookup"><span data-stu-id="4018c-149">If you want to reach the maximum number of developers and projects, use the .NET Framework 4.0 as your baseline target.</span></span> <span data-ttu-id="4018c-150">Pour cibler le .NET Framework, vous devez commencer par utiliser le Moniker du Framework cible approprié qui correspond à la version du .NET Framework que vous voulez prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4018c-150">To target the .NET Framework, you will need to begin by using the correct Target Framework Moniker (TFM) that corresponds to the .NET Framework version you wish to support.</span></span>

```
.NET Framework 2.0   --> net20
.NET Framework 3.0   --> net30
.NET Framework 3.5   --> net35
.NET Framework 4.0   --> net40
.NET Framework 4.5   --> net45
.NET Framework 4.5.1 --> net451
.NET Framework 4.5.2 --> net452
.NET Framework 4.6   --> net46
.NET Framework 4.6.1 --> net461
.NET Framework 4.6.2 --> net462
.NET Framework 4.7   --> net47
```

<span data-ttu-id="4018c-151">Insérez ensuite ce Moniker du Framework cible dans la section `TargetFramework` de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="4018c-151">You then insert this TFM into the `TargetFramework` section of your project file.</span></span> <span data-ttu-id="4018c-152">Par exemple, voici comment écrire une bibliothèque qui cible le .NET Framework 4.0 :</span><span class="sxs-lookup"><span data-stu-id="4018c-152">For example, here's how you would write a library which targets the .NET Framework 4.0:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFramework>net40</TargetFramework>
  </PropertyGroup>
</Project>
```

<span data-ttu-id="4018c-153">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="4018c-153">And that's it!</span></span> <span data-ttu-id="4018c-154">Bien que ce code se compilait uniquement pour .NET Framework 4, vous pouvez utiliser la bibliothèque sur des versions plus récentes du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4018c-154">Although this compiled only for the .NET Framework 4, you can use the library on newer versions of the .NET Framework.</span></span>

## <a name="how-to-multitarget"></a><span data-ttu-id="4018c-155">Comment multicibler</span><span class="sxs-lookup"><span data-stu-id="4018c-155">How to Multitarget</span></span>

> [!NOTE]
> <span data-ttu-id="4018c-156">Les instructions suivantes supposent que le .NET Framework est installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4018c-156">The following instructions assume you have the .NET Framework installed on your machine.</span></span> <span data-ttu-id="4018c-157">Reportez-vous à la section [Prérequis](#prerequisites) pour savoir quelles dépendances doivent être installées et à partir d’où les télécharger.</span><span class="sxs-lookup"><span data-stu-id="4018c-157">Refer to the [Prerequisites](#prerequisites) section to learn which dependencies you need to install and where to download them from.</span></span>

<span data-ttu-id="4018c-158">Vous devrez peut-être cibler des versions antérieures du .NET Framework si votre projet prend en charge à la fois .NET Framework et .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4018c-158">You may need to target older versions of the .NET Framework when your project supports both the .NET Framework and .NET Core.</span></span> <span data-ttu-id="4018c-159">Dans ce scénario, si vous voulez utiliser des API et des constructions de langage plus récentes pour des cibles plus récentes, utilisez des directives `#if` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="4018c-159">In this scenario, if you want to use newer APIs and language constructs for the newer targets, use `#if` directives in your code.</span></span> <span data-ttu-id="4018c-160">Vous pouvez aussi avoir besoin d’ajouter différents packages et différentes dépendances pour chaque plateforme que vous ciblez pour inclure les différentes API nécessaires à chaque cas.</span><span class="sxs-lookup"><span data-stu-id="4018c-160">You also might need to add different packages and dependencies for each platform you're targeting to include the different APIs needed for each case.</span></span>

<span data-ttu-id="4018c-161">Supposons, par exemple, que vous avez une bibliothèque qui effectue des opérations réseau sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="4018c-161">For example, let's say you have a library that performs networking operations over HTTP.</span></span> <span data-ttu-id="4018c-162">Pour .NET Standard et les versions .NET Framework 4.5 ou ultérieures, vous pouvez utiliser la classe `HttpClient` à partir de l’espace de noms `System.Net.Http`.</span><span class="sxs-lookup"><span data-stu-id="4018c-162">For .NET Standard and the .NET Framework versions 4.5 or higher, you can use the `HttpClient` class from the `System.Net.Http` namespace.</span></span> <span data-ttu-id="4018c-163">Toutefois, les versions antérieures du .NET Framework ne disposent pas de la classe `HttpClient`. Vous pourriez donc utiliser la classe `WebClient` à partir de l’espace de noms `System.Net` à la place.</span><span class="sxs-lookup"><span data-stu-id="4018c-163">However, earlier versions of the .NET Framework don't have the `HttpClient` class, so you could use the `WebClient` class from the `System.Net` namespace for those instead.</span></span>

<span data-ttu-id="4018c-164">Voici à quoi peut ressembler votre fichier projet :</span><span class="sxs-lookup"><span data-stu-id="4018c-164">Your project file could look like this:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <TargetFrameworks>netstandard1.4;net40;net45</TargetFrameworks>
  </PropertyGroup>

  <!-- Need to conditionally bring in references for the .NET Framework 4.0 target -->
  <ItemGroup Condition="'$(TargetFramework)' == 'net40'">
    <Reference Include="System.Net" />
  </ItemGroup>

  <!-- Need to conditionally bring in references for the .NET Framework 4.5 target -->
  <ItemGroup Condition="'$(TargetFramework)' == 'net45'">
    <Reference Include="System.Net.Http" />
    <Reference Include="System.Threading.Tasks" />
  </ItemGroup>
</Project>
```

<span data-ttu-id="4018c-165">Notez trois changements majeurs ici :</span><span class="sxs-lookup"><span data-stu-id="4018c-165">You'll notice three major changes here:</span></span>

1. <span data-ttu-id="4018c-166">Le nœud `TargetFramework` a été remplacé par `TargetFrameworks`, et trois Monikers du Framework cible sont exprimés à l’intérieur.</span><span class="sxs-lookup"><span data-stu-id="4018c-166">The `TargetFramework` node has been replaced by `TargetFrameworks`, and three TFMs are expressed inside.</span></span>
1. <span data-ttu-id="4018c-167">Un nœud `<ItemGroup>` est présent pour l’extraction de cible `net40 ` dans une référence .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4018c-167">There is an `<ItemGroup>` node for the `net40 ` target pulling in one .NET Framework reference.</span></span>
1. <span data-ttu-id="4018c-168">Un nœud `<ItemGroup>` est présent pour l’extraction de cible `net45` dans deux références .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4018c-168">There is an `<ItemGroup>` node for the `net45` target pulling in two .NET Framework references.</span></span>

<span data-ttu-id="4018c-169">Le système de build est informé des symboles de préprocesseur suivants utilisés dans les directives `#if`:</span><span class="sxs-lookup"><span data-stu-id="4018c-169">The build system is aware of the following preprocessor symbols used in `#if` directives:</span></span>

[!INCLUDE [Preprocessor symbols](~/includes/preprocessor-symbols.md)]

<span data-ttu-id="4018c-170">Voici un exemple d’utilisation de la compilation conditionnelle par cible :</span><span class="sxs-lookup"><span data-stu-id="4018c-170">Here is an example making use of conditional compilation per-target:</span></span>

```csharp
using System;
using System.Text.RegularExpressions;
#if NET40
// This only compiles for the .NET Framework 4 targets
using System.Net;
#else
 // This compiles for all other targets
using System.Net.Http;
using System.Threading.Tasks;
#endif

namespace MultitargetLib
{
    public class Library
    {
#if NET40
        private readonly WebClient _client = new WebClient();
        private readonly object _locker = new object();
#else
        private readonly HttpClient _client = new HttpClient();
#endif

#if NET40
        // .NET Framework 4.0 does not have async/await
        public string GetDotNetCount()
        {
            string url = "http://www.dotnetfoundation.org/";

            var uri = new Uri(url);

            string result = "";

            // Lock here to provide thread-safety.
            lock(_locker)
            {
                result = _client.DownloadString(uri);
            }

            int dotNetCount = Regex.Matches(result, ".NET").Count;

            return $"Dotnet Foundation mentions .NET {dotNetCount} times!";
        }
#else
        // .NET 4.5+ can use async/await!
        public async Task<string> GetDotNetCountAsync()
        {
            string url = "http://www.dotnetfoundation.org/";

            // HttpClient is thread-safe, so no need to explicitly lock here
            var result = await _client.GetStringAsync(url);

            int dotNetCount = Regex.Matches(result, ".NET").Count;

            return $"dotnetfoundation.org mentions .NET {dotNetCount} times in its HTML!";
        }
#endif
    }
}
```

<span data-ttu-id="4018c-171">Si vous générez ce projet avec `dotnet build`, notez la présence de trois répertoires sous le dossier `bin/` :</span><span class="sxs-lookup"><span data-stu-id="4018c-171">If you build this project with `dotnet build`, you'll notice three directories under the `bin/` folder:</span></span>

```
net40/
net45/
netstandard1.4/
```

<span data-ttu-id="4018c-172">Chacun d’entre eux contient les fichiers `.dll` pour chaque cible.</span><span class="sxs-lookup"><span data-stu-id="4018c-172">Each of these contain the `.dll` files for each target.</span></span>

## <a name="how-to-test-libraries-on-net-core"></a><span data-ttu-id="4018c-173">Comment tester les bibliothèques sur .NET Core</span><span class="sxs-lookup"><span data-stu-id="4018c-173">How to test libraries on .NET Core</span></span>

<span data-ttu-id="4018c-174">Il est important de pouvoir effectuer des tests sur plusieurs plateformes.</span><span class="sxs-lookup"><span data-stu-id="4018c-174">It's important to be able to test across platforms.</span></span> <span data-ttu-id="4018c-175">Vous pouvez utiliser [xUnit](http://xunit.github.io/) ou MSTest dans leur version d’origine.</span><span class="sxs-lookup"><span data-stu-id="4018c-175">You can use either [xUnit](http://xunit.github.io/) or MSTest out of the box.</span></span> <span data-ttu-id="4018c-176">Les deux conviennent parfaitement à la réalisation de tests unitaires sur votre bibliothèque sur .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4018c-176">Both are perfectly suitable for unit testing your library on .NET Core.</span></span> <span data-ttu-id="4018c-177">La façon dont vous configurez votre solution avec des projets de test dépend de la [structure de votre solution](#structuring-a-solution).</span><span class="sxs-lookup"><span data-stu-id="4018c-177">How you set up your solution with test projects will depend on the [structure of your solution](#structuring-a-solution).</span></span> <span data-ttu-id="4018c-178">L’exemple suivant part du principe que les répertoires de test et source résident dans le même répertoire de premier niveau.</span><span class="sxs-lookup"><span data-stu-id="4018c-178">The following example assumes that the test and source directories live in the same top-level directory.</span></span>

> [!NOTE]
> <span data-ttu-id="4018c-179">Cet exemple utilise certaines [commandes CLI .NET Core](../tools/index.md).</span><span class="sxs-lookup"><span data-stu-id="4018c-179">This uses some [.NET Core CLI commands](../tools/index.md).</span></span> <span data-ttu-id="4018c-180">Pour plus d’informations, consultez [dotnet new](../tools/dotnet-new.md) et [dotnet sln](../tools/dotnet-sln.md).</span><span class="sxs-lookup"><span data-stu-id="4018c-180">See [dotnet new](../tools/dotnet-new.md) and [dotnet sln](../tools/dotnet-sln.md) for more information.</span></span>

1. <span data-ttu-id="4018c-181">Configurez votre solution.</span><span class="sxs-lookup"><span data-stu-id="4018c-181">Set up your solution.</span></span> <span data-ttu-id="4018c-182">Pour cela, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4018c-182">You can do so with the following commands:</span></span>

   ```bash
   mkdir SolutionWithSrcAndTest
   cd SolutionWithSrcAndTest
   dotnet new sln
   dotnet new classlib -o MyProject
   dotnet new xunit -o MyProject.Test
   dotnet sln add MyProject/MyProject.csproj
   dotnet sln add MyProject.Test/MyProject.Test.csproj
   ```

   <span data-ttu-id="4018c-183">Cette commande crée des projets et les relie dans une solution.</span><span class="sxs-lookup"><span data-stu-id="4018c-183">This will create projects and link them together in a solution.</span></span> <span data-ttu-id="4018c-184">Votre répertoire pour `SolutionWithSrcAndTest` doit ressembler à ceci :</span><span class="sxs-lookup"><span data-stu-id="4018c-184">Your directory for `SolutionWithSrcAndTest` should look like this:</span></span>

   ```
   /SolutionWithSrcAndTest
   |__SolutionWithSrcAndTest.sln
   |__MyProject/
   |__MyProject.Test/
   ```

1. <span data-ttu-id="4018c-185">Accédez au répertoire du projet de test et ajoutez une référence à `MyProject.Test` à partir de `MyProject`.</span><span class="sxs-lookup"><span data-stu-id="4018c-185">Navigate to the test project's directory and add a reference to `MyProject.Test` from `MyProject`.</span></span>

   ```bash
   cd MyProject.Test
   dotnet add reference ../MyProject/MyProject.csproj
   ```

1. <span data-ttu-id="4018c-186">Restaurez les packages et générez les projets :</span><span class="sxs-lookup"><span data-stu-id="4018c-186">Restore packages and build projects:</span></span>

   ```bash
   dotnet restore
   dotnet build
   ```

   [!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

1. <span data-ttu-id="4018c-187">Exécutez la commande `dotnet test` pour vérifier que xUnit s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4018c-187">Verify that xUnit runs by executing the `dotnet test` command.</span></span> <span data-ttu-id="4018c-188">Si vous avez choisi d’utiliser MSTest, le Test Runner de console MSTest doit s’exécuter à la place.</span><span class="sxs-lookup"><span data-stu-id="4018c-188">If you chose to use MSTest, then the MSTest console runner should run instead.</span></span>
    
<span data-ttu-id="4018c-189">Et voilà !</span><span class="sxs-lookup"><span data-stu-id="4018c-189">And that's it!</span></span> <span data-ttu-id="4018c-190">Vous pouvez maintenant tester votre bibliothèque sur toutes les plateformes à l’aide des outils en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4018c-190">You can now test your library across all platforms using command line tools.</span></span> <span data-ttu-id="4018c-191">Maintenant que vous avez tout configuré, le test de votre bibliothèque est très simple :</span><span class="sxs-lookup"><span data-stu-id="4018c-191">To continue testing now that you have everything set up, testing your library is very simple:</span></span>

1. <span data-ttu-id="4018c-192">Apportez des modifications à votre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4018c-192">Make changes to your library.</span></span>
1. <span data-ttu-id="4018c-193">Exécutez les tests à partir de la ligne de commande, dans votre répertoire de test, avec la commande `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="4018c-193">Run tests from the command line, in your test directory, with `dotnet test` command.</span></span>

<span data-ttu-id="4018c-194">Votre code est automatiquement régénéré quand vous appelez la commande `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="4018c-194">Your code will be automatically rebuilt when you invoke `dotnet test` command.</span></span>

## <a name="how-to-use-multiple-projects"></a><span data-ttu-id="4018c-195">Comment utiliser plusieurs projets</span><span class="sxs-lookup"><span data-stu-id="4018c-195">How to use multiple projects</span></span>

<span data-ttu-id="4018c-196">Les bibliothèques plus volumineuses ont souvent besoin de placer des fonctionnalités dans différents projets.</span><span class="sxs-lookup"><span data-stu-id="4018c-196">A common need for larger libraries is to place functionality in different projects.</span></span>

<span data-ttu-id="4018c-197">Imaginez que vous vouliez créer une bibliothèque pouvant être utilisée en langage C# et F#.</span><span class="sxs-lookup"><span data-stu-id="4018c-197">Imagine you wished to build a library which could be consumed in idiomatic C# and F#.</span></span> <span data-ttu-id="4018c-198">Cela signifierait que les consommateurs de votre bibliothèque les utilisent dans des formes qui sont naturelles en C# ou F#.</span><span class="sxs-lookup"><span data-stu-id="4018c-198">That would mean that consumers of your library consume them in ways which are natural to C# or F#.</span></span> <span data-ttu-id="4018c-199">Par exemple, en C#, vous pouvez utiliser la bibliothèque de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="4018c-199">For example, in C# you might consume the library like this:</span></span>

```csharp
using AwesomeLibrary.CSharp;

public Task DoThings(Data data)
{
    var convertResult = await AwesomeLibrary.ConvertAsync(data);
    var result = AwesomeLibrary.Process(convertResult);
    // do something with result
}
```

<span data-ttu-id="4018c-200">En F#, le code peut se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="4018c-200">In F#, it might look like this:</span></span>

```fsharp
open AwesomeLibrary.FSharp

let doWork data = async {
    let! result = AwesomeLibrary.AsyncConvert data // Uses an F# async function rather than C# async method
    // do something with result
}
```

<span data-ttu-id="4018c-201">Les scénarios de consommation tels que celui-ci signifient que les API auxquelles vous accédez ont une structure différente en C# et F#.</span><span class="sxs-lookup"><span data-stu-id="4018c-201">Consumption scenarios like this mean that the APIs being accessed have to have a different structure for C# and F#.</span></span>  <span data-ttu-id="4018c-202">Pour réaliser ceci, il est courant de factoriser toute la logique d’une bibliothèque dans un projet principal et d’avoir des projets C# et F# définissant les couches API qui effectuent des appels à ce projet principal.</span><span class="sxs-lookup"><span data-stu-id="4018c-202">A common approach to accomplishing this is to factor all of the logic of a library into a core project, with C# and F# projects defining the API layers that call into that core project.</span></span>  <span data-ttu-id="4018c-203">Le reste de la section utilise les noms suivants :</span><span class="sxs-lookup"><span data-stu-id="4018c-203">The rest of the section will use the following names:</span></span>

* <span data-ttu-id="4018c-204">**AwesomeLibrary.Core** : projet principal qui contient toute la logique de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4018c-204">**AwesomeLibrary.Core** - A core project which contains all logic for the library</span></span>
* <span data-ttu-id="4018c-205">**AwesomeLibrary.CSharp** : projet avec des API publiques destinées à être consommées en C#</span><span class="sxs-lookup"><span data-stu-id="4018c-205">**AwesomeLibrary.CSharp** - A project with public APIs intended for consumption in C#</span></span>
* <span data-ttu-id="4018c-206">**AwesomeLibrary.CSharp** : projet avec des API publiques destinées à être consommées en F#</span><span class="sxs-lookup"><span data-stu-id="4018c-206">**AwesomeLibrary.FSharp** - A project with public APIs intended for consumption in F#</span></span>

<span data-ttu-id="4018c-207">Vous pouvez exécuter les commandes suivantes dans votre terminal pour produire la même structure que ce guide :</span><span class="sxs-lookup"><span data-stu-id="4018c-207">You can run the following commands in your terminal to produce the same structure as this guide:</span></span>

```console
mkdir AwesomeLibrary && cd AwesomeLibrary
dotnet new sln
mkdir AwesomeLibrary.Core && cd AwesomeLibrary.Core && dotnet new classlib
cd ..
mkdir AwesomeLibrary.CSharp && cd AwesomeLibrary.CSharp && dotnet new classlib
cd ..
mkdir AwesomeLibrary.FSharp && cd AwesomeLibrary.FSharp && dotnet new classlib -lang F#
cd ..
dotnet sln add AwesomeLibrary.Core/AwesomeLibrary.Core.csproj
dotnet sln add AwesomeLibrary.CSharp/AwesomeLibrary.CSharp.csproj
dotnet sln add AwesomeLibrary.FSharp/AwesomeLibrary.FSharp.fsproj
```

<span data-ttu-id="4018c-208">Cette opération ajoute les trois projets ci-dessus et un fichier solution qui les relie.</span><span class="sxs-lookup"><span data-stu-id="4018c-208">This will add the three projects above and a solution file which links them together.</span></span> <span data-ttu-id="4018c-209">Le fait de créer le fichier solution et de lier des projets vous permet de restaurer et de générer des projets à partir d’un niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="4018c-209">Creating the solution file and linking projects will allow you to restore and build projects from a top-level.</span></span>

### <a name="project-to-project-referencing"></a><span data-ttu-id="4018c-210">Références entre projets</span><span class="sxs-lookup"><span data-stu-id="4018c-210">Project-to-project referencing</span></span>

<span data-ttu-id="4018c-211">La meilleure façon de référencer un projet consiste à utiliser l’interface CLI .NET Core pour ajouter une référence de projet.</span><span class="sxs-lookup"><span data-stu-id="4018c-211">The best way to reference a project is to use the .NET Core CLI to add a project reference.</span></span> <span data-ttu-id="4018c-212">À partir des répertoires de projet **AwesomeLibrary.CSharp** et de **AwesomeLibrary.FSharp**, vous pouvez exécuter la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4018c-212">From the **AwesomeLibrary.CSharp** and **AwesomeLibrary.FSharp** project directories, you can run the following command:</span></span>

```console
$ dotnet add reference ../AwesomeLibrary.Core/AwesomeLibrary.Core.csproj
```

<span data-ttu-id="4018c-213">Les fichiers projet pour **AwesomeLibrary.CSharp** et **AwesomeLibrary.FSharp** référencent désormais **AwesomeLibrary.Core** comme cible de `ProjectReference`.</span><span class="sxs-lookup"><span data-stu-id="4018c-213">The project files for both **AwesomeLibrary.CSharp** and **AwesomeLibrary.FSharp** will now reference **AwesomeLibrary.Core** as a `ProjectReference` target.</span></span>  <span data-ttu-id="4018c-214">Pour le vérifier, confirmez la présence des éléments suivants dans les fichiers projet :</span><span class="sxs-lookup"><span data-stu-id="4018c-214">You can verify this by inspecting the project files and seeing the following in them:</span></span>

```xml
<ItemGroup>
  <ProjectReference Include="..\AwesomeLibrary.Core\AwesomeLibrary.Core.csproj" />
</ItemGroup>
```

<span data-ttu-id="4018c-215">Vous pouvez ajouter manuellement cette section à chaque fichier projet si vous préférez ne pas utiliser l’interface CLI .NET Core.</span><span class="sxs-lookup"><span data-stu-id="4018c-215">You can add this section to each project file manually if you prefer not to use the .NET Core CLI.</span></span>

### <a name="structuring-a-solution"></a><span data-ttu-id="4018c-216">Structurer une solution</span><span class="sxs-lookup"><span data-stu-id="4018c-216">Structuring a solution</span></span>

<span data-ttu-id="4018c-217">Un autre aspect important des solutions à projets multiples est la mise en place d’une bonne structure de projet globale.</span><span class="sxs-lookup"><span data-stu-id="4018c-217">Another important aspect of multi-project solutions is establishing a good overall project structure.</span></span> <span data-ttu-id="4018c-218">Vous pouvez organiser le code comme vous le souhaitez, et tant que vous liez chaque projet à votre fichier solution avec `dotnet sln add`, vous pouvez exécuter `dotnet restore` et `dotnet build` au niveau de la solution.</span><span class="sxs-lookup"><span data-stu-id="4018c-218">You can organize code however you like, and as long as you link each project to your solution file with `dotnet sln add`, you will be able to run `dotnet restore` and `dotnet build` at the solution level.</span></span>
