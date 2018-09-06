---
title: Génération SQL dans le Fournisseur d'exemples
ms.date: 03/30/2017
ms.assetid: e70f553d-4622-4627-928e-1aa2ee605d8e
ms.openlocfilehash: cba1cec6d7ef0fdf8d4d4cf6c8e44fb325cf6447
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44041296"
---
# <a name="sql-generation-in-the-sample-provider"></a><span data-ttu-id="b88f4-102">Génération SQL dans le Fournisseur d'exemples</span><span class="sxs-lookup"><span data-stu-id="b88f4-102">SQL Generation in the Sample Provider</span></span>
<span data-ttu-id="b88f4-103">Le [Entity Framework Sample Provider](https://go.microsoft.com/fwlink/?LinkId=180616) montre les nouveaux composants des fournisseurs de données ADO.NET qui prennent en charge la [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b88f4-103">The [Entity Framework Sample Provider](https://go.microsoft.com/fwlink/?LinkId=180616) demonstrates the new components of ADO.NET Data Providers that support the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span>  <span data-ttu-id="b88f4-104">Il utilise une base de données SQL Server 2005 et est implémenté comme un wrapper pour le fournisseur de données System.Data.SqlClient ADO.NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="b88f4-104">It works with a SQL Server 2005 database and is implemented as a wrapper for the System.Data.SqlClient ADO.NET 2.0 Data Provider.</span></span>  
  
 <span data-ttu-id="b88f4-105">Le module Génération SQL du Fournisseur d'exemples (situé sous le dossier Génération SQL, à l'exception du fichier DmlSqlGenerator.cs) prend un DbQueryCommandTree d'entrée et produit une instruction SQL SELECT unique.</span><span class="sxs-lookup"><span data-stu-id="b88f4-105">The SQL Generation module of the Sample Provider (located under the SQL Generation folder, except for the file DmlSqlGenerator.cs) takes an input DbQueryCommandTree and produces a single SQL SELECT statement.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b88f4-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b88f4-106">In This Section</span></span>  
 <span data-ttu-id="b88f4-107">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b88f4-107">This section includes the following topics:</span></span>  
  
 [<span data-ttu-id="b88f4-108">Architecture et conception</span><span class="sxs-lookup"><span data-stu-id="b88f4-108">Architecture and Design</span></span>](../../../../../docs/framework/data/adonet/ef/architecture-and-design.md)  
  
 [<span data-ttu-id="b88f4-109">Procédure pas à pas : génération SQL</span><span class="sxs-lookup"><span data-stu-id="b88f4-109">Walkthrough: SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/walkthrough-sql-generation.md)  
  
## <a name="see-also"></a><span data-ttu-id="b88f4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b88f4-110">See Also</span></span>  
 [<span data-ttu-id="b88f4-111">Génération SQL</span><span class="sxs-lookup"><span data-stu-id="b88f4-111">SQL Generation</span></span>](../../../../../docs/framework/data/adonet/ef/sql-generation.md)
