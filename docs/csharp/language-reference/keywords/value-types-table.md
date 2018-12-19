---
title: Tableau des types valeur - Référence C#
ms.custom: seodec18
ms.date: 08/24/2018
helpviewer_keywords:
- value types [C#], table
- types [C#], value types
- types [C#], suffixes
ms.assetid: 67d8f631-b6e3-4d83-9910-5ec497f8c5f3
ms.openlocfilehash: d651350f46c0ec1947be9f4f586c341514356fd2
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53244152"
---
# <a name="value-types-table-c-reference"></a>Tableau des types valeur (référence C#)

Le tableau suivant présente les types valeur dans C#.  
  
|Type de valeur|Category|Suffixe du type|  
|----------------|--------------|-----------------|  
|[bool](bool.md)|Booléen||  
|[byte](byte.md)|Non signé, numérique, [intégral](integral-types-table.md)||  
|[char](char.md)|Non signé, numérique, [intégral](integral-types-table.md)||  
|[decimal](decimal.md)|Numérique, [virgule flottante](floating-point-types-table.md)|M ou m|  
|[double](double.md)|Numérique, [virgule flottante](floating-point-types-table.md)|D ou d|  
|[enum](enum.md)|Énumération||  
|[float](float.md)|Numérique, [virgule flottante](floating-point-types-table.md)|F ou f|  
|[int](int.md)|Signé, numérique, [intégral](integral-types-table.md)||  
|[long](long.md)|Signé, numérique, [intégral](integral-types-table.md)|L ou l|  
|[sbyte](sbyte.md)|Signé, numérique, [intégral](integral-types-table.md)||  
|[short](short.md)|Signé, numérique, [intégral](integral-types-table.md)||  
|[struct](struct.md)|Structure définie par l’utilisateur||  
|[uint](uint.md)|Non signé, numérique, [intégral](integral-types-table.md)|U ou u|  
|[ulong](ulong.md)|Non signé, numérique, [intégral](integral-types-table.md)|UL, Ul, uL, ul, LU, Lu, lU ou lu|  
|[ushort](ushort.md)|Non signé, numérique, [intégral](integral-types-table.md)||  

## <a name="remarks"></a>Notes

Utilisez un suffixe de type pour spécifier un type d’un littéral numérique. Par exemple :

```csharp
decimal a = 0.1M;
```

Quand un [littéral numérique entier](~/_csharplang/spec/lexical-structure.md#integer-literals) n’a pas de suffixe, il a le premier type parmi les types suivants où sa valeur peut être représentée : `int`, `uint`, `long`, `ulong`.

Si un [littéral numérique réel](~/_csharplang/spec/lexical-structure.md#real-literals) n’a pas de suffixe, il a le type `double`.

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Tableaux de référence des types](reference-tables-for-types.md)
- [Tableau des valeurs par défaut](default-values-table.md)
- [Types valeur](value-types.md)
- [Tableau des formats des résultats numériques](formatting-numeric-results-table.md)
