---
title: Types Nullable (Guide de programmation C#)
description: Découvrir les types Nullable C# et comment les utiliser
ms.date: 07/30/2018
helpviewer_keywords:
- nullable types [C#]
- C# language, nullable types
- types [C#], nullable
ms.assetid: e473cb01-28ca-42be-9cea-f717055d72c6
ms.openlocfilehash: 2af0704abcad00c75a5d40bfe2d0523d07ee6a3f
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "43885046"
---
# <a name="nullable-types-c-programming-guide"></a>Types Nullable (Guide de programmation C#)

Les types Nullable sont des instances du struct <xref:System.Nullable%601?displayProperty=nameWithType>. Les types Nullable peuvent représenter toutes les valeurs d’un type sous-jacent `T` ainsi qu’une autre valeur [null](../../language-reference/keywords/null.md). Le type sous-jacent `T` peut être n’importe quel [type valeur](../../language-reference/keywords/value-types.md) non nullable. `T` ne peut pas être un type référence.

Par exemple, vous pouvez affecter `null` ou toute valeur entière à partir de <xref:System.Int32.MinValue?displayProperty=nameWithType> à <xref:System.Int32.MaxValue?displayProperty=nameWithType> à un `Nullable<int>` et [true](../../language-reference/keywords/true-literal.md), [false](../../language-reference/keywords/false-literal.md) ou `null` à un `Nullable<bool>`.

Utilisez un type nullable lorsque vous avez besoin de représenter la valeur non definie d’un type sous-jacent. Une variable booléenne peut avoir uniquement deux valeurs : true et false. Il n’existe aucune valeur « non définie ». Dans de nombreuses applications de programmation, notamment dans les interactions de base de données, une valeur de variable peut être indéfinie ou manquante. Par exemple, un champ dans une base de données peut contenir les valeurs true ou false, ou aucune valeur du tout. Vous utilisez un type `Nullable<bool>` dans ce cas.

Les types Nullable possèdent les caractéristiques suivantes :
  
- Les types Nullable représentent des variables de type valeur qui peuvent avoir la valeur `null`. Il n’est pas possible de créer un type Nullable à partir d’un type référence. (Les types référence prennent déjà en charge la valeur `null`.)  
  
- La syntaxe `T?` est l’abréviation de `Nullable<T>`. Les deux formats sont interchangeables.  
  
- Affectez une valeur à un type Nullable, comme vous le feriez pour un type valeur sous-jacent : `int? x = 10;` ou `double? d = 4.108;`. Vous pouvez également affecter la valeur `null` : `int? x = null;`.  
  
- Utilisez les propriétés <xref:System.Nullable%601.HasValue%2A?displayProperty=nameWithType> et <xref:System.Nullable%601.Value%2A?displayProperty=nameWithType> en lecture seule pour rechercher les valeurs null et récupérer la valeur, comme indiqué dans l’exemple suivant : `if (x.HasValue) y = x.Value;`  
  
  - La propriété <xref:System.Nullable%601.HasValue%2A> retourne `true` si la variable contient une valeur, ou `false` si elle est `null`.
  
  - La propriété <xref:System.Nullable%601.Value%2A> retourne une valeur si <xref:System.Nullable%601.HasValue%2A> retourne `true`. Sinon, une exception <xref:System.InvalidOperationException> est levée.  
  
- Vous pouvez également utiliser les opérateurs `==` et `!=` avec un type Nullable, comme le montre l’exemple suivant : `if (x != null) y = x.Value;`. Si `a` et `b` sont tous les deux null, `a == b` prend la valeur `true`.  

- À compter de C# 7.0, vous pouvez utiliser les [critères spéciaux](../../pattern-matching.md#the-is-type-pattern-expression) pour examiner et obtenir une valeur d’un type Nullable : `if (x is int valueOfX) y = valueOfX;`.
  
- La valeur par défaut de `T?` est une instance dont la propriété <xref:System.Nullable%601.HasValue%2A> retourne `false`.  

- Utilisez la méthode <xref:System.Nullable%601.GetValueOrDefault> pour retourner la valeur affectée, ou la valeur [par défaut](../../language-reference/keywords/default-values-table.md) du type valeur sous-jacent si la valeur du type Nullable est `null`.  

- Utilisez la méthode <xref:System.Nullable%601.GetValueOrDefault(%600)> pour retourner la valeur affectée, ou la valeur par défaut fournie si la valeur du type Nullable est `null`.
  
- Utilisez l’[opérateur null-coalescing](../../language-reference/operators/null-coalescing-operator.md), `??`, pour affecter une valeur à un type sous-jacent basé sur une valeur du type Nullable : `int? x = null; int y = x ?? -1;`. Dans l’exemple, dans la mesure où `x` est null, la valeur de résultat de `y` est `-1`.

- Si une conversion définie par l’utilisateur est définie entre deux types de données, la même conversion peut également être utilisée avec les versions Nullable de ces types de données.
  
- Les types Nullable imbriqués ne sont pas autorisés. Il n’est pas possible de compiler la ligne suivante : `Nullable<Nullable<int>> n;`  

Pour plus d’informations, consultez les rubriques [Utilisation des types Nullable](using-nullable-types.md) et [Guide pratique pour identifier un type Nullable](how-to-identify-a-nullable-type.md).
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Nullable%601?displayProperty=nameWithType>  
- <xref:System.Nullable?displayProperty=nameWithType>  
- [?? Opérateur](../../language-reference/operators/null-coalescing-operator.md)  
- [Guide de programmation C#](../index.md)  
- [Guide C#](../../index.md)  
- [Référence C#](../../language-reference/index.md)  
- [Types valeur Nullable (Visual Basic)](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)  
