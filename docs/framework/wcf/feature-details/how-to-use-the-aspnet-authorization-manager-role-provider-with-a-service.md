---
title: 'Procédure : utiliser le fournisseur de rôle du Gestionnaire d’autorisations ASP.NET avec un service'
ms.date: 03/30/2017
ms.assetid: f21deb81-91ef-49ef-94d6-494785143271
ms.openlocfilehash: ebdfa8bd7d222c4f9a33b6718b215d327d589c6d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62047293"
---
# <a name="how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service"></a><span data-ttu-id="ffc27-102">Procédure : utiliser le fournisseur de rôle du Gestionnaire d’autorisations ASP.NET avec un service</span><span class="sxs-lookup"><span data-stu-id="ffc27-102">How to: Use the ASP.NET Authorization Manager Role Provider with a Service</span></span>
<span data-ttu-id="ffc27-103">Lorsque [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] héberge un service Web, vous pouvez intégrer le Gestionnaire d'autorisations dans l'application pour fournir l'autorisation au service.</span><span class="sxs-lookup"><span data-stu-id="ffc27-103">When [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] hosts a Web service, you can integrate Authorization Manager into the application to provide authorization to the service.</span></span> <span data-ttu-id="ffc27-104">Le Gestionnaire d'autorisations permet à un développeur d'applications de définir des opérations individuelles qui peuvent être regroupées pour former des tâches.</span><span class="sxs-lookup"><span data-stu-id="ffc27-104">Authorization Manager enables an application developer to define individual operations, which can be grouped together to form tasks.</span></span> <span data-ttu-id="ffc27-105">Un administrateur peut autoriser ensuite que les rôles exécutent des tâches spécifiques ou des opérations individuelles.</span><span class="sxs-lookup"><span data-stu-id="ffc27-105">An administrator can then authorize roles to perform specific tasks or individual operations.</span></span> <span data-ttu-id="ffc27-106">Le Gestionnaire d’autorisations fournit un outil d’administration sous la forme d’un composant logiciel enfichable MMC (Microsoft Management Console) pour gérer des rôles, des tâches, des opérations et des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ffc27-106">Authorization Manager provides an administration tool as a Microsoft Management Console (MMC) snap-in to manage roles, tasks, operations, and users.</span></span> <span data-ttu-id="ffc27-107">Les administrateurs configurent un magasin de stratégie du Gestionnaire d'autorisations dans un fichier XML, Active Directory, ou dans un magasin Active Directory en mode application (ADAM).</span><span class="sxs-lookup"><span data-stu-id="ffc27-107">Administrators configure an Authorization Manager policy store in an XML file, Active Directory, or in an Active Directory Application Mode (ADAM) store.</span></span>  
  
 <span data-ttu-id="ffc27-108">Le Gestionnaire d'autorisations est intégré dans l'application en configurant le fournisseur de rôle [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] du Gestionnaire d'autorisations pour l'application [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] qui héberge le service Web.</span><span class="sxs-lookup"><span data-stu-id="ffc27-108">Authorization Manager is Integrated into the application by configuring the Authorization Manager [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] role provider for the [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] application that is hosting the Web service.</span></span> <span data-ttu-id="ffc27-109">Comme les autres [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] les fournisseurs de rôles, le Gestionnaire d’autorisations [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] fournisseur de rôle est configuré à l’aide de la <`providers`> élément.</span><span class="sxs-lookup"><span data-stu-id="ffc27-109">Like other [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] role providers, the Authorization Manager [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] role provider is configured using the <`providers`> element.</span></span>  
  
 <span data-ttu-id="ffc27-110">L'exemple de code suivant représente une partie d'un fichier de configuration pour un service Web qui intègre le Gestionnaire d'autorisations dans l'application.</span><span class="sxs-lookup"><span data-stu-id="ffc27-110">The following code example is a portion of a configuration file for a Web service that is integrating Authorization Manager into the application.</span></span>  
  
```xml  
<system.web>  
    <roleManager enabled="true" defaultProvider="AzManRoleProvider">  
      <providers>  
        <add name="AzManRoleProvider"  
             type="System.Web.Security.AuthorizationStoreRoleProvider, System.Web, Version=2.0.0.0, Culture=neutral, publicKeyToken=b03f5f7f11d50a3a"  
             connectionStringName="AzManPolicyStoreConnectionString"   
             applicationName="SecureService"/>  
      </providers>  
    </roleManager>  
</system.web>  
```  
  
 <span data-ttu-id="ffc27-111">Pour plus d’informations sur l’intégration d’un [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] fournisseur de rôles avec une application WCF, consultez [Comment : Utiliser le fournisseur de rôle ASP.NET avec un Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="ffc27-111">For more information about integrating an [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] role provider with a WCF application, see [How to: Use the ASP.NET Role Provider with a Service](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md).</span></span> <span data-ttu-id="ffc27-112">Pour plus d’informations sur l’utilisation du Gestionnaire d’autorisations avec [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], consultez [Comment : Utilisez le Gestionnaire d’autorisations (AzMan) avec ASP.NET 2.0](https://go.microsoft.com/fwlink/?LinkId=71303).</span><span class="sxs-lookup"><span data-stu-id="ffc27-112">For more information about using Authorization Manager with [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], see [How to: Use Authorization Manager (AzMan) with ASP.NET 2.0](https://go.microsoft.com/fwlink/?LinkId=71303).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffc27-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffc27-113">See also</span></span>

- [<span data-ttu-id="ffc27-114">Guide pratique pour Utiliser le fournisseur de rôle ASP.NET avec un Service</span><span class="sxs-lookup"><span data-stu-id="ffc27-114">How to: Use the ASP.NET Role Provider with a Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)
