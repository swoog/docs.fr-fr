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
ms.openlocfilehash: 54a18d0cc10e42829b48b0ef75bb77ab0d47b45f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33597456"
---
# <a name="narrowing-visual-basic"></a><span data-ttu-id="e023c-102">Narrowing (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e023c-102">Narrowing (Visual Basic)</span></span>
<span data-ttu-id="e023c-103">Indique qu’un opérateur de conversion (`CType`) convertit une classe ou structure en un type qui peut ne pas pouvoir contenir certaines des valeurs possibles de la classe ou la structure d’origine.</span><span class="sxs-lookup"><span data-stu-id="e023c-103">Indicates that a conversion operator (`CType`) converts a class or structure to a type that might not be able to hold some of the possible values of the original class or structure.</span></span>  
  
## <a name="converting-with-the-narrowing-keyword"></a><span data-ttu-id="e023c-104">Conversion avec le mot clé restrictive</span><span class="sxs-lookup"><span data-stu-id="e023c-104">Converting with the Narrowing Keyword</span></span>  
 <span data-ttu-id="e023c-105">La procédure de conversion doit spécifier `Public Shared` à `Narrowing`.</span><span class="sxs-lookup"><span data-stu-id="e023c-105">The conversion procedure must specify `Public Shared` in addition to `Narrowing`.</span></span>  
  
 <span data-ttu-id="e023c-106">Les conversions restrictives ne pas toujours réussisse au moment de l’exécution et peut échouer ou entraîner une perte de données.</span><span class="sxs-lookup"><span data-stu-id="e023c-106">Narrowing conversions do not always succeed at run time, and can fail or incur data loss.</span></span> <span data-ttu-id="e023c-107">Exemples `Long` à `Integer`, `String` à `Date`et un type de base en un type dérivé.</span><span class="sxs-lookup"><span data-stu-id="e023c-107">Examples are `Long` to `Integer`, `String` to `Date`, and a base type to a derived type.</span></span> <span data-ttu-id="e023c-108">Cette dernière conversion est restrictive parce que le type de base ne peut pas contenir tous les membres du type dérivé et n’est donc pas une instance du type dérivé.</span><span class="sxs-lookup"><span data-stu-id="e023c-108">This last conversion is narrowing because the base type might not contain all the members of the derived type and thus is not an instance of the derived type.</span></span>  
  
 <span data-ttu-id="e023c-109">Si `Option Strict` est `On`, le code utilisateur doit utiliser `CType` pour toutes les conversions restrictives.</span><span class="sxs-lookup"><span data-stu-id="e023c-109">If `Option Strict` is `On`, the consuming code must use `CType` for all narrowing conversions.</span></span>  
  
 <span data-ttu-id="e023c-110">Le `Narrowing` mot clé peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="e023c-110">The `Narrowing` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="e023c-111">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="e023c-111">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="e023c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e023c-112">See Also</span></span>  
 [<span data-ttu-id="e023c-113">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="e023c-113">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="e023c-114">Widening</span><span class="sxs-lookup"><span data-stu-id="e023c-114">Widening</span></span>](../../../visual-basic/language-reference/modifiers/widening.md)  
 [<span data-ttu-id="e023c-115">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="e023c-115">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)  
 [<span data-ttu-id="e023c-116">Guide pratique : définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="e023c-116">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)  
 [<span data-ttu-id="e023c-117">CType (fonction)</span><span class="sxs-lookup"><span data-stu-id="e023c-117">CType Function</span></span>](../../../visual-basic/language-reference/functions/ctype-function.md)  
 [<span data-ttu-id="e023c-118">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="e023c-118">Option Strict Statement</span></span>](../../../visual-basic/language-reference/statements/option-strict-statement.md)
