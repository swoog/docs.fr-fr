---
title: Function, instruction (Visual Basic)
ms.date: 05/12/2018
f1_keywords:
- vb.Function
helpviewer_keywords:
- procedures [Visual Basic], creating
- Function procedures [Visual Basic], Function statement syntax
- functions [Visual Basic], function procedures
- ParamArray keyword [Visual Basic], Function statements
- Private keyword [Visual Basic], Function statements
- declarations [Visual Basic], procedures
- procedures [Visual Basic], declaration
- Public keyword [Visual Basic], in Function statement
- ByVal keyword [Visual Basic], Function statements
- procedures [Visual Basic], recursive
- Implements keyword [Visual Basic], Function statements
- procedures [Visual Basic], returning values
- Exit statement [Visual Basic], in Function procedures
- recursive procedures
- As keyword [Visual Basic], in Function statement
- Optional keyword [Visual Basic], Function statements
- Function statement [Visual Basic]
- Visual Basic code, Function procedures
- procedures [Visual Basic], function
- ByRef keyword [Visual Basic], Function statements
- Friend keyword [Visual Basic], Function statements
- End keyword [Visual Basic], Function statements
- Handles keyword [Visual Basic], Function statements
ms.assetid: a4497077-0f46-4ede-a27f-9e8670df52b9
ms.openlocfilehash: dffe67d1c31b0fe7c037839ba0588793a461f276
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58818460"
---
# <a name="function-statement-visual-basic"></a><span data-ttu-id="6aad4-102">Function, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6aad4-102">Function Statement (Visual Basic)</span></span>
<span data-ttu-id="6aad4-103">Déclare le nom, paramètres et le code qui définissent une `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-103">Declares the name, parameters, and code that define a `Function` procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6aad4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aad4-104">Syntax</span></span>  
  
```  
[ <attributelist> ] [ accessmodifier ] [ proceduremodifiers ] [ Shared ] [ Shadows ] [ Async | Iterator ]  
Function name [ (Of typeparamlist) ] [ (parameterlist) ] [ As returntype ] [ Implements implementslist | Handles eventlist ]  
    [ statements ]  
    [ Exit Function ]  
    [ statements ]  
End Function  
```  
  
## <a name="parts"></a><span data-ttu-id="6aad4-105">Composants</span><span class="sxs-lookup"><span data-stu-id="6aad4-105">Parts</span></span>  
  
-   `attributelist`  
  
     <span data-ttu-id="6aad4-106">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6aad4-106">Optional.</span></span> <span data-ttu-id="6aad4-107">Consultez [liste d’attributs](attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-107">See [Attribute List](attribute-list.md).</span></span>  
  
-   `accessmodifier`  
  
     <span data-ttu-id="6aad4-108">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6aad4-108">Optional.</span></span> <span data-ttu-id="6aad4-109">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6aad4-109">Can be one of the following:</span></span>  
  
    -   [<span data-ttu-id="6aad4-110">Public</span><span class="sxs-lookup"><span data-stu-id="6aad4-110">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)  
  
    -   [<span data-ttu-id="6aad4-111">Protected</span><span class="sxs-lookup"><span data-stu-id="6aad4-111">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)  
  
    -   [<span data-ttu-id="6aad4-112">Friend</span><span class="sxs-lookup"><span data-stu-id="6aad4-112">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)  
  
    -   [<span data-ttu-id="6aad4-113">Private</span><span class="sxs-lookup"><span data-stu-id="6aad4-113">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)  
  
    -   [<span data-ttu-id="6aad4-114">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="6aad4-114">Protected Friend</span></span>](../../language-reference/modifiers/protected-friend.md)

    - [<span data-ttu-id="6aad4-115">Private Protected</span><span class="sxs-lookup"><span data-stu-id="6aad4-115">Private Protected</span></span>](../../language-reference/modifiers/private-protected.md)  
  
     <span data-ttu-id="6aad4-116">Consultez [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-116">See [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>  
  
-   `proceduremodifiers`  
  
     <span data-ttu-id="6aad4-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-117">Optional.</span></span> <span data-ttu-id="6aad4-118">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="6aad4-118">Can be one of the following:</span></span>  
  
    -   [<span data-ttu-id="6aad4-119">Overloads</span><span class="sxs-lookup"><span data-stu-id="6aad4-119">Overloads</span></span>](../../../visual-basic/language-reference/modifiers/overloads.md)  
  
    -   [<span data-ttu-id="6aad4-120">Overrides</span><span class="sxs-lookup"><span data-stu-id="6aad4-120">Overrides</span></span>](../../../visual-basic/language-reference/modifiers/overrides.md)  
  
    -   [<span data-ttu-id="6aad4-121">Overridable</span><span class="sxs-lookup"><span data-stu-id="6aad4-121">Overridable</span></span>](../../../visual-basic/language-reference/modifiers/overridable.md)  
  
    -   [<span data-ttu-id="6aad4-122">NotOverridable</span><span class="sxs-lookup"><span data-stu-id="6aad4-122">NotOverridable</span></span>](../../../visual-basic/language-reference/modifiers/notoverridable.md)  
  
    -   [<span data-ttu-id="6aad4-123">MustOverride</span><span class="sxs-lookup"><span data-stu-id="6aad4-123">MustOverride</span></span>](../../../visual-basic/language-reference/modifiers/mustoverride.md)  
  
    -   `MustOverride Overrides`  
  
    -   `NotOverridable Overrides`  
  
-   `Shared`  
  
     <span data-ttu-id="6aad4-124">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-124">Optional.</span></span> <span data-ttu-id="6aad4-125">Consultez [partagé](../../../visual-basic/language-reference/modifiers/shared.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-125">See [Shared](../../../visual-basic/language-reference/modifiers/shared.md).</span></span>  
  
-   `Shadows`  
  
     <span data-ttu-id="6aad4-126">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-126">Optional.</span></span> <span data-ttu-id="6aad4-127">Consultez [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-127">See [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span></span>  
  
-   `Async`  
  
     <span data-ttu-id="6aad4-128">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-128">Optional.</span></span> <span data-ttu-id="6aad4-129">Consultez [Async](../../../visual-basic/language-reference/modifiers/async.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-129">See [Async](../../../visual-basic/language-reference/modifiers/async.md).</span></span>  
  
-   `Iterator`  
  
     <span data-ttu-id="6aad4-130">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-130">Optional.</span></span> <span data-ttu-id="6aad4-131">Consultez [itérateur](../../../visual-basic/language-reference/modifiers/iterator.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-131">See [Iterator](../../../visual-basic/language-reference/modifiers/iterator.md).</span></span>  
  
-   `name`  
  
     <span data-ttu-id="6aad4-132">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6aad4-132">Required.</span></span> <span data-ttu-id="6aad4-133">Nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-133">Name of the procedure.</span></span> <span data-ttu-id="6aad4-134">Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-134">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>  
  
-   `typeparamlist`  
  
     <span data-ttu-id="6aad4-135">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-135">Optional.</span></span> <span data-ttu-id="6aad4-136">Liste de paramètres de type pour une procédure générique.</span><span class="sxs-lookup"><span data-stu-id="6aad4-136">List of type parameters for a generic procedure.</span></span> <span data-ttu-id="6aad4-137">Consultez [tapez liste](type-list.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-137">See [Type List](type-list.md).</span></span>  
  
-   `parameterlist`  
  
     <span data-ttu-id="6aad4-138">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-138">Optional.</span></span> <span data-ttu-id="6aad4-139">Liste des noms de variables locales qui représentent les paramètres de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-139">List of local variable names representing the parameters of this procedure.</span></span> <span data-ttu-id="6aad4-140">Consultez [liste de paramètres](parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-140">See [Parameter List](parameter-list.md).</span></span>  
  
-   `returntype`  
  
     <span data-ttu-id="6aad4-141">Obligatoire si `Option Strict` est `On`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-141">Required if `Option Strict` is `On`.</span></span> <span data-ttu-id="6aad4-142">Type de données de la valeur retournée par cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-142">Data type of the value returned by this procedure.</span></span>  
  
-   `Implements`  
  
     <span data-ttu-id="6aad4-143">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6aad4-143">Optional.</span></span> <span data-ttu-id="6aad4-144">Indique que cette procédure implémente un ou plusieurs `Function` procédures, chacune étant définie dans une interface implémentée par la classe ou la structure conteneur de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-144">Indicates that this procedure implements one or more `Function` procedures, each one defined in an interface implemented by this procedure's containing class or structure.</span></span> <span data-ttu-id="6aad4-145">Consultez [implémente instruction](implements-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-145">See [Implements Statement](implements-statement.md).</span></span>  
  
-   `implementslist`  
  
     <span data-ttu-id="6aad4-146">Obligatoire si `Implements` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6aad4-146">Required if `Implements` is supplied.</span></span> <span data-ttu-id="6aad4-147">Liste des procédures `Function` en cours d'implémentation.</span><span class="sxs-lookup"><span data-stu-id="6aad4-147">List of `Function` procedures being implemented.</span></span>  
  
     `implementedprocedure [ , implementedprocedure ... ]`  
  
     <span data-ttu-id="6aad4-148">Chaque `implementedprocedure` emploie la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6aad4-148">Each `implementedprocedure` has the following syntax and parts:</span></span>  
  
     `interface.definedname`  
  
    |<span data-ttu-id="6aad4-149">Élément</span><span class="sxs-lookup"><span data-stu-id="6aad4-149">Part</span></span>|<span data-ttu-id="6aad4-150">Description</span><span class="sxs-lookup"><span data-stu-id="6aad4-150">Description</span></span>|  
    |---|---|  
    |`interface`|<span data-ttu-id="6aad4-151">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6aad4-151">Required.</span></span> <span data-ttu-id="6aad4-152">Nom d’une interface implémentée par cette procédure classe ou la structure conteneur.</span><span class="sxs-lookup"><span data-stu-id="6aad4-152">Name of an interface implemented by this procedure's containing class or structure.</span></span>|  
    |`definedname`|<span data-ttu-id="6aad4-153">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6aad4-153">Required.</span></span> <span data-ttu-id="6aad4-154">Nom par lequel la procédure est définie dans `interface`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-154">Name by which the procedure is defined in `interface`.</span></span>|  
  
-   `Handles`  
  
     <span data-ttu-id="6aad4-155">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-155">Optional.</span></span> <span data-ttu-id="6aad4-156">Indique que cette procédure peut gérer un ou plusieurs événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6aad4-156">Indicates that this procedure can handle one or more specific events.</span></span> <span data-ttu-id="6aad4-157">Consultez [gère](handles-clause.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-157">See [Handles](handles-clause.md).</span></span>  
  
-   `eventlist`  
  
     <span data-ttu-id="6aad4-158">Obligatoire si `Handles` est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6aad4-158">Required if `Handles` is supplied.</span></span> <span data-ttu-id="6aad4-159">Liste des événements qui que gère cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-159">List of events this procedure handles.</span></span>  
  
     `eventspecifier [ , eventspecifier ... ]`  
  
     <span data-ttu-id="6aad4-160">Chaque `eventspecifier` emploie la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6aad4-160">Each `eventspecifier` has the following syntax and parts:</span></span>  
  
     `eventvariable.event`  
  
    |<span data-ttu-id="6aad4-161">Élément</span><span class="sxs-lookup"><span data-stu-id="6aad4-161">Part</span></span>|<span data-ttu-id="6aad4-162">Description</span><span class="sxs-lookup"><span data-stu-id="6aad4-162">Description</span></span>|  
    |---|---|  
    |`eventvariable`|<span data-ttu-id="6aad4-163">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6aad4-163">Required.</span></span> <span data-ttu-id="6aad4-164">Variable objet déclarée avec le type de données de la classe ou structure qui déclenche l’événement.</span><span class="sxs-lookup"><span data-stu-id="6aad4-164">Object variable declared with the data type of the class or structure that raises the event.</span></span>|  
    |`event`|<span data-ttu-id="6aad4-165">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6aad4-165">Required.</span></span> <span data-ttu-id="6aad4-166">Nom de l’événement que gère cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-166">Name of the event this procedure handles.</span></span>|  
  
-   `statements`  
  
     <span data-ttu-id="6aad4-167">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6aad4-167">Optional.</span></span> <span data-ttu-id="6aad4-168">Bloc d’instructions à exécuter dans cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-168">Block of statements to be executed within this procedure.</span></span>  
  
-   `End Function`  
  
     <span data-ttu-id="6aad4-169">Termine la définition de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-169">Terminates the definition of this procedure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6aad4-170">Notes</span><span class="sxs-lookup"><span data-stu-id="6aad4-170">Remarks</span></span>  
 <span data-ttu-id="6aad4-171">Tout le code exécutable doit être à l’intérieur d’une procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-171">All executable code must be inside a procedure.</span></span> <span data-ttu-id="6aad4-172">Chaque procédure, à son tour, est déclarée dans une classe, une structure ou un module qui correspond à la classe de conteneur, la structure ou le module.</span><span class="sxs-lookup"><span data-stu-id="6aad4-172">Each procedure, in turn, is declared within a class, a structure, or a module that is referred to as the containing class, structure, or module.</span></span>  
  
 <span data-ttu-id="6aad4-173">Pour retourner une valeur au code appelant, utilisez un `Function` procédure ; sinon, utilisez un `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-173">To return a value to the calling code, use a `Function` procedure; otherwise, use a `Sub` procedure.</span></span>  
  
## <a name="defining-a-function"></a><span data-ttu-id="6aad4-174">Définition d’une fonction</span><span class="sxs-lookup"><span data-stu-id="6aad4-174">Defining a Function</span></span>  
 <span data-ttu-id="6aad4-175">Vous pouvez définir un `Function` procédure uniquement au niveau du module.</span><span class="sxs-lookup"><span data-stu-id="6aad4-175">You can define a `Function` procedure only at the module level.</span></span> <span data-ttu-id="6aad4-176">Par conséquent, le contexte de déclaration pour une fonction doit être une classe, une structure, un module ou une interface et ne peut pas être un fichier source, un espace de noms, une procédure ou un bloc.</span><span class="sxs-lookup"><span data-stu-id="6aad4-176">Therefore, the declaration context for a function must be a class, a structure, a module, or an interface and can't be a source file, a namespace, a procedure, or a block.</span></span> <span data-ttu-id="6aad4-177">Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](declaration-contexts-and-default-access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-177">For more information, see [Declaration Contexts and Default Access Levels](declaration-contexts-and-default-access-levels.md).</span></span>  
  
 <span data-ttu-id="6aad4-178">`Function` les procédures par défaut d’un accès public.</span><span class="sxs-lookup"><span data-stu-id="6aad4-178">`Function` procedures default to public access.</span></span> <span data-ttu-id="6aad4-179">Vous pouvez ajuster leurs niveaux d’accès avec les modificateurs d’accès.</span><span class="sxs-lookup"><span data-stu-id="6aad4-179">You can adjust their access levels with the access modifiers.</span></span>  
  
 <span data-ttu-id="6aad4-180">Un `Function` procédure peut déclarer le type de données de la valeur de retour de la procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-180">A `Function` procedure can declare the data type of the value that the procedure returns.</span></span> <span data-ttu-id="6aad4-181">Vous pouvez spécifier n’importe quel type de données ou le nom d’une énumération, une structure, une classe ou une interface.</span><span class="sxs-lookup"><span data-stu-id="6aad4-181">You can specify any data type or the name of an enumeration, a structure, a class, or an interface.</span></span> <span data-ttu-id="6aad4-182">Si vous ne spécifiez pas le `returntype` , la procédure retourne `Object`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-182">If you don't specify the `returntype` parameter, the procedure returns `Object`.</span></span>  
  
 <span data-ttu-id="6aad4-183">Si cette procédure utilise le `Implements` mot clé, la classe de conteneur ou la structure doit également avoir un `Implements` instruction qui suit immédiatement sa `Class` ou `Structure` instruction.</span><span class="sxs-lookup"><span data-stu-id="6aad4-183">If this procedure uses the `Implements` keyword, the containing class or structure must also have an `Implements` statement that immediately follows its `Class` or `Structure` statement.</span></span> <span data-ttu-id="6aad4-184">Le `Implements` instruction doit inclure chaque interface spécifiée dans `implementslist`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-184">The `Implements` statement must include each interface that's specified in `implementslist`.</span></span> <span data-ttu-id="6aad4-185">Toutefois, le nom par lequel une interface définit les `Function` (dans `definedname`) n’a pas besoin de correspondre au nom de cette procédure (dans `name`).</span><span class="sxs-lookup"><span data-stu-id="6aad4-185">However, the name by which an interface defines the `Function` (in `definedname`) doesn't need to match the name of this procedure (in `name`).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6aad4-186">Vous pouvez utiliser des expressions lambda pour définir des expressions de fonction inline.</span><span class="sxs-lookup"><span data-stu-id="6aad4-186">You can use lambda expressions to define function expressions inline.</span></span> <span data-ttu-id="6aad4-187">Pour plus d’informations, consultez [Expression de fonction](../../../visual-basic/language-reference/operators/function-expression.md) et [Expressions Lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-187">For more information, see [Function Expression](../../../visual-basic/language-reference/operators/function-expression.md) and [Lambda Expressions](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span></span>  
  
## <a name="returning-from-a-function"></a><span data-ttu-id="6aad4-188">Retour d’une fonction</span><span class="sxs-lookup"><span data-stu-id="6aad4-188">Returning from a Function</span></span>  
 <span data-ttu-id="6aad4-189">Lorsque le `Function` procédure retourne au code appelant, l’exécution se poursuit avec l’instruction qui suit l’instruction qui a appelé la procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-189">When the `Function` procedure returns to the calling code, execution continues with the statement that follows the statement that called the procedure.</span></span>  
  
 <span data-ttu-id="6aad4-190">Pour retourner une valeur à partir d’une fonction, vous pouvez affecter la valeur pour le nom de fonction ou l’inclure dans un `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="6aad4-190">To return a value from a function, you can either assign the value to the function name or include it in a `Return` statement.</span></span>  
  
 <span data-ttu-id="6aad4-191">La `Return` instruction assigne la valeur de retour simultanément et quitte la fonction, comme le montre l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6aad4-191">The `Return` statement simultaneously assigns the return value and exits the function, as the following example shows.</span></span>  
  
 [!code-vb[VbVbalrStatements#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#24)]  
  
 <span data-ttu-id="6aad4-192">L’exemple suivant affecte la valeur de retour pour le nom de fonction `myFunction` et utilise ensuite la `Exit Function` instruction à retourner.</span><span class="sxs-lookup"><span data-stu-id="6aad4-192">The following example assigns the return value to the function name `myFunction` and then uses the `Exit Function` statement to return.</span></span>  
  
 [!code-vb[VbVbalrStatements#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#23)]  
  
 <span data-ttu-id="6aad4-193">Le `Exit Function` et `Return` instructions provoquent la sortie immédiate à partir d’un `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-193">The `Exit Function` and `Return` statements cause an immediate exit from a `Function` procedure.</span></span> <span data-ttu-id="6aad4-194">Un nombre quelconque de `Exit Function` et `Return` instructions peuvent apparaître n’importe où dans la procédure, et vous pouvez combiner `Exit Function` et `Return` instructions.</span><span class="sxs-lookup"><span data-stu-id="6aad4-194">Any number of `Exit Function` and `Return` statements can appear anywhere in the procedure, and you can mix `Exit Function` and `Return` statements.</span></span>  
  
 <span data-ttu-id="6aad4-195">Si vous utilisez `Exit Function` sans assigner une valeur à `name`, la procédure retourne la valeur par défaut pour le type de données qui est spécifié dans `returntype`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-195">If you use `Exit Function` without assigning a value to `name`, the procedure returns the default value for the data type that's specified in `returntype`.</span></span> <span data-ttu-id="6aad4-196">Si `returntype` n’est pas spécifié, la procédure retourne `Nothing`, qui est la valeur par défaut `Object`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-196">If `returntype` isn't specified, the procedure returns `Nothing`, which is the default value for `Object`.</span></span>  
  
## <a name="calling-a-function"></a><span data-ttu-id="6aad4-197">Appel d’une fonction</span><span class="sxs-lookup"><span data-stu-id="6aad4-197">Calling a Function</span></span>  
 <span data-ttu-id="6aad4-198">Vous appelez un `Function` procédure en utilisant le nom de la procédure, suivi de la liste d’arguments entre parenthèses, dans une expression.</span><span class="sxs-lookup"><span data-stu-id="6aad4-198">You call a `Function` procedure by using the procedure name, followed by the argument list in parentheses, in an expression.</span></span> <span data-ttu-id="6aad4-199">Vous pouvez omettre les parenthèses uniquement si vous ne fournissez des arguments.</span><span class="sxs-lookup"><span data-stu-id="6aad4-199">You can omit the parentheses only if you aren't supplying any arguments.</span></span> <span data-ttu-id="6aad4-200">Toutefois, votre code est plus lisible si vous incluez toujours les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="6aad4-200">However, your code is more readable if you always include the parentheses.</span></span>  
  
 <span data-ttu-id="6aad4-201">Vous appelez un `Function` procédure fonctionne de la même façon que vous appelez n’importe quelle bibliothèque comme `Sqrt`, `Cos`, ou `ChrW`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-201">You call a `Function` procedure the same way that you call any library function such as `Sqrt`, `Cos`, or `ChrW`.</span></span>  
  
 <span data-ttu-id="6aad4-202">Vous pouvez également appeler une fonction à l’aide de la `Call` mot clé.</span><span class="sxs-lookup"><span data-stu-id="6aad4-202">You can also call a function by using the `Call` keyword.</span></span> <span data-ttu-id="6aad4-203">Dans ce cas, la valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6aad4-203">In that case, the return value is ignored.</span></span> <span data-ttu-id="6aad4-204">Utilisation de la `Call` mot clé n’est pas recommandé dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="6aad4-204">Use of the `Call` keyword isn't recommended in most cases.</span></span> <span data-ttu-id="6aad4-205">Pour plus d’informations, consultez [instruction Call](call-statement.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-205">For more information, see [Call Statement](call-statement.md).</span></span>  
  
 <span data-ttu-id="6aad4-206">Visual Basic réorganise quelquefois les expressions arithmétiques pour améliorer les performances internes.</span><span class="sxs-lookup"><span data-stu-id="6aad4-206">Visual Basic sometimes rearranges arithmetic expressions to increase internal efficiency.</span></span> <span data-ttu-id="6aad4-207">Pour cette raison, vous ne devez pas utiliser un `Function` procédure dans une expression arithmétique quand la fonction modifie la valeur des variables dans la même expression.</span><span class="sxs-lookup"><span data-stu-id="6aad4-207">For that reason, you shouldn't use a `Function` procedure in an arithmetic expression when the function changes the value of variables in the same expression.</span></span>  
  
## <a name="async-functions"></a><span data-ttu-id="6aad4-208">Fonctions asynchrones</span><span class="sxs-lookup"><span data-stu-id="6aad4-208">Async Functions</span></span>  
 <span data-ttu-id="6aad4-209">Le *Async* fonctionnalité vous permet d’appeler des fonctions asynchrones sans utiliser de rappels explicites ni fractionner manuellement votre code entre plusieurs fonctions ou expressions lambda.</span><span class="sxs-lookup"><span data-stu-id="6aad4-209">The *Async* feature allows you to invoke asynchronous functions without using explicit callbacks or manually splitting your code across multiple functions or lambda expressions.</span></span>  
  
 <span data-ttu-id="6aad4-210">Si vous marquez une fonction avec la [Async](../../../visual-basic/language-reference/modifiers/async.md) modificateur, vous pouvez utiliser la [Await](../../../visual-basic/language-reference/operators/await-operator.md) opérateur dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="6aad4-210">If you mark a function with the [Async](../../../visual-basic/language-reference/modifiers/async.md) modifier, you can use the [Await](../../../visual-basic/language-reference/operators/await-operator.md) operator in the function.</span></span> <span data-ttu-id="6aad4-211">Quand le contrôle atteint une `Await` expression dans le `Async` fonction, contrôle retourne à l’appelant et la progression dans la fonction est interrompue jusqu'à ce que la tâche attendue se termine.</span><span class="sxs-lookup"><span data-stu-id="6aad4-211">When control reaches an `Await` expression in the `Async` function, control returns to the caller, and progress in the function is suspended until the awaited task completes.</span></span> <span data-ttu-id="6aad4-212">Lorsque la tâche est terminée, l’exécution peut reprendre dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="6aad4-212">When the task is complete, execution can resume in the function.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6aad4-213">Un `Async` procédure retourne à l’appelant quand il rencontre le premier objet await qui n’est pas encore terminé ou qu’il arrive à la fin de la `Async` procédure, selon ce qui se produit en premier.</span><span class="sxs-lookup"><span data-stu-id="6aad4-213">An `Async` procedure returns to the caller when either it encounters the first awaited object that’s not yet complete, or it gets to the end of the `Async` procedure, whichever occurs first.</span></span>  
  
 <span data-ttu-id="6aad4-214">Un `Async` fonction peut avoir un type de retour <xref:System.Threading.Tasks.Task%601> ou <xref:System.Threading.Tasks.Task>.</span><span class="sxs-lookup"><span data-stu-id="6aad4-214">An `Async` function can have a return type of <xref:System.Threading.Tasks.Task%601> or <xref:System.Threading.Tasks.Task>.</span></span> <span data-ttu-id="6aad4-215">Un exemple d’un `Async` fonction qui a un type de retour de <xref:System.Threading.Tasks.Task%601> est fourni ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="6aad4-215">An example of an `Async` function that has a return type of <xref:System.Threading.Tasks.Task%601> is provided below.</span></span>  
  
 <span data-ttu-id="6aad4-216">Un `Async` fonction ne peut pas déclarer de [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) paramètres.</span><span class="sxs-lookup"><span data-stu-id="6aad4-216">An `Async` function cannot declare any [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) parameters.</span></span>  
  
 <span data-ttu-id="6aad4-217">Un [Sub, instruction](sub-statement.md) peut également être marquée avec le `Async` modificateur.</span><span class="sxs-lookup"><span data-stu-id="6aad4-217">A [Sub Statement](sub-statement.md) can also be marked with the `Async` modifier.</span></span> <span data-ttu-id="6aad4-218">Cela est principalement utilisé pour les gestionnaires d’événements, où une valeur ne peut pas être retournée.</span><span class="sxs-lookup"><span data-stu-id="6aad4-218">This is primarily used for event handlers, where a value cannot be returned.</span></span> <span data-ttu-id="6aad4-219">Un `Async` `Sub` procédure ne peut pas être attendue et l’appelant d’une `Async` `Sub` procédure ne peut pas intercepter les exceptions levées par le `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-219">An `Async` `Sub` procedure can't be awaited, and the caller of an `Async` `Sub` procedure can't catch exceptions that are thrown by the `Sub` procedure.</span></span>  
  
 <span data-ttu-id="6aad4-220">Pour plus d’informations sur `Async` fonctions, consultez [programmation asynchrone avec Async et Await](../../../visual-basic/programming-guide/concepts/async/index.md), [flux de contrôle dans les programmes Async](../../../visual-basic/programming-guide/concepts/async/control-flow-in-async-programs.md), et [Types de retour Async](../../../visual-basic/programming-guide/concepts/async/async-return-types.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-220">For more information about `Async` functions, see [Asynchronous Programming with Async and Await](../../../visual-basic/programming-guide/concepts/async/index.md), [Control Flow in Async Programs](../../../visual-basic/programming-guide/concepts/async/control-flow-in-async-programs.md), and [Async Return Types](../../../visual-basic/programming-guide/concepts/async/async-return-types.md).</span></span>  
  
## <a name="iterator-functions"></a><span data-ttu-id="6aad4-221">Fonctions d’itérateur</span><span class="sxs-lookup"><span data-stu-id="6aad4-221">Iterator Functions</span></span>  
 <span data-ttu-id="6aad4-222">Un *itérateur* fonction effectue une itération personnalisée sur une collection, comme une liste ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="6aad4-222">An *iterator* function performs a custom iteration over a collection, such as a list or array.</span></span> <span data-ttu-id="6aad4-223">Une fonction d’itérateur utilise le [Yield](yield-statement.md) instruction pour retourner chaque élément un par un.</span><span class="sxs-lookup"><span data-stu-id="6aad4-223">An iterator function uses the [Yield](yield-statement.md) statement to return each element one at a time.</span></span> <span data-ttu-id="6aad4-224">Quand un [Yield](yield-statement.md) instruction est atteinte, l’emplacement actuel dans le code est mémorisé.</span><span class="sxs-lookup"><span data-stu-id="6aad4-224">When a [Yield](yield-statement.md) statement is reached, the current location in code is remembered.</span></span> <span data-ttu-id="6aad4-225">L’exécution est redémarrée à partir de cet emplacement lors de l’appel suivant de la fonction d’itérateur.</span><span class="sxs-lookup"><span data-stu-id="6aad4-225">Execution is restarted from that location the next time the iterator function is called.</span></span>  
  
 <span data-ttu-id="6aad4-226">Vous appelez un itérateur depuis le code client en utilisant un [For Each... Suivant](for-each-next-statement.md) instruction.</span><span class="sxs-lookup"><span data-stu-id="6aad4-226">You call an iterator from client code by using a [For Each…Next](for-each-next-statement.md) statement.</span></span>  
  
 <span data-ttu-id="6aad4-227">Le type de retour d’une fonction d’itérateur peut être <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator>, ou <xref:System.Collections.Generic.IEnumerator%601>.</span><span class="sxs-lookup"><span data-stu-id="6aad4-227">The return type of an iterator function can be <xref:System.Collections.IEnumerable>, <xref:System.Collections.Generic.IEnumerable%601>, <xref:System.Collections.IEnumerator>, or <xref:System.Collections.Generic.IEnumerator%601>.</span></span>  
  
 <span data-ttu-id="6aad4-228">Pour plus d'informations, consultez [Itérateurs](../../programming-guide/concepts/iterators.md).</span><span class="sxs-lookup"><span data-stu-id="6aad4-228">For more information, see [Iterators](../../programming-guide/concepts/iterators.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="6aad4-229">Exemple</span><span class="sxs-lookup"><span data-stu-id="6aad4-229">Example</span></span>  
 <span data-ttu-id="6aad4-230">L’exemple suivant utilise le `Function` instruction pour déclarer le nom, le paramètres et le code qui forment le corps d’un `Function` procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-230">The following example uses the `Function` statement to declare the name, parameters, and code that form the body of a `Function` procedure.</span></span> <span data-ttu-id="6aad4-231">Le `ParamArray` modificateur permet à la fonction d’accepter un nombre variable d’arguments.</span><span class="sxs-lookup"><span data-stu-id="6aad4-231">The `ParamArray` modifier enables the function to accept a variable number of arguments.</span></span>  
  
 [!code-vb[VbVbalrStatements#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#25)]  
  
## <a name="example"></a><span data-ttu-id="6aad4-232">Exemple</span><span class="sxs-lookup"><span data-stu-id="6aad4-232">Example</span></span>  
 <span data-ttu-id="6aad4-233">L’exemple suivant appelle la fonction déclarée dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="6aad4-233">The following example invokes the function declared in the preceding example.</span></span>  
  
 [!code-vb[VbVbalrStatements#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#26)]  
  
## <a name="example"></a><span data-ttu-id="6aad4-234">Exemple</span><span class="sxs-lookup"><span data-stu-id="6aad4-234">Example</span></span>  
 <span data-ttu-id="6aad4-235">Dans l’exemple suivant, `DelayAsync` est un `Async` `Function` qui a un type de retour <xref:System.Threading.Tasks.Task%601>.</span><span class="sxs-lookup"><span data-stu-id="6aad4-235">In the following example, `DelayAsync` is an `Async` `Function` that has a return type of <xref:System.Threading.Tasks.Task%601>.</span></span> <span data-ttu-id="6aad4-236">`DelayAsync` a une instruction `Return` qui retourne un entier.</span><span class="sxs-lookup"><span data-stu-id="6aad4-236">`DelayAsync` has a `Return` statement that returns an integer.</span></span> <span data-ttu-id="6aad4-237">Par conséquent, la déclaration de fonction de `DelayAsync` doit avoir un type de retour `Task(Of Integer)`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-237">Therefore the function declaration of `DelayAsync` needs to have a return type of `Task(Of Integer)`.</span></span> <span data-ttu-id="6aad4-238">Étant donné que le type de retour est `Task(Of Integer)`, l’évaluation de la `Await` expression dans `DoSomethingAsync` produit un entier.</span><span class="sxs-lookup"><span data-stu-id="6aad4-238">Because the return type is `Task(Of Integer)`, the evaluation of the `Await` expression in `DoSomethingAsync` produces an integer.</span></span> <span data-ttu-id="6aad4-239">Cela est illustré dans cette déclaration : `Dim result As Integer = Await delayTask`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-239">This is demonstrated in this statement: `Dim result As Integer = Await delayTask`.</span></span>  
  
 <span data-ttu-id="6aad4-240">Le `startButton_Click` procédure est un exemple d’un `Async Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="6aad4-240">The `startButton_Click` procedure is an example of an `Async Sub` procedure.</span></span> <span data-ttu-id="6aad4-241">Étant donné que `DoSomethingAsync` est un `Async` (fonction), la tâche pour l’appel à `DoSomethingAsync` doit être attendue, comme le montre l’instruction suivante : `Await DoSomethingAsync()`.</span><span class="sxs-lookup"><span data-stu-id="6aad4-241">Because `DoSomethingAsync` is an `Async` function, the task for the call to `DoSomethingAsync` must be awaited, as the following statement demonstrates: `Await DoSomethingAsync()`.</span></span> <span data-ttu-id="6aad4-242">Le `startButton_Click` `Sub` procédure doit être définie avec la `Async` modificateur, car il possède un `Await` expression.</span><span class="sxs-lookup"><span data-stu-id="6aad4-242">The `startButton_Click` `Sub` procedure must be defined with the `Async` modifier because it has an `Await` expression.</span></span>  
  
 [!code-vb[csAsyncMethod#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/csasyncmethod/vb/mainwindow.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="6aad4-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aad4-243">See also</span></span>

- [<span data-ttu-id="6aad4-244">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="6aad4-244">Sub Statement</span></span>](sub-statement.md)
- [<span data-ttu-id="6aad4-245">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="6aad4-245">Function Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/function-procedures.md)
- [<span data-ttu-id="6aad4-246">Liste de paramètres</span><span class="sxs-lookup"><span data-stu-id="6aad4-246">Parameter List</span></span>](parameter-list.md)
- [<span data-ttu-id="6aad4-247">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="6aad4-247">Dim Statement</span></span>](dim-statement.md)
- [<span data-ttu-id="6aad4-248">Call (instruction)</span><span class="sxs-lookup"><span data-stu-id="6aad4-248">Call Statement</span></span>](call-statement.md)
- [<span data-ttu-id="6aad4-249">Of</span><span class="sxs-lookup"><span data-stu-id="6aad4-249">Of</span></span>](of-clause.md)
- [<span data-ttu-id="6aad4-250">tableaux de paramètres</span><span class="sxs-lookup"><span data-stu-id="6aad4-250">Parameter Arrays</span></span>](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md)
- [<span data-ttu-id="6aad4-251">Guide pratique pour utiliser une classe générique</span><span class="sxs-lookup"><span data-stu-id="6aad4-251">How to: Use a Generic Class</span></span>](../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)
- [<span data-ttu-id="6aad4-252">Procédures de dépannage</span><span class="sxs-lookup"><span data-stu-id="6aad4-252">Troubleshooting Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/troubleshooting-procedures.md)
- [<span data-ttu-id="6aad4-253">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="6aad4-253">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="6aad4-254">Expression de fonction</span><span class="sxs-lookup"><span data-stu-id="6aad4-254">Function Expression</span></span>](../../../visual-basic/language-reference/operators/function-expression.md)
