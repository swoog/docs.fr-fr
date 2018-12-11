---
title: 'Considérations relatives à une architecture sans serveur : applications sans serveur'
description: Comprendre les défis de la conception des applications sans serveur, à partir de la gestion de l’état et le stockage persistant à l’échelle, de journalisation, le suivi et diagnostics.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: b12a09c0fcef7e7ff954a3f959fb9e3080a6e859
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53155062"
---
# <a name="serverless-architecture-considerations"></a>Considérations relatives à une architecture sans serveur

Adoption d’une architecture sans serveur n’est fourni avec certains défis. Cette section explore certaines des considérations plus courantes à connaître. Tous ces défis proposent des solutions. Comme avec tous les choix d’architecture, la décision d’Adoptez le serverless doit être prise uniquement après avoir soigneusement les avantages et inconvénients. Selon les besoins de votre application, vous pouvez décider de qu'une implémentation sans serveur n’est pas la solution idéale pour certains composants.

## <a name="managing-state"></a>Gestion de l’état

Les fonctions sans serveur, comme les microservices en général, sont sans état par défaut. L’état en évitant permet sans serveur est éphémère, monter en charge et pour assurer la résilience sans un point central de défaillance. Dans certains cas, les processus d’entreprise nécessitent état. Si votre processus requiert que l’état, vous avez deux options. Vous pouvez adopter un modèle autre que sans serveur, ou interagir avec un service distinct qui fournit l’état. Ajout d’un état peut compliquer la solution et rendre plus difficile à l’échelle et potentiellement créer un point de défaillance unique. Étudiez attentivement si votre fonction requiert absolument l’état. Si la réponse est « Oui », déterminez s’il est toujours judicieux de mettre en œuvre sans serveur.

Il existe plusieurs solutions à adopter l’état sans compromettre les avantages de sans serveur. Voici quelques-unes des solutions plus populaires :

* Utiliser un magasin de données temporaire ou d’un cache distribué, comme Redis
* État de Store dans une base de données, tels que SQL ou CosmosDB
* Gérer l’état via un moteur de flux de travail comme fonctions durables

La dernière ligne est que vous devez être conscient de la nécessité d’une gestion d’état dans les processus que vous envisagez d’implémenter avec sans serveur.

## <a name="long-running-processes"></a>Processus à long terme

Nombreux avantages liés à sans serveur s’appuient sur les processus en cours éphémère. Les temps d’exécution courtes rendent plus facile pour le fournisseur sans serveur libérer des ressources que les fonctions de fonctions de fin et le partage entre les hôtes. La plupart des fournisseurs de cloud limiter la durée totale, que votre fonction peut s’exécuter à environ 10 minutes. Si votre processus peut prendre plus de temps, vous pouvez envisager une autre implémentation.

Il existe quelques exceptions et les solutions. Une solution peut être pour arrêter votre processus en composants plus petits qui individuellement prennent moins de temps à exécuter. Si votre processus s’exécute longtemps en raison des dépendances, vous pouvez également envisager un flux de travail asynchrone à l’aide d’une solution telle que des fonctions durables. Fonctions durables suspendre et mettre à jour l’état de votre processus pendant qu’il attend sur un processus externe se termine. Traitement asynchrone réduit le temps que le processus s’exécute.

## <a name="startup-time"></a>Temps de démarrage

Un problème potentiel avec des implémentations sans serveur est le temps de démarrage. Pour économiser les ressources, de nombreux fournisseurs sans serveur créent infrastructure « à la demande. » Lorsqu’une fonction sans serveur est déclenchée après une période de temps, les ressources pour héberger la fonction deviez être créé ou redémarré. Dans certaines situations, les démarrages à froid peuvent entraîner des retards de quelques secondes. Temps de démarrage varie entre les fournisseurs et les niveaux de service. Il existe plusieurs approches pour les temps de démarrage adresse s’il est important de réduire à la réussite de l’application.

* Certains fournisseurs permettent aux utilisateurs de payer pour les niveaux de service qui garantissent l’infrastructure est « always on ».
* Implémenter un mécanisme keep-alive (ping le point de terminaison pour qu’il soit « éveillés »).
* Utiliser l’orchestration, comme Kubernetes avec une approche de la fonction en conteneur (l’hôte est déjà en cours d’exécution pour la rotation de nouvelles instances est extrêmement rapide).

## <a name="database-updates-and-migrations"></a>Migrations et mises à jour de la base de données

L’avantage du code sans serveur est que vous pouvez libérer des nouvelles fonctions sans avoir à redéployer l’application entière. Cet avantage peut devenir un inconvénient lorsqu’une base de données relationnelle est impliqué. Modifications apportées aux schémas de base de données sont difficiles à synchroniser avec les mises à jour sans serveur. Défis supplémentaires sont posés lorsque des problèmes surgissent et les modifications doivent être restaurées. L’intégrité des données est l’une des raisons qui est recommandé pour les microservices et les fonctions sans serveur que qu’ils possèdent leurs propres données. Il est possible de déployer les modifications comme une seule unité de calcul et de données. La réalité est que de nombreux systèmes hérités fonctionnalité des bases de données back-end volumineuses qui doivent être synchronisées avec l’architecture sans serveur.

Une approche courante pour résoudre des versions de schéma consiste à jamais modifier les propriétés existantes et les colonnes, mais à la place ajouter de nouvelles informations. Par exemple, considérez une modification apportée à déplacer à partir d’une valeur booléenne « completed » indicateur pour une liste de tâches à une « date d’achèvement ». Au lieu de supprimer l’ancien champ, la modification de la base de données sera :

1. Ajoutez un champ Nouveau « date de fin ».
1. Transformez le champ booléen « terminé » à une fonction calculée qui détermine si la date d’achèvement est après la date actuelle.
1. Ajouter un déclencheur pour définir la date d’achèvement à la date actuelle lorsque la valeur booléenne terminée est définie sur true.

La séquence de modifications garantit que le code hérité continue à s’exécuter « tel quel », tandis que les fonctions sans serveur plus récente peuvent tirer parti du nouveau champ.

Pour plus d’informations sur les données dans les architectures sans serveur, consultez [défis et solutions pour la gestion de données distribuée](../microservices-architecture/architect-microservice-container-applications/distributed-data-management.md).

## <a name="scaling"></a>Mise à l'échelle

Il est souvent à tort que sans serveur ne signifie « aucun serveur ». Il s’agit en fait « moins serveur. » Il le fait est qu'une infrastructure de sauvegarde est importante de comprendre quand il s’agit de mise à l’échelle. Plateformes plus serverless fournissent un ensemble de contrôles pour gérer la façon dont l’infrastructure doit mettre à l’échelle lors de la densité de l’événement augmente. Vous pouvez choisir parmi une variété d’options, mais votre stratégie peut varier en fonction de la fonction. En outre, les fonctions sont généralement exécutées sous un hôte associées, afin que les fonctions sur le même hôte ont les mêmes options de mise à l’échelle. Par conséquent, il est nécessaire organiser et aborder les fonctions sont hébergées en fonction des exigences de mise à l’échelle.

Règles souvent spécifient comment monter en puissance (augmenter les ressources hôtes) et la montée en puissance (augmenter le nombre d’instances d’hôte) en fonction des paramètres différents. Déclencheurs pour les échelles peuvent inclure la planification, taux de demandes, l’utilisation du processeur et utilisation de la mémoire. Souvent de meilleures performances ont un coût supérieur. L’une des approches moins coûteux, basé sur la consommation ne peuvent pas mettre à l’échelle comme rapidement lorsque le taux de demandes soudainement augmente. Il existe un compromis entre le paiement à l’avance « coût d’assurance » par rapport à payer strictement « en tant que vous allez » et risquer des réponses plus lents en raison d’une augmentation soudaine de la demande.

## <a name="monitoring-tracing-and-logging"></a>Surveillance, le suivi et journalisation

Un aspect souvent négligée en matière de DevOps surveille les applications une fois déployées. Il est important de disposer d’une stratégie pour surveiller les fonctions sans serveur. Le principal défi est souvent corrélation ou reconnaît lorsqu’un utilisateur appelle plusieurs fonctions dans le cadre de l’interaction même. Plateformes plus sans serveur permettent une journalisation de console peut être importé dans des outils tiers. Il existe également des options pour automatiser la collecte de données de télémétrie, créer et suivre les ID de corrélation et surveiller les actions spécifiques pour obtenir des informations détaillées. Azure fournit des avancées [plateforme d’Application Insights](https://docs.microsoft.com/azure/azure-functions/functions-monitoring) pour la surveillance et analytique.

## <a name="inter-service-dependencies"></a>Dépendances entre services

Une architecture sans serveur peut inclure des fonctions qui s’appuient sur d’autres fonctions. En fait, il n’est pas rare que dans une architecture sans serveur pour disposer de plusieurs services s’appellent mutuellement en tant que partie d’une interaction ou d’une transaction distribuée. Pour éviter un couplage important, il est recommandé que les services ne référencent mutuellement directement. Lorsque le point de terminaison pour un service doit être modifié, des références directes pourrait entraîner la refactorisation principale. Une solution suggérée consiste à fournir un mécanisme de découverte de service, par exemple un Registre, qui fournit le point de terminaison approprié pour un type de demande. Une autre solution consiste à tirer parti des services de messagerie telles que les files d’attente ou rubriques pour la communication entre les services.

## <a name="managing-failure-and-providing-resiliency"></a>La gestion des défaillances et fournir la résilience

Il est également important de prendre en compte la *modèle disjoncteur*: Si, pour une raison quelconque, un service continue d’échouer, il n’est pas recommandé d’appeler ce service à plusieurs reprises. Au lieu de cela, un autre service est appelé, ou un message retourné jusqu'à ce que l’intégrité du service dépendant est rétablie. L’architecture sans serveur doit prendre en compte la stratégie de résolution et la gestion des dépendances entre services.

Pour continuer le modèle disjoncteur, services doivent être résilient et tolérant aux pannes. Une tolérance de panne désigne la capacité de votre application pour continuer à s’exécuter même après des exceptions inattendues ou États non valides sont rencontrées. Une tolérance de panne est généralement une fonction du code lui-même et comment il a écrit pour gérer les exceptions. La résilience fait référence à la capacité de l’application est à la récupération après des échecs. La résilience est généralement gérée par la plateforme sans serveur. La plateforme doit être en mesure de faire tourner une nouvelle instance de la fonction sans serveur en cas d’échec de l’existant. La plate-forme doit également être suffisamment intelligente s’arrête de nouvelles instances en cas d’échec de chaque nouvelle instance.

Pour plus d’informations, consultez [implémentation du modèle de disjoncteur](../microservices-architecture/implement-resilient-applications/implement-circuit-breaker-pattern.md).

## <a name="versioning-and-greenblue-deployments"></a>Déploiements de contrôle de version et vert/bleu

Un avantage majeur de sans serveur est la possibilité de mettre à niveau d’une fonction spécifique sans avoir à redéployer l’application entière. Pour les mises à niveau réussisse, les fonctions doivent être avec contrôle de version afin que les services qui les appellent sont acheminés vers la version correcte du code. Une stratégie pour le déploiement de nouvelles versions est également importante. Une approche courante consiste à utiliser « vert/bleu déploiements » Le déploiement vert est la fonction active. Une nouvelle version de « bleue » est déployée en production et testée. Lorsque les tests réussissent, les versions de vertes et bleues sont échangées afin de la nouvelle version est fourni en direct. Si des problèmes sont rencontrés, ils peuvent être échangés en retour. Prise en charge le contrôle de version et les déploiements vert/bleu nécessite une combinaison de création de fonctions pour s’adapter aux changements de version et l’utilisation de la plateforme sans serveur pour gérer les déploiements. Une approche possible consiste à utiliser des proxys qui sont décrites dans le [plateforme serverless Azure](azure-functions.md#proxies) chapitre.

>[!div class="step-by-step"]
>[Précédent](serverless-architecture.md)
>[Suivant](serverless-design-examples.md)