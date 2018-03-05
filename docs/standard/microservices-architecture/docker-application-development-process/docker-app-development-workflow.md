---
title: "Workflow de développement des applications Docker"
description: "Architecture des microservices .NET pour les applications .NET en conteneur | Workflow de développement des applications Docker"
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 8537b1db27f512ec0bfc2f23589efe8199ca3287
ms.sourcegitcommit: c3957fdb990060559d73cca44ab3e2c7b4d049c0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2018
---
# <a name="development-workflow-for-docker-apps"></a>Workflow de développement des applications Docker

Le cycle de vie du développement d’une application débute sur une machine de développeur, là où le développeur code l’application dans le langage de son choix et où il teste localement sa nouvelle application. Quels que soient le langage, le framework et la plateforme choisis par le développeur, avec ce workflow, le développeur crée et teste toujours des conteneurs Docker, mais il le fait en local.

Chaque conteneur (instance d’une image Docker) inclut les éléments suivants :

-   Un système d’exploitation sélectionné (par exemple, une distribution Linux, Windows Nano Server ou Windows Server Core)

-   Des fichiers ajoutés par le développeur (binaires de l’application, etc.)

-   Des informations de configuration (paramètres d’environnement et dépendances)

## <a name="workflow-for-developing-docker-container-based-applications"></a>Workflow pour développer des applications basées sur des conteneurs Docker

Cette section décrit le workflow de développement de la *boucle interne* pour les applications basées sur des conteneurs Docker. Dans ce workflow de la boucle interne, le workflow DevOps plus global n’est pas pris en compte et seules les étapes de développement effectuées sur l’ordinateur du développeur sont couvertes. Les étapes initiales de configuration de l’environnement ne sont pas incluses non plus, car elles sont effectuées une seule fois.

Une application est composée de vos propres services et de bibliothèques supplémentaires (dépendances). La figure 5-1 illustre les principales étapes qu’un développeur doit généralement effectuer pour créer une application Docker.

![](./media/image1.png)

**Figure 5-1.** Workflow pas à pas pour développer des applications Docker en conteneur

Ce guide décrit tout ce processus en détail, en expliquant chacune des étapes majeures dans l’optique d’un environnement Visual Studio.

Si vous optez pour une approche de développement avec un éditeur ou une interface CLI (par exemple, Visual Studio Code plus la CLI Docker sur macOS ou Windows), vous aurez besoin de connaître toutes les étapes, sans doute de manière plus détaillée que pour Visual Studio. Pour plus d’informations sur le développement dans un environnement CLI, consultez le livre électronique [Containerized Docker Application lifecycle with Microsoft Platforms and Tools](http://aka.ms/dockerlifecycleebook/).

Si vous utilisez Visual Studio 2015 ou Visual Studio 2017, bon nombre de ces étapes sont faites à votre place, ce qui vous fait gagner énormément de temps dans votre travail. Cela est encore plus vrai si vous utilisez Visual Studio 2017 et ciblez des applications multiconteneurs. Par exemple, avec un seul clic de souris, Visual Studio ajoute les fichiers Dockerfile et docker-compose.yml à vos projets, avec la configuration de votre application. Quand vous exécutez l’application dans Visual Studio, le programme crée l’image Docker et exécute l’application multiconteneur directement dans Docker. Il vous permet même de déboguer plusieurs conteneurs à la fois. Grâce à ces fonctionnalités, vous allez développer nettement plus vite.

Toutefois, même si Visual Studio effectue ces étapes automatiquement, il est essentiel que vous compreniez les dessous de chaque étape dans Docker. C’est pourquoi nous détaillons chaque étape dans le guide qui suit.

![](./media/image2.png)

## <a name="step-1-start-coding-and-create-your-initial-application-or-service-baseline"></a>Étape 1. Commencer le codage et créer votre base de référence initiale pour l’application ou le service

Le développement d’une application se déroule de façon similaire avec ou sans Docker. La différence est que, lors du développement avec Docker, vous déployez et testez l’application ou les services exécutés dans des conteneurs Docker dans votre environnement local. Le conteneur peut être un conteneur Linux ou Windows.

### <a name="set-up-your-local-environment-with-visual-studio"></a>Configurer votre environnement local avec Visual Studio

Pour commencer, assurez-vous que [Docker Community Edition (CE)](https://www.docker.com/community-edition) pour Windows est installé, comme cela est expliqué dans les instructions suivantes :

[Get started with Docker CE for Windows](https://docs.docker.com/docker-for-windows/)

Vérifiez également que Visual Studio 2017 est installé. Nous vous recommandons d’utiliser cette version plutôt que Visual Studio 2015 avec le complément Visual Studio Tools pour Docker, car Visual Studio 2017 offre une prise en charge de Docker plus complète, notamment pour le débogage des conteneurs. Visual Studio 2017 inclut les outils pour Docker si vous avez sélectionné la charge de travail **.NET Core et Docker** au moment de son installation, comme illustré à la figure 5-2.

![](./media/image3.png)

**Figure 5-2**. Sélection de la charge de travail **.NET Core et Docker** durant l’installation de Visual Studio 2017

Vous pouvez commencer le codage de votre application en.NET brut (généralement dans .NET Core si vous envisagez d’utiliser des conteneurs) même si vous n’avez pas encore activé Docker dans votre application, ni effectuer de déploiement et de test dans Docker. Toutefois, nous vous recommandons de commencer à travailler dans Docker le plus tôt possible, car Docker sera le véritable environnement de développement, et vous pourrez détecter les problèmes éventuels dès le début. Nous le conseillons d’autant plus que Visual Studio rend l’utilisation de Docker extrêmement simple et intuitive. L’exemple le plus significatif est le débogage des applications multiconteneurs à partir de Visual Studio.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Get started with Docker CE for Windows**
    [*https://docs.docker.com/docker-for-windows/*](https://docs.docker.com/docker-for-windows/)

-   **Visual Studio 2017**
    [*https://www.visualstudio.com/downloads/*](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

![](./media/image4.png)

## <a name="step-2-create-a-dockerfile-related-to-an-existing-net-base-image"></a>Étape 2. Créer un fichier Dockerfile associé à une image de base .NET existante

Vous avez besoin d’un fichier Dockerfile pour chaque image personnalisée que vous souhaitez créer. Vous avez également besoin d’un fichier Dockerfile pour chaque conteneur à déployer, que vous choisissiez de le déployer automatiquement à partir de Visual Studio ou manuellement à l’aide de la CLI Docker (commandes docker run et docker-compose). Si votre application contient un seul service personnalisé, créez un seul fichier Dockerfile. Si votre application contient plusieurs services (comme dans une architecture de microservices), vous devez créer un fichier Dockerfile pour chaque service.

Le fichier Dockerfile est créé dans le dossier racine de votre application ou service. Il contient les commandes qui indiquent à Docker comment configurer et exécuter votre application ou service dans un conteneur. Vous pouvez créer manuellement un fichier Dockerfile dans le code et l’ajouter à votre projet, avec vos dépendances .NET.

Avec Visual Studio et ses outils pour Docker, cette tâche se fait en quelques clics de souris seulement. Quand vous créez un projet dans Visual Studio 2017, vous avez une option nommée **Activer la prise en charge de Docker** (voir la figure 5-3).

![](./media/image5.png)

**Figure 5-3**. Option Activer la prise en charge de Docker affichée lors de la création d’un projet dans Visual Studio 2017

Vous pouvez aussi activer la prise en charge de Docker dans un projet nouveau ou existant en cliquant avec le bouton droit sur votre fichier projet dans Visual Studio et en sélectionnant l’option **Ajouter-Prise en charge de Docker**, comme le montre la figure 5-4.

![](./media/image6.png)

**Figure 5-4**. Activation de la prise en charge de Docker dans un projet Visual Studio 2017 existant

Cette action sur un projet (par exemple, une application Web ASP.NET ou un service Web API) ajoute un fichier Dockerfile au projet avec la configuration requise. Elle ajoute également un fichier docker-compose.yml qui s’applique à la solution entière. Dans les sections suivantes, nous décrivons les informations à ajouter dans chacun de ces fichiers. Visual Studio peut effectuer cette tâche à votre place, mais il est utile de savoir ce que contient un fichier Dockerfile.

### <a name="option-a-creating-a-project-using-an-existing-official-net-docker-image"></a>Option A : Création d’un projet à l’aide d’une image Docker .NET officielle existante

Le plus souvent, vous créez une image personnalisée pour votre conteneur à partir d’une image de base que vous obtenez d’un dépôt officiel dans le registre [Docker Hub](https://hub.docker.com/). C’est précisément ce qui se passe en arrière-plan quand vous activez la prise en charge de Docker dans Visual Studio. Votre fichier Dockerfile utilise une image aspnetcore existante.

Précédemment, nous avons expliqué quels images et dépôts Docker vous pouvez utiliser selon le framework et le système d’exploitation que vous avez choisis. Par exemple, si vous souhaitez utiliser ASP.NET Core (Windows ou Linux), vous devez utiliser l’image microsoft/aspnetcore:2.0. La seule chose à faire est donc de spécifier l’image Docker de base à utiliser pour votre conteneur. Pour cela, vous ajoutez FROM microsoft/aspnetcore:2.0 dans votre fichier Dockerfile. Cette opération est effectuée automatiquement par Visual Studio, mais si vous avez à mettre à jour la version, vous devez modifier cette valeur.

L’utilisation d’un dépôt d’images .NET officiel fourni dans le Docker Hub avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur toutes les machines (y compris celles de développement, test et production).

L’extrait de code suivant est un exemple de fichier Dockerfile pour un conteneur ASP.NET Core.

```
FROM microsoft/aspnetcore:2.0
  
ARG source
  
WORKDIR /app
  
EXPOSE 80
  
COPY ${source:-obj/Docker/publish} .
  
ENTRYPOINT ["dotnet", " MySingleContainerWebApp.dll "]
```

Dans ce cas, le conteneur est basé sur la version 2.0 de l’image Docker ASP.NET Core officielle (multi-arch pour Linux et Windows). Il s’agit du paramètre `FROM microsoft/aspnetcore:2.0`. (Pour plus d’informations sur cette image de base, consultez la page [Image Docker ASP.NET Core](https://hub.docker.com/r/microsoft/aspnetcore/) et la page [Image Docker .NET Core](https://hub.docker.com/r/microsoft/dotnet/).) Dans le fichier Dockerfile, vous devez également indiquer à Docker d’écouter le port TCP qui sera utilisé au moment de l’exécution (dans cet exemple, le port 80 est configuré avec le paramètre EXPOSE).

Vous pouvez spécifier des paramètres de configuration supplémentaires dans le fichier Dockerfile, en fonction du langage et du framework que vous utilisez. Par exemple, la ligne ENTRYPOINT avec \["dotnet", "MySingleContainerWebApp.dll"\] indique à Docker d’exécuter une application .NET Core. Si vous utilisez le SDK et l’interface CLI (dotnet) de .NET Core pour créer et exécuter l’application .NET, ce paramètre est différent. L’essentiel à retenir est que la ligne ENTRYPOINT et certains autres paramètres varient selon le langage et la plateforme choisis pour votre application.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Création d’images Docker pour les applications .NET Core**
    [*https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images*](../../../core/docker/building-net-docker-images.md)

-   **Créer votre propre image**. Documentation officielle de Docker.
    [*https://docs.docker.com/engine/tutorials/dockerimages/*](https://docs.docker.com/engine/tutorials/dockerimages/)

### <a name="using-multi-arch-image-repositories"></a>Utilisation de dépôts d’images multi-arch

Un dépôt peut contenir des variantes de plateforme, comme une image Linux et une image Windows. Cette fonctionnalité permet aux fournisseurs comme Microsoft (créateurs d’images de base) de créer un dépôt commun pour plusieurs plateformes (Linux et Windows). Par exemple, le dépôt [microsoft/dotnet](https://hub.docker.com/r/microsoft/aspnetcore/) disponible dans le registre Docker Hub fournit une prise en charge de Linux et Windows Nano Server en utilisant le même nom de dépôt.

Si vous spécifiez une balise, le ciblage d’une plateforme est explicite, comme dans les cas suivants :

-   **microsoft/aspnetcore:2.0.0-jessie**

        .NET Core 2.0 runtime-only on Linux 

-   **microsoft/aspnetcore:2.0.0-nanoserver**

        .NET Core 2.0 runtime-only on Windows Nano Server

Cependant, et cela est nouveau depuis le milieu de l’année 2017, si vous spécifiez le même nom d’image avec la même balise, les nouvelles images multi-arch (comme l’image aspnetcore qui prend en charge multi-arch) utiliseront la version Windows ou Linux selon le système d’exploitation de l’hôte Docker que vous déployez, comme cela est montré dans l’exemple suivant :

-   **microsoft/aspnetcore:2.0**

        Multi-arch: .NET Core 2.0 runtime-only on Linux or Windows Nano Server depending on the Docker host OS

Ainsi, quand vous tirez (pull) une image d’un hôte Windows, la variante Windows est tirée et quand vous tirez le même nom d’image d’un hôte Linux, la variante Linux est tirée.

### <a name="option-b-creating-your-base-image-from-scratch"></a>Option B : Créer votre image de base à partir de zéro

Vous pouvez créer votre propre image de base Docker à partir de zéro. Ce scénario n’est pas recommandé si vous n’êtes pas encore familiarisé avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Images .NET Core multi-arch**.
https://github.com/dotnet/announcements/issues/14 
-   **Créer une image de base**. Documentation officielle de Docker.
    [*https://docs.docker.com/engine/userguide/eng-image/baseimages/*](https://docs.docker.com/engine/userguide/eng-image/baseimages/)

![](./media/image7.png)

## <a name="step-3-create-your-custom-docker-images-and-embed-your-application-or-service-in-them"></a>Étape 3. Créer vos images Docker personnalisées et incorporer votre application ou service dans ces images

Pour chaque service inclus dans votre application, vous devez créer une image associée. Si votre application est composée uniquement d’un service ou d’une application web, vous avez besoin d’une seule image.

Sachez que les images Docker sont créées automatiquement dans Visual Studio. Les étapes suivantes s’appliquent uniquement dans le cadre du workflow avec un éditeur ou une CLI. Elles sont expliquées pour vous permettre de bien en comprendre tous les dessous.

En tant que développeur, vous avez besoin d’écrire du code et de le tester localement avant de pousser (push) une fonctionnalité ou un changement terminé à votre système de contrôle de code source (par exemple, à GitHub). Cela signifie que vous devez créer les images Docker et déployer des conteneurs sur un hôte Docker local (machine virtuelle Windows ou Linux), et exécuter, tester et déboguer dans ces conteneurs locaux.

Pour créer une image personnalisée dans votre environnement local avec la CLI Docker et votre fichier Dockerfile, vous pouvez utiliser la commande docker build, comme indiqué dans la figure 5-5.

![](./media/image8.png)

**Figure 5-5**. Création d’une image Docker personnalisée

Si vous le souhaitez, au lieu d’exécuter la commande docker build directement à partir du dossier de projet, vous pouvez d’abord exécuter la commande dotnet publish pour créer un dossier déployable contenant les binaires et bibliothèques .NET nécessaires, puis utiliser la commande docker build.

Cela crée une image Docker nommée cesardl/netcore-webapi-microservice-docker:first. Dans ce cas, :first est une balise qui représente une version spécifique. Vous pouvez répéter cette étape pour chaque image personnalisée à créer pour votre application Docker composée.

Quand une application est constituée de plusieurs conteneurs (c’est donc une application multiconteneur), vous pouvez également utiliser la commande docker-compose up --build pour créer toutes les images associées avec une seule commande à l’aide des métadonnées exposées dans les fichiers docker-compose.yml associés.

Vous pouvez rechercher les images existantes dans votre dépôt local avec la commande docker images (voir la figure 5-6).

![](./media/image9.png)

**Figure 5-6.** Affichage des images existantes à l’aide de la commande docker images

### <a name="creating-docker-images-with-visual-studio"></a>Création d’images Docker avec Visual Studio

Quand vous utilisez Visual Studio pour créer un projet avec la prise en charge de Docker, vous ne créez pas une image explicitement. Au lieu de cela, l’image est créée pour vous quand vous appuyez sur F5 et exécutez l’application ou le service Docker. Cette étape est automatique dans Visual Studio. Vous ne la verrez donc pas à l’écran, mais il est important d’en comprendre le mécanisme.

![](./media/image10.png)

## <a name="step-4-define-your-services-in-docker-composeyml-when-building-a-multi-container-docker-application"></a>Étape 4. Définir vos services dans docker-compose.yml lors de la création d’une application Docker multiconteneur

Le fichier [docker-compose.yml](https://docs.docker.com/compose/compose-file/) vous permet de définir un ensemble de services à déployer ensemble comme application composée avec les commandes de déploiement.

Pour utiliser un fichier docker-compose.yml, vous devez d’abord le créer dans votre dossier solution principal ou racine. Le contenu du fichier doit être semblable à l’exemple suivant :

```yml
version: '3'
  
services:

  webmvc:
    image: eshop/web
    environment:
      - CatalogUrl=http://catalog.api
      - OrderingUrl=http://ordering.api
    ports:
      - "80:80"
    depends_on:
      - catalog.api
      - ordering.api

  catalog.api:
    image: eshop/catalog.api
    environment: 
      - ConnectionString=Server=sql.data;Database=CatalogDB;…
    ports:
      - "81:80"
    depends_on:
      - sql.data

  ordering.api:
    image: eshop/ordering.api
    environment:
      - ConnectionString=Server=sql.data;Database=OrderingDb;…
    ports:
      - "82:80"
    extra_hosts:
      - "CESARDLBOOKVHD:10.0.75.1"
    depends_on:
      - sql.data

  sql.data:
    image: mssql-server-linux:latest
    environment:
      - SA_PASSWORD=Pass@word
      - ACCEPT_EULA=Y
    ports:
      - "5433:1433"

```

Notez que ce fichier docker-compose.yml est une version simplifiée et fusionnée. Il contient des données de configuration statiques pour chaque conteneur (comme le nom de l’image personnalisée), qui s’appliquent toujours, ainsi que des informations de configuration variables selon l’environnement de déploiement, comme la chaîne de connexion. Dans des sections ultérieures, vous découvrirez comment vous pouvez fractionner le fichier de configuration docker-compose.yml en plusieurs fichiers docker-compose et substituer les valeurs en fonction de l’environnement et du type d’exécution (debug ou release).

L’exemple de fichier docker-compose.yml définit cinq services : le service webmvc (une application web), deux microservices (catalog.api et ordering.api), et un conteneur source de données (sql.data), basé sur SQL Server pour Linux exécuté en tant que conteneur. Chaque service étant déployé en tant que conteneur, une image Docker est nécessaire pour chacun.

Le fichier docker-compose.yml spécifie les conteneurs utilisés, mais aussi la configuration de chaque conteneur. Par exemple, la définition du conteneur webmvc dans le fichier .yml :

-   Utilise une image eshop/web:latest précréée. Toutefois, vous pouvez également configurer l’image à créer à l’exécution de docker-compose avec une configuration supplémentaire basée sur une section :build dans le fichier docker-compose.

-   Initialise deux variables d’environnement (CatalogUrl et OrderingUrl).

-   Transfère le port exposé 80 sur le conteneur vers le port externe 80 sur la machine hôte.

-   Lie l’application web aux services catalog et ordering avec le paramètre depends\_on. Cela force le service à attendre le démarrage de ces services.

Nous reparlerons du fichier docker-compose.yml dans une section ultérieure, quand nous expliquerons comment implémenter des microservices et des applications multiconteneurs.

### <a name="working-with-docker-composeyml-in-visual-studio-2017"></a>Utilisation de docker-compose.yml dans Visual Studio 2017

Quand vous ajoutez une prise en charge de la solution Docker à un projet de service dans une solution Visual Studio, comme illustré à la figure 5-7, Visual Studio ajoute un fichier Dockerfile à votre projet, et il ajoute une section service (projet) dans votre solution avec les fichiers docker-compose.yml. Il s’agit d’une méthode simple pour commencer à composer votre solution multiconteneur. Vous pouvez ensuite ouvrir les fichiers docker-compose.yml et les mettre à jour avec des fonctionnalités supplémentaires.

![](./media/image6.png)

**Figure 5-7**. Ajout de la prise en charge de Docker dans Visual Studio 2017 en cliquant avec le bouton droit sur un projet ASP.NET Core

L’ajout de la prise en charge de Docker dans Visual Studio ajoute le fichier Dockerfile à votre projet, mais ajoute aussi les informations de configuration dans plusieurs fichiers docker-compose.yml globaux définis au niveau de la solution.

Après avoir ajouté la prise en charge de Docker à votre solution dans Visual Studio, vous verrez également un nouveau nœud (dans le fichier projet docker-compose.dcproj) dans l’Explorateur de solutions. Ce nœud contient les fichiers docker-compose.yml qui ont été ajoutés (voir la figure 5-8).

![](./media/image11.PNG)

**Figure 5-8**. Nœud d’arborescence **docker-compose** ajouté dans l’Explorateur de solutions de Visual Studio 2017

Vous pouvez aussi déployer une application multiconteneur avec un seul fichier docker-compose.yml en utilisant la commande docker-compose up. Toutefois, Visual Studio ajoute un groupe de fichiers pour vous permettre de substituer les valeurs selon l’environnement (développement ou production) et le type d’exécution (release ou debug). Cette fonctionnalité sera expliquée dans des sections ultérieures.

![](./media/image12.png)

## <a name="step-5-build-and-run-your-docker-application"></a>Étape 5. Générer et exécuter votre application Docker

Si votre application n’a qu’un seul conteneur, vous pouvez l’exécuter en la déployant sur l’hôte Docker (machine virtuelle ou serveur physique). Si votre application contient plusieurs services, vous pouvez la déployer en tant qu’application composée, soit à l’aide d’une seule commande CLI (docker-compose up), soit avec Visual Studio, qui utilise cette commande en arrière-plan. Examinons les différentes options.

### <a name="option-a-running-a-single-container-with-docker-cli"></a>Option A : Exécution d’un seul conteneur avec la CLI Docker

Vous pouvez exécuter un conteneur Docker à l’aide de la commande docker run, comme dans la figure 5-9 :

```
  docker run -t -d -p 80:5000 cesardl/netcore-webapi-microservice-docker:first
```

![](./media/image13.png)

**Figure 5-9**. Exécution d’un conteneur Docker à l’aide de la commande docker run

Dans ce cas, la commande lie le port interne 5000 du conteneur au port 80 de la machine hôte. Cela signifie que l’hôte écoute le port 80 et transfère le port sur le port 5000 sur le conteneur.

### <a name="option-b-running-a-multi-container-application"></a>Option B : Exécution d’une application multiconteneur

Dans la plupart des scénarios d’entreprise, une application Docker est composée de plusieurs services, ce qui signifie que vous devez exécuter une application multiconteneur, comme illustré à la figure 5-10.

![](./media/image14.png)

**Figure 5-10**. Machine virtuelle avec des conteneurs Docker déployés

#### <a name="running-a-multi-container-application-with-the-docker-cli"></a>Exécution d’une application multiconteneur avec la CLI Docker

Pour exécuter une application multiconteneur avec la CLI Docker, exécutez la commande docker-compose up. Cette commande utilise le fichier docker-compose.yml défini au niveau de la solution pour déployer une application multiconteneur. La figure 5-11 montre les résultats de l’exécution de la commande à partir de votre répertoire de projet principal, qui contient le fichier docker-compose.yml.

![](./media/image15.png)

**Figure 5-11**. Exemple de résultats de l’exécution de la commande docker-compose up

Après l’exécution de la commande docker-compose up, l’application et ses conteneurs associés sont déployés sur votre hôte Docker, comme illustré dans la représentation de machine virtuelle à la figure 5-10.

#### <a name="running-and-debugging-a-multi-container-application-with-visual-studio"></a>Exécution et débogage d’une application multiconteneur avec Visual Studio 

L’exécution d’une application multiconteneur à l’aide de Visual Studio 2017 est extrêmement simple. En plus d’exécuter l’application multiconteneur, vous pouvez déboguer tous ses conteneurs directement dans Visual Studio en définissant des points d’arrêt réguliers.

Comme nous l’avons mentionné plus haut, chaque fois que vous ajoutez la prise en charge de la solution Docker à un projet dans une solution, ce projet est configuré dans le fichier docker-compose.yml global (au niveau de la solution), ce qui vous permet d’exécuter ou de déboguer la solution dans son intégralité. Visual Studio démarre un conteneur pour chaque projet pour lequel la prise en charge de la solution Docker est activée, puis il effectue automatiquement toutes les étapes internes (dotnet publish, docker build, etc.).

Le point important ici est que, comme indiqué dans la figure 5-12, Visual Studio 2017 fournit une commande **Docker** supplémentaire associée à l’action de la touche F5. Cette option vous permet d’exécuter ou de déboguer une application multiconteneur en exécutant tous les conteneurs qui sont définis dans les fichiers docker-compose.yml au niveau de la solution. Pour déboguer des solutions multiconteneurs, vous pouvez définir plusieurs points d’arrêt, chaque point d’arrêt dans un projet (conteneur) distinct, et, pendant le débogage à partir de Visual Studio, vous vous arrêtez aux points d’arrêt définis dans les différents projets et exécutés sur des conteneurs différents.

![](./media/image16.png)

**Figure 5-12**. Exécution d’applications multiconteneurs dans Visual Studio 2017

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Déployer un conteneur ASP.NET sur un hôte Docker distant**
    [*https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker*](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

### <a name="a-note-about-testing-and-deploying-with-orchestrators"></a>Note sur le test et le déploiement avec des orchestrateurs

Les commandes docker-compose up et docker run (ou l’exécution et le débogage des conteneurs dans Visual Studio) sont une approche appropriée pour tester les conteneurs dans votre environnement de développement. Mais n’utilisez pas cette approche si vous ciblez des clusters Docker et des orchestrateurs tels que Docker Swarm, Mesosphere DC/OS ou Kubernetes. Si vous utilisez un cluster comme le [mode Docker Swarm](https://docs.docker.com/engine/swarm/) (disponible dans Docker CE pour Windows et Mac depuis la version 1.12), vous devez déployer et tester avec des commandes supplémentaires comme [docker service create](https://docs.docker.com/engine/reference/commandline/service_create/) pour des services uniques. Si vous déployez une application composée de plusieurs conteneurs, utilisez [docker compose bundle](https://docs.docker.com/compose/reference/bundle/) et [docker deploy myBundleFile](https://docs.docker.com/engine/reference/commandline/deploy/) pour déployer cette application en tant que *pile*. Pour plus d’informations, consultez le billet de blog [Introducing Experimental Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) dans la documentation Docker disponible sur le site Docker.

Avec [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) et [Kubernetes](http://kubernetes.io/docs/user-guide/deployments/), vous devez également utiliser des commandes et scripts de déploiement différents.

![](./media/image17.png)

## <a name="step-6-test-your-docker-application-using-your-local-docker-host"></a>Étape 6. Tester votre application Docker à l’aide de l’hôte Docker local

Cette étape varie en fonction de ce que fait votre application. Dans une application web .NET Core simple qui est déployée en tant que service ou conteneur unique, vous pouvez accéder au service en ouvrant un navigateur sur l’hôte Docker et en accédant à ce site comme indiqué à la figure 5-13. (Si la configuration dans le fichier Dockerfile mappe le conteneur à un autre port sur l’hôte que le port 80, incluez l’adresse de l’hôte dans l’URL.)

![](./media/image18.png)

**Figure 5-13**. Exemple de test de l’application Docker en local avec localhost

Si localhost ne pointe pas vers l’IP de l’hôte Docker (contrairement à la configuration par défaut quand vous utilisez Docker CE), spécifiez l’adresse IP de la carte réseau de votre machine pour pouvoir accéder à votre service.

Notez que cette URL dans le navigateur utilise le port 80 pour l’exemple de conteneur particulier présenté ici. Toutefois, en interne, les requêtes sont redirigées vers le port 5000, car le déploiement a été fait de cette façon avec la commande docker run, comme nous l’avons expliqué dans une étape précédente.

Vous pouvez également tester l’application en exécutant curl à partir du terminal, comme indiqué à la figure 5-14. Dans une installation Docker sur Windows, l’IP par défaut de l’hôte Docker est toujours 10.0.75.1 en plus de l’adresse IP réelle de votre machine.

![](./media/image19.png)

**Figure 5-14**. Exemple de test de l’application Docker en local avec curl

### <a name="testing-and-debugging-containers-with-visual-studio-2017"></a>Test et débogage des conteneurs avec Visual Studio 2017

Quand vous exécutez et déboguez les conteneurs avec Visual Studio 2017, vous pouvez déboguer l’application .NET pratiquement de la même façon que pour une exécution sans conteneurs.

### <a name="testing-and-debugging-without-visual-studio"></a>Test et débogage sans Visual Studio

Si vous avez choisi l’approche de développement avec un éditeur ou une CLI, le débogage des conteneurs est plus difficile. Vous pouvez alors déboguer les conteneurs en générant des traces.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Débogage d’applications dans un conteneur Docker local**
    [*https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh*](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

-   **Steve Lasker. Build, Debug, Deploy ASP.NET Core Apps with Docker.** Vidéo.
    [*https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T115*](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T115)

## <a name="simplified-workflow-when-developing-containers-with-visual-studio"></a>Workflow simplifié du développement de conteneurs avec Visual Studio

En effet, le workflow avec Visual Studio est beaucoup plus simple que si vous utilisez un éditeur ou une CLI. La plupart des étapes requises par Docker liées aux fichiers Dockerfile et docker-compose.yml sont masquées ou simplifiées par Visual Studio, comme illustré à la figure 5-15.

![](./media/image20.png)

**Figure 5-15**. Workflow simplifié du développement avec Visual Studio

De plus, notez que vous devez effectuer l’étape 2 (ajout de la prise en charge de Docker à vos projets) une seule fois. Le workflow est donc similaire aux tâches de développement que vous avez l’habitude de faire dans le cadre d’un développement avec .NET. Vous devez comprendre ce qui se passe en arrière-plan (le processus de création d’image, les images de base utilisées, le déploiement des conteneurs, etc.). Par ailleurs, vous aurez parfois besoin de modifier le fichier Dockerfile ou docker-compose.yml pour personnaliser les comportements. Au final, Visual Studio simplifie considérablement la plupart des tâches et vous permet de développer beaucoup plus rapidement.

### <a name="additional-resources"></a>Ressources supplémentaires

-   **Steve Lasker. .NET Docker Development with Visual Studio 2017**
    [*https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111*](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111)

-   **Jeffrey T. Fritz. Put a .NET Core App in a Container with the new Docker Tools for Visual Studio**
    [*https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/*](https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/)

## <a name="using-powershell-commands-in-a-dockerfile-to-set-up-windows-containers"></a>Utilisation de commandes PowerShell dans un fichier Dockerfile pour configurer des conteneurs Windows 

Les [conteneurs Windows](https://msdn.microsoft.com/en-us/virtualization/windowscontainers/about/about_overview) vous permettent de convertir vos applications Windows existantes en images Docker, puis de les déployer avec les mêmes outils que le reste de l’écosystème Docker. Pour utiliser les conteneurs Windows, vous exécutez des commandes PowerShell dans le fichier Dockerfile, comme indiqué dans l’exemple suivant :

```
FROM microsoft/windowsservercore
  
LABEL Description="IIS" Vendor="Microsoft" Version="10"
  
RUN powershell -Command Add-WindowsFeature Web-Server
  
CMD [ "ping", "localhost", "-t" ]
```

Dans ce cas, nous utilisons une image de base Windows Server Core (le paramètre FROM) et nous installons IIS à l’aide d’une commande PowerShell (le paramètre RUN). De la même façon, vous pouvez également utiliser des commandes PowerShell pour configurer des composants supplémentaires comme ASP.NET 4.x, .NET 4.6 ou tout autre logiciel Windows. Par exemple, la commande suivante dans un fichier Dockerfile configure ASP.NET 4.5 :

```
RUN powershell add-windowsfeature web-asp-net45
```

### <a name="additional-resources"></a>Ressources supplémentaires

-   **aspnet-docker/Dockerfile.** Exemples de commandes PowerShell à exécuter à partir de fichiers Dockerfile pour ajouter des fonctionnalités Windows.
    [*https://github.com/Microsoft/aspnet-docker/blob/master/4.6.2/Dockerfile*](https://github.com/Microsoft/aspnet-docker/blob/master/4.6.2/Dockerfile)

>[!div class="step-by-step"]
[Previous] (index.md) [Next] (../net-core-single-containers-linux-windows-server-hosts/index.md)
