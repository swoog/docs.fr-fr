---
title: Enum, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Enum
helpviewer_keywords:
- enumerated constants [Visual Basic]
- Enum statement [Visual Basic]
- Private keyword [Visual Basic], Enum statements
- Public keyword [Visual Basic], in Enum statement
- variables [Visual Basic], enumeration
- constants [Visual Basic], enumerated
ms.assetid: a45e51f1-65ff-48e1-bf32-79130f137377
ms.openlocfilehash: 0a761c39b51a8d71919a84cbbbf6739fc1f5bcea
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64754618"
---
# <a name="enum-statement-visual-basic"></a><span data-ttu-id="30632-102">Enum, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="30632-102">Enum Statement (Visual Basic)</span></span>

<span data-ttu-id="30632-103">Déclare une énumération et définit les valeurs de ses membres.</span><span class="sxs-lookup"><span data-stu-id="30632-103">Declares an enumeration and defines the values of its members.</span></span>

## <a name="syntax"></a><span data-ttu-id="30632-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30632-104">Syntax</span></span>

```
[ <attributelist> ] [ accessmodifier ]  [ Shadows ]
Enum enumerationname [ As datatype ]
   memberlist
End Enum
```

## <a name="parts"></a><span data-ttu-id="30632-105">Composants</span><span class="sxs-lookup"><span data-stu-id="30632-105">Parts</span></span>

- `attributelist`

  <span data-ttu-id="30632-106">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="30632-106">Optional.</span></span> <span data-ttu-id="30632-107">Liste des attributs qui s’appliquent à cette énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-107">List of attributes that apply to this enumeration.</span></span> <span data-ttu-id="30632-108">Vous devez placer le [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md) figurant entre crochets («`<`« et »`>`»).</span><span class="sxs-lookup"><span data-stu-id="30632-108">You must enclose the [attribute list](../../../visual-basic/language-reference/statements/attribute-list.md) in angle brackets ("`<`" and "`>`").</span></span>

  <span data-ttu-id="30632-109">Le <xref:System.FlagsAttribute> attribut indique que la valeur d’une instance de l’énumération peut inclure plusieurs membres de l’énumération, et que chaque membre représente un champ de bits dans la valeur d’énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-109">The <xref:System.FlagsAttribute> attribute indicates that the value of an instance of the enumeration can include multiple enumeration members, and that each member represents a bit field in the enumeration value.</span></span>

- `accessmodifier`

  <span data-ttu-id="30632-110">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="30632-110">Optional.</span></span> <span data-ttu-id="30632-111">Spécifie le code peut accéder à cette énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-111">Specifies what code can access this enumeration.</span></span> <span data-ttu-id="30632-112">Il peut s'agir d'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="30632-112">Can be one of the following:</span></span>

  - [<span data-ttu-id="30632-113">Public</span><span class="sxs-lookup"><span data-stu-id="30632-113">Public</span></span>](../../../visual-basic/language-reference/modifiers/public.md)

  - [<span data-ttu-id="30632-114">Protected</span><span class="sxs-lookup"><span data-stu-id="30632-114">Protected</span></span>](../../../visual-basic/language-reference/modifiers/protected.md)

  - [<span data-ttu-id="30632-115">Friend</span><span class="sxs-lookup"><span data-stu-id="30632-115">Friend</span></span>](../../../visual-basic/language-reference/modifiers/friend.md)

  - [<span data-ttu-id="30632-116">Private</span><span class="sxs-lookup"><span data-stu-id="30632-116">Private</span></span>](../../../visual-basic/language-reference/modifiers/private.md)

  - [<span data-ttu-id="30632-117">Protected Friend</span><span class="sxs-lookup"><span data-stu-id="30632-117">Protected Friend</span></span>](../../language-reference/modifiers/protected-friend.md)

  - [<span data-ttu-id="30632-118">Private Protected</span><span class="sxs-lookup"><span data-stu-id="30632-118">Private Protected</span></span>](../../language-reference/modifiers/private-protected.md)

- `Shadows`

  <span data-ttu-id="30632-119">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="30632-119">Optional.</span></span> <span data-ttu-id="30632-120">Spécifie que cette énumération redéclare et masque un élément de programmation portant le même nom ou un ensemble d’éléments surchargés, dans une classe de base.</span><span class="sxs-lookup"><span data-stu-id="30632-120">Specifies that this enumeration redeclares and hides an identically named programming element, or set of overloaded elements, in a base class.</span></span> <span data-ttu-id="30632-121">Vous pouvez spécifier [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md) uniquement sur l’énumération elle-même, et non sur un de ses membres.</span><span class="sxs-lookup"><span data-stu-id="30632-121">You can specify [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md) only on the enumeration itself, not on any of its members.</span></span>

- `enumerationname`

  <span data-ttu-id="30632-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="30632-122">Required.</span></span> <span data-ttu-id="30632-123">Nom de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-123">Name of the enumeration.</span></span> <span data-ttu-id="30632-124">Pour plus d’informations sur les noms valides, consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span><span class="sxs-lookup"><span data-stu-id="30632-124">For information on valid names, see [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).</span></span>

- `datatype`

  <span data-ttu-id="30632-125">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="30632-125">Optional.</span></span> <span data-ttu-id="30632-126">Type de données de l’énumération et tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="30632-126">Data type of the enumeration and all its members.</span></span>

- `memberlist`

  <span data-ttu-id="30632-127">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="30632-127">Required.</span></span> <span data-ttu-id="30632-128">Liste de constantes de membres déclarées dans cette instruction.</span><span class="sxs-lookup"><span data-stu-id="30632-128">List of member constants being declared in this statement.</span></span> <span data-ttu-id="30632-129">Plusieurs membres apparaissent sur les lignes de code source individuel.</span><span class="sxs-lookup"><span data-stu-id="30632-129">Multiple members appear on individual source code lines.</span></span>

  <span data-ttu-id="30632-130">Chaque `member` a la syntaxe et les éléments suivants : `[<attribute list>] member name [ = initializer ]`</span><span class="sxs-lookup"><span data-stu-id="30632-130">Each `member` has the following syntax and parts: `[<attribute list>] member name [ = initializer ]`</span></span>

  |<span data-ttu-id="30632-131">Élément</span><span class="sxs-lookup"><span data-stu-id="30632-131">Part</span></span>|<span data-ttu-id="30632-132">Description</span><span class="sxs-lookup"><span data-stu-id="30632-132">Description</span></span>|
  |---|---|
  |`membername`|<span data-ttu-id="30632-133">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="30632-133">Required.</span></span> <span data-ttu-id="30632-134">Nom de ce membre.</span><span class="sxs-lookup"><span data-stu-id="30632-134">Name of this member.</span></span>|
  |`initializer`|<span data-ttu-id="30632-135">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="30632-135">Optional.</span></span> <span data-ttu-id="30632-136">Expression qui est évaluée au moment de la compilation et assignée à ce membre.</span><span class="sxs-lookup"><span data-stu-id="30632-136">Expression that is evaluated at compile time and assigned to this member.</span></span>|

- <span data-ttu-id="30632-137">`End` `Enum`</span><span class="sxs-lookup"><span data-stu-id="30632-137">`End` `Enum`</span></span>

  <span data-ttu-id="30632-138">Met fin au bloc `Enum`.</span><span class="sxs-lookup"><span data-stu-id="30632-138">Terminates the `Enum` block.</span></span>

## <a name="remarks"></a><span data-ttu-id="30632-139">Notes</span><span class="sxs-lookup"><span data-stu-id="30632-139">Remarks</span></span>

<span data-ttu-id="30632-140">Si vous avez un ensemble de valeurs immuables qui sont liés logiquement entre eux, vous pouvez les définir ensemble dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-140">If you have a set of unchanging values that are logically related to each other, you can define them together in an enumeration.</span></span> <span data-ttu-id="30632-141">Cela fournit des noms explicites pour l’énumération et ses membres, qui sont plus faciles à retenir que leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="30632-141">This provides meaningful names for the enumeration and its members, which are easier to remember than their values.</span></span> <span data-ttu-id="30632-142">Vous pouvez ensuite utiliser les membres d’énumération à de nombreux endroits dans votre code.</span><span class="sxs-lookup"><span data-stu-id="30632-142">You can then use the enumeration members in many places in your code.</span></span>

<span data-ttu-id="30632-143">Les avantages de l’aide des énumérations sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="30632-143">The benefits of using enumerations include the following:</span></span>

- <span data-ttu-id="30632-144">Réduit les erreurs provoquées par transposant ou entrée incorrecte de nombres.</span><span class="sxs-lookup"><span data-stu-id="30632-144">Reduces errors caused by transposing or mistyping numbers.</span></span>

- <span data-ttu-id="30632-145">Rend plus facile de modifier les valeurs à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="30632-145">Makes it easy to change values in the future.</span></span>

- <span data-ttu-id="30632-146">Rend le code plus facile à lire, ce qui signifie qu’il est moins probable que les erreurs seront présentées.</span><span class="sxs-lookup"><span data-stu-id="30632-146">Makes code easier to read, which means it is less likely that errors will be introduced.</span></span>

- <span data-ttu-id="30632-147">Garantit la compatibilité ascendante.</span><span class="sxs-lookup"><span data-stu-id="30632-147">Ensures forward compatibility.</span></span> <span data-ttu-id="30632-148">Si vous utilisez des énumérations, votre code est moins susceptible d’échouer si à l’avenir quelqu'un modifie les valeurs correspondant aux noms de membre.</span><span class="sxs-lookup"><span data-stu-id="30632-148">If you use enumerations, your code is less likely to fail if in the future someone changes the values corresponding to the member names.</span></span>

<span data-ttu-id="30632-149">Une énumération a un nom, un type de données sous-jacent et un jeu de membres.</span><span class="sxs-lookup"><span data-stu-id="30632-149">An enumeration has a name, an underlying data type, and a set of members.</span></span> <span data-ttu-id="30632-150">Chaque membre représente une constante.</span><span class="sxs-lookup"><span data-stu-id="30632-150">Each member represents a constant.</span></span>

<span data-ttu-id="30632-151">Une énumération déclarée au niveau de la classe, structure, module ou niveau de l’interface, en dehors de toute procédure, est un *énumération membre*.</span><span class="sxs-lookup"><span data-stu-id="30632-151">An enumeration declared at class, structure, module, or interface level, outside any procedure, is a *member enumeration*.</span></span> <span data-ttu-id="30632-152">Il est membre de la classe, une structure, un module ou une interface qui le déclare.</span><span class="sxs-lookup"><span data-stu-id="30632-152">It is a member of the class, structure, module, or interface that declares it.</span></span>

<span data-ttu-id="30632-153">Les énumérations de membres accessibles à partir de n’importe où au sein de leur classe, une structure, un module ou une interface.</span><span class="sxs-lookup"><span data-stu-id="30632-153">Member enumerations can be accessed from anywhere within their class, structure, module, or interface.</span></span> <span data-ttu-id="30632-154">Code en dehors d’une classe, d’une structure ou un module doit qualifier le nom d’une énumération de membre avec le nom de cette classe, une structure ou un module.</span><span class="sxs-lookup"><span data-stu-id="30632-154">Code outside a class, structure, or module must qualify a member enumeration's name with the name of that class, structure, or module.</span></span> <span data-ttu-id="30632-155">Vous pouvez éviter la nécessité d’utiliser des noms qualifiés complets en ajoutant un [importations](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) instruction dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="30632-155">You can avoid the need to use fully qualified names by adding an [Imports](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md) statement to the source file.</span></span>

<span data-ttu-id="30632-156">Une énumération déclarée au niveau de l’espace de noms, en dehors de toute classe, une structure, un module ou une interface, est un membre de l’espace de noms dans lequel elle apparaît.</span><span class="sxs-lookup"><span data-stu-id="30632-156">An enumeration declared at namespace level, outside any class, structure, module, or interface, is a member of the namespace in which it appears.</span></span>

<span data-ttu-id="30632-157">Le *contexte de déclaration* pour une énumération doit être un fichier source, espace de noms, classe, structure, module ou interface et ne peut pas être une procédure.</span><span class="sxs-lookup"><span data-stu-id="30632-157">The *declaration context* for an enumeration must be a source file, namespace, class, structure, module, or interface, and cannot be a procedure.</span></span> <span data-ttu-id="30632-158">Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="30632-158">For more information, see [Declaration Contexts and Default Access Levels](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).</span></span>

<span data-ttu-id="30632-159">Vous pouvez appliquer des attributs à une énumération dans sa globalité, mais pas à ses membres individuellement.</span><span class="sxs-lookup"><span data-stu-id="30632-159">You can apply attributes to an enumeration as a whole, but not to its members individually.</span></span> <span data-ttu-id="30632-160">Un attribut fournit des informations aux métadonnées de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="30632-160">An attribute contributes information to the assembly's metadata.</span></span>

## <a name="data-type"></a><span data-ttu-id="30632-161">Type de données</span><span class="sxs-lookup"><span data-stu-id="30632-161">Data Type</span></span>

<span data-ttu-id="30632-162">La `Enum` instruction peut déclarer le type de données d’une énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-162">The `Enum` statement can declare the data type of an enumeration.</span></span> <span data-ttu-id="30632-163">Chaque membre prend le type de données de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-163">Each member takes the enumeration's data type.</span></span> <span data-ttu-id="30632-164">Vous pouvez spécifier `Byte`, `Integer`, `Long`, `SByte`, `Short`, `UInteger`, `ULong`, ou `UShort`.</span><span class="sxs-lookup"><span data-stu-id="30632-164">You can specify `Byte`, `Integer`, `Long`, `SByte`, `Short`, `UInteger`, `ULong`, or `UShort`.</span></span>

<span data-ttu-id="30632-165">Si vous ne spécifiez pas `datatype` pour l’énumération, chaque membre prend le type de données de ses `initializer`.</span><span class="sxs-lookup"><span data-stu-id="30632-165">If you do not specify `datatype` for the enumeration, each member takes the data type of its `initializer`.</span></span> <span data-ttu-id="30632-166">Si vous spécifiez à la fois `datatype` et `initializer`, le type de données de `initializer` doit être convertible en `datatype`.</span><span class="sxs-lookup"><span data-stu-id="30632-166">If you specify both `datatype` and `initializer`, the data type of `initializer` must be convertible to `datatype`.</span></span> <span data-ttu-id="30632-167">Si ni `datatype` ni `initializer` est présent, le type de données par défaut, `Integer`.</span><span class="sxs-lookup"><span data-stu-id="30632-167">If neither `datatype` nor `initializer` is present, the data type defaults to `Integer`.</span></span>

## <a name="initializing-members"></a><span data-ttu-id="30632-168">L’initialisation des membres</span><span class="sxs-lookup"><span data-stu-id="30632-168">Initializing Members</span></span>

<span data-ttu-id="30632-169">Le `Enum` instruction peut initialiser le contenu de membres sélectionnés dans `memberlist`.</span><span class="sxs-lookup"><span data-stu-id="30632-169">The `Enum` statement can initialize the contents of selected members in `memberlist`.</span></span> <span data-ttu-id="30632-170">Vous utilisez `initializer` pour fournir une expression à assigner au membre.</span><span class="sxs-lookup"><span data-stu-id="30632-170">You use `initializer` to supply an expression to be assigned to the member.</span></span>

<span data-ttu-id="30632-171">Si vous ne spécifiez pas `initializer` pour un membre, Visual Basic initialise soit à zéro (s’il s’agit de la première `member` dans `memberlist`), ou une valeur supérieure d’une unité à celle de la précédant immédiatement `member`.</span><span class="sxs-lookup"><span data-stu-id="30632-171">If you do not specify `initializer` for a member, Visual Basic initializes it either to zero (if it is the first `member` in `memberlist`), or to a value greater by one than that of the immediately preceding `member`.</span></span>

<span data-ttu-id="30632-172">L’expression fournie dans chaque `initializer` peut être n’importe quelle combinaison de littéraux, les autres constantes qui sont déjà définies et les membres de l’énumération qui sont déjà définies, y compris un membre précédent de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-172">The expression supplied in each `initializer` can be any combination of literals, other constants that are already defined, and enumeration members that are already defined, including a previous member of this enumeration.</span></span> <span data-ttu-id="30632-173">Vous pouvez utiliser des opérateurs arithmétiques et logiques pour combiner ces éléments.</span><span class="sxs-lookup"><span data-stu-id="30632-173">You can use arithmetic and logical operators to combine such elements.</span></span>

<span data-ttu-id="30632-174">Vous ne pouvez pas utiliser des variables ou des fonctions dans `initializer`.</span><span class="sxs-lookup"><span data-stu-id="30632-174">You cannot use variables or functions in `initializer`.</span></span> <span data-ttu-id="30632-175">Toutefois, vous pouvez utiliser des mots clés de conversion comme `CByte` et `CShort`.</span><span class="sxs-lookup"><span data-stu-id="30632-175">However, you can use conversion keywords such as `CByte` and `CShort`.</span></span> <span data-ttu-id="30632-176">Vous pouvez également utiliser `AscW` si vous l’appelez avec une constante `String` ou `Char` argument, étant donné que qui peut être évaluée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="30632-176">You can also use `AscW` if you call it with a constant `String` or `Char` argument, since that can be evaluated at compile time.</span></span>

<span data-ttu-id="30632-177">Les énumérations ne peuvent pas avoir de valeurs à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="30632-177">Enumerations cannot have floating-point values.</span></span> <span data-ttu-id="30632-178">Si un membre est affecté une valeur à virgule flottante et `Option Strict` est la valeur on, une erreur du compilateur se produit.</span><span class="sxs-lookup"><span data-stu-id="30632-178">If a member is assigned a floating-point value and `Option Strict` is set to on, a compiler error occurs.</span></span> <span data-ttu-id="30632-179">Si `Option Strict` est désactivée, la valeur est automatiquement convertie en la `Enum` type.</span><span class="sxs-lookup"><span data-stu-id="30632-179">If `Option Strict` is off, the value is automatically converted to the `Enum` type.</span></span>

<span data-ttu-id="30632-180">Si la valeur d’un membre dépasse la plage autorisée pour le type de données sous-jacent, ou si vous initialisez un membre à la valeur maximale autorisée par le type de données sous-jacent, le compilateur signale une erreur.</span><span class="sxs-lookup"><span data-stu-id="30632-180">If the value of a member exceeds the allowable range for the underlying data type, or if you initialize any member to the maximum value allowed by the underlying data type, the compiler reports an error.</span></span>

## <a name="modifiers"></a><span data-ttu-id="30632-181">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="30632-181">Modifiers</span></span>

<span data-ttu-id="30632-182">Classe, structure, module et interface membres énumérations par défaut d’un accès public.</span><span class="sxs-lookup"><span data-stu-id="30632-182">Class, structure, module, and interface member enumerations default to public access.</span></span> <span data-ttu-id="30632-183">Vous pouvez ajuster leurs niveaux d’accès avec les modificateurs d’accès.</span><span class="sxs-lookup"><span data-stu-id="30632-183">You can adjust their access levels with the access modifiers.</span></span> <span data-ttu-id="30632-184">Namespace membre énumérations par défaut d’un accès ami.</span><span class="sxs-lookup"><span data-stu-id="30632-184">Namespace member enumerations default to friend access.</span></span> <span data-ttu-id="30632-185">Vous pouvez ajuster leurs niveaux d’accès public, mais pas pour privé ou protégé.</span><span class="sxs-lookup"><span data-stu-id="30632-185">You can adjust their access levels to public, but not to private or protected.</span></span> <span data-ttu-id="30632-186">Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="30632-186">For more information, see [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>

<span data-ttu-id="30632-187">Tous les membres d’énumération ont un accès public, et vous ne pouvez pas utiliser les modificateurs d’accès sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="30632-187">All enumeration members have public access, and you cannot use any access modifiers on them.</span></span> <span data-ttu-id="30632-188">Toutefois, si l’énumération elle-même a un niveau d’accès plus restreint, le niveau d’accès spécifié d’énumération est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="30632-188">However, if the enumeration itself has a more restricted access level, the specified enumeration access level takes precedence.</span></span>

<span data-ttu-id="30632-189">Par défaut, toutes les énumérations sont des types et leurs champs sont des constantes.</span><span class="sxs-lookup"><span data-stu-id="30632-189">By default, all enumerations are types and their fields are constants.</span></span> <span data-ttu-id="30632-190">Par conséquent le `Shared`, `Static`, et `ReadOnly` mots clés ne peut pas être utilisés pour déclarer une énumération ou ses membres.</span><span class="sxs-lookup"><span data-stu-id="30632-190">Therefore the `Shared`, `Static`, and `ReadOnly` keywords cannot be used when declaring an enumeration or its members.</span></span>

## <a name="assigning-multiple-values"></a><span data-ttu-id="30632-191">Affectation de plusieurs valeurs</span><span class="sxs-lookup"><span data-stu-id="30632-191">Assigning Multiple Values</span></span>

<span data-ttu-id="30632-192">Énumérations représentent généralement les valeurs qui s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="30632-192">Enumerations typically represent mutually exclusive values.</span></span> <span data-ttu-id="30632-193">En incluant le <xref:System.FlagsAttribute> d’attribut dans le `Enum` déclaration, vous pouvez affecter à la place plusieurs valeurs à une instance de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-193">By including the <xref:System.FlagsAttribute> attribute in the `Enum` declaration, you can instead assign multiple values to an instance of the enumeration.</span></span> <span data-ttu-id="30632-194">Le <xref:System.FlagsAttribute> attribut spécifie que l’énumération être traitée comme un champ de bits, autrement dit, un jeu d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="30632-194">The <xref:System.FlagsAttribute> attribute specifies that the enumeration be treated as a bit field, that is, a set of flags.</span></span> <span data-ttu-id="30632-195">Ils sont appelés *au niveau du bit* énumérations.</span><span class="sxs-lookup"><span data-stu-id="30632-195">These are called *bitwise* enumerations.</span></span>

<span data-ttu-id="30632-196">Lorsque vous déclarez une énumération à l’aide de la <xref:System.FlagsAttribute> attribut, nous vous recommandons d’utiliser puissances de 2, qui est, 1, 2, 4, 8, 16 et ainsi de suite, pour les valeurs.</span><span class="sxs-lookup"><span data-stu-id="30632-196">When you declare an enumeration by using the <xref:System.FlagsAttribute> attribute, we recommend that you use powers of 2, that is, 1, 2, 4, 8, 16, and so on, for the values.</span></span> <span data-ttu-id="30632-197">Nous vous recommandons également de « None » soit le nom d’un membre dont la valeur est 0.</span><span class="sxs-lookup"><span data-stu-id="30632-197">We also recommend that "None" be the name of a member whose value is 0.</span></span> <span data-ttu-id="30632-198">Pour obtenir des instructions supplémentaires, consultez <xref:System.FlagsAttribute> et <xref:System.Enum>.</span><span class="sxs-lookup"><span data-stu-id="30632-198">For additional guidelines, see <xref:System.FlagsAttribute> and <xref:System.Enum>.</span></span>

## <a name="example"></a><span data-ttu-id="30632-199">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-199">Example</span></span>

<span data-ttu-id="30632-200">L’exemple suivant montre comment utiliser l’instruction `Enum`.</span><span class="sxs-lookup"><span data-stu-id="30632-200">The following example shows how to use the `Enum` statement.</span></span> <span data-ttu-id="30632-201">Notez que le membre est appelé `EggSizeEnum.Medium`et non comme `Medium`.</span><span class="sxs-lookup"><span data-stu-id="30632-201">Note that the member is referred to as `EggSizeEnum.Medium`, and not as `Medium`.</span></span>

[!code-vb[VbEnumsTask#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class1.vb#41)]

## <a name="example"></a><span data-ttu-id="30632-202">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-202">Example</span></span>

<span data-ttu-id="30632-203">La méthode dans l’exemple suivant est en dehors de la `Egg` classe.</span><span class="sxs-lookup"><span data-stu-id="30632-203">The method in the following example is outside the `Egg` class.</span></span> <span data-ttu-id="30632-204">Par conséquent, `EggSizeEnum` est le nom complet en tant que `Egg.EggSizeEnum`.</span><span class="sxs-lookup"><span data-stu-id="30632-204">Therefore, `EggSizeEnum` is fully qualified as `Egg.EggSizeEnum`.</span></span>

[!code-vb[VbEnumsTask#42](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class1.vb#42)]

## <a name="example"></a><span data-ttu-id="30632-205">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-205">Example</span></span>

<span data-ttu-id="30632-206">L’exemple suivant utilise la `Enum` instruction pour définir un ensemble de connexes les valeurs des constantes nommées.</span><span class="sxs-lookup"><span data-stu-id="30632-206">The following example uses the `Enum` statement to define a related set of named constant values.</span></span> <span data-ttu-id="30632-207">Dans ce cas, les valeurs sont des couleurs, que vous pouvez choisir de concevoir des formulaires de saisie de données pour une base de données.</span><span class="sxs-lookup"><span data-stu-id="30632-207">In this case, the values are colors you might choose to design data entry forms for a database.</span></span>

[!code-vb[VbEnumsTask#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#30)]

## <a name="example"></a><span data-ttu-id="30632-208">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-208">Example</span></span>

<span data-ttu-id="30632-209">L’exemple suivant montre les valeurs qui incluent des nombres positifs et négatifs.</span><span class="sxs-lookup"><span data-stu-id="30632-209">The following example shows values that include both positive and negative numbers.</span></span>

[!code-vb[VbEnumsTask#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#31)]

## <a name="example"></a><span data-ttu-id="30632-210">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-210">Example</span></span>

<span data-ttu-id="30632-211">Dans l’exemple suivant, un `As` clause est utilisée pour spécifier le `datatype` d’une énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-211">In the following example, an `As` clause is used to specify the `datatype` of an enumeration.</span></span>

[!code-vb[VbEnumsTask#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#6)]

## <a name="example"></a><span data-ttu-id="30632-212">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-212">Example</span></span>

<span data-ttu-id="30632-213">L’exemple suivant montre comment utiliser une énumération au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="30632-213">The following example shows how to use a bitwise enumeration.</span></span> <span data-ttu-id="30632-214">Plusieurs valeurs peuvent être affectés à une instance d’une énumération au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="30632-214">Multiple values can be assigned to an instance of a bitwise enumeration.</span></span> <span data-ttu-id="30632-215">Le `Enum` déclaration inclut le <xref:System.FlagsAttribute> attribut, qui indique que l’énumération peut être traitée comme un jeu d’indicateurs.</span><span class="sxs-lookup"><span data-stu-id="30632-215">The `Enum` declaration includes the <xref:System.FlagsAttribute> attribute, which indicates that the enumeration can be treated as a set of flags.</span></span>

[!code-vb[VbEnumsTask#61](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class1.vb#61)]

## <a name="example"></a><span data-ttu-id="30632-216">Exemple</span><span class="sxs-lookup"><span data-stu-id="30632-216">Example</span></span>

<span data-ttu-id="30632-217">L’exemple suivant effectue une itération dans une énumération.</span><span class="sxs-lookup"><span data-stu-id="30632-217">The following example iterates through an enumeration.</span></span> <span data-ttu-id="30632-218">Il utilise le <xref:System.Enum.GetNames%2A> méthode pour extraire un tableau de noms de membre de l’énumération, et <xref:System.Enum.GetValues%2A> pour récupérer un tableau de valeurs de membre.</span><span class="sxs-lookup"><span data-stu-id="30632-218">It uses the <xref:System.Enum.GetNames%2A> method to retrieve an array of member names from the enumeration, and <xref:System.Enum.GetValues%2A> to retrieve an array of member values.</span></span>

[!code-vb[VbEnumsTask#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class1.vb#51)]

## <a name="see-also"></a><span data-ttu-id="30632-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30632-219">See also</span></span>

- <xref:System.Enum>
- <xref:Microsoft.VisualBasic.Strings.AscW%2A>
- [<span data-ttu-id="30632-220">Const (instruction)</span><span class="sxs-lookup"><span data-stu-id="30632-220">Const Statement</span></span>](../../../visual-basic/language-reference/statements/const-statement.md)
- [<span data-ttu-id="30632-221">Dim (instruction)</span><span class="sxs-lookup"><span data-stu-id="30632-221">Dim Statement</span></span>](../../../visual-basic/language-reference/statements/dim-statement.md)
- [<span data-ttu-id="30632-222">Conversions implicites et explicites</span><span class="sxs-lookup"><span data-stu-id="30632-222">Implicit and Explicit Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [<span data-ttu-id="30632-223">Fonctions de conversion de types</span><span class="sxs-lookup"><span data-stu-id="30632-223">Type Conversion Functions</span></span>](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="30632-224">Constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="30632-224">Constants and Enumerations</span></span>](../../../visual-basic/language-reference/constants-and-enumerations.md)
