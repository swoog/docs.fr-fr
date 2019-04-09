---
title: Langage d'Entity SQL
ms.date: 03/30/2017
ms.assetid: 9e7d8837-28c5-429d-a824-7bafb59724cf
ms.openlocfilehash: 09ec1a5518ec0847b54394449f32b3068c811577
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59140931"
---
# <a name="entity-sql-language"></a><span data-ttu-id="b8b65-102">Langage d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="b8b65-102">Entity SQL Language</span></span>
<span data-ttu-id="b8b65-103">Entity SQL est un langage de requête indépendant du stockage et semblable à SQL.</span><span class="sxs-lookup"><span data-stu-id="b8b65-103">Entity SQL is a storage-independent query language that is similar to SQL.</span></span> <span data-ttu-id="b8b65-104">Entity SQL vous permet d'interroger des données d'entité, en tant qu'objets ou sous une forme tabulaire.</span><span class="sxs-lookup"><span data-stu-id="b8b65-104">Entity SQL allows you to query entity data, either as objects or in a tabular form.</span></span> <span data-ttu-id="b8b65-105">Vous devez envisager d'utiliser Entity SQL dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="b8b65-105">You should consider using Entity SQL in the following cases:</span></span>  
  
-   <span data-ttu-id="b8b65-106">Lorsqu'une requête doit être construite dynamiquement au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="b8b65-106">When a query must be dynamically constructed at runtime.</span></span> <span data-ttu-id="b8b65-107">Dans ce cas, vous devez également envisager d'utiliser les méthodes du Générateur de requêtes d'<xref:System.Data.Objects.ObjectQuery%601> au lieu de construire une chaîne de requête Entity SQL au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="b8b65-107">In this case, you should also consider using the query builder methods of <xref:System.Data.Objects.ObjectQuery%601> instead of constructing an Entity SQL query string at runtime.</span></span>  
  
-   <span data-ttu-id="b8b65-108">Lorsque vous voulez définir une requête dans le cadre de la définition du modèle.</span><span class="sxs-lookup"><span data-stu-id="b8b65-108">When you want to define a query as part of the model definition.</span></span> <span data-ttu-id="b8b65-109">Seul Entity SQL est pris en charge dans un modèle de données.</span><span class="sxs-lookup"><span data-stu-id="b8b65-109">Only Entity SQL is supported in a data model.</span></span> <span data-ttu-id="b8b65-110">Pour plus d’informations, consultez [élément QueryView (MSL)](/ef/ef6/modeling/designer/advanced/edmx/msl-spec#queryview-element-msl)</span><span class="sxs-lookup"><span data-stu-id="b8b65-110">For more information, see [QueryView Element (MSL)](/ef/ef6/modeling/designer/advanced/edmx/msl-spec#queryview-element-msl)</span></span>  
  
-   <span data-ttu-id="b8b65-111">Lorsque vous utilisez EntityClient pour retourner des données d'entité en lecture seule sous la forme d'ensembles de lignes à l'aide d'un <xref:System.Data.EntityClient.EntityDataReader>.</span><span class="sxs-lookup"><span data-stu-id="b8b65-111">When using EntityClient to return read-only entity data as rowsets using a <xref:System.Data.EntityClient.EntityDataReader>.</span></span> <span data-ttu-id="b8b65-112">Pour plus d’informations, consultez [fournisseur EntityClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).</span><span class="sxs-lookup"><span data-stu-id="b8b65-112">For more information, see [EntityClient Provider for the Entity Framework](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).</span></span>  
  
-   <span data-ttu-id="b8b65-113">Si vous êtes déjà un expert des langages de requête basés sur SQL, Entity SQL peut vous sembler le choix le plus naturel.</span><span class="sxs-lookup"><span data-stu-id="b8b65-113">If you are already an expert in SQL-based query languages, Entity SQL may seem the most natural to you.</span></span>  
  
## <a name="using-entity-sql-with-the-entityclient-provider"></a><span data-ttu-id="b8b65-114">Utilisation de Entity SQL avec le fournisseur EntityClient</span><span class="sxs-lookup"><span data-stu-id="b8b65-114">Using Entity SQL with the EntityClient provider</span></span>  
 <span data-ttu-id="b8b65-115">Pour plus d'informations sur l'utilisation de Entity SQL avec le fournisseur EntityClient, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8b65-115">If you want to use Entity SQL with the EntityClient provider, see the following topics for more information:</span></span>  
  
 [<span data-ttu-id="b8b65-116">Fournisseur EntityClient pour Entity Framework</span><span class="sxs-lookup"><span data-stu-id="b8b65-116">EntityClient Provider for the Entity Framework</span></span>](../../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)  
  
 [<span data-ttu-id="b8b65-117">Procédure : Créer une chaîne de connexion EntityConnection</span><span class="sxs-lookup"><span data-stu-id="b8b65-117">How to: Build an EntityConnection Connection String</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-build-an-entityconnection-connection-string.md)  
  
 [<span data-ttu-id="b8b65-118">Procédure : Exécuter une requête qui retourne des résultats PrimitiveType</span><span class="sxs-lookup"><span data-stu-id="b8b65-118">How to: Execute a Query that Returns PrimitiveType Results</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-primitivetype-results.md)  
  
 [<span data-ttu-id="b8b65-119">Procédure : Exécuter une requête qui retourne des résultats StructuralType</span><span class="sxs-lookup"><span data-stu-id="b8b65-119">How to: Execute a Query that Returns StructuralType Results</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md)  
  
 [<span data-ttu-id="b8b65-120">Procédure : Exécuter une requête qui retourne des résultats RefType</span><span class="sxs-lookup"><span data-stu-id="b8b65-120">How to: Execute a Query that Returns RefType Results</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-reftype-results.md)  
  
 [<span data-ttu-id="b8b65-121">Procédure : Exécuter une requête qui retourne des types complexes</span><span class="sxs-lookup"><span data-stu-id="b8b65-121">How to: Execute a Query that Returns Complex Types</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-complex-types.md)  
  
 [<span data-ttu-id="b8b65-122">Procédure : Exécuter une requête qui retourne des collections imbriquées</span><span class="sxs-lookup"><span data-stu-id="b8b65-122">How to: Execute a Query that Returns Nested Collections</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-nested-collections.md)  
  
 [<span data-ttu-id="b8b65-123">Procédure : Exécuter une requête paramétrable Entity SQL avec EntityCommand</span><span class="sxs-lookup"><span data-stu-id="b8b65-123">How to: Execute a Parameterized Entity SQL Query Using EntityCommand</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-parameterized-entity-sql-query-using-entitycommand.md)  
  
 [<span data-ttu-id="b8b65-124">Procédure : Exécuter une procédure stockée paramétrable avec EntityCommand</span><span class="sxs-lookup"><span data-stu-id="b8b65-124">How to: Execute a Parameterized Stored Procedure Using EntityCommand</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-parameterized-stored-procedure-using-entitycommand.md)  
  
 [<span data-ttu-id="b8b65-125">Procédure : Exécuter une requête polymorphe</span><span class="sxs-lookup"><span data-stu-id="b8b65-125">How to: Execute a Polymorphic Query</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-polymorphic-query.md)  
  
 [<span data-ttu-id="b8b65-126">Procédure : Parcourir les relations avec l’opérateur Navigate</span><span class="sxs-lookup"><span data-stu-id="b8b65-126">How to: Navigate Relationships with the Navigate Operator</span></span>](../../../../../../docs/framework/data/adonet/ef/how-to-navigate-relationships-with-the-navigate-operator.md)  
  
## <a name="using-entity-sql-with-object-queries"></a><span data-ttu-id="b8b65-127">Utilisation de Entity SQL avec des requêtes d'objet</span><span class="sxs-lookup"><span data-stu-id="b8b65-127">Using Entity SQL with object queries</span></span>  
 <span data-ttu-id="b8b65-128">Pour plus d'informations sur l'utilisation de Entity SQL avec des requêtes d'objet, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b8b65-128">If you want to use Entity SQL with object queries, see the following topics for more information:</span></span>  
  
 [<span data-ttu-id="b8b65-129">Procédure : Exécuter une requête qui retourne des objets de Type d’entité</span><span class="sxs-lookup"><span data-stu-id="b8b65-129">How to: Execute a Query that Returns Entity Type Objects</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738694(v=vs.100))  
  
 [<span data-ttu-id="b8b65-130">Procédure : Exécuter une requête paramétrable</span><span class="sxs-lookup"><span data-stu-id="b8b65-130">How to: Execute a Parameterized Query</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738521(v=vs.100))  
  
 [<span data-ttu-id="b8b65-131">Procédure : Naviguer parmi les relations à l’aide des propriétés de Navigation</span><span class="sxs-lookup"><span data-stu-id="b8b65-131">How to: Navigate Relationships Using Navigation Properties</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896321(v=vs.100))  
  
 [<span data-ttu-id="b8b65-132">Procédure : Appeler une fonction définie par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="b8b65-132">How to: Call a User-Defined Function</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/dd490951(v=vs.100))  
  
 [<span data-ttu-id="b8b65-133">Procédure : filtrer les données</span><span class="sxs-lookup"><span data-stu-id="b8b65-133">How to: Filter Data</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716755(v=vs.100))  
  
 [<span data-ttu-id="b8b65-134">Procédure : trier les données</span><span class="sxs-lookup"><span data-stu-id="b8b65-134">How to: Sort Data</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716784(v=vs.100))  
  
 [<span data-ttu-id="b8b65-135">Procédure : Regrouper des données</span><span class="sxs-lookup"><span data-stu-id="b8b65-135">How to: Group Data</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896341(v=vs.100))  
  
 [<span data-ttu-id="b8b65-136">Procédure : Agréger des données</span><span class="sxs-lookup"><span data-stu-id="b8b65-136">How to: Aggregate Data</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716738(v=vs.100))  
  
 [<span data-ttu-id="b8b65-137">Procédure : Exécuter une requête qui retourne des objets de Type anonyme</span><span class="sxs-lookup"><span data-stu-id="b8b65-137">How to: Execute a Query that Returns Anonymous Type Objects</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738512(v=vs.100))  
  
 [<span data-ttu-id="b8b65-138">Procédure : Exécuter une requête qui retourne une Collection de Types primitifs</span><span class="sxs-lookup"><span data-stu-id="b8b65-138">How to: Execute a Query that Returns a Collection of Primitive Types</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738451(v=vs.100))  
  
 [<span data-ttu-id="b8b65-139">Procédure : interroger les objets connexes d'un EntityCollection</span><span class="sxs-lookup"><span data-stu-id="b8b65-139">How to: Query Related Objects in an EntityCollection</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716708(v=vs.100))  
  
 [<span data-ttu-id="b8b65-140">Procédure : Ordonner l’Union de deux requêtes</span><span class="sxs-lookup"><span data-stu-id="b8b65-140">How to: Order the Union of Two Queries</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896299(v=vs.100))  
  
 [<span data-ttu-id="b8b65-141">Procédure : Parcourir les résultats de la requête</span><span class="sxs-lookup"><span data-stu-id="b8b65-141">How to: Page Through Query Results</span></span>](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))  
  
## <a name="in-this-section"></a><span data-ttu-id="b8b65-142">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b8b65-142">In This Section</span></span>  
 [<span data-ttu-id="b8b65-143">Vue d'ensemble d'Entity SQL</span><span class="sxs-lookup"><span data-stu-id="b8b65-143">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
  
 [<span data-ttu-id="b8b65-144">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="b8b65-144">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
  
## <a name="see-also"></a><span data-ttu-id="b8b65-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8b65-145">See also</span></span>

- [<span data-ttu-id="b8b65-146">ADO.NET Entity Framework</span><span class="sxs-lookup"><span data-stu-id="b8b65-146">ADO.NET Entity Framework</span></span>](../../../../../../docs/framework/data/adonet/ef/index.md)
- [<span data-ttu-id="b8b65-147">Informations de référence sur le langage</span><span class="sxs-lookup"><span data-stu-id="b8b65-147">Language Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/index.md)
