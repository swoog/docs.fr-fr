---
title: Oracle et ADO.NET
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8ee8e389-53cf-45cf-80bd-1df63ef34f2e
ms.openlocfilehash: 012a5b55d052f5f06da5c152da79f4676b2bff4e
ms.sourcegitcommit: c4e9d05644c9cb89de5ce6002723de107ea2e2c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2019
ms.locfileid: "65877945"
---
# <a name="oracle-and-adonet"></a><span data-ttu-id="1ee73-102">Oracle et ADO.NET</span><span class="sxs-lookup"><span data-stu-id="1ee73-102">Oracle and ADO.NET</span></span>
> [!NOTE]
>  <span data-ttu-id="1ee73-103">Les types dans <xref:System.Data.OracleClient> sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="1ee73-103">The types in <xref:System.Data.OracleClient> are deprecated.</span></span> <span data-ttu-id="1ee73-104">Les types restent pris en charge dans la version actuelle du .NET Framework, mais seront supprimés dans une mise en production ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1ee73-104">The types remain supported in the current version of.NET Framework but will be removed in a future release.</span></span> <span data-ttu-id="1ee73-105">Microsoft recommande l'utilisation d'un fournisseur Oracle tiers.</span><span class="sxs-lookup"><span data-stu-id="1ee73-105">Microsoft recommends that you use a third-party Oracle provider.</span></span>  
  
 <span data-ttu-id="1ee73-106">Cette section décrit les fonctionnalités et comportements qui sont spécifiques au fournisseur de données .NET Framework pour Oracle.</span><span class="sxs-lookup"><span data-stu-id="1ee73-106">This section describes features and behaviors that are specific to the .NET Framework Data Provider for Oracle.</span></span>  
  
 <span data-ttu-id="1ee73-107">Le fournisseur de données .NET Framework pour Oracle permet d’accéder à une base de données Oracle à l’aide de l’Interface OCI (Oracle Call) tel que fourni par le logiciel Client Oracle.</span><span class="sxs-lookup"><span data-stu-id="1ee73-107">The .NET Framework Data Provider for Oracle provides access to an Oracle database using the Oracle Call Interface (OCI) as provided by Oracle Client software.</span></span> <span data-ttu-id="1ee73-108">La fonctionnalité du fournisseur de données est conçue pour être similaire à celle des fournisseurs de données .NET Framework pour SQL Server, OLE DB et ODBC.</span><span class="sxs-lookup"><span data-stu-id="1ee73-108">The functionality of the data provider is designed to be similar to that of the .NET Framework data providers for SQL Server, OLE DB, and ODBC.</span></span>  
  
 <span data-ttu-id="1ee73-109">Pour utiliser le fournisseur de données .NET Framework pour Oracle, une application doit référencer le <xref:System.Data.OracleClient> espace de noms comme suit :</span><span class="sxs-lookup"><span data-stu-id="1ee73-109">To use the .NET Framework Data Provider for Oracle, an application must reference the <xref:System.Data.OracleClient> namespace as follows:</span></span>  
  
```vb  
Imports System.Data.OracleClient  
```  
  
```csharp  
using System.Data.OracleClient;  
```  
  
 <span data-ttu-id="1ee73-110">Vous devez également inclure une référence à la DLL lorsque vous compilez votre code.</span><span class="sxs-lookup"><span data-stu-id="1ee73-110">You also must include a reference to the DLL when you compile your code.</span></span> <span data-ttu-id="1ee73-111">Par exemple, si vous compilez un programme C#, votre ligne de commande doit inclure :</span><span class="sxs-lookup"><span data-stu-id="1ee73-111">For example, if you are compiling a C# program, your command line should include:</span></span>  
  
```  
csc /r:System.Data.OracleClient.dll  
```  
  
## <a name="in-this-section"></a><span data-ttu-id="1ee73-112">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="1ee73-112">In This Section</span></span>  
 [<span data-ttu-id="1ee73-113">Configuration système requise</span><span class="sxs-lookup"><span data-stu-id="1ee73-113">System Requirements</span></span>](../../../../docs/framework/data/adonet/system-requirements-for-the-dotnet-data-provider-for-oracle.md)  
 <span data-ttu-id="1ee73-114">Décrit la configuration requise pour utiliser le fournisseur de données .NET Framework pour Oracle et décrit un certain nombre de problèmes à connaître lors de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="1ee73-114">Describes requirements for using the .NET Framework Data Provider for Oracle, and describes a number of issues to be aware when using it.</span></span>  
  
 [<span data-ttu-id="1ee73-115">BFILE Oracle</span><span class="sxs-lookup"><span data-stu-id="1ee73-115">Oracle BFILEs</span></span>](../../../../docs/framework/data/adonet/oracle-bfiles.md)  
 <span data-ttu-id="1ee73-116">Décrit la classe <xref:System.Data.OracleClient.OracleBFile> qui est utilisée pour travailler avec le type de données Oracle BFILE.</span><span class="sxs-lookup"><span data-stu-id="1ee73-116">Describes the <xref:System.Data.OracleClient.OracleBFile> class, which is used to work with the Oracle BFILE data type.</span></span>  
  
 [<span data-ttu-id="1ee73-117">LOB Oracle</span><span class="sxs-lookup"><span data-stu-id="1ee73-117">Oracle LOBs</span></span>](../../../../docs/framework/data/adonet/oracle-lobs.md)  
 <span data-ttu-id="1ee73-118">Décrit la classe <xref:System.Data.OracleClient.OracleLob> qui est utilisée pour travailler avec les types de données Oracle LOB.</span><span class="sxs-lookup"><span data-stu-id="1ee73-118">Describes the <xref:System.Data.OracleClient.OracleLob> class, which is used to work with Oracle LOB data types.</span></span>  
  
 [<span data-ttu-id="1ee73-119">REF CURSOR Oracle</span><span class="sxs-lookup"><span data-stu-id="1ee73-119">Oracle REF CURSORs</span></span>](../../../../docs/framework/data/adonet/oracle-ref-cursors.md)  
 <span data-ttu-id="1ee73-120">Décrit la prise en charge pour le type de données Oracle REF CURSOR.</span><span class="sxs-lookup"><span data-stu-id="1ee73-120">Describes support for the Oracle REF CURSOR data type.</span></span>  
  
 [<span data-ttu-id="1ee73-121">OracleTypes</span><span class="sxs-lookup"><span data-stu-id="1ee73-121">OracleTypes</span></span>](../../../../docs/framework/data/adonet/oracletypes.md)  
 <span data-ttu-id="1ee73-122">Décrit les structures que vous pouvez utiliser pour travailler avec des types de données Oracle, notamment <xref:System.Data.OracleClient.OracleNumber> et <xref:System.Data.OracleClient.OracleString>.</span><span class="sxs-lookup"><span data-stu-id="1ee73-122">Describes structures you can use to work with Oracle data types, including <xref:System.Data.OracleClient.OracleNumber> and <xref:System.Data.OracleClient.OracleString>.</span></span>  
  
 [<span data-ttu-id="1ee73-123">Séquences Oracle</span><span class="sxs-lookup"><span data-stu-id="1ee73-123">Oracle Sequences</span></span>](../../../../docs/framework/data/adonet/oracle-sequences.md)  
 <span data-ttu-id="1ee73-124">Décrit la prise en charge de l'extraction des valeurs de séquence Oracle générées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="1ee73-124">Describes support for retrieving the server-generated key Oracle Sequence values.</span></span>  
  
 [<span data-ttu-id="1ee73-125">Mappages de types de données Oracle</span><span class="sxs-lookup"><span data-stu-id="1ee73-125">Oracle Data Type Mappings</span></span>](../../../../docs/framework/data/adonet/oracle-data-type-mappings.md)  
 <span data-ttu-id="1ee73-126">Répertorie les types de données Oracle et leurs mappages sur le <xref:System.Data.OracleClient.OracleDataReader>.</span><span class="sxs-lookup"><span data-stu-id="1ee73-126">Lists Oracle data types and their mappings to the <xref:System.Data.OracleClient.OracleDataReader>.</span></span>  
  
 [<span data-ttu-id="1ee73-127">Transactions distribuées Oracle</span><span class="sxs-lookup"><span data-stu-id="1ee73-127">Oracle Distributed Transactions</span></span>](../../../../docs/framework/data/adonet/oracle-distributed-transactions.md)  
 <span data-ttu-id="1ee73-128">Décrit la manière dont l’objet <xref:System.Data.OracleClient.OracleConnection> s’inscrit automatiquement dans une transaction distribuée existante s’il détermine qu’une transaction est active.</span><span class="sxs-lookup"><span data-stu-id="1ee73-128">Describes how the <xref:System.Data.OracleClient.OracleConnection> object automatically enlists in an existing distributed transaction if it determines that a transaction is active.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="1ee73-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ee73-129">Related Sections</span></span>  
 [<span data-ttu-id="1ee73-130">Sécurisation des applications ADO.NET</span><span class="sxs-lookup"><span data-stu-id="1ee73-130">Securing ADO.NET Applications</span></span>](../../../../docs/framework/data/adonet/securing-ado-net-applications.md)  
 <span data-ttu-id="1ee73-131">Décrit des pratiques de codage sécurisées dans ADO.NET.</span><span class="sxs-lookup"><span data-stu-id="1ee73-131">Describes secure coding practices when using ADO.NET.</span></span>  
  
 [<span data-ttu-id="1ee73-132">DataSets, DataTables et DataViews</span><span class="sxs-lookup"><span data-stu-id="1ee73-132">DataSets, DataTables, and DataViews</span></span>](../../../../docs/framework/data/adonet/dataset-datatable-dataview/index.md)  
 <span data-ttu-id="1ee73-133">Explique comment créer et utiliser des `DataSets`, des `DataSets` typés, des `DataTables` et des `DataViews`.</span><span class="sxs-lookup"><span data-stu-id="1ee73-133">Describes how to create and use `DataSets`, typed `DataSets`, `DataTables`, and `DataViews`.</span></span>  
  
 [<span data-ttu-id="1ee73-134">Extraction et modification de données dans ADO.NET</span><span class="sxs-lookup"><span data-stu-id="1ee73-134">Retrieving and Modifying Data in ADO.NET</span></span>](../../../../docs/framework/data/adonet/retrieving-and-modifying-data.md)  
 <span data-ttu-id="1ee73-135">Décrit comment utiliser des données dans ADO.NET.</span><span class="sxs-lookup"><span data-stu-id="1ee73-135">Describes how to work with data in ADO.NET.</span></span>  
  
 [<span data-ttu-id="1ee73-136">SQL Server et ADO.NET</span><span class="sxs-lookup"><span data-stu-id="1ee73-136">SQL Server and ADO.NET</span></span>](../../../../docs/framework/data/adonet/sql/index.md)  
 <span data-ttu-id="1ee73-137">Décrit comment utiliser des fonctions et fonctionnalités spécifiques à SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1ee73-137">Describes how to work with features and functionality that are specific to SQL Server.</span></span>  
  
 [<span data-ttu-id="1ee73-138">DbProviderFactories</span><span class="sxs-lookup"><span data-stu-id="1ee73-138">DbProviderFactories</span></span>](../../../../docs/framework/data/adonet/dbproviderfactories.md)  
 <span data-ttu-id="1ee73-139">Décrit des classes génériques qui vous permettent d'écrire du code indépendant du fournisseur dans ADO.NET.</span><span class="sxs-lookup"><span data-stu-id="1ee73-139">Describes generic classes that allow you to write provider-independent code in ADO.NET.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ee73-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ee73-140">See also</span></span>

- [<span data-ttu-id="1ee73-141">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="1ee73-141">ADO.NET</span></span>](../../../../docs/framework/data/adonet/index.md)
- [<span data-ttu-id="1ee73-142">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="1ee73-142">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
