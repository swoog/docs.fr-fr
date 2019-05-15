---
title: Fournisseur de données .NET Framework
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 03a9fc62-2d24-491a-9fe6-d6bdb6dcb131
ms.openlocfilehash: 9fead8a5d54fba7232831bba349f27b7eed4657b
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65583784"
---
# <a name="net-framework-data-providers"></a>Fournisseur de données .NET Framework
Un fournisseur de données .NET Framework est utilisé pour la connexion à une base de données, l’exécution de commandes et l’extraction des résultats. Ces résultats sont traités directement, placés dans un objet <xref:System.Data.DataSet> pour pouvoir être exposés à l'utilisateur le cas échéant, combinés aux données de différentes sources ou accessibles à distance entre couches. Fournisseurs de données .NET framework sont légers et création d’une couche minimale entre la source de données et le code, augmentent les performances sans nuire aux fonctionnalités.  
  
 Le tableau suivant répertorie les fournisseurs de données qui sont inclus dans le .NET Framework.  
  
|fournisseur de données .NET Framework|Description|  
|-------------------------------------------------------------------------------|-----------------|  
|Fournisseur de données .NET Framework pour SQL Server|Fournit l'accès aux données pour Microsoft SQL Server. Utilise l'espace de noms <xref:System.Data.SqlClient> .|  
|Fournisseur de données .NET Framework pour OLE DB|Pour les sources de données exposées à l'aide de OLE DB. Utilise l'espace de noms <xref:System.Data.OleDb> .|  
|fournisseur de données .NET Framework pour ODBC|Pour les sources de données exposées à l'aide de ODBC. Utilise l'espace de noms <xref:System.Data.Odbc> .|  
|fournisseur de données .NET Framework pour Oracle|Pour les sources de données Oracle. Le fournisseur de données .NET Framework pour Oracle prend en charge le logiciel client Oracle version 8.1.7 et versions ultérieures et utilise le <xref:System.Data.OracleClient> espace de noms.|  
|fournisseur EntityClient|Fournit un accès aux données pour les applications EDM (Entity Data Model). Utilise l'espace de noms <xref:System.Data.EntityClient> .|  
|Fournisseur de données .NET framework pour SQL Server Compact 4.0.|Fournit l’accès aux données pour Microsoft SQL Server Compact 4.0. Utilise l’espace de noms [System.Data.SqlServerCe](https://docs.microsoft.com/previous-versions/sql/compact/sql-server-compact-4.0/ec4st0e3(v=vs.100)) .|  
  
## <a name="core-objects-of-net-framework-data-providers"></a>Objets principaux des fournisseurs de données .NET Framework  
 Le tableau suivant décrit les quatre principaux objets qui composent un fournisseur de données .NET Framework.  
  
|Object|Description|  
|------------|-----------------|  
|`Connection`|Établit une connexion à une source de données spécifique. La classe de base pour tous les objets `Connection` est la classe <xref:System.Data.Common.DbConnection> .|  
|`Command`|Exécute une commande sur une source de données. Expose `Parameters` et peut exécuter dans la portée d'une `Transaction` à partir d'un `Connection`. La classe de base pour tous les objets `Command` est la classe <xref:System.Data.Common.DbCommand> .|  
|`DataReader`|Lit un flux de données avant uniquement (forward only) et en lecture seule à partir d'une source de données. La classe de base pour tous les objets `DataReader` est la classe <xref:System.Data.Common.DbDataReader> .|  
|`DataAdapter`|Remplit un `DataSet` et répercute les mises à jour dans la source de données. La classe de base pour tous les objets `DataAdapter` est la classe <xref:System.Data.Common.DbDataAdapter> .|  
  
 En plus des principales classes répertoriées dans le tableau précédemment dans ce document, un fournisseur de données .NET Framework contient également les classes répertoriées dans le tableau suivant.  
  
|Object|Description|  
|------------|-----------------|  
|`Transaction`|Inscrit des commandes dans des transactions au niveau de la source de données. La classe de base pour tous les objets `Transaction` est la classe <xref:System.Data.Common.DbTransaction> . ADO.NET fournit aussi la prise en charge pour les transactions à l'aide des classes dans l'espace de noms <xref:System.Transactions> .|  
|`CommandBuilder`|Objet d'assistance qui génère automatiquement les propriétés de commande d'un `DataAdapter` ou dérive les informations sur les paramètres à partir d'une procédure stockée et remplit la collection `Parameters` d'un objet `Command` . La classe de base pour tous les objets `CommandBuilder` est la classe <xref:System.Data.Common.DbCommandBuilder> .|  
|`ConnectionStringBuilder`|Objet d'assistance qui offre une manière simple de créer et de gérer le contenu de chaînes de connexion utilisées par les objets `Connection` . La classe de base pour tous les objets `ConnectionStringBuilder` est la classe <xref:System.Data.Common.DbConnectionStringBuilder> .|  
|`Parameter`|Définit les paramètres des valeurs d'entrée, de sortie et de retour pour les commandes et les procédures stockées. La classe de base pour tous les objets `Parameter` est la classe <xref:System.Data.Common.DbParameter> .|  
|`Exception`|Retourné en cas d'erreur au niveau de la source de données. Une erreur au niveau du client, les fournisseurs de données .NET Framework lèvent une exception .NET Framework. La classe de base pour tous les objets `Exception` est la classe <xref:System.Data.Common.DbException> .|  
|`Error`|Expose les informations provenant d'un avertissement ou d'une erreur retournée par une source de données.|  
|`ClientPermission`|Fourni pour les attributs de sécurité d’accès du code du fournisseur de données .NET Framework. La classe de base pour tous les objets `ClientPermission` est la classe <xref:System.Data.Common.DBDataPermission> .|  
  
## <a name="net-framework-data-provider-for-sql-server-sqlclient"></a>Fournisseur de données .NET Framework pour SQL Server (SqlClient)  
 Le fournisseur de données .NET Framework pour SQL Server (SqlClient) utilise son propre protocole pour communiquer avec SQL Server. Il est léger et fonctionne bien car il est optimisé pour accéder à un serveur SQL Server directement sans l’ajout d’une couche OLE DB ou ODBC Open Database Connectivity (). L’illustration suivante compare le fournisseur de données .NET Framework pour SQL Server avec le fournisseur de données .NET Framework pour OLE DB. Le fournisseur de données .NET Framework pour OLE DB communique avec une source de données OLE DB via le composant de Service OLE DB, qui fournit le regroupement de connexions et les services de transaction et le fournisseur OLE DB pour la source de données.  
  
> [!NOTE]
>  Le fournisseur de données .NET Framework pour ODBC présente une architecture similaire au fournisseur de données .NET Framework pour OLE DB ; par exemple, il appelle un composant de Service ODBC.  
  
 ![Fournisseurs de données](../../../../docs/framework/data/adonet/media/netdataproviders-bpuedev11.gif "NETDataProviders_bpuedev11")  
Comparaison du fournisseur de données .NET Framework pour SQL Server et du fournisseur de données .NET Framework pour OLE DB  
  
 Le fournisseur de données .NET Framework pour les classes de SQL Server se trouvent dans le <xref:System.Data.SqlClient> espace de noms.  
  
 Le fournisseur de données .NET Framework pour SQL Server prend en charge les transactions locales et distribuées. Pour les transactions distribuées, le fournisseur de données .NET Framework pour SQL Server, par défaut, automatiquement inscrit dans une transaction et obtient les détails de transaction des Services de composants Windows ou <xref:System.Transactions>. Pour plus d’informations, consultez [Transactions et la concurrence](../../../../docs/framework/data/adonet/transactions-and-concurrency.md).  
  
 L'exemple de code suivant montre comment inclure l'espace de noms `System.Data.SqlClient` dans vos applications.  
  
```vb  
Imports System.Data.SqlClient  
```  
  
```csharp  
using System.Data.SqlClient;  
```  
  
## <a name="net-framework-data-provider-for-ole-db"></a>Fournisseur de données .NET Framework pour OLE DB  
 Le fournisseur de données .NET Framework pour OLE DB (OleDb) utilise OLE DB natif via COM interop pour accéder aux données. Le fournisseur de données .NET Framework pour OLE DB prend en charge les transactions locales et distribuées. Pour les transactions distribuées, le fournisseur de données .NET Framework pour OLE DB, par défaut, automatiquement inscrit dans une transaction et obtient les détails de transaction des Services de composants Windows. Pour plus d’informations, consultez [Transactions et la concurrence](../../../../docs/framework/data/adonet/transactions-and-concurrency.md).  
  
 Le tableau suivant montre les fournisseurs qui ont été testés avec [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)].  
  
|Pilote|Fournisseur|  
|------------|--------------|  
|SQLOLEDB|Fournisseur Microsoft OLE DB pour SQL Server|  
|MSDAORA|Fournisseur Microsoft OLE DB pour Oracle|  
|Microsoft.Jet.OLEDB.4.0|Fournisseur OLE DB pour Microsoft Jet|  
  
> [!NOTE]
>  Il est déconseillé d'utiliser une base de données Access (Jet) comme source de données pour les applications multithread, telles que les applications [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] . Si vous devez utiliser Jet comme source de données pour une application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] , sachez que les applications [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] qui se connectent à une base de données Access peuvent rencontrer des problèmes de connexion.  
  
 Le fournisseur de données .NET Framework pour OLE DB ne prend pas en charge les interfaces OLE DB version 2.5. Les fournisseurs OLE DB qui requièrent la prise en charge des interfaces OLE DB 2.5 fonctionnera pas correctement avec le fournisseur de données .NET Framework pour OLE DB. C'est le cas du fournisseur Microsoft OLE DB pour Exchange et du fournisseur Microsoft OLE DB pour Internet Publishing.  
  
 Le fournisseur de données .NET Framework pour OLE DB ne fonctionne pas avec le fournisseur OLE DB pour ODBC (MSDASQL). Pour accéder à une source de données ODBC à l’aide [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)], utilisez le fournisseur de données .NET Framework pour ODBC.  
  
 Fournisseur de données .NET framework pour OLE DB classes se trouvent dans le <xref:System.Data.OleDb> espace de noms. L'exemple de code suivant montre comment inclure l'espace de noms `System.Data.OleDb` dans vos applications.  
  
```vb  
Imports System.Data.OleDb  
```  
  
```csharp  
using System.Data.OleDb;  
```  
  
## <a name="net-framework-data-provider-for-odbc"></a>fournisseur de données .NET Framework pour ODBC  
 Le fournisseur de données .NET Framework pour ODBC (Odbc) utilise le Gestionnaire de pilotes (DM) ODBC natif pour accéder aux données. Le fournisseur de données pour ODBC prend en charge les transactions locales et distribuées. Pour les transactions distribuées, le fournisseur de données ODBC s’inscrit automatiquement par défaut dans une transaction et obtient des détails de transaction des services de composants Windows. Pour plus d’informations, consultez [Transactions et la concurrence](../../../../docs/framework/data/adonet/transactions-and-concurrency.md).  
  
 Le tableau suivant indique les pilotes ODBC qui ont été testés avec [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)].  
  
|Pilote|  
|------------|  
|SQL Server|  
|Microsoft ODBC pour Oracle|  
|Pilote Microsoft Access (*.mdb)|  
  
 Fournisseur de données .NET framework pour les classes ODBC sont situés dans le <xref:System.Data.Odbc> espace de noms.  
  
 L'exemple de code suivant montre comment inclure l'espace de noms `System.Data.Odbc` dans vos applications.  
  
```vb  
Imports System.Data.Odbc  
```  
  
```csharp  
using System.Data.Odbc;  
```  
  
> [!NOTE]
>  Le fournisseur de données .NET Framework pour ODBC requiert MDAC version 2.6 ou ultérieure et MDAC 2.8 SP1 est recommandé. Vous pouvez télécharger MDAC 2.8 SP1 à partir du [Data Access and Storage Developer Center](https://go.microsoft.com/fwlink/?linkid=4173).  
  
## <a name="net-framework-data-provider-for-oracle"></a>fournisseur de données .NET Framework pour Oracle  
 Le fournisseur de données .NET Framework pour Oracle (OracleClient) permet l’accès aux sources de données Oracle via le logiciel de connectivité client Oracle. Il prend en charge le logiciel client Oracle version 8.1.7 ou ultérieure. Le fournisseur de données prend en charge les transactions locales et distribuées. Pour plus d’informations, consultez [Transactions et la concurrence](../../../../docs/framework/data/adonet/transactions-and-concurrency.md).  
  
 Le fournisseur de données .NET Framework pour Oracle requiert le logiciel du client Oracle (version 8.1.7 ou une version ultérieure) sur le système avant de vous connecter à une source de données Oracle.  
  
 Fournisseur de données .NET framework pour les classes d’Oracle sont situés dans le <xref:System.Data.OracleClient> espace de noms et sont contenues dans le `System.Data.OracleClient.dll` assembly. Vous devez référencer `System.Data.dll` ainsi que `System.Data.OracleClient.dll` lorsque vous compilez une application qui utilise le fournisseur de données.  
  
 L'exemple de code suivant montre comment inclure l'espace de noms `System.Data.OracleClient` dans vos applications.  
  
```vb  
Imports System.Data  
Imports System.Data.OracleClient  
```  
  
```csharp  
using System.Data;  
using System.Data.OracleClient;  
```  
  
## <a name="choosing-a-net-framework-data-provider"></a>Choix d'un fournisseur de données .NET Framework  
 Selon la source de données et de conception pour votre application, votre choix de fournisseur de données .NET Framework peut améliorer les performances, fonctionnalité et l’intégrité de votre application. Le tableau suivant présente les avantages et les limites de chaque fournisseur de données .NET Framework.  
  
|Fournisseur|Notes|  
|--------------|-----------|  
|Fournisseur de données .NET Framework pour SQL Server|Recommandé pour les applications de couche intermédiaire qui utilisent Microsoft SQL Server.<br /><br /> Recommandé pour les applications monocouches qui utilisent Microsoft Database Engine (MSDE) ou SQL Server.<br /><br /> Recommandé dans l’utilisation du fournisseur OLE DB pour SQL Server (SQLOLEDB) avec le fournisseur de données .NET Framework pour OLE DB.|  
|Fournisseur de données .NET Framework pour OLE DB|Pour SQL Server, le fournisseur de données .NET Framework pour SQL Server est recommandé au lieu de ce fournisseur.<br /><br /> Il est recommandé pour les applications monocouches qui utilisent des bases de données Microsoft Access. L'utilisation d'une base de données Access pour une application de couche intermédiaire est déconseillée.|  
|fournisseur de données .NET Framework pour ODBC|Recommandé pour les applications monocouches et de couche intermédiaire qui utilisent des sources de données ODBC.|  
|fournisseur de données .NET Framework pour Oracle|Recommandé pour les applications monocouches et de couche intermédiaire qui utilisent des sources de données Oracle.|  
  
## <a name="entityclient-provider"></a>fournisseur EntityClient  
 Le fournisseur EntityClient permet d'accéder aux données basées sur un modèle de données d'entité EDM (Entity Data Model). Contrairement aux autres fournisseurs de données .NET Framework, il n'interagit pas directement avec une source de données. Au lieu de cela, il utilise Entity SQL pour communiquer avec le fournisseur de données sous-jacent. Pour plus d’informations, consultez [fournisseur EntityClient pour Entity Framework](./ef/entityclient-provider-for-the-entity-framework.md).  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble d’ADO.NET](../../../../docs/framework/data/adonet/ado-net-overview.md)
- [Extraction et modification de données dans ADO.NET](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
