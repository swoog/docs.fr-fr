---
title: 'À l’aide de la gestion des packages avec F # pour Azure'
description: 'Permet de gérer les dépendances de F # Azure Paket ou Nuget'
author: sylvanc
ms.date: 09/20/2016
ms.openlocfilehash: fd9c4a15ab0741d44d6d5cf909b7219d310affb0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33566967"
---
# <a name="package-management-for-f-azure-dependencies"></a>Gestion des packages pour les dépendances F# Azure

Il est facile d’obtention de packages pour le développement Azure lorsque vous utilisez un gestionnaire de package. Les deux options sont [Paket](https://fsprojects.github.io/Paket/) et [NuGet](https://www.nuget.org/).

## <a name="using-paket"></a>À l’aide de Paket

Si vous utilisez [Paket](https://fsprojects.github.io/Paket/) comme gestionnaire de dépendance, vous pouvez utiliser la `paket.exe` outil pour ajouter des dépendances Azure. Par exemple :

    > paket add nuget WindowsAzure.Storage

Ou, si vous utilisez [Mono](https://www.mono-project.com/) pour le développement d’inter-plateformes .NET :

    > mono paket.exe add nuget WindowsAzure.Storage

Cela ajoutera `WindowsAzure.Storage` à votre jeu de dépendances de package pour le projet dans le répertoire actif, vous devez modifier le `paket.dependencies` de fichiers et de télécharger le package. Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :

    > paket install

Ou, pour le développement Mono :

    > mono paket.exe install

Vous pouvez mettre à jour toutes les dépendances de votre package vers la dernière version à ceci :

    > paket update

Ou, pour le développement Mono :

    > mono paket.exe update

## <a name="using-nuget"></a>À l’aide de Nuget

Si vous utilisez [NuGet](https://www.nuget.org/) comme gestionnaire de dépendance, vous pouvez utiliser la `nuget.exe` outil pour ajouter des dépendances Azure. Par exemple :

    > nuget install WindowsAzure.Storage -ExcludeVersion

Ou, pour le développement Mono :

    > mono nuget.exe install WindowsAzure.Storage -ExcludeVersion

Cela ajoutera `WindowsAzure.Storage` à votre jeu de dépendances de package pour le projet dans le répertoire actif et téléchargez le package. Si vous avez configuré précédemment des dépendances, ou que vous travaillez avec un projet où les dépendances ont été définis par un autre développeur, vous pouvez résoudre et installer des dépendances localement comme suit :

    > nuget restore 

Ou, pour le développement Mono :

    > mono nuget.exe restore

Vous pouvez mettre à jour toutes les dépendances de votre package vers la dernière version à ceci :

    > nuget update

Ou, pour le développement Mono :

    > mono nuget.exe update

## <a name="referencing-assemblies"></a>Référencement d'assemblys

Pour utiliser vos packages dans votre script F #, vous devez référencer les assemblys inclus dans les packages à l’aide un `#r` la directive. Par exemple :

    > #r "packages/WindowsAzure.Storage/lib/net40/Microsoft.WindowsAzure.Storage.dll"

Comme vous pouvez le voir, vous devez spécifier le chemin d’accès relatif à la DLL et le nom complet de la DLL, qui peut ne pas être exactement le même que le nom du package. Le chemin d’accès inclut une version du framework et éventuellement un numéro de version du package. Pour rechercher tous les assemblys installés, vous pouvez utiliser quelque chose comme ceci sur une ligne de commande de Windows :

    > cd packages/WindowsAzure.Storage
    > dir /s/b *.dll

Ou dans un interpréteur de commandes Unix, quelque chose comme ceci :

    > find packages/WindowsAzure.Storage -name "*.dll"

Cela vous donne les chemins d’accès vers les assemblys installés. À partir de là, vous pouvez sélectionner le chemin d’accès approprié pour votre version de framework.
