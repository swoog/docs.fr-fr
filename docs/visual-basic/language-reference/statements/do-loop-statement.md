---
title: Do...Loop, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Do
- vb.Loop
- vb.Until
helpviewer_keywords:
- conditional statements [Visual Basic], Do�Loop
- while statement [Visual Basic], Do...Loop
- execution [Visual Basic], conditional
- Do loops
- Until keyword [Visual Basic], Do...Loop statement
- Do...Loop statement
- instructions, repeating
- Do statement [Visual Basic]
- Exit statement [Visual Basic], in Do...Loop statements
- loop structures [Visual Basic], Do�Loop statements
- do-while statements [Visual Basic]
- loops, exiting
- Loop keyword [Visual Basic], Do...Loop statement
ms.assetid: 892f9096-b3e2-4aee-834d-83bc4e2c379d
ms.openlocfilehash: 3ff3d67f38f510b798da3e470de066cff1e98f29
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638773"
---
# <a name="doloop-statement-visual-basic"></a><span data-ttu-id="8f7ec-102">Do...Loop, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8f7ec-102">Do...Loop Statement (Visual Basic)</span></span>
<span data-ttu-id="8f7ec-103">Répète un bloc d’instructions tant qu’un `Boolean` condition est `True` ou jusqu'à ce que la condition devient `True`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-103">Repeats a block of statements while a `Boolean` condition is `True` or until the condition becomes `True`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f7ec-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f7ec-104">Syntax</span></span>  
  
```  
Do { While | Until } condition  
    [ statements ]  
    [ Continue Do ]  
    [ statements ]  
    [ Exit Do ]  
    [ statements ]  
Loop  
-or-  
Do  
    [ statements ]  
    [ Continue Do ]  
    [ statements ]  
    [ Exit Do ]  
    [ statements ]  
Loop { While | Until } condition  
```  
  
## <a name="parts"></a><span data-ttu-id="8f7ec-105">Composants</span><span class="sxs-lookup"><span data-stu-id="8f7ec-105">Parts</span></span>  
  
|<span data-ttu-id="8f7ec-106">Terme</span><span class="sxs-lookup"><span data-stu-id="8f7ec-106">Term</span></span>|<span data-ttu-id="8f7ec-107">Définition</span><span class="sxs-lookup"><span data-stu-id="8f7ec-107">Definition</span></span>|  
|---|---|  
|`Do`|<span data-ttu-id="8f7ec-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-108">Required.</span></span> <span data-ttu-id="8f7ec-109">Démarre la définition de la `Do` boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-109">Starts the definition of the `Do` loop.</span></span>|  
|`While`|<span data-ttu-id="8f7ec-110">Requis, sauf si l'option `Until` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-110">Required unless `Until` is used.</span></span> <span data-ttu-id="8f7ec-111">Répétez la boucle jusqu'à ce que `condition` est `False`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-111">Repeat the loop until `condition` is `False`.</span></span>|  
|`Until`|<span data-ttu-id="8f7ec-112">Requis, sauf si l'option `While` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-112">Required unless `While` is used.</span></span> <span data-ttu-id="8f7ec-113">Répétez la boucle jusqu'à ce que `condition` est `True`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-113">Repeat the loop until `condition` is `True`.</span></span>|  
|`condition`|<span data-ttu-id="8f7ec-114">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-114">Optional.</span></span> <span data-ttu-id="8f7ec-115">`Boolean` expression.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-115">`Boolean` expression.</span></span> <span data-ttu-id="8f7ec-116">Si `condition` est `Nothing`, Visual Basic traite en tant que `False`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-116">If `condition` is `Nothing`, Visual Basic treats it as `False`.</span></span>|  
|`statements`|<span data-ttu-id="8f7ec-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-117">Optional.</span></span> <span data-ttu-id="8f7ec-118">Une ou plusieurs instructions sont répétées lors ou jusqu'à ce que, `condition` est `True`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-118">One or more statements that are repeated while, or until, `condition` is `True`.</span></span>|  
|`Continue Do`|<span data-ttu-id="8f7ec-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-119">Optional.</span></span> <span data-ttu-id="8f7ec-120">Transfère le contrôle à l’itération suivante de la `Do` boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-120">Transfers control to the next iteration of the `Do` loop.</span></span>|  
|`Exit Do`|<span data-ttu-id="8f7ec-121">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-121">Optional.</span></span> <span data-ttu-id="8f7ec-122">Transfère le contrôle de la `Do` boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-122">Transfers control out of the `Do` loop.</span></span>|  
|`Loop`|<span data-ttu-id="8f7ec-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-123">Required.</span></span> <span data-ttu-id="8f7ec-124">Termine la définition de la `Do` boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-124">Terminates the definition of the `Do` loop.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8f7ec-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8f7ec-125">Remarks</span></span>  
 <span data-ttu-id="8f7ec-126">Utilisez un `Do...Loop` structure lorsque vous souhaitez répéter un ensemble d’instructions un nombre indéfini de fois, jusqu'à ce qu’une condition est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-126">Use a `Do...Loop` structure when you want to repeat a set of statements an indefinite number of times, until a condition is satisfied.</span></span> <span data-ttu-id="8f7ec-127">Si vous souhaitez répéter les instructions un nombre défini de fois, le [pour... L’instruction suivante](../../../visual-basic/language-reference/statements/for-next-statement.md) constitue généralement un meilleur choix.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-127">If you want to repeat the statements a set number of times, the [For...Next Statement](../../../visual-basic/language-reference/statements/for-next-statement.md) is usually a better choice.</span></span>  
  
 <span data-ttu-id="8f7ec-128">Vous pouvez utiliser `While` ou `Until` pour spécifier `condition`, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-128">You can use either `While` or `Until` to specify `condition`, but not both.</span></span>  
  
 <span data-ttu-id="8f7ec-129">Vous pouvez tester `condition` qu’une seule fois, au début ou la fin de la boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-129">You can test `condition` only one time, at either the start or the end of the loop.</span></span> <span data-ttu-id="8f7ec-130">Si vous testez `condition` au début de la boucle (dans le `Do` instruction), la boucle ne peut pas s’exécuter même une seule fois.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-130">If you test `condition` at the start of the loop (in the `Do` statement), the loop might not run even one time.</span></span> <span data-ttu-id="8f7ec-131">Si vous testez à la fin de la boucle (dans le `Loop` instruction), la boucle s’exécute toujours au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-131">If you test at the end of the loop (in the `Loop` statement), the loop always runs at least one time.</span></span>  
  
 <span data-ttu-id="8f7ec-132">La condition généralement le résultat d’une comparaison de deux valeurs, mais il peut être toute expression qui prend la valeur d’un [Type de données booléen](../../../visual-basic/language-reference/data-types/boolean-data-type.md) valeur (`True` ou `False`).</span><span class="sxs-lookup"><span data-stu-id="8f7ec-132">The condition usually results from a comparison of two values, but it can be any expression that evaluates to a [Boolean Data Type](../../../visual-basic/language-reference/data-types/boolean-data-type.md) value (`True` or `False`).</span></span> <span data-ttu-id="8f7ec-133">Cela inclut les valeurs d’autres types de données, telles que des types numériques, qui ont été convertis en `Boolean`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-133">This includes values of other data types, such as numeric types, that have been converted to `Boolean`.</span></span>  
  
 <span data-ttu-id="8f7ec-134">Vous pouvez imbriquer `Do` boucles en plaçant une boucle à l’intérieur d’une autre.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-134">You can nest `Do` loops by putting one loop within another.</span></span> <span data-ttu-id="8f7ec-135">Vous pouvez également imbriquer des différents types de structures de contrôle dans d’autres.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-135">You can also nest different kinds of control structures within each other.</span></span> <span data-ttu-id="8f7ec-136">Pour plus d’informations, consultez [Structures de contrôle imbriquées](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).</span><span class="sxs-lookup"><span data-stu-id="8f7ec-136">For more information, see [Nested Control Structures](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8f7ec-137">Le `Do...Loop` structure vous donne plus de souplesse que le [tandis que... Tandis que l’instruction End](../../../visual-basic/language-reference/statements/while-end-while-statement.md) , car elle vous permet de décider s’il faut mettre fin à la boucle lorsque `condition` cesse d’être `True` ou quand il devient `True`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-137">The `Do...Loop` structure gives you more flexibility than the [While...End While Statement](../../../visual-basic/language-reference/statements/while-end-while-statement.md) because it enables you to decide whether to end the loop when `condition` stops being `True` or when it first becomes `True`.</span></span> <span data-ttu-id="8f7ec-138">Il vous permet également de tester `condition` au début ou la fin de la boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-138">It also enables you to test `condition` at either the start or the end of the loop.</span></span>  
  
## <a name="exit-do"></a><span data-ttu-id="8f7ec-139">Exit Do</span><span class="sxs-lookup"><span data-stu-id="8f7ec-139">Exit Do</span></span>  
 <span data-ttu-id="8f7ec-140">Le [Exit Do](../../../visual-basic/language-reference/statements/exit-statement.md) instruction peut fournir une autre façon de quitter un `Do…Loop`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-140">The [Exit Do](../../../visual-basic/language-reference/statements/exit-statement.md) statement can provide an alternative way to exit a `Do…Loop`.</span></span> <span data-ttu-id="8f7ec-141">`Exit Do` transfère le contrôle immédiatement à l’instruction qui suit la `Loop` instruction.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-141">`Exit Do` transfers control immediately to the statement that follows the `Loop` statement.</span></span>  
  
 <span data-ttu-id="8f7ec-142">`Exit Do` est souvent utilisé après l’évaluation de certaines conditions, par exemple dans un `If...Then...Else` structure.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-142">`Exit Do` is often used after some condition is evaluated, for example in an `If...Then...Else` structure.</span></span> <span data-ttu-id="8f7ec-143">Vous souhaiterez peut-être quitter une boucle si vous détectez une condition qui rend inutile ou impossible pour poursuivre l’itération, comme une valeur erronée ou une demande d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-143">You might want to exit a loop if you detect a condition that makes it unnecessary or impossible to continue iterating, such as an erroneous value or a termination request.</span></span> <span data-ttu-id="8f7ec-144">Une des utilisations de `Exit Do` pour tester une condition qui peut entraîner un *boucle sans fin*, qui est une boucle qui pourrait s’exécuter de volumineux ou même infini de fois.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-144">One use of `Exit Do` is to test for a condition that could cause an *endless loop*, which is a loop that could run a large or even infinite number of times.</span></span> <span data-ttu-id="8f7ec-145">Vous pouvez utiliser `Exit Do` pour abandonner la boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-145">You can use `Exit Do` to escape the loop.</span></span>  
  
 <span data-ttu-id="8f7ec-146">Vous pouvez inclure un nombre quelconque de `Exit Do` instructions n’importe où dans un `Do…Loop`.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-146">You can include any number of `Exit Do` statements anywhere in a `Do…Loop`.</span></span>  
  
 <span data-ttu-id="8f7ec-147">Lorsqu’il est utilisé dans imbriqués `Do` boucles, `Exit Do` transfère le contrôle en dehors de la boucle la plus profonde et dans le niveau d’imbrication supérieur suivant.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-147">When used within nested `Do` loops, `Exit Do` transfers control out of the innermost loop and into the next higher level of nesting.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8f7ec-148">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f7ec-148">Example</span></span>  
 <span data-ttu-id="8f7ec-149">Dans l’exemple suivant, les instructions dans la boucle continuent à s’exécuter jusqu'à ce que le `index` variable est supérieure à 10.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-149">In the following example, the statements in the loop continue to run until the `index` variable is greater than 10.</span></span> <span data-ttu-id="8f7ec-150">Le `Until` clause est à la fin de la boucle.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-150">The `Until` clause is at the end of the loop.</span></span>  
  
 [!code-vb[VbVbalrStatements#131](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#131)]  
  
## <a name="example"></a><span data-ttu-id="8f7ec-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f7ec-151">Example</span></span>  
 <span data-ttu-id="8f7ec-152">L’exemple suivant utilise un `While` clause au lieu d’un `Until` clause, et `condition` est testée au début de la boucle et non à la fin.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-152">The following example uses a `While` clause instead of an `Until` clause, and `condition` is tested at the start of the loop instead of at the end.</span></span>  
  
 [!code-vb[VbVbalrStatements#132](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#132)]  
  
## <a name="example"></a><span data-ttu-id="8f7ec-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f7ec-153">Example</span></span>  
 <span data-ttu-id="8f7ec-154">Dans l’exemple suivant, `condition` arrête la boucle lorsque la `index` variable est supérieure à 100.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-154">In the following example, `condition` stops the loop when the `index` variable is greater than 100.</span></span> <span data-ttu-id="8f7ec-155">Le `If` instruction dans la boucle, cependant, entraîne la `Exit Do` instruction pour arrêter la boucle lorsque la variable d’index est supérieure à 10.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-155">The `If` statement in the loop, however, causes the `Exit Do` statement to stop the loop when the index variable is greater than 10.</span></span>  
  
 [!code-vb[VbVbalrStatements#133](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#133)]  
  
## <a name="example"></a><span data-ttu-id="8f7ec-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="8f7ec-156">Example</span></span>  
 <span data-ttu-id="8f7ec-157">L’exemple suivant lit toutes les lignes dans un fichier texte.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-157">The following example reads all lines in a text file.</span></span> <span data-ttu-id="8f7ec-158">Le <xref:System.IO.File.OpenText%2A> méthode ouvre le fichier et retourne un <xref:System.IO.StreamReader> qui lit les caractères.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-158">The <xref:System.IO.File.OpenText%2A> method opens the file and returns a <xref:System.IO.StreamReader> that reads the characters.</span></span> <span data-ttu-id="8f7ec-159">Dans le `Do...Loop` condition, le <xref:System.IO.StreamReader.Peek%2A> méthode de la `StreamReader` détermine s’il existe des caractères supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8f7ec-159">In the `Do...Loop` condition, the <xref:System.IO.StreamReader.Peek%2A> method of the `StreamReader` determines whether there are any additional characters.</span></span>  
  
 [!code-vb[VbVbalrStatements#134](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class10.vb#134)]  
  
## <a name="see-also"></a><span data-ttu-id="8f7ec-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f7ec-160">See also</span></span>

- [<span data-ttu-id="8f7ec-161">Structures de boucle</span><span class="sxs-lookup"><span data-stu-id="8f7ec-161">Loop Structures</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/loop-structures.md)
- [<span data-ttu-id="8f7ec-162">For...Next (instruction)</span><span class="sxs-lookup"><span data-stu-id="8f7ec-162">For...Next Statement</span></span>](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [<span data-ttu-id="8f7ec-163">Booléen (type de données)</span><span class="sxs-lookup"><span data-stu-id="8f7ec-163">Boolean Data Type</span></span>](../../../visual-basic/language-reference/data-types/boolean-data-type.md)
- [<span data-ttu-id="8f7ec-164">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="8f7ec-164">Nested Control Structures</span></span>](../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
- [<span data-ttu-id="8f7ec-165">Exit (instruction)</span><span class="sxs-lookup"><span data-stu-id="8f7ec-165">Exit Statement</span></span>](../../../visual-basic/language-reference/statements/exit-statement.md)
- [<span data-ttu-id="8f7ec-166">While...End While (instruction)</span><span class="sxs-lookup"><span data-stu-id="8f7ec-166">While...End While Statement</span></span>](../../../visual-basic/language-reference/statements/while-end-while-statement.md)
