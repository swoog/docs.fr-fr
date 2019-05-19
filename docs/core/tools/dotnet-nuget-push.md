---
title: Commande dotnet nuget push
description: La commande dotnet nuget push exécute un envoi (push) d’un package sur le serveur et le publie.
author: karann-msft
ms.date: 12/04/2018
ms.openlocfilehash: 7382cb93da3d7ed68f5731b3996c735c3f1461e4
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65631711"
---
# <a name="dotnet-nuget-push"></a><span data-ttu-id="79902-103">dotnet nuget push</span><span class="sxs-lookup"><span data-stu-id="79902-103">dotnet nuget push</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="79902-104">Name</span><span class="sxs-lookup"><span data-stu-id="79902-104">Name</span></span>

<span data-ttu-id="79902-105">`dotnet nuget push` - Exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="79902-105">`dotnet nuget push` - Pushes a package to the server and publishes it.</span></span>

## <a name="synopsis"></a><span data-ttu-id="79902-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="79902-106">Synopsis</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="79902-107">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="79902-107">.NET Core 2.x</span></span>](#tab/netcore2x)

```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [--interactive] [-k|--api-key] [-n|--no-symbols]
    [--no-service-endpoint] [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="79902-108">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="79902-108">.NET Core 1.x</span></span>](#tab/netcore1x)

```
dotnet nuget push [<ROOT>] [-d|--disable-buffering] [--force-english-output] [-k|--api-key] [-n|--no-symbols]
    [-s|--source] [-sk|--symbol-api-key] [-ss|--symbol-source] [-t|--timeout]
dotnet nuget push [-h|--help]
```

---

## <a name="description"></a><span data-ttu-id="79902-109">Description</span><span class="sxs-lookup"><span data-stu-id="79902-109">Description</span></span>

<span data-ttu-id="79902-110">La commande `dotnet nuget push` exécute un push d’un package sur le serveur et le publie.</span><span class="sxs-lookup"><span data-stu-id="79902-110">The `dotnet nuget push` command pushes a package to the server and publishes it.</span></span> <span data-ttu-id="79902-111">La commande push utilise les informations serveur et d’identification trouvées dans le fichier ou la chaîne de fichiers de configuration NuGet du système.</span><span class="sxs-lookup"><span data-stu-id="79902-111">The push command uses server and credential details found in the system's NuGet config file or chain of config files.</span></span> <span data-ttu-id="79902-112">Pour plus d’informations sur les fichiers de configuration, consultez [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior) (Configuration du comportement de NuGet ).</span><span class="sxs-lookup"><span data-stu-id="79902-112">For more information on config files, see [Configuring NuGet Behavior](/nuget/consume-packages/configuring-nuget-behavior).</span></span> <span data-ttu-id="79902-113">La configuration par défaut de NuGet est obtenue en chargeant *%AppData%\NuGet\NuGet.config* (Windows) ou *$HOME/.local/share* (Linux/macOS), puis en chargeant tout fichier *nuget.config* ou *.nuget\nuget.config* à partir de la racine du lecteur jusqu’au répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="79902-113">NuGet's default configuration is obtained by loading *%AppData%\NuGet\NuGet.config* (Windows) or *$HOME/.local/share* (Linux/macOS), then loading any *nuget.config* or *.nuget\nuget.config* starting from the root of drive and ending in the current directory.</span></span>

## <a name="arguments"></a><span data-ttu-id="79902-114">Arguments</span><span class="sxs-lookup"><span data-stu-id="79902-114">Arguments</span></span>

* **`ROOT`**

  <span data-ttu-id="79902-115">Spécifie le chemin de fichier au package devant faire l’objet d’un envoi (push).</span><span class="sxs-lookup"><span data-stu-id="79902-115">Specifies the file path to the package to be pushed.</span></span>

## <a name="options"></a><span data-ttu-id="79902-116">Options</span><span class="sxs-lookup"><span data-stu-id="79902-116">Options</span></span>

# <a name="net-core-2xtabnetcore2x"></a>[<span data-ttu-id="79902-117">.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="79902-117">.NET Core 2.x</span></span>](#tab/netcore2x)

* **`-d|--disable-buffering`**

  <span data-ttu-id="79902-118">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="79902-118">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

* **`--force-english-output`**

  <span data-ttu-id="79902-119">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="79902-119">Forces the application to run using an invariant, English-based culture.</span></span>

* **`-h|--help`**

<span data-ttu-id="79902-120">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="79902-120">Prints out a short help for the command.</span></span>

* **`--interactive`**

  <span data-ttu-id="79902-121">Autorise la commande pour bloquer et exige une action manuelle pour des opérations comme l'authentification.</span><span class="sxs-lookup"><span data-stu-id="79902-121">Allows the command to block and requires manual action for operations like authentication.</span></span> <span data-ttu-id="79902-122">Option disponible à partir du SDK .NET Core 2.2.</span><span class="sxs-lookup"><span data-stu-id="79902-122">Option available since .NET Core 2.2 SDK.</span></span>

* **`-k|--api-key <API_KEY>`**

  <span data-ttu-id="79902-123">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="79902-123">The API key for the server.</span></span>

* **`-n|--no-symbols`**

  <span data-ttu-id="79902-124">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="79902-124">Doesn't push symbols (even if present).</span></span>

* **`--no-service-endpoint`**

  <span data-ttu-id="79902-125">N’ajoute pas « api/v2/package » à l’URL source.</span><span class="sxs-lookup"><span data-stu-id="79902-125">Doesn't append "api/v2/package" to the source URL.</span></span> <span data-ttu-id="79902-126">Option disponible à partir du kit SDK .NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="79902-126">Option available since .NET Core 2.1 SDK.</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="79902-127">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="79902-127">Specifies the server URL.</span></span> <span data-ttu-id="79902-128">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="79902-128">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

* **`-sk|--symbol-api-key <API_KEY>`**

  <span data-ttu-id="79902-129">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="79902-129">The API key for the symbol server.</span></span>

* **`-ss|--symbol-source <SOURCE>`**

  <span data-ttu-id="79902-130">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="79902-130">Specifies the symbol server URL.</span></span>

* **`-t|--timeout <TIMEOUT>`**

  <span data-ttu-id="79902-131">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="79902-131">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="79902-132">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="79902-132">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="79902-133">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="79902-133">Specifying 0 (zero seconds) applies the default value.</span></span>

# <a name="net-core-1xtabnetcore1x"></a>[<span data-ttu-id="79902-134">.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="79902-134">.NET Core 1.x</span></span>](#tab/netcore1x)

* **`-d|--disable-buffering`**

  <span data-ttu-id="79902-135">Désactive la mise en mémoire tampon pendant le transfert push vers un serveur HTTP(S) afin de réduire l’utilisation de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="79902-135">Disables buffering when pushing to an HTTP(S) server to reduce memory usage.</span></span>

* **`--force-english-output`**

  <span data-ttu-id="79902-136">Force l’application à s’exécuter avec les paramètres régionaux Anglais (culture indifférente).</span><span class="sxs-lookup"><span data-stu-id="79902-136">Forces the application to run using an invariant, English-based culture.</span></span>

* **`-h|--help`**

  <span data-ttu-id="79902-137">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="79902-137">Prints out a short help for the command.</span></span>

* **`-k|--api-key <API_KEY>`**

  <span data-ttu-id="79902-138">Clé d’API pour le serveur.</span><span class="sxs-lookup"><span data-stu-id="79902-138">The API key for the server.</span></span>

* **`-n|--no-symbols`**

  <span data-ttu-id="79902-139">N’envoie pas les symboles (même s’ils sont présents).</span><span class="sxs-lookup"><span data-stu-id="79902-139">Doesn't push symbols (even if present).</span></span>

* **`-s|--source <SOURCE>`**

  <span data-ttu-id="79902-140">Spécifie l’URL du serveur.</span><span class="sxs-lookup"><span data-stu-id="79902-140">Specifies the server URL.</span></span> <span data-ttu-id="79902-141">Cette option est obligatoire, sauf si la valeur de configuration de `DefaultPushSource` est définie dans le fichier de configuration NuGet.</span><span class="sxs-lookup"><span data-stu-id="79902-141">This option is required unless `DefaultPushSource` config value is set in the NuGet config file.</span></span>

* **`-sk|--symbol-api-key <API_KEY>`**

  <span data-ttu-id="79902-142">Clé d’API pour le serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="79902-142">The API key for the symbol server.</span></span>

* **`-ss|--symbol-source <SOURCE>`**

  <span data-ttu-id="79902-143">Spécifie l’URL du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="79902-143">Specifies the symbol server URL.</span></span>

* **`-t|--timeout <TIMEOUT>`**

  <span data-ttu-id="79902-144">Spécifie le délai d’attente, en secondes, pour effectuer un push vers un serveur.</span><span class="sxs-lookup"><span data-stu-id="79902-144">Specifies the timeout for pushing to a server in seconds.</span></span> <span data-ttu-id="79902-145">La valeur par défaut est 300 secondes (5 minutes).</span><span class="sxs-lookup"><span data-stu-id="79902-145">Defaults to 300 seconds (5 minutes).</span></span> <span data-ttu-id="79902-146">Si vous spécifiez 0 (zéro seconde), la valeur par défaut s’applique.</span><span class="sxs-lookup"><span data-stu-id="79902-146">Specifying 0 (zero seconds) applies the default value.</span></span>

---

## <a name="examples"></a><span data-ttu-id="79902-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="79902-147">Examples</span></span>

* <span data-ttu-id="79902-148">Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant une clé API :</span><span class="sxs-lookup"><span data-stu-id="79902-148">Pushes *foo.nupkg* to the default push source, specifying an API key:</span></span>

  ```console
  dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a
  ```

* <span data-ttu-id="79902-149">Envoyez (push) *foo.nupkg* à la source de push personnalisée `https://customsource`, en spécifiant une clé API :</span><span class="sxs-lookup"><span data-stu-id="79902-149">Push *foo.nupkg* to the custom push source `https://customsource`, specifying an API key:</span></span>

  ```console
  dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s https://customsource/
  ```

* <span data-ttu-id="79902-150">Effectuer une transmission de type push de *foo.nupkg* vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="79902-150">Pushes *foo.nupkg* to the default push source:</span></span>

  ```console
  dotnet nuget push foo.nupkg
  ```

* <span data-ttu-id="79902-151">Effectuer une transmission de type push de *foo.symbols.nupkg* vers la source de symboles par défaut :</span><span class="sxs-lookup"><span data-stu-id="79902-151">Pushes *foo.symbols.nupkg* to the default symbols source:</span></span>

  ```console
  dotnet nuget push foo.symbols.nupkg
  ```

* <span data-ttu-id="79902-152">Envoie (push) *foo.nupkg* à la source de push par défaut, en spécifiant un délai d’attente de 360 secondes :</span><span class="sxs-lookup"><span data-stu-id="79902-152">Pushes *foo.nupkg* to the default push source, specifying a 360-second timeout:</span></span>

  ```console
  dotnet nuget push foo.nupkg --timeout 360
  ```

* <span data-ttu-id="79902-153">Effectuer une transmission de type push de tous les fichiers *.nupkg* du répertoire actif vers la source de push par défaut :</span><span class="sxs-lookup"><span data-stu-id="79902-153">Pushes all *.nupkg* files in the current directory to the default push source:</span></span>

  ```console
  dotnet nuget push *.nupkg
  ```
