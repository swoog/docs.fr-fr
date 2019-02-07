---
title: ->, opérateur - Référence C#
ms.custom: seodec18
ms.date: 11/26/2018
f1_keywords:
- ->_CSharpKeyword
helpviewer_keywords:
- member access operator (->) [C#]
- -> operator [C#]
ms.assetid: e39ccdc1-f1ff-4a92-bf1d-ac2c8c11316a
ms.openlocfilehash: be74f02a85aa05cdab32768ed38222fc4d9289b1
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55255365"
---
# <a name="--operator-c-reference"></a>->, opérateur (référence C#)

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
