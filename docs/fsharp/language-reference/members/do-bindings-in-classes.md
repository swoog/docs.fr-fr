---
title: Liaisons do dans les classes
description: Découvrez comment utiliser un F# 'do' liaison dans une définition de classe, qui effectue des actions lorsque l’objet est construit ou lorsque le type est tout d’abord utilisé.
ms.date: 05/16/2016
ms.openlocfilehash: c924c882974989436d8ea404ebee0a7ef3c54fd3
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641797"
---
# <a name="do-bindings-in-classes"></a><span data-ttu-id="63432-103">Liaisons do dans les classes</span><span class="sxs-lookup"><span data-stu-id="63432-103">do Bindings in Classes</span></span>

<span data-ttu-id="63432-104">Un `do` liaison dans une définition de classe effectue des actions lorsque l’objet est construit ou, pour une analyse statique `do` liaison, lorsque le type est tout d’abord utilisé.</span><span class="sxs-lookup"><span data-stu-id="63432-104">A `do` binding in a class definition performs actions when the object is constructed or, for a static `do` binding, when the type is first used.</span></span>

## <a name="syntax"></a><span data-ttu-id="63432-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63432-105">Syntax</span></span>

```fsharp
[static] do expression
```

## <a name="remarks"></a><span data-ttu-id="63432-106">Notes</span><span class="sxs-lookup"><span data-stu-id="63432-106">Remarks</span></span>

<span data-ttu-id="63432-107">Un `do` liaison apparaît avec ou après `let` liaisons mais avant les définitions de membre dans une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="63432-107">A `do` binding appears together with or after `let` bindings but before member definitions in a class definition.</span></span> <span data-ttu-id="63432-108">Bien que le `do` mot clé est facultatif pour `do` liaisons au niveau du module, il n’est pas facultatif pour `do` liaisons dans une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="63432-108">Although the `do` keyword is optional for `do` bindings at the module level, it is not optional for `do` bindings in a class definition.</span></span>

<span data-ttu-id="63432-109">Pour la construction de chaque objet d’un type donné, non statique `do` liaisons et non statiques `let` sont exécutées dans l’ordre dans lequel ils apparaissent dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="63432-109">For the construction of every object of any given type, non-static `do` bindings and non-static `let` bindings are executed in the order in which they appear in the class definition.</span></span> <span data-ttu-id="63432-110">Plusieurs `do` liaisons peuvent se produire dans un type.</span><span class="sxs-lookup"><span data-stu-id="63432-110">Multiple `do` bindings can occur in one type.</span></span> <span data-ttu-id="63432-111">Le non-static `let` liaisons et non statiques `do` deviennent le corps du constructeur principal.</span><span class="sxs-lookup"><span data-stu-id="63432-111">The non-static `let` bindings and the non-static `do` bindings become the body of the primary constructor.</span></span> <span data-ttu-id="63432-112">Le code dans le non-static `do` section des liaisons peut référencer les paramètres du constructeur principal et des valeurs ou des fonctions qui sont définies dans le `let` section des liaisons.</span><span class="sxs-lookup"><span data-stu-id="63432-112">The code in the non-static `do` bindings section can reference the primary constructor parameters and any values or functions that are defined in the `let` bindings section.</span></span>

<span data-ttu-id="63432-113">Non statiques `do` liaisons peuvent accéder aux membres de la classe tant que la classe a un auto-identificateur défini par un `as` mot clé dans la classe de titre et tant que toutes les utilisations de ces membres sont qualifiées avec l’auto-identificateur pour la classe.</span><span class="sxs-lookup"><span data-stu-id="63432-113">Non-static `do` bindings can access members of the class as long as the class has a self identifier that is defined by an `as` keyword in the class heading, and as long as all uses of those members are qualified with the self identifier for the class.</span></span>

<span data-ttu-id="63432-114">Étant donné que `let` liaisons initialisent les champs privés d’une classe, ce qui est souvent nécessaire pour garantir que les membres se comportent comme prévu, `do` liaisons sont généralement placées après `let` liaisons afin que le code dans le `do` peut de liaison exécuter avec un objet entièrement initialisé.</span><span class="sxs-lookup"><span data-stu-id="63432-114">Because `let` bindings initialize the private fields of a class, which is often necessary to guarantee that members behave as expected, `do` bindings are usually put after `let` bindings so that code in the `do` binding can execute with a fully initialized object.</span></span> <span data-ttu-id="63432-115">Si votre code tente d’utiliser un membre avant l’initialisation est terminée, une exception InvalidOperationException est déclenchée.</span><span class="sxs-lookup"><span data-stu-id="63432-115">If your code attempts to use a member before the initialization is complete, an InvalidOperationException is raised.</span></span>

<span data-ttu-id="63432-116">Statique `do` liaisons peuvent référencer des membres statiques ou champs de la classe, mais pas de membres ou des champs de l’instance.</span><span class="sxs-lookup"><span data-stu-id="63432-116">Static `do` bindings can reference static members or fields of the enclosing class but not instance members or fields.</span></span> <span data-ttu-id="63432-117">Statique `do` liaisons deviennent partie intégrante de l’initialiseur statique pour la classe, qui est toujours exécuté avant la première utilisation de la classe.</span><span class="sxs-lookup"><span data-stu-id="63432-117">Static `do` bindings become part of the static initializer for the class, which is guaranteed to execute before the class is first used.</span></span>

<span data-ttu-id="63432-118">Les attributs sont ignorés pour `do` liaisons dans les types.</span><span class="sxs-lookup"><span data-stu-id="63432-118">Attributes are ignored for `do` bindings in types.</span></span> <span data-ttu-id="63432-119">Si un attribut n’est requis pour le code qui s’exécute dans un `do` de liaison, elle doit s’appliquer au constructeur principal.</span><span class="sxs-lookup"><span data-stu-id="63432-119">If an attribute is required for code that executes in a `do` binding, it must be applied to the primary constructor.</span></span>

<span data-ttu-id="63432-120">Dans le code suivant, une classe a statique `do` liaison et non statiques `do` liaison.</span><span class="sxs-lookup"><span data-stu-id="63432-120">In the following code, a class has a static `do` binding and a non-static `do` binding.</span></span> <span data-ttu-id="63432-121">L’objet a un constructeur qui possède deux paramètres, `a` et `b`, et deux champs privés sont définis dans le `let` liaisons pour la classe.</span><span class="sxs-lookup"><span data-stu-id="63432-121">The object has a constructor that has two parameters, `a` and `b`, and two private fields are defined in the `let` bindings for the class.</span></span> <span data-ttu-id="63432-122">Deux propriétés sont également définies.</span><span class="sxs-lookup"><span data-stu-id="63432-122">Two properties are also defined.</span></span> <span data-ttu-id="63432-123">Tous ces éléments sont dans la portée de la non statique `do` section des liaisons, comme cela est illustré par la ligne qui imprime toutes ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="63432-123">All of these are in scope in the non-static `do` bindings section, as is illustrated by the line that prints all those values.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3101.fs)]

<span data-ttu-id="63432-124">La sortie est la suivante.</span><span class="sxs-lookup"><span data-stu-id="63432-124">The output is as follows.</span></span>

```console
Initializing MyType.
Initializing object 1 2 2 4 8 16
```

## <a name="see-also"></a><span data-ttu-id="63432-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63432-125">See also</span></span>

- [<span data-ttu-id="63432-126">Membres</span><span class="sxs-lookup"><span data-stu-id="63432-126">Members</span></span>](index.md)
- [<span data-ttu-id="63432-127">Classes</span><span class="sxs-lookup"><span data-stu-id="63432-127">Classes</span></span>](../classes.md)
- [<span data-ttu-id="63432-128">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="63432-128">Constructors</span></span>](constructors.md)
- [<span data-ttu-id="63432-129">Liaisons `let` dans des classes</span><span class="sxs-lookup"><span data-stu-id="63432-129">`let` Bindings in Classes</span></span>](let-bindings-in-classes.md)
- [<span data-ttu-id="63432-130">`do` liaisons</span><span class="sxs-lookup"><span data-stu-id="63432-130">`do` Bindings</span></span>](../functions/do-Bindings.md)
