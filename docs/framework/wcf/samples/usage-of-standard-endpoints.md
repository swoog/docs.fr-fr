---
title: Utilisation de points de terminaison standard
ms.date: 03/30/2017
ms.assetid: ecd6a62f-9619-4778-a497-6f888087a9ea
ms.openlocfilehash: 4ef0714acad12db1414e34fbb476b4ae7d1d9fb2
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59304608"
---
# <a name="usage-of-standard-endpoints"></a><span data-ttu-id="da2ee-102">Utilisation de points de terminaison standard</span><span class="sxs-lookup"><span data-stu-id="da2ee-102">Usage of Standard Endpoints</span></span>

<span data-ttu-id="da2ee-103">Cet exemple montre comment utiliser des points de terminaison standard dans des fichiers de configuration de service.</span><span class="sxs-lookup"><span data-stu-id="da2ee-103">This sample demonstrates how to use standard endpoints in service configuration files.</span></span> <span data-ttu-id="da2ee-104">Un point de terminaison standard permet à l’utilisateur de simplifier des définitions de point de terminaison en utilisant une propriété unique pour décrire une combinaison adresse, liaison et contrat avec les propriétés supplémentaires qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="da2ee-104">A standard endpoint allows the user to simplify endpoint definitions by using a single property to describe an address, binding and contract combination with additional properties associated to it.</span></span> <span data-ttu-id="da2ee-105">Cet exemple montre comment définir et implémenter un point de terminaison standard personnalisé et comment définir des propriétés spécifiques dans le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="da2ee-105">This sample demonstrates how to define and implement a custom standard endpoint and how to define specific properties in the endpoint.</span></span>

## <a name="sample-details"></a><span data-ttu-id="da2ee-106">Détails de l'exemple</span><span class="sxs-lookup"><span data-stu-id="da2ee-106">Sample Details</span></span>

<span data-ttu-id="da2ee-107">Les points de terminaison de service peuvent être spécifiés en fournissant trois paramètres : adresse, liaison et contrat.</span><span class="sxs-lookup"><span data-stu-id="da2ee-107">Service endpoints can be specified by supplying three parameters: address, binding and contract.</span></span> <span data-ttu-id="da2ee-108">D'autres paramètres peuvent être fournis : configuration du comportement, en-têtes, URI d'écoute, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="da2ee-108">Other parameters that can be supplied include behavior configuration, headers, listen URI, and so on.</span></span> <span data-ttu-id="da2ee-109">Il peut arriver que certains ou l’ensemble des adresses, liaisons et contrats aient des valeurs qui ne peuvent pas changer.</span><span class="sxs-lookup"><span data-stu-id="da2ee-109">In some cases, any or all of addresses, bindings and contracts have values that cannot change.</span></span> <span data-ttu-id="da2ee-110">C'est pourquoi il est possible d'utiliser des points de terminaison standard.</span><span class="sxs-lookup"><span data-stu-id="da2ee-110">For this reason, it is possible to use standard endpoints.</span></span> <span data-ttu-id="da2ee-111">Les points de terminaison d'échange de métadonnées et de découverte en sont des exemples.</span><span class="sxs-lookup"><span data-stu-id="da2ee-111">Some examples of such endpoints include metadata exchange endpoints and discovery endpoints.</span></span> <span data-ttu-id="da2ee-112">Les points de terminaison standard facilitent également l'utilisation en autorisant la configuration de points de terminaison de service sans avoir à fournir des informations d'une nature fixe ou à créer leurs propres points de terminaison standard, afin, par exemple, de faciliter l'utilisation en fournissant un jeu raisonnable de valeurs par défaut, ce qui réduit les commentaires des fichiers de configuration.</span><span class="sxs-lookup"><span data-stu-id="da2ee-112">Standard endpoints also improve usability by allowing configuration of service endpoints without having to provide information of a fixed nature or to create their own standard endpoints, for example to improve usability by supplying a reasonable set of default values and thus reducing the verbosity of configuration files.</span></span>

<span data-ttu-id="da2ee-113">Cet exemple se compose de deux projets : le service qui définit deux points de terminaison standard et le client qui communique avec ce service.</span><span class="sxs-lookup"><span data-stu-id="da2ee-113">This sample consists of two projects: the service that defines two standard endpoints and the client that communicates with the service.</span></span> <span data-ttu-id="da2ee-114">La façon dont les points de terminaison standard du service sont définis dans le fichier de configuration est illustrée dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="da2ee-114">The way the standard endpoints are defined for the service in the configuration file is show in the following example.</span></span>

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <system.serviceModel>
    <extensions>
      <endpointExtensions>
        <add name="customEndpoint" type="Microsoft.Samples.StandardEndpoints.CustomEndpointCollectionElement, service" />
      </endpointExtensions>
    </extensions>
    <services>
      <service name="Microsoft.Samples.StandardEndpoints.CalculatorService">
        <endpoint address="http://localhost:8000/Samples/Service.svc/customEndpoint" contract="Microsoft.Samples.StandardEndpoints.ICalculator" kind="customEndpoint" />
        <endpoint kind="mexEndpoint" />
      </service>
    </services>
    <behaviors>
      <serviceBehaviors>
        <behavior>
          <serviceMetadata httpGetEnabled="True"/>
        </behavior>
      </serviceBehaviors>
    </behaviors>
    <standardEndpoints>
      <customEndpoint>
        <standardEndpoint property="True" />
      </customEndpoint>
    </standardEndpoints>
  </system.serviceModel>
</configuration>
```

<span data-ttu-id="da2ee-115">Le premier point de terminaison défini pour le service est du genre `customEndpoint` (dont la définition est visible dans la section `<standardEndpoints>`) où la valeur `property` est affectée à la propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="da2ee-115">The first endpoint defined for the service is of kind `customEndpoint`, whose definition can be seen in the `<standardEndpoints>` section, in which the property `property` is given the value `true`.</span></span> <span data-ttu-id="da2ee-116">C'est le cas d'un point de terminaison personnalisé avec une nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="da2ee-116">This is the case of an endpoint customized with a new property.</span></span> <span data-ttu-id="da2ee-117">Le deuxième point de terminaison correspond à un point de terminaison de métadonnées, où les valeurs d’adresse, de liaison et de contrat sont fixes.</span><span class="sxs-lookup"><span data-stu-id="da2ee-117">The second endpoint corresponds to a metadata endpoint, in which the values for address, binding and contract are fixed.</span></span>

<span data-ttu-id="da2ee-118">Pour définir l'élément du point de terminaison standard, une classe qui dérive de `StandardEndpointElement` doit être créée.</span><span class="sxs-lookup"><span data-stu-id="da2ee-118">To define the standard endpoint element, a class that derives from `StandardEndpointElement` must be created.</span></span> <span data-ttu-id="da2ee-119">Dans le cas de cet exemple, la classe `CustomEndpointElement` a été définie comme indiqué dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="da2ee-119">In the case of this sample, the `CustomEndpointElement` class has been defined as shown in the following example.</span></span>

```csharp
public class CustomEndpointElement : StandardEndpointElement
{
    public bool Property
    {
        get { return (bool)base["property"]; }
        set { base["property"] = value; }
    }

    protected override ConfigurationPropertyCollection Properties
    {
        get
        {
            ConfigurationPropertyCollection properties = base.Properties;
            properties.Add(new ConfigurationProperty("property", typeof(bool), false, ConfigurationPropertyOptions.None));
            return properties;
        }
    }

    protected override Type EndpointType
    {
        get { return typeof(CustomEndpoint); }
    }

    protected override ServiceEndpoint CreateServiceEndpoint(ContractDescription contract)
    {
        return new CustomEndpoint();
    }

    protected override void OnApplyConfiguration(ServiceEndpoint endpoint, ServiceEndpointElement serviceEndpointElement)
    {
        CustomEndpoint customEndpoint = (CustomEndpoint)endpoint;
        customEndpoint.Property = this.Property;
    }

    protected override void OnApplyConfiguration(ServiceEndpoint endpoint, ChannelEndpointElement channelEndpointElement)
    {
        CustomEndpoint customEndpoint = (CustomEndpoint)endpoint;
        customEndpoint.Property = this.Property;
    }

    protected override void OnInitializeAndValidate(ServiceEndpointElement serviceEndpointElement)
    {
    }

    protected override void OnInitializeAndValidate(ChannelEndpointElement channelEndpointElement)
    {
    }
}
```

<span data-ttu-id="da2ee-120">Dans la fonction `CreateServiceEndpoint`, un objet `CustomEndpoint` est créé.</span><span class="sxs-lookup"><span data-stu-id="da2ee-120">In the `CreateServiceEndpoint` function, a `CustomEndpoint` object is created.</span></span> <span data-ttu-id="da2ee-121">Sa définition est illustrée dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="da2ee-121">Its definition is shown in the following example:</span></span>

```csharp
public class CustomEndpoint : ServiceEndpoint
{
    public CustomEndpoint()
        : this(string.Empty)
    {
    }

    public CustomEndpoint(string address)
        : this(address, ContractDescription.GetContract(typeof(ICalculator)))
    {
    }

    public CustomEndpoint(string address, ContractDescription contract)
        : base(contract)
    {
        this.Binding = new BasicHttpBinding();
        this.IsSystemEndpoint = false;
    }

    public bool Property
    {
        get;
        set;
    }
}
```

 <span data-ttu-id="da2ee-122">Pour permettre la communication entre service et client, une référence au service est créée dans le client.</span><span class="sxs-lookup"><span data-stu-id="da2ee-122">To perform the communication between service and client, a service reference is created in the client to the service.</span></span> <span data-ttu-id="da2ee-123">Lorsque l'exemple est généré et exécuté, le service s'exécute et le client communique avec lui.</span><span class="sxs-lookup"><span data-stu-id="da2ee-123">When the sample is built and executed, the service executes and the client communicates with it.</span></span> <span data-ttu-id="da2ee-124">Notez que la référence de service doit être mise à jour à chaque modification du service.</span><span class="sxs-lookup"><span data-stu-id="da2ee-124">Note that the service reference should be updated every time there is some change in the service.</span></span>

#### <a name="to-use-this-sample"></a><span data-ttu-id="da2ee-125">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="da2ee-125">To use this sample</span></span>

1. <span data-ttu-id="da2ee-126">À l’aide de Visual Studio 2012, ouvrez le fichier StandardEndpoints.sln.</span><span class="sxs-lookup"><span data-stu-id="da2ee-126">Using Visual Studio 2012, open the StandardEndpoints.sln file.</span></span>

2. <span data-ttu-id="da2ee-127">Permettez à plusieurs projets de démarrer.</span><span class="sxs-lookup"><span data-stu-id="da2ee-127">Enable multiple projects to start up.</span></span>

    1.  <span data-ttu-id="da2ee-128">Dans **l’Explorateur de solutions**, avec le bouton droit de la solution de points de terminaison Standard, puis sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="da2ee-128">In **Solution Explorer**, right-click the Standard Endpoints solution and then select **Properties**.</span></span>

    2.  <span data-ttu-id="da2ee-129">Dans **propriétés communes**, sélectionnez **projet de démarrage**, puis cliquez sur **plusieurs projets de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="da2ee-129">In **Common Properties**, select **Startup Project**, and then click **Multiple Startup Projects**.</span></span>

    3.  <span data-ttu-id="da2ee-130">Déplacer le projet de Service au début de la liste, avec la **Action** définie sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="da2ee-130">Move the Service project to the beginning of the list, with the **Action** set to **Start**.</span></span>

    4.  <span data-ttu-id="da2ee-131">Déplacer le projet Client après le projet de Service, également avec la **Action** définie sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="da2ee-131">Move the Client project after the Service project, also with the **Action** set to **Start**.</span></span>

         <span data-ttu-id="da2ee-132">De cette façon, le projet Client est exécuté après le projet Service.</span><span class="sxs-lookup"><span data-stu-id="da2ee-132">This specifies that the Client project is executed after the Service project.</span></span>

3. <span data-ttu-id="da2ee-133">Pour exécuter la solution, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="da2ee-133">To run the solution, press F5.</span></span>

> [!NOTE]
> <span data-ttu-id="da2ee-134">Si ces étapes ne fonctionnent pas, assurez-vous que votre environnement a été correctement configuré, en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="da2ee-134">If these steps don't work, then make sure that your environment has been properly set up, using the following steps:</span></span>
>
> 1. <span data-ttu-id="da2ee-135">Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="da2ee-135">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>
> 2. <span data-ttu-id="da2ee-136">Pour générer la solution, suivez les instructions de [génération des exemples Windows Communication Foundation](building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="da2ee-136">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>
> 3. <span data-ttu-id="da2ee-137">Pour exécuter l’exemple dans un seul ou plusieurs configurations d’ordinateur, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="da2ee-137">To run the sample in a single or multiple computer configurations, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da2ee-138">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="da2ee-138">The samples may already be installed on your machine.</span></span> <span data-ttu-id="da2ee-139">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="da2ee-139">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="da2ee-140">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="da2ee-140">If this directory doesn't exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="da2ee-141">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="da2ee-141">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Services\StandardEndpoints`
