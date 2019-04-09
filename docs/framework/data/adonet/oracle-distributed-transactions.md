---
title: Transactions distribuées Oracle
ms.date: 03/30/2017
ms.assetid: c340ca81-ef79-402f-b204-c5156b890fe5
ms.openlocfilehash: 4af1c98818f1929850c5ae78892c64993a93d4d2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59116215"
---
# <a name="oracle-distributed-transactions"></a><span data-ttu-id="b78ef-102">Transactions distribuées Oracle</span><span class="sxs-lookup"><span data-stu-id="b78ef-102">Oracle Distributed Transactions</span></span>
<span data-ttu-id="b78ef-103">L'objet <xref:System.Data.OracleClient.OracleConnection> s'inscrit automatiquement dans une transaction distribuée existante s'il détermine qu'une transaction est active.</span><span class="sxs-lookup"><span data-stu-id="b78ef-103">The <xref:System.Data.OracleClient.OracleConnection> object automatically enlists in an existing distributed transaction if it determines that a transaction is active.</span></span> <span data-ttu-id="b78ef-104">L’inscription automatique dans une transaction se produit lorsque la connexion est ouverte et extraite du pool de connexions.</span><span class="sxs-lookup"><span data-stu-id="b78ef-104">Automatic transaction enlistment occurs when the connection is opened or retrieved from the connection pool.</span></span> <span data-ttu-id="b78ef-105">Vous pouvez désactiver l'inscription automatique dans des transactions existantes en spécifiant</span><span class="sxs-lookup"><span data-stu-id="b78ef-105">You can disable auto-enlistment in existing transactions by specifying</span></span>  
  
```  
Enlist=false  
```  
  
 <span data-ttu-id="b78ef-106">comme paramètre de chaîne de connexion pour un <xref:System.Data.OracleClient.OracleConnection>.</span><span class="sxs-lookup"><span data-stu-id="b78ef-106">as a connection string parameter for an <xref:System.Data.OracleClient.OracleConnection>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b78ef-107">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b78ef-107">See also</span></span>

- [<span data-ttu-id="b78ef-108">Oracle et ADO.NET</span><span class="sxs-lookup"><span data-stu-id="b78ef-108">Oracle and ADO.NET</span></span>](../../../../docs/framework/data/adonet/oracle-and-adonet.md)
- [<span data-ttu-id="b78ef-109">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="b78ef-109">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
