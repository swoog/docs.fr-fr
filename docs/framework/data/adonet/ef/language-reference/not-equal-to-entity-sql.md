---
title: '!= (différent de) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 3b4a02ad-ddfc-4c42-8dfa-676234461312
ms.openlocfilehash: d5e59fe61dbc05a48e98f5720dca446482b9968e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568130"
---
# <a name="-not-equal-to-entity-sql"></a><span data-ttu-id="e622f-102">!= (différent de) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="e622f-102">!= (Not Equal To) (Entity SQL)</span></span>
<span data-ttu-id="e622f-103">Compare deux expressions pour déterminer si l'expression de gauche est différente de l'expression de droite.</span><span class="sxs-lookup"><span data-stu-id="e622f-103">Compares two expressions to determine whether the left expression is not equal to the right expression.</span></span> <span data-ttu-id="e622f-104">L'opérateur != (différent de) est d'un point de vue fonctionnel équivalent à l'opérateur <>.</span><span class="sxs-lookup"><span data-stu-id="e622f-104">The != (Not Equal To) operator is functionally equivalent to the <> operator.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e622f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e622f-105">Syntax</span></span>  
  
```  
expression != expression  
or  
expression <> expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="e622f-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="e622f-106">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="e622f-107">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="e622f-107">Any valid expression.</span></span> <span data-ttu-id="e622f-108">Les deux expressions doivent posséder des types de données implicitement convertibles.</span><span class="sxs-lookup"><span data-stu-id="e622f-108">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="e622f-109">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="e622f-109">Result Types</span></span>  
 <span data-ttu-id="e622f-110">`true` si l'expression de gauche est différente de l'expression de droite ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="e622f-110">`true` if the left expression is not equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e622f-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="e622f-111">Example</span></span>  
 <span data-ttu-id="e622f-112">La requête Entity SQL ci-dessous utilise l'opérateur != pour comparer deux expressions afin de déterminer si l'expression de gauche est différente de l'expression de droite.</span><span class="sxs-lookup"><span data-stu-id="e622f-112">The following Entity SQL query uses the != operator to compare two expressions to determine whether the left expression is not equal to the right expression.</span></span> <span data-ttu-id="e622f-113">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="e622f-113">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="e622f-114">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e622f-114">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="e622f-115">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="e622f-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="e622f-116">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="e622f-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#NOT_EQUALS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#not_equals)]  
  
## <a name="see-also"></a><span data-ttu-id="e622f-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e622f-117">See also</span></span>
- [<span data-ttu-id="e622f-118">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="e622f-118">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
