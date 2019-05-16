---
title: Exécuter des applications composées et basées sur des microservices dans des environnements de production
description: Familiarisez-vous avec les composants clés pour exécuter des applications basées sur le conteneur en production
ms.date: 02/15/2019
ms.openlocfilehash: 69df3d39a00b91cbe59c96e5fcab841a60943bcc
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644963"
---
# <a name="run-composed-and-microservices-based-applications-in-production-environments"></a>Exécuter des applications composées et basées sur des microservices dans des environnements de production

Applications composées par plusieurs microservices n’avez pas besoin d’être déployés dans des clusters orchestrator afin de simplifier la complexité du déploiement et le rendre viable du point de vue informatique. Sans un cluster orchestrateur, il serait difficile de déployer et de monter en charge une application de microservices complexes.

## <a name="introduction-to-orchestrators-schedulers-and-container-clusters"></a>Introduction aux orchestrateurs, les planificateurs et les clusters de conteneurs

Plus haut dans ce livre électronique, *clusters* et *planificateurs* ont été introduites dans le cadre de la discussion sur l’architecture logicielle et le développement. Kubernetes et Service Fabric sont des exemples de clusters Docker. Les deux de ces orchestrateurs peuvent fonctionner comme une partie de l’infrastructure fournie par Microsoft Azure Kubernetes Service.

Lorsque les applications sont montés sur plusieurs systèmes d’hôte, la possibilité de gérer chaque système hôte et clarifient la complexité de la plateforme sous-jacente devient intéressante. C’est précisément ce que fournissent les orchestrateurs et des planificateurs. Examinons une brève les ici :

- **Planificateurs**. « Planification » désigne la capacité d’un administrateur pour charger un fichier de service sur un système hôte qui établit la façon d’exécuter un conteneur spécifique. Lancement de conteneurs dans un cluster Docker a tendance à être appelé de planification. Bien que la planification fait référence à l’acte spécifique du chargement de la définition de service, dans un sens plus général, les planificateurs sont responsables de raccordement au système d’initialisation d’un ordinateur hôte pour gérer les services dans la capacité nécessaire.

   Un planificateur de cluster a plusieurs objectifs : utilisation efficace des ressources du cluster, l’utilisation des contraintes de positionnement fournie par l’utilisateur, des applications rapidement le point de ne pas les laisser dans un état d’attente, ayant un degré de « équité, « en cours robuste aux erreurs, et toujours être disponible.

- **Orchestrateurs**. Plateformes étendent les fonctionnalités de gestion de cycle de vie des charges de travail complexes, plusieurs conteneurs déployés sur un cluster d’hôtes. En faisant abstraction de l’infrastructure hôte, outils d’orchestration de permettent aux utilisateurs de traiter l’ensemble du cluster comme une cible de déploiement unique.

   Le processus d’orchestration implique des outils et une plateforme qui peut automatiser tous les aspects de gestion des applications à partir de placement initial ou le déploiement par conteneur ; déplacement des conteneurs vers des hôtes différents en fonction de la santé de son hôte ou les performances ; le contrôle de version et propagée mises à jour et l’intégrité de la surveillance des fonctions qui prennent en charge la mise à l’échelle et basculement ; et bien plus encore.

   Orchestration est un terme général qui fait référence à la planification du conteneur gestion du cluster et éventuellement l’approvisionnement des hôtes supplémentaires.

Les fonctionnalités fournies par les orchestrateurs et des planificateurs sont complexes à développer et créer à partir de zéro, par conséquent vous souhaite utiliser des solutions d’orchestration de fournisseurs.

>[!div class="step-by-step"]
>[Précédent](index.md)
>[Suivant](manage-production-docker-environments.md)
