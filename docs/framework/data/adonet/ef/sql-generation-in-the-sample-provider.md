---
title: Génération SQL dans le Fournisseur d'exemples
ms.date: 03/30/2017
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
ms.openlocfilehash: 7275a67927d7692dc943e2555d65d1f7d6e4ba5a
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32762151"
---
# <a name="sql-generation-in-the-sample-provider"></a><span data-ttu-id="8bf5b-102">Génération SQL dans le Fournisseur d'exemples</span><span class="sxs-lookup"><span data-stu-id="8bf5b-102">SQL Generation in the Sample Provider</span></span>
<span data-ttu-id="8bf5b-103">Le [Entity Framework Sample Provider](http://go.microsoft.com/fwlink/?LinkId=180616) illustre les composants de fournisseurs de données ADO.NET qui prennent en charge la [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="8bf5b-103">The [Entity Framework Sample Provider](http://go.microsoft.com/fwlink/?LinkId=180616) demonstrates the new components of ADO.NET Data Providers that support the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span>  <span data-ttu-id="8bf5b-104">Il utilise une base de données SQL Server 2005 et est implémenté comme un wrapper pour le fournisseur de données System.Data.SqlClient ADO.NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-104">It works with a SQL Server 2005 database and is implemented as a wrapper for the System.Data.SqlClient ADO.NET 2.0 Data Provider.</span></span>  
  
 <span data-ttu-id="8bf5b-105">Le module Génération SQL du Fournisseur d'exemples (situé sous le dossier Génération SQL, à l'exception du fichier DmlSqlGenerator.cs) prend un DbQueryCommandTree d'entrée et produit une instruction SQL SELECT unique.</span><span class="sxs-lookup"><span data-stu-id="8bf5b-105">The SQL Generation module of the Sample Provider (located under the SQL Generation folder, except for the file DmlSqlGenerator.cs) takes an input DbQueryCommandTree and produces a single SQL SELECT statement.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="8bf5b-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8bf5b-106">In This Section</span></span>  
 <span data-ttu-id="8bf5b-107">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8bf5b-107">This section includes the following topics:</span></span>  
  
 [<span data-ttu-id="8bf5b-108">Architecture et conception</span><span class="sxs-lookup"><span data-stu-id="8bf5b-108">Architecture and Design</span></span>](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [<span data-ttu-id="8bf5b-109">Procédure pas à pas : génération SQL</span><span class="sxs-lookup"><span data-stu-id="8bf5b-109">Walkthrough: SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a><span data-ttu-id="8bf5b-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bf5b-110">See Also</span></span>  
 [<span data-ttu-id="8bf5b-111">Génération SQL</span><span class="sxs-lookup"><span data-stu-id="8bf5b-111">SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
