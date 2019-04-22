---
title: Opérateur IsNot (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.isnot
helpviewer_keywords:
- IsNot operator [Visual Basic]
ms.assetid: 8dd2bcdb-0166-48a2-9094-60dfb448f36c
ms.openlocfilehash: e07a775eec003a3e488f6909181aed3f742b4b91
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58833514"
---
# <a name="isnot-operator-visual-basic"></a><span data-ttu-id="7f236-102">Opérateur IsNot (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7f236-102">IsNot Operator (Visual Basic)</span></span>
<span data-ttu-id="7f236-103">Compare deux variables de référence d’objet.</span><span class="sxs-lookup"><span data-stu-id="7f236-103">Compares two object reference variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f236-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f236-104">Syntax</span></span>  
  
```  
result = object1 IsNot object2  
```  
  
## <a name="parts"></a><span data-ttu-id="7f236-105">Composants</span><span class="sxs-lookup"><span data-stu-id="7f236-105">Parts</span></span>  
 `result`  
 <span data-ttu-id="7f236-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7f236-106">Required.</span></span> <span data-ttu-id="7f236-107">Valeur `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="7f236-107">A `Boolean` value.</span></span>  
  
 `object1`  
 <span data-ttu-id="7f236-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7f236-108">Required.</span></span> <span data-ttu-id="7f236-109">N’importe quel `Object` variable ou une expression.</span><span class="sxs-lookup"><span data-stu-id="7f236-109">Any `Object` variable or expression.</span></span>  
  
 `object2`  
 <span data-ttu-id="7f236-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7f236-110">Required.</span></span> <span data-ttu-id="7f236-111">N’importe quel `Object` variable ou une expression.</span><span class="sxs-lookup"><span data-stu-id="7f236-111">Any `Object` variable or expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7f236-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7f236-112">Remarks</span></span>  
 <span data-ttu-id="7f236-113">Le `IsNot` opérateur détermine si deux références d’objet font référence à des objets différents.</span><span class="sxs-lookup"><span data-stu-id="7f236-113">The `IsNot` operator determines if two object references refer to different objects.</span></span> <span data-ttu-id="7f236-114">Toutefois, il n’effectue pas de comparaisons de valeurs.</span><span class="sxs-lookup"><span data-stu-id="7f236-114">However, it does not perform value comparisons.</span></span> <span data-ttu-id="7f236-115">Si `object1` et `object2` se rapportent à la même instance d’objet, `result` est `False`; si elles ne le faites pas, `result` est `True`.</span><span class="sxs-lookup"><span data-stu-id="7f236-115">If `object1` and `object2` both refer to the exact same object instance, `result` is `False`; if they do not, `result` is `True`.</span></span>  
  
 <span data-ttu-id="7f236-116">`IsNot` est l’opposé de le `Is` opérateur.</span><span class="sxs-lookup"><span data-stu-id="7f236-116">`IsNot` is the opposite of the `Is` operator.</span></span> <span data-ttu-id="7f236-117">L’avantage de `IsNot` est que vous pouvez éviter la syntaxe difficile avec `Not` et `Is`, qui peut être difficile à lire.</span><span class="sxs-lookup"><span data-stu-id="7f236-117">The advantage of `IsNot` is that you can avoid awkward syntax with `Not` and `Is`, which can be difficult to read.</span></span>  
  
 <span data-ttu-id="7f236-118">Vous pouvez utiliser la `Is` et `IsNot` opérateurs pour tester des objets à liaison anticipée et liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="7f236-118">You can use the `Is` and `IsNot` operators to test both early-bound and late-bound objects.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7f236-119">Le `IsNot` opérateur ne peut pas être utilisé pour comparer des expressions retournées à partir de la `TypeOf` opérateur.</span><span class="sxs-lookup"><span data-stu-id="7f236-119">The `IsNot` operator cannot be used to compare expressions returned from the `TypeOf` operator.</span></span> <span data-ttu-id="7f236-120">Au lieu de cela, vous devez utiliser le `Not` et `Is` opérateurs.</span><span class="sxs-lookup"><span data-stu-id="7f236-120">Instead, you must use the `Not` and `Is` operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7f236-121">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f236-121">Example</span></span>  
 <span data-ttu-id="7f236-122">L’exemple de code suivant utilise à la fois le `Is` opérateur et la `IsNot` opérateur pour effectuer la même comparaison.</span><span class="sxs-lookup"><span data-stu-id="7f236-122">The following code example uses both the `Is` operator and the `IsNot` operator to accomplish the same comparison.</span></span>  
  
 [!code-vb[VbVbalrOperators#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#29)]  
  
## <a name="see-also"></a><span data-ttu-id="7f236-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f236-123">See also</span></span>

- [<span data-ttu-id="7f236-124">Is (opérateur)</span><span class="sxs-lookup"><span data-stu-id="7f236-124">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)
- [<span data-ttu-id="7f236-125">TypeOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="7f236-125">TypeOf Operator</span></span>](../../../visual-basic/language-reference/operators/typeof-operator.md)
- [<span data-ttu-id="7f236-126">Priorité des opérateurs en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7f236-126">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [<span data-ttu-id="7f236-127">Guide pratique pour Tester si deux objets sont identiques</span><span class="sxs-lookup"><span data-stu-id="7f236-127">How to: Test Whether Two Objects Are the Same</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-test-whether-two-objects-are-the-same.md)
