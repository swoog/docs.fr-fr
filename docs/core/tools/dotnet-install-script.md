---
title: Scripts dotnet-install
description: Découvrez les scripts dotnet-install pour installer les outils CLI .NET Core et le runtime partagé.
author: blackdwarf
ms.author: mairaw
ms.date: 09/11/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.workload:
- dotnetcore
ms.openlocfilehash: 96336df087ea2ad01584010f0715ad31e079b663
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="dotnet-install-scripts-reference"></a><span data-ttu-id="b3c62-103">Documentation sur les scripts dotnet-install</span><span class="sxs-lookup"><span data-stu-id="b3c62-103">dotnet-install scripts reference</span></span>

## <a name="name"></a><span data-ttu-id="b3c62-104">Name</span><span class="sxs-lookup"><span data-stu-id="b3c62-104">Name</span></span>

<span data-ttu-id="b3c62-105">`dotnet-install.ps1` | `dotnet-install.sh` : script utilisé pour installer les outils .NET Core CLI et le runtime partagé.</span><span class="sxs-lookup"><span data-stu-id="b3c62-105">`dotnet-install.ps1` | `dotnet-install.sh` - Script used to install the .NET Core CLI tools and the shared runtime.</span></span>

## <a name="synopsis"></a><span data-ttu-id="b3c62-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b3c62-106">Synopsis</span></span>

<span data-ttu-id="b3c62-107">Windows :</span><span class="sxs-lookup"><span data-stu-id="b3c62-107">Windows:</span></span>

`dotnet-install.ps1 [-Channel] [-Version] [-InstallDir] [-Architecture] [-SharedRuntime] [-DryRun] [-NoPath] [-AzureFeed] [-ProxyAddress] [--Verbose] [--Help]`

<span data-ttu-id="b3c62-108">Mac OS/Linux :</span><span class="sxs-lookup"><span data-stu-id="b3c62-108">macOS/Linux:</span></span>

`dotnet-install.sh [--channel] [--version] [--install-dir] [--architecture] [--shared-runtime] [--dry-run] [--no-path] [--azure-feed] [--verbose] [--help]`

## <a name="description"></a><span data-ttu-id="b3c62-109">Description</span><span class="sxs-lookup"><span data-stu-id="b3c62-109">Description</span></span>

<span data-ttu-id="b3c62-110">Les scripts `dotnet-install` sont utilisés pour effectuer une installation non administrateur du SDK .NET Core, qui inclut les outils .NET Core CLI et le runtime partagé.</span><span class="sxs-lookup"><span data-stu-id="b3c62-110">The `dotnet-install` scripts are used to perform a non-admin installation of the .NET Core SDK, which includes the .NET Core CLI tools and the shared runtime.</span></span>

<span data-ttu-id="b3c62-111">Nous vous recommandons d’utiliser la version stable hébergée sur le [site web principal de .NET Core](https://dot.net).</span><span class="sxs-lookup"><span data-stu-id="b3c62-111">We recommend that you use the stable version that is hosted on [.NET Core main website](https://dot.net).</span></span> <span data-ttu-id="b3c62-112">Les chemins d’accès directs aux scripts sont :</span><span class="sxs-lookup"><span data-stu-id="b3c62-112">The direct paths to the scripts are:</span></span>

* <span data-ttu-id="b3c62-113">https://dot.net/v1/dotnet-install.sh (bash, UNIX)</span><span class="sxs-lookup"><span data-stu-id="b3c62-113">https://dot.net/v1/dotnet-install.sh (bash, UNIX)</span></span>
* <span data-ttu-id="b3c62-114">https://dot.net/v1/dotnet-install.ps1 (Powershell, Windows)</span><span class="sxs-lookup"><span data-stu-id="b3c62-114">https://dot.net/v1/dotnet-install.ps1 (Powershell, Windows)</span></span>

<span data-ttu-id="b3c62-115">La principale utilité de ces scripts réside dans les scénarios d’automatisation et les installations non administrateur.</span><span class="sxs-lookup"><span data-stu-id="b3c62-115">The main usefulness of these scripts is in automation scenarios and non-admin installations.</span></span> <span data-ttu-id="b3c62-116">Il existe deux scripts : un script PowerShell qui fonctionne sous Windows.</span><span class="sxs-lookup"><span data-stu-id="b3c62-116">There are two scripts: One is a PowerShell script that works on Windows.</span></span> <span data-ttu-id="b3c62-117">L’autre script est un script bash qui fonctionne sur Linux/macOS.</span><span class="sxs-lookup"><span data-stu-id="b3c62-117">The other script is a bash script that works on Linux/macOS.</span></span> <span data-ttu-id="b3c62-118">Les deux scripts ont le même comportement.</span><span class="sxs-lookup"><span data-stu-id="b3c62-118">Both scripts have the same behavior.</span></span> <span data-ttu-id="b3c62-119">Comme le script bash lit également les commutateurs PowerShell, vous pouvez utiliser ces derniers avec le script sur les systèmes Linux/macOS.</span><span class="sxs-lookup"><span data-stu-id="b3c62-119">The bash script also reads PowerShell switches, so you can use PowerShell switches with the script on Linux/macOS systems.</span></span> 

<span data-ttu-id="b3c62-120">Les scripts d’installation téléchargent le fichier ZIP/tarball à partir des cibles de builds CLI, puis poursuivent l’installation dans l’emplacement par défaut ou dans un emplacement spécifié par `-InstallDir|--install-dir`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-120">The installation scripts download the ZIP/tarball file from the CLI build drops and proceed to install it in either the default location or in a location specified by `-InstallDir|--install-dir`.</span></span> <span data-ttu-id="b3c62-121">Par défaut, les scripts d’installation téléchargent et installent le Kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="b3c62-121">By default, the installation scripts download the SDK and install it.</span></span> <span data-ttu-id="b3c62-122">Si vous souhaitez obtenir uniquement le runtime partagé, spécifiez l’argument `--shared-runtime`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-122">If you wish to only obtain the shared runtime, specify the `--shared-runtime` argument.</span></span> 

<span data-ttu-id="b3c62-123">Par défaut, le script ajoute l’emplacement d’installation $PATH pour la session active.</span><span class="sxs-lookup"><span data-stu-id="b3c62-123">By default, the script adds the install location to the $PATH for the current session.</span></span> <span data-ttu-id="b3c62-124">Remplacez ce comportement par défaut en spécifiant l’argument `--no-path`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-124">Override this default behavior by specifying the `--no-path` argument.</span></span> 

<span data-ttu-id="b3c62-125">Avant d’exécuter le script, installez les [dépendances](https://github.com/dotnet/core/blob/master/Documentation/prereqs.md) nécessaires.</span><span class="sxs-lookup"><span data-stu-id="b3c62-125">Before running the script, install the required [dependencies](https://github.com/dotnet/core/blob/master/Documentation/prereqs.md).</span></span>

<span data-ttu-id="b3c62-126">Vous pouvez installer une version spécifique à l’aide de l’argument `--version`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-126">You can install a specific version using the `--version` argument.</span></span> <span data-ttu-id="b3c62-127">La version doit être spécifiée en trois parties (par exemple, 1.0.0-13232).</span><span class="sxs-lookup"><span data-stu-id="b3c62-127">The version must be specified as a 3-part version (for example, 1.0.0-13232).</span></span> <span data-ttu-id="b3c62-128">Si aucune valeur n’est spécifiée, la version `latest` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b3c62-128">If omitted, it uses the `latest` version.</span></span>

## <a name="options"></a><span data-ttu-id="b3c62-129">Options</span><span class="sxs-lookup"><span data-stu-id="b3c62-129">Options</span></span>

`-Channel <CHANNEL>`

<span data-ttu-id="b3c62-130">Spécifie le canal source pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="b3c62-130">Specifies the source channel for the installation.</span></span> <span data-ttu-id="b3c62-131">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="b3c62-131">The possible values are:</span></span>

- <span data-ttu-id="b3c62-132">`Current` - Version actuelle</span><span class="sxs-lookup"><span data-stu-id="b3c62-132">`Current` - Current release</span></span>
- <span data-ttu-id="b3c62-133">`LTS` - Canal de prise en charge à long terme (version prise en charge actuelle)</span><span class="sxs-lookup"><span data-stu-id="b3c62-133">`LTS` - Long-Term Support channel (current supported release)</span></span>
- <span data-ttu-id="b3c62-134">Version en deux parties au format X.Y représentant une version spécifique (par exemple, `2.0` ou `1.0`)</span><span class="sxs-lookup"><span data-stu-id="b3c62-134">Two-part version in X.Y format representing a specific release (for example, `2.0` or `1.0`)</span></span>
- <span data-ttu-id="b3c62-135">Nom de la branche [par exemple, `release/2.0.0`, `release/2.0.0-preview2` ou `master` pour la version la plus récente de la branche `master` (versions nocturnes « bleeding edge »)]</span><span class="sxs-lookup"><span data-stu-id="b3c62-135">Branch name [for example, `release/2.0.0`, `release/2.0.0-preview2`, or `master` for the latest from the `master` branch ("bleeding edge" nightly releases)]</span></span>

<span data-ttu-id="b3c62-136">La valeur par défaut est `LTS`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-136">The default value is `LTS`.</span></span> <span data-ttu-id="b3c62-137">Pour plus d’informations sur les canaux de prise en charge de .NET, consultez la rubrique [Cycle de prise en charge de .NET Core](https://www.microsoft.com/net/core/support).</span><span class="sxs-lookup"><span data-stu-id="b3c62-137">For more information on .NET support channels, see the [.NET Core Support Lifecycle](https://www.microsoft.com/net/core/support) topic.</span></span>

`-Version <VERSION>`

<span data-ttu-id="b3c62-138">Représente une version spécifique.</span><span class="sxs-lookup"><span data-stu-id="b3c62-138">Represents a specific build version.</span></span> <span data-ttu-id="b3c62-139">Les valeurs possibles sont :</span><span class="sxs-lookup"><span data-stu-id="b3c62-139">The possible values are:</span></span>

- <span data-ttu-id="b3c62-140">`latest` - Dernière version sur le canal (utilisée avec l’option `-Channel`)</span><span class="sxs-lookup"><span data-stu-id="b3c62-140">`latest` - Latest build on the channel (used with the `-Channel` option)</span></span>
- <span data-ttu-id="b3c62-141">`coherent` - Dernière version cohérente sur le canal ; utilise la dernière combinaison de packages stable (utilisée avec les options `-Channel` de nom de branche)</span><span class="sxs-lookup"><span data-stu-id="b3c62-141">`coherent` - Latest coherent build on the channel; uses the latest stable package combination (used with Branch name `-Channel` options)</span></span>
- <span data-ttu-id="b3c62-142">Version en trois parties au format X.Y.Z représentant une version spécifique ; remplace l’option `-Channel`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-142">Three-part version in X.Y.Z format representing a specific build version; supersedes the `-Channel` option.</span></span> <span data-ttu-id="b3c62-143">Par exemple :`2.0.0-preview2-006120`</span><span class="sxs-lookup"><span data-stu-id="b3c62-143">For example: `2.0.0-preview2-006120`</span></span>

<span data-ttu-id="b3c62-144">Si aucune valeur n'est spécifiée, la valeur utilisée par défaut pour `-Version` est `latest`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-144">If omitted, `-Version` defaults to `latest`.</span></span>

`-InstallDir <DIRECTORY>`

<span data-ttu-id="b3c62-145">Spécifie le chemin d’accès de l’installation.</span><span class="sxs-lookup"><span data-stu-id="b3c62-145">Specifies the installation path.</span></span> <span data-ttu-id="b3c62-146">S’il n’existe pas déjà, le répertoire est créé.</span><span class="sxs-lookup"><span data-stu-id="b3c62-146">The directory is created if it doesn't exist.</span></span> <span data-ttu-id="b3c62-147">La valeur par défaut est *% LocalAppData%\.dotnet*.</span><span class="sxs-lookup"><span data-stu-id="b3c62-147">The default value is *%LocalAppData%\.dotnet*.</span></span> <span data-ttu-id="b3c62-148">Remarque : Les fichiers binaires sont placés directement dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="b3c62-148">Note that binaries are placed directly in the directory.</span></span>

`-Architecture <ARCHITECTURE>`

<span data-ttu-id="b3c62-149">Architecture des fichiers binaires .NET Core à installer.</span><span class="sxs-lookup"><span data-stu-id="b3c62-149">Architecture of the .NET Core binaries to install.</span></span> <span data-ttu-id="b3c62-150">Les valeurs possibles sont `auto`, `x64` et `x86`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-150">Possible values are `auto`, `x64`, and `x86`.</span></span> <span data-ttu-id="b3c62-151">La valeur par défaut est `auto`, qui représente l’architecture de système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b3c62-151">The default value is `auto`, which represents the currently running OS architecture.</span></span>

`-SharedRuntime`

<span data-ttu-id="b3c62-152">S’il est défini, ce commutateur limite l’installation au runtime partagé.</span><span class="sxs-lookup"><span data-stu-id="b3c62-152">If set, this switch limits installation to the shared runtime.</span></span> <span data-ttu-id="b3c62-153">La totalité du SDK n’est pas installée.</span><span class="sxs-lookup"><span data-stu-id="b3c62-153">The entire SDK isn't installed.</span></span>

`-DryRun`

<span data-ttu-id="b3c62-154">Si cette option est définie, le script n’effectue pas l’installation, mais affiche à la place la ligne de commande à utiliser pour installer la version de l’interface CLI .NET Core actuellement demandée.</span><span class="sxs-lookup"><span data-stu-id="b3c62-154">If set, the script won't perform the installation; but instead, it displays what command line to use to consistently install the currently requested version of the .NET Core CLI.</span></span> <span data-ttu-id="b3c62-155">Par exemple, si vous spécifiez la version `latest`, elle affiche un lien avec la version spécifique, pour que cette commande puisse être utilisée de façon déterministe dans un script de génération.</span><span class="sxs-lookup"><span data-stu-id="b3c62-155">For example if you specify version `latest`, it displays a link with the specific version so that this command can be used deterministically in a build script.</span></span> <span data-ttu-id="b3c62-156">Elle affiche également l’emplacement du fichier binaire si vous préférez l’installer ou le télécharger vous-même.</span><span class="sxs-lookup"><span data-stu-id="b3c62-156">It also displays the binary's location if you prefer to install or download it yourself.</span></span>

`-NoPath`

<span data-ttu-id="b3c62-157">Si cette option est définie, le préfixe /installdir n’est pas exporté dans le chemin de la session actuelle.</span><span class="sxs-lookup"><span data-stu-id="b3c62-157">If set, the prefix/installdir are not exported to the path for the current session.</span></span> <span data-ttu-id="b3c62-158">Par défaut, le script modifie le chemin, ce qui rend les outils CLI disponibles immédiatement après l’installation.</span><span class="sxs-lookup"><span data-stu-id="b3c62-158">By default, the script will modify the PATH, which makes the CLI tools available immediately after install.</span></span>

`-AzureFeed`

<span data-ttu-id="b3c62-159">Spécifie l’URL du flux Azure à utiliser par ce programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="b3c62-159">Specifies the URL for the Azure feed to the installer.</span></span> <span data-ttu-id="b3c62-160">Il n’est pas recommandé de modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="b3c62-160">It isn't recommended that you change this value.</span></span> <span data-ttu-id="b3c62-161">La valeur par défaut est `https://dotnetcli.azureedge.net/dotnet`.</span><span class="sxs-lookup"><span data-stu-id="b3c62-161">The default is `https://dotnetcli.azureedge.net/dotnet`.</span></span>

`-ProxyAddress`

<span data-ttu-id="b3c62-162">Si cette option est définie, le programme d’installation utilise le proxy pendant la création de demandes web.</span><span class="sxs-lookup"><span data-stu-id="b3c62-162">If set, the installer uses the proxy when making web requests.</span></span> <span data-ttu-id="b3c62-163">(valide uniquement pour Windows)</span><span class="sxs-lookup"><span data-stu-id="b3c62-163">(Only valid for Windows)</span></span>

`--verbose`

<span data-ttu-id="b3c62-164">Affiche les informations de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="b3c62-164">Display diagnostics information.</span></span>

`--help`

<span data-ttu-id="b3c62-165">Affiche l’aide pour le script.</span><span class="sxs-lookup"><span data-stu-id="b3c62-165">Prints out help for the script.</span></span>

## <a name="examples"></a><span data-ttu-id="b3c62-166">Exemples</span><span class="sxs-lookup"><span data-stu-id="b3c62-166">Examples</span></span>

<span data-ttu-id="b3c62-167">Installez la dernière version LTS (Long Term Support) à l’emplacement par défaut :</span><span class="sxs-lookup"><span data-stu-id="b3c62-167">Install the latest long-term supported (LTS) version to the default location:</span></span>

<span data-ttu-id="b3c62-168">Windows :</span><span class="sxs-lookup"><span data-stu-id="b3c62-168">Windows:</span></span>

`./dotnet-install.ps1 -Channel LTS`

<span data-ttu-id="b3c62-169">Mac OS/Linux :</span><span class="sxs-lookup"><span data-stu-id="b3c62-169">macOS/Linux:</span></span>

`./dotnet-install.sh --channel LTS`

<span data-ttu-id="b3c62-170">Installez la dernière version depuis le canal 2.0 à l’emplacement spécifié :</span><span class="sxs-lookup"><span data-stu-id="b3c62-170">Install the latest version from 2.0 channel to the specified location:</span></span>

<span data-ttu-id="b3c62-171">Windows :</span><span class="sxs-lookup"><span data-stu-id="b3c62-171">Windows:</span></span>

`./dotnet-install.ps1 -Channel 2.0 -InstallDir C:\cli`

<span data-ttu-id="b3c62-172">Mac OS/Linux :</span><span class="sxs-lookup"><span data-stu-id="b3c62-172">macOS/Linux:</span></span>

`./dotnet-install.sh --channel 2.0 --install-dir ~/cli`

<span data-ttu-id="b3c62-173">Installez la version 1.1.0 du runtime partagé :</span><span class="sxs-lookup"><span data-stu-id="b3c62-173">Install the 1.1.0 version of the shared runtime:</span></span>

<span data-ttu-id="b3c62-174">Windows :</span><span class="sxs-lookup"><span data-stu-id="b3c62-174">Windows:</span></span>

`./dotnet-install.ps1 -SharedRuntime -Version 1.1.0`

<span data-ttu-id="b3c62-175">Mac OS/Linux :</span><span class="sxs-lookup"><span data-stu-id="b3c62-175">macOS/Linux:</span></span>

`./dotnet-install.sh --shared-runtime --version 1.1.0`

<span data-ttu-id="b3c62-176">Obtenir le script et installer les exemples unilignes de l’interface CLI .NET Core :</span><span class="sxs-lookup"><span data-stu-id="b3c62-176">Obtain script and install .NET Core CLI one-liner examples:</span></span>

<span data-ttu-id="b3c62-177">Windows :</span><span class="sxs-lookup"><span data-stu-id="b3c62-177">Windows:</span></span>

`@powershell -NoProfile -ExecutionPolicy unrestricted -Command "&([scriptblock]::Create((Invoke-WebRequest -useb 'https://dot.net/v1/dotnet-install.ps1'))) <additional install-script args>"`

<span data-ttu-id="b3c62-178">Mac OS/Linux :</span><span class="sxs-lookup"><span data-stu-id="b3c62-178">macOS/Linux:</span></span>

`curl -sSL https://dot.net/v1/dotnet-install.sh | bash /dev/stdin <additional install-script args>`

## <a name="see-also"></a><span data-ttu-id="b3c62-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c62-179">See also</span></span>

<span data-ttu-id="b3c62-180">[Versions de .NET Core](https://github.com/dotnet/core/releases) </span><span class="sxs-lookup"><span data-stu-id="b3c62-180">[.NET Core releases](https://github.com/dotnet/core/releases) </span></span>  
[<span data-ttu-id="b3c62-181">Archive de téléchargement de .NET Core Runtime et du Kit SDK</span><span class="sxs-lookup"><span data-stu-id="b3c62-181">.NET Core Runtime and SDK download archive</span></span>](https://github.com/dotnet/core/blob/master/release-notes/download-archive.md)
