---
title: uint, mot clé - Référence C#
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- uint
- uint_CSharpKeyword
helpviewer_keywords:
- uint keyword [C#]
ms.openlocfilehash: 9a60460f67f9b6cf0b57d40ebf2789536e870d75
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633144"
---
# <a name="uint-c-reference"></a>uint (référence C#)

Le mot clé `uint` désigne un type intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.

|Type|Plage|Size|Type .NET|
|----------|-----------|----------|-------------------------|
|`uint`|de 0 à 4 294 967 295|Entier 32 bits non signé|<xref:System.UInt32?displayProperty=nameWithType>|

**Note** Le type `uint` n’est pas conforme CLS. Utilisez `int` autant que possible.

## <a name="literals"></a>Littéraux

Vous pouvez déclarer et initialiser une variable `uint` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0). Si le littéral entier est en dehors de la plage autorisée pour le type `uint` (autrement dit, s’il est inférieur à <xref:System.UInt32.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt32.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.

Dans l’exemple suivant, les entiers égaux à 3 000 000 000 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `uint`.

[!code-csharp[uint](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UInt)]

> [!NOTE]
> Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire. Les littéraux décimaux n’ont pas de préfixe.

À partir de C# 7.0, quelques fonctionnalités ont été ajoutées pour améliorer la lisibilité :

- C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.
- C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe. Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.

Voici quelques exemples.

[!code-csharp[uint](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#UIntS)]

Les littéraux entiers peuvent également inclure un suffixe qui désigne le type. Le suffixe `U` ou « u » désigne un type `uint` ou `ulong`, selon la valeur numérique du littéral. L’exemple suivant utilise le suffixe `u` pour désigner un entier non signé des deux types. Notez que le premier littéral est un type `uint`, car sa valeur est inférieure à <xref:System.UInt32.MaxValue?displayProperty=nameWithType>, tandis que le deuxième est un type `ulong`, car sa valeur est supérieure à <xref:System.UInt32.MaxValue?displayProperty=nameWithType>.

[!code-csharp[usuffix](~/samples/snippets/csharp/language-reference/keywords/numeric-suffixes.cs#1)]

Quand un littéral entier n’a pas de suffixe, son type est le premier des types suivants dans lesquels sa valeur peut être représentée :

1. [int](int.md)
2. `uint`
3. [long](long.md)
4. [ulong](ulong.md)

## <a name="conversions"></a>Conversions

Il existe une conversion implicite prédéfinie de `uint` en [long](long.md), [ulong](ulong.md), [float](float.md), [double](double.md) et [decimal](decimal.md). Par exemple :

```csharp
float myFloat = 4294967290;   // OK: implicit conversion to float
```

Il existe une conversion implicite prédéfinie de [byte](byte.md), [ushort](ushort.md) ou [char](char.md) en `uint`. Dans le cas contraire, vous devez utiliser un cast. Par exemple, l’instruction d’assignation suivante génère une erreur de compilation sans cast :

```csharp
long aLong = 22;
// Error -- no implicit conversion from long:
uint uInt1 = aLong;
// OK -- explicit conversion:
uint uInt2 = (uint)aLong;
```

Remarquez également qu’il n’existe pas de conversion implicite des types virgule flottante en `uint`. Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :

```csharp
// Error -- no implicit conversion from double:
uint x = 3.0;
// OK -- explicit conversion:
uint y = (uint)3.0;
```

Pour plus d’informations sur les expressions arithmétiques dans lesquelles coexistent des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).

Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.

## <a name="see-also"></a>Voir aussi

- <xref:System.UInt32>
- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Tableau des types intégraux](integral-types-table.md)
- [Tableau des types intégrés](built-in-types-table.md)
- [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md)
- [Tableau des conversions numériques explicites](explicit-numeric-conversions-table.md)
