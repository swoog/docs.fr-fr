---
title: Regroupement de connexions
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 955c057f-aea8-4ba8-aa6d-e3dfa18ba8d5
caps.latest.revision: 3
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: 3cc97ec0681e58facd30e3dbbb74001676a6e451
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="connection-pooling"></a><span data-ttu-id="533c8-102">Regroupement de connexions</span><span class="sxs-lookup"><span data-stu-id="533c8-102">Connection Pooling</span></span>
<span data-ttu-id="533c8-103">Se connecter à une source de données peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="533c8-103">Connecting to a data source can be time consuming.</span></span> <span data-ttu-id="533c8-104">Pour réduire le coût de l’ouverture de connexions, ADO.NET utilise une technique d’optimisation nommée *le regroupement de connexions*, ce qui réduit le coût de l’ouverture et la fermeture des connexions.</span><span class="sxs-lookup"><span data-stu-id="533c8-104">To minimize the cost of opening connections, ADO.NET uses an optimization technique called *connection pooling*, which minimizes the cost of repeatedly opening and closing connections.</span></span> <span data-ttu-id="533c8-105">Le regroupement de connexions est géré différemment pour les fournisseurs de données .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="533c8-105">Connection pooling is handled differently for the .NET Framework data providers.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="533c8-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="533c8-106">In This Section</span></span>  
 [<span data-ttu-id="533c8-107">Regroupement de connexions SQL Server (ADO.NET)</span><span class="sxs-lookup"><span data-stu-id="533c8-107">SQL Server Connection Pooling (ADO.NET)</span></span>](../../../../docs/framework/data/adonet/sql-server-connection-pooling.md)  
 <span data-ttu-id="533c8-108">Fournit une vue d’ensemble du regroupement de connexions et décrit le fonctionne du regroupement de connexions dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="533c8-108">Provides an overview of connection pooling and describes how connection pooling works in SQL Server.</span></span>  
  
 [<span data-ttu-id="533c8-109">Regroupement de connexions OLE DB, ODBC et Oracle</span><span class="sxs-lookup"><span data-stu-id="533c8-109">OLE DB, ODBC, and Oracle Connection Pooling</span></span>](../../../../docs/framework/data/adonet/ole-db-odbc-and-oracle-connection-pooling.md)  
 <span data-ttu-id="533c8-110">Décrit le regroupement de connexions pour les fournisseurs de données .NET Framework pour OLE DB, ODBC et Oracle.</span><span class="sxs-lookup"><span data-stu-id="533c8-110">Describes connection pooling for the .NET Framework Data Provider for OLE DB, the .NET Framework Data Provider for ODBC, and the .NET Framework Data Provider for Oracle.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="533c8-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="533c8-111">See Also</span></span>  
 [<span data-ttu-id="533c8-112">Extraction et modification de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="533c8-112">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [<span data-ttu-id="533c8-113">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="533c8-113">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
