---
title: = (égal à) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 948eb588-7080-4046-bb48-633b007393bf
ms.openlocfilehash: bda314208a25426be321ba307be96067b1df2ac8
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32761397"
---
# <a name="-equals-entity-sql"></a><span data-ttu-id="1cdd0-102">= (égal à) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="1cdd0-102">= (Equals) (Entity SQL)</span></span>
<span data-ttu-id="1cdd0-103">Compare l'égalité de deux expressions.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-103">Compares the equality of two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1cdd0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cdd0-104">Syntax</span></span>  
  
```  
expression = expression  
or   
expression == expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="1cdd0-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="1cdd0-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="1cdd0-106">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-106">Any valid expression.</span></span> <span data-ttu-id="1cdd0-107">Les deux expressions doivent posséder des types de données implicitement convertibles.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-107">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="1cdd0-108">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="1cdd0-108">Result Types</span></span>  
 <span data-ttu-id="1cdd0-109">`true` si l'expression de gauche est égale à l'expression de droite ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-109">`true` if the left expression is equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1cdd0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1cdd0-110">Remarks</span></span>  
 <span data-ttu-id="1cdd0-111">L'opérateur « = = » est équivalent à « = ».</span><span class="sxs-lookup"><span data-stu-id="1cdd0-111">The == operator is equivalent to =.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1cdd0-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="1cdd0-112">Example</span></span>  
 <span data-ttu-id="1cdd0-113">La requête Entity SQL ci-dessous utilise l'opérateur de comparaison « = » pour comparer l'égalité de deux expressions.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-113">The following Entity SQL query uses = comparison operator to compare the equality of two expressions.</span></span> <span data-ttu-id="1cdd0-114">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="1cdd0-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="1cdd0-115">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1cdd0-115">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="1cdd0-116">Suivez la procédure indiquée dans [Guide pratique pour exécuter une requête qui retourne les résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="1cdd0-116">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="1cdd0-117">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="1cdd0-117">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#EQUALS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#equals)]  
  
## <a name="see-also"></a><span data-ttu-id="1cdd0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cdd0-118">See Also</span></span>  
 [<span data-ttu-id="1cdd0-119">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="1cdd0-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
