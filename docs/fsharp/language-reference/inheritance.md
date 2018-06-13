---
title: Héritage (F#)
description: "Découvrez comment spécifier des relations d’héritage F # à l’aide du mot clé 'inherit'."
ms.date: 05/16/2016
ms.openlocfilehash: 3d0c0785fc595315a8283979b99d0ec4fc5cbc0d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33564767"
---
# <a name="inheritance"></a><span data-ttu-id="bea36-103">Héritage</span><span class="sxs-lookup"><span data-stu-id="bea36-103">Inheritance</span></span>

<span data-ttu-id="bea36-104">L’héritage est utilisé pour modéliser la relation « est-un », ou sous-typage, dans la programmation orientée objet.</span><span class="sxs-lookup"><span data-stu-id="bea36-104">Inheritance is used to model the "is-a" relationship, or subtyping, in object-oriented programming.</span></span>


## <a name="specifying-inheritance-relationships"></a><span data-ttu-id="bea36-105">Spécification de relations d’héritage</span><span class="sxs-lookup"><span data-stu-id="bea36-105">Specifying Inheritance Relationships</span></span>
<span data-ttu-id="bea36-106">Vous spécifiez des relations d’héritage à l’aide de la `inherit` mot clé dans une déclaration de classe.</span><span class="sxs-lookup"><span data-stu-id="bea36-106">You specify inheritance relationships by using the `inherit` keyword in a class declaration.</span></span> <span data-ttu-id="bea36-107">La forme syntaxique de base est illustrée dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bea36-107">The basic syntactical form is shown in the following example.</span></span>

```fsharp
type MyDerived(...) =
    inherit MyBase(...)
```

<span data-ttu-id="bea36-108">Une classe peut avoir au plus une classe de base directe.</span><span class="sxs-lookup"><span data-stu-id="bea36-108">A class can have at most one direct base class.</span></span> <span data-ttu-id="bea36-109">Si vous ne spécifiez pas une classe de base à l’aide de la `inherit` (mot clé), la classe hérite implicitement de `System.Object`.</span><span class="sxs-lookup"><span data-stu-id="bea36-109">If you do not specify a base class by using the `inherit` keyword, the class implicitly inherits from `System.Object`.</span></span>


## <a name="inherited-members"></a><span data-ttu-id="bea36-110">Membres hérités</span><span class="sxs-lookup"><span data-stu-id="bea36-110">Inherited Members</span></span>
<span data-ttu-id="bea36-111">Si une classe hérite d’une autre classe, les méthodes et les membres de la classe de base sont disponibles pour les utilisateurs de la classe dérivée, comme si elles étaient des membres directs de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="bea36-111">If a class inherits from another class, the methods and members of the base class are available to users of the derived class as if they were direct members of the derived class.</span></span>

<span data-ttu-id="bea36-112">Les liaisons let et les paramètres du constructeur sont privés à une classe et, par conséquent, ne peut pas être accessible à partir de classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="bea36-112">Any let bindings and constructor parameters are private to a class and, therefore, cannot be accessed from derived classes.</span></span>

<span data-ttu-id="bea36-113">Le mot clé `base` est disponible dans les classes dérivées et fait référence à l’instance de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="bea36-113">The keyword `base` is available in derived classes and refers to the base class instance.</span></span> <span data-ttu-id="bea36-114">Il est utilisé comme auto-identificateur.</span><span class="sxs-lookup"><span data-stu-id="bea36-114">It is used like the self-identifier.</span></span>


## <a name="virtual-methods-and-overrides"></a><span data-ttu-id="bea36-115">Les méthodes virtuelles et remplacements</span><span class="sxs-lookup"><span data-stu-id="bea36-115">Virtual Methods and Overrides</span></span>
<span data-ttu-id="bea36-116">Méthodes virtuelles (et les propriétés) fonctionnent différemment en F # par rapport aux autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="bea36-116">Virtual methods (and properties) work somewhat differently in F# as compared to other .NET languages.</span></span> <span data-ttu-id="bea36-117">Pour déclarer un nouveau membre virtuel, vous utilisez la `abstract` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="bea36-117">To declare a new virtual member, you use the `abstract` keyword.</span></span> <span data-ttu-id="bea36-118">Pour cela, indépendamment de si vous fournissez une implémentation par défaut de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="bea36-118">You do this regardless of whether you provide a default implementation for that method.</span></span> <span data-ttu-id="bea36-119">Par conséquent, une définition complète d’une méthode virtuelle dans une classe de base suit ce modèle :</span><span class="sxs-lookup"><span data-stu-id="bea36-119">Thus a complete definition of a virtual method in a base class follows this pattern:</span></span>

```fsharp
abstract member [method-name] : [type]

default [self-identifier].[method-name] [argument-list] = [method-body]
```

<span data-ttu-id="bea36-120">Et, dans une classe dérivée, une substitution de cette méthode virtuelle suit ce modèle :</span><span class="sxs-lookup"><span data-stu-id="bea36-120">And in a derived class, an override of this virtual method follows this pattern:</span></span>

```fsharp
override [self-identifier].[method-name] [argument-list] = [method-body]
```

<span data-ttu-id="bea36-121">Si vous omettez l’implémentation par défaut dans la classe de base, la classe de base est une classe abstraite.</span><span class="sxs-lookup"><span data-stu-id="bea36-121">If you omit the default implementation in the base class, the base class becomes an abstract class.</span></span>

<span data-ttu-id="bea36-122">L’exemple de code suivant illustre la déclaration d’une nouvelle méthode virtuelle `function1` dans une classe de base et comment la substituer dans une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="bea36-122">The following code example illustrates the declaration of a new virtual method `function1` in a base class and how to override it in a derived class.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2601.fs)]
    
## <a name="constructors-and-inheritance"></a><span data-ttu-id="bea36-123">Constructeurs et héritage</span><span class="sxs-lookup"><span data-stu-id="bea36-123">Constructors and Inheritance</span></span>
<span data-ttu-id="bea36-124">Le constructeur de la classe de base doit être appelé dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="bea36-124">The constructor for the base class must be called in the derived class.</span></span> <span data-ttu-id="bea36-125">Les arguments du constructeur de classe de base apparaissent dans la liste d’arguments dans le `inherit` clause.</span><span class="sxs-lookup"><span data-stu-id="bea36-125">The arguments for the base class constructor appear in the argument list in the `inherit` clause.</span></span> <span data-ttu-id="bea36-126">Les valeurs qui sont utilisées doivent être déterminées à partir des arguments fournis au constructeur de classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="bea36-126">The values that are used must be determined from the arguments supplied to the derived class constructor.</span></span>

<span data-ttu-id="bea36-127">Le code suivant montre une classe de base et une classe dérivée, où la classe dérivée appelle le constructeur de classe de base dans la clause d’héritage :</span><span class="sxs-lookup"><span data-stu-id="bea36-127">The following code shows a base class and a derived class, where the derived class calls the base class constructor in the inherit clause:</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2602.fs)]

<span data-ttu-id="bea36-128">Dans le cas de plusieurs constructeurs, le code suivant peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="bea36-128">In the case of multiple constructors, the following code can be used.</span></span> <span data-ttu-id="bea36-129">La première ligne des constructeurs de classe dérivée est la `inherit` clause et les champs s’affichent en tant que champs explicites qui sont déclarées avec le `val` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="bea36-129">The first line of the derived class constructors is the `inherit` clause, and the fields appear as explicit fields that are declared with the `val` keyword.</span></span> <span data-ttu-id="bea36-130">Pour plus d’informations, consultez [champs explicites : le `val` mot clé](members/explicit-fields-the-val-keyword.md).</span><span class="sxs-lookup"><span data-stu-id="bea36-130">For more information, see [Explicit Fields: The `val` Keyword](members/explicit-fields-the-val-keyword.md).</span></span>

```fsharp
type BaseClass =
    val string1 : string
    new (str) = { string1 = str }
    new () = { string1 = "" }

type DerivedClass =
    inherit BaseClass

    val string2 : string
    new (str1, str2) = { inherit BaseClass(str1); string2 = str2 }
    new (str2) = { inherit BaseClass(); string2 = str2 }

let obj1 = DerivedClass("A", "B")
let obj2 = DerivedClass("A")
```

## <a name="alternatives-to-inheritance"></a><span data-ttu-id="bea36-131">Alternatives à l’héritage</span><span class="sxs-lookup"><span data-stu-id="bea36-131">Alternatives to Inheritance</span></span>
<span data-ttu-id="bea36-132">Dans le cas où une modification mineure d’un type est requise, envisagez d’utiliser une expression d’objet en guise d’alternative à l’héritage.</span><span class="sxs-lookup"><span data-stu-id="bea36-132">In cases where a minor modification of a type is required, consider using an object expression as an alternative to inheritance.</span></span> <span data-ttu-id="bea36-133">L’exemple suivant illustre l’utilisation d’une expression d’objet en guise d’alternative à la création d’un type dérivé :</span><span class="sxs-lookup"><span data-stu-id="bea36-133">The following example illustrates the use of an object expression as an alternative to creating a new derived type:</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2603.fs)]

<span data-ttu-id="bea36-134">Pour plus d’informations sur les expressions d’objet, consultez [Expressions d’objet](object-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="bea36-134">For more information about object expressions, see [Object Expressions](object-expressions.md).</span></span>

<span data-ttu-id="bea36-135">Lorsque vous créez des hiérarchies d’objets, envisagez d’utiliser une union discriminée au lieu de l’héritage.</span><span class="sxs-lookup"><span data-stu-id="bea36-135">When you are creating object hierarchies, consider using a discriminated union instead of inheritance.</span></span> <span data-ttu-id="bea36-136">Les unions discriminées peuvent également comportement du modèle variée des différents objets qui partagent un type global commun.</span><span class="sxs-lookup"><span data-stu-id="bea36-136">Discriminated unions can also model varied behavior of different objects that share a common overall type.</span></span> <span data-ttu-id="bea36-137">Une union discriminée unique peut souvent supprimer la nécessité pour un nombre de classes dérivées qui sont des variations mineures de l’autre.</span><span class="sxs-lookup"><span data-stu-id="bea36-137">A single discriminated union can often eliminate the need for a number of derived classes that are minor variations of each other.</span></span> <span data-ttu-id="bea36-138">Pour plus d’informations sur les unions discriminées, consultez [les Unions discriminées](discriminated-unions.md).</span><span class="sxs-lookup"><span data-stu-id="bea36-138">For information about discriminated unions, see [Discriminated Unions](discriminated-unions.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="bea36-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bea36-139">See Also</span></span>
[<span data-ttu-id="bea36-140">Expressions d'objet</span><span class="sxs-lookup"><span data-stu-id="bea36-140">Object Expressions</span></span>](object-expressions.md)

[<span data-ttu-id="bea36-141">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="bea36-141">F# Language Reference</span></span>](index.md)
