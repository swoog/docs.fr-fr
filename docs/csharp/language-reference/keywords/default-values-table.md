---
title: Tableau des valeurs par défaut - Référence C#
ms.custom: seodec18
description: Découvrez quelles sont les valeurs par défaut des types valeur C#.
ms.date: 08/23/2018
helpviewer_keywords:
- constructors [C#], return values
- keywords [C#], new
- default constructor [C#]
- defaults [C#]
- value types [C#], initializing
- variables [C#], value types
- constructors [C#], default constructor
- types [C#], default constructor return values
ms.openlocfilehash: 19e9e4f94ab573f2313c185a08192d89103b98fd
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53237036"
---
# <a name="default-values-table-c-reference"></a>Tableau des valeurs par défaut (référence C#)

Le tableau suivant présente les valeurs par défaut des [types valeur](value-types.md).

|Type de valeur|Valeur par défaut|
|----------------|-------------------|
|[bool](bool.md)|`false`|
|[byte](byte.md)|0|
|[char](char.md)|'\0'|
|[decimal](decimal.md)|0M|
|[double](double.md)|0.0D|
|[enum](enum.md)|Valeur produite par l’expression `(E)0`, où `E` est l’identificateur de l’enum.|
|[float](float.md)|0.0F|
|[int](int.md)|0|
|[long](long.md)|0L|
|[sbyte](sbyte.md)|0|
|[short](short.md)|0|
|[struct](struct.md)|Valeur produite en affectant à tous les champs de type valeur leur valeur par défaut et à tous les champs de type référence la valeur `null`.|
|[uint](uint.md)|0|
|[ulong](ulong.md)|0|
|[ushort](ushort.md)|0|

## <a name="remarks"></a>Notes

Vous ne pouvez pas utiliser des variables non initialisées en C#. Vous pouvez initialiser une variable avec la valeur par défaut de son type. Vous pouvez également utiliser la valeur par défaut d’un type pour spécifier la valeur par défaut de l’[argument facultatif](../../programming-guide/classes-and-structs/named-and-optional-arguments.md#optional-arguments) d’une méthode.

Utilisez l’[expression de valeur par défaut](../../programming-guide/statements-expressions-operators/default-value-expressions.md) pour produire la valeur par défaut d’un type, comme illustré dans l’exemple suivant :

```csharp
int a = default(int);
```

À compter de C# 7.1, vous pouvez utiliser le [littéral `default`](../../programming-guide/statements-expressions-operators/default-value-expressions.md#default-literal-and-type-inference) pour initialiser une variable avec la valeur par défaut de son type :

```csharp
int a = default;
```

Vous pouvez également utiliser le constructeur par défaut ou le constructeur par défaut implicite pour produire la valeur par défaut d’un type valeur, comme illustré dans l’exemple suivant. Pour plus d’informations sur les constructeurs, consultez l’article [Constructeurs](../../programming-guide/classes-and-structs/constructors.md).

```csharp
int a = new int();
```

La valeur par défaut de tout [type référence](reference-types.md) est `null`. La valeur par défaut d’un [type nullable](../../programming-guide/nullable-types/index.md) est une instance pour laquelle la propriété <xref:System.Nullable%601.HasValue%2A> est `false` et la propriété <xref:System.Nullable%601.Value%2A> n’est pas définie.

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Tableaux de référence des types](reference-tables-for-types.md)
- [Types valeur](value-types.md)
- [Tableau des types valeur](value-types-table.md)
- [Tableaux des types intégrés](built-in-types-table.md)
