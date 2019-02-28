---
title: Distinct, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryDistinct
helpviewer_keywords:
- Distinct clause [Visual Basic]
- Distinct statement [Visual Basic]
- queries [Visual Basic], Distinct
ms.assetid: 86f42614-0d8f-4ffc-b888-ce8a37a8d36a
ms.openlocfilehash: 00a2e52bd6669869bb2e25bc2857f1598da5763f
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56971245"
---
# <a name="distinct-clause-visual-basic"></a><span data-ttu-id="0ab14-102">Distinct, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0ab14-102">Distinct Clause (Visual Basic)</span></span>
<span data-ttu-id="0ab14-103">Restreint les valeurs de la variable de portée actuelle pour éliminer les valeurs en double dans les clauses de requête suivantes.</span><span class="sxs-lookup"><span data-stu-id="0ab14-103">Restricts the values of the current range variable to eliminate duplicate values in subsequent query clauses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ab14-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ab14-104">Syntax</span></span>  
  
```  
Distinct  
```  
  
## <a name="remarks"></a><span data-ttu-id="0ab14-105">Notes</span><span class="sxs-lookup"><span data-stu-id="0ab14-105">Remarks</span></span>  
 <span data-ttu-id="0ab14-106">Vous pouvez utiliser le `Distinct` clause pour retourner une liste d’éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="0ab14-106">You can use the `Distinct` clause to return a list of unique items.</span></span> <span data-ttu-id="0ab14-107">Le `Distinct` clause provoque la requête d’ignorer les résultats de requête en double.</span><span class="sxs-lookup"><span data-stu-id="0ab14-107">The `Distinct` clause causes the query to ignore duplicate query results.</span></span> <span data-ttu-id="0ab14-108">Le `Distinct` clause s’applique aux valeurs en double pour tous les champs spécifiés par de retour le `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="0ab14-108">The `Distinct` clause applies to duplicate values for all return fields specified by the `Select` clause.</span></span> <span data-ttu-id="0ab14-109">Si aucun `Select` clause est spécifiée, le `Distinct` clause est appliquée à la variable de portée pour la requête identifiée dans le `From` clause.</span><span class="sxs-lookup"><span data-stu-id="0ab14-109">If no `Select` clause is specified, the `Distinct` clause is applied to the range variable for the query identified in the `From` clause.</span></span> <span data-ttu-id="0ab14-110">Si la variable de portée n’est pas un type immuable, la requête ignore uniquement un résultat de requête si tous les membres du type correspond à un résultat de requête existant.</span><span class="sxs-lookup"><span data-stu-id="0ab14-110">If the range variable is not an immutable type, the query will only ignore a query result if all members of the type match an existing query result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ab14-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="0ab14-111">Example</span></span>  
 <span data-ttu-id="0ab14-112">L’expression de requête suivante joint une liste de clients et une liste de commandes du client.</span><span class="sxs-lookup"><span data-stu-id="0ab14-112">The following query expression joins a list of customers and a list of customer orders.</span></span> <span data-ttu-id="0ab14-113">Le `Distinct` clause est incluse pour retourner une liste de noms de clients uniques et dates de commande.</span><span class="sxs-lookup"><span data-stu-id="0ab14-113">The `Distinct` clause is included to return a list of unique customer names and order dates.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbSimpleQuerySamples/VB/QuerySamples1.vb#20)]  
  
## <a name="see-also"></a><span data-ttu-id="0ab14-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ab14-114">See also</span></span>
- [<span data-ttu-id="0ab14-115">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0ab14-115">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [<span data-ttu-id="0ab14-116">Requêtes</span><span class="sxs-lookup"><span data-stu-id="0ab14-116">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)
- [<span data-ttu-id="0ab14-117">From (clause)</span><span class="sxs-lookup"><span data-stu-id="0ab14-117">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)
- [<span data-ttu-id="0ab14-118">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="0ab14-118">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)
- [<span data-ttu-id="0ab14-119">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="0ab14-119">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
