---
title: Mappages de types de données dans ADO.NET
ms.date: 03/30/2017
ms.assetid: d4afab94-ada6-4c77-a73c-41f17bae6b5a
ms.openlocfilehash: 4e85db4732da664848cee2ef48f9a880a86fef18
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65583758"
---
# <a name="data-type-mappings-in-adonet"></a>Mappages de types de données dans ADO.NET
Le .NET Framework est basé sur le système de type commun, qui définit la manière dont les types sont déclarés, utilisés et gérés dans le runtime. Il est constitué de types de valeur et de types de référence, qui dérivent tous du type de base <xref:System.Object>. Lorsque vous travaillez avec une source de données, le type de données est déduit du fournisseur de données s'il n'est pas explicitement spécifié. Par exemple, un objet <xref:System.Data.DataSet> est indépendant de toute source de données spécifique. Les données d'un `DataSet` sont extraites d'une source de données et les modifications y sont répercutées à l'aide d'un `DataAdapter`. Cela signifie que, lorsqu’un `DataAdapter` remplit un <xref:System.Data.DataTable> dans un `DataSet` avec des valeurs à partir d’une source de données, les types de données qui en résulte des colonnes dans le `DataTable` sont des types .NET Framework, au lieu de types spécifiques au fournisseur de données .NET Framework qui est utilisé pour se connecter à la source de données.  
  
 De même, quand un `DataReader` retourne une valeur à partir d’une source de données, la valeur résultante est stockée dans une variable locale qui a un type .NET Framework. Pour les deux le `Fill` opérations de la `DataAdapter` et `Get` méthodes de la `DataReader`, le type .NET Framework est déduit à partir de la valeur retournée par le fournisseur de données .NET Framework.  
  
 Si vous ne souhaitez pas utiliser le type de données déduit, vous pouvez appeler les méthodes d’accesseur typé du `DataReader`, lorsque vous connaissez le type spécifique de la valeur retournée. Méthodes d’accesseur typées offrir de meilleures performances en retournant une valeur comme un type .NET Framework spécifique, ce qui évite la conversion de type supplémentaire.  
  
> [!NOTE]
>  Les valeurs NULL pour les types de données de fournisseur de données .NET Framework sont représentées par `DBNull.Value`.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Mappages de types de données SQL Server](../../../../docs/framework/data/adonet/sql-server-data-type-mappings.md)  
 Répertorie les mappages de types de données déduits et les méthodes d'accesseur de données pour <xref:System.Data.SqlClient>.  
  
 [Mappages de types de données OLE DB](../../../../docs/framework/data/adonet/ole-db-data-type-mappings.md)  
 Répertorie les mappages de types de données déduits et les méthodes d'accesseur de données pour <xref:System.Data.OleDb>.  
  
 [Mappages de types de données ODBC](../../../../docs/framework/data/adonet/odbc-data-type-mappings.md)  
 Répertorie les mappages de types de données déduits et les méthodes d'accesseur de données pour <xref:System.Data.Odbc>.  
  
 [Mappages de types de données Oracle](../../../../docs/framework/data/adonet/oracle-data-type-mappings.md)  
 Répertorie les mappages de types de données déduits et les méthodes d'accesseur de données pour <xref:System.Data.OracleClient>.  
  
 [Nombres à virgule flottante](../../../../docs/framework/data/adonet/floating-point-numbers.md)  
 Décrit les problèmes que les développeurs rencontrent fréquemment lorsqu'ils utilisent des nombres à virgule flottante.  
  
## <a name="see-also"></a>Voir aussi

- [Types de données SQL Server et ADO.NET](../../../../docs/framework/data/adonet/sql/sql-server-data-types.md)
- [Configuration des paramètres et des types de données des paramètres](../../../../docs/framework/data/adonet/configuring-parameters-and-parameter-data-types.md)
- [Récupération des informations de schéma de base de données](../../../../docs/framework/data/adonet/retrieving-database-schema-information.md)
- [Système de type commun](../../../../docs/standard/base-types/common-type-system.md)
- [Conversion de Types](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/t8s7t9bf(v=vs.90))
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
