---
title: 'Prise en main stockage Blob Azure avec F #'
description: Store les données non structurées dans le cloud avec stockage Blob Azure.
author: sylvanc
ms.date: 09/20/2016
ms.openlocfilehash: ea9dc334ec9c2bcd4a80cc501d4b6634da5f64e4
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44037280"
---
# <a name="get-started-with-azure-blob-storage-using-f"></a><span data-ttu-id="f1ba0-103">Prise en main stockage Blob Azure avec F #</span><span class="sxs-lookup"><span data-stu-id="f1ba0-103">Get started with Azure Blob storage using F#</span></span> #

<span data-ttu-id="f1ba0-104">Le stockage Blob Azure est un service qui stocke les données non structurées dans le cloud en tant qu’objets/objets blob.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-104">Azure Blob storage is a service that stores unstructured data in the cloud as objects/blobs.</span></span> <span data-ttu-id="f1ba0-105">Le stockage Blob permet de stocker n’importe quel type de données texte ou binaires, par exemple un document, un fichier multimédia ou un programme d’installation d’application.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-105">Blob storage can store any type of text or binary data, such as a document, media file, or application installer.</span></span> <span data-ttu-id="f1ba0-106">Le stockage Blob est également appelé stockage d’objets.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-106">Blob storage is also referred to as object storage.</span></span>

<span data-ttu-id="f1ba0-107">Cet article vous montre comment effectuer des tâches courantes à l’aide du stockage d’objets Blob.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-107">This article shows you how to perform common tasks using Blob storage.</span></span> <span data-ttu-id="f1ba0-108">Les exemples sont écrits à l’aide de F # à l’aide de la bibliothèque cliente de stockage Azure pour .NET.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-108">The samples are written using F# using the Azure Storage Client Library for .NET.</span></span> <span data-ttu-id="f1ba0-109">Les tâches couvertes incluent comment télécharger, répertorier, télécharger et supprimer des objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-109">The tasks covered include how to upload, list, download, and delete blobs.</span></span>

<span data-ttu-id="f1ba0-110">Pour obtenir une vue d’ensemble conceptuelle de stockage d’objets blob, consultez [le guide de .NET pour le stockage blob](/azure/storage/storage-dotnet-how-to-use-blobs).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-110">For a conceptual overview of blob storage, see [the .NET guide for blob storage](/azure/storage/storage-dotnet-how-to-use-blobs).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f1ba0-111">Prérequis</span><span class="sxs-lookup"><span data-stu-id="f1ba0-111">Prerequisites</span></span>

<span data-ttu-id="f1ba0-112">Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-112">To use this guide, you must first [create an Azure storage account](/azure/storage/storage-create-storage-account).</span></span> <span data-ttu-id="f1ba0-113">Vous devez également votre clé d’accès de stockage pour ce compte.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-113">You also need your storage access key for this account.</span></span>

## <a name="create-an-f-script-and-start-f-interactive"></a><span data-ttu-id="f1ba0-114">Créer de Script F # et démarrer F # Interactive</span><span class="sxs-lookup"><span data-stu-id="f1ba0-114">Create an F# Script and Start F# Interactive</span></span>

<span data-ttu-id="f1ba0-115">Les exemples de cet article peuvent être utilisés dans une application F # ou un script F #.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-115">The samples in this article can be used in either an F# application or an F# script.</span></span> <span data-ttu-id="f1ba0-116">Pour créer un script F #, créez un fichier avec le `.fsx` extension, par exemple `blobs.fsx`, dans votre environnement de développement F #.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-116">To create an F# script, create a file with the `.fsx` extension, for example `blobs.fsx`, in your F# development environment.</span></span>

<span data-ttu-id="f1ba0-117">Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` et `Microsoft.WindowsAzure.ConfigurationManager` packages et référence `WindowsAzure.Storage.dll` et `Microsoft.WindowsAzure.Configuration.dll` dans votre script à l’aide un `#r` directive.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-117">Next, use a [package manager](package-management.md) such as [Paket](https://fsprojects.github.io/Paket/) or [NuGet](https://www.nuget.org/) to install the `WindowsAzure.Storage` and `Microsoft.WindowsAzure.ConfigurationManager` packages and reference `WindowsAzure.Storage.dll` and `Microsoft.WindowsAzure.Configuration.dll` in your script using a `#r` directive.</span></span>

### <a name="add-namespace-declarations"></a><span data-ttu-id="f1ba0-118">Ajoutez les déclarations d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1ba0-118">Add namespace declarations</span></span>

<span data-ttu-id="f1ba0-119">Ajoutez le code suivant `open` instructions au début de la `blobs.fsx` fichier :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-119">Add the following `open` statements to the top of the `blobs.fsx` file:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L1-L5)]

### <a name="get-your-connection-string"></a><span data-ttu-id="f1ba0-120">Obtenir votre chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="f1ba0-120">Get your connection string</span></span>

<span data-ttu-id="f1ba0-121">Vous avez besoin d’une chaîne de connexion de stockage Azure pour ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-121">You need an Azure Storage connection string for this tutorial.</span></span> <span data-ttu-id="f1ba0-122">Pour plus d’informations sur les chaînes de connexion, consultez [configuration des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-122">For more information about connection strings, see [Configure Storage Connection Strings](/azure/storage/storage-configure-connection-string).</span></span>

<span data-ttu-id="f1ba0-123">Pour ce didacticiel, vous entrez votre chaîne de connexion dans votre script, comme suit :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-123">For the tutorial, you enter your connection string in your script, like this:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L11-L11)]

<span data-ttu-id="f1ba0-124">Toutefois, il s’agit de **déconseillé** projets de réel.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-124">However, this is **not recommended** for real projects.</span></span> <span data-ttu-id="f1ba0-125">Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-125">Your storage account key is similar to the root password for your storage account.</span></span> <span data-ttu-id="f1ba0-126">Veillez toujours à protéger votre clé de compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-126">Always be careful to protect your storage account key.</span></span> <span data-ttu-id="f1ba0-127">Évitez de la communiquer à d’autres utilisateurs, coder en dur, ou l’enregistrer dans un fichier texte brut qui n’est accessible à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-127">Avoid distributing it to other users, hard-coding it, or saving it in a plain-text file that is accessible to others.</span></span> <span data-ttu-id="f1ba0-128">Vous pouvez régénérer votre clé à l’aide du portail Azure si vous pensez qu’il a peut-être été compromise.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-128">You can regenerate your key using the Azure Portal if you believe it may have been compromised.</span></span>

<span data-ttu-id="f1ba0-129">Applications de réel, la meilleure façon de conserver votre chaîne de connexion de stockage est dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-129">For real applications, the best way to maintain your storage connection string is in a configuration file.</span></span> <span data-ttu-id="f1ba0-130">Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-130">To fetch the connection string from a configuration file, you can do this:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L13-L15)]

<span data-ttu-id="f1ba0-131">L’utilisation d’Azure Configuration Manager est facultative.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-131">Using Azure Configuration Manager is optional.</span></span> <span data-ttu-id="f1ba0-132">Vous pouvez également utiliser une API telle que du .NET Framework `ConfigurationManager` type.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-132">You can also use an API such as the .NET Framework's `ConfigurationManager` type.</span></span>

### <a name="parse-the-connection-string"></a><span data-ttu-id="f1ba0-133">Analyser la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="f1ba0-133">Parse the connection string</span></span>

<span data-ttu-id="f1ba0-134">Pour analyser la chaîne de connexion, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-134">To parse the connection string, use:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L21-L22)]

<span data-ttu-id="f1ba0-135">Cette commande renvoie un `CloudStorageAccount`.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-135">This returns a `CloudStorageAccount`.</span></span>

### <a name="create-some-local-dummy-data"></a><span data-ttu-id="f1ba0-136">Créer des données factices locales</span><span class="sxs-lookup"><span data-stu-id="f1ba0-136">Create some local dummy data</span></span>

<span data-ttu-id="f1ba0-137">Avant de commencer, créez des données locales factices dans le répertoire de notre script.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-137">Before you begin, create some dummy local data in the directory of our script.</span></span> <span data-ttu-id="f1ba0-138">Plus tard, vous chargez ces données.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-138">Later you upload this data.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L28-L30)]

### <a name="create-the-blob-service-client"></a><span data-ttu-id="f1ba0-139">Créer le client de service Blob</span><span class="sxs-lookup"><span data-stu-id="f1ba0-139">Create the Blob service client</span></span>

<span data-ttu-id="f1ba0-140">Le `CloudBlobClient` type vous permet de récupérer les conteneurs et objets BLOB stockés dans le stockage Blob.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-140">The `CloudBlobClient` type enables you to retrieve containers and blobs stored in Blob storage.</span></span> <span data-ttu-id="f1ba0-141">Voici une façon de créer le client du service :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-141">Here's one way to create the service client:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L36-L36)]

<span data-ttu-id="f1ba0-142">Vous êtes maintenant prêt à écrire du code qui lit et écrit des données dans le stockage d’objets Blob.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-142">Now you are ready to write code that reads data from and writes data to Blob storage.</span></span>

## <a name="create-a-container"></a><span data-ttu-id="f1ba0-143">Créer un conteneur</span><span class="sxs-lookup"><span data-stu-id="f1ba0-143">Create a container</span></span>

<span data-ttu-id="f1ba0-144">Cet exemple montre comment créer un conteneur si elle n’existe pas déjà :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-144">This example shows how to create a container if it does not already exist:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L42-L46)]

<span data-ttu-id="f1ba0-145">Par défaut, le nouveau conteneur est privé, ce qui signifie que vous devez spécifier votre clé d’accès de stockage pour télécharger des objets BLOB à partir de ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-145">By default, the new container is private, meaning that you must specify your storage access key to download blobs from this container.</span></span> <span data-ttu-id="f1ba0-146">Si vous souhaitez mettre les fichiers dans le conteneur de disposition tout le monde, vous pouvez définir le conteneur public en utilisant le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-146">If you want to make the files within the container available to everyone, you can set the container to be public using the following code:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L48-L49)]

<span data-ttu-id="f1ba0-147">Quiconque sur Internet permettre afficher les objets BLOB dans un conteneur public, mais vous pouvez modifier ou les supprimer que si vous disposez de la clé d’accès de compte approprié ou une signature d’accès partagé.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-147">Anyone on the Internet can see blobs in a public container, but you can modify or delete them only if you have the appropriate account access key or a shared access signature.</span></span>

## <a name="upload-a-blob-into-a-container"></a><span data-ttu-id="f1ba0-148">Charger un objet blob dans un conteneur</span><span class="sxs-lookup"><span data-stu-id="f1ba0-148">Upload a blob into a container</span></span>

<span data-ttu-id="f1ba0-149">Stockage d’objets Blob Azure prend en charge les objets BLOB de blocs et objets BLOB de pages.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-149">Azure Blob Storage supports block blobs and page blobs.</span></span> <span data-ttu-id="f1ba0-150">Dans la plupart des cas, un objet blob de blocs est le type recommandé à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-150">In most cases, a block blob is the recommended type to use.</span></span>

<span data-ttu-id="f1ba0-151">Pour télécharger un fichier à un objet blob de blocs, obtenez une référence de conteneur et utilisez-la pour obtenir une référence d’objet blob de bloc.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-151">To upload a file to a block blob, get a container reference and use it to get a block blob reference.</span></span> <span data-ttu-id="f1ba0-152">Une fois que vous avez une référence d’objet blob, vous pouvez télécharger n’importe quel flux de données à ce dernier en appelant le `UploadFromFile` (méthode).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-152">Once you have a blob reference, you can upload any stream of data to it by calling the `UploadFromFile` method.</span></span> <span data-ttu-id="f1ba0-153">Cette opération crée l’objet blob s’il n’a pas précédemment existe ou écraser s’il n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-153">This operation creates the blob if it didn't previously exist, or overwrite it if it does exist.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L55-L59)]

## <a name="list-the-blobs-in-a-container"></a><span data-ttu-id="f1ba0-154">Répertorier les objets BLOB dans un conteneur</span><span class="sxs-lookup"><span data-stu-id="f1ba0-154">List the blobs in a container</span></span>

<span data-ttu-id="f1ba0-155">Pour répertorier les objets BLOB dans un conteneur, commencez par obtenir une référence de conteneur.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-155">To list the blobs in a container, first get a container reference.</span></span> <span data-ttu-id="f1ba0-156">Vous pouvez ensuite utiliser le conteneur `ListBlobs` méthode pour récupérer les objets BLOB et/ou les répertoires qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-156">You can then use the container's `ListBlobs` method to retrieve the blobs and/or directories within it.</span></span> <span data-ttu-id="f1ba0-157">Pour accéder à l’ensemble des propriétés et méthodes d’un `IListBlobItem`, vous devez le convertir en un `CloudBlockBlob`, `CloudPageBlob`, ou `CloudBlobDirectory` objet.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-157">To access the rich set of properties and methods for a returned `IListBlobItem`, you must cast it to a `CloudBlockBlob`, `CloudPageBlob`, or `CloudBlobDirectory` object.</span></span> <span data-ttu-id="f1ba0-158">Si le type est inconnu, vous pouvez utiliser une vérification de type pour déterminer quelle cible de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-158">If the type is unknown, you can use a type check to determine which to cast it to.</span></span> <span data-ttu-id="f1ba0-159">Le code suivant montre comment récupérer et générer l’URI de chaque élément dans le `mydata` conteneur :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-159">The following code demonstrates how to retrieve and output the URI of each item in the `mydata` container:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L67-L80)]

<span data-ttu-id="f1ba0-160">Vous pouvez également des objets BLOB de nom avec les informations de chemin d’accès dans leurs noms.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-160">You can also name blobs with path information in their names.</span></span> <span data-ttu-id="f1ba0-161">Cette opération crée une structure de répertoire virtuel que vous pouvez organiser et parcourir comme vous le feriez pour un système de fichiers traditionnel.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-161">This creates a virtual directory structure that you can organize and traverse as you would a traditional file system.</span></span> <span data-ttu-id="f1ba0-162">Notez que la structure de répertoires est uniquement virtuelle : les seules ressources disponibles dans le stockage d’objets Blob sont des conteneurs et objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-162">Note that the directory structure is virtual only - the only resources available in Blob storage are containers and blobs.</span></span> <span data-ttu-id="f1ba0-163">Toutefois, la bibliothèque cliente storage propose un `CloudBlobDirectory` objet pour faire référence à un répertoire virtuel et simplifier le processus d’utilisation des objets BLOB sont organisés de cette façon.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-163">However, the storage client library offers a `CloudBlobDirectory` object to refer to a virtual directory and simplify the process of working with blobs that are organized in this way.</span></span>

<span data-ttu-id="f1ba0-164">Par exemple, prenez l’ensemble suivant d’objets BLOB de blocs dans un conteneur nommé `photos`:</span><span class="sxs-lookup"><span data-stu-id="f1ba0-164">For example, consider the following set of block blobs in a container named `photos`:</span></span>

<span data-ttu-id="f1ba0-165">*photo1.jpg*
*2015/architecture/description.txt*
*2015/architecture/photo3.jpg*
*2015/architecture/photo4.jpg*
*2016/architecture/photo5.jpg*
*2016/architecture/photo6.jpg*
*2016/architecture/description.txt*
*2016/photo7.jpg*</span><span class="sxs-lookup"><span data-stu-id="f1ba0-165">*photo1.jpg*
*2015/architecture/description.txt*
*2015/architecture/photo3.jpg*
*2015/architecture/photo4.jpg*
*2016/architecture/photo5.jpg*
*2016/architecture/photo6.jpg*
*2016/architecture/description.txt*
*2016/photo7.jpg*</span></span>

<span data-ttu-id="f1ba0-166">Lorsque vous appelez `ListBlobs` sur un conteneur (comme dans l’exemple ci-dessus), une liste hiérarchique est retournée.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-166">When you call `ListBlobs` on a container (as in the above sample), a hierarchical listing is returned.</span></span> <span data-ttu-id="f1ba0-167">Si elle contient à la fois `CloudBlobDirectory` et `CloudBlockBlob` objets représentant les répertoires et les objets BLOB du conteneur, respectivement, puis le résultat ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-167">If it contains both `CloudBlobDirectory` and `CloudBlockBlob` objects, representing the directories and blobs in the container, respectively, then the resulting output looks similar to this:</span></span>

```console
Directory: https://<accountname>.blob.core.windows.net/photos/2015/
Directory: https://<accountname>.blob.core.windows.net/photos/2016/
Block blob of length 505623: https://<accountname>.blob.core.windows.net/photos/photo1.jpg
```

<span data-ttu-id="f1ba0-168">Si vous le souhaitez, vous pouvez définir le `UseFlatBlobListing` paramètre de la `ListBlobs` méthode `true`.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-168">Optionally, you can set the `UseFlatBlobListing` parameter of the `ListBlobs` method to `true`.</span></span> <span data-ttu-id="f1ba0-169">Dans ce cas, chaque objet blob dans le conteneur est retourné comme un `CloudBlockBlob` objet.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-169">In this case, every blob in the container is returned as a `CloudBlockBlob` object.</span></span> <span data-ttu-id="f1ba0-170">L’appel à `ListBlobs` pour retourner une liste plate ressemble à ceci :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-170">The call to `ListBlobs` to return a flat listing looks like this:</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L82-L89)]

<span data-ttu-id="f1ba0-171">et, en fonction du contenu actuel de votre conteneur, les résultats ressemblent à ceci :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-171">and, depending on the current contents of your container, the results look like this:</span></span>

```console
Block blob of length 4: https://<accountname>.blob.core.windows.net/photos/2015/architecture/description.txt
Block blob of length 314618: https://<accountname>.blob.core.windows.net/photos/2015/architecture/photo3.jpg
Block blob of length 522713: https://<accountname>.blob.core.windows.net/photos/2015/architecture/photo4.jpg
Block blob of length 4: https://<accountname>.blob.core.windows.net/photos/2016/architecture/description.txt
Block blob of length 419048: https://<accountname>.blob.core.windows.net/photos/2016/architecture/photo5.jpg
Block blob of length 506388: https://<accountname>.blob.core.windows.net/photos/2016/architecture/photo6.jpg
Block blob of length 399751: https://<accountname>.blob.core.windows.net/photos/2016/photo7.jpg
Block blob of length 505623: https://<accountname>.blob.core.windows.net/photos/photo1.jpg
```

## <a name="download-blobs"></a><span data-ttu-id="f1ba0-172">Télécharger des objets BLOB</span><span class="sxs-lookup"><span data-stu-id="f1ba0-172">Download blobs</span></span>

<span data-ttu-id="f1ba0-173">Pour télécharger des objets BLOB, commencez par récupérer une référence d’objet blob, puis appelez le `DownloadToStream` (méthode).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-173">To download blobs, first retrieve a blob reference and then call the `DownloadToStream` method.</span></span> <span data-ttu-id="f1ba0-174">L’exemple suivant utilise la `DownloadToStream` méthode pour transférer le contenu de l’objet blob vers un objet de flux persistant dans un fichier local.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-174">The following example uses the `DownloadToStream` method to transfer the blob contents to a stream object that you can then persist to a local file.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L95-L101)]

<span data-ttu-id="f1ba0-175">Vous pouvez également utiliser le `DownloadToStream` méthode pour télécharger le contenu d’un objet blob comme une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-175">You can also use the `DownloadToStream` method to download the contents of a blob as a text string.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L103-L106)]

## <a name="delete-blobs"></a><span data-ttu-id="f1ba0-176">Supprimer des objets BLOB</span><span class="sxs-lookup"><span data-stu-id="f1ba0-176">Delete blobs</span></span>

<span data-ttu-id="f1ba0-177">Pour supprimer un objet blob, commencez par obtenir une référence d’objet blob, puis appelez le `Delete` méthode dessus.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-177">To delete a blob, first get a blob reference and then call the `Delete` method on it.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L112-L116)]

## <a name="list-blobs-in-pages-asynchronously"></a><span data-ttu-id="f1ba0-178">Répertorier les objets BLOB dans les pages de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="f1ba0-178">List blobs in pages asynchronously</span></span>

<span data-ttu-id="f1ba0-179">Si vous répertoriez un grand nombre d’objets BLOB, ou si vous souhaitez contrôler le nombre de résultats renvoyés dans une opération de liste, vous pouvez répertorier les objets BLOB dans les pages de résultats.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-179">If you are listing a large number of blobs, or you want to control the number of results you return in one listing operation, you can list blobs in pages of results.</span></span> <span data-ttu-id="f1ba0-180">Cet exemple montre comment renvoyer des résultats dans des pages en mode asynchrone, afin que l’exécution n’est pas bloquée lors de l’attente pour renvoyer un grand ensemble de résultats.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-180">This example shows how to return results in pages asynchronously, so that execution is not blocked while waiting to return a large set of results.</span></span>

<span data-ttu-id="f1ba0-181">Cet exemple montre une liste plate d’objets blob, mais vous pouvez également effectuer une liste hiérarchique, en définissant le `useFlatBlobListing` paramètre de la `ListBlobsSegmentedAsync` méthode `false`.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-181">This example shows a flat blob listing, but you can also perform a hierarchical listing, by setting the `useFlatBlobListing` parameter of the `ListBlobsSegmentedAsync` method to `false`.</span></span>

<span data-ttu-id="f1ba0-182">L’exemple définit une méthode asynchrone, à l’aide un `async` bloc.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-182">The sample defines an asynchronous method, using an `async` block.</span></span> <span data-ttu-id="f1ba0-183">Le ``let!`` mot clé suspend l’exécution de l’exemple de méthode jusqu'à ce que la tâche de la liste se termine.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-183">The ``let!`` keyword suspends execution of the sample method until the listing task completes.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L122-L160)]

<span data-ttu-id="f1ba0-184">Nous pouvons maintenant utiliser cette routine asynchrone comme suit.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-184">We can now use this asynchronous routine as follows.</span></span> <span data-ttu-id="f1ba0-185">Tout d’abord vous chargez des données factices (en utilisant le fichier local créé précédemment dans ce didacticiel).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-185">First you upload some dummy data (using the local file created earlier in this tutorial).</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L162-L166)]

<span data-ttu-id="f1ba0-186">À présent, appelez la routine.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-186">Now, call the routine.</span></span> <span data-ttu-id="f1ba0-187">Vous utilisez `Async.RunSynchronously` pour forcer l’exécution de l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-187">You use `Async.RunSynchronously` to force the execution of the asynchronous operation.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L168-L168)]

## <a name="writing-to-an-append-blob"></a><span data-ttu-id="f1ba0-188">Écriture dans un objet blob d’ajout</span><span class="sxs-lookup"><span data-stu-id="f1ba0-188">Writing to an append blob</span></span>

<span data-ttu-id="f1ba0-189">Un objet blob d’ajout est optimisé pour les opérations d’ajout, telles que la journalisation.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-189">An append blob is optimized for append operations, such as logging.</span></span> <span data-ttu-id="f1ba0-190">Comme un objet blob de blocs, un objet blob d’ajout est constitué de blocs, mais lorsque vous ajoutez un nouveau bloc à un objet blob d’ajout, elle est toujours ajoutée à la fin de l’objet blob.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-190">Like a block blob, an append blob is comprised of blocks, but when you add a new block to an append blob, it is always appended to the end of the blob.</span></span> <span data-ttu-id="f1ba0-191">Vous ne pouvez pas mettre à jour ou supprimer un bloc dans un objet blob d’ajout.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-191">You cannot update or delete an existing block in an append blob.</span></span> <span data-ttu-id="f1ba0-192">L’ID de bloc pour un objet blob d’ajout ne sont pas exposés comme ils le sont pour un objet blob de blocs.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-192">The block IDs for an append blob are not exposed as they are for a block blob.</span></span>

<span data-ttu-id="f1ba0-193">Chaque bloc dans un objet blob d’ajout peut avoir une taille différente, avec un maximum de 4 Mo, et un objet blob d’ajout peut inclure un maximum de 50 000 blocs.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-193">Each block in an append blob can be a different size, up to a maximum of 4 MB, and an append blob can include a maximum of 50,000 blocks.</span></span> <span data-ttu-id="f1ba0-194">La taille maximale d’un objet blob d’ajout est donc légèrement supérieure à 195 Go (4 Mo X 50 000 blocs).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-194">The maximum size of an append blob is therefore slightly more than 195 GB (4 MB X 50,000 blocks).</span></span>

<span data-ttu-id="f1ba0-195">L’exemple suivant crée un objet blob d’ajout et y ajoute des données, simulation d’une opération de journalisation simple.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-195">The following example creates a new append blob and appends some data to it, simulating a simple logging operation.</span></span>

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L174-L203)]

<span data-ttu-id="f1ba0-196">Consultez [objets BLOB de blocs, objets BLOB de pages et objets BLOB d’ajout](https://msdn.microsoft.com/library/azure/ee691964.aspx) pour plus d’informations sur les différences entre les trois types d’objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-196">See [Understanding Block Blobs, Page Blobs, and Append Blobs](https://msdn.microsoft.com/library/azure/ee691964.aspx) for more information about the differences between the three types of blobs.</span></span>

## <a name="concurrent-access"></a><span data-ttu-id="f1ba0-197">Accès simultané</span><span class="sxs-lookup"><span data-stu-id="f1ba0-197">Concurrent access</span></span>

<span data-ttu-id="f1ba0-198">Pour prendre en charge les accès simultanés à un objet blob à partir de plusieurs clients ou de plusieurs instances de processus, vous pouvez utiliser **ETags** ou **baux**.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-198">To support concurrent access to a blob from multiple clients or multiple process instances, you can use **ETags** or **leases**.</span></span>

* <span data-ttu-id="f1ba0-199">**ETag** -offre un moyen de détecter que l’objet blob ou le conteneur a été modifié par un autre processus</span><span class="sxs-lookup"><span data-stu-id="f1ba0-199">**Etag** - provides a way to detect that the blob or container has been modified by another process</span></span>

* <span data-ttu-id="f1ba0-200">**Bail** -offre un moyen pour obtenir exclusif, renouvelable, écrire ou supprimer l’accès à un objet blob pour une période donnée</span><span class="sxs-lookup"><span data-stu-id="f1ba0-200">**Lease** - provides a way to obtain exclusive, renewable, write or delete access to a blob for a period of time</span></span>

<span data-ttu-id="f1ba0-201">Pour plus d’informations, consultez [la gestion de l’accès concurrentiel dans Microsoft Azure Storage](https://azure.microsoft.com/blog/managing-concurrency-in-microsoft-azure-storage-2/).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-201">For more information, see [Managing Concurrency in Microsoft Azure Storage](https://azure.microsoft.com/blog/managing-concurrency-in-microsoft-azure-storage-2/).</span></span>

## <a name="naming-containers"></a><span data-ttu-id="f1ba0-202">Conteneurs d’attribution</span><span class="sxs-lookup"><span data-stu-id="f1ba0-202">Naming containers</span></span>

<span data-ttu-id="f1ba0-203">Chaque objet blob dans le stockage Azure doit résider dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-203">Every blob in Azure storage must reside in a container.</span></span> <span data-ttu-id="f1ba0-204">Le conteneur fait partie du nom d’objet blob.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-204">The container forms part of the blob name.</span></span> <span data-ttu-id="f1ba0-205">Par exemple, `mydata` est le nom du conteneur dans ces objets blob d’exemple URI :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-205">For example, `mydata` is the name of the container in these sample blob URIs:</span></span>

    https://storagesample.blob.core.windows.net/mydata/blob1.txt
    https://storagesample.blob.core.windows.net/mydata/photos/myphoto.jpg

<span data-ttu-id="f1ba0-206">Un nom de conteneur doit être un nom DNS valide, conforme aux règles d’affectation de noms suivantes :</span><span class="sxs-lookup"><span data-stu-id="f1ba0-206">A container name must be a valid DNS name, conforming to the following naming rules:</span></span>

1. <span data-ttu-id="f1ba0-207">Les noms de conteneur doivent commencer par une lettre ou un chiffre et peuvent contenir uniquement des lettres, des chiffres et des tirets (-).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-207">Container names must start with a letter or number, and can contain only letters, numbers, and the dash (-) character.</span></span>
1. <span data-ttu-id="f1ba0-208">Chaque tiret (-) doit être immédiatement précédé et suivi par une lettre ou un chiffre ; tirets consécutifs ne sont pas autorisés dans les noms de conteneur.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-208">Every dash (-) character must be immediately preceded and followed by a letter or number; consecutive dashes are not permitted in container names.</span></span>
1. <span data-ttu-id="f1ba0-209">Toutes les lettres d’un nom de conteneur doivent être en minuscules.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-209">All letters in a container name must be lowercase.</span></span>
1. <span data-ttu-id="f1ba0-210">Les noms de conteneur doivent être compris entre 3 et 63 caractères.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-210">Container names must be from 3 through 63 characters long.</span></span>

<span data-ttu-id="f1ba0-211">Notez que le nom d’un conteneur doit toujours être en minuscules.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-211">Note that the name of a container must always be lowercase.</span></span> <span data-ttu-id="f1ba0-212">Si vous incluez une lettre majuscule dans un nom de conteneur ou violer les règles de nommage des conteneurs, vous pouvez recevoir une erreur 400 (demande incorrecte).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-212">If you include an upper-case letter in a container name, or otherwise violate the container naming rules, you may receive a 400 error (Bad Request).</span></span>

## <a name="managing-security-for-blobs"></a><span data-ttu-id="f1ba0-213">Gestion de la sécurité pour les objets BLOB</span><span class="sxs-lookup"><span data-stu-id="f1ba0-213">Managing security for blobs</span></span>

<span data-ttu-id="f1ba0-214">Par défaut, le stockage Azure conserve vos données sécurisées en limitant l’accès au propriétaire du compte, qui est en possession des clés d’accès au compte.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-214">By default, Azure Storage keeps your data secure by limiting access to the account owner, who is in possession of the account access keys.</span></span> <span data-ttu-id="f1ba0-215">Lorsque vous avez besoin de partager des données d’objet blob dans votre compte de stockage, il est important de le faire sans compromettre la sécurité de vos clés d’accès de compte.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-215">When you need to share blob data in your storage account, it is important to do so without compromising the security of your account access keys.</span></span> <span data-ttu-id="f1ba0-216">En outre, vous pouvez chiffrer les données d’objets blob pour vous assurer qu’elles sont sécurisées sur le réseau et dans le stockage Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-216">Additionally, you can encrypt blob data to ensure that it is secure going over the wire and in Azure Storage.</span></span>

### <a name="controlling-access-to-blob-data"></a><span data-ttu-id="f1ba0-217">Contrôler l’accès aux données d’objets blob</span><span class="sxs-lookup"><span data-stu-id="f1ba0-217">Controlling access to blob data</span></span>

<span data-ttu-id="f1ba0-218">Par défaut, les données blob dans votre compte de stockage sont accessibles uniquement au propriétaire de compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-218">By default, the blob data in your storage account is accessible only to storage account owner.</span></span> <span data-ttu-id="f1ba0-219">Authentification des demandes auprès de stockage d’objets Blob requiert la clé d’accès de compte par défaut.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-219">Authenticating requests against Blob storage requires the account access key by default.</span></span> <span data-ttu-id="f1ba0-220">Toutefois, vous souhaiterez rendre certaines données d’objets blob disponibles aux autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-220">However, you might want to make certain blob data available to other users.</span></span>

<span data-ttu-id="f1ba0-221">Pour plus d’informations sur la façon de contrôler l’accès pour le stockage d’objets blob, consultez [le guide de .NET pour la section de stockage d’objets blob sur le contrôle d’accès](/azure/storage/storage-dotnet-how-to-use-blobs#controlling-access-to-blob-data).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-221">For details on how to control access to blob storage, see [the .NET guide for blob storage section on access control](/azure/storage/storage-dotnet-how-to-use-blobs#controlling-access-to-blob-data).</span></span>


### <a name="encrypting-blob-data"></a><span data-ttu-id="f1ba0-222">Chiffrement des données d’objet blob</span><span class="sxs-lookup"><span data-stu-id="f1ba0-222">Encrypting blob data</span></span>

<span data-ttu-id="f1ba0-223">Stockage Azure prend en charge le chiffrement des données blob à la fois au niveau du client et sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-223">Azure Storage supports encrypting blob data both at the client and on the server.</span></span>

<span data-ttu-id="f1ba0-224">Pour plus d’informations sur le chiffrement des données blob, consultez [le guide de .NET pour la section de stockage d’objets blob sur le chiffrement](/azure/storage/storage-dotnet-how-to-use-blobs#encrypting-blob-data).</span><span class="sxs-lookup"><span data-stu-id="f1ba0-224">For details on encrypting blob data, see [the .NET guide for blob storage section on encryption](/azure/storage/storage-dotnet-how-to-use-blobs#encrypting-blob-data).</span></span>

## <a name="next-steps"></a><span data-ttu-id="f1ba0-225">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="f1ba0-225">Next steps</span></span>

<span data-ttu-id="f1ba0-226">Maintenant que vous avez appris les principes fondamentaux de stockage d’objets Blob, suivez ces liens pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-226">Now that you've learned the basics of Blob storage, follow these links to learn more.</span></span>

### <a name="tools"></a><span data-ttu-id="f1ba0-227">Outils</span><span class="sxs-lookup"><span data-stu-id="f1ba0-227">Tools</span></span>
- <span data-ttu-id="f1ba0-228">[F # AzureStorageTypeProvider](https://fsprojects.github.io/AzureStorageTypeProvider/) un fournisseur de Type F # qui peut être utilisé pour Explorer les ressources Blob, Table et file d’attente Azure Storage et d’appliquer facilement des opérations CRUD sur les.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-228">[F# AzureStorageTypeProvider](https://fsprojects.github.io/AzureStorageTypeProvider/) An F# Type Provider which can be used to explore Blob, Table and Queue Azure Storage assets and easily apply CRUD operations on them.</span></span>
- <span data-ttu-id="f1ba0-229">[FSharp.Azure.Storage](https://github.com/fsprojects/FSharp.Azure.Storage) F # API pour l’utilisation du service de stockage de Table Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="f1ba0-229">[FSharp.Azure.Storage](https://github.com/fsprojects/FSharp.Azure.Storage) An F# API for using Microsoft Azure Table Storage service</span></span>
- <span data-ttu-id="f1ba0-230">[Microsoft Azure Storage Explorer (MASE)](/azure/vs-azure-tools-storage-manage-with-storage-explorer) est une application autonome et gratuite de Microsoft qui vous permet d’exploiter visuellement les données de stockage Azure sur Windows, OS X et Linux.</span><span class="sxs-lookup"><span data-stu-id="f1ba0-230">[Microsoft Azure Storage Explorer (MASE)](/azure/vs-azure-tools-storage-manage-with-storage-explorer) is a free, standalone app from Microsoft that enables you to work visually with Azure Storage data on Windows, OS X, and Linux.</span></span>

### <a name="blob-storage-reference"></a><span data-ttu-id="f1ba0-231">Référence d’objet BLOB stockage</span><span class="sxs-lookup"><span data-stu-id="f1ba0-231">Blob storage reference</span></span>

- [<span data-ttu-id="f1ba0-232">API de stockage Azure pour .NET</span><span class="sxs-lookup"><span data-stu-id="f1ba0-232">Azure Storage APIs for .NET</span></span>](/dotnet/api/overview/azure/storage)
- [<span data-ttu-id="f1ba0-233">Référence de l’API REST des Services de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="f1ba0-233">Azure Storage Services REST API Reference</span></span>](/rest/api/storageservices/Azure-Storage-Services-REST-API-Reference)

### <a name="related-guides"></a><span data-ttu-id="f1ba0-234">Guides connexes</span><span class="sxs-lookup"><span data-stu-id="f1ba0-234">Related guides</span></span>

- [<span data-ttu-id="f1ba0-235">Prise en main stockage Blob Azure en c#</span><span class="sxs-lookup"><span data-stu-id="f1ba0-235">Getting Started with Azure Blob Storage in C#</span></span>](https://azure.microsoft.com/resources/samples/storage-blob-dotnet-getting-started/)
- [<span data-ttu-id="f1ba0-236">Transférer des données avec l’utilitaire de ligne de commande AzCopy sur Windows</span><span class="sxs-lookup"><span data-stu-id="f1ba0-236">Transfer data with the AzCopy command-line utility on Windows</span></span>](/azure/storage/common/storage-use-azcopy)
- [<span data-ttu-id="f1ba0-237">Transfert de données avec l’utilitaire de ligne de commande AzCopy sur Linux</span><span class="sxs-lookup"><span data-stu-id="f1ba0-237">Transfer data with the AzCopy command-line utility on Linux</span></span>](/azure/storage/common/storage-use-azcopy-linux)
- [<span data-ttu-id="f1ba0-238">Configurer les chaînes de connexion de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="f1ba0-238">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)
- [<span data-ttu-id="f1ba0-239">Blog de l’équipe stockage Azure</span><span class="sxs-lookup"><span data-stu-id="f1ba0-239">Azure Storage Team Blog</span></span>](https://blogs.msdn.microsoft.com/windowsazurestorage/)
