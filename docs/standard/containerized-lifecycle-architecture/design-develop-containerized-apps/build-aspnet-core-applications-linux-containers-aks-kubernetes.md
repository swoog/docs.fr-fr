---
title: Créer des applications ASP.NET Core 2.1 déployées en tant que conteneurs Linux dans les clusters AKS/Kubernetes
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: b03b6fab9dcd53e97c2bc4d7e5c958ca4b931077
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56221467"
---
# <a name="build-aspnet-core-21-applications-deployed-as-linux-containers-into-akskubernetes-orchestrator"></a><span data-ttu-id="c649c-103">Créer des applications ASP.NET Core 2.1 déployées comme conteneurs Linux dans ACS/Kubernetes orchestrator</span><span class="sxs-lookup"><span data-stu-id="c649c-103">Build ASP.NET Core 2.1 applications deployed as Linux containers into AKS/Kubernetes orchestrator</span></span>

<span data-ttu-id="c649c-104">Azure Kubernetes service (AKS) est Kubernetes orchestrations services gérés d’Azure qui simplifient la gestion et le déploiement de conteneur.</span><span class="sxs-lookup"><span data-stu-id="c649c-104">Azure Kubernetes Services (AKS) is Azure's managed Kubernetes orchestrations services that simplify container deployment and management.</span></span>

<span data-ttu-id="c649c-105">AKS les fonctionnalités principales sont :</span><span class="sxs-lookup"><span data-stu-id="c649c-105">AKS main features are:</span></span>

- <span data-ttu-id="c649c-106">Un plan de contrôle hébergé sur Azure</span><span class="sxs-lookup"><span data-stu-id="c649c-106">An Azure-hosted control plane</span></span>
- <span data-ttu-id="c649c-107">Mises à niveau automatisées</span><span class="sxs-lookup"><span data-stu-id="c649c-107">Automated upgrades</span></span>
- <span data-ttu-id="c649c-108">Réparation automatique</span><span class="sxs-lookup"><span data-stu-id="c649c-108">Self-healing</span></span>
- <span data-ttu-id="c649c-109">Mise à l’échelle de configurable utilisateur</span><span class="sxs-lookup"><span data-stu-id="c649c-109">User configurable scaling</span></span>
- <span data-ttu-id="c649c-110">Une expérience utilisateur plus simple pour les développeurs et les opérateurs du cluster.</span><span class="sxs-lookup"><span data-stu-id="c649c-110">A simpler user experience for both developers and cluster operators.</span></span>

<span data-ttu-id="c649c-111">Les exemples suivants Explorer la création d’une application ASP.NET Core 2.1, s’exécute sur Linux et déploie vers un Cluster AKS dans Azure, tandis que le développement est effectué à l’aide de Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="c649c-111">The following examples explore the creation of an ASP.NET Core 2.1 application that runs on Linux and deploys to an AKS Cluster in Azure, while development is done using Visual Studio 2017.</span></span>

## <a name="creating-the-aspnet-core-21-project-using-visual-studio-2017"></a><span data-ttu-id="c649c-112">Création du projet ASP.NET Core 2.1 à l’aide de Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="c649c-112">Creating the ASP.NET Core 2.1 Project using Visual Studio 2017</span></span>

<span data-ttu-id="c649c-113">ASP.NET Core est une plateforme de développement à usage général gérée par Microsoft et la Communauté .NET sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="c649c-113">ASP.NET Core is a general-purpose development platform maintained by Microsoft and the .NET community on GitHub.</span></span> <span data-ttu-id="c649c-114">Cette multiplateforme prend en charge Windows, macOS et Linux. Elle peut être utilisée dans des scénarios d’appareil, de cloud et d’incorporation/IoT.</span><span class="sxs-lookup"><span data-stu-id="c649c-114">It is cross-platform, supporting Windows, macOS and Linux, and can be used in device, cloud, and embedded/IoT scenarios.</span></span>

<span data-ttu-id="c649c-115">Cet exemple utilise un projet simple qui repose basé sur un modèle API Web de Visual Studio, vous n’avez pas besoin d’autres bases de connaissances pour créer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c649c-115">This example uses a simple project that's based based on a Visual Studio Web API template, so you don't need any additional knowledge to create the sample.</span></span> <span data-ttu-id="c649c-116">Vous devez uniquement créer le projet à l’aide d’un modèle standard qui inclut tous les éléments pour exécuter un petit projet avec une API REST, à l’aide de la technologie ASP.NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="c649c-116">You only have to create the project using a standard template that includes all the elements to run a small project with a REST API, using ASP.NET Core 2.1 technology.</span></span>

![Ajouter la fenêtre Nouveau projet dans Visual Studio, sélectionnez l’Application Web ASP.NET Core.](media/create-aspnet-core-application.png)

<span data-ttu-id="c649c-118">**Figure 4-36**.</span><span class="sxs-lookup"><span data-stu-id="c649c-118">**Figure 4-36**.</span></span> <span data-ttu-id="c649c-119">Création d’Application ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="c649c-119">Creating ASP.NET Core Application</span></span>

<span data-ttu-id="c649c-120">Pour créer l’exemple de projet, vous devez sélectionner **fichier** > **New** > **projet** sur Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c649c-120">To create the sample project, you have to select **File** > **New** > **Project** on Visual Studio.</span></span> <span data-ttu-id="c649c-121">Puis vous verrez une liste de modèles pour plusieurs types de projets, où vous avez besoin de rechercher **Web** > **.NET Core** dans le volet gauche.</span><span class="sxs-lookup"><span data-stu-id="c649c-121">Then you'll see a list of templates for several types of projects, where you have to look for **Web** > **.NET Core** on the left panel.</span></span> <span data-ttu-id="c649c-122">Pour cet exemple, sélectionnez **Application Web ASP.NET Core**.</span><span class="sxs-lookup"><span data-stu-id="c649c-122">For this example select **ASP.NET Core Web Application**.</span></span>

<span data-ttu-id="c649c-123">Dans la boîte de dialogue suivante, assurez-vous que vous avez sélectionné .NET Core et ASP.NET Core 2.1 comme framework cible dans les triceps supérieurs, comme indiqué dans la figure 4-37 et puis sélectionnez l’option de l’API, pour créer une application API Web ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="c649c-123">In the next dialog ensure that you have selected .NET Core and ASP.NET Core 2.1 as the target framework in the top pulldowns, as shown in figure 4-37, and then select the API option, to create an ASP.NET Core Web API application.</span></span>

<span data-ttu-id="c649c-124">Le .NET Core 2.1 est inclus dans Visual Studio 2017 version 15.7.0 ou une version ultérieure et est automatiquement installé et configuré pour vous lorsque vous sélectionnez le **.NET Core le développement multiplateforme** charge de travail lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="c649c-124">The .NET Core 2.1 is included in Visual Studio 2017 version 15.7.0 or higher and is automatically installed and configured for you when you select the **.NET Core cross-platform development** workload during installation.</span></span>

![Visual Studio boîte de dialogue Choisir le type d’une Application Web ASP.NET Core avec l’option API sélectionnée.](media/create-web-api-application.png)

<span data-ttu-id="c649c-126">**Figure 4-37**.</span><span class="sxs-lookup"><span data-stu-id="c649c-126">**Figure 4-37**.</span></span> <span data-ttu-id="c649c-127">Type de projet en sélectionnant ASP.NET CORE 2.1 et l’API Web</span><span class="sxs-lookup"><span data-stu-id="c649c-127">Selecting ASP.NET CORE 2.1 and Web API project type</span></span>

<span data-ttu-id="c649c-128">Si vous avez des versions précédentes de .NET Core, vous pouvez télécharger et installer la version 2.1 à partir de <https://www.microsoft.com/net/download/core#/sdk>.</span><span class="sxs-lookup"><span data-stu-id="c649c-128">If you have any previous version of .NET Core, you can download and install the 2.1 version from <https://www.microsoft.com/net/download/core#/sdk>.</span></span>

<span data-ttu-id="c649c-129">Vous pouvez ajouter la prise en charge Docker lors de la création du projet à l’étape précédente, ou version ultérieure, en cas de besoin après avoir démarré le projet.</span><span class="sxs-lookup"><span data-stu-id="c649c-129">You can add Docker support when creating the project in the previous step, or later, if the need arises after starting the project.</span></span> <span data-ttu-id="c649c-130">Pour ajouter la prise en charge de Docker après la création du projet, cliquez sur le fichier projet dans le **l’Explorateur de solutions** et sélectionnez **ajouter** > **prise en charge Docker** sur le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="c649c-130">To add the Docker support after the project creation, right-click on the project file in the **Solution Explorer** and select **Add** > **Docker support** on the context menu.</span></span>

![Option de menu contextuel pour ajouter la prise en charge Docker à un projet existant : Cliquez avec le bouton droit (sur le projet) > Ajouter > prise en charge Docker.](media/add-docker-support-to-project.png)

<span data-ttu-id="c649c-132">**Figure 4-38**.</span><span class="sxs-lookup"><span data-stu-id="c649c-132">**Figure 4-38**.</span></span> <span data-ttu-id="c649c-133">Ajout de prise en charge Docker à un projet existant</span><span class="sxs-lookup"><span data-stu-id="c649c-133">Adding Docker support to existing project</span></span>

<span data-ttu-id="c649c-134">Pour effectuer un ajout prise en charge de Docker, vous avez le choix de Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="c649c-134">To complete adding Docker support, you have the choice of Windows or Linux.</span></span> <span data-ttu-id="c649c-135">Dans ce cas, sélectionnez **Linux**, car ACS ne prend pas en charge les conteneurs Windows (comme de fin 2018).</span><span class="sxs-lookup"><span data-stu-id="c649c-135">In this case, select **Linux**, because AKS doesn’t support Windows Containers (as of late 2018).</span></span>

![Boîte de dialogue Options pour sélectionner le système d’exploitation cible pour le fichier Dockerfile.](media/select-linux-docker-support.png)

<span data-ttu-id="c649c-137">**Figure 4-39**.</span><span class="sxs-lookup"><span data-stu-id="c649c-137">**Figure 4-39**.</span></span> <span data-ttu-id="c649c-138">Sélection des conteneurs Linux.</span><span class="sxs-lookup"><span data-stu-id="c649c-138">Selecting Linux containers.</span></span>

<span data-ttu-id="c649c-139">Avec ces étapes simples, vous devez exécuter sur un conteneur Linux de votre application ASP.NET Core 2.1.</span><span class="sxs-lookup"><span data-stu-id="c649c-139">With these simple steps, you will have your ASP.NET Core 2.1 application running on a Linux container.</span></span>

<span data-ttu-id="c649c-140">Comme vous pouvez le voir, l’intégration entre Visual Studio 2017 et Docker est entièrement orientée vers la productivité du développeur.</span><span class="sxs-lookup"><span data-stu-id="c649c-140">As you can see, the integration between Visual Studio 2017 and Docker is totally oriented to the developer’s productivity.</span></span>

<span data-ttu-id="c649c-141">Maintenant vous pouvez appuyer sur **F5** pour générer et exécuter votre application.</span><span class="sxs-lookup"><span data-stu-id="c649c-141">Now you can press **F5** to build and run your application.</span></span>

<span data-ttu-id="c649c-142">Après avoir exécuté le projet, vous pouvez répertorier les images à l’aide de la `docker images` commande.</span><span class="sxs-lookup"><span data-stu-id="c649c-142">After running the project, you can list the images using the `docker images` command.</span></span> <span data-ttu-id="c649c-143">Vous devez voir le `mssampleapplication` image créée avec le déploiement automatique de notre projet avec Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="c649c-143">You should see the `mssampleapplication` image created with the automatic deploy of our project with Visual Studio 2017.</span></span>

```console
docker images
```

![La sortie de console à partir de la commande d’images docker, affiche une liste avec : Référentiel de balise, ID de l’Image, Created (date) et taille.](media/docker-images-command.png)

<span data-ttu-id="c649c-145">**Figure 4-40**.</span><span class="sxs-lookup"><span data-stu-id="c649c-145">**Figure 4-40**.</span></span> <span data-ttu-id="c649c-146">Affichage des images Docker</span><span class="sxs-lookup"><span data-stu-id="c649c-146">View of Docker images</span></span>

## <a name="register-the-solution-in-the-azure-container-registry"></a><span data-ttu-id="c649c-147">Enregistrez la Solution dans le Registre de conteneurs Azure</span><span class="sxs-lookup"><span data-stu-id="c649c-147">Register the Solution in the Azure Container Registry</span></span>

<span data-ttu-id="c649c-148">Télécharger l’image à n’importe quel Registre Docker, comme [Azure Container Registry (ACR)](https://azure.microsoft.com/services/container-registry/) ou sur Docker Hub pour les images peuvent être déployées sur le cluster AKS à partir de ce Registre.</span><span class="sxs-lookup"><span data-stu-id="c649c-148">Upload the image to any Docker registry, like [Azure Container Registry (ACR)](https://azure.microsoft.com/services/container-registry/) or Docker Hub so the images can be deployed to the AKS cluster from that registry.</span></span> <span data-ttu-id="c649c-149">Dans ce cas, nous allons charger l’image dans Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c649c-149">In this case, we’re uploading the image to Azure Container Registry.</span></span>

### <a name="create-the-image-in-release-mode"></a><span data-ttu-id="c649c-150">Créer l’image en mode de mise en production</span><span class="sxs-lookup"><span data-stu-id="c649c-150">Create the image in Release mode</span></span>

<span data-ttu-id="c649c-151">Créer l’image dans **version** (prêt pour la production) en Mode modification à la mise en production comme indiqué ici et appuyez sur F5 pour réexécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="c649c-151">Create the image in **Release** Mode (ready for production) changing to Release as shown here and press F5 to run the application again.</span></span>

![Option de la barre d’outils dans Visual Studio pour générer en mode release.](media/select-release-mode.png)

<span data-ttu-id="c649c-153">**Figure 4-41**.</span><span class="sxs-lookup"><span data-stu-id="c649c-153">**Figure 4-41**.</span></span> <span data-ttu-id="c649c-154">Sélection du Mode de mise en production</span><span class="sxs-lookup"><span data-stu-id="c649c-154">Selecting Release Mode</span></span>

<span data-ttu-id="c649c-155">Si vous exécutez le `docker image` commande, vous verrez les deux images créées.</span><span class="sxs-lookup"><span data-stu-id="c649c-155">If you execute the `docker image` command, you'll see both images created.</span></span> <span data-ttu-id="c649c-156">L’autre pour `debug` et l’autre pour `release` mode.</span><span class="sxs-lookup"><span data-stu-id="c649c-156">One for `debug` and the other for `release` mode.</span></span>

### <a name="create-a-new-tag-for-the-image"></a><span data-ttu-id="c649c-157">Créer une balise pour l’Image</span><span class="sxs-lookup"><span data-stu-id="c649c-157">Create a new Tag for the Image</span></span>

<span data-ttu-id="c649c-158">Chaque image de conteneur doit être marquée avec le `loginServer` nom du Registre.</span><span class="sxs-lookup"><span data-stu-id="c649c-158">Each container image needs to be tagged with the `loginServer` name of the registry.</span></span> <span data-ttu-id="c649c-159">Cette balise est utilisée pour le routage lors de l’envoi des images de conteneur à un registre d’image.</span><span class="sxs-lookup"><span data-stu-id="c649c-159">This tag is used for routing when pushing container images to an image registry.</span></span>

<span data-ttu-id="c649c-160">Vous pouvez afficher le `loginServer` nom à partir du portail Azure, en prenant les informations à partir du Registre de conteneur Azure</span><span class="sxs-lookup"><span data-stu-id="c649c-160">You can view the `loginServer` name from the Azure portal, taking the information from the Azure Container Registry</span></span>

![Vue du navigateur du nom du Registre de conteneurs Azure, dans le coin supérieur droit.](media/loginServer-name.png)

<span data-ttu-id="c649c-162">**Figure 4-42**.</span><span class="sxs-lookup"><span data-stu-id="c649c-162">**Figure 4-42**.</span></span> <span data-ttu-id="c649c-163">Affichage du nom du Registre</span><span class="sxs-lookup"><span data-stu-id="c649c-163">View of the name of the Registry</span></span>

<span data-ttu-id="c649c-164">Ou en exécutant la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c649c-164">Or by running the following command:</span></span>

```console
az acr list --resource-group MSSampleResourceGroup --query "[].{acrLoginServer:loginServer}" --output table
```

![Console de sortie à partir de la commande ci-dessus.](media/az-cli-loginServer-name.png)

<span data-ttu-id="c649c-166">**Figure 4-43**.</span><span class="sxs-lookup"><span data-stu-id="c649c-166">**Figure 4-43**.</span></span> <span data-ttu-id="c649c-167">Obtenir le nom du Registre à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="c649c-167">Get the name of the registry using PowerShell</span></span>

<span data-ttu-id="c649c-168">Dans les deux cas, vous devez obtenir le nom.</span><span class="sxs-lookup"><span data-stu-id="c649c-168">In both cases, you'll obtain the name.</span></span> <span data-ttu-id="c649c-169">Dans notre exemple, `mssampleacr.azurecr.io`.</span><span class="sxs-lookup"><span data-stu-id="c649c-169">In our example, `mssampleacr.azurecr.io`.</span></span>

<span data-ttu-id="c649c-170">Vous pouvez désormais marquer l’image, en prenant la dernière image (image de mise en production), avec la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c649c-170">Now you can tag the image, taking the latest image (Release image), with the following command:</span></span>

```console
docker tag mssampleaksapplication:latest mssampleacr.azurecr.io/mssampleaksapplication:v1
```

<span data-ttu-id="c649c-171">Après avoir exécuté le `docker tag` de commande, de répertorier les images avec le `docker images` commande.</span><span class="sxs-lookup"><span data-stu-id="c649c-171">After running the `docker tag` command, list the images with the `docker images` command.</span></span> <span data-ttu-id="c649c-172">Vous devez voir l’image avec la nouvelle balise.</span><span class="sxs-lookup"><span data-stu-id="c649c-172">You should see the image with the new tag.</span></span>

![Console de sortie à partir de la commande d’images docker.](media/tagged-docker-images-list.png)

<span data-ttu-id="c649c-174">**Figure 4-44**.</span><span class="sxs-lookup"><span data-stu-id="c649c-174">**Figure 4-44**.</span></span> <span data-ttu-id="c649c-175">Affichage d’images avec balises</span><span class="sxs-lookup"><span data-stu-id="c649c-175">View of tagged images</span></span>

### <a name="push-the-image-into-the-azure-acr"></a><span data-ttu-id="c649c-176">Envoyez l’image dans l’ACR Azure</span><span class="sxs-lookup"><span data-stu-id="c649c-176">Push the image into the Azure ACR</span></span>

<span data-ttu-id="c649c-177">Envoyez l’image dans l’ACR Azure, à l’aide de la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="c649c-177">Push the image into the Azure ACR, using the following command:</span></span>

```console
docker push mssampleacr.azurecr.io/mssampleaksapplication:v1
```

<span data-ttu-id="c649c-178">Cette commande prend un certain temps le téléchargement des images, mais vous donne des commentaires dans le processus.</span><span class="sxs-lookup"><span data-stu-id="c649c-178">This command takes a while uploading the images but gives you feedback in the process.</span></span>

![Sortie à partir de la commande push docker de la console : affiche une barre de progression basé sur des caractères pour chaque couche.](media/uploading-image-to-acr.png)

<span data-ttu-id="c649c-180">**Figure 4-45**.</span><span class="sxs-lookup"><span data-stu-id="c649c-180">**Figure 4-45**.</span></span> <span data-ttu-id="c649c-181">Chargement de l’image à l’ACR</span><span class="sxs-lookup"><span data-stu-id="c649c-181">Uploading the image to the ACR</span></span>

<span data-ttu-id="c649c-182">Vous pouvez le voir ci-dessous le résultat que vous devez obtenir lorsque le processus est terminé :</span><span class="sxs-lookup"><span data-stu-id="c649c-182">You can see below the result you should get when the process completes:</span></span>

![Sortie à partir de la commande push docker, terminée, affichant toutes les couches ou les nœuds de la console.](media/uploading-docker-images-complete.png)

<span data-ttu-id="c649c-184">**Figure 4-46**.</span><span class="sxs-lookup"><span data-stu-id="c649c-184">**Figure 4-46**.</span></span> <span data-ttu-id="c649c-185">Affichage de nœuds</span><span class="sxs-lookup"><span data-stu-id="c649c-185">View of nodes</span></span>

<span data-ttu-id="c649c-186">L’étape suivante consiste à déployer votre conteneur dans votre cluster ACS Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c649c-186">The next step is to deploy your container into your AKS Kubernetes cluster.</span></span> <span data-ttu-id="c649c-187">Pour que vous avez besoin d’un fichier (**.yml déployer le fichier**), dans ce cas, contenant :</span><span class="sxs-lookup"><span data-stu-id="c649c-187">For that you need a file (**.yml deploy file**) that, in this case, contains:</span></span>

```yml
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: mssamplesbook
spec:
  replicas: 1
  template:
    metadata:
      labels:
        app: mssample-kub-app
    spec:
      containers:
        - mane: mssample-services-app
          image: mssampleacr.azurecr.io/mssampleaksapplication:v1
          ports:
            - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
    name: mssample-kub-app
spec:
  ports:
    - name: http-port
      port: 80
      targetPort: 80
  selector:
    app: mssample-kub-app
  type: LoadBalancer
```

> [!NOTE]
> <span data-ttu-id="c649c-188">Pour plus d’informations sur le déploiement avec Kubernetes, consultez : <https://kubernetes.io/docs/reference/kubectl/cheatsheet/></span><span class="sxs-lookup"><span data-stu-id="c649c-188">For more information on deployment with Kubernetes see: <https://kubernetes.io/docs/reference/kubectl/cheatsheet/></span></span>

<span data-ttu-id="c649c-189">Maintenant vous êtes presque prêt à déployer à l’aide **Kubectl**, mais vous devez tout d’abord obtenir les informations d’identification pour le Cluster AKS avec cette commande :</span><span class="sxs-lookup"><span data-stu-id="c649c-189">Now you're almost ready to deploy using **Kubectl**, but first you must get the credentials to the AKS Cluster with this command:</span></span>

```console
az aks get-credentials --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

![Console de sortie à partir de la commande ci-dessus : Fusionné MSSampleK8Cluster » en tant que contexte actuel dans /root/.kube/config](media/getting-aks-credentials.png)

<span data-ttu-id="c649c-191">**Figure 4-47**.</span><span class="sxs-lookup"><span data-stu-id="c649c-191">**Figure 4-47**.</span></span> <span data-ttu-id="c649c-192">obtention des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="c649c-192">getting credentials</span></span>

<span data-ttu-id="c649c-193">Ensuite, utilisez le `kubectl create` commande pour lancer le déploiement.</span><span class="sxs-lookup"><span data-stu-id="c649c-193">Then, use the `kubectl create` command to launch the deployment.</span></span>

```console
kubectl create -f mssample-deploy.yml
```

![Console de sortie à partir de la commande ci-dessus : déploiement « mssamplesbook » créé.](media/kubectl-create-command.png)

<span data-ttu-id="c649c-196">**Figure 4-48**.</span><span class="sxs-lookup"><span data-stu-id="c649c-196">**Figure 4-48**.</span></span> <span data-ttu-id="c649c-197">Déployer sur Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c649c-197">Deploy to Kubernetes</span></span>

<span data-ttu-id="c649c-198">Lorsque le déploiement terminé, vous pouvez accéder à la console Kubernetes avec un proxy local auquel vous pouvez accéder temporellement avec cette commande :</span><span class="sxs-lookup"><span data-stu-id="c649c-198">When the deployment completes, you can access the Kubernetes console with a local proxy that you can temporally access with this command:</span></span>

```console
az aks browse --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

<span data-ttu-id="c649c-199">Et en accédant à l’url `http://127.0.0.1:8001`.</span><span class="sxs-lookup"><span data-stu-id="c649c-199">And accessing the url `http://127.0.0.1:8001`.</span></span>

![Vue du navigateur du tableau de bord Kubernetes, montrant les déploiements, les Pods, les jeux de réplicas et les Services.](media/kubernetes-cluster-information.png)

<span data-ttu-id="c649c-201">**Figure 4-49**.</span><span class="sxs-lookup"><span data-stu-id="c649c-201">**Figure 4-49**.</span></span> <span data-ttu-id="c649c-202">Afficher les informations de cluster Kubernetes</span><span class="sxs-lookup"><span data-stu-id="c649c-202">View Kubernetes cluster information</span></span>

<span data-ttu-id="c649c-203">Vous disposez maintenant de votre application déployée sur Azure, à l’aide d’un conteneur Linux et un Cluster de Kubernetes ACS.</span><span class="sxs-lookup"><span data-stu-id="c649c-203">Now you have your application deployed on Azure, using a Linux Container, and an AKS Kubernetes Cluster.</span></span> <span data-ttu-id="c649c-204">Vous pouvez accéder à votre application accédant à l’adresse IP publique de votre service, vous pouvez obtenir à partir du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="c649c-204">You can access your app browsing to the public IP of your service, which you can get from the Azure portal.</span></span>

> [!NOTE]
> <span data-ttu-id="c649c-205">Vous pouvez voir comment créer le Cluster AKS pour cet exemple dans la section [ **déployer vers Azure Kubernetes Service (AKS)** ](deploy-azure-kubernetes-service.md) sur ce guide.</span><span class="sxs-lookup"><span data-stu-id="c649c-205">You can see how to create the AKS Cluster for this sample in section [**Deploy to Azure Kubernetes Service (AKS)**](deploy-azure-kubernetes-service.md) on this guide.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="c649c-206">[Précédent](set-up-windows-containers-with-powershell.md)
>[Suivant](../docker-devops-workflow/index.md)</span><span class="sxs-lookup"><span data-stu-id="c649c-206">[Previous](set-up-windows-containers-with-powershell.md)
[Next](../docker-devops-workflow/index.md)</span></span>
