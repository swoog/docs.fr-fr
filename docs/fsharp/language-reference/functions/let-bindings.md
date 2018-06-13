---
title: Liaisons let (F#)
description: "Découvrez comment utiliser une liaison qui associe un identificateur à une valeur ou une fonction ' let' F #."
ms.date: 05/16/2016
ms.openlocfilehash: bcdf01747c2a1d0ba9a894188dae1d42acdf9104
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33566270"
---
# <a name="let-bindings"></a><span data-ttu-id="3fd1c-103">Liaisons let</span><span class="sxs-lookup"><span data-stu-id="3fd1c-103">let Bindings</span></span>

<span data-ttu-id="3fd1c-104">A *liaison* associe un identificateur à une valeur ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-104">A *binding* associates an identifier with a value or function.</span></span> <span data-ttu-id="3fd1c-105">Vous utilisez la `let` (mot clé) pour lier un nom à une valeur ou une fonction.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-105">You use the `let` keyword to bind a name to a value or function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd1c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fd1c-106">Syntax</span></span>

```fsharp
// Binding a value:
let identifier-or-pattern [: type] =expressionbody-expression
// Binding a function value:
let identifier parameter-list [: return-type ] =expressionbody-expression
```

## <a name="remarks"></a><span data-ttu-id="3fd1c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3fd1c-107">Remarks</span></span>

<span data-ttu-id="3fd1c-108">Le `let` mot clé est utilisé dans des expressions pour définir des valeurs ou des valeurs de fonction pour un ou plusieurs noms de liaison.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-108">The `let` keyword is used in binding expressions to define values or function values for one or more names.</span></span> <span data-ttu-id="3fd1c-109">La forme la plus simple du `let` expression lie un nom à une valeur simple, comme suit.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-109">The simplest form of the `let` expression binds a name to a simple value, as follows.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1101.fs)]

<span data-ttu-id="3fd1c-110">Si vous séparez l’expression de l’identificateur à l’aide d’une nouvelle ligne, vous devez mettre en retrait chaque ligne de l’expression, comme dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-110">If you separate the expression from the identifier by using a new line, you must indent each line of the expression, as in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1102.fs)]

<span data-ttu-id="3fd1c-111">Au lieu de simplement un nom, un modèle qui contient les noms peut être spécifié, par exemple, un tuple, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-111">Instead of just a name, a pattern that contains names can be specified, for example, a tuple, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1103.fs)]

<span data-ttu-id="3fd1c-112">Le *expression de corps* est l’expression dans laquelle les noms sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-112">The *body-expression* is the expression in which the names are used.</span></span> <span data-ttu-id="3fd1c-113">L’expression de corps apparaît sur sa propre ligne, mise en retrait de ligne exactement avec le premier caractère dans le `let` (mot clé) :</span><span class="sxs-lookup"><span data-stu-id="3fd1c-113">The body expression appears on its own line, indented to line up exactly with the first character in the `let` keyword:</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1104.fs)]

<span data-ttu-id="3fd1c-114">A `let` liaison peut apparaître au niveau du module, dans la définition d’un type de classe, ou dans des portées locales, par exemple dans une définition de fonction.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-114">A `let` binding can appear at the module level, in the definition of a class type, or in local scopes, such as in a function definition.</span></span> <span data-ttu-id="3fd1c-115">A `let` liaison de haut niveau dans un module ou d’un type de classe n’a pas besoin d’avoir une expression de corps, mais à d’autres niveaux de portée, l’expression de corps est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-115">A `let` binding at the top level in a module or in a class type does not need to have a body expression, but at other scope levels, the body expression is required.</span></span> <span data-ttu-id="3fd1c-116">Les noms liés sont utilisables après le point de définition, mais pas à tout moment avant le `let` liaison s’affiche, comme cela est illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-116">The bound names are usable after the point of definition, but not at any point before the `let` binding appears, as is illustrated in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1105.fs)]
    
## <a name="function-bindings"></a><span data-ttu-id="3fd1c-117">Liaisons de fonction</span><span class="sxs-lookup"><span data-stu-id="3fd1c-117">Function Bindings</span></span>

<span data-ttu-id="3fd1c-118">Liaisons de fonction suivent les règles pour les liaisons de valeur, à ceci près que les liaisons de fonction incluent le nom de fonction et les paramètres, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-118">Function bindings follow the rules for value bindings, except that function bindings include the function name and the parameters, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1106.fs)]

<span data-ttu-id="3fd1c-119">En règle générale, les paramètres sont des modèles, tels que d’un modèle de tuple :</span><span class="sxs-lookup"><span data-stu-id="3fd1c-119">In general, parameters are patterns, such as a tuple pattern:</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1107.fs)]

<span data-ttu-id="3fd1c-120">A `let` expression de liaison prend la valeur de la dernière expression.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-120">A `let` binding expression evaluates to the value of the last expression.</span></span> <span data-ttu-id="3fd1c-121">Par conséquent, dans l’exemple de code suivant, la valeur de `result` est calculée à partir de `100 * function3 (1, 2)`, qui prend la valeur `300`.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-121">Therefore, in the following code example, the value of `result` is computed from `100 * function3 (1, 2)`, which evaluates to `300`.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1109.fs)]

<span data-ttu-id="3fd1c-122">Pour plus d’informations, consultez [Fonctions](index.md).</span><span class="sxs-lookup"><span data-stu-id="3fd1c-122">For more information, see [Functions](index.md).</span></span>

## <a name="type-annotations"></a><span data-ttu-id="3fd1c-123">Annotations de type</span><span class="sxs-lookup"><span data-stu-id="3fd1c-123">Type Annotations</span></span>

<span data-ttu-id="3fd1c-124">Vous pouvez spécifier les types des paramètres en incluant un signe deux-points ( :) suivi d’un nom de type, le tout entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-124">You can specify types for parameters by including a colon (:) followed by a type name, all enclosed in parentheses.</span></span> <span data-ttu-id="3fd1c-125">Vous pouvez également spécifier le type de la valeur de retour en ajoutant le signe deux-points et le type après le dernier paramètre.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-125">You can also specify the type of the return value by appending the colon and type after the last parameter.</span></span> <span data-ttu-id="3fd1c-126">Les annotations de type complète pour `function1`, avec des entiers comme types de paramètres, se présente comme suit.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-126">The full type annotations for `function1`, with integers as the parameter types, would be as follows.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1108.fs)]

<span data-ttu-id="3fd1c-127">Lorsqu’il n’y a aucun paramètre de type explicite, l’inférence de type est utilisé pour déterminer les types de paramètres de fonctions.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-127">When there are no explicit type parameters, type inference is used to determine the types of parameters of functions.</span></span> <span data-ttu-id="3fd1c-128">Cela peut inclure la généralisation automatique du type d’un paramètre générique.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-128">This can include automatically generalizing the type of a parameter to be generic.</span></span>

<span data-ttu-id="3fd1c-129">Pour plus d’informations, consultez [généralisation automatique](../generics/automatic-generalization.md) et [l’inférence de Type](../type-inference.md).</span><span class="sxs-lookup"><span data-stu-id="3fd1c-129">For more information, see [Automatic Generalization](../generics/automatic-generalization.md) and [Type Inference](../type-inference.md).</span></span>

## <a name="let-bindings-in-classes"></a><span data-ttu-id="3fd1c-130">Liaisons let dans des classes</span><span class="sxs-lookup"><span data-stu-id="3fd1c-130">let Bindings in Classes</span></span>

<span data-ttu-id="3fd1c-131">A `let` liaison peut apparaître dans un type de classe, mais pas dans une structure ou un type d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-131">A `let` binding can appear in a class type but not in a structure or record type.</span></span> <span data-ttu-id="3fd1c-132">Pour utiliser une liaison let dans un type de classe, la classe doit avoir un constructeur principal.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-132">To use a let binding in a class type, the class must have a primary constructor.</span></span> <span data-ttu-id="3fd1c-133">Paramètres du constructeur doivent apparaître après le nom de type dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-133">Constructor parameters must appear after the type name in the class definition.</span></span> <span data-ttu-id="3fd1c-134">A `let` liaison dans un type de classe définit les champs privés et les membres de ce type de classe et, avec `do` liaisons dans le type, le code du constructeur principal pour le type de formulaires.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-134">A `let` binding in a class type defines private fields and members for that class type and, together with `do` bindings in the type, forms the code for the primary constructor for the type.</span></span> <span data-ttu-id="3fd1c-135">Les exemples de code suivants montrent une classe `MyClass` avec les champs privés `field1` et `field2`.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-135">The following code examples show a class `MyClass` with private fields `field1` and `field2`.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1110.fs)]

<span data-ttu-id="3fd1c-136">Les étendues de `field1` et `field2` sont limitées au type dans lequel ils sont déclarés.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-136">The scopes of `field1` and `field2` are limited to the type in which they are declared.</span></span> <span data-ttu-id="3fd1c-137">Pour plus d’informations, consultez [ `let` liaisons dans les Classes](../members/let-bindings-in-classes.md) et [Classes](../classes.md).</span><span class="sxs-lookup"><span data-stu-id="3fd1c-137">For more information, see [`let` Bindings in Classes](../members/let-bindings-in-classes.md) and [Classes](../classes.md).</span></span>

## <a name="type-parameters-in-let-bindings"></a><span data-ttu-id="3fd1c-138">Paramètres de type dans les liaisons let</span><span class="sxs-lookup"><span data-stu-id="3fd1c-138">Type Parameters in let Bindings</span></span>

<span data-ttu-id="3fd1c-139">A `let` liaison au niveau du module dans un type, ou dans une expression de calcul peut avoir des paramètres de type explicite.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-139">A `let` binding at the module level, in a type, or in a computation expression can have explicit type parameters.</span></span> <span data-ttu-id="3fd1c-140">Une liaison let dans une expression, comme dans une définition de fonction, ne peut pas avoir de paramètres de type.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-140">A let binding in an expression, such as within a function definition, cannot have type parameters.</span></span> <span data-ttu-id="3fd1c-141">Pour plus d’informations, consultez la page [Génériques](../generics/index.md).</span><span class="sxs-lookup"><span data-stu-id="3fd1c-141">For more information, see [Generics](../generics/index.md).</span></span>

## <a name="attributes-on-let-bindings"></a><span data-ttu-id="3fd1c-142">Attributs sur les liaisons let</span><span class="sxs-lookup"><span data-stu-id="3fd1c-142">Attributes on let Bindings</span></span>

<span data-ttu-id="3fd1c-143">Les attributs peuvent être appliqués au niveau supérieur `let` liaisons dans un module, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-143">Attributes can be applied to top-level `let` bindings in a module, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1111.fs)]
    
## <a name="scope-and-accessibility-of-let-bindings"></a><span data-ttu-id="3fd1c-144">Portée et l’accessibilité des liaisons Let</span><span class="sxs-lookup"><span data-stu-id="3fd1c-144">Scope and Accessibility of Let Bindings</span></span>

<span data-ttu-id="3fd1c-145">L’étendue d’une entité déclarée avec une liaison let est limitée à la partie de l’objet contenant l’étendue (par exemple, une fonction, un module, fichier ou classe) une fois que la liaison s’affiche.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-145">The scope of an entity declared with a let binding is limited to the portion of the containing scope (such as a function, module, file or class) after the binding appears.</span></span> <span data-ttu-id="3fd1c-146">Par conséquent, il peut être désignée qu’une liaison let introduit un nom dans une étendue.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-146">Therefore, it can be said that a let binding introduces a name into a scope.</span></span> <span data-ttu-id="3fd1c-147">Dans un module, une valeur de liées à let ou une fonction est accessible aux clients d’un module tant que le module est accessible, étant donné que les liaisons let dans un module sont compilés dans des fonctions publiques du module.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-147">In a module, a let-bound value or function is accessible to clients of a module as long as the module is accessible, since the let bindings in a module are compiled into public functions of the module.</span></span> <span data-ttu-id="3fd1c-148">En revanche, les liaisons let dans une classe sont privées à la classe.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-148">By contrast, let bindings in a class are private to the class.</span></span>

<span data-ttu-id="3fd1c-149">En règle générale, les fonctions dans les modules doivent être qualifiées par le nom du module lorsqu’il est utilisé par le code client.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-149">Normally, functions in modules must be qualified by the name of the module when used by client code.</span></span> <span data-ttu-id="3fd1c-150">Par exemple, si un module `Module1` a une fonction `function1`, spécifient les utilisateurs `Module1.function1` pour faire référence à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-150">For example, if a module `Module1` has a function `function1`, users would specify `Module1.function1` to refer to the function.</span></span>

<span data-ttu-id="3fd1c-151">Les utilisateurs d’un module peuvent utiliser une déclaration d’importation à disposition les fonctions dans ce module pour une utilisation sans être qualifié par le nom du module.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-151">Users of a module may use an import declaration to make the functions within that module available for use without being qualified by the module name.</span></span> <span data-ttu-id="3fd1c-152">Dans l’exemple mentionnés ci-dessus, les utilisateurs du module peuvent ouvrir dans ce cas le module à l’aide de l’ouvrir de déclaration d’importation `Module1` et par la suite faire `function1` directement.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-152">In the example just mentioned, users of the module can in that case open the module by using the import declaration open `Module1` and thereafter refer to `function1` directly.</span></span>

```fsharp
module Module1 =
    let function1 x = x + 1.0

module Module2 =
    let function2 x =
        Module1.function1 x

open Module1

let function3 x =
    function1 x
```

<span data-ttu-id="3fd1c-153">Certains modules ont l’attribut [RequireQualifiedAccess](https://msdn.microsoft.com/library/8b9b6ade-0471-4413-ac5d-638cd0de5f15), ce qui signifie que les fonctions qu’ils exposent doivent être qualifiées avec le nom du module.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-153">Some modules have the attribute [RequireQualifiedAccess](https://msdn.microsoft.com/library/8b9b6ade-0471-4413-ac5d-638cd0de5f15), which means that the functions that they expose must be qualified with the name of the module.</span></span> <span data-ttu-id="3fd1c-154">Par exemple, le module F # liste a cet attribut.</span><span class="sxs-lookup"><span data-stu-id="3fd1c-154">For example, the F# List module has this attribute.</span></span>

<span data-ttu-id="3fd1c-155">Pour plus d’informations sur les modules et contrôle d’accès, consultez [Modules](../modules.md) et [le contrôle d’accès](../access-control.md).</span><span class="sxs-lookup"><span data-stu-id="3fd1c-155">For more information on modules and access control, see [Modules](../modules.md) and [Access Control](../access-control.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="3fd1c-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fd1c-156">See Also</span></span>

[<span data-ttu-id="3fd1c-157">Fonctions</span><span class="sxs-lookup"><span data-stu-id="3fd1c-157">Functions</span></span>](index.md)

[<span data-ttu-id="3fd1c-158">Liaisons `let` dans des classes</span><span class="sxs-lookup"><span data-stu-id="3fd1c-158">`let` Bindings in Classes</span></span>](../members/let-bindings-in-classes.md)
