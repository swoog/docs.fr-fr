---
title: Expressions constantes
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 9d98a7be-b110-4edb-8eba-bed10f250b6d
ms.openlocfilehash: 10c74ede8d490bf96a9d0855889669bdc2628b01
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209201"
---
# <a name="constant-expressions"></a><span data-ttu-id="5fa9a-102">Expressions constantes</span><span class="sxs-lookup"><span data-stu-id="5fa9a-102">Constant Expressions</span></span>
<span data-ttu-id="5fa9a-103">Une expression constante est composée d'une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-103">A constant expression consists of a constant value.</span></span> <span data-ttu-id="5fa9a-104">Les valeurs constantes sont converties directement en expressions d’arborescence de commandes constantes, sans aucune traduction sur le client.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-104">Constant values are directly converted to constant command tree expressions, without any translation on the client.</span></span> <span data-ttu-id="5fa9a-105">Cela inclut les expressions qui génèrent une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-105">This includes expressions that result in a constant value.</span></span> <span data-ttu-id="5fa9a-106">Par conséquent, le comportement de la source de données doit être prévu pour toutes les expressions impliquant des constantes.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-106">Therefore, data source behavior should be expected for all expressions involving constants.</span></span> <span data-ttu-id="5fa9a-107">Il peut en résulter un comportement différent du comportement CLR.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-107">This can result in behavior that differs from CLR behavior.</span></span>  
  
 <span data-ttu-id="5fa9a-108">L'exemple suivant illustre une expression constante qui est évaluée sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-108">The following example shows a constant expression that is evaluated on the server.</span></span>  
  
 [!code-csharp[DP L2E Conceptual Examples#ConstantExpression](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Conceptual Examples/CS/Program.cs#constantexpression)]
 [!code-vb[DP L2E Conceptual Examples#ConstantExpression](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Conceptual Examples/VB/Module1.vb#constantexpression)]  
  
 [!INCLUDE[linq_entities](../../../../../../includes/linq-entities-md.md)] <span data-ttu-id="5fa9a-109">ne prend pas en charge l'utilisation d'une classe d'utilisateur comme constante.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-109">does not support using a user class as a constant.</span></span> <span data-ttu-id="5fa9a-110">Toutefois, une référence de propriété sur une classe d'utilisateur est considérée comme une constante. Elle est donc convertie en expression constante d'arborescence de commandes et exécutée sur la source de données.</span><span class="sxs-lookup"><span data-stu-id="5fa9a-110">However, a property reference on a user class is considered a constant, and will be converted to a command tree constant expression and executed on the data source.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fa9a-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fa9a-111">See also</span></span>

- [<span data-ttu-id="5fa9a-112">Expressions dans les requêtes LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="5fa9a-112">Expressions in LINQ to Entities Queries</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/expressions-in-linq-to-entities-queries.md)
