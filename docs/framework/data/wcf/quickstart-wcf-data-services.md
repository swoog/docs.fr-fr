---
title: Démarrage rapide (services de données WCF)
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, quick-start example
- WCF Data Services, Entity Data Model (EDM) service
ms.assetid: 7b18ca1e-d4d6-4c7a-afb9-ce3cebb98a8d
ms.openlocfilehash: 1a30f7e65efc65bf47abd61e5bfdfa85b58ae3a2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33365395"
---
# <a name="quickstart-wcf-data-services"></a><span data-ttu-id="01a7e-102">Démarrage rapide (services de données WCF)</span><span class="sxs-lookup"><span data-stu-id="01a7e-102">Quickstart (WCF Data Services)</span></span>
<span data-ttu-id="01a7e-103">Ce démarrage rapide vous aide à vous familiariser avec [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] et [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] via une série de tâches qui prennent en charge les rubriques de [mise en route](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="01a7e-103">This quickstart helps you become familiar with [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] and the [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] through a series of tasks that support the topics in [Getting Started](../../../../docs/framework/data/wcf/getting-started-with-wcf-data-services.md).</span></span>  
  
## <a name="what-you-will-learn"></a><span data-ttu-id="01a7e-104">Contenu du didacticiel</span><span class="sxs-lookup"><span data-stu-id="01a7e-104">What You Will Learn</span></span>  
 <span data-ttu-id="01a7e-105">La première tâche dans ce démarrage rapide montre comment créer un service de données pour exposer un flux [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] issu de l'exemple de base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="01a7e-105">The first task in this quickstart shows how to create a data service to expose an [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] feed from the Northwind sample database.</span></span> <span data-ttu-id="01a7e-106">Dans les rubriques ultérieures, vous accéderez au flux [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] à l'aide d'un navigateur Web et vous créerez également une application cliente Windows Presentation Foundation (WPF) qui consomme le flux [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] à l'aide de bibliothèques clientes.</span><span class="sxs-lookup"><span data-stu-id="01a7e-106">In later topics, you will access the [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] feed by using a Web browser, and also create a Windows Presentation Foundation (WPF) client application that consumes the [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] feed by using client libraries.</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="01a7e-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="01a7e-107">Prerequisites</span></span>  
 <span data-ttu-id="01a7e-108">Pour effectuer ce démarrage rapide, vous devez installer les composants suivants :</span><span class="sxs-lookup"><span data-stu-id="01a7e-108">To complete this quickstart, you must install the following components:</span></span>  
  
-   [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)]<span data-ttu-id="01a7e-109">.</span><span class="sxs-lookup"><span data-stu-id="01a7e-109">.</span></span>  
  
-   <span data-ttu-id="01a7e-110">Une instance de [!INCLUDE[msCoName](../../../../includes/msconame-md.md)] SQL Server.</span><span class="sxs-lookup"><span data-stu-id="01a7e-110">An instance of [!INCLUDE[msCoName](../../../../includes/msconame-md.md)] SQL Server.</span></span> <span data-ttu-id="01a7e-111">Cela inclut SQL Server Express, qui est inclus dans une installation par défaut de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="01a7e-111">This includes SQL Server Express, which is included in a default installation of Visual Studio.</span></span>  
  
-   <span data-ttu-id="01a7e-112">Exemple de base de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="01a7e-112">The Northwind sample database.</span></span> <span data-ttu-id="01a7e-113">Pour télécharger cet exemple de base de données, consultez la page de téléchargement, [Exemples de bases de données pour SQL Server](http://go.microsoft.com/fwlink/?linkid=24758).</span><span class="sxs-lookup"><span data-stu-id="01a7e-113">To download this sample database, see the download page, [Sample Databases for SQL Server](http://go.microsoft.com/fwlink/?linkid=24758).</span></span>  
  
## <a name="wcf-data-services-quickstart-tasks"></a><span data-ttu-id="01a7e-114">Tâches de démarrage rapide WCF Data Services</span><span class="sxs-lookup"><span data-stu-id="01a7e-114">WCF Data Services Quickstart Tasks</span></span>  
 [<span data-ttu-id="01a7e-115">Création du service de données</span><span class="sxs-lookup"><span data-stu-id="01a7e-115">Creating the Data Service</span></span>](../../../../docs/framework/data/wcf/creating-the-data-service.md)  
 <span data-ttu-id="01a7e-116">Définir l'application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] , définir le modèle de données, créer le service de données et autoriser l'accès aux ressources.</span><span class="sxs-lookup"><span data-stu-id="01a7e-116">Define the [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] application, define the data model, create the data service, and enable access to resources.</span></span>  
  
 [<span data-ttu-id="01a7e-117">Accès au service à partir d’un navigateur web</span><span class="sxs-lookup"><span data-stu-id="01a7e-117">Accessing the Service from a Web Browser</span></span>](../../../../docs/framework/data/wcf/accessing-the-service-from-a-web-browser-wcf-data-services-quickstart.md)  
 <span data-ttu-id="01a7e-118">Démarrer le service à partir de Visual Studio et accéder au service en soumettant des demandes HTTP GET via un navigateur Web au flux exposé.</span><span class="sxs-lookup"><span data-stu-id="01a7e-118">Start the service from Visual Studio and access the service by submitting HTTP GET requests through a Web browser to the exposed feed.</span></span>  
  
 [<span data-ttu-id="01a7e-119">Création de l’application cliente du .NET Framework</span><span class="sxs-lookup"><span data-stu-id="01a7e-119">Creating the .NET Framework Client Application</span></span>](../../../../docs/framework/data/wcf/creating-the-dotnet-client-application-wcf-data-services-quickstart.md)  
 <span data-ttu-id="01a7e-120">Créer une application cliente [!INCLUDE[avalon2](../../../../includes/avalon2-md.md)] pour consommer le flux [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] , lier des données aux contrôles Windows, modifier les données liées dans les contrôles dépendants, puis renvoyer les modifications au service de données.</span><span class="sxs-lookup"><span data-stu-id="01a7e-120">Create a [!INCLUDE[avalon2](../../../../includes/avalon2-md.md)] client application to consume the [!INCLUDE[ssODataShort](../../../../includes/ssodatashort-md.md)] feed, bind data to Windows controls, change data in the bound controls, and then send the changes back to the data service.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="01a7e-121">Les fichiers projet d’une version terminée du démarrage rapide peuvent être téléchargés à partir de la page [WCF Data Services Quickstart (OData Service and WPF Client)](http://go.microsoft.com/fwlink/?LinkId=179994) .</span><span class="sxs-lookup"><span data-stu-id="01a7e-121">Project files from a completed version of the quickstart can be downloaded from the [WCF Data Services Documentation Samples](http://go.microsoft.com/fwlink/?LinkId=179994) page.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="01a7e-122">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="01a7e-122">Next Steps</span></span>  
 <span data-ttu-id="01a7e-123">[Démarrer le didacticiel Démarrage rapide](../../../../docs/framework/data/wcf/creating-the-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="01a7e-123">[Start the Quickstart](../../../../docs/framework/data/wcf/creating-the-data-service.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01a7e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01a7e-124">See Also</span></span>  
 [<span data-ttu-id="01a7e-125">ADO.NET Entity Framework</span><span class="sxs-lookup"><span data-stu-id="01a7e-125">ADO.NET Entity Framework</span></span>](../../../../docs/framework/data/adonet/ef/index.md)
