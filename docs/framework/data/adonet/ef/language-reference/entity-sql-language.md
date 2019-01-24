---
title: Langage d'Entity SQL
ms.date: 03/30/2017
ms.assetid: 9e7d8837-28c5-429d-a824-7bafb59724cf
ms.openlocfilehash: 0c698f04c3b95ffb204a20d41e91ef3f6210c5d8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54494094"
---
# <a name="entity-sql-language"></a>Langage d'Entity SQL
Entity SQL est un langage de requête indépendant du stockage et semblable à SQL. Entity SQL vous permet d'interroger des données d'entité, en tant qu'objets ou sous une forme tabulaire. Vous devez envisager d'utiliser Entity SQL dans les cas suivants :  
  
-   Lorsqu'une requête doit être construite dynamiquement au moment de l'exécution. Dans ce cas, vous devez également envisager d'utiliser les méthodes du Générateur de requêtes d'<xref:System.Data.Objects.ObjectQuery%601> au lieu de construire une chaîne de requête Entity SQL au moment de l'exécution.  
  
-   Lorsque vous voulez définir une requête dans le cadre de la définition du modèle. Seul Entity SQL est pris en charge dans un modèle de données. Pour plus d’informations, consultez [élément QueryView (MSL)](/ef/ef6/modeling/designer/advanced/edmx/msl-spec#queryview-element-msl)  
  
-   Lorsque vous utilisez EntityClient pour retourner des données d'entité en lecture seule sous la forme d'ensembles de lignes à l'aide d'un <xref:System.Data.EntityClient.EntityDataReader>. Pour plus d’informations, consultez [fournisseur EntityClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).  
  
-   Si vous êtes déjà un expert des langages de requête basés sur SQL, Entity SQL peut vous sembler le choix le plus naturel.  
  
## <a name="using-entity-sql-with-the-entityclient-provider"></a>Utilisation de Entity SQL avec le fournisseur EntityClient  
 Pour plus d'informations sur l'utilisation de Entity SQL avec le fournisseur EntityClient, consultez les rubriques suivantes :  
  
 [Fournisseur EntityClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)  
  
 [Guide pratique pour Créer une chaîne de connexion EntityConnection](../../../../../../docs/framework/data/adonet/ef/how-to-build-an-entityconnection-connection-string.md)  
  
 [Guide pratique pour Exécuter une requête qui retourne les résultats PrimitiveType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md)  
  
 [Guide pratique pour Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)  
  
 [Guide pratique pour Exécuter une requête qui retourne les résultats RefType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-reftype-results.md)  
  
 [Guide pratique pour Exécuter une requête qui retourne des Types complexes](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-complex-types.md)  
  
 [Guide pratique pour Exécuter une requête qui retourne les Collections imbriquées](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-nested-collections.md)  
  
 [Guide pratique pour Exécuter une requête paramétrée Entity SQL à l’aide d’EntityCommand](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-parameterized-entity-sql-query-using-entitycommand.md)  
  
 [Guide pratique pour Exécuter une procédure stockée paramétrée utilisant EntityCommand](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-parameterized-stored-procedure-using-entitycommand.md)  
  
 [Guide pratique pour Exécuter une requête polymorphe](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-polymorphic-query.md)  
  
 [Guide pratique pour Naviguer parmi les relations avec l’opérateur Navigate](../../../../../../docs/framework/data/adonet/ef/how-to-navigate-relationships-with-the-navigate-operator.md)  
  
## <a name="using-entity-sql-with-object-queries"></a>Utilisation de Entity SQL avec des requêtes d'objet  
 Pour plus d'informations sur l'utilisation de Entity SQL avec des requêtes d'objet, consultez les rubriques suivantes :  
  
 [Guide pratique pour Exécuter une requête qui retourne des objets de Type d’entité](https://msdn.microsoft.com/library/f73e137d-1534-42bb-9e31-99ca42c19b48)  
  
 [Guide pratique pour Exécuter une requête paramétrable](https://msdn.microsoft.com/library/42048f03-c65c-4d98-b50a-3e7d537a63e8)  
  
 [Guide pratique pour Naviguer parmi les relations à l’aide des propriétés de Navigation](https://msdn.microsoft.com/library/b1d71c7d-16a7-4b46-96ac-690176bd5057)  
  
 [Guide pratique pour Appeler une fonction définie par l’utilisateur](https://msdn.microsoft.com/library/ad131b86-8b4e-4747-8605-d4fc64fb9d02)  
  
 [Guide pratique pour Filtrer les données](https://msdn.microsoft.com/library/776f8556-3350-4572-804a-b1513515c1b2)  
  
 [Guide pratique pour Trier des données](https://msdn.microsoft.com/library/c05f2506-cb9d-4ebc-822b-300042ad53e7)  
  
 [Guide pratique pour Regrouper des données](https://msdn.microsoft.com/library/df801d9d-9a8a-4157-97a6-5016b18998e1)  
  
 [Guide pratique pour Agréger des données](https://msdn.microsoft.com/library/4cf04ce8-3c0f-4f88-9d97-8fac8622598d)  
  
 [Guide pratique pour Exécuter une requête qui retourne des objets de Type anonyme](https://msdn.microsoft.com/library/3b264025-e911-4d73-90ce-992d2b9d189d)  
  
 [Guide pratique pour Exécuter une requête qui retourne une Collection de Types primitifs](https://msdn.microsoft.com/library/115b52c0-4f27-4253-8991-284b450000b5)  
  
 [Guide pratique pour Interroger les objets connexes dans une EntityCollection](https://msdn.microsoft.com/library/11ce946f-16f8-4c1d-9d80-f740853807ba)  
  
 [Guide pratique pour Ordonner l’Union de deux requêtes](https://msdn.microsoft.com/library/853c583a-eaba-4400-830d-be974e735313)  
  
 [Guide pratique pour Parcourir les résultats de la requête](https://msdn.microsoft.com/library/ffc0f920-e7de-42e0-9b12-ef356421d030)  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
  
 [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
  
## <a name="see-also"></a>Voir aussi
- [ADO.NET Entity Framework](../../../../../../docs/framework/data/adonet/ef/index.md)
- [Informations de référence sur le langage](../../../../../../docs/framework/data/adonet/ef/language-reference/index.md)
