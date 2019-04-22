---
title: Structures de boucle (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- control flow [Visual Basic], loops
- For keyword [Visual Basic], loop structures
- loops
- loop structures [Visual Basic]
- statements [Visual Basic], loop
- Do statement [Visual Basic], Do loops
- conditional statements [Visual Basic], loop structures
ms.assetid: ecacb09b-a4c9-42be-98b2-a15d368b5db8
ms.openlocfilehash: 56165eecce5e73c4e06235dac1691774fb39b794
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58833304"
---
# <a name="loop-structures-visual-basic"></a><span data-ttu-id="6aecd-102">Structures de boucle (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6aecd-102">Loop Structures (Visual Basic)</span></span>
<span data-ttu-id="6aecd-103">Structures de boucle de Visual Basic vous permettent de vous permettent d’exécuter une ou plusieurs lignes de code de façon répétée.</span><span class="sxs-lookup"><span data-stu-id="6aecd-103">Visual Basic loop structures allow you to run one or more lines of code repetitively.</span></span> <span data-ttu-id="6aecd-104">Vous pouvez répéter les instructions dans une structure de boucle jusqu'à ce qu’une condition est `True`, jusqu'à ce qu’une condition est `False`, un nombre de fois, ou qu’une seule fois pour chaque élément spécifié dans une collection.</span><span class="sxs-lookup"><span data-stu-id="6aecd-104">You can repeat the statements in a loop structure until a condition is `True`, until a condition is `False`, a specified number of times, or once for each element in a collection.</span></span>  
  
 <span data-ttu-id="6aecd-105">L’illustration suivante montre une structure de boucle qui exécute un ensemble d’instructions jusqu'à ce qu’une condition devienne true :</span><span class="sxs-lookup"><span data-stu-id="6aecd-105">The following illustration shows a loop structure that runs a set of statements until a condition becomes true:</span></span>  
  
 ![Organigramme illustrant un Do... Jusqu'à ce que la boucle.](./media/loop-structures/do-until-loop-true-condition.gif)  
  
## <a name="while-loops"></a><span data-ttu-id="6aecd-107">Boucles while</span><span class="sxs-lookup"><span data-stu-id="6aecd-107">While Loops</span></span>  
 <span data-ttu-id="6aecd-108">Le `While`... `End While` construction exécute un ensemble d’instructions tant que la condition spécifiée dans le `While` instruction est `True`.</span><span class="sxs-lookup"><span data-stu-id="6aecd-108">The `While`...`End While` construction runs a set of statements as long as the condition specified in the `While` statement is `True`.</span></span> <span data-ttu-id="6aecd-109">Pour plus d’informations, consultez [tandis que... Fin While, instruction](../../../../visual-basic/language-reference/statements/while-end-while-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6aecd-109">For more information, see [While...End While Statement](../../../../visual-basic/language-reference/statements/while-end-while-statement.md).</span></span>  
  
## <a name="do-loops"></a><span data-ttu-id="6aecd-110">Boucles Do</span><span class="sxs-lookup"><span data-stu-id="6aecd-110">Do Loops</span></span>  
 <span data-ttu-id="6aecd-111">Le `Do`... `Loop` construction vous permet de tester une condition au début ou à la fin d’une structure de boucle.</span><span class="sxs-lookup"><span data-stu-id="6aecd-111">The `Do`...`Loop` construction allows you to test a condition at either the beginning or the end of a loop structure.</span></span> <span data-ttu-id="6aecd-112">Vous pouvez également spécifier s’il faut répéter la boucle, tandis que la condition reste `True` ou jusqu'à ce qu’il devienne `True`.</span><span class="sxs-lookup"><span data-stu-id="6aecd-112">You can also specify whether to repeat the loop while the condition remains `True` or until it becomes `True`.</span></span> <span data-ttu-id="6aecd-113">Pour plus d’informations, consultez [faire... Instruction de boucle](../../../../visual-basic/language-reference/statements/do-loop-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6aecd-113">For more information, see [Do...Loop Statement](../../../../visual-basic/language-reference/statements/do-loop-statement.md).</span></span>  
  
## <a name="for-loops"></a><span data-ttu-id="6aecd-114">Boucles for</span><span class="sxs-lookup"><span data-stu-id="6aecd-114">For Loops</span></span>  
 <span data-ttu-id="6aecd-115">Le `For`... `Next` exécute la boucle un nombre défini de fois.</span><span class="sxs-lookup"><span data-stu-id="6aecd-115">The `For`...`Next` construction performs the loop a set number of times.</span></span> <span data-ttu-id="6aecd-116">Elle utilise une variable de contrôle de boucle, également appelée un *compteur*, pour assurer le suivi des répétitions.</span><span class="sxs-lookup"><span data-stu-id="6aecd-116">It uses a loop control variable, also called a *counter*, to keep track of the repetitions.</span></span> <span data-ttu-id="6aecd-117">Vous spécifiez le début et fin des valeurs pour ce compteur, et vous pouvez éventuellement spécifier la quantité d’incrémentation d’une répétition à la suivante.</span><span class="sxs-lookup"><span data-stu-id="6aecd-117">You specify the starting and ending values for this counter, and you can optionally specify the amount by which it increases from one repetition to the next.</span></span> <span data-ttu-id="6aecd-118">Pour plus d’informations, consultez [pour... L’instruction suivante](../../../../visual-basic/language-reference/statements/for-next-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6aecd-118">For more information, see [For...Next Statement](../../../../visual-basic/language-reference/statements/for-next-statement.md).</span></span>  
  
## <a name="for-each-loops"></a><span data-ttu-id="6aecd-119">Boucles For Each</span><span class="sxs-lookup"><span data-stu-id="6aecd-119">For Each Loops</span></span>  
 <span data-ttu-id="6aecd-120">Le `For Each`... `Next` construction exécute un ensemble d’instructions une fois pour chaque élément d’une collection.</span><span class="sxs-lookup"><span data-stu-id="6aecd-120">The `For Each`...`Next` construction runs a set of statements once for each element in a collection.</span></span> <span data-ttu-id="6aecd-121">Vous spécifiez la variable de contrôle de boucle, mais vous n’êtes pas obligé de déterminer le début ou de fin des valeurs pour qu’il.</span><span class="sxs-lookup"><span data-stu-id="6aecd-121">You specify the loop control variable, but you do not have to determine starting or ending values for it.</span></span> <span data-ttu-id="6aecd-122">Pour plus d’informations, consultez [For Each... L’instruction suivante](../../../../visual-basic/language-reference/statements/for-each-next-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6aecd-122">For more information, see [For Each...Next Statement](../../../../visual-basic/language-reference/statements/for-each-next-statement.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6aecd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aecd-123">See also</span></span>

- [<span data-ttu-id="6aecd-124">Flux de contrôle</span><span class="sxs-lookup"><span data-stu-id="6aecd-124">Control Flow</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/index.md)
- [<span data-ttu-id="6aecd-125">Structures de décision</span><span class="sxs-lookup"><span data-stu-id="6aecd-125">Decision Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/decision-structures.md)
- [<span data-ttu-id="6aecd-126">Autres structures de contrôle</span><span class="sxs-lookup"><span data-stu-id="6aecd-126">Other Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/other-control-structures.md)
- [<span data-ttu-id="6aecd-127">Structures de contrôle imbriquées</span><span class="sxs-lookup"><span data-stu-id="6aecd-127">Nested Control Structures</span></span>](../../../../visual-basic/programming-guide/language-features/control-flow/nested-control-structures.md)
