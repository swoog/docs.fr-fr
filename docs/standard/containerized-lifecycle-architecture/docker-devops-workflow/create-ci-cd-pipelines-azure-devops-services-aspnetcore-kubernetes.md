---
title: Étapes du workflow DevOps de la boucle externe pour une application Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
ms.date: 02/15/2019
ms.openlocfilehash: 9fdc5acfd375e4f2266859f061ef1c854286b914
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65644986"
---
# <a name="creating-cicd-pipelines-in-azure-devops-services-for-a-net-core-20-application-on-containers-and-deploying-to-a-kubernetes-cluster"></a>Création de pipelines CI/CD dans Azure DevOps Services pour une application .NET Core 2.0 sur des conteneurs et déploiement sur un cluster Kubernetes

Dans la Figure 5-12, vous pouvez voir le scénario de DevOps de bout en bout qui couvrent la gestion du code, la compilation de code, générer des images Docker, les images Docker push vers un Registre Docker et enfin le déploiement sur un cluster Kubernetes dans Azure.

![Flux de travail : Démarrage de l’ordinateur de développement. Envoi vers un référentiel commence la tâche de génération/CI à l’aide d’une image personnalisée qui est poussée vers un Registre Docker et puis est utilisée par la tâche de déploiement/CD, enfin, en exécutant un push sur AKS.](media/docker-workflow-ci-cd-aks.png)

**Figure 5-12**. Scénario CI/CD Création d’images Docker et le déploiement sur un cluster Kubernetes dans Azure

Il est important de souligner que les deux pipelines, la build/CI et la mise en production et de livraison, sont connectés via le Registre Docker (par exemple, Docker Hub ou Azure Container Registry). Le Registre Docker est une des principales différences par rapport à un processus CI/CD traditionnel sans Docker.

Comme indiqué dans la Figure 5-13, la première phase est le pipeline de build/CI. Dans les Services Azure DevOps, vous pouvez créer des pipelines de build/CI qui compiler le code, créez les images Docker et les envoient vers un Registre Docker comme Docker Hub ou Azure Container Registry.

![Affichage du navigateur de Azure DevOps, définition de tâche de processus de génération.](media/build-ci-pipeline-azure-devops-push-to-docker-registry.png)

**Figure 5-13**. Pipeline de build/CI dans Azure DevOps création d’images Docker et lui envoyer des images vers un Registre Docker

La deuxième phase consiste à créer un pipeline de déploiement/mise en production. Dans les Services Azure DevOps, vous pouvez facilement créer un pipeline de déploiement ciblant un cluster Kubernetes à l’aide de tâches Kubernetes pour Azure DevOps Services, comme indiqué dans la Figure 5-14.

![Affichage du navigateur de Azure DevOps, déployez à la définition de tâche de Kubernetes.](media/release-cd-pipeline-azure-devops-deploy-to-kubernetes.png)

**Figure 5-14**. Pipeline de mise en production et de livraison dans le déploiement d’Azure DevOps Services sur un cluster Kubernetes

> [! Procédure pas à pas] déploiement eShopModernized sur Kubernetes :
>
> Pour une description détaillée des pipelines d’Azure DevOps CI/CD déploiement sur Kubernetes, consultez ce billet : \
><https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-CI-CD)>

>[!div class="step-by-step"]
>[Précédent](docker-application-outer-loop-devops-workflow.md)
>[Suivant](../run-manage-monitor-docker-environments/index.md)
