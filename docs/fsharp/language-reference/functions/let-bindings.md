---
title: Liaisons let
description: Découvrez comment utiliser un F# 'let' liaison, qui associe un identificateur à une valeur ou une fonction.
ms.date: 05/16/2016
ms.openlocfilehash: 45de82acf6f4423698cd8037266968e023f40dcb
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53612671"
---
# <a name="let-bindings"></a>Liaisons let

Un *liaison* associe un identificateur à une valeur ou une fonction. Vous utilisez le `let` mot clé à lier un nom à une valeur ou une fonction.

## <a name="syntax"></a>Syntaxe

```fsharp
// Binding a value:
let identifier-or-pattern [: type] =expressionbody-expression
// Binding a function value:
let identifier parameter-list [: return-type ] =expressionbody-expression
```

## <a name="remarks"></a>Notes

Le `let` mot clé est utilisé dans les expressions pour définir des valeurs ou des valeurs de fonction pour un ou plusieurs noms de liaison. La forme la plus simple du `let` expression lie un nom à une valeur simple, comme suit.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1101.fs)]

Si vous séparez l’expression de l’identificateur à l’aide d’une nouvelle ligne, vous devez mettre en retrait chaque ligne de l’expression, comme dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1102.fs)]

Au lieu de simplement un nom, vous pouvez spécifier un modèle qui contient les noms, par exemple, un tuple, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1103.fs)]

Le *expression de corps* est l’expression dans laquelle les noms sont utilisés. L’expression de corps apparaît sur sa propre ligne, mise en retrait de ligne exactement avec le premier caractère dans le `let` mot clé :

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1104.fs)]

Un `let` liaison peut apparaître qu’au niveau du module, dans la définition d’un type de classe, ou dans des portées locales, par exemple dans une définition de fonction. Un `let` liaison au niveau d’un module ou d’un type de classe supérieur est inutile d’avoir une expression de corps, mais à d’autres niveaux de portée, l’expression de corps est obligatoire. Les noms liés sont utilisables après le point de définition, mais pas à tout moment avant le `let` liaison s’affiche, comme cela est illustré dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1105.fs)]

## <a name="function-bindings"></a>Liaisons de fonction

Liaisons de fonction suivent les règles pour les liaisons de valeur, à ceci près que les liaisons de fonction incluent le nom de fonction et les paramètres, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1106.fs)]

En règle générale, les paramètres sont des modèles, tels que d’un modèle de tuple :

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1107.fs)]

Un `let` expression de liaison prend la valeur de la dernière expression. Par conséquent, dans l’exemple de code suivant, la valeur de `result` est calculée à partir de `100 * function3 (1, 2)`, qui prend la valeur `300`.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1109.fs)]

Pour plus d’informations, consultez [Fonctions](index.md).

## <a name="type-annotations"></a>Annotations de type

Vous pouvez spécifier les types des paramètres en incluant un signe deux-points ( :).) suivi d’un nom de type, tout entre parenthèses. Vous pouvez également spécifier le type de la valeur de retour en ajoutant le signe deux-points et le type après le dernier paramètre. Les annotations de type complet pour `function1`, avec des entiers comme types de paramètre, se présente comme suit.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1108.fs)]

Lorsqu’il n’y a aucun paramètre de type explicite, l’inférence de type est utilisé pour déterminer les types de paramètres de fonctions. Cela peut inclure la généralisation automatique du type d’un paramètre générique.

Pour plus d’informations, consultez [généralisation automatique](../generics/automatic-generalization.md) et [l’inférence de Type](../type-inference.md).

## <a name="let-bindings-in-classes"></a>Liaisons let dans des classes

Un `let` liaison peut apparaître dans un type de classe, mais pas dans une structure ou un type d’enregistrement. Pour utiliser une liaison let dans un type de classe, la classe doit avoir un constructeur principal. Les paramètres de constructeur doivent apparaître après le nom de type dans la définition de classe. Un `let` liaison dans un type de classe définit les champs privés et les membres de ce type de classe et, conjointement avec `do` liaisons dans le type, le code pour le constructeur principal pour le type de formulaires. Les exemples de code suivants montrent une classe `MyClass` avec les champs privés `field1` et `field2`.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1110.fs)]

Les étendues de `field1` et `field2` sont limitées au type dans lequel ils sont déclarés. Pour plus d’informations, consultez [ `let` liaisons dans les Classes](../members/let-bindings-in-classes.md) et [Classes](../classes.md).

## <a name="type-parameters-in-let-bindings"></a>Paramètres de type dans les liaisons let

Un `let` liaison au niveau du module, dans un type, ou dans une expression de calcul peut avoir des paramètres de type explicite. Une liaison let dans une expression, comme dans une définition de fonction ne peut pas avoir de paramètres de type. Pour plus d’informations, consultez la page [Génériques](../generics/index.md).

## <a name="attributes-on-let-bindings"></a>Attributs sur les liaisons let

Attributs peuvent être appliqués au niveau supérieur `let` liaisons dans un module, comme indiqué dans le code suivant.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-1/snippet1111.fs)]

## <a name="scope-and-accessibility-of-let-bindings"></a>Portée et l’accessibilité des liaisons Let

L’étendue d’une entité déclarée avec une liaison let est limitée à la partie de l’objet contenant l’étendue (par exemple, une fonction, module, fichier ou classe) une fois que la liaison s’affiche. Par conséquent, il peut être désignée qu’une liaison let introduit un nom dans une étendue. Dans un module, une valeur liée aux let ou une fonction est accessible aux clients d’un module tant que le module est accessible, étant donné que les liaisons let dans un module sont compilés dans des fonctions publiques du module. En revanche, les liaisons let dans une classe sont privés à la classe.

Normalement, les fonctions dans les modules doivent être qualifiées par le nom du module lorsqu’il est utilisé par le code client. Par exemple, si un module `Module1` possède une fonction `function1`, spécifient les utilisateurs `Module1.function1` pour faire référence à la fonction.

Les utilisateurs d’un module peuvent utiliser une déclaration d’importation pour rendre les fonctions au sein de ce module disponibles pour une utilisation sans ne soient pas qualifiées par le nom du module. Dans l’exemple mentionné, les utilisateurs du module peuvent dans ce cas ouvrir le module à l’aide de l’ouverture de déclaration d’importation `Module1` et par la suite, reportez-vous à `function1` directement.

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

Certains modules ont l’attribut [RequireQualifiedAccess](https://msdn.microsoft.com/library/8b9b6ade-0471-4413-ac5d-638cd0de5f15), ce qui signifie que les fonctions qu’ils exposent doivent être qualifiées avec le nom du module. Par exemple, le F# module List a cet attribut.

Pour plus d’informations sur les modules et contrôle d’accès, consultez [Modules](../modules.md) et [contrôle d’accès](../access-control.md).

## <a name="see-also"></a>Voir aussi

- [Fonctions](index.md)
- [Liaisons `let` dans des classes](../members/let-bindings-in-classes.md)