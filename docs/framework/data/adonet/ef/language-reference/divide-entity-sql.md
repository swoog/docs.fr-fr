---
title: '- (Diviser) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: ef48c368-f3ed-4275-8ada-4e9649781262
ms.openlocfilehash: 38feaf4509ea2ed2838efe4daa257cdff144e863
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53147695"
---
# <a name="-divide-entity-sql"></a><span data-ttu-id="0b593-102">/ (Divide) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="0b593-102">/ (Divide) (Entity SQL)</span></span>
<span data-ttu-id="0b593-103">Divise un nombre par un autre.</span><span class="sxs-lookup"><span data-stu-id="0b593-103">Divides one number by another.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b593-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b593-104">Syntax</span></span>  
  
```  
dividend / divisor  
```  
  
## <a name="arguments"></a><span data-ttu-id="0b593-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="0b593-105">Arguments</span></span>  
 `dividend`  
 <span data-ttu-id="0b593-106">Expression numérique à diviser.</span><span class="sxs-lookup"><span data-stu-id="0b593-106">The numeric expression to divide.</span></span> <span data-ttu-id="0b593-107">`dividend` correspond à toute expression valide de l'un des types de données numériques.</span><span class="sxs-lookup"><span data-stu-id="0b593-107">`dividend` is any valid expression of any one of the numeric data types.</span></span>  
  
 `divisor`  
 <span data-ttu-id="0b593-108">Expression numérique par laquelle diviser le dividende.</span><span class="sxs-lookup"><span data-stu-id="0b593-108">The numeric expression to divide the dividend by.</span></span> <span data-ttu-id="0b593-109">`divisor` correspond à toute expression valide de l'un des types de données numériques.</span><span class="sxs-lookup"><span data-stu-id="0b593-109">`divisor` is any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="0b593-110">Types de résultats</span><span class="sxs-lookup"><span data-stu-id="0b593-110">Result Types</span></span>  
 <span data-ttu-id="0b593-111">Type de données qui résulte de la promotion de type implicite de deux arguments.</span><span class="sxs-lookup"><span data-stu-id="0b593-111">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="0b593-112">Pour plus d’informations sur la promotion de type implicite, consultez [système de Type](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="0b593-112">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="0b593-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="0b593-113">Example</span></span>  
 <span data-ttu-id="0b593-114">La requête Entity SQL ci-dessous utilise l’arithmétique / opérateur pour diviser un nombre par un autre.</span><span class="sxs-lookup"><span data-stu-id="0b593-114">The following Entity SQL query uses the / arithmetic operator to divide one number by another.</span></span> <span data-ttu-id="0b593-115">Cette requête est basée sur le modèle de vente AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="0b593-115">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="0b593-116">Pour compiler et exécuter cette requête, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b593-116">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="0b593-117">Suivez la procédure décrite dans [Comment : Exécuter une requête qui retourne des résultats StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="0b593-117">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="0b593-118">Transmettez à la méthode `ExecuteStructuralTypeQuery` la requête suivante en tant qu'argument :</span><span class="sxs-lookup"><span data-stu-id="0b593-118">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#DIVIDE](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#divide)]  
  
## <a name="see-also"></a><span data-ttu-id="0b593-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b593-119">See Also</span></span>  
 [<span data-ttu-id="0b593-120">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="0b593-120">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
