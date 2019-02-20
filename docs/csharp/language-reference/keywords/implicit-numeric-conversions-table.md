---
title: Tableau des conversions numériques implicites - Référence C#
ms.custom: seodec18
ms.date: 09/05/2018
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
ms.openlocfilehash: 703f60f48e1e569e0ffcab66ff7ccc91d4a49514
ms.sourcegitcommit: d2ccb199ae6bc5787b4762e9ea6d3f6fe88677af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56093552"
---
# <a name="implicit-numeric-conversions-table-c-reference"></a>Tableau des conversions numériques implicites (référence C#)

Le tableau suivant montre les conversions implicites prédéfinies entre les types numériques .NET.
  
|From|À|  
|----------|--------|  
|[sbyte](sbyte.md)|`short`, `int`, `long`, `float`, `double` ou `decimal`|  
|[byte](byte.md)|`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`|  
|[char](char.md)|`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`|  
|[short](short.md)|`int`, `long`, `float`, `double` ou `decimal`|  
|[ushort](ushort.md)|`int`, `uint`, `long`, `ulong`, `float`, `double` ou `decimal`|  
|[int](int.md)|`long`, `float`, `double` ou `decimal`|  
|[uint](uint.md)|`long`, `ulong`, `float`, `double` ou `decimal`|  
|[long](long.md)|`float`, `double`ou `decimal`|  
|[ulong](ulong.md)|`float`, `double`ou `decimal`|  
|[float](float.md)|`double`|  
  
## <a name="remarks"></a>Remarques  

- Un [type intégral](integral-types-table.md) est implicitement convertible en [type à virgule flottante](floating-point-types-table.md).

- La précision, et non la magnitude, peut être perdue dans les conversions de `int`, `uint`, `long` ou `ulong` à `float`, et de `long` ou `ulong` à `double`.  
  
- Il n’existe aucune conversion implicite vers les types `char`, `byte` et `sbyte`.  

- Il n’existe aucune conversion implicite à partir des types `double` et `decimal`.
  
- Il n’existe aucune conversion implicite entre le type `decimal` et le type `float` ou `double`.  
  
- La valeur d’une expression constante de type `int` (par exemple, une valeur représentée par un littéral intégral) peut être convertie en `sbyte`, `byte`, `short`, `ushort`, `uint` ou `ulong`, à condition qu’elle se trouve dans la plage du type de destination :

  ```csharp
  byte a = 13;    // Compiles
  byte b = 300;   // CS0031: Constant value '300' cannot be converted to a 'byte'
  ```

Pour plus d’informations sur les conversions implicites, consultez la section [Conversions implicites](~/_csharplang/spec/conversions.md#implicit-conversions) de la [Spécification du langage C#](../language-specification/index.md).
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Tableau des types intégraux](integral-types-table.md)
- [Tableau des types à virgule flottante](floating-point-types-table.md)
- [Tableaux des types intégrés](built-in-types-table.md)
- [Tableau des conversions numériques explicites](explicit-numeric-conversions-table.md)
- [Cast et conversions de types](../../programming-guide/types/casting-and-type-conversions.md)
