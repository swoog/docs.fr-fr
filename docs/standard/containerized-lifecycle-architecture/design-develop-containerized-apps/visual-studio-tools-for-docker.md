---
title: Visual Studio Tools pour Docker sur Windows
description: Familiarisez-vous avec les outils Docker disponibles dans Visual Studio 2017 version 15.7 et ultérieure.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.custom: vs-dotnet
ms.openlocfilehash: 431a0f34ba913c18c35e28ca45660495403bf688
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61795566"
---
# <a name="use-docker-tools-in-visual-studio-2017-on-windows"></a>Utilisez des outils Docker dans Visual Studio 2017 sur Windows

Le flux de travail de développeur lorsque vous utilisez les outils Docker inclus dans Visual Studio 2017 version 15.7 et ultérieure, est similaire à l’aide de Visual Studio Code et interface CLI Docker (en fait, il est basé sur la même interface CLI Docker), mais il est plus facile de commencer, simplifie le processus, et Fournit une plus grande productivité pour la build, exécuter et composer des tâches. Elle peut également exécuter et déboguer vos conteneurs via habituelles `F5` et `Ctrl+F5` clés à partir de Visual Studio. Vous pouvez même déboguer une solution dans son intégralité si ses conteneurs sont définis dans le même `docker-compose.yml` fichier au niveau de la solution.

## <a name="configure-your-local-environment"></a>Configurer votre environnement local

Avec les dernières versions de Docker pour Windows, il est plus facile que jamais pour développer des applications Docker, car le programme d’installation est simple, comme expliqué dans les références suivantes.

> [!TIP]
> Pour en savoir plus sur l’installation de Docker pour Windows, accédez à (<https://docs.docker.com/docker-for-windows/>).

## <a name="docker-support-in-visual-studio-2017"></a>Prise en charge de docker dans Visual Studio 2017

Il existe deux niveaux de prise en charge de Docker que vous pouvez ajouter à un projet. Dans les projets ASP.NET Core, vous pouvez simplement ajouter un `Dockerfile` fichier au projet en activant la prise en charge Docker. Le niveau suivant est prise en charge de conteneurs d’orchestration, qui ajoute un `Dockerfile` au projet (s’il n’existe pas déjà) et un `docker-compose.yml` fichier au niveau de la solution. Prise en charge d’orchestration de conteneur, via Docker Compose, est ajouté par défaut dans Visual Studio 2017 version 15.0 pour 15.7. Prise en charge d’orchestration de conteneur est une fonctionnalité à activer dans les versions de Visual Studio 2017 15,8 ou version ultérieures. Version 15.8 une version ultérieure prennent en charge Docker Compose et Service Fabric.

Le **Ajouter > prise en charge Docker** et **Ajouter > prise en charge de conteneurs Orchestrator** commandes se trouvent sur le menu contextuel (ou le menu contextuel) du nœud du projet pour un projet ASP.NET Core dans  **L’Explorateur de solutions**, comme illustré dans la Figure 4-31 :

![Option de menu Ajouter la prise en charge de Docker dans Visual Studio](./media/add-docker-support-menu.png)

**Figure 4-31**. Ajout de prise en charge Docker à un projet Visual Studio 2017

### <a name="add-docker-support"></a>Ajouter la prise en charge Docker

Vous pouvez ajouter la prise en charge Docker à un projet ASP.NET Core existant en sélectionnant **ajouter** > **prennent en charge de Docker** dans **l’Explorateur de solutions**. Vous pouvez également activer la prise en charge de Docker lors de la création du projet en sélectionnant **activer la prise en charge Docker** dans le **nouvelle Application de Web ASP.NET Core** boîte de dialogue qui s’ouvre après avoir cliqué sur **OK** dans le **nouveau projet** boîte de dialogue, comme illustré dans la Figure 4-32.

![Activer la prise en charge de Docker pour une nouvelle application web ASP.NET Core dans Visual Studio](./media/enable-docker-support-visual-studio.png)

**Figure 4-32**. Activer la prise en charge Docker lors de la création du projet dans Visual Studio 2017

Lorsque vous ajoutez ou activez la prise en charge Docker, Visual Studio ajoute un *Dockerfile* fichier au projet.

> [!NOTE]
> Lorsque vous activez la prise en charge de Docker Compose lors de la création de projet pour un projet ASP.NET (.NET Framework, pas un projet .NET Core) comme indiqué dans la Figure 4-33, prise en charge d’orchestration de conteneurs est également ajouté.

![Activer la prise en charge de Docker Compose pour un projet ASP.NET](media/enable-docker-compose-support.png)

**Figure 4-33**. Prise en charge de Docker Compose pour un projet ASP.NET dans Visual Studio 2017

### <a name="add-container-orchestration-support"></a>Ajouter la prise en charge d’orchestration de conteneurs

Lorsque vous souhaitez composer une solution de plusieurs conteneurs, ajouter la prise en charge d’orchestration de conteneurs à vos projets. Cela vous permet d’exécuter et déboguer un groupe de conteneurs (un ensemble de la solution) en même temps, si elles sont définies dans le même *docker-compose.yml* fichier.

Pour ajouter la prise en charge d’orchestration de conteneur, cliquez sur le nœud solution ou projet dans **l’Explorateur de solutions**, puis choisissez **Ajouter > Orchestration de conteneur prend en charge**. Puis choisissez **Docker Compose** ou **Service Fabric** pour gérer les conteneurs.

Après avoir ajouté la prise en charge d’orchestration de conteneurs à votre projet, vous voyez un fichier Dockerfile ajouté au projet et un **docker-compose** dossier ajouté à la solution dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-34 :

![Fichiers Docker dans l’Explorateur de solutions de Visual Studio](media/docker-support-solution-explorer.png)

**Figure 4-34**. Fichiers docker dans l’Explorateur de solutions dans Visual Studio 2017

Si le fichier *docker-compose.yml* existe déjà, Visual Studio ajoute simplement les lignes de code de configuration requises.

## <a name="configure-docker-tools"></a>Configurer les outils Docker

Dans le menu principal, choisissez **Outils > Options**et développez **conteneur Outils > paramètres**. Les paramètres d’outils de conteneur s’affichent.

![Docker pour Visual Studio outils options, montrant : Extraire automatiquement des images Docker nécessaires lors du chargement du projet, démarrer automatiquement les conteneurs en arrière-plan, arrêter automatiquement les conteneurs sur la solution de fermeture et ne pas demander de l’approbation certificat SSL.](./media/visual-studio-docker-tools-options.png)

**Figure 4-35**. Options des outils docker

Le tableau suivant peut vous aider à décider comment définir ces options.

| Nom | Paramètre par défaut | S'applique à | Description |
| -----|:---------------:|:----------:| ----------- |
| Extraire automatiquement des images Docker nécessaires lors du chargement du projet | Activé | Docker Compose | Pour améliorer les performances lors du chargement des projets, Visual Studio démarre une opération d’extraction de Docker en arrière-plan afin que lorsque vous êtes prêt à exécuter votre code, l’image est déjà téléchargée ou en cours de téléchargement. Si vous êtes simplement charger les projets et parcourez le code, vous pouvez désactiver cette option pour éviter le téléchargement des images de conteneur que vous n’avez pas besoin. |
| Démarrer automatiquement les conteneurs en arrière-plan | Activé | Docker Compose | À nouveau pour de meilleures performances, Visual Studio crée un conteneur avec les montages de volume prêt pour lorsque vous générez et exécutez votre conteneur. Si vous souhaitez contrôler la création de votre conteneur, désactivez cette option. |
| Ferment automatiquement les conteneurs kill sur la solution | Activé | Docker Compose | Désactiver cette option si vous souhaitez que les conteneurs de votre solution continuer à exécuter après la fermeture de la solution ou de fermeture de Visual Studio. |
| Ne demande pas de certificat SSL localhost approbation | Off | Projets ASP.NET Core 2.1 | Si le certificat SSL localhost n’est pas approuvé, Visual Studio vous invite chaque fois que vous exécutez votre projet, sauf si cette case à cocher est activée. |

> [!WARNING]
> Si le certificat SSL localhost n’est pas approuvé et que vous cochez la case pour supprimer l’invite, les demandes web HTTPS peuvent échouer lors de l’exécution dans votre application ou service. Dans ce cas, désactivez le **ne pas demander** case à cocher, exécuter votre projet et indiquer l’approbation à l’invite.

> [!TIP]
> Pour plus d’informations sur la mise en œuvre des services et l’utilisation de Visual Studio Tools pour Docker, lisez les articles suivants :
>
>Débogage d’applications dans un conteneur Docker local : <https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh>
>
>Déployer un conteneur ASP.NET sur un Registre de conteneur à l’aide de Visual Studio : <https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker>

>[!div class="step-by-step"]
>[Précédent](docker-apps-inner-loop-workflow.md)
>[Suivant](set-up-windows-containers-with-powershell.md)
