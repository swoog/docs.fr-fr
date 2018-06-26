---
title: Commande dotnet nuget push - Interface CLI .NET Core
description: La commande dotnet nuget push exécute un envoi (push) d’un package sur le serveur et le publie.
author: karann-msft
ms.author: mairaw
ms.date: 06/01/2018
ms.openlocfilehash: 8a64f9cdc11d03bed82a132265c3b4e1de290807
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34728574"
---
# <a name="dotnet-nuget-push"></a>dotnet nuget push

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet nuget push` - Exécute un push d’un package sur le serveur et le publie.

## <a name="synopsis"></a>Résumé

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [--no-service-endpoint] [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
---

## <a name="description"></a>Description

La commande `dotnet nuget push` exécute un push d’un package sur le serveur et le publie. La commande push utilise les informations serveur et d’identification trouvées dans le fichier ou la chaîne de fichiers de configuration NuGet du système. Pour plus d’informations sur les fichiers de configuration, consultez [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior) (Configuration du comportement de NuGet ). La configuration par défaut de NuGet est obtenue en chargeant *%AppData%\NuGet\NuGet.config* (Windows) ou *$HOME/.local/share* (Linux/macOS), puis en chargeant tout fichier *nuget.config* ou *.nuget\nuget.config* à partir de la racine du lecteur jusqu’au répertoire actif.

## <a name="arguments"></a>Arguments

`ROOT`

Spécifie le chemin de fichier au package devant faire l’objet d’un envoi (push).

## <a name="options"></a>Options

# <a name="net-core-21tabnetcore21"></a>[.NET Core 2.1](#tab/netcore21)

`-d|--disable-buffering`

Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.

`--force-english-output`

Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

`-h|--help`

Affiche une aide brève pour la commande.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`-n|--no-symbols`

N’envoie pas les symboles (même s’ils sont présents).

`--no-service-endpoint`

N’ajoute pas « api/v2/package » à l’URL source.

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.

`-sk|--symbol-api-key <API_KEY>`

Clé d’API pour le serveur de symboles.

`-ss|--symbol-source <SOURCE>`

Spécifie l’URL du serveur de symboles.

`-t|--timeout <TIMEOUT>`

Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur. La valeur par défaut est 300 secondes (5 minutes). Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.

# <a name="net-core-20tabnetcore20"></a>[.NET Core 2.0](#tab/netcore20)

`-d|--disable-buffering`

Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.

`--force-english-output`

Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

`-h|--help`

Affiche une aide brève pour la commande.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`-n|--no-symbols`

N’envoie pas les symboles (même s’ils sont présents).

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.

`-sk|--symbol-api-key <API_KEY>`

Clé d’API pour le serveur de symboles.

`-ss|--symbol-source <SOURCE>`

Spécifie l’URL du serveur de symboles.

`-t|--timeout <TIMEOUT>`

Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur. La valeur par défaut est 300 secondes (5 minutes). Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.

# <a name="net-core-1xtabnetcore1x"></a>[.NET Core 1.x](#tab/netcore1x)

`-d|--disable-buffering`

Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.

`--force-english-output`

Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).

`-h|--help`

Affiche une aide brève pour la commande.

`-k|--api-key <API_KEY>`

Clé d’API pour le serveur.

`-n|--no-symbols`

N’envoie pas les symboles (même s’ils sont présents).

`-s|--source <SOURCE>`

Spécifie l’URL du serveur. Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.

`-sk|--symbol-api-key <API_KEY>`

Clé d’API pour le serveur de symboles.

`-ss|--symbol-source <SOURCE>`

Spécifie l’URL du serveur de symboles.

`-t|--timeout <TIMEOUT>`

Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur. La valeur par défaut est 300 secondes (5 minutes). Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.

---

## <a name="examples"></a>Exemples

Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant une clé API :

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

Envoyez (push) *foo.nupkg* à la source de push personnalisée `http://customsource`, en spécifiant une clé API :

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s http://customsource/`

Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut :

`dotnet nuget push foo.nupkg`

Effectuer une transmission de type push de *foo.symbols.nupkg* vers la source de symboles par défaut :

`dotnet nuget push foo.symbols.nupkg`

Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant un délai d’attente de 360 secondes :

`dotnet nuget push foo.nupkg --timeout 360`

Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut :

`dotnet nuget push *.nupkg`

Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut, en spécifiant un fichier de configuration personnalisé *./config/My.Config* :

`dotnet nuget push *.nupkg --config-file ./config/My.Config`
