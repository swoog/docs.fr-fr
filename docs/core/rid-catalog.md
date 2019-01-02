---
title: Catalogue d’identificateurs de runtime (RID) .NET Core
description: Découvrez plus en détails l’identificateur de runtime (RID) et la façon dont les identificateurs RID sont utilisés dans .NET Core.
ms.date: 07/19/2018
ms.openlocfilehash: b801b7866b563ae06499d8ccd2d07cf5fd52b928
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53170196"
---
# <a name="net-core-rid-catalog"></a><span data-ttu-id="73b6c-103">Catalogue RID .NET Core</span><span class="sxs-lookup"><span data-stu-id="73b6c-103">.NET Core RID Catalog</span></span>

<span data-ttu-id="73b6c-104">RID est l’abréviation de *Runtime IDentifier* (identificateur de runtime).</span><span class="sxs-lookup"><span data-stu-id="73b6c-104">RID is short for *Runtime IDentifier*.</span></span> <span data-ttu-id="73b6c-105">Les valeurs RID sont utilisées pour identifier les plateformes cibles où l’application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="73b6c-105">RID values are used to identify target platforms where the application runs.</span></span>
<span data-ttu-id="73b6c-106">Elles sont utilisées par les packages .NET pour représenter des ressources spécifiques à une plateforme dans les packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="73b6c-106">They're used by .NET packages to represent platform-specific assets in NuGet packages.</span></span> <span data-ttu-id="73b6c-107">Les valeurs suivantes sont des exemples d’identificateurs RID : `linux-x64`, `ubuntu.14.04-x64`, `win7-x64` ou `osx.10.12-x64`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-107">The following values are examples of RIDs: `linux-x64`, `ubuntu.14.04-x64`, `win7-x64`, or `osx.10.12-x64`.</span></span>
<span data-ttu-id="73b6c-108">Pour les packages ayant des dépendances natives, les RID désignent les plateformes sur lesquelles ils peuvent être restaurés.</span><span class="sxs-lookup"><span data-stu-id="73b6c-108">For the packages with native dependencies, the RID designates on which platforms the package can be restored.</span></span>

<span data-ttu-id="73b6c-109">Un seul RID peut être défini dans l’élément `<RuntimeIdentifier>` de votre fichier projet.</span><span class="sxs-lookup"><span data-stu-id="73b6c-109">A single RID can be set in the `<RuntimeIdentifier>` element of your project file.</span></span> <span data-ttu-id="73b6c-110">Les RID multiples peuvent être définis sous forme de liste de valeurs séparées par des points-virgules dans l’élément `<RuntimeIdentifiers>` du fichier projet.</span><span class="sxs-lookup"><span data-stu-id="73b6c-110">Multiple RIDs can be defined as a semicolon-delimited list in the project file's `<RuntimeIdentifiers>` element.</span></span> <span data-ttu-id="73b6c-111">Ils sont également utilisés par le biais de l’option `--runtime` avec les [commandes de l’interface CLI .NET Core](./tools/index.md) suivantes :</span><span class="sxs-lookup"><span data-stu-id="73b6c-111">They're also used via the `--runtime` option with the following [.NET Core CLI commands](./tools/index.md):</span></span>

- [<span data-ttu-id="73b6c-112">dotnet build</span><span class="sxs-lookup"><span data-stu-id="73b6c-112">dotnet build</span></span>](./tools/dotnet-build.md)
- [<span data-ttu-id="73b6c-113">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="73b6c-113">dotnet clean</span></span>](./tools/dotnet-clean.md)
- [<span data-ttu-id="73b6c-114">dotnet pack</span><span class="sxs-lookup"><span data-stu-id="73b6c-114">dotnet pack</span></span>](./tools/dotnet-pack.md)
- [<span data-ttu-id="73b6c-115">dotnet publish</span><span class="sxs-lookup"><span data-stu-id="73b6c-115">dotnet publish</span></span>](./tools/dotnet-publish.md)
- [<span data-ttu-id="73b6c-116">dotnet restore</span><span class="sxs-lookup"><span data-stu-id="73b6c-116">dotnet restore</span></span>](./tools/dotnet-restore.md)
- [<span data-ttu-id="73b6c-117">dotnet run</span><span class="sxs-lookup"><span data-stu-id="73b6c-117">dotnet run</span></span>](./tools/dotnet-run.md)
- [<span data-ttu-id="73b6c-118">dotnet store</span><span class="sxs-lookup"><span data-stu-id="73b6c-118">dotnet store</span></span>](./tools/dotnet-store.md)

<span data-ttu-id="73b6c-119">Les RID qui représentent des systèmes d’exploitation concrets suivent généralement ce modèle : `[os].[version]-[architecture]-[additional qualifiers]` où :</span><span class="sxs-lookup"><span data-stu-id="73b6c-119">RIDs that represent concrete operating systems usually follow this pattern: `[os].[version]-[architecture]-[additional qualifiers]` where:</span></span>

- <span data-ttu-id="73b6c-120">`[os]` représente le moniker du système d’exploitation/de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="73b6c-120">`[os]` is the operating/platform system moniker.</span></span> <span data-ttu-id="73b6c-121">Par exemple, `ubuntu`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-121">For example, `ubuntu`.</span></span>

- <span data-ttu-id="73b6c-122">`[version]` représente la version du système d’exploitation sous la forme d’un numéro de version (`.`) séparé par un point.</span><span class="sxs-lookup"><span data-stu-id="73b6c-122">`[version]` is the operating system version in the form of a dot-separated (`.`) version number.</span></span> <span data-ttu-id="73b6c-123">Par exemple, `15.10`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-123">For example, `15.10`.</span></span>

  - <span data-ttu-id="73b6c-124">La version **ne doit pas** correspondre à des versions marketing, car celles-ci représentent souvent plusieurs versions distinctes du système d’exploitation avec une surface d’exposition variable des API de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="73b6c-124">The version **shouldn't** be marketing versions, as they often represent multiple discrete versions of the operating system with varying platform API surface area.</span></span>

- <span data-ttu-id="73b6c-125">`[architecture]` représente l’architecture de processeur.</span><span class="sxs-lookup"><span data-stu-id="73b6c-125">`[architecture]` is the processor architecture.</span></span> <span data-ttu-id="73b6c-126">Par exemple : `x86`, `x64`, `arm` ou `arm64`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-126">For example: `x86`, `x64`, `arm`, or `arm64`.</span></span>

- <span data-ttu-id="73b6c-127">`[additional qualifiers]` permet de distinguer davantage les plateformes.</span><span class="sxs-lookup"><span data-stu-id="73b6c-127">`[additional qualifiers]` further differentiate different platforms.</span></span> <span data-ttu-id="73b6c-128">Par exemple : `aot` ou `corert`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-128">For example: `aot` or `corert`.</span></span>

## <a name="rid-graph"></a><span data-ttu-id="73b6c-129">Graphe RID</span><span class="sxs-lookup"><span data-stu-id="73b6c-129">RID graph</span></span>

<span data-ttu-id="73b6c-130">Le graphe RID ou le graphe de secours du runtime consiste en une liste d’identificateurs RID compatibles entre eux.</span><span class="sxs-lookup"><span data-stu-id="73b6c-130">The RID graph or runtime fallback graph is a list of RIDs that are compatible with each other.</span></span> <span data-ttu-id="73b6c-131">Les RID sont définis dans le package [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/).</span><span class="sxs-lookup"><span data-stu-id="73b6c-131">The RIDs are defined in the [Microsoft.NETCore.Platforms](https://www.nuget.org/packages/Microsoft.NETCore.Platforms/) package.</span></span> <span data-ttu-id="73b6c-132">Vous pouvez consulter la liste des RID pris en charge et le graphe RID dans le fichier [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json), situé dans le référentiel CoreFX.</span><span class="sxs-lookup"><span data-stu-id="73b6c-132">You can see the list of supported RIDs and the RID graph in the [*runtime.json*](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) file, which is located at the CoreFX repo.</span></span> <span data-ttu-id="73b6c-133">Dans ce fichier, vous pouvez voir que tous les RID, sauf celui de base, contiennent une instruction `"#import"`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-133">In this file, you can see that all RIDs, except for the base one, contain an `"#import"` statement.</span></span> <span data-ttu-id="73b6c-134">Ces instructions indiquent des RID compatibles.</span><span class="sxs-lookup"><span data-stu-id="73b6c-134">These statements indicate compatible RIDs.</span></span>

<span data-ttu-id="73b6c-135">Lorsque NuGet restaure des packages, il tente de trouver une correspondance exacte pour le runtime spécifié.</span><span class="sxs-lookup"><span data-stu-id="73b6c-135">When NuGet restores packages, it tries to find an exact match for the specified runtime.</span></span>
<span data-ttu-id="73b6c-136">Si aucune correspondance exacte n’est trouvée, NuGet remonte le graphe jusqu'à ce qu’il trouve le système compatible le plus proche selon le graphe RID.</span><span class="sxs-lookup"><span data-stu-id="73b6c-136">If an exact match is not found, NuGet walks back the graph until it finds the closest compatible system according to the RID graph.</span></span>

<span data-ttu-id="73b6c-137">L’exemple suivant est l’entrée réelle pour le RID `osx.10.12-x64` :</span><span class="sxs-lookup"><span data-stu-id="73b6c-137">The following example is the actual entry for the `osx.10.12-x64` RID:</span></span>

```json
"osx.10.12-x64": {
    "#import": [ "osx.10.12", "osx.10.11-x64" ]
}
```

<span data-ttu-id="73b6c-138">Le RID ci-dessus indique que `osx.10.12-x64` importe `osx.10.11-x64`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-138">The above RID specifies that `osx.10.12-x64` imports `osx.10.11-x64`.</span></span> <span data-ttu-id="73b6c-139">Donc, lorsque NuGet restaure des packages, il tente de trouver une correspondance exacte pour `osx.10.12-x64` dans le package.</span><span class="sxs-lookup"><span data-stu-id="73b6c-139">So, when NuGet restores packages, it tries to find an exact match for  `osx.10.12-x64` in the package.</span></span> <span data-ttu-id="73b6c-140">Si NuGet ne trouve pas le runtime spécifique, il peut restaurer des packages qui spécifient des runtimes `osx.10.11-x64`, par exemple.</span><span class="sxs-lookup"><span data-stu-id="73b6c-140">If NuGet cannot find the specific runtime, it can restore packages that specify `osx.10.11-x64` runtimes, for example.</span></span>

<span data-ttu-id="73b6c-141">L’exemple suivant illustre un graphe RID légèrement plus grand également défini dans le fichier *runtime.json* :</span><span class="sxs-lookup"><span data-stu-id="73b6c-141">The following example shows a slightly bigger RID graph also defined in the *runtime.json*  file:</span></span>

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

<span data-ttu-id="73b6c-142">Tous les RID sont finalement remappés au RID `any` racine.</span><span class="sxs-lookup"><span data-stu-id="73b6c-142">All RIDs eventually map back to the root `any` RID.</span></span>

<span data-ttu-id="73b6c-143">Lorsque vous utilisez les RID, il existe quelques remarques que vous devez garder à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="73b6c-143">There are some considerations about RIDs that you have to keep in mind when working with them:</span></span>

- <span data-ttu-id="73b6c-144">Les RID sont des **chaînes opaques** qui doivent être considérées comme des boîtes noires.</span><span class="sxs-lookup"><span data-stu-id="73b6c-144">RIDs are **opaque strings** and should be treated as black boxes.</span></span>
- <span data-ttu-id="73b6c-145">Ne générez pas les RID par programme.</span><span class="sxs-lookup"><span data-stu-id="73b6c-145">Don't build RIDs programmatically.</span></span>
- <span data-ttu-id="73b6c-146">Utilisez des RID déjà définis pour la plateforme.</span><span class="sxs-lookup"><span data-stu-id="73b6c-146">Use RIDs that are already defined for the platform.</span></span>
- <span data-ttu-id="73b6c-147">Les RID se devant d’être spécifiques, ne déduisez rien de leur valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="73b6c-147">The RIDs need to be specific, so don't assume anything from the actual RID value.</span></span>

## <a name="using-rids"></a><span data-ttu-id="73b6c-148">Utilisation de RID</span><span class="sxs-lookup"><span data-stu-id="73b6c-148">Using RIDs</span></span>

<span data-ttu-id="73b6c-149">Pour utiliser des RID, vous devez savoir lesquels existent.</span><span class="sxs-lookup"><span data-stu-id="73b6c-149">To be able to use RIDs, you have to know which RIDs exist.</span></span> <span data-ttu-id="73b6c-150">De nouvelles valeurs sont régulièrement ajoutées à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="73b6c-150">New values are added regularly to the platform.</span></span>
<span data-ttu-id="73b6c-151">Pour en connaître la version complète la plus récente, consultez le fichier [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) dans le référentiel CoreFX.</span><span class="sxs-lookup"><span data-stu-id="73b6c-151">For the latest and complete version, see the [runtime.json](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/runtime.json) file on CoreFX repo.</span></span>

<span data-ttu-id="73b6c-152">Le kit SDK .NET Core 2.0 introduit le concept d’identificateurs RID portables.</span><span class="sxs-lookup"><span data-stu-id="73b6c-152">.NET Core 2.0 SDK introduces the concept of portable RIDs.</span></span> <span data-ttu-id="73b6c-153">Il s’agit de nouvelles valeurs ajoutées au graphe RID qui ne sont liées à aucune version ou distribution du système d’exploitation spécifique.</span><span class="sxs-lookup"><span data-stu-id="73b6c-153">They are new values added to the RID graph that aren't tied to a specific version or OS distribution.</span></span> <span data-ttu-id="73b6c-154">Elles sont particulièrement utiles lors du traitement de plusieurs distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="73b6c-154">They're particularly useful when dealing with multiple Linux distros.</span></span>

<span data-ttu-id="73b6c-155">La liste suivante présente les RID les plus courants utilisés pour chaque système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="73b6c-155">The following list shows the most common RIDs used for each OS.</span></span> <span data-ttu-id="73b6c-156">Elle ne traite pas les valeurs `arm` ou `corert`.</span><span class="sxs-lookup"><span data-stu-id="73b6c-156">It doesn't cover `arm` or `corert` values.</span></span>

## <a name="windows-rids"></a><span data-ttu-id="73b6c-157">RID Windows</span><span class="sxs-lookup"><span data-stu-id="73b6c-157">Windows RIDs</span></span>

- <span data-ttu-id="73b6c-158">Portable</span><span class="sxs-lookup"><span data-stu-id="73b6c-158">Portable</span></span>
  - `win-x86`
  - `win-x64`
- <span data-ttu-id="73b6c-159">Windows 7 / Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="73b6c-159">Windows 7 / Windows Server 2008 R2</span></span>
  - `win7-x64`
  - `win7-x86`
- <span data-ttu-id="73b6c-160">Windows 8 / Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73b6c-160">Windows 8 / Windows Server 2012</span></span>
  - `win8-x64`
  - `win8-x86`
  - `win8-arm`
- <span data-ttu-id="73b6c-161">Windows 8.1 / Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="73b6c-161">Windows 8.1 / Windows Server 2012 R2</span></span>
  - `win81-x64`
  - `win81-x86`
  - `win81-arm`
- <span data-ttu-id="73b6c-162">Windows 10 / Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="73b6c-162">Windows 10 / Windows Server 2016</span></span>
  - `win10-x64`
  - `win10-x86`
  - `win10-arm`
  - `win10-arm64`

<span data-ttu-id="73b6c-163">Pour plus d’informations, consultez [Configuration requise pour .NET Core sur Windows](windows-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="73b6c-163">See [Prerequisites for .NET Core on Windows](windows-prerequisites.md) for more information.</span></span>

## <a name="linux-rids"></a><span data-ttu-id="73b6c-164">RID Linux</span><span class="sxs-lookup"><span data-stu-id="73b6c-164">Linux RIDs</span></span>

- <span data-ttu-id="73b6c-165">Portable</span><span class="sxs-lookup"><span data-stu-id="73b6c-165">Portable</span></span>
  - `linux-x64`
- <span data-ttu-id="73b6c-166">CentOS</span><span class="sxs-lookup"><span data-stu-id="73b6c-166">CentOS</span></span>
  - `centos-x64`
  - `centos.7-x64`
- <span data-ttu-id="73b6c-167">Debian</span><span class="sxs-lookup"><span data-stu-id="73b6c-167">Debian</span></span>
  - `debian-x64`
  - `debian.8-x64`
  - <span data-ttu-id="73b6c-168">`debian.9-x64` (.NET Core 1.1 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-168">`debian.9-x64` (.NET Core 1.1 or later versions)</span></span>
- <span data-ttu-id="73b6c-169">Fedora</span><span class="sxs-lookup"><span data-stu-id="73b6c-169">Fedora</span></span>
  - `fedora-x64`
  - `fedora.27-x64`
  - <span data-ttu-id="73b6c-170">`fedora.28-x64` (.NET Core 1.1 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-170">`fedora.28-x64` (.NET Core 1.1 or later versions)</span></span>
- <span data-ttu-id="73b6c-171">Gentoo (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-171">Gentoo (.NET Core 2.0 or later versions)</span></span>
  - `gentoo-x64`
- <span data-ttu-id="73b6c-172">openSUSE</span><span class="sxs-lookup"><span data-stu-id="73b6c-172">openSUSE</span></span>
  - `opensuse-x64`
  - `opensuse.42.3-x64`
- <span data-ttu-id="73b6c-173">Oracle Linux</span><span class="sxs-lookup"><span data-stu-id="73b6c-173">Oracle Linux</span></span>
  - `ol-x64`
  - `ol.7-x64`
  - `ol.7.0-x64`
  - `ol.7.1-x64`
  - `ol.7.2-x64`
  - `ol.7.3-x64`
  - `ol.7.4-x64`
- <span data-ttu-id="73b6c-174">Red Hat Enterprise Linux</span><span class="sxs-lookup"><span data-stu-id="73b6c-174">Red Hat Enterprise Linux</span></span>
  - `rhel-x64`
  - <span data-ttu-id="73b6c-175">`rhel.6-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-175">`rhel.6-x64` (.NET Core 2.0 or later versions)</span></span>
  - `rhel.7-x64`
  - `rhel.7.1-x64`
  - `rhel.7.2-x64`
  - <span data-ttu-id="73b6c-176">`rhel.7.3-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-176">`rhel.7.3-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="73b6c-177">`rhel.7.4-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-177">`rhel.7.4-x64` (.NET Core 2.0 or later versions)</span></span>
- <span data-ttu-id="73b6c-178">Tizen (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-178">Tizen (.NET Core 2.0 or later versions)</span></span>
  - `tizen`
  - `tizen.4.0.0`
  - `tizen.5.0.0`
- <span data-ttu-id="73b6c-179">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="73b6c-179">Ubuntu</span></span>
  - `ubuntu-x64`
  - `ubuntu.14.04-x64`
  - `ubuntu.16.04-x64`
  - `ubuntu.17.10-x64`
  - `ubuntu.18.04-x64`
- <span data-ttu-id="73b6c-180">Dérivés d’Ubuntu</span><span class="sxs-lookup"><span data-stu-id="73b6c-180">Ubuntu derivatives</span></span>
  - `linuxmint.17-x64`
  - `linuxmint.17.1-x64`
  - `linuxmint.17.2-x64`
  - `linuxmint.17.3-x64`
  - <span data-ttu-id="73b6c-181">`linuxmint.18-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-181">`linuxmint.18-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="73b6c-182">`linuxmint.18.1-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-182">`linuxmint.18.1-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="73b6c-183">`linuxmint.18.2-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-183">`linuxmint.18.2-x64` (.NET Core 2.0 or later versions)</span></span>
  - <span data-ttu-id="73b6c-184">`linuxmint.18.3-x64` (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-184">`linuxmint.18.3-x64` (.NET Core 2.0 or later versions)</span></span>
- <span data-ttu-id="73b6c-185">SUSE Enterprise Linux (SLES) (.NET Core 2.0 ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="73b6c-185">SUSE Enterprise Linux (SLES) (.NET Core 2.0 or later versions)</span></span>
  - `sles-x64`
  - `sles.12-x64`
  - `sles.12.1-x64`
  - `sles.12.2-x64`
  - `sles.12.3-x64`
- <span data-ttu-id="73b6c-186">Alpine Linux (.NET Core 2.1 ou version ultérieure)</span><span class="sxs-lookup"><span data-stu-id="73b6c-186">Alpine Linux (.NET Core 2.1 or later versions)</span></span>
  - `alpine-x64`
  - `alpine.3.7-x64`

<span data-ttu-id="73b6c-187">Pour plus d’informations, consultez [Configuration requise pour .NET Core sur Linux](linux-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="73b6c-187">See [Prerequisites for .NET Core on Linux](linux-prerequisites.md) for more information.</span></span>

## <a name="macos-rids"></a><span data-ttu-id="73b6c-188">RID macOS</span><span class="sxs-lookup"><span data-stu-id="73b6c-188">macOS RIDs</span></span>

<span data-ttu-id="73b6c-189">Les RID macOS utilisent l’ancien logo « OSX ».</span><span class="sxs-lookup"><span data-stu-id="73b6c-189">macOS RIDs use the older "OSX" branding.</span></span>

- <span data-ttu-id="73b6c-190">`osx-x64` (.NET Core 2.0 ou versions ultérieures, la version minimale est `osx.10.12-x64`)</span><span class="sxs-lookup"><span data-stu-id="73b6c-190">`osx-x64` (.NET Core 2.0 or later versions, minimum version is `osx.10.12-x64`)</span></span>
- `osx.10.10-x64`
- `osx.10.11-x64`
- <span data-ttu-id="73b6c-191">`osx.10.12-x64` (.NET Core 1.1 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-191">`osx.10.12-x64` (.NET Core 1.1 or later versions)</span></span>
- `osx.10.13-x64`

<span data-ttu-id="73b6c-192">Pour plus d’informations, consultez [Configuration requise pour .NET Core sur macOS](macos-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="73b6c-192">See [Prerequisites for .NET Core on macOS](macos-prerequisites.md) for more information.</span></span>

## <a name="android-rids-net-core-20-or-later-versions"></a><span data-ttu-id="73b6c-193">RID Android (.NET Core 2.0 ou versions ultérieures)</span><span class="sxs-lookup"><span data-stu-id="73b6c-193">Android RIDs (.NET Core 2.0 or later versions)</span></span>

- `android`
- `android.21`

## <a name="see-also"></a><span data-ttu-id="73b6c-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73b6c-194">See also</span></span>

* [<span data-ttu-id="73b6c-195">ID du runtime</span><span class="sxs-lookup"><span data-stu-id="73b6c-195">Runtime IDs</span></span>](https://github.com/dotnet/corefx/blob/master/pkg/Microsoft.NETCore.Platforms/readme.md)
