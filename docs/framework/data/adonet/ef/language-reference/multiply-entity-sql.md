---
title: '* (Multiplication) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 508ce246-4e86-47dd-a605-4af4bebb9891
ms.openlocfilehash: ecb0a55e403dddc5f7e69947035c8aa1fe7560ad
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32762544"
---
# <a name="-multiply-entity-sql"></a><span data-ttu-id="15f35-102">\* (Multiplier) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="15f35-102">\* (Multiply) (Entity SQL)</span></span>
<span data-ttu-id="15f35-103">Multiplie deux expressions.</span><span class="sxs-lookup"><span data-stu-id="15f35-103">Multiplies two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="15f35-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15f35-104">Syntax</span></span>  
  
```  
expression * expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="15f35-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="15f35-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="15f35-106">Toute expression valide de l'un des types de données numériques.</span><span class="sxs-lookup"><span data-stu-id="15f35-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="15f35-107">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="15f35-107">Result Types</span></span>  
 <span data-ttu-id="15f35-108">Type de données qui résulte de la promotion de type implicite de deux arguments.</span><span class="sxs-lookup"><span data-stu-id="15f35-108">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="15f35-109">Pour plus d’informations sur la promotion de type implicite, consultez [système de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="15f35-109">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="15f35-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="15f35-110">Example</span></span>  
 <span data-ttu-id="15f35-111">La requête Entity SQL ci-dessous utilise l'opérateur arithmétique \* pour multiplier deux nombres.</span><span class="sxs-lookup"><span data-stu-id="15f35-111">The following Entity SQL query uses the \* arithmetic operator to multiply two numbers.</span></span> <span data-ttu-id="15f35-112">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="15f35-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="15f35-113">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="15f35-113">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="15f35-114">Suivez la procédure indiquée dans [Guide pratique pour exécuter une requête qui retourne les résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="15f35-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="15f35-115">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="15f35-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#MULTIPLY](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#multiply)]  
  
## <a name="see-also"></a><span data-ttu-id="15f35-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15f35-116">See Also</span></span>  
 [<span data-ttu-id="15f35-117">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="15f35-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
