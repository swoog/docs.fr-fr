---
title: Tableau des conversions numériques explicites - Référence C#
ms.custom: seodec18
ms.date: 09/06/2018
helpviewer_keywords:
- conversions [C#], explicit numeric
- numeric conversions [C#], explicit
- explicit numeric conversion [C#]
- numeric data types [C#]
- types [C#], explicit numeric conversions
- type conversion [C#], explicit numeric
ms.assetid: f3bb9e76-6b92-4df7-bc36-f866c24e1dfd
ms.openlocfilehash: 90691ae0d9de35831b7b3119493e4e9cd81720e6
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236308"
---
# <a name="explicit-numeric-conversions-table-c-reference"></a>Tableau des conversions numériques explicites (référence C#)

Le tableau suivant indique les conversions explicites prédéfinies entre les types numériques .NET pour lesquels il n’existe aucune [conversion implicite](implicit-numeric-conversions-table.md).

|From|À|  
|----------|--------|  
|[sbyte](sbyte.md)|`byte`, `ushort`, `uint`, `ulong` ou `char`|  
|[byte](byte.md)|`sbyte` ou `char`|  
|[short](short.md)|`sbyte`, `byte`, `ushort`, `uint`, `ulong` ou `char`|  
|[ushort](ushort.md)|`sbyte`, `byte`, `short` ou `char`|  
|[int](int.md)|`sbyte`, `byte`, `short`, `ushort`, `uint`, `ulong` ou `char`|  
|[uint](uint.md)|`sbyte`, `byte`, `short`, `ushort`, `int` ou `char`|  
|[long](long.md)|`sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `ulong` ou `char`|  
|[ulong](ulong.md)|`sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `long` ou `char`|  
|[char](char.md)|`sbyte`, `byte`ou `short`|  
|[float](float.md)|`sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `long`, `ulong`, `char` ou `decimal`|  
|[double](double.md)|`sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `long`, `ulong`, `char`, `float` ou `decimal`|  
|[decimal](decimal.md)|`sbyte`, `byte`, `short`, `ushort`, `int`, `uint`, `long`, `ulong`, `char`, `float` ou `double`|  
  
## <a name="remarks"></a>Notes  
  
- La conversion numérique explicite peut entraîner une perte de précision ou la levée d’une exception, généralement <xref:System.OverflowException>.  

- Quand vous convertissez une valeur d’un type intégral en un autre type intégral, le résultat varie selon le [contexte de vérification](checked-and-unchecked.md) du dépassement. Dans un contexte vérifié, la conversion réussit si la valeur source se situe dans la plage du type de destination. Sinon, une exception <xref:System.OverflowException> est levée. Dans un contexte non vérifié, la conversion réussit toujours et procède comme suit :

  - Si le type source est plus grand que le type de destination, la valeur source est tronquée via l’abandon de ses bits « supplémentaires » les plus significatifs. Le résultat est ensuite traité en tant que valeur du type de destination.

  - Si le type source est plus petit que le type de destination, la valeur source fait l’objet d’une extension de signe ou d’une extension de zéros, pour avoir la même taille que le type de destination. L’extension de signe est utilisée si le type source est signé. L’extension de zéro est utilisée si le type source est non signé. Le résultat est ensuite traité en tant que valeur du type de destination.

  - Si le type source a la même taille que le type de destination, la valeur source est traitée comme une valeur du type de destination.
  
- Quand vous convertissez une valeur de type `decimal` en type intégral, la valeur source est arrondie vers zéro à la valeur intégrale la plus proche. Si la valeur intégrale obtenue se trouve en dehors de la plage du type de destination, une exception <xref:System.OverflowException> est levée.  
  
- Quand vous convertissez une valeur `double` ou `float` en type intégral, cette valeur est arrondie vers zéro, à la valeur intégrale la plus proche. Si la valeur intégrale résultante se situe en dehors de la plage du type de destination, le résultat varie selon le [contexte de vérification](checked-and-unchecked.md) du dépassement. Dans un contexte vérifié, une exception <xref:System.OverflowException> est levée, alors que dans un contexte non vérifié, le résultat est une valeur non spécifiée du type de destination.  
  
- Quand vous convertissez `double` en `float`, la valeur `double` est arrondie à la valeur `float` la plus proche. Si la valeur `double` est inférieure ou supérieure à la plage de valeurs autorisées pour le type de destination, la conversion a pour résultat la valeur zéro ou un nombre infini.  
  
- Dans le cas d’une conversion de `float` ou `double` en `decimal`, la valeur source est convertie en une représentation `decimal` et arrondie au nombre le plus proche après la 28ème décimale, si nécessaire. Selon la valeur de la valeur source, la conversion peut aboutir à l’un des résultats suivants :  

  - Si la valeur source est trop petite pour être représentée en tant que `decimal`, le résultat est zéro.  

  - Si la valeur source est une valeur non numérique (NaN), un nombre infini ou une valeur trop grande pour être représentée au format `decimal`, une exception <xref:System.OverflowException> est levée.  
  
- Quand vous convertissez `decimal` en `float` ou `double`, la valeur `decimal` est arrondie à la valeur `double` ou `float` la plus proche.  
  
 Pour plus d’informations sur les conversions explicites, consultez la section [Conversions explicites](~/_csharplang/spec/conversions.md#explicit-conversions) de la [Spécification du langage C#](../language-specification/index.md).
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Cast et conversions de types](../../programming-guide/types/casting-and-type-conversions.md)
- [(), opérateur](../operators/invocation-operator.md)
- [Tableau des types intégraux](integral-types-table.md)
- [Tableau des types à virgule flottante](floating-point-types-table.md)
- [Tableaux des types intégrés](built-in-types-table.md)
- [Tableau des conversions numériques implicites](implicit-numeric-conversions-table.md)
