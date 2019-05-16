---
title: Approches de déploiement d’architecture - applications sans serveur
description: Un repère de façons différentes architectures d’entreprise sont déployés dans le cloud, comparaison entre IaaS, PaaS, conteneurs et sans serveur.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 75fd35a906048a96dbd9f6205ead832dfd667455
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65643380"
---
# <a name="architecture-deployment-approaches"></a>Approches du déploiement de l’architecture

Quel que soit l’architecture approche permet de concevoir une application métier, l’implémentation ou le déploiement de ces applications peut-être varier. Les entreprises hébergent des applications sur tous les éléments du matériel physique pour les fonctions sans serveur.

## <a name="n-tier-applications"></a>Applications multicouches

Le [modèle d’architecture multiniveau](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/n-tier) une architecture mature et simplement fait référence aux applications qui séparent les différentes couches de logiques dans les niveaux physiques distincts. Architecture multiniveau est une implémentation physique de l’architecture de couche N. L’implémentation la plus courante de cette architecture inclut :

* Une couche de présentation, par exemple une application web.
* Un niveau d’accès API ou des données, comme une API REST.
* Une couche de données, par exemple une base de données SQL.

![Architecture multiniveau](./media/n-tier-architecture.png)

Solutions multicouches présentent les caractéristiques suivantes :

* Projets sont généralement alignées avec les niveaux.
* Tests peuvent être abordées sous différemment par niveau.
* Niveaux de fournissent des couches d’abstraction, par exemple la couche de présentation connaît généralement les détails d’implémentation de la couche données.
* En règle générale, les couches interagissent uniquement avec les couches adjacentes.
* Les versions sont souvent gérés par le projet et par conséquent tier, niveau. Une simple modification de l’API peut nécessiter une nouvelle version d’un niveau intermédiaire entière.

Cette approche présente plusieurs avantages, notamment :

* Isolation de la base de données (souvent le serveur frontal n’a pas un accès direct au serveur principal de base de données).
* Réutilisation de l’API (par exemple, mobile, bureau et les clients d’application web peuvent tous les réutiliser les mêmes API).
* Possibilité de monter en charge des niveaux indépendamment des autres.
* Refactorisation d’isolation : un niveau peut être refactorisé sans affecter les autres niveaux.

## <a name="on-premises-and-infrastructure-as-a-service-iaas"></a>En local et l’Infrastructure en tant que Service (IaaS)

L’approche traditionnelle à l’hébergement d’applications nécessite l’achat de matériel et de la gestion de toutes les installations de logiciels, y compris le système d’exploitation. À l’origine ce qui impliquait centres de données coûteux et de matériel physique. Les défis auxquels sont fournis avec le fonctionnement du matériel physique sont nombreux, y compris :

* La nécessité d’acheter excédentaire pour « mesure de précaution » ou de pics de scénarios à la demande.
* Sécurisation de l’accès physique au matériel.
* Responsabilité de défaillance matérielle (par exemple, la défaillance de disque).
* Refroidissement.
* Configuration de routeurs et les équilibreurs de charge.
* Redondance de l’alimentation.
* Sécurisation de l’accès aux logiciels.

![Approche IaaS](./media/iaas-approach.png)

La virtualisation de matériel, via des « machines virtuelles » permet d’Infrastructure en tant que Service (IaaS). Ordinateurs hôtes sont partitionnés efficacement pour fournir des ressources pour les instances avec des allocations pour leur propre mémoire, UC et de stockage. L’équipe approvisionne les machines virtuelles nécessaires et configure les réseaux associés et l’accès au stockage.

Pour plus d’informations, consultez [machine virtuelle architecture de référence multiniveau](https://docs.microsoft.com/azure/architecture/reference-architectures/virtual-machines-windows/n-tier).

Bien que la virtualisation et l’Infrastructure en tant que Service (IaaS) résoudre les problèmes de nombreuses, il laisse toujours autant de responsabilités entre les mains de l’équipe d’infrastructure. L’équipe gère les versions de système d’exploitation applique les correctifs de sécurité et installe les dépendances tierces sur les ordinateurs cibles. Applications souvent se comportent différemment sur les machines de production par rapport à l’environnement de test. Problèmes surviennent en raison des versions de dépendance différente et/ou les niveaux de référence (SKU) du système d’exploitation. Bien que de nombreuses entreprises déploient des applications multicouches pour ces cibles, de nombreuses entreprises bénéficient du déploiement à un autre modèle natif cloud tel que [plateforme en tant que Service](#platform-as-a-service-paas). Architectures de microservices sont plus difficile en raison des exigences de monter en charge pour l’élasticité et la résilience.

Pour plus d’informations, consultez [machines virtuelles](https://docs.microsoft.com/azure/virtual-machines/).

## <a name="platform-as-a-service-paas"></a>Plateforme en tant que Service (PaaS)

Plateforme comme un Service (PaaS) offre configuré les développeurs peuvent incorporer directement dans des solutions. PaaS est un autre terme pour les d’hébergement géré. Il élimine la nécessité de gérer le système d’exploitation de base, les correctifs de sécurité et dans de nombreux cas, toutes les dépendances tierces. Applications web, bases de données, des exemples de plateformes et de backends mobiles.

PaaS résout les défis courants pour IaaS. PaaS permet au développeur de se concentrer sur le schéma de base de données ou de code plutôt que la façon dont il est déployé. PaaS présentent les avantages suivants :

* Payez pour utiliser les modèles qui éliminent la surcharge d’un investissement dans des machines inactifs.
* Diriger le déploiement et DevOps amélioré, intégration continue (CI) et les pipelines de livraison continue (CD).
* Mises à niveau automatiques, les mises à jour et les correctifs de sécurité.
* Bouton-poussoir montée en puissance et montée en puissance (élastique).

Le principal inconvénient de PaaS traditionnellement vis-à-vis d’un fournisseur. Par exemple, certains fournisseurs PaaS uniquement en charge ASP.NET, Node.js, ou autres langages spécifiques et les plateformes. Produits tels qu’Azure App Service ont évolué pour résoudre plusieurs plateformes et de prendre en charge une variété de langages et infrastructures pour l’hébergement d’applications web.

![Plateforme en tant qu’une Architecture de Service](./media/paas-architecture.png)

## <a name="software-as-a-service-saas"></a>Software as a Service (SaaS)

Logiciel en tant que Service ou SaaS est centralisée hébergé et disponible sans installation locale ou approvisionner. SaaS est souvent hébergé sur PaaS en tant que plateforme de déploiement des logiciels. SaaS fournit des services pour exécuter et se connecter avec les logiciels existants. SaaS est souvent industrie et verticales spécifiques. SaaS est souvent concédé sous licence et fournit généralement un modèle client/serveur. La plupart des offres SaaS utilisent des applications basées sur le web pour le client. Entreprises considère généralement SaaS comme une solution d’entreprise aux offres de licence. Souvent, il n’est pas implémenté en contrepartie d’architecture pour l’évolutivité et la facilité de gestion d’une application. En effet, la plupart des solutions SaaS s’appuient sur IaaS, PaaS et/ou sans serveur back-ends.

En savoir plus sur SaaS via un [exemple d’application](https://docs.microsoft.com/azure/sql-database/saas-tenancy-welcome-wingtip-tickets-app).

## <a name="containers-and-functions-as-a-service-faas"></a>Conteneurs et les fonctions en tant que Service (FaaS)

Les conteneurs sont une solution intéressante qui permet les avantages de PaaS de type sans la surcharge IaaS. Un conteneur est essentiellement un runtime qui contient les éléments essentiels nécessaires pour exécuter une application unique. La partie du noyau ou core du système d’exploitation hôte et de services de stockage sont partagées par un hôte. Le noyau partagé permet aux conteneurs d’être légers (certains sont simples méga-octets, par rapport à la taille du gigaoctet des machines virtuelles classiques). Avec les hôtes déjà en cours d’exécution, les conteneurs peuvent être démarrés rapidement, ce qui facilite la haute disponibilité. La possibilité de tourner des conteneurs rapidement fournit également des couches supplémentaires de la résilience. Docker est une des implémentations plus populaires de conteneurs.

Conteneurs présentent les avantages suivants :

* Légère et portable
* Autonome donc pas nécessaire d’installer les dépendances
* Fournir un environnement cohérent indépendamment de l’hôte (exactement les mêmes sur un ordinateur portable que sur un serveur cloud s’exécute)
* Peut être configuré rapidement pour la montée en puissance
* Peut être redémarré rapidement pour récupérer après une panne

Un conteneur s’exécute sur un hôte de conteneur (qui à son tour peut s’exécuter sur un un ordinateur nu ou une machine virtuelle). Plusieurs conteneurs ou les instances des mêmes conteneurs peuvent s’exécuter sur un seul hôte. Pour le basculement true et la résilience, conteneurs doivent être mis à l’échelle entre les hôtes.

Pour plus d’informations sur les conteneurs Docker, consultez [What ' s Docker](../microservices-architecture/container-docker-introduction/docker-defined.md)?

La gestion des conteneurs entre hôtes généralement nécessite un outil d’orchestration tels que Kubernetes. Configuration et gestion des solutions d’orchestration peuvent ajouter une charge supplémentaire et la complexité aux projets. Heureusement, de nombreux fournisseurs de cloud fournissent des services d’orchestration via des solutions PaaS pour simplifier la gestion de conteneurs.

L’image suivante illustre un exemple installation Kubernetes. L’adresse de nœuds dans l’installation de montée en charge et le basculement. Elles s’exécutent Docker instances de conteneur qui sont gérés par le serveur maître. Le *kubelet* est le client qui relaie les commandes à partir de Kubernetes à Docker.

![Kubernetes](./media/kubernetes-example.png)

Pour plus d’informations sur l’orchestration, consultez [Kubernetes sur Azure](https://docs.microsoft.com/azure/aks/intro-kubernetes).

Fonctions en tant que Service (FaaS) est un service de conteneur spécialisé qui est similaire à sans serveur. Une implémentation spécifique de FaaS, appelé [OpenFaaS](https://github.com/openfaas/faas), repose sur des conteneurs pour fournir des fonctionnalités sans serveur. OpenFaaS fournit des modèles de ce package toutes les dépendances de conteneur nécessaires à l’exécution d’un morceau de code. À l’aide de modèles simplifie le processus de déploiement de code comme une unité fonctionnelle. OpenFaaS cible des architectures qui contiennent déjà des conteneurs et orchestrateurs, car il peut utiliser l’infrastructure existante. Bien qu’il fournisse des fonctionnalités sans serveur, il spécifiquement vous impose d’utiliser Docker et un orchestrateur.

## <a name="serverless"></a>Sans serveur

Une architecture sans serveur offre une séparation claire entre le code et son environnement d’hébergement. Vous implémentez le code dans un *fonction* qui est appelée par un *déclencheur*. Une fois que cette fonction s’arrête, toutes ses ressources nécessaires peuvent être libérés. Le déclencheur peut être manuelle, un processus a expiré, une requête HTTP ou un téléchargement de fichier. Le résultat du déclencheur est l’exécution du code. Bien que les plateformes sans serveur varient, plus fournir un accès aux API et les liaisons prédéfinies pour rationaliser des tâches telles que l’écriture des résultats de base de données ou de la file d’attente.

Sans serveur est une architecture qui s’appuie fortement sur l’abstraction de l’environnement d’hôte pour vous concentrer sur le code. Elle peut être considérée comme *moins server*.

Solutions de conteneur fournissent aux développeurs existants créer des scripts pour publier du code pour les images sans serveur prêt. Autres implémentations utilisent les solutions PaaS existantes pour fournir une architecture évolutive.

L’abstraction signifie que l’équipe DevOps ne configurer ou gérer des serveurs, ni des conteneurs spécifiques. Le code de hôtes plateforme sans serveur, sous forme de script ou des exécutables empaquetées créée avec un SDK connexe et alloue les ressources nécessaires pour le code à l’échelle.

L’illustration suivante les diagrammes de quatre composants sans serveur. Une requête HTTP provoque l’exécution de code API d’extraction. L’API d’extraction insère le code dans une base de données, et l’instruction insert déclenche plusieurs autres fonctions à exécuter pour effectuer des tâches telles que les tâches de calcul et exécuter la commande.

![Mise en œuvre sans serveur](./media/serverless-implementation.png)

Les avantages de sans serveur :

* **Haute densité.** Nombre d’instances du même code sans serveur permettre s’exécuter sur le même hôte par rapport aux conteneurs ou des machines virtuelles. L’échelle d’instances sur plusieurs hôtes augmenter et diminuer la résilience.
* **Facturation de micro**. Facture de fournisseurs plus sans serveur basée sur les exécutions sans serveur, l’activation des économies énormes dans certains scénarios.
* **Mise à l’échelle instantanée**. Sans serveur peut évoluer pour correspondre à des charges de travail automatiquement et rapidement.
* **Temps de mise sur le marché plus rapide** les développeurs se concentrer sur le code et les déployer directement sur la plateforme sans serveur. Composants peuvent être libérés indépendamment les uns des autres.

Sans serveur est abordée plus souvent dans le contexte de calcul, mais peut s’appliquent également aux données. Par exemple, [SQL Azure](https://docs.microsoft.com/azure/sql-database) et [Cosmos DB](https://docs.microsoft.com/azure/cosmos-db) fournissent tous deux des bases de données cloud qui ne nécessitent pas de vous permettent de configurer des ordinateurs hôtes ou clusters. Ce livre se concentre sur le calcul sans serveur.

## <a name="summary"></a>Récapitulatif

Il existe un large éventail d’options disponibles pour l’architecture, notamment une approche hybride. Sans serveur simplifie l’approche, la gestion et le coût de fonctionnalités d’application au détriment de la portabilité et le contrôle. Toutefois, nombreuses plateformes sans serveur exposent configuration pour vous aider à optimiser la solution. Bonnes pratiques de programmation peuvent également entraîner au code plus portable et moins de verrouillage de plateforme sans serveur. Le tableau suivant illustre les approches d’architecture côte à côte. Choisissez sans serveur en fonction de votre groupe identique besoins, si vous souhaitez gérer le runtime, et comment vous pouvez interrompre vos charges de travail en petits composants. Vous allez découvrir les défis potentiels avec serverless et d’autres points de décision dans le chapitre suivant.

|         |IaaS     |PaaS     |Conteneur|Sans serveur|
|---------|---------|---------|---------|----------|
|**Échelle**|MACHINE VIRTUELLE       |Instance |Application      |Fonction  |
|**Résumés**|Matériel|Plateforme|Système d’exploitation hôte|Runtime   |
|**Unité** |MACHINE VIRTUELLE       |Projet  |Image    |Code      |
|**Durée de vie**|mois|Jours du mois|Minutes jours|Millisecondes à quelques Minutes|
|**responsabilité**|Système d’exploitation, les dépendances, runtime et les applications|Applications et dépendances|Runtime, les dépendances et les applications|Fonction

* **Mise à l’échelle** fait référence à l’unité qui est utilisée pour mettre à l’échelle de l’application
* **Effectue l’abstraction** fait référence à la couche est abstrait par l’implémentation
* **Unité** fait référence à la portée de ce qui est déployé
* **Durée de vie** fait référence à l’exécution classique d’une instance spécifique
* **Responsabilité** fait référence à la surcharge liée à générer, déployer et tenir à jour de l’application

Le chapitre suivant sera vous concentrer sur une architecture sans serveur, cas d’usage et modèles de conception.

## <a name="recommended-resources"></a>Ressources recommandées

* [Guide d’architecture application Windows Azure](https://docs.microsoft.com/azure/architecture/guide/)
* [Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db)
* [Azure SQL](https://docs.microsoft.com/azure/sql-database)
* [Modèle d’architecture multiniveau](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/n-tier)
* [Kubernetes sur Azure](https://docs.microsoft.com/azure/aks/intro-kubernetes)
* [Microservices](https://docs.microsoft.com/azure/architecture/guide/architecture-styles/microservices)
* [Architecture de référence de machine virtuelle à plusieurs niveaux](https://docs.microsoft.com/azure/architecture/reference-architectures/virtual-machines-windows/n-tier)
* [Machines virtuelles](https://docs.microsoft.com/azure/virtual-machines/)
* [Qu’est-ce que Docker ?](../microservices-architecture/container-docker-introduction/docker-defined.md)
* [Exemple d’application Wingtip Tickets SaaS](https://docs.microsoft.com/azure/sql-database/saas-tenancy-welcome-wingtip-tickets-app)

>[!div class="step-by-step"]
>[Précédent](architecture-approaches.md)
>[Suivant](serverless-architecture.md)
