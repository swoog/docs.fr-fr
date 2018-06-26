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
# <a name="dotnet-nuget-push"></a><span data-ttu-id="657b5-103">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="657b5-103">dotnet nuget push</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="657b5-104">Name</span><span class="sxs-lookup"><span data-stu-id="657b5-104">Name</span></span>

<span data-ttu-id="657b5-105">`dotnet nuget push` - Exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="657b5-105">`dotnet nuget push` - Pushes a package to the server and publishes it.</span></span>

## <a name="synopsis"></a><span data-ttu-id="657b5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="657b5-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="657b5-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="657b5-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [--no-service-endpoint] [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="657b5-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="657b5-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="657b5-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="657b5-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="657b5-110">Description</span><span class="sxs-lookup"><span data-stu-id="657b5-110">Description</span></span>

<span data-ttu-id="657b5-111">La commande `dotnet nuget push` exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="657b5-111">The `dotnet nuget push` command pushes a package to the server and publishes it.</span></span> <span data-ttu-id="657b5-112">La commande push utilise les informations serveur et d’identification trouvées dans le fichier ou la chaîne de fichiers de configuration NuGet du système.</span><span class="sxs-lookup"><span data-stu-id="657b5-112">The push command uses server and credential details found in the system's NuGet config file or chain of config files.</span></span> <span data-ttu-id="657b5-113">Pour plus d’informations sur les fichiers de configuration, consultez [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior) (Configuration du comportement de NuGet ).</span><span class="sxs-lookup"><span data-stu-id="657b5-113">For more information on config files, see [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior).</span></span> <span data-ttu-id="657b5-114">La configuration par défaut de NuGet est obtenue en chargeant *%AppData%\NuGet\NuGet.config* (Windows) ou *$HOME/.local/share* (Linux/macOS), puis en chargeant tout fichier *nuget.config* ou *.nuget\nuget.config* à partir de la racine du lecteur jusqu’au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="657b5-114">NuGet's default configuration is obtained by loading *%AppData%\NuGet\NuGet.config* (Windows) or *$HOME/.local/share* (Linux/macOS), then loading any *nuget.config* or *.nuget\nuget.config* starting from the root of drive and ending in the current directory.</span></span>

## <a name="arguments"></a><span data-ttu-id="657b5-115">Arguments</span><span class="sxs-lookup"><span data-stu-id="657b5-115">Arguments</span></span>

`ROOT`

<span data-ttu-id="657b5-116">Spécifie le chemin de fichier au package devant faire l’objet d’un envoi (push).</span><span class="sxs-lookup"><span data-stu-id="657b5-116">Specifies the file path to the package to be pushed.</span></span>

## <a name="options"></a><span data-ttu-id="657b5-117">Options</span><span class="sxs-lookup"><span data-stu-id="657b5-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="657b5-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="657b5-118">.NET Core 2.1</span></span>](#tab/netcore21)

`-d|--disable-buffering`

<span data-ttu-id="657b5-119">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="657b5-119">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

`--force-english-output`

<span data-ttu-id="657b5-120">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="657b5-120">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="657b5-121">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="657b5-121">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="657b5-122">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-122">The API key for the server.</span></span>

`-n|--no-symbols`

<span data-ttu-id="657b5-123">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="657b5-123">Doesn't push symbols (even if present).</span></span>

`--no-service-endpoint`

<span data-ttu-id="657b5-124">N’ajoute pas « api/v2/package » à l’URL source.</span><span class="sxs-lookup"><span data-stu-id="657b5-124">Doesn't append "api/v2/package" to the source URL.</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="657b5-125">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-125">Specifies the server URL.</span></span> <span data-ttu-id="657b5-126">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="657b5-126">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`-sk|--symbol-api-key <API_KEY>`

<span data-ttu-id="657b5-127">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="657b5-127">The API key for the symbol server.</span></span>

`-ss|--symbol-source <SOURCE>`

<span data-ttu-id="657b5-128">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="657b5-128">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="657b5-129">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-129">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="657b5-130">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="657b5-130">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="657b5-131">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="657b5-131">Specifying 0 (zero seconds) applies the default value.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="657b5-132">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="657b5-132">.NET Core 2.0</span></span>](#tab/netcore20)

`-d|--disable-buffering`

<span data-ttu-id="657b5-133">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="657b5-133">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

`--force-english-output`

<span data-ttu-id="657b5-134">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="657b5-134">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="657b5-135">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="657b5-135">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="657b5-136">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-136">The API key for the server.</span></span>

`-n|--no-symbols`

<span data-ttu-id="657b5-137">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="657b5-137">Doesn't push symbols (even if present).</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="657b5-138">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-138">Specifies the server URL.</span></span> <span data-ttu-id="657b5-139">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="657b5-139">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`-sk|--symbol-api-key <API_KEY>`

<span data-ttu-id="657b5-140">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="657b5-140">The API key for the symbol server.</span></span>

`-ss|--symbol-source <SOURCE>`

<span data-ttu-id="657b5-141">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="657b5-141">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="657b5-142">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-142">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="657b5-143">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="657b5-143">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="657b5-144">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="657b5-144">Specifying 0 (zero seconds) applies the default value.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="657b5-145">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="657b5-145">.NET Core 1.x</span></span>](#tab/netcore1x)

`-d|--disable-buffering`

<span data-ttu-id="657b5-146">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="657b5-146">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

`--force-english-output`

<span data-ttu-id="657b5-147">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="657b5-147">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="657b5-148">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="657b5-148">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="657b5-149">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-149">The API key for the server.</span></span>

`-n|--no-symbols`

<span data-ttu-id="657b5-150">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="657b5-150">Doesn't push symbols (even if present).</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="657b5-151">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-151">Specifies the server URL.</span></span> <span data-ttu-id="657b5-152">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="657b5-152">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`-sk|--symbol-api-key <API_KEY>`

<span data-ttu-id="657b5-153">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="657b5-153">The API key for the symbol server.</span></span>

`-ss|--symbol-source <SOURCE>`

<span data-ttu-id="657b5-154">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="657b5-154">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="657b5-155">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="657b5-155">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="657b5-156">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="657b5-156">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="657b5-157">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="657b5-157">Specifying 0 (zero seconds) applies the default value.</span></span>

---

## <a name="examples"></a><span data-ttu-id="657b5-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="657b5-158">Examples</span></span>

<span data-ttu-id="657b5-159">Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant une clé API :</span><span class="sxs-lookup"><span data-stu-id="657b5-159">Pushes *foo.nupkg* to the default push source, specifying an API key:</span></span>

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

<span data-ttu-id="657b5-160">Envoyez (push) *foo.nupkg* à la source de push personnalisée `http://customsource`, en spécifiant une clé API :</span><span class="sxs-lookup"><span data-stu-id="657b5-160">Push *foo.nupkg* to the custom push source `http://customsource`, specifying an API key:</span></span>

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s http://customsource/`

<span data-ttu-id="657b5-161">Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="657b5-161">Pushes *foo.nupkg* to the default push source:</span></span>

`dotnet nuget push foo.nupkg`

<span data-ttu-id="657b5-162">Effectuer une transmission de type push de *foo.symbols.nupkg* vers la source de symboles par défaut :</span><span class="sxs-lookup"><span data-stu-id="657b5-162">Pushes *foo.symbols.nupkg* to the default symbols source:</span></span>

`dotnet nuget push foo.symbols.nupkg`

<span data-ttu-id="657b5-163">Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant un délai d’attente de 360 secondes :</span><span class="sxs-lookup"><span data-stu-id="657b5-163">Pushes *foo.nupkg* to the default push source, specifying a 360-second timeout:</span></span>

`dotnet nuget push foo.nupkg --timeout 360`

<span data-ttu-id="657b5-164">Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="657b5-164">Pushes all *.nupkg* files in the current directory to the default push source:</span></span>

`dotnet nuget push *.nupkg`

<span data-ttu-id="657b5-165">Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut, en spécifiant un fichier de configuration personnalisé *./config/My.Config* :</span><span class="sxs-lookup"><span data-stu-id="657b5-165">Pushes all *.nupkg* files in the current directory to the default push source, specifying a custom config file *./config/My.Config*:</span></span>

`dotnet nuget push *.nupkg --config-file ./config/My.Config`
