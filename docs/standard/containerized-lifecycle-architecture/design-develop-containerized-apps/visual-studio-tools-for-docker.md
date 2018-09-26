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
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="2a9dc-103">À l’aide de Visual Studio Tools pour Docker (Visual Studio sur Windows)</span><span class="sxs-lookup"><span data-stu-id="2a9dc-103">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="2a9dc-104">Visual Studio Tools pour le flux de travail de développeur Docker est similaire à l’aide de Visual Studio Code et interface CLI Docker (il est basé sur la même interface CLI Docker).</span><span class="sxs-lookup"><span data-stu-id="2a9dc-104">The Visual Studio Tools for Docker developer workflow is similar to using Visual Studio Code and Docker CLI (it is based on the same Docker CLI).</span></span> <span data-ttu-id="2a9dc-105">Visual Studio Tools pour Docker facilite la prise en main, simplifie le processus et fournit une plus grande productivité pour la génération, exécutez et composer des tâches.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-105">Visual Studio Tools for Docker makes it even easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="2a9dc-106">Exécuter et déboguer vos conteneurs via des actions simples comme **F5** et **Ctrl**+**F5**.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-106">Execute and debug your containers via simple actions like **F5** and **Ctrl**+**F5**.</span></span>

> [!NOTE]
> <span data-ttu-id="2a9dc-107">Cet article s’applique à Visual Studio sur Windows et non dans Visual Studio pour Mac.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-107">This article applies to Visual Studio on Windows, and not Visual Studio for Mac.</span></span>

## <a name="configure-your-local-environment"></a><span data-ttu-id="2a9dc-108">Configurer votre environnement local</span><span class="sxs-lookup"><span data-stu-id="2a9dc-108">Configure your local environment</span></span>

<span data-ttu-id="2a9dc-109">Avec les dernières versions de Docker pour Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), le programme d’installation simple permet de facilement développer des applications Docker.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-109">With the latest versions of Docker for Windows ([https://docs.docker.com/docker-for-windows/](https://docs.docker.com/docker-for-windows/)), the straightforward setup makes it easy to develop Docker applications.</span></span>

<span data-ttu-id="2a9dc-110">Prise en charge docker est inclus dans Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-110">Docker support is included in Visual Studio 2017.</span></span> <span data-ttu-id="2a9dc-111">Téléchargez Visual Studio 2017 ici : [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span><span class="sxs-lookup"><span data-stu-id="2a9dc-111">Download Visual Studio 2017 here: [https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs)</span></span>

## <a name="use-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="2a9dc-112">Utilisez des outils Docker dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="2a9dc-112">Use Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="2a9dc-113">Il existe deux niveaux de prise en charge de Docker que vous pouvez ajouter à un projet.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-113">There are two levels of Docker support you can add to a project.</span></span> <span data-ttu-id="2a9dc-114">Dans les projets d’application web .NET Core, vous pouvez simplement ajouter un *Dockerfile* fichier au projet en activant la prise en charge Docker.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-114">In .NET Core web app projects, you can just add a *Dockerfile* file to the project by enabling Docker support.</span></span> <span data-ttu-id="2a9dc-115">Le niveau suivant est prise en charge de conteneurs orchestrator, ce qui ajoute un *Dockerfile* au projet (s’il n’existe pas déjà) et un *docker-compose.yml* fichier au niveau de la solution.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-115">The next level is container orchestrator support, which adds a *Dockerfile* to the project (if it doesn't already exist) and a *docker-compose.yml* file at the solution level.</span></span>

<span data-ttu-id="2a9dc-116">Le **ajouter** > **prise en charge Docker** et **ajouter** > **prise en charge de conteneurs Orchestrator** sont des commandes situé sur le menu contextuel (ou le menu contextuel) du nœud du projet pour un projet d’application web dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-26 :</span><span class="sxs-lookup"><span data-stu-id="2a9dc-116">The **Add** > **Docker Support** and **Add** > **Container Orchestrator Support** commands are located on the right-click menu (or context menu) of the project node for a web app project in **Solution Explorer**, as shown in Figure 4-26:</span></span>

![Ajoutez l’option de menu de prise en charge Docker dans Visual Studio](media/add-docker-support-menu.png)

<span data-ttu-id="2a9dc-118">Figure 4-26 : ajout de prise en charge Docker à un projet Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="2a9dc-118">Figure 4-26: Adding Docker support to a Visual Studio 2017 project</span></span>

### <a name="add-docker-support"></a><span data-ttu-id="2a9dc-119">Ajouter la prise en charge Docker</span><span class="sxs-lookup"><span data-stu-id="2a9dc-119">Add Docker support</span></span>

<span data-ttu-id="2a9dc-120">Vous pouvez ajouter la prise en charge Docker à un projet d’application web .NET Core existant en sélectionnant **ajouter** > **prennent en charge de Docker** dans **l’Explorateur de solutions**.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-120">You can add Docker support to an existing .NET Core web app project by selecting **Add** > **Docker Support** in **Solution Explorer**.</span></span> <span data-ttu-id="2a9dc-121">Vous pouvez également activer la prise en charge de Docker lors de la création du projet en sélectionnant **activer la prise en charge Docker** dans le **nouvelle Application de Web ASP.NET Core** boîte de dialogue qui s’ouvre après avoir cliqué sur **OK** dans le **nouveau projet** boîte de dialogue, comme illustré dans la Figure 4-27.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-121">You can also enable Docker support during project creation by selecting **Enable Docker Support** in the **New ASP.NET Core Web Application** dialog box that opens after you click **OK** in the **New Project** dialog box, as shown in Figure 4-27.</span></span>

![Activer la prise en charge de Docker pour l’application web ASP.NET Core dans Visual Studio](./media/enable-docker-support-visual-studio.png)

<span data-ttu-id="2a9dc-123">Figure 4-27 : activer la prise en charge Docker lors de la création du projet dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="2a9dc-123">Figure 4-27: Enable Docker support during project creation in Visual Studio 2017</span></span>

<span data-ttu-id="2a9dc-124">Lorsque vous ajoutez ou activez la prise en charge Docker, Visual Studio ajoute un *Dockerfile* fichier au projet.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-124">When you add or enable Docker support, Visual Studio adds a *Dockerfile* file to the project.</span></span>

> [!NOTE]
> <span data-ttu-id="2a9dc-125">Lorsque vous activez la prise en charge de Docker Compose lors de la création de projet pour un projet d’application web .NET Framework (pas un projet .NET Core web application) comme indiqué dans la Figure 4-28, conteneur orchestrator prise en charge est également ajoutée.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-125">When you enable Docker Compose support during project creation for a .NET Framework web app project (not a .NET Core web app project) as shown in Figure 4-28, container orchestrator support is also added.</span></span>
>
> ![Activer Docker compose prise en charge pour un projet d’application web .NET Framework](media/enable-docker-compose-support.png)

> <span data-ttu-id="2a9dc-127">Figure 4-28 : l’activation de prise en charge de Docker Compose sur un projet d’application web .NET Framework dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="2a9dc-127">Figure 4-28: Enabling Docker Compose support on a .NET Framework web app project in Visual Studio 2017</span></span>

### <a name="add-container-orchestrator-support"></a><span data-ttu-id="2a9dc-128">Ajouter la prise en charge de conteneurs orchestrator</span><span class="sxs-lookup"><span data-stu-id="2a9dc-128">Add container orchestrator support</span></span>

<span data-ttu-id="2a9dc-129">Lorsque vous souhaitez composer une solution multiconteneur, ajouter la prise en charge de conteneurs orchestrator à vos projets.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-129">When you want to compose a multicontainer solution, add container orchestrator support to your projects.</span></span> <span data-ttu-id="2a9dc-130">Lorsque vous ajoutez la prise en charge de conteneurs orchestrator, Visual Studio ajoute un *Dockerfile* au projet (s’il n’existe pas déjà) et global *docker-compose.yml* fichier au niveau de la solution.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-130">When you add container orchestrator support, Visual Studio adds a *Dockerfile* to the project (if it doesn't already exist) and a global *docker-compose.yml* file at the solution level.</span></span> <span data-ttu-id="2a9dc-131">Cela vous permet d’exécuter et déboguer un groupe de conteneurs (un ensemble de la solution) en même temps, si elles sont définies dans le même *docker-compose.yml* fichier.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-131">This lets you run and debug a group of containers (a whole solution) at the same time if they're defined in the same *docker-compose.yml* file.</span></span> <span data-ttu-id="2a9dc-132">Si *docker-compose.yml* existe déjà, Visual Studio ajoute simplement les lignes de code de configuration requises.</span><span class="sxs-lookup"><span data-stu-id="2a9dc-132">If *docker-compose.yml* already exists, Visual Studio just adds the required lines of configuration code to it.</span></span>

<span data-ttu-id="2a9dc-133">Après avoir ajouté la prise en charge d’orchestration de conteneurs à votre projet, vous voyez un fichier Dockerfile ajouté au projet et un **docker-compose** dossier ajouté à la solution dans **l’Explorateur de solutions**, comme illustré dans la Figure 4-29 :</span><span class="sxs-lookup"><span data-stu-id="2a9dc-133">After you add container orchestration support to your project, you see a Dockerfile added to the project and a **docker-compose** folder added to the solution in **Solution Explorer**, as shown in Figure 4-29:</span></span>

![Fichiers docker dans l’Explorateur de solutions dans Visual Studio](media/docker-support-solution-explorer.png)

<span data-ttu-id="2a9dc-135">Figure 4-29 : les fichiers de Docker dans l’Explorateur de solutions dans Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="2a9dc-135">Figure 4-29: Docker files in Solution Explorer in Visual Studio 2017</span></span>

<span data-ttu-id="2a9dc-136">**Plus d’informations :** pour plus d’informations sur la mise en œuvre des services et l’utilisation de Visual Studio Tools pour Docker, lisez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="2a9dc-136">**More information:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="2a9dc-137">Générer, déboguer, mettre à jour et actualiser des applications dans un conteneur Docker local : [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="2a9dc-137">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="2a9dc-138">Déployer un conteneur Docker ASP.NET Core sur un Registre de conteneurs : [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="2a9dc-138">Deploy an ASP.NET Core Docker container to a container registry: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="2a9dc-139">[Précédent](docker-apps-inner-loop-workflow.md)
[Suivant](set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="2a9dc-139">[Previous](docker-apps-inner-loop-workflow.md)
[Next](set-up-windows-containers-with-powershell.md)</span></span>