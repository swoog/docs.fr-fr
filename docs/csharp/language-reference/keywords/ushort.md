---
title: ushort, mot clé - Référence C#
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- ushort
- ushort_CSharpKeyword
helpviewer_keywords:
- ushort keyword [C#]
ms.assetid: 1a7dbaae-b7a0-4111-872a-c88a6d3981ac
ms.openlocfilehash: 934e25576a8a24c176a54ec6af984459b513fe5a
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53614455"
---
# <a name="ushort-c-reference"></a>ushort (référence C#)

Le mot clé `ushort` indique un type de données intégral qui stocke des valeurs selon la taille et la plage indiquées dans le tableau suivant.

|Type|Plage|Size|Type .NET|
|----------|-----------|----------|-------------------------|
|`ushort`|0 à 65 535|Entier 16 bits non signé|<xref:System.UInt16?displayProperty=nameWithType>|

## <a name="literals"></a>Littéraux

Vous pouvez déclarer et initialiser une variable `ushort` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0). Si le littéral entier est en dehors de la plage autorisée pour le type `ushort` (autrement dit, s’il est inférieur à <xref:System.UInt16.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt16.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.

Dans l’exemple suivant, les entiers égaux à 65 034 représentés comme des littéraux décimaux, hexadécimaux et binaires sont implicitement convertis à partir de valeurs [int](int.md) en `ushort`.

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShort)]

> [!NOTE]
> Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire. Les littéraux décimaux n’ont pas de préfixe.

À partir de C# 7.0, quelques fonctionnalités ont été ajoutées pour améliorer la lisibilité :

- C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.
- C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe. Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.

Voici quelques exemples.

[!code-csharp[UShort](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UShortS)]

## <a name="compiler-overload-resolution"></a>Résolution de surcharge du compilateur

Vous devez utiliser un cast lors de l’appel de méthodes surchargées. Prenons l’exemple des méthodes surchargées suivantes ayant pour paramètres `ushort` et [int](int.md) :

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(ushort s) {}
```

L’utilisation du cast `ushort` garantit l’appel du type correct, par exemple :

```csharp
// Calls the method with the int parameter:
SampleMethod(5);
// Calls the method with the ushort parameter:
SampleMethod((ushort)5);
```

## <a name="conversions"></a>Conversions

Il existe une conversion implicite prédéfinie de `ushort` en [int](int.md), [uint](uint.md), [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md) ou [decimal](decimal.md).

Il existe une conversion implicite prédéfinie de [byte](byte.md) ou [char](char.md) en `ushort`. Sinon, vous devez utiliser un cast pour effectuer une conversion explicite. Considérons, par exemple, les deux variables `ushort` `x` et `y` suivantes :

```csharp
ushort x = 5, y = 12;
```

L’instruction d’assignation suivante entraîne une erreur de compilation, car l’expression arithmétique située à droite de l’opérateur d’assignation donne la valeur `int` par défaut.

```csharp
ushort z = x + y;   // Error: conversion from int to ushort
```

Pour corriger ce problème, utilisez un cast :

```csharp
ushort z = (ushort)(x + y);   // OK: explicit conversion
```

Il est cependant possible d’utiliser les instructions suivantes dans lesquelles la variable de destination a une taille de stockage égale ou supérieure :

```csharp
int m = x + y;
long n = x + y;
```

Notez aussi qu’il n’existe pas de conversion implicite des types virgule flottante en `ushort`. Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :

```csharp
// Error -- no implicit conversion from double:
ushort x = 3.0;
// OK -- explicit conversion:
ushort y = (ushort)3.0;
```

Pour plus d’informations sur les expressions arithmétiques dans lesquelles coexistent des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).

Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.

## <a name="see-also"></a>Voir aussi

- <xref:System.UInt16>
- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Tableau des types intégraux](integral-types-table.md)
- [Tableau des types intégrés](built-in-types-table.md)
- [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md)
- [Tableau des conversions numériques explicites](explicit-numeric-conversions-table.md)
