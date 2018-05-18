---
title: Expressions de valeur par défaut (Guide de programmation C#)
description: Les expressions de valeur par défaut produisent la valeur par défaut des types référence et des types valeur
ms.date: 04/25/2018
helpviewer_keywords:
- generics [C#], default keyword
- default keyword [C#], generic programming
ms.openlocfilehash: be51ad253a2939f538144caf4500f39e144c1664
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="default-value-expressions-c-programming-guide"></a>Expressions de valeur par défaut (Guide de programmation C#)

Une expression de valeur par défaut `default(T)` produit la valeur par défaut d’un type `T`. Le tableau suivant montre les valeurs qui sont produites pour différents types :

|Type|Valeur par défaut|
|---------|---------|
|tout type référence ;|`null`|
|Type de valeur numérique|Zéro|
|[bool](../../language-reference/keywords/bool.md)|`false`|
|[char](../../language-reference/keywords/char.md)|`'\0'`|
|[enum](../../language-reference/keywords/enum.md)|Valeur produite par l’expression `(E)0`, où `E` est l’identificateur de l’enum.|
|[struct](../../language-reference/keywords/struct.md)|Valeur produite en affectant à tous les champs de type valeur leur valeur par défaut et à tous les champs de type référence la valeur `null`.|
|Types Nullable|Instance pour laquelle la propriété <xref:System.Nullable%601.HasValue%2A> a la valeur `false` et la propriété <xref:System.Nullable%601.Value%2A> n’est pas définie.|

Les expressions de valeur par défaut sont particulièrement utiles dans les méthodes et classes génériques. Le problème qui se pose avec l’utilisation des génériques est de savoir comment assigner une valeur par défaut à un type paramétrable `T` quand vous ne connaissez pas les éléments suivants à l’avance :

- Si `T` est un type référence ou un type valeur.
- Si `T` est un type valeur, qu’il s’agisse d’une valeur numérique ou d’un struct.

 Avec une variable `t` d’un type paramétré `T`, l’instruction `t = null` est valide uniquement si `T` est un type référence. L’affectation de `t = 0` fonctionne uniquement pour les types valeur numériques mais pas pour les structs. Pour résoudre ce problème, utilisez une expression de valeur par défaut :

```csharp
T t = default(T);
```

L’expression `default(T)` n’est pas limitée aux classes et aux méthodes génériques. Vous pouvez utiliser les expressions de valeur par défaut avec n’importe quel type managé. Toutes ces expressions sont valides :

 [!code-csharp[csProgGuideGenerics#1](../../../../samples/snippets/csharp/programming-guide/statements-expressions-operators/default-value-expressions.cs)]

 L’exemple suivant de la classe `GenericList<T>` montre comment utiliser l’opérateur `default(T)` dans une classe générique. Pour plus d’informations, consultez [Introduction aux génériques](../generics/introduction-to-generics.md).

 [!code-csharp[csProgGuideGenerics#2](../../../../samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#Snippet41)]

## <a name="default-literal-and-type-inference"></a>Littéral par défaut et inférence de type

À partir de C# 7.1, vous pouvez utiliser les littéraux `default` pour les expressions de valeur par défaut quand le compilateur peut déduire le type de l’expression. Le littéral `default` génère la même valeur que l’équivalent `default(T)`, où `T` est le type déduit. Vous pouvez ainsi alléger votre code en réduisant la redondance de déclarer un type plusieurs fois. Vous pouvez utiliser le littéral `default` dans l’un des emplacements suivants :

- initialiseur de variable
- assignation de variable
- déclaration de la valeur par défaut d’un paramètre facultatif
- valeur pour un argument d’appel de méthode
- instruction return (ou expression dans un membre expression-bodied)

L’exemple suivant illustre plusieurs utilisations du littéral `default` dans une expression de valeur par défaut :

[!code-csharp[csProgGuideGenerics#3](../../../../samples/snippets/csharp/programming-guide/statements-expressions-operators/default-literal.cs)]

## <a name="see-also"></a>Voir aussi

 <xref:System.Collections.Generic>  
 [Guide de programmation C#](../index.md)  
 [Génériques (guide de programmation C#)](../generics/index.md)  
 [Méthodes génériques](../generics/generic-methods.md)  
 [Génériques en .NET](~/docs/standard/generics/index.md)  
 [Tableau des valeurs par défaut](../../language-reference/keywords/default-values-table.md)
