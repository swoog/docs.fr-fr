---
title: 'Procédure : Appeler une procédure qui retourne une valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedure calls [Visual Basic], returning values
- Visual Basic code, procedures
- procedures [Visual Basic], calling
- procedures [Visual Basic], returning a value
ms.assetid: a445127b-0f5f-465a-98fb-3e514b93d115
ms.openlocfilehash: 8d9c7f3eadfa0095e0ed49b3a7a207fd3f7f8769
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525454"
---
# <a name="how-to-call-a-procedure-that-returns-a-value-visual-basic"></a><span data-ttu-id="3f13e-102">Procédure : Appeler une procédure qui retourne une valeur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3f13e-102">How to: Call a Procedure That Returns a Value (Visual Basic)</span></span>
<span data-ttu-id="3f13e-103">Un `Function` procédure retourne une valeur au code appelant.</span><span class="sxs-lookup"><span data-stu-id="3f13e-103">A `Function` procedure returns a value to the calling code.</span></span> <span data-ttu-id="3f13e-104">Vous appelez en incluant son nom et ses arguments soit situé à droite d’une instruction d’assignation ou dans une expression.</span><span class="sxs-lookup"><span data-stu-id="3f13e-104">You call it by including its name and arguments either on the right side of an assignment statement or in an expression.</span></span>  
  
### <a name="to-call-a-function-procedure-within-an-expression"></a><span data-ttu-id="3f13e-105">Pour appeler une procédure de fonction dans une expression</span><span class="sxs-lookup"><span data-stu-id="3f13e-105">To call a Function procedure within an expression</span></span>  
  
1.  <span data-ttu-id="3f13e-106">Utiliser le `Function` la même façon que vous utiliseriez une variable de nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="3f13e-106">Use the `Function` procedure name the same way you would use a variable.</span></span> <span data-ttu-id="3f13e-107">Vous pouvez utiliser un `Function` partout où vous pouvez utiliser une variable ou une constante dans une expression d’appel de procédure.</span><span class="sxs-lookup"><span data-stu-id="3f13e-107">You can use a `Function` procedure call anywhere you can use a variable or constant in an expression.</span></span>  
  
2.  <span data-ttu-id="3f13e-108">Faites suivre le nom de procédure avec des parenthèses pour encadrer la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3f13e-108">Follow the procedure name with parentheses to enclose the argument list.</span></span> <span data-ttu-id="3f13e-109">S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="3f13e-109">If there are no arguments, you can optionally omit the parentheses.</span></span> <span data-ttu-id="3f13e-110">Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="3f13e-110">However, using the parentheses makes your code easier to read.</span></span>  
  
3.  <span data-ttu-id="3f13e-111">Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3f13e-111">Place the arguments in the argument list within the parentheses, separated by commas.</span></span> <span data-ttu-id="3f13e-112">Veillez à vous fournir les arguments dans le même ordre que les `Function` procédure définit les paramètres correspondants.</span><span class="sxs-lookup"><span data-stu-id="3f13e-112">Be sure you supply the arguments in the same order that the `Function` procedure defines the corresponding parameters.</span></span>  
  
     <span data-ttu-id="3f13e-113">Vous pouvez également transmettre un ou plusieurs arguments par nom.</span><span class="sxs-lookup"><span data-stu-id="3f13e-113">Alternatively, you can pass one or more arguments by name.</span></span> <span data-ttu-id="3f13e-114">Pour plus d’informations, consultez [en passant les Arguments par Position et par nom](./passing-arguments-by-position-and-by-name.md).</span><span class="sxs-lookup"><span data-stu-id="3f13e-114">For more information, see [Passing Arguments by Position and by Name](./passing-arguments-by-position-and-by-name.md).</span></span>  
  
4.  <span data-ttu-id="3f13e-115">La valeur retournée par la procédure participe à l’expression comme la valeur d’une variable ou constante le ferait.</span><span class="sxs-lookup"><span data-stu-id="3f13e-115">The value returned from the procedure participates in the expression just as the value of a variable or constant would.</span></span>  
  
### <a name="to-call-a-function-procedure-in-an-assignment-statement"></a><span data-ttu-id="3f13e-116">Pour appeler une procédure de fonction dans une instruction d’assignation</span><span class="sxs-lookup"><span data-stu-id="3f13e-116">To call a Function procedure in an assignment statement</span></span>  
  
1.  <span data-ttu-id="3f13e-117">Utilisez le `Function` nom de procédure suivant égaux (`=`) connectez-vous à l’instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="3f13e-117">Use the `Function` procedure name following the equal (`=`) sign in the assignment statement.</span></span>  
  
2.  <span data-ttu-id="3f13e-118">Faites suivre le nom de procédure avec des parenthèses pour encadrer la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3f13e-118">Follow the procedure name with parentheses to enclose the argument list.</span></span> <span data-ttu-id="3f13e-119">S’il n’y a aucun argument, vous pouvez éventuellement omettre les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="3f13e-119">If there are no arguments, you can optionally omit the parentheses.</span></span> <span data-ttu-id="3f13e-120">Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="3f13e-120">However, using the parentheses makes your code easier to read.</span></span>  
  
3.  <span data-ttu-id="3f13e-121">Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="3f13e-121">Place the arguments in the argument list within the parentheses, separated by commas.</span></span> <span data-ttu-id="3f13e-122">Veillez à vous fournir les arguments dans le même ordre que les `Function` procédure définit les paramètres correspondants, sauf si vous les transmettez par nom.</span><span class="sxs-lookup"><span data-stu-id="3f13e-122">Be sure you supply the arguments in the same order that the `Function` procedure defines the corresponding parameters, unless you are passing them by name.</span></span>  
  
4.  <span data-ttu-id="3f13e-123">La valeur retournée par la procédure est stockée dans la variable ou la propriété sur le côté gauche de l’instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="3f13e-123">The value returned from the procedure is stored in the variable or property on the left side of the assignment statement.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f13e-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f13e-124">Example</span></span>  
 <span data-ttu-id="3f13e-125">L’exemple suivant appelle le Visual Basic <xref:Microsoft.VisualBasic.Interaction.Environ%2A> pour récupérer la valeur de variable d’environnement de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3f13e-125">The following example calls the Visual Basic <xref:Microsoft.VisualBasic.Interaction.Environ%2A> to retrieve the value of an operating system environment variable.</span></span> <span data-ttu-id="3f13e-126">La première ligne appelle `Environ` au sein d’une expression et la deuxième ligne l’appelle dans une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="3f13e-126">The first line calls `Environ` within an expression, and the second line calls it in an assignment statement.</span></span> <span data-ttu-id="3f13e-127">`Environ` prend le nom de variable comme unique argument.</span><span class="sxs-lookup"><span data-stu-id="3f13e-127">`Environ` takes the variable name as its sole argument.</span></span> <span data-ttu-id="3f13e-128">Elle retourne la valeur de la variable au code appelant.</span><span class="sxs-lookup"><span data-stu-id="3f13e-128">It returns the variable's value to the calling code.</span></span>  
  
 [!code-vb[VbVbcnProcedures#7](./codesnippet/VisualBasic/how-to-call-a-procedure-that-returns-a-value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="3f13e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f13e-129">See also</span></span>
- [<span data-ttu-id="3f13e-130">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="3f13e-130">Function Procedures</span></span>](./function-procedures.md)
- [<span data-ttu-id="3f13e-131">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="3f13e-131">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)
- [<span data-ttu-id="3f13e-132">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="3f13e-132">Function Statement</span></span>](../../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="3f13e-133">Guide pratique pour Créer une procédure qui retourne une valeur</span><span class="sxs-lookup"><span data-stu-id="3f13e-133">How to: Create a Procedure that Returns a Value</span></span>](./how-to-create-a-procedure-that-returns-a-value.md)
- [<span data-ttu-id="3f13e-134">Guide pratique pour Retourner une valeur à partir d’une procédure</span><span class="sxs-lookup"><span data-stu-id="3f13e-134">How to: Return a Value from a Procedure</span></span>](./how-to-return-a-value-from-a-procedure.md)
- [<span data-ttu-id="3f13e-135">Guide pratique pour Appeler une procédure qui ne retourne pas de valeur</span><span class="sxs-lookup"><span data-stu-id="3f13e-135">How to: Call a Procedure that Does Not Return a Value</span></span>](./how-to-call-a-procedure-that-does-not-return-a-value.md)
