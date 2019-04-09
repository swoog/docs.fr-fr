---
title: Extraction et modification de données dans ADO.NET
ms.date: 03/30/2017
ms.assetid: 722e7f87-3691-46c6-87e8-7d159722d675
ms.openlocfilehash: bf26cd216b456e912dbaf0019114ea8e60b439a1
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59097618"
---
# <a name="retrieving-and-modifying-data-in-adonet"></a>Extraction et modification de données dans ADO.NET
Une fonction principale de toute application de base de données consiste à se connecter à une source de données et extraire les données qu'elle contient. Les fournisseurs de données .NET Framework d’ADO.NET font Office de passerelle entre une application et une source de données, ce qui vous permet d’exécuter des commandes et d’extraire des données à l’aide un **DataReader** ou un **DataAdapter** . Une fonction clé de toute application de base de données est la capacité à mettre à jour les données stockées dans la base de données. Dans ADO.NET, la mise à jour des données implique l’utilisation de la **DataAdapter** et <xref:System.Data.DataSet>, et **commande** objets ; et il peuvent également impliquer l’utilisation de transactions.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Connexion à une source de données](../../../../docs/framework/data/adonet/connecting-to-a-data-source.md)  
 Décrit comment établir une connexion à une source de données et comment travailler avec des événements de connexion.  
  
 [Chaînes de connexion](../../../../docs/framework/data/adonet/connection-strings.md)  
 Contient des rubriques qui décrivent divers aspects de l'utilisation de chaînes de connexion, y compris des mots clés de chaîne de connexion, des informations de sécurité, ainsi que de leur stockage et leur extraction.  
  
 [Regroupement de connexions](../../../../docs/framework/data/adonet/connection-pooling.md)  
 Décrit le regroupement de connexions pour les fournisseurs de données .NET Framework.  
  
 [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 Contient des rubriques qui décrivent comment créer des commandes et des générateurs de commande, configurer des paramètres et exécuter des commandes pour extraire et modifier des données.  
  
 [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)  
 Contient des rubriques qui décrivent les objets DataReader et DataAdapter, les paramètres, la gestion des événements DataAdapter et l'exécution d'opérations par lots.  
  
 [Transactions et accès simultané](../../../../docs/framework/data/adonet/transactions-and-concurrency.md)  
 Contient des rubriques qui décrivent comment effectuer des transactions locales, des transactions distribuées et travailler avec l’accès concurrentiel optimiste.  
  
 [Extraction de l'identité ou de valeurs à numérotation automatique](../../../../docs/framework/data/adonet/retrieving-identity-or-autonumber-values.md)  
 Fournit un exemple de mappage des valeurs générées pour un **identité** colonne dans une table SQL Server ou pour un **NuméroAuto** champ dans une table Microsoft Access, à une colonne d’une ligne insérée dans une table. Traite de la fusion de valeurs d'identité dans un `DataTable`.  
  
 [Extraction de données binaires](../../../../docs/framework/data/adonet/retrieving-binary-data.md)  
 Décrit comment récupérer des données binaires ou grosses structures de données à l’aide de `CommandBehavior`.`SequentialAccess` Pour modifier le comportement par défaut d’un `DataReader`.  
  
 [Modification des données avec les procédures stockées](../../../../docs/framework/data/adonet/modifying-data-with-stored-procedures.md)  
 Décrit comment utiliser des paramètres d'entrée et sortie de procédure stockée afin d'insérer une ligne dans une base de données et retourner une nouvelle valeur d'identité.  
  
 [Extraction des informations de schéma de base de données](../../../../docs/framework/data/adonet/retrieving-database-schema-information.md)  
 Décrit la manière d'obtenir des bases de données ou des catalogues disponibles, des tables et des vues dans une base de données, des contraintes existantes pour des tables et d'autres informations de schéma à partir d'une source de données.  
  
 [DbProviderFactories](../../../../docs/framework/data/adonet/dbproviderfactories.md)  
 Décrit le modèle fabrique de fournisseurs et illustre l'utilisation des classes de base dans l'espace de noms `System.Data.Common`.  
  
 [Traçage de données dans ADO.NET](../../../../docs/framework/data/adonet/data-tracing.md)  
 Décrit la manière dont ADO.NET offre une fonctionnalité intégrée de traçage de données.  
  
 [Compteurs de performances](../../../../docs/framework/data/adonet/performance-counters.md)  
 Décrit les compteurs de performance disponibles pour `SqlClient` et `OracleClient`.  
  
 [Programmation asynchrone](../../../../docs/framework/data/adonet/asynchronous-programming.md)  
 Décrit la prise en charge [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)] de la programmation asynchrone.  
  
 [Prise en charge de la diffusion en continu pour SqlClient](../../../../docs/framework/data/adonet/sqlclient-streaming-support.md)  
 Explique comment écrire des applications ces flux de données à partir de SQL Server sans avoir à charger entièrement en mémoire.  
  
## <a name="see-also"></a>Voir aussi

- [Mappages de types de données dans ADO.NET](../../../../docs/framework/data/adonet/data-type-mappings-in-ado-net.md)
- [DataSets, DataTables et DataViews](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)
- [Sécurisation des applications ADO.NET](../../../../docs/framework/data/adonet/securing-ado-net-applications.md)
- [SQL Server et ADO.NET](../../../../docs/framework/data/adonet/sql/index.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
