---
title: Intégration CLR SQL Server
ms.date: 03/30/2017
ms.assetid: c7a324c4-160d-44c2-b593-641af06eca61
ms.openlocfilehash: 5f6c1dcccaddeadb65e6fc949960b0232d00ed81
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2018
ms.locfileid: "45646072"
---
# <a name="sql-server-common-language-runtime-integration"></a><span data-ttu-id="e9507-102">Intégration CLR SQL Server</span><span class="sxs-lookup"><span data-stu-id="e9507-102">SQL Server Common Language Runtime Integration</span></span>
<span data-ttu-id="e9507-103">SQL Server 2005 a introduit l'intégration du composant Common Language Runtime (CLR) de .NET Framework pour Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e9507-103">SQL Server 2005 introduced the integration of the common language runtime (CLR) component of the .NET Framework for Microsoft Windows.</span></span> <span data-ttu-id="e9507-104">Cela signifie que vous pouvez écrire des procédures stockées, des déclencheurs, des types définis par l'utilisateur, des fonctions définies par l'utilisateur, des agrégats définis par l'utilisateur et des fonctions de flux évaluées par une table, en utilisant tout langage .NET Framework, notamment Microsoft Visual Basic .NET et Microsoft Visual C#.</span><span class="sxs-lookup"><span data-stu-id="e9507-104">This means that you can write stored procedures, triggers, user-defined types, user-defined functions, user-defined aggregates, and streaming table-valued functions, using any .NET Framework language, including Microsoft Visual Basic .NET and Microsoft Visual C#.</span></span> <span data-ttu-id="e9507-105">L'espace de noms <xref:Microsoft.SqlServer.Server> contient un ensemble de nouvelles API permettant au code managé d'interagir avec l'environnement Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9507-105">The <xref:Microsoft.SqlServer.Server> namespace contains a set of new application programming interfaces (APIs) so that managed code can interact with the Microsoft SQL Server environment.</span></span>  
  
 <span data-ttu-id="e9507-106">Cette section décrit les fonctions et les comportements spécifiques à l'intégration de CLR dans SQL Server et aux extensions spécifiques au mode in-process SQL Server pour ADO.NET.</span><span class="sxs-lookup"><span data-stu-id="e9507-106">This section describes features and behaviors that are specific to SQL Server common language runtime (CLR) integration and the SQL Server in-process specific extensions to ADO.NET.</span></span>  
  
 <span data-ttu-id="e9507-107">Cette section a uniquement pour but de fournir les informations indispensables pour commencer à programmer avec l'intégration de CLR dans SQL Server et n'est nullement exhaustive.</span><span class="sxs-lookup"><span data-stu-id="e9507-107">This section is meant to provide only enough information to get started programming with SQL Server CLR integration, and is not meant to be comprehensive.</span></span> <span data-ttu-id="e9507-108">Pour obtenir des informations plus détaillées, voir la documentation en ligne de SQL Server pour la version de SQL Server que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="e9507-108">For more detailed information, see the version of SQL Server Books Online for the version of SQL Server you are using.</span></span>  
  
 <span data-ttu-id="e9507-109">**Documentation en ligne de SQL Server**</span><span class="sxs-lookup"><span data-stu-id="e9507-109">**SQL Server Books Online**</span></span>  
  
1.  [<span data-ttu-id="e9507-110">Concepts de programmation intégration Common Language Runtime (CLR)</span><span class="sxs-lookup"><span data-stu-id="e9507-110">Common Language Runtime (CLR) Integration Programming Concepts</span></span>](https://go.microsoft.com/fwlink/?LinkId=115240)  
  
## <a name="in-this-section"></a><span data-ttu-id="e9507-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e9507-111">In This Section</span></span>  
 [<span data-ttu-id="e9507-112">Introduction à l’intégration CLR SQL Server</span><span class="sxs-lookup"><span data-stu-id="e9507-112">Introduction to SQL Server CLR Integration</span></span>](../../../../../docs/framework/data/adonet/sql/introduction-to-sql-server-clr-integration.md)  
 <span data-ttu-id="e9507-113">Fournit une présentation de l'intégration de CLR dans SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e9507-113">Provides an introduction to SQL Server CLR integration.</span></span> <span data-ttu-id="e9507-114">Fournit des liens vers d'autres rubriques.</span><span class="sxs-lookup"><span data-stu-id="e9507-114">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="e9507-115">Fonctions CLR définies par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e9507-115">CLR User-Defined Functions</span></span>](../../../../../docs/framework/data/adonet/sql/clr-user-defined-functions.md)  
 <span data-ttu-id="e9507-116">Décrit comment implémenter et utiliser les différents types de fonctions CLR : fonctions table, fonctions scalaires et fonctions d'agrégation définies par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9507-116">Describes how to implement and use the various types of CLR functions: table-valued, scalar, and user-defined aggregate functions.</span></span>  
  
 [<span data-ttu-id="e9507-117">Types CLR définis par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e9507-117">CLR User-Defined Types</span></span>](../../../../../docs/framework/data/adonet/sql/clr-user-defined-types.md)  
 <span data-ttu-id="e9507-118">Décrit comment implémenter et utiliser des types CLR définis par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9507-118">Describes how to implement and use CLR user-defined types.</span></span> <span data-ttu-id="e9507-119">Fournit des liens vers d'autres rubriques.</span><span class="sxs-lookup"><span data-stu-id="e9507-119">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="e9507-120">Procédures stockées CLR</span><span class="sxs-lookup"><span data-stu-id="e9507-120">CLR Stored Procedures</span></span>](../../../../../docs/framework/data/adonet/sql/clr-stored-procedures.md)  
 <span data-ttu-id="e9507-121">Décrit comment implémenter et utiliser des procédures stockées CLR.</span><span class="sxs-lookup"><span data-stu-id="e9507-121">Describes how to implement and use CLR stored procedures.</span></span> <span data-ttu-id="e9507-122">Fournit des liens vers d'autres rubriques.</span><span class="sxs-lookup"><span data-stu-id="e9507-122">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="e9507-123">Déclencheurs CLR</span><span class="sxs-lookup"><span data-stu-id="e9507-123">CLR Triggers</span></span>](../../../../../docs/framework/data/adonet/sql/clr-triggers.md)  
 <span data-ttu-id="e9507-124">Décrit comment implémenter et utiliser des déclencheurs CLR.</span><span class="sxs-lookup"><span data-stu-id="e9507-124">Describes how to implement and use CLR triggers.</span></span> <span data-ttu-id="e9507-125">Fournit des liens vers d'autres rubriques.</span><span class="sxs-lookup"><span data-stu-id="e9507-125">Provides links to additional topics.</span></span>  
  
 [<span data-ttu-id="e9507-126">Connexion de contexte</span><span class="sxs-lookup"><span data-stu-id="e9507-126">The Context Connection</span></span>](../../../../../docs/framework/data/adonet/sql/the-context-connection.md)  
 <span data-ttu-id="e9507-127">Décrit la connexion de contexte.</span><span class="sxs-lookup"><span data-stu-id="e9507-127">Describes the context connection.</span></span>  
  
 [<span data-ttu-id="e9507-128">Comportement SQL Server spécifique au processus d’ADO.NET</span><span class="sxs-lookup"><span data-stu-id="e9507-128">SQL Server In-Process-Specific Behavior of ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/sql-server-in-process-specific-behavior-of-adonet.md)  
 <span data-ttu-id="e9507-129">Décrit les extensions spécifiques au mode in-process SQL Server pour ADO.NET et la connexion de contexte.</span><span class="sxs-lookup"><span data-stu-id="e9507-129">Describes the SQL Server in-process specific extensions to ADO.NET, and the context connection.</span></span> <span data-ttu-id="e9507-130">Fournit des liens vers d'autres rubriques.</span><span class="sxs-lookup"><span data-stu-id="e9507-130">Provides links to additional topics.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9507-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9507-131">See Also</span></span>  
 [<span data-ttu-id="e9507-132">SQL Server et ADO.NET</span><span class="sxs-lookup"><span data-stu-id="e9507-132">SQL Server and ADO.NET</span></span>](../../../../../docs/framework/data/adonet/sql/index.md)  
 [<span data-ttu-id="e9507-133">Création d’objets SQL Server 2005 dans le Code managé</span><span class="sxs-lookup"><span data-stu-id="e9507-133">Creating SQL Server 2005 Objects In Managed Code</span></span>](https://msdn.microsoft.com/library/5358a825-e19b-49aa-8214-674ce5fed1da)  
 [<span data-ttu-id="e9507-134">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="e9507-134">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
