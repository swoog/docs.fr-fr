---
title: 'Prise en main le stockage de Table Azure à l’aide de F #'
description: Stocker des données structurées dans le cloud à l’aide du stockage Azure Table ou la base de données Azure Cosmos.
keywords: 'Visual f #, f #, fonctionnelle de programmation, .NET, .NET Core, Azure'
author: sylvanc
ms.author: phcart
ms.date: 03/26/2018
ms.topic: article
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 9e5d6cea-a98c-461e-a5cc-75f1d154eafd
ms.openlocfilehash: 6d40211e13e8d213aa5a40d585dd384abf49ddfa
ms.sourcegitcommit: 935d5267c44f9bce801468ef95f44572f1417e8c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/28/2018
---
# <a name="get-started-with-azure-table-storage-and-the-azure-cosmos-db-table-api-using-f"></a><span data-ttu-id="5bdf2-104">Prise en main avec stockage de Table Azure et l’API de Table Azure Cosmos DB à l’aide de F #</span><span class="sxs-lookup"><span data-stu-id="5bdf2-104">Get started with Azure Table storage and the Azure Cosmos DB Table API using F#</span></span> # 

<span data-ttu-id="5bdf2-105">Stockage de Table Azure est un service qui stocke des données structurées NoSQL dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-105">Azure Table storage is a service that stores structured NoSQL data in the cloud.</span></span> <span data-ttu-id="5bdf2-106">Stockage de table est un magasin de clé/attribut avec une conception schemaless.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-106">Table storage is a key/attribute store with a schemaless design.</span></span> <span data-ttu-id="5bdf2-107">Le stockage de Table étant schemaless, il est facile à adapter vos données en fonction des besoins de votre evolve d’application.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-107">Because Table storage is schemaless, it's easy to adapt your data as the needs of your application evolve.</span></span> <span data-ttu-id="5bdf2-108">Accès aux données est rapide et économique pour tous les types d’applications.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-108">Access to data is fast and cost-effective for all kinds of applications.</span></span> <span data-ttu-id="5bdf2-109">Stockage de table est généralement nettement plus faible coût que SQL traditionnel pour les volumes de données similaires.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-109">Table storage is typically significantly lower in cost than traditional SQL for similar volumes of data.</span></span>

<span data-ttu-id="5bdf2-110">Vous pouvez utiliser le stockage de Table pour stocker les jeux de données flexibles, telles que les données utilisateur pour les applications web, carnets d’adresses, les informations de périphérique et tout autre type de métadonnées nécessaires à votre service.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-110">You can use Table storage to store flexible datasets, such as user data for web applications, address books, device information, and any other type of metadata that your service requires.</span></span> <span data-ttu-id="5bdf2-111">Vous pouvez stocker n’importe quel nombre d’entités dans une table, et un compte de stockage peut contenir n’importe quel nombre de tables, jusqu'à la limite de capacité du compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-111">You can store any number of entities in a table, and a storage account may contain any number of tables, up to the capacity limit of the storage account.</span></span>

<span data-ttu-id="5bdf2-112">Base de données Azure Cosmos fournit l’API de Table pour les applications qui sont écrites pour le stockage de Table Azure et qui nécessitent les fonctionnalités premium telles que :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-112">Azure Cosmos DB provides the Table API for applications that are written for Azure Table storage and that require premium capabilities such as:</span></span>

- <span data-ttu-id="5bdf2-113">Clé en main distribution globale.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-113">Turnkey global distribution.</span></span>
- <span data-ttu-id="5bdf2-114">Débit dédié dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-114">Dedicated throughput worldwide.</span></span>
- <span data-ttu-id="5bdf2-115">Latences chiffre milliseconde au 99e centile.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-115">Single-digit millisecond latencies at the 99th percentile.</span></span>
- <span data-ttu-id="5bdf2-116">Garantie de haute disponibilité.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-116">Guaranteed high availability.</span></span>
- <span data-ttu-id="5bdf2-117">L’indexation secondaire automatique.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-117">Automatic secondary indexing.</span></span>

<span data-ttu-id="5bdf2-118">Les applications écrites pour le stockage Azure Table peuvent migrer vers la base de données Azure Cosmos à l’aide de l’API de Table sans aucune modification de code et tirer parti des fonctionnalités premium.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-118">Applications written for Azure Table storage can migrate to Azure Cosmos DB by using the Table API with no code changes and take advantage of premium capabilities.</span></span> <span data-ttu-id="5bdf2-119">L’API de Table a client SDK disponibles pour .NET, Java, Python et Node.js.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-119">The Table API has client SDKs available for .NET, Java, Python, and Node.js.</span></span>

<span data-ttu-id="5bdf2-120">Pour plus d’informations, consultez [Introduction à l’API de Table de base de données Azure Cosmos](https://docs.microsoft.com/azure/cosmos-db/table-introduction).</span><span class="sxs-lookup"><span data-stu-id="5bdf2-120">For more information, see [Introduction to Azure Cosmos DB Table API](https://docs.microsoft.com/azure/cosmos-db/table-introduction).</span></span>

## <a name="about-this-tutorial"></a><span data-ttu-id="5bdf2-121">À propos de ce didacticiel</span><span class="sxs-lookup"><span data-stu-id="5bdf2-121">About this tutorial</span></span>

<span data-ttu-id="5bdf2-122">Ce didacticiel montre comment écrire du code F # pour effectuer des tâches courantes à l’aide de l’API de base de données Table Azure Cosmos, y compris la création et la suppression d’une table et insertion, mise à jour, suppression et interrogation des données de table ou de stockage de Table Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-122">This tutorial shows how to write F# code to do some common tasks using Azure Table storage or the Azure Cosmos DB Table API, including creating and deleting a table and inserting, updating, deleting, and querying table data.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5bdf2-123">Prérequis</span><span class="sxs-lookup"><span data-stu-id="5bdf2-123">Prerequisites</span></span>

<span data-ttu-id="5bdf2-124">Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account) ou [compte de base de données Azure Cosmos](https://azure.microsoft.com/try/cosmosdb/).</span><span class="sxs-lookup"><span data-stu-id="5bdf2-124">To use this guide, you must first [create an Azure storage account](/azure/storage/storage-create-storage-account) or [Azure Cosmos DB account](https://azure.microsoft.com/try/cosmosdb/).</span></span>


## <a name="create-an-f-script-and-start-f-interactive"></a><span data-ttu-id="5bdf2-125">Créer un Script F # et démarrer) (F # Interactive</span><span class="sxs-lookup"><span data-stu-id="5bdf2-125">Create an F# Script and Start F# Interactive</span></span>

<span data-ttu-id="5bdf2-126">Les exemples présentés dans cet article peuvent être utilisées dans une application F # ou un script F #.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-126">The samples in this article can be used in either an F# application or an F# script.</span></span> <span data-ttu-id="5bdf2-127">Pour créer un script F #, créez un fichier avec le `.fsx` extension, par exemple `tables.fsx`, dans votre environnement de développement F #.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-127">To create an F# script, create a file with the `.fsx` extension, for example `tables.fsx`, in your F# development environment.</span></span>

<span data-ttu-id="5bdf2-128">Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` package et référence `WindowsAzure.Storage.dll` dans votre script à l’aide d’un `#r`la directive.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-128">Next, use a [package manager](package-management.md) such as [Paket](https://fsprojects.github.io/Paket/) or [NuGet](https://www.nuget.org/) to install the `WindowsAzure.Storage` package and reference `WindowsAzure.Storage.dll` in your script using a `#r` directive.</span></span> <span data-ttu-id="5bdf2-129">Effectuez à nouveau pour `Microsoft.WindowsAzure.ConfigurationManager` afin d’obtenir de l’espace de noms Microsoft.Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-129">Do it again for `Microsoft.WindowsAzure.ConfigurationManager` in order to get the Microsoft.Azure namespace.</span></span>

### <a name="add-namespace-declarations"></a><span data-ttu-id="5bdf2-130">Ajoutez les déclarations d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="5bdf2-130">Add namespace declarations</span></span>

<span data-ttu-id="5bdf2-131">Ajoutez le code suivant `open` instructions au début de la `tables.fsx` fichier :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-131">Add the following `open` statements to the top of the `tables.fsx` file:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L1-L5)]

### <a name="get-your-azure-storage-connection-string"></a><span data-ttu-id="5bdf2-132">Obtenir votre chaîne de connexion de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="5bdf2-132">Get your Azure Storage connection string</span></span>

<span data-ttu-id="5bdf2-133">Si vous vous connectez au service de la Table de stockage Azure, vous devez votre chaîne de connexion pour ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-133">If you're connecting to Azure Storage Table service, you'll need your connection string for this tutorial.</span></span> <span data-ttu-id="5bdf2-134">Vous pouvez copier votre chaîne de connexion à partir du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-134">You can copy your connection string from the Azure portal.</span></span> <span data-ttu-id="5bdf2-135">Pour plus d’informations sur les chaînes de connexion, consultez [configurer des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).</span><span class="sxs-lookup"><span data-stu-id="5bdf2-135">For more information about connection strings, see [Configure Storage Connection Strings](/azure/storage/storage-configure-connection-string).</span></span>

### <a name="get-your-azure-cosmos-db-connection-string"></a><span data-ttu-id="5bdf2-136">Obtenir votre chaîne de connexion de base de données Azure Cosmos</span><span class="sxs-lookup"><span data-stu-id="5bdf2-136">Get your Azure Cosmos DB connection string</span></span>

<span data-ttu-id="5bdf2-137">Si vous vous connectez à la base de données Azure Cosmos, vous devez votre chaîne de connexion pour ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-137">If you're connecting to Azure Cosmos DB, you'll need your connection string for this tutorial.</span></span> <span data-ttu-id="5bdf2-138">Vous pouvez copier votre chaîne de connexion à partir du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-138">You can copy your connection string from the Azure portal.</span></span> <span data-ttu-id="5bdf2-139">Dans le portail Azure, dans votre compte de base de données Cosmos, accédez à **paramètres** > **chaîne de connexion**, puis cliquez sur le **copie** bouton pour copier votre connexion principale Chaîne.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-139">In the Azure portal, in your Cosmos DB account, go to **Settings** > **Connection String**, and click the **Copy** button to copy your Primary Connection String.</span></span> 

<span data-ttu-id="5bdf2-140">Pour le didacticiel, entrez votre chaîne de connexion dans votre script, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-140">For the tutorial, enter your connection string in your script, like the following example:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L11-L11)]

<span data-ttu-id="5bdf2-141">Toutefois, il s’agit de **déconseillé** projets réels.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-141">However, this is **not recommended** for real projects.</span></span> <span data-ttu-id="5bdf2-142">Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-142">Your storage account key is similar to the root password for your storage account.</span></span> <span data-ttu-id="5bdf2-143">Veillez toujours à protéger votre clé de compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-143">Always be careful to protect your storage account key.</span></span> <span data-ttu-id="5bdf2-144">Éviter la distribuer à d’autres utilisateurs, le codage en dur, ou l’enregistrer dans un fichier texte brut qui est accessible à d’autres personnes.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-144">Avoid distributing it to other users, hard-coding it, or saving it in a plain-text file that is accessible to others.</span></span> <span data-ttu-id="5bdf2-145">Vous pouvez régénérer votre clé à l’aide du portail Azure, si vous pensez qu’il a peut-être été compromis.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-145">You can regenerate your key using the Azure Portal if you believe it may have been compromised.</span></span>

<span data-ttu-id="5bdf2-146">Les applications de réel, la meilleure façon de mettre à jour votre chaîne de connexion de stockage est dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-146">For real applications, the best way to maintain your storage connection string is in a configuration file.</span></span> <span data-ttu-id="5bdf2-147">Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-147">To fetch the connection string from a configuration file, you can do this:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L13-L15)]

<span data-ttu-id="5bdf2-148">À l’aide du Gestionnaire de Configuration de Azure est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-148">Using Azure Configuration Manager is optional.</span></span> <span data-ttu-id="5bdf2-149">Vous pouvez également utiliser une API telle que .NET Framework `ConfigurationManager` type.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-149">You can also use an API such as the .NET Framework's `ConfigurationManager` type.</span></span>

### <a name="parse-the-connection-string"></a><span data-ttu-id="5bdf2-150">Analyser la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="5bdf2-150">Parse the connection string</span></span>

<span data-ttu-id="5bdf2-151">Pour analyser la chaîne de connexion, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-151">To parse the connection string, use:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L21-L22)]

<span data-ttu-id="5bdf2-152">Cette opération retourne un `CloudStorageAccount`.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-152">This returns a `CloudStorageAccount`.</span></span>

### <a name="create-the-table-service-client"></a><span data-ttu-id="5bdf2-153">Créer le client de service de Table</span><span class="sxs-lookup"><span data-stu-id="5bdf2-153">Create the Table service client</span></span>

<span data-ttu-id="5bdf2-154">La `CloudTableClient` classe vous permet de récupérer des tables et des entités dans le stockage Table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-154">The `CloudTableClient` class enables you to retrieve tables and entities in Table storage.</span></span> <span data-ttu-id="5bdf2-155">Voici une méthode pour créer le client du service :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-155">Here's one way to create the service client:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L28-L29)]

<span data-ttu-id="5bdf2-156">Vous êtes maintenant prêt à écrire du code qui lit les données à partir d’et écrit des données dans le stockage de Table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-156">Now you are ready to write code that reads data from and writes data to Table storage.</span></span>

### <a name="create-a-table"></a><span data-ttu-id="5bdf2-157">Créer une table</span><span class="sxs-lookup"><span data-stu-id="5bdf2-157">Create a table</span></span>

<span data-ttu-id="5bdf2-158">Cet exemple montre comment créer une table si elle n’existe pas déjà :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-158">This example shows how to create a table if it does not already exist:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L35-L39)]

### <a name="add-an-entity-to-a-table"></a><span data-ttu-id="5bdf2-159">Ajouter une entité à une table</span><span class="sxs-lookup"><span data-stu-id="5bdf2-159">Add an entity to a table</span></span>

<span data-ttu-id="5bdf2-160">Une entité doit avoir un type qui hérite de `TableEntity`.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-160">An entity has to have a type that inherits from `TableEntity`.</span></span> <span data-ttu-id="5bdf2-161">Vous pouvez étendre `TableEntity` dans comme vous le souhaitez, mais votre type *doit* avoir un constructeur sans paramètre.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-161">You can extend `TableEntity` in any way you like, but your type *must* have a parameter-less constructor.</span></span> <span data-ttu-id="5bdf2-162">Seules les propriétés qui ont les `get` et `set` sont stockées dans votre Table Azure.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-162">Only properties that have both `get` and `set` are stored in your Azure Table.</span></span>

<span data-ttu-id="5bdf2-163">Partition de l’entité et la clé de ligne identifient de façon unique l’entité dans la table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-163">An entity's partition and row key uniquely identify the entity in the table.</span></span> <span data-ttu-id="5bdf2-164">Entités avec la même clé de partition peuvent être interrogées plus rapidement que ceux avec des clés de partition différente, mais à l’aide de clés de partition divers permet une plus grande évolutivité d’opérations parallèles.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-164">Entities with the same partition key can be queried faster than those with different partition keys, but using diverse partition keys allows for greater scalability of parallel operations.</span></span>

<span data-ttu-id="5bdf2-165">Voici un exemple d’un `Customer` qui utilise le `lastName` comme clé de partition et le `firstName` comme clé de ligne.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-165">Here's an example of a `Customer` that uses the `lastName` as the partition key and the `firstName` as the row key.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L45-L52)]

<span data-ttu-id="5bdf2-166">Ajoutez maintenant `Customer` à la table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-166">Now add `Customer` to the table.</span></span> <span data-ttu-id="5bdf2-167">Pour ce faire, créez un `TableOperation` qui s’exécute sur la table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-167">To do so, create a `TableOperation` that executes on the table.</span></span> <span data-ttu-id="5bdf2-168">Dans ce cas, vous créez un `Insert` opération.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-168">In this case, you create an `Insert` operation.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L54-L55)]

### <a name="insert-a-batch-of-entities"></a><span data-ttu-id="5bdf2-169">Insérer un lot d’entités</span><span class="sxs-lookup"><span data-stu-id="5bdf2-169">Insert a batch of entities</span></span>

<span data-ttu-id="5bdf2-170">Vous pouvez insérer un lot d’entités dans une table à l’aide d’une seule opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-170">You can insert a batch of entities into a table using a single write operation.</span></span> <span data-ttu-id="5bdf2-171">Autorisent les opérations par lots vous permet de combiner des opérations en une seule exécution, mais ils présentent quelques restrictions :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-171">Batch operations allow you to combine operations into a single execution, but they have some restrictions:</span></span>

- <span data-ttu-id="5bdf2-172">Vous pouvez effectuer des mises à jour, supprime et l’insère dans la même opération de traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-172">You can perform updates, deletes, and inserts in the same batch operation.</span></span>
- <span data-ttu-id="5bdf2-173">Une opération de traitement peut inclure jusqu'à 100 entités.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-173">A batch operation can include up to 100 entities.</span></span>
- <span data-ttu-id="5bdf2-174">Toutes les entités dans une opération par lot doivent avoir la même clé de partition.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-174">All entities in a batch operation must have the same partition key.</span></span>
- <span data-ttu-id="5bdf2-175">Bien qu’il soit possible d’effectuer une requête dans un traitement par lots, il doit être la seule opération dans le lot.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-175">While it is possible to perform a query in a batch operation, it must be the only operation in the batch.</span></span>

<span data-ttu-id="5bdf2-176">Voici un code qui combine les deux insertions dans une opération de traitement :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-176">Here's some code that combines two inserts into a batch operation:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L62-L71)]

### <a name="retrieve-all-entities-in-a-partition"></a><span data-ttu-id="5bdf2-177">Récupérer toutes les entités dans une partition</span><span class="sxs-lookup"><span data-stu-id="5bdf2-177">Retrieve all entities in a partition</span></span>

<span data-ttu-id="5bdf2-178">Pour interroger une table pour toutes les entités dans une partition, utilisez un `TableQuery` objet.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-178">To query a table for all entities in a partition, use a `TableQuery` object.</span></span> <span data-ttu-id="5bdf2-179">Ici, vous filtrez pour les entités dont « Smith » est la clé de partition.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-179">Here, you filter for entities where "Smith" is the partition key.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L77-L82)]

<span data-ttu-id="5bdf2-180">Maintenant, vous imprimez les résultats :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-180">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L84-L85)]


### <a name="retrieve-a-range-of-entities-in-a-partition"></a><span data-ttu-id="5bdf2-181">Récupérer une plage d’entités dans une partition</span><span class="sxs-lookup"><span data-stu-id="5bdf2-181">Retrieve a range of entities in a partition</span></span>

<span data-ttu-id="5bdf2-182">Si vous ne souhaitez pas toutes les entités dans une partition de requête, vous pouvez spécifier une plage en combinant le filtre de clé de partition avec un filtre de clé de ligne.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-182">If you don't want to query all the entities in a partition, you can specify a range by combining the partition key filter with a row key filter.</span></span> <span data-ttu-id="5bdf2-183">Ici, vous utilisez des deux filtres pour obtenir toutes les entités dans la partition « Smith » où la clé de ligne (prénom) commence par une lettre au plus tôt le « M » dans l’alphabet.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-183">Here, you use two filters to get all entities in the "Smith" partition where the row key (first name) starts with a letter earlier than "M" in the alphabet.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L91-L100)]

<span data-ttu-id="5bdf2-184">Maintenant, vous imprimez les résultats :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-184">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L102-L103)]

### <a name="retrieve-a-single-entity"></a><span data-ttu-id="5bdf2-185">Extraire une seule entité</span><span class="sxs-lookup"><span data-stu-id="5bdf2-185">Retrieve a single entity</span></span>

<span data-ttu-id="5bdf2-186">Vous pouvez écrire une requête pour récupérer une entité unique et spécifique.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-186">You can write a query to retrieve a single, specific entity.</span></span> <span data-ttu-id="5bdf2-187">Ici, vous utilisez un `TableOperation` pour spécifier le client « Ben Smith ».</span><span class="sxs-lookup"><span data-stu-id="5bdf2-187">Here, you use a `TableOperation` to specify the customer "Ben Smith".</span></span> <span data-ttu-id="5bdf2-188">Au lieu d’une collection, vous obtenez en retour un `Customer`.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-188">Instead of a collection, you get back a `Customer`.</span></span> <span data-ttu-id="5bdf2-189">Spécification de la clé de partition et la clé de ligne dans une requête est le moyen le plus rapide pour récupérer une seule entité du service de Table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-189">Specifying both the partition key and the row key in a query is the fastest way to retrieve a single entity from the Table service.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L109-L111)]

<span data-ttu-id="5bdf2-190">Maintenant, vous imprimez les résultats :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-190">You now print the results:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L113-L115)]


### <a name="replace-an-entity"></a><span data-ttu-id="5bdf2-191">Remplacer une entité</span><span class="sxs-lookup"><span data-stu-id="5bdf2-191">Replace an entity</span></span>

<span data-ttu-id="5bdf2-192">Pour mettre à jour une entité, récupérer à partir du service de Table, de modifier l’objet d’entité, puis enregistrer les modifications dans le service de Table à l’aide un `Replace` opération.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-192">To update an entity, retrieve it from the Table service, modify the entity object, and then save the changes back to the Table service using a `Replace` operation.</span></span> <span data-ttu-id="5bdf2-193">Cela entraîne l’entité à remplacer entièrement sur le serveur, à moins que l’entité sur le serveur a changé depuis sa récupération, auquel cas l’opération échoue.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-193">This causes the entity to be fully replaced on the server, unless the entity on the server has changed since it was retrieved, in which case the operation fails.</span></span> <span data-ttu-id="5bdf2-194">Cet échec est d’empêcher votre application de remplacer par inadvertance les modifications provenant d’autres sources.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-194">This failure is to prevent your application from inadvertently overwriting changes from other sources.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L121-L128)]

### <a name="insert-or-replace-an-entity"></a><span data-ttu-id="5bdf2-195">Insérer ou remplacer une entité</span><span class="sxs-lookup"><span data-stu-id="5bdf2-195">Insert-or-replace an entity</span></span>

<span data-ttu-id="5bdf2-196">Parfois, vous ne connaissez pas si une entité existe dans la table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-196">Sometimes, you don't know whether an entity exists in the table.</span></span> <span data-ttu-id="5bdf2-197">Et, dans ce cas, les valeurs actuelles stockées qu’il contient ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-197">And if it does, the current values stored in it are no longer needed.</span></span> <span data-ttu-id="5bdf2-198">Vous pouvez utiliser `InsertOrReplace` pour créer l’entité ou le remplacer si elle existe, quel que soit son état.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-198">You can use `InsertOrReplace` to create the entity, or replace it if it exists, regardless of its state.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L134-L141)]

### <a name="query-a-subset-of-entity-properties"></a><span data-ttu-id="5bdf2-199">Un sous-ensemble de propriétés de l’entité de requête</span><span class="sxs-lookup"><span data-stu-id="5bdf2-199">Query a subset of entity properties</span></span>

<span data-ttu-id="5bdf2-200">Une requête de table peut récupérer seulement quelques propriétés d’une entité au lieu de tous les.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-200">A table query can retrieve just a few properties from an entity instead of all of them.</span></span> <span data-ttu-id="5bdf2-201">Cette technique, appelée projection, peut améliorer les performances, en particulier pour les entités de grande taille.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-201">This technique, called projection, can improve query performance, especially for large entities.</span></span> <span data-ttu-id="5bdf2-202">Ici, vous revenez à l’aide des adresses de messagerie uniquement `DynamicTableEntity` et `EntityResolver`.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-202">Here, you return only email addresses using `DynamicTableEntity` and `EntityResolver`.</span></span> <span data-ttu-id="5bdf2-203">Notez que la projection n’est pas pris en charge sur l’émulateur de stockage local, pour que ce code s’exécute uniquement lorsque vous utilisez un compte sur le service de Table.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-203">Note that projection is not supported on the local storage emulator, so this code runs only when you're using an account on the Table service.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L147-L158)]

### <a name="retrieve-entities-in-pages-asynchronously"></a><span data-ttu-id="5bdf2-204">Récupérer des entités dans les pages de façon asynchrone</span><span class="sxs-lookup"><span data-stu-id="5bdf2-204">Retrieve entities in pages asynchronously</span></span>

<span data-ttu-id="5bdf2-205">Si vous lisez un grand nombre d’entités, et que vous souhaitez les traiter comme ils sont récupérés, plutôt que d’en attente pour tous les à retourner, vous pouvez utiliser une requête segmentée.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-205">If you are reading a large number of entities, and you want to process them as they are retrieved rather than waiting for them all to return, you can use a segmented query.</span></span> <span data-ttu-id="5bdf2-206">Ici, vous des résultats dans les pages à l’aide d’un flux de travail asynchrone afin que l’exécution n’est pas bloquée pendant que vous patientez pour un grand ensemble de résultats à retourner.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-206">Here, you return results in pages by using an async workflow so that execution is not blocked while you're waiting for a large set of results to return.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L163-L178)]

<span data-ttu-id="5bdf2-207">Vous exécutez maintenant ce calcul synchrone :</span><span class="sxs-lookup"><span data-stu-id="5bdf2-207">You now execute this computation synchronously:</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L180-L180)]

### <a name="delete-an-entity"></a><span data-ttu-id="5bdf2-208">Supprimer une entité</span><span class="sxs-lookup"><span data-stu-id="5bdf2-208">Delete an entity</span></span>

<span data-ttu-id="5bdf2-209">Vous pouvez supprimer une entité une fois que vous l’avez extrait.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-209">You can delete an entity after you have retrieved it.</span></span> <span data-ttu-id="5bdf2-210">Comme avec la mise à jour une entité, il échoue si l’entité a été modifié depuis son.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-210">As with updating an entity, this fails if the entity has changed since you retrieved it.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L186-L187)]

### <a name="delete-a-table"></a><span data-ttu-id="5bdf2-211">Supprimer une table</span><span class="sxs-lookup"><span data-stu-id="5bdf2-211">Delete a table</span></span>

<span data-ttu-id="5bdf2-212">Vous pouvez supprimer une table à partir d’un compte de stockage.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-212">You can delete a table from a storage account.</span></span> <span data-ttu-id="5bdf2-213">Une table qui a été supprimée n’est pas disponible pour être recréé pour une période de temps après la suppression.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-213">A table that has been deleted will be unavailable to be re-created for a period of time following the deletion.</span></span>

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L193-L193)]

## <a name="next-steps"></a><span data-ttu-id="5bdf2-214">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="5bdf2-214">Next steps</span></span>

<span data-ttu-id="5bdf2-215">Maintenant que vous avez appris les notions de base du stockage Table, suivez ces liens pour en savoir plus sur les tâches de stockage plus complexes et de l’API de Table de base de données Azure Cosmos.</span><span class="sxs-lookup"><span data-stu-id="5bdf2-215">Now that you've learned the basics of Table storage, follow these links to learn about more complex storage tasks and the Azure Cosmos DB Table API.</span></span>

- [<span data-ttu-id="5bdf2-216">Introduction à Azure Cosmos API de Table de base de données</span><span class="sxs-lookup"><span data-stu-id="5bdf2-216">Introduction to Azure Cosmos DB Table API</span></span>](https://docs.microsoft.com/azure/cosmos-db/table-introduction)
- [<span data-ttu-id="5bdf2-217">Bibliothèque cliente de stockage pour la référence .NET</span><span class="sxs-lookup"><span data-stu-id="5bdf2-217">Storage Client Library for .NET reference</span></span>](https://docs.microsoft.com/dotnet/api/overview/azure/storage?view=azure-dotnet)
- [<span data-ttu-id="5bdf2-218">Fournisseur de Type de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="5bdf2-218">Azure Storage Type Provider</span></span>](http://fsprojects.github.io/AzureStorageTypeProvider/)
- [<span data-ttu-id="5bdf2-219">Blog de l’équipe stockage Azure</span><span class="sxs-lookup"><span data-stu-id="5bdf2-219">Azure Storage Team Blog</span></span>](http://blogs.msdn.com/b/windowsazurestorage/)
- [<span data-ttu-id="5bdf2-220">Configuration des chaînes de connexion</span><span class="sxs-lookup"><span data-stu-id="5bdf2-220">Configuring Connection Strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)
- [<span data-ttu-id="5bdf2-221">Prise en main avec un stockage de Table Windows Azure dans .NET</span><span class="sxs-lookup"><span data-stu-id="5bdf2-221">Getting Started with Azure Table Storage in .NET</span></span>](https://azure.microsoft.com/resources/samples/storage-table-dotnet-getting-started/)
