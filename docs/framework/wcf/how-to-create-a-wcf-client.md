---
title: 'Tutoriel : Créer un client Windows Communication Foundation'
ms.date: 03/19/2019
helpviewer_keywords:
- clients [WCF], running
- WCF clients [WCF], running
ms.assetid: a67884cc-1c4b-416b-8c96-5c954099f19f
ms.openlocfilehash: a16a0ccabfd0f9fbe69db1ea88d4613185f3c1da
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59174367"
---
# <a name="tutorial-create-a-windows-communication-foundation-client"></a><span data-ttu-id="beaeb-102">Tutoriel : Créer un client Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="beaeb-102">Tutorial: Create a Windows Communication Foundation client</span></span>

<span data-ttu-id="beaeb-103">Ce didacticiel décrit la quatrième des cinq tâches requises pour créer une application Windows Communication Foundation (WCF) de base.</span><span class="sxs-lookup"><span data-stu-id="beaeb-103">This tutorial describes the fourth of five tasks required to create a basic Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="beaeb-104">Pour une vue d’ensemble des didacticiels, consultez [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="beaeb-104">For an overview of the tutorials, see [Tutorial: Get started with Windows Communication Foundation applications](getting-started-tutorial.md).</span></span>

<span data-ttu-id="beaeb-105">La tâche suivante pour créer une application WCF consiste à créer un client en récupérant des métadonnées à partir d’un service WCF.</span><span class="sxs-lookup"><span data-stu-id="beaeb-105">The next task for creating a WCF application is to create a client by retrieving metadata from a WCF service.</span></span> <span data-ttu-id="beaeb-106">Visual Studio vous permet d’ajouter une référence de service, qui obtient les métadonnées de point de terminaison MEX du service.</span><span class="sxs-lookup"><span data-stu-id="beaeb-106">You use Visual Studio to add a service reference, which gets the metadata from the service’s MEX endpoint.</span></span> <span data-ttu-id="beaeb-107">Visual Studio génère ensuite un fichier de code source managé pour un proxy de client dans la langue que vous avez choisie.</span><span class="sxs-lookup"><span data-stu-id="beaeb-107">Visual Studio then generates a managed source code file for a client proxy in the language you've chosen.</span></span> <span data-ttu-id="beaeb-108">Il crée également un fichier de configuration de client (*App.config*).</span><span class="sxs-lookup"><span data-stu-id="beaeb-108">It also creates a client configuration file (*App.config*).</span></span> <span data-ttu-id="beaeb-109">Ce fichier permet à l’application client pour se connecter au service à un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="beaeb-109">This file enables the client application to connect to the service at an endpoint.</span></span> 

> [!NOTE]
> <span data-ttu-id="beaeb-110">Si vous appelez un service WCF à partir d’un projet de bibliothèque de classes dans Visual Studio, utilisez le **ajouter une référence de Service** fonctionnalité pour générer automatiquement un proxy et un fichier de configuration associé.</span><span class="sxs-lookup"><span data-stu-id="beaeb-110">If you call a WCF service from a class library project in Visual Studio, use the **Add Service Reference** feature to automatically generate a proxy and associated configuration file.</span></span> <span data-ttu-id="beaeb-111">Toutefois, étant donné que les projets bibliothèque de classes n’utilisent pas ce fichier de configuration, vous devez ajouter les paramètres dans le fichier de configuration généré pour le *App.config* fichier pour le fichier exécutable qui appelle la bibliothèque de classes.</span><span class="sxs-lookup"><span data-stu-id="beaeb-111">However, because class library projects don't use this configuration file, you need to add the settings in the generated configuration file to the *App.config* file for the executable that calls the class library.</span></span>

> [!NOTE]
> <span data-ttu-id="beaeb-112">Comme alternative, utilisez la [outil ServiceModel Metadata Utility](#servicemodel-metadata-utility-tool) au lieu de Visual Studio pour générer le fichier de configuration et de la classe proxy.</span><span class="sxs-lookup"><span data-stu-id="beaeb-112">As an alternative, use the [ServiceModel Metadata Utility tool](#servicemodel-metadata-utility-tool) instead of Visual Studio to generate the proxy class and configuration file.</span></span>

<span data-ttu-id="beaeb-113">L'application cliente utilise la classe proxy générée pour communiquer avec le service.</span><span class="sxs-lookup"><span data-stu-id="beaeb-113">The client application uses the generated proxy class to communicate with the service.</span></span> <span data-ttu-id="beaeb-114">Cette procédure est décrite dans [didacticiel : Utiliser un client](how-to-use-a-wcf-client.md).</span><span class="sxs-lookup"><span data-stu-id="beaeb-114">This procedure is described in [Tutorial: Use a client](how-to-use-a-wcf-client.md).</span></span>

<span data-ttu-id="beaeb-115">Dans ce didacticiel, vous apprendrez à :</span><span class="sxs-lookup"><span data-stu-id="beaeb-115">In this tutorial, you learn how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="beaeb-116">Créez et configurez un projet d’application console pour le client WCF.</span><span class="sxs-lookup"><span data-stu-id="beaeb-116">Create and configure a console app project for the WCF client.</span></span>
> - <span data-ttu-id="beaeb-117">Ajouter une référence de service au service WCF pour générer les fichiers de configuration et de la classe proxy.</span><span class="sxs-lookup"><span data-stu-id="beaeb-117">Add a service reference to the WCF service to generate the proxy class and configuration files.</span></span>

## <a name="create-a-windows-communication-foundation-client"></a><span data-ttu-id="beaeb-118">Créer un client Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="beaeb-118">Create a Windows Communication Foundation client</span></span>

1. <span data-ttu-id="beaeb-119">Créer un projet d’application console dans Visual Studio :</span><span class="sxs-lookup"><span data-stu-id="beaeb-119">Create a console app project in Visual Studio:</span></span> 

    1. <span data-ttu-id="beaeb-120">À partir de la **fichier** menu, sélectionnez **Open** > **projet/Solution** et accédez à la **GettingStarted** solution vous créé précédemment (*GettingStarted.sln*).</span><span class="sxs-lookup"><span data-stu-id="beaeb-120">From the **File** menu, select **Open** > **Project/Solution** and browse to the **GettingStarted** solution you previously created (*GettingStarted.sln*).</span></span> <span data-ttu-id="beaeb-121">Sélectionnez **Ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-121">Select **Open**.</span></span>

    2. <span data-ttu-id="beaeb-122">À partir de la **vue** menu, sélectionnez **l’Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-122">From the **View** menu, select **Solution Explorer**.</span></span>

    3. <span data-ttu-id="beaeb-123">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStarted** solution (nœud supérieur) et sélectionnez **ajouter** > **denouveauprojet** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="beaeb-123">In the **Solution Explorer** window, select the **GettingStarted** solution (top node), and then select **Add** > **New Project** from the shortcut menu.</span></span> 
    
    4. <span data-ttu-id="beaeb-124">Dans le **ajouter un nouveau projet** fenêtre, sur le côté gauche, sélectionnez le **Windows Desktop** catégorie sous **Visual C#**  ou **Visual Basic**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-124">In the **Add New Project** window, on the left side, select the **Windows Desktop** category under **Visual C#** or **Visual Basic**.</span></span> 

    5. <span data-ttu-id="beaeb-125">Sélectionnez le **application Console (.NET Framework)** modèle, puis entrez *GettingStartedClient* pour le **nom**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-125">Select the **Console App (.NET Framework)** template, and enter *GettingStartedClient* for the **Name**.</span></span> <span data-ttu-id="beaeb-126">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-126">Select **OK**.</span></span>

2. <span data-ttu-id="beaeb-127">Ajouter une référence dans le **GettingStartedClient** de projet pour le <xref:System.ServiceModel> assembly :</span><span class="sxs-lookup"><span data-stu-id="beaeb-127">Add a reference in the **GettingStartedClient** project to the <xref:System.ServiceModel> assembly:</span></span> 

    1.  <span data-ttu-id="beaeb-128">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedClient** de projet, puis sélectionnez **ajouter une référence** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="beaeb-128">In the **Solution Explorer** window, select the **References** folder under the **GettingStartedClient** project, and then select **Add Reference** from the shortcut menu.</span></span> 

    2. <span data-ttu-id="beaeb-129">Dans le **ajouter une référence** fenêtre, sous **assemblys** sur le côté gauche de la fenêtre, sélectionnez **Framework**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-129">In the **Add Reference** window, under **Assemblies** on the left side of the window, select **Framework**.</span></span>
    
    3. <span data-ttu-id="beaeb-130">Recherchez et sélectionnez **System.ServiceModel**, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-130">Find and select **System.ServiceModel**, and then choose **OK**.</span></span> 

    4. <span data-ttu-id="beaeb-131">Enregistrez la solution en sélectionnant **fichier** > **Enregistrer tout**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-131">Save the solution by selecting **File** > **Save All**.</span></span>

3. <span data-ttu-id="beaeb-132">Ajoutez une référence de service pour le service de calculatrice :</span><span class="sxs-lookup"><span data-stu-id="beaeb-132">Add a service reference to the calculator service:</span></span>

   1. <span data-ttu-id="beaeb-133">Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **références** dossier sous le **GettingStartedClient** de projet, puis sélectionnez **ajouter une référence de Service**  dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="beaeb-133">In the **Solution Explorer** window, select the **References** folder under the **GettingStartedClient** project, and then select **Add Service Reference** from the shortcut menu.</span></span>

   2. <span data-ttu-id="beaeb-134">Dans le **ajouter une référence de Service** fenêtre, sélectionnez **Discover**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-134">In the **Add Service Reference** window, select **Discover**.</span></span>

      <span data-ttu-id="beaeb-135">Le CalculatorService service démarre et que Visual Studio affiche dans le **Services** boîte.</span><span class="sxs-lookup"><span data-stu-id="beaeb-135">The CalculatorService service starts and Visual Studio displays it in the **Services** box.</span></span>

   3. <span data-ttu-id="beaeb-136">Sélectionnez **CalculatorService** pour le développer et afficher les contrats de service implémentés par le service.</span><span class="sxs-lookup"><span data-stu-id="beaeb-136">Select **CalculatorService** to expand it and display the service contracts implemented by the service.</span></span> <span data-ttu-id="beaeb-137">Laissez la valeur par défaut **Namespace** et choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="beaeb-137">Leave the default **Namespace** and choose **OK**.</span></span>

      <span data-ttu-id="beaeb-138">Visual Studio ajoute un nouvel élément sous le **Services connectés** dossier dans le **GettingStartedClient** projet.</span><span class="sxs-lookup"><span data-stu-id="beaeb-138">Visual Studio adds a new item under the **Connected Services** folder in the **GettingStartedClient** project.</span></span> 

### <a name="servicemodel-metadata-utility-tool"></a><span data-ttu-id="beaeb-139">Outil ServiceModel Metadata Utility</span><span class="sxs-lookup"><span data-stu-id="beaeb-139">ServiceModel Metadata Utility tool</span></span>

<span data-ttu-id="beaeb-140">Les exemples suivants montrent comment utiliser éventuellement le [ServiceModel Metadata Utility tool (Svcutil.exe)](servicemodel-metadata-utility-tool-svcutil-exe.md) pour générer le fichier de classe proxy.</span><span class="sxs-lookup"><span data-stu-id="beaeb-140">The following examples show how to optionally use the [ServiceModel Metadata Utility tool (Svcutil.exe)](servicemodel-metadata-utility-tool-svcutil-exe.md) to generate the proxy class file.</span></span> <span data-ttu-id="beaeb-141">Cet outil génère le fichier de classe de proxy et le *App.config* fichier.</span><span class="sxs-lookup"><span data-stu-id="beaeb-141">This tool generates the proxy class file and the *App.config* file.</span></span> <span data-ttu-id="beaeb-142">Les exemples suivants montrent comment générer le proxy dans C# et Visual Basic, respectivement :</span><span class="sxs-lookup"><span data-stu-id="beaeb-142">The following examples show how to generate the proxy in C# and Visual Basic, respectively:</span></span>

```shell
svcutil.exe /language:cs /out:generatedProxy.cs /config:app.config http://localhost:8000/GettingStarted/CalculatorService
```

```shell
svcutil.exe /language:vb /out:generatedProxy.vb /config:app.config http://localhost:8000/GettingStarted/CalculatorService
```

### <a name="client-configuration-file"></a><span data-ttu-id="beaeb-143">Fichier de configuration client</span><span class="sxs-lookup"><span data-stu-id="beaeb-143">Client configuration file</span></span>

<span data-ttu-id="beaeb-144">Une fois que vous avez créé le client, Visual Studio crée le **App.config** fichier de configuration dans le **GettingStartedClient** projet, qui doit être similaire à l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="beaeb-144">After you've created the client, Visual Studio creates the **App.config** configuration file in the **GettingStartedClient** project, which should be similar to the following example:</span></span>

```xml
    <?xml version="1.0" encoding="utf-8" ?>
    <configuration>
        <startup>
            <!-- specifies the version of WCF to use-->
            <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.6.1" />
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
                <endpoint address="http://localhost:8000/GettingStarted/CalculatorService"
                    binding="wsHttpBinding" bindingConfiguration="WSHttpBinding_ICalculator"
                    contract="ServiceReference1.ICalculator" name="WSHttpBinding_ICalculator">
                    <identity>
                        <dns value="localhost" />
                    </identity>
                </endpoint>
            </client>
        </system.serviceModel>
    </configuration>
```

<span data-ttu-id="beaeb-145">Sous le [ \<system.serviceModel >](../configure-apps/file-schema/wcf/system-servicemodel.md) section, notez le [ \<point de terminaison >](../configure-apps/file-schema/wcf/endpoint-element.md) élément.</span><span class="sxs-lookup"><span data-stu-id="beaeb-145">Under the [\<system.serviceModel>](../configure-apps/file-schema/wcf/system-servicemodel.md) section, notice the [\<endpoint>](../configure-apps/file-schema/wcf/endpoint-element.md) element.</span></span> <span data-ttu-id="beaeb-146">Le **&lt;point de terminaison&gt;** élément définit le point de terminaison que le client utilise pour accéder au service comme suit :</span><span class="sxs-lookup"><span data-stu-id="beaeb-146">The **&lt;endpoint&gt;** element defines the endpoint that the client uses to access the service as follows:</span></span>
- <span data-ttu-id="beaeb-147">Adresse : `http://localhost:8000/GettingStarted/CalculatorService`.</span><span class="sxs-lookup"><span data-stu-id="beaeb-147">Address: `http://localhost:8000/GettingStarted/CalculatorService`.</span></span> <span data-ttu-id="beaeb-148">Adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="beaeb-148">The address of the endpoint.</span></span>
- <span data-ttu-id="beaeb-149">Contrat de service : `ServiceReference1.ICalculator`.</span><span class="sxs-lookup"><span data-stu-id="beaeb-149">Service contract: `ServiceReference1.ICalculator`.</span></span> <span data-ttu-id="beaeb-150">Le contrat de service gère la communication entre le client WCF et le service.</span><span class="sxs-lookup"><span data-stu-id="beaeb-150">The service contract handles communication between the WCF client and the service.</span></span> <span data-ttu-id="beaeb-151">Visual Studio a généré ce contrat lorsque vous avez utilisé son **ajouter une référence de Service** (fonction).</span><span class="sxs-lookup"><span data-stu-id="beaeb-151">Visual Studio generated this contract when you used its **Add Service Reference** function.</span></span> <span data-ttu-id="beaeb-152">Il est en fait une copie du contrat que vous avez défini dans le projet GettingStartedLib.</span><span class="sxs-lookup"><span data-stu-id="beaeb-152">It's essentially a copy of the contract that you defined in the GettingStartedLib project.</span></span> 
- <span data-ttu-id="beaeb-153">Liaison : <xref:System.ServiceModel.WSHttpBinding>.</span><span class="sxs-lookup"><span data-stu-id="beaeb-153">Binding: <xref:System.ServiceModel.WSHttpBinding>.</span></span> <span data-ttu-id="beaeb-154">La liaison spécifie le protocole HTTP comme transport, sécurité interopérable et d’autres détails de configuration.</span><span class="sxs-lookup"><span data-stu-id="beaeb-154">The binding specifies HTTP as the transport, interoperable security, and other configuration details.</span></span>

## <a name="next-steps"></a><span data-ttu-id="beaeb-155">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="beaeb-155">Next steps</span></span>

<span data-ttu-id="beaeb-156">Dans ce didacticiel, vous avez appris à :</span><span class="sxs-lookup"><span data-stu-id="beaeb-156">In this tutorial, you learned how to:</span></span>
> [!div class="checklist"]
> - <span data-ttu-id="beaeb-157">Créez et configurez un projet d’application console pour le client WCF.</span><span class="sxs-lookup"><span data-stu-id="beaeb-157">Create and configure a console app project for the WCF client.</span></span>
> - <span data-ttu-id="beaeb-158">Ajouter une référence de service au service WCF pour générer les fichiers de configuration et de la classe proxy pour l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="beaeb-158">Add a service reference to the WCF service to generate the proxy class and configuration files for the client application.</span></span>

<span data-ttu-id="beaeb-159">Passez au didacticiel suivant pour apprendre à utiliser le client généré.</span><span class="sxs-lookup"><span data-stu-id="beaeb-159">Advance to the next tutorial to learn how to use the generated client.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="beaeb-160">Tutoriel : Utiliser un client WCF</span><span class="sxs-lookup"><span data-stu-id="beaeb-160">Tutorial: Use a WCF client</span></span>](how-to-use-a-wcf-client.md)
