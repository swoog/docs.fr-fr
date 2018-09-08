---
title: Propriétés indexées (F#)
description: 'En savoir plus sur les propriétés indexées F #, qui sont des propriétés qui fournissent un accès de type tableau aux données classées.'
ms.date: 05/16/2016
ms.openlocfilehash: e56e4e2ea3f35df4c8ec46012357242cb6ce69f3
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44179271"
---
# <a name="indexed-properties"></a><span data-ttu-id="f2d44-103">Propriétés indexées</span><span class="sxs-lookup"><span data-stu-id="f2d44-103">Indexed Properties</span></span>

<span data-ttu-id="f2d44-104">*Propriétés indexées* propriétés qui fournissent un accès de type tableau aux sont classées les données.</span><span class="sxs-lookup"><span data-stu-id="f2d44-104">*Indexed properties* are properties that provide array-like access to ordered data.</span></span> <span data-ttu-id="f2d44-105">Ils se présentent sous trois formes :</span><span class="sxs-lookup"><span data-stu-id="f2d44-105">They come in three forms:</span></span>

* `Item`
* `Ordinal`
* `Cardinal`

<span data-ttu-id="f2d44-106">Un membre F # doit être nommé un de ces trois noms pour fournir un accès de type tableau.</span><span class="sxs-lookup"><span data-stu-id="f2d44-106">An F# member must be named one of these three names to provide array-like access.</span></span> <span data-ttu-id="f2d44-107">`IndexerName` est utilisé pour représenter l’un des trois options ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f2d44-107">`IndexerName` is used to represent any of the three options below:</span></span>

## <a name="syntax"></a><span data-ttu-id="f2d44-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2d44-108">Syntax</span></span>

```fsharp
// Indexed property that has both get and set defined.
member self-identifier.IndexerName
    with get(index-variable) =
        get-function-body
    and set index-variablesvalue-variables =
        set-function-body

// Indexed property that has get only.
member self-identifier.IndexerName(index-variable) =
    get-function-body

// Alternative syntax for indexed property with get only
member self-identifier.IndexerName
    with get(index-variables) =
        get-function-body

// Indexed property that has set only.
member self-identifier.IndexerName
    with set index-variablesvalue-variables = 
        set-function-body
```

## <a name="remarks"></a><span data-ttu-id="f2d44-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f2d44-109">Remarks</span></span>

<span data-ttu-id="f2d44-110">Les formes de la syntaxe précédente montrent comment définir des propriétés indexées qui ont les deux un `get` et un `set` (méthode), ont un `get` méthode uniquement, ou avoir un `set` méthode uniquement.</span><span class="sxs-lookup"><span data-stu-id="f2d44-110">The forms of the previous syntax show how to define indexed properties that have both a `get` and a `set` method, have a `get` method only, or have a `set` method only.</span></span> <span data-ttu-id="f2d44-111">Vous pouvez également combiner les deux la syntaxe indiquée pour get uniquement et la syntaxe indiquée pour set uniquement et produire une propriété qui possède à la fois get et set.</span><span class="sxs-lookup"><span data-stu-id="f2d44-111">You can also combine both the syntax shown for get only and the syntax shown for set only, and produce a property that has both get and set.</span></span> <span data-ttu-id="f2d44-112">Cette dernière forme vous permet de placer des modificateurs d’accessibilité différente et des attributs sur la méthode get et de définir des méthodes.</span><span class="sxs-lookup"><span data-stu-id="f2d44-112">This latter form allows you to put different accessibility modifiers and attributes on the get and set methods.</span></span>

<span data-ttu-id="f2d44-113">Lorsque le *IndexerName* est `Item`, le compilateur traite la propriété comme une propriété indexée par défaut.</span><span class="sxs-lookup"><span data-stu-id="f2d44-113">When the *IndexerName* is `Item`, the compiler treats the property as a default indexed property.</span></span> <span data-ttu-id="f2d44-114">Un *propriété indexée par défaut* est une propriété que vous pouvez accéder à l’aide de la syntaxe de type tableau sur l’instance d’objet.</span><span class="sxs-lookup"><span data-stu-id="f2d44-114">A *default indexed property* is a property that you can access by using array-like syntax on the object instance.</span></span> <span data-ttu-id="f2d44-115">Par exemple, si `obj` est un objet du type qui définit cette propriété, la syntaxe `obj.[index]` est utilisé pour accéder à la propriété.</span><span class="sxs-lookup"><span data-stu-id="f2d44-115">For example, if `obj` is an object of the type that defines this property, the syntax `obj.[index]` is used to access the property.</span></span>

<span data-ttu-id="f2d44-116">La syntaxe pour l’accès à une propriété indexée par défaut consiste à fournir le nom de la propriété et l’index entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="f2d44-116">The syntax for accessing a nondefault indexed property is to provide the name of the property and the index in parentheses.</span></span> <span data-ttu-id="f2d44-117">Par exemple, si la propriété est `Ordinal`, vous écrivez `obj.Ordinal(index)` pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="f2d44-117">For example, if the property is `Ordinal`, you write `obj.Ordinal(index)` to access it.</span></span>

<span data-ttu-id="f2d44-118">Quelle que soit la forme que vous utilisez, vous devez toujours utiliser la forme curryfiée pour la `set` méthode sur une propriété indexée.</span><span class="sxs-lookup"><span data-stu-id="f2d44-118">Regardless of which form you use, you should always use the curried form for the `set` method on an indexed property.</span></span> <span data-ttu-id="f2d44-119">Pour plus d’informations sur les fonctions curryfiées, consultez [fonctions](../functions/index.md).</span><span class="sxs-lookup"><span data-stu-id="f2d44-119">For information about curried functions, see [Functions](../functions/index.md).</span></span>

## <a name="example"></a><span data-ttu-id="f2d44-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="f2d44-120">Example</span></span>

<span data-ttu-id="f2d44-121">L’exemple de code suivant illustre la définition et l’utilisation de la valeur par défaut et les propriétés indexées par défaut qui ont get et définir des méthodes.</span><span class="sxs-lookup"><span data-stu-id="f2d44-121">The following code example illustrates the definition and use of default and non-default indexed properties that have get and set methods.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3301.fs)]

## <a name="output"></a><span data-ttu-id="f2d44-122">Sortie</span><span class="sxs-lookup"><span data-stu-id="f2d44-122">Output</span></span>

```
ONE two three four five six seven eight nine ten
ONE first two second three third four fourth five fifth six 6th
seven seventh eight eighth nine ninth ten tenth
```

## <a name="indexed-properties-with-multiple-index-variables"></a><span data-ttu-id="f2d44-123">Propriétés indexées avec plusieurs Variables d’Index</span><span class="sxs-lookup"><span data-stu-id="f2d44-123">Indexed Properties with Multiple Index Variables</span></span>

<span data-ttu-id="f2d44-124">Propriétés indexées peuvent avoir plus d’une variable d’index.</span><span class="sxs-lookup"><span data-stu-id="f2d44-124">Indexed properties can have more than one index variable.</span></span> <span data-ttu-id="f2d44-125">Dans ce cas, les variables sont séparées par des virgules lorsque la propriété est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f2d44-125">In that case, the variables are separated by commas when the property is used.</span></span> <span data-ttu-id="f2d44-126">La méthode set dans une telle propriété doit avoir deux arguments curryfiés, le premier d'entre eux est un tuple qui contient les clés et le second est la valeur définie.</span><span class="sxs-lookup"><span data-stu-id="f2d44-126">The set method in such a property must have two curried arguments, the first of which is a tuple containing the keys, and the second of which is the value being set.</span></span>

<span data-ttu-id="f2d44-127">Le code suivant illustre l’utilisation d’une propriété indexée avec plusieurs variables d’index.</span><span class="sxs-lookup"><span data-stu-id="f2d44-127">The following code demonstrates the use of an indexed property with multiple index variables.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet3302.fs)]

## <a name="see-also"></a><span data-ttu-id="f2d44-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d44-128">See also</span></span>

- [<span data-ttu-id="f2d44-129">Membres</span><span class="sxs-lookup"><span data-stu-id="f2d44-129">Members</span></span>](index.md)
