---
title: DbProviderFactories
ms.date: 03/30/2017
ms.assetid: 2a8e2640-3a49-42a1-a3a9-b43026907ae1
ms.openlocfilehash: 255ef115e6851b5f1d93744b54ec88990746d9cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54543538"
---
# <a name="dbproviderfactories"></a><span data-ttu-id="fcafc-102">DbProviderFactories</span><span class="sxs-lookup"><span data-stu-id="fcafc-102">DbProviderFactories</span></span>
<span data-ttu-id="fcafc-103">L'espace de noms <xref:System.Data.Common> fournit des classes permettant de créer des instances <xref:System.Data.Common.DbProviderFactory> afin d'utiliser des sources de données spécifiques.</span><span class="sxs-lookup"><span data-stu-id="fcafc-103">The <xref:System.Data.Common> namespace provides classes for creating <xref:System.Data.Common.DbProviderFactory> instances to work with specific data sources.</span></span> <span data-ttu-id="fcafc-104">Lorsque vous créez une instance <xref:System.Data.Common.DbProviderFactory> et que vous lui passez des informations sur le fournisseur de données, `DbProviderFactory` peut déterminer l'objet de connexion fortement typé correct à retourner en fonction des informations qui lui ont été fournies.</span><span class="sxs-lookup"><span data-stu-id="fcafc-104">When you create a <xref:System.Data.Common.DbProviderFactory> instance and pass it information about the data provider, the `DbProviderFactory` can determine the correct, strongly typed connection object to return based on the information it has been provided.</span></span>  
  
 <span data-ttu-id="fcafc-105">Depuis .NET Framework version 4, les fournisseurs de données tels que <xref:System.Data.Odbc>, <xref:System.Data.OleDb>, <xref:System.Data.SqlClient> et <xref:System.Data.OracleClient> ne sont plus répertoriés dans le fichier machine.config, contrairement aux fournisseurs personnalisés qui continueront à y figurer.</span><span class="sxs-lookup"><span data-stu-id="fcafc-105">Beginning in the .NET Framework version 4, data providers such as <xref:System.Data.Odbc>, <xref:System.Data.OleDb>, <xref:System.Data.SqlClient>, and <xref:System.Data.OracleClient> are no longer listed in machine.config file, but custom providers will continue to be listed there.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fcafc-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="fcafc-106">In This Section</span></span>  
 [<span data-ttu-id="fcafc-107">Vue d’ensemble du modèle Factory</span><span class="sxs-lookup"><span data-stu-id="fcafc-107">Factory Model Overview</span></span>](../../../../docs/framework/data/adonet/factory-model-overview.md)  
 <span data-ttu-id="fcafc-108">Fournit une vue d’ensemble du modèle de design factory et de l’interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="fcafc-108">Provides an overview of the factory design pattern and programming interface.</span></span>  
  
 [<span data-ttu-id="fcafc-109">Obtention d’un DbProviderFactory</span><span class="sxs-lookup"><span data-stu-id="fcafc-109">Obtaining a DbProviderFactory</span></span>](../../../../docs/framework/data/adonet/obtaining-a-dbproviderfactory.md)  
 <span data-ttu-id="fcafc-110">Montre comment répertorier les fournisseurs de données installés et créer <xref:System.Data.Common.DbConnection> à partir de `DbProviderFactory`.</span><span class="sxs-lookup"><span data-stu-id="fcafc-110">Demonstrates how to list the installed data providers and create a <xref:System.Data.Common.DbConnection> from a `DbProviderFactory`.</span></span>  
  
 [<span data-ttu-id="fcafc-111">DbConnection, DbCommand et DbException</span><span class="sxs-lookup"><span data-stu-id="fcafc-111">DbConnection, DbCommand and DbException</span></span>](../../../../docs/framework/data/adonet/dbconnection-dbcommand-and-dbexception.md)  
 <span data-ttu-id="fcafc-112">Montre comment créer <xref:System.Data.Common.DbCommand> et <xref:System.Data.Common.DbDataReader> et comment gérer des erreurs de données à l'aide de <xref:System.Data.Common.DbException>.</span><span class="sxs-lookup"><span data-stu-id="fcafc-112">Demonstrates how to create a <xref:System.Data.Common.DbCommand> and <xref:System.Data.Common.DbDataReader>, and how to handle data errors using <xref:System.Data.Common.DbException>.</span></span>  
  
 [<span data-ttu-id="fcafc-113">Modification des données avec un DbDataAdapter</span><span class="sxs-lookup"><span data-stu-id="fcafc-113">Modifying Data with a DbDataAdapter</span></span>](../../../../docs/framework/data/adonet/modifying-data-with-a-dbdataadapter.md)  
 <span data-ttu-id="fcafc-114">Montre comment utiliser <xref:System.Data.Common.DbCommandBuilder> avec <xref:System.Data.Common.DbDataAdapter> pour récupérer et modifier des données.</span><span class="sxs-lookup"><span data-stu-id="fcafc-114">Demonstrates how to use a <xref:System.Data.Common.DbCommandBuilder> with a <xref:System.Data.Common.DbDataAdapter> to retrieve and modify data.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcafc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fcafc-115">See also</span></span>
- [<span data-ttu-id="fcafc-116">Extraction et modification de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="fcafc-116">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)
- [<span data-ttu-id="fcafc-117">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="fcafc-117">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
