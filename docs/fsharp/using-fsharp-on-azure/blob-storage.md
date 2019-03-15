---
title: Prise en main stockage Blob Azure à l’aideF#
description: Store les données non structurées dans le cloud avec stockage Blob Azure.
author: sylvanc
ms.date: 09/20/2016
ms.openlocfilehash: 62178edf22ad48d0388f34488b68d135068d50a2
ms.sourcegitcommit: 69bf8b719d4c289eec7b45336d0b933dd7927841
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57846426"
---
# <a name="get-started-with-azure-blob-storage-using-f"></a>Prise en main stockage Blob Azure avec F\#

Le stockage Blob Azure est un service qui stocke les données non structurées dans le cloud en tant qu’objets/objets blob. Le stockage Blob permet de stocker n’importe quel type de données texte ou binaires, par exemple un document, un fichier multimédia ou un programme d’installation d’application. Le stockage Blob est également appelé stockage d’objets.

Cet article vous montre comment effectuer des tâches courantes à l’aide du stockage d’objets Blob. Les exemples sont écrits à l’aide de F# à l’aide de la bibliothèque cliente de stockage Azure pour .NET. Les tâches couvertes incluent comment télécharger, répertorier, télécharger et supprimer des objets BLOB.

Pour obtenir une vue d’ensemble conceptuelle de stockage d’objets blob, consultez [le guide de .NET pour le stockage blob](/azure/storage/storage-dotnet-how-to-use-blobs).

## <a name="prerequisites"></a>Prérequis

Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account). Vous devez également votre clé d’accès de stockage pour ce compte.

## <a name="create-an-f-script-and-start-f-interactive"></a>Créer un F# de Script et démarrer F# Interactive

Les exemples de cet article peuvent être utilisées dans un F# application ou un F# script. Pour créer un F# de script, créez un fichier avec le `.fsx` extension, par exemple `blobs.fsx`, dans votre F# environnement de développement.

Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` et `Microsoft.WindowsAzure.ConfigurationManager` packages et référence `WindowsAzure.Storage.dll` et `Microsoft.WindowsAzure.Configuration.dll` dans votre script à l’aide un `#r` directive.

### <a name="add-namespace-declarations"></a>Ajoutez les déclarations d’espace de noms

Ajoutez le code suivant `open` instructions au début de la `blobs.fsx` fichier :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L1-L5)]

### <a name="get-your-connection-string"></a>Obtenir votre chaîne de connexion

Vous avez besoin d’une chaîne de connexion de stockage Azure pour ce didacticiel. Pour plus d’informations sur les chaînes de connexion, consultez [configuration des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).

Pour ce didacticiel, vous entrez votre chaîne de connexion dans votre script, comme suit :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L11-L11)]

Toutefois, il s’agit de **déconseillé** projets de réel. Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage. Veillez toujours à protéger votre clé de compte de stockage. Évitez de la communiquer à d’autres utilisateurs, coder en dur, ou l’enregistrer dans un fichier texte brut qui n’est accessible à d’autres personnes. Vous pouvez régénérer votre clé à l’aide du portail Azure si vous pensez qu’il a peut-être été compromise.

Applications de réel, la meilleure façon de conserver votre chaîne de connexion de stockage est dans un fichier de configuration. Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L13-L15)]

L’utilisation d’Azure Configuration Manager est facultative. Vous pouvez également utiliser une API telle que du .NET Framework `ConfigurationManager` type.

### <a name="parse-the-connection-string"></a>Analyser la chaîne de connexion

Pour analyser la chaîne de connexion, utilisez :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L21-L22)]

Cette commande renvoie un `CloudStorageAccount`.

### <a name="create-some-local-dummy-data"></a>Créer des données factices locales

Avant de commencer, créez des données locales factices dans le répertoire de notre script. Plus tard, vous chargez ces données.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L28-L30)]

### <a name="create-the-blob-service-client"></a>Créer le client de service Blob

Le `CloudBlobClient` type vous permet de récupérer les conteneurs et objets BLOB stockés dans le stockage Blob. Voici une façon de créer le client du service :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L36-L36)]

Vous êtes maintenant prêt à écrire du code qui lit et écrit des données dans le stockage d’objets Blob.

## <a name="create-a-container"></a>Créer un conteneur

Cet exemple montre comment créer un conteneur si elle n’existe pas déjà :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L42-L46)]

Par défaut, le nouveau conteneur est privé, ce qui signifie que vous devez spécifier votre clé d’accès de stockage pour télécharger des objets BLOB à partir de ce conteneur. Si vous souhaitez mettre les fichiers dans le conteneur de disposition tout le monde, vous pouvez définir le conteneur public en utilisant le code suivant :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L48-L49)]

Quiconque sur Internet permettre afficher les objets BLOB dans un conteneur public, mais vous pouvez modifier ou les supprimer que si vous disposez de la clé d’accès de compte approprié ou une signature d’accès partagé.

## <a name="upload-a-blob-into-a-container"></a>Charger un objet blob dans un conteneur

Stockage d’objets Blob Azure prend en charge les objets BLOB de blocs et objets BLOB de pages. Dans la plupart des cas, un objet blob de blocs est le type recommandé à utiliser.

Pour télécharger un fichier à un objet blob de blocs, obtenez une référence de conteneur et utilisez-la pour obtenir une référence d’objet blob de bloc. Une fois que vous avez une référence d’objet blob, vous pouvez télécharger n’importe quel flux de données à ce dernier en appelant le `UploadFromFile` (méthode). Cette opération crée l’objet blob s’il n’a pas précédemment existe ou écraser s’il n’existe pas.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L55-L59)]

## <a name="list-the-blobs-in-a-container"></a>Répertorier les objets BLOB dans un conteneur

Pour répertorier les objets BLOB dans un conteneur, commencez par obtenir une référence de conteneur. Vous pouvez ensuite utiliser le conteneur `ListBlobs` méthode pour récupérer les objets BLOB et/ou les répertoires qu’il contient. Pour accéder à l’ensemble des propriétés et méthodes d’un `IListBlobItem`, vous devez le convertir en un `CloudBlockBlob`, `CloudPageBlob`, ou `CloudBlobDirectory` objet. Si le type est inconnu, vous pouvez utiliser une vérification de type pour déterminer quelle cible de l’appel. Le code suivant montre comment récupérer et générer l’URI de chaque élément dans le `mydata` conteneur :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L67-L80)]

Vous pouvez également des objets BLOB de nom avec les informations de chemin d’accès dans leurs noms. Cette opération crée une structure de répertoire virtuel que vous pouvez organiser et parcourir comme vous le feriez pour un système de fichiers traditionnel. Notez que la structure de répertoires est uniquement virtuelle : les seules ressources disponibles dans le stockage d’objets Blob sont des conteneurs et objets BLOB. Toutefois, la bibliothèque cliente storage propose un `CloudBlobDirectory` objet pour faire référence à un répertoire virtuel et simplifier le processus d’utilisation des objets BLOB sont organisés de cette façon.

Par exemple, prenez l’ensemble suivant d’objets BLOB de blocs dans un conteneur nommé `photos`:

*photo1.jpg*\
*2015/architecture/description.txt*\
*2015/architecture/photo3.jpg*\
*2015/architecture/photo4.jpg*\
*2016/architecture/photo5.jpg*\
*2016/architecture/photo6.jpg*\
*2016/architecture/description.txt*\
*2016/photo7.jpg*\

Lorsque vous appelez `ListBlobs` sur un conteneur (comme dans l’exemple ci-dessus), une liste hiérarchique est retournée. Si elle contient à la fois `CloudBlobDirectory` et `CloudBlockBlob` objets représentant les répertoires et les objets BLOB du conteneur, respectivement, puis le résultat ressemble à ceci :

```console
Directory: https://<accountname>.blob.core.windows.net/photos/2015/
Directory: https://<accountname>.blob.core.windows.net/photos/2016/
Block blob of length 505623: https://<accountname>.blob.core.windows.net/photos/photo1.jpg
```

Si vous le souhaitez, vous pouvez définir le `UseFlatBlobListing` paramètre de la `ListBlobs` méthode `true`. Dans ce cas, chaque objet blob dans le conteneur est retourné comme un `CloudBlockBlob` objet. L’appel à `ListBlobs` pour retourner une liste plate ressemble à ceci :

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L82-L89)]

et, en fonction du contenu actuel de votre conteneur, les résultats ressemblent à ceci :

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

## <a name="download-blobs"></a>Télécharger des objets BLOB

Pour télécharger des objets BLOB, commencez par récupérer une référence d’objet blob, puis appelez le `DownloadToStream` (méthode). L’exemple suivant utilise la `DownloadToStream` méthode pour transférer le contenu de l’objet blob vers un objet de flux persistant dans un fichier local.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L95-L101)]

Vous pouvez également utiliser le `DownloadToStream` méthode pour télécharger le contenu d’un objet blob comme une chaîne de texte.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L103-L106)]

## <a name="delete-blobs"></a>Supprimer des objets BLOB

Pour supprimer un objet blob, commencez par obtenir une référence d’objet blob, puis appelez le `Delete` méthode dessus.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L112-L116)]

## <a name="list-blobs-in-pages-asynchronously"></a>Répertorier les objets BLOB dans les pages de façon asynchrone

Si vous répertoriez un grand nombre d’objets BLOB, ou si vous souhaitez contrôler le nombre de résultats renvoyés dans une opération de liste, vous pouvez répertorier les objets BLOB dans les pages de résultats. Cet exemple montre comment renvoyer des résultats dans des pages en mode asynchrone, afin que l’exécution n’est pas bloquée lors de l’attente pour renvoyer un grand ensemble de résultats.

Cet exemple montre une liste plate d’objets blob, mais vous pouvez également effectuer une liste hiérarchique, en définissant le `useFlatBlobListing` paramètre de la `ListBlobsSegmentedAsync` méthode `false`.

L’exemple définit une méthode asynchrone, à l’aide un `async` bloc. Le ``let!`` mot clé suspend l’exécution de l’exemple de méthode jusqu'à ce que la tâche de la liste se termine.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L122-L160)]

Nous pouvons maintenant utiliser cette routine asynchrone comme suit. Tout d’abord vous chargez des données factices (en utilisant le fichier local créé précédemment dans ce didacticiel).

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L162-L166)]

À présent, appelez la routine. Vous utilisez `Async.RunSynchronously` pour forcer l’exécution de l’opération asynchrone.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L168-L168)]

## <a name="writing-to-an-append-blob"></a>Écriture dans un objet blob d’ajout

Un objet blob d’ajout est optimisé pour les opérations d’ajout, telles que la journalisation. Comme un objet blob de blocs, un objet blob d’ajout est constitué de blocs, mais lorsque vous ajoutez un nouveau bloc à un objet blob d’ajout, elle est toujours ajoutée à la fin de l’objet blob. Vous ne pouvez pas mettre à jour ou supprimer un bloc dans un objet blob d’ajout. L’ID de bloc pour un objet blob d’ajout ne sont pas exposés comme ils le sont pour un objet blob de blocs.

Chaque bloc dans un objet blob d’ajout peut avoir une taille différente, avec un maximum de 4 Mo, et un objet blob d’ajout peut inclure un maximum de 50 000 blocs. La taille maximale d’un objet blob d’ajout est donc légèrement supérieure à 195 Go (4 Mo X 50 000 blocs).

L’exemple suivant crée un objet blob d’ajout et y ajoute des données, simulation d’une opération de journalisation simple.

[!code-fsharp[BlobStorage](../../../samples/snippets/fsharp/azure/blob-storage.fsx#L174-L203)]

Consultez [objets BLOB de blocs, objets BLOB de pages et objets BLOB d’ajout](https://msdn.microsoft.com/library/azure/ee691964.aspx) pour plus d’informations sur les différences entre les trois types d’objets BLOB.

## <a name="concurrent-access"></a>Accès simultané

Pour prendre en charge les accès simultanés à un objet blob à partir de plusieurs clients ou de plusieurs instances de processus, vous pouvez utiliser **ETags** ou **baux**.

* **ETag** -offre un moyen de détecter que l’objet blob ou le conteneur a été modifié par un autre processus

* **Bail** -offre un moyen pour obtenir exclusif, renouvelable, écrire ou supprimer l’accès à un objet blob pour une période donnée

Pour plus d’informations, consultez [la gestion de l’accès concurrentiel dans Microsoft Azure Storage](https://azure.microsoft.com/blog/managing-concurrency-in-microsoft-azure-storage-2/).

## <a name="naming-containers"></a>Conteneurs d’attribution

Chaque objet blob dans le stockage Azure doit résider dans un conteneur. Le conteneur fait partie du nom d’objet blob. Par exemple, `mydata` est le nom du conteneur dans ces objets blob d’exemple URI :

    https://storagesample.blob.core.windows.net/mydata/blob1.txt
    https://storagesample.blob.core.windows.net/mydata/photos/myphoto.jpg

Un nom de conteneur doit être un nom DNS valide, conforme aux règles d’affectation de noms suivantes :

1. Les noms de conteneur doivent commencer par une lettre ou un chiffre et peuvent contenir uniquement des lettres, des chiffres et des tirets (-).
1. Chaque tiret (-) doit être immédiatement précédé et suivi par une lettre ou un chiffre ; tirets consécutifs ne sont pas autorisés dans les noms de conteneur.
1. Toutes les lettres d’un nom de conteneur doivent être en minuscules.
1. Les noms de conteneur doivent être compris entre 3 et 63 caractères.

Notez que le nom d’un conteneur doit toujours être en minuscules. Si vous incluez une lettre majuscule dans un nom de conteneur ou violer les règles de nommage des conteneurs, vous pouvez recevoir une erreur 400 (demande incorrecte).

## <a name="managing-security-for-blobs"></a>Gestion de la sécurité pour les objets BLOB

Par défaut, le stockage Azure conserve vos données sécurisées en limitant l’accès au propriétaire du compte, qui est en possession des clés d’accès au compte. Lorsque vous avez besoin de partager des données d’objet blob dans votre compte de stockage, il est important de le faire sans compromettre la sécurité de vos clés d’accès de compte. En outre, vous pouvez chiffrer les données d’objets blob pour vous assurer qu’elles sont sécurisées sur le réseau et dans le stockage Azure.

### <a name="controlling-access-to-blob-data"></a>Contrôler l’accès aux données d’objets blob

Par défaut, les données blob dans votre compte de stockage sont accessibles uniquement au propriétaire de compte de stockage. Authentification des demandes auprès de stockage d’objets Blob requiert la clé d’accès de compte par défaut. Toutefois, vous souhaiterez rendre certaines données d’objets blob disponibles aux autres utilisateurs.

### <a name="encrypting-blob-data"></a>Chiffrement des données d’objet blob

Stockage Azure prend en charge le chiffrement des données blob à la fois au niveau du client et sur le serveur.

## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous avez appris les principes fondamentaux de stockage d’objets Blob, suivez ces liens pour en savoir plus.

### <a name="tools"></a>Outils

- [F#AzureStorageTypeProvider](https://fsprojects.github.io/AzureStorageTypeProvider/)\
Un F# fournisseur de Type qui peut être utilisé pour Explorer les ressources Blob, Table et file d’attente Azure Storage et appliquer facilement des opérations CRUD sur ces derniers.

- [FSharp.Azure.Storage](https://github.com/fsprojects/FSharp.Azure.Storage)\
Un F# API pour l’utilisation du service de stockage de Table Microsoft Azure

- [Microsoft Azure Storage Explorer (MASE)](/azure/vs-azure-tools-storage-manage-with-storage-explorer)\
Une application autonome et gratuite de Microsoft qui vous permet d’exploiter visuellement les données de stockage Azure sur Windows, OS X et Linux.

### <a name="blob-storage-reference"></a>Référence d’objet BLOB stockage

- [API de stockage Azure pour .NET](/dotnet/api/overview/azure/storage)
- [Référence de l’API REST des Services de stockage Azure](/rest/api/storageservices/Azure-Storage-Services-REST-API-Reference)

### <a name="related-guides"></a>Guides connexes

- [Prise en main stockage Blob Azure en c#](https://azure.microsoft.com/resources/samples/storage-blob-dotnet-getting-started/)
- [Transférer des données avec l’utilitaire de ligne de commande AzCopy sur Windows](/azure/storage/common/storage-use-azcopy)
- [Transfert de données avec l’utilitaire de ligne de commande AzCopy sur Linux](/azure/storage/common/storage-use-azcopy-linux)
- [Configurer les chaînes de connexion de stockage Azure](/azure/storage/common/storage-configure-connection-string)
- [Blog de l’équipe stockage Azure](https://blogs.msdn.microsoft.com/windowsazurestorage/)
- [Démarrage rapide : Utiliser .NET pour créer un objet blob dans le stockage d’objets](/azure/storage/blobs/storage-quickstart-blobs-dotnet)
