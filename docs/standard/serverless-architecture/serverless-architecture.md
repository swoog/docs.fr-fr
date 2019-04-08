---
title: Architecture sans serveur - applications sans serveur
description: Exploration des différentes architectures et les applications qui sont prises en charge par les architectures sans serveur, y compris les applications web, mobiles et IoT.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 60d225d9794d5c15b0cd8e42800ccad4d7872756
ms.sourcegitcommit: c6f69b0cf149f6b54483a6d5c2ece222913f43ce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55904793"
---
# <a name="serverless-architecture"></a>Architecture sans serveur

Il existe plusieurs approches à l’utilisation de [sans serveur](http://azure.com/serverless) architectures. Ce chapitre explore les exemples d’architectures courantes qui s’intègrent sans serveur. Il couvre également les problèmes qui peuvent poser des problèmes supplémentaires ou requièrent une attention supplémentaire lors de l’implémentation sans serveur. Enfin, plusieurs exemples de conception sont fournies qui illustrent les différents cas d’utilisation sans serveur.

Les hôtes sans serveur utilisent souvent une existante basée sur le conteneur ou une couche de PaaS pour gérer les instances sans serveur. Par exemple, Azure Functions est basée sur [Azure App Service](https://docs.microsoft.com/azure/app-service/). Le Service d’application est utilisé pour monter en charge d’instances et de gérer le runtime qui exécute le code Azure Functions. Pour les fonctions Windows, les exécutions de l’hôte en tant que PaaS et les échelles out le runtime .NET. Pour les fonctions basés sur Linux, l’hôte s’appuie sur les conteneurs.

![Architecture de fonctions Azure](./media/azure-functions-architecture.png)

Les principales tâches Web fournit un contexte d’exécution de la fonction. Le Runtime de langage exécute des scripts, exécute des bibliothèques et héberge l’infrastructure pour le langage cible. Par exemple, Node.js est utilisé pour exécuter des fonctions JavaScript et .NET Framework est utilisé pour exécuter des fonctions C#. Vous en apprendrez davantage sur les options de langage et plateforme plus loin dans ce chapitre.

Certains projets peuvent tirer parti d’une approche plus « complète » pour sans serveur. Les applications qui s’appuient sur des microservices peuvent implémenter tous les microservices à l’aide de la technologie sans serveur. La majorité des applications sont hybride, suivant une conception multicouche et de l’utilisation sans serveur pour les composants qui judicieux, car les composants sont modulaire et évolutif de façon indépendante. Pour aider à bien comprendre ces scénarios, cette section décrit quelques exemples d’architecture courants qui utilisent sans serveur.

## <a name="full-serverless-back-end"></a>Complète sans serveur back-end

Le serveur principal complète sans serveur est idéal pour plusieurs types de scénarios, en particulier lors de la création de nouveaux ou applications de « mode champs vert ». Une application avec une grande surface d’exposition d’API peut-être tirer parti de l’implémentation de chaque API comme une fonction sans serveur. Les applications qui reposent sur l’architecture de microservices sont un autre exemple qui peut être implémenté comme un serveur principal complète sans serveur. Les microservices communiquent via des protocoles différents entre eux. Des scénarios spécifiques sont les suivantes :

* API basée sur les produits SaaS (exemple : processeur de paiements financiers).
* Applications pilotées par des messages (exemple : solution de surveillance des appareils).
* Applications axées sur l’intégration entre les services (exemple : application de réservation des compagnies aériennes).
* Processus qui s’exécutent périodiquement (exemple : nettoyage de base de données en fonction de minuteur).
* Applications axées sur la transformation de données (exemple : importation déclenchée par le chargement de fichiers).
* Extrayez les processus de transformation et chargement (ETL).

Il existe des cas d’usage autres, plus spécifiques qui sont traités plus loin dans ce document.

## <a name="monoliths-and-starving-the-beast"></a>Monolithes et « priver le beast »

Constitue un défi courant est migration d’une application monolithique existante vers le cloud. L’approche moins risqué consiste à « lift- and -shift » entièrement sur des machines virtuelles. Nombreux magasins préfèrent utiliser la migration comme une opportunité pour moderniser leur base de code. Une approche pratique de la migration est appelée « priver le beast. » Dans ce scénario, le MONOLITHE est migrée « en l’état » pour commencer. Ensuite, les services sélectionnés sont modernisées. Dans certains cas, la signature du service est identique à l’original : il est simplement hébergé en tant que fonction. Les clients sont mis à jour pour utiliser le nouveau service plutôt que le point de terminaison MONOLITHE. En attendant, les étapes telles que la réplication de base de données permettent de microservices héberger leur propre stockage, même lorsque les transactions sont toujours gérées par l’application monolithique. Finalement, tous les clients sont migrés vers les nouveaux services. Le MONOLITHE est « privé » (ses services n’est plus appelés) jusqu'à ce que toutes les fonctionnalités a été remplacée. La combinaison de serverless et proxys peuvent faciliter une grande partie de cette migration.

![Migration de MONOLITHE sans serveur](./media/serverless-monolith-migration.png)

Pour en savoir plus sur cette approche, regardez la vidéo : [Importez votre application dans le cloud avec Azure Functions sans serveur](https://channel9.msdn.com/Events/Connect/2017/E102).

## <a name="web-apps"></a>Applications web

Applications Web sont d’excellents candidats pour les applications sans serveur. Il existe deux approches courantes pour les applications web aujourd'hui : gérée par le serveur et pilotés par client (par exemple, les applications à Page unique ou SPA). Applications web d’orientée serveur utilisent généralement une couche d’intergiciel (middleware) pour émettre des appels d’API pour restituer l’interface utilisateur web. Les applications SPA effectuer des appels d’API REST directement à partir du navigateur. Dans les deux scénarios, sans serveur peut prendre en charge l’intergiciel (middleware) ou une demande d’API REST en fournissant la logique métier nécessaire. Une architecture commune consiste à mettre en place un serveur web statique léger. L’Application à Page unique (SPA) fait Office de HTML, CSS, JavaScript et autres ressources de navigateur. L’application web se connecte ensuite à un serveur principal de microservices.

## <a name="mobile-back-ends"></a>Backends mobiles

Le paradigme pilotée par événements des applications sans serveur rend idéal pour le back-ends mobiles. L’appareil mobile déclenche les événements et le code sans serveur s’exécute pour répondre aux requêtes. En tirant parti d’un modèle sans serveur permet aux développeurs d’améliorer la logique métier sans avoir à déployer une mise à jour de l’application complète. L’approche sans serveur permet également aux équipes de partager des points de terminaison et travailler en parallèle.

Développeurs d’applications mobiles peuvent générer une logique métier sans devenir des experts sur le côté serveur. En règle générale, des applications mobiles connectaient à des services locaux. Création de la couche de service requis la présentation de la plateforme de serveur et le paradigme de programmation. Les développeurs a travaillé avec des opérations pour approvisionner les serveurs et les configurer de manière appropriée. Parfois, plusieurs jours ou semaines ont été passées sur la création d’un pipeline de déploiement. Tous ces défis sont abordés par sans serveur.

Sans serveur fait abstraction les dépendances côté serveur et permet au développeur de se concentrer sur la logique métier. Par exemple, un développeur mobile ayant créé des applications à l’aide d’une infrastructure JavaScript peut générer également des fonctions sans serveur avec JavaScript. L’hôte sans serveur gère le système d’exploitation, une instance de Node.js pour héberger le code, les dépendances de package et bien plus encore. Le développeur est fourni à un simple ensemble d’entrées et un modèle standard pour les sorties. Ils puis peuvent se concentrer sur la création et le test de la logique métier. Ils sont donc en mesure d’utiliser des compétences existantes pour générer la logique de back-end pour l’application mobile sans avoir à apprendre de nouvelles plateformes ou devenir un développeur « côté serveur ».

![Fin de backends mobiles](./media/serverless-mobile-backend.png)

La plupart des fournisseurs de cloud offrent des produits sans serveur basés sur mobile qui simplifient le cycle de développement mobile. Les produits peuvent automatiser le provisionnement des bases de données pour conserver les données, gérer les problèmes de DevOps, fournissez basé sur le cloud génère et test des infrastructures et la possibilité de processus d’entreprise de script à l’aide du développeur, la langue par défaut. Suivant une approche sans serveur centrée sur les mobiles peut de rationaliser les processus. Sans serveur supprime la surcharge considérable de l’approvisionnement, la configuration et la maintenance des serveurs pour le serveur principal mobile.

## <a name="internet-of-things-iot"></a>Internet des objets (IoT)

IoT fait référence à des objets physiques qui sont connectés en réseau. Ils sont parfois appelées « appareils connectés » ou « périphériques intelligents. » Tout depuis les voitures et les distributeurs automatiques peuvent être connectés et envoyer des informations allant de l’inventaire pour les données de capteur telles que la température et d’humidité. Dans l’entreprise, IoT fournit des améliorations de processus d’entreprise via la surveillance et d’automatisation. Données IoT peuvent être utilisées pour réguler le climat dans un entrepôt de grande taille ou de suivi des stocks via la chaîne logistique. IoT peut détecter les dépassements de capacité sur les produits chimiques et appeler le service incendie lors de la détection de fumée.

Le nombre élevé d’appareils et souvent des informations dicte une architecture basée sur les événements à l’itinéraire et traiter des messages. Sans serveur est une solution idéale pour plusieurs raisons :

* Permet de mettre à l’échelle en tant que le volume de périphériques et des données augmente.
* Prend en charge l’ajout de nouveaux points de terminaison pour prendre en charge les nouveaux appareils et capteurs.
* Facilite le contrôle de version indépendant pour les développeurs peuvent mettre à jour la logique métier pour un périphérique spécifique sans avoir à déployer l’ensemble du système.
* La résilience et la mort.

L’omniprésence des IoT a entraîné plusieurs produits sans serveur qui se concentrent spécifiquement sur les problèmes IoT, tel que [Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub). Sans serveur automatise les tâches telles que l’inscription, l’application des stratégies, le suivi et même déploiement de code pour les appareils à *le bord*. Le bord fait référence à des périphériques tels que les capteurs et régulateurs qui sont connectés à, mais pas une partie active d’Internet.

>[!div class="step-by-step"]
>[Précédent](architecture-approaches.md)
>[Suivant](serverless-architecture-considerations.md)
