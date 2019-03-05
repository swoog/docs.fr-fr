---
title: '[], opérateur - Référence C#'
ms.custom: seodec18
ms.date: 01/10/2019
f1_keywords:
- '[]_CSharpKeyword'
helpviewer_keywords:
- subscript operator [C#]
- square brackets [ ] operator [C#]
- '[] operator [C#]'
- indexing operator [C#]
ms.assetid: 5c16bb45-88f7-45ff-b42c-1af1972b042c
ms.openlocfilehash: 9088393f61d300ee76e56e320bec17b4a79bfebb
ms.sourcegitcommit: bd28ff1e312eaba9718c4f7ea272c2d4781a7cac
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/26/2019
ms.locfileid: "56835588"
---
# <a name="-operator-c-reference"></a>[], opérateur (référence C#)

Les crochets, `[]`, sont généralement utilisés pour l’accès à un élément tableau, indexeur ou pointeur.

Pour plus d’informations sur l’accès aux éléments pointeur, consultez [Guide pratique pour accéder à un élément de tableau à l’aide d’un pointeur](../../programming-guide/unsafe-code-pointers/how-to-access-an-array-element-with-a-pointer.md).

Vous utilisez également des crochets pour spécifier des [attributs](../../programming-guide/concepts/attributes/index.md) :

```csharp
[System.Diagnostics.Conditional("DEBUG")]
void TraceMethod() {}
```

## <a name="array-access"></a>Accès aux tableaux

L’exemple suivant montre comment accéder à des éléments tableau :

[!code-csharp-interactive[array access](~/samples/snippets/csharp/language-reference/operators/IndexOperatorExamples.cs#Arrays)]

Si un index de tableau est en dehors des limites de la dimension correspondante d’un tableau, une <xref:System.IndexOutOfRangeException> est levée.

Comme le montre l’exemple précédent, vous utilisez également des crochets dans la déclaration d’un type tableau et l’instanciation des instances de tableau.

Pour plus d’informations sur les tableaux, consultez [Tableaux](../../programming-guide/arrays/index.md).

## <a name="indexer-access"></a>Accès aux indexeurs

L’exemple suivant utilise le type .NET <xref:System.Collections.Generic.Dictionary%602> afin d’illustrer l’accès aux indexeurs :

[!code-csharp-interactive[indexer access](~/samples/snippets/csharp/language-reference/operators/IndexOperatorExamples.cs#Indexers)]

Les indexeurs vous permettent d’indexer des instances d’un type défini par l’utilisateur en procédant de la même façon que pour l’indexation de tableau. Contrairement aux index de tableau, qui doivent être des entiers, les arguments d’indexeur peuvent être déclarés comme étant de n’importe quel type.

Pour plus d’informations sur les indexeurs, consultez [Indexeurs](../../programming-guide/indexers/index.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

L’opérateur d’accès à un élément `[]` n’est pas considéré comme un opérateur surchargeable. Utilisez des [indexeurs](../../programming-guide/indexers/index.md) pour prendre en charge l’indexation avec des types définis par l’utilisateur.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez les sections [Accès à un élément](~/_csharplang/spec/expressions.md#element-access) et [Accès aux éléments de pointeur](~/_csharplang/spec/unsafe-code.md#pointer-element-access) de la [Spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Tableaux](../../programming-guide/arrays/index.md)
- [Indexeurs](../../programming-guide/indexers/index.md)
- [Types de pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md)
- [Attributs](../../programming-guide/concepts/attributes/index.md)
- [Opérateurs ?. et ?[]](null-conditional-operators.md)