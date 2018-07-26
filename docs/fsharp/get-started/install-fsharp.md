---
title: 'Installer F #'
description: 'Découvrez comment installer F # en fonction de votre environnement.'
ms.date: 07/03/2018
ms.openlocfilehash: 142265a95e1d3ee1603a89f650a24c6a45709181
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37878844"
---
# <a name="install-f"></a>Installer F # #

Vous pouvez installer F # de plusieurs façons, selon votre environnement.

## <a name="install-f-with-visual-studio"></a>Installer F # avec Visual Studio

Si vous effectuez un téléchargement [Visual Studio](https://visualstudio.microsoft.com/) pour la première fois, il installera d’abord le programme d’installation de Visual Studio. Installez la référence SKU appropriée de Visual Studio à partir du programme d’installation. Si vous avez déjà installé, cliquez sur **modifier**.

Vous verrez ensuite une liste de charges de travail. Sélectionnez **ASP.NET et développement web**, qui installe F # prise en charge, prise en charge .NET Core, et les projets F # prise en charge pour ASP.NET Core.

Ensuite, cliquez sur **modifier** dans l’angle inférieur droit.  Cela installera tout ce dont vous avez sélectionné. Vous pouvez ensuite ouvrir Visual Studio 2017 avec prise en charge de langage F # en cliquant sur **lancer**.

## <a name="install-f-with-visual-studio-for-mac"></a>Installer F # avec Visual Studio pour Mac

F # est installé par défaut dans [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/mac/), quelle que soit la configuration que vous choisissez.

Une fois l’installation terminée, cliquez sur « Démarrer Visual Studio ». Vous pouvez également la lancer via Finder sur macOS.

## <a name="install-f-with-visual-studio-code"></a>Installer F # avec Visual Studio Code

Vous devez avoir [git installé](https://git-scm.com/download) et disponible sur votre chemin d’accès s’utiliser des modèles de projet Ionide. Vous pouvez vérifier qu’il est correctement installé en tapant `git --version` à l’invite de commandes et en appuyant sur **entrée**.

### <a name="macostabmacos"></a>[macOS](#tab/macos)

Utilise Ionide [Mono](http://www.mono-project.com). Le moyen le plus simple pour installer Mono sur macOS est via Homebrew. Tapez simplement la commande suivante dans votre terminal :

```console
brew install mono
```

Vous devez également installer le [du SDK .NET Core](https://www.microsoft.com/net/download).

### <a name="linuxtablinux"></a>[Linux](#tab/linux)

Sur Linux, Ionide utilise également [Mono](https://www.mono-project.com). Si vous êtes sur Debian ou Ubuntu, vous pouvez utiliser les éléments suivants :

```console
sudo apt-get update
sudo apt-get install mono-complete fsharp
```

Vous devez également installer le [du SDK .NET Core](https://www.microsoft.com/net/download).

### <a name="windowstabwindows"></a>[Windows](#tab/windows)

Si vous êtes sur Windows, vous devez [installer Visual Studio avec prise en charge F #](#install-f-with-visual-studio). Cette opération installe tous les composants nécessaires pour écrire, compiler et exécuter du code F #.

Vous devez également installer le [du SDK .NET Core](https://www.microsoft.com/net/download/).

---

Vous devez ensuite [Visual Studio Code](https://code.visualstudio.com) installé.

Ensuite, cliquez sur l’icône des Extensions et recherchez « Ionide » :

Le plug-in uniquement requis pour la prise en charge F # dans Visual Studio Code est [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp). Toutefois, vous pouvez également installer [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) pour obtenir [fictif](https://fsharp.github.io/FAKE/) prennent en charge et [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) pour obtenir [Paket](https://fsprojects.github.io/Paket/) prennent en charge. FALSIFIER et Paket sont F # Communauté des outils supplémentaires pour la création de projets et de gestion des dépendances, respectivement.