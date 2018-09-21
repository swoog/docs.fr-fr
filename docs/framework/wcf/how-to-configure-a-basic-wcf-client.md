---
title: 'Comment : configurer un client Windows Communication Foundation de base'
ms.date: 09/14/2018
helpviewer_keywords:
- WCF clients [WCF], configuring
ms.assetid: d067b86d-afb0-47bf-94f6-45180a3d8d78
ms.openlocfilehash: 3f267edf87711de8a5969e3e0b577648008c5a75
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46562188"
---
# <a name="how-to-configure-a-basic-windows-communication-foundation-client"></a><span data-ttu-id="c9379-102">Comment : configurer un client Windows Communication Foundation de base</span><span class="sxs-lookup"><span data-stu-id="c9379-102">How to: Configure a Basic Windows Communication Foundation Client</span></span>

<span data-ttu-id="c9379-103">Il s’agit de la cinquième des six tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="c9379-103">This is the fifth of six tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="c9379-104">Pour une vue d’ensemble des six tâches, consultez la rubrique [Tutoriel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="c9379-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>

<span data-ttu-id="c9379-105">Cette rubrique décrit le fichier de configuration de client qui a été généré à l’aide de la **ajouter une référence de Service** des fonctionnalités de Visual Studio ou le [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span><span class="sxs-lookup"><span data-stu-id="c9379-105">This topic discusses the client configuration file that was generated using the **Add Service Reference** functionality of Visual Studio or the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md).</span></span> <span data-ttu-id="c9379-106">La configuration du client consiste à spécifier le point de terminaison que le client utilise pour accéder au service.</span><span class="sxs-lookup"><span data-stu-id="c9379-106">Configuring the client consists of specifying the endpoint that the client uses to access the service.</span></span> <span data-ttu-id="c9379-107">Un point de terminaison a une adresse, une liaison et un contrat, et chacun d'entre eux doit être spécifié en cours de la configuration du client.</span><span class="sxs-lookup"><span data-stu-id="c9379-107">An endpoint has an address, a binding, and a contract, and each of these must be specified in the process of configuring the client.</span></span>

## <a name="configure-a-windows-communication-foundation-client"></a><span data-ttu-id="c9379-108">Configurer un client Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="c9379-108">Configure a Windows Communication Foundation client</span></span>

<span data-ttu-id="c9379-109">Ouvrez le fichier de configuration généré (App.config) du projet GettingStartedClient.</span><span class="sxs-lookup"><span data-stu-id="c9379-109">Open the generated configuration file (App.config) from the GettingStartedClient project.</span></span> <span data-ttu-id="c9379-110">L'exemple suivant est une vue du fichier de configuration généré.</span><span class="sxs-lookup"><span data-stu-id="c9379-110">The following example is a view of the generated configuration file.</span></span> <span data-ttu-id="c9379-111">Sous le [ \<system.serviceModel >](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, recherchez le [ \<point de terminaison >](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) élément.</span><span class="sxs-lookup"><span data-stu-id="c9379-111">Under the [\<system.serviceModel>](../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md) section, find the [\<endpoint>](https://msdn.microsoft.com/library/13aa23b7-2f08-4add-8dbf-a99f8127c017) element.</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
          <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5,Profile=Client" />
        </startup>
        <system.serviceModel>
            <bindings>
                <!-- Uses wsHttpBinding-->
                <wsHttpBinding>
                    <binding name="WSHttpBinding_ICalculator" />
                </wsHttpBinding>
            </bindings>
            <client>
                <!-- specifies the endpoint to use when calling the service -->
                <endpoint address="http://localhost:8000/ServiceModelSamples/Service/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <userPrincipalName value="migree@redmond.corp.microsoft.com" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

<span data-ttu-id="c9379-112">Cet exemple configure le point de terminaison que le client utilise pour accéder au service qui se trouve à l’adresse suivante : `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="c9379-112">This example configures the endpoint that the client uses to access the service that is located at the following address: `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`.</span></span>

<span data-ttu-id="c9379-113">L'élément de point de terminaison spécifie que le contrat de service `ServiceReference1.ICalculator` est utilisé pour la communication entre le client et le service WCF.</span><span class="sxs-lookup"><span data-stu-id="c9379-113">The endpoint element specifies that the `ServiceReference1.ICalculator` service contract is used for communication between the WCF client and service.</span></span> <span data-ttu-id="c9379-114">Le canal WCF est configuré avec <xref:System.ServiceModel.WSHttpBinding> fourni par le système.</span><span class="sxs-lookup"><span data-stu-id="c9379-114">The WCF channel is configured with the system-provided <xref:System.ServiceModel.WSHttpBinding>.</span></span> <span data-ttu-id="c9379-115">Ce contrat a été généré à l’aide de **ajouter une référence de Service** dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c9379-115">This contract was generated by using **Add Service Reference** in Visual Studio.</span></span> <span data-ttu-id="c9379-116">Il s'agit essentiellement d'une copie du contrat défini dans le projet GettingStartedLib.</span><span class="sxs-lookup"><span data-stu-id="c9379-116">It is essentially a copy of the contract that was defined in the GettingStartedLib project.</span></span> <span data-ttu-id="c9379-117">La liaison <xref:System.ServiceModel.WSHttpBinding> spécifie le protocole HTTP pour le transport, la sécurité interopérable et d'autres détails de configuration.</span><span class="sxs-lookup"><span data-stu-id="c9379-117">The <xref:System.ServiceModel.WSHttpBinding> binding specifies HTTP as the transport, interoperable security, and other configuration details.</span></span>

<span data-ttu-id="c9379-118">Pour plus d’informations sur l’utilisation du client généré avec cette configuration, consultez [Comment : utiliser un Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span><span class="sxs-lookup"><span data-stu-id="c9379-118">For more information about how to use the generated client with this configuration, see [How to: Use a Client](../../../docs/framework/wcf/how-to-use-a-wcf-client.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="c9379-119">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="c9379-119">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="c9379-120">Comment : utiliser un client WCF</span><span class="sxs-lookup"><span data-stu-id="c9379-120">How to: Use a WCF client</span></span>](../../../docs/framework/wcf/how-to-use-a-wcf-client.md)

## <a name="see-also"></a><span data-ttu-id="c9379-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9379-121">See also</span></span>

- [<span data-ttu-id="c9379-122">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="c9379-122">Using Bindings to Configure Services and Clients</span></span>](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="c9379-123">Outil ServiceModel Metadata Utility (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="c9379-123">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="c9379-124">Guide pratique pour créer un client</span><span class="sxs-lookup"><span data-stu-id="c9379-124">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)
- [<span data-ttu-id="c9379-125">Prise en main</span><span class="sxs-lookup"><span data-stu-id="c9379-125">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)
- [<span data-ttu-id="c9379-126">Auto-hébergement</span><span class="sxs-lookup"><span data-stu-id="c9379-126">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)