---
title: Commande dotnet nuget push - Interface CLI .NET Core
description: La commande dotnet nuget push exécute un envoi (push) d’un package sur le serveur et le publie.
author: karann-msft
ms.author: mairaw
ms.date: 08/14/2017
ms.openlocfilehash: 090b11646a81859eeadb5fe9d36b43721fc70a5f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="dotnet-nuget-push"></a>dotnet nuget push

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet nuget push` - Exécute un push d’un package sur le serveur et le publie.

## <a name="synopsis"></a>Résumé

`dotnet nuget push [<ROOT>] [-s|--source] [-ss|--symbol-source] [-t|--timeout] [-k|--api-key] [-sk|--symbol-api-key] [-d|--disable-buffering] [-n|--no-symbols] [--force-english-output] [-h|--help]`

## <a name="description"></a>Description

La commande `dotnet nuget push` exécute un push d’un package sur le serveur et le publie. La commande push utilise les informations serveur et d’identification trouvées dans le fichier ou la chaîne de fichiers de configuration NuGet du système. Pour plus d’informations sur les fichiers de configuration, consultez [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior) (Configuration du comportement de NuGet ). La configuration par défaut de NuGet est obtenue en chargeant *%AppData%\NuGet\NuGet.config* (Windows) ou *$HOME/.local/share* (Linux/macOS), puis en chargeant tout fichier *nuget.config* ou *.nuget\nuget.config* à partir de la racine du lecteur jusqu’au répertoire actif.

## <a name="arguments"></a>Arguments

`ROOT`

Spécifie le chemin de fichier au package devant faire l’objet d’un envoi (push).

## <a name="options"></a>Options

`-h|--help`

Affiche une aide brève pour la commande.

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.

`--symbol-source <SOURCE>`

Spécifie l’URL du serveur de symboles.

`-t|--timeout <TIMEOUT>`

Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur. La valeur par défaut est 300 secondes (5 minutes). Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`--symbol-api-key <API_KEY>`

Clé d’API pour le serveur de symboles.

`-d|--disable-buffering`

Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.

`-n|--no-symbols`

N’envoie pas les symboles (même s’ils sont présents).

`--force-english-output`

Force toutes les sorties enregistrées à être en anglais.

## <a name="examples"></a>Exemples

Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut, en fournissant une clé API :

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

Effectuer une transmission de type push de *foo.nupkg* vers la source de push personnalisée `http://customsource`, en fournissant une clé API :

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s http://customsource/`

Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut :

`dotnet nuget push foo.nupkg`

Effectuer une transmission de type push de *foo.symbols.nupkg* vers la source de symboles par défaut :

`dotnet nuget push foo.symbols.nupkg`

Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut, en spécifiant un délai d’attente de 360 secondes :

`dotnet nuget push foo.nupkg --timeout 360`

Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut :

`dotnet nuget push *.nupkg`

Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut, en spécifiant un fichier de configuration personnalisé *./config/My.Config* :

`dotnet nuget push *.nupkg --config-file ./config/My.Config`
