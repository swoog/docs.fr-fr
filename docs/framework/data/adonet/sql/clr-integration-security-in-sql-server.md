---
title: Sécurité de l'intégration du CLR dans SQL Server
ms.date: 03/30/2017
ms.assetid: 489fe096-fd1d-42de-8438-bf7aed46aea2
ms.openlocfilehash: 946401211d515df9ba5b9e38d7cfd10730973b64
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61878486"
---
# <a name="clr-integration-security-in-sql-server"></a><span data-ttu-id="d07f7-102">Sécurité de l'intégration du CLR dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="d07f7-102">CLR Integration Security in SQL Server</span></span>
<span data-ttu-id="d07f7-103">Microsoft SQL Server introduit le composant Common Language Runtime (CLR) du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d07f7-103">Microsoft SQL Server provides the integration of the common language runtime (CLR) component of the .NET Framework.</span></span> <span data-ttu-id="d07f7-104">L'intégration du CLR vous permet d'écrire des procédures stockées, des déclencheurs, des types définis par l'utilisateur, des fonctions définies par l'utilisateur, des agrégats définis par l'utilisateur et des fonctions de flux évaluées par une table, en utilisant tout langage .NET Framework, tel que Microsoft Visual Basic .NET ou Microsoft Visual C#.</span><span class="sxs-lookup"><span data-stu-id="d07f7-104">CLR integration allows you to write stored procedures, triggers, user-defined types, user-defined functions, user-defined aggregates, and streaming table-valued functions, using any .NET Framework language, such as Microsoft Visual Basic .NET or Microsoft Visual C#.</span></span>  
  
 <span data-ttu-id="d07f7-105">Le CLR prend en charge un modèle de sécurité appelé sécurité d'accès du code (CAS) pour le code managé.</span><span class="sxs-lookup"><span data-stu-id="d07f7-105">The CLR supports a security model called code access security (CAS) for managed code.</span></span> <span data-ttu-id="d07f7-106">Dans ce modèle, les autorisations sont accordées aux assemblys en fonction de la preuve fournie par le code dans les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d07f7-106">In this model, permissions are granted to assemblies based on evidence supplied by the code in metadata.</span></span> <span data-ttu-id="d07f7-107">SQL Server intègre le modèle de sécurité de SQL Server, basé sur l'utilisateur avec le modèle de sécurité du CLR, basé sur l'accès du code.</span><span class="sxs-lookup"><span data-stu-id="d07f7-107">SQL Server integrates the user-based security model of SQL Server with the code access-based security model of the CLR.</span></span>  
  
## <a name="external-resources"></a><span data-ttu-id="d07f7-108">Ressources externes</span><span class="sxs-lookup"><span data-stu-id="d07f7-108">External Resources</span></span>  
 <span data-ttu-id="d07f7-109">Pour plus d'informations sur l'intégration du CLR avec SQL Server, voir les ressources répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d07f7-109">For more information on CLR integration with SQL Server, see the following resources.</span></span>  
  
|<span data-ttu-id="d07f7-110">Ressource</span><span class="sxs-lookup"><span data-stu-id="d07f7-110">Resource</span></span>|<span data-ttu-id="d07f7-111">Description</span><span class="sxs-lookup"><span data-stu-id="d07f7-111">Description</span></span>|  
|--------------|-----------------|  
|[<span data-ttu-id="d07f7-112">Sécurité d’accès du code</span><span class="sxs-lookup"><span data-stu-id="d07f7-112">Code Access Security</span></span>](../../../../../docs/framework/misc/code-access-security.md)|<span data-ttu-id="d07f7-113">Contient des rubriques qui décrivent la sécurité d'accès du code dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d07f7-113">Contains topics describing CAS in the .NET Framework.</span></span>|  
|[<span data-ttu-id="d07f7-114">Sécurité d’intégration du CLR</span><span class="sxs-lookup"><span data-stu-id="d07f7-114">CLR Integration Security</span></span>](/sql/relational-databases/clr-integration/security/clr-integration-security)|<span data-ttu-id="d07f7-115">Présente le modèle de sécurité pour le code managé qui s'exécute au sein de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d07f7-115">Discusses the security model for managed code executing inside of SQL Server.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d07f7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d07f7-116">See also</span></span>

- [<span data-ttu-id="d07f7-117">Sécurisation des applications ADO.NET</span><span class="sxs-lookup"><span data-stu-id="d07f7-117">Securing ADO.NET Applications</span></span>](../../../../../docs/framework/data/adonet/securing-ado-net-applications.md)
- [<span data-ttu-id="d07f7-118">Scénarios de sécurité des applications dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="d07f7-118">Application Security Scenarios in SQL Server</span></span>](../../../../../docs/framework/data/adonet/sql/application-security-scenarios-in-sql-server.md)
- [<span data-ttu-id="d07f7-119">Intégration CLR SQL Server</span><span class="sxs-lookup"><span data-stu-id="d07f7-119">SQL Server Common Language Runtime Integration</span></span>](../../../../../docs/framework/data/adonet/sql/sql-server-common-language-runtime-integration.md)
- [<span data-ttu-id="d07f7-120">Vue d’ensemble d’ADO.NET</span><span class="sxs-lookup"><span data-stu-id="d07f7-120">ADO.NET Overview</span></span>](../../../../../docs/framework/data/adonet/ado-net-overview.md)
