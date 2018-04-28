---
title: Commande dotnet nuget push - Interface CLI .NET Core
description: La commande dotnet nuget push exécute un envoi (push) d’un package sur le serveur et le publie.
author: karann-msft
ms.author: mairaw
ms.date: 08/14/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.workload:
- dotnetcore
ms.openlocfilehash: 29bc05c42bff9ace3fac2328ba44e15e4746e10e
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="dotnet-nuget-push"></a><span data-ttu-id="73291-103">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="73291-103">dotnet nuget push</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="73291-104">Name</span><span class="sxs-lookup"><span data-stu-id="73291-104">Name</span></span>

<span data-ttu-id="73291-105">`dotnet nuget push` - Exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="73291-105">`dotnet nuget push` - Pushes a package to the server and publishes it.</span></span>

## <a name="synopsis"></a><span data-ttu-id="73291-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="73291-106">Synopsis</span></span>

`dotnet nuget push [<ROOT>] [-s|--source] [-ss|--symbol-source] [-t|--timeout] [-k|--api-key] [-sk|--symbol-api-key] [-d|--disable-buffering] [-n|--no-symbols] [--force-english-output] [-h|--help]`

## <a name="description"></a><span data-ttu-id="73291-107">Description</span><span class="sxs-lookup"><span data-stu-id="73291-107">Description</span></span>

<span data-ttu-id="73291-108">La commande `dotnet nuget push` exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="73291-108">The `dotnet nuget push` command pushes a package to the server and publishes it.</span></span> <span data-ttu-id="73291-109">La commande push utilise les informations serveur et d’identification trouvées dans le fichier ou la chaîne de fichiers de configuration NuGet du système.</span><span class="sxs-lookup"><span data-stu-id="73291-109">The push command uses server and credential details found in the system's NuGet config file or chain of config files.</span></span> <span data-ttu-id="73291-110">Pour plus d’informations sur les fichiers de configuration, consultez [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior) (Configuration du comportement de NuGet ).</span><span class="sxs-lookup"><span data-stu-id="73291-110">For more information on config files, see [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior).</span></span> <span data-ttu-id="73291-111">La configuration par défaut de NuGet est obtenue en chargeant *%AppData%\NuGet\NuGet.config* (Windows) ou *$HOME/.local/share* (Linux/macOS), puis en chargeant tout fichier *nuget.config* ou *.nuget\nuget.config* à partir de la racine du lecteur jusqu’au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="73291-111">NuGet's default configuration is obtained by loading *%AppData%\NuGet\NuGet.config* (Windows) or *$HOME/.local/share* (Linux/macOS), then loading any *nuget.config* or *.nuget\nuget.config* starting from the root of drive and ending in the current directory.</span></span>

## <a name="arguments"></a><span data-ttu-id="73291-112">Arguments</span><span class="sxs-lookup"><span data-stu-id="73291-112">Arguments</span></span>

`ROOT`

<span data-ttu-id="73291-113">Spécifie le chemin de fichier au package devant faire l’objet d’un envoi (push).</span><span class="sxs-lookup"><span data-stu-id="73291-113">Specifies the file path to the package to be pushed.</span></span>

## <a name="options"></a><span data-ttu-id="73291-114">Options</span><span class="sxs-lookup"><span data-stu-id="73291-114">Options</span></span>

`-h|--help`

<span data-ttu-id="73291-115">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="73291-115">Prints out a short help for the command.</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="73291-116">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="73291-116">Specifies the server URL.</span></span> <span data-ttu-id="73291-117">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="73291-117">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`--symbol-source <SOURCE>`

<span data-ttu-id="73291-118">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="73291-118">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="73291-119">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="73291-119">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="73291-120">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="73291-120">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="73291-121">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="73291-121">Specifying 0 (zero seconds) applies the default value.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="73291-122">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="73291-122">The API key for the server.</span></span>

`--symbol-api-key <API_KEY>`

<span data-ttu-id="73291-123">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="73291-123">The API key for the symbol server.</span></span>

`-d|--disable-buffering`

<span data-ttu-id="73291-124">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="73291-124">Disables buffering when pushing to an HTTP(S) server to decrease memory usage.</span></span>

`-n|--no-symbols`

<span data-ttu-id="73291-125">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="73291-125">Doesn't push symbols (even if present).</span></span>

`--force-english-output`

<span data-ttu-id="73291-126">Force toutes les sorties enregistrées à être en anglais.</span><span class="sxs-lookup"><span data-stu-id="73291-126">Forces all logged output in English.</span></span>

## <a name="examples"></a><span data-ttu-id="73291-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="73291-127">Examples</span></span>

<span data-ttu-id="73291-128">Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut, en fournissant une clé API :</span><span class="sxs-lookup"><span data-stu-id="73291-128">Pushes *foo.nupkg* to the default push source, providing an API key:</span></span>

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

<span data-ttu-id="73291-129">Effectuer une transmission de type push de *foo.nupkg* vers la source de push personnalisée `http://customsource`, en fournissant une clé API :</span><span class="sxs-lookup"><span data-stu-id="73291-129">Push *foo.nupkg* to the custom push source `http://customsource`, providing an API key:</span></span>

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s http://customsource/`

<span data-ttu-id="73291-130">Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="73291-130">Pushes *foo.nupkg* to the default push source:</span></span>

`dotnet nuget push foo.nupkg`

<span data-ttu-id="73291-131">Effectuer une transmission de type push de *foo.symbols.nupkg* vers la source de symboles par défaut :</span><span class="sxs-lookup"><span data-stu-id="73291-131">Pushes *foo.symbols.nupkg* to the default symbols source:</span></span>

`dotnet nuget push foo.symbols.nupkg`

<span data-ttu-id="73291-132">Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut, en spécifiant un délai d’attente de 360 secondes :</span><span class="sxs-lookup"><span data-stu-id="73291-132">Pushes *foo.nupkg* to the default push source, specifying a 360 second timeout:</span></span>

`dotnet nuget push foo.nupkg --timeout 360`

<span data-ttu-id="73291-133">Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="73291-133">Pushes all *.nupkg* files in the current directory to the default push source:</span></span>

`dotnet nuget push *.nupkg`

<span data-ttu-id="73291-134">Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut, en spécifiant un fichier de configuration personnalisé *./config/My.Config* :</span><span class="sxs-lookup"><span data-stu-id="73291-134">Pushes all *.nupkg* files in the current directory to the default push source, specifying a custom config file *./config/My.Config*:</span></span>

`dotnet nuget push *.nupkg --config-file ./config/My.Config`
