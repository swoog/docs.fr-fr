---
title: Mappages des types de données Oracle
ms.date: 03/30/2017
ms.assetid: ec34ae21-bbbb-4adb-b672-83865e2a8451
ms.openlocfilehash: c1fb3a6838e6a1b242255d4035c10ab0ec07d536
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59104570"
---
# <a name="oracle-data-type-mappings"></a>Mappages des types de données Oracle
La table suivante répertorie les types de données Oracle et leurs mappages sur le <xref:System.Data.OracleClient.OracleDataReader>.  
  
|Type de données Oracle|Type de données .NET Framework retourné par OracleDataReader.GetValue|Type de données OracleClient retourné par OracleDataReader.GetOracleValue|Notes|  
|----------------------|--------------------------------------------------------------------|------------------------------------------------------------------------|-------------|  
|**BFILE**|**Byte[]**|<xref:System.Data.OracleClient.OracleBFile>||  
|**BLOB**|**Byte[]**|<xref:System.Data.OracleClient.OracleLob>||  
|**CHAR**|**Chaîne**|<xref:System.Data.OracleClient.OracleString>||  
|**CLOB**|**Chaîne**|<xref:System.Data.OracleClient.OracleLob>||  
|**DATE**|**DateTime**|<xref:System.Data.OracleClient.OracleDateTime>||  
|**FLOAT**|**Decimal**|<xref:System.Data.OracleClient.OracleNumber>|Ce type de données est un alias pour le **nombre** type de données et est conçu afin que le <xref:System.Data.OracleClient.OracleDataReader> retourne un **System.Decimal** ou <xref:System.Data.OracleClient.OracleNumber> plutôt qu’une valeur à virgule flottante. L'utilisation du type de données .NET Framework peut entraîner un dépassement.|  
|**INTEGER**|**Decimal**|<xref:System.Data.OracleClient.OracleNumber>|Ce type de données est un alias pour le **Number (38)** type de données et est conçu afin que le <xref:System.Data.OracleClient.OracleDataReader> retourne un **System.Decimal** ou <xref:System.Data.OracleClient.OracleNumber> au lieu d’une valeur entière. L'utilisation du type de données .NET Framework peut entraîner un dépassement.|  
|**INTERVAL YEAR TO MONTH**|**Int32**|<xref:System.Data.OracleClient.OracleMonthSpan>||  
|**INTERVAL DAY TO SECOND**|**TimeSpan**|<xref:System.Data.OracleClient.OracleTimeSpan>||  
|**LONG**|**Chaîne**|<xref:System.Data.OracleClient.OracleString>||  
|**LONG RAW**|**Byte[]**|<xref:System.Data.OracleClient.OracleBinary>||  
|**NCHAR**|**Chaîne**|<xref:System.Data.OracleClient.OracleString>||  
|**NCLOB**|**Chaîne**|<xref:System.Data.OracleClient.OracleLob>||  
|**NUMBER**|**Decimal**|<xref:System.Data.OracleClient.OracleNumber>|L'utilisation du type de données .NET Framework peut entraîner un dépassement.|  
|**NVARCHAR2**|**Chaîne**|<xref:System.Data.OracleClient.OracleString>||  
|**RAW**|**Byte[]**|<xref:System.Data.OracleClient.OracleBinary>||  
|**REF CURSOR**|||Oracle **REF CURSOR** type de données n’est pas pris en charge par le <xref:System.Data.OracleClient.OracleDataReader> objet.|  
|**ROWID**|**Chaîne**|<xref:System.Data.OracleClient.OracleString>||  
|**TIMESTAMP**|**DateTime**|<xref:System.Data.OracleClient.OracleDateTime>||  
|**TIMESTAMP WITH LOCAL TIME ZONE**|**DateTime**|<xref:System.Data.OracleClient.OracleDateTime>||  
|**TIMESTAMP WITH TIME ZONE**|**DateTime**|<xref:System.Data.OracleClient.OracleDateTime>||  
|**UNSIGNED INTEGER**|**nombre**|<xref:System.Data.OracleClient.OracleNumber>|Ce type de données est un alias pour le **Number (38)** type de données et est conçu afin que le <xref:System.Data.OracleClient.OracleDataReader> retourne un **System.Decimal** ou <xref:System.Data.OracleClient.OracleNumber> au lieu d’une valeur entière non signée. L'utilisation du type de données .NET Framework peut entraîner un dépassement.|  
|**VARCHAR2**|**Chaîne**|<xref:System.Data.OracleClient.OracleString>||  
  
 Le tableau suivant répertorie les types de données Oracle et les types de données .NET Framework (**System.Data.DbType** et <xref:System.Data.OracleClient.OracleType>) à utiliser lors de leur liaison en tant que paramètres.  
  
|Type de données Oracle|Énumération DbType à lier comme paramètre|Énumération OracleType à lier comme paramètre|Notes|  
|----------------------|-----------------------------------------------|---------------------------------------------------|-------------|  
|**BFILE**||**BFile**|Oracle n’autorise la liaison un **BFILE** comme un **BFILE** paramètre. Le fournisseur de données .NET pour Oracle ne construit pas automatiquement un pour vous si vous tentez de lier une non -**BFILE** valeur, telle que **byte []** ou <xref:System.Data.OracleClient.OracleBinary>.|  
|**BLOB**||**Blob**|Oracle n’autorise la liaison un **BLOB** comme un **BLOB** paramètre. Le fournisseur de données .NET pour Oracle ne construit pas automatiquement un pour vous si vous tentez de lier une non -**BLOB** valeur, telle que **byte []** ou <xref:System.Data.OracleClient.OracleBinary>.|  
|**CHAR**|**AnsiStringFixedLength**|**Char**||  
|**CLOB**||**Clob**|Oracle n’autorise la liaison un **CLOB** comme un **CLOB** paramètre. Le fournisseur de données .NET pour Oracle ne construit pas automatiquement un pour vous si vous tentez de lier une non -**CLOB** valeur, telle que **System.String** ou <xref:System.Data.OracleClient.OracleString>.|  
|**DATE**|**DateTime**|**DateTime**||  
|**FLOAT**|**Simple, Double, Decimal**|**Float, Double, Number**|<xref:System.Data.OracleClient.OracleParameter.Size%2A> Détermine le **System.Data.DBType** et <xref:System.Data.OracleClient.OracleType>.|  
|**INTEGER**|**SByte, Int16, Int32, Int64, Decimal**|**SByte, Int16, Int32, Number**|<xref:System.Data.OracleClient.OracleParameter.Size%2A> Détermine le **System.Data.DBType** et <xref:System.Data.OracleClient.OracleType>.|  
|**INTERVAL YEAR TO MONTH**|**Int32**|**IntervalYearToMonth**|<xref:System.Data.OracleClient.OracleType> est disponible uniquement lors de l’utilisation à la fois Oracle 9i du logiciel client et serveur.|  
|**INTERVAL DAY TO SECOND**|**Object**|**IntervalDayToSecond**|<xref:System.Data.OracleClient.OracleType> est disponible uniquement lors de l’utilisation à la fois Oracle 9i du logiciel client et serveur.|  
|**LONG**|**AnsiString**|**LongVarChar**||  
|**LONG RAW**|**Binaire**|**LongRaw**||  
|**NCHAR**|**StringFixedLength**|**NChar**||  
|**NCLOB**||**NClob**|Oracle n’autorise la liaison un **NCLOB** comme un **NCLOB** paramètre. Le fournisseur de données .NET pour Oracle ne construit pas automatiquement un pour vous si vous tentez de lier une non -**NCLOB** valeur, telle que **System.String** ou <xref:System.Data.OracleClient.OracleString>.|  
|**NUMBER**|**VarNumeric**|**nombre**||  
|**NVARCHAR2**|**Chaîne**|**NVarChar**||  
|**RAW**|**Binaire**|**Raw**||  
|**REF CURSOR**||**Curseur**|Pour plus d’informations, consultez [REF CURSOR Oracle](../../../../docs/framework/data/adonet/oracle-ref-cursors.md).|  
|**ROWID**|**AnsiString**|**Rowid**||  
|**TIMESTAMP**|**DateTime**|**Horodateur**|<xref:System.Data.OracleClient.OracleType> est disponible uniquement lors de l’utilisation à la fois Oracle 9i du logiciel client et serveur.|  
|**TIMESTAMP WITH LOCAL TIME ZONE**|**DateTime**|**TimestampLocal**|<xref:System.Data.OracleClient.OracleType> est disponible uniquement lors de l’utilisation à la fois Oracle 9i du logiciel client et serveur.|  
|**TIMESTAMP WITH TIME ZONE**|**DateTime**|**TimestampWithTz**|<xref:System.Data.OracleClient.OracleType> est disponible uniquement lors de l’utilisation à la fois Oracle 9i du logiciel client et serveur.|  
|**UNSIGNED INTEGER**|**Byte, UInt16, UInt32, UInt64, Decimal**|**Byte, UInt16, Uint32, Number**|<xref:System.Data.OracleClient.OracleParameter.Size%2A> Détermine le **System.Data.DBType** et <xref:System.Data.OracleClient.OracleType>.|  
|**VARCHAR2**|**AnsiString**|**VarChar**||  
  
 Le **InputOutput**, **sortie**, et **ReturnValue** **ParameterDirection** valeurs utilisées par le <xref:System.Data.OracleClient.OracleParameter.Value%2A> propriété de la <xref:System.Data.OracleClient.OracleParameter> objet sont des types de données .NET Framework, sauf si la valeur d’entrée est un type de données Oracle (par exemple, <xref:System.Data.OracleClient.OracleNumber> ou <xref:System.Data.OracleClient.OracleString>). Cela ne s’applique pas aux **REF CURSOR**, **BFILE**, ou **LOB** types de données.  
  
## <a name="see-also"></a>Voir aussi

- [Oracle et ADO.NET](../../../../docs/framework/data/adonet/oracle-and-adonet.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
