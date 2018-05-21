---
title: Tableau des valeurs par défaut (référence C#)
description: Découvrez les valeurs par défaut des types valeur qui sont retournées par les constructeurs par défaut.
ms.date: 07/20/2015
helpviewer_keywords:
- constructors [C#], return values
- keywords [C#], new
- default constructor [C#]
- defaults [C#]
- value types [C#], initializing
- variables [C#], value types
- constructors [C#], default constructor
- types [C#], default constructor return values
ms.openlocfilehash: 634a55304534b4269487f29be1fbb4930f51d8ca
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="default-values-table-c-reference"></a>Tableau des valeurs par défaut (référence C#)

Le tableau suivant indique les valeurs par défaut de types valeur qui sont retournées par les constructeurs par défaut. Les constructeurs par défaut sont appelés au moyen de l’opérateur `new`, comme suit :

```csharp
int myInt = new int();
```

L’instruction qui précède produit le même résultat que la suivante :

```csharp
int myInt = 0;
```

Pour rappel, il n’est pas possible d’utiliser en C# des variables qui n’ont pas été initialisées.

|Type de valeur|Valeur par défaut|
|----------------|-------------------|
|[bool](bool.md)|`false`|
|[byte](byte.md)|0|
|[char](char.md)|'\0'|
|[decimal](decimal.md)|0M|
|[double](double.md)|0.0D|
|[enum](enum.md)|Valeur produite par l’expression (E)0, où E est l’identificateur de l’enum.|
|[float](float.md)|0.0F|
|[int](int.md)|0|
|[long](long.md)|0L|
|[sbyte](sbyte.md)|0|
|[short](short.md)|0|
|[struct](struct.md)|Valeur produite en affectant à tous les champs de type valeur leur valeur par défaut et à tous les champs de type référence la valeur `null`.|
|[uint](uint.md)|0|
|[ulong](ulong.md)|0|
|[ushort](ushort.md)|0|

## <a name="see-also"></a>Voir aussi
 [Référence C#](../index.md)  
 [Guide de programmation C#](../../programming-guide/index.md)  
 [Tableau des types valeur](value-types-table.md)  
 [Types valeur](value-types.md)  
 [Tableau des types intégrés](built-in-types-table.md)  
 [Tableaux de référence des types](reference-tables-for-types.md)
