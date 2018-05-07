---
title: 'Prise en main le stockage de Table Azure à l’aide de F #'
description: Stocker des données structurées dans le cloud à l’aide du stockage Azure Table ou la base de données Azure Cosmos.
author: sylvanc
ms.date: 03/26/2018
ms.openlocfilehash: ac81bc88db1436aa4d5f576da61a90839df04b99
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="get-started-with-azure-table-storage-and-the-azure-cosmos-db-table-api-using-f"></a>Prise en main avec stockage de Table Azure et l’API de Table Azure Cosmos DB à l’aide de F # # 

Stockage de Table Azure est un service qui stocke des données structurées NoSQL dans le cloud. Stockage de table est un magasin de clé/attribut avec une conception schemaless. Le stockage de Table étant schemaless, il est facile à adapter vos données en fonction des besoins de votre evolve d’application. Accès aux données est rapide et économique pour tous les types d’applications. Stockage de table est généralement nettement plus faible coût que SQL traditionnel pour les volumes de données similaires.

Vous pouvez utiliser le stockage de Table pour stocker les jeux de données flexibles, telles que les données utilisateur pour les applications web, carnets d’adresses, les informations de périphérique et tout autre type de métadonnées nécessaires à votre service. Vous pouvez stocker n’importe quel nombre d’entités dans une table, et un compte de stockage peut contenir n’importe quel nombre de tables, jusqu'à la limite de capacité du compte de stockage.

Base de données Azure Cosmos fournit l’API de Table pour les applications qui sont écrites pour le stockage de Table Azure et qui nécessitent les fonctionnalités premium telles que :

- Clé en main distribution globale.
- Débit dédié dans le monde entier.
- Latences chiffre milliseconde au 99e centile.
- Garantie de haute disponibilité.
- L’indexation secondaire automatique.

Les applications écrites pour le stockage Azure Table peuvent migrer vers la base de données Azure Cosmos à l’aide de l’API de Table sans aucune modification de code et tirer parti des fonctionnalités premium. L’API de Table a client SDK disponibles pour .NET, Java, Python et Node.js.

Pour plus d’informations, consultez [Introduction à l’API de Table de base de données Azure Cosmos](https://docs.microsoft.com/azure/cosmos-db/table-introduction).

## <a name="about-this-tutorial"></a>À propos de ce didacticiel

Ce didacticiel montre comment écrire du code F # pour effectuer des tâches courantes à l’aide de l’API de base de données Table Azure Cosmos, y compris la création et la suppression d’une table et insertion, mise à jour, suppression et interrogation des données de table ou de stockage de Table Azure.

## <a name="prerequisites"></a>Prérequis

Pour utiliser ce guide, vous devez d’abord [créer un compte de stockage Azure](/azure/storage/storage-create-storage-account) ou [compte de base de données Azure Cosmos](https://azure.microsoft.com/try/cosmosdb/).


## <a name="create-an-f-script-and-start-f-interactive"></a>Créer un Script F # et démarrer) (F # Interactive

Les exemples présentés dans cet article peuvent être utilisées dans une application F # ou un script F #. Pour créer un script F #, créez un fichier avec le `.fsx` extension, par exemple `tables.fsx`, dans votre environnement de développement F #.

Ensuite, utilisez un [Gestionnaire de package](package-management.md) comme [Paket](https://fsprojects.github.io/Paket/) ou [NuGet](https://www.nuget.org/) pour installer le `WindowsAzure.Storage` package et référence `WindowsAzure.Storage.dll` dans votre script à l’aide d’un `#r`la directive. Effectuez à nouveau pour `Microsoft.WindowsAzure.ConfigurationManager` afin d’obtenir de l’espace de noms Microsoft.Azure.

### <a name="add-namespace-declarations"></a>Ajoutez les déclarations d’espace de noms

Ajoutez le code suivant `open` instructions au début de la `tables.fsx` fichier :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L1-L5)]

### <a name="get-your-azure-storage-connection-string"></a>Obtenir votre chaîne de connexion de stockage Azure

Si vous vous connectez au service de la Table de stockage Azure, vous devez votre chaîne de connexion pour ce didacticiel. Vous pouvez copier votre chaîne de connexion à partir du portail Azure. Pour plus d’informations sur les chaînes de connexion, consultez [configurer des chaînes de connexion stockage](/azure/storage/storage-configure-connection-string).

### <a name="get-your-azure-cosmos-db-connection-string"></a>Obtenir votre chaîne de connexion de base de données Azure Cosmos

Si vous vous connectez à la base de données Azure Cosmos, vous devez votre chaîne de connexion pour ce didacticiel. Vous pouvez copier votre chaîne de connexion à partir du portail Azure. Dans le portail Azure, dans votre compte de base de données Cosmos, accédez à **paramètres** > **chaîne de connexion**, puis cliquez sur le **copie** bouton pour copier votre connexion principale Chaîne. 

Pour le didacticiel, entrez votre chaîne de connexion dans votre script, comme dans l’exemple suivant :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L11-L11)]

Toutefois, il s’agit de **déconseillé** projets réels. Votre clé de compte de stockage est similaire au mot de passe racine pour votre compte de stockage. Veillez toujours à protéger votre clé de compte de stockage. Éviter la distribuer à d’autres utilisateurs, le codage en dur, ou l’enregistrer dans un fichier texte brut qui est accessible à d’autres personnes. Vous pouvez régénérer votre clé à l’aide du portail Azure, si vous pensez qu’il a peut-être été compromis.

Les applications de réel, la meilleure façon de mettre à jour votre chaîne de connexion de stockage est dans un fichier de configuration. Pour extraire la chaîne de connexion à partir d’un fichier de configuration, vous pouvez effectuer ceci :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L13-L15)]

À l’aide du Gestionnaire de Configuration de Azure est facultatif. Vous pouvez également utiliser une API telle que .NET Framework `ConfigurationManager` type.

### <a name="parse-the-connection-string"></a>Analyser la chaîne de connexion

Pour analyser la chaîne de connexion, utilisez :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L21-L22)]

Cette opération retourne un `CloudStorageAccount`.

### <a name="create-the-table-service-client"></a>Créer le client de service de Table

La `CloudTableClient` classe vous permet de récupérer des tables et des entités dans le stockage Table. Voici une méthode pour créer le client du service :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L28-L29)]

Vous êtes maintenant prêt à écrire du code qui lit les données à partir d’et écrit des données dans le stockage de Table.

### <a name="create-a-table"></a>Créer une table

Cet exemple montre comment créer une table si elle n’existe pas déjà :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L35-L39)]

### <a name="add-an-entity-to-a-table"></a>Ajouter une entité à une table

Une entité doit avoir un type qui hérite de `TableEntity`. Vous pouvez étendre `TableEntity` dans comme vous le souhaitez, mais votre type *doit* avoir un constructeur sans paramètre. Seules les propriétés qui ont les `get` et `set` sont stockées dans votre Table Azure.

Partition de l’entité et la clé de ligne identifient de façon unique l’entité dans la table. Entités avec la même clé de partition peuvent être interrogées plus rapidement que ceux avec des clés de partition différente, mais à l’aide de clés de partition divers permet une plus grande évolutivité d’opérations parallèles.

Voici un exemple d’un `Customer` qui utilise le `lastName` comme clé de partition et le `firstName` comme clé de ligne.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L45-L52)]

Ajoutez maintenant `Customer` à la table. Pour ce faire, créez un `TableOperation` qui s’exécute sur la table. Dans ce cas, vous créez un `Insert` opération.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L54-L55)]

### <a name="insert-a-batch-of-entities"></a>Insérer un lot d’entités

Vous pouvez insérer un lot d’entités dans une table à l’aide d’une seule opération d’écriture. Autorisent les opérations par lots vous permet de combiner des opérations en une seule exécution, mais ils présentent quelques restrictions :

- Vous pouvez effectuer des mises à jour, supprime et l’insère dans la même opération de traitement par lots.
- Une opération de traitement peut inclure jusqu'à 100 entités.
- Toutes les entités dans une opération par lot doivent avoir la même clé de partition.
- Bien qu’il soit possible d’effectuer une requête dans un traitement par lots, il doit être la seule opération dans le lot.

Voici un code qui combine les deux insertions dans une opération de traitement :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L62-L71)]

### <a name="retrieve-all-entities-in-a-partition"></a>Récupérer toutes les entités dans une partition

Pour interroger une table pour toutes les entités dans une partition, utilisez un `TableQuery` objet. Ici, vous filtrez pour les entités dont « Smith » est la clé de partition.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L77-L82)]

Maintenant, vous imprimez les résultats :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L84-L85)]


### <a name="retrieve-a-range-of-entities-in-a-partition"></a>Récupérer une plage d’entités dans une partition

Si vous ne souhaitez pas toutes les entités dans une partition de requête, vous pouvez spécifier une plage en combinant le filtre de clé de partition avec un filtre de clé de ligne. Ici, vous utilisez des deux filtres pour obtenir toutes les entités dans la partition « Smith » où la clé de ligne (prénom) commence par une lettre au plus tôt le « M » dans l’alphabet.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L91-L100)]

Maintenant, vous imprimez les résultats :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L102-L103)]

### <a name="retrieve-a-single-entity"></a>Extraire une seule entité

Vous pouvez écrire une requête pour récupérer une entité unique et spécifique. Ici, vous utilisez un `TableOperation` pour spécifier le client « Ben Smith ». Au lieu d’une collection, vous obtenez en retour un `Customer`. Spécification de la clé de partition et la clé de ligne dans une requête est le moyen le plus rapide pour récupérer une seule entité du service de Table.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L109-L111)]

Maintenant, vous imprimez les résultats :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L113-L115)]


### <a name="replace-an-entity"></a>Remplacer une entité

Pour mettre à jour une entité, récupérer à partir du service de Table, de modifier l’objet d’entité, puis enregistrer les modifications dans le service de Table à l’aide un `Replace` opération. Cela entraîne l’entité à remplacer entièrement sur le serveur, à moins que l’entité sur le serveur a changé depuis sa récupération, auquel cas l’opération échoue. Cet échec est d’empêcher votre application de remplacer par inadvertance les modifications provenant d’autres sources.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L121-L128)]

### <a name="insert-or-replace-an-entity"></a>Insérer ou remplacer une entité

Parfois, vous ne connaissez pas si une entité existe dans la table. Et, dans ce cas, les valeurs actuelles stockées qu’il contient ne sont plus nécessaires. Vous pouvez utiliser `InsertOrReplace` pour créer l’entité ou le remplacer si elle existe, quel que soit son état.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L134-L141)]

### <a name="query-a-subset-of-entity-properties"></a>Un sous-ensemble de propriétés de l’entité de requête

Une requête de table peut récupérer seulement quelques propriétés d’une entité au lieu de tous les. Cette technique, appelée projection, peut améliorer les performances, en particulier pour les entités de grande taille. Ici, vous revenez à l’aide des adresses de messagerie uniquement `DynamicTableEntity` et `EntityResolver`. Notez que la projection n’est pas pris en charge sur l’émulateur de stockage local, pour que ce code s’exécute uniquement lorsque vous utilisez un compte sur le service de Table.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L147-L158)]

### <a name="retrieve-entities-in-pages-asynchronously"></a>Récupérer des entités dans les pages de façon asynchrone

Si vous lisez un grand nombre d’entités, et que vous souhaitez les traiter comme ils sont récupérés, plutôt que d’en attente pour tous les à retourner, vous pouvez utiliser une requête segmentée. Ici, vous des résultats dans les pages à l’aide d’un flux de travail asynchrone afin que l’exécution n’est pas bloquée pendant que vous patientez pour un grand ensemble de résultats à retourner.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L163-L178)]

Vous exécutez maintenant ce calcul synchrone :

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L180-L180)]

### <a name="delete-an-entity"></a>Supprimer une entité

Vous pouvez supprimer une entité une fois que vous l’avez extrait. Comme avec la mise à jour une entité, il échoue si l’entité a été modifié depuis son.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L186-L187)]

### <a name="delete-a-table"></a>Supprimer une table

Vous pouvez supprimer une table à partir d’un compte de stockage. Une table qui a été supprimée n’est pas disponible pour être recréé pour une période de temps après la suppression.

[!code-fsharp[TableStorage](../../../samples/snippets/fsharp/azure/table-storage.fsx#L193-L193)]

## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous avez appris les notions de base du stockage Table, suivez ces liens pour en savoir plus sur les tâches de stockage plus complexes et de l’API de Table de base de données Azure Cosmos.

- [Introduction à Azure Cosmos API de Table de base de données](https://docs.microsoft.com/azure/cosmos-db/table-introduction)
- [Bibliothèque cliente de stockage pour la référence .NET](https://docs.microsoft.com/dotnet/api/overview/azure/storage?view=azure-dotnet)
- [Fournisseur de Type de stockage Azure](http://fsprojects.github.io/AzureStorageTypeProvider/)
- [Blog de l’équipe stockage Azure](http://blogs.msdn.com/b/windowsazurestorage/)
- [Configuration des chaînes de connexion](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)
- [Prise en main avec un stockage de Table Windows Azure dans .NET](https://azure.microsoft.com/resources/samples/storage-table-dotnet-getting-started/)
