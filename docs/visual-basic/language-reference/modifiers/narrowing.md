---
title: Narrowing (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.narrowing
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Narrowing keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: a207ee91-aca4-4771-b4e2-713f029bf2bb
ms.openlocfilehash: eb5f021371291483b8eb2a13727a9fda94540638
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58838844"
---
# <a name="narrowing-visual-basic"></a><span data-ttu-id="eb27f-102">Narrowing (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="eb27f-102">Narrowing (Visual Basic)</span></span>
<span data-ttu-id="eb27f-103">Indique qu’un opérateur de conversion (`CType`) convertit une classe ou structure à un type qui peut ne pas pouvoir contenir certaines des valeurs possibles de la classe ou la structure d’origine.</span><span class="sxs-lookup"><span data-stu-id="eb27f-103">Indicates that a conversion operator (`CType`) converts a class or structure to a type that might not be able to hold some of the possible values of the original class or structure.</span></span>  
  
## <a name="converting-with-the-narrowing-keyword"></a><span data-ttu-id="eb27f-104">Conversion avec le mot clé restrictive</span><span class="sxs-lookup"><span data-stu-id="eb27f-104">Converting with the Narrowing Keyword</span></span>  
 <span data-ttu-id="eb27f-105">La procédure de conversion doit spécifier `Public Shared` outre `Narrowing`.</span><span class="sxs-lookup"><span data-stu-id="eb27f-105">The conversion procedure must specify `Public Shared` in addition to `Narrowing`.</span></span>  
  
 <span data-ttu-id="eb27f-106">Les conversions restrictives ne pas toujours réussisse au moment de l’exécution et peut échouer ou entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="eb27f-106">Narrowing conversions do not always succeed at run time, and can fail or incur data loss.</span></span> <span data-ttu-id="eb27f-107">Sont des exemples `Long` à `Integer`, `String` à `Date`et un type de base en un type dérivé.</span><span class="sxs-lookup"><span data-stu-id="eb27f-107">Examples are `Long` to `Integer`, `String` to `Date`, and a base type to a derived type.</span></span> <span data-ttu-id="eb27f-108">Cette dernière conversion est restrictive, car le type de base ne peut pas contenir tous les membres du type dérivé et n’est donc pas une instance du type dérivé.</span><span class="sxs-lookup"><span data-stu-id="eb27f-108">This last conversion is narrowing because the base type might not contain all the members of the derived type and thus is not an instance of the derived type.</span></span>  
  
 <span data-ttu-id="eb27f-109">Si `Option Strict` est `On`, le code utilisateur doit utiliser `CType` pour toutes les conversions restrictives.</span><span class="sxs-lookup"><span data-stu-id="eb27f-109">If `Option Strict` is `On`, the consuming code must use `CType` for all narrowing conversions.</span></span>  
  
 <span data-ttu-id="eb27f-110">Le `Narrowing` mot clé peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="eb27f-110">The `Narrowing` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="eb27f-111">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="eb27f-111">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="eb27f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb27f-112">See also</span></span>

- [<span data-ttu-id="eb27f-113">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="eb27f-113">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="eb27f-114">Widening</span><span class="sxs-lookup"><span data-stu-id="eb27f-114">Widening</span></span>](../../../visual-basic/language-reference/modifiers/widening.md)
- [<span data-ttu-id="eb27f-115">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="eb27f-115">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="eb27f-116">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="eb27f-116">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="eb27f-117">CType (fonction)</span><span class="sxs-lookup"><span data-stu-id="eb27f-117">CType Function</span></span>](../../../visual-basic/language-reference/functions/ctype-function.md)
- [<span data-ttu-id="eb27f-118">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="eb27f-118">Option Strict Statement</span></span>](../../../visual-basic/language-reference/statements/option-strict-statement.md)
