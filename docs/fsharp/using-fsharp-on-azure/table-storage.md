---
title: 'Prise en main le stockage Table Azure en F #'
description: Store données structurées dans le cloud à l’aide du stockage Table Azure ou Azure Cosmos DB.
author: sylvanc
ms.date: 03/26/2018
ms.openlocfilehash: 2d793ba8653833ff384f1824e303b08e05aba69b
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519533"
---
# <a name="get-started-with-azure-table-storage-and-the-azure-cosmos-db-table-api-using-f"></a>Bien démarrer avec stockage Table Azure et l’API de Table Azure Cosmos DB à l’aide de F # # 

Stockage Table Azure est un service qui stocke des données NoSQL structurées dans le cloud. Stockage de table est un magasin de clés/attributs doté d’une conception sans schéma. Étant donné que le stockage de tables est sans schéma, il est facile d’adapter vos données en tant que l’évolution des besoins de votre application. Accès aux données est rapide et économique pour toutes sortes d’applications. Stockage table est généralement beaucoup moins coûteux que le SQL traditionnel pour des volumes de données similaires.

Vous pouvez utiliser le stockage de Table pour stocker des jeux de données flexibles, telles que les données utilisateur pour les applications web, carnets d’adresses, informations sur l’appareil et tout autre type de métadonnées nécessaires à votre service. Vous pouvez stocker n’importe quel nombre d’entités dans une table, et un compte de stockage peut contenir un nombre quelconque de tables, jusqu'à la limite de capacité du compte de stockage.

Azure Cosmos DB fournit l’API de Table pour les applications qui sont écrites pour le stockage Table Azure et qui nécessitent des fonctionnalités premium telles que :

- Une distribution mondiale.
- Débit dédié dans le monde entier.
- Temps de latence en quelques millisecondes au 99e centile.
- Haute disponibilité garantie.
- L’indexation automatique secondaire.

Les applications écrites pour le stockage Table Azure peuvent migrer vers Azure Cosmos DB à l’aide de l’API de Table sans aucune modification de code et tirer parti des fonctionnalités premium. L’API de Table a des kits pour .NET, Java, Python et Node.js.

Pour plus d’informations, consultez [Introduction à l’API de Table Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/table-introduction).

## <a name="about-this-tutorial"></a>À propos de ce didacticiel

Ce didacticiel montre comment écrire du code F # pour effectuer certaines tâches courantes à l’aide du stockage Table Azure ou l’API Azure Cosmos DB Table, y compris la création et suppression d’une table et insertion de la mise à jour, suppression et interrogation des données de table.

## <a name="prerequisites"></a>Prérequis

Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account) ou [compte Azure Cosmos DB](https://azure.microsoft.com/try/cosmosdb/).


## <a name="create-an-f-script-and-start-f-interactive"></a>Créer de Script F # et démarrer F # Interactive

Les exemples de cet article peuvent être utilisés dans une application F # ou un script F #. Pour créer un script F #, créez un fichier avec le `.fsx` extension, par exemple `tables.fsx`, dans votre environnement de développement F #.

Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` package et référence `WindowsAzure.Storage.dll` dans votre script à l’aide d’un `#r`directive. Effectuez à nouveau pour `Microsoft.WindowsAzure.ConfigurationManager` afin d’obtenir de l’espace de noms Microsoft.Azure.

### <a name="add-namespace-declarations"></a>Ajoutez les déclarations d’espace de noms

Ajoutez le code suivant `open` instructions au début de la `tables.fsx` fichier :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L1-L5)]

### <a name="get-your-azure-storage-connection-string"></a>Obtenir votre chaîne de connexion de stockage Azure

Si vous vous connectez au service de Table de stockage Azure, vous aurez besoin de votre chaîne de connexion pour ce didacticiel. Vous pouvez copier votre chaîne de connexion à partir du portail Azure. Pour plus d’informations sur les chaînes de connexion, consultez [configuration des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).

### <a name="get-your-azure-cosmos-db-connection-string"></a>Obtenir votre chaîne de connexion Azure Cosmos DB

Si vous vous connectez à Azure Cosmos DB, vous aurez besoin de votre chaîne de connexion pour ce didacticiel. Vous pouvez copier votre chaîne de connexion à partir du portail Azure. Dans le portail Azure, dans votre compte Cosmos DB, accédez à **paramètres** > **chaîne de connexion**, puis cliquez sur le **copie** bouton pour copier votre connexion principale Chaîne. 

Pour ce didacticiel, entrez votre chaîne de connexion dans votre script, comme dans l’exemple suivant :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L11-L11)]

Toutefois, il s’agit de **déconseillé** projets de réel. Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage. Veillez toujours à protéger votre clé de compte de stockage. Évitez de la communiquer à d’autres utilisateurs, coder en dur, ou l’enregistrer dans un fichier texte brut qui n’est accessible à d’autres personnes. Vous pouvez régénérer votre clé à l’aide du portail Azure si vous pensez qu’il a peut-être été compromise.

Applications de réel, la meilleure façon de conserver votre chaîne de connexion de stockage est dans un fichier de configuration. Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L13-L15)]

L’utilisation d’Azure Configuration Manager est facultative. Vous pouvez également utiliser une API telle que du .NET Framework `ConfigurationManager` type.

### <a name="parse-the-connection-string"></a>Analyser la chaîne de connexion

Pour analyser la chaîne de connexion, utilisez :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L21-L22)]

Cette commande renvoie un `CloudStorageAccount`.

### <a name="create-the-table-service-client"></a>Créer le client de service de Table

Le `CloudTableClient` classe vous permet de récupérer des tables et des entités dans le stockage Table. Voici une façon de créer le client du service :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L28-L29)]

Vous êtes maintenant prêt à écrire du code qui lit et écrit des données dans le stockage Table.

### <a name="create-a-table"></a>Créer une table

Cet exemple montre comment créer une table si elle n’existe pas déjà :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L35-L39)]

### <a name="add-an-entity-to-a-table"></a>Ajouter une entité à une table

Une entité doit avoir un type qui hérite de `TableEntity`. Vous pouvez étendre `TableEntity` dans comme vous le souhaitez, mais votre type *doit* avoir un constructeur sans paramètre. Seules les propriétés qui ont les deux `get` et `set` sont stockés dans votre Table Azure.

Partition de l’entité et la clé de ligne identifient de manière unique l’entité dans la table. Entités avec la même clé de partition peuvent être interrogées plus rapides que celles avec des clés de partition différente, mais à l’aide de différentes clés de partition permet une plus grande évolutivité d’opérations parallèles.

Voici un exemple d’un `Customer` qui utilise le `lastName` comme clé de partition et le `firstName` comme clé de ligne.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L45-L52)]

Ajoutez maintenant `Customer` à la table. Pour ce faire, créez un `TableOperation` qui s’exécute sur la table. Dans ce cas, vous créez un `Insert` opération.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L54-L55)]

### <a name="insert-a-batch-of-entities"></a>Insérer un lot d’entités

Vous pouvez insérer un lot d’entités dans une table à l’aide d’une seule opération d’écriture. Autorisent les opérations par lots vous permet de combiner des opérations en une seule exécution, mais ils présentent quelques restrictions :

- Vous pouvez effectuer des mises à jour, suppressions et des insertions dans la même opération de traitement par lots.
- Une opération par lot peut inclure jusqu'à 100 entités.
- Toutes les entités dans une opération par lot doivent avoir la même clé de partition.
- Bien qu’il soit possible d’effectuer une requête dans une opération par lot, il doit être la seule opération dans le lot.

Voici un code qui associe deux insertions dans une opération par lot :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L62-L71)]

### <a name="retrieve-all-entities-in-a-partition"></a>Récupérer toutes les entités dans une partition

Pour interroger une table pour toutes les entités dans une partition, utilisez un `TableQuery` objet. Ici, vous filtrez pour les entités dont « Smith » est la clé de partition.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L77-L82)]

Maintenant, vous imprimez les résultats :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L84-L85)]


### <a name="retrieve-a-range-of-entities-in-a-partition"></a>Récupérer un ensemble d’entités dans une partition

Si vous ne souhaitez pas interroger toutes les entités dans une partition, vous pouvez spécifier une plage en combinant le filtre de clé de partition avec un filtre de clé de ligne. Ici, vous utilisez des deux filtres pour obtenir toutes les entités dans la partition « Smith » où la clé de ligne (prénom) commence par une lettre antérieure à « M » dans l’alphabet.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L91-L100)]

Maintenant, vous imprimez les résultats :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L102-L103)]

### <a name="retrieve-a-single-entity"></a>Extraire une seule entité

Vous pouvez écrire une requête pour récupérer une entité unique. Ici, vous utilisez un `TableOperation` pour spécifier le client « Ben Smith ». Au lieu d’une collection, vous obtenez en retour un `Customer`. Spécification de la clé de partition et la clé de ligne dans une requête est le moyen le plus rapide pour récupérer une entité unique à partir du service de Table.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L109-L111)]

Maintenant, vous imprimez les résultats :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L113-L115)]


### <a name="replace-an-entity"></a>Remplacer une entité

Pour mettre à jour une entité, récupérez-la du service de Table, modifiez l’objet d’entité, puis enregistrez les modifications vers le service de Table à l’aide un `Replace` opération. Cela entraîne l’entité à remplacer entièrement sur le serveur, sauf si l’entité sur le serveur a changé depuis sa récupération, auquel cas l’opération échoue. Cet échec survient pour empêcher votre application de remplacer par inadvertance les modifications provenant d’autres sources.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L121-L128)]

### <a name="insert-or-replace-an-entity"></a>Insérer ou remplacer une entité

Parfois, vous ne connaissez pas si une entité existe dans la table. Et, le cas échéant, les valeurs actuelles stockées qu’il contient ne sont plus nécessaires. Vous pouvez utiliser `InsertOrReplace` pour créer l’entité, ou remplacez-la si elle existe, quel que soit son état.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L134-L141)]

### <a name="query-a-subset-of-entity-properties"></a>Interroger un sous-ensemble des propriétés de l’entité

Une requête de table peut récupérer uniquement quelques propriétés d’une entité et non la totalité d'entre eux. Cette technique, appelée projection, peut améliorer les performances des requêtes, en particulier pour les entités volumineuses. Ici, vous revenez à l’aide des adresses e-mail uniquement `DynamicTableEntity` et `EntityResolver`. Notez que la projection n’est pas pris en charge sur l’émulateur de stockage local, ce code s’exécute donc uniquement si vous utilisez un compte sur le service de Table.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L147-L158)]

### <a name="retrieve-entities-in-pages-asynchronously"></a>Récupérer des entités dans les pages de manière asynchrone

Si vous lisez un grand nombre d’entités, et que vous souhaitez les traiter comme ils sont récupérés, plutôt que d’attendre toutes les à retourner, vous pouvez utiliser une requête segmentée. Ici, pour retourner des résultats dans les pages à l’aide d’un flux de travail asynchrone afin que l’exécution n’est pas bloquée pendant que vous attendez un grand ensemble de résultats à retourner.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L163-L178)]

Vous maintenant exécuter ce calcul synchrone :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L180-L180)]

### <a name="delete-an-entity"></a>Supprimer une entité

Vous pouvez supprimer une entité après l’avoir récupérée. il. Comme avec la mise à jour une entité, cette opération échoue si l’entité a changé depuis sa récupération.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L186-L187)]

### <a name="delete-a-table"></a>Supprimer une table

Vous pouvez supprimer une table à partir d’un compte de stockage. Une table qui a été supprimée n’est pas disponible pour être recréée pendant une période de temps après la suppression.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L193-L193)]

## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous avez appris les bases du stockage de Table, suivez ces liens pour en savoir plus sur les tâches de stockage plus complexes et de l’API de Table Azure Cosmos DB.

- [Introduction à l’API Azure Cosmos DB Table](https://docs.microsoft.com/azure/cosmos-db/table-introduction)
- [Bibliothèque cliente de stockage pour .NET](https://docs.microsoft.com/dotnet/api/overview/azure/storage?view=azure-dotnet)
- [Fournisseur de Type de stockage Azure](http://fsprojects.github.io/AzureStorageTypeProvider/)
- [Blog de l’équipe stockage Azure](https://blogs.msdn.com/b/windowsazurestorage/)
- [Configuration des chaînes de connexion](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)
- [Bien démarrer avec stockage Table Azure dans .NET](https://azure.microsoft.com/resources/samples/storage-table-dotnet-getting-started/)
