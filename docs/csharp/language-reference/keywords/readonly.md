---
title: readonly, mot clé (référence C#)
ms.date: 06/21/2018
f1_keywords:
- readonly_CSharpKeyword
- readonly
helpviewer_keywords:
- readonly keyword [C#]
ms.assetid: 2f8081f6-0de2-4903-898d-99696c48d2f4
ms.openlocfilehash: d09ce4ea972a3064298eebdf0b8b80999ee8441e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44227283"
---
# <a name="readonly-c-reference"></a>readonly (référence C#)

Le mot clé `readonly` est un modificateur qui peut être utilisé dans trois contextes :

- Dans une [déclaration de champ](#readonly-field-example), `readonly` indique qu’une affectation à destination d’un champ peut survenir uniquement dans le cadre de la déclaration ou dans un constructeur de la même classe.
- Dans une définition [`readonly struct`](#readonly-struct-example), `readonly` indique que le `struct` est immuable.
- Dans un [`ref readonly`retour de la méthode](#ref-readonly-return-example), le modificateur `readonly` indique que la méthode retourne une référence et que les écritures ne sont pas autorisés pour cette référence.

Les deux contextes finaux ont été ajoutés dans C# 7.2.

## <a name="readonly-field-example"></a>Exemple de champ en lecture seule

Dans cet exemple, la valeur du champ `year` ne peut pas être modifiée dans la méthode `ChangeYear`, même si une valeur lui est affectée dans le constructeur de classe :

[!code-csharp[Readonly Field example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyField)]

Vous pouvez affecter une valeur à un champ `readonly` uniquement dans les contextes suivants :

- Lorsque la variable est initialisée dans la déclaration, par exemple :

```csharp
public readonly int y = 5;
```

- Dans un constructeur d’instance de la classe qui contient la déclaration de champ d’instance.
- Dans le constructeur statique de la classe qui contient la déclaration de champ statique.

Ces contextes de constructeur sont aussi les seuls contextes dans lesquels il est possible de passer un champ `readonly` comme paramètre [out](out-parameter-modifier.md) ou [ref](ref.md).

> [!NOTE]
> Le mot clé `readonly` est différent du mot clé [const](const.md). Un champ `const` ne peut être initialisé qu'au moment de la déclaration du champ. Un champ `readonly` peut être initialisé dans la déclaration ou dans un constructeur. C'est pourquoi, les champs `readonly` peuvent avoir des valeurs différentes en fonction du constructeur utilisé. De même, alors qu’un champ `const` est une constante au moment de la compilation, le champ `readonly` peut être utilisé pour des constantes au moment de l’exécution, comme dans l’exemple suivant :

```csharp
public static readonly uint timeStamp = (uint)DateTime.Now.Ticks;
```

[!code-csharp[Initialize readonly Field example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#InitReadonlyField)]

Dans l’exemple précédent, si vous utilisez une instruction telle que dans l’exemple suivant :

`p2.y = 66;        // Error`

vous obtenez le message d’erreur du compilateur :

`A readonly field cannot be assigned to (except in a constructor or a variable initializer)`

## <a name="readonly-struct-example"></a>Exemple de struct readonly

Le modificateur `readonly` dans une définition `struct` déclare que le struct est **immuable**. Chaque champ d’instance du `struct` doit être marqué `readonly`, comme dans l’exemple suivant :

[!code-csharp[readonly struct example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyStruct)]

L’exemple précédent utilise les [propriétés automatiques readonly](../../properties.md#read-only) pour déclarer son stockage. Il donne l’instruction au compilateur de créer des champs de stockage `readonly` pour ces propriétés. Vous pouvez aussi déclarer des champs `readonly` directement :

```csharp
public readonly struct Point
{
    public readonly double X;
    public readonly double Y;

    public Point(double x, double y) => (X, Y) = (x, y);

    public override string ToString() => $"({X}, {Y})";
}
```

L’ajout d’un champ non marqué `readonly` génère l’erreur `CS8340` du compilateur : « Les champs d’instance de structs readonly doivent être en lecture seule ».

## <a name="ref-readonly-return-example"></a>Exemple de retour ref readonly

Le modificateur `readonly` au niveau d’un `ref return` indique que la référence retournée ne peut pas être modifiée. L’exemple suivant retourne une référence à l’origine. Il utilise le modificateur `readonly` pour indiquer que les appelants ne peuvent pas modifier l’origine :

[!code-csharp[readonly struct example](~/samples/snippets/csharp/keywords/ReadonlyKeywordExamples.cs#ReadonlyReturn)]
Le type retourné ne doit pas nécessairement être un `readonly struct`. Tout type pouvant être retourné par `ref` peut être retourné par `ref readonly`.

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Modificateurs](modifiers.md)
- [const](const.md)
- [Champs](../../programming-guide/classes-and-structs/fields.md)
