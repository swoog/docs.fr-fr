---
title: Widening (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.widening
helpviewer_keywords:
- conversions [Visual Basic], type
- type conversion [Visual Basic]
- conversions [Visual Basic], data type
- Widening keyword [Visual Basic]
- data type conversion [Visual Basic]
ms.assetid: 646ae263-94d3-40a2-b0cc-64f619292f56
ms.openlocfilehash: 2323aa38c81ce4e027f256d0e29c069f7ec77c00
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33595310"
---
# <a name="widening-visual-basic"></a><span data-ttu-id="7c050-102">Widening (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7c050-102">Widening (Visual Basic)</span></span>
<span data-ttu-id="7c050-103">Indique qu’un opérateur de conversion (`CType`) convertit une classe ou structure en un type qui peut contenir toutes les valeurs possibles de la classe ou la structure d’origine.</span><span class="sxs-lookup"><span data-stu-id="7c050-103">Indicates that a conversion operator (`CType`) converts a class or structure to a type that can hold all possible values of the original class or structure.</span></span>  
  
## <a name="converting-with-the-widening-keyword"></a><span data-ttu-id="7c050-104">Conversion avec le mot clé étendue</span><span class="sxs-lookup"><span data-stu-id="7c050-104">Converting with the Widening Keyword</span></span>  
 <span data-ttu-id="7c050-105">La procédure de conversion doit spécifier `Public Shared` à `Widening`.</span><span class="sxs-lookup"><span data-stu-id="7c050-105">The conversion procedure must specify `Public Shared` in addition to `Widening`.</span></span>  
  
 <span data-ttu-id="7c050-106">Les conversions étendues réussissent toujours en cours d’exécution et sans jamais aucune perte de données.</span><span class="sxs-lookup"><span data-stu-id="7c050-106">Widening conversions always succeed at run time and never incur data loss.</span></span> <span data-ttu-id="7c050-107">Exemples `Single` à `Double`, `Char` à `String`et un type dérivé vers son type de base.</span><span class="sxs-lookup"><span data-stu-id="7c050-107">Examples are `Single` to `Double`, `Char` to `String`, and a derived type to its base type.</span></span> <span data-ttu-id="7c050-108">Cette dernière conversion est étendue parce que le type dérivé contient tous les membres du type de base et est donc une instance du type de base.</span><span class="sxs-lookup"><span data-stu-id="7c050-108">This last conversion is widening because the derived type contains all the members of the base type and thus is an instance of the base type.</span></span>  
  
 <span data-ttu-id="7c050-109">Le code utilisateur ne doit pas utiliser `CType` pour les conversions étendues, même si `Option Strict` est `On`.</span><span class="sxs-lookup"><span data-stu-id="7c050-109">The consuming code does not have to use `CType` for widening conversions, even if `Option Strict` is `On`.</span></span>  
  
 <span data-ttu-id="7c050-110">Le `Widening` mot clé peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="7c050-110">The `Widening` keyword can be used in this context:</span></span>  
  
 [<span data-ttu-id="7c050-111">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="7c050-111">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
  
 <span data-ttu-id="7c050-112">Par exemple des définitions d’étendues et restrictives des opérateurs de conversion, consultez [Comment : définir un opérateur de Conversion](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).</span><span class="sxs-lookup"><span data-stu-id="7c050-112">For example definitions of widening and narrowing conversion operators, see [How to: Define a Conversion Operator](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7c050-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c050-113">See Also</span></span>  
 [<span data-ttu-id="7c050-114">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="7c050-114">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="7c050-115">Narrowing</span><span class="sxs-lookup"><span data-stu-id="7c050-115">Narrowing</span></span>](../../../visual-basic/language-reference/modifiers/narrowing.md)  
 [<span data-ttu-id="7c050-116">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="7c050-116">Widening and Narrowing Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)  
 [<span data-ttu-id="7c050-117">Guide pratique : définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="7c050-117">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)  
 [<span data-ttu-id="7c050-118">CType (fonction)</span><span class="sxs-lookup"><span data-stu-id="7c050-118">CType Function</span></span>](../../../visual-basic/language-reference/functions/ctype-function.md)  
 [<span data-ttu-id="7c050-119">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="7c050-119">Option Strict Statement</span></span>](../../../visual-basic/language-reference/statements/option-strict-statement.md)  
 [<span data-ttu-id="7c050-120">Guide pratique : définir un opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="7c050-120">How to: Define a Conversion Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
