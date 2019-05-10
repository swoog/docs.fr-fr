---
title: Langage d'Entity SQL
ms.date: 03/30/2017
ms.assetid: 9e7d8837-28c5-429d-a824-7bafb59724cf
ms.openlocfilehash: ecbf9bc555594d205281237559037ac2a0e1cdb0
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64631704"
---
# <a name="entity-sql-language"></a>Langage d'Entity SQL
Entity SQL est un langage de requête indépendant du stockage et semblable à SQL. Entity SQL vous permet d'interroger des données d'entité, en tant qu'objets ou sous une forme tabulaire. Vous devez envisager d'utiliser Entity SQL dans les cas suivants :  
  
- Lorsqu'une requête doit être construite dynamiquement au moment de l'exécution. Dans ce cas, vous devez également envisager d'utiliser les méthodes du Générateur de requêtes d'<xref:System.Data.Objects.ObjectQuery%601> au lieu de construire une chaîne de requête Entity SQL au moment de l'exécution.  
  
- Lorsque vous voulez définir une requête dans le cadre de la définition du modèle. Seul Entity SQL est pris en charge dans un modèle de données. Pour plus d’informations, consultez [élément QueryView (MSL)](/ef/ef6/modeling/designer/advanced/edmx/msl-spec#queryview-element-msl)  
  
- Lorsque vous utilisez EntityClient pour retourner des données d'entité en lecture seule sous la forme d'ensembles de lignes à l'aide d'un <xref:System.Data.EntityClient.EntityDataReader>. Pour plus d’informations, consultez [fournisseur EntityClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).  
  
- Si vous êtes déjà un expert des langages de requête basés sur SQL, Entity SQL peut vous sembler le choix le plus naturel.  
  
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
  
 [Guide pratique pour Exécuter une requête qui retourne des objets de Type d’entité](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738694(v=vs.100))  
  
 [Guide pratique pour Exécuter une requête paramétrable](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))  
  
 [Guide pratique pour Naviguer parmi les relations à l’aide des propriétés de Navigation](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896321(v=vs.100))  
  
 [Guide pratique pour Appeler une fonction définie par l’utilisateur](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd490951(v=vs.100))  
  
 [Guide pratique pour Filtrer les données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716755(v=vs.100))  
  
 [Guide pratique pour Trier des données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716784(v=vs.100))  
  
 [Guide pratique pour Regrouper des données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896341(v=vs.100))  
  
 [Guide pratique pour Agréger des données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716738(v=vs.100))  
  
 [Guide pratique pour Exécuter une requête qui retourne des objets de Type anonyme](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738512(v=vs.100))  
  
 [Guide pratique pour Exécuter une requête qui retourne une Collection de Types primitifs](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738451(v=vs.100))  
  
 [Guide pratique pour Interroger les objets connexes dans une EntityCollection](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716708(v=vs.100))  
  
 [Guide pratique pour Ordonner l’Union de deux requêtes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896299(v=vs.100))  
  
 [Guide pratique pour Parcourir les résultats de la requête](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))  
  
## <a name="in-this-section"></a>Dans cette section  
 [Vue d’ensemble d’Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
  
 [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
  
## <a name="see-also"></a>Voir aussi

- [ADO.NET Entity Framework](../../../../../../docs/framework/data/adonet/ef/index.md)
- [Informations de référence sur le langage](../../../../../../docs/framework/data/adonet/ef/language-reference/index.md)
