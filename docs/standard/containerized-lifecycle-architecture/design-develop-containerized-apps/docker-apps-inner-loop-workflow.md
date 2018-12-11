---
title: Flux de travail de développement de la boucle interne pour les applications Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: f7acb60e6136c0250d18bdce23ac21fb6aa80b34
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148858"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a>Flux de travail de développement de la boucle interne pour les applications Docker

Avant de déclencher le flux de travail de boucle externe couvrant l’ensemble DevOps cycle, tout cela commence sur chaque machine de développeur, codage de l’application elle-même, à l’aide de leurs plateformes ou langages préférés et de le tester localement (Figure 4-14). Mais dans tous les cas, vous aurez un point très important en commun, peu importe quel langage, infrastructure ou plateformes que vous choisissez. Dans ce flux de travail spécifique, vous toujours développez et testez des conteneurs Docker, mais localement.

![](./media/image18.png)

Figure 4-14 : Contexte de développement de la boucle interne

Le conteneur ou une instance d’une image Docker contiendra ces composants :

-   Une sélection de système d’exploitation (par exemple, une distribution Linux ou Windows)

-   Fichiers ajoutés par le développeur (par exemple, les binaires d’application)

-   Configuration (par exemple, les paramètres d’environnement et les dépendances)

-   Instructions pour les processus pour exécuter par Docker

Vous pouvez configurer le flux de travail de développement de la boucle interne qui utilise Docker en tant que le processus (décrit dans la section suivante). Prenez en compte que les premières étapes pour configurer l’environnement n’est pas inclus, car vous devez le faire qu’une seule fois.

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a>Création d’une application unique dans un conteneur Docker à l’aide de Visual Studio Code et interface CLI Docker

Les applications sont constituées à partir de vos propres services ainsi que des bibliothèques supplémentaires (dépendances).

Figure 4-15 montre les étapes de base que vous devez généralement exécuter lors de la création d’une application Docker, suivie d’une description détaillée de chaque étape.

![](./media/image19.png)

Figure 4-15 : Flux de travail général pour le cycle de vie pour les applications Docker en conteneur à l’aide de la CLI Docker

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a>Étape 1 : Commencer le codage dans Visual Studio Code et créer votre base de référence de l’application ou du service initial

Manière de développer votre application est assez similaire à la façon de que procéder sans Docker. La différence est que lors du développement, vous déployez et testez l’application ou les services qui s’exécutent dans des conteneurs Docker placés dans votre environnement local (comme un Linux VM ou de Windows).

**Configuration de votre environnement local**

Avec les dernières versions de Docker pour Mac et Windows, il est plus facile que jamais pour développer des applications de Docker, et le programme d’installation est simple.

**Plus d’informations** pour obtenir des instructions sur la configuration de Docker pour Windows, accédez à [ https://docs.docker.com/docker-for-windows/ ](https://docs.docker.com/docker-for-windows/).

Pour obtenir des instructions sur la configuration Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.

Vous devez en outre, un éditeur de code afin que vous pouvez développer en fait votre application tout en utilisant l’interface CLI Docker.

Microsoft fournit Visual Studio Code, qui est un éditeur de code léger qui est pris en charge sur Mac, Windows et Linux et fournit des fonctionnalités IntelliSense avec [prise en charge de nombreux langages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python et la plupart les langages modernes), [débogage](https://code.visualstudio.com/Docs/editor/debugging), [une intégration avec Git](https://code.visualstudio.com/Docs/editor/versioncontrol) et [prise en charge des extensions](https://code.visualstudio.com/docs/extensions/overview). Cet éditeur est parfait pour les développeurs Mac et Linux. Dans Windows, vous pouvez également utiliser l’application complète de Visual Studio.

**Plus d’informations** pour obtenir des instructions sur l’installation de Visual Studio pour Windows, Mac ou Linux, accédez à <https://code.visualstudio.com/docs/setup/setup-overview/>.

Vous pouvez utiliser avec l’interface CLI Docker et écrivez votre code à l’aide de n’importe quel éditeur de code, mais si vous utilisez Visual Studio Code, il est facilement auteur Dockerfile et les fichiers docker-compose.yml dans votre espace de travail. En outre, vous pouvez exécuter des tâches de Visual Studio Code à partir de l’IDE qui invite les scripts qui peuvent être en cours d’exécution des opérations élaborées à l’aide de la CLI Docker sous.

Visual Studio Code est fourni par une extension, vous devez installer. Pour ce faire, appuyez sur Ctrl + Maj + P, tapez **ext installer**, puis exécutez les Extensions : Installer la commande d’Extension pour afficher la liste des extensions Marketplace. Ensuite, tapez **docker** pour filtrer les résultats, puis sélectionnez le fichier Dockerfile et le fichier Docker Compose (yml) extension de prise en charge, comme illustré dans la Figure 4-16.

![](./media/image20.png)

Figure 4-16 : L’installation de l’Extension Docker dans Visual Studio Code

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a>Étape 2 : Créer un fichier DockerFile associé à une image existante (système d’exploitation brut ou des environnements de développement tels que .NET Core, Node.js et Ruby)

Vous devez un fichier DockerFile par une image personnalisée à générer et par conteneur à déployer, par conséquent, si votre application se compose d’un seul service personnalisé, vous devez un fichier DockerFile unique. Toutefois, si votre application est composée de plusieurs services (comme dans une architecture de microservices), vous devez créer un fichier Dockerfile par service.

Le fichier DockerFile est généralement placé dans le dossier racine de votre application ou service et contient les commandes requises pour que cette Docker sache comment configurer et exécuter l’application ou le service. Vous pouvez créer votre fichier DockerFile et ajoutez-le à votre projet, ainsi que votre code (node.js, .NET Core, etc.), ou, si vous ne connaissez pas l’environnement, examinons l’info-bulle suivante.

> [!TIP]
> Vous pouvez utiliser un outil de ligne de commande appelé [yo docker](https://github.com/Microsoft/generator-docker), qui structure des fichiers à partir de votre projet dans le langage que vous choisissez et ajoute les fichiers de configuration Docker requis. En fait, pour aider les développeurs qui débutent, il crée le fichier DockerFile approprié, docker-compose.yml et autres scripts associés pour générer et exécuter vos conteneurs Docker. Ce générateur yeoman vous invitera à quelques questions, vous demandant votre hôte de conteneur de langage et de destination sélectionné de développement.

![yo docker](./media/image21.png)

Par exemple, la Figure 4-17 montre les deux captures d’écran à partir de terminaux dans Windows et sur un Mac, dans les deux cas, en cours d’exécution yo docker, ce qui génère les projets de code échantillon (actuellement .NET Core, Golang et Node.js en tant que langues prises en charge) déjà configurés pour fonctionner sur haut de Docker.

![](./media/image22.PNG)  ![](./media/image23.png)

Figure 4-17 : yo docker outil de commande dans Windows (à gauche) et sur un Mac

Figure 4-18 présente un exemple à l’aide d’yo docker une fois que vous avez un projet .NET Core existant en place pour être généré automatiquement.

![](./media/image24.PNG)

Figure 4-18 : yo docker avec un .NET Core existants du projet en place

À partir du fichier DockerFile, vous spécifiez quelle image Docker de base à utiliser (par exemple, à l’aide de « FROM microsoft/dotnet:1.0.0-core »). Vous allez généralement générer votre image personnalisée sur une image de base que vous pouvez obtenir à partir de n’importe quel dépôt officiel dans le [Registre Docker Hub](https://hub.docker.com/) (comme un [image pour .NET Core](https://hub.docker.com/r/microsoft/dotnet/) ou un [pour Node.js](https://hub.docker.com/_/node/)).

***Option a : Utilisez une image Docker officielle existante***

À l’aide d’un dépôt officiel de la pile de langage avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur toutes les machines (y compris le développement, test et production).

Voici un exemple de fichier DockerFile pour un conteneur .NET Core :

```
# Base Docker image to use
FROM microsoft/aspnetcore:1.0.1\

# Set the Working Directory and files to be copied to the image
ARG source
WORKDIR /app
COPY ${source:-bin/Release/PublishOutput} .

# Configure the listening port to 80 (Internal/Secured port within Docker host)
EXPOSE 80

# Application entry point
ENTRYPOINT ["dotnet", "MyCustomMicroservice.dll"]
```

Dans ce cas, il est à l’aide de la version 1.0.1 de l’image Docker ASP.NET Core officielle pour Linux nommé microsoft/aspnetcore:1.0.1. Pour plus d’informations, consultez le [page de l’Image Docker ASP.NET Core](https://hub.docker.com/r/microsoft/aspnetcore/) et [page de l’Image Docker .NET Core](https://hub.docker.com/r/microsoft/dotnet/). Vous également pouvez utiliser une autre image comparable à nœud : 4-onbuild pour Node.js ou de nombreux autres images préconfigurées pour les langages de développement, qui sont disponibles dans [Docker Hub](https://hub.docker.com/explore/).

Dans le fichier DockerFile, vous devez également indiquer à Docker d’écouter sur le port TCP que vous utiliserez lors de l’exécution (par exemple, le port 80).

Il existe des autres lignes de configuration que vous pouvez ajouter dans le fichier DockerFile en fonction de la langue/infrastructure que vous utilisez, pour que Docker sache comment exécuter l’application. Par exemple, vous devez la ligne ENTRYPOINT avec \[« dotnet », « MyCustomMicroservice.dll »\] pour exécuter une application .NET Core, bien que vous pouvez avoir plusieurs variantes selon l’approche pour générer et exécuter votre service. Si vous utilisez le Kit de développement logiciel et l’interface CLI dotnet pour générer et exécuter l’application .NET, il serait légèrement différente. L’essentiel est que la ligne ENTRYPOINT ainsi que des lignes supplémentaires sera différents selon la langue/plateforme que vous choisissez pour votre application.

**Plus d’informations** pour plus d’informations sur la création d’images Docker pour les applications .NET Core, accédez à <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.

Pour en savoir plus sur la création de vos propres images, accédez à [ https://docs.docker.com/engine/\ didacticiels/dockerimages/](https://docs.docker.com/engine/tutorials/dockerimages/).

**Référentiels d’images multi-plateformes**

Comme les conteneurs Windows deviennent de plus en plus répandus, un référentiel unique peut contenir des variantes de plateforme, comme une image Linux et Windows. Il s’agit d’une nouvelle fonctionnalité proposée dans Docker qui rend possible pour les fournisseurs d’utiliser un référentiel unique pour couvrir plusieurs plateformes, telles que [microsoft/aspdotnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) référentiel, ce qui est disponible sur le Registre DockerHub. Comme la fonctionnalité entre Active, extraction de cette image à partir d’un ordinateur hôte Windows extraira la variante de Windows, tandis que l’extraction du même nom d’image à partir d’un hôte Linux extraira la variante Linux.

***Option b : Créer votre image de base à partir de zéro***

Vous pouvez créer votre propre image de base de Docker à partir de zéro, comme expliqué dans cet [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) à partir de Docker. Il s’agit d’un scénario qui n’est probablement pas vous convient le mieux si vous débutez avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a>Étape 3 : Créer votre l’incorporation de votre service qu’il contient des images Docker personnalisées

Pour chaque service personnalisé qui compose votre application, vous devez créer une image associée. Si votre application est composée d’un service unique ou d’application web, vous aurez besoin en une seule image.

> [!NOTE]
> Lorsque prenant en compte la « boucle externe flux de travail DevOps », les images seront créés par un processus de génération automatisé dès que vous ajoutez votre code source à un référentiel Git (intégration continue) pour les images sont créées dans cet environnement global à partir de votre code source.

Toutefois, avant de nous estimons qu’accédant à cet itinéraire de la boucle externe, nous devons vérifier que l’application Docker réellement fonctionne correctement afin qu’ils n’est pas envoyé de code qui peut ne pas fonctionne correctement pour le système de contrôle de code source (Git, etc.).

Par conséquent, chaque développeur doit d’abord faire tout le processus de boucle interne pour tester localement et continuer à développer jusqu'à ce qu’ils souhaitent push d’une fonctionnalité complète ou de modifier le système de contrôle source.

Pour créer une image dans votre environnement local et à l’aide du fichier DockerFile, vous pouvez utiliser la commande docker build, comme illustré dans la Figure 4-19 (vous pouvez également exécuter docker-compose up--build pour les applications composées de plusieurs conteneurs/Services).

![](./media/image25.png)

Figure 4-19 : Build de docker en cours d’exécution

Si vous le souhaitez, au lieu d’exécuter directement docker build à partir du dossier du projet, vous pouvez tout d’abord créer un dossier déployable avec les bibliothèques .NET nécessaires à l’aide de l’exécution dotnet commande publish, et puis exécutez build de docker.

Dans cet exemple, cela crée une image Docker avec le nom cesardl/netcore-webapi-microservice-docker : first ( : tout d’abord est une balise, comme une version spécifique). Vous pouvez effectuer cette étape pour chaque image personnalisée que vous créez pour votre application Docker composée avec plusieurs conteneurs.

Vous trouverez les images existantes dans votre référentiel local (votre ordinateur de développement) à l’aide de docker commande images, comme illustré dans la Figure 4-20.

![](./media/image26.png)

Figure 4-20 : Affichage des images existantes à l’aide d’images docker

### <a name="step-4-optional-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a>Étape 4 : (Facultatif) Définir vos services dans docker-compose.yml lors de la création d’une application Docker composée avec plusieurs services

Avec le fichier docker-compose.yml, vous pouvez définir un ensemble de services à être déployé comme une application composée avec les commandes de déploiement expliqués dans la section étape suivante.

Vous devez créer ce fichier dans votre main ou un dossier de solution racine ; Il doit avoir un contenu similaire dans le fichier docker-compose.yml suivant :

```yml
version: '2'
services:
  web:
    build: .
    ports:
     - "81:80"
    volumes:
     - .:/code
    depends_on:
     - redis
  redis:
    image: redis
```

Dans ce cas particulier, ce fichier définit deux services : le service web (votre service personnalisé) et le service redis (un service de cache bien connu). Chaque service sera déployé en tant que conteneur, nous devons utiliser une image Docker concrete pour chacun. Pour ce service web particulier, l’image doit effectuer les opérations suivantes :

-   Construire à partir du fichier DockerFile dans le répertoire actif

-   Transférer le port exposé 80 sur le conteneur sur le port 81 sur l’ordinateur hôte

-   Monter le répertoire du projet sur l’ordinateur hôte/code au sein du conteneur, ce qui permet de modifier le code sans avoir à recréer l’image

-   Lier le service web au service redis

Le service redis utilise le [dernière image publique redis](https://hub.docker.com/_/redis/) extraite du Registre Docker Hub. [redis](https://redis.io/) est un système de cache très populaire pour les applications côté serveur.

### <a name="step-5-build-and-run-your-docker-app"></a>Étape 5 : Générer et exécuter votre application Docker

Si votre application a uniquement un seul conteneur, vous devez l’exécuter en la déployant sur votre hôte Docker (machine virtuelle ou serveur physique). Toutefois, si votre application est composée de plusieurs services, vous devez *composer*, trop. Nous allons voir les différentes options.

***Option a : Exécuter un conteneur unique ou un service***

Vous pouvez exécuter l’image Docker à l’aide de la commande docker run, comme illustré ici :

```
docker run -t -d -p 80:5000
cesardl/netcore-webapi-microservice-docker:first
```

Notez que pour ce déploiement, nous allons être redirection des demandes envoyées vers le port 80 vers le port interne 5000. À présent, l’application est à l’écoute sur le port externe 80 au niveau de l’hôte.

***Option b : Composer et exécuter une application de plusieurs conteneurs***

Dans la plupart des scénarios d’entreprise, une application Docker est composée de plusieurs services. Dans ce cas, vous pouvez exécuter la commande docker-compose haut (Figure 4-21), qui utilisera le fichier docker-compose.yml que vous avez peut-être créé précédemment. Exécution de cette commande déploie une application composée avec toutes ses conteneurs associés.

![](./media/image27.png)

Figure 4-21 : Résultats de l’exécution de la commande « docker-compose up »

Après avoir exécuté docker-compose haut, vous déployez votre application et ses conteneurs associés sur votre hôte Docker, comme illustré dans la Figure 4-22, dans la représentation sous forme de machine virtuelle.

![](./media/image28.png)

Figure 4-22 : Machine virtuelle avec des conteneurs Docker déployés

Remarque docker compose haut et docker exécuter peut être suffisant pour le test de vos conteneurs dans votre environnement de développement, mais vous ne pouvez pas les utiliser du tout si vous prévoyez d’utiliser des clusters Docker et orchestrateurs tels que Docker Swarm, Mesosphere DC/OS ou Kubernetes pour être en mesure de monter en puissance. Si vous utilisez un cluster comme [mode Docker Swarm](https://docs.docker.com/engine/swarm/) (disponible dans Docker pour Windows et Mac depuis la version 1.12), vous devez déployer et tester avec des commandes supplémentaires telles que la création du service de docker pour des services uniques, ou lorsque vous êtes déploiement d’une application composée de plusieurs conteneurs, à l’aide de docker compose bundle et docker déployer myBundleFile, en déployant l’application composée comme une pile, comme expliqué dans l’article [Distributed Application Bundles](https://blog.docker.com/2016/06/docker-app-bundle/) à partir de Docker.

Pour [DC/OS](https://mesosphere.com/blog/2015/09/02/dcos-cli-command-line-tool-datacenter/) et [Kubernetes](https://kubernetes.io/docs/user-guide/deployments/#creating-a-deployment) vous utiliseriez les commandes de déploiement différents et des scripts, également.

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a>Étape 6 : Tester votre application Docker (local, dans votre machine virtuelle de CD locale)

Cette étape varie en fonction de ce que fait votre application.

Dans une très simple .NET Core API Web « Hello World » déployé comme un seul conteneur ou un service, vous devez simplement accéder au service en fournissant le port TCP spécifié dans le fichier DockerFile.

Si localhost est désactivée, pour accéder à votre service, vous pouvez trouver l’adresse IP de l’ordinateur à l’aide de cette commande :

docker-machine ip *votre nom de conteneur*

Sur l’hôte Docker, ouvrez un navigateur et accédez à ce site ; Vous devez voir votre application ou du service en cours d’exécution, comme illustré dans la Figure 4-23.

![](./media/image29.png)

Figure 4-23 : Test de votre application Docker localement en utilisant localhost

Notez qu’il utilise le port 80, mais en interne qu’il a été redirigée vers le port 5000, parce que c’est la façon dont elle a été déployée avec docker run, comme expliqué précédemment.

Vous pouvez tester cela à l’aide de CURL à partir du terminal. Dans une installation de Docker sur Windows, l’adresse IP par défaut est 10.0.75.1, comme illustré dans la Figure 4-24.

![](./media/image30.png)

Figure 4-24 : Test d’une application de Docker localement à l’aide de CURL

**Débogage d’un conteneur en cours d’exécution sur Docker**

Visual Studio Code prend en charge le débogage Docker si vous utilisez Node.js et autres plateformes telles que les conteneurs .NET Core.

Vous également pouvez déboguer les conteneurs .NET Core dans Docker lors de l’utilisation de Visual Studio, comme décrit dans la section suivante.

**Plus d’informations :** pour en savoir plus sur le débogage des conteneurs Docker de Node.js, accédez à <https://blog.docker.com/2016/07/live-debugging-docker/> et [ https://blogs.msdn.microsoft.com/\ utilisateur\_ed/2016/02/27 / Visual-Studio-code-New-Features-13-Big-Debugging-Updates-Rich-Object-Hover-Conditional-Breakpoints-Node-js-mono-more/](https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/).

>[!div class="step-by-step"]
>[Précédent](docker-apps-development-environment.md)
>[Suivant](visual-studio-tools-for-docker.md)