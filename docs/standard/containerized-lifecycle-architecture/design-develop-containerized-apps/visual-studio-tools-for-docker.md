---
title: Visual Studio Tools pour Docker sur Windows
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/12/2018
ms.custom: vs-dotnet
ms.openlocfilehash: cd140c12ef4a0187cce096e013937d5c98cd4b39
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47170793"
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a>À l’aide de Visual Studio Tools pour Docker (Visual Studio sur Windows)

Visual Studio Tools pour le flux de travail de développeur Docker est similaire à l’aide de Visual Studio Code et interface CLI Docker (il est basé sur la même interface CLI Docker). Visual Studio Tools pour Docker facilite la prise en main, simplifie le processus et fournit une plus grande productivité pour la génération, exécutez et composer des tâches. Exécuter et déboguer vos conteneurs via des actions simples comme **F5** et **Ctrl**+**F5**.

> [!NOTE]
> Cet article s’applique à Visual Studio sur Windows et non dans Visual Studio pour Mac.

## <a name="configure-your-local-environment"></a>Configurer votre environnement local

Avec les dernières versions de Docker pour Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), le programme d’installation simple permet de facilement développer des applications Docker.

Prise en charge docker est inclus dans Visual Studio 2017. Téléchargez Visual Studio 2017 ici : [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)

## <a name="use-docker-tools-in-visual-studio-2017"></a>Utilisez des outils Docker dans Visual Studio 2017

Il existe deux niveaux de prise en charge de Docker que vous pouvez ajouter à un projet. Dans les projets d’application web .NET Core, vous pouvez simplement ajouter un *Dockerfile* fichier au projet en activant la prise en charge Docker. Le niveau suivant est prise en charge de conteneurs orchestrator, ce qui ajoute un *Dockerfile* au projet (s’il n’existe pas déjà) et un *docker-compose.yml* fichier au niveau de la solution.

Le **ajouter** > **prise en charge Docker** et **ajouter** > **prise en charge de conteneurs Orchestrator** sont des commandes situé sur le menu contextuel (ou le menu contextuel) du nœud du projet pour un projet d’application web dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-26 :

![Ajoutez l’option de menu de prise en charge Docker dans Visual Studio](media/add-docker-support-menu.png)

Figure 4-26 : ajout de prise en charge Docker à un projet Visual Studio 2017

### <a name="add-docker-support"></a>Ajouter la prise en charge Docker

Vous pouvez ajouter la prise en charge Docker à un projet d’application web .NET Core existant en sélectionnant **ajouter** > **prennent en charge de Docker** dans **l’Explorateur de solutions**. Vous pouvez également activer la prise en charge de Docker lors de la création du projet en sélectionnant **activer la prise en charge Docker** dans le **nouvelle Application de Web ASP.NET Core** boîte de dialogue qui s’ouvre après avoir cliqué sur **OK** dans le **nouveau projet** boîte de dialogue, comme illustré dans la Figure 4-27.

![Activer la prise en charge de Docker pour l’application web ASP.NET Core dans Visual Studio](./media/enable-docker-support-visual-studio.png)

Figure 4-27 : activer la prise en charge Docker lors de la création du projet dans Visual Studio 2017

Lorsque vous ajoutez ou activez la prise en charge Docker, Visual Studio ajoute un *Dockerfile* fichier au projet.

> [!NOTE]
> Lorsque vous activez la prise en charge de Docker Compose lors de la création de projet pour un projet d’application web .NET Framework (pas un projet .NET Core web application) comme indiqué dans la Figure 4-28, conteneur orchestrator prise en charge est également ajoutée.
>
> ![Activer Docker compose prise en charge pour un projet d’application web .NET Framework](media/enable-docker-compose-support.png)

> Figure 4-28 : l’activation de prise en charge de Docker Compose sur un projet d’application web .NET Framework dans Visual Studio 2017

### <a name="add-container-orchestrator-support"></a>Ajouter la prise en charge de conteneurs orchestrator

Lorsque vous souhaitez composer une solution multiconteneur, ajouter la prise en charge de conteneurs orchestrator à vos projets. Lorsque vous ajoutez la prise en charge de conteneurs orchestrator, Visual Studio ajoute un *Dockerfile* au projet (s’il n’existe pas déjà) et global *docker-compose.yml* fichier au niveau de la solution. Cela vous permet d’exécuter et déboguer un groupe de conteneurs (un ensemble de la solution) en même temps, si elles sont définies dans le même *docker-compose.yml* fichier. Si *docker-compose.yml* existe déjà, Visual Studio ajoute simplement les lignes de code de configuration requises.

Après avoir ajouté la prise en charge d’orchestration de conteneurs à votre projet, vous voyez un fichier Dockerfile ajouté au projet et un **docker-compose** dossier ajouté à la solution dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-29 :

![Fichiers docker dans l’Explorateur de solutions dans Visual Studio](media/docker-support-solution-explorer.png)

Figure 4-29 : les fichiers de Docker dans l’Explorateur de solutions dans Visual Studio 2017

**Plus d’informations :** pour plus d’informations sur la mise en œuvre des services et l’utilisation de Visual Studio Tools pour Docker, lisez les articles suivants :

Générer, déboguer, mettre à jour et actualiser des applications dans un conteneur Docker local : [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)

Déployer un conteneur Docker ASP.NET Core sur un Registre de conteneurs : [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)

>[!div class="step-by-step"]
[Précédent](docker-apps-inner-loop-workflow.md)
[Suivant](set-up-windows-containers-with-powershell.md)