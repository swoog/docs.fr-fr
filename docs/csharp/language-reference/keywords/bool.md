---
title: bool, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- bool_CSharpKeyword
- bool
helpviewer_keywords:
- bool keyword [C#]
ms.assetid: 551cfe35-2632-4343-af49-33ad12da08e2
ms.openlocfilehash: d6b0cb91dd9b8159919b0d155bb2f9773e7ba534
ms.sourcegitcommit: c217b067985905cb21eafc5dd9a83568d7ff4e45
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2018
ms.locfileid: "36315106"
---
# <a name="bool-c-reference"></a>bool (référence C#)

Le mot clé `bool` est un alias de <xref:System.Boolean?displayProperty=nameWithType>. Il s’utilise pour déclarer des variables qui stockent les valeurs booléennes [true](../../../csharp/language-reference/keywords/true.md) et [false](../../../csharp/language-reference/keywords/false.md).

> [!NOTE]
> Si vous avez besoin d’une variable booléenne qui peut également avoir la valeur `null`, utilisez `bool?`. Pour plus d’informations, consultez [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md).

## <a name="literals"></a>Littéraux

Vous pouvez assigner une valeur booléenne à une variable `bool`. Vous pouvez également assigner à une variable `bool` une expression dont le résultat est une valeur `bool`.

[!code-csharp[csrefKeywordsTypes#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#1)]

La valeur par défaut d’une variable `bool` est `false`. La valeur par défaut d’une variable `bool?` est `null`.

## <a name="conversions"></a>Conversions

Dans C++, une valeur de type `bool` peut être convertie en une valeur de type `int`. En d’autres termes, `false` équivaut à zéro et `true` équivaut à une valeur différente de zéro. Dans C#, il n’y a pas de conversion possible entre le type `bool` et les autres types. Par exemple, l’instruction `if` suivante n’est pas valide dans C# :

[!code-csharp[csrefKeywordsTypes#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#2)]

Pour tester une variable du type `int`, vous devez la comparer explicitement à une valeur, telle que zéro, comme suit :

[!code-csharp[csrefKeywordsTypes#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#3)]

## <a name="example"></a>Exemple

Dans cet exemple, vous tapez un caractère, et le programme vérifie si le caractère entré est une lettre. Si c’est une lettre, le programme vérifie s’il s’agit d’une minuscule ou d’une majuscule. Ces vérifications sont effectuées avec les méthodes <xref:System.Char.IsLetter%2A>, et <xref:System.Char.IsLower%2A>, qui retournent toutes les deux le type `bool` :

[!code-csharp[csrefKeywordsTypes#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/keywordsTypes.cs#4)]

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

[Référence C#](../../../csharp/language-reference/index.md)  
[Guide de programmation C#](../../../csharp/programming-guide/index.md)  
[Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
[Tableau des types intégraux](../../../csharp/language-reference/keywords/integral-types-table.md)  
[Tableau des types intégrés](../../../csharp/language-reference/keywords/built-in-types-table.md)  
[Tableau des conversions numériques implicites](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
[Tableau des conversions numériques explicites](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)  