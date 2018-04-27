---
title: Environnement de développement pour les applications Docker
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
ms.prod: .net
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ddd1006c8c6728d4d315442f409f8fa33e54f9a3
ms.sourcegitcommit: 2e8acae16ae802f2d6d04e3ce0a6dbf04e476513
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2018
---
# <a name="development-environment-for-docker-apps"></a><span data-ttu-id="eda1d-103">Environnement de développement pour les applications Docker</span><span class="sxs-lookup"><span data-stu-id="eda1d-103">Development environment for Docker apps</span></span>

## <a name="development-tools-choices-ide-or-editor"></a><span data-ttu-id="eda1d-104">Choix des outils de développement : IDE ou éditeur</span><span class="sxs-lookup"><span data-stu-id="eda1d-104">Development tools choices: IDE or editor</span></span>

<span data-ttu-id="eda1d-105">Sans que si vous préférez un IDE complet et puissant ou un éditeur léger et agile, Microsoft a vous couvert en matière de développement d’applications de Docker.</span><span class="sxs-lookup"><span data-stu-id="eda1d-105">No matter if you prefer a full and powerful IDE or a lightweight and agile editor, Microsoft has you covered when it comes to developing Docker applications.</span></span>

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a><span data-ttu-id="eda1d-106">Visual Studio Code et Docker CLI (les outils multiplateformes pour Mac, Linux et Windows)</span><span class="sxs-lookup"><span data-stu-id="eda1d-106">Visual Studio Code and Docker CLI (cross-platform tools for Mac, Linux, and Windows)</span></span>

<span data-ttu-id="eda1d-107">Si vous préférez un éditeur léger, inter-plateformes prenant en charge de n’importe quel langage de développement, vous pouvez utiliser le Code de Visual Studio et l’interface CLI de Docker.</span><span class="sxs-lookup"><span data-stu-id="eda1d-107">If you prefer a lightweight, cross-platform editor supporting any development language, you can use Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="eda1d-108">Ces produits fournissent une expérience simple et robuste, qui est essentielle pour rationaliser le flux de travail du développeur.</span><span class="sxs-lookup"><span data-stu-id="eda1d-108">These products provide a simple yet robust experience, which is critical for streamlining the developer workflow.</span></span> <span data-ttu-id="eda1d-109">En installant « Docker pour Mac » ou « Docker pour Windows » (environnement de développement), les développeurs de Docker peuvent utiliser des CLI Docker unique pour créer des applications pour Windows ou Linux (environnement d’exécution).</span><span class="sxs-lookup"><span data-stu-id="eda1d-109">By installing "Docker for Mac" or "Docker for Windows" (development environment), Docker developers can use a single Docker CLI to build apps for both Windows or Linux (runtime environment).</span></span> <span data-ttu-id="eda1d-110">De plus, Visual Studio Code prend en charge les extensions de Docker avec IntelliSense pour les fichiers Dockerfile et tâches de raccourci exécuter des commandes Docker à partir de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="eda1d-110">Plus, Visual Studio Code supports extensions for Docker with IntelliSense for Dockerfiles and shortcut-tasks to run Docker commands from the editor.</span></span>

> [!NOTE]
> <span data-ttu-id="eda1d-111">Pour télécharger le Code de Visual Studio, accédez à <https://code.visualstudio.com/download>.</span><span class="sxs-lookup"><span data-stu-id="eda1d-111">To download Visual Studio Code, go to <https://code.visualstudio.com/download>.</span></span>

<span data-ttu-id="eda1d-112">Pour télécharger Docker pour Mac et Windows, accédez à <http://www.docker.com/products/docker>.</span><span class="sxs-lookup"><span data-stu-id="eda1d-112">To download Docker for Mac and Windows, go to <http://www.docker.com/products/docker>.</span></span>

### <a name="visual-studio-with-docker-tools"></a><span data-ttu-id="eda1d-113">Visual Studio avec des outils de Docker</span><span class="sxs-lookup"><span data-stu-id="eda1d-113">Visual Studio with Docker Tools</span></span>

<span data-ttu-id="eda1d-114">Lorsque vous utilisez Visual Studio 2015, vous pouvez installer les outils complémentaires « Docker des outils pour Visual Studio ».</span><span class="sxs-lookup"><span data-stu-id="eda1d-114">When you're using Visual Studio 2015 you can install the add-on tools "Docker Tools for Visual Studio."</span></span> <span data-ttu-id="eda1d-115">Pour Visual Studio 2017, outils Docker sont intégrés déjà.</span><span class="sxs-lookup"><span data-stu-id="eda1d-115">For Visual Studio 2017, Docker Tools come built in already.</span></span> <span data-ttu-id="eda1d-116">Dans les deux cas, vous pouvez développer, exécuter et valider vos applications directement dans l’environnement Docker choisi.</span><span class="sxs-lookup"><span data-stu-id="eda1d-116">In both cases you can develop, run, and validate your applications directly in the chosen Docker environment.</span></span> <span data-ttu-id="eda1d-117">F5 (unique ou plusieurs conteneurs) de votre application directement dans une Docker héberger avec débogage ou appuyez sur Ctrl + F5 pour actualiser votre application sans avoir à reconstruire le conteneur et les modifier.</span><span class="sxs-lookup"><span data-stu-id="eda1d-117">F5 your application (single container or multiple containers) directly into a Docker host with debugging, or press Ctrl+F5 to edit and refresh your app without having to rebuild the container.</span></span> <span data-ttu-id="eda1d-118">Il s’agit du choix de la plus simple et plus puissant pour les développeurs Windows en créant des conteneurs Docker pour Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="eda1d-118">This is the simplest and more powerful choice for Windows developers creating Docker containers for Linux or Windows.</span></span>

> [!NOTE]
> <span data-ttu-id="eda1d-119">Pour télécharger les outils Docker pour Visual Studio, accédez à <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span><span class="sxs-lookup"><span data-stu-id="eda1d-119">To download Docker Tools for Visual Studio, go to <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.</span></span>

## <a name="language-and-framework-choices"></a><span data-ttu-id="eda1d-120">Choix de langue et le framework</span><span class="sxs-lookup"><span data-stu-id="eda1d-120">Language and framework choices</span></span>

<span data-ttu-id="eda1d-121">Vous pouvez développer des applications de Docker et les outils de Microsoft avec les langues les plus récents.</span><span class="sxs-lookup"><span data-stu-id="eda1d-121">You can develop Docker applications and Microsoft tools with most modern languages.</span></span> <span data-ttu-id="eda1d-122">Voici une liste initiale, mais vous n’êtes pas limité à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="eda1d-122">The following is an initial list, but you are not limited to it:</span></span>

-   <span data-ttu-id="eda1d-123">.NET core et ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="eda1d-123">.NET Core and ASP.NET Core</span></span>

-   <span data-ttu-id="eda1d-124">Node.js</span><span class="sxs-lookup"><span data-stu-id="eda1d-124">Node.js</span></span>

-   <span data-ttu-id="eda1d-125">Golang</span><span class="sxs-lookup"><span data-stu-id="eda1d-125">Golang</span></span>

-   <span data-ttu-id="eda1d-126">Java</span><span class="sxs-lookup"><span data-stu-id="eda1d-126">Java</span></span>

-   <span data-ttu-id="eda1d-127">Ruby</span><span class="sxs-lookup"><span data-stu-id="eda1d-127">Ruby</span></span>

-   <span data-ttu-id="eda1d-128">Python</span><span class="sxs-lookup"><span data-stu-id="eda1d-128">Python</span></span>

<span data-ttu-id="eda1d-129">En fait, vous pouvez utiliser n’importe quel langage moderne pris en charge par Docker sur Windows ou Linux.</span><span class="sxs-lookup"><span data-stu-id="eda1d-129">Basically, you can use any modern language supported by Docker in Linux or Windows.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="eda1d-130">[Précédente] (orchestrer-haute-évolutivité-availability.md) [suivant] (docker-applications-interne-boucle-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="eda1d-130">[Previous] (orchestrate-high-scalability-availability.md) [Next] (docker-apps-inner-loop-workflow.md)</span></span>
