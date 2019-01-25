---
title: Conversion simplifiée des délégués (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- relaxed delegate conversion [Visual Basic]
- delegates [Visual Basic], relaxed conversion
- conversions [Visual Basic], relaxed delegate
ms.assetid: 64f371d0-5416-4f65-b23b-adcbf556e81c
ms.openlocfilehash: e2838b6473b8c00927073a530b4b49870fcfa9c6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600377"
---
# <a name="relaxed-delegate-conversion-visual-basic"></a><span data-ttu-id="8d298-102">Conversion simplifiée des délégués (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8d298-102">Relaxed Delegate Conversion (Visual Basic)</span></span>
<span data-ttu-id="8d298-103">Conversion simplifiée des délégués vous permet de vous permettent d’affecter des sous-routines et des fonctions aux délégués ou aux gestionnaires même lorsque leurs signatures ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="8d298-103">Relaxed delegate conversion enables you to assign subs and functions to delegates or handlers even when their signatures are not identical.</span></span> <span data-ttu-id="8d298-104">Par conséquent, la liaison aux délégués devient cohérente avec la liaison déjà autorisée pour les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="8d298-104">Therefore, binding to delegates becomes consistent with the binding already allowed for method invocations.</span></span>  
  
## <a name="parameters-and-return-type"></a><span data-ttu-id="8d298-105">Paramètres et Type de retour</span><span class="sxs-lookup"><span data-stu-id="8d298-105">Parameters and Return Type</span></span>  
 <span data-ttu-id="8d298-106">À la place de correspondance exacte de signature, la conversion simplifiée requiert que les conditions suivantes est remplie lorsque `Option Strict` est défini sur `On`:</span><span class="sxs-lookup"><span data-stu-id="8d298-106">In place of exact signature match, relaxed conversion requires that the following conditions be met when `Option Strict` is set to `On`:</span></span>  
  
-   <span data-ttu-id="8d298-107">Une conversion étendue doit avoir le type de données de chaque paramètre de délégué au type de données du paramètre correspondant de la fonction attribué ou `Sub`.</span><span class="sxs-lookup"><span data-stu-id="8d298-107">A widening conversion must exist from the data type of each delegate parameter to the data type of the corresponding parameter of the assigned function or `Sub`.</span></span> <span data-ttu-id="8d298-108">Dans l’exemple suivant, le délégué `Del1` a un paramètre, un `Integer`.</span><span class="sxs-lookup"><span data-stu-id="8d298-108">In the following example, the delegate `Del1` has one parameter, an `Integer`.</span></span> <span data-ttu-id="8d298-109">Paramètre `m` dans l’expression lambda assigné expressions doivent avoir un type de données pour laquelle il existe une conversion étendue de `Integer`, tel que `Long` ou `Double`.</span><span class="sxs-lookup"><span data-stu-id="8d298-109">Parameter `m` in the assigned lambda expressions must have a data type for which there is a widening conversion from `Integer`, such as `Long` or `Double`.</span></span>  
  
     [!code-vb[VbVbalrRelaxedDelegates#1](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_1.vb)]  
  
     [!code-vb[VbVbalrRelaxedDelegates#2](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_2.vb)]  
  
     <span data-ttu-id="8d298-110">Les conversions restrictives sont autorisées uniquement lorsque `Option Strict` est défini sur `Off`.</span><span class="sxs-lookup"><span data-stu-id="8d298-110">Narrowing conversions are permitted only when `Option Strict` is set to `Off`.</span></span>  
  
     [!code-vb[VbVbalrRelaxedDelegates#8](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_3.vb)]  
  
-   <span data-ttu-id="8d298-111">Une conversion étendue doit exister dans la direction opposée du type de retour de la fonction assignée ou `Sub` pour le type de retour du délégué.</span><span class="sxs-lookup"><span data-stu-id="8d298-111">A widening conversion must exist in the opposite direction from the return type of the assigned function or `Sub` to the return type of the delegate.</span></span> <span data-ttu-id="8d298-112">Dans les exemples suivants, le corps de chaque expression lambda assignée doit correspondre à un type de données qui s’étend à `Integer` , car le type de retour de `del1` est `Integer`.</span><span class="sxs-lookup"><span data-stu-id="8d298-112">In the following examples, the body of each assigned lambda expression must evaluate to a data type that widens to `Integer` because the return type of `del1` is `Integer`.</span></span>  
  
     [!code-vb[VbVbalrRelaxedDelegates#3](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_4.vb)]  
  
 <span data-ttu-id="8d298-113">Si `Option Strict` est défini sur `Off`, la restriction étendue est supprimée dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="8d298-113">If `Option Strict` is set to `Off`, the widening restriction is removed in both directions.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#4](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_5.vb)]  
  
## <a name="omitting-parameter-specifications"></a><span data-ttu-id="8d298-114">L’omission des spécifications de paramètre</span><span class="sxs-lookup"><span data-stu-id="8d298-114">Omitting Parameter Specifications</span></span>  
 <span data-ttu-id="8d298-115">Délégués souples permettent d’omettre complètement les spécifications de paramètre dans la méthode assignée :</span><span class="sxs-lookup"><span data-stu-id="8d298-115">Relaxed delegates also allow you to completely omit parameter specifications in the assigned method:</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#5](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_6.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#6](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_7.vb)]  
  
 <span data-ttu-id="8d298-116">Notez que vous ne pouvez pas spécifier certains paramètres et omettre d’autres.</span><span class="sxs-lookup"><span data-stu-id="8d298-116">Note that you cannot specify some parameters and omit others.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#15](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_8.vb)]  
  
 <span data-ttu-id="8d298-117">La possibilité d’omettre des paramètres est utile dans une situation telles que la définition d’un gestionnaire d’événements, où plusieurs paramètres complexes sont impliqués.</span><span class="sxs-lookup"><span data-stu-id="8d298-117">The ability to omit parameters is helpful in a situation such as defining an event handler, where several complex parameters are involved.</span></span> <span data-ttu-id="8d298-118">Les arguments de certains gestionnaires d’événements ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="8d298-118">The arguments to some event handlers are not used.</span></span> <span data-ttu-id="8d298-119">Au lieu de cela, le gestionnaire accède directement à l’état du contrôle sur lequel l’événement est enregistré et ignore les arguments.</span><span class="sxs-lookup"><span data-stu-id="8d298-119">Instead, the handler directly accesses the state of the control on which the event is registered, and ignores the arguments.</span></span> <span data-ttu-id="8d298-120">Délégués souples permettent d’omettre les arguments dans les déclarations qui ne comprennent aucune ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="8d298-120">Relaxed delegates allow you to omit the arguments in such declarations when no ambiguities result.</span></span> <span data-ttu-id="8d298-121">Dans l’exemple suivant, la méthode entièrement spécifiée `OnClick` peut être réécrite en tant que `RelaxedOnClick`.</span><span class="sxs-lookup"><span data-stu-id="8d298-121">In the following example, the fully specified method `OnClick` can be rewritten as `RelaxedOnClick`.</span></span>  
  
```vb  
Sub OnClick(ByVal sender As Object, ByVal e As EventArgs) Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
  
Sub RelaxedOnClick() Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
```  
  
## <a name="addressof-examples"></a><span data-ttu-id="8d298-122">Exemples d’AddressOf</span><span class="sxs-lookup"><span data-stu-id="8d298-122">AddressOf Examples</span></span>  
 <span data-ttu-id="8d298-123">Pour faciliter les relations de type voir, les expressions lambda sont utilisées dans les exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="8d298-123">Lambda expressions are used in the previous examples to make the type relationships easy to see.</span></span> <span data-ttu-id="8d298-124">Toutefois, les mêmes simplifications sont autorisées pour les assignations de délégués qui utilisent `AddressOf`, `Handles`, ou `AddHandler`.</span><span class="sxs-lookup"><span data-stu-id="8d298-124">However, the same relaxations are permitted for delegate assignments that use `AddressOf`, `Handles`, or `AddHandler`.</span></span>  
  
 <span data-ttu-id="8d298-125">Dans l’exemple suivant, les fonctions `f1`, `f2`, `f3`, et `f4` peuvent être affectés à `Del1`.</span><span class="sxs-lookup"><span data-stu-id="8d298-125">In the following example, functions `f1`, `f2`, `f3`, and `f4` can all be assigned to `Del1`.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#1](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_1.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#7](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_9.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#9](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_10.vb)]  
  
 <span data-ttu-id="8d298-126">L’exemple suivant est valide uniquement lorsque `Option Strict` est défini sur `Off`.</span><span class="sxs-lookup"><span data-stu-id="8d298-126">The following example is valid only when `Option Strict` is set to `Off`.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#14](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_11.vb)]  
  
## <a name="dropping-function-returns"></a><span data-ttu-id="8d298-127">Suppression des retours de fonction</span><span class="sxs-lookup"><span data-stu-id="8d298-127">Dropping Function Returns</span></span>  
 <span data-ttu-id="8d298-128">Conversion simplifiée des délégués vous permet d’assigner une fonction à un `Sub` délégué, en ignorant la valeur de retournée de la fonction.</span><span class="sxs-lookup"><span data-stu-id="8d298-128">Relaxed delegate conversion enables you to assign a function to a `Sub` delegate, effectively ignoring the return value of the function.</span></span> <span data-ttu-id="8d298-129">Toutefois, vous ne pouvez pas assigner un `Sub` à un délégué de fonction.</span><span class="sxs-lookup"><span data-stu-id="8d298-129">However, you cannot assign a `Sub` to a function delegate.</span></span> <span data-ttu-id="8d298-130">Dans l’exemple suivant, l’adresse de fonction `doubler` est affectée à `Sub` déléguer `Del3`.</span><span class="sxs-lookup"><span data-stu-id="8d298-130">In the following example, the address of function `doubler` is assigned to `Sub` delegate `Del3`.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#10](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_12.vb)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#11](../../../../visual-basic/programming-guide/language-features/delegates/codesnippet/VisualBasic/relaxed-delegate-conversion_13.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="8d298-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d298-131">See also</span></span>
- [<span data-ttu-id="8d298-132">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="8d298-132">Lambda Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="8d298-133">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="8d298-133">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="8d298-134">Délégués</span><span class="sxs-lookup"><span data-stu-id="8d298-134">Delegates</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="8d298-135">Guide pratique pour Passer des procédures à une autre procédure en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8d298-135">How to: Pass Procedures to Another Procedure in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)
- [<span data-ttu-id="8d298-136">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="8d298-136">Local Type Inference</span></span>](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="8d298-137">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="8d298-137">Option Strict Statement</span></span>](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
