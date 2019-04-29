---
title: Langage d'Entity SQL
ms.date: 03/30/2017
ms.assetid: 9e7d8837-28c5-429d-a824-7bafb59724cf
ms.openlocfilehash: 09ec1a5518ec0847b54394449f32b3068c811577
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785188"
---
# <a name="entity-sql-language"></a><span data-ttu-id="04333-102">Langage d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="04333-102">Entity SQL Language</span></span>
<span data-ttu-id="04333-103">Entity SQL est un langage de requête indépendant du stockage et semblable à SQL.</span><span class="sxs-lookup"><span data-stu-id="04333-103">Entity SQL is a storage-independent query language that is similar to SQL.</span></span> <span data-ttu-id="04333-104">Entity SQL vous permet d'interroger des données d'entité, en tant qu'objets ou sous une forme tabulaire.</span><span class="sxs-lookup"><span data-stu-id="04333-104">Entity SQL allows you to query entity data, either as objects or in a tabular form.</span></span> <span data-ttu-id="04333-105">Vous devez envisager d'utiliser Entity SQL dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="04333-105">You should consider using Entity SQL in the following cases:</span></span>  
  
- <span data-ttu-id="04333-106">Lorsqu'une requête doit être construite dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="04333-106">When a query must be dynamically constructed at runtime.</span></span> <span data-ttu-id="04333-107">Dans ce cas, vous devez également envisager d'utiliser les méthodes du Générateur de requêtes d'<xref:System.Data.Objects.ObjectQuery%601> au lieu de construire une chaîne de requête Entity SQL au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="04333-107">In this case, you should also consider using the query builder methods of <xref:System.Data.Objects.ObjectQuery%601> instead of constructing an Entity SQL query string at runtime.</span></span>  
  
- <span data-ttu-id="04333-108">Lorsque vous voulez définir une requête dans le cadre de la définition du modèle.</span><span class="sxs-lookup"><span data-stu-id="04333-108">When you want to define a query as part of the model definition.</span></span> <span data-ttu-id="04333-109">Seul Entity SQL est pris en charge dans un modèle de données.</span><span class="sxs-lookup"><span data-stu-id="04333-109">Only Entity SQL is supported in a data model.</span></span> <span data-ttu-id="04333-110">Pour plus d’informations, consultez [élément QueryView (MSL)](/ef/ef6/modeling/designer/advanced/edmx/msl-spec#queryview-element-msl)</span><span class="sxs-lookup"><span data-stu-id="04333-110">For more information, see [QueryView Element (MSL)](/ef/ef6/modeling/designer/advanced/edmx/msl-spec#queryview-element-msl)</span></span>  
  
- <span data-ttu-id="04333-111">Lorsque vous utilisez EntityClient pour retourner des données d'entité en lecture seule sous la forme d'ensembles de lignes à l'aide d'un <xref:System.Data.EntityClient.EntityDataReader>.</span><span class="sxs-lookup"><span data-stu-id="04333-111">When using EntityClient to return read-only entity data as rowsets using a <xref:System.Data.EntityClient.EntityDataReader>.</span></span> <span data-ttu-id="04333-112">Pour plus d’informations, consultez [fournisseur EntityClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).</span><span class="sxs-lookup"><span data-stu-id="04333-112">For more information, see [EntityClient Provider for the Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).</span></span>  
  
- <span data-ttu-id="04333-113">Si vous êtes déjà un expert des langages de requête basés sur SQL, Entity SQL peut vous sembler le choix le plus naturel.</span><span class="sxs-lookup"><span data-stu-id="04333-113">If you are already an expert in SQL-based query languages, Entity SQL may seem the most natural to you.</span></span>  
  
## <a name="using-entity-sql-with-the-entityclient-provider"></a><span data-ttu-id="04333-114">Utilisation de Entity SQL avec le fournisseur EntityClient</span><span class="sxs-lookup"><span data-stu-id="04333-114">Using Entity SQL with the EntityClient provider</span></span>  
 <span data-ttu-id="04333-115">Pour plus d'informations sur l'utilisation de Entity SQL avec le fournisseur EntityClient, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="04333-115">If you want to use Entity SQL with the EntityClient provider, see the following topics for more information:</span></span>  
  
 [<span data-ttu-id="04333-116">Fournisseur EntityClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="04333-116">EntityClient Provider for the Entity Framework</span></span>](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)  
  
 [<span data-ttu-id="04333-117">Guide pratique pour Créer une chaîne de connexion EntityConnection</span><span class="sxs-lookup"><span data-stu-id="04333-117">How to: Build an EntityConnection Connection String</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-build-an-entityconnection-connection-string.md)  
  
 [<span data-ttu-id="04333-118">Guide pratique pour Exécuter une requête qui retourne les résultats PrimitiveType</span><span class="sxs-lookup"><span data-stu-id="04333-118">How to: Execute a Query that Returns PrimitiveType Results</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md)  
  
 [<span data-ttu-id="04333-119">Guide pratique pour Exécuter une requête qui retourne des résultats StructuralType</span><span class="sxs-lookup"><span data-stu-id="04333-119">How to: Execute a Query that Returns StructuralType Results</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)  
  
 [<span data-ttu-id="04333-120">Guide pratique pour Exécuter une requête qui retourne les résultats RefType</span><span class="sxs-lookup"><span data-stu-id="04333-120">How to: Execute a Query that Returns RefType Results</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-reftype-results.md)  
  
 [<span data-ttu-id="04333-121">Guide pratique pour Exécuter une requête qui retourne des Types complexes</span><span class="sxs-lookup"><span data-stu-id="04333-121">How to: Execute a Query that Returns Complex Types</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-complex-types.md)  
  
 [<span data-ttu-id="04333-122">Guide pratique pour Exécuter une requête qui retourne les Collections imbriquées</span><span class="sxs-lookup"><span data-stu-id="04333-122">How to: Execute a Query that Returns Nested Collections</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-nested-collections.md)  
  
 [<span data-ttu-id="04333-123">Guide pratique pour Exécuter une requête paramétrée Entity SQL à l’aide d’EntityCommand</span><span class="sxs-lookup"><span data-stu-id="04333-123">How to: Execute a Parameterized Entity SQL Query Using EntityCommand</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-parameterized-entity-sql-query-using-entitycommand.md)  
  
 [<span data-ttu-id="04333-124">Guide pratique pour Exécuter une procédure stockée paramétrée utilisant EntityCommand</span><span class="sxs-lookup"><span data-stu-id="04333-124">How to: Execute a Parameterized Stored Procedure Using EntityCommand</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-parameterized-stored-procedure-using-entitycommand.md)  
  
 [<span data-ttu-id="04333-125">Guide pratique pour Exécuter une requête polymorphe</span><span class="sxs-lookup"><span data-stu-id="04333-125">How to: Execute a Polymorphic Query</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-polymorphic-query.md)  
  
 [<span data-ttu-id="04333-126">Guide pratique pour Naviguer parmi les relations avec l’opérateur Navigate</span><span class="sxs-lookup"><span data-stu-id="04333-126">How to: Navigate Relationships with the Navigate Operator</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-navigate-relationships-with-the-navigate-operator.md)  
  
## <a name="using-entity-sql-with-object-queries"></a><span data-ttu-id="04333-127">Utilisation de Entity SQL avec des requêtes d'objet</span><span class="sxs-lookup"><span data-stu-id="04333-127">Using Entity SQL with object queries</span></span>  
 <span data-ttu-id="04333-128">Pour plus d'informations sur l'utilisation de Entity SQL avec des requêtes d'objet, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="04333-128">If you want to use Entity SQL with object queries, see the following topics for more information:</span></span>  
  
 <span data-ttu-id="04333-129">[Guide pratique pour Exécuter une requête qui retourne des objets de Type d’entité](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738694(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-129">[How to: Execute a Query that Returns Entity Type Objects](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738694(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-130">[Guide pratique pour Exécuter une requête paramétrable](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-130">[How to: Execute a Parameterized Query](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-131">[Guide pratique pour Naviguer parmi les relations à l’aide des propriétés de Navigation](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896321(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-131">[How to: Navigate Relationships Using Navigation Properties](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896321(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-132">[Guide pratique pour Appeler une fonction définie par l’utilisateur](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd490951(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-132">[How to: Call a User-Defined Function](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd490951(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-133">[Guide pratique pour Filtrer les données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716755(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-133">[How to: Filter Data](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716755(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-134">[Guide pratique pour Trier des données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716784(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-134">[How to: Sort Data](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716784(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-135">[Guide pratique pour Regrouper des données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896341(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-135">[How to: Group Data](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896341(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-136">[Guide pratique pour Agréger des données](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716738(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-136">[How to: Aggregate Data](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716738(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-137">[Guide pratique pour Exécuter une requête qui retourne des objets de Type anonyme](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738512(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-137">[How to: Execute a Query that Returns Anonymous Type Objects](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738512(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-138">[Guide pratique pour Exécuter une requête qui retourne une Collection de Types primitifs](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738451(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-138">[How to: Execute a Query that Returns a Collection of Primitive Types](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738451(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-139">[Guide pratique pour Interroger les objets connexes dans une EntityCollection](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716708(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-139">[How to: Query Related Objects in an EntityCollection](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716708(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-140">[Guide pratique pour Ordonner l’Union de deux requêtes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896299(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-140">[How to: Order the Union of Two Queries](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896299(v=vs.100))</span></span>  
  
 <span data-ttu-id="04333-141">[Guide pratique pour Parcourir les résultats de la requête](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="04333-141">[How to: Page Through Query Results](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="04333-142">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="04333-142">In This Section</span></span>  
 [<span data-ttu-id="04333-143">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="04333-143">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
  
 [<span data-ttu-id="04333-144">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="04333-144">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
  
## <a name="see-also"></a><span data-ttu-id="04333-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04333-145">See also</span></span>

- [<span data-ttu-id="04333-146">ADO.NET Entity Framework</span><span class="sxs-lookup"><span data-stu-id="04333-146">ADO.NET Entity Framework</span></span>](../../../../../../docs/framework/data/adonet/ef/index.md)
- [<span data-ttu-id="04333-147">Informations de référence sur le langage</span><span class="sxs-lookup"><span data-stu-id="04333-147">Language Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/index.md)
