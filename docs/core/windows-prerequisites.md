---
title: Configuration requise pour .NET Core sur Windows
description: Découvrez les dépendances nécessaires sur votre machine Windows pour développer et exécuter des applications .NET Core.
author: mairaw
ms.author: mairaw
ms.date: 08/31/2018
ms.openlocfilehash: 63c0de2b413f38458dba89506f4070760b3f53f8
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45747466"
---
# <a name="prerequisites-for-net-core-on-windows"></a>Configuration requise pour .NET Core sur Windows

Cet article montre les dépendances nécessaires pour développer des applications .NET Core sur Windows. Les versions de système d’exploitation et les dépendances prises en charge ci-après s’appliquent aux trois façons de développer des applications .NET Core sur Windows :

* [Ligne de commande](tutorials/using-with-xplat-cli.md)
* [Visual Studio 2017](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)
* [Visual Studio Code](https://code.visualstudio.com/)

## <a name="net-core-supported-windows-versions"></a>Versions Windows prises en charge par .NET Core

.NET Core est pris en charge par les versions suivantes de :

* Windows 7 SP1
* Windows 8.1
* Mise à jour anniversaire Windows 10 (version 1607) ou ultérieur
* Windows Server 2008 R2 SP1 (version complète ou Server Core)
* Windows Server 2012 SP1 (version complète ou Server Core)
* Windows Server 2012 R2 (version complète ou Server Core)
* Windows Server 2016 ou versions ultérieures (version complète, Server Core ou Nano Server)

## <a name="net-core-supported-operating-systems"></a>Systèmes d’exploitation pris en charge par .NET Core

Les articles suivants dressent la liste complète des systèmes d’exploitation .NET Core pris en charge par version :

* [.NET Core 2.1 - Versions de système d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md)
* [.NET Core 2.0 - Versions de système d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/2.0/2.0-supported-os.md)
* [.NET Core 1.x - Versions de système d’exploitation prises en charge](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md)

## <a name="net-core-dependencies"></a>Dépendances .NET Core

.NET Core 1.1 et ses versions antérieures nécessitent le package redistribuable Visual C++ lors de l’exécution sur des versions de Windows antérieures à Windows 10 et Windows Server 2016. Cette dépendance est installée automatiquement par le programme d’installation de .NET Core.

Vous devez installer [Microsoft Visual C++ 2015 Redistributable Update 3](https://www.microsoft.com/download/details.aspx?id=52685) manuellement quand :

* vous installez .NET Core avec le [script du programme d’installation](./tools/dotnet-install-script.md) ;
* vous déployez une application .NET Core autonome.
* Génération du produit à partir de la source.
* Installation de .NET Core via un fichier *.zip*. Ceci peut inclure des serveurs de builds/CI/CD.

> [!NOTE]
> **Pour Windows 8.1 et versions antérieures, ou Windows Server 2012 R2 et versions antérieures :**
>
> Vérifiez que votre installation Windows est à jour et comprend le correctif logiciel [KB2999226](https://support.microsoft.com/en-us/help/2999226/update-for-universal-c-runtime-in-windows), installable via Windows Update. Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur semblable à celle-ci : `The program can't start because api-ms-win-crt-runtime-1-1-0.dll is missing from your computer. Try reinstalling the program to fix this problem.`
>
> **Pour Windows 7 ou Windows Server 2008 R2 :**
>
> Outre KB2999226, vérifiez également que la mise à jour [KB2533623](https://support.microsoft.com/en-us/help/2533623/microsoft-security-advisory-insecure-library-loading-could-allow-remot) est installée. Si cette mise à jour n’est pas installée, quand vous lancez une application .NET Core, vous recevez une erreur comme celle-ci : `The library hostfxr.dll was found, but loading it from C:\<path_to_app>\hostfxr.dll failed`.

## <a name="prerequisites-with-visual-studio-2017"></a>Prérequis pour Visual Studio 2017

Vous pouvez utiliser l’éditeur de votre choix pour développer des applications .NET Core à l’aide du Kit SDK .NET Core. Visual Studio 2017 fournit un environnement de développement intégré pour les applications .NET Core sur Windows.

Vous trouverez plus d’informations sur les modifications apportées à Visual Studio 2017 dans les [notes de publication](/visualstudio/releasenotes/vs2017-relnotes).

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)

Pour développer des applications .NET Core 2.1 dans Visual Studio 2017 :

 1. [Téléchargez et installez Visual Studio 2017 version 15.7.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-8-workloads.jpg)

Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, par défaut, Visual Studio 2017 15.7 utilise le SDK .NET Core 2.0, et Visual Studio 2017 15.8 utilise le SDK 2.1.

 2. Si vous utilisez Visual Studio 2017 15.7, installez le [SDK .NET Core 2.1](https://www.microsoft.com/net/download/core) ou effectuez la mise à niveau vers Visual Studio 2017 15.8.

 3. Reciblez vos projets .NET Core existants ou nouveaux vers .NET Core 2.1 en vous aidant des instructions suivantes :
    * Dans le menu **Projet**, choisissez **Propriétés**.
    * Dans le menu de sélection du **framework cible**, choisissez **.NET Core 2.1**.

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

Une fois que vous avez configuré Visual Studio avec le SDK .NET Core 2.1, vous pouvez effectuer les actions suivantes :

* Ouvrir, générer et exécuter les projets .NET Core 1.x et 2.x existants.
* Recibler les projets .NET Core 1.x et 2.0 vers .NET Core 2.1, les générer et les exécuter.
* Créer des projets .NET Core 2.1.

# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)

Pour développer des applications .NET Core 2.0 dans Visual Studio 2017 :

 1. [Téléchargez et installez Visual Studio 2017 version 15.3.0 ou version ultérieure](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs-15-3-workloads.jpg)

Une fois installé l’ensemble d’outils **Développement multiplateforme .NET Core**, Visual Studio 2017 utilise .NET Core 1.x par défaut. Installez le SDK .NET Core 2.0 pour bénéficier de la prise en charge de .NET Core 2.0 dans Visual Studio 2017.

 2. Installez le [SDK .NET Core 2.0](https://www.microsoft.com/net/download/dotnet-core/2.0).
 3. Reciblez vos projets .NET Core 1.x existants ou nouveaux vers .NET Core 2.0 en vous aidant des instructions suivantes :
    * Dans le menu **Projet**, choisissez **Propriétés**.
    * Dans le menu de sélection **framework cible**, choisissez **.NET Core 2.0**.

![Capture d’écran de la propriété de projet Application Visual Studio 2017 avec définition de l’élément de menu framework cible sur « .NET Core 2.0 »](./media/windows-prerequisites/Targeting-dotnetCore2.png)

Une fois le SDK .NET Core 2.0 installé, Visual Studio 2017 l’utilise par défaut et prend en charge les actions suivantes :

* Ouvrir, générer et exécuter les projets .NET Core 1.x existants.
* Recibler les projets .NET Core 1.x vers .NET Core 2.0, les générer et les exécuter.
* Créer des projets .NET Core 2.0.

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

Pur développer des applications .NET Core 1.x dans Visual Studio, [téléchargez et installez Visual Studio 2017](/visualstudio/install/install-visual-studio) en sélectionnant la charge de travail **Développement multiplateforme .NET Core** (dans la section **Autres ensembles d’outils**).

![Capture d’écran de l’installation de Visual Studio 2017 avec la charge de travail « Développement multiplateforme .NET Core » sélectionnée](./media/windows-prerequisites/vs_workloads.jpg)

> [!IMPORTANT]
> Bien que vous puissiez utiliser Visual Studio 2015 pour le développement .NET Core 1.x, nous vous le déconseillons pour les raisons suivantes :
  > * Les outils .NET Core sont une préversion, qui n’est pas prise en charge.
  > * Les projets sont basés sur project.json, configuration qui est dépréciée.
>
> Pour plus d’informations sur les changements de format de projet, consultez la page [Vue d’ensemble des modifications](./tools/cli-msbuild-architecture.md).
---

<a name="vs-mapping"></a>

> [!TIP]
> Pour vérifier votre version de Visual Studio 2017 :
>
> * Dans le menu **Aide**, choisissez **À propos de Microsoft Visual Studio**.
> * Dans la boîte de dialogue **À propos de Microsoft Visual Studio**, vérifiez le numéro de version.
>   * Pour les applications .NET Core 2.2 Preview 1, Visual Studio 2017 version 15.9 (disponible en préversion) ou une version ultérieure.
>   * Pour les applications .NET Core 2.1, Visual Studio 2017 version 15.7 ou ultérieure.
>   * Pour les applications .NET Core 2.0, Visual Studio 2017 version 15.3 ou ultérieure.
>   * Pour les applications .NET Core 1.x, Visual Studio 2017 version 15.0 ou ultérieure.
