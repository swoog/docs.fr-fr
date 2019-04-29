---
title: Collections de schémas OLE DB
ms.date: 03/30/2017
ms.assetid: 6380c36b-658e-4d67-91e8-7131ef4a7c2c
ms.openlocfilehash: 6dc187b0a876d9e167a74f2381db156dde2764fe
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61771993"
---
# <a name="ole-db-schema-collections"></a>Collections de schémas OLE DB
Cette section traite de la prise en charge des collections de schémas pour les fournisseurs OLE DB de Microsoft SQL Server, Oracle et Microsoft Jet.  
  
## <a name="microsoft-sql-server-ole-db-provider"></a>Fournisseur Microsoft SQL Server OLE DB  
 Le pilote OLE DB Microsoft SQL Server prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :  
  
- Tables  
  
- Colonnes  
  
- Procédures  
  
- ProcedureParameters  
  
- Catalogue  
  
- Index  
  
### <a name="tables"></a>Tables  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|TABLE_TYPE|Chaîne|  
|TABLE_GUID|GUID|  
|DESCRIPTION|Chaîne|  
|TABLE_PROPID|Int64|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="columns"></a>Colonnes  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|ORDINAL_POSITION|Int64|  
|COLUMN_HASDEFAULT|Booléen|  
|COLUMN_DEFAULT|Chaîne|  
|COLUMN_FLAGS|Int64|  
|IS_NULLABLE|Booléen|  
|DATA_TYPE|Int32|  
|TYPE_GUID|GUID|  
|CHARACTER_MAXIMUM_LENGTH|Int64|  
|CHARACTER_OCTET_LENGTH|Int64|  
|NUMERIC_PRECISION|Int32|  
|NUMERIC_SCALE|Int16|  
|DATETIME_PRECISION|Int64|  
|CHARACTER_SET_CATALOG|Chaîne|  
|CHARACTER_SET_SCHEMA|Chaîne|  
|CHARACTER_SET_NAME|Chaîne|  
|COLLATION_CATALOG|Chaîne|  
|COLLATION_SCHEMA|Chaîne|  
|COLLATION_NAME|Chaîne|  
|DOMAIN_CATALOG|Chaîne|  
|DOMAIN_SCHEMA|Chaîne|  
|DOMAIN_NAME|Chaîne|  
|DESCRIPTION|Chaîne|  
|COLUMN_LCID|Int32|  
|COLUMN_COMPFLAGS|Int32|  
|COLUMN_SORTID|Int32|  
|COLUMN_TDSCOLLATION|Byte[]|  
|IS_COMPUTED|Booléen|  
  
### <a name="procedures"></a>Procédures  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|PROCEDURE_CATALOG|Chaîne|  
|PROCEDURE_SCHEMA|Chaîne|  
|PROCEDURE_NAME|Chaîne|  
|PROCEDURE_TYPE|Int16|  
|PROCEDURE_DEFINITION|Chaîne|  
|DESCRIPTION|Chaîne|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="procedureparameters"></a>ProcedureParameters  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|PROCEDURE_CATALOG|Chaîne|  
|PROCEDURE_SCHEMA|Chaîne|  
|PROCEDURE_NAME|Chaîne|  
|PARAMETER_NAME|Chaîne|  
|ORDINAL_POSITION|Int32|  
|PARAMETER_TYPE|Int32|  
|PARAMETER_HASDEFAULT|Booléen|  
|PARAMETER_DEFAULT|Chaîne|  
|IS_NULLABLE|Booléen|  
|DATA_TYPE|Int32|  
|CHARACTER_MAXIMUM_LENGTH|Int64|  
|CHARACTER_OCTET_LENGTH|Int64|  
|NUMERIC_PRECISION|Int32|  
|NUMERIC_SCALE|Int16|  
|DESCRIPTION|Chaîne|  
|TYPE_NAME|Chaîne|  
|LOCAL_TYPE_NAME|Chaîne|  
  
### <a name="catalog"></a>Catalogue  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|CATALOG_NAME|Chaîne|  
|DESCRIPTION|Chaîne|  
  
### <a name="indexes"></a>Index  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|INDEX_CATALOG|Chaîne|  
|INDEX_SCHEMA|Chaîne|  
|INDEX_NAME|Chaîne|  
|PRIMARY_KEY|Booléen|  
|UNIQUE|Booléen|  
|CLUSTERED|Booléen|  
|TYPE|Int32|  
|FILL_FACTOR|Int32|  
|INITIAL_SIZE|Int32|  
|NULLS|Int32|  
|SORT_BOOKMARKS|Booléen|  
|AUTO_UPDATE|Booléen|  
|NULL_COLLATION|Int32|  
|ORDINAL_POSITION|Int64|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|COLLATION|Int16|  
|CARDINALITY|Decimal|  
|PAGES|Int32|  
|FILTER_CONDITION|Chaîne|  
|INTEGRATED|Booléen|  
  
## <a name="microsoft-oracle-ole-db-provider"></a>Fournisseur Microsoft Oracle OLE DB  
 Le pilote Microsoft Oracle OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :  
  
- Tables  
  
- Colonnes  
  
- Procédures  
  
- ProcedureColumns  
  
- ProcedureParameters  
  
- Affichages  
  
- Index  
  
### <a name="tables"></a>Tables  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|TABLE_TYPE|Chaîne|  
|TABLE_GUID|GUID|  
|DESCRIPTION|Chaîne|  
|TABLE_PROPID|Int64|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="columns"></a>Colonnes  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|ORDINAL_POSITION|Int64|  
|COLUMN_HASDEFAULT|Booléen|  
|COLUMN_DEFAULT|Chaîne|  
|COLUMN_FLAGS|Int64|  
|IS_NULLABLE|Booléen|  
|DATA_TYPE|Int32|  
|TYPE_GUID|GUID|  
|CHARACTER_MAXIMUM_LENGTH|Int64|  
|CHARACTER_OCTET_LENGTH|Int64|  
|NUMERIC_PRECISION|Int32|  
|NUMERIC_SCALE|Int16|  
|DATETIME_PRECISION|Int64|  
|CHARACTER_SET_CATALOG|Chaîne|  
|CHARACTER_SET_SCHEMA|Chaîne|  
|CHARACTER_SET_NAME|Chaîne|  
|COLLATION_CATALOG|Chaîne|  
|COLLATION_SCHEMA|Chaîne|  
|COLLATION_NAME|Chaîne|  
|DOMAIN_CATALOG|Chaîne|  
|DOMAIN_SCHEMA|Chaîne|  
|DOMAIN_NAME|Chaîne|  
|DESCRIPTION|Chaîne|  
  
### <a name="procedures"></a>Procédures  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|PROCEDURE_CATALOG|Chaîne|  
|PROCEDURE_SCHEMA|Chaîne|  
|PROCEDURE_NAME|Chaîne|  
|PROCEDURE_TYPE|Int16|  
|PROCEDURE_DEFINITION|Chaîne|  
|DESCRIPTION|Chaîne|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="procedurecolumns"></a>ProcedureColumns  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|PROCEDURE_CATALOG|Chaîne|  
|PROCEDURE_SCHEMA|Chaîne|  
|PROCEDURE_NAME|Chaîne|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|ROWSET_NUMBER|Int64|  
|ORDINAL_POSITION|Int64|  
|IS_NULLABLE|Booléen|  
|DATA_TYPE|Int32|  
|TYPE_GUID|GUID|  
|CHARACTER_MAXIMUM_LENGTH|Int64|  
|CHARACTER_OCTET_LENGTH|Int64|  
|NUMERIC_PRECISION|Int32|  
|NUMERIC_SCALE|Int16|  
|DESCRIPTION|Chaîne|  
|OVERLOAD|Int16|  
  
### <a name="views"></a>Affichages  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|VIEW_DEFINITION|Chaîne|  
|CHECK_OPTION|Booléen|  
|IS_UPDATABLE|Booléen|  
|DESCRIPTION|Chaîne|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="indexes"></a>Index  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|INDEX_CATALOG|Chaîne|  
|INDEX_SCHEMA|Chaîne|  
|INDEX_NAME|Chaîne|  
|PRIMARY_KEY|Booléen|  
|UNIQUE|Booléen|  
|CLUSTERED|Booléen|  
|TYPE|Int32|  
|FILL_FACTOR|Int32|  
|INITIAL_SIZE|Int32|  
|NULLS|Int32|  
|SORT_BOOKMARKS|Booléen|  
|AUTO_UPDATE|Booléen|  
|NULL_COLLATION|Int32|  
|ORDINAL_POSITION|Int64|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|COLLATION|Int16|  
|CARDINALITY|Decimal|  
|PAGES|Int32|  
|FILTER_CONDITION|Chaîne|  
|INTEGRATED|Booléen|  
  
## <a name="microsoft-jet-ole-db-provider"></a>Fournisseur Microsoft Jet OLE DB  
 Le pilote Microsoft Jet OLE DB prend en charge les collections de schémas spécifiques suivantes en plus des collections de schémas courantes :  
  
- Tables  
  
- Colonnes  
  
- Procédures  
  
- Affichages  
  
- Index  
  
### <a name="tables"></a>Tables  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|TABLE_TYPE|Chaîne|  
|TABLE_GUID|GUID|  
|DESCRIPTION|Chaîne|  
|TABLE_PROPID|Int64|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="columns"></a>Colonnes  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|ORDINAL_POSITION|Int64|  
|COLUMN_HASDEFAULT|Booléen|  
|COLUMN_DEFAULT|Chaîne|  
|COLUMN_FLAGS|Int64|  
|IS_NULLABLE|Booléen|  
|DATA_TYPE|Int32|  
|TYPE_GUID|GUID|  
|CHARACTER_MAXIMUM_LENGTH|Int64|  
|CHARACTER_OCTET_LENGTH|Int64|  
|NUMERIC_PRECISION|Int32|  
|NUMERIC_SCALE|Int16|  
|DATETIME_PRECISION|Int64|  
|CHARACTER_SET_CATALOG|Chaîne|  
|CHARACTER_SET_SCHEMA|Chaîne|  
|CHARACTER_SET_NAME|Chaîne|  
|COLLATION_CATALOG|Chaîne|  
|COLLATION_SCHEMA|Chaîne|  
|COLLATION_NAME|Chaîne|  
|DOMAIN_CATALOG|Chaîne|  
|DOMAIN_SCHEMA|Chaîne|  
|DOMAIN_NAME|Chaîne|  
|DESCRIPTION|Chaîne|  
  
### <a name="procedures"></a>Procédures  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|PROCEDURE_CATALOG|Chaîne|  
|PROCEDURE_SCHEMA|Chaîne|  
|PROCEDURE_NAME|Chaîne|  
|PROCEDURE_TYPE|Int16|  
|PROCEDURE_DEFINITION|Chaîne|  
|DESCRIPTION|Chaîne|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="views"></a>Affichages  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|VIEW_DEFINITION|Chaîne|  
|CHECK_OPTION|Booléen|  
|IS_UPDATABLE|Booléen|  
|DESCRIPTION|Chaîne|  
|DATE_CREATED|DateTime|  
|DATE_MODIFIED|DateTime|  
  
### <a name="indexes"></a>Index  
  
|Nom de colonne|Type de données|  
|----------------|--------------|  
|TABLE_CATALOG|Chaîne|  
|TABLE_SCHEMA|Chaîne|  
|TABLE_NAME|Chaîne|  
|INDEX_CATALOG|Chaîne|  
|INDEX_SCHEMA|Chaîne|  
|INDEX_NAME|Chaîne|  
|PRIMARY_KEY|Booléen|  
|UNIQUE|Booléen|  
|CLUSTERED|Booléen|  
|TYPE|Int32|  
|FILL_FACTOR|Int32|  
|INITIAL_SIZE|Int32|  
|NULLS|Int32|  
|SORT_BOOKMARKS|Booléen|  
|AUTO_UPDATE|Booléen|  
|NULL_COLLATION|Int32|  
|ORDINAL_POSITION|Int64|  
|COLUMN_NAME|Chaîne|  
|COLUMN_GUID|GUID|  
|COLUMN_PROPID|Int64|  
|COLLATION|Int16|  
|CARDINALITY|Decimal|  
|PAGES|Int32|  
|FILTER_CONDITION|Chaîne|  
|INTEGRATED|Booléen|  
  
## <a name="see-also"></a>Voir aussi

- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
