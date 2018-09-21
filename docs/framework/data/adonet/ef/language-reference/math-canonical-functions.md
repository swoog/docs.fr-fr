---
title: Fonctions mathématiques canoniques
ms.date: 03/30/2017
ms.assetid: 6f6cddc6-b561-4ebe-84b6-841ef5b4113b
ms.openlocfilehash: 0fc9f4942c3f76f139ab7e4400005f0bfe80204e
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46537252"
---
# <a name="math-canonical-functions"></a>Fonctions mathématiques canoniques

Entity SQL inclut les fonctions canoniques mathématiques suivantes :
  
## <a name="absvalue"></a>Abs(valeur)

Retourne la valeur absolue de `value`.

**Arguments**

Un `Int16`, `Int32`, `Int64`, `Byte`, `Single`, `Double`, et `Decimal`.

**Valeur de retour**

Type d'élément `value`.

**Exemple**

`Abs(-2)`

## <a name="ceilingvalue"></a>Ceiling(valeur)

Retourne le plus petit entier qui n'est pas inférieur à `value`.

**Arguments**

Un `Single`, `Double`, et `Decimal`.

**Valeur de retour**

Type d'élément `value`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_ceiling)]
[!code-sql[DP EntityServices Concepts#EDM_CEILING](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_ceiling)]

## <a name="floorvalue"></a>Floor(valeur)

Retourne le plus grand entier qui n'est pas supérieur à `value`.

**Arguments**

Un `Single`, `Double`, et `Decimal`.

**Valeur de retour**

Type d'élément `value`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#edm_floor)]
[!code-sql[DP EntityServices Concepts#EDM_FLOOR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#edm_floor)]

## <a name="powervalue-exponent"></a>Power(valeur, exposant)

Retourne le résultat de `value` à l'exposant `exponent` spécifié.

**Arguments**

|  |  |
|--|--|
|`value` | Un `Int32, Int64, Double`, ou `Decimal`. |
|`exponent` | Un `Int64`, `Double`, ou `Decimal`. |

**Valeur de retour**

Type d'élément `value`.

**Exemple**

`Power(748.58,2)`

## <a name="roundvalue"></a>Round(valeur)

Retourne la partie entière de `value`, arrondie à l'entier le plus proche.

**Arguments**

Un `Single`, `Double`, et `Decimal`.

**Valeur de retour**

Type d'élément `value`.

**Exemple**

`Round(748.58)`

## <a name="roundvalue-digits"></a>Round(valeur, chiffres)

Retourne `value`, arrondi aux `digits` spécifiés les plus proches.

**Arguments**

|  |  |
|--|--|
|`value`|`Double` ou `Decimal`.|
|`digits`|`Int16` ou `Int32`.|

**Valeur de retour**

Type d'élément `value`.

**Exemple**

`Round(748.58,1)`

## <a name="truncatevalue-digits"></a>Truncate(valeur, chiffres)

Retourne `value`, tronqué aux `digits` spécifiés les plus proches.

**Arguments**

|  |  |
|--|--|
|`value`|`Double` ou `Decimal`.|
|`digits`|`Int16` ou `Int32`.|

**Valeur de retour**

Type d'élément `value`.

**Exemple**

`Truncate(748.58,1)`  
  
 Ces fonctions retournent `null` si une entrée de valeur `null` est fournie.  
  
 Des fonctionnalités équivalentes sont disponibles dans le fournisseur managé Client Microsoft SQL. Pour plus d’informations, consultez [fonctions SqlClient pour Entity Framework](../../../../../../docs/framework/data/adonet/ef/sqlclient-for-ef-functions.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Fonctions canoniques](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
