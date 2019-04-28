---
title: Génération SQL dans le Fournisseur d'exemples
ms.date: 03/30/2017
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
ms.openlocfilehash: 88223930b65ccec9d030104c62d8b4b2e77ddbe2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61879292"
---
# <a name="sql-generation-in-the-sample-provider"></a><span data-ttu-id="82d90-102">Génération SQL dans le Fournisseur d'exemples</span><span class="sxs-lookup"><span data-stu-id="82d90-102">SQL Generation in the Sample Provider</span></span>
<span data-ttu-id="82d90-103">Le [Entity Framework Sample Provider](https://code.msdn.microsoft.com/windowsdesktop/Entity-Framework-Sample-6a9801d0) montre les nouveaux composants des fournisseurs de données ADO.NET qui prennent en charge la [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="82d90-103">The [Entity Framework Sample Provider](https://code.msdn.microsoft.com/windowsdesktop/Entity-Framework-Sample-6a9801d0) demonstrates the new components of ADO.NET Data Providers that support the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span>  <span data-ttu-id="82d90-104">Il utilise une base de données SQL Server 2005 et est implémenté comme un wrapper pour le fournisseur de données System.Data.SqlClient ADO.NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="82d90-104">It works with a SQL Server 2005 database and is implemented as a wrapper for the System.Data.SqlClient ADO.NET 2.0 Data Provider.</span></span>  
  
 <span data-ttu-id="82d90-105">Le module Génération SQL du Fournisseur d’exemples (situé sous le dossier Génération SQL, à l’exception du fichier DmlSqlGenerator.cs) prend un DbQueryCommandTree d’entrée et produit une instruction SQL SELECT unique.</span><span class="sxs-lookup"><span data-stu-id="82d90-105">The SQL Generation module of the Sample Provider (located under the SQL Generation folder, except for the file DmlSqlGenerator.cs) takes an input DbQueryCommandTree and produces a single SQL SELECT statement.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="82d90-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="82d90-106">In This Section</span></span>  
 <span data-ttu-id="82d90-107">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="82d90-107">This section includes the following topics:</span></span>  
  
 [<span data-ttu-id="82d90-108">Architecture et conception</span><span class="sxs-lookup"><span data-stu-id="82d90-108">Architecture and Design</span></span>](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [<span data-ttu-id="82d90-109">Procédure pas à pas : Génération SQL</span><span class="sxs-lookup"><span data-stu-id="82d90-109">Walkthrough: SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a><span data-ttu-id="82d90-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82d90-110">See also</span></span>

- [<span data-ttu-id="82d90-111">Génération SQL</span><span class="sxs-lookup"><span data-stu-id="82d90-111">SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
