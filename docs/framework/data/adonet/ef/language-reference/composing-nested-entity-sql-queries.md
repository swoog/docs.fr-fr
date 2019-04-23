---
title: Composition de requêtes Entity SQL imbriquées
ms.date: 03/30/2017
ms.assetid: 685d4cd3-2c1f-419f-bb46-c9d97a351eeb
ms.openlocfilehash: 4d6892e96cfbc9c5ba9d389aa03588c5133c7943
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137980"
---
# <a name="composing-nested-entity-sql-queries"></a><span data-ttu-id="cba9b-102">Composition de requêtes Entity SQL imbriquées</span><span class="sxs-lookup"><span data-stu-id="cba9b-102">Composing Nested Entity SQL Queries</span></span>
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="cba9b-103">est un langage fonctionnel riche.</span><span class="sxs-lookup"><span data-stu-id="cba9b-103">is a rich functional language.</span></span> <span data-ttu-id="cba9b-104">Le bloc de construction [!INCLUDE[esql](../../../../../../includes/esql-md.md)] est une expression.</span><span class="sxs-lookup"><span data-stu-id="cba9b-104">The building block of [!INCLUDE[esql](../../../../../../includes/esql-md.md)] is an expression.</span></span> <span data-ttu-id="cba9b-105">Contrairement au langage SQL classique, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] n’est pas limité à un jeu de résultats tabulaire : [!INCLUDE[esql](../../../../../../includes/esql-md.md)] prend en charge la composition d’expressions complexes pouvant contenir des littéraux, des paramètres ou des expressions imbriquées.</span><span class="sxs-lookup"><span data-stu-id="cba9b-105">Unlike conventional SQL, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] is not limited to a tabular result set: [!INCLUDE[esql](../../../../../../includes/esql-md.md)] supports composing complex expressions that can have literals, parameters, or nested expressions.</span></span> <span data-ttu-id="cba9b-106">Une valeur dans l’expression peut être paramétrée ou composée d’une autre expression.</span><span class="sxs-lookup"><span data-stu-id="cba9b-106">A value in the expression can be parameterized or composed of some other expression.</span></span>  
  
## <a name="nested-expressions"></a><span data-ttu-id="cba9b-107">Expressions imbriquées</span><span class="sxs-lookup"><span data-stu-id="cba9b-107">Nested Expressions</span></span>  
 <span data-ttu-id="cba9b-108">Une expression imbriquée peut être placée partout où une valeur du type qu'elle retourne est acceptée.</span><span class="sxs-lookup"><span data-stu-id="cba9b-108">A nested expression can be placed anywhere a value of the type it returns is accepted.</span></span> <span data-ttu-id="cba9b-109">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cba9b-109">For example:</span></span>  
  
```  
-- Returns a hierarchical collection of three elements at top-level.   
-- x must be passed in the parameter collection.  
ROW(@x, {@x}, {@x, 4, 5}, {@x, 7, 8, 9})  
  
-- Returns a hierarchical collection of one element at top-level.  
-- x must be passed in the parameter collection.  
{{{@x}}};  
```  
  
 <span data-ttu-id="cba9b-110">Une requête imbriquée peut être placée dans une clause de projection.</span><span class="sxs-lookup"><span data-stu-id="cba9b-110">A nested query can be placed in a projection clause.</span></span> <span data-ttu-id="cba9b-111">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cba9b-111">For example:</span></span>  
  
```  
-- Returns a collection of rows where each row contains an Address entity.  
-- and a collection of references to its corresponding SalesOrderHeader entities.  
SELECT address, (SELECT DEREF(soh)   
                    FROM NAVIGATE(address, AdventureWorksModel.FK_SalesOrderHeader_Address_BillToAddressID) AS soh)   
                    AS salesOrderHeader FROM AdventureWorksEntities.Address AS address  
```  
  
 <span data-ttu-id="cba9b-112">Dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)], les requêtes imbriquées doivent toujours être placées entre parenthèses :</span><span class="sxs-lookup"><span data-stu-id="cba9b-112">In [!INCLUDE[esql](../../../../../../includes/esql-md.md)], nested queries must always be enclosed in parentheses:</span></span>  
  
```  
-- Pseudo-Entity SQL  
( SELECT …  
FROM … )  
UNION ALL  
( SELECT …  
FROM … );  
```  
  
 <span data-ttu-id="cba9b-113">L'exemple suivant montre comment imbriquer correctement des expressions dans [!INCLUDE[esql](../../../../../../includes/esql-md.md)] : [Guide pratique pour Ordonner l’Union de deux requêtes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896299(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="cba9b-113">The following example demonstrates how to properly nest expressions in [!INCLUDE[esql](../../../../../../includes/esql-md.md)]: [How to: Order the Union of Two Queries](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896299(v=vs.100)).</span></span>  
  
## <a name="nested-queries-in-projection"></a><span data-ttu-id="cba9b-114">Requêtes imbriquées dans la projection</span><span class="sxs-lookup"><span data-stu-id="cba9b-114">Nested Queries in Projection</span></span>  
 <span data-ttu-id="cba9b-115">Les requêtes imbriquées d'une clause de projection peuvent être traduites en requêtes de produit cartésien sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="cba9b-115">Nested queries in the project clause might get translated into Cartesian product queries on the server.</span></span> <span data-ttu-id="cba9b-116">Sur certains serveurs principaux dont SQL Server, cela peut avoir pour conséquences l'augmentation de volume de la table TempDB et une diminution des performances du serveur.</span><span class="sxs-lookup"><span data-stu-id="cba9b-116">In some backend servers, including SLQ Server, this can cause the TempDB table to get very large, which can adversely affect server performance.</span></span>  
  
 <span data-ttu-id="cba9b-117">Vous trouverez ci-dessous un exemple de ce type de requête :</span><span class="sxs-lookup"><span data-stu-id="cba9b-117">The following is an example of such a query:</span></span>  
  
```  
SELECT c, (SELECT c, (SELECT c FROM AdventureWorksModel.Vendor AS c  ) As Inner2 FROM AdventureWorksModel.JobCandidate AS c  ) As Inner1 FROM AdventureWorksModel.EmployeeDepartmentHistory AS c  
```  
  
## <a name="ordering-nested-queries"></a><span data-ttu-id="cba9b-118">Ordre de tri des requêtes imbriquées</span><span class="sxs-lookup"><span data-stu-id="cba9b-118">Ordering Nested Queries</span></span>  
 <span data-ttu-id="cba9b-119">Dans Entity Framework, une expression imbriquée peut être placée n'importe où dans la requête.</span><span class="sxs-lookup"><span data-stu-id="cba9b-119">In the Entity Framework, a nested expression can be placed anywhere in the query.</span></span> <span data-ttu-id="cba9b-120">Entity SQL offrant une grande souplesse dans l'écriture des requêtes, il est possible d'écrire une requête qui contient un classement des requêtes imbriquées.</span><span class="sxs-lookup"><span data-stu-id="cba9b-120">Because Entity SQL allows great flexibility in writing queries, it is possible to write a query that contains an ordering of nested queries.</span></span> <span data-ttu-id="cba9b-121">Toutefois, l'ordre d'une requête imbriquée n'est pas conservé.</span><span class="sxs-lookup"><span data-stu-id="cba9b-121">However, the order of a nested query is not preserved.</span></span>  
  
```  
-- The following query will order the results by last name.  
SELECT C1.FirstName, C1.LastName  
        FROM AdventureWorksModel.Contact as C1  
        ORDER BY C1.LastName  
```  
  
```  
-- In the following query, ordering of the nested query is ignored.  
SELECT C2.FirstName, C2.LastName  
    FROM (SELECT C1.FirstName, C1.LastName  
        FROM AdventureWorksModel.Contact as C1  
        ORDER BY C1.LastName) as C2  
```  
  
## <a name="see-also"></a><span data-ttu-id="cba9b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cba9b-122">See also</span></span>

- [<span data-ttu-id="cba9b-123">Vue d’ensemble d’Entity SQL</span><span class="sxs-lookup"><span data-stu-id="cba9b-123">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
