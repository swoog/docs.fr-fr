---
title: Configuration requise pour .NET Core sur Mac
description: Versions macOS et dépendances .NET Core prises en charge pour développer, déployer et exécuter des applications .NET Core sur des ordinateurs macOS.
author: guardrex
ms.author: mairaw
ms.date: 09/27/2017
ms.openlocfilehash: 31fee3bbc85daa66019b63e50b48509b79606fce
ms.sourcegitcommit: c217b067985905cb21eafc5dd9a83568d7ff4e45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36315064"
---
# <a name="prerequisites-for-net-core-on-macos"></a><span data-ttu-id="27ce7-103">Configuration requise pour .NET Core sur macOS</span><span class="sxs-lookup"><span data-stu-id="27ce7-103">Prerequisites for .NET Core on macOS</span></span>

<span data-ttu-id="27ce7-104">Cet article vous présente les versions macOS et les dépendances .NET Core prises en charge nécessaires pour développer, déployer et exécuter des applications .NET Core sur des ordinateurs macOS.</span><span class="sxs-lookup"><span data-stu-id="27ce7-104">This article shows you the supported macOS versions and .NET Core dependencies that you need to develop, deploy, and run .NET Core applications on macOS machines.</span></span> <span data-ttu-id="27ce7-105">Les versions de système d’exploitation et dépendances prises en charge suivantes s’appliquent aux trois méthodes de développement des applications .NET Core sur un Mac : via la [ligne de commande de votre éditeur favori](tutorials/using-with-xplat-cli.md), [Visual Studio Code](https://code.visualstudio.com/) et [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/visual-studio-mac/).</span><span class="sxs-lookup"><span data-stu-id="27ce7-105">The supported OS versions and dependencies that follow apply to the three ways of developing .NET Core apps on a Mac: via the [command-line with your favorite editor](tutorials/using-with-xplat-cli.md), [Visual Studio Code](https://code.visualstudio.com/), and [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/visual-studio-mac/).</span></span>

## <a name="supported-macos-versions"></a><span data-ttu-id="27ce7-106">Versions macOS prises en charge</span><span class="sxs-lookup"><span data-stu-id="27ce7-106">Supported macOS versions</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="27ce7-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="27ce7-107">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="27ce7-108">.NET Core 2.x est pris en charge par les versions suivantes de macOS :</span><span class="sxs-lookup"><span data-stu-id="27ce7-108">.NET Core 2.x is supported on the following versions of macOS:</span></span>

* <span data-ttu-id="27ce7-109">macOS 10.12 « Sierra » et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="27ce7-109">macOS 10.12 "Sierra" and later versions</span></span>

<span data-ttu-id="27ce7-110">Consultez [.NET Core 2.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 2.x, les systèmes d’exploitation non pris en charge et des liens sur la politique concernant le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="27ce7-110">See [.NET Core 2.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) for the complete list of .NET Core 2.x supported operating systems, out of support OS versions, and lifecycle policy links.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="27ce7-111">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="27ce7-111">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="27ce7-112">.NET Core 1.x est pris en charge par les versions suivantes de macOS :</span><span class="sxs-lookup"><span data-stu-id="27ce7-112">.NET Core 1.x is supported on the following versions of macOS:</span></span>

* <span data-ttu-id="27ce7-113">macOS 10.12 "Sierra"</span><span class="sxs-lookup"><span data-stu-id="27ce7-113">macOS 10.12 "Sierra"</span></span>
* <span data-ttu-id="27ce7-114">macOS 10.11 "El Capitan"</span><span class="sxs-lookup"><span data-stu-id="27ce7-114">macOS 10.11 "El Capitan"</span></span>

<span data-ttu-id="27ce7-115">Consultez [.NET Core 1.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 1.x, les systèmes d’exploitation non pris en charge et des liens sur la politique concernant le cycle de vie.</span><span class="sxs-lookup"><span data-stu-id="27ce7-115">See [.NET Core 1.x Supported OS Versions](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) for the complete list of .NET Core 1.x supported operating systems, out of support OS versions, and lifecycle policy links.</span></span>

---

## <a name="net-core-dependencies"></a><span data-ttu-id="27ce7-116">Dépendances .NET Core</span><span class="sxs-lookup"><span data-stu-id="27ce7-116">.NET Core dependencies</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="27ce7-117">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="27ce7-117">.NET Core 2.x</span></span>](#tab/netcore2x)

<span data-ttu-id="27ce7-118">Téléchargez et installez le kit SDK .NET Core à partir de [Téléchargements .NET](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="27ce7-118">Download and install the .NET Core SDK from [.NET Downloads](https://www.microsoft.com/net/download/core).</span></span> <span data-ttu-id="27ce7-119">Si vous rencontrez des problèmes d’installation sur macOS, consultez la rubrique [Problèmes connus](https://github.com/dotnet/core/tree/master/release-notes/2.0) associée à la version installée.</span><span class="sxs-lookup"><span data-stu-id="27ce7-119">If you have problems with the installation on macOS, consult the [Known issues](https://github.com/dotnet/core/tree/master/release-notes/2.0) topic for the version you have installed.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="27ce7-120">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="27ce7-120">.NET Core 1.x</span></span>](#tab/netcore1x)

<span data-ttu-id="27ce7-121">**.NET Core 1.x**</span><span class="sxs-lookup"><span data-stu-id="27ce7-121">**.NET Core 1.x**</span></span>

<span data-ttu-id="27ce7-122">.NET Core 1.x nécessite OpenSSL lors d’une exécution sous macOS.</span><span class="sxs-lookup"><span data-stu-id="27ce7-122">.NET Core 1.x requires OpenSSL when running on macOS.</span></span> <span data-ttu-id="27ce7-123">Un moyen simple d’obtenir OpenSSL consiste à utiliser le gestionnaire de package [Homebrew (« brew »)](https://brew.sh/) pour macOS.</span><span class="sxs-lookup"><span data-stu-id="27ce7-123">An easy way to obtain OpenSSL is by using the [Homebrew ("brew")](https://brew.sh/) package manager for macOS.</span></span> <span data-ttu-id="27ce7-124">Après avoir installé *brew*, installez OpenSSL en exécutant les commandes suivantes dans une invite de Terminal (commande) :</span><span class="sxs-lookup"><span data-stu-id="27ce7-124">After installing *brew*, install OpenSSL by executing the following commands at a Terminal (command) prompt:</span></span>

```console
brew update
brew install openssl
mkdir -p /usr/local/lib
ln -s /usr/local/opt/openssl/lib/libcrypto.1.0.0.dylib /usr/local/lib/
ln -s /usr/local/opt/openssl/lib/libssl.1.0.0.dylib /usr/local/lib/
```

<span data-ttu-id="27ce7-125">Téléchargez et installez le kit SDK .NET Core à partir de [Téléchargements .NET](https://www.microsoft.com/net/download/core).</span><span class="sxs-lookup"><span data-stu-id="27ce7-125">Download and install the .NET Core SDK from [.NET Downloads](https://www.microsoft.com/net/download/core).</span></span> <span data-ttu-id="27ce7-126">Si vous rencontrez des problèmes d’installation sur macOS, consultez les rubriques [Problèmes connus 1.0.0](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.0-known-issues.md) et [Problèmes connus 1.0.1](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.1-known-issues.md).</span><span class="sxs-lookup"><span data-stu-id="27ce7-126">If you have problems with the installation on macOS, consult the [1.0.0 Known Issues](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.0-known-issues.md) and [1.0.1 Known Issues](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.1-known-issues.md) topics.</span></span>

---

## <a name="increase-the-maximum-open-file-limit-net-core-versions-before-net-core-sdk-202"></a><span data-ttu-id="27ce7-127">Augmentez la limite maximale d’ouverture de fichier (dans les versions .NET Core antérieures à .NET Core SDK 2.0.2)</span><span class="sxs-lookup"><span data-stu-id="27ce7-127">Increase the maximum open file limit (.NET Core versions before .NET Core SDK 2.0.2)</span></span> 

<span data-ttu-id="27ce7-128">Dans les versions de .NET Core antérieures à .NET Core SDK 2.0.2, la limite d’ouverture de fichier par défaut sur macOS peut ne pas suffire pour certaines charges de travail .NET Core, telles que la restauration de projets ou l’exécution de tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="27ce7-128">In older .NET Core versions (before .NET Core SDK 2.0.2), the default open file limit on macOS may not be sufficient for some .NET Core workloads, such as restoring projects or running unit tests.</span></span>

<span data-ttu-id="27ce7-129">Vous pouvez augmenter cette limite en effectuant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="27ce7-129">You can increase this limit by following these steps:</span></span>

1. <span data-ttu-id="27ce7-130">À l’aide d’un éditeur de texte, créez un fichier _/Library/LaunchDaemons/limit.maxfiles.plist_ et enregistrez le fichier avec le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="27ce7-130">Using a text editor, create a new file _/Library/LaunchDaemons/limit.maxfiles.plist_, and save the file with this content:</span></span>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN"
        "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
  <dict>
    <key>Label</key>
    <string>limit.maxfiles</string>
    <key>ProgramArguments</key>
    <array>
      <string>launchctl</string>
      <string>limit</string>
      <string>maxfiles</string>
      <string>2048</string>
      <string>4096</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
    <key>ServiceIPC</key>
    <false/>
  </dict>
</plist>
```

2. <span data-ttu-id="27ce7-131">Dans une fenêtre de terminal, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="27ce7-131">In a terminal window, run the following command:</span></span>

```console
echo 'ulimit -n 2048' | sudo tee -a /etc/profile
```

3. <span data-ttu-id="27ce7-132">Redémarrez votre Mac pour appliquer ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="27ce7-132">Reboot your Mac to apply these settings.</span></span>

## <a name="visual-studio-for-mac"></a><span data-ttu-id="27ce7-133">Visual Studio pour Mac</span><span class="sxs-lookup"><span data-stu-id="27ce7-133">Visual Studio for Mac</span></span>

<span data-ttu-id="27ce7-134">Vous pouvez utiliser l’éditeur de votre choix pour développer des applications .NET Core à l’aide du Kit SDK .NET Core.</span><span class="sxs-lookup"><span data-stu-id="27ce7-134">You can use any editor to develop .NET Core applications using the .NET Core SDK.</span></span> <span data-ttu-id="27ce7-135">Toutefois, si vous voulez développer des applications .NET Core sous Mac dans un environnement de développement intégré, vous pouvez utiliser [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/visual-studio-mac/).</span><span class="sxs-lookup"><span data-stu-id="27ce7-135">However, if you want to develop .NET Core applications on a Mac in an integrated development environment, you can use [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/visual-studio-mac/).</span></span> 

<span data-ttu-id="27ce7-136">Le développement .NET Core sur macOS avec Visual Studio pour Mac nécessite :</span><span class="sxs-lookup"><span data-stu-id="27ce7-136">.NET Core development on macOS with Visual Studio for Mac requires:</span></span>

* <span data-ttu-id="27ce7-137">Une version prise en charge du système d’exploitation macOS</span><span class="sxs-lookup"><span data-stu-id="27ce7-137">A supported version of the macOS operating system</span></span>
* <span data-ttu-id="27ce7-138">OpenSSL (.NET Core 1.x uniquement ; .NET Core 2.x utilise les services de sécurité disponibles en mode natif dans macOS)</span><span class="sxs-lookup"><span data-stu-id="27ce7-138">OpenSSL (.NET Core 1.x only; .NET Core 2.x uses security services available natively in macOS)</span></span>
* <span data-ttu-id="27ce7-139">.NET Core SDK pour Mac</span><span class="sxs-lookup"><span data-stu-id="27ce7-139">.NET Core SDK for Mac</span></span>
* [<span data-ttu-id="27ce7-140">Visual Studio pour Mac</span><span class="sxs-lookup"><span data-stu-id="27ce7-140">Visual Studio for Mac</span></span>](https://visualstudio.microsoft.com/vs/visual-studio-mac/)
