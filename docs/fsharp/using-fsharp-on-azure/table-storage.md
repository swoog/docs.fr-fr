---
title: Prise en main à l’aide du stockage Table AzureF#
description: Store données structurées dans le cloud à l’aide du stockage Table Azure ou Azure Cosmos DB.
author: sylvanc
ms.date: 03/26/2018
ms.openlocfilehash: 2b74a33023065ea809c2d7eb6202b1a254018422
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966006"
---
# <a name="get-started-with-azure-table-storage-and-the-azure-cosmos-db-table-api-using-f"></a><span data-ttu-id="a67c4-103">Bien démarrer avec stockage Table Azure et l’API de Table Azure Cosmos DB à l’aide de F\#</span><span class="sxs-lookup"><span data-stu-id="a67c4-103">Get started with Azure Table storage and the Azure Cosmos DB Table API using F\#</span></span>

<span data-ttu-id="a67c4-104">Stockage Table Azure est un service qui stocke des données NoSQL structurées dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="a67c4-104">Azure Table storage is a service that stores structured NoSQL data in the cloud.</span></span> <span data-ttu-id="a67c4-105">Stockage de table est un magasin de clés/attributs doté d’une conception sans schéma.</span><span class="sxs-lookup"><span data-stu-id="a67c4-105">Table storage is a key/attribute store with a schemaless design.</span></span> <span data-ttu-id="a67c4-106">Étant donné que le stockage de tables est sans schéma, il est facile d’adapter vos données en tant que l’évolution des besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="a67c4-106">Because Table storage is schemaless, it's easy to adapt your data as the needs of your application evolve.</span></span> <span data-ttu-id="a67c4-107">Accès aux données est rapide et économique pour toutes sortes d’applications.</span><span class="sxs-lookup"><span data-stu-id="a67c4-107">Access to data is fast and cost-effective for all kinds of applications.</span></span> <span data-ttu-id="a67c4-108">Stockage table est généralement beaucoup moins coûteux que le SQL traditionnel pour des volumes de données similaires.</span><span class="sxs-lookup"><span data-stu-id="a67c4-108">Table storage is typically significantly lower in cost than traditional SQL for similar volumes of data.</span></span>

<span data-ttu-id="a67c4-109">Vous pouvez utiliser le stockage de Table pour stocker des jeux de données flexibles, telles que les données utilisateur pour les applications web, carnets d’adresses, informations sur l’appareil et tout autre type de métadonnées nécessaires à votre service.</span><span class="sxs-lookup"><span data-stu-id="a67c4-109">You can use Table storage to store flexible datasets, such as user data for web applications, address books, device information, and any other type of metadata that your service requires.</span></span> <span data-ttu-id="a67c4-110">Vous pouvez stocker n’importe quel nombre d’entités dans une table, et un compte de stockage peut contenir un nombre quelconque de tables, jusqu'à la limite de capacité du compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="a67c4-110">You can store any number of entities in a table, and a storage account may contain any number of tables, up to the capacity limit of the storage account.</span></span>

<span data-ttu-id="a67c4-111">Azure Cosmos DB fournit l’API de Table pour les applications qui sont écrites pour le stockage Table Azure et qui nécessitent des fonctionnalités premium telles que :</span><span class="sxs-lookup"><span data-stu-id="a67c4-111">Azure Cosmos DB provides the Table API for applications that are written for Azure Table storage and that require premium capabilities such as:</span></span>

- <span data-ttu-id="a67c4-112">Une distribution mondiale.</span><span class="sxs-lookup"><span data-stu-id="a67c4-112">Turnkey global distribution.</span></span>
- <span data-ttu-id="a67c4-113">Débit dédié dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="a67c4-113">Dedicated throughput worldwide.</span></span>
- <span data-ttu-id="a67c4-114">Temps de latence en quelques millisecondes au 99e centile.</span><span class="sxs-lookup"><span data-stu-id="a67c4-114">Single-digit millisecond latencies at the 99th percentile.</span></span>
- <span data-ttu-id="a67c4-115">Haute disponibilité garantie.</span><span class="sxs-lookup"><span data-stu-id="a67c4-115">Guaranteed high availability.</span></span>
- <span data-ttu-id="a67c4-116">L’indexation automatique secondaire.</span><span class="sxs-lookup"><span data-stu-id="a67c4-116">Automatic secondary indexing.</span></span>

<span data-ttu-id="a67c4-117">Les applications écrites pour le stockage Table Azure peuvent migrer vers Azure Cosmos DB à l’aide de l’API de Table sans aucune modification de code et tirer parti des fonctionnalités premium.</span><span class="sxs-lookup"><span data-stu-id="a67c4-117">Applications written for Azure Table storage can migrate to Azure Cosmos DB by using the Table API with no code changes and take advantage of premium capabilities.</span></span> <span data-ttu-id="a67c4-118">L’API de Table a des kits pour .NET, Java, Python et Node.js.</span><span class="sxs-lookup"><span data-stu-id="a67c4-118">The Table API has client SDKs available for .NET, Java, Python, and Node.js.</span></span>

<span data-ttu-id="a67c4-119">Pour plus d’informations, consultez [Introduction à l’API de Table Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/table-introduction).</span><span class="sxs-lookup"><span data-stu-id="a67c4-119">For more information, see [Introduction to Azure Cosmos DB Table API](https://docs.microsoft.com/azure/cosmos-db/table-introduction).</span></span>

## <a name="about-this-tutorial"></a><span data-ttu-id="a67c4-120">À propos de ce didacticiel</span><span class="sxs-lookup"><span data-stu-id="a67c4-120">About this tutorial</span></span>

<span data-ttu-id="a67c4-121">Ce didacticiel montre comment écrire F# code pour effectuer certaines tâches courantes à l’aide du stockage Table Azure ou l’API Azure Cosmos DB Table, y compris la création et suppression d’une table et insertion de la mise à jour, suppression et interrogation des données de table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-121">This tutorial shows how to write F# code to do some common tasks using Azure Table storage or the Azure Cosmos DB Table API, including creating and deleting a table and inserting, updating, deleting, and querying table data.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a67c4-122">Prérequis</span><span class="sxs-lookup"><span data-stu-id="a67c4-122">Prerequisites</span></span>

<span data-ttu-id="a67c4-123">Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account) ou [compte Azure Cosmos DB](https://azure.microsoft.com/try/cosmosdb/).</span><span class="sxs-lookup"><span data-stu-id="a67c4-123">To use this guide, you must first [create an Azure storage account](/azure/storage/storage-create-storage-account) or [Azure Cosmos DB account](https://azure.microsoft.com/try/cosmosdb/).</span></span>


## <a name="create-an-f-script-and-start-f-interactive"></a><span data-ttu-id="a67c4-124">Créer un F# de Script et démarrer F# Interactive</span><span class="sxs-lookup"><span data-stu-id="a67c4-124">Create an F# Script and Start F# Interactive</span></span>

<span data-ttu-id="a67c4-125">Les exemples de cet article peuvent être utilisées dans un F# application ou un F# script.</span><span class="sxs-lookup"><span data-stu-id="a67c4-125">The samples in this article can be used in either an F# application or an F# script.</span></span> <span data-ttu-id="a67c4-126">Pour créer un F# de script, créez un fichier avec le `.fsx` extension, par exemple `tables.fsx`, dans votre F# environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="a67c4-126">To create an F# script, create a file with the `.fsx` extension, for example `tables.fsx`, in your F# development environment.</span></span>

<span data-ttu-id="a67c4-127">Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` package et référence `WindowsAzure.Storage.dll` dans votre script à l’aide d’un `#r`directive.</span><span class="sxs-lookup"><span data-stu-id="a67c4-127">Next, use a [package manager](package-management.md) such as [Paket](https://fsprojects.github.io/Paket/) or [NuGet](https://www.nuget.org/) to install the `WindowsAzure.Storage` package and reference `WindowsAzure.Storage.dll` in your script using a `#r` directive.</span></span> <span data-ttu-id="a67c4-128">Effectuez à nouveau pour `Microsoft.WindowsAzure.ConfigurationManager` afin d’obtenir de l’espace de noms Microsoft.Azure.</span><span class="sxs-lookup"><span data-stu-id="a67c4-128">Do it again for `Microsoft.WindowsAzure.ConfigurationManager` in order to get the Microsoft.Azure namespace.</span></span>

### <a name="add-namespace-declarations"></a><span data-ttu-id="a67c4-129">Ajoutez les déclarations d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="a67c4-129">Add namespace declarations</span></span>

<span data-ttu-id="a67c4-130">Ajoutez le code suivant `open` instructions au début de la `tables.fsx` fichier :</span><span class="sxs-lookup"><span data-stu-id="a67c4-130">Add the following `open` statements to the top of the `tables.fsx` file:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L1-L5)]

### <a name="get-your-azure-storage-connection-string"></a><span data-ttu-id="a67c4-131">Obtenir votre chaîne de connexion de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="a67c4-131">Get your Azure Storage connection string</span></span>

<span data-ttu-id="a67c4-132">Si vous vous connectez au service de Table de stockage Azure, vous aurez besoin de votre chaîne de connexion pour ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="a67c4-132">If you're connecting to Azure Storage Table service, you'll need your connection string for this tutorial.</span></span> <span data-ttu-id="a67c4-133">Vous pouvez copier votre chaîne de connexion à partir du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="a67c4-133">You can copy your connection string from the Azure portal.</span></span> <span data-ttu-id="a67c4-134">Pour plus d’informations sur les chaînes de connexion, consultez [configuration des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).</span><span class="sxs-lookup"><span data-stu-id="a67c4-134">For more information about connection strings, see [Configure Storage Connection Strings](/azure/storage/storage-configure-connection-string).</span></span>

### <a name="get-your-azure-cosmos-db-connection-string"></a><span data-ttu-id="a67c4-135">Obtenir votre chaîne de connexion Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="a67c4-135">Get your Azure Cosmos DB connection string</span></span>

<span data-ttu-id="a67c4-136">Si vous vous connectez à Azure Cosmos DB, vous aurez besoin de votre chaîne de connexion pour ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="a67c4-136">If you're connecting to Azure Cosmos DB, you'll need your connection string for this tutorial.</span></span> <span data-ttu-id="a67c4-137">Vous pouvez copier votre chaîne de connexion à partir du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="a67c4-137">You can copy your connection string from the Azure portal.</span></span> <span data-ttu-id="a67c4-138">Dans le portail Azure, dans votre compte Cosmos DB, accédez à **paramètres** > **chaîne de connexion**, puis cliquez sur le **copie** bouton pour copier votre connexion principale Chaîne.</span><span class="sxs-lookup"><span data-stu-id="a67c4-138">In the Azure portal, in your Cosmos DB account, go to **Settings** > **Connection String**, and click the **Copy** button to copy your Primary Connection String.</span></span> 

<span data-ttu-id="a67c4-139">Pour ce didacticiel, entrez votre chaîne de connexion dans votre script, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="a67c4-139">For the tutorial, enter your connection string in your script, like the following example:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L11-L11)]

<span data-ttu-id="a67c4-140">Toutefois, il s’agit de **déconseillé** projets de réel.</span><span class="sxs-lookup"><span data-stu-id="a67c4-140">However, this is **not recommended** for real projects.</span></span> <span data-ttu-id="a67c4-141">Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="a67c4-141">Your storage account key is similar to the root password for your storage account.</span></span> <span data-ttu-id="a67c4-142">Veillez toujours à protéger votre clé de compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="a67c4-142">Always be careful to protect your storage account key.</span></span> <span data-ttu-id="a67c4-143">Évitez de la communiquer à d’autres utilisateurs, coder en dur, ou l’enregistrer dans un fichier texte brut qui n’est accessible à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="a67c4-143">Avoid distributing it to other users, hard-coding it, or saving it in a plain-text file that is accessible to others.</span></span> <span data-ttu-id="a67c4-144">Vous pouvez régénérer votre clé à l’aide du portail Azure si vous pensez qu’il a peut-être été compromise.</span><span class="sxs-lookup"><span data-stu-id="a67c4-144">You can regenerate your key using the Azure Portal if you believe it may have been compromised.</span></span>

<span data-ttu-id="a67c4-145">Applications de réel, la meilleure façon de conserver votre chaîne de connexion de stockage est dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="a67c4-145">For real applications, the best way to maintain your storage connection string is in a configuration file.</span></span> <span data-ttu-id="a67c4-146">Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :</span><span class="sxs-lookup"><span data-stu-id="a67c4-146">To fetch the connection string from a configuration file, you can do this:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L13-L15)]

<span data-ttu-id="a67c4-147">L’utilisation d’Azure Configuration Manager est facultative.</span><span class="sxs-lookup"><span data-stu-id="a67c4-147">Using Azure Configuration Manager is optional.</span></span> <span data-ttu-id="a67c4-148">Vous pouvez également utiliser une API telle que du .NET Framework `ConfigurationManager` type.</span><span class="sxs-lookup"><span data-stu-id="a67c4-148">You can also use an API such as the .NET Framework's `ConfigurationManager` type.</span></span>

### <a name="parse-the-connection-string"></a><span data-ttu-id="a67c4-149">Analyser la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="a67c4-149">Parse the connection string</span></span>

<span data-ttu-id="a67c4-150">Pour analyser la chaîne de connexion, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a67c4-150">To parse the connection string, use:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L21-L22)]

<span data-ttu-id="a67c4-151">Cette commande renvoie un `CloudStorageAccount`.</span><span class="sxs-lookup"><span data-stu-id="a67c4-151">This returns a `CloudStorageAccount`.</span></span>

### <a name="create-the-table-service-client"></a><span data-ttu-id="a67c4-152">Créer le client de service de Table</span><span class="sxs-lookup"><span data-stu-id="a67c4-152">Create the Table service client</span></span>

<span data-ttu-id="a67c4-153">Le `CloudTableClient` classe vous permet de récupérer des tables et des entités dans le stockage Table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-153">The `CloudTableClient` class enables you to retrieve tables and entities in Table storage.</span></span> <span data-ttu-id="a67c4-154">Voici une façon de créer le client du service :</span><span class="sxs-lookup"><span data-stu-id="a67c4-154">Here's one way to create the service client:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L28-L29)]

<span data-ttu-id="a67c4-155">Vous êtes maintenant prêt à écrire du code qui lit et écrit des données dans le stockage Table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-155">Now you are ready to write code that reads data from and writes data to Table storage.</span></span>

### <a name="create-a-table"></a><span data-ttu-id="a67c4-156">Créer une table</span><span class="sxs-lookup"><span data-stu-id="a67c4-156">Create a table</span></span>

<span data-ttu-id="a67c4-157">Cet exemple montre comment créer une table si elle n’existe pas déjà :</span><span class="sxs-lookup"><span data-stu-id="a67c4-157">This example shows how to create a table if it does not already exist:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L35-L39)]

### <a name="add-an-entity-to-a-table"></a><span data-ttu-id="a67c4-158">Ajouter une entité à une table</span><span class="sxs-lookup"><span data-stu-id="a67c4-158">Add an entity to a table</span></span>

<span data-ttu-id="a67c4-159">Une entité doit avoir un type qui hérite de `TableEntity`.</span><span class="sxs-lookup"><span data-stu-id="a67c4-159">An entity has to have a type that inherits from `TableEntity`.</span></span> <span data-ttu-id="a67c4-160">Vous pouvez étendre `TableEntity` dans comme vous le souhaitez, mais votre type *doit* avoir un constructeur sans paramètre.</span><span class="sxs-lookup"><span data-stu-id="a67c4-160">You can extend `TableEntity` in any way you like, but your type *must* have a parameter-less constructor.</span></span> <span data-ttu-id="a67c4-161">Seules les propriétés qui ont les deux `get` et `set` sont stockés dans votre Table Azure.</span><span class="sxs-lookup"><span data-stu-id="a67c4-161">Only properties that have both `get` and `set` are stored in your Azure Table.</span></span>

<span data-ttu-id="a67c4-162">Partition de l’entité et la clé de ligne identifient de manière unique l’entité dans la table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-162">An entity's partition and row key uniquely identify the entity in the table.</span></span> <span data-ttu-id="a67c4-163">Entités avec la même clé de partition peuvent être interrogées plus rapides que celles avec des clés de partition différente, mais à l’aide de différentes clés de partition permet une plus grande évolutivité d’opérations parallèles.</span><span class="sxs-lookup"><span data-stu-id="a67c4-163">Entities with the same partition key can be queried faster than those with different partition keys, but using diverse partition keys allows for greater scalability of parallel operations.</span></span>

<span data-ttu-id="a67c4-164">Voici un exemple d’un `Customer` qui utilise le `lastName` comme clé de partition et le `firstName` comme clé de ligne.</span><span class="sxs-lookup"><span data-stu-id="a67c4-164">Here's an example of a `Customer` that uses the `lastName` as the partition key and the `firstName` as the row key.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L45-L52)]

<span data-ttu-id="a67c4-165">Ajoutez maintenant `Customer` à la table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-165">Now add `Customer` to the table.</span></span> <span data-ttu-id="a67c4-166">Pour ce faire, créez un `TableOperation` qui s’exécute sur la table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-166">To do so, create a `TableOperation` that executes on the table.</span></span> <span data-ttu-id="a67c4-167">Dans ce cas, vous créez un `Insert` opération.</span><span class="sxs-lookup"><span data-stu-id="a67c4-167">In this case, you create an `Insert` operation.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L54-L55)]

### <a name="insert-a-batch-of-entities"></a><span data-ttu-id="a67c4-168">Insérer un lot d’entités</span><span class="sxs-lookup"><span data-stu-id="a67c4-168">Insert a batch of entities</span></span>

<span data-ttu-id="a67c4-169">Vous pouvez insérer un lot d’entités dans une table à l’aide d’une seule opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="a67c4-169">You can insert a batch of entities into a table using a single write operation.</span></span> <span data-ttu-id="a67c4-170">Autorisent les opérations par lots vous permet de combiner des opérations en une seule exécution, mais ils présentent quelques restrictions :</span><span class="sxs-lookup"><span data-stu-id="a67c4-170">Batch operations allow you to combine operations into a single execution, but they have some restrictions:</span></span>

- <span data-ttu-id="a67c4-171">Vous pouvez effectuer des mises à jour, suppressions et des insertions dans la même opération de traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="a67c4-171">You can perform updates, deletes, and inserts in the same batch operation.</span></span>
- <span data-ttu-id="a67c4-172">Une opération par lot peut inclure jusqu'à 100 entités.</span><span class="sxs-lookup"><span data-stu-id="a67c4-172">A batch operation can include up to 100 entities.</span></span>
- <span data-ttu-id="a67c4-173">Toutes les entités dans une opération par lot doivent avoir la même clé de partition.</span><span class="sxs-lookup"><span data-stu-id="a67c4-173">All entities in a batch operation must have the same partition key.</span></span>
- <span data-ttu-id="a67c4-174">Bien qu’il soit possible d’effectuer une requête dans une opération par lot, il doit être la seule opération dans le lot.</span><span class="sxs-lookup"><span data-stu-id="a67c4-174">While it is possible to perform a query in a batch operation, it must be the only operation in the batch.</span></span>

<span data-ttu-id="a67c4-175">Voici un code qui associe deux insertions dans une opération par lot :</span><span class="sxs-lookup"><span data-stu-id="a67c4-175">Here's some code that combines two inserts into a batch operation:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L62-L71)]

### <a name="retrieve-all-entities-in-a-partition"></a><span data-ttu-id="a67c4-176">Récupérer toutes les entités dans une partition</span><span class="sxs-lookup"><span data-stu-id="a67c4-176">Retrieve all entities in a partition</span></span>

<span data-ttu-id="a67c4-177">Pour interroger une table pour toutes les entités dans une partition, utilisez un `TableQuery` objet.</span><span class="sxs-lookup"><span data-stu-id="a67c4-177">To query a table for all entities in a partition, use a `TableQuery` object.</span></span> <span data-ttu-id="a67c4-178">Ici, vous filtrez pour les entités dont « Smith » est la clé de partition.</span><span class="sxs-lookup"><span data-stu-id="a67c4-178">Here, you filter for entities where "Smith" is the partition key.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L77-L82)]

<span data-ttu-id="a67c4-179">Maintenant, vous imprimez les résultats :</span><span class="sxs-lookup"><span data-stu-id="a67c4-179">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L84-L85)]


### <a name="retrieve-a-range-of-entities-in-a-partition"></a><span data-ttu-id="a67c4-180">Récupérer un ensemble d’entités dans une partition</span><span class="sxs-lookup"><span data-stu-id="a67c4-180">Retrieve a range of entities in a partition</span></span>

<span data-ttu-id="a67c4-181">Si vous ne souhaitez pas interroger toutes les entités dans une partition, vous pouvez spécifier une plage en combinant le filtre de clé de partition avec un filtre de clé de ligne.</span><span class="sxs-lookup"><span data-stu-id="a67c4-181">If you don't want to query all the entities in a partition, you can specify a range by combining the partition key filter with a row key filter.</span></span> <span data-ttu-id="a67c4-182">Ici, vous utilisez des deux filtres pour obtenir toutes les entités dans la partition « Smith » où la clé de ligne (prénom) commence par une lettre antérieure à « M » dans l’alphabet.</span><span class="sxs-lookup"><span data-stu-id="a67c4-182">Here, you use two filters to get all entities in the "Smith" partition where the row key (first name) starts with a letter earlier than "M" in the alphabet.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L91-L100)]

<span data-ttu-id="a67c4-183">Maintenant, vous imprimez les résultats :</span><span class="sxs-lookup"><span data-stu-id="a67c4-183">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L102-L103)]

### <a name="retrieve-a-single-entity"></a><span data-ttu-id="a67c4-184">Extraire une seule entité</span><span class="sxs-lookup"><span data-stu-id="a67c4-184">Retrieve a single entity</span></span>

<span data-ttu-id="a67c4-185">Vous pouvez écrire une requête pour récupérer une entité unique.</span><span class="sxs-lookup"><span data-stu-id="a67c4-185">You can write a query to retrieve a single, specific entity.</span></span> <span data-ttu-id="a67c4-186">Ici, vous utilisez un `TableOperation` pour spécifier le client « Ben Smith ».</span><span class="sxs-lookup"><span data-stu-id="a67c4-186">Here, you use a `TableOperation` to specify the customer "Ben Smith".</span></span> <span data-ttu-id="a67c4-187">Au lieu d’une collection, vous obtenez en retour un `Customer`.</span><span class="sxs-lookup"><span data-stu-id="a67c4-187">Instead of a collection, you get back a `Customer`.</span></span> <span data-ttu-id="a67c4-188">Spécification de la clé de partition et la clé de ligne dans une requête est le moyen le plus rapide pour récupérer une entité unique à partir du service de Table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-188">Specifying both the partition key and the row key in a query is the fastest way to retrieve a single entity from the Table service.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L109-L111)]

<span data-ttu-id="a67c4-189">Maintenant, vous imprimez les résultats :</span><span class="sxs-lookup"><span data-stu-id="a67c4-189">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L113-L115)]


### <a name="replace-an-entity"></a><span data-ttu-id="a67c4-190">Remplacer une entité</span><span class="sxs-lookup"><span data-stu-id="a67c4-190">Replace an entity</span></span>

<span data-ttu-id="a67c4-191">Pour mettre à jour une entité, récupérez-la du service de Table, modifiez l’objet d’entité, puis enregistrez les modifications vers le service de Table à l’aide un `Replace` opération.</span><span class="sxs-lookup"><span data-stu-id="a67c4-191">To update an entity, retrieve it from the Table service, modify the entity object, and then save the changes back to the Table service using a `Replace` operation.</span></span> <span data-ttu-id="a67c4-192">Cela entraîne l’entité à remplacer entièrement sur le serveur, sauf si l’entité sur le serveur a changé depuis sa récupération, auquel cas l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="a67c4-192">This causes the entity to be fully replaced on the server, unless the entity on the server has changed since it was retrieved, in which case the operation fails.</span></span> <span data-ttu-id="a67c4-193">Cet échec survient pour empêcher votre application de remplacer par inadvertance les modifications provenant d’autres sources.</span><span class="sxs-lookup"><span data-stu-id="a67c4-193">This failure is to prevent your application from inadvertently overwriting changes from other sources.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L121-L128)]

### <a name="insert-or-replace-an-entity"></a><span data-ttu-id="a67c4-194">Insérer ou remplacer une entité</span><span class="sxs-lookup"><span data-stu-id="a67c4-194">Insert-or-replace an entity</span></span>

<span data-ttu-id="a67c4-195">Parfois, vous ne connaissez pas si une entité existe dans la table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-195">Sometimes, you don't know whether an entity exists in the table.</span></span> <span data-ttu-id="a67c4-196">Et, le cas échéant, les valeurs actuelles stockées qu’il contient ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a67c4-196">And if it does, the current values stored in it are no longer needed.</span></span> <span data-ttu-id="a67c4-197">Vous pouvez utiliser `InsertOrReplace` pour créer l’entité, ou remplacez-la si elle existe, quel que soit son état.</span><span class="sxs-lookup"><span data-stu-id="a67c4-197">You can use `InsertOrReplace` to create the entity, or replace it if it exists, regardless of its state.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L134-L141)]

### <a name="query-a-subset-of-entity-properties"></a><span data-ttu-id="a67c4-198">Interroger un sous-ensemble des propriétés de l’entité</span><span class="sxs-lookup"><span data-stu-id="a67c4-198">Query a subset of entity properties</span></span>

<span data-ttu-id="a67c4-199">Une requête de table peut récupérer uniquement quelques propriétés d’une entité et non la totalité d'entre eux.</span><span class="sxs-lookup"><span data-stu-id="a67c4-199">A table query can retrieve just a few properties from an entity instead of all of them.</span></span> <span data-ttu-id="a67c4-200">Cette technique, appelée projection, peut améliorer les performances des requêtes, en particulier pour les entités volumineuses.</span><span class="sxs-lookup"><span data-stu-id="a67c4-200">This technique, called projection, can improve query performance, especially for large entities.</span></span> <span data-ttu-id="a67c4-201">Ici, vous revenez à l’aide des adresses e-mail uniquement `DynamicTableEntity` et `EntityResolver`.</span><span class="sxs-lookup"><span data-stu-id="a67c4-201">Here, you return only email addresses using `DynamicTableEntity` and `EntityResolver`.</span></span> <span data-ttu-id="a67c4-202">Notez que la projection n’est pas pris en charge sur l’émulateur de stockage local, ce code s’exécute donc uniquement si vous utilisez un compte sur le service de Table.</span><span class="sxs-lookup"><span data-stu-id="a67c4-202">Note that projection is not supported on the local storage emulator, so this code runs only when you're using an account on the Table service.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L147-L158)]

### <a name="retrieve-entities-in-pages-asynchronously"></a><span data-ttu-id="a67c4-203">Récupérer des entités dans les pages de manière asynchrone</span><span class="sxs-lookup"><span data-stu-id="a67c4-203">Retrieve entities in pages asynchronously</span></span>

<span data-ttu-id="a67c4-204">Si vous lisez un grand nombre d’entités, et que vous souhaitez les traiter comme ils sont récupérés, plutôt que d’attendre toutes les à retourner, vous pouvez utiliser une requête segmentée.</span><span class="sxs-lookup"><span data-stu-id="a67c4-204">If you are reading a large number of entities, and you want to process them as they are retrieved rather than waiting for them all to return, you can use a segmented query.</span></span> <span data-ttu-id="a67c4-205">Ici, pour retourner des résultats dans les pages à l’aide d’un flux de travail asynchrone afin que l’exécution n’est pas bloquée pendant que vous attendez un grand ensemble de résultats à retourner.</span><span class="sxs-lookup"><span data-stu-id="a67c4-205">Here, you return results in pages by using an async workflow so that execution is not blocked while you're waiting for a large set of results to return.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L163-L178)]

<span data-ttu-id="a67c4-206">Vous maintenant exécuter ce calcul synchrone :</span><span class="sxs-lookup"><span data-stu-id="a67c4-206">You now execute this computation synchronously:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L180-L180)]

### <a name="delete-an-entity"></a><span data-ttu-id="a67c4-207">Supprimer une entité</span><span class="sxs-lookup"><span data-stu-id="a67c4-207">Delete an entity</span></span>

<span data-ttu-id="a67c4-208">Vous pouvez supprimer une entité après l’avoir récupérée. il.</span><span class="sxs-lookup"><span data-stu-id="a67c4-208">You can delete an entity after you have retrieved it.</span></span> <span data-ttu-id="a67c4-209">Comme avec la mise à jour une entité, cette opération échoue si l’entité a changé depuis sa récupération.</span><span class="sxs-lookup"><span data-stu-id="a67c4-209">As with updating an entity, this fails if the entity has changed since you retrieved it.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L186-L187)]

### <a name="delete-a-table"></a><span data-ttu-id="a67c4-210">Supprimer une table</span><span class="sxs-lookup"><span data-stu-id="a67c4-210">Delete a table</span></span>

<span data-ttu-id="a67c4-211">Vous pouvez supprimer une table à partir d’un compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="a67c4-211">You can delete a table from a storage account.</span></span> <span data-ttu-id="a67c4-212">Une table qui a été supprimée n’est pas disponible pour être recréée pendant une période de temps après la suppression.</span><span class="sxs-lookup"><span data-stu-id="a67c4-212">A table that has been deleted will be unavailable to be re-created for a period of time following the deletion.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L193-L193)]

## <a name="next-steps"></a><span data-ttu-id="a67c4-213">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a67c4-213">Next steps</span></span>

<span data-ttu-id="a67c4-214">Maintenant que vous avez appris les bases du stockage de Table, suivez ces liens pour en savoir plus sur les tâches de stockage plus complexes et de l’API de Table Azure Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a67c4-214">Now that you've learned the basics of Table storage, follow these links to learn about more complex storage tasks and the Azure Cosmos DB Table API.</span></span>

- [<span data-ttu-id="a67c4-215">Introduction à l’API Azure Cosmos DB Table</span><span class="sxs-lookup"><span data-stu-id="a67c4-215">Introduction to Azure Cosmos DB Table API</span></span>](https://docs.microsoft.com/azure/cosmos-db/table-introduction)
- [<span data-ttu-id="a67c4-216">Bibliothèque cliente de stockage pour .NET</span><span class="sxs-lookup"><span data-stu-id="a67c4-216">Storage Client Library for .NET reference</span></span>](https://docs.microsoft.com/dotnet/api/overview/azure/storage?view=azure-dotnet)
- [<span data-ttu-id="a67c4-217">Fournisseur de Type de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="a67c4-217">Azure Storage Type Provider</span></span>](https://fsprojects.github.io/AzureStorageTypeProvider/)
- [<span data-ttu-id="a67c4-218">Blog de l’équipe stockage Azure</span><span class="sxs-lookup"><span data-stu-id="a67c4-218">Azure Storage Team Blog</span></span>](https://blogs.msdn.com/b/windowsazurestorage/)
- [<span data-ttu-id="a67c4-219">Configuration des chaînes de connexion</span><span class="sxs-lookup"><span data-stu-id="a67c4-219">Configuring Connection Strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)
- [<span data-ttu-id="a67c4-220">Bien démarrer avec stockage Table Azure dans .NET</span><span class="sxs-lookup"><span data-stu-id="a67c4-220">Getting Started with Azure Table Storage in .NET</span></span>](https://azure.microsoft.com/resources/samples/storage-table-dotnet-getting-started/)
