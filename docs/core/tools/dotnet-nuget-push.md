---
title: Commande dotnet nuget push - Interface CLI .NET Core
description: La commande dotnet nuget push exécute un envoi (push) d’un package sur le serveur et le publie.
author: karann-msft
ms.author: mairaw
ms.date: 09/04/2018
ms.openlocfilehash: b9c0fad886cd1234325c58bf61b1a010bce421d9
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/29/2018
ms.locfileid: "50200020"
---
# <a name="dotnet-nuget-push"></a><span data-ttu-id="c94db-103">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="c94db-103">dotnet nuget push</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="c94db-104">Name</span><span class="sxs-lookup"><span data-stu-id="c94db-104">Name</span></span>

<span data-ttu-id="c94db-105">`dotnet nuget push` - Exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="c94db-105">`dotnet nuget push` - Pushes a package to the server and publishes it.</span></span>

## <a name="synopsis"></a><span data-ttu-id="c94db-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c94db-106">Synopsis</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="c94db-107">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="c94db-107">.NET Core 2.1</span></span>](#tab/netcore21)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [--no-service-endpoint] [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="c94db-108">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c94db-108">.NET Core 2.0</span></span>](#tab/netcore20)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="c94db-109">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="c94db-109">.NET Core 1.x</span></span>](#tab/netcore1x)
```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```
---

## <a name="description"></a><span data-ttu-id="c94db-110">Description</span><span class="sxs-lookup"><span data-stu-id="c94db-110">Description</span></span>

<span data-ttu-id="c94db-111">La commande `dotnet nuget push` exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="c94db-111">The `dotnet nuget push` command pushes a package to the server and publishes it.</span></span> <span data-ttu-id="c94db-112">La commande push utilise les informations serveur et d’identification trouvées dans le fichier ou la chaîne de fichiers de configuration NuGet du système.</span><span class="sxs-lookup"><span data-stu-id="c94db-112">The push command uses server and credential details found in the system's NuGet config file or chain of config files.</span></span> <span data-ttu-id="c94db-113">Pour plus d’informations sur les fichiers de configuration, consultez [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior) (Configuration du comportement de NuGet ).</span><span class="sxs-lookup"><span data-stu-id="c94db-113">For more information on config files, see [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior).</span></span> <span data-ttu-id="c94db-114">La configuration par défaut de NuGet est obtenue en chargeant *%AppData%\NuGet\NuGet.config* (Windows) ou *$HOME/.local/share* (Linux/macOS), puis en chargeant tout fichier *nuget.config* ou *.nuget\nuget.config* à partir de la racine du lecteur jusqu’au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="c94db-114">NuGet's default configuration is obtained by loading *%AppData%\NuGet\NuGet.config* (Windows) or *$HOME/.local/share* (Linux/macOS), then loading any *nuget.config* or *.nuget\nuget.config* starting from the root of drive and ending in the current directory.</span></span>

## <a name="arguments"></a><span data-ttu-id="c94db-115">Arguments</span><span class="sxs-lookup"><span data-stu-id="c94db-115">Arguments</span></span>

`ROOT`

<span data-ttu-id="c94db-116">Spécifie le chemin de fichier au package devant faire l’objet d’un envoi (push).</span><span class="sxs-lookup"><span data-stu-id="c94db-116">Specifies the file path to the package to be pushed.</span></span>

## <a name="options"></a><span data-ttu-id="c94db-117">Options</span><span class="sxs-lookup"><span data-stu-id="c94db-117">Options</span></span>

# <a name="net-core-21tabnetcore21"></a>[<span data-ttu-id="c94db-118">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="c94db-118">.NET Core 2.1</span></span>](#tab/netcore21)

`-d|--disable-buffering`

<span data-ttu-id="c94db-119">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c94db-119">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

`--force-english-output`

<span data-ttu-id="c94db-120">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="c94db-120">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="c94db-121">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="c94db-121">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="c94db-122">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-122">The API key for the server.</span></span>

`-n|--no-symbols`

<span data-ttu-id="c94db-123">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="c94db-123">Doesn't push symbols (even if present).</span></span>

`--no-service-endpoint`

<span data-ttu-id="c94db-124">N’ajoute pas « api/v2/package » à l’URL source.</span><span class="sxs-lookup"><span data-stu-id="c94db-124">Doesn't append "api/v2/package" to the source URL.</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="c94db-125">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-125">Specifies the server URL.</span></span> <span data-ttu-id="c94db-126">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="c94db-126">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`-sk|--symbol-api-key <API_KEY>`

<span data-ttu-id="c94db-127">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="c94db-127">The API key for the symbol server.</span></span>

`-ss|--symbol-source <SOURCE>`

<span data-ttu-id="c94db-128">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="c94db-128">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="c94db-129">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-129">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="c94db-130">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="c94db-130">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="c94db-131">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="c94db-131">Specifying 0 (zero seconds) applies the default value.</span></span>

# <a name="net-core-20tabnetcore20"></a>[<span data-ttu-id="c94db-132">.NET Core 2.0</span><span class="sxs-lookup"><span data-stu-id="c94db-132">.NET Core 2.0</span></span>](#tab/netcore20)

`-d|--disable-buffering`

<span data-ttu-id="c94db-133">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c94db-133">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

`--force-english-output`

<span data-ttu-id="c94db-134">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="c94db-134">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="c94db-135">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="c94db-135">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="c94db-136">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-136">The API key for the server.</span></span>

`-n|--no-symbols`

<span data-ttu-id="c94db-137">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="c94db-137">Doesn't push symbols (even if present).</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="c94db-138">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-138">Specifies the server URL.</span></span> <span data-ttu-id="c94db-139">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="c94db-139">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`-sk|--symbol-api-key <API_KEY>`

<span data-ttu-id="c94db-140">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="c94db-140">The API key for the symbol server.</span></span>

`-ss|--symbol-source <SOURCE>`

<span data-ttu-id="c94db-141">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="c94db-141">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="c94db-142">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-142">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="c94db-143">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="c94db-143">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="c94db-144">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="c94db-144">Specifying 0 (zero seconds) applies the default value.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="c94db-145">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="c94db-145">.NET Core 1.x</span></span>](#tab/netcore1x)

`-d|--disable-buffering`

<span data-ttu-id="c94db-146">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c94db-146">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

`--force-english-output`

<span data-ttu-id="c94db-147">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="c94db-147">Forces the application to run using an invariant, English-based culture.</span></span>

`-h|--help`

<span data-ttu-id="c94db-148">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="c94db-148">Prints out a short help for the command.</span></span>

`-k|--api-key <API_KEY>`

<span data-ttu-id="c94db-149">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-149">The API key for the server.</span></span>

`-n|--no-symbols`

<span data-ttu-id="c94db-150">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="c94db-150">Doesn't push symbols (even if present).</span></span>

`-s|--source <SOURCE>`

<span data-ttu-id="c94db-151">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-151">Specifies the server URL.</span></span> <span data-ttu-id="c94db-152">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="c94db-152">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

`-sk|--symbol-api-key <API_KEY>`

<span data-ttu-id="c94db-153">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="c94db-153">The API key for the symbol server.</span></span>

`-ss|--symbol-source <SOURCE>`

<span data-ttu-id="c94db-154">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="c94db-154">Specifies the symbol server URL.</span></span>

`-t|--timeout <TIMEOUT>`

<span data-ttu-id="c94db-155">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="c94db-155">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="c94db-156">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="c94db-156">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="c94db-157">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="c94db-157">Specifying 0 (zero seconds) applies the default value.</span></span>

---

## <a name="examples"></a><span data-ttu-id="c94db-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="c94db-158">Examples</span></span>

<span data-ttu-id="c94db-159">Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant une clé API :</span><span class="sxs-lookup"><span data-stu-id="c94db-159">Pushes *foo.nupkg* to the default push source, specifying an API key:</span></span>

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

<span data-ttu-id="c94db-160">Envoyez (push) *foo.nupkg* à la source de push personnalisée `https://customsource`, en spécifiant une clé API :</span><span class="sxs-lookup"><span data-stu-id="c94db-160">Push *foo.nupkg* to the custom push source `https://customsource`, specifying an API key:</span></span>

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s https://customsource/`

<span data-ttu-id="c94db-161">Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="c94db-161">Pushes *foo.nupkg* to the default push source:</span></span>

`dotnet nuget push foo.nupkg`

<span data-ttu-id="c94db-162">Effectuer une transmission de type push de *foo.symbols.nupkg* vers la source de symboles par défaut :</span><span class="sxs-lookup"><span data-stu-id="c94db-162">Pushes *foo.symbols.nupkg* to the default symbols source:</span></span>

`dotnet nuget push foo.symbols.nupkg`

<span data-ttu-id="c94db-163">Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant un délai d’attente de 360 secondes :</span><span class="sxs-lookup"><span data-stu-id="c94db-163">Pushes *foo.nupkg* to the default push source, specifying a 360-second timeout:</span></span>

`dotnet nuget push foo.nupkg --timeout 360`

<span data-ttu-id="c94db-164">Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="c94db-164">Pushes all *.nupkg* files in the current directory to the default push source:</span></span>

`dotnet nuget push *.nupkg`
