---
title: Syntaxe détaillée (F#)
description: 'Découvrez la différence entre la syntaxe détaillée et légère dans le langage de programmation F #.'
ms.date: 05/16/2016
ms.openlocfilehash: b4f2354738da4692cb444e5e7dd9531d80d26664
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2018
ms.locfileid: "45589311"
---
# <a name="verbose-syntax"></a>Syntaxe détaillée

Il existe deux formes de syntaxe disponibles pour de nombreuses constructions dans le langage F # : *syntaxe détaillée* et *syntaxe simplifiée*. La syntaxe détaillée n’est pas aussi couramment utilisée, mais présente l’avantage d’être moins sensibles à la mise en retrait. La syntaxe simplifiée est plus courte et utilise la mise en retrait pour signaler le début et la fin de constructions, plutôt que mots clés supplémentaires comme `begin`, `end`, `in`, et ainsi de suite. La syntaxe par défaut est la syntaxe simplifiée. Cette rubrique décrit la syntaxe des constructions F # lorsque la syntaxe simplifiée n’est pas activée. La syntaxe détaillée est toujours activée, même si vous activez la syntaxe simplifiée, vous pouvez toujours utiliser la syntaxe détaillée pour certaines constructions. Vous pouvez désactiver la syntaxe simplifiée à l’aide de la `#light "off"` directive.

## <a name="table-of-constructs"></a>Tableau de constructions

Le tableau suivant présente la syntaxe simplifiée et détaillée pour les constructions de langage F # dans des contextes où il existe une différence entre les deux formes. Dans ce tableau, les crochets pointus (&lt;&gt;) placez des éléments de syntaxe fourni par l’utilisateur. Reportez-vous à la documentation pour chaque construction de langage pour des informations plus détaillées sur la syntaxe utilisée dans ces constructions.

<table>
<tr>
<th>Construction de langage</th>
<th>Syntaxe simplifiée</th>
<th>Syntaxe détaillée</th>
</tr>
<tr>
<td>
expressions composées
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


imbriquée `let` liaisons

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
bloc de code
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
<tr><td>Enregistrement
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
<tr><td>class
</td><td>
```
type <class-name>(<params>) = ... ```

</td><td>

```
type <class-name>(<params>) =
    class
        ...
    end
```
</td>
</tr>
<tr><td>structure</td><td>

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
<tr><td>union discriminée</td><td>

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
<tr><td>interface</td><td>

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
<tr><td>expression d’objet</td><td>

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
<tr><td>implémentation de l'interface</td><td>

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
<tr><td>extension de type</td><td>

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
<tr><td>module</td><td>

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

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
- [Directives de compilateur](compiler-directives.md)
- [Indications pour la mise en forme du code](code-formatting-guidelines.md)
