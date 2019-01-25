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
ms.openlocfilehash: bd88c05f16a2027b0367effebef809cb5e5abfe8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617433"
---
# <a name="narrowing-visual-basic"></a><span data-ttu-id="6c64d-102">Narrowing (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6c64d-102">Narrowing (Visual Basic)</span></span>
<span data-ttu-id="6c64d-103">Indique qu’un opérateur de conversion (`CType`) convertit une classe ou structure à un type qui peut ne pas pouvoir contenir certaines des valeurs possibles de la classe ou la structure d’origine.</span><span class="sxs-lookup"><span data-stu-id="6c64d-103">Indicates that a conversion operator (`CType`) converts a class or structure to a type that might not be able to hold some of the possible values of the original class or structure.</span></span>  
  
## <a name="converting-with-the-narrowing-keyword"></a><span data-ttu-id="6c64d-104">Conversion avec le mot clé restrictive</span><span class="sxs-lookup"><span data-stu-id="6c64d-104">Converting with the Narrowing Keyword</span></span>  
 <span data-ttu-id="6c64d-105">La procédure de conversion doit spécifier `Public Shared` outre `Narrowing`.</span><span class="sxs-lookup"><span data-stu-id="6c64d-105">The conversion procedure must specify `Public Shared` in addition to `Narrowing`.</span></span>  
  
 <span data-ttu-id="6c64d-106">Les conversions restrictives ne pas toujours réussisse au moment de l’exécution et peut échouer ou entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="6c64d-106">Narrowing conversions do not always succeed at run time, and can fail or incur data loss.</span></span> <span data-ttu-id="6c64d-107">Sont des exemples `Long` à `Integer`, `String` à `Date`et un type de base en un type dérivé.</span><span class="sxs-lookup"><span data-stu-id="6c64d-107">Examples are `Long` to `Integer`, `String` to `Date`, and a base type to a derived type.</span></span> <span data-ttu-id="6c64d-108">Cette dernière conversion est restrictive, car le type de base ne peut pas contenir tous les membres du type dérivé et n’est donc pas une instance du type dérivé.</span><span class="sxs-lookup"><span data-stu-id="6c64d-108">This last conversion is narrowing because the base type might not contain all the members of the derived type and thus is not an instance of the derived type.</span></span>  
  
 <span data-ttu-id="6c64d-109">Si `Option Strict` est `On`, le code utilisateur doit utiliser `CType` pour toutes les conversions restrictives.</span><span class="sxs-lookup"><span data-stu-id="6c64d-109">If `Option Strict` is `On`, the consuming code must use `CType` for all narrowing conversions.</span></span>  
  
 <span data-ttu-id="6c64d-110">Le `Narrowing` mot clé peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="6c64d-110">The `Narrowing` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="6c64d-111">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="6c64d-111">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="6c64d-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c64d-112">See also</span></span>
- [<span data-ttu-id="6c64d-113">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="6c64d-113">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="6c64d-114">Widening</span><span class="sxs-lookup"><span data-stu-id="6c64d-114">Widening</span></span>](../../../visual-basic/language-reference/modifiers/widening.md)
- [<span data-ttu-id="6c64d-115">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="6c64d-115">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="6c64d-116">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="6c64d-116">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="6c64d-117">CType (fonction)</span><span class="sxs-lookup"><span data-stu-id="6c64d-117">CType Function</span></span>](../../../visual-basic/language-reference/functions/ctype-function.md)
- [<span data-ttu-id="6c64d-118">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="6c64d-118">Option Strict Statement</span></span>](../../../visual-basic/language-reference/statements/option-strict-statement.md)
