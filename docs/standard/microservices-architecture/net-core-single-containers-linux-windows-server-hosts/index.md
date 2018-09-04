---
title: Déploiement d’applications web .NET Core basées sur un seul conteneur sur des hôtes Linux ou Windows Nano Server
description: Architecture des microservices .NET pour les applications .NET en conteneur | Déploiement d’applications web .NET Core basées sur un seul conteneur sur des hôtes Linux ou Windows Nano Server
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 06/27/2018
ms.openlocfilehash: 45be99a86a52ed450b795ca5f91c01ab82c7da47
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43388626"
---
# <a name="deploying-single-container-based-net-core-web-applications-on-linux-or-windows-nano-server-hosts"></a>Déploiement d’applications web .NET Core basées sur un seul conteneur sur des hôtes Linux ou Windows Nano Server

_Vous pouvez utiliser des conteneurs Docker pour effectuer un déploiement monolithique d’applications web simples. Cela a pour effet d’améliorer les pipelines d’intégration continue et de déploiement continu et cela contribuer à la réussite du déploiement en production. Fini les « Comment cela se fait-il que cela fonctionne sur ma machine, mais pas en production ? »_

Une architecture basée sur des microservices présente de nombreux avantages, mais ces avantages se payent par une complexité accrue. Dans certains cas, les inconvénients prennent le pas sur les avantages et une application à déploiement monolithique s’exécutant dans un seul ou dans quelques conteneurs seulement est une meilleure option.

Il n’est pas toujours évident de décomposer une application monolithique en plusieurs microservices bien distincts. Vous avez appris que ces microservices devaient être partitionnés par fonction : ils doivent fonctionner indépendamment les uns des autres pour optimiser la résilience de l’application. Si vous ne pouvez pas proposer l’application par tranches de fonctionnalités, la diviser ne fait qu’ajouter de la complexité.

Une application n’est pas pour autant nécessairement amenée à mettre à l’échelle les fonctionnalités de façon indépendante. Supposons qu’au début de l’existence de l’application de référence `eShopOnContainers`, le trafic ne justifiait pas de séparer les fonctionnalités en différents microservices. Le trafic était si faible que le fait d’ajouter des ressources à un service revenait en fait à les ajouter à tous les services. Séparer l’application en services distincts aurait apporté des avantages minimes au regard du travail supplémentaire que cela demandait.

De même, lors de la phase initiale du développement d’une application, vous n’avez peut-être pas une idée précise de là où se trouvent les limites fonctionnelles naturelles. Même à un stade de développement où le produit est viable, il est possible que cette séparation naturelle ne se dégage toujours pas.

Certaines de ces conditions peuvent être passagères. Vous pouvez commencer par créer une application monolithique et séparer par la suite certaines fonctionnalités en les développant et les déployant sous forme de microservices. D’autres conditions peuvent être essentielles à l’espace de problème de l’application, ce qui signifie que l’application risque de ne jamais être divisée en plusieurs microservices.

Séparer une application en divers processus distincts induit aussi des coûts. Il est plus complexe de séparer des fonctionnalités en différents processus. Les protocoles de communication deviennent plus complexes. Au lieu d’appeler des méthodes, vous devez utiliser des communications asynchrones entre les services. Quand il s’agit de déplacer une architecture de microservices, vous devez ajouter de nombreux blocs de construction implémentés dans la version des microservices de l’application `eShopOnContainers` : gestion du bus d’événements, résilience des messages et nouvelles tentatives, cohérence à terme, etc.

Une version très simplifiée d’eShopOnContainers (nommée [eShopWeb](https://github.com/dotnet-architecture/eShopOnContainers/tree/master/src/Web/WebMonolithic) et figurant dans le même dépôt GitHub) s’exécute en tant qu’application MVC monolithique. Comme nous l’avons vu, ce choix de conception offre des avantages. Vous pouvez télécharger la source de cette application sur GitHub et l’exécuter localement. Même cette application monolithique gagne à être déployée dans un environnement de conteneurs.

Tout d’abord, un déploiement en conteneur signifie que chaque instance de l’application s’exécute dans le même environnement. Cela inclut l’environnement de développement dans lequel les tests de la première heure et le développement ont été réalisés. L’équipe de développement peut exécuter l’application dans un environnement à conteneurs qui correspond à l’environnement de production.

En outre, la montée en charge des applications en conteneur est moins coûteuse. Comme nous l’avons vu précédemment, l’environnement à conteneurs permet un meilleur partage des ressources que les environnements à machines virtuelles classiques.

Enfin, la mise en conteneur de l’application contraint à établir une séparation entre la logique métier et le serveur de stockage. À mesure que l’application monte en charge, les différents conteneurs dépendent tous d’un même support de stockage physique. Il s’agit généralement d’un serveur à haute disponibilité exécutant une base de données SQL Server.

## <a name="application-tour"></a>Exploration de l’application

L’application [eShopWeb](https://github.com/dotnet-architecture/eShopOnContainers/tree/master/src/Web/WebMonolithic) représente une partie de l’application eShopOnContainers s’exécutant en tant qu’application monolithique, c’est-à-dire une application basée sur ASP.NET Core MVC s’exécutant sur .NET Core. Elle propose pour l’essentiel les fonctionnalités de consultation de catalogue décrites dans les sections précédentes.

L’application utilise une base de données SQL Server pour le stockage de catalogue. Dans les déploiements basés sur des conteneurs, cette application monolithique peut accéder au même magasin de données que l’application basée sur des microservices. L’application est configurée pour exécuter SQL Server dans un conteneur à côté de l’application monolithique. Dans un environnement de production, SQL Server s’exécuterait sur une machine à haute disponibilité, en dehors de l’hôte Docker. Pour des raisons pratiques, dans un environnement de développement ou de test, il est recommandé d’exécuter SQL Server dans son propre conteneur.

L’ensemble initial de fonctionnalités permet uniquement la consultation du catalogue. Par des mises à jour, il serait possible d’activer l’ensemble complet de fonctionnalités de l’application en conteneur. Une architecture d’application web monolithique plus avancée est décrite dans le livre électronique [ASP.NET Web Application architecture practices](https://aka.ms/webappebook) et [l’exemple d’application eShopOnWeb](https://aka.ms/WebAppArchitecture) associé.

## <a name="docker-support"></a>Prise en charge de Docker

Le projet eShopOnWeb s’exécute sur .NET Core. Cela signifie qu’il peut s’exécuter dans des conteneurs Linux ou Windows. Notez que pour le déploiement de Docker, vous devez utiliser le même type d’hôte pour SQL Server. Les conteneurs Linux offrent un plus faible encombrement et sont à privilégier.

Visual Studio propose un modèle de projet qui ajoute la prise en charge de Docker à une solution. Cliquez avec le bouton droit sur le projet, cliquez sur **Ajouter**, puis sur **Prise en charge de Docker**. Le modèle ajoute un fichier Dockerfile à votre projet, ainsi qu’un nouveau projet **docker-compose** qui fournit un fichier *docker-compose.yml* de démarrage. Cette étape a déjà été effectuée dans le projet eShopOnWeb téléchargé sur GitHub. Vous pouvez constater que la solution contient le projet **eShopOnWeb** et le projet **docker-compose**, comme illustré dans la figure 6-1.

![](./media/image1.png)

**Figure 6-1** : le projet **docker-composer** dans une application web à conteneur unique

Ces fichiers sont des fichiers docker-composer standard, conformément à n’importe quel projet Docker. Vous pouvez les utiliser avec Visual Studio ou à partir de la ligne de commande. Cette application s’exécute sur .NET Core et utilise des conteneurs Linux. Vous pouvez donc aussi le coder, le générer et l’exécuter sur un Mac ou sur une machine Linux.

Le fichier *docker-compose.yml* contient des informations sur les images à générer et les conteneurs à lancer. Les modèles spécifient comment générer l’image `eshopweb` et comment lancer les conteneurs de l’application. Vous devez ajouter la dépendance de SQL Server en incluant une image pour celui-ci (par exemple `mssql-server-linux`), ainsi qu’un service pour l’image sql.data permettant à Docker de générer et de lancer ce conteneur. Ces paramètres sont illustrés dans l’exemple suivant :

```yml
version: '2'

services:
  eshopweb:
    image: eshop/web
    build:
    context: ./eShopWeb
    dockerfile: Dockerfile
    depends_on:
      - sql.data

  sql.data:
    image: microsoft/mssql-server-linux
```

La directive `depends_on` indique à Docker que l’image eShopWeb dépend de l’image sql.data. Les lignes en dessous de `depends_on` sont les instructions pour générer une image étiquetée `sql.data` avec l’image `microsoft/mssql-server-linux`.

Le projet **docker-compose** affiche les autres fichiers docker-compose sous le nœud principal *docker-compose.yml* pour indiquer visuellement que ces fichiers sont apparentés. Le fichier *docker-compose-override.yml* contient les paramètres pour les deux services, comme des chaînes de connexion et d’autres paramètres d’application.

L’exemple suivant montre le fichier *docker-compose.vs.debug.yml*, qui contient les paramètres utilisés pour le débogage dans Visual Studio. Dans ce fichier, la balise dev est ajoutée à l’image eshopweb. Ceci permet de séparer le débogage des images des versions, et de vous éviter ainsi de déployer accidentellement les informations de débogage dans un environnement de production :

```yml
version: '2'

services:
  eshopweb:
    image: eshop/web:dev
    build:
    args:
    source: ${DOCKER_BUILD_SOURCE}
    environment:
      - DOTNET_USE_POLLING_FILE_WATCHER=1
    volumes:
      - ./eShopWeb:/app
      - ~/.nuget/packages:/root/.nuget/packages:ro
      - ~/clrdbg:/clrdbg:ro
    entrypoint: tail -f /dev/null
    labels:
      - "com.microsoft.visualstudio.targetoperatingsystem=linux"
```

Le dernier fichier ajouté est *docker-compose.ci.build.yml*. Il permet de générer le projet à partir d’un serveur CI depuis la ligne de commande. Ce fichier compose démarre un conteneur Docker qui génère les images nécessaires à votre application. L’exemple suivant montre le contenu du fichier *docker-compose.ci.build.yml* :

```yml
version: '2'

services:
  ci-build:
    image: microsoft/aspnetcore-build:latest
    volumes:
      - .:/src
    working_dir: /src
  command: /bin/bash -c "dotnet restore ./eShopWeb.sln && dotnet publish  ./eShopWeb.sln -c Release -o ./obj/Docker/publish"
```

> [!NOTE]
> À compter de .NET Core SDK 2.0, la commande [dotnet restore](../../../core/tools/dotnet-restore.md) s’exécute automatiquement quand [dotnet publish](../../../core/tools/dotnet-publish.md) est exécuté.

Notez que l’image est une image de build ASP.NET Core. Cette image comprend le kit SDK et les outils de génération permettant de générer votre application et de créer les images nécessaires. Le fait d’exécuter le projet **docker-composer** avec ce fichier a pour effet de démarrer le conteneur de build à partir de l’image, puis de générer l’image de votre application dans ce conteneur. Vous spécifiez ce fichier *docker-compose* dans la ligne de commande pour générer votre application dans un conteneur Docker, puis vous la lancez.

Dans Visual Studio, vous pouvez exécuter votre application dans des conteneurs Docker en sélectionnant le projet **docker-composer** comme projet de démarrage, puis en appuyant sur Ctrl+F5 (F5 pour déboguer), comme vous le feriez avec n’importe quelle autre application. Quand vous démarrez le projet **docker-compose**, Visual Studio exécute **docker-compose** en utilisant le fichier *docker-compose.yml*, le fichier *docker-compose.override.yml* et un des fichiers docker-compose.vs.\*. Une fois que l’application a démarré, Visual Studio lance automatiquement le navigateur.

Si vous lancez l’application dans le débogueur, Visual Studio s’attache à l’application en cours d’exécution dans Docker.

## <a name="troubleshooting"></a>Résolution des problèmes

Cette section décrit certains problèmes que vous êtes susceptible de rencontrer pendant l’exécution locale de conteneurs et propose des correctifs.

### <a name="stop-docker-containers"></a>Arrêter des conteneurs Docker

Après avoir lancé l’application en conteneur, les conteneurs continuent de s’exécuter, même après avoir arrêté le débogage. Vous pouvez exécuter la commande `docker ps` depuis la ligne de commande pour voir quels conteneurs s’exécutent. La commande `docker stop` permet d’arrêter un conteneur en cours d’exécution, comme le montre la figure 6-2.

![](./media/image2.png)

**Figure 6-2** : affichage et arrêt de conteneurs à l’aide des commandes CLI docker ps et docker stop

Vous pouvez être amené à arrêter les processus en cours d’exécution quand vous basculez d’une configuration à une autre. Sinon, le conteneur qui exécute l’application web utilise le port de votre application (en l’occurrence, le port 5106).

### <a name="add-docker-to-your-projects"></a>Ajout de Docker à vos projets

L’Assistant qui ajoute la prise en charge de Docker communique avec le processus Docker en cours d’exécution. Si Docker n’est pas en cours d’exécution au moment où vous démarrez l’Assistant, celui-ci ne fonctionne pas correctement. L’Assistant examine votre choix de conteneur actuel pour ajouter la prise en charge de Docker appropriée. Pour ajouter la prise en charge des conteneurs Windows, exécutez l’Assistant pendant que Docker s’exécute avec les conteneurs Windows configurés. Pour ajouter la prise en charge des conteneurs Linux, exécutez l’Assistant pendant que Docker s’exécute avec les conteneurs Linux configurés.

>[!div class="step-by-step"]
[Précédent](../docker-application-development-process/docker-app-development-workflow.md)
[Suivant](../containerize-net-framework-applications/index.md)
