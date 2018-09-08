---
title: Données binaires et à valeurs élevées SQL Server
ms.date: 03/30/2017
ms.assetid: e00827b3-7511-4b2d-91d7-851ca86cc6b5
ms.openlocfilehash: 9ebbe23dfbcac7825ce449dd40f62b921d13ab4a
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44209158"
---
# <a name="sql-server-binary-and-large-value-data"></a><span data-ttu-id="f95c9-102">Données binaires et à valeurs élevées SQL Server</span><span class="sxs-lookup"><span data-stu-id="f95c9-102">SQL Server Binary and Large-Value Data</span></span>
<span data-ttu-id="f95c9-103">SQL Server fournit le spécificateur `max`, qui étend la capacité de stockage des types de données `varchar`, `nvarchar` et `varbinary`.</span><span class="sxs-lookup"><span data-stu-id="f95c9-103">SQL Server provides the `max` specifier, which expands the storage capacity of the `varchar`, `nvarchar`, and `varbinary` data types.</span></span> <span data-ttu-id="f95c9-104">`varchar(max)`, `nvarchar(max)`, et `varbinary(max)` sont appelés collectivement *les types de données de grande valeur*.</span><span class="sxs-lookup"><span data-stu-id="f95c9-104">`varchar(max)`, `nvarchar(max)`, and `varbinary(max)` are collectively called *large-value data types*.</span></span> <span data-ttu-id="f95c9-105">Les types de données de valeur élevée permettent de stocker jusqu'à 2^31-1 octets de données.</span><span class="sxs-lookup"><span data-stu-id="f95c9-105">You can use the large-value data types to store up to 2^31-1 bytes of data.</span></span>  
  
 <span data-ttu-id="f95c9-106">SQL Server 2008 introduit l'attribut FILESTREAM, qui n'est pas un type de données, mais plutôt un attribut pouvant être défini sur une colonne et permettant alors de stocker des données de valeur élevée dans le système de fichiers et non dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="f95c9-106">SQL Server 2008 introduces the FILESTREAM attribute, which is not a data type, but rather an attribute that can be defined on a column, allowing large-value data to be stored on the file system instead of in the database.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f95c9-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f95c9-107">In This Section</span></span>  
 [<span data-ttu-id="f95c9-108">Modification de données de valeurs élevées (max) dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="f95c9-108">Modifying Large-Value (max) Data in ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/modifying-large-value-max-data.md)  
 <span data-ttu-id="f95c9-109">Décrit comment utiliser les types de données de valeur volumineux.</span><span class="sxs-lookup"><span data-stu-id="f95c9-109">Describes how to work with the large-value data types.</span></span>  
  
 [<span data-ttu-id="f95c9-110">Données FILESTREAM</span><span class="sxs-lookup"><span data-stu-id="f95c9-110">FILESTREAM Data</span></span>](../../../../../docs/framework/data/adonet/sql/filestream-data.md)  
 <span data-ttu-id="f95c9-111">Décrit comment utiliser les données de valeur élevée stockées dans SQL Server 2008 avec l'attribut FILESTREAM.</span><span class="sxs-lookup"><span data-stu-id="f95c9-111">Describes how to work with large-value data stored in SQL Server 2008 with the FILESTREAM attribute.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f95c9-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f95c9-112">See Also</span></span>  
 [<span data-ttu-id="f95c9-113">Types de données SQL Server et ADO.NET</span><span class="sxs-lookup"><span data-stu-id="f95c9-113">SQL Server Data Types and ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/sql-server-data-types.md)  
 [<span data-ttu-id="f95c9-114">Opérations sur les données SQL Server dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="f95c9-114">SQL Server Data Operations in ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/sql-server-data-operations.md)  
 [<span data-ttu-id="f95c9-115">Extraction et modification de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="f95c9-115">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 [<span data-ttu-id="f95c9-116">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="f95c9-116">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
