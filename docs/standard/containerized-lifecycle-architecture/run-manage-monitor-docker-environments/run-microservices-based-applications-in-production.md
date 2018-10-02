---
title: Exécuter des applications composées et basées sur des microservices dans des environnements de production
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: 18e6cb1fb5f496b66c89cb8e009a67894b8a76ad
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48046394"
---
# <a name="run-composed-and-microservices-based-applications-in-production-environments"></a>Exécuter des applications composées et basées sur des microservices dans des environnements de production

Applications composées par plusieurs microservices n’avez pas besoin d’être déployés dans des clusters orchestrator afin de simplifier la complexité du déploiement et le rendre viable du point de vue informatique. Sans un cluster orchestrateur, il serait très difficile de déployer et de montée en puissance une application de microservices complexes.

## <a name="introduction-to-orchestrators-schedulers-and-container-clusters"></a>Introduction aux orchestrateurs, les planificateurs et les clusters de conteneurs

Plus haut dans ce livre électronique, nous avons introduit *clusters* et *planificateurs* dans le cadre de la discussion sur l’architecture logicielle et le développement. Exemples de clusters Docker sont Docker Swarm et Mesosphere Datacenter Operating System (DC/OS). Ces deux éléments peuvent fonctionner comme une partie de l’infrastructure fournie par Microsoft Azure Container Service.

Lorsque les applications sont montés sur plusieurs systèmes d’hôte, la possibilité de gérer chaque système hôte et clarifient la complexité de la plateforme sous-jacente devient intéressante. C’est précisément ce que fournissent les orchestrateurs et des planificateurs. Examinons une brève les ici :

- **Planificateurs**. « Planification » désigne la capacité d’un administrateur pour charger un fichier de service sur un système hôte qui établit la façon d’exécuter un conteneur spécifique. Lancement de conteneurs dans un cluster Docker a tendance à être appelé de planification. Bien que la planification fait référence à l’acte spécifique du chargement de la définition de service, dans un sens plus général, les planificateurs sont responsables de raccordement au système d’initialisation d’un ordinateur hôte pour gérer les services dans la capacité nécessaire.

   Un planificateur de cluster a plusieurs objectifs : utilisation efficace des ressources du cluster, l’utilisation des contraintes de positionnement fournie par l’utilisateur, des applications rapidement le point de ne pas les laisser dans un état d’attente, ayant un degré de « équité, « en cours robuste aux erreurs, et toujours être disponible.

- **Orchestration**. Plateformes d’étendent les fonctionnalités de gestion de cycle de vie à complexes, des charges de travail déployées sur un cluster d’hôtes. En faisant abstraction de l’infrastructure hôte, outils d’orchestration de permettent aux utilisateurs de traiter l’ensemble du cluster comme une cible de déploiement unique.

   Le processus d’orchestration implique des outils et une plateforme qui peut automatiser tous les aspects de gestion des applications à partir de placement initial ou le déploiement par conteneur ; déplacement des conteneurs vers des hôtes différents en fonction de la santé de son hôte ou les performances ; le contrôle de version et propagée mises à jour et l’intégrité de la surveillance des fonctions qui prennent en charge la mise à l’échelle et basculement ; et bien plus encore.

   Orchestration est un terme général qui fait référence à la planification du conteneur gestion du cluster et éventuellement l’approvisionnement des hôtes supplémentaires.

Les fonctionnalités fournies par les orchestrateurs et des planificateurs sont très complexes à développer et créer à partir de zéro, et par conséquent vous souhaite rendre utilisation d’orchestration solutions offertes par les fournisseurs.


>[!div class="step-by-step"]
[Précédent](index.md)
[Suivant](manage-production-docker-environments.md)
