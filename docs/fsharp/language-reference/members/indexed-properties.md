---
title: Propriétés indexées (F#)
description: En savoir plus sur les propriétés indexées dans F#, qui permettent l’accès de type tableau aux données ordonnées.
ms.date: 10/17/2018
ms.openlocfilehash: 3dac60eba3d9e7a9c3e76ad7ee051e6b30b88636
ms.sourcegitcommit: db8b83057d052c1f9f249d128b08d4423af0f7c2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "49452246"
---
# <a name="indexed-properties"></a><span data-ttu-id="1e083-103">Propriétés indexées</span><span class="sxs-lookup"><span data-stu-id="1e083-103">Indexed Properties</span></span>

<span data-ttu-id="1e083-104">Lorsque vous définissez une classe qui effectue l’abstraction sur le tri des données, il peut parfois être utile de fournir un accès indexé à ces données sans exposer l’implémentation sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="1e083-104">When defining a class that abstracts over ordered data, it can sometimes be helpful to provide indexed access to that data without exposing the underlying implementation.</span></span> <span data-ttu-id="1e083-105">Cette opération est effectuée avec la `Index` membre.</span><span class="sxs-lookup"><span data-stu-id="1e083-105">This is done with the `Index` member.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e083-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e083-106">Syntax</span></span>

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.Index
    with get(index-values) =
        get-member-body
    and set index-values values-to-set =
        set-member-body

// Indexed property with get only
member self-identifier.Index
    with get(index-values) =
        get-member-body

// Indexed property that has set only.
member self-identifier.Index
    with set index-values values-to-set =
        set-member-body
```

## <a name="remarks"></a><span data-ttu-id="1e083-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1e083-107">Remarks</span></span>

<span data-ttu-id="1e083-108">Les formes de la syntaxe précédente montrent comment définir des propriétés indexées qui ont les deux un `get` et un `set` (méthode), ont un `get` méthode uniquement, ou avoir un `set` méthode uniquement.</span><span class="sxs-lookup"><span data-stu-id="1e083-108">The forms of the previous syntax show how to define indexed properties that have both a `get` and a `set` method, have a `get` method only, or have a `set` method only.</span></span> <span data-ttu-id="1e083-109">Vous pouvez également combiner les deux la syntaxe indiquée pour get uniquement et la syntaxe indiquée pour set uniquement et produire une propriété qui possède à la fois get et set.</span><span class="sxs-lookup"><span data-stu-id="1e083-109">You can also combine both the syntax shown for get only and the syntax shown for set only, and produce a property that has both get and set.</span></span> <span data-ttu-id="1e083-110">Cette dernière forme vous permet de placer des modificateurs d’accessibilité différente et des attributs sur la méthode get et de définir des méthodes.</span><span class="sxs-lookup"><span data-stu-id="1e083-110">This latter form allows you to put different accessibility modifiers and attributes on the get and set methods.</span></span>

<span data-ttu-id="1e083-111">En utilisant le nom `Item`, le compilateur traite la propriété comme une propriété indexée par défaut.</span><span class="sxs-lookup"><span data-stu-id="1e083-111">By using the name `Item`, the compiler treats the property as a default indexed property.</span></span> <span data-ttu-id="1e083-112">Un *propriété indexée par défaut* est une propriété que vous pouvez accéder à l’aide de la syntaxe de type tableau sur l’instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="1e083-112">A *default indexed property* is a property that you can access by using array-like syntax on the object instance.</span></span> <span data-ttu-id="1e083-113">Par exemple, si `o` est un objet du type qui définit cette propriété, la syntaxe `o.[index]` est utilisé pour accéder à la propriété.</span><span class="sxs-lookup"><span data-stu-id="1e083-113">For example, if `o` is an object of the type that defines this property, the syntax `o.[index]` is used to access the property.</span></span>

<span data-ttu-id="1e083-114">La syntaxe permettant d’accéder à une propriété indexée par défaut consiste à fournir le nom de la propriété et l’index entre parenthèses, comme un membre régulier.</span><span class="sxs-lookup"><span data-stu-id="1e083-114">The syntax for accessing a non-default indexed property is to provide the name of the property and the index in parentheses, just like a regular member.</span></span> <span data-ttu-id="1e083-115">Par exemple, si la propriété sur `o` est appelée `Ordinal`, vous écrivez `o.Ordinal(index)` pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="1e083-115">For example, if the property on `o` is called `Ordinal`, you write `o.Ordinal(index)` to access it.</span></span>

<span data-ttu-id="1e083-116">Quelle que soit la forme que vous utilisez, vous devez toujours utiliser la forme curryfiée pour la méthode set sur une propriété indexée.</span><span class="sxs-lookup"><span data-stu-id="1e083-116">Regardless of which form you use, you should always use the curried form for the set method on an indexed property.</span></span> <span data-ttu-id="1e083-117">Pour plus d’informations sur les fonctions curryfiées, consultez [fonctions](../functions/index.md).</span><span class="sxs-lookup"><span data-stu-id="1e083-117">For information about curried functions, see [Functions](../functions/index.md).</span></span>

## <a name="example"></a><span data-ttu-id="1e083-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="1e083-118">Example</span></span>

<span data-ttu-id="1e083-119">L’exemple de code suivant illustre la définition et l’utilisation de la valeur par défaut et les propriétés indexées par défaut qui ont get et définir des méthodes.</span><span class="sxs-lookup"><span data-stu-id="1e083-119">The following code example illustrates the definition and use of default and non-default indexed properties that have get and set methods.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a><span data-ttu-id="1e083-120">Sortie</span><span class="sxs-lookup"><span data-stu-id="1e083-120">Output</span></span>

```console
ONE two three four five six seven eight nine ten
ONE first two second three third four fourth five fifth six 6th
seven seventh eight eighth nine ninth ten tenth
```

## <a name="indexed-properties-with-multiple-index-variables"></a><span data-ttu-id="1e083-121">Propriétés indexées avec plusieurs Variables d’Index</span><span class="sxs-lookup"><span data-stu-id="1e083-121">Indexed Properties with Multiple Index Variables</span></span>

<span data-ttu-id="1e083-122">Propriétés indexées peuvent avoir plus d’une variable d’index.</span><span class="sxs-lookup"><span data-stu-id="1e083-122">Indexed properties can have more than one index variable.</span></span> <span data-ttu-id="1e083-123">Dans ce cas, les variables sont séparées par des virgules lorsque la propriété est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1e083-123">In that case, the variables are separated by commas when the property is used.</span></span> <span data-ttu-id="1e083-124">La méthode set dans une telle propriété doit avoir deux arguments curryfiés, le premier d'entre eux est un tuple qui contient les clés et le second est la valeur définie.</span><span class="sxs-lookup"><span data-stu-id="1e083-124">The set method in such a property must have two curried arguments, the first of which is a tuple containing the keys, and the second of which is the value being set.</span></span>

<span data-ttu-id="1e083-125">Le code suivant illustre l’utilisation d’une propriété indexée avec plusieurs variables d’index.</span><span class="sxs-lookup"><span data-stu-id="1e083-125">The following code demonstrates the use of an indexed property with multiple index variables.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3302.fs)]

## <a name="see-also"></a><span data-ttu-id="1e083-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e083-126">See also</span></span>

- [<span data-ttu-id="1e083-127">Membres</span><span class="sxs-lookup"><span data-stu-id="1e083-127">Members</span></span>](index.md)
