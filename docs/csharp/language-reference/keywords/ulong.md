---
title: ulong, mot clé - Référence C#
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- ulong_CSharpKeyword
- ulong
helpviewer_keywords:
- ulong keyword [C#]
ms.assetid: f2ece624-837a-40cf-92c5-343e7f33397c
ms.openlocfilehash: 97db22612e900658746f40cd117ff941135027a1
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53235018"
---
# <a name="ulong-c-reference"></a>ulong (référence C#)

Le mot clé `ulong` désigne un type intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.

|Type|Plage|Size|Type .NET|
|----------|-----------|----------|-------------------------|
|`ulong`|de 0 à 18 446 744 073 709 551 615|Entier 64 bits non signé|<xref:System.UInt64?displayProperty=nameWithType>|

## <a name="literals"></a>Littéraux

Vous pouvez déclarer et initialiser une variable `ulong` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).  Si le littéral entier est en dehors de la plage autorisée pour le type `ulong` (autrement dit, s’il est inférieur à <xref:System.UInt64.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.UInt64.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.

Dans l’exemple suivant, les entiers égaux à 7 934 076 125 représentés comme des littéraux décimaux, hexadécimaux et binaires sont assignés aux valeurs `ulong`.

[!code-csharp[ulong](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#ULong)]

> [!NOTE]
> Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire. Les littéraux décimaux n’ont pas de préfixe.

À partir de C# 7.0, quelques fonctionnalités ont été ajoutées pour améliorer la lisibilité :

- C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.
- C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe. Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.

Voici quelques exemples.

[!code-csharp[long](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#LongS)]

Les littéraux entiers peuvent également inclure un suffixe qui désigne le type. Le suffixe `UL` ou `ul` identifie sans ambiguïté un littéral numérique comme une valeur `ulong`. Le suffixe `L` désigne un type `ulong` si la valeur du littéral dépasse <xref:System.Int64.MaxValue?displayProperty=nameWithType>. Le suffixe `U` ou `u` désigne un type `ulong` si la valeur du littéral dépasse <xref:System.UInt32.MaxValue?displayProperty=nameWithType>. L’exemple suivant utilise le suffixe `ul` pour désigner un entier long :

[!code-csharp[ulsuffix](~/samples/snippets/csharp/language-reference/keywords/numeric-suffixes.cs#2)]

Quand un littéral entier n’a pas de suffixe, son type est le premier des types suivants dans lesquels sa valeur peut être représentée :

1. [int](int.md)
2. [uint](uint.md)
3. [long](long.md)
4. `ulong`

## <a name="compiler-overload-resolution"></a>Résolution de surcharge du compilateur

Une utilisation courante du suffixe est d’appeler des méthodes surchargées. Prenons l’exemple des méthodes surchargées suivantes ayant pour paramètres `ulong` et [int](int.md) :

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(ulong l) {}
```

L’utilisation d’un suffixe avec le paramètre `ulong` garantit que le type correct est appelé, par exemple :

```csharp
SampleMethod(5);    // Calling the method with the int parameter
SampleMethod(5UL);  // Calling the method with the ulong parameter
```

## <a name="conversions"></a>Conversions

Il existe une conversion implicite prédéfinie de `ulong` en [float](float.md), [double](double.md) ou [decimal](decimal.md).

Il n’existe aucune conversion implicite de `ulong` en un type intégral. Par exemple, l’instruction suivante génère une erreur de compilation sans cast explicite :

```csharp
long long1 = 8UL;   // Error: no implicit conversion from ulong
```

Il existe une conversion implicite prédéfinie de [byte](byte.md), [ushort](ushort.md), [uint](uint.md) ou [char](char.md) en `ulong`.

De plus, il n’existe pas de conversion implicite des types virgule flottante en `ulong`. Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :

```csharp
// Error -- no implicit conversion from double:
ulong x = 3.0;
// OK -- explicit conversion:
ulong y = (ulong)3.0;
```

Pour plus d’informations sur les expressions arithmétiques combinant des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).

Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.

## <a name="see-also"></a>Voir aussi

- <xref:System.UInt64>
- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Tableau des types intégraux](integral-types-table.md)
- [Tableau des types intégrés](built-in-types-table.md)
- [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md)
- [Tableau des conversions numériques explicites](explicit-numeric-conversions-table.md)
