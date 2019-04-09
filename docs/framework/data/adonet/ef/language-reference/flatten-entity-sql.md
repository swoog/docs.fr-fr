---
title: FLATTEN (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 1a670c63-0a29-4738-80e6-101f66af05c3
ms.openlocfilehash: 76fba91f27479df19bbc4ac6e120d615a16f1d42
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59115113"
---
# <a name="flatten-entity-sql"></a><span data-ttu-id="86d9d-102">FLATTEN (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="86d9d-102">FLATTEN (Entity SQL)</span></span>
<span data-ttu-id="86d9d-103">Convertit une collection de collections en collection plane.</span><span class="sxs-lookup"><span data-stu-id="86d9d-103">Converts a collection of collections into a flattened collection.</span></span> <span data-ttu-id="86d9d-104">La nouvelle collection contient les mêmes éléments que l'ancienne, mais sans structure imbriquée.</span><span class="sxs-lookup"><span data-stu-id="86d9d-104">The new collection contains all the same elements as the old collection, but without a nested structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86d9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86d9d-105">Syntax</span></span>  
  
```  
FLATTEN ( collection )  
```  
  
## <a name="arguments"></a><span data-ttu-id="86d9d-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="86d9d-106">Arguments</span></span>  
 `collection`  
 <span data-ttu-id="86d9d-107">Expression valide qui retourne une collection de collections de valeurs à aplanir en une seule.</span><span class="sxs-lookup"><span data-stu-id="86d9d-107">Any valid expression that returns a collection of value collections to flatten into a single collection.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="86d9d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="86d9d-108">Remarks</span></span>  
 `FLATTEN` <span data-ttu-id="86d9d-109">Parmi les [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateurs de jeu.</span><span class="sxs-lookup"><span data-stu-id="86d9d-109">is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="86d9d-110">Tous les opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont évalués de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="86d9d-110">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="86d9d-111">Consultez [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md) pour des informations de priorité pour la [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateurs de jeu.</span><span class="sxs-lookup"><span data-stu-id="86d9d-111">See [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md) for precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="86d9d-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="86d9d-112">Example</span></span>  
 <span data-ttu-id="86d9d-113">La requête Entity SQL ci-dessous utilise l'opérateur `FLATTEN` pour convertir une collection de collections en collection plane.</span><span class="sxs-lookup"><span data-stu-id="86d9d-113">The following Entity SQL query uses the `FLATTEN` operator to convert a collection of collections into a flattened collection.</span></span> <span data-ttu-id="86d9d-114">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="86d9d-114">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="86d9d-115">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="86d9d-115">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="86d9d-116">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="86d9d-116">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#FLATTEN](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#flatten)]  
  
## <a name="see-also"></a><span data-ttu-id="86d9d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86d9d-117">See also</span></span>

- [<span data-ttu-id="86d9d-118">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="86d9d-118">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
