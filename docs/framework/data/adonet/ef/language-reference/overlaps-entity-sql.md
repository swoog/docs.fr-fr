---
title: OVERLAPS (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
ms.openlocfilehash: 9d909fb7efbb29619351cfc866b0f84381d0b80b
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59319636"
---
# <a name="overlaps-entity-sql"></a><span data-ttu-id="bed54-102">OVERLAPS (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="bed54-102">OVERLAPS (Entity SQL)</span></span>
<span data-ttu-id="bed54-103">Détermine si deux collections ont des éléments en commun.</span><span class="sxs-lookup"><span data-stu-id="bed54-103">Determines whether two collections have common elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bed54-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bed54-104">Syntax</span></span>  
  
```  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="bed54-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="bed54-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="bed54-106">Toute expression de requête valide qui retourne une collection à comparer avec la collection retournée par une autre expression de requête.</span><span class="sxs-lookup"><span data-stu-id="bed54-106">Any valid query expression that returns a collection to compare with the collection returned from another query expression.</span></span> <span data-ttu-id="bed54-107">Toutes les expressions doivent être du même type que le `expression`ou d'un type de base commun ou dérivé de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bed54-107">All expressions must be of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bed54-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bed54-108">Return Value</span></span>  
 `true` <span data-ttu-id="bed54-109">Si les deux collections ont des éléments en commun ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="bed54-109">if the two collections have common elements; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bed54-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bed54-110">Remarks</span></span>  
 <span data-ttu-id="bed54-111">OVERLAPS est fonctionnellement équivalent à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="bed54-111">OVERLAPS provides functionally equivalent to the following:</span></span>  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 <span data-ttu-id="bed54-112">OVERLAPS est l'un des opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="bed54-112">OVERLAPS is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="bed54-113">Tous les opérateurs de jeu [!INCLUDE[esql](../../../../../../includes/esql-md.md)] sont évalués de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="bed54-113">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="bed54-114">Pour plus d’informations de priorité pour le [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateurs de jeu, consultez [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="bed54-114">For precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators, see [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="bed54-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="bed54-115">Example</span></span>  
 <span data-ttu-id="bed54-116">La requête Entity SQL ci-dessous utilise l'opérateur OVERLAPS pour déterminer si deux collections ont une valeur commune.</span><span class="sxs-lookup"><span data-stu-id="bed54-116">The following Entity SQL query uses the OVERLAPS operator to determines whether two collections have a common value.</span></span> <span data-ttu-id="bed54-117">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="bed54-117">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="bed54-118">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="bed54-118">To compile and run this, follow these steps:</span></span>  
  
1. <span data-ttu-id="bed54-119">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="bed54-119">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="bed54-120">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="bed54-120">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#OVERLAPS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#overlaps)]  
  
## <a name="see-also"></a><span data-ttu-id="bed54-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bed54-121">See also</span></span>

- [<span data-ttu-id="bed54-122">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="bed54-122">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
