---
title: Visual Studio Tools pour Docker sur Windows
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: 79e9b5cc9bac317a368583013abbc5124ef2c9ac
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53151211"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>À l’aide de Visual Studio Tools pour Docker (Visual Studio sur Windows)

Visual Studio Tools pour le flux de travail de développement Docker est similaire au flux de travail lors de l’utilisation de Visual Studio Code et interface CLI Docker. En fait, il est basé sur la même interface CLI Docker, mais il est plus facile commencer, simplifie le processus et fournit une plus grande productivité pour la build, exécuter et composer des tâches. Exécuter et déboguer vos conteneurs via des actions simples comme **F5** et **Ctrl**+**F5**. Avec la prise en charge d’orchestration de conteneur facultatif, en plus de pouvoir exécuter et déboguer un conteneur unique, vous pouvez exécuter et déboguer un groupe de conteneurs (un ensemble de la solution) en même temps.

> [!NOTE]
> Cet article s’applique à Visual Studio sur Windows et non dans Visual Studio pour Mac.

## <a name="configure-your-local-environment"></a>Configurer votre environnement local

Avec les dernières versions de Docker pour Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), le programme d’installation simple permet de facilement développer des applications Docker.

Prise en charge docker est inclus dans Visual Studio 2017. Téléchargez Visual Studio 2017 ici : [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

## <a name="use-docker-tools-in-visual-studio-2017"></a>Utilisez des outils Docker dans Visual Studio 2017

Il existe deux niveaux de prise en charge de Docker que vous pouvez ajouter à un projet. Dans les projets d’application web .NET Core, vous pouvez simplement ajouter un *Dockerfile* fichier au projet en activant la prise en charge Docker. Le niveau suivant est prise en charge de conteneurs d’orchestration, qui ajoute un *Dockerfile* au projet (s’il n’existe pas déjà) et un *docker-compose.yml* fichier au niveau de la solution. Prise en charge d’orchestration de conteneur, via Docker Compose, est ajouté par défaut dans Visual Studio 2017 version 15.7 ou une version antérieure. Prise en charge d’orchestration de conteneur est une fonctionnalité à activer dans les versions de Visual Studio 2017 15.8 ou une version ultérieure, auquel cas Docker Compose et Service Fabric sont pris en charge.

Le **ajouter** > **prise en charge Docker** et **ajouter** > **orchestration de conteneur prise en charge** sont des commandes situé sur le menu contextuel (ou le menu contextuel) du nœud du projet pour un projet d’application web dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-26 :

![Ajoutez l’option de menu de prise en charge Docker dans Visual Studio](media/add-docker-support-menu.png)

Figure 4-26 : Ajout de prise en charge Docker à un projet Visual Studio 2017

### <a name="add-docker-support"></a>Ajouter la prise en charge Docker

Vous pouvez ajouter la prise en charge Docker à un projet d’application web .NET Core existant en sélectionnant **ajouter** > **prennent en charge de Docker** dans **l’Explorateur de solutions**. Vous pouvez également activer la prise en charge de Docker lors de la création du projet en sélectionnant **activer la prise en charge Docker** dans le **nouvelle Application de Web ASP.NET Core** boîte de dialogue qui s’ouvre après avoir cliqué sur **OK** dans le **nouveau projet** boîte de dialogue, comme illustré dans la Figure 4-27.

![Activer la prise en charge de Docker pour l’application web ASP.NET Core dans Visual Studio](./media/enable-docker-support-visual-studio.png)

Figure 4-27 : Activer la prise en charge Docker lors de la création du projet dans Visual Studio 2017

Lorsque vous ajoutez ou activez la prise en charge Docker, Visual Studio ajoute un *Dockerfile* fichier au projet.

> [!NOTE]
> Lorsque vous activez la prise en charge de Docker Compose lors de la création de projet pour un projet d’application web .NET Framework (pas un projet .NET Core web application) comme indiqué dans la Figure 4-28, prise en charge d’orchestration de conteneurs est également ajouté.
>
> ![Activer Docker compose prise en charge pour un projet d’application web .NET Framework](media/enable-docker-compose-support.png)

> Figure 4-28 : Prise en charge de Docker Compose sur un projet d’application web .NET Framework dans Visual Studio 2017

### <a name="add-container-orchestration-support"></a>Ajouter la prise en charge d’orchestration de conteneurs

Lorsque vous souhaitez composer une solution multiconteneur, ajouter la prise en charge d’orchestration de conteneurs à vos projets. Cela vous permet d’exécuter et déboguer un groupe de conteneurs (un ensemble de la solution) en même temps, si elles sont définies dans le même *docker-compose.yml* fichier.

Pour ajouter la prise en charge d’orchestration de conteneur, cliquez sur le nœud solution ou projet dans **l’Explorateur de solutions**, puis choisissez **ajouter** > **d’Orchestration de conteneur prend en charge de**. Puis choisissez **Docker Compose** ou **Service Fabric** pour gérer les conteneurs.

Après avoir ajouté la prise en charge d’orchestration de conteneurs à votre projet, vous voyez un fichier Dockerfile ajouté au projet et un **docker-compose** dossier ajouté à la solution dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-29 :

![Fichiers docker dans l’Explorateur de solutions dans Visual Studio](media/docker-support-solution-explorer.png)

Figure 4-29 : Fichiers docker dans l’Explorateur de solutions dans Visual Studio 2017

Si *docker-compose.yml* existe déjà, Visual Studio ajoute simplement les lignes de code de configuration requises.

## <a name="configure-docker-tools"></a>Configurer les outils Docker

Dans le menu principal, choisissez **outils** > **Options**et développez **conteneur outils** > **paramètres**. Les paramètres d’outils de conteneur s’affichent.

![](./media/visual-studio-docker-tools-options.png)

Figure 4-30 : Options des outils docker

Le tableau suivant peut vous aider à décider comment définir ces options.

| Name | Paramètre par défaut | S'applique à | Description |
| -----|:---------------:|:----------:| ----------- |
| Extraire automatiquement des images Docker nécessaires lors du chargement du projet | Activé | Docker Compose | Pour augmenter les performances lors du chargement des projets, Visual Studio démarre une opération d’extraction de Docker en arrière-plan afin que lorsque vous êtes prêt à exécuter votre code, l’image est déjà téléchargée ou en cours de téléchargement. Si vous êtes simplement charger les projets et parcourez le code, vous pouvez désactiver cette option pour éviter le téléchargement des images de conteneur que vous n’avez pas besoin. |
| Démarrer automatiquement les conteneurs en arrière-plan | Activé | Docker Compose | À nouveau pour de meilleures performances, Visual Studio crée un conteneur avec les montages de volume prêt pour lorsque vous générez et exécutez votre conteneur. Si vous souhaitez contrôler la création de votre conteneur, désactivez cette option. |
| Ferment automatiquement les conteneurs kill sur la solution | Activé | Docker Compose | Désactiver cette option si vous souhaitez que les conteneurs de votre solution continuer à exécuter après la fermeture de la solution ou de fermeture de Visual Studio. |
| Ne demande pas de certificat SSL localhost approbation | Off | Projets ASP.NET Core 2.1 | Si le certificat SSL localhost n’est pas approuvé, Visual Studio vous invite chaque fois que vous exécutez votre projet, sauf si cette case à cocher est activée. |

> [!WARNING]
> Si le certificat SSL localhost n’est pas approuvé et que vous cochez la case pour supprimer l’invite, les demandes web HTTPS peuvent échouer lors de l’exécution dans votre application ou service. Dans ce cas, désactivez le **ne pas demander** case à cocher, exécuter votre projet et indiquer l’approbation à l’invite.

**Plus d’informations :** pour plus d’informations sur la mise en œuvre des services et l’utilisation de Visual Studio Tools pour Docker, lisez les articles suivants :

Générer, déboguer, mettre à jour et actualiser des applications dans un conteneur Docker local : [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

Déployer un conteneur Docker ASP.NET Core sur un Registre de conteneurs : [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
>[Précédent](docker-apps-inner-loop-workflow.md)
>[Suivant](set-up-windows-containers-with-powershell.md)