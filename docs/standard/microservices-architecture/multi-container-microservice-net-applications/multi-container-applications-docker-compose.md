---
title: "Définition de votre application à plusieurs conteneurs avec docker-compose.yml"
description: "Architecture des microservices .NET pour les applications .NET en conteneur | Définition de votre application à plusieurs conteneurs avec docker-compose.yml"
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/30/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: c4fed5c7ba5c2048d103f22bd2b463c143013280
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="defining-your-multi-container-application-with-docker-composeyml"></a><span data-ttu-id="f940d-104">Définition de votre application à plusieurs conteneurs avec docker-compose.yml</span><span class="sxs-lookup"><span data-stu-id="f940d-104">Defining your multi-container application with docker-compose.yml</span></span> 

<span data-ttu-id="f940d-105">Dans ce guide, le fichier [docker-compose.yml](https://docs.docker.com/compose/compose-file/) a été introduit dans la section [Étape 4. Définir vos services dans docker-compose.yml au moment de générer une application Docker à plusieurs conteneurs](#step4_define_svcs_in_docker_compose_yml).</span><span class="sxs-lookup"><span data-stu-id="f940d-105">In this guide, the [docker-compose.yml](https://docs.docker.com/compose/compose-file/) file was introduced in the section [Step 4. Define your services in docker-compose.yml when building a multi-container Docker application](#step4_define_svcs_in_docker_compose_yml).</span></span> <span data-ttu-id="f940d-106">Toutefois, il existe d’autres modes d’utilisation des fichiers docker-compose qui méritent d’être abordés plus en détail.</span><span class="sxs-lookup"><span data-stu-id="f940d-106">However, there are additional ways to use the docker-compose files that are worth exploring in further detail.</span></span>

<span data-ttu-id="f940d-107">Par exemple, vous pouvez décrire explicitement la façon dont vous souhaitez déployer votre application à plusieurs conteneurs dans le fichier docker-compose.yml.</span><span class="sxs-lookup"><span data-stu-id="f940d-107">For example, you can explicitly describe how you want to deploy your multi-container application in the docker-compose.yml file.</span></span> <span data-ttu-id="f940d-108">Éventuellement, vous pouvez également décrire la façon dont vous allez générer vos images Docker personnalisées.</span><span class="sxs-lookup"><span data-stu-id="f940d-108">Optionally, you can also describe how you are going to build your custom Docker images.</span></span> <span data-ttu-id="f940d-109">(Vous pouvez également générer des images Docker personnalisées avec l’interface de ligne de commande Docker CLI.)</span><span class="sxs-lookup"><span data-stu-id="f940d-109">(Custom Docker images can also be built with the Docker CLI.)</span></span>

<span data-ttu-id="f940d-110">Pour l’essentiel, vous définissez chacun des conteneurs à déployer, ainsi que certaines caractéristiques relatives à chaque déploiement de conteneur.</span><span class="sxs-lookup"><span data-stu-id="f940d-110">Basically, you define each of the containers you want to deploy plus certain characteristics for each container deployment.</span></span> <span data-ttu-id="f940d-111">Une fois que vous disposez d’un fichier de description de déploiement à plusieurs conteneurs, vous pouvez déployer l’ensemble de la solution en une seule action orchestrée par la commande CLI [docker-compose up](https://docs.docker.com/compose/overview/), ou la déployer de manière transparente à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f940d-111">Once you have a multi-container deployment description file, you can deploy the whole solution in a single action orchestrated by the [docker-compose up](https://docs.docker.com/compose/overview/) CLI command, or you can deploy it transparently from Visual Studio.</span></span> <span data-ttu-id="f940d-112">Sinon, vous devez utiliser Docker CLI pour effectuer un déploiement conteneur par conteneur en plusieurs étapes à l’aide de la commande docker run depuis la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f940d-112">Otherwise, you would need to use the Docker CLI to deploy container-by-container in multiple steps by using the docker run command from the command line.</span></span> <span data-ttu-id="f940d-113">Ainsi, chaque service défini dans docker-compose.yml doit spécifier une seule image ou une seule build.</span><span class="sxs-lookup"><span data-stu-id="f940d-113">Therefore, each service defined in docker-compose.yml must specify exactly one image or build.</span></span> <span data-ttu-id="f940d-114">Les autres clés sont facultatives et sont analogues à leurs homologues de ligne de commande docker run.</span><span class="sxs-lookup"><span data-stu-id="f940d-114">Other keys are optional, and are analogous to their docker run command-line counterparts.</span></span>

<span data-ttu-id="f940d-115">Le code YAML suivant représente la définition d’un éventuel fichier docker-compose.yml global mais unique pour l’exemple eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="f940d-115">The following YAML code is the definition of a possible global but single docker-compose.yml file for the eShopOnContainers sample.</span></span> <span data-ttu-id="f940d-116">Il ne s’agit pas du fichier docker-compose réel d’eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="f940d-116">This is not the actual docker-compose file from eShopOnContainers.</span></span> <span data-ttu-id="f940d-117">Il s’agit plutôt d’une version simplifiée et centralisée dans un fichier unique, ce qui n’est pas la meilleure façon d’utiliser les fichiers docker-compose, comme cela sera expliqué plus tard.</span><span class="sxs-lookup"><span data-stu-id="f940d-117">Instead, it is a simplified and consolidated version in a single file, which is not the best way to work with docker-compose files, as will be explained later.</span></span>

```yml
version: '2'

services:
  webmvc:
    image: eshop/webmvc
    environment:
      - CatalogUrl=http://catalog.api
      - OrderingUrl=http://ordering.api
      - BasketUrl=http://basket.api
    ports:
      - "5100:80"
    depends_on:
      - catalog.api
      - ordering.api
      - basket.api

  catalog.api:
    image: eshop/catalog.api
    environment:
      - ConnectionString=Server=sql.data;Initial Catalog=CatalogData;User Id=sa;Password=your@password
    expose:
      - "80"
    ports:
      - "5101:80"
    #extra hosts can be used for standalone SQL Server or services at the dev PC
    extra_hosts:
      - "CESARDLSURFBOOK:10.0.75.1"
    depends_on:
      - sql.data

  ordering.api:
    image: eshop/ordering.api
    environment:
      - ConnectionString=Server=sql.data;Database=Services.OrderingDb;User Id=sa;Password=your@password
    ports:
      - "5102:80"
    #extra hosts can be used for standalone SQL Server or services at the dev PC
    extra_hosts:
      - "CESARDLSURFBOOK:10.0.75.1"
    depends_on:
      - sql.data

  basket.api:
    image: eshop/basket.api
    environment:
      - ConnectionString=sql.data
    ports:
      - "5103:80"
    depends_on:
      - sql.data

  sql.data:
    environment:
      - SA_PASSWORD=your@password
      - ACCEPT_EULA=Y
    ports:
      - "5434:1433"

  basket.data:
    image: redis
```

<span data-ttu-id="f940d-118">La clé racine de ce fichier est services.</span><span class="sxs-lookup"><span data-stu-id="f940d-118">The root key in this file is services.</span></span> <span data-ttu-id="f940d-119">Sous cette clé, vous définissez les services que vous souhaitez déployer et exécuter quand vous exécutez la commande docker-compose up, ou quand vous effectuez un déploiement à partir de Visual Studio à l’aide du fichier docker-compose.yml.</span><span class="sxs-lookup"><span data-stu-id="f940d-119">Under that key you define the services you want to deploy and run when you execute the docker-compose up command or when you deploy from Visual Studio by using this docker-compose.yml file.</span></span> <span data-ttu-id="f940d-120">Dans ce cas, plusieurs services sont définis pour le fichier docker-compose.yml, comme indiqué dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="f940d-120">In this case, the docker-compose.yml file has multiple services defined, as described in the following list.</span></span>

-   <span data-ttu-id="f940d-121">Conteneur webmvc incluant l’application ASP.NET Core MVC, qui consomme les microservices à partir du code C\# côté serveur</span><span class="sxs-lookup"><span data-stu-id="f940d-121">webmvc Container including the ASP.NET Core MVC application consuming the microservices from server-side C\#</span></span>

-   <span data-ttu-id="f940d-122">Conteneur catalog.api incluant le microservice de l’API web ASP.NET Core du catalogue</span><span class="sxs-lookup"><span data-stu-id="f940d-122">catalog.api Container including the Catalog ASP.NET Core Web API microservice</span></span>

-   <span data-ttu-id="f940d-123">Conteneur ordering.api incluant le microservice de l’API web ASP.NET Core des commandes</span><span class="sxs-lookup"><span data-stu-id="f940d-123">ordering.api Container including the Ordering ASP.NET Core Web API microservice</span></span>

-   <span data-ttu-id="f940d-124">Conteneur sql.data exécutant SQL Server pour Linux et contenant les bases de données de microservices</span><span class="sxs-lookup"><span data-stu-id="f940d-124">sql.data Container running SQL Server for Linux, holding the microservices databases</span></span>

-   <span data-ttu-id="f940d-125">Conteneur basket.api incluant le microservice de l’API web ASP.NET Core du panier</span><span class="sxs-lookup"><span data-stu-id="f940d-125">basket.api Container with the Basket ASP.NET Core Web API microservice</span></span>

-   <span data-ttu-id="f940d-126">Conteneur basket.data exécutant le Cache Service REDIS, avec la base de données du panier en tant que cache REDIS</span><span class="sxs-lookup"><span data-stu-id="f940d-126">basket.data Container running the REDIS cache service, with the basket database as a REDIS cache</span></span>

### <a name="a-simple-web-service-api-container"></a><span data-ttu-id="f940d-127">Conteneur d’API de service web simple</span><span class="sxs-lookup"><span data-stu-id="f940d-127">A simple Web Service API container</span></span>

<span data-ttu-id="f940d-128">Dans la mesure où il se concentre sur un seul conteneur, le microservice du conteneur catalog.api a une définition simple :</span><span class="sxs-lookup"><span data-stu-id="f940d-128">Focusing on a single container, the catalog.api container-microservice has a straightforward definition:</span></span>

```yml
  catalog.api:
    image: eshop/catalog.api
    environment:
      - ConnectionString=Server=catalog.data;Initial Catalog=CatalogData;User Id=sa;Password=your@password
    expose:
      - "80"
    ports:
      - "5101:80"
    #extra hosts can be used for standalone SQL Server or services at the dev PC
    extra_hosts:
      - "CESARDLSURFBOOK:10.0.75.1"
    depends_on:
      - sql.data
```

<span data-ttu-id="f940d-129">Ce service conteneurisé a la configuration de base suivante :</span><span class="sxs-lookup"><span data-stu-id="f940d-129">This containerized service has the following basic configuration:</span></span>

-   <span data-ttu-id="f940d-130">Il est basé sur l’image personnalisée eshop/catalog.api.</span><span class="sxs-lookup"><span data-stu-id="f940d-130">It is based on the custom eshop/catalog.api image.</span></span> <span data-ttu-id="f940d-131">Par souci de simplicité, il n’existe aucun paramètre build: key dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="f940d-131">For simplicity’s sake, there is no build: key setting in the file.</span></span> <span data-ttu-id="f940d-132">Cela signifie que l’image doit avoir été générée (avec docker build) ou téléchargée (avec la commande docker pull) au préalable, depuis n’importe quel registre Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-132">This means that the image must have been previously built (with docker build) or have been downloaded (with the docker pull command) from any Docker registry.</span></span>

-   <span data-ttu-id="f940d-133">Il définit une variable d’environnement nommée ConnectionString à l’aide de la chaîne de connexion à utiliser par Entity Framework pour accéder à l’instance SQL Server qui contient le modèle de données du catalogue.</span><span class="sxs-lookup"><span data-stu-id="f940d-133">It defines an environment variable named ConnectionString with the connection string to be used by Entity Framework to access the SQL Server instance that contains the catalog data model.</span></span> <span data-ttu-id="f940d-134">Dans le cas présent, le même conteneur SQL Server contient plusieurs bases de données.</span><span class="sxs-lookup"><span data-stu-id="f940d-134">In this case, the same SQL Server container is holding multiple databases.</span></span> <span data-ttu-id="f940d-135">Vous avez donc besoin de moins de mémoire sur votre machine de développement pour Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-135">Therefore, you need less memory in your development machine for Docker.</span></span> <span data-ttu-id="f940d-136">Toutefois, vous pouvez également déployer un conteneur SQL Server pour chaque base de données de microservice.</span><span class="sxs-lookup"><span data-stu-id="f940d-136">However, you could also deploy one SQL Server container for each microservice database.</span></span>

-   <span data-ttu-id="f940d-137">Le nom SQL Server est sql.data, le même nom que celui utilisé pour le conteneur qui exécute l’instance SQL Server pour Linux.</span><span class="sxs-lookup"><span data-stu-id="f940d-137">The SQL Server name is sql.data, which is the same name used for the container that is running the SQL Server instance for Linux.</span></span> <span data-ttu-id="f940d-138">Cela est très pratique, car cette résolution de noms (interne à l’hôte Docker) permet de résoudre l’adresse réseau, ce qui vous évite d’avoir à connaître l’adresse IP interne des conteneurs auxquels vous accédez à partir d’autres conteneurs.</span><span class="sxs-lookup"><span data-stu-id="f940d-138">This is convenient; being able to use this name resolution (internal to the Docker host) will resolve the network address so you don’t need to know the internal IP for the containers you are accessing from other containers.</span></span>

<span data-ttu-id="f940d-139">Dans la mesure où la chaîne de connexion est définie par une variable d’environnement, vous pouvez définir cette variable via un autre mécanisme et à un autre moment.</span><span class="sxs-lookup"><span data-stu-id="f940d-139">Because the connection string is defined by an environment variable, you could set that variable through a different mechanism and at a different time.</span></span> <span data-ttu-id="f940d-140">Par exemple, vous pouvez définir une chaîne de connexion distincte durant le déploiement en production sur les hôtes finaux, ou à partir de vos pipelines d’intégration continue/de livraison continue dans VSTS ou votre système DevOps préféré.</span><span class="sxs-lookup"><span data-stu-id="f940d-140">For example, you could set a different connection string when deploying to production in the final hosts, or by doing it from your CI/CD pipelines in VSTS or your preferred DevOps system.</span></span>

-   <span data-ttu-id="f940d-141">Il expose le port 80 pour l’accès interne au service catalog.api dans l’hôte Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-141">It exposes port 80 for internal access to the catalog.api service within the Docker host.</span></span> <span data-ttu-id="f940d-142">L’hôte est une machine virtuelle Linux, car elle est basée sur une image Docker pour Linux, mais vous pouvez configurer le conteneur pour qu’il s’exécute plutôt sur une image Windows.</span><span class="sxs-lookup"><span data-stu-id="f940d-142">The host is currently a Linux VM because it is based on a Docker image for Linux, but you could configure the container to run on a Windows image instead.</span></span>

-   <span data-ttu-id="f940d-143">Il réachemine le port 80 exposé sur le conteneur vers le port 5101 de la machine hôte Docker (machine virtuelle Linux).</span><span class="sxs-lookup"><span data-stu-id="f940d-143">It forwards the exposed port 80 on the container to port 5101 on the Docker host machine (the Linux VM).</span></span>

-   <span data-ttu-id="f940d-144">Il lie le service web au service sql.data (instance SQL Server pour la base de données Linux s’exécutant dans un conteneur).</span><span class="sxs-lookup"><span data-stu-id="f940d-144">It links the web service to the sql.data service (the SQL Server instance for Linux database running in a container).</span></span> <span data-ttu-id="f940d-145">Quand vous spécifiez cette dépendance, le conteneur catalog.api ne démarre pas tant que le conteneur sql.data n’a pas démarré. Cela est important, car catalog.api a besoin que la base de données SQL Server soit d’abord opérationnelle.</span><span class="sxs-lookup"><span data-stu-id="f940d-145">When you specify this dependency, the catalog.api container will not start until the sql.data container has already started; this is important because catalog.api needs to have the SQL Server database up and running first.</span></span> <span data-ttu-id="f940d-146">Toutefois, ce genre de dépendance de conteneur ne suffit pas dans la plupart des cas, car Docker effectue uniquement une vérification au niveau du conteneur.</span><span class="sxs-lookup"><span data-stu-id="f940d-146">However, this kind of container dependency is not enough in many cases, because Docker checks only at the container level.</span></span> <span data-ttu-id="f940d-147">Parfois, le service (dans le cas présent, SQL Server) n’est peut-être pas encore prêt. Il est donc conseillé d’implémenter une logique de réexécution avec interruption exponentielle dans vos microservices clients.</span><span class="sxs-lookup"><span data-stu-id="f940d-147">Sometimes the service (in this case SQL Server) might still not be ready, so it is advisable to implement retry logic with exponential backoff in your client microservices.</span></span> <span data-ttu-id="f940d-148">Ainsi, si un conteneur de dépendances n’est pas prêt pendant une courte période, l’application reste résiliente.</span><span class="sxs-lookup"><span data-stu-id="f940d-148">That way, if a dependency container is not ready for a short time, the application will still be resilient.</span></span>

-   <span data-ttu-id="f940d-149">Il est configuré pour autoriser l’accès aux serveurs externes : le paramètre extra\_hosts vous permet d’accéder à des serveurs ou machines externes à l’hôte Docker (c’est-à-dire, situées en dehors de la machine virtuelle Linux par défaut qui est un hôte Docker de développement), par exemple une instance SQL Server locale sur votre PC de développement.</span><span class="sxs-lookup"><span data-stu-id="f940d-149">It is configured to allow access to external servers: the extra\_hosts setting allows you to access external servers or machines outside of the Docker host (that is, outside the default Linux VM which is a development Docker host), such as a local SQL Server instance on your development PC.</span></span>

<span data-ttu-id="f940d-150">Il existe également d’autres paramètres docker-compose.yml plus avancés que nous aborderons dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f940d-150">There are also other, more advanced docker-compose.yml settings that we will discuss in the following sections.</span></span>

### <a name="using-docker-compose-files-to-target-multiple-environments"></a><span data-ttu-id="f940d-151">Utilisation de fichiers docker-compose pour cibler plusieurs environnements</span><span class="sxs-lookup"><span data-stu-id="f940d-151">Using docker-compose files to target multiple environments</span></span>

<span data-ttu-id="f940d-152">Les fichiers docker-compose.yml sont des fichiers de définition. Ils peuvent être utilisés par plusieurs infrastructures qui comprennent ce format.</span><span class="sxs-lookup"><span data-stu-id="f940d-152">The docker-compose.yml files are definition files and can be used by multiple infrastructures that understand that format.</span></span> <span data-ttu-id="f940d-153">L’outil le plus simple est la commande docker-compose. Toutefois, d’autres outils tels que les orchestrateurs (par exemple, Docker Swarm) comprennent également ce fichier.</span><span class="sxs-lookup"><span data-stu-id="f940d-153">The most straightforward tool is the docker-compose command, but other tools like orchestrators (for example, Docker Swarm) also understand that file.</span></span>

<span data-ttu-id="f940d-154">Ainsi, à l’aide de la commande docker-compose, vous pouvez cibler les principaux scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="f940d-154">Therefore, by using the docker-compose command you can target the following main scenarios.</span></span>

#### <a name="development-environments"></a><span data-ttu-id="f940d-155">Environnements de développement</span><span class="sxs-lookup"><span data-stu-id="f940d-155">Development environments</span></span>

<span data-ttu-id="f940d-156">Quand vous développez des applications, il est important de pouvoir les exécuter dans un environnement de développement isolé.</span><span class="sxs-lookup"><span data-stu-id="f940d-156">When you develop applications, it is important to be able to run an application in an isolated development environment.</span></span> <span data-ttu-id="f940d-157">Vous pouvez vous servir de la commande CLI docker-compose pour créer cet environnement, ou utiliser Visual Studio qui exécute docker-compose de manière interne.</span><span class="sxs-lookup"><span data-stu-id="f940d-157">You can use the docker-compose CLI command to create that environment or use Visual Studio which uses docker-compose under the covers.</span></span>

<span data-ttu-id="f940d-158">Le fichier docker-compose.yml vous permet de configurer et de documenter toutes les dépendances de service de votre application (autres services, mises en cache, bases de données, files d’attente, etc.).</span><span class="sxs-lookup"><span data-stu-id="f940d-158">The docker-compose.yml file allows you to configure and document all your application’s service dependencies (other services, cache, databases, queues, etc.).</span></span> <span data-ttu-id="f940d-159">À l’aide de la commande CLI docker-compose, vous pouvez créer et démarrer un ou plusieurs conteneurs pour chaque dépendance avec une seule commande (docker-compose up).</span><span class="sxs-lookup"><span data-stu-id="f940d-159">Using the docker-compose CLI command, you can create and start one or more containers for each dependency with a single command (docker-compose up).</span></span>

<span data-ttu-id="f940d-160">Les fichiers docker-compose.yml sont des fichiers config interprétés par le moteur Docker. Toutefois, ils servent également de fichiers de documentation pratiques sur la composition de votre application à plusieurs conteneurs.</span><span class="sxs-lookup"><span data-stu-id="f940d-160">The docker-compose.yml files are configuration files interpreted by Docker engine but also serve as convenient documentation files about the composition of your multi-container application.</span></span>

#### <a name="testing-environments"></a><span data-ttu-id="f940d-161">Environnements de test</span><span class="sxs-lookup"><span data-stu-id="f940d-161">Testing environments</span></span>

<span data-ttu-id="f940d-162">Les tests unitaires et les tests d’intégration sont une partie importante d’un processus de déploiement continu ou d’intégration continue (CI).</span><span class="sxs-lookup"><span data-stu-id="f940d-162">An important part of any continuous deployment (CD) or continuous integration (CI) process are the unit tests and integration tests.</span></span> <span data-ttu-id="f940d-163">Ces tests automatisés nécessitent un environnement isolé pour ne pas être impactés par les utilisateurs ou par tout autre changement dans les données de l’application.</span><span class="sxs-lookup"><span data-stu-id="f940d-163">These automated tests require an isolated environment so they are not impacted by the users or any other change in the application’s data.</span></span>

<span data-ttu-id="f940d-164">Avec Docker Compose, vous pouvez créer et détruire très facilement cet environnement isolé en quelques commandes, à partir de votre invite de commandes ou de vos scripts, à l’image des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f940d-164">With Docker Compose you can create and destroy that isolated environment very easily in a few commands from your command prompt or scripts, like the following commands:</span></span>

```
docker-compose up -d
./run_unit_tests
docker-compose down
```

#### <a name="production-deployments"></a><span data-ttu-id="f940d-165">Déploiements de production</span><span class="sxs-lookup"><span data-stu-id="f940d-165">Production deployments</span></span>

<span data-ttu-id="f940d-166">Vous pouvez également utiliser Compose pour effectuer un déploiement sur un moteur Docker distant.</span><span class="sxs-lookup"><span data-stu-id="f940d-166">You can also use Compose to deploy to a remote Docker Engine.</span></span> <span data-ttu-id="f940d-167">Il est assez courant d’effectuer un déploiement sur une seule instance d’hôte Docker (par exemple une machine virtuelle de production ou un serveur provisionné avec [Docker Machine](https://docs.docker.com/machine/overview/)).</span><span class="sxs-lookup"><span data-stu-id="f940d-167">A typical case is to deploy to a single Docker host instance (like a production VM or server provisioned with [Docker Machine](https://docs.docker.com/machine/overview/)).</span></span> <span data-ttu-id="f940d-168">Toutefois, il peut aussi s’agir d’un cluster [Docker Swarm](https://docs.docker.com/swarm/overview/) complet, car les clusters sont également compatibles avec les fichiers docker-compose.yml.</span><span class="sxs-lookup"><span data-stu-id="f940d-168">But it could also be an entire [Docker Swarm](https://docs.docker.com/swarm/overview/) cluster, because clusters are also compatible with the docker-compose.yml files.</span></span>

<span data-ttu-id="f940d-169">Si vous utilisez un autre orchestrateur (Azure Service Fabric, Mesos DC/OS, Kubernetes, etc.), vous devrez peut-être ajouter des paramètres d’installation et des paramètres de configuration de métadonnées comme ceux de docker-compose.yml, mais dans le format demandé par l’autre orchestrateur.</span><span class="sxs-lookup"><span data-stu-id="f940d-169">If you are using any other orchestrator (Azure Service Fabric, Mesos DC/OS, Kubernetes, etc.), you might need to add setup and metadata configuration settings like those in docker-compose.yml, but in the format required by the other orchestrator.</span></span>

<span data-ttu-id="f940d-170">Dans tous les cas, docker-compose est un outil pratique et un format de métadonnées adapté aux workflows de développement, de test et de production, même si le workflow de production peut varier selon l’orchestrateur utilisé.</span><span class="sxs-lookup"><span data-stu-id="f940d-170">In any case, docker-compose is a convenient tool and metadata format for development, testing and production workflows, although the production workflow might vary on the orchestrator you are using.</span></span>

### <a name="using-multiple-docker-compose-files-to-handle-several-environments"></a><span data-ttu-id="f940d-171">Utilisation de plusieurs fichiers docker-compose pour prendre en charge plusieurs environnements</span><span class="sxs-lookup"><span data-stu-id="f940d-171">Using multiple docker-compose files to handle several environments</span></span>

<span data-ttu-id="f940d-172">Quand vous ciblez des environnements différents, vous devez utiliser plusieurs fichiers Compose.</span><span class="sxs-lookup"><span data-stu-id="f940d-172">When targeting different environments, you should use multiple compose files.</span></span> <span data-ttu-id="f940d-173">Cela vous permet de créer plusieurs variantes de configuration en fonction de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="f940d-173">This lets you create multiple configuration variants depending on the environment.</span></span>

#### <a name="overriding-the-base-docker-compose-file"></a><span data-ttu-id="f940d-174">Remplacement du fichier docker-compose de base</span><span class="sxs-lookup"><span data-stu-id="f940d-174">Overriding the base docker-compose file</span></span>

<span data-ttu-id="f940d-175">Vous pouvez utiliser un fichier docker-compose.yml unique comme dans les exemples simplifiés présentés dans les sections précédentes.</span><span class="sxs-lookup"><span data-stu-id="f940d-175">You could use a single docker-compose.yml file as in the simplified examples shown in previous sections.</span></span> <span data-ttu-id="f940d-176">Toutefois, cela n’est pas recommandé pour la plupart des applications.</span><span class="sxs-lookup"><span data-stu-id="f940d-176">However, that is not recommended for most applications.</span></span>

<span data-ttu-id="f940d-177">Par défaut, Compose lit deux fichiers, un fichier docker-compose.yml et un fichier docker-compose.override.yml facultatif.</span><span class="sxs-lookup"><span data-stu-id="f940d-177">By default, Compose reads two files, a docker-compose.yml and an optional docker-compose.override.yml file.</span></span> <span data-ttu-id="f940d-178">Comme le montre la figure 8-11, quand vous utilisez Visual Studio et que vous activez la prise en charge de Docker, Visual Studio crée également un fichier docker-compose.ci.build supplémentaire que vous pouvez utiliser à partir de vos pipelines d’intégration continue/de livraison continue comme dans VSTS.</span><span class="sxs-lookup"><span data-stu-id="f940d-178">As shown in Figure 8-11, when you are using Visual Studio and enabling Docker support, Visual Studio also creates an additional docker-compose.ci.build,yml file for you to use from your CI/CD pipelines like in VSTS.</span></span>

![](./media/image12.png)

<span data-ttu-id="f940d-179">**Figure 8-11**.</span><span class="sxs-lookup"><span data-stu-id="f940d-179">**Figure 8-11**.</span></span> <span data-ttu-id="f940d-180">Fichiers docker-compose dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="f940d-180">docker-compose files in Visual Studio 2017</span></span>

<span data-ttu-id="f940d-181">Vous pouvez modifier les fichiers docker-compose à l’aide de n’importe quel éditeur, par exemple Visual Studio Code ou Sublime, et lancer l’application avec la commande docker-compose up.</span><span class="sxs-lookup"><span data-stu-id="f940d-181">You can edit the docker-compose files with any editor, like Visual Studio Code or Sublime, and run the application with the docker-compose up command.</span></span>

<span data-ttu-id="f940d-182">Par convention, le fichier docker-compose.yml contient votre configuration de base et d’autres paramètres statiques.</span><span class="sxs-lookup"><span data-stu-id="f940d-182">By convention, the docker-compose.yml file contains your base configuration and other static settings.</span></span> <span data-ttu-id="f940d-183">Cela signifie que la configuration du service ne doit pas changer en fonction de l’environnement de déploiement ciblé.</span><span class="sxs-lookup"><span data-stu-id="f940d-183">That means that the service configuration should not change depending on the deployment environment you are targeting.</span></span>

<span data-ttu-id="f940d-184">Comme son nom l’indique, le fichier docker-compose.override.yml contient des paramètres de configuration qui remplacent la configuration de base par une configuration dépendante de l’environnement de déploiement.</span><span class="sxs-lookup"><span data-stu-id="f940d-184">The docker-compose.override.yml file, as its name suggests, contains configuration settings that override the base configuration, such as configuration that depends on the deployment environment.</span></span> <span data-ttu-id="f940d-185">Vous pouvez également avoir plusieurs fichiers de substitution avec des noms différents.</span><span class="sxs-lookup"><span data-stu-id="f940d-185">You can have multiple override files with different names also.</span></span> <span data-ttu-id="f940d-186">Les fichiers de substitution contiennent généralement des informations supplémentaires nécessaires à l’application mais spécifiques à un environnement ou un déploiement.</span><span class="sxs-lookup"><span data-stu-id="f940d-186">The override files usually contain additional information needed by the application but specific to an environment or to a deployment.</span></span>

#### <a name="targeting-multiple-environments"></a><span data-ttu-id="f940d-187">Ciblage de plusieurs environnements</span><span class="sxs-lookup"><span data-stu-id="f940d-187">Targeting multiple environments</span></span>

<span data-ttu-id="f940d-188">Il est courant de définir plusieurs fichiers Compose pour cibler plusieurs environnements : production, préproduction, intégration continue (CI) ou développement, par exemple.</span><span class="sxs-lookup"><span data-stu-id="f940d-188">A typical use case is when you define multiple compose files so you can target multiple environments, like production, staging, CI, or development.</span></span> <span data-ttu-id="f940d-189">Pour permettre la prise en charge de ces différences, vous pouvez scinder votre configuration Compose en plusieurs fichiers, comme le montre la figure 8-12.</span><span class="sxs-lookup"><span data-stu-id="f940d-189">To support these differences, you can split your Compose configuration into multiple files, as shown in Figure 8-12.</span></span>

![](./media/image13.png)

<span data-ttu-id="f940d-190">**Figure 8-12**.</span><span class="sxs-lookup"><span data-stu-id="f940d-190">**Figure 8-12**.</span></span> <span data-ttu-id="f940d-191">Plusieurs fichiers docker-compose remplaçant des valeurs du fichier docker-compose.yml de base</span><span class="sxs-lookup"><span data-stu-id="f940d-191">Multiple docker-compose files overriding values in the base docker-compose.yml file</span></span>

<span data-ttu-id="f940d-192">Vous commencez avec le fichier docker-compose.yml de base.</span><span class="sxs-lookup"><span data-stu-id="f940d-192">You start with the base docker-compose.yml file.</span></span> <span data-ttu-id="f940d-193">Ce fichier de base doit contenir les paramètres de configuration de base ou statiques qui ne changent pas en fonction de l’environnement.</span><span class="sxs-lookup"><span data-stu-id="f940d-193">This base file has to contain the base or static configuration settings that do not change depending on the environment.</span></span> <span data-ttu-id="f940d-194">Par exemple, eShopOnContainers contient le fichier de base docker-compose.yml suivant.</span><span class="sxs-lookup"><span data-stu-id="f940d-194">For example, the eShopOnContainers has the following docker-compose.yml file as the base file.</span></span>

```yml
#docker-compose.yml (Base)
version: '3'
services:
  basket.api:
    image: eshop/basket.api:${TAG:-latest}
    build:
      context: ./src/Services/Basket/Basket.API
      dockerfile: Dockerfile    
    depends_on:
      - basket.data
      - identity.api
      - rabbitmq

  catalog.api:
    image: eshop/catalog.api:${TAG:-latest}
    build:
      context: ./src/Services/Catalog/Catalog.API
      dockerfile: Dockerfile    
    depends_on:
      - sql.data
      - rabbitmq

  marketing.api:
    image: eshop/marketing.api:${TAG:-latest}
    build:
      context: ./src/Services/Marketing/Marketing.API
      dockerfile: Dockerfile    
    depends_on:
      - sql.data
      - nosql.data
      - identity.api
      - rabbitmq

  webmvc:
    image: eshop/webmvc:${TAG:-latest}
    build:
      context: ./src/Web/WebMVC
      dockerfile: Dockerfile    
    depends_on:
      - catalog.api
      - ordering.api
      - identity.api
      - basket.api
      - marketing.api

  sql.data:
    image: microsoft/mssql-server-linux:2017-latest

  nosql.data:
    image: mongo

  basket.data:
    image: redis
      
  rabbitmq:
    image: rabbitmq:3-management

```

<span data-ttu-id="f940d-195">Les valeurs du fichier docker-compose.yml de base ne doivent pas changer malgré les différents environnements de déploiement cibles.</span><span class="sxs-lookup"><span data-stu-id="f940d-195">The values in the base docker-compose.yml file should not change because of different target deployment environments.</span></span>

<span data-ttu-id="f940d-196">Si vous vous concentrez sur la définition de service webmvc, par exemple, vous pouvez constater que les informations sont les mêmes, quel que soit l’environnement ciblé.</span><span class="sxs-lookup"><span data-stu-id="f940d-196">If you focus on the webmvc service definition, for instance, you can see how that information is much the same no matter what environment you might be targeting.</span></span> <span data-ttu-id="f940d-197">Vous disposez des informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f940d-197">You have the following information:</span></span>

-   <span data-ttu-id="f940d-198">Nom du service : webmvc</span><span class="sxs-lookup"><span data-stu-id="f940d-198">The service name: webmvc.</span></span>

-   <span data-ttu-id="f940d-199">Image personnalisée du conteneur : eshop/webmvc</span><span class="sxs-lookup"><span data-stu-id="f940d-199">The container’s custom image: eshop/webmvc.</span></span>

-   <span data-ttu-id="f940d-200">Commande de génération de l’image Docker personnalisée, indiquant quel fichier Docker utiliser</span><span class="sxs-lookup"><span data-stu-id="f940d-200">The command to build the custom Docker image, indicating which Dockerfile to use.</span></span>

-   <span data-ttu-id="f940d-201">Dépendances avec d’autres services, pour empêcher ce conteneur de démarrer avant les autres conteneurs de dépendances</span><span class="sxs-lookup"><span data-stu-id="f940d-201">Dependencies on other services, so this container does not start until the other dependency containers have started.</span></span>

<span data-ttu-id="f940d-202">Vous pouvez avoir une configuration supplémentaire, mais le point important est que le fichier docker-compose.yml de base vous sert simplement à définir les informations communes aux environnements.</span><span class="sxs-lookup"><span data-stu-id="f940d-202">You can have additional configuration, but the important point is that in the base docker-compose.yml file, you just want to set the information that is common across environments.</span></span> <span data-ttu-id="f940d-203">Ensuite, dans le fichier docker-compose.override.yml ou les fichiers similaires de production ou de préproduction, vous devez placer une configuration spécifique à chaque environnement.</span><span class="sxs-lookup"><span data-stu-id="f940d-203">Then in the docker-compose.override.yml or similar files for production or staging, you should place configuration that is specific for each environment.</span></span>

<span data-ttu-id="f940d-204">En règle générale, le fichier docker-compose.override.yml est utilisé pour votre environnement de développement, comme dans l’exemple suivant d’eShopOnContainers :</span><span class="sxs-lookup"><span data-stu-id="f940d-204">Usually, the docker-compose.override.yml is used for your development environment, as in the following example from eShopOnContainers:</span></span>

```yml
#docker-compose.override.yml (Extended config for DEVELOPMENT env.)
version: '3'

services: 
# Simplified number of services here: 
      
  basket.api:
    environment:
      - ASPNETCORE_ENVIRONMENT=Development
      - ASPNETCORE_URLS=http://0.0.0.0:80
      - ConnectionString=${ESHOP_AZURE_REDIS_BASKET_DB:-basket.data}
      - identityUrl=http://identity.api              
      - IdentityUrlExternal=http://${ESHOP_EXTERNAL_DNS_NAME_OR_IP}:5105
      - EventBusConnection=${ESHOP_AZURE_SERVICE_BUS:-rabbitmq}
      - EventBusUserName=${ESHOP_SERVICE_BUS_USERNAME}
      - EventBusPassword=${ESHOP_SERVICE_BUS_PASSWORD}      
      - AzureServiceBusEnabled=False
      - ApplicationInsights__InstrumentationKey=${INSTRUMENTATION_KEY}
      - OrchestratorType=${ORCHESTRATOR_TYPE}
      - UseLoadTest=${USE_LOADTEST:-False}

    ports:
      - "5103:80"

  catalog.api:
    environment:
      - ASPNETCORE_ENVIRONMENT=Development
      - ASPNETCORE_URLS=http://0.0.0.0:80
      - ConnectionString=${ESHOP_AZURE_CATALOG_DB:-Server=sql.data;Database=Microsoft.eShopOnContainers.Services.CatalogDb;User Id=sa;Password=Pass@word}
      - PicBaseUrl=${ESHOP_AZURE_STORAGE_CATALOG_URL:-http://localhost:5101/api/v1/catalog/items/[0]/pic/}   
      - EventBusConnection=${ESHOP_AZURE_SERVICE_BUS:-rabbitmq}
      - EventBusUserName=${ESHOP_SERVICE_BUS_USERNAME}
      - EventBusPassword=${ESHOP_SERVICE_BUS_PASSWORD}         
      - AzureStorageAccountName=${ESHOP_AZURE_STORAGE_CATALOG_NAME}
      - AzureStorageAccountKey=${ESHOP_AZURE_STORAGE_CATALOG_KEY}
      - UseCustomizationData=True
      - AzureServiceBusEnabled=False
      - AzureStorageEnabled=False
      - ApplicationInsights__InstrumentationKey=${INSTRUMENTATION_KEY}
      - OrchestratorType=${ORCHESTRATOR_TYPE}
    ports:
      - "5101:80"

  marketing.api:
    environment:
      - ASPNETCORE_ENVIRONMENT=Development
      - ASPNETCORE_URLS=http://0.0.0.0:80
      - ConnectionString=${ESHOP_AZURE_MARKETING_DB:-Server=sql.data;Database=Microsoft.eShopOnContainers.Services.MarketingDb;User Id=sa;Password=Pass@word}
      - MongoConnectionString=${ESHOP_AZURE_COSMOSDB:-mongodb://nosql.data}
      - MongoDatabase=MarketingDb
      - EventBusConnection=${ESHOP_AZURE_SERVICE_BUS:-rabbitmq}
      - EventBusUserName=${ESHOP_SERVICE_BUS_USERNAME}
      - EventBusPassword=${ESHOP_SERVICE_BUS_PASSWORD}          
      - identityUrl=http://identity.api              
      - IdentityUrlExternal=http://${ESHOP_EXTERNAL_DNS_NAME_OR_IP}:5105
      - CampaignDetailFunctionUri=${ESHOP_AZUREFUNC_CAMPAIGN_DETAILS_URI}
      - PicBaseUrl=${ESHOP_AZURE_STORAGE_MARKETING_URL:-http://localhost:5110/api/v1/campaigns/[0]/pic/}
      - AzureStorageAccountName=${ESHOP_AZURE_STORAGE_MARKETING_NAME}
      - AzureStorageAccountKey=${ESHOP_AZURE_STORAGE_MARKETING_KEY}
      - AzureServiceBusEnabled=False
      - AzureStorageEnabled=False
      - ApplicationInsights__InstrumentationKey=${INSTRUMENTATION_KEY}
      - OrchestratorType=${ORCHESTRATOR_TYPE}
      - UseLoadTest=${USE_LOADTEST:-False}
    ports:
      - "5110:80"

  webmvc:
    environment:
      - ASPNETCORE_ENVIRONMENT=Development
      - ASPNETCORE_URLS=http://0.0.0.0:80
      - CatalogUrl=http://catalog.api
      - OrderingUrl=http://ordering.api
      - BasketUrl=http://basket.api
      - LocationsUrl=http://locations.api
      - IdentityUrl=http://10.0.75.1:5105
      - MarketingUrl=http://marketing.api                                                    
      - CatalogUrlHC=http://catalog.api/hc
      - OrderingUrlHC=http://ordering.api/hc
      - IdentityUrlHC=http://identity.api/hc     
      - BasketUrlHC=http://basket.api/hc
      - MarketingUrlHC=http://marketing.api/hc
      - PaymentUrlHC=http://payment.api/hc
      - UseCustomizationData=True
      - ApplicationInsights__InstrumentationKey=${INSTRUMENTATION_KEY}
      - OrchestratorType=${ORCHESTRATOR_TYPE}
      - UseLoadTest=${USE_LOADTEST:-False}
    ports:
      - "5100:80"
  sql.data:
    environment:
      - MSSQL_SA_PASSWORD=Pass@word
      - ACCEPT_EULA=Y
      - MSSQL_PID=Developer
    ports:
      - "5433:1433"
  nosql.data:
    ports:
      - "27017:27017"
  basket.data:
    ports:
      - "6379:6379"      
  rabbitmq:
    ports:
      - "15672:15672"
      - "5672:5672"

```

<span data-ttu-id="f940d-205">Dans cet exemple, la configuration de substitution de l’environnement de développement expose certains ports à l’hôte, définit les variables d’environnement à l’aide d’URL de redirection et spécifie les chaînes de connexion de l’environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="f940d-205">In this example, the development override configuration exposes some ports to the host, defines environment variables with redirect URLs, and specifies connection strings for the development environment.</span></span> <span data-ttu-id="f940d-206">Ces paramètres concernent juste l’environnement de développement.</span><span class="sxs-lookup"><span data-stu-id="f940d-206">These settings are all just for the development environment.</span></span>

<span data-ttu-id="f940d-207">Quand vous exécutez `docker-compose up`, ou quand vous lancez cette commande à partir de Visual Studio, elle lit automatiquement les remplacements comme si elle fusionnait les deux fichiers.</span><span class="sxs-lookup"><span data-stu-id="f940d-207">When you run `docker-compose up` (or launch it from Visual Studio), the command reads the overrides automatically as if it were merging both files.</span></span>

<span data-ttu-id="f940d-208">Supposons que vous souhaitiez un autre fichier Compose pour l’environnement de production, avec d’autres valeurs de configuration, ports ou chaînes de connexion.</span><span class="sxs-lookup"><span data-stu-id="f940d-208">Suppose that you want another Compose file for the production environment, with different configuration values, ports or connection strings.</span></span> <span data-ttu-id="f940d-209">Vous pouvez créer un autre fichier de substitution, par exemple le fichier nommé `docker-compose.prod.yml`, avec d’autres paramètres et variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="f940d-209">You can create another override file, like file named `docker-compose.prod.yml` with different settings and environment variables.</span></span>  <span data-ttu-id="f940d-210">Ce fichier peut être stocké dans un autre dépôt Git, ou être géré et sécurisé par une autre équipe.</span><span class="sxs-lookup"><span data-stu-id="f940d-210">That file might be stored in a different Git repo or managed and secured by a different team.</span></span>

#### <a name="how-to-deploy-with-a-specific-override-file"></a><span data-ttu-id="f940d-211">Comment effectuer un déploiement avec un fichier de substitution spécifique</span><span class="sxs-lookup"><span data-stu-id="f940d-211">How to deploy with a specific override file</span></span>

<span data-ttu-id="f940d-212">Pour utiliser plusieurs fichiers de substitution ou un fichier de substitution avec un autre nom, vous pouvez spécifier l’option -f avec la commande docker-compose et les fichiers souhaités.</span><span class="sxs-lookup"><span data-stu-id="f940d-212">To use multiple override files, or an override file with a different name, you can use the -f option with the docker-compose command and specify the files.</span></span> <span data-ttu-id="f940d-213">Compose fusionne les fichiers dans l’ordre indiqué sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f940d-213">Compose merges files in the order they are specified on the command line.</span></span> <span data-ttu-id="f940d-214">L’exemple suivant montre comment effectuer un déploiement avec des fichiers de substitution.</span><span class="sxs-lookup"><span data-stu-id="f940d-214">The following example shows how to deploy with override files.</span></span>

```
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d
```

#### <a name="using-environment-variables-in-docker-compose-files"></a><span data-ttu-id="f940d-215">Utilisation de variables d’environnement dans les fichiers docker-compose</span><span class="sxs-lookup"><span data-stu-id="f940d-215">Using environment variables in docker-compose files</span></span>

<span data-ttu-id="f940d-216">Il est pratique, surtout dans les environnements de production, d’obtenir des informations de configuration à partir de variables d’environnement, comme nous l’avons montré dans les exemples précédents.</span><span class="sxs-lookup"><span data-stu-id="f940d-216">It is convenient, especially in production environments, to be able to get configuration information from environment variables, as we have shown in previous examples.</span></span> <span data-ttu-id="f940d-217">Vous référencez une variable d’environnement dans vos fichiers docker-compose à l’aide de la syntaxe \${MY\_VAR}.</span><span class="sxs-lookup"><span data-stu-id="f940d-217">You reference an environment variable in your docker-compose files using the syntax \${MY\_VAR}.</span></span> <span data-ttu-id="f940d-218">La ligne suivante d’un fichier docker-compose.prod.yml montre comment référencer la valeur d’une variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="f940d-218">The following line from a docker-compose.prod.yml file shows how to reference the value of an environment variable.</span></span>

```yml
IdentityUrl=http://${ESHOP_PROD_EXTERNAL_DNS_NAME_OR_IP}:5105
```

<span data-ttu-id="f940d-219">Les variables d’environnement sont créées et initialisées de différentes manières, en fonction de votre environnement hôte (Linux, Windows, cluster Cloud, etc.).</span><span class="sxs-lookup"><span data-stu-id="f940d-219">Environment variables are created and initialized in different ways, depending on your host environment (Linux, Windows, Cloud cluster, etc.).</span></span> <span data-ttu-id="f940d-220">Toutefois, une approche pratique consiste à utiliser un fichier .env.</span><span class="sxs-lookup"><span data-stu-id="f940d-220">However, a convenient approach is to use an .env file.</span></span> <span data-ttu-id="f940d-221">Les fichiers docker-compose prennent en charge la déclaration de variables d’environnement par défaut dans le fichier .env.</span><span class="sxs-lookup"><span data-stu-id="f940d-221">The docker-compose files support declaring default environment variables in the .env file.</span></span> <span data-ttu-id="f940d-222">Ces valeurs de variables d’environnement sont les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="f940d-222">These values for the environment variables are the default values.</span></span> <span data-ttu-id="f940d-223">Toutefois, elles peuvent être remplacées par les valeurs que vous avez définies dans chacun de vos environnements (OS hôte ou variables d’environnement de votre cluster).</span><span class="sxs-lookup"><span data-stu-id="f940d-223">But they can be overridden by the values you might have defined in each of your environments (host OS or environment variables from your cluster).</span></span> <span data-ttu-id="f940d-224">Vous placez ce fichier .env dans le dossier à partir duquel la commande docker-compose est exécutée.</span><span class="sxs-lookup"><span data-stu-id="f940d-224">You place this .env file in the folder where the docker-compose command is executed from.</span></span>

<span data-ttu-id="f940d-225">L’exemple suivant illustre un fichier .env semblable au fichier [.env](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/.env) de l’application eShopOnContainers.</span><span class="sxs-lookup"><span data-stu-id="f940d-225">The following example shows an .env file like the [.env](https://github.com/dotnet-architecture/eShopOnContainers/blob/master/.env) file for the eShopOnContainers application.</span></span>

```
# .env file

ESHOP_EXTERNAL_DNS_NAME_OR_IP=localhost

ESHOP_PROD_EXTERNAL_DNS_NAME_OR_IP=10.121.122.92
```

<span data-ttu-id="f940d-226">Docker-compose s’attend à ce que chaque ligne d’un fichier .env soit au format &lt;variable&gt;=&lt;valeurs&gt;.</span><span class="sxs-lookup"><span data-stu-id="f940d-226">Docker-compose expects each line in an .env file to be in the format &lt;variable&gt;=&lt;value&gt;.</span></span>

<span data-ttu-id="f940d-227">Notez que les valeurs définies dans l’environnement d’exécution remplacent toujours les valeurs définies dans le fichier .env.</span><span class="sxs-lookup"><span data-stu-id="f940d-227">Note that the values set in the runtime environment always override the values defined inside the .env file.</span></span> <span data-ttu-id="f940d-228">De même, les valeurs passées via les arguments de ligne de commande remplacent également les valeurs par défaut définies dans le fichier .env.</span><span class="sxs-lookup"><span data-stu-id="f940d-228">In a similar way, values passed via command-line command arguments also override the default values set in the .env file.</span></span>

#### <a name="additional-resources"></a><span data-ttu-id="f940d-229">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f940d-229">Additional resources</span></span>

-   <span data-ttu-id="f940d-230">**Vue d’ensemble de Docker Compose**
    [*https://docs.docker.com/compose/overview/*](https://docs.docker.com/compose/overview/)</span><span class="sxs-lookup"><span data-stu-id="f940d-230">**Overview of Docker Compose**
[*https://docs.docker.com/compose/overview/*](https://docs.docker.com/compose/overview/)</span></span>

-   <span data-ttu-id="f940d-231">**Fichiers Compose multiples**
    [*https://docs.docker.com/compose/extends/\#multiple-compose-files*](https://docs.docker.com/compose/extends/#multiple-compose-files)</span><span class="sxs-lookup"><span data-stu-id="f940d-231">**Multiple Compose files**
[*https://docs.docker.com/compose/extends/\#multiple-compose-files*](https://docs.docker.com/compose/extends/#multiple-compose-files)</span></span>

### <a name="building-optimized-aspnet-core-docker-images"></a><span data-ttu-id="f940d-232">Génération d’images Docker ASP.NET Core optimisées</span><span class="sxs-lookup"><span data-stu-id="f940d-232">Building optimized ASP.NET Core Docker images</span></span>

<span data-ttu-id="f940d-233">Si vous recherchez des sources relatives à Docker et .NET Core sur Internet, vous trouverez des fichiers Docker qui illustrent la simplicité de la génération d’une image Docker. En effet, il vous suffit de copier votre source dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="f940d-233">If you are exploring Docker and .NET Core on sources on the Internet, you will find Dockerfiles that demonstrate the simplicity of building a Docker image by copying your source into a container.</span></span> <span data-ttu-id="f940d-234">Ces exemples suggèrent qu’à l’aide d’une configuration toute simple, vous pouvez disposer d’une image Docker où l’environnement et votre application font partie d’un même package.</span><span class="sxs-lookup"><span data-stu-id="f940d-234">These examples suggest that by using a simple configuration, you can have a Docker image with the environment packaged with your application.</span></span> <span data-ttu-id="f940d-235">L’exemple suivant montre un fichier Docker de ce genre.</span><span class="sxs-lookup"><span data-stu-id="f940d-235">The following example shows a simple Dockerfile in this vein.</span></span>

```
FROM microsoft/dotnet

WORKDIR /app

ENV ASPNETCORE_URLS http://+:80

EXPOSE 80

COPY . .

RUN dotnet restore

ENTRYPOINT ["dotnet", "run"]
```

<span data-ttu-id="f940d-236">Un fichier Docker comme celui-ci va fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="f940d-236">A Dockerfile like this will work.</span></span> <span data-ttu-id="f940d-237">Toutefois, vous pouvez considérablement optimiser vos images, en particulier vos images de production.</span><span class="sxs-lookup"><span data-stu-id="f940d-237">However, you can substantially optimize your images, especially your production images.</span></span>

<span data-ttu-id="f940d-238">Dans le modèle reposant sur un conteneur et des microservices, vous démarrez constamment des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="f940d-238">In the container and microservices model, you are constantly starting containers.</span></span> <span data-ttu-id="f940d-239">En règle générale, l’utilisation de conteneurs n’entraîne pas le redémarrage d’un conteneur en veille, car le conteneur peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="f940d-239">The typical way of using containers does not restart a sleeping container, because the container is disposable.</span></span> <span data-ttu-id="f940d-240">Les orchestrateurs (comme Docker Swarm, Kubernetes, DCOS ou Azure Service Fabric) créent simplement des instances d’images.</span><span class="sxs-lookup"><span data-stu-id="f940d-240">Orchestrators (like Docker Swarm, Kubernetes, DCOS or Azure Service Fabric) simply create new instances of images.</span></span> <span data-ttu-id="f940d-241">Cela signifie que vous devez effectuer une optimisation en précompilant l’application au moment de sa génération pour accélérer le processus d’instanciation.</span><span class="sxs-lookup"><span data-stu-id="f940d-241">What this means is that you would need to optimize by precompiling the application when it is built so the instantiation process will be faster.</span></span> <span data-ttu-id="f940d-242">Une fois que le conteneur a démarré, il est prêt à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="f940d-242">When the container is started, it should be ready to run.</span></span> <span data-ttu-id="f940d-243">N’effectuez pas d’opérations de restauration ou de compilation au moment de l’exécution, à l’aide des commandes dotnet restore et dotnet build via l’interface en ligne de commande dotnet CLI, comme cela est indiqué dans de nombreux billets de blog sur .NET Core et Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-243">You should not restore and compile at run time, using dotnet restore and dotnet build commands from the dotnet CLI that, as you see in many blog posts about .NET Core and Docker.</span></span>

<span data-ttu-id="f940d-244">L’équipe .NET a effectué un travail important pour faire de .NET Core et d’ASP.NET Core un framework optimisé pour les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="f940d-244">The .NET team has been doing important work to make .NET Core and ASP.NET Core a container-optimized framework.</span></span> <span data-ttu-id="f940d-245">.NET Core n’est pas seulement un framework léger avec un faible encombrement mémoire. L’équipe s’est concentrée sur le niveau de performance de démarrage et a produit des images Docker optimisées, par exemple l’image [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) disponible sur [Docker Hub](https://hub.docker.com/r/microsoft/aspnetcore/), en comparaison des images [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) ou [microsoft/nanoserver](https://github.com/dotnet/dotnet-docker/blob/master/1.0/nanoserver/runtime/Dockerfile) classiques.</span><span class="sxs-lookup"><span data-stu-id="f940d-245">Not only is .NET Core a lightweight framework with a small memory footprint; the team has focused on startup performance and produced some optimized Docker images, like the [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) image available at [Docker Hub](https://hub.docker.com/r/microsoft/aspnetcore/), in comparison to the regular [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) or [microsoft/nanoserver](https://github.com/dotnet/dotnet-docker/blob/master/1.0/nanoserver/runtime/Dockerfile) images.</span></span> <span data-ttu-id="f940d-246">L’image [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) affecte automatiquement à aspnetcore\_urls le port 80, et définit le cache d’assemblys préalable à l’exécution de ngen. Ces deux paramètres entraînent un démarrage plus rapide.</span><span class="sxs-lookup"><span data-stu-id="f940d-246">The [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) image provides automatic setting of aspnetcore\_urls to port 80 and the pre-ngend cache of assemblies; both of these settings result in faster startup.</span></span>

#### <a name="additional-resources"></a><span data-ttu-id="f940d-247">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f940d-247">Additional resources</span></span>

-   <span data-ttu-id="f940d-248">**Génération d’images Docker optimisées avec ASP.NET Core**
    [*https://blogs.msdn.microsoft.com/stevelasker/2016/09/29/building-optimized-docker-images-with-asp-net-core/*](https://blogs.msdn.microsoft.com/stevelasker/2016/09/29/building-optimized-docker-images-with-asp-net-core/)</span><span class="sxs-lookup"><span data-stu-id="f940d-248">**Building Optimized Docker Images with ASP.NET Core**
[*https://blogs.msdn.microsoft.com/stevelasker/2016/09/29/building-optimized-docker-images-with-asp-net-core/*](https://blogs.msdn.microsoft.com/stevelasker/2016/09/29/building-optimized-docker-images-with-asp-net-core/)</span></span>

### <a name="building-the-application-from-a-build-ci-container"></a><span data-ttu-id="f940d-249">Génération de l’application à partir d’un conteneur de build (intégration continue)</span><span class="sxs-lookup"><span data-stu-id="f940d-249">Building the application from a build (CI) container</span></span>

<span data-ttu-id="f940d-250">Docker présente un autre avantage : il vous permet de générer votre application à partir d’un conteneur préconfiguré, comme le montre la figure 8-13, ce qui vous évite de créer une machine de build ou une machine virtuelle pour générer votre application.</span><span class="sxs-lookup"><span data-stu-id="f940d-250">Another benefit of Docker is that you can build your application from a preconfigured container, as shown in Figure 8-13, so you do not need to create a build machine or VM to build your application.</span></span> <span data-ttu-id="f940d-251">Vous pouvez utiliser ou tester ce conteneur de build en l’exécutant sur votre machine de développement.</span><span class="sxs-lookup"><span data-stu-id="f940d-251">You can use or test that build container by running it at your development machine.</span></span> <span data-ttu-id="f940d-252">Mais voici le plus intéressant : vous pouvez utiliser le même conteneur de build à partir de votre pipeline d’intégration continue (CI).</span><span class="sxs-lookup"><span data-stu-id="f940d-252">But what is even more interesting is that you can use the same build container from your CI (Continuous Integration) pipeline.</span></span>

![](./media/image14.png)

<span data-ttu-id="f940d-253">**Figure 8-13**.</span><span class="sxs-lookup"><span data-stu-id="f940d-253">**Figure 8-13**.</span></span> <span data-ttu-id="f940d-254">Conteneur de build Docker compilant vos fichiers binaires .NET</span><span class="sxs-lookup"><span data-stu-id="f940d-254">Docker build-container compiling your .NET binaries</span></span> 

<span data-ttu-id="f940d-255">Pour ce scénario, nous fournissons l’image [microsoft/aspnetcore-build](https://hub.docker.com/r/microsoft/aspnetcore-build/), qui vous permet de compiler et générer vos applications ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="f940d-255">For this scenario, we provide the [microsoft/aspnetcore-build](https://hub.docker.com/r/microsoft/aspnetcore-build/) image, which you can use to compile and build your ASP.NET Core apps.</span></span> <span data-ttu-id="f940d-256">La sortie est placée dans une image basée sur l’image [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/), qui est une image d’exécution optimisée, comme nous l’avons déjà indiqué.</span><span class="sxs-lookup"><span data-stu-id="f940d-256">The output is placed in an image based on the [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) image, which is an optimized runtime image, as previously noted.</span></span>

<span data-ttu-id="f940d-257">L’image aspnetcore-build contient tout ce dont vous avez besoin pour compiler une application ASP.NET Core, notamment .NET Core, le kit ASP.NET SDK, npm, Bower, Gulp, etc.</span><span class="sxs-lookup"><span data-stu-id="f940d-257">The aspnetcore-build image contains everything you need in order to compile an ASP.NET Core application, including .NET Core, the ASP.NET SDK, npm, Bower, Gulp, etc.</span></span>

<span data-ttu-id="f940d-258">Nous avons besoin de ces dépendances au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="f940d-258">We need these dependencies at build time.</span></span> <span data-ttu-id="f940d-259">Mais nous ne souhaitons pas les conserver avec l’application au moment de l’exécution, car cela augmente inutilement la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="f940d-259">But we do not want to carry these with the application at runtime, because it would make the image unnecessarily large.</span></span> <span data-ttu-id="f940d-260">Dans l’application eShopOnContainers, vous pouvez générer l’application à partir d’un conteneur en exécutant simplement la commande docker-compose suivante.</span><span class="sxs-lookup"><span data-stu-id="f940d-260">In the eShopOnContainers application, you can build the application from a container by just running the following docker-compose command.</span></span>

```
  docker-compose -f docker-compose.ci.build.yml up
```

<span data-ttu-id="f940d-261">La figure 8-14 montre l’exécution de cette commande sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f940d-261">Figure 8-14 shows this command running at the command line.</span></span>

![](./media/image15.png)

<span data-ttu-id="f940d-262">**Figure 8-14.**</span><span class="sxs-lookup"><span data-stu-id="f940d-262">**Figure 8-14.**</span></span> <span data-ttu-id="f940d-263">Génération de votre application .NET à partir d’un conteneur</span><span class="sxs-lookup"><span data-stu-id="f940d-263">Building your .NET application from a container</span></span>

<span data-ttu-id="f940d-264">Comme vous pouvez le voir, le conteneur en cours d’exécution est le conteneur ci-build\_1.</span><span class="sxs-lookup"><span data-stu-id="f940d-264">As you can see, the container that is running is the ci-build\_1 container.</span></span> <span data-ttu-id="f940d-265">Ceci est basé sur l’image aspnetcore-build pour permettre la compilation et la génération de l’ensemble de votre application depuis le conteneur au lieu de votre PC.</span><span class="sxs-lookup"><span data-stu-id="f940d-265">This is based on the aspnetcore-build image so that it can compile and build your whole application from within that container instead of from your PC.</span></span> <span data-ttu-id="f940d-266">C’est pourquoi, en réalité, la génération et la compilation des projets .NET Core sont effectuées dans Linux, car ce conteneur est exécuté sur l’hôte Docker Linux par défaut.</span><span class="sxs-lookup"><span data-stu-id="f940d-266">That is why in reality it is building and compiling the .NET Core projects in Linux—because that container is running on the default Docker Linux host.</span></span>

<span data-ttu-id="f940d-267">Le fichier [docker-compose.ci.build.yml](https://github.com/dotnet/eShopOnContainers/blob/master/docker-compose.ci.build.yml) de cette image (provenant d’eShopOnContainers) contient le code suivant.</span><span class="sxs-lookup"><span data-stu-id="f940d-267">The [docker-compose.ci.build.yml](https://github.com/dotnet/eShopOnContainers/blob/master/docker-compose.ci.build.yml) file for that image (part of eShopOnContainers) contains the following code.</span></span> <span data-ttu-id="f940d-268">Vous pouvez voir qu’il démarre un conteneur de build à l’aide de l’image [microsoft/aspnetcore-build](https://hub.docker.com/r/microsoft/aspnetcore-build/).</span><span class="sxs-lookup"><span data-stu-id="f940d-268">You can see that it starts a build container using the [microsoft/aspnetcore-build](https://hub.docker.com/r/microsoft/aspnetcore-build/) image.</span></span>

```yml
version: '3'

services:

  ci-build:

    image: microsoft/aspnetcore-build:2.0

    volumes:
      - .:/src

    working_dir: /src

    command: /bin/bash -c "pushd ./src/Web/WebSPA && npm rebuild node-sass && popd && dotnet restore ./eShopOnContainers-ServicesAndWebApps.sln && dotnet publish ./eShopOnContainers-ServicesAndWebApps.sln -c Release -o ./obj/Docker/publish"

```

* <span data-ttu-id="f940d-269">À partir de **.NET Core 2.0**, la commande `dotnet restore` s’exécute automatiquement quand la commande `dotnet publish` est exécutée.</span><span class="sxs-lookup"><span data-stu-id="f940d-269">Starting with **.NET Core 2.0**, `dotnet restore` command executes automatically when the `dotnet publish` command is executed.</span></span>

<span data-ttu-id="f940d-270">Une fois que le conteneur de build est opérationnel, il exécute les commandes dotnet restore et dotnet publish du kit .NET SDK sur tous les projets de la solution pour compiler les bits .NET.</span><span class="sxs-lookup"><span data-stu-id="f940d-270">Once the build container is up and running, it runs the .NET SDK dotnet restore and dotnet publish commands against all the projects in the solution in order to compile the .NET bits.</span></span> <span data-ttu-id="f940d-271">Dans ce cas, eShopOnContainers dispose également d’un SPA basé sur TypeScript et Angular pour le code client. Il doit également vérifier les dépendances JavaScript avec npm, mais cette action n’est pas liée aux bits .NET.</span><span class="sxs-lookup"><span data-stu-id="f940d-271">In this case, because eShopOnContainers also has an SPA based on TypeScript and Angular for the client code, it also needs to check JavaScript dependencies with npm, but that action is not related to the .NET bits.</span></span>

<span data-ttu-id="f940d-272">La commande dotnet publish génère et publie la sortie compilée du dossier de chaque projet sur le dossier ../obj/Docker/publish, comme le montre la figure 8-15.</span><span class="sxs-lookup"><span data-stu-id="f940d-272">The dotnet publish command builds and publishes the compiled output within each project’s folder to the ../obj/Docker/publish folder, as shown in Figure 8-15.</span></span>

![](./media/image16.png)

<span data-ttu-id="f940d-273">**Figure 8-15.**</span><span class="sxs-lookup"><span data-stu-id="f940d-273">**Figure 8-15.**</span></span> <span data-ttu-id="f940d-274">Fichiers binaires générés par la commande dotnet publish</span><span class="sxs-lookup"><span data-stu-id="f940d-274">Binary files generated by the dotnet publish command</span></span>

#### <a name="creating-the-docker-images-from-the-cli"></a><span data-ttu-id="f940d-275">Création des images Docker à partir de l’interface CLI</span><span class="sxs-lookup"><span data-stu-id="f940d-275">Creating the Docker images from the CLI</span></span>

<span data-ttu-id="f940d-276">Une fois que la sortie de l’application est publiée sur les dossiers correspondants (dans chaque projet), l’étape suivante consiste à générer les images Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-276">Once the application output is published to the related folders (within each project), the next step is to actually build the Docker images.</span></span> <span data-ttu-id="f940d-277">Pour ce faire, utilisez les commandes docker-compose build et docker-compose up, comme illustré dans la figure 8-16.</span><span class="sxs-lookup"><span data-stu-id="f940d-277">To do this, you use the docker-compose build and docker-compose up commands, as shown in Figure 8-16.</span></span>

![](./media/image17.png)

<span data-ttu-id="f940d-278">**Figure 8-16.**</span><span class="sxs-lookup"><span data-stu-id="f940d-278">**Figure 8-16.**</span></span> <span data-ttu-id="f940d-279">Génération d’images Docker et exécution des conteneurs</span><span class="sxs-lookup"><span data-stu-id="f940d-279">Building Docker images and running the containers</span></span>

<span data-ttu-id="f940d-280">Dans la figure 8-17, vous pouvez voir comment fonctionne la commande docker-compose build.</span><span class="sxs-lookup"><span data-stu-id="f940d-280">In Figure 8-17, you can see how the docker-compose build command runs.</span></span>

![](./media/image18.png)

<span data-ttu-id="f940d-281">**Figure 8-17**.</span><span class="sxs-lookup"><span data-stu-id="f940d-281">**Figure 8-17**.</span></span> <span data-ttu-id="f940d-282">Génération des images Docker à l’aide de la commande docker-compose build</span><span class="sxs-lookup"><span data-stu-id="f940d-282">Building the Docker images with the docker-compose build command</span></span>

<span data-ttu-id="f940d-283">La différence entre les commandes docker-compose build et docker-compose up vient du fait que docker-compose up génère et démarre les images.</span><span class="sxs-lookup"><span data-stu-id="f940d-283">The difference between the docker-compose build and docker-compose up commands is that docker-compose up both builds and starts the images.</span></span>

<span data-ttu-id="f940d-284">Quand vous utilisez Visual Studio, toutes ces étapes sont effectuées de manière interne.</span><span class="sxs-lookup"><span data-stu-id="f940d-284">When you use Visual Studio, all these steps are performed under the covers.</span></span> <span data-ttu-id="f940d-285">Visual Studio compile votre application .NET, crée les images Docker et déploie les conteneurs sur l’hôte Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-285">Visual Studio compiles your .NET application, creates the Docker images, and deploys the containers into the Docker host.</span></span> <span data-ttu-id="f940d-286">Visual Studio offre des fonctionnalités supplémentaires, par exemple déboguer directement vos conteneurs s’exécutant dans Docker.</span><span class="sxs-lookup"><span data-stu-id="f940d-286">Visual Studio offers additional features, like the ability to debug your containers running in Docker, directly from Visual Studio.</span></span>

<span data-ttu-id="f940d-287">Ainsi, vous pouvez générer votre application en procédant de la même façon que votre pipeline d’intégration continue/de livraison continue : à partir d’un conteneur et non d’une machine locale.</span><span class="sxs-lookup"><span data-stu-id="f940d-287">The overall takeway here is that you are able to build your application the same way your CI/CD pipeline should build it—from a container instead of from a local machine.</span></span> <span data-ttu-id="f940d-288">Une fois les images créées, il vous suffit d’exécuter les images Docker à l’aide de la commande docker-compose up.</span><span class="sxs-lookup"><span data-stu-id="f940d-288">After having the images created, then you just need to run the Docker images using the docker-compose up command.</span></span>

#### <a name="additional-resources"></a><span data-ttu-id="f940d-289">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f940d-289">Additional resources</span></span>

-   <span data-ttu-id="f940d-290">**Génération de bits à partir d’un conteneur : configuration de la solution eShopOnContainers dans un environnement Windows CLI (dotnet CLI, Docker CLI et VS Code)**
    [*https://github.com/dotnet/eShopOnContainers/wiki/03.-Setting-the-eShopOnContainers-solution-up-in-a-Windows-CLI-environment-(dotnet-CLI,-Docker-CLI-and-VS-Code)*](https://github.com/dotnet/eShopOnContainers/wiki/03.-Setting-the-eShopOnContainers-solution-up-in-a-Windows-CLI-environment-(dotnet-CLI,-Docker-CLI-and-VS-Code))</span><span class="sxs-lookup"><span data-stu-id="f940d-290">**Building bits from a container: Setting the eShopOnContainers solution up in a Windows CLI environment (dotnet CLI, Docker CLI and VS Code)**
[*https://github.com/dotnet/eShopOnContainers/wiki/03.-Setting-the-eShopOnContainers-solution-up-in-a-Windows-CLI-environment-(dotnet-CLI,-Docker-CLI-and-VS-Code)*](https://github.com/dotnet/eShopOnContainers/wiki/03.-Setting-the-eShopOnContainers-solution-up-in-a-Windows-CLI-environment-(dotnet-CLI,-Docker-CLI-and-VS-Code))</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="f940d-291">[Précédent] (data-driven-crud-microservice.md) [Suivant] (database-server-container.md)</span><span class="sxs-lookup"><span data-stu-id="f940d-291">[Previous] (data-driven-crud-microservice.md) [Next] (database-server-container.md)</span></span>
