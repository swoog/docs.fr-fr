---
title: Configuration simplifiée pour WCF Services
ms.date: 03/30/2017
ms.assetid: 1e39ec25-18a3-4fdc-b6a3-9dfafbd60112
ms.openlocfilehash: 80e2ac83ec0e07176d6afe6d34c63fb4d8e836d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33502262"
---
# <a name="simplified-configuration-for-wcf-services"></a><span data-ttu-id="c501c-102">Configuration simplifiée pour WCF Services</span><span class="sxs-lookup"><span data-stu-id="c501c-102">Simplified Configuration for WCF Services</span></span>
<span data-ttu-id="c501c-103">Cet exemple montre comment implémenter et configurer un service classique et le client à l’aide de Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="c501c-103">This sample demonstrates how to implement and configure a typical service and client using Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="c501c-104">Cet exemple constitue la base de tous les autres exemples de technologie de base.</span><span class="sxs-lookup"><span data-stu-id="c501c-104">This sample is the basis for all other basic technology samples.</span></span>  
  
 <span data-ttu-id="c501c-105">Ce service, qui expose un point de terminaison permettant de communiquer avec le service, utilise la configuration simplifiée de [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c501c-105">This service, which exposes an endpoint for communicating with the service, uses the simplified configuration in [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)].</span></span> <span data-ttu-id="c501c-106">Avant [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], le point de terminaison est généralement défini dans un fichier de configuration (Web.config), comme le montre l'exemple de code de configuration suivant.</span><span class="sxs-lookup"><span data-stu-id="c501c-106">Prior to [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], the endpoint is typically defined in a configuration file (Web.config), as shown in the following example configuration code.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<!-- Copyright ©) Microsoft Corporation.  All Rights Reserved. -->  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="CalculatorServiceBehavior">  
          <serviceMetadata httpGetEnabled="True"/>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <services>  
      <service name="Microsoft.Samples.GettingStarted.CalculatorService"  
               behaviorConfiguration="CalculatorServiceBehavior">  
        <endpoint address="" binding="basicHttpBinding" contract="ICalculator"/>  
        <endpoint address="mex" binding="mexHttpBinding" contract="IMetadataExchange"/>  
      </service>  
    </services>  
  </system.serviceModel>  
</configuration>  
```  
  
 <span data-ttu-id="c501c-107">Dans [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], l'élément `<service>` est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c501c-107">In [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)], the `<service>` element is optional.</span></span> <span data-ttu-id="c501c-108">Lorsqu'un service ne définit pas de points de terminaison, un point de terminaison est ajouté au service pour chaque adresse de base et contrat implémentés.</span><span class="sxs-lookup"><span data-stu-id="c501c-108">When a service does not define any endpoints, an endpoint for each base address and contract implemented are added to the service.</span></span> <span data-ttu-id="c501c-109">L'adresse de base est ajoutée au nom du contrat pour déterminer le point de terminaison et la liaison est déterminée par le schéma d'adresse.</span><span class="sxs-lookup"><span data-stu-id="c501c-109">The base address is appended to the contract name to determine the endpoint and the binding is determined by the address scheme.</span></span> <span data-ttu-id="c501c-110">L'exemple de code suivant montre un fichier de configuration simplifié.</span><span class="sxs-lookup"><span data-stu-id="c501c-110">The following code example demonstrates a simplified configuration file.</span></span> <span data-ttu-id="c501c-111">Tel qu’il est configuré, le service est accessible à http://localhost/servicemodelsamples/service.svc par un client sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c501c-111">As configured, the service can be accessed at http://localhost/servicemodelsamples/service.svc by a client on the same computer.</span></span> <span data-ttu-id="c501c-112">Pour que les clients installés sur des ordinateurs distants puissent accéder au service, un nom de domaine complet doit être spécifié au lieu de localhost.</span><span class="sxs-lookup"><span data-stu-id="c501c-112">For clients on remote computers to access the service, a fully-qualified domain name must be specified instead of localhost.</span></span> <span data-ttu-id="c501c-113">Par défaut, le service n'expose pas de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="c501c-113">The service does not expose metadata by default.</span></span> <span data-ttu-id="c501c-114">Comme tel, le service active le comportement <xref:System.ServiceModel.Description.ServiceMetadataBehavior>.</span><span class="sxs-lookup"><span data-stu-id="c501c-114">As such, the service turns on the <xref:System.ServiceModel.Description.ServiceMetadataBehavior> behavior.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<!-- Copyright © Microsoft Corporation.  All Rights Reserved. -->  
<configuration>  
  <system.serviceModel>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="">  
          <serviceMetadata httpGetEnabled="True"/>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
  </system.serviceModel>  
</configuration>  
```  
  
### <a name="to-use-this-sample"></a><span data-ttu-id="c501c-115">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="c501c-115">To use this sample</span></span>  
  
1.  <span data-ttu-id="c501c-116">Assurez-vous d’avoir effectué la [procédure d’installation d’à usage unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="c501c-116">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2.  <span data-ttu-id="c501c-117">Pour générer la solution, suivez les instructions de [génération des exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="c501c-117">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
3.  <span data-ttu-id="c501c-118">Exécutez l'exemple en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="c501c-118">Run the sample by following these steps:</span></span>  
  
    1.  <span data-ttu-id="c501c-119">Bouton droit sur le **Service** de projet et sélectionnez **définir comme projet de démarrage**, puis appuyez sur **Ctrl + F5**.</span><span class="sxs-lookup"><span data-stu-id="c501c-119">Right click the **Service** project and select **Set as StartUp project**, then press **Ctrl+F5**.</span></span>  
  
    2.  <span data-ttu-id="c501c-120">Attendez le message de la console confirmant le bon fonctionnement du service.</span><span class="sxs-lookup"><span data-stu-id="c501c-120">Wait for the console output confirming that the service is up and running.</span></span>  
  
    3.  <span data-ttu-id="c501c-121">Bouton droit sur le **Client** de projet et sélectionnez **définir comme projet de démarrage**, puis appuyez sur **Ctrl + F5**.</span><span class="sxs-lookup"><span data-stu-id="c501c-121">Right click the **Client** project and select **Set as StartUp project**, then press **Ctrl+F5**.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="c501c-122">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c501c-122">The samples may already be installed on your computer.</span></span> <span data-ttu-id="c501c-123">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="c501c-123">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="c501c-124">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="c501c-124">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="c501c-125">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="c501c-125">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\ConfigSimplificationIn40`  
  
## <a name="see-also"></a><span data-ttu-id="c501c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c501c-126">See Also</span></span>  
 [<span data-ttu-id="c501c-127">Exemples de gestion de AppFabric</span><span class="sxs-lookup"><span data-stu-id="c501c-127">AppFabric Management Samples</span></span>](http://go.microsoft.com/fwlink/?LinkId=193960)  
 [<span data-ttu-id="c501c-128">Configuration simplifiée</span><span class="sxs-lookup"><span data-stu-id="c501c-128">Simplified Configuration</span></span>](../../../../docs/framework/wcf/simplified-configuration.md)
