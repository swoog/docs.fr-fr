---
title: Expressions dans les requêtes LINQ to Entities
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d70b502f-6a15-4120-b4fe-500b173ad9cc
ms.openlocfilehash: 6ec61a295f50fa64c484902ed811a627a22ee1c7
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55828044"
---
# <a name="expressions-in-linq-to-entities-queries"></a><span data-ttu-id="6d2c3-102">Expressions dans les requêtes LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="6d2c3-102">Expressions in LINQ to Entities Queries</span></span>
<span data-ttu-id="6d2c3-103">Une expression est un fragment de code qui peut correspondre à une valeur, un objet, une méthode ou un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-103">An expression is a fragment of code that can be evaluated to a single value, object, method, or namespace.</span></span> <span data-ttu-id="6d2c3-104">Elle peut contenir une valeur littérale, un appel de méthode, un opérateur et ses opérandes ou un nom simple.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-104">Expressions can contain a literal value, a method call, an operator and its operands, or a simple name.</span></span> <span data-ttu-id="6d2c3-105">Un nom simple peut être le nom d'une variable, d'un membre de type, d'un paramètre de méthode, d'un espace de noms ou d'un type.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-105">Simple names can be the name of a variable, type member, method parameter, namespace or type.</span></span> <span data-ttu-id="6d2c3-106">Les expressions peuvent utiliser des opérateurs qui à leur tour utilisent d'autres expressions comme des paramètres, ou des appels de méthode dont les paramètres sont à leur tour d'autres appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-106">Expressions can use operators that in turn use other expressions as parameters, or method calls whose parameters are in turn other method calls.</span></span> <span data-ttu-id="6d2c3-107">Par conséquent, les expressions peuvent être simples ou très complexes.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-107">Therefore, expressions can range from simple to very complex.</span></span>  
  
 <span data-ttu-id="6d2c3-108">Dans [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] requêtes, les expressions peuvent contenir tout élément autorisé par les types dans le <xref:System.Linq.Expressions> espace de noms, y compris les expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-108">In [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] queries, expressions can contain anything allowed by the types within the <xref:System.Linq.Expressions> namespace, including lambda expressions.</span></span> <span data-ttu-id="6d2c3-109">Les expressions utilisables dans les requêtes [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] sont un surensemble des expressions qui permettent d'interroger [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="6d2c3-109">The expressions that can be used in [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] queries are a superset of the expressions that can be used to query the [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)].</span></span>  <span data-ttu-id="6d2c3-110">Les expressions qui font partie des requêtes sur le [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] sont limitées aux opérations prises en charge par `ObjectQuery<T>` et la source de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="6d2c3-110">Expressions that are part of queries against the [!INCLUDE[adonet_ef](../../../../../../includes/adonet-ef-md.md)] are limited to operations supported by `ObjectQuery<T>` and the underlying data source.</span></span>  
  
 <span data-ttu-id="6d2c3-111">Dans l'exemple suivant, la comparaison dans la clause `Where` est une expression :</span><span class="sxs-lookup"><span data-stu-id="6d2c3-111">In the following example, the comparison in the `Where` clause is an expression:</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#whereexpression)]
 [!code-vb[DP L2E Conceptual Examples#WhereExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#whereexpression)]  
  
> [!NOTE]
>  <span data-ttu-id="6d2c3-112">Les constructions de langage spécifiques, telles que C# `unchecked`, n'ont aucune signification dans [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)].</span><span class="sxs-lookup"><span data-stu-id="6d2c3-112">Specific language constructs, such as C# `unchecked`, have no meaning in [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)].</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6d2c3-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="6d2c3-113">In This Section</span></span>  
 [<span data-ttu-id="6d2c3-114">Expressions de constantes</span><span class="sxs-lookup"><span data-stu-id="6d2c3-114">Constant Expressions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/constant-expressions.md)  
  
 [<span data-ttu-id="6d2c3-115">Expressions de comparaison</span><span class="sxs-lookup"><span data-stu-id="6d2c3-115">Comparison Expressions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/comparison-expressions.md)  
  
 [<span data-ttu-id="6d2c3-116">Comparaisons Null</span><span class="sxs-lookup"><span data-stu-id="6d2c3-116">Null Comparisons</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/null-comparisons.md)  
  
 [<span data-ttu-id="6d2c3-117">Expressions d’initialisation</span><span class="sxs-lookup"><span data-stu-id="6d2c3-117">Initialization Expressions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/initialization-expressions.md)  
  
 [<span data-ttu-id="6d2c3-118">Relations, les propriétés de navigation et les clés étrangères</span><span class="sxs-lookup"><span data-stu-id="6d2c3-118">Relationships, navigation properties and foreign keys</span></span>](/ef/ef6/fundamentals/relationships)  
  
## <a name="see-also"></a><span data-ttu-id="6d2c3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d2c3-119">See also</span></span>
- [<span data-ttu-id="6d2c3-120">ADO.NET Entity Framework</span><span class="sxs-lookup"><span data-stu-id="6d2c3-120">ADO.NET Entity Framework</span></span>](../../../../../../docs/framework/data/adonet/ef/index.md)
