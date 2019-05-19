---
title: À l’aide de la gestion des packages avec F# pour Azure
description: Permet de gérer Paket ou Nuget F# dépendances Azure
author: sylvanc
ms.date: 09/20/2016
ms.openlocfilehash: b180024e2276a2fd7786f35cb922b1aa1d91f0ad
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65880017"
---
# <a name="package-management-for-f-azure-dependencies"></a>Gestion des packages pour les dépendances F# Azure

Il est facile d’obtenir des packages pour le développement Azure lorsque vous utilisez un gestionnaire de package. Les deux options sont [Paket](https://fsprojects.github.io/Paket/) et [NuGet](https://www.nuget.org/).

## <a name="using-paket"></a>À l’aide de Paket

Si vous utilisez [Paket](https://fsprojects.github.io/Paket/) en tant que votre gestionnaire de dépendances, vous pouvez utiliser le `paket.exe` outil pour ajouter des dépendances Azure. Exemple :

```
> paket add nuget WindowsAzure.Storage
```

Ou, si vous utilisez [Mono](https://www.mono-project.com/) pour le développement multiplateforme .NET :

```
> mono paket.exe add nuget WindowsAzure.Storage
```

Cela ajoutera `WindowsAzure.Storage` dans votre jeu de dépendances de package pour le projet dans le répertoire actif, vous devez modifier le `paket.dependencies` de fichier et téléchargez le package. Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :

```
> paket install
```

Ou, pour le développement Mono :

```
> mono paket.exe install
```

Vous pouvez mettre à jour toutes vos dépendances de package vers la dernière version comme suit :

```
> paket update
```

Ou, pour le développement Mono :

```
> mono paket.exe update
```

## <a name="using-nuget"></a>À l’aide de Nuget

Si vous utilisez [NuGet](https://www.nuget.org/) en tant que votre gestionnaire de dépendances, vous pouvez utiliser le `nuget.exe` outil pour ajouter des dépendances Azure. Exemple :

```
> nuget install WindowsAzure.Storage -ExcludeVersion
```

Ou, pour le développement Mono :

```
> mono nuget.exe install WindowsAzure.Storage -ExcludeVersion
```

Cela ajoutera `WindowsAzure.Storage` dans votre jeu de dépendances de package pour le projet dans le répertoire actif et le téléchargement du package. Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :

```
> nuget restore
```

Ou, pour le développement Mono :

```
> mono nuget.exe restore
```

Vous pouvez mettre à jour toutes vos dépendances de package vers la dernière version comme suit :

```
> nuget update
```

Ou, pour le développement Mono :

```
> mono nuget.exe update
```

## <a name="referencing-assemblies"></a>Référencement d'assemblys

Pour pouvoir utiliser vos packages dans votre F# script, vous devez référencer les assemblys inclus dans les packages en utilisant un `#r` directive. Exemple :

```
> #r "packages/WindowsAzure.Storage/lib/net40/Microsoft.WindowsAzure.Storage.dll"
```

Comme vous pouvez le voir, vous devez spécifier le chemin d’accès relatif à la DLL et le nom complet de la DLL, qui ne peut être exactement le même que le nom du package. Le chemin d’accès inclut une version de framework et éventuellement un numéro de version du package. Pour rechercher tous les assemblys installés, vous pouvez utiliser quelque chose comme ceci sur une ligne de commande de Windows :

```
> cd packages/WindowsAzure.Storage
> dir /s/b *.dll
```

Ou dans un interpréteur de commandes Unix, quelque chose comme ceci :

```
> find packages/WindowsAzure.Storage -name "*.dll"
```

Cela vous donnera les chemins d’accès aux assemblys installés. À partir de là, vous pouvez sélectionner le chemin d’accès correct pour votre version de framework.
