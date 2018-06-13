---
title: Caractères spéciaux dans le code (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.)
- vb.(
- vb.colon
- vb.!
- vb..
- 'vb.:'
helpviewer_keywords:
- special characters [Visual Basic], in code
- parentheses [Visual Basic], using in code
- colons (:)
- period character in code
- dot operator (.)
- dictionary access operator [Visual Basic]
- concatenation operators [Visual Basic], special characters in code
- concatenation operators [Visual Basic], vs. addition operator
- '! operator'
- separators [Visual Basic], using in code
- operators [Visual Basic], dictionary access
- ': separator character'
- member access operator [Visual Basic]
- addition operator [Visual Basic]
- operators [Visual Basic], member access
- . operator
- exclamation points
- separators
- exclamation point operator (!)
- Visual Basic code, special characters
ms.assetid: 310dce0c-45b5-4e0d-83e9-32df258d2a3e
ms.openlocfilehash: 932b38d97b36292e66bfad91a9a3799459d3b73c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33654354"
---
# <a name="special-characters-in-code-visual-basic"></a><span data-ttu-id="3c82e-102">Caractères spéciaux dans le code (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3c82e-102">Special Characters in Code (Visual Basic)</span></span>
<span data-ttu-id="3c82e-103">Vous devez parfois utiliser des caractères spéciaux dans votre code, autrement dit, les caractères qui ne sont pas alphabétiques ou numériques.</span><span class="sxs-lookup"><span data-stu-id="3c82e-103">Sometimes you have to use special characters in your code, that is, characters that are not alphabetical or numeric.</span></span> <span data-ttu-id="3c82e-104">La ponctuation et caractères spéciaux dans le jeu de caractères de Visual Basic ont plusieurs utilisations, de l’organisation du texte de programme à la définition des tâches effectuées par le compilateur ou le programme compilé.</span><span class="sxs-lookup"><span data-stu-id="3c82e-104">The punctuation and special characters in the Visual Basic character set have various uses, from organizing program text to defining the tasks that the compiler or the compiled program performs.</span></span> <span data-ttu-id="3c82e-105">Ils ne spécifient pas d'opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="3c82e-105">They do not specify an operation to be performed.</span></span>  
  
## <a name="parentheses"></a><span data-ttu-id="3c82e-106">Entre parenthèses</span><span class="sxs-lookup"><span data-stu-id="3c82e-106">Parentheses</span></span>  
 <span data-ttu-id="3c82e-107">Utilisez des parenthèses lorsque vous définissez une procédure, comme un `Sub` ou `Function`.</span><span class="sxs-lookup"><span data-stu-id="3c82e-107">Use parentheses when you define a procedure, such as a `Sub` or `Function`.</span></span> <span data-ttu-id="3c82e-108">Vous devez placer toutes les listes d’arguments de procédure entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="3c82e-108">You must enclose all procedure argument lists in parentheses.</span></span> <span data-ttu-id="3c82e-109">Vous également utilisez des parenthèses pour insérer des variables ou arguments en groupes logiques, en particulier pour substituer l’ordre par défaut de priorité des opérateurs dans une expression complexe.</span><span class="sxs-lookup"><span data-stu-id="3c82e-109">You also use parentheses for putting variables or arguments into logical groups, especially to override the default order of operator precedence in a complex expression.</span></span> <span data-ttu-id="3c82e-110">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="3c82e-110">The following example illustrates this.</span></span>  
  
 [!code-vb[VbVbcnConventions#11](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/special-characters-in-code_1.vb)]  
  
 <span data-ttu-id="3c82e-111">Après l’exécution du code précédent, la valeur de `d` est 8.225 et la valeur de `e` est 3.</span><span class="sxs-lookup"><span data-stu-id="3c82e-111">Following execution of the previous code, the value of `d` is 8.225 and the value of `e` is 3.</span></span> <span data-ttu-id="3c82e-112">Le calcul de `d` utilise la priorité par défaut de `/` sur `+` et équivaut à `d = b + (c / a)`.</span><span class="sxs-lookup"><span data-stu-id="3c82e-112">The calculation for `d` uses the default precedence of `/` over `+` and is equivalent to `d = b + (c / a)`.</span></span> <span data-ttu-id="3c82e-113">Les parenthèses dans le calcul de `e` la priorité par défaut.</span><span class="sxs-lookup"><span data-stu-id="3c82e-113">The parentheses in the calculation for `e` override the default precedence.</span></span>  
  
## <a name="separators"></a><span data-ttu-id="3c82e-114">Séparateurs</span><span class="sxs-lookup"><span data-stu-id="3c82e-114">Separators</span></span>  
 <span data-ttu-id="3c82e-115">Les séparateurs de faire ce que leur nom le suggère : séparent les différentes sections de code.</span><span class="sxs-lookup"><span data-stu-id="3c82e-115">Separators do what their name suggests: they separate sections of code.</span></span> <span data-ttu-id="3c82e-116">En Visual Basic, le caractère de séparation est le signe deux-points (`:`).</span><span class="sxs-lookup"><span data-stu-id="3c82e-116">In Visual Basic, the separator character is the colon (`:`).</span></span> <span data-ttu-id="3c82e-117">Utilisez des séparateurs lorsque vous voulez inclure plusieurs instructions sur une seule ligne à la place des lignes distinctes.</span><span class="sxs-lookup"><span data-stu-id="3c82e-117">Use separators when you want to include multiple statements on a single line instead of separate lines.</span></span> <span data-ttu-id="3c82e-118">Cela économise de l’espace et améliore la lisibilité de votre code.</span><span class="sxs-lookup"><span data-stu-id="3c82e-118">This saves space and improves the readability of your code.</span></span> <span data-ttu-id="3c82e-119">L’exemple suivant montre les trois instructions séparées par un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="3c82e-119">The following example shows three statements separated by colons.</span></span>  
  
 [!code-vb[VbVbcnConventions#12](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/special-characters-in-code_2.vb)]  
  
 <span data-ttu-id="3c82e-120">Pour plus d’informations, consultez [Comment : arrêt et combiner des instructions dans le Code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md).</span><span class="sxs-lookup"><span data-stu-id="3c82e-120">For more information, see [How to: Break and Combine Statements in Code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md).</span></span>  
  
 <span data-ttu-id="3c82e-121">Le signe deux-points (`:`) caractère est également utilisé pour identifier une étiquette d’instruction.</span><span class="sxs-lookup"><span data-stu-id="3c82e-121">The colon (`:`) character is also used to identify a statement label.</span></span> <span data-ttu-id="3c82e-122">Pour plus d’informations, consultez [Comment : instructions de l’étiquette](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md).</span><span class="sxs-lookup"><span data-stu-id="3c82e-122">For more information, see [How to: Label Statements](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md).</span></span>  
  
## <a name="concatenation"></a><span data-ttu-id="3c82e-123">Concaténation</span><span class="sxs-lookup"><span data-stu-id="3c82e-123">Concatenation</span></span>  
 <span data-ttu-id="3c82e-124">Utilisez le `&` opérateur pour *concaténation*, ou lier plusieurs chaînes.</span><span class="sxs-lookup"><span data-stu-id="3c82e-124">Use the `&` operator for *concatenation*, or linking strings together.</span></span> <span data-ttu-id="3c82e-125">Ne confondez pas avec le `+` opérateur, qui additionne les valeurs numériques.</span><span class="sxs-lookup"><span data-stu-id="3c82e-125">Do not confuse it with the `+` operator, which adds together numeric values.</span></span> <span data-ttu-id="3c82e-126">Si vous utilisez le `+` pour concaténer lorsque vous utilisez des valeurs numériques, vous pouvez obtenir des résultats incorrects.</span><span class="sxs-lookup"><span data-stu-id="3c82e-126">If you use the `+` operator to concatenate when you operate on numeric values, you can obtain incorrect results.</span></span> <span data-ttu-id="3c82e-127">Cela est illustré par l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="3c82e-127">The following example demonstrates this.</span></span>  
  
 [!code-vb[VbVbcnConventions#13](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/special-characters-in-code_3.vb)]  
  
 <span data-ttu-id="3c82e-128">Après l’exécution du code précédent, la valeur de `resultA` est 21.01 et la valeur de `resultB` est « 10.0111 ».</span><span class="sxs-lookup"><span data-stu-id="3c82e-128">Following execution of the previous code, the value of `resultA` is 21.01 and the value of `resultB` is "10.0111".</span></span>  
  
## <a name="member-access-operators"></a><span data-ttu-id="3c82e-129">Opérateurs d’accès au membre</span><span class="sxs-lookup"><span data-stu-id="3c82e-129">Member Access Operators</span></span>  
 <span data-ttu-id="3c82e-130">Pour accéder à un membre d’un type, utilisez le point (`.`) ou un point d’exclamation (`!`) opérateur entre le nom de type et le nom du membre.</span><span class="sxs-lookup"><span data-stu-id="3c82e-130">To access a member of a type, you use the dot (`.`) or exclamation point (`!`) operator between the type name and the member name.</span></span>  
  
### <a name="dot--operator"></a><span data-ttu-id="3c82e-131">Point (.) Opérateur</span><span class="sxs-lookup"><span data-stu-id="3c82e-131">Dot (.) Operator</span></span>  
 <span data-ttu-id="3c82e-132">Utilisez le `.` opérateur sur une classe, structure, interface, énumération ou comme un opérateur d’accès au membre.</span><span class="sxs-lookup"><span data-stu-id="3c82e-132">Use the `.` operator on a class, structure, interface, or enumeration as a member access operator.</span></span> <span data-ttu-id="3c82e-133">Le membre peut être un champ, une propriété, un événement ou une méthode.</span><span class="sxs-lookup"><span data-stu-id="3c82e-133">The member can be a field, property, event, or method.</span></span> <span data-ttu-id="3c82e-134">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="3c82e-134">The following example illustrates this.</span></span>  
  
 [!code-vb[VbVbcnConventions#14](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/special-characters-in-code_4.vb)]  
  
### <a name="exclamation-point--operator"></a><span data-ttu-id="3c82e-135">Point d’exclamation ( !) Opérateur</span><span class="sxs-lookup"><span data-stu-id="3c82e-135">Exclamation Point (!) Operator</span></span>  
 <span data-ttu-id="3c82e-136">Utilisez le `!` opérateur uniquement sur une classe ou une interface en tant qu’un opérateur d’accès au dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="3c82e-136">Use the `!` operator only on a class or interface as a dictionary access operator.</span></span> <span data-ttu-id="3c82e-137">La classe ou interface doit avoir une propriété par défaut qui accepte un seul `String` argument.</span><span class="sxs-lookup"><span data-stu-id="3c82e-137">The class or interface must have a default property that accepts a single `String` argument.</span></span> <span data-ttu-id="3c82e-138">L’identificateur qui suit immédiatement la `!` opérateur devient la valeur de l’argument passée à la propriété par défaut sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c82e-138">The identifier immediately following the `!` operator becomes the argument value passed to the default property as a string.</span></span> <span data-ttu-id="3c82e-139">Cela est illustré par l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="3c82e-139">The following example demonstrates this.</span></span>  
  
 [!code-vb[VbVbcnConventions#15](../../../visual-basic/programming-guide/language-features/codesnippet/VisualBasic/special-characters-in-code_5.vb)]  
  
 <span data-ttu-id="3c82e-140">Les trois lignes de sortie de `MsgBox` tous les affichent la valeur `32856`.</span><span class="sxs-lookup"><span data-stu-id="3c82e-140">The three output lines of `MsgBox` all display the value `32856`.</span></span> <span data-ttu-id="3c82e-141">La première ligne utilise l’accès traditionnel à la propriété `index`, la seconde utilise le fait que `index` est la propriété par défaut de la classe `hasDefault`, et la troisième utilise l’accès au dictionnaire pour la classe.</span><span class="sxs-lookup"><span data-stu-id="3c82e-141">The first line uses the traditional access to property `index`, the second makes use of the fact that `index` is the default property of class `hasDefault`, and the third uses dictionary access to the class.</span></span>  
  
 <span data-ttu-id="3c82e-142">Notez que le second opérande de le `!` opérateur doit être un identificateur Visual Basic valid ne pas entourée de guillemets doubles (`" "`).</span><span class="sxs-lookup"><span data-stu-id="3c82e-142">Note that the second operand of the `!` operator must be a valid Visual Basic identifier not enclosed in double quotation marks (`" "`).</span></span> <span data-ttu-id="3c82e-143">En d’autres termes, vous ne pouvez pas utiliser un littéral de chaîne ou une variable de chaîne.</span><span class="sxs-lookup"><span data-stu-id="3c82e-143">In other words, you cannot use a string literal or string variable.</span></span> <span data-ttu-id="3c82e-144">La modification ci-dessous à la dernière ligne de la `MsgBox` appel génère une erreur car `"X"` est une chaîne encadrée de littéral.</span><span class="sxs-lookup"><span data-stu-id="3c82e-144">The following change to the last line of the `MsgBox` call generates an error because `"X"` is an enclosed string literal.</span></span>  
  
 `"Dictionary access returns " & hD!"X")`  
  
> [!NOTE]
>  <span data-ttu-id="3c82e-145">Références à des regroupements par défaut doivent être explicites.</span><span class="sxs-lookup"><span data-stu-id="3c82e-145">References to default collections must be explicit.</span></span> <span data-ttu-id="3c82e-146">En particulier, vous ne pouvez pas utiliser le `!` opérateur sur une variable à liaison tardive.</span><span class="sxs-lookup"><span data-stu-id="3c82e-146">In particular, you cannot use the `!` operator on a late-bound variable.</span></span>  
  
 <span data-ttu-id="3c82e-147">Le `!` caractère est également utilisé comme le `Single` caractère de type.</span><span class="sxs-lookup"><span data-stu-id="3c82e-147">The `!` character is also used as the `Single` type character.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c82e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c82e-148">See Also</span></span>  
 [<span data-ttu-id="3c82e-149">Structure de programme et conventions de codage</span><span class="sxs-lookup"><span data-stu-id="3c82e-149">Program Structure and Code Conventions</span></span>](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)  
 [<span data-ttu-id="3c82e-150">Caractères de type</span><span class="sxs-lookup"><span data-stu-id="3c82e-150">Type Characters</span></span>](../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
