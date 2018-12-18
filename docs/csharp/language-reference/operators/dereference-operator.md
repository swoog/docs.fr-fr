---
title: -&gt;, opérateur - Référence C#
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: bb1ccd026f403e68565c5c7681943d8017578d01
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53234888"
---
# <a name="-gt-operator-c-reference"></a>-&gt;, opérateur (Référence C#)

L’opérateur d’accès au membre pointeur `->` combine l’accès au membre et l’indirection du pointeur.

Si `x` est un pointeur de type `T*` et `y` un membre accessible de `T`, une expression de la forme :

```csharp
x->y
```

est équivalent à

```csharp
(*x).y
```

L’opérateur `->` réclame un contexte [unsafe](../keywords/unsafe.md).

Pour plus d’informations, voir [Guide pratique : accéder à un membre avec un pointeur](../../programming-guide/unsafe-code-pointers/how-to-access-a-member-with-a-pointer.md).

## <a name="operator-overloadability"></a>Capacité de surcharge de l’opérateur

L’opérateur `->` ne peut pas être surchargé.

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, voir la section [Accès au membre pointeur](~/_csharplang/spec/unsafe-code.md#pointer-member-access) de la [spécification du langage C#](../language-specification/index.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
- [Types de pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md)
