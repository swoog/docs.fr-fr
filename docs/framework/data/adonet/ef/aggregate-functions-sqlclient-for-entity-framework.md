---
title: Fonctions d’agrégation (SqlClient pour Entity Framework)
ms.date: 03/30/2017
ms.assetid: 03303f01-b591-4efc-9875-f9c608edff0b
ms.openlocfilehash: 55a10b82ffc189f5cf4118cb225a96963226256e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54724185"
---
# <a name="aggregate-functions-sqlclient-for-entity-framework"></a>Fonctions d’agrégation (SqlClient pour Entity Framework)
Le fournisseur de données .NET Framework pour SQL Server (SqlClient) fournit des fonctions d'agrégation. Les fonctions d'agrégation effectuent des calculs sur un ensemble de valeurs d'entrée et retournent une valeur. Ces fonctions se trouvent dans l'espace de noms SqlServer, lequel est disponible lorsque vous utilisez SqlClient. La propriété d’espace de noms d’un fournisseur permet à Entity Framework de découvrir le préfixe attribué par ce fournisseur à des constructions spécifiques, telles que des types et des fonctions.  
  
 Voici les fonctions d’agrégation SqlClient.  

## <a name="avgexpression"></a>AVG(expression)

Retourne la moyenne des valeurs d’une collection. Les valeurs NULL sont ignorées.

**Arguments**

Un `Int32`, `Int64`, `Double`, et `Decimal`.

**Valeur de retour**

Type d'élément `expression`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_avg)]
 [!code-sql[DP EntityServices Concepts#SQLSERVER_AVG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_avg)]

## <a name="checksumaggcollection"></a>CHECKSUM_AGG(collection)
 
 Retourne la somme de contrôle des valeurs d’une collection. Les valeurs NULL sont ignorées.
 
 **Arguments**
 
 Une Collection (`Int32`).
 
 **Valeur de retour**
 
 Élément `Int32`.
 
 **Exemple**
 
 [!code-csharp[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_checksum)]
 [!code-sql[DP EntityServices Concepts#SQLSERVER_CHECKSUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_checksum)]
   
## <a name="countexpression"></a>Count(expression)

Retourne le nombre d’éléments d’une collection sous la forme d’une valeur `Int32`.

**Arguments**

Une Collection\<T >, où T est un des types suivants :

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|`Guid` (non retourné dans SQL Server 2000)|

**Valeur de retour**

Élément `Int32`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_COUNT](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_count)]
[ ! code non-SQL[DP EntityServices Concepts #SQLSERVER_COUNT](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_count)
 
## <a name="countbigexpression"></a>COUNT_BIG(expression)
 
 Retourne le nombre d’éléments d’une collection sous la forme d’une valeur `bigint`.
 
 **Arguments**
 
 Collection(T), où T est un des types suivants :
 
 |   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`|`Guid` (non retourné dans SQL Server 2000)|

**Valeur de retour**

Élément `Int64`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_countbig)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_COUNTBIG](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_countbig)]

## <a name="maxexpression"></a>MAX(expression)

Retourne la valeur maximale contenue dans la collection.

**Arguments**

Collection(T), où T est un des types suivants : 

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

**Valeur de retour**

Type d'élément `expression`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_max)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_MAX](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_max)]

## <a name="minexpression"></a>MIN(expression)

Retourne la valeur minimale contenue dans une collection.

**Arguments**

Collection(T), où T est un des types suivants : 

|   |   |   |   |
|---|---|---|---|
|`Boolean`|`Double`|`DateTime`|`DateTimeOffset`|
|`Time`|`String`|`Binary`||

**Valeur de retour**

Type d'élément `expression`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_min)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_MIN](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_min)]

## <a name="stdevexpression"></a>StDev(expression)

Retourne l'écart type statistique de toutes les valeurs de l'expression spécifiée.

**Arguments**

Une Collection (`Double`).

**Valeur de retour**

`Double`

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_stdev)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEV](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdev)]

## <a name="stdevpexpression"></a>StDevP(expression)

Retourne l'écart type statistique du remplissage de toutes les valeurs de l'expression spécifiée.

**Arguments**

Une Collection (`Double`).

**Valeur de retour**

`Double`

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_stdevp)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_STDEVP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_stdevp)]

## <a name="sumexpression"></a>SUM(expression)

Retourne la somme de toutes les valeurs de la collection.

**Arguments**

Un Collection(T) où T est un des types suivants : `Int32`, `Int64`, `Double`, `Decimal`.

**Valeur de retour**

Type d'élément `expression`.

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_sum)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_SUM](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_sum)]

## <a name="varexpression"></a>VAR(expression)

Retourne la variance statistique de toutes les valeurs dans l'expression spécifiée.

**Arguments**

Une Collection (`Double`).

**Valeur de retour**

`Double`

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_var)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_VAR](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_var)]

## <a name="varpexpression"></a>VARP(expression)

Retourne la variance statistique de remplissage pour toutes les valeurs de l'expression spécifiée.

**Arguments**

Une Collection (`Double`).

**Valeur de retour**

`Double`

**Exemple**

[!code-csharp[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/entitysql.cs#sqlserver_varp)]
[!code-sql[DP EntityServices Concepts#SQLSERVER_VARP](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#sqlserver_varp)] 
  
## <a name="see-also"></a>Voir aussi

Pour plus d'informations sur les fonctions d'agrégation prises en charge par SqlClient, voir la documentation correspondant à la version de SQL Server que vous avez spécifiée dans le manifeste du fournisseur SqlClient :  

**SQL Server 2005**: [Fonctions d’agrégation (Transact-SQL)](https://docs.microsoft.com/previous-versions/sql/sql-server-2005/ms173454(v=sql.90))  
**SQL Server 2008 et versions ultérieur**:  [Fonctions d’agrégation (Transact-SQL)](/sql/t-sql/functions/aggregate-functions-transact-sql)  
- [Langage Entity SQL](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
- [Fonctions canoniques d’agrégation](../../../../../docs/framework/data/adonet/ef/language-reference/aggregate-canonical-functions.md)
