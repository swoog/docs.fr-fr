---
title: Mappages de types de données ODBC
ms.date: 03/30/2017
ms.assetid: 43c35d32-831d-480f-a150-78f7e869d17f
ms.openlocfilehash: 8165ab933352394e29cbe93a9e8ba64267f8ae60
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772214"
---
# <a name="odbc-data-type-mappings"></a>Mappages de types de données ODBC
Le tableau suivant présente le type [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] déduit pour les types de données du fournisseur de données .NET Framework pour ODBC (<xref:System.Data.Odbc>). Les méthodes d’accesseur typées pour les <xref:System.Data.Odbc.OdbcDataReader> sont également répertoriés.  
  
|Type ODBC|Type [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]|Accesseur typé [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]|  
|---------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|  
|SQL_BIGINT|Int64|GetInt64()|  
|SQL_BINARY|Byte[]|GetBytes()|  
|SQL_BIT|Booléen|GetBoolean()|  
|SQL_CHAR|Chaîne<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_DECIMAL|Decimal|GetDecimal()|  
|SQL_DOUBLE|Double|GetDouble()|  
|SQL_GUID|GUID|GetGuid()|  
|SQL_INTEGER|Int32|GetInt32()|  
|SQL_LONG_VARCHAR|Chaîne<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_LONGVARBINARY|Byte[]|GetBytes()|  
|SQL_NUMERIC|Decimal|GetDecimal()|  
|SQL_REAL|Single|GetFloat()|  
|SQL_SMALLINT|Int16|GetInt16()|  
|SQL_TINYINT|Byte|GetByte()|  
|SQL_TYPE_TIMES|DateTime|GetDateTime()|  
|SQL_TYPE_TIMESTAMP|DateTime|GetDateTime()|  
|SQL_VARBINARY|Byte[]|GetBytes()|  
|SQL_WCHAR|Chaîne<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_WLONGVARCHAR|Chaîne<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
|SQL_WVARCHAR|Chaîne<br /><br /> Char[]|GetString()<br /><br /> GetChars()|  
  
## <a name="see-also"></a>Voir aussi

- [Extraction et modification de données dans ADO.NET](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
