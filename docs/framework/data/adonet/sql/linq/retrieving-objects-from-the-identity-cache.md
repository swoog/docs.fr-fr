---
title: Récupération d'objets du cache d'identité
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 96c13903-ccb6-4a0e-ab6a-8ca955ca314d
ms.openlocfilehash: dceda9dce794e0a08cc9cd7905cf3cd0685898d4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569152"
---
# <a name="retrieving-objects-from-the-identity-cache"></a><span data-ttu-id="39095-102">Récupération d'objets du cache d'identité</span><span class="sxs-lookup"><span data-stu-id="39095-102">Retrieving Objects from the Identity Cache</span></span>
<span data-ttu-id="39095-103">Cette rubrique décrit les types des requêtes LINQ to SQL qui retournent un objet à partir du cache d'identité qui est géré par le <xref:System.Data.Linq.DataContext>.</span><span class="sxs-lookup"><span data-stu-id="39095-103">This topic describes the types of LINQ to SQL queries that return an object from the identity cache that is managed by the <xref:System.Data.Linq.DataContext>.</span></span>  
  
 <span data-ttu-id="39095-104">Dans LINQ to SQL, l'une des façons utilisées par le <xref:System.Data.Linq.DataContext> pour gérer les objets consiste à journaliser les identités d'objet dans un cache d'identité au fur et à mesure que les requêtes sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="39095-104">In LINQ to SQL, one of the ways in which the <xref:System.Data.Linq.DataContext> manages objects is by logging object identities in an identity cache as queries are executed.</span></span> <span data-ttu-id="39095-105">Dans certains cas, LINQ to SQL essaie de récupérer un objet à partir du cache d'identité avant l'exécution d'une requête dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="39095-105">In some cases, LINQ to SQL will attempt to retrieve an object from the identity cache before executing a query in the database.</span></span>  
  
 <span data-ttu-id="39095-106">Généralement, pour qu'une requête LINQ to SQL retourne un objet à partir du cache d'identité, la requête doit être basée sur la clé primaire d'un objet et doit retourner un objet unique.</span><span class="sxs-lookup"><span data-stu-id="39095-106">In general, for a LINQ to SQL query to return an object from the identity cache, the query must be based on the primary key of an object and must return a single object.</span></span> <span data-ttu-id="39095-107">En particulier, la requête doit se présenter sous l'une des formes générales suivantes.</span><span class="sxs-lookup"><span data-stu-id="39095-107">In particular, the query must be in one of the general forms shown below.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="39095-108">Les requêtes précompilées ne retournent pas d'objets à partir du cache d'identité.</span><span class="sxs-lookup"><span data-stu-id="39095-108">Pre-compiled queries will not return objects from the identity cache.</span></span> <span data-ttu-id="39095-109">Pour plus d’informations sur les requêtes précompilées, consultez <xref:System.Data.Linq.CompiledQuery> et [Comment : Store et réutiliser des requêtes](../../../../../../docs/framework/data/adonet/sql/linq/how-to-store-and-reuse-queries.md).</span><span class="sxs-lookup"><span data-stu-id="39095-109">For more information about pre-compiled queries, see <xref:System.Data.Linq.CompiledQuery> and [How to: Store and Reuse Queries](../../../../../../docs/framework/data/adonet/sql/linq/how-to-store-and-reuse-queries.md).</span></span>  
  
 <span data-ttu-id="39095-110">Une requête doit se présenter sous l'une des formes générales suivantes pour pouvoir récupérer un objet à partir du cache d'identité :</span><span class="sxs-lookup"><span data-stu-id="39095-110">A query must be in one of the following general forms to retrieve an object from the identity cache:</span></span>  
  
-   <span data-ttu-id="39095-111"><xref:System.Data.Linq.Table%601> `.Function1(` `predicate` `)`</span><span class="sxs-lookup"><span data-stu-id="39095-111"><xref:System.Data.Linq.Table%601> `.Function1(` `predicate` `)`</span></span>  
  
-   <span data-ttu-id="39095-112"><xref:System.Data.Linq.Table%601> `.Function1(` `predicate` `).Function2()`</span><span class="sxs-lookup"><span data-stu-id="39095-112"><xref:System.Data.Linq.Table%601> `.Function1(` `predicate` `).Function2()`</span></span>  
  
 <span data-ttu-id="39095-113">Dans ces formes générales, `Function1`, `Function2` et `predicate` sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="39095-113">In these general forms, `Function1`, `Function2`, and `predicate` are defined as follows.</span></span>  
  
 <span data-ttu-id="39095-114">`Function1` peut être l'une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="39095-114">`Function1` can be any of the following:</span></span>  
  
-   <xref:System.Linq.Queryable.Where%2A>  
  
-   <xref:System.Linq.Queryable.First%2A>  
  
-   <xref:System.Linq.Queryable.FirstOrDefault%2A>  
  
-   <xref:System.Linq.Queryable.Single%2A>  
  
-   <xref:System.Linq.Queryable.SingleOrDefault%2A>  
  
 <span data-ttu-id="39095-115">`Function2` peut être l'une des fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="39095-115">`Function2` can be any of the following:</span></span>  
  
-   <xref:System.Linq.Queryable.First%2A>  
  
-   <xref:System.Linq.Queryable.FirstOrDefault%2A>  
  
-   <xref:System.Linq.Queryable.Single%2A>  
  
-   <xref:System.Linq.Queryable.SingleOrDefault%2A>  
  
 <span data-ttu-id="39095-116">`predicate` doit être une expression dans laquelle la propriété de la clé primaire de l'objet est définie sur une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="39095-116">`predicate` must be an expression in which the object's primary key property is set to a constant value.</span></span> <span data-ttu-id="39095-117">Si la clé primaire d'un objet est définie par plusieurs propriétés, chaque propriété de clé primaire doit être définie sur une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="39095-117">If an object has a primary key defined by more than one property, each primary key property must be set to a constant value.</span></span> <span data-ttu-id="39095-118">Vous trouverez ci-dessous des exemples de formes requises pour `predicate` :</span><span class="sxs-lookup"><span data-stu-id="39095-118">The following are examples of the form `predicate` must take:</span></span>  
  
-   `c => c.PK == constant_value`  
  
-   `c => c.PK1 == constant_value1 && c=> c.PK2 == constant_value2`  
  
## <a name="example"></a><span data-ttu-id="39095-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="39095-119">Example</span></span>  
 <span data-ttu-id="39095-120">Le code suivant fournit des exemples de types de requêtes LINQ to SQL qui récupèrent un objet à partir du cache d'identité.</span><span class="sxs-lookup"><span data-stu-id="39095-120">The following code provides examples of the types of LINQ to SQL queries that retrieve an object from the identity cache.</span></span>  
  
 [!code-csharp[L2S_QueryCache#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/l2s_querycache/cs/program.cs#1)]
 [!code-vb[L2S_QueryCache#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/l2s_querycache/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="39095-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39095-121">See also</span></span>
- [<span data-ttu-id="39095-122">Concepts relatifs aux requêtes</span><span class="sxs-lookup"><span data-stu-id="39095-122">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
- [<span data-ttu-id="39095-123">Identité d’un objet</span><span class="sxs-lookup"><span data-stu-id="39095-123">Object Identity</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/object-identity.md)
- [<span data-ttu-id="39095-124">Informations générales</span><span class="sxs-lookup"><span data-stu-id="39095-124">Background Information</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/background-information.md)
- [<span data-ttu-id="39095-125">Identité d’un objet</span><span class="sxs-lookup"><span data-stu-id="39095-125">Object Identity</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/object-identity.md)
