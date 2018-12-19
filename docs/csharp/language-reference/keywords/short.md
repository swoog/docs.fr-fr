---
title: short - Référence C#
ms.custom: seodec18
ms.date: 03/14/2017
f1_keywords:
- short
- short_CSharpKeyword
helpviewer_keywords:
- short keyword [C#]
ms.assetid: 04c10688-e51a-4a87-bfec-83f7fb42ff11
ms.openlocfilehash: 8c38a4158f627f41d1667eb96478cd499de78772
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53238897"
---
# <a name="short-c-reference"></a>short (référence C#)

`short` désigne un type de données intégral qui stocke des valeurs en fonction de la taille et de la plage indiquées dans le tableau suivant.

|Type|Plage|Size|Type .NET|
|----------|-----------|----------|-------------------------|
|`short`|de -32 768 à 32 767|Entier 16 bits signé|<xref:System.Int16?displayProperty=nameWithType>|

## <a name="literals"></a>Littéraux

Vous pouvez déclarer et initialiser une variable `short` en lui assignant un littéral décimal, hexadécimal ou binaire (à compter de C# 7.0).  Si le littéral entier est en dehors de la plage autorisée pour le type `short` (autrement dit, s’il est inférieur à <xref:System.Int16.MinValue?displayProperty=nameWithType> ou supérieur à <xref:System.Int16.MaxValue?displayProperty=nameWithType>), une erreur de compilation se produit.

Dans l’exemple suivant, les entiers égaux à 1 034 représentés comme des littéraux décimaux, hexadécimaux et binaires sont implicitement convertis à partir de valeurs [int](int.md) en `short`.

[!code-csharp[Short](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#Short)]

> [!NOTE]
> Vous utilisez le préfixe `0x` ou `0X` pour désigner un littéral hexadécimal, et le préfixe `0b` ou `0B` pour désigner un littéral binaire. Les littéraux décimaux n’ont pas de préfixe.

À compter de C# 7.0, des fonctionnalités ont été ajoutées pour améliorer la lisibilité.

- C# 7.0 prend en charge l’utilisation du caractère de soulignement (`_`) comme séparateur numérique.
- C# 7.2 prend en charge l’utilisation de `_` comme séparateur de chiffres pour un littéral binaire ou hexadécimal, après le préfixe. Un trait de soulignement n’est pas autorisé au début d’un littéral décimal.

Voici quelques exemples.

[!code-csharp[Short](~/samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#ShortS)]

## <a name="compiler-overload-resolution"></a>Résolution de surcharge du compilateur

Un cast doit être utilisé lors de l’appel de méthodes surchargées. Prenons l’exemple des méthodes surchargées suivantes ayant pour paramètres `short` et [int](int.md) :

```csharp
public static void SampleMethod(int i) {}
public static void SampleMethod(short s) {}
```

L’utilisation du cast `short` garantit l’appel du type correct, par exemple :

```csharp
SampleMethod(5);         // Calling the method with the int parameter
SampleMethod((short)5);  // Calling the method with the short parameter
```

## <a name="conversions"></a>Conversions

Il existe une conversion implicite prédéfinie de `short` en [int](int.md), [long](long.md), [float](float.md), [double](double.md) ou [decimal](decimal.md).

Vous ne pouvez pas convertir implicitement des types numériques non littéraux de taille de stockage supérieure à `short` (consultez le [tableau des types intégraux](integral-types-table.md) pour voir les tailles de stockage des types intégraux). Prenez l’exemple des deux variables `short``x` et `y` suivantes :

```csharp
short x = 5, y = 12;
```

L’instruction d’assignation suivante entraîne une erreur de compilation, car l’expression arithmétique située à droite de l’opérateur d’assignation donne la valeur [int](int.md) par défaut.

```csharp
short z  = x + y;        // Compiler error CS0266: no conversion from int to short
```

Pour corriger ce problème, utilisez un cast :

```csharp
short z  = (short)(x + y);   // Explicit conversion
```

Il est toutefois possible d’utiliser les instructions suivantes, dans lesquelles la variable de destination a une taille de stockage égale ou supérieure :

```csharp
int m = x + y;
long n = x + y;
```

Il n’existe pas de conversion implicite des types virgule flottante en `short`. Par exemple, l’instruction suivante génère une erreur du compilateur, sauf si vous utilisez un cast explicite :

```csharp
short x = 3.0;          // Error: no implicit conversion from double
short y = (short)3.0;   // OK: explicit conversion
```

Pour plus d’informations sur les expressions arithmétiques combinant des types virgule flottante et des types intégraux, consultez [float](float.md) et [double](double.md).

Pour plus d’informations sur les règles des conversions numériques implicites, consultez le [tableau des conversions numériques implicites](implicit-numeric-conversions-table.md).

## <a name="c-language-specification"></a>spécification du langage C#

Pour plus d’informations, consultez [Types intégraux](~/_csharplang/spec/types.md#integral-types) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.

## <a name="see-also"></a>Voir aussi

- <xref:System.Int16>
- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Tableau des types intégraux](integral-types-table.md)
- [Tableau des types intégrés](built-in-types-table.md)
- [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md)
- [Tableau des conversions numériques explicites](explicit-numeric-conversions-table.md)