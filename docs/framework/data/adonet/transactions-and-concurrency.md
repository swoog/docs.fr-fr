---
title: Transactions et accès simultané
ms.date: 03/30/2017
ms.assetid: f46570de-9e50-4fe6-8710-a8c31fa8569b
ms.openlocfilehash: ba857031a54374ee295c2bfd724e7fb8651b7c1f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61933703"
---
# <a name="transactions-and-concurrency"></a>Transactions et accès simultané
Une transaction est composée d’une seule commande ou d’un groupe de commandes qui s’exécutent sous forme de package. Les transactions vous permettent de combiner plusieurs opérations en une seule unité de travail. Si une panne se produit pendant la transaction, toutes les mises à jour sont ramenées dans l’état qui était le leur avant le début de la transaction.  
  
 Une transaction doit être conforme aux propriétés ACID (atomicité, cohérence, isolation et durabilité) afin de garantir la cohérence des données. La plupart des systèmes de bases de données relationnelles, tels que Microsoft SQL Server, prennent en charge des transactions en offrant des fonctionnalités de verrouillage, de journalisation et de gestion des transactions lorsqu’une application cliente exécute une opération de mise à jour, d’insertion ou de suppression.  
  
> [!NOTE]
>  Les transactions impliquant plusieurs ressources peuvent réduire l'accès concurrentiel si des verrous sont conservés trop longtemps. Par conséquent, réduisez autant que possible les transactions.  
  
 Si une transaction implique plusieurs tables dans la même base de données ou le même serveur, des transactions explicites dans des procédures stockées fonctionnent souvent mieux. Vous pouvez créer des transactions dans des procédures stockées SQL Server à l'aide des instructions Transact-SQL `BEGIN TRANSACTION`, `COMMIT TRANSACTION` et `ROLLBACK TRANSACTION`. Pour plus d'informations, voir la documentation en ligne de SQL Server.  
  
 Les transactions impliquant différents gestionnaires de ressources, tel qu’une transaction entre SQL Server et Oracle, requièrent une transaction distribuée.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Transactions locales](../../../../docs/framework/data/adonet/local-transactions.md)  
 Montre comment effectuer des transactions sur une base de données.  
  
 [Transactions distribuées](../../../../docs/framework/data/adonet/distributed-transactions.md)  
 Décrit comment effectuer des transactions distribuées dans ADO.NET.  
  
 [Intégration de System.Transactions à SQL Server](../../../../docs/framework/data/adonet/system-transactions-integration-with-sql-server.md)  
 Décrit <xref:System.Transactions> intégration avec SQL Server pour travailler avec les transactions distribuées.  
  
 [Accès concurrentiel optimiste](../../../../docs/framework/data/adonet/optimistic-concurrency.md)  
 Décrit les accès concurrentiels optimiste et pessimiste et la manière de tester les violations d'accès concurrentiel.  
  
## <a name="see-also"></a>Voir aussi

- [Notions de base des transactions](../../../../docs/framework/data/transactions/transaction-fundamentals.md)
- [Connexion à une source de données](../../../../docs/framework/data/adonet/connecting-to-a-data-source.md)
- [Commandes et paramètres](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [DataAdapters et DataReaders](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [DbProviderFactories](../../../../docs/framework/data/adonet/dbproviderfactories.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
