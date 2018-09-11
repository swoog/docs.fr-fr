---
title: Syntaxe détaillée (F#)
description: 'Découvrez la différence entre la syntaxe détaillée et légère dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: b4f2354738da4692cb444e5e7dd9531d80d26664
ms.sourcegitcommit: 8c2ece71e54f46aef9a2153540d0bda7e74b19a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/11/2018
ms.locfileid: "44367940"
---
# <a name="verbose-syntax"></a><span data-ttu-id="04fc4-103">Syntaxe détaillée</span><span class="sxs-lookup"><span data-stu-id="04fc4-103">Verbose Syntax</span></span>

<span data-ttu-id="04fc4-104">Il existe deux formes de syntaxe disponibles pour de nombreuses constructions dans le langage F # : *syntaxe détaillée* et *syntaxe simplifiée*.</span><span class="sxs-lookup"><span data-stu-id="04fc4-104">There are two forms of syntax available for many constructs in the F# language: *verbose syntax* and *lightweight syntax*.</span></span> <span data-ttu-id="04fc4-105">La syntaxe détaillée n’est pas aussi couramment utilisée, mais présente l’avantage d’être moins sensibles à la mise en retrait.</span><span class="sxs-lookup"><span data-stu-id="04fc4-105">The verbose syntax is not as commonly used, but has the advantage of being less sensitive to indentation.</span></span> <span data-ttu-id="04fc4-106">La syntaxe simplifiée est plus courte et utilise la mise en retrait pour signaler le début et la fin de constructions, plutôt que mots clés supplémentaires comme `begin`, `end`, `in`, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="04fc4-106">The lightweight syntax is shorter and uses indentation to signal the beginning and end of constructs, rather than additional keywords like `begin`, `end`, `in`, and so on.</span></span> <span data-ttu-id="04fc4-107">La syntaxe par défaut est la syntaxe simplifiée.</span><span class="sxs-lookup"><span data-stu-id="04fc4-107">The default syntax is the lightweight syntax.</span></span> <span data-ttu-id="04fc4-108">Cette rubrique décrit la syntaxe des constructions F # lorsque la syntaxe simplifiée n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="04fc4-108">This topic describes the syntax for F# constructs when lightweight syntax is not enabled.</span></span> <span data-ttu-id="04fc4-109">La syntaxe détaillée est toujours activée, même si vous activez la syntaxe simplifiée, vous pouvez toujours utiliser la syntaxe détaillée pour certaines constructions.</span><span class="sxs-lookup"><span data-stu-id="04fc4-109">Verbose syntax is always enabled, so even if you enable lightweight syntax, you can still use verbose syntax for some constructs.</span></span> <span data-ttu-id="04fc4-110">Vous pouvez désactiver la syntaxe simplifiée à l’aide de la `#light "off"` directive.</span><span class="sxs-lookup"><span data-stu-id="04fc4-110">You can disable lightweight syntax by using the `#light "off"` directive.</span></span>

## <a name="table-of-constructs"></a><span data-ttu-id="04fc4-111">Tableau de constructions</span><span class="sxs-lookup"><span data-stu-id="04fc4-111">Table of Constructs</span></span>

<span data-ttu-id="04fc4-112">Le tableau suivant présente la syntaxe simplifiée et détaillée pour les constructions de langage F # dans des contextes où il existe une différence entre les deux formes.</span><span class="sxs-lookup"><span data-stu-id="04fc4-112">The following table shows the lightweight and verbose syntax for F# language constructs in contexts where there is a difference between the two forms.</span></span> <span data-ttu-id="04fc4-113">Dans ce tableau, les crochets pointus (&lt;&gt;) placez des éléments de syntaxe fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04fc4-113">In this table, angle brackets (&lt;&gt;) enclose user-supplied syntax elements.</span></span> <span data-ttu-id="04fc4-114">Reportez-vous à la documentation pour chaque construction de langage pour des informations plus détaillées sur la syntaxe utilisée dans ces constructions.</span><span class="sxs-lookup"><span data-stu-id="04fc4-114">Refer to the documentation for each language construct for more detailed information about the syntax used within these constructs.</span></span>

<table>
<tr>
<th><span data-ttu-id="04fc4-115">Construction de langage</span><span class="sxs-lookup"><span data-stu-id="04fc4-115">Language construct</span></span></th>
<th><span data-ttu-id="04fc4-116">Syntaxe simplifiée</span><span class="sxs-lookup"><span data-stu-id="04fc4-116">Lightweight syntax</span></span></th>
<th><span data-ttu-id="04fc4-117">Syntaxe détaillée</span><span class="sxs-lookup"><span data-stu-id="04fc4-117">Verbose syntax</span></span></th>
</tr>
<tr>
<td>
<span data-ttu-id="04fc4-118">expressions composées</span><span class="sxs-lookup"><span data-stu-id="04fc4-118">compound expressions</span></span>
</td>
<td>

```xml
<expression1>
<expression2>
```
</td><td>

```
<expression1>; <expression2>
```

</td>
</tr>
<tr><td>


<span data-ttu-id="04fc4-119">imbriquée `let` liaisons</span><span class="sxs-lookup"><span data-stu-id="04fc4-119">nested `let` bindings</span></span>

</td><td>
```
let f x =
    let a = 1
    let b = 2
    x + a + b
```

</td><td>

```
let f x =
    let a = 1 in
    let b = 2 in
    x + a + b
```

</td>
</tr>
<tr><td>
<span data-ttu-id="04fc4-120">bloc de code</span><span class="sxs-lookup"><span data-stu-id="04fc4-120">code block</span></span>
</td><td>

```
(
    <expression1>
    <expression2>
)
```

</td><td>

```
begin
    <expression1>;
    <expression2>;
end
```
</td>
</tr>
<tr><td>
`for...do`
</td><td>

```
for counter = start to finish do
    ...
```

</td><td>

```
for counter = start to finish do
    ...
done
```

</td>
</tr>
<tr><td>
`while...do`
</td><td>

```
while <condition> do
    ...
```

</td><td>

```
while <condition> do
    ...
done
```

</td>
</tr>
<tr><td>
`for...in`
</td><td>

```
for var in start .. finish do
    ...
```

</td><td>

```
for var in start .. finish do
    ...
done
```

</td>
</tr>
<tr><td>
`do`
</td><td>

```
do
    ...
```

</td><td>

```
do
    ...
in
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-121">Enregistrement</span><span class="sxs-lookup"><span data-stu-id="04fc4-121">record</span></span>
</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    <value-or-member-definitions>
```

</td><td>

```
type <record-name> =
    {
        <field-declarations>
    }
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-122">class</span><span class="sxs-lookup"><span data-stu-id="04fc4-122">class</span></span>
</td><td><span data-ttu-id="04fc4-123">
```
type <class-name>(<params>) = ... ```

</span><span class="sxs-lookup"><span data-stu-id="04fc4-123">
```
type <class-name>(<params>) = ... ```

</span></span></td><td>

```
type <class-name>(<params>) =
    class
        ...
    end
```
</td>
</tr>
<tr><td><span data-ttu-id="04fc4-124">structure</span><span class="sxs-lookup"><span data-stu-id="04fc4-124">structure</span></span></td><td>

```
[<StructAttribute>]
type <structure-name> =
    ...
```
</td><td>

```
type <structure-name> =
    struct
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-125">union discriminée</span><span class="sxs-lookup"><span data-stu-id="04fc4-125">discriminated union</span></span></td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    <value-or-member definitions>
```
</td><td>

```
type <union-name> =
    | ...
    | ...
    ...
    with
        <value-or-member-definitions>
    end    
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-126">interface</span><span class="sxs-lookup"><span data-stu-id="04fc4-126">interface</span></span></td><td>

```
type <interface-name> =
    ...
```
</td><td>

```
type <interface-name> =
    interface
        ...
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-127">expression d’objet</span><span class="sxs-lookup"><span data-stu-id="04fc4-127">object expression</span></span></td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
        <interface-implementations>
}
```

</td><td>

```
{ new <type-name>
    with
        <value-or-member-definitions>
    end
    <interface-implementations>
}
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-128">implémentation de l'interface</span><span class="sxs-lookup"><span data-stu-id="04fc4-128">interface implementation</span></span></td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
interface <interface-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-129">extension de type</span><span class="sxs-lookup"><span data-stu-id="04fc4-129">type extension</span></span></td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
```

</td><td>

```
type <type-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td><span data-ttu-id="04fc4-130">module</span><span class="sxs-lookup"><span data-stu-id="04fc4-130">module</span></span></td><td>

```
module <module-name> =
    ...
```

</td><td>

```
module <module-name> =
    begin
        ...
    end
```

</td>
</tr>
</table>

## <a name="see-also"></a><span data-ttu-id="04fc4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04fc4-131">See also</span></span>

- [<span data-ttu-id="04fc4-132">Informations de référence du langage F#</span><span class="sxs-lookup"><span data-stu-id="04fc4-132">F# Language Reference</span></span>](index.md)
- [<span data-ttu-id="04fc4-133">Directives de compilateur</span><span class="sxs-lookup"><span data-stu-id="04fc4-133">Compiler Directives</span></span>](compiler-directives.md)
- [<span data-ttu-id="04fc4-134">Indications pour la mise en forme du code</span><span class="sxs-lookup"><span data-stu-id="04fc4-134">Code Formatting Guidelines</span></span>](code-formatting-guidelines.md)
