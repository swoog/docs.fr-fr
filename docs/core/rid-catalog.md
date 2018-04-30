---
title: Catalogue d’identificateurs de runtime (RID) .NET Core
description: Découvrez plus en détails l’identificateur de runtime (RID) et la façon dont les identificateurs RID sont utilisés dans .NET Core.
author: mairaw
ms.author: mairaw
ms.date: 09/07/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.workload:
- dotnetcore
ms.openlocfilehash: 42707d96744ff765c2ea6ae2298da3e8b27f912f
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="net-core-rid-catalog"></a><span data-ttu-id="89bb4-103">Catalogue RID .NET Core</span><span class="sxs-lookup"><span data-stu-id="89bb4-103">.NET Core RID Catalog</span></span>

<span data-ttu-id="89bb4-104">RID est l’abréviation de *Runtime IDentifier* (identificateur de runtime).</span><span class="sxs-lookup"><span data-stu-id="89bb4-104">RID is short for *Runtime IDentifier*.</span></span> <span data-ttu-id="89bb4-105">Les valeurs RID sont utilisées pour identifier les plateformes cibles où l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="89bb4-105">RID values are used to identify target platforms where the application runs.</span></span>
<span data-ttu-id="89bb4-106">Elles sont utilisées par les packages .NET pour représenter des ressources spécifiques à une plateforme dans les packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="89bb4-106">They're used by .NET packages to represent platform-specific assets in NuGet packages.</span></span> <span data-ttu-id="89bb4-107">Les valeurs suivantes sont des exemples d’identificateurs RID : `linux-x64`, `ubuntu.14.04-x64`, `win7-x64` ou `osx.10.12-x64`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-107">The following values are examples of RIDs: `linux-x64`, `ubuntu.14.04-x64`, `win7-x64`, or `osx.10.12-x64`.</span></span>
<span data-ttu-id="89bb4-108">Pour les packages ayant des dépendances natives, les RID désignent les plateformes sur lesquelles ils peuvent être restaurés.</span><span class="sxs-lookup"><span data-stu-id="89bb4-108">For the packages with native dependencies, the RID designates on which platforms the package can be restored.</span></span>

<span data-ttu-id="89bb4-109">Un seul RID peut être défini dans l’élément `<RuntimeIdentifier>` de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="89bb4-109">A single RID can be set in the `<RuntimeIdentifier>` element of your project file.</span></span> <span data-ttu-id="89bb4-110">Les RID multiples peuvent être définis sous forme de liste de valeurs séparées par des points-virgules dans l’élément `<RuntimeIdentifiers>` du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="89bb4-110">Multiple RIDs can be defined as a semicolon-delimited list in the project file's `<RuntimeIdentifiers>` element.</span></span> <span data-ttu-id="89bb4-111">Ils sont également utilisés par le biais de l’option `--runtime` avec les [commandes de l’interface CLI .NET Core](./tools/index.md) suivantes :</span><span class="sxs-lookup"><span data-stu-id="89bb4-111">They're also used via the `--runtime` option with the following [.NET Core CLI commands](./tools/index.md):</span></span>

- [<span data-ttu-id="89bb4-112">dotnet build</span><span class="sxs-lookup"><span data-stu-id="89bb4-112">dotnet build</span></span>](./tools/dotnet-build.md)
- [<span data-ttu-id="89bb4-113">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="89bb4-113">dotnet clean</span></span>](./tools/dotnet-clean.md)
- [<span data-ttu-id="89bb4-114">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="89bb4-114">dotnet pack</span></span>](./tools/dotnet-pack.md)
- [<span data-ttu-id="89bb4-115">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="89bb4-115">dotnet publish</span></span>](./tools/dotnet-publish.md)
- [<span data-ttu-id="89bb4-116">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="89bb4-116">dotnet restore</span></span>](./tools/dotnet-restore.md)
- [<span data-ttu-id="89bb4-117">dotnet run</span><span class="sxs-lookup"><span data-stu-id="89bb4-117">dotnet run</span></span>](./tools/dotnet-run.md)
- [<span data-ttu-id="89bb4-118">dotnet store</span><span class="sxs-lookup"><span data-stu-id="89bb4-118">dotnet store</span></span>](./tools/dotnet-store.md)

<span data-ttu-id="89bb4-119">Les RID qui représentent des systèmes d’exploitation concrets suivent généralement ce modèle : `[os].[version]-[architecture]-[additional qualifiers]` où :</span><span class="sxs-lookup"><span data-stu-id="89bb4-119">RIDs that represent concrete operating systems usually follow this pattern: `[os].[version]-[architecture]-[additional qualifiers]` where:</span></span>

- <span data-ttu-id="89bb4-120">`[os]` représente le moniker du système d’exploitation/de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="89bb4-120">`[os]` is the operating/platform system moniker.</span></span> <span data-ttu-id="89bb4-121">Par exemple, `ubuntu`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-121">For example, `ubuntu`.</span></span>

- <span data-ttu-id="89bb4-122">`[version]` représente la version du système d’exploitation sous la forme d’un numéro de version (`.`) séparé par un point.</span><span class="sxs-lookup"><span data-stu-id="89bb4-122">`[version]` is the operating system version in the form of a dot-separated (`.`) version number.</span></span> <span data-ttu-id="89bb4-123">Par exemple, `15.10`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-123">For example, `15.10`.</span></span>

  - <span data-ttu-id="89bb4-124">La version **ne doit pas** correspondre à des versions marketing, car celles-ci représentent souvent plusieurs versions distinctes du système d’exploitation avec une surface d’exposition variable des API de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="89bb4-124">The version **shouldn't** be marketing versions, as they often represent multiple discrete versions of the operating system with varying platform API surface area.</span></span>

- <span data-ttu-id="89bb4-125">`[architecture]` représente l’architecture de processeur.</span><span class="sxs-lookup"><span data-stu-id="89bb4-125">`[architecture]` is the processor architecture.</span></span> <span data-ttu-id="89bb4-126">Par exemple : `x86`, `x64`, `arm` ou `arm64`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-126">For example: `x86`, `x64`, `arm`, or `arm64`.</span></span>

- <span data-ttu-id="89bb4-127">`[additional qualifiers]` permet de distinguer davantage les plateformes.</span><span class="sxs-lookup"><span data-stu-id="89bb4-127">`[additional qualifiers]` further differentiate different platforms.</span></span> <span data-ttu-id="89bb4-128">Par exemple : `aot` ou `corert`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-128">For example: `aot` or `corert`.</span></span>

## <a name="rid-graph"></a><span data-ttu-id="89bb4-129">Graphe RID</span><span class="sxs-lookup"><span data-stu-id="89bb4-129">RID graph</span></span>

<span data-ttu-id="89bb4-130">Le graphe RID ou le graphe de secours du runtime consiste en une liste d’identificateurs RID compatibles entre eux.</span><span class="sxs-lookup"><span data-stu-id="89bb4-130">The RID graph or runtime fallback graph is a list of RIDs that are compatible with each other.</span></span> <span data-ttu-id="89bb4-131">Les RID sont définis dans le package [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/).</span><span class="sxs-lookup"><span data-stu-id="89bb4-131">The RIDs are defined in the [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/) package.</span></span> <span data-ttu-id="89bb4-132">Vous pouvez consulter la liste des RID pris en charge et le graphe RID dans le fichier [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json), situé dans le référentiel CoreFX.</span><span class="sxs-lookup"><span data-stu-id="89bb4-132">You can see the list of supported RIDs and the RID graph in the [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) file, which is located at the CoreFX repo.</span></span> <span data-ttu-id="89bb4-133">Dans ce fichier, vous pouvez voir que tous les RID, sauf celui de base, contiennent une instruction `"#import"`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-133">In this file, you can see that all RIDs, except for the base one, contain an `"#import"` statement.</span></span> <span data-ttu-id="89bb4-134">Ces instructions indiquent des RID compatibles.</span><span class="sxs-lookup"><span data-stu-id="89bb4-134">These statements indicate compatible RIDs.</span></span>

<span data-ttu-id="89bb4-135">Lorsque NuGet restaure des packages, il tente de trouver une correspondance exacte pour le runtime spécifié.</span><span class="sxs-lookup"><span data-stu-id="89bb4-135">When NuGet restores packages, it tries to find an exact match for the specified runtime.</span></span>
<span data-ttu-id="89bb4-136">Si aucune correspondance exacte n’est trouvée, NuGet remonte le graphe jusqu'à ce qu’il trouve le système compatible le plus proche selon le graphe RID.</span><span class="sxs-lookup"><span data-stu-id="89bb4-136">If an exact match is not found, NuGet walks back the graph until it finds the closest compatible system according to the RID graph.</span></span>

<span data-ttu-id="89bb4-137">L’exemple suivant est l’entrée réelle pour le RID `osx.10.12-x64` :</span><span class="sxs-lookup"><span data-stu-id="89bb4-137">The following example is the actual entry for the `osx.10.12-x64` RID:</span></span>

```json
"osx.10.12-x64": {
    "#import": [ "osx.10.12", "osx.10.11-x64" ]
}
```

<span data-ttu-id="89bb4-138">Le RID ci-dessus indique que `osx.10.12-x64` importe `osx.10.11-x64`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-138">The above RID specifies that `osx.10.12-x64` imports `osx.10.11-x64`.</span></span> <span data-ttu-id="89bb4-139">Donc, lorsque NuGet restaure des packages, il tente de trouver une correspondance exacte pour `osx.10.12-x64` dans le package.</span><span class="sxs-lookup"><span data-stu-id="89bb4-139">So, when NuGet restores packages, it tries to find an exact match for  `osx.10.12-x64` in the package.</span></span> <span data-ttu-id="89bb4-140">Si NuGet ne trouve pas le runtime spécifique, il peut restaurer des packages qui spécifient des runtimes `osx.10.11-x64`, par exemple.</span><span class="sxs-lookup"><span data-stu-id="89bb4-140">If NuGet cannot find the specific runtime, it can restore packages that specify `osx.10.11-x64` runtimes, for example.</span></span>

<span data-ttu-id="89bb4-141">L’exemple suivant illustre un graphe RID légèrement plus grand également défini dans le fichier *runtime.json* :</span><span class="sxs-lookup"><span data-stu-id="89bb4-141">The following example shows a slightly bigger RID graph also defined in the *runtime.json*  file:</span></span>

```
    win7-x64    win7-x86
       |   \   /    |
       |   win7     |
       |     |      |
    win-x64  |  win-x86
          \  |  /
            win
             |
            any
```

<span data-ttu-id="89bb4-142">Tous les RID sont finalement remappés au RID `any` racine.</span><span class="sxs-lookup"><span data-stu-id="89bb4-142">All RIDs eventually map back to the root `any` RID.</span></span>

<span data-ttu-id="89bb4-143">Lorsque vous utilisez les RID, il existe quelques remarques que vous devez garder à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="89bb4-143">There are some considerations about RIDs that you have to keep in mind when working with them:</span></span>

- <span data-ttu-id="89bb4-144">Les RID sont des **chaînes opaques** qui doivent être considérées comme des boîtes noires.</span><span class="sxs-lookup"><span data-stu-id="89bb4-144">RIDs are **opaque strings** and should be treated as black boxes.</span></span>
- <span data-ttu-id="89bb4-145">Ne générez pas les RID par programme.</span><span class="sxs-lookup"><span data-stu-id="89bb4-145">Don't build RIDs programmatically.</span></span>
- <span data-ttu-id="89bb4-146">Utilisez des RID déjà définis pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="89bb4-146">Use RIDs that are already defined for the platform.</span></span>
- <span data-ttu-id="89bb4-147">Les RID se devant d’être spécifiques, ne déduisez rien de leur valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="89bb4-147">The RIDs need to be specific, so don't assume anything from the actual RID value.</span></span>

## <a name="using-rids"></a><span data-ttu-id="89bb4-148">Utilisation de RID</span><span class="sxs-lookup"><span data-stu-id="89bb4-148">Using RIDs</span></span>

<span data-ttu-id="89bb4-149">Pour utiliser des RID, vous devez savoir lesquels existent.</span><span class="sxs-lookup"><span data-stu-id="89bb4-149">To be able to use RIDs, you have to know which RIDs exist.</span></span> <span data-ttu-id="89bb4-150">De nouvelles valeurs sont régulièrement ajoutées à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="89bb4-150">New values are added regularly to the platform.</span></span>
<span data-ttu-id="89bb4-151">Pour en connaître la version complète la plus récente, consultez le fichier [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) dans le référentiel CoreFX.</span><span class="sxs-lookup"><span data-stu-id="89bb4-151">For the latest and complete version, see the [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) file on CoreFX repo.</span></span>

<span data-ttu-id="89bb4-152">Le kit SDK .NET Core 2.0 introduit le concept d’identificateurs RID portables.</span><span class="sxs-lookup"><span data-stu-id="89bb4-152">.NET Core 2.0 SDK introduces the concept of portable RIDs.</span></span> <span data-ttu-id="89bb4-153">Il s’agit de nouvelles valeurs ajoutées au graphe RID qui ne sont liées à aucune version ou distribution du système d’exploitation spécifique.</span><span class="sxs-lookup"><span data-stu-id="89bb4-153">They are new values added to the RID graph that aren't tied to a specific version or OS distribution.</span></span> <span data-ttu-id="89bb4-154">Elles sont particulièrement utiles lors du traitement de plusieurs distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="89bb4-154">They're particularly useful when dealing with multiple Linux distros.</span></span>

<span data-ttu-id="89bb4-155">La liste suivante présente les RID les plus courants utilisés pour chaque système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="89bb4-155">The following list shows the most common RIDs used for each OS.</span></span> <span data-ttu-id="89bb4-156">Elle ne traite pas les valeurs `arm` ou `corert`.</span><span class="sxs-lookup"><span data-stu-id="89bb4-156">It doesn't cover `arm` or `corert` values.</span></span>

## <a name="windows-rids"></a><span data-ttu-id="89bb4-157">RID Windows</span><span class="sxs-lookup"><span data-stu-id="89bb4-157">Windows RIDs</span></span>

- <span data-ttu-id="89bb4-158">Portable</span><span class="sxs-lookup"><span data-stu-id="89bb4-158">Portable</span></span>
  - `win-x86`
  - `win-x64`
- <span data-ttu-id="89bb4-159">Windows 7 / Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89bb4-159">Windows 7 / Windows Server 2008 R2</span></span>
  - `win7-x64`
  - `win7-x86`
- <span data-ttu-id="89bb4-160">Windows 8 / Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89bb4-160">Windows 8 / Windows Server 2012</span></span>
  - `win8-x64`
  - `win8-x86`
  - `win8-arm`
- <span data-ttu-id="89bb4-161">Windows 8.1 / Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="89bb4-161">Windows 8.1 / Windows Server 2012 R2</span></span>
  - `win81-x64`
  - `win81-x86`
  - `win81-arm`
- <span data-ttu-id="89bb4-162">Windows 10 / Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="89bb4-162">Windows 10 / Windows Server 2016</span></span>
  - `win10-x64`
  - `win10-x86`
  - `win10-arm`
  - `win10-arm64`

<span data-ttu-id="89bb4-163">Pour plus d’informations, consultez [Configuration requise pour .NET Core sur Windows](windows-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="89bb4-163">See [Prerequisites for .NET Core on Windows](windows-prerequisites.md) for more information.</span></span>

## <a name="linux-rids"></a><span data-ttu-id="89bb4-164">RID Linux</span><span class="sxs-lookup"><span data-stu-id="89bb4-164">Linux RIDs</span></span>

- <span data-ttu-id="89bb4-165">Portable</span><span class="sxs-lookup"><span data-stu-id="89bb4-165">Portable</span></span>
  - `linux-x64`
- <span data-ttu-id="89bb4-166">CentOS</span><span class="sxs-lookup"><span data-stu-id="89bb4-166">CentOS</span></span>
  - `centos-x64`
  - `centos.7-x64`
- <span data-ttu-id="89bb4-167">Debian</span><span class="sxs-lookup"><span data-stu-id="89bb4-167">Debian</span></span>
  - `debian-x64`
  - `debian.8-x64`
- <span data-ttu-id="89bb4-168">Fedora</span><span class="sxs-lookup"><span data-stu-id="89bb4-168">Fedora</span></span>
  - `fedora-x64`
  - `fedora.24-x64`
  - <span data-ttu-id="89bb4-169">`fedora.25-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-169">`fedora.25-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="89bb4-170">`fedora.26-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-170">`fedora.26-x64` (.NET Core 2.0 or later versions)</span></span>
- <span data-ttu-id="89bb4-171">Gentoo (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-171">Gentoo (.NET Core 2.0 or later versions)</span></span>
  - `gentoo-x64`
- <span data-ttu-id="89bb4-172">openSUSE</span><span class="sxs-lookup"><span data-stu-id="89bb4-172">openSUSE</span></span>
  - `opensuse-x64`
  - `opensuse.42.1-x64`
- <span data-ttu-id="89bb4-173">Oracle Linux</span><span class="sxs-lookup"><span data-stu-id="89bb4-173">Oracle Linux</span></span>
  - `ol-x64`
  - `ol.7-x64`
  - `ol.7.0-x64`
  - `ol.7.1-x64`
  - `ol.7.2-x64`
- <span data-ttu-id="89bb4-174">Red Hat Enterprise Linux</span><span class="sxs-lookup"><span data-stu-id="89bb4-174">Red Hat Enterprise Linux</span></span>
  - `rhel-x64`
  - <span data-ttu-id="89bb4-175">`rhel.6-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-175">`rhel.6-x64` (.NET Core 2.0 or later versions)</span></span>
  - `rhel.7-x64`
  - `rhel.7.1-x64`
  - `rhel.7.2-x64`
  - <span data-ttu-id="89bb4-176">`rhel.7.3-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-176">`rhel.7.3-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="89bb4-177">`rhel.7.4-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-177">`rhel.7.4-x64` (.NET Core 2.0 or later versions)</span></span>
- <span data-ttu-id="89bb4-178">Tizen (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-178">Tizen (.NET Core 2.0 or later versions)</span></span>
  - `tizen`
- <span data-ttu-id="89bb4-179">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="89bb4-179">Ubuntu</span></span>
  - `ubuntu-x64`
  - `ubuntu.14.04-x64`
  - `ubuntu.14.10-x64`
  - `ubuntu.15.04-x64`
  - `ubuntu.15.10-x64`
  - `ubuntu.16.04-x64`
  - `ubuntu.16.10-x64`
- <span data-ttu-id="89bb4-180">Dérivés d’Ubuntu</span><span class="sxs-lookup"><span data-stu-id="89bb4-180">Ubuntu derivatives</span></span>
  - `linuxmint.17-x64`
  - `linuxmint.17.1-x64`
  - `linuxmint.17.2-x64`
  - `linuxmint.17.3-x64`
  - `linuxmint.18-x64`
  - <span data-ttu-id="89bb4-181">`linuxmint.18.1-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-181">`linuxmint.18.1-x64` (.NET Core 2.0 or later versions)</span></span>

<span data-ttu-id="89bb4-182">Pour plus d’informations, consultez [Configuration requise pour .NET Core sur Linux](linux-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="89bb4-182">See [Prerequisites for .NET Core on Linux](linux-prerequisites.md) for more information.</span></span>

## <a name="macos-rids"></a><span data-ttu-id="89bb4-183">RID macOS</span><span class="sxs-lookup"><span data-stu-id="89bb4-183">macOS RIDs</span></span>

<span data-ttu-id="89bb4-184">Les RID macOS utilisent l’ancien logo « OSX ».</span><span class="sxs-lookup"><span data-stu-id="89bb4-184">macOS RIDs use the older "OSX" branding.</span></span>

- <span data-ttu-id="89bb4-185">`osx-x64` (.NET Core 2.0 ou versions ultérieures, la version minimale est `osx.10.12-x64`)</span><span class="sxs-lookup"><span data-stu-id="89bb4-185">`osx-x64` (.NET Core 2.0 or later versions, minimum version is `osx.10.12-x64`)</span></span>
- `osx.10.10-x64`
- `osx.10.11-x64`
- <span data-ttu-id="89bb4-186">`osx.10.12-x64` (.NET Core 1.1 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-186">`osx.10.12-x64` (.NET Core 1.1 or later versions)</span></span>
- `osx.10.13-x64`

<span data-ttu-id="89bb4-187">Pour plus d’informations, consultez [Configuration requise pour .NET Core sur macOS](macos-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="89bb4-187">See [Prerequisites for .NET Core on macOS](macos-prerequisites.md) for more information.</span></span>

## <a name="android-rids-net-core-20-or-later-versions"></a><span data-ttu-id="89bb4-188">RID Android (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="89bb4-188">Android RIDs (.NET Core 2.0 or later versions)</span></span>

- `android`
- `android.21`

## <a name="see-also"></a><span data-ttu-id="89bb4-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89bb4-189">See also</span></span>

[<span data-ttu-id="89bb4-190">ID du runtime</span><span class="sxs-lookup"><span data-stu-id="89bb4-190">Runtime IDs</span></span>](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/readme.md)
