---
title: 'Comment : migrer le code client des services Web ASP.NET vers Windows Communication Foundation'
ms.date: 03/30/2017
ms.assetid: 2e0a22a7-e1d5-4718-8997-4319a7cd9027
ms.openlocfilehash: cb60f9cb2e8f35ee703b049eae9e3d99c1ec7d49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33491128"
---
# <a name="how-to-migrate-aspnet-web-service-client-code-to-the-windows-communication-foundation"></a><span data-ttu-id="47fd8-102">Comment : migrer le code client des services Web ASP.NET vers Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="47fd8-102">How to: Migrate ASP.NET Web Service Client Code to the Windows Communication Foundation</span></span>
<span data-ttu-id="47fd8-103">La procédure suivante décrit les étapes générales à suivre pour migrer le code client de Service Web ASP.NET vers WCF.</span><span class="sxs-lookup"><span data-stu-id="47fd8-103">The following procedure describes the broad steps that need to be followed to migrate ASP.NET Web Service client code to WCF.</span></span>  
  
## <a name="procedure"></a><span data-ttu-id="47fd8-104">Procédure</span><span class="sxs-lookup"><span data-stu-id="47fd8-104">Procedure</span></span>  
  
#### <a name="to-migrate-aspnet-web-service-client-code-to-wcf"></a><span data-ttu-id="47fd8-105">Pour migrer le code client des services Web ASP.NET vers WCF</span><span class="sxs-lookup"><span data-stu-id="47fd8-105">To migrate ASP.NET Web Service client code to WCF</span></span>  
  
1.  <span data-ttu-id="47fd8-106">Assurez-vous qu'un jeu complet de tests existe pour le client.</span><span class="sxs-lookup"><span data-stu-id="47fd8-106">Ensure that a comprehensive set of tests exist for the client.</span></span>  
  
2.  <span data-ttu-id="47fd8-107">Utilisez Visual Studio 2005 pour mettre à niveau l'application cliente vers .NET 2.0.</span><span class="sxs-lookup"><span data-stu-id="47fd8-107">Use Visual Studio 2005 to upgrade the client application to .NET 2.0.</span></span> <span data-ttu-id="47fd8-108">Exécutez l'ensemble des tests.</span><span class="sxs-lookup"><span data-stu-id="47fd8-108">Run the set of tests.</span></span>  
  
3.  <span data-ttu-id="47fd8-109">Supprimez le code client ASP.NET du projet client.</span><span class="sxs-lookup"><span data-stu-id="47fd8-109">Remove ASP.NET client code from the client project.</span></span> <span data-ttu-id="47fd8-110">Ce code se trouve dans les modules générés à l'aide de l'outil WSDL.exe.</span><span class="sxs-lookup"><span data-stu-id="47fd8-110">That code is in modules generated using the WSDL.exe tool.</span></span>  
  
4.  <span data-ttu-id="47fd8-111">Générer le code du client WCF à l’aide du [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span><span class="sxs-lookup"><span data-stu-id="47fd8-111">Generate WCF client code using the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="47fd8-112">Ajoutez ce code au projet client et fusionnez la sortie de la configuration dans le fichier de configuration existant du client.</span><span class="sxs-lookup"><span data-stu-id="47fd8-112">Add that code to the client project and merge the configuration output into the client’s existing configuration file.</span></span>  
  
5.  <span data-ttu-id="47fd8-113">Compilez l'application.</span><span class="sxs-lookup"><span data-stu-id="47fd8-113">Compile the application.</span></span> <span data-ttu-id="47fd8-114">Réparer les erreurs de compilation en remplaçant les références pour les types de clients anciens ASP.NET avec des références aux nouveaux types de client WCF.</span><span class="sxs-lookup"><span data-stu-id="47fd8-114">Repair the compilation errors by replacing references to the former ASP.NET client types with references to the new WCF client types.</span></span>  
  
6.  <span data-ttu-id="47fd8-115">Exécutez l'ensemble des tests.</span><span class="sxs-lookup"><span data-stu-id="47fd8-115">Run the set of tests.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47fd8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47fd8-116">See Also</span></span>  
 [<span data-ttu-id="47fd8-117">Guide pratique pour migrer le code d’un service web ASP.NET vers Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="47fd8-117">How to: Migrate ASP.NET Web Service Code to the Windows Communication Foundation</span></span>](../../../../docs/framework/wcf/feature-details/migrate-asp-net-web-service-to-wcf.md)
