---
title: Conversion simplifiée des délégués (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- relaxed delegate conversion [Visual Basic]
- delegates [Visual Basic], relaxed conversion
- conversions [Visual Basic], relaxed delegate
ms.assetid: 64f371d0-5416-4f65-b23b-adcbf556e81c
ms.openlocfilehash: 96941754f17326893437cdcf83c588880e010cc0
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56979504"
---
# <a name="relaxed-delegate-conversion-visual-basic"></a><span data-ttu-id="b03cb-102">Conversion simplifiée des délégués (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b03cb-102">Relaxed Delegate Conversion (Visual Basic)</span></span>
<span data-ttu-id="b03cb-103">Conversion simplifiée des délégués vous permet de vous permettent d’affecter des sous-routines et des fonctions aux délégués ou aux gestionnaires même lorsque leurs signatures ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="b03cb-103">Relaxed delegate conversion enables you to assign subs and functions to delegates or handlers even when their signatures are not identical.</span></span> <span data-ttu-id="b03cb-104">Par conséquent, la liaison aux délégués devient cohérente avec la liaison déjà autorisée pour les appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="b03cb-104">Therefore, binding to delegates becomes consistent with the binding already allowed for method invocations.</span></span>  
  
## <a name="parameters-and-return-type"></a><span data-ttu-id="b03cb-105">Paramètres et Type de retour</span><span class="sxs-lookup"><span data-stu-id="b03cb-105">Parameters and Return Type</span></span>  
 <span data-ttu-id="b03cb-106">À la place de correspondance exacte de signature, la conversion simplifiée requiert que les conditions suivantes est remplie lorsque `Option Strict` est défini sur `On`:</span><span class="sxs-lookup"><span data-stu-id="b03cb-106">In place of exact signature match, relaxed conversion requires that the following conditions be met when `Option Strict` is set to `On`:</span></span>  
  
-   <span data-ttu-id="b03cb-107">Une conversion étendue doit avoir le type de données de chaque paramètre de délégué au type de données du paramètre correspondant de la fonction attribué ou `Sub`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-107">A widening conversion must exist from the data type of each delegate parameter to the data type of the corresponding parameter of the assigned function or `Sub`.</span></span> <span data-ttu-id="b03cb-108">Dans l’exemple suivant, le délégué `Del1` a un paramètre, un `Integer`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-108">In the following example, the delegate `Del1` has one parameter, an `Integer`.</span></span> <span data-ttu-id="b03cb-109">Paramètre `m` dans l’expression lambda assigné expressions doivent avoir un type de données pour laquelle il existe une conversion étendue de `Integer`, tel que `Long` ou `Double`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-109">Parameter `m` in the assigned lambda expressions must have a data type for which there is a widening conversion from `Integer`, such as `Long` or `Double`.</span></span>  
  
     [!code-vb[VbVbalrRelaxedDelegates#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#1)]  
  
     [!code-vb[VbVbalrRelaxedDelegates#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#2)]  
  
     <span data-ttu-id="b03cb-110">Les conversions restrictives sont autorisées uniquement lorsque `Option Strict` est défini sur `Off`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-110">Narrowing conversions are permitted only when `Option Strict` is set to `Off`.</span></span>  
  
     [!code-vb[VbVbalrRelaxedDelegates#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module2.vb#8)]  
  
-   <span data-ttu-id="b03cb-111">Une conversion étendue doit exister dans la direction opposée du type de retour de la fonction assignée ou `Sub` pour le type de retour du délégué.</span><span class="sxs-lookup"><span data-stu-id="b03cb-111">A widening conversion must exist in the opposite direction from the return type of the assigned function or `Sub` to the return type of the delegate.</span></span> <span data-ttu-id="b03cb-112">Dans les exemples suivants, le corps de chaque expression lambda assignée doit correspondre à un type de données qui s’étend à `Integer` , car le type de retour de `del1` est `Integer`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-112">In the following examples, the body of each assigned lambda expression must evaluate to a data type that widens to `Integer` because the return type of `del1` is `Integer`.</span></span>  
  
     [!code-vb[VbVbalrRelaxedDelegates#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#3)]  
  
 <span data-ttu-id="b03cb-113">Si `Option Strict` est défini sur `Off`, la restriction étendue est supprimée dans les deux sens.</span><span class="sxs-lookup"><span data-stu-id="b03cb-113">If `Option Strict` is set to `Off`, the widening restriction is removed in both directions.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module2.vb#4)]  
  
## <a name="omitting-parameter-specifications"></a><span data-ttu-id="b03cb-114">L’omission des spécifications de paramètre</span><span class="sxs-lookup"><span data-stu-id="b03cb-114">Omitting Parameter Specifications</span></span>  
 <span data-ttu-id="b03cb-115">Délégués souples permettent d’omettre complètement les spécifications de paramètre dans la méthode assignée :</span><span class="sxs-lookup"><span data-stu-id="b03cb-115">Relaxed delegates also allow you to completely omit parameter specifications in the assigned method:</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#5)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#6)]  
  
 <span data-ttu-id="b03cb-116">Notez que vous ne pouvez pas spécifier certains paramètres et omettre d’autres.</span><span class="sxs-lookup"><span data-stu-id="b03cb-116">Note that you cannot specify some parameters and omit others.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#15)]  
  
 <span data-ttu-id="b03cb-117">La possibilité d’omettre des paramètres est utile dans une situation telles que la définition d’un gestionnaire d’événements, où plusieurs paramètres complexes sont impliqués.</span><span class="sxs-lookup"><span data-stu-id="b03cb-117">The ability to omit parameters is helpful in a situation such as defining an event handler, where several complex parameters are involved.</span></span> <span data-ttu-id="b03cb-118">Les arguments de certains gestionnaires d’événements ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="b03cb-118">The arguments to some event handlers are not used.</span></span> <span data-ttu-id="b03cb-119">Au lieu de cela, le gestionnaire accède directement à l’état du contrôle sur lequel l’événement est enregistré et ignore les arguments.</span><span class="sxs-lookup"><span data-stu-id="b03cb-119">Instead, the handler directly accesses the state of the control on which the event is registered, and ignores the arguments.</span></span> <span data-ttu-id="b03cb-120">Délégués souples permettent d’omettre les arguments dans les déclarations qui ne comprennent aucune ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="b03cb-120">Relaxed delegates allow you to omit the arguments in such declarations when no ambiguities result.</span></span> <span data-ttu-id="b03cb-121">Dans l’exemple suivant, la méthode entièrement spécifiée `OnClick` peut être réécrite en tant que `RelaxedOnClick`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-121">In the following example, the fully specified method `OnClick` can be rewritten as `RelaxedOnClick`.</span></span>  
  
```vb  
Sub OnClick(ByVal sender As Object, ByVal e As EventArgs) Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
  
Sub RelaxedOnClick() Handles b.Click  
    MessageBox.Show("Hello World from" + b.Text)  
End Sub  
```  
  
## <a name="addressof-examples"></a><span data-ttu-id="b03cb-122">Exemples d’AddressOf</span><span class="sxs-lookup"><span data-stu-id="b03cb-122">AddressOf Examples</span></span>  
 <span data-ttu-id="b03cb-123">Pour faciliter les relations de type voir, les expressions lambda sont utilisées dans les exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="b03cb-123">Lambda expressions are used in the previous examples to make the type relationships easy to see.</span></span> <span data-ttu-id="b03cb-124">Toutefois, les mêmes simplifications sont autorisées pour les assignations de délégués qui utilisent `AddressOf`, `Handles`, ou `AddHandler`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-124">However, the same relaxations are permitted for delegate assignments that use `AddressOf`, `Handles`, or `AddHandler`.</span></span>  
  
 <span data-ttu-id="b03cb-125">Dans l’exemple suivant, les fonctions `f1`, `f2`, `f3`, et `f4` peuvent être affectés à `Del1`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-125">In the following example, functions `f1`, `f2`, `f3`, and `f4` can all be assigned to `Del1`.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#1)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#7)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#9)]  
  
 <span data-ttu-id="b03cb-126">L’exemple suivant est valide uniquement lorsque `Option Strict` est défini sur `Off`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-126">The following example is valid only when `Option Strict` is set to `Off`.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module2.vb#14)]  
  
## <a name="dropping-function-returns"></a><span data-ttu-id="b03cb-127">Suppression des retours de fonction</span><span class="sxs-lookup"><span data-stu-id="b03cb-127">Dropping Function Returns</span></span>  
 <span data-ttu-id="b03cb-128">Conversion simplifiée des délégués vous permet d’assigner une fonction à un `Sub` délégué, en ignorant la valeur de retournée de la fonction.</span><span class="sxs-lookup"><span data-stu-id="b03cb-128">Relaxed delegate conversion enables you to assign a function to a `Sub` delegate, effectively ignoring the return value of the function.</span></span> <span data-ttu-id="b03cb-129">Toutefois, vous ne pouvez pas assigner un `Sub` à un délégué de fonction.</span><span class="sxs-lookup"><span data-stu-id="b03cb-129">However, you cannot assign a `Sub` to a function delegate.</span></span> <span data-ttu-id="b03cb-130">Dans l’exemple suivant, l’adresse de fonction `doubler` est affectée à `Sub` déléguer `Del3`.</span><span class="sxs-lookup"><span data-stu-id="b03cb-130">In the following example, the address of function `doubler` is assigned to `Sub` delegate `Del3`.</span></span>  
  
 [!code-vb[VbVbalrRelaxedDelegates#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#10)]  
  
 [!code-vb[VbVbalrRelaxedDelegates#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrRelaxedDelegates/VB/Module1.vb#11)]  
  
## <a name="see-also"></a><span data-ttu-id="b03cb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b03cb-131">See also</span></span>
- [<span data-ttu-id="b03cb-132">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="b03cb-132">Lambda Expressions</span></span>](../../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="b03cb-133">Conversions étendues et restrictives</span><span class="sxs-lookup"><span data-stu-id="b03cb-133">Widening and Narrowing Conversions</span></span>](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
- [<span data-ttu-id="b03cb-134">Délégués</span><span class="sxs-lookup"><span data-stu-id="b03cb-134">Delegates</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="b03cb-135">Guide pratique pour Passer des procédures à une autre procédure en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b03cb-135">How to: Pass Procedures to Another Procedure in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)
- [<span data-ttu-id="b03cb-136">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="b03cb-136">Local Type Inference</span></span>](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [<span data-ttu-id="b03cb-137">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="b03cb-137">Option Strict Statement</span></span>](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
