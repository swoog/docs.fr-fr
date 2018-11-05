---
title: Prérequis pour .NET Core sur Linux
description: Versions Linux et dépendances .NET Core prises en charge pour développer, déployer et exécuter des applications .NET Core sur des ordinateurs Linux.
author: jralexander
ms.author: johalex
ms.date: 08/20/2018
ms.openlocfilehash: 4939dfb642c2aef9da593a193f42334f1d57e067
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48842266"
---
# <a name="prerequisites-for-net-core-on-linux"></a>Prérequis pour .NET Core sur Linux

Cet article montre les dépendances nécessaires pour développer des applications .NET Core sur Linux. Les distributions/versions Linux et les dépendances prises en charge ci-après s’appliquent aux deux façons de développer des applications .NET Core sur Linux :

* [Ligne de commande avec votre éditeur favori](tutorials/using-with-xplat-cli.md)
* [Visual Studio Code](https://code.visualstudio.com/)

> [!NOTE]
> Le kit SDK .NET Core n’est pas nécessaire pour les environnements/serveurs de production. Seul le package du Runtime .NET Core est nécessaire pour les applications déployées dans des environnements de production. Le Runtime .NET Core est déployé avec les applications dans le cadre d’un déploiement autonome, mais il doit être déployé séparément pour des applications déployées qui dépendent du framework. Pour plus d’informations sur les types de déploiements autonomes et dépendants du framework, consultez [Déploiement d’applications .NET Core](./deploying/index.md). Consultez également [Self-contained Linux applications](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md) pour obtenir des instructions spécifiques.

## <a name="supported-linux-versions"></a>Versions de Linux prises en charge

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

.NET Core 2.x traite Linux comme un seul système d’exploitation. Il existe une seule version Linux (par architecture de puce) pour les distributions Linux prises en charge.

**NET Core 2.1**

NET Core 2.1 est pris en charge sur les distributions/versions Linux suivantes :

* Red Hat Enterprise Linux 7, 6 - 64 bits (`x86_64` ou `amd64`)
* CentOS 7 - 64 bits (`x86_64` ou `amd64`) 
* Oracle Linux 7 - 64 bits (`x86_64` ou `amd64`) 
* Fedora 28, 27 - 64 bits (`x86_64` ou `amd64`) 
* Debian 9 (64 bits, `amd64`), 8.7 ou une version ultérieure – 64 bits (`arm32` ou `x86_64`)
* Ubuntu 18.04 (64 bits, `arm32`), 16.04, 14.04 – 64 bits (`x86_64` ou `amd64`)
* Linux Mint 18, 17 - 64 bits (`x86_64` ou `amd64`)
* openSUSE 42.3 ou version ultérieure - 64 bits (`x86_64` ou `amd64`)
* SUSE Enterprise Linux (SLES) 12 Service Pack 2 ou version ultérieure - 64 bits (`x86_64` ou `amd64`)
* Alpine Linux 3.7 ou version ultérieure - 64 bits (`x86_64` ou `amd64`)

Consultez [.NET Core 2.1 - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation, distributions et versions pris en charge par .NET Core 2.1, les systèmes d’exploitation non pris en charge et des liens sur la politique concernant le cycle de vie.

**NET Core 2.0**

NET Core 2.0 est pris en charge sur les distributions/versions Linux 64 bits suivantes (`x86_64` ou `amd64`) :

* Red Hat Enterprise Linux 7, 6
* CentOS 7
* Oracle Linux 7
* Fedora 27
* Debian 9, 8.7 ou versions ultérieures
* Ubuntu 18.04, 16.04, 14.04
* Linux Mint 18, 17
* openSUSE 42.3 ou versions ultérieures
* SUSE Enterprise Linux (SLES) 12 Service Pack 2 ou ultérieur

Consultez [.NET Core 2.0 - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation, distributions et versions pris en charge par .NET Core 2.0, les systèmes d’exploitation non pris en charge et des liens sur la politique concernant le cycle de vie.

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

.NET Core 1.x est pris en charge sur les distributions/versions Linux 64 bits suivantes (`x86_64` ou `amd64`) :

* Red Hat Enterprise Linux 7
* CentOS 7
* Oracle Linux 7
* Fedora 28 (.NET Core 1.1), 27
* Debian 8.2 ou versions ultérieures
* Ubuntu 18.04 (.NET Core 1.1), 16.04, 14.04
* Linux Mint 17
* openSUSE 42.3 ou versions ultérieures (.NET Core 1.1)

Consultez [.NET Core 1.x - Versions des systèmes d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) pour obtenir la liste complète des systèmes d’exploitation pris en charge par .NET Core 1.x, les systèmes d’exploitation non pris en charge et des liens sur la politique concernant le cycle de vie.

---

## <a name="linux-distribution-dependencies"></a>Dépendances des distributions Linux

Les éléments suivants sont destinés à être des exemples. Les versions et les noms exacts peuvent varier légèrement sur la distribution Linux que vous choisissez.

### <a name="ubuntu"></a>Ubuntu

Les distributions Ubuntu nécessitent l’installation des bibliothèques suivantes :

* liblttng-ust0
* libcurl3
* libssl1.0.0
* libkrb5-3
* zlib1g
* libicu52 (pour 14.x)
* libicu55 (pour 16.x)
* libicu57 (pour 17.x)
* libicu60 (pour 18.x)

Pour les versions antérieures à .NET Core 2.1, les dépendances suivantes sont également requises :

* libunwind8
* libuuid1

### <a name="centos-and-fedora"></a>CentOS et Fedora

Les distributions CentOS nécessitent l’installation des bibliothèques suivantes :

* lttng-ust
* libcurl
* openssl-libs
* krb5-libs
* libicu
* zlib

Utilisateurs de Fedora : si votre version d’openssl >= 1.1, vous devez installer compat-openssl10.

Pour les versions antérieures à .NET Core 2.1, les dépendances suivantes sont également requises :

* libunwind
* libuuid

Pour plus d’informations sur les dépendances, consultez [Applications Linux autonomes](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md) (en anglais).

## <a name="installing-net-core-dependencies-with-the-native-installers"></a>Installation des dépendances .NET Core avec les programmes d’installation natifs

Les programmes d’installation natifs .NET Core sont disponibles pour les distributions/versions Linux prises en charge. Les programmes d’installation natifs requièrent un accès administrateur (sudo) au serveur. L’avantage d’utiliser un programme d’installation natif est que toutes les dépendances natives .NET Core sont installées. En outre, les programmes d’installation natifs installent le SDK .NET Core à l’échelle du système.

Sur Linux, il existe deux choix pour le package de programme d’installation :

* Utilisation d’un gestionnaire de package basé sur le flux, tel qu’apt-get pour Ubuntu, ou yum pour CentOS/RHEL.
* Utilisation des packages eux-mêmes, DEB ou RPM

### <a name="scripting-installs-with-the-net-core-installer-script"></a>Script d’installation avec le script de programme d’installation de .NET Core

Les [scripts dotnet-install](./tools/dotnet-install-script.md) sont utilisés pour effectuer une installation non administrateur de la chaîne d’outils CLI et du runtime partagé. Vous pouvez télécharger le script à partir de [https://dot.net/v1/dotnet-install.sh](https://dot.net/v1/dotnet-install.sh).

Le script installe par défaut la dernière version de « LTS », qui correspond à .NET Core 1.1. Pour installer .NET Core 2.x, exécutez le script avec le commutateur suivant :

```console
./dotnet-install.sh -c Current
```

Le script bash du programme d’installation est utilisé dans les scénarios d’automatisation et dans les installations non administratives. Comme ce script lit également les commutateurs PowerShell, ces derniers peuvent être utilisés avec le script sur les systèmes Linux/OS X.

## <a name="install-net-core-for-supported-red-hat-enterprise-linux-rhel-versions"></a>Installer .NET Core pour les versions prises en charge de Red Hat Enterprise Linux (RHEL)

Pour installer .NET Core sur des versions de RHEL prises en charge :

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

**.NET Core 2.1**

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Pour obtenir les dernières informations sur l’installation de .NET Core 2.1 sur Red Hat Enterprise Linux, consultez le [Guide de prise en main de .NET Core 2.1](https://access.redhat.com/documentation/en-us/net_core/2.1/html/getting_started_guide/)

**.NET Core 2.0**

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Pour obtenir les dernières informations sur l’installation de .NET Core 2.0 sur Red Hat Enterprise Linux, consultez le [Guide de prise en main de .NET Core 2.0](https://access.redhat.com/documentation/en-us/net_core/2.0/html/getting_started_guide/) 

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

**.NET Core 1.1**

1. Supprimez du système toute **version antérieure** de .NET Core.

2.  Pour obtenir les dernières informations sur l’installation de .NET Core 1.1 sur Red Hat Enterprise Linux, consultez le [Guide de démarrage rapide de .NET Core 1.1](https://access.redhat.com/documentation/en-us/net_core/1.1/html/getting_started_guide/)
     
**.NET Core 1.0**

1. Supprimez du système toute **version antérieure** de .NET Core.

2.  Pour obtenir les dernières informations sur l’installation de .NET Core 1.0 sur Red Hat Enterprise Linux, consultez le [Guide de démarrage rapide de .NET Core 1.0](https://access.redhat.com/documentation/en-us/net_core/1.0/html/getting_started_guide/)

Pour obtenir de l’aide sur l’inscription à l’accès au canal Red Hat .NET, consultez le [chapitre 1 du guide de prise en main de .NET Core 1.1](https://access.redhat.com/documentation/en/net-core/1.1/paged/getting-started-guide/) sur Red Hat.

---

## <a name="install-net-core-for-supported-ubuntu-and-linux-mint-distributionsversions-64-bit"></a>Installer .NET Core pour les versions/distributions (64 bits) prises en charge d’Ubuntu et de Linux Mint

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 2.x sur des versions/distributions (64 bits) prises en charge d’Ubuntu et de Linux Mint :

**.NET Core 2.0**

|Runtimes / SDK          |Ubuntu 18.04    |Ubuntu 17.10    |Ubuntu 16.04 / Linux Mint 18|Ubuntu 14.04 / Linux Mint 17|
|-------------------------|----------------|----------------|----------------------------|----------------------------|
|Runtime .NET Core 2.0.9  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.9)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.9)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.9)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.9)            |
|Runtime .NET Core 2.0.8  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.8)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.8)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.8)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.8)            |
|Runtime .NET Core 2.0.7  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.7)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.7)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.7)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.7)            |
|Runtime .NET Core 2.0.6  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.6)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.6)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.6)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.6)            |
|Runtime .NET Core 2.0.5  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.0.5)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.0.5)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.0.5)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.0.5)            |
|Kit SDK .NET Core 2.1.202    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.202)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.202)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.202)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.202)            |
|Kit SDK .NET Core 2.1.201    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.201)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.201)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.201)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.201)            |
|SDK .NET Core 2.1.200    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.200)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.200)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.200)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.200)            |
|SDK .NET Core 2.1.105    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.105)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.105)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.105)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.105)            |
|SDK .NET Core 2.1.103    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.103)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.103)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.103)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.103)            |
|SDK .NET Core 2.0.3      |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.0.3)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.0.3)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.0.3)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.0.3)            |
|SDK .NET Core 2.0.0      |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.0.0)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.0.0)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.0.0)          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.0.0)            |

**.NET Core 2.1**

>[!IMPORTANT]
> Pour utiliser .NET Core 2.1 avec Visual Studio, vous devez [installer Visual Studio 2017 15.7 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).

|Runtimes / SDK          |Ubuntu 18.04    |Ubuntu 17.10    |Ubuntu 16.04 / Linux Mint 18|Ubuntu 14.04 / Linux Mint 17|
|-------------------------|----------------|----------------|----------------------------|----------------------------|
|Runtime .NET Core 2.1.2          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.1.2)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.1.2)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.1.2)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.1.2)            |
|Kit SDK .NET Core 2.1.400     |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.400)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.400)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.400)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.400)            |
|Kit SDK .NET Core 2.1.302     |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.302)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.302)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.302)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.302)            |
|Runtime .NET Core 2.1.1          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.1.1)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.1.1)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.1.1)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.1.1)            |
|Kit SDK .NET Core 2.1.301     |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.301)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.301)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.301)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.301)            |
|Runtime .NET Core 2.1.0          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/runtime-2.1.0)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/runtime-2.1.0)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/runtime-2.1.0)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/runtime-2.1.0)            |
|SDK .NET Core 2.1.300     |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu18-04/sdk-2.1.300)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu17-10/sdk-2.1.300)|[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu16-04/sdk-2.1.300)            |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/ubuntu14-04/sdk-2.1.300)            |

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 1.x sur des versions/distributions (64 bits) prises en charge d’Ubuntu et de Linux Mint :

| Runtimes / SDK         |Ubuntu 16.04 / Linux Mint 18|Ubuntu 14.04 / Linux Mint 17|
|-------------------------|----------------------------|----------------------------|
|Runtime .NET Core 1.1.9  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.9-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.1.8  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.1.7  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.1.6  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.1.5  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.1.4  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.0.10 |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.0.9  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.0.8  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.0.7  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.0.5  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-ubuntu-14.04-x64-binaries)            |
|Runtime .NET Core 1.0.4  |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-ubuntu-14.04-x64-binaries)            |
|Kit SDK .NET Core 1.1.10     |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-ubuntu-14.04-x64-binaries)            |
|Kit SDK .NET Core 1.1.9      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-ubuntu-14.04-x64-binaries)            |
|SDK .NET Core 1.1.8      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-ubuntu-14.04-x64-binaries)            |
|SDK .NET Core 1.1.7      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-ubuntu-14.04-x64-binaries)            |
|Kit SDK .NET Core 1.1.5      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-ubuntu-14.04-x64-binaries)            |
|Kit SDK .NET Core 1.1.4      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-ubuntu-14.04-x64-binaries)            |
|SDK .NET Core 1.0.4      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-ubuntu-14.04-x64-binaries)            |
|SDK .NET Core 1.0.1      |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-ubuntu-16.04-x64-binaries)            |[Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-ubuntu-14.04-x64-binaries)            |

---

## <a name="install-net-core-for-supported-debian-versions-64-bit"></a>Installer .NET Core pour les versions (64 bits) prises en charge de Debian

Pour installer .NET Core sur des versions (64 bits) prises en charge de Debian :

> [!NOTE]
> Un répertoire contrôlé par l’utilisateur est requis pour les installations du système Linux système depuis tar.gz.

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 2.x sur des versions (64 bits) prises en charge de Debian :

**.NET Core 2.0**

|Runtimes / SDK          |Debian 9       |Debian 8       |
|-------------------------|---------------|---------------|
|Runtime .NET Core 2.0.9  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.9)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.9)   |
|Runtime .NET Core 2.0.8  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.8)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.8)   |
|Runtime .NET Core 2.0.7  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.7)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.7)   |
|Runtime .NET Core 2.0.6  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.6)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.6)   |
|Runtime .NET Core 2.0.5  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.5)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.5)   |
|Runtime .NET Core 2.0.3  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.3)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.3)   |
|Runtime .NET Core 2.0.0  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.0.0)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.0.0)   |
|Kit SDK .NET Core 2.1.202    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.202)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.202)   |
|Kit SDK .NET Core 2.1.201    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.201)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.201)   |
|SDK .NET Core 2.1.200    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.200)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.200)   |
|SDK .NET Core 2.1.105    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.105)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.105)   |
|SDK .NET Core 2.1.105    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.105)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.105)   |
|Kit SDK .NET Core 2.1.104    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.104)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.104)   |
|SDK .NET Core 2.1.103    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.103)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.103)   |
|Kit SDK .NET Core 2.1.102    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.102)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.102)   |
|Kit SDK .NET Core 2.1.101    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.101)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.101)   |
|SDK .NET Core 2.0.3      |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.0.3)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.0.3)   |
|SDK .NET Core 2.0.0      |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.0.0)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.0.0)   |

**.NET Core 2.1**

>[!IMPORTANT]
> Pour utiliser .NET Core 2.1 avec Visual Studio, vous devez [installer Visual Studio 2017 15.7 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).

|Runtimes / SDK                  |Debian 9       |Debian 8       |
|---------------------------------|---------------|---------------|
|Runtime .NET Core 2.1.2          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.1.2)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.1.2)   |
|Kit SDK .NET Core 2.1.400        |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.400)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.400)        |
|Kit SDK .NET Core 2.1.302        |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.302)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.302)        |
|Runtime .NET Core 2.1.1          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.1.1)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.1.1)   |
|Kit SDK .NET Core 2.1.301        |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.301)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.301)        |
|Runtime .NET Core 2.1.0          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/runtime-2.1.0)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/runtime-2.1.0)   |
|SDK .NET Core 2.1.300        |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian9/sdk-2.1.300)   |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/debian8/sdk-2.1.300)        |

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 1.x sur Debian 9 ou Debian 8 :

* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.9-linux-debian-x64-binaries) du Runtime .NET Core 1.1.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-debian-x64-binaries) du Runtime .NET Core 1.1.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-debian-x64-binaries) du Runtime .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-debian-x64-binaries) du Runtime .NET Core 1.1.6
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-debian-x64-binaries) du Runtime .NET Core 1.1.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-debian-x64-binaries) du Runtime .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-debian-x64-binaries) du Runtime .NET Core 1.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-debian-x64-binaries) du Runtime .NET Core 1.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.0-linux-debian-x64-binaries) du Runtime .NET Core 1.1.0
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-debian-x64-binaries) du Runtime .NET Core 1.0.10
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-debian-x64-binaries) du Runtime .NET Core 1.0.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-debian-x64-binaries) du Runtime .NET Core 1.0.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-debian-x64-binaries) du Runtime .NET Core 1.0.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-debian-x64-binaries) du Runtime .NET Core 1.0.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-debian-x64-binaries) du Runtime .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-debian-x64-binaries) du kit SDK .NET Core 1.1.10
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-debian-x64-binaries) du kit SDK .NET Core 1.1.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-debian-x64-binaries) du SDK .NET Core 1.1.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-debian-x64-binaries) du SDK .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-debian-x64-binaries) du kit SDK .NET Core 1.1.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-debian-x64-binaries) du kit SDK .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-debian-x64-binaries) du SDK .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-debian-x64-binaries) du SDK .NET Core 1.0.1

---

## <a name="install-net-core-for-supported-fedora-versions-64-bit"></a>Installer .NET Core pour les versions (64 bits) prises en charge de Fedora

Pour installer .NET Core sur des versions prises en charge de Fedora :

> [!NOTE]
> Un répertoire contrôlé par l’utilisateur est requis pour les installations du système Linux système depuis tar.gz.

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 2.x sur des versions (64 bits) prises en charge de Fedora :

**.NET Core 2.0**

|Runtimes / SDK          |Fedora 26 ou version ultérieure |Fedora 25 ou version antérieure |
|-------------------------|-------------------|----------------------|
|Runtime .NET Core 2.0.9  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.9)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.9)           |
|Runtime .NET Core 2.0.8  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.8)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.8)           |
|Runtime .NET Core 2.0.7  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.7)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.7)           |
|Runtime .NET Core 2.0.6  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.6)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.6)           |
|Runtime .NET Core 2.0.5  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.5)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.5)           |
|Runtime .NET Core 2.0.3  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.3)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.3)           |
|Runtime .NET Core 2.0.0  |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/runtime-2.0.0)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/runtime-2.0.0)           |
|SDK .NET Core 2.1.200    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.1.200)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.1.200)           |
|SDK .NET Core 2.1.105    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.1.105)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.1.105)           |
|SDK .NET Core 2.1.103    |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.1.103)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.1.103)           |
|SDK .NET Core 2.0.3      |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora26/sdk-2.0.3)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora25/sdk-2.0.3)           |

**.NET Core 2.1**

>[!IMPORTANT]
> Pour utiliser .NET Core 2.1 avec Visual Studio, vous devez [installer Visual Studio 2017 15.7 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).

|Runtimes / SDK                  |Fedora 28          |Fedora 27             |
|---------------------------------|-------------------|----------------------|
|Runtime .NET Core 2.1.2          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/runtime-2.1.2)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/runtime-2.1.2)           |
|Kit SDK .NET Core 2.1.400          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.400)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.400)           |
|Kit SDK .NET Core 2.1.302          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.302)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.302)           |
|Runtime .NET Core 2.1.1          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/runtime-2.1.1)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/runtime-2.1.1)           |
|Kit SDK .NET Core 2.1.301          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.301)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.301)           |
|Runtime .NET Core 2.1.0          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/runtime-2.1.0)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/runtime-2.1.0)           |
|SDK .NET Core 2.1.300          |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora28/sdk-2.1.300)       |[Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/fedora27/sdk-2.1.300)           |

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 1.x sur des versions (64 bits) prises en charge de Fedora :

**Fedora 24**

* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.6
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-fedora-24-x64-binaries) du Runtime .NET Core 1.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-fedora-24-x64-binaries) du kit SDK .NET Core 1.1.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-fedora-24-x64-binaries) du SDK .NET Core 1.1.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-fedora-24-x64-binaries) du SDK .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5linux-fedora-24-x64-binaries) du kit SDK .NET Core 1.1.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5linux-fedora-24-x64-binaries) du kit SDK .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-debian-x64-binaries) du SDK .NET Core 1.0.1

**Fedora 23**

* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-fedora-23-x64-binaries) du Runtime .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-fedora-23-x64-binaries) du Runtime .NET Core 1.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-fedora-23-x64-binaries) du Runtime .NET Core 1.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-fedora-23-x64-binaries) du Runtime .NET Core 1.0.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-fedora-23-x64-binaries) du Runtime .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4linux-fedora-23-x64-binaries) du kit SDK .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.2linux-fedora-23-x64-binaries) du kit SDK .NET Core 1.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.2linux-fedora-23-x64-binaries) du kit SDK .NET Core 1.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-fedora-23-x64-binaries) du SDK .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-fedora-23-x64-binaries) du SDK .NET Core 1.0.1

---

## <a name="install-net-core-for-supported-centos-and-oracle-linux-distributionsversions-64-bit"></a>Installer .NET Core pour les versions/distributions (64 bits) prises en charge de CentOS et d’Oracle Linux

Pour installer .NET Core pour les versions/distributions (64 bits) prises en charge de CentOS et d’Oracle Linux :

> [!NOTE]
> Un répertoire contrôlé par l’utilisateur est requis pour les installations du système Linux système depuis tar.gz.

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 2.x sur des versions/distributions (64 bits) prises en charge de CentOS et d’Oracle Linux :

**.NET Core 2.0**

* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.9) du Runtime .NET Core 2.0.9
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.8) du Runtime .NET Core 2.0.8
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.7) du Runtime .NET Core 2.0.7
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.6) du Runtime .NET Core 2.0.6
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.5) du Runtime .NET Core 2.0.5
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.3) du Runtime .NET Core 2.0.3
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.0.0) du Runtime .NET Core 2.0.0
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.202) du kit SDK .NET Core 2.1.202
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.201) du kit SDK .NET Core 2.1.201
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.200) du SDK .NET Core 2.1.200
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.105) du SDK .NET Core 2.1.105
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.104) du kit SDK .NET Core 2.1.104
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.103) du SDK .NET Core 2.1.103
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.102) du kit SDK .NET Core 2.1.102
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.0.3) du SDK .NET Core 2.0.3
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.0.0) du SDK .NET Core 2.0.0
 
**.NET Core 2.1**

>[!IMPORTANT]
> Pour utiliser .NET Core 2.1 avec Visual Studio, vous devez [installer Visual Studio 2017 15.7 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).

* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.1.2) du Runtime .NET Core 2.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.400) du kit SDK .NET Core 2.1.400
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.302) du kit SDK .NET Core 2.1.302
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.1.1) du Runtime .NET Core 2.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.301) du kit SDK .NET Core 2.1.301
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/runtime-2.1.0) du Runtime .NET Core 2.1.0
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/centos/sdk-2.1.300) du SDK .NET Core 2.1.300

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 1.x sur des versions/distributions (64 bits) prises en charge de CentOS et d’Oracle Linux :

* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.9-linux-centos-x64-binaries) du Runtime .NET Core 1.1.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.8-linux-centos-x64-binaries) du Runtime .NET Core 1.1.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-centos-x64-binaries) du Runtime .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-centos-x64-binaries) du Runtime .NET Core 1.1.6
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.5-linux-centos-x64-binaries) du Runtime .NET Core 1.1.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.4-linux-centos-x64-binaries) du Runtime .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.2-linux-centos-x64-binaries) du Runtime .NET Core 1.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.1-linux-centos-x64-binaries) du Runtime .NET Core 1.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.12-linux-centos-x64-binaries) du Runtime .NET Core 1.0.12
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.11-linux-centos-x64-binaries) du Runtime .NET Core 1.0.11
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.10-linux-centos-x64-binaries) du Runtime .NET Core 1.0.10
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.9-linux-centos-x64-binaries) du Runtime .NET Core 1.0.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.8-linux-centos-x64-binaries) du Runtime .NET Core 1.0.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.7-linux-centos-x64-binaries) du Runtime .NET Core 1.0.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.5-linux-centos-x64-binaries) du Runtime .NET Core 1.0.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.0.4-linux-centos-x64-binaries) du Runtime .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.10-linux-centos-x64-binaries) du kit SDK .NET Core 1.1.10
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.9-linux-centos-x64-binaries) du kit SDK .NET Core 1.1.9
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.8-linux-centos-x64-binaries) du SDK .NET Core 1.1.8
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-centos-x64-binaries) du SDK .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.5-linux-centos-x64-binaries) du kit SDK .NET Core 1.1.5
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.4-linux-centos-x64-binaries) du kit SDK .NET Core 1.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-centos-x64-binaries) du SDK .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-centos-x64-binaries) du SDK .NET Core 1.0.1

---

## <a name="install-net-core-for-supported-suse-linux-enterprise-server-and-opensuse-distributionsversions-64-bit"></a>Installer .NET Core pour des versions/distributions (64 bits) prises en charge de SUSE Linux Enterprise Server et d’OpenSUSE

Pour installer .NET Core 2.x sur des versions/distributions (64 bits) prises en charge de SUSE Linux Enterprise Server et d’OpenSUSE :

# <a name="net-core-2xtabnetcore2x"></a>[.NET Core 2.x](#tab/netcore2x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 2.x sur des versions/distributions (64 bits) prises en charge de SUSE Linux Enterprise Server et d’OpenSUSE :

**.NET Core 2.0**

**SUSE Linux Enterprise Server**

* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.9) du Runtime .NET Core 2.0.9
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.8) du Runtime .NET Core 2.0.8
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.7) du Runtime .NET Core 2.0.7
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.6) du Runtime .NET Core 2.0.6
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.5) du Runtime .NET Core 2.0.5
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.3) du Runtime .NET Core 2.0.3
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.0.0) du Runtime .NET Core 2.0.0
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.202) du kit SDK .NET Core 2.1.202
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.201) du kit SDK .NET Core 2.1.201
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.200) du SDK .NET Core 2.1.200
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.105) du SDK .NET Core 2.1.105
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.104) du kit SDK .NET Core 2.1.104
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.103) du SDK .NET Core 2.1.103
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.102) du kit SDK .NET Core 2.1.102
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.101) du kit SDK .NET Core 2.1.101
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.100) du kit SDK .NET Core 2.1.100
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.4) du kit SDK .NET Core 2.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.2) du kit SDK .NET Core 2.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.0.3) du SDK .NET Core 2.0.3
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.0.0) du SDK .NET Core 2.0.0

**openSUSE**

* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.9) du Runtime .NET Core 2.0.9
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.8) du Runtime .NET Core 2.0.8
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.7) du Runtime .NET Core 2.0.7
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.6) du Runtime .NET Core 2.0.6
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.5) du Runtime .NET Core 2.0.5
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.3) du Runtime .NET Core 2.0.3
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.0.0) du Runtime .NET Core 2.0.0
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.202) du kit SDK .NET Core 2.1.202
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.201) du kit SDK .NET Core 2.1.201
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.200) du SDK .NET Core 2.1.200
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.105) du SDK .NET Core 2.1.105
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.103) du SDK .NET Core 2.1.103
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.102) du kit SDK .NET Core 2.1.102
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.101) du kit SDK .NET Core 2.1.101
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.100) du kit SDK .NET Core 2.1.100
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.4) du kit SDK .NET Core 2.1.4
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.2) du kit SDK .NET Core 2.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.0.3) du SDK .NET Core 2.0.3
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.0.0) du SDK .NET Core 2.0.0
 
**.NET Core 2.1**

>[!IMPORTANT]
> Pour utiliser .NET Core 2.1 avec Visual Studio, vous devez [installer Visual Studio 2017 15.7 ou version ultérieure](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017).

**SUSE Linux Enterprise Server**

* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.1.2) du Runtime .NET Core 2.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.400) du kit SDK .NET Core 2.1.400
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.302) du kit SDK .NET Core 2.1.302
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.1.1) du Runtime .NET Core 2.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.301) du kit SDK .NET Core 2.1.301
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/runtime-2.1.0) du Runtime .NET Core 2.1.0
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/sles/sdk-2.1.300) du SDK .NET Core 2.1.300

**openSUSE**

* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.1.2) du Runtime .NET Core 2.1.2
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.400) du kit SDK .NET Core 2.1.400
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.302) du kit SDK .NET Core 2.1.302
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.1.1) du Runtime .NET Core 2.1.1
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.301) du kit SDK .NET Core 2.1.301
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/runtime-2.1.0) du Runtime .NET Core 2.1.0
* [Lien d’installation](https://www.microsoft.com/net/download/linux-package-manager/opensuse/sdk-2.1.300) du SDK .NET Core 2.1.300

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

1. Supprimez du système toute **version antérieure** de .NET Core.

2. Installer .NET Core 1.x sur des versions/distributions (64 bits) prises en charge de SUSE Linux Enterprise Server et d’OpenSUSE :

**SUSE Linux Enterprise Server 13.2**

* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.7-linux-opensuse-13.2-x64-binaries) du Runtime .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-1.1.6-linux-opensuse-13.2-x64-binaries) du Runtime .NET Core 1.1.6
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.1.7-linux-opensuse-13.2-x64-binaries) du SDK .NET Core 1.1.7
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.4-linux-opensuse-13.2-x64-binaries) du SDK .NET Core 1.0.4
* [Lien d’installation](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-1.0.1-linux-opensuse-13.2-x64-binaries) du SDK .NET Core 1.0.1

---

## <a name="install-net-core-for-supported-alpine-linux-versions-64-bit"></a>Installer .NET Core pour des versions Alpine Linux prises en charge (64 bits)

> [!NOTE]
> Un répertoire contrôlé par l’utilisateur est requis pour les installations du système Linux système depuis tar.gz.

Téléchargez et suivez les instructions d’installation de .NET Core 2.1 pour les versions Alpine Linux prises en charge (64 bits) à l’aide des liens suivants :

* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.2-linux-x64-alpine-binaries) du Runtime .NET Core 2.1.2
* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.400-linux-x64-alpine-binaries) du kit SDK .NET Core 2.1.400
* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.302-linux-x64-alpine-binaries) du kit SDK .NET Core 2.1.302
* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.1-linux-x64-alpine-binaries) du Runtime .NET Core 2.1.1
* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.301-linux-x64-alpine-binaries) du kit SDK .NET Core 2.1.301
* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-runtime-2.1.0-linux-x64-alpine-binaries) du Runtime .NET Core 2.1.0
* [Lien de téléchargement](https://www.microsoft.com/net/download/thank-you/dotnet-sdk-2.1.300-linux-x64-alpine-binaries) du SDK .NET Core 2.1.300

> [!IMPORTANT]
> En cas de problème avec une installation de .NET Core sur une distribution/version de Linux prise en charge, consultez les rubriques suivantes correspondant à vos distributions/versions installées :
> * [Problèmes connus avec .NET Core 2.1](https://github.com/dotnet/core/tree/master/release-notes/2.1)
> * [Problèmes connus avec .NET Core 2.0](https://github.com/dotnet/core/tree/master/release-notes/2.0)
> * [Problèmes connus avec .NET Core 1.1](https://github.com/dotnet/core/blob/master/release-notes/1.1)
> * [Problèmes connus avec .NET Core 1.0](https://github.com/dotnet/core/blob/master/release-notes/1.0)
