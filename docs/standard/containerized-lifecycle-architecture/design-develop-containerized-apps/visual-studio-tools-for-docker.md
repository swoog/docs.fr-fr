---
title: À l’aide de Visual Studio Tools pour Docker (Visual Studio sur Windows)
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: af14c92ab27885deec878dc33e7b94035f43e65b
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45743824"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>À l’aide de Visual Studio Tools pour Docker (Visual Studio sur Windows)

Le flux de travail de développement lors de l’utilisation de Visual Studio Tools pour Docker est similaire au flux de travail lors de l’utilisation de Visual Studio Code et interface CLI Docker. En fait, il est basé sur la même interface CLI Docker, mais il est plus facile commencer, simplifie le processus et fournit une plus grande productivité pour la build, exécuter et composer des tâches. Il est également en mesure d’exécuter et déboguer vos conteneurs via des actions simples telles que F5 et Ctrl + F5 dans Visual Studio. Avec la prise en charge d’orchestration de conteneur facultatif, en plus de pouvoir exécuter et déboguer un conteneur unique, vous pouvez exécuter et déboguer un groupe de conteneurs (un ensemble de la solution) en même temps. Définir les conteneurs dans le même *docker-compose.yml* fichier au niveau de la solution.

## <a name="configuring-your-local-environment"></a>Configuration de votre environnement local

Prise en charge docker est inclus dans Visual Studio 2017 avec des charges de travail .NET et .NET Core installés. Installer Docker pour Windows séparément.

Avec les dernières versions de Docker pour Windows, il est plus facile que jamais pour développer des applications Docker, car le programme d’installation est simple, comme expliqué dans les références suivantes.

**Plus d’informations :** pour en savoir plus sur l’installation de Docker pour Windows, accédez à <https://docs.docker.com/docker-for-windows/>.

**Plus d’informations :** pour obtenir des instructions sur l’installation de Visual Studio, accédez à [ https://visualstudio.microsoft.com/downloads/ ](https://visualstudio.microsoft.com/downloads/).

Pour plus d’informations sur l’installation de Visual Studio Tools pour Docker, accédez à <http://aka.ms/vstoolsfordocker> et <https://docs.microsoft.com/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker>.

## <a name="using-docker-tools-in-visual-studio-2017"></a>À l’aide des outils Docker dans Visual Studio 2017

Lors de l’ajout de prise en charge Docker à un projet (voir Figure 4-26), Visual Studio ajoute un *Dockerfile* à la racine du projet.

![L’activation de la prise en charge de la Solution Docker dans un projet Visual Studio 2017](./media/image32.png)

Figure 4-26 : activer la prise en charge de la Solution Docker dans un projet Visual Studio 2017

 Prise en charge d’orchestration de conteneur, via Docker Compose, est ajouté par défaut dans Visual Studio 2017 version 15.7 ou une version antérieure. Prise en charge d’orchestration de conteneur est une fonctionnalité à activer dans les versions de Visual Studio 2017 15.8 ou une version ultérieure, auquel cas Docker Compose et Service Fabric sont pris en charge.

Avec Visual Studio version 15,8 et versions ultérieure, vous pouvez ajouter la prise en charge de plusieurs projets dans une solution qui ont chacune un conteneur associé. Avec le bouton droit sur le nœud de solution ou projet dans **l’Explorateur de solutions**, puis choisissez **ajouter** > **prise en charge d’Orchestration de conteneurs**.  Puis choisissez **Docker Compose** ou **Service Fabric** pour gérer les conteneurs.

Lorsque vous choisissez **Docker Compose**, Visual Studio ajoute une section de service dans votre solution *docker-compose.yml* fichiers (ou crée les fichiers s’ils n’existent pas). Il est un moyen simple de commencer la composition de votre solution multiconteneur ; Vous pouvez ensuite ouvrir le *docker-compose.yml* de fichiers et de les mettre à jour avec des fonctionnalités supplémentaires.

Cette action ajoute les configuration requise de lignes de code pour un *docker-compose.yml* définie au niveau de la solution.

Vous également pourrez activer la prise en charge de Docker lors de la création d’un projet ASP.NET Core dans Visual Studio 2017, comme indiqué dans la Figure 4-27.

![Prise en charge Docker sous tension lors de la création d’un projet](./media/image33.png)

Figure 4-27 : activer prise en charge Docker lors de la création d’un projet

Après avoir ajouté la prise en charge Docker à votre solution dans Visual Studio, apparaît également une nouvelle arborescence de nœuds dans **l’Explorateur de solutions** avec l’ajout *docker-compose.yml* des fichiers, comme illustré dans la Figure 4-28.

![fichiers docker-compose.yml affichent désormais dans l’Explorateur de solutions](./media/image34.PNG)

Figure 4-28 : fichiers docker-compose.yml affichent désormais dans **l’Explorateur de solutions**

Vous pouvez déployer une application à conteneurs multiples à l’aide d’un seul *docker-compose.yml* fichier lorsque vous exécutez `docker-compose up`; Toutefois, Visual Studio ajoute un groupe de fichiers, donc vous pouvez remplacer les valeurs en fonction de l’environnement (développement ou production) et l’exécution (release ou debug) de type. Cette fonctionnalité est expliquée mieux dans les chapitres.

Vous pouvez également utiliser Service Fabric au lieu de Docker Compose pour gérer plusieurs conteneurs. Consultez [didacticiel : déployer une application .NET dans un conteneur Windows sur Azure Service Fabric](https://docs.microsoft.com/azure/service-fabric/service-fabric-host-app-in-a-container).

**Plus d’informations :** pour plus d’informations sur la mise en œuvre des services et l’utilisation de Visual Studio Tools pour Docker, lisez les articles suivants :

Générer, déboguer, mettre à jour et actualiser des applications dans un conteneur Docker local : [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

Déployer un conteneur Docker ASP.NET Core sur un Registre de conteneurs : [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
[Précédent](docker-apps-inner-loop-workflow.md)
[Suivant](set-up-windows-containers-with-powershell.md)
