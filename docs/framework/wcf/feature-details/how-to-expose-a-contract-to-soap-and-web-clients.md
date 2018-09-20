---
title: 'Comment : exposer un contrat à des clients SOAP et Web'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: bb765a48-12f2-430d-a54d-6f0c20f2a23a
ms.openlocfilehash: d82c5e3fc33528eadc3c404cca59a3dcf905e0e2
ms.sourcegitcommit: 3ab9254890a52a50762995fa6d7d77a00348db7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46323971"
---
# <a name="how-to-expose-a-contract-to-soap-and-web-clients"></a><span data-ttu-id="780d8-102">Comment : exposer un contrat à des clients SOAP et Web</span><span class="sxs-lookup"><span data-stu-id="780d8-102">How to: Expose a Contract to SOAP and Web Clients</span></span>

<span data-ttu-id="780d8-103">Par défaut, Windows Communication Foundation (WCF), points de terminaison disponibles uniquement aux clients SOAP.</span><span class="sxs-lookup"><span data-stu-id="780d8-103">By default, Windows Communication Foundation (WCF) makes endpoints available only to SOAP clients.</span></span> <span data-ttu-id="780d8-104">Dans [Comment : créer un Service WCF Web HTTP de base](../../../../docs/framework/wcf/feature-details/how-to-create-a-basic-wcf-web-http-service.md), un point de terminaison est accessible aux clients non-SOAP.</span><span class="sxs-lookup"><span data-stu-id="780d8-104">In [How to: Create a Basic WCF Web HTTP Service](../../../../docs/framework/wcf/feature-details/how-to-create-a-basic-wcf-web-http-service.md), an endpoint is made available to non-SOAP clients.</span></span> <span data-ttu-id="780d8-105">Dans certains cas, vous pouvez souhaiter rendre le même contrat disponible pour les deux, comme point de terminaison Web et comme point de terminaison SOAP.</span><span class="sxs-lookup"><span data-stu-id="780d8-105">There may be times when you want to make the same contract available both ways, as a Web endpoint and as a SOAP endpoint.</span></span> <span data-ttu-id="780d8-106">Cette rubrique explique comment procéder.</span><span class="sxs-lookup"><span data-stu-id="780d8-106">This topic shows an example of how to do this.</span></span>

## <a name="to-define-the-service-contract"></a><span data-ttu-id="780d8-107">Pour définir le contrat de service</span><span class="sxs-lookup"><span data-stu-id="780d8-107">To define the service contract</span></span>

1. <span data-ttu-id="780d8-108">Définir un contrat de service à l’aide d’une interface marquée avec le <xref:System.ServiceModel.ServiceContractAttribute>, <xref:System.ServiceModel.Web.WebInvokeAttribute> et <xref:System.ServiceModel.Web.WebGetAttribute> des attributs, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="780d8-108">Define a service contract using an interface marked with the <xref:System.ServiceModel.ServiceContractAttribute>, <xref:System.ServiceModel.Web.WebInvokeAttribute> and the <xref:System.ServiceModel.Web.WebGetAttribute> attributes, as shown in the following code:</span></span>

    [!code-csharp[htSoapWeb#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#0)]
    [!code-vb[htSoapWeb#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#0)]

    > [!NOTE]
    > <span data-ttu-id="780d8-109">Par défaut, <xref:System.ServiceModel.Web.WebInvokeAttribute> mappe des appels POST à l'opération.</span><span class="sxs-lookup"><span data-stu-id="780d8-109">By default <xref:System.ServiceModel.Web.WebInvokeAttribute> maps POST calls to the operation.</span></span> <span data-ttu-id="780d8-110">Toutefois, vous pouvez spécifier la méthode pour mapper à l'opération un paramètre pour "method=".</span><span class="sxs-lookup"><span data-stu-id="780d8-110">You can, however, specify the method to map to the operation by specifying a "method=" parameter.</span></span> <span data-ttu-id="780d8-111"><xref:System.ServiceModel.Web.WebGetAttribute> n'a pas de paramètre « method= » et mappe uniquement des appels GET à l'opération de service.</span><span class="sxs-lookup"><span data-stu-id="780d8-111"><xref:System.ServiceModel.Web.WebGetAttribute> does not have a "method=" parameter and only maps GET calls to the service operation.</span></span>

2. <span data-ttu-id="780d8-112">Implémentez le contrat de service, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="780d8-112">Implement the service contract, as shown in the following code:</span></span>

     [!code-csharp[htSoapWeb#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#1)]
     [!code-vb[htSoapWeb#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#1)]

## <a name="to-host-the-service"></a><span data-ttu-id="780d8-113">Pour héberger le service</span><span class="sxs-lookup"><span data-stu-id="780d8-113">To host the service</span></span>

1. <span data-ttu-id="780d8-114">Créer un <xref:System.ServiceModel.ServiceHost> de l’objet, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="780d8-114">Create a <xref:System.ServiceModel.ServiceHost> object, as shown in the following code:</span></span>

     [!code-csharp[htSoapWeb#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#2)]
     [!code-vb[htSoapWeb#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#2)]

2. <span data-ttu-id="780d8-115">Ajouter un <xref:System.ServiceModel.Description.ServiceEndpoint> avec <xref:System.ServiceModel.BasicHttpBinding> pour le point de terminaison SOAP, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="780d8-115">Add a <xref:System.ServiceModel.Description.ServiceEndpoint> with <xref:System.ServiceModel.BasicHttpBinding> for the SOAP endpoint, as shown in the following code:</span></span>

     [!code-csharp[htSoapWeb#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#3)]
     [!code-vb[htSoapWeb#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#3)]

3. <span data-ttu-id="780d8-116">Ajouter un <xref:System.ServiceModel.Description.ServiceEndpoint> avec <xref:System.ServiceModel.WebHttpBinding> pour le point de terminaison non-SOAP et ajoutez le <xref:System.ServiceModel.Description.WebHttpBehavior> au point de terminaison, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="780d8-116">Add a <xref:System.ServiceModel.Description.ServiceEndpoint> with <xref:System.ServiceModel.WebHttpBinding> for the non-SOAP endpoint and add the <xref:System.ServiceModel.Description.WebHttpBehavior> to the endpoint, as shown in the following code:</span></span>

     [!code-csharp[htSoapWeb#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#4)]
     [!code-vb[htSoapWeb#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#4)]

4. <span data-ttu-id="780d8-117">Appelez `Open()` sur un <xref:System.ServiceModel.ServiceHost> instance pour ouvrir l’hôte de service, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="780d8-117">Call `Open()` on a <xref:System.ServiceModel.ServiceHost> instance to open the service host, as shown in the following code:</span></span>

     [!code-csharp[htSoapWeb#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#5)]
     [!code-vb[htSoapWeb#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#5)]

## <a name="to-call-service-operations-mapped-to-get-in-internet-explorer"></a><span data-ttu-id="780d8-118">Pour appeler des opérations de service mappées à GET dans Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="780d8-118">To call service operations mapped to GET in Internet Explorer</span></span>

1. <span data-ttu-id="780d8-119">Ouvrez Internet Explorer et tapez «`http://localhost:8000/Web/EchoWithGet?s=Hello, world!`» et appuyez sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="780d8-119">Open Internet Explorer and type "`http://localhost:8000/Web/EchoWithGet?s=Hello, world!`" and press ENTER.</span></span> <span data-ttu-id="780d8-120">L’URL contient l’adresse de base du service (`http://localhost:8000/`), l’adresse relative du point de terminaison (« »), l’opération de service à appeler (« EchoWithGet ») et un point d’interrogation suivi d’une liste de paramètres séparés par une esperluette (&).</span><span class="sxs-lookup"><span data-stu-id="780d8-120">The URL contains the base address of the service (`http://localhost:8000/`), the relative address of the endpoint (""), the service operation to call ("EchoWithGet"), and a question mark followed by a list of named parameters separated by an ampersand (&).</span></span>

## <a name="to-call-service-operations-on-the-web-endpoint-in-code"></a><span data-ttu-id="780d8-121">Pour appeler des opérations de service sur le point de terminaison Web dans le code</span><span class="sxs-lookup"><span data-stu-id="780d8-121">To call service operations on the Web endpoint in code</span></span>

1. <span data-ttu-id="780d8-122">Créez une instance de <xref:System.ServiceModel.Web.WebChannelFactory%601> au sein d'un bloc `using`, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="780d8-122">Create an instance of <xref:System.ServiceModel.Web.WebChannelFactory%601> within a `using` block, as shown in the following code.</span></span>

     [!code-csharp[htSoapWeb#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#6)]
     [!code-vb[htSoapWeb#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#6)]

> [!NOTE]
> <span data-ttu-id="780d8-123">`Close()` est automatiquement appelé sur le canal à la fin du bloc `using`.</span><span class="sxs-lookup"><span data-stu-id="780d8-123">`Close()` is automatically called on the channel at the end of the `using` block.</span></span>

1. <span data-ttu-id="780d8-124">Créez le canal, puis appelez le service, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="780d8-124">Create the channel and call the service, as shown in the following code.</span></span>

     [!code-csharp[htSoapWeb#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#8)]
     [!code-vb[htSoapWeb#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#8)]

## <a name="to-call-service-operations-on-the-soap-endpoint"></a><span data-ttu-id="780d8-125">Pour appeler des opérations de service sur le point de terminaison SOAP</span><span class="sxs-lookup"><span data-stu-id="780d8-125">To call service operations on the SOAP endpoint</span></span>

1. <span data-ttu-id="780d8-126">Créez une instance de <xref:System.ServiceModel.ChannelFactory> au sein d'un bloc `using`, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="780d8-126">Create an instance of <xref:System.ServiceModel.ChannelFactory> within a `using` block, as shown in the following code.</span></span>

    [!code-csharp[htSoapWeb#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#10)]
    [!code-vb[htSoapWeb#10](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#10)]

2. <span data-ttu-id="780d8-127">Créez le canal, puis appelez le service, comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="780d8-127">Create the channel and call the service, as shown in the following code.</span></span>

    [!code-csharp[htSoapWeb#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#11)]
    [!code-vb[htSoapWeb#11](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#11)]

## <a name="to-close-the-service-host"></a><span data-ttu-id="780d8-128">Pour fermer l'hôte de service</span><span class="sxs-lookup"><span data-stu-id="780d8-128">To close the service host</span></span>

1. <span data-ttu-id="780d8-129">Fermez l'hôte de service comme illustré dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="780d8-129">Close the service host, as shown in the following code.</span></span>

    [!code-csharp[htSoapWeb#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#9)]
    [!code-vb[htSoapWeb#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#9)]

## <a name="example"></a><span data-ttu-id="780d8-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="780d8-130">Example</span></span>

<span data-ttu-id="780d8-131">Voici l’intégralité du code pour cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="780d8-131">The following is the full code listing for this topic:</span></span>

[!code-csharp[htSoapWeb#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/htsoapweb/cs/program.cs#13)]
[!code-vb[htSoapWeb#13](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htsoapweb/vb/program.vb#13)]

## <a name="compiling-the-code"></a><span data-ttu-id="780d8-132">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="780d8-132">Compiling the code</span></span>

 <span data-ttu-id="780d8-133">Lors de la compilation de Service.cs, référencez System.ServiceModel.dll et System.ServiceModel.Web.dll.</span><span class="sxs-lookup"><span data-stu-id="780d8-133">When compiling Service.cs, reference System.ServiceModel.dll and System.ServiceModel.Web.dll.</span></span>

## <a name="see-also"></a><span data-ttu-id="780d8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="780d8-134">See also</span></span>

- <xref:System.ServiceModel.WebHttpBinding>
- <xref:System.ServiceModel.Web.WebGetAttribute>
- <xref:System.ServiceModel.Web.WebInvokeAttribute>
- <xref:System.ServiceModel.Web.WebServiceHost>
- <xref:System.ServiceModel.ChannelFactory>
- <xref:System.ServiceModel.Description.WebHttpBehavior>
- [<span data-ttu-id="780d8-135">Modèle de programmation HTTP web WCF</span><span class="sxs-lookup"><span data-stu-id="780d8-135">WCF Web HTTP Programming Model</span></span>](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md)