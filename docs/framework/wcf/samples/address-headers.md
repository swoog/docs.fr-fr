---
title: Address Headers
ms.date: 03/30/2017
ms.assetid: b0c94d4a-3bde-4b4d-bb6d-9f12bc3a6940
ms.openlocfilehash: 4ccb309178251b32068d6cdbb81874322f991bb9
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57673234"
---
# <a name="address-headers"></a><span data-ttu-id="ca820-102">Address Headers</span><span class="sxs-lookup"><span data-stu-id="ca820-102">Address Headers</span></span>

<span data-ttu-id="ca820-103">Cet exemple montre comment les clients peuvent passer des paramètres de référence à un service à l’aide de Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="ca820-103">The Address Headers sample demonstrates how clients can pass reference parameters to a service using Windows Communication Foundation (WCF).</span></span>

> [!NOTE]
> <span data-ttu-id="ca820-104">La procédure d'installation ainsi que les instructions de génération relatives à cet exemple figurent à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ca820-104">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="ca820-105">La spécification WS-Addressing définit la référence de point de terminaison permettant de s'adresser à un point de terminaison de service Web particulier.</span><span class="sxs-lookup"><span data-stu-id="ca820-105">The WS-Addressing specification defines the notion of an endpoint reference as a way to address a particular Web service endpoint.</span></span> <span data-ttu-id="ca820-106">Dans WCF, les références de point de terminaison sont modélisées à l’aide de la `EndpointAddress` classe - `EndpointAddress` est le type du champ adresse de la `ServiceEndpoint` classe.</span><span class="sxs-lookup"><span data-stu-id="ca820-106">In WCF, endpoint references are modeled using the `EndpointAddress` class - `EndpointAddress` is the type of the Address field of the `ServiceEndpoint` class.</span></span>

<span data-ttu-id="ca820-107">Chaque référence dans le modèle de référence de point de terminaison peut contenir des paramètres ajoutant des informations d'identification supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ca820-107">Part of the endpoint reference model is that each reference can carry some reference parameters that add extra identifying information.</span></span> <span data-ttu-id="ca820-108">Dans WCF, ces paramètres de référence sont modélisés en tant qu’instances de `AddressHeader` classe.</span><span class="sxs-lookup"><span data-stu-id="ca820-108">In WCF, these reference parameters are modeled as instances of `AddressHeader` class.</span></span>

<span data-ttu-id="ca820-109">Dans cet exemple, le client ajoute un paramètre de référence à l'adresse `EndpointAddress` de point de terminaison du client.</span><span class="sxs-lookup"><span data-stu-id="ca820-109">In this sample, the client adds a reference parameter to the `EndpointAddress` of the client endpoint.</span></span> <span data-ttu-id="ca820-110">Le service recherche ce paramètre et utilise sa valeur dans la logique de son opération « Hello ».</span><span class="sxs-lookup"><span data-stu-id="ca820-110">The service looks for this reference parameter and uses its value in the logic of its "Hello" service operation.</span></span>

## <a name="client"></a><span data-ttu-id="ca820-111">Client</span><span class="sxs-lookup"><span data-stu-id="ca820-111">Client</span></span>

<span data-ttu-id="ca820-112">Pour que le client envoie un paramètre de référence, il doit ajouter un en-tête `AddressHeader` à l'adresse `EndpointAddress` du `ServiceEndpoint`.</span><span class="sxs-lookup"><span data-stu-id="ca820-112">For the client to send a reference parameter, it must add an `AddressHeader` to the `EndpointAddress` of the `ServiceEndpoint`.</span></span> <span data-ttu-id="ca820-113">La classe `EndpointAddress` étant immuable, le changement d'une adresse de point de terminaison doit être effectué à l'aide de la classe `EndpointAddressBuilder`.</span><span class="sxs-lookup"><span data-stu-id="ca820-113">Because the `EndpointAddress` class is immutable, modification of an endpoint address must be done using the `EndpointAddressBuilder` class.</span></span> <span data-ttu-id="ca820-114">Le code suivant initialise le client pour envoyer un paramètre de référence dans le cadre de son message.</span><span class="sxs-lookup"><span data-stu-id="ca820-114">The following code initializes the client to send a reference parameter as part of its message.</span></span>

```csharp
HelloClient client = new HelloClient();
EndpointAddressBuilder builder =
    new EndpointAddressBuilder(client.Endpoint.Address);
AddressHeader header =
    AddressHeader.CreateAddressHeader(IDName, IDNamespace, "John");
builder.Headers.Add(header);
client.Endpoint.Address = builder.ToEndpointAddress();
```

<span data-ttu-id="ca820-115">Le code crée un `EndpointAddressBuilder` en utilisant comme valeur initiale l'adresse `EndpointAddress` d'origine.</span><span class="sxs-lookup"><span data-stu-id="ca820-115">The code creates an `EndpointAddressBuilder` using the original `EndpointAddress` as an initial value.</span></span> <span data-ttu-id="ca820-116">Il ajoute ensuite un en-tête d’adresse qui vient d’être créé ; l’appel à `CreateAddressHeader` crée un en-tête avec un nom particulier, un espace de noms et une valeur.</span><span class="sxs-lookup"><span data-stu-id="ca820-116">It then adds a newly created address header; the call to `CreateAddressHeader` creates a header with a particular name, namespace, and value.</span></span> <span data-ttu-id="ca820-117">Dans cet exemple, la valeur est « John ».</span><span class="sxs-lookup"><span data-stu-id="ca820-117">Here the value is "John".</span></span> <span data-ttu-id="ca820-118">Une fois l'en-tête ajouté au générateur, la méthode `ToEndpointAddress()` reconvertit le générateur (altérable) en une adresse de point de terminaison (immuable) assignée de nouveau au champ d'adresse de point de terminaison du client.</span><span class="sxs-lookup"><span data-stu-id="ca820-118">Once the header is added to the builder, the `ToEndpointAddress()` method converts the (mutable) builder back into an (immutable) endpoint address, which is assigned back to the client endpoint's Address field.</span></span>

<span data-ttu-id="ca820-119">À présent, lorsque le client appelle la méthode `Console.WriteLine(client.Hello());`, le service peut obtenir la valeur de ce paramètre d'adresse, comme en témoigne le résultat obtenu par le client.</span><span class="sxs-lookup"><span data-stu-id="ca820-119">Now when the client calls `Console.WriteLine(client.Hello());`, the service is able to get the value of this address parameter, as seen in the resulting output of the client.</span></span>

`Hello, John`

## <a name="server"></a><span data-ttu-id="ca820-120">Serveur</span><span class="sxs-lookup"><span data-stu-id="ca820-120">Server</span></span>

<span data-ttu-id="ca820-121">L'implémentation de l'opération de service `Hello()` utilise le contexte `OperationContext` actuel pour inspecter la valeur des en-têtes figurant dans le message entrant.</span><span class="sxs-lookup"><span data-stu-id="ca820-121">The implementation of the service operation `Hello()` uses the current `OperationContext` to inspect the values of the headers on the incoming message.</span></span>

```csharp
string id = null;
// look at headers on incoming message
for (int i = 0;
     i < OperationContext.Current.IncomingMessageHeaders.Count;
     ++i)
{
    MessageHeaderInfo h = OperationContext.Current.IncomingMessageHeaders[i];
    // for any reference parameters with the correct name & namespace
    if (h.IsReferenceParameter &&
        h.Name == IDName &&
        h.Namespace == IDNamespace)
    {
        // read the value of that header
        XmlReader xr = OperationContext.Current.IncomingMessageHeaders.GetReaderAtHeader(i);
        id = xr.ReadElementContentAsString();
    }
}
return "Hello, " + id;
```

<span data-ttu-id="ca820-122">Le code recherche les en-têtes correspondant à des paramètres de référence contenant le nom défini en parcourant tous les en-têtes figurant dans le message entrant.</span><span class="sxs-lookup"><span data-stu-id="ca820-122">The code iterates over all the headers on the incoming message, looking for headers that are reference parameters with the particular name and.</span></span> <span data-ttu-id="ca820-123">Lorsqu'il trouve un tel paramètre, il lit sa valeur, puis la stocke dans la variable « id ».</span><span class="sxs-lookup"><span data-stu-id="ca820-123">When the parameter is found, it reads the value of the parameter and stores it in the "id" variable.</span></span>

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ca820-124">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="ca820-124">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="ca820-125">Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ca820-125">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="ca820-126">Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ca820-126">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>

3. <span data-ttu-id="ca820-127">Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ca820-127">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca820-128">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ca820-128">The samples may already be installed on your machine.</span></span> <span data-ttu-id="ca820-129">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="ca820-129">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="ca820-130">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="ca820-130">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ca820-131">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="ca820-131">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Client\AddressHeaders`
