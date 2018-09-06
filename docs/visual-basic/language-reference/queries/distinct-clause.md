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
ms.openlocfilehash: 18d09d8018303aab6a69801c84c7ec9c6ea19ca9
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43788621"
---
# <a name="distinct-clause-visual-basic"></a><span data-ttu-id="6929e-102">Distinct, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6929e-102">Distinct Clause (Visual Basic)</span></span>
<span data-ttu-id="6929e-103">Restreint les valeurs de la variable de portée actuelle pour éliminer les valeurs en double dans les clauses de requête suivantes.</span><span class="sxs-lookup"><span data-stu-id="6929e-103">Restricts the values of the current range variable to eliminate duplicate values in subsequent query clauses.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6929e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6929e-104">Syntax</span></span>  
  
```  
Distinct  
```  
  
## <a name="remarks"></a><span data-ttu-id="6929e-105">Notes</span><span class="sxs-lookup"><span data-stu-id="6929e-105">Remarks</span></span>  
 <span data-ttu-id="6929e-106">Vous pouvez utiliser le `Distinct` clause pour retourner une liste d’éléments uniques.</span><span class="sxs-lookup"><span data-stu-id="6929e-106">You can use the `Distinct` clause to return a list of unique items.</span></span> <span data-ttu-id="6929e-107">Le `Distinct` clause provoque la requête d’ignorer les résultats de requête en double.</span><span class="sxs-lookup"><span data-stu-id="6929e-107">The `Distinct` clause causes the query to ignore duplicate query results.</span></span> <span data-ttu-id="6929e-108">Le `Distinct` clause s’applique aux valeurs en double pour tous les champs spécifiés par de retour le `Select` clause.</span><span class="sxs-lookup"><span data-stu-id="6929e-108">The `Distinct` clause applies to duplicate values for all return fields specified by the `Select` clause.</span></span> <span data-ttu-id="6929e-109">Si aucun `Select` clause est spécifiée, le `Distinct` clause est appliquée à la variable de portée pour la requête identifiée dans le `From` clause.</span><span class="sxs-lookup"><span data-stu-id="6929e-109">If no `Select` clause is specified, the `Distinct` clause is applied to the range variable for the query identified in the `From` clause.</span></span> <span data-ttu-id="6929e-110">Si la variable de portée n’est pas un type immuable, la requête ignore uniquement un résultat de requête si tous les membres du type correspond à un résultat de requête existant.</span><span class="sxs-lookup"><span data-stu-id="6929e-110">If the range variable is not an immutable type, the query will only ignore a query result if all members of the type match an existing query result.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6929e-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="6929e-111">Example</span></span>  
 <span data-ttu-id="6929e-112">L’expression de requête suivante joint une liste de clients et une liste de commandes du client.</span><span class="sxs-lookup"><span data-stu-id="6929e-112">The following query expression joins a list of customers and a list of customer orders.</span></span> <span data-ttu-id="6929e-113">Le `Distinct` clause est incluse pour retourner une liste de noms de clients uniques et dates de commande.</span><span class="sxs-lookup"><span data-stu-id="6929e-113">The `Distinct` clause is included to return a list of unique customer names and order dates.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#20](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/distinct-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="6929e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6929e-114">See Also</span></span>  
 [<span data-ttu-id="6929e-115">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6929e-115">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="6929e-116">Requêtes</span><span class="sxs-lookup"><span data-stu-id="6929e-116">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="6929e-117">From (clause)</span><span class="sxs-lookup"><span data-stu-id="6929e-117">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
 [<span data-ttu-id="6929e-118">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="6929e-118">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="6929e-119">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="6929e-119">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
