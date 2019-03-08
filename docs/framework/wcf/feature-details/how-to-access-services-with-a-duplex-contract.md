---
title: 'Procédure : Access services avec un contrat duplex'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- duplex contracts [WCF]
ms.assetid: 746a9d64-f21c-426c-b85d-972e916ec6c5
ms.openlocfilehash: 366fd9d6aa220bcbec1ee8fb2a04d1b84755800a
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57678681"
---
# <a name="how-to-access-services-with-a-duplex-contract"></a><span data-ttu-id="af037-102">Procédure : Access services avec un contrat duplex</span><span class="sxs-lookup"><span data-stu-id="af037-102">How to: Access services with a duplex contract</span></span>

<span data-ttu-id="af037-103">L’une des fonctionnalités de Windows Communication Foundation (WCF) sont la possibilité de créer un service qui utilise un modèle de messagerie duplex.</span><span class="sxs-lookup"><span data-stu-id="af037-103">One feature of Windows Communication Foundation (WCF) is the ability to create a service that uses a duplex messaging pattern.</span></span> <span data-ttu-id="af037-104">Ce modèle permet à un service de communiquer avec un client via un rappel.</span><span class="sxs-lookup"><span data-stu-id="af037-104">This pattern allows a service to communicate with the client through a callback.</span></span> <span data-ttu-id="af037-105">Cette rubrique montre comment créer un client WCF dans une classe de client qui implémente l’interface de rappel.</span><span class="sxs-lookup"><span data-stu-id="af037-105">This topic shows the steps to create a WCF client in a client class that implements the callback interface.</span></span>

<span data-ttu-id="af037-106">Une liaison double expose l'adresse IP du client au service.</span><span class="sxs-lookup"><span data-stu-id="af037-106">A dual binding exposes the IP address of the client to the service.</span></span> <span data-ttu-id="af037-107">Ce client doit utiliser un mode de sécurité afin de garantir sa connexion à un service fiable.</span><span class="sxs-lookup"><span data-stu-id="af037-107">The client should use security to ensure that it connects only to services it trusts.</span></span>

<span data-ttu-id="af037-108">Pour obtenir un didacticiel sur la création d’un service WCF de base et un client, consultez [Getting Started Tutorial](../../../../docs/framework/wcf/getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="af037-108">For a tutorial on creating a basic WCF service and client, see [Getting Started Tutorial](../../../../docs/framework/wcf/getting-started-tutorial.md).</span></span>

## <a name="to-access-a-duplex-service"></a><span data-ttu-id="af037-109">Pour accéder à un service duplex</span><span class="sxs-lookup"><span data-stu-id="af037-109">To access a duplex service</span></span>

1. <span data-ttu-id="af037-110">Créez un service qui contient deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="af037-110">Create a service that contains two interfaces.</span></span> <span data-ttu-id="af037-111">La première interface est pour le service, la deuxième est pour le rappel.</span><span class="sxs-lookup"><span data-stu-id="af037-111">The first interface is for the service, the second is for the callback.</span></span> <span data-ttu-id="af037-112">Pour plus d’informations sur la création d’un service duplex, consultez [Comment : Créer un contrat Duplex](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).</span><span class="sxs-lookup"><span data-stu-id="af037-112">For more information about creating a duplex service, see [How to: Create a Duplex Contract](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md).</span></span>

2. <span data-ttu-id="af037-113">Exécutez le service.</span><span class="sxs-lookup"><span data-stu-id="af037-113">Run the service.</span></span>

3. <span data-ttu-id="af037-114">Utilisez le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer des contrats (interfaces) pour le client.</span><span class="sxs-lookup"><span data-stu-id="af037-114">Use the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) to generate contracts (interfaces) for the client.</span></span> <span data-ttu-id="af037-115">Pour savoir comment procéder, consultez [Comment : Créer un Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span><span class="sxs-lookup"><span data-stu-id="af037-115">For information about how to do this, see  [How to: Create a Client](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md).</span></span>

4. <span data-ttu-id="af037-116">Implémentez l'interface de rappel dans la classe client, comme illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="af037-116">Implement the callback interface in the client class, as shown in the following example.</span></span>

    ```csharp
    public class CallbackHandler : ICalculatorDuplexCallback
    {
        public void Result(double result)
        {
            Console.WriteLine("Result ({0})", result);
        }
        public void Equation(string equation)
        {
            Console.WriteLine("Equation({0})", equation);
        }
    }
    ```

    ```vb
    Public Class CallbackHandler
    Implements ICalculatorDuplexCallback
       Public Sub Result (ByVal result As Double)
          Console.WriteLine("Result ({0})", result)
       End Sub
        Public Sub Equation(ByVal equation As String)
            Console.WriteLine("Equation({0})", equation)
        End Sub
    End Class
    ```

5. <span data-ttu-id="af037-117">Créez une instance de la classe <xref:System.ServiceModel.InstanceContext>.</span><span class="sxs-lookup"><span data-stu-id="af037-117">Create an instance of the <xref:System.ServiceModel.InstanceContext> class.</span></span> <span data-ttu-id="af037-118">Le constructeur a besoin d'une instance de la classe client.</span><span class="sxs-lookup"><span data-stu-id="af037-118">The constructor requires an instance of the client class.</span></span>

    ```csharp
    InstanceContext site = new InstanceContext(new CallbackHandler());
    ```

    ```vb
    Dim site As InstanceContext = New InstanceContext(new CallbackHandler())
    ```

6. <span data-ttu-id="af037-119">Créez une instance du client WCF à l’aide du constructeur qui nécessite un <xref:System.ServiceModel.InstanceContext> objet.</span><span class="sxs-lookup"><span data-stu-id="af037-119">Create an instance of the WCF client using the constructor that requires an <xref:System.ServiceModel.InstanceContext> object.</span></span> <span data-ttu-id="af037-120">Le second paramètre du constructeur correspond au nom du point de terminaison trouvé dans le fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="af037-120">The second parameter of the constructor is the name of an endpoint found in the configuration file.</span></span>

    ```csharp
    CalculatorDuplexClient wcfClient = new CalculatorDuplexClient(site, "default");
    ```

    ```vb
    Dim wcfClient As New CalculatorDuplexClient(site, "default")
    ```

7. <span data-ttu-id="af037-121">Appelez les méthodes du client WCF en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="af037-121">Call the methods of the WCF client as required.</span></span>

## <a name="example"></a><span data-ttu-id="af037-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="af037-122">Example</span></span>

<span data-ttu-id="af037-123">L'exemple de code suivant illustre comment créer une classe client qui accède à un contrat duplex.</span><span class="sxs-lookup"><span data-stu-id="af037-123">The following code example demonstrates how to create a client class that accesses a duplex contract.</span></span>

[!code-csharp[S_DuplexClients#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_duplexclients/cs/client.cs#1)]
[!code-vb[S_DuplexClients#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_duplexclients/vb/client.vb#1)]

## <a name="see-also"></a><span data-ttu-id="af037-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af037-124">See also</span></span>

- [<span data-ttu-id="af037-125">Didacticiel Bien démarrer</span><span class="sxs-lookup"><span data-stu-id="af037-125">Getting Started Tutorial</span></span>](../../../../docs/framework/wcf/getting-started-tutorial.md)
- [<span data-ttu-id="af037-126">Guide pratique pour Créer un contrat Duplex</span><span class="sxs-lookup"><span data-stu-id="af037-126">How to: Create a Duplex Contract</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)
- [<span data-ttu-id="af037-127">Outil ServiceModel Metadata Utility (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="af037-127">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="af037-128">Guide pratique pour Créer un Client</span><span class="sxs-lookup"><span data-stu-id="af037-128">How to: Create a Client</span></span>](../../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [<span data-ttu-id="af037-129">Guide pratique pour Utiliser la classe ChannelFactory</span><span class="sxs-lookup"><span data-stu-id="af037-129">How to: Use the ChannelFactory</span></span>](../../../../docs/framework/wcf/feature-details/how-to-use-the-channelfactory.md)
