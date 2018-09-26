---
title: 'Comment : héberger un service WCF dans une application managée'
ms.date: 09/17/2018
dev_langs:
- csharp
- vb
ms.assetid: 5eb29db0-b6dc-4e77-8c68-0a62f79d743b
ms.openlocfilehash: 131d99457427e0818f78076d987f550a99ad7cf0
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47196848"
---
# <a name="how-to-host-a-wcf-service-in-a-managed-app"></a><span data-ttu-id="7a46e-102">Comment : héberger un service WCF dans une application gérée</span><span class="sxs-lookup"><span data-stu-id="7a46e-102">How to: Host a WCF service in a managed app</span></span>

<span data-ttu-id="7a46e-103">Pour héberger un service à l'intérieur d'une application managée, incorporez le code du service à l'intérieur du code de l'application managée, définissez un point de terminaison pour le service soit de manière impérative dans le code, soit de façon déclarative par le biais de la configuration ou à l'aide des points de terminaison par défaut, puis créez une instance de <xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="7a46e-103">To host a service inside a managed application, embed the code for the service inside the managed application code, define an endpoint for the service either imperatively in code, declaratively through configuration, or using default endpoints, and then create an instance of <xref:System.ServiceModel.ServiceHost>.</span></span>

<span data-ttu-id="7a46e-104">Pour commencer à recevoir des messages, appelez <xref:System.ServiceModel.ICommunicationObject.Open%2A><xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="7a46e-104">To start receiving messages, call <xref:System.ServiceModel.ICommunicationObject.Open%2A> on <xref:System.ServiceModel.ServiceHost>.</span></span> <span data-ttu-id="7a46e-105">De cette manière, vous créez et ouvrez l'écouteur pour le service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-105">This creates and opens the listener for the service.</span></span> <span data-ttu-id="7a46e-106">L'hébergement d'un service selon cette méthode est souvent appelé « auto-hébergement » parce que l'application managée effectue le travail d'hébergement elle-même.</span><span class="sxs-lookup"><span data-stu-id="7a46e-106">Hosting a service in this way is often referred to as "self-hosting" because the managed application is doing the hosting work itself.</span></span> <span data-ttu-id="7a46e-107">Pour fermer le service, appelez <xref:System.ServiceModel.Channels.CommunicationObject.Close%2A?displayProperty=nameWithType> sur <xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="7a46e-107">To close the service, call <xref:System.ServiceModel.Channels.CommunicationObject.Close%2A?displayProperty=nameWithType> on <xref:System.ServiceModel.ServiceHost>.</span></span>

<span data-ttu-id="7a46e-108">Un service peut également être hébergé dans un service Windows managé, dans le service IIS (Internet Information Services), ou le service WAS (Windows Process Activation Service).</span><span class="sxs-lookup"><span data-stu-id="7a46e-108">A service can also be hosted in a managed Windows service, in Internet Information Services (IIS), or in Windows Process Activation Service (WAS).</span></span> <span data-ttu-id="7a46e-109">Pour plus d’informations sur les options pour un service d’hébergement, consultez [Services d’hébergement](../../../docs/framework/wcf/hosting-services.md).</span><span class="sxs-lookup"><span data-stu-id="7a46e-109">For more information about hosting options for a service, see [Hosting Services](../../../docs/framework/wcf/hosting-services.md).</span></span>

<span data-ttu-id="7a46e-110">L'hébergement d'un service dans une application managée constitue l'option d'hébergement la plus flexible parce qu'il requiert le déploiement de moins d'infrastructure.</span><span class="sxs-lookup"><span data-stu-id="7a46e-110">Hosting a service in a managed application is the most flexible option because it requires the least infrastructure to deploy.</span></span> <span data-ttu-id="7a46e-111">Pour plus d’informations sur l’hébergement de services dans les applications managées, consultez [hébergement dans une Application gérée par](../../../docs/framework/wcf/feature-details/hosting-in-a-managed-application.md).</span><span class="sxs-lookup"><span data-stu-id="7a46e-111">For more information about hosting services in managed applications, see [Hosting in a Managed Application](../../../docs/framework/wcf/feature-details/hosting-in-a-managed-application.md).</span></span>

<span data-ttu-id="7a46e-112">La procédure suivante montre comment implémenter un service auto-hébergé dans une application console.</span><span class="sxs-lookup"><span data-stu-id="7a46e-112">The following procedure demonstrates how to implement a self-hosted service in a console application.</span></span>

## <a name="create-a-self-hosted-service"></a><span data-ttu-id="7a46e-113">Créer un service auto-hébergé</span><span class="sxs-lookup"><span data-stu-id="7a46e-113">Create a self-hosted service</span></span>

1. <span data-ttu-id="7a46e-114">Créer une nouvelle application de console :</span><span class="sxs-lookup"><span data-stu-id="7a46e-114">Create a new console application:</span></span>

   1. <span data-ttu-id="7a46e-115">Ouvrez Visual Studio et sélectionnez **New** > **projet** à partir de la **fichier** menu.</span><span class="sxs-lookup"><span data-stu-id="7a46e-115">Open Visual Studio and select **New** > **Project** from the **File** menu.</span></span>

   2. <span data-ttu-id="7a46e-116">Dans le **modèles installés** liste, sélectionnez **Visual C#** ou **Visual Basic**, puis sélectionnez **Windows Desktop**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-116">In the **Installed Templates** list, select **Visual C#** or **Visual Basic**, and then select **Windows Desktop**.</span></span>

   3. <span data-ttu-id="7a46e-117">Sélectionnez le **application Console** modèle.</span><span class="sxs-lookup"><span data-stu-id="7a46e-117">Select the **Console App** template.</span></span> <span data-ttu-id="7a46e-118">Type `SelfHost` dans le **nom** zone, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-118">Type `SelfHost` in the **Name** box and then choose **OK**.</span></span>

2. <span data-ttu-id="7a46e-119">Avec le bouton droit **SelfHost** dans **l’Explorateur de solutions** et sélectionnez **ajouter une référence**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-119">Right-click **SelfHost** in **Solution Explorer** and select **Add Reference**.</span></span> <span data-ttu-id="7a46e-120">Sélectionnez **System.ServiceModel** à partir de la **.NET** onglet, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-120">Select **System.ServiceModel** from the **.NET** tab and then choose **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="7a46e-121">Si le **l’Explorateur de solutions** fenêtre n’est pas visible, sélectionnez **l’Explorateur de solutions** à partir de la **vue** menu.</span><span class="sxs-lookup"><span data-stu-id="7a46e-121">If the **Solution Explorer** window is not visible, select **Solution Explorer** from the **View** menu.</span></span>

3. <span data-ttu-id="7a46e-122">Double-cliquez sur **Program.cs** ou **Module1.vb** dans **l’Explorateur de solutions** pour l’ouvrir dans la fenêtre de code, s’il n’est pas déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="7a46e-122">Double-click **Program.cs** or **Module1.vb** in **Solution Explorer** to open it in the code window, if it's not already open.</span></span> <span data-ttu-id="7a46e-123">Ajoutez les instructions suivantes en haut du fichier :</span><span class="sxs-lookup"><span data-stu-id="7a46e-123">Add the following statements at the top of the file:</span></span>

     [!code-csharp[CFX_SelfHost4#1](../../../samples/snippets/csharp/VS_Snippets_CFX/cfx_selfhost4/cs/program.cs#1)]
     [!code-vb[CFX_SelfHost4#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/cfx_selfhost4/vb/module1.vb#1)]

4. <span data-ttu-id="7a46e-124">Définissez et implémentez un contrat de service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-124">Define and implement a service contract.</span></span> <span data-ttu-id="7a46e-125">Cet exemple définit un `HelloWorldService` qui retourne un message basé sur l'entrée au service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-125">This example defines a `HelloWorldService` that returns a message based on the input to the service.</span></span>

     [!code-csharp[CFX_SelfHost4#2](../../../samples/snippets/csharp/VS_Snippets_CFX/cfx_selfhost4/cs/program.cs#2)]
     [!code-vb[CFX_SelfHost4#2](../../../samples/snippets/visualbasic/VS_Snippets_CFX/cfx_selfhost4/vb/module1.vb#2)]

    > [!NOTE]
    > <span data-ttu-id="7a46e-126">Pour plus d’informations sur la façon de définir et implémenter une interface de service, consultez [Comment : définir un contrat de Service](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md) et [Comment : implémenter un contrat de Service](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md).</span><span class="sxs-lookup"><span data-stu-id="7a46e-126">For more information about how to define and implement a service interface, see [How to: Define a Service Contract](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md) and [How to: Implement a Service Contract](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md).</span></span>

5. <span data-ttu-id="7a46e-127">En tête de la méthode `Main`, créez une instance de la classe <xref:System.Uri> avec l'adresse de base du service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-127">At the top of the `Main` method, create an instance of the <xref:System.Uri> class with the base address for the service.</span></span>

     [!code-csharp[CFX_SelfHost4#3](../../../samples/snippets/csharp/VS_Snippets_CFX/cfx_selfhost4/cs/program.cs#3)]
     [!code-vb[CFX_SelfHost4#3](../../../samples/snippets/visualbasic/VS_Snippets_CFX/cfx_selfhost4/vb/module1.vb#3)]

6. <span data-ttu-id="7a46e-128">Créez une instance de la classe <xref:System.ServiceModel.ServiceHost>, en passant un <xref:System.Type> qui représente le type de service et l'URI d'adresse de base (Uniform Resource Identifier) à <xref:System.ServiceModel.ServiceHost.%23ctor%28System.Type%2CSystem.Uri%5B%5D%29>.</span><span class="sxs-lookup"><span data-stu-id="7a46e-128">Create an instance of the <xref:System.ServiceModel.ServiceHost> class, passing a <xref:System.Type> that represents the service type and the base address Uniform Resource Identifier (URI) to the <xref:System.ServiceModel.ServiceHost.%23ctor%28System.Type%2CSystem.Uri%5B%5D%29>.</span></span> <span data-ttu-id="7a46e-129">Activez la publication des métadonnées, puis appelez la méthode <xref:System.ServiceModel.ICommunicationObject.Open%2A> sur <xref:System.ServiceModel.ServiceHost> pour initialiser le service et le préparer à recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="7a46e-129">Enable metadata publishing, and then call the <xref:System.ServiceModel.ICommunicationObject.Open%2A> method on the <xref:System.ServiceModel.ServiceHost> to initialize the service and prepare it to receive messages.</span></span>

     [!code-csharp[CFX_SelfHost4#4](../../../samples/snippets/csharp/VS_Snippets_CFX/cfx_selfhost4/cs/program.cs#4)]
     [!code-vb[CFX_SelfHost4#4](../../../samples/snippets/visualbasic/VS_Snippets_CFX/cfx_selfhost4/vb/module1.vb#4)]

    > [!NOTE]
    > <span data-ttu-id="7a46e-130">Cet exemple utilise les points de terminaison par défaut et aucun fichier de configuration n'est requis pour ce service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-130">This example uses default endpoints, and no configuration file is required for this service.</span></span> <span data-ttu-id="7a46e-131">Si aucun point de terminaison n'est configuré, le runtime en crée un pour chaque adresse de base pour chaque contrat de service implémenté par le service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-131">If no endpoints are configured, then the runtime creates one endpoint for each base address for each service contract implemented by the service.</span></span> <span data-ttu-id="7a46e-132">Pour plus d’informations sur les points de terminaison par défaut, consultez [Simplified Configuration](../../../docs/framework/wcf/simplified-configuration.md) et [Simplified Configuration for WCF Services](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="7a46e-132">For more information about default endpoints, see [Simplified Configuration](../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>

7. <span data-ttu-id="7a46e-133">Appuyez sur **Ctrl**+**MAJ**+**B** pour générer la solution.</span><span class="sxs-lookup"><span data-stu-id="7a46e-133">Press **Ctrl**+**Shift**+**B** to build the solution.</span></span>

## <a name="test-the-service"></a><span data-ttu-id="7a46e-134">Tester le service</span><span class="sxs-lookup"><span data-stu-id="7a46e-134">Test the service</span></span>

1. <span data-ttu-id="7a46e-135">Appuyez sur **Ctrl**+**F5** pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="7a46e-135">Press **Ctrl**+**F5** to run the service.</span></span>

2. <span data-ttu-id="7a46e-136">Ouvrez **Client Test WCF**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-136">Open **WCF Test Client**.</span></span>

    > [!TIP]
    > <span data-ttu-id="7a46e-137">Pour ouvrir **Client Test WCF**, ouvrez l’invite de commandes développeur pour Visual Studio et exécutez **WcfTestClient.exe**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-137">To open **WCF Test Client**, open Developer Command Prompt for Visual Studio and execute **WcfTestClient.exe**.</span></span>

3. <span data-ttu-id="7a46e-138">Sélectionnez **ajouter un Service** à partir de la **fichier** menu.</span><span class="sxs-lookup"><span data-stu-id="7a46e-138">Select **Add Service** from the **File** menu.</span></span>

4. <span data-ttu-id="7a46e-139">Type `http://localhost:8080/hello` dans la zone d’adresse et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-139">Type `http://localhost:8080/hello` into the address box and click **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="7a46e-140">Assurez-vous que le service est en cours d'exécution, sinon cette étape échouera.</span><span class="sxs-lookup"><span data-stu-id="7a46e-140">Make sure the service is running or else this step fails.</span></span> <span data-ttu-id="7a46e-141">Si vous avez changé l'adresse de base dans le code, utilisez cette adresse modifiée dans cette étape.</span><span class="sxs-lookup"><span data-stu-id="7a46e-141">If you have changed the base address in the code, then use the modified base address in this step.</span></span>

5. <span data-ttu-id="7a46e-142">Double-cliquez sur **SayHello** sous le **Mes projets de Service** nœud.</span><span class="sxs-lookup"><span data-stu-id="7a46e-142">Double-click **SayHello** under the **My Service Projects** node.</span></span> <span data-ttu-id="7a46e-143">Tapez votre nom dans la **valeur** colonne dans le **demande** liste, puis cliquez sur **Invoke**.</span><span class="sxs-lookup"><span data-stu-id="7a46e-143">Type your name into the **Value** column in the **Request** list, and click **Invoke**.</span></span>

   <span data-ttu-id="7a46e-144">Un message de réponse s’affiche dans le **réponse** liste.</span><span class="sxs-lookup"><span data-stu-id="7a46e-144">A reply message appears in the **Response** list.</span></span>

## <a name="example"></a><span data-ttu-id="7a46e-145">Exemple</span><span class="sxs-lookup"><span data-stu-id="7a46e-145">Example</span></span>

<span data-ttu-id="7a46e-146">L'exemple suivant crée un objet <xref:System.ServiceModel.ServiceHost> pour héberger un service de type `HelloWorldService`, puis appelle la méthode <xref:System.ServiceModel.ICommunicationObject.Open%2A> sur <xref:System.ServiceModel.ServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="7a46e-146">The following example creates a <xref:System.ServiceModel.ServiceHost> object to host a service of type `HelloWorldService`, and then calls the <xref:System.ServiceModel.ICommunicationObject.Open%2A> method on <xref:System.ServiceModel.ServiceHost>.</span></span> <span data-ttu-id="7a46e-147">Une adresse de base est fournie dans le code, la publication des métadonnées est activée et les points de terminaison par défaut sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="7a46e-147">A base address is provided in code, metadata publishing is enabled, and default endpoints are used.</span></span>

[!code-csharp[CFX_SelfHost4#5](../../../samples/snippets/csharp/VS_Snippets_CFX/cfx_selfhost4/cs/program.cs#5)]
[!code-vb[CFX_SelfHost4#5](../../../samples/snippets/visualbasic/VS_Snippets_CFX/cfx_selfhost4/vb/module1.vb#5)]

## <a name="see-also"></a><span data-ttu-id="7a46e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a46e-148">See also</span></span>

- <xref:System.Uri>
- <xref:System.Configuration.ConfigurationManager.AppSettings%2A>
- <xref:System.Configuration.ConfigurationManager>
- [<span data-ttu-id="7a46e-149">How to: Host a WCF Service in IIS (Comment : héberger un service WCF dans IIS)</span><span class="sxs-lookup"><span data-stu-id="7a46e-149">How to: Host a WCF Service in IIS</span></span>](../../../docs/framework/wcf/feature-details/how-to-host-a-wcf-service-in-iis.md)
- [<span data-ttu-id="7a46e-150">Auto-hébergement</span><span class="sxs-lookup"><span data-stu-id="7a46e-150">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)
- [<span data-ttu-id="7a46e-151">Hébergement de services</span><span class="sxs-lookup"><span data-stu-id="7a46e-151">Hosting Services</span></span>](../../../docs/framework/wcf/hosting-services.md)
- [<span data-ttu-id="7a46e-152">Guide pratique pour définir un contrat de service</span><span class="sxs-lookup"><span data-stu-id="7a46e-152">How to: Define a Service Contract</span></span>](../../../docs/framework/wcf/how-to-define-a-wcf-service-contract.md)
- [<span data-ttu-id="7a46e-153">Guide pratique pour implémenter un contrat de service</span><span class="sxs-lookup"><span data-stu-id="7a46e-153">How to: Implement a Service Contract</span></span>](../../../docs/framework/wcf/how-to-implement-a-wcf-contract.md)
- [<span data-ttu-id="7a46e-154">Outil ServiceModel Metadata Utility (Svcutil.exe)</span><span class="sxs-lookup"><span data-stu-id="7a46e-154">ServiceModel Metadata Utility Tool (Svcutil.exe)</span></span>](../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
- [<span data-ttu-id="7a46e-155">Utilisation de liaisons pour configurer des services et des clients</span><span class="sxs-lookup"><span data-stu-id="7a46e-155">Using Bindings to Configure Services and Clients</span></span>](../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)
- [<span data-ttu-id="7a46e-156">Liaisons fournies par le système</span><span class="sxs-lookup"><span data-stu-id="7a46e-156">System-Provided Bindings</span></span>](../../../docs/framework/wcf/system-provided-bindings.md)