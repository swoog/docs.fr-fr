---
title: Exemple Basic
ms.date: 03/30/2017
ms.assetid: c1910bc1-3d0a-4fa6-b12a-4ed6fe759620
ms.openlocfilehash: 1ceee6dd11b59ab9b43797ca8b1fd80c232fc8ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62002636"
---
# <a name="basic-sample"></a><span data-ttu-id="e3e37-102">Exemple Basic</span><span class="sxs-lookup"><span data-stu-id="e3e37-102">Basic Sample</span></span>
<span data-ttu-id="e3e37-103">Cet exemple montre comment rendre un service détectable, et comment rechercher et appeler un service détectable.</span><span class="sxs-lookup"><span data-stu-id="e3e37-103">This sample shows how to make a service discoverable and how to search for and call a discoverable service.</span></span> <span data-ttu-id="e3e37-104">Cet exemple est composé de deux projets : service et client.</span><span class="sxs-lookup"><span data-stu-id="e3e37-104">This sample is composed of two projects: service and client.</span></span>

> [!NOTE]
>  <span data-ttu-id="e3e37-105">Cet exemple implémente la découverte dans le code.</span><span class="sxs-lookup"><span data-stu-id="e3e37-105">This sample implements discovery in code.</span></span>  <span data-ttu-id="e3e37-106">Pour obtenir un exemple qui implémente la découverte dans configuration, consultez [Configuration](../../../../docs/framework/wcf/samples/configuration-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e3e37-106">For a sample that implements discovery in configuration, see [Configuration](../../../../docs/framework/wcf/samples/configuration-sample.md).</span></span>  
  
## <a name="service"></a><span data-ttu-id="e3e37-107">Service</span><span class="sxs-lookup"><span data-stu-id="e3e37-107">Service</span></span>  
 <span data-ttu-id="e3e37-108">Il s'agit d'une implémentation simple du service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="e3e37-108">This is a simple calculator service implementation.</span></span> <span data-ttu-id="e3e37-109">Le code de découverte associé se trouve dans `Main`, où un <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior> est ajouté à l'hôte de service et où un <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> est ajouté comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e3e37-109">The discovery related code can be found in `Main` where a <xref:System.ServiceModel.Discovery.ServiceDiscoveryBehavior> is added to the service host and a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> is added as shown in the following code.</span></span>  
  
```csharp
using (ServiceHost serviceHost = new ServiceHost(typeof(CalculatorService), baseAddress))  
{  
    serviceHost.AddServiceEndpoint(typeof(ICalculatorService), new   
      WSHttpBinding(), String.Empty);  
  
    // Make the service discoverable over UDP multicast  
    serviceHost.Description.Behaviors.Add(new ServiceDiscoveryBehavior());                  
    serviceHost.AddServiceEndpoint(new UdpDiscoveryEndpoint());  
  
    serviceHost.Open();  
    // ...  
}  
```  
  
## <a name="client"></a><span data-ttu-id="e3e37-110">Client</span><span class="sxs-lookup"><span data-stu-id="e3e37-110">Client</span></span>  
 <span data-ttu-id="e3e37-111">Le client utilise un <xref:System.ServiceModel.Discovery.DynamicEndpoint> pour localiser le service.</span><span class="sxs-lookup"><span data-stu-id="e3e37-111">The client uses a <xref:System.ServiceModel.Discovery.DynamicEndpoint> to locate the service.</span></span> <span data-ttu-id="e3e37-112">Le <xref:System.ServiceModel.Discovery.DynamicEndpoint>, un point de terminaison standard, résout le point de terminaison du service lorsque le client est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e3e37-112">The <xref:System.ServiceModel.Discovery.DynamicEndpoint>, a standard endpoint, resolves the endpoint of the service when the client is opened.</span></span> <span data-ttu-id="e3e37-113">Dans ce cas, le <xref:System.ServiceModel.Discovery.DynamicEndpoint> recherche le service en se basant sur son contrat.</span><span class="sxs-lookup"><span data-stu-id="e3e37-113">In this case, the <xref:System.ServiceModel.Discovery.DynamicEndpoint> looks for the service based on the service contract.</span></span> <span data-ttu-id="e3e37-114">Le <xref:System.ServiceModel.Discovery.DynamicEndpoint> effectue la recherche sur un <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> par défaut.</span><span class="sxs-lookup"><span data-stu-id="e3e37-114">The <xref:System.ServiceModel.Discovery.DynamicEndpoint> conducts the search over a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> by default.</span></span> <span data-ttu-id="e3e37-115">Lorsqu’il trouve un point de terminaison de service, le client se connecte à ce service sur la liaison spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e3e37-115">Once it locates a service endpoint, the client connects to that service over the specified binding.</span></span>  
  
```csharp  
public static void Main()  
{  
   DynamicEndpoint dynamicEndpoint = new DynamicEndpoint( ContractDescription.GetContract(typeof(ICalculatorService)), new WSHttpBinding());  
   // ...  
}              
```  
  
 <span data-ttu-id="e3e37-116">Le client définit une méthode nommée `InvokeCalculatorService` qui utilise la classe <xref:System.ServiceModel.Discovery.DiscoveryClient> pour rechercher des services.</span><span class="sxs-lookup"><span data-stu-id="e3e37-116">The client defines a method called `InvokeCalculatorService` that uses the <xref:System.ServiceModel.Discovery.DiscoveryClient> class to search for services.</span></span> <span data-ttu-id="e3e37-117">Le <xref:System.ServiceModel.Discovery.DynamicEndpoint> hérite de <xref:System.ServiceModel.Description.ServiceEndpoint>, de sorte qu'il peut être passé à la méthode `InvokeCalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="e3e37-117">The <xref:System.ServiceModel.Discovery.DynamicEndpoint> inherits from <xref:System.ServiceModel.Description.ServiceEndpoint>, so it can be passed to the `InvokeCalculatorService` method.</span></span> <span data-ttu-id="e3e37-118">L'exemple utilise ensuite le <xref:System.ServiceModel.Discovery.DynamicEndpoint> pour créer une instance de `CalculatorServiceClient` et appelle les différentes opérations du service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="e3e37-118">The example then uses the <xref:System.ServiceModel.Discovery.DynamicEndpoint> to create an instance of `CalculatorServiceClient` and calls the various operations of the calculator service.</span></span>  
  
```csharp  
static void InvokeCalculatorService(ServiceEndpoint serviceEndpoint)  
{  
   // Create a client  
   CalculatorServiceClient client = new CalculatorServiceClient(serviceEndpoint);  
  
   Console.WriteLine("Invoking CalculatorService");  
   Console.WriteLine();  
  
   double value1 = 100.00D;  
   double value2 = 15.99D;  
  
   // Call the Add service operation.  
   double result = client.Add(value1, value2);  
   Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);  
  
   // Call the Subtract service operation.  
   result = client.Subtract(value1, value2);  
   Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result);  
  
   // Call the Multiply service operation.  
   result = client.Multiply(value1, value2);  
   Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result);  
  
   // Call the Divide service operation.  
   result = client.Divide(value1, value2);  
   Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result);  
   Console.WriteLine();  
  
   //Closing the client gracefully closes the connection and cleans up resources  
   client.Close();  
}  
```  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="e3e37-119">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="e3e37-119">To use this sample</span></span>  
  
1. <span data-ttu-id="e3e37-120">Cet exemple utilise des points de terminaison HTTP et pour exécuter cet exemple, des listes de contrôle d'accès (ACL) d'URL appropriées doivent être ajoutées.</span><span class="sxs-lookup"><span data-stu-id="e3e37-120">This sample uses HTTP endpoints and to run this sample, proper URL ACLs must be added.</span></span> <span data-ttu-id="e3e37-121">Pour plus d’informations, consultez [configuration de HTTP et HTTPS](https://go.microsoft.com/fwlink/?LinkId=70353).</span><span class="sxs-lookup"><span data-stu-id="e3e37-121">For more information, see [Configuring HTTP and HTTPS](https://go.microsoft.com/fwlink/?LinkId=70353).</span></span> <span data-ttu-id="e3e37-122">L'exécution de la commande suivante avec un privilège élevé doit ajouter les ACL appropriées.</span><span class="sxs-lookup"><span data-stu-id="e3e37-122">Executing the following command at an elevated privilege should add the appropriate ACLs.</span></span> <span data-ttu-id="e3e37-123">Vous pouvez substituer vos domaine et nom d’utilisateur aux arguments suivants si la commande ne fonctionne pas telle quelle.</span><span class="sxs-lookup"><span data-stu-id="e3e37-123">You may want to substitute your Domain and Username for the following arguments if the command does not work as is.</span></span> `netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%`  
  
2. <span data-ttu-id="e3e37-124">À l’aide de Visual Studio 2012, ouvrez Basic.sln et générez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e3e37-124">Using Visual Studio 2012, open the Basic.sln and build the sample.</span></span>  
  
3. <span data-ttu-id="e3e37-125">Exécutez l'application service.exe.</span><span class="sxs-lookup"><span data-stu-id="e3e37-125">Run the service.exe application.</span></span>  
  
4. <span data-ttu-id="e3e37-126">Une fois le service démarré, exécutez client.exe.</span><span class="sxs-lookup"><span data-stu-id="e3e37-126">After the service has started, run the client.exe.</span></span>  
  
5. <span data-ttu-id="e3e37-127">Observez que le client a trouvé le service sans connaître son adresse.</span><span class="sxs-lookup"><span data-stu-id="e3e37-127">Observe that the client was able to find the service without knowing its address.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e3e37-128">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e3e37-128">The samples may already be installed on your machine.</span></span> <span data-ttu-id="e3e37-129">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="e3e37-129">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="e3e37-130">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="e3e37-130">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="e3e37-131">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="e3e37-131">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\Basic`  
