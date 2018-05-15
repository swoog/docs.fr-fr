---
title: Connexion à une source de données dans ADO.NET
ms.date: 03/30/2017
ms.assetid: 9abc3f92-1be3-4e1a-b360-762dc689650e
ms.openlocfilehash: 27653c3e1f14e08fc8b5e1225a441072778a0cc8
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="connecting-to-a-data-source-in-adonet"></a><span data-ttu-id="80375-102">Connexion à une source de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="80375-102">Connecting to a Data Source in ADO.NET</span></span>
<span data-ttu-id="80375-103">Dans ADO.NET, vous utilisez un **connexion** objet pour se connecter à une source de données spécifique en fournissant des informations d’authentification nécessaires dans une chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="80375-103">In ADO.NET you use a **Connection** object to connect to a specific data source by supplying necessary authentication information in a connection string.</span></span> <span data-ttu-id="80375-104">Le **connexion** objet que vous utilisez varie selon le type de source de données.</span><span class="sxs-lookup"><span data-stu-id="80375-104">The **Connection** object you use depends on the type of data source.</span></span>  
  
 <span data-ttu-id="80375-105">Chaque fournisseur de données .NET Framework inclut dans le .NET Framework comprend un objet <xref:System.Data.Common.DbConnection> : le fournisseur de données .ENT Framework pour OLE DB inclut un objet <xref:System.Data.OleDb.OleDbConnection>, le fournisseur de données .NET Framework pour SQL Server inclut un objet <xref:System.Data.SqlClient.SqlConnection>, le fournisseur de données .NET Framework pour ODBC inclut un objet <xref:System.Data.Odbc.OdbcConnection> et le fournisseur de données .NET Framework pour Oracle inclut un objet <xref:System.Data.OracleClient.OracleConnection>.</span><span class="sxs-lookup"><span data-stu-id="80375-105">Each .NET Framework data provider included with the .NET Framework has a <xref:System.Data.Common.DbConnection> object: the .NET Framework Data Provider for OLE DB includes an <xref:System.Data.OleDb.OleDbConnection> object, the .NET Framework Data Provider for SQL Server includes a <xref:System.Data.SqlClient.SqlConnection> object, the .NET Framework Data Provider for ODBC includes an <xref:System.Data.Odbc.OdbcConnection> object, and the .NET Framework Data Provider for Oracle includes an <xref:System.Data.OracleClient.OracleConnection> object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="80375-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="80375-106">In This Section</span></span>  
 [<span data-ttu-id="80375-107">Établissement de la connexion</span><span class="sxs-lookup"><span data-stu-id="80375-107">Establishing the Connection</span></span>](../../../../docs/framework/data/adonet/establishing-the-connection.md)  
 <span data-ttu-id="80375-108">Décrit comment utiliser un **connexion** objet pour établir une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="80375-108">Describes how to use a **Connection** object to establish a connection to a data source.</span></span>  
  
 [<span data-ttu-id="80375-109">Événements de connexion</span><span class="sxs-lookup"><span data-stu-id="80375-109">Connection Events</span></span>](../../../../docs/framework/data/adonet/connection-events.md)  
 <span data-ttu-id="80375-110">Décrit comment utiliser un **InfoMessage** événements pour récupérer des messages d’information à partir d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="80375-110">Describes how to use an **InfoMessage** event to retrieve informational messages from a data source.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80375-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80375-111">See Also</span></span>  
 [<span data-ttu-id="80375-112">Chaînes de connexion</span><span class="sxs-lookup"><span data-stu-id="80375-112">Connection Strings</span></span>](../../../../docs/framework/data/adonet/connection-strings.md)  
 [<span data-ttu-id="80375-113">Regroupement de connexions</span><span class="sxs-lookup"><span data-stu-id="80375-113">Connection Pooling</span></span>](../../../../docs/framework/data/adonet/connection-pooling.md)  
 [<span data-ttu-id="80375-114">Commandes et paramètres</span><span class="sxs-lookup"><span data-stu-id="80375-114">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)  
 [<span data-ttu-id="80375-115">DataAdapters et DataReaders</span><span class="sxs-lookup"><span data-stu-id="80375-115">DataAdapters and DataReaders</span></span>](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)  
 [<span data-ttu-id="80375-116">Transactions et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="80375-116">Transactions and Concurrency</span></span>](../../../../docs/framework/data/adonet/transactions-and-concurrency.md)  
 [<span data-ttu-id="80375-117">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="80375-117">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
