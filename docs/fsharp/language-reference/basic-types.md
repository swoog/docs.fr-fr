---
title: 'Types de base (F #)'
description: 'Découvrir les types de base fondamentales qui sont utilisés dans le langage F #.'
ms.date: 07/09/2018
ms.openlocfilehash: 8f948d066323527b09b1d3f9f4167b95b1c875cf
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45686100"
---
# <a name="basic-types"></a>Types de base

Cette rubrique répertorie les types de base qui sont définies dans le langage F #. Ces types sont le plus fondamental en F #, constituant la base de presque chaque programme F #. Ils représentent un sur-ensemble des types primitifs .NET.

|Type|Type .NET|Description|
|----|---------|-----------|
|`bool`|<xref:System.Boolean>|Les valeurs possibles sont `true` et `false`.|
|`byte`|<xref:System.Byte>|Valeurs comprises entre 0 et 255.|
|`sbyte`|<xref:System.SByte>|Valeurs comprises entre -128 et 127.|
|`int16`|<xref:System.Int16>|Valeurs comprise entre -32768 et 32767.|
|`uint16`|<xref:System.UInt16>|Valeurs comprises entre 0 et 65535.|
|`int`|<xref:System.Int32>|Valeurs d’allant de -2,147,483,648 à 2 147 483 647.|
|`uint32`|<xref:System.UInt32>|Valeurs de 0 à 4 294 967 295.|
|`int64`|<xref:System.Int64>|Valeurs de -9,223,372,036,854,775,808 à 9,223,372,036,854,775,807.|
|`uint64`|<xref:System.UInt64>|Valeurs comprises entre 0 et 18,446,744,073,709,551,615.|
|`nativeint`|<xref:System.IntPtr>|Un pointeur natif comme un entier signé.|
|`unativeint`|<xref:System.UIntPtr>|Un pointeur natif sous forme d’entier non signé.|
|`char`|<xref:System.Char>|Valeurs de caractères Unicode.|
|`string`|<xref:System.String>|Texte Unicode.|
|`decimal`|<xref:System.Decimal>|Type de données qui comporte au moins 28 chiffres significatifs à virgule flottante.|
|`unit`|non applicable|Indique l’absence d’une valeur réelle. Le type n'a qu’une seule valeur formelle, qui est indiquée `()`. La valeur unitaire, `()`, est souvent utilisé comme espace réservé où une valeur est requise, mais aucune valeur réelle n’est disponible ou a de sens.|
|`void`|<xref:System.Void>|Indique le type ou la valeur.|
|`float32`, `single`|<xref:System.Single>|Type à virgule flottante 32 bits.|
|`float`, `double`|<xref:System.Double>|Type à virgule flottante 64 bits.|

>[!NOTE]
Vous pouvez effectuer des calculs avec des entiers trop grandes pour le type d’entier 64 bits à l’aide de la [bigint](https://msdn.microsoft.com/library/dc8be18d-4042-46c4-b136-2f21a84f6efa) type. `bigint` n’est pas considéré comme un type de base ; Il est l’abréviation de `System.Numerics.BigInteger`.

## <a name="see-also"></a>Voir aussi

- [Informations de référence du langage F#](index.md)
