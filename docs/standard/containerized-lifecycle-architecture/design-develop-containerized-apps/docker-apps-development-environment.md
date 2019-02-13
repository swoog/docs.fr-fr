---
title: Environnement de développement pour les applications Docker
description: Découvrez les options d’outil de développement plus importantes qui prennent en charge le cycle de développement de Docker.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: 1d22b45a8eee9198d337df9f0b8b4b78371fa31a
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219995"
---
# <a name="development-environment-for-docker-apps"></a><span data-ttu-id="7b4ed-103">Environnement de développement pour les applications Docker</span><span class="sxs-lookup"><span data-stu-id="7b4ed-103">Development environment for Docker apps</span></span>

## <a name="development-tools-choices-ide-or-editor"></a><span data-ttu-id="7b4ed-104">Choix des outils de développement : IDE ou éditeur</span><span class="sxs-lookup"><span data-stu-id="7b4ed-104">Development tools choices: IDE or editor</span></span>

<span data-ttu-id="7b4ed-105">Non que si vous préférez un IDE complet et puissant ou un éditeur léger et agile, Microsoft a prévu lorsqu’il s’agit de développer des applications Docker.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-105">No matter if you prefer a full and powerful IDE or a lightweight and agile editor, Microsoft has you covered when it comes to developing Docker applications.</span></span>

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a><span data-ttu-id="7b4ed-106">Visual Studio Code et Docker CLI (les outils multiplateformes pour Mac, Linux et Windows)</span><span class="sxs-lookup"><span data-stu-id="7b4ed-106">Visual Studio Code and Docker CLI (cross-platform tools for Mac, Linux, and Windows)</span></span>

<span data-ttu-id="7b4ed-107">Si vous préférez un éditeur léger et multiplateforme prenant en charge de n’importe quel langage de développement, vous pouvez utiliser Visual Studio Code et interface CLI Docker.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-107">If you prefer a lightweight, cross-platform editor supporting any development language, you can use Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="7b4ed-108">Ces produits fournissent une expérience simple et robuste, ce qui est essentielle pour rationaliser le flux de travail de développeur.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-108">These products provide a simple yet robust experience, which is critical for streamlining the developer workflow.</span></span> <span data-ttu-id="7b4ed-109">En installant « Docker pour Mac » ou « Docker pour Windows » (environnement de développement), les développeurs Docker peuvent utiliser une seule interface CLI Docker pour créer des applications pour Windows ou Linux (environnement d’exécution).</span><span class="sxs-lookup"><span data-stu-id="7b4ed-109">By installing "Docker for Mac" or "Docker for Windows" (development environment), Docker developers can use a single Docker CLI to build apps for both Windows or Linux (runtime environment).</span></span> <span data-ttu-id="7b4ed-110">En outre, Visual Studio Code prend en charge les extensions pour Docker avec IntelliSense pour les fichiers Dockerfile et les tâches de raccourci exécuter des commandes Docker à partir de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-110">Plus, Visual Studio Code supports extensions for Docker with IntelliSense for Dockerfiles and shortcut-tasks to run Docker commands from the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="7b4ed-111">Pour télécharger Visual Studio Code, accédez à <https://code.visualstudio.com/download>.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-111">To download Visual Studio Code, go to <https://code.visualstudio.com/download>.</span></span>

<span data-ttu-id="7b4ed-112">Pour télécharger Docker pour Mac et Windows, accédez à <https://www.docker.com/products/docker>.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-112">To download Docker for Mac and Windows, go to <https://www.docker.com/products/docker>.</span></span>

### <a name="visual-studio-with-docker-tools"></a><span data-ttu-id="7b4ed-113">Visual Studio avec des outils Docker</span><span class="sxs-lookup"><span data-stu-id="7b4ed-113">Visual Studio with Docker Tools</span></span>

<span data-ttu-id="7b4ed-114">Lorsque vous utilisez Visual Studio 2015, vous pouvez installer les outils de module complémentaire « Outils Docker pour Visual Studio ».</span><span class="sxs-lookup"><span data-stu-id="7b4ed-114">When you're using Visual Studio 2015 you can install the add-on tools "Docker Tools for Visual Studio."</span></span> <span data-ttu-id="7b4ed-115">Pour Visual Studio 2017, outils Docker sont fournis intégrées déjà.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-115">For Visual Studio 2017, Docker Tools come built in already.</span></span> <span data-ttu-id="7b4ed-116">Dans les deux cas, que vous pouvez développer, exécuter et valider vos applications directement dans l’environnement Docker choisi.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-116">In both cases you can develop, run, and validate your applications directly in the chosen Docker environment.</span></span> <span data-ttu-id="7b4ed-117">F5 votre application (conteneur unique ou plusieurs conteneurs) directement dans un Docker héberger avec débogage, ou appuyez sur Ctrl + F5 pour modifier et actualiser votre application sans avoir à recréer le conteneur.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-117">F5 your application (single container or multiple containers) directly into a Docker host with debugging, or press Ctrl+F5 to edit and refresh your app without having to rebuild the container.</span></span> <span data-ttu-id="7b4ed-118">Ce choix est le plus simple et plus puissant pour les développeurs Windows en créant des conteneurs Docker pour Linux ou Windows.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-118">This is the simplest and more powerful choice for Windows developers creating Docker containers for Linux or Windows.</span></span>

> [!NOTE]
> <span data-ttu-id="7b4ed-119">Pour télécharger les outils Docker pour Visual Studio, accédez à <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-119">To download Docker Tools for Visual Studio, go to <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span></span>

## <a name="language-and-framework-choices"></a><span data-ttu-id="7b4ed-120">Choix de langage et de framework</span><span class="sxs-lookup"><span data-stu-id="7b4ed-120">Language and framework choices</span></span>

<span data-ttu-id="7b4ed-121">Vous pouvez développer des applications de Docker et les outils de Microsoft avec les langages les plus récents.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-121">You can develop Docker applications and Microsoft tools with most modern languages.</span></span> <span data-ttu-id="7b4ed-122">Voici une liste initiale, mais vous n’êtes pas limité à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="7b4ed-122">The following is an initial list, but you are not limited to it:</span></span>

-   <span data-ttu-id="7b4ed-123">.NET Core et ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="7b4ed-123">.NET Core and ASP.NET Core</span></span>
-   <span data-ttu-id="7b4ed-124">Node.js</span><span class="sxs-lookup"><span data-stu-id="7b4ed-124">Node.js</span></span>
-   <span data-ttu-id="7b4ed-125">Golang</span><span class="sxs-lookup"><span data-stu-id="7b4ed-125">Golang</span></span>
-   <span data-ttu-id="7b4ed-126">Java</span><span class="sxs-lookup"><span data-stu-id="7b4ed-126">Java</span></span>
-   <span data-ttu-id="7b4ed-127">Ruby</span><span class="sxs-lookup"><span data-stu-id="7b4ed-127">Ruby</span></span>
-   <span data-ttu-id="7b4ed-128">Python</span><span class="sxs-lookup"><span data-stu-id="7b4ed-128">Python</span></span>

<span data-ttu-id="7b4ed-129">En fait, vous pouvez utiliser n’importe quel langage moderne pris en charge par Docker sur Linux ou Windows.</span><span class="sxs-lookup"><span data-stu-id="7b4ed-129">Basically, you can use any modern language supported by Docker in Linux or Windows.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="7b4ed-130">[Précédent](deploy-azure-kubernetes-service.md)
>[Suivant](docker-apps-inner-loop-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="7b4ed-130">[Previous](deploy-azure-kubernetes-service.md)
[Next](docker-apps-inner-loop-workflow.md)</span></span>