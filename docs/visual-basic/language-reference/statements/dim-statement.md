---
title: Dim, instruction (Visual Basic)
ms.date: 05/12/2018
f1_keywords:
- vb.Dim
- Dim
helpviewer_keywords:
- Public keyword [Visual Basic], in Dim statement
- Dim statement [Visual Basic]
- fixed-length strings [Visual Basic], declaring
- variables [Visual Basic], declaring
- WithEvents keyword [Visual Basic], Dim statement
- dynamic arrays [Visual Basic], Dim statement
- variables [Visual Basic], initializing
- '{} braces'
- fields [Visual Basic], as member variables
- declarations [Visual Basic], dynamic arrays
- member variables [Visual Basic]
- default values [Visual Basic]
- data types [Visual Basic], assigning
- braces {}
- As keyword [Visual Basic], in Dim statement
- arrays [Visual Basic], declaring
- New keyword [Visual Basic], Dim statement
- To keyword [Visual Basic], in Dim statement
- storage [Visual Basic], allocating
- local variables [Visual Basic]
- declaration statements [Visual Basic]
- Dim statement [Visual Basic], syntax
- variables [Visual Basic], member and local
ms.assetid: fae3eca1-f0b2-4400-994b-7aa58a848448
ms.openlocfilehash: 5a16060efc45cc0642aa6612d02644e252cd53d9
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64751796"
---
# <a name="dim-statement-visual-basic"></a><span data-ttu-id="d8428-102">Dim, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8428-102">Dim Statement (Visual Basic)</span></span>

<span data-ttu-id="d8428-103">Déclare et alloue de l’espace de stockage pour une ou plusieurs variables.</span><span class="sxs-lookup"><span data-stu-id="d8428-103">Declares and allocates storage space for one or more variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8428-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8428-104">Syntax</span></span>

```
[ <attributelist> ] [ accessmodifier ] [[ Shared ] [ Shadows ] | [ Static ]] [ ReadOnly ]
Dim [ WithEvents ] variablelist
```

## <a name="parts"></a><span data-ttu-id="d8428-105">Composants</span><span class="sxs-lookup"><span data-stu-id="d8428-105">Parts</span></span>

- `attributelist`

  <span data-ttu-id="d8428-106">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-106">Optional.</span></span> <span data-ttu-id="d8428-107">Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-107">See [Attribute List](../../../visual-basic/language-reference/statements/attribute-list.md).</span></span>

- `accessmodifier`

  <span data-ttu-id="d8428-108">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-108">Optional.</span></span> <span data-ttu-id="d8428-109">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8428-109">Can be one of the following:</span></span>

  - [<span data-ttu-id="d8428-110">Public</span><span class="sxs-lookup"><span data-stu-id="d8428-110">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)

  - [<span data-ttu-id="d8428-111">Protected</span><span class="sxs-lookup"><span data-stu-id="d8428-111">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)

  - [<span data-ttu-id="d8428-112">Friend</span><span class="sxs-lookup"><span data-stu-id="d8428-112">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)

  - [<span data-ttu-id="d8428-113">Private</span><span class="sxs-lookup"><span data-stu-id="d8428-113">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)

  - [<span data-ttu-id="d8428-114">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="d8428-114">Protected Friend</span></span>](../../language-reference/modifiers/protected-friend.md)

  - [<span data-ttu-id="d8428-115">Private Protected</span><span class="sxs-lookup"><span data-stu-id="d8428-115">Private Protected</span></span>](../../language-reference/modifiers/private-protected.md)

  <span data-ttu-id="d8428-116">Consultez [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-116">See [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>

- `Shared`

  <span data-ttu-id="d8428-117">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-117">Optional.</span></span> <span data-ttu-id="d8428-118">Consultez [partagé](../../../visual-basic/language-reference/modifiers/shared.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-118">See [Shared](../../../visual-basic/language-reference/modifiers/shared.md).</span></span>

- `Shadows`

  <span data-ttu-id="d8428-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-119">Optional.</span></span> <span data-ttu-id="d8428-120">Consultez [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-120">See [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).</span></span>

- `Static`

  <span data-ttu-id="d8428-121">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-121">Optional.</span></span> <span data-ttu-id="d8428-122">Consultez [statique](../../../visual-basic/language-reference/modifiers/static.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-122">See [Static](../../../visual-basic/language-reference/modifiers/static.md).</span></span>

- `ReadOnly`

  <span data-ttu-id="d8428-123">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-123">Optional.</span></span> <span data-ttu-id="d8428-124">Consultez [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-124">See [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).</span></span>

- `WithEvents`

<span data-ttu-id="d8428-125">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-125">Optional.</span></span> <span data-ttu-id="d8428-126">Spécifie qu’il s’agit de variables objets qui font référence aux instances d’une classe qui peut déclencher des événements.</span><span class="sxs-lookup"><span data-stu-id="d8428-126">Specifies that these are object variables that refer to instances of a class that can raise events.</span></span> <span data-ttu-id="d8428-127">Consultez [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-127">See [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md).</span></span>

- `variablelist`

  <span data-ttu-id="d8428-128">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d8428-128">Required.</span></span> <span data-ttu-id="d8428-129">Liste des variables déclarées dans cette instruction.</span><span class="sxs-lookup"><span data-stu-id="d8428-129">List of variables being declared in this statement.</span></span>

  `variable [ , variable ... ]`

  <span data-ttu-id="d8428-130">Chaque `variable` emploie la syntaxe et les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8428-130">Each `variable` has the following syntax and parts:</span></span>

  <span data-ttu-id="d8428-131">`variablename [ ( [ boundslist ] ) ] [ As [ New ] datatype [ With`{`[ .propertyname = propinitializer [ , ... ] ] } ] ] [ = initializer ]`</span><span class="sxs-lookup"><span data-stu-id="d8428-131">`variablename [ ( [ boundslist ] ) ] [ As [ New ] datatype [ With`{`[ .propertyname = propinitializer [ , ... ] ] } ] ] [ = initializer ]`</span></span>

  |<span data-ttu-id="d8428-132">Élément</span><span class="sxs-lookup"><span data-stu-id="d8428-132">Part</span></span>|<span data-ttu-id="d8428-133">Description</span><span class="sxs-lookup"><span data-stu-id="d8428-133">Description</span></span>|
  |---|---|
  |`variablename`|<span data-ttu-id="d8428-134">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d8428-134">Required.</span></span> <span data-ttu-id="d8428-135">Nom de la variable.</span><span class="sxs-lookup"><span data-stu-id="d8428-135">Name of the variable.</span></span> <span data-ttu-id="d8428-136">Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-136">See [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>|
  |`boundslist`|<span data-ttu-id="d8428-137">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-137">Optional.</span></span> <span data-ttu-id="d8428-138">Liste des limites de chaque dimension d’une variable tableau.</span><span class="sxs-lookup"><span data-stu-id="d8428-138">List of bounds of each dimension of an array variable.</span></span>|
  |`New`|<span data-ttu-id="d8428-139">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-139">Optional.</span></span> <span data-ttu-id="d8428-140">Crée une nouvelle instance de la classe lors de la `Dim` instruction s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d8428-140">Creates a new instance of the class when the `Dim` statement runs.</span></span>|
  |`datatype`|<span data-ttu-id="d8428-141">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-141">Optional.</span></span> <span data-ttu-id="d8428-142">Type de données de la variable.</span><span class="sxs-lookup"><span data-stu-id="d8428-142">Data type of the variable.</span></span>|
  |`With`|<span data-ttu-id="d8428-143">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-143">Optional.</span></span> <span data-ttu-id="d8428-144">Présente la liste d’initialiseurs objet.</span><span class="sxs-lookup"><span data-stu-id="d8428-144">Introduces the object initializer list.</span></span>|
  |`propertyname`|<span data-ttu-id="d8428-145">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="d8428-145">Optional.</span></span> <span data-ttu-id="d8428-146">Le nom d’une propriété dans la classe, vous effectuez une instance de.</span><span class="sxs-lookup"><span data-stu-id="d8428-146">The name of a property in the class you are making an instance of.</span></span>|
  |`propinitializer`|<span data-ttu-id="d8428-147">Requis après `propertyname` =.</span><span class="sxs-lookup"><span data-stu-id="d8428-147">Required after `propertyname` =.</span></span> <span data-ttu-id="d8428-148">L’expression qui est évaluée et assignée au nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="d8428-148">The expression that is evaluated and assigned to the property name.</span></span>|
  |`initializer`|<span data-ttu-id="d8428-149">Facultatif si `New` n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="d8428-149">Optional if `New` is not specified.</span></span> <span data-ttu-id="d8428-150">Expression qui est évaluée et assignée à la variable lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="d8428-150">Expression that is evaluated and assigned to the variable when it is created.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d8428-151">Notes</span><span class="sxs-lookup"><span data-stu-id="d8428-151">Remarks</span></span>

<span data-ttu-id="d8428-152">Le compilateur Visual Basic utilise le `Dim` instruction pour déterminer le type de données de la variable et d’autres informations, telles que le code peut accéder à la variable.</span><span class="sxs-lookup"><span data-stu-id="d8428-152">The Visual Basic compiler uses the `Dim` statement to determine the variable's data type and other information, such as what code can access the variable.</span></span> <span data-ttu-id="d8428-153">L’exemple suivant déclare une variable qui doit contenir un `Integer` valeur.</span><span class="sxs-lookup"><span data-stu-id="d8428-153">The following example declares a variable to hold an `Integer` value.</span></span>

```vb
Dim numberOfStudents As Integer
```

<span data-ttu-id="d8428-154">Vous pouvez spécifier n’importe quel type de données ou le nom d’une énumération, une structure, une classe ou une interface.</span><span class="sxs-lookup"><span data-stu-id="d8428-154">You can specify any data type or the name of an enumeration, structure, class, or interface.</span></span>

```vb
Dim finished As Boolean
Dim monitorBox As System.Windows.Forms.Form
```

<span data-ttu-id="d8428-155">Pour un type référence, vous utilisez le `New` mot clé pour créer une nouvelle instance de la classe ou une structure qui est spécifié par le type de données.</span><span class="sxs-lookup"><span data-stu-id="d8428-155">For a reference type, you use the `New` keyword to create a new instance of the class or structure that is specified by the data type.</span></span> <span data-ttu-id="d8428-156">Si vous utilisez `New`, vous n’utilisez pas une expression d’initialiseur.</span><span class="sxs-lookup"><span data-stu-id="d8428-156">If you use `New`, you do not use an initializer expression.</span></span> <span data-ttu-id="d8428-157">Au lieu de cela, vous fournissez des arguments, s’ils sont requis, au constructeur de la classe à partir de laquelle vous créez la variable.</span><span class="sxs-lookup"><span data-stu-id="d8428-157">Instead, you supply arguments, if they are required, to the constructor of the class from which you are creating the variable.</span></span>

```vb
Dim bottomLabel As New System.Windows.Forms.Label
```

<span data-ttu-id="d8428-158">Vous pouvez déclarer une variable dans une procédure, un bloc, une classe, une structure ou un module.</span><span class="sxs-lookup"><span data-stu-id="d8428-158">You can declare a variable in a procedure, block, class, structure, or module.</span></span> <span data-ttu-id="d8428-159">Vous ne pouvez pas déclarer une variable dans un fichier source, un espace de noms ou une interface.</span><span class="sxs-lookup"><span data-stu-id="d8428-159">You cannot declare a variable in a source file, namespace, or interface.</span></span> <span data-ttu-id="d8428-160">Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-160">For more information, see [Declaration Contexts and Default Access Levels](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span></span>

<span data-ttu-id="d8428-161">Une variable déclarée au niveau du module, en dehors de toute procédure, est un *variable membre* ou *champ*.</span><span class="sxs-lookup"><span data-stu-id="d8428-161">A variable that is declared at module level, outside any procedure, is a *member variable* or *field*.</span></span> <span data-ttu-id="d8428-162">Les variables membres sont dans la portée tout au long de leur classe, une structure ou un module.</span><span class="sxs-lookup"><span data-stu-id="d8428-162">Member variables are in scope throughout their class, structure, or module.</span></span> <span data-ttu-id="d8428-163">Une variable déclarée au niveau de la procédure est un *variable locale*.</span><span class="sxs-lookup"><span data-stu-id="d8428-163">A variable that is declared at procedure level is a *local variable*.</span></span> <span data-ttu-id="d8428-164">Variables locales sont dans la portée uniquement au sein de leur procédure ou un bloc.</span><span class="sxs-lookup"><span data-stu-id="d8428-164">Local variables are in scope only within their procedure or block.</span></span>

<span data-ttu-id="d8428-165">Les modificateurs d’accès suivants sont utilisés pour déclarer des variables en dehors d’une procédure : `Public`, `Protected`, `Friend`, `Protected Friend`, et `Private`.</span><span class="sxs-lookup"><span data-stu-id="d8428-165">The following access modifiers are used to declare variables outside a procedure: `Public`, `Protected`, `Friend`, `Protected Friend`, and `Private`.</span></span> <span data-ttu-id="d8428-166">Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-166">For more information, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>

<span data-ttu-id="d8428-167">Le `Dim` mot clé est facultatif et généralement omis si vous spécifiez un des modificateurs suivants : `Public`, `Protected`, `Friend`, `Protected Friend`, `Private`, `Shared`, `Shadows`, `Static`, `ReadOnly`, ou `WithEvents`.</span><span class="sxs-lookup"><span data-stu-id="d8428-167">The `Dim` keyword is optional and usually omitted if you specify any of the following modifiers: `Public`, `Protected`, `Friend`, `Protected Friend`, `Private`, `Shared`, `Shadows`, `Static`, `ReadOnly`, or `WithEvents`.</span></span>

```vb
Public maximumAllowed As Double
Protected Friend currentUserName As String
Private salary As Decimal
Static runningTotal As Integer
```

<span data-ttu-id="d8428-168">Si `Option Explicit` est activée (valeur par défaut), le compilateur requiert une déclaration pour chaque variable que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="d8428-168">If `Option Explicit` is on (the default), the compiler requires a declaration for every variable you use.</span></span> <span data-ttu-id="d8428-169">Pour plus d’informations, consultez [Option Explicit, instruction](../../../visual-basic/language-reference/statements/option-explicit-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-169">For more information, see [Option Explicit Statement](../../../visual-basic/language-reference/statements/option-explicit-statement.md).</span></span>

## <a name="specifying-an-initial-value"></a><span data-ttu-id="d8428-170">Spécifier une valeur initiale</span><span class="sxs-lookup"><span data-stu-id="d8428-170">Specifying an Initial Value</span></span>

<span data-ttu-id="d8428-171">Vous pouvez affecter une valeur à une variable lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="d8428-171">You can assign a value to a variable when it is created.</span></span> <span data-ttu-id="d8428-172">Pour un type valeur, vous utilisez un *initialiseur* pour fournir une expression à assigner à la variable.</span><span class="sxs-lookup"><span data-stu-id="d8428-172">For a value type, you use an *initializer* to supply an expression to be assigned to the variable.</span></span> <span data-ttu-id="d8428-173">L’expression doit correspondre à une constante qui peut être calculée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d8428-173">The expression must evaluate to a constant that can be calculated at compile time.</span></span>

```vb
Dim quantity As Integer = 10
Dim message As String = "Just started"
```

<span data-ttu-id="d8428-174">Si un initialiseur est spécifié et un type de données n’est pas spécifié dans un `As` clause, *l’inférence de type* permet de déduire le type de données à partir de l’initialiseur.</span><span class="sxs-lookup"><span data-stu-id="d8428-174">If an initializer is specified and a data type is not specified in an `As` clause, *type inference* is used to infer the data type from the initializer.</span></span> <span data-ttu-id="d8428-175">Dans l’exemple suivant, les deux `num1` et `num2` sont fortement typées en tant qu’entiers.</span><span class="sxs-lookup"><span data-stu-id="d8428-175">In the following example, both `num1` and `num2` are strongly typed as integers.</span></span> <span data-ttu-id="d8428-176">Dans la seconde déclaration, l’inférence de type déduit le type à partir de la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="d8428-176">In the second declaration, type inference infers the type from the value 3.</span></span>

```vb
' Use explicit typing.
Dim num1 As Integer = 3

' Use local type inference.
Dim num2 = 3
```

<span data-ttu-id="d8428-177">Inférence de type s’applique au niveau de la procédure.</span><span class="sxs-lookup"><span data-stu-id="d8428-177">Type inference applies at the procedure level.</span></span> <span data-ttu-id="d8428-178">Il ne s’applique pas à l’extérieur d’une procédure dans une classe, une structure, un module ou une interface.</span><span class="sxs-lookup"><span data-stu-id="d8428-178">It does not apply outside a procedure in a class, structure, module, or interface.</span></span> <span data-ttu-id="d8428-179">Pour plus d’informations sur l’inférence de type, consultez [Option Infer, instruction](../../../visual-basic/language-reference/statements/option-infer-statement.md) et [l’inférence de Type Local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-179">For more information about type inference, see [Option Infer Statement](../../../visual-basic/language-reference/statements/option-infer-statement.md) and [Local Type Inference](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).</span></span>

<span data-ttu-id="d8428-180">Pour plus d’informations sur ce qui se passe quand un type de données ou un initialiseur n’est pas spécifié, consultez [par défaut des Types de données et les valeurs](../../../visual-basic/language-reference/statements/dim-statement.md#default) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d8428-180">For information about what happens when a data type or initializer is not specified, see [Default Data Types and Values](../../../visual-basic/language-reference/statements/dim-statement.md#default) later in this topic.</span></span>

<span data-ttu-id="d8428-181">Vous pouvez utiliser un *initialiseur d’objet* pour déclarer des instances de types nommés et anonymes.</span><span class="sxs-lookup"><span data-stu-id="d8428-181">You can use an *object initializer* to declare instances of named and anonymous types.</span></span> <span data-ttu-id="d8428-182">Le code suivant crée une instance d’un `Student` classe et utilise un initialiseur d’objet pour initialiser des propriétés.</span><span class="sxs-lookup"><span data-stu-id="d8428-182">The following code creates an instance of a `Student` class and uses an object initializer to initialize properties.</span></span>

```vb
Dim student1 As New Student With {.First = "Michael",
                                  .Last = "Tucker"}
```

<span data-ttu-id="d8428-183">Pour plus d’informations sur les initialiseurs d’objets, consultez [Comment : Déclarez un objet à l’aide d’un initialiseur d’objet](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-declare-an-object-by-using-an-object-initializer.md), [initialiseurs d’objets : Types nommés et anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md), et [Types anonymes](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-183">For more information about object initializers, see [How to: Declare an Object by Using an Object Initializer](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-declare-an-object-by-using-an-object-initializer.md), [Object Initializers: Named and Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md), and [Anonymous Types](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md).</span></span>

## <a name="declaring-multiple-variables"></a><span data-ttu-id="d8428-184">Déclaration de Variables multiples</span><span class="sxs-lookup"><span data-stu-id="d8428-184">Declaring Multiple Variables</span></span>

<span data-ttu-id="d8428-185">Vous pouvez déclarer plusieurs variables dans la même instruction de déclaration, en spécifiant le nom de variable pour chacun d'entre eux et suivre chaque nom de tableau avec des parenthèses.</span><span class="sxs-lookup"><span data-stu-id="d8428-185">You can declare several variables in one declaration statement, specifying the variable name for each one, and following each array name with parentheses.</span></span> <span data-ttu-id="d8428-186">Les variables multiples sont séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d8428-186">Multiple variables are separated by commas.</span></span>

```vb
Dim lastTime, nextTime, allTimes() As Date
```

<span data-ttu-id="d8428-187">Si vous déclarez plusieurs variables avec une `As` clause, vous ne pouvez pas fournir un initialiseur pour ce groupe de variables.</span><span class="sxs-lookup"><span data-stu-id="d8428-187">If you declare more than one variable with one `As` clause, you cannot supply an initializer for that group of variables.</span></span>

<span data-ttu-id="d8428-188">Vous pouvez spécifier différents types de données pour différentes variables à l’aide d’un distinct `As` pour chaque variable que vous déclarez.</span><span class="sxs-lookup"><span data-stu-id="d8428-188">You can specify different data types for different variables by using a separate `As` clause for each variable you declare.</span></span> <span data-ttu-id="d8428-189">Chaque variable prend le type de données spécifié dans la première `As` clause rencontrée après son `variablename` partie.</span><span class="sxs-lookup"><span data-stu-id="d8428-189">Each variable takes the data type specified in the first `As` clause encountered after its `variablename` part.</span></span>

```vb
Dim a, b, c As Single, x, y As Double, i As Integer
' a, b, and c are all Single; x and y are both Double
```

## <a name="arrays"></a><span data-ttu-id="d8428-190">Tableaux</span><span class="sxs-lookup"><span data-stu-id="d8428-190">Arrays</span></span>

<span data-ttu-id="d8428-191">Vous pouvez déclarer une variable qui doit contenir un *tableau*, qui peut contenir plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="d8428-191">You can declare a variable to hold an *array*, which can hold multiple values.</span></span> <span data-ttu-id="d8428-192">Pour spécifier qu’une variable contient un tableau, suivez son `variablename` immédiatement avec des parenthèses.</span><span class="sxs-lookup"><span data-stu-id="d8428-192">To specify that a variable holds an array, follow its `variablename` immediately with parentheses.</span></span> <span data-ttu-id="d8428-193">Pour plus d’informations sur les tableaux, consultez [Tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-193">For more information about arrays, see [Arrays](../../../visual-basic/programming-guide/language-features/arrays/index.md).</span></span>

<span data-ttu-id="d8428-194">Vous pouvez spécifier la limite inférieure et supérieure de chaque dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="d8428-194">You can specify the lower and upper bound of each dimension of an array.</span></span> <span data-ttu-id="d8428-195">Pour ce faire, vous devez inclure un `boundslist` dans les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="d8428-195">To do this, include a `boundslist` inside the parentheses.</span></span> <span data-ttu-id="d8428-196">Pour chaque dimension, le `boundslist` spécifie la limite supérieure et éventuellement la limite inférieure.</span><span class="sxs-lookup"><span data-stu-id="d8428-196">For each dimension, the `boundslist` specifies the upper bound and optionally the lower bound.</span></span> <span data-ttu-id="d8428-197">La limite inférieure est toujours égal à zéro, que vous spécifiiez ou non.</span><span class="sxs-lookup"><span data-stu-id="d8428-197">The lower bound is always zero, whether you specify it or not.</span></span> <span data-ttu-id="d8428-198">Chaque index peut varier de zéro à sa valeur de limite supérieure.</span><span class="sxs-lookup"><span data-stu-id="d8428-198">Each index can vary from zero through its upper bound value.</span></span>

<span data-ttu-id="d8428-199">Les deux instructions suivantes sont équivalentes.</span><span class="sxs-lookup"><span data-stu-id="d8428-199">The following two statements are equivalent.</span></span> <span data-ttu-id="d8428-200">Chaque instruction déclare un tableau de 21 `Integer` éléments.</span><span class="sxs-lookup"><span data-stu-id="d8428-200">Each statement declares an array of 21 `Integer` elements.</span></span> <span data-ttu-id="d8428-201">Lorsque vous accédez au tableau, l’index peut varier de 0 à 20.</span><span class="sxs-lookup"><span data-stu-id="d8428-201">When you access the array, the index can vary from 0 through 20.</span></span>

```vb
Dim totals(20) As Integer
Dim totals(0 To 20) As Integer
```

<span data-ttu-id="d8428-202">L’instruction suivante déclare un tableau à deux dimensions de type `Double`.</span><span class="sxs-lookup"><span data-stu-id="d8428-202">The following statement declares a two-dimensional array of type `Double`.</span></span> <span data-ttu-id="d8428-203">Le tableau a 4 lignes (3 + 1) de 6 colonnes (5 + 1) chaque.</span><span class="sxs-lookup"><span data-stu-id="d8428-203">The array has 4 rows (3 + 1) of 6 columns (5 + 1) each.</span></span> <span data-ttu-id="d8428-204">Notez qu’une limite supérieure représente la valeur la plus élevée possible pour l’index, et non la longueur de la dimension.</span><span class="sxs-lookup"><span data-stu-id="d8428-204">Note that an upper bound represents the highest possible value for the index, not the length of the dimension.</span></span> <span data-ttu-id="d8428-205">La longueur de la dimension est la limite supérieure plus un.</span><span class="sxs-lookup"><span data-stu-id="d8428-205">The length of the dimension is the upper bound plus one.</span></span>

```vb
Dim matrix2(3, 5) As Double
```

<span data-ttu-id="d8428-206">Un tableau peut avoir de 1 à 32 dimensions.</span><span class="sxs-lookup"><span data-stu-id="d8428-206">An array can have from 1 to 32 dimensions.</span></span>

<span data-ttu-id="d8428-207">Vous pouvez laisser toutes les limites vides dans une déclaration de tableau.</span><span class="sxs-lookup"><span data-stu-id="d8428-207">You can leave all the bounds blank in an array declaration.</span></span> <span data-ttu-id="d8428-208">Si vous procédez ainsi, le tableau a le nombre de dimensions que vous spécifiez, mais il n’est pas initialisée.</span><span class="sxs-lookup"><span data-stu-id="d8428-208">If you do this, the array has the number of dimensions you specify, but it is uninitialized.</span></span> <span data-ttu-id="d8428-209">Il a la valeur `Nothing` jusqu'à ce que vous initialisez au moins certains de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="d8428-209">It has a value of `Nothing` until you initialize at least some of its elements.</span></span> <span data-ttu-id="d8428-210">La `Dim` instruction doit spécifier des limites pour toutes les dimensions ou pas de dimensions.</span><span class="sxs-lookup"><span data-stu-id="d8428-210">The `Dim` statement must specify bounds either for all dimensions or for no dimensions.</span></span>

```vb
' Declare an array with blank array bounds.
Dim messages() As String
' Initialize the array.
ReDim messages(4)
```

<span data-ttu-id="d8428-211">Si le tableau a plusieurs dimensions, vous devez inclure des virgules entre parenthèses pour indiquer le nombre de dimensions.</span><span class="sxs-lookup"><span data-stu-id="d8428-211">If the array has more than one dimension, you must include commas between the parentheses to indicate the number of dimensions.</span></span>

```vb
Dim oneDimension(), twoDimensions(,), threeDimensions(,,) As Byte
```

<span data-ttu-id="d8428-212">Vous pouvez déclarer un *tableau de longueur zéro* en déclarant une des dimensions du tableau-1.</span><span class="sxs-lookup"><span data-stu-id="d8428-212">You can declare a *zero-length array* by declaring one of the array's dimensions to be -1.</span></span> <span data-ttu-id="d8428-213">Une variable qui contient un tableau de longueur zéro n’a pas la valeur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="d8428-213">A variable that holds a zero-length array does not have the value `Nothing`.</span></span> <span data-ttu-id="d8428-214">Tableaux de longueur zéro sont requis par certaines fonctions du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="d8428-214">Zero-length arrays are required by certain common language runtime functions.</span></span> <span data-ttu-id="d8428-215">Si vous essayez d’accéder à un tel tableau, une exception runtime se produit.</span><span class="sxs-lookup"><span data-stu-id="d8428-215">If you try to access such an array, a runtime exception occurs.</span></span> <span data-ttu-id="d8428-216">Pour plus d’informations, consultez [tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-216">For more information, see [Arrays](../../../visual-basic/programming-guide/language-features/arrays/index.md).</span></span>

<span data-ttu-id="d8428-217">Vous pouvez initialiser les valeurs d’un tableau à l’aide d’un littéral de tableau.</span><span class="sxs-lookup"><span data-stu-id="d8428-217">You can initialize the values of an array by using an array literal.</span></span> <span data-ttu-id="d8428-218">Pour ce faire, entourent les valeurs d’initialisation entre accolades (`{}`).</span><span class="sxs-lookup"><span data-stu-id="d8428-218">To do this, surround the initialization values with braces (`{}`).</span></span>

```vb
Dim longArray() As Long = {0, 1, 2, 3}
```

<span data-ttu-id="d8428-219">Pour les tableaux multidimensionnels, l’initialisation de chaque dimension séparée est placée entre accolades dans la dimension externe.</span><span class="sxs-lookup"><span data-stu-id="d8428-219">For multidimensional arrays, the initialization for each separate dimension is enclosed in braces in the outer dimension.</span></span> <span data-ttu-id="d8428-220">Les éléments sont spécifiés dans l’ordre ligne-champ.</span><span class="sxs-lookup"><span data-stu-id="d8428-220">The elements are specified in row-major order.</span></span>

```vb
Dim twoDimensions(,) As Integer = {{0, 1, 2}, {10, 11, 12}}
```

<span data-ttu-id="d8428-221">Pour plus d’informations sur les littéraux de tableau, consultez [tableaux](../../../visual-basic/programming-guide/language-features/arrays/index.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-221">For more information about array literals, see [Arrays](../../../visual-basic/programming-guide/language-features/arrays/index.md).</span></span>

## <a name="default"></a> <span data-ttu-id="d8428-222">Valeurs et Types de données par défaut</span><span class="sxs-lookup"><span data-stu-id="d8428-222">Default Data Types and Values</span></span>

<span data-ttu-id="d8428-223">Le tableau suivant décrit les résultats des diverses combinaisons de spécification du type de données et d'un initialiseur dans une instruction `Dim`.</span><span class="sxs-lookup"><span data-stu-id="d8428-223">The following table describes the results of various combinations of specifying the data type and initializer in a `Dim` statement.</span></span>

|<span data-ttu-id="d8428-224">Type de données spécifié ?</span><span class="sxs-lookup"><span data-stu-id="d8428-224">Data type specified?</span></span>|<span data-ttu-id="d8428-225">Initialiseur spécifié ?</span><span class="sxs-lookup"><span data-stu-id="d8428-225">Initializer specified?</span></span>|<span data-ttu-id="d8428-226">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8428-226">Example</span></span>|<span data-ttu-id="d8428-227">Résultat</span><span class="sxs-lookup"><span data-stu-id="d8428-227">Result</span></span>|
|---|---|---|---|
|<span data-ttu-id="d8428-228">Non</span><span class="sxs-lookup"><span data-stu-id="d8428-228">No</span></span>|<span data-ttu-id="d8428-229">Non</span><span class="sxs-lookup"><span data-stu-id="d8428-229">No</span></span>|`Dim qty`|<span data-ttu-id="d8428-230">Si [Option Strict](../../../visual-basic/language-reference/statements/option-strict-statement.md) est désactivé (par défaut), la variable est définie sur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="d8428-230">If [Option Strict](../../../visual-basic/language-reference/statements/option-strict-statement.md) is off (the default), the variable is set to `Nothing`.</span></span><br /><br /> <span data-ttu-id="d8428-231">Si `Option Strict` est activé, une erreur se produit au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d8428-231">If `Option Strict` is on, a compile-time error occurs.</span></span>|
|<span data-ttu-id="d8428-232">Non</span><span class="sxs-lookup"><span data-stu-id="d8428-232">No</span></span>|<span data-ttu-id="d8428-233">Oui</span><span class="sxs-lookup"><span data-stu-id="d8428-233">Yes</span></span>|`Dim qty = 5`|<span data-ttu-id="d8428-234">Si [Option Infer](../../../visual-basic/language-reference/statements/option-infer-statement.md) est activée (valeur par défaut), type de la variable prend les données de l’initialiseur.</span><span class="sxs-lookup"><span data-stu-id="d8428-234">If [Option Infer](../../../visual-basic/language-reference/statements/option-infer-statement.md) is on (the default), the variable takes the data type of the initializer.</span></span> <span data-ttu-id="d8428-235">Consultez [inférence de Type Local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-235">See [Local Type Inference](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md).</span></span><br /><br /> <span data-ttu-id="d8428-236">Si `Option Infer` est désactivé et que `Option Strict` est désactivé, la variable prend le type de données de `Object`.</span><span class="sxs-lookup"><span data-stu-id="d8428-236">If `Option Infer` is off and `Option Strict` is off, the variable takes the data type of `Object`.</span></span><br /><br /> <span data-ttu-id="d8428-237">Si `Option Infer` est désactivé et que `Option Strict` est activé, une erreur se produit au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d8428-237">If `Option Infer` is off and `Option Strict` is on, a compile-time error occurs.</span></span>|
|<span data-ttu-id="d8428-238">Oui</span><span class="sxs-lookup"><span data-stu-id="d8428-238">Yes</span></span>|<span data-ttu-id="d8428-239">Non</span><span class="sxs-lookup"><span data-stu-id="d8428-239">No</span></span>|`Dim qty As Integer`|<span data-ttu-id="d8428-240">La variable est initialisée avec la valeur par défaut du type de données.</span><span class="sxs-lookup"><span data-stu-id="d8428-240">The variable is initialized to the default value for the data type.</span></span> <span data-ttu-id="d8428-241">Consultez le tableau plus loin dans cette section.</span><span class="sxs-lookup"><span data-stu-id="d8428-241">See the table later in this section.</span></span>|
|<span data-ttu-id="d8428-242">Oui</span><span class="sxs-lookup"><span data-stu-id="d8428-242">Yes</span></span>|<span data-ttu-id="d8428-243">Oui</span><span class="sxs-lookup"><span data-stu-id="d8428-243">Yes</span></span>|`Dim qty  As Integer = 5`|<span data-ttu-id="d8428-244">Si le type de données de l’initialiseur ne peut pas être converti dans le type de données spécifié, une erreur se produit au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="d8428-244">If the data type of the initializer is not convertible to the specified data type, a compile-time error occurs.</span></span>|

<span data-ttu-id="d8428-245">Si vous spécifiez un type de données mais que vous ne spécifiez pas un initialiseur, Visual Basic initialise la variable à la valeur par défaut pour son type de données.</span><span class="sxs-lookup"><span data-stu-id="d8428-245">If you specify a data type but do not specify an initializer, Visual Basic initializes the variable to the default value for its data type.</span></span> <span data-ttu-id="d8428-246">Le tableau suivant présente la valeur par défaut des valeurs d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="d8428-246">The following table shows the default initialization values.</span></span>

|<span data-ttu-id="d8428-247">Type de données</span><span class="sxs-lookup"><span data-stu-id="d8428-247">Data type</span></span>|<span data-ttu-id="d8428-248">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="d8428-248">Default value</span></span>|
|---|---|
|<span data-ttu-id="d8428-249">Tous les types numériques (y compris `Byte` et `SByte`)</span><span class="sxs-lookup"><span data-stu-id="d8428-249">All numeric types (including `Byte` and `SByte`)</span></span>|<span data-ttu-id="d8428-250">0</span><span class="sxs-lookup"><span data-stu-id="d8428-250">0</span></span>|
|`Char`|<span data-ttu-id="d8428-251">0 (binaire)</span><span class="sxs-lookup"><span data-stu-id="d8428-251">Binary 0</span></span>|
|<span data-ttu-id="d8428-252">Tous les types référence (y compris `Object`, `String`et tous les tableaux)</span><span class="sxs-lookup"><span data-stu-id="d8428-252">All reference types (including `Object`, `String`, and all arrays)</span></span>|`Nothing`|
|`Boolean`|`False`|
|`Date`|<span data-ttu-id="d8428-253">12 h 00 le 1er janvier de l’année 1 (01/01/0001 12:00:00 AM)</span><span class="sxs-lookup"><span data-stu-id="d8428-253">12:00 AM of January 1 of the year 1 (01/01/0001 12:00:00 AM)</span></span>|

<span data-ttu-id="d8428-254">Chaque élément d’une structure est initialisé comme s’il s’agissait d’une variable distincte.</span><span class="sxs-lookup"><span data-stu-id="d8428-254">Each element of a structure is initialized as if it were a separate variable.</span></span> <span data-ttu-id="d8428-255">Si vous déclarez la longueur d’un tableau, mais ne pas initialisez ses éléments, chaque élément est initialisé comme s’il s’agissait d’une variable distincte.</span><span class="sxs-lookup"><span data-stu-id="d8428-255">If you declare the length of an array but do not initialize its elements, each element is initialized as if it were a separate variable.</span></span>

## <a name="static-local-variable-lifetime"></a><span data-ttu-id="d8428-256">Durée de vie Variable locale statique</span><span class="sxs-lookup"><span data-stu-id="d8428-256">Static Local Variable Lifetime</span></span>

<span data-ttu-id="d8428-257">A `Static` variable locale a une durée de vie plus longue que celle de la procédure dans laquelle elle est déclarée.</span><span class="sxs-lookup"><span data-stu-id="d8428-257">A `Static` local variable has a longer lifetime than that of the procedure in which it is declared.</span></span> <span data-ttu-id="d8428-258">Les limites de durée de vie de la variable dépendent où la procédure est déclarée et qu’il s’agisse `Shared`.</span><span class="sxs-lookup"><span data-stu-id="d8428-258">The boundaries of the variable's lifetime depend on where the procedure is declared and whether it is `Shared`.</span></span>

|<span data-ttu-id="d8428-259">Déclaration de procédure</span><span class="sxs-lookup"><span data-stu-id="d8428-259">Procedure declaration</span></span>|<span data-ttu-id="d8428-260">Variable initialisée</span><span class="sxs-lookup"><span data-stu-id="d8428-260">Variable initialized</span></span>|<span data-ttu-id="d8428-261">Variable n’existe plus.</span><span class="sxs-lookup"><span data-stu-id="d8428-261">Variable stops existing</span></span>|
|---|---|---|
|<span data-ttu-id="d8428-262">Dans un module</span><span class="sxs-lookup"><span data-stu-id="d8428-262">In a module</span></span>|<span data-ttu-id="d8428-263">La première fois que la procédure est appelée.</span><span class="sxs-lookup"><span data-stu-id="d8428-263">The first time the procedure is called</span></span>|<span data-ttu-id="d8428-264">Lorsque votre programme s’arrête l’exécution</span><span class="sxs-lookup"><span data-stu-id="d8428-264">When your program stops execution</span></span>|
|<span data-ttu-id="d8428-265">Dans une classe ou une structure, la procédure est `Shared`</span><span class="sxs-lookup"><span data-stu-id="d8428-265">In a class or structure, procedure is `Shared`</span></span>|<span data-ttu-id="d8428-266">La première fois que la procédure est appelée sur une instance spécifique ou sur la classe ou la structure elle-même</span><span class="sxs-lookup"><span data-stu-id="d8428-266">The first time the procedure is called either on a specific instance or on the class or structure itself</span></span>|<span data-ttu-id="d8428-267">Lorsque votre programme s’arrête l’exécution</span><span class="sxs-lookup"><span data-stu-id="d8428-267">When your program stops execution</span></span>|
|<span data-ttu-id="d8428-268">Dans une classe ou une structure, la procédure n’est pas `Shared`</span><span class="sxs-lookup"><span data-stu-id="d8428-268">In a class or structure, procedure isn't `Shared`</span></span>|<span data-ttu-id="d8428-269">La première fois que la procédure est appelée sur une instance spécifique</span><span class="sxs-lookup"><span data-stu-id="d8428-269">The first time the procedure is called on a specific instance</span></span>|<span data-ttu-id="d8428-270">Lorsque l’instance est libérée pour le garbage collection (GC)</span><span class="sxs-lookup"><span data-stu-id="d8428-270">When the instance is released for garbage collection (GC)</span></span>|

## <a name="attributes-and-modifiers"></a><span data-ttu-id="d8428-271">Attributs et modificateurs</span><span class="sxs-lookup"><span data-stu-id="d8428-271">Attributes and Modifiers</span></span>

<span data-ttu-id="d8428-272">Vous pouvez appliquer des attributs qu’aux variables de membre, et non aux variables locales.</span><span class="sxs-lookup"><span data-stu-id="d8428-272">You can apply attributes only to member variables, not to local variables.</span></span> <span data-ttu-id="d8428-273">Un attribut fournit des informations aux métadonnées de l’assembly qui n’est pas significatif pour le stockage temporaire tel que des variables locales.</span><span class="sxs-lookup"><span data-stu-id="d8428-273">An attribute contributes information to the assembly's metadata, which is not meaningful for temporary storage such as local variables.</span></span>

<span data-ttu-id="d8428-274">Au niveau du module, vous ne pouvez pas utiliser le `Static` modificateur pour déclarer des variables de membre.</span><span class="sxs-lookup"><span data-stu-id="d8428-274">At module level, you cannot use the `Static` modifier to declare member variables.</span></span> <span data-ttu-id="d8428-275">Au niveau de la procédure, vous ne pouvez pas utiliser `Shared`, `Shadows`, `ReadOnly`, `WithEvents`, ou un modificateur d’accès pour déclarer des variables locales.</span><span class="sxs-lookup"><span data-stu-id="d8428-275">At procedure level, you cannot use `Shared`, `Shadows`, `ReadOnly`, `WithEvents`, or any access modifiers to declare local variables.</span></span>

<span data-ttu-id="d8428-276">Vous pouvez spécifier le code peut accéder à une variable en fournissant un `accessmodifier`.</span><span class="sxs-lookup"><span data-stu-id="d8428-276">You can specify what code can access a variable by supplying an `accessmodifier`.</span></span> <span data-ttu-id="d8428-277">Classe et le module membre variables (en dehors de toute procédure) par défaut d’un accès privé et par défaut de variables de membre structure d’un accès public.</span><span class="sxs-lookup"><span data-stu-id="d8428-277">Class and module member variables (outside any procedure) default to private access, and structure member variables default to public access.</span></span> <span data-ttu-id="d8428-278">Vous pouvez ajuster leurs niveaux d’accès avec les modificateurs d’accès.</span><span class="sxs-lookup"><span data-stu-id="d8428-278">You can adjust their access levels with the access modifiers.</span></span> <span data-ttu-id="d8428-279">Vous ne pouvez pas utiliser les modificateurs d’accès sur les variables locales (à l’intérieur d’une procédure).</span><span class="sxs-lookup"><span data-stu-id="d8428-279">You cannot use access modifiers on local variables (inside a procedure).</span></span>

<span data-ttu-id="d8428-280">Vous pouvez spécifier `WithEvents` uniquement sur des variables de membre, et non sur les variables locales à l’intérieur d’une procédure.</span><span class="sxs-lookup"><span data-stu-id="d8428-280">You can specify `WithEvents` only on member variables, not on local variables inside a procedure.</span></span> <span data-ttu-id="d8428-281">Si vous spécifiez `WithEvents`, le type de données de la variable doit être un type class spécifique, pas `Object`.</span><span class="sxs-lookup"><span data-stu-id="d8428-281">If you specify `WithEvents`, the data type of the variable must be a specific class type, not `Object`.</span></span> <span data-ttu-id="d8428-282">Vous ne pouvez pas déclarer un tableau avec `WithEvents`.</span><span class="sxs-lookup"><span data-stu-id="d8428-282">You cannot declare an array with `WithEvents`.</span></span> <span data-ttu-id="d8428-283">Pour plus d’informations sur les événements, consultez [événements](../../../visual-basic/programming-guide/language-features/events/index.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-283">For more information about events, see [Events](../../../visual-basic/programming-guide/language-features/events/index.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d8428-284">Code en dehors d’une classe, structure ou module doit qualifier le nom d’une variable membre avec le nom de cette classe, une structure ou un module.</span><span class="sxs-lookup"><span data-stu-id="d8428-284">Code outside a class, structure, or module must qualify a member variable's name with the name of that class, structure, or module.</span></span> <span data-ttu-id="d8428-285">Code en dehors de qu'une procédure ou un bloc ne peut pas faire référence à des variables locales de cette procédure ou un bloc.</span><span class="sxs-lookup"><span data-stu-id="d8428-285">Code outside a procedure or block cannot refer to any local variables within that procedure or block.</span></span>

## <a name="releasing-managed-resources"></a><span data-ttu-id="d8428-286">Libération des ressources managées</span><span class="sxs-lookup"><span data-stu-id="d8428-286">Releasing Managed Resources</span></span>

<span data-ttu-id="d8428-287">Le garbage collector .NET Framework supprime les ressources managées sans codage supplémentaire de votre part.</span><span class="sxs-lookup"><span data-stu-id="d8428-287">The .NET Framework garbage collector disposes of managed resources without any extra coding on your part.</span></span> <span data-ttu-id="d8428-288">Toutefois, vous pouvez forcer la suppression d’une ressource managée au lieu d’attendre le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="d8428-288">However, you can force the disposal of a managed resource instead of waiting for the garbage collector.</span></span>

<span data-ttu-id="d8428-289">Si une classe conserve une ressource particulièrement précieuse et rare (par exemple, un handle de connexion ou un fichier de base de données), il pourrez vous ne souhaitez pas attendre le prochain garbage collection pour nettoyer une instance de classe qui n’est plus en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="d8428-289">If a class holds onto a particularly valuable and scarce resource (such as a database connection or file handle), you might not want to wait until the next garbage collection to clean up a class instance that's no longer in use.</span></span> <span data-ttu-id="d8428-290">Une classe peut implémenter la <xref:System.IDisposable> interface afin de fournir un moyen pour libérer les ressources avant un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d8428-290">A class may implement the <xref:System.IDisposable> interface to provide a way to release resources before a garbage collection.</span></span> <span data-ttu-id="d8428-291">Une classe qui implémente cette interface expose un `Dispose` méthode qui peut être appelée pour forcer à libérer immédiatement des ressources intéressantes.</span><span class="sxs-lookup"><span data-stu-id="d8428-291">A class that implements that interface exposes a `Dispose` method that can be called to force valuable resources to be released immediately.</span></span>

<span data-ttu-id="d8428-292">La `Using` instruction automatise le processus d’acquisition d’une ressource, l’exécution d’un ensemble d’instructions, puis supprimez-le de la ressource.</span><span class="sxs-lookup"><span data-stu-id="d8428-292">The `Using` statement automates the process of acquiring a resource, executing a set of statements, and then disposing of the resource.</span></span> <span data-ttu-id="d8428-293">Toutefois, la ressource doit implémenter le <xref:System.IDisposable> interface.</span><span class="sxs-lookup"><span data-stu-id="d8428-293">However, the resource must implement the <xref:System.IDisposable> interface.</span></span> <span data-ttu-id="d8428-294">Pour plus d’informations, consultez [using, instruction](../../../visual-basic/language-reference/statements/using-statement.md).</span><span class="sxs-lookup"><span data-stu-id="d8428-294">For more information, see [Using Statement](../../../visual-basic/language-reference/statements/using-statement.md).</span></span>

## <a name="example"></a><span data-ttu-id="d8428-295">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8428-295">Example</span></span>

<span data-ttu-id="d8428-296">L’exemple suivant déclare les variables à l’aide de la `Dim` instruction avec diverses options.</span><span class="sxs-lookup"><span data-stu-id="d8428-296">The following example declares variables by using the `Dim` statement with various options.</span></span>

[!code-vb[VbVbalrStatements#141](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class11.vb#141)]

## <a name="example"></a><span data-ttu-id="d8428-297">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8428-297">Example</span></span>

<span data-ttu-id="d8428-298">L’exemple suivant répertorie les nombres premiers entre 1 et 30.</span><span class="sxs-lookup"><span data-stu-id="d8428-298">The following example lists the prime numbers between 1 and 30.</span></span> <span data-ttu-id="d8428-299">La portée des variables locales est décrite dans les commentaires de code.</span><span class="sxs-lookup"><span data-stu-id="d8428-299">The scope of local variables is described in code comments.</span></span>

[!code-vb[VbVbalrStatements#142](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class11.vb#142)]

## <a name="example"></a><span data-ttu-id="d8428-300">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8428-300">Example</span></span>

<span data-ttu-id="d8428-301">Dans l’exemple suivant, le `speedValue` variable est déclarée au niveau de la classe.</span><span class="sxs-lookup"><span data-stu-id="d8428-301">In the following example, the `speedValue` variable is declared at the class level.</span></span> <span data-ttu-id="d8428-302">Le `Private` mot clé est utilisé pour déclarer la variable.</span><span class="sxs-lookup"><span data-stu-id="d8428-302">The `Private` keyword is used to declare the variable.</span></span> <span data-ttu-id="d8428-303">La variable est accessible par n’importe quelle procédure dans le `Car` classe.</span><span class="sxs-lookup"><span data-stu-id="d8428-303">The variable can be accessed by any procedure in the `Car` class.</span></span>

[!code-vb[VbVbalrStatements#144](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class11.vb#144)]

[!code-vb[VbVbalrStatements#145](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/class11.vb#145)]

## <a name="see-also"></a><span data-ttu-id="d8428-304">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8428-304">See also</span></span>

- [<span data-ttu-id="d8428-305">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="d8428-305">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)
- [<span data-ttu-id="d8428-306">ReDim (instruction)</span><span class="sxs-lookup"><span data-stu-id="d8428-306">ReDim Statement</span></span>](../../../visual-basic/language-reference/statements/redim-statement.md)
- [<span data-ttu-id="d8428-307">Option Explicit (instruction)</span><span class="sxs-lookup"><span data-stu-id="d8428-307">Option Explicit Statement</span></span>](../../../visual-basic/language-reference/statements/option-explicit-statement.md)
- [<span data-ttu-id="d8428-308">Option Infer (instruction)</span><span class="sxs-lookup"><span data-stu-id="d8428-308">Option Infer Statement</span></span>](../../../visual-basic/language-reference/statements/option-infer-statement.md)
- [<span data-ttu-id="d8428-309">Option Strict (instruction)</span><span class="sxs-lookup"><span data-stu-id="d8428-309">Option Strict Statement</span></span>](../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [<span data-ttu-id="d8428-310">Page Compiler, Concepteur de projet (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8428-310">Compile Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/compile-page-project-designer-visual-basic)
- [<span data-ttu-id="d8428-311">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="d8428-311">Variable Declaration</span></span>](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="d8428-312">Tableaux</span><span class="sxs-lookup"><span data-stu-id="d8428-312">Arrays</span></span>](../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [<span data-ttu-id="d8428-313">Initialiseurs d’objets : Types nommés et anonymes</span><span class="sxs-lookup"><span data-stu-id="d8428-313">Object Initializers: Named and Anonymous Types</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)
- [<span data-ttu-id="d8428-314">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="d8428-314">Anonymous Types</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/anonymous-types.md)
- [<span data-ttu-id="d8428-315">Initialiseurs d’objets : Types nommés et anonymes</span><span class="sxs-lookup"><span data-stu-id="d8428-315">Object Initializers: Named and Anonymous Types</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/object-initializers-named-and-anonymous-types.md)
- [<span data-ttu-id="d8428-316">Guide pratique pour Déclarez un objet à l’aide d’un initialiseur d’objet</span><span class="sxs-lookup"><span data-stu-id="d8428-316">How to: Declare an Object by Using an Object Initializer</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/how-to-declare-an-object-by-using-an-object-initializer.md)
- [<span data-ttu-id="d8428-317">Inférence de type local</span><span class="sxs-lookup"><span data-stu-id="d8428-317">Local Type Inference</span></span>](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
