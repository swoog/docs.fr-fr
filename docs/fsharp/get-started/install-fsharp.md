---
title: InstallerF#
description: Découvrez comment installer F# en fonction de votre environnement.
ms.date: 08/28/2018
ms.openlocfilehash: 792c61c0522cd4d0c68a64572f2892ce33f71ea6
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59331973"
---
# <a name="install-f"></a>Installer F\#

Vous pouvez installer F# de plusieurs façons, selon votre environnement.

## <a name="install-f-with-visual-studio"></a>Installer F# avec Visual Studio

Si vous effectuez un téléchargement [Visual Studio](https://visualstudio.microsoft.com/vs/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link) pour la première fois, il installera d’abord le programme d’installation de Visual Studio. Installez la référence SKU appropriée de Visual Studio à partir du programme d’installation. Si vous avez déjà installé, cliquez sur **modifier**.

Vous verrez ensuite une liste de charges de travail. Sélectionnez **ASP.NET et développement web** qui installera F# prise en charge et .NET Core prend en charge pour les projets ASP.NET Core.

Ensuite, cliquez sur **modifier** dans l’angle inférieur droit.  Cela installera tout ce dont vous avez sélectionné. Vous pouvez ensuite ouvrir Visual Studio 2017 avec F# prise en charge de la langue en cliquant sur **lancer**.

## <a name="install-f-with-visual-studio-for-mac"></a>Installer F# avec Visual Studio pour Mac

F#est installé par défaut dans [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link), quelle que soit la configuration que vous choisissez.

Une fois l’installation terminée, cliquez sur « Démarrer Visual Studio ». Vous pouvez également la lancer via Finder sur macOS.

## <a name="install-f-with-visual-studio-code"></a>Installer F# avec Visual Studio Code

Vous devez avoir [git installé](https://git-scm.com/download) et disponible sur votre chemin d’accès s’utiliser des modèles de projet. Vous pouvez vérifier qu’il est correctement installé en tapant `git --version` à l’invite de commandes et en appuyant sur **entrée**.

### [<a name="macos"></a>macOS](#tab/macos)

[Mono](https://www.mono-project.com) est utilisé pour [ F# Interactive](../tutorials/fsharp-interactive/index.md) prennent en charge. Le moyen le plus simple pour installer Mono sur macOS est via Homebrew. Tapez simplement la commande suivante dans votre terminal :

```console
brew install mono
```

Installez également le [du SDK .NET Core](https://www.microsoft.com/net/download).

### [<a name="linux"></a>Linux](#tab/linux)

[Mono](https://www.mono-project.com) est utilisé pour [ F# Interactive](../tutorials/fsharp-interactive/index.md) prennent en charge. Si vous êtes sur Debian ou Ubuntu, vous pouvez utiliser les éléments suivants :

```console
sudo apt-get update
sudo apt-get install mono-complete fsharp
```

Installez également le [du SDK .NET Core](https://www.microsoft.com/net/download).

### [<a name="windows"></a>Windows](#tab/windows)

Installer [Visual Studio avec F# prennent en charge](#install-f-with-visual-studio). Cette opération installe tous les composants nécessaires pour écrire, compiler et exécuter F# code.

Installez également le [du SDK .NET Core](https://www.microsoft.com/net/download/).

---

Vous devez ensuite [Visual Studio Code](https://code.visualstudio.com) installé.

Ensuite, cliquez sur l’icône des Extensions et recherchez « Ionide » :

Le plug-in uniquement requis pour F# est prise en charge dans Visual Studio Code [Ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp). Toutefois, vous pouvez également installer [Ionide-FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) pour obtenir [fictif](https://fsharp.github.io/FAKE/) prennent en charge et [Ionide-Paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) pour obtenir [Paket](https://fsprojects.github.io/Paket/) prennent en charge. FALSIFIER et Paket sont supplémentaires F# outils de la Communauté pour la création de projets et de gestion des dépendances, respectivement.
