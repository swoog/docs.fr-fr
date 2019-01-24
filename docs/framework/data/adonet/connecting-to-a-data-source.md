---
title: Connexion à une source de données dans ADO.NET
ms.date: 03/30/2017
ms.assetid: 9abc3f92-1be3-4e1a-b360-762dc689650e
ms.openlocfilehash: 20cf22e1c9b9bf18dd3109cb9589c05a6c27d4d8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701740"
---
# <a name="connecting-to-a-data-source-in-adonet"></a><span data-ttu-id="74932-102">Connexion à une source de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="74932-102">Connecting to a Data Source in ADO.NET</span></span>
<span data-ttu-id="74932-103">Dans ADO.NET, vous utilisez un **connexion** objet pour se connecter à une source de données spécifique en fournissant des informations d’authentification nécessaires dans une chaîne de connexion.</span><span class="sxs-lookup"><span data-stu-id="74932-103">In ADO.NET you use a **Connection** object to connect to a specific data source by supplying necessary authentication information in a connection string.</span></span> <span data-ttu-id="74932-104">Le **connexion** objet que vous utilisez varie selon le type de source de données.</span><span class="sxs-lookup"><span data-stu-id="74932-104">The **Connection** object you use depends on the type of data source.</span></span>  
  
 <span data-ttu-id="74932-105">Chaque fournisseur de données .NET Framework inclut dans le .NET Framework comprend un objet <xref:System.Data.Common.DbConnection> : le fournisseur de données .ENT Framework pour OLE DB inclut un objet <xref:System.Data.OleDb.OleDbConnection>, le fournisseur de données .NET Framework pour SQL Server inclut un objet <xref:System.Data.SqlClient.SqlConnection>, le fournisseur de données .NET Framework pour ODBC inclut un objet <xref:System.Data.Odbc.OdbcConnection> et le fournisseur de données .NET Framework pour Oracle inclut un objet <xref:System.Data.OracleClient.OracleConnection>.</span><span class="sxs-lookup"><span data-stu-id="74932-105">Each .NET Framework data provider included with the .NET Framework has a <xref:System.Data.Common.DbConnection> object: the .NET Framework Data Provider for OLE DB includes an <xref:System.Data.OleDb.OleDbConnection> object, the .NET Framework Data Provider for SQL Server includes a <xref:System.Data.SqlClient.SqlConnection> object, the .NET Framework Data Provider for ODBC includes an <xref:System.Data.Odbc.OdbcConnection> object, and the .NET Framework Data Provider for Oracle includes an <xref:System.Data.OracleClient.OracleConnection> object.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="74932-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="74932-106">In This Section</span></span>  
 [<span data-ttu-id="74932-107">Établissement de la connexion</span><span class="sxs-lookup"><span data-stu-id="74932-107">Establishing the Connection</span></span>](../../../../docs/framework/data/adonet/establishing-the-connection.md)  
 <span data-ttu-id="74932-108">Décrit comment utiliser un **connexion** objet pour établir une connexion à une source de données.</span><span class="sxs-lookup"><span data-stu-id="74932-108">Describes how to use a **Connection** object to establish a connection to a data source.</span></span>  
  
 [<span data-ttu-id="74932-109">Événements de connexion</span><span class="sxs-lookup"><span data-stu-id="74932-109">Connection Events</span></span>](../../../../docs/framework/data/adonet/connection-events.md)  
 <span data-ttu-id="74932-110">Décrit comment utiliser un **InfoMessage** événement afin de récupérer les messages d’information à partir d’une source de données.</span><span class="sxs-lookup"><span data-stu-id="74932-110">Describes how to use an **InfoMessage** event to retrieve informational messages from a data source.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="74932-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74932-111">See also</span></span>
- [<span data-ttu-id="74932-112">Chaînes de connexion</span><span class="sxs-lookup"><span data-stu-id="74932-112">Connection Strings</span></span>](../../../../docs/framework/data/adonet/connection-strings.md)
- [<span data-ttu-id="74932-113">Regroupement de connexions</span><span class="sxs-lookup"><span data-stu-id="74932-113">Connection Pooling</span></span>](../../../../docs/framework/data/adonet/connection-pooling.md)
- [<span data-ttu-id="74932-114">Commandes et paramètres</span><span class="sxs-lookup"><span data-stu-id="74932-114">Commands and Parameters</span></span>](../../../../docs/framework/data/adonet/commands-and-parameters.md)
- [<span data-ttu-id="74932-115">DataAdapters et DataReaders</span><span class="sxs-lookup"><span data-stu-id="74932-115">DataAdapters and DataReaders</span></span>](../../../../docs/framework/data/adonet/dataadapters-and-datareaders.md)
- [<span data-ttu-id="74932-116">Transactions et accès concurrentiel</span><span class="sxs-lookup"><span data-stu-id="74932-116">Transactions and Concurrency</span></span>](../../../../docs/framework/data/adonet/transactions-and-concurrency.md)
- [<span data-ttu-id="74932-117">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="74932-117">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
