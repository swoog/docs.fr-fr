---
title: COLLECTION (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 03228bfa-be3a-4ccc-82f8-eee429f85cf1
ms.openlocfilehash: 8cd440571726796ee3d2c91e0d2f6b50571e8e27
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785325"
---
# <a name="collection-entity-sql"></a><span data-ttu-id="55e98-102">COLLECTION (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="55e98-102">COLLECTION (Entity SQL)</span></span>
<span data-ttu-id="55e98-103">Le mot clé COLLECTION est utilisé uniquement dans la définition d'une fonction incluse.</span><span class="sxs-lookup"><span data-stu-id="55e98-103">The COLLECTION keyword is only used in the definition of an inline function.</span></span> <span data-ttu-id="55e98-104">Les fonctions de collection sont des fonctions qui fonctionnent sur une collection de valeurs et produisent une sortie scalaire.</span><span class="sxs-lookup"><span data-stu-id="55e98-104">Collection functions are functions that operate on a collection of values and produce a scalar output.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55e98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55e98-105">Syntax</span></span>  
  
```  
COLLECTION(type_definition)   
```  
  
## <a name="arguments"></a><span data-ttu-id="55e98-106">Arguments</span><span class="sxs-lookup"><span data-stu-id="55e98-106">Arguments</span></span>  
 `type_definition`  
 <span data-ttu-id="55e98-107">Expression qui retourne une collection de types, lignes ou références pris en charge.</span><span class="sxs-lookup"><span data-stu-id="55e98-107">An expression that returns a collection of supported types, rows, or references.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55e98-108">Notes</span><span class="sxs-lookup"><span data-stu-id="55e98-108">Remarks</span></span>  
 <span data-ttu-id="55e98-109">Pour plus d’informations sur le mot clé COLLECTION, consultez [Type Definitions](../../../../../../docs/framework/data/adonet/ef/language-reference/type-definitions-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="55e98-109">For more information about the COLLECTION keyword, see [Type Definitions](../../../../../../docs/framework/data/adonet/ef/language-reference/type-definitions-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="55e98-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="55e98-110">Example</span></span>  
 <span data-ttu-id="55e98-111">L'exemple suivant montre comment utiliser le mot clé COLLECTION pour déclarer une collection de décimales en tant qu'argument pour une fonction de requête incluse.</span><span class="sxs-lookup"><span data-stu-id="55e98-111">The following sample shows how to use the COLLECTION keyword to declare a collection of decimals as an argument for an inline query function.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#Collection_GroupPartition](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#collection_grouppartition)]  
  
## <a name="see-also"></a><span data-ttu-id="55e98-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55e98-112">See also</span></span>

- [<span data-ttu-id="55e98-113">Référence Entity SQL</span><span class="sxs-lookup"><span data-stu-id="55e98-113">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
