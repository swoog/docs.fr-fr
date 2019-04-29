---
title: Valeurs des colonnes SQL XML
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d97ce4da-f09c-4d1e-85b7-a0ccedd7246a
ms.openlocfilehash: 803357f9ae97eee2cbbf5e777dbc1210ded26ab2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61670129"
---
# <a name="sql-xml-column-values"></a>Valeurs des colonnes SQL XML
SQL Server prend en charge la `xml` type de données, et les développeurs peuvent extraire des ensembles de résultats incluant ce type à l’aide d’un comportement standard de la <xref:System.Data.SqlClient.SqlCommand> classe. Une colonne `xml` peut être extraite comme toute colonne (par exemple, dans un <xref:System.Data.SqlClient.SqlDataReader>) mais si vous souhaitez utiliser le contenu de la colonne comme XML, vous devez utiliser un <xref:System.Xml.XmlReader>.  
  
## <a name="example"></a>Exemple  
 L’application console suivante sélectionne deux lignes, chacune contenant un `xml` colonne, à partir de la **Sales.Store** table dans le **AdventureWorks** de base de données à un <xref:System.Data.SqlClient.SqlDataReader> instance. Pour chaque ligne, la valeur de la colonne `xml` est lue à l'aide de la méthode <xref:System.Data.SqlClient.SqlDataReader.GetSqlXml%2A> de <xref:System.Data.SqlClient.SqlDataReader>. La valeur est stockée dans un <xref:System.Xml.XmlReader>. Notez que vous devez utiliser la méthode <xref:System.Data.SqlClient.SqlDataReader.GetSqlXml%2A> plutôt que la méthode <xref:System.Data.IDataRecord.GetValue%2A> si vous souhaitez définir le contenu comme une variable <xref:System.Data.SqlTypes.SqlXml> ; <xref:System.Data.IDataRecord.GetValue%2A> retourne la valeur de la colonne `xml` comme chaîne.  
  
> [!NOTE]
>  Le **AdventureWorks** base de données exemple n’est pas installé par défaut lorsque vous installez SQL Server. Vous pouvez l'installer en exécutant l'Installation de SQL Server.  
  
 [!code-csharp[DataWorks SqlClient.GetXmlDataReader#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlClient.GetXmlDataReader/CS/source.cs#1)]
 [!code-vb[DataWorks SqlClient.GetXmlDataReader#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlClient.GetXmlDataReader/VB/source.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Data.SqlTypes.SqlXml>
- [Données XML dans SQL Server](../../../../../docs/framework/data/adonet/sql/xml-data-in-sql-server.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
