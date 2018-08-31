---
title: Let, clause (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QueryLet
helpviewer_keywords:
- queries [Visual Basic], Let
- Let clause [Visual Basic]
- Let statement [Visual Basic]
ms.assetid: 981aa516-16eb-4c53-b1f1-5aa3e82f316e
ms.openlocfilehash: 34c0fd239d9e08dab4a107cb8447941e7ab3ecbe
ms.sourcegitcommit: fe02afbc39e78afd78cc6050e4a9c12a75f579f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/30/2018
ms.locfileid: "43255819"
---
# <a name="let-clause-visual-basic"></a><span data-ttu-id="f2624-102">Let, clause (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f2624-102">Let Clause (Visual Basic)</span></span>
<span data-ttu-id="f2624-103">Calcule une valeur et l’assigne à une nouvelle variable dans la requête.</span><span class="sxs-lookup"><span data-stu-id="f2624-103">Computes a value and assigns it to a new variable within the query.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2624-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2624-104">Syntax</span></span>  
  
```  
Let variable = expression [, ...]  
```  
  
## <a name="parts"></a><span data-ttu-id="f2624-105">Composants</span><span class="sxs-lookup"><span data-stu-id="f2624-105">Parts</span></span>  
  
|<span data-ttu-id="f2624-106">Terme</span><span class="sxs-lookup"><span data-stu-id="f2624-106">Term</span></span>|<span data-ttu-id="f2624-107">Définition</span><span class="sxs-lookup"><span data-stu-id="f2624-107">Definition</span></span>|  
|---|---|  
|`variable`|<span data-ttu-id="f2624-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f2624-108">Required.</span></span> <span data-ttu-id="f2624-109">Un alias qui peut être utilisé pour référencer les résultats de l’expression fournie.</span><span class="sxs-lookup"><span data-stu-id="f2624-109">An alias that can be used to reference the results of the supplied expression.</span></span>|  
|`expression`|<span data-ttu-id="f2624-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f2624-110">Required.</span></span> <span data-ttu-id="f2624-111">Une expression qui sera évaluée et assignée à la variable spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f2624-111">An expression that will be evaluated and assigned to the specified variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f2624-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f2624-112">Remarks</span></span>  
 <span data-ttu-id="f2624-113">Le `Let` clause vous permet de calculer des valeurs pour chaque résultat de la requête et les référencent en utilisant un alias.</span><span class="sxs-lookup"><span data-stu-id="f2624-113">The `Let` clause enables you to compute values for each query result and reference them by using an alias.</span></span> <span data-ttu-id="f2624-114">L’alias peut être utilisé dans d’autres clauses, telles que le `Where` clause.</span><span class="sxs-lookup"><span data-stu-id="f2624-114">The alias can be used in other clauses, such as the `Where` clause.</span></span> <span data-ttu-id="f2624-115">Le `Let` clause vous permet de créer une instruction de requête qui est plus facile à lire, car vous pouvez spécifier un alias pour une clause d’expression incluse dans la requête et substituer l’alias chaque fois que la clause d’expression est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f2624-115">The `Let` clause enables you to create a query statement that is easier to read because you can specify an alias for an expression clause included in the query and substitute the alias each time the expression clause is used.</span></span>  
  
 <span data-ttu-id="f2624-116">Vous pouvez inclure un nombre quelconque de `variable` et `expression` attributions dans le `Let` clause.</span><span class="sxs-lookup"><span data-stu-id="f2624-116">You can include any number of `variable` and `expression` assignments in the `Let` clause.</span></span> <span data-ttu-id="f2624-117">Séparez chaque affectation par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="f2624-117">Separate each assignment with a comma (,).</span></span>  
  
## <a name="example"></a><span data-ttu-id="f2624-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2624-118">Example</span></span>  
 <span data-ttu-id="f2624-119">Le code suivant exemple utilise le `Let` clause pour calculer une remise de 10 pour cent sur les produits.</span><span class="sxs-lookup"><span data-stu-id="f2624-119">The following code example uses the `Let` clause to compute a 10 percent discount on products.</span></span>  
  
 [!code-vb[VbSimpleQuerySamples#16](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/let-clause_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="f2624-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2624-120">See Also</span></span>  
 [<span data-ttu-id="f2624-121">Introduction à LINQ en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f2624-121">Introduction to LINQ in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [<span data-ttu-id="f2624-122">Requêtes</span><span class="sxs-lookup"><span data-stu-id="f2624-122">Queries</span></span>](../../../visual-basic/language-reference/queries/index.md)  
 [<span data-ttu-id="f2624-123">Select (clause)</span><span class="sxs-lookup"><span data-stu-id="f2624-123">Select Clause</span></span>](../../../visual-basic/language-reference/queries/select-clause.md)  
 [<span data-ttu-id="f2624-124">From (clause)</span><span class="sxs-lookup"><span data-stu-id="f2624-124">From Clause</span></span>](../../../visual-basic/language-reference/queries/from-clause.md)  
 [<span data-ttu-id="f2624-125">Where (clause)</span><span class="sxs-lookup"><span data-stu-id="f2624-125">Where Clause</span></span>](../../../visual-basic/language-reference/queries/where-clause.md)
