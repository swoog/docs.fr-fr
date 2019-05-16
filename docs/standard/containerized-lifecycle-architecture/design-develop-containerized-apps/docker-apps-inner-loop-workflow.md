---
title: Workflow de développement de la boucle interne pour les applications Docker
description: Découvrez le flux de travail « boucle intérieure » pour le développement d’applications Docker.
ms.date: 02/15/2019
ms.openlocfilehash: ce573546f61b98c2f93e998203497fa949e9efe8
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644850"
---
# <a name="inner-loop-development-workflow-for-docker-apps"></a>Workflow de développement de la boucle interne pour les applications Docker

Avant de déclencher le flux de travail de boucle externe couvrant l’ensemble DevOps cycle, tout cela commence sur chaque machine de développeur, codage de l’application elle-même, à l’aide de leurs plateformes ou langages préférés et de le tester localement (Figure 4-21). Mais dans tous les cas, vous aurez un point important en commun, peu importe quel langage, infrastructure ou plateformes que vous choisissez. Dans ce flux de travail spécifique, vous toujours développez et testez des conteneurs Docker, mais localement.

![Étape 1 : Code/Run/Debug](./media/image18.png)

**Figure 4-21**. Contexte de développement de la boucle interne

Le conteneur ou une instance d’une image Docker contiendra ces composants :

- Une sélection de système d’exploitation (par exemple, une distribution Linux ou Windows)

- Fichiers ajoutés par le développeur (par exemple, les binaires d’application)

- Configuration (par exemple, les paramètres d’environnement et les dépendances)

- Instructions pour les processus pour exécuter par Docker

Vous pouvez configurer le flux de travail de développement de la boucle interne qui utilise Docker en tant que le processus (décrit dans la section suivante). Prendre en compte que les premières étapes pour configurer l’environnement ne sont pas inclus, car vous devez uniquement une seule fois.

## <a name="building-a-single-app-within-a-docker-container-using-visual-studio-code-and-docker-cli"></a>Création d’une application unique dans un conteneur Docker à l’aide de Visual Studio Code et interface CLI Docker

Les applications sont constituées à partir de vos propres services ainsi que des bibliothèques supplémentaires (dépendances).

Figure 4-22 montre les étapes de base que vous devez généralement exécuter lors de la création d’une application Docker, suivie d’une description détaillée de chaque étape.

![Vue d’ensemble du flux de travail : Étape 1 : Code, étape 2 : écrire des fichiers Dockerfile, étape 3 : créer des images définies avec les fichiers Dockerfile, étape 4 : définir des services avec le fichier docker-compose, étape 5 : exécution conteneurs ou applications composées, étape 6 - tester des applications, étape 7 - Push pour lancer la boucle externe (pipelines CI/CD) ou de continuer de veloping.](./media/image19.png)

**Figure 4-22**. Flux de travail général pour le cycle de vie pour les applications Docker en conteneur à l’aide de la CLI Docker

### <a name="step-1-start-coding-in-visual-studio-code-and-create-your-initial-appservice-baseline"></a>Étape 1 : Commencer le codage dans Visual Studio Code et créer votre base de référence de l’application ou du service initial

Manière de développer votre application est similaire à la façon de que procéder sans Docker. La différence est que lors du développement, vous déployez et testez votre application ou les services qui s’exécutent dans des conteneurs Docker placés dans votre environnement local (comme un Linux VM ou de Windows).

**Configuration de votre environnement local**

Avec les dernières versions de Docker pour Mac et Windows, il est plus facile que jamais pour développer des applications de Docker, et le programme d’installation est simple.

> [!INFORMATION]
>
> Pour obtenir des instructions sur la configuration de Docker pour Windows, accédez à <https://docs.docker.com/docker-for-windows/>.
>
>Pour obtenir des instructions sur la configuration Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.

Vous devez en outre, un éditeur de code afin que vous pouvez développer en fait votre application tout en utilisant l’interface CLI Docker.

Microsoft fournit Visual Studio Code, qui est un éditeur de code léger qui est pris en charge sur Mac, Windows et Linux et fournit des fonctionnalités IntelliSense avec [prise en charge de nombreux langages](https://code.visualstudio.com/docs/languages/overview) (JavaScript, .NET, Go, Java, Ruby, Python et la plupart les langages modernes), [débogage](https://code.visualstudio.com/Docs/editor/debugging), [une intégration avec Git](https://code.visualstudio.com/Docs/editor/versioncontrol) et [prise en charge des extensions](https://code.visualstudio.com/docs/extensions/overview). Cet éditeur est parfait pour les développeurs Mac et Linux. Dans Windows, vous pouvez également utiliser l’application complète de Visual Studio.

> [!INFORMATION]
>
> Pour obtenir des instructions sur l’installation de Visual Studio Code pour Windows, Mac ou Linux, accédez à <https://code.visualstudio.com/docs/setup/setup-overview/>.
>
> Pour obtenir des instructions sur la configuration Docker pour Mac, accédez à <https://docs.docker.com/docker-for-mac/>.

Vous pouvez utiliser avec l’interface CLI Docker et écrivez votre code à l’aide de n’importe quel éditeur de code, mais à l’aide de Visual Studio Code avec l’extension Docker facilite auteur `Dockerfile` et `docker-compose.yml` fichiers dans votre espace de travail. Vous pouvez également exécuter des tâches et des scripts à partir de l’IDE de Visual Studio Code pour exécuter des commandes Docker à l’aide de l’interface CLI Docker en dessous.

L’extension Docker pour VS Code fournit les fonctionnalités suivantes :

- Automatique `Dockerfile` et `docker-compose.yml` génération de fichiers

- Conseils de mise en surbrillance et le pointage de syntaxe pour `docker-compose.yml` et `Dockerfile` fichiers

- IntelliSense (saisie semi-automatique) pour `Dockerfile` et `docker-compose.yml` fichiers

- Linting (erreurs et avertissements) pour `Dockerfile` fichiers

- Intégration de Palette (F1) pour les commandes Docker les plus courantes de commande

- Intégration de l’Explorateur pour la gestion des Images et des conteneurs

- Déployer des images à partir de DockerHub et des registres de conteneurs Azure sur Azure App Service

Pour installer l’extension Docker, appuyez sur Ctrl + Maj + P, tapez `ext install`, puis exécutez la commande d’installer l’Extension pour afficher la liste des extensions Marketplace. Ensuite, tapez **docker** pour filtrer les résultats, puis sélectionnez l’extension de la prise en charge Docker, comme illustré dans la Figure 4-23.

![Affichage de l’extension Docker pour VS Code.](./media/image20.png)

**Figure 4-23**. L’installation de l’Extension Docker dans Visual Studio Code

### <a name="step-2-create-a-dockerfile-related-to-an-existing-image-plain-os-or-dev-environments-like-net-core-nodejs-and-ruby"></a>Étape 2 : Créer un fichier DockerFile associé à une image existante (système d’exploitation brut ou des environnements de développement tels que .NET Core, Node.js et Ruby)

Vous aurez besoin d’un `DockerFile` par une image personnalisée à générer et par conteneur à déployer. Si votre application est composée d’un seul service personnalisé, vous aurez besoin d’un seul `DockerFile`. Mais si votre application est composée de plusieurs services (comme dans une architecture de microservices), vous avez besoin d’un `Dockerfile` par service.

Le `DockerFile` est généralement placé dans le dossier racine de votre application ou service et contient les commandes requises pour que cette Docker sache comment configurer et exécuter l’application ou le service. Vous pouvez créer votre `DockerFile` et ajoutez-le à votre projet, ainsi que votre code (node.js, .NET Core, etc.), ou, si vous débutez avec l’environnement, examinons l’info-bulle suivante.

> [!TIP]
>
> Vous pouvez utiliser l’extension Docker pour vous guider lors de l’utilisation du `Dockerfile` et `docker-compose.yml` les fichiers liés à vos conteneurs Docker. Finalement, vous allez probablement écrire ces types de fichiers sans cet outil, mais à l’aide de l’extension Docker est un bon point de départ qui permettra d’accélérer votre courbe d’apprentissage.

Dans la Figure 4-24, vous pouvez voir comment une commande docker-compose fichier est ajouté à l’aide de l’Extension Docker pour VS Code.

![Affichage de la console de l’extension Docker pour VS Code.](./media/image24.png)

**Figure 4-24**. Fichiers docker ajoutés à l’aide de la **fichiers Docker ajouter à la commande de l’espace de travail**

Lorsque vous ajoutez un fichier DockerFile, vous spécifiez quelle image Docker de base vous allez utiliser (comme à l’aide de `FROM mcr.microsoft.com/dotnet/core/aspnet`). Vous allez générer généralement votre image personnalisée sur une image de base que vous obtenez à partir de n’importe quel dépôt officiel dans le [Registre Docker Hub](https://hub.docker.com/) (comme un [image pour .NET Core](https://hub.docker.com/_/microsoft-dotnet-core/) ou celui [pour Node.js](https://hub.docker.com/_/node/)).

***Utilisez une image Docker officielle existante***

À l’aide d’un dépôt officiel de la pile de langage avec un numéro de version garantit que les mêmes fonctionnalités de langage sont disponibles sur toutes les machines (y compris le développement, test et production).

Voici un exemple de fichier DockerFile pour un conteneur .NET Core :

```Dockerfile
# Base Docker image to use  
FROM mcr.microsoft.com/dotnet/core/aspnet:2.2
  
# Set the Working Directory and files to be copied to the image  
ARG source  
WORKDIR /app  
COPY ${source:-bin/Release/PublishOutput} .  
  
# Configure the listening port to 80 (Internal/Secured port within Docker host)  
EXPOSE 80  
  
# Application entry point  
ENTRYPOINT ["dotnet", "MyCustomMicroservice.dll"]
```

Dans ce cas, l’image est basée sur la version 2.2 de l’image Docker ASP.NET Core officielle (multi-arch pour Linux et Windows), conformément à la ligne `FROM mcr.microsoft.com/dotnet/core/aspnet:2.2`. (Pour plus d’informations sur cette rubrique, consultez le [Image Docker ASP.NET Core](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) page et le [Image Docker .NET Core](https://hub.docker.com/_/microsoft-dotnet-core/) page).

Dans le fichier DockerFile, vous pouvez également demander à Docker d’écouter sur le port TCP que vous utiliserez lors de l’exécution (par exemple, le port 80).

Vous pouvez spécifier des paramètres de configuration supplémentaires dans le fichier Dockerfile, en fonction du langage et du framework que vous utilisez. Par exemple, le `ENTRYPOINT` ligne avec `["dotnet", "MySingleContainerWebApp.dll"]` indique à Docker pour exécuter une application .NET Core. Si vous utilisez le Kit de développement et de l’interface CLI .NET Core (`dotnet CLI`) pour générer et exécuter l’application .NET, ce paramètre est différent. Le point clé ici est que la ligne ENTRYPOINT et autres paramètres dépendent de la langue et la plateforme que vous choisissez pour votre application.

> [!INFORMATION]
>
> Pour plus d’informations sur la création d’images Docker pour les applications .NET Core, accédez à <https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images>.
>
> Pour en savoir plus sur la création de vos propres images, accédez à <https://docs.docker.com/engine/tutorials/dockerimages/>.

**Utiliser les référentiels d’images multi-arch**

Un nom d’image unique dans un référentiel peut contenir des variantes de plateforme, par exemple une image Linux et une image de Windows. Cette fonctionnalité permet aux fournisseurs comme Microsoft (créateurs d’images de base) créer un référentiel unique pour plusieurs plateformes (autrement dit, Linux et Windows). Par exemple, le [dotnet/core/aspnet](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) référentiel disponible dans le Registre Docker Hub fournit la prise en charge de Linux et Windows Nano Server en utilisant le même nom d’image.

Extraction de la [dotnet/core/aspnet](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) image à partir d’un ordinateur hôte Windows extrait la variante de Windows, tandis que l’extraction du même nom d’image à partir d’un hôte Linux extrait la variante Linux.

***Créer votre image de base à partir de zéro***

Vous pouvez créer votre propre image de base de Docker à partir de zéro, comme expliqué dans cet [article](https://docs.docker.com/engine/userguide/eng-image/baseimages/) à partir de Docker. Ce scénario n’est probablement pas vous convient le mieux si vous venez de démarrer avec Docker, mais si vous souhaitez définir les bits spécifiques de votre propre image de base, vous pouvez le faire.

### <a name="step-3-create-your-custom-docker-images-embedding-your-service-in-it"></a>Étape 3 : Créer votre l’incorporation de votre service qu’il contient des images Docker personnalisées

Pour chaque service personnalisé qui compose votre application, vous devez créer une image associée. Si votre application est composée d’un service unique ou d’application web, vous aurez besoin en une seule image.

> [!NOTE]
>
> Lorsque prenant en compte la « boucle externe flux de travail DevOps », les images seront créées par un processus de génération automatisé dès que vous ajoutez votre code source à un référentiel Git (intégration continue), donc les images sont créées dans cet environnement global à partir de votre code source.
>
> Mais nous estimons qu’accédant à cet itinéraire de la boucle externe, nous devons vérifier que l’application Docker réellement fonctionne correctement afin qu’ils n’est pas envoyé de code qui peut ne pas fonctionne correctement pour le système de contrôle de code source (Git, etc.).
>
> Par conséquent, chaque développeur doit d’abord faire tout le processus de boucle interne pour tester localement et continuer à développer jusqu'à ce qu’ils souhaitent push d’une fonctionnalité complète ou de modifier le système de contrôle source.

Pour créer une image dans votre environnement local et à l’aide du fichier DockerFile, vous pouvez utiliser la commande docker build, comme illustré dans la Figure 4-25 (vous pouvez également exécuter `docker-compose up --build` pour des applications composées de plusieurs conteneurs/Services).

![Sortie de la console de la build de docker-compose, affichant les images de la progression du téléchargement.](./media/image25.png)

**Figure 4-25**. Build de docker en cours d’exécution

Si vous le souhaitez, au lieu d’exécuter directement `docker build` à partir du dossier de projet, vous pouvez tout d’abord générer un dossier déployable avec les bibliothèques .NET nécessaires à l’aide de l’exécution `dotnet publish` commande, puis exécutez `docker build`.

Cet exemple crée une image Docker avec le nom `cesardl/netcore-webapi-microservice-docker:first` (`:first` est une balise, comme une version spécifique). Vous pouvez effectuer cette étape pour chaque image personnalisée que vous créez pour votre application Docker composée avec plusieurs conteneurs.

Vous trouverez les images existantes dans votre référentiel local (votre ordinateur de développement) à l’aide de docker commande images, comme illustré dans la Figure 4-26.

![Sortie à partir d’images docker de commande, affichant les images existantes de la console.](./media/image26.png)

**Figure 4-26**. Affichage des images existantes à l’aide d’images docker

### <a name="step-4-define-your-services-in-docker-composeyml-when-building-a-composed-docker-app-with-multiple-services"></a>Étape 4 : Définir vos services dans docker-compose.yml lors de la création d’une application Docker composée avec plusieurs services

Avec le `docker-compose.yml` fichier, vous pouvez définir un ensemble de services à être déployé comme une application composée avec les commandes de déploiement expliqués dans la section étape suivante.

Créez ce fichier dans votre main ou un dossier de solution racine ; Il doit avoir contenu similaire à celle illustrée dans ce `docker-compose.yml` fichier :

```yml
version: '3.4'
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

- Construire à partir du fichier DockerFile dans le répertoire actif

- Transférer le port exposé 80 sur le conteneur sur le port 81 sur l’ordinateur hôte

- Monter le répertoire du projet sur l’ordinateur hôte/code au sein du conteneur, ce qui permet de modifier le code sans avoir à recréer l’image

- Lier le service web au service redis

Le service redis utilise le [dernière image publique redis](https://hub.docker.com/_/redis/) extraite du Registre Docker Hub. [redis](https://redis.io/) est un système de cache bien connu pour les applications côté serveur.

### <a name="step-5-build-and-run-your-docker-app"></a>Étape 5 : Générer et exécuter votre application Docker

Si votre application a uniquement un seul conteneur, vous devez l’exécuter en la déployant sur votre hôte Docker (machine virtuelle ou serveur physique). Toutefois, si votre application est composée de plusieurs services, vous devez *composer*, trop. Nous allons voir les différentes options.

***Option a : Exécuter un conteneur unique ou un service***

Vous pouvez exécuter l’image Docker à l’aide de la commande docker run, comme illustré ici :

```console
docker run -t -d -p 80:5000 cesardl/netcore-webapi-microservice-docker:first
```

Pour ce déploiement, nous allons redirection des demandes envoyées vers le port 80 vers le port interne 5000. Maintenant l’application est à l’écoute sur le port externe 80 au niveau de l’hôte.

***Option b : Composer et exécuter une application de plusieurs conteneurs***

Dans la plupart des scénarios d’entreprise, une application Docker est composée de plusieurs services. Dans ce cas, vous pouvez exécuter la `docker-compose up` commande (Figure 4-27), qui utilise le fichier docker-compose.yml que vous avez peut-être créé précédemment. Exécution de cette commande déploie une application composée avec toutes ses conteneurs associés.

![Sortie à partir de la console le-commande docker compose up.](./media/image27.png)

**Figure 4-27**. Résultats de l’exécution de la commande « docker-compose up »

Après avoir exécuté `docker-compose up`, vous déployez votre application et ses conteneurs associés sur votre hôte Docker, comme illustré dans la Figure 4-28, dans la représentation sous forme de machine virtuelle.

![Machine virtuelle exécutant des applications à plusieurs conteneurs.](./media/image28.png)

**Figure 4-28**. Machine virtuelle avec des conteneurs Docker déployés

### <a name="step-6-test-your-docker-application-locally-in-your-local-cd-vm"></a>Étape 6 : Tester votre application Docker (local, dans votre machine virtuelle de CD locale)

Cette étape varie en fonction de ce que fait votre application.

Dans une simple API .NET Core Web « Hello World » déployé comme un seul conteneur ou un service, vous devez simplement accéder au service en fournissant le port TCP spécifié dans le fichier DockerFile.

Si localhost est désactivée, pour accéder à votre service, vous pouvez trouver l’adresse IP de l’ordinateur à l’aide de cette commande :

```console
docker-machine {IP} {YOUR-CONTAINER-NAME}
```

Sur l’hôte Docker, ouvrez un navigateur et accédez à ce site ; Vous devez voir votre application ou du service en cours d’exécution, comme illustré dans la Figure 4-29.

![Affichage du navigateur de la réponse à partir de localhost/API/values.](./media/image29.png)

**Figure 4-29**. Test de votre application Docker localement en utilisant localhost

Notez qu’il utilise le port 80, mais en interne qu’il est redirigé vers le port 5000, parce que c’est la façon dont elle a été déployée avec `docker run`, comme expliqué précédemment.

Vous pouvez tester cela à l’aide de CURL à partir du terminal. Dans une installation de Docker sur Windows, l’adresse IP par défaut est 10.0.75.1, comme illustré dans la Figure 4-30.

![Sortie à partir de l’obtention de la console le http://10.0.75.1/API/values avec curl](./media/image30.png)

**Figure 4-30**. Test d’une application de Docker localement à l’aide de CURL

**Débogage d’un conteneur en cours d’exécution sur Docker**

Visual Studio Code prend en charge le débogage Docker si vous utilisez Node.js et autres plateformes telles que les conteneurs .NET Core.

Vous également pouvez déboguer les conteneurs .NET Core ou .NET Framework dans Docker lorsque vous utilisez Visual Studio pour Windows ou Mac, comme décrit dans la section suivante.

> [!INFORMATION]
>
> Pour en savoir plus sur le débogage des conteneurs Docker de Node.js, accédez à <https://blog.docker.com/2016/07/live-debugging-docker/> et <https://blogs.msdn.microsoft.com/user_ed/2016/02/27/visual-studio-code-new-features-13-big-debugging-updates-rich-object-hover-conditional-breakpoints-node-js-mono-more/>.

>[!div class="step-by-step"]
>[Précédent](docker-apps-development-environment.md)
>[Suivant](visual-studio-tools-for-docker.md)
