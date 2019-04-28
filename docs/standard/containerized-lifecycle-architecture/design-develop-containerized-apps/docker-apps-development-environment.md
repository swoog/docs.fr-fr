---
title: Environnement de développement pour les applications Docker
description: Découvrez les options d’outil de développement plus importantes qui prennent en charge le cycle de développement de Docker.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 3a2fcbe3b9380083622b6ce72cea4bab17d7c2ea
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61799318"
---
# <a name="development-environment-for-docker-apps"></a><span data-ttu-id="34c8f-103">Environnement de développement pour les applications Docker</span><span class="sxs-lookup"><span data-stu-id="34c8f-103">Development environment for Docker apps</span></span>

## <a name="development-tools-choices-ide-or-editor"></a><span data-ttu-id="34c8f-104">Choix des outils de développement : IDE ou éditeur</span><span class="sxs-lookup"><span data-stu-id="34c8f-104">Development tools choices: IDE or editor</span></span>

<span data-ttu-id="34c8f-105">Non que si vous préférez un IDE complet et puissant ou un éditeur léger et agile, Microsoft a prévu lorsqu’il s’agit de développer des applications Docker.</span><span class="sxs-lookup"><span data-stu-id="34c8f-105">No matter if you prefer a full and powerful IDE or a lightweight and agile editor, Microsoft has you covered when it comes to developing Docker applications.</span></span>

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a><span data-ttu-id="34c8f-106">Visual Studio Code et Docker CLI (les outils multiplateformes pour Mac, Linux et Windows)</span><span class="sxs-lookup"><span data-stu-id="34c8f-106">Visual Studio Code and Docker CLI (cross-platform tools for Mac, Linux, and Windows)</span></span>

<span data-ttu-id="34c8f-107">Si vous préférez un éditeur léger et multiplateforme prenant en charge de n’importe quel langage de développement, vous pouvez utiliser Visual Studio Code et interface CLI Docker.</span><span class="sxs-lookup"><span data-stu-id="34c8f-107">If you prefer a lightweight, cross-platform editor supporting any development language, you can use Visual Studio Code and Docker CLI.</span></span> <span data-ttu-id="34c8f-108">Ces produits fournissent une expérience simple et robuste, ce qui est essentielle pour rationaliser le flux de travail de développeur.</span><span class="sxs-lookup"><span data-stu-id="34c8f-108">These products provide a simple yet robust experience, which is critical for streamlining the developer workflow.</span></span> <span data-ttu-id="34c8f-109">En installant « Docker pour Mac » ou « Docker pour Windows » (environnement de développement), les développeurs Docker peuvent utiliser une seule interface CLI Docker pour créer des applications pour Windows ou Linux (environnement d’exécution).</span><span class="sxs-lookup"><span data-stu-id="34c8f-109">By installing "Docker for Mac" or "Docker for Windows" (development environment), Docker developers can use a single Docker CLI to build apps for both Windows or Linux (runtime environment).</span></span> <span data-ttu-id="34c8f-110">En outre, Visual Studio Code prend en charge les extensions pour Docker avec IntelliSense pour les fichiers Dockerfile et les tâches de raccourci exécuter des commandes Docker à partir de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="34c8f-110">Plus, Visual Studio Code supports extensions for Docker with IntelliSense for Dockerfiles and shortcut-tasks to run Docker commands from the editor.</span></span>

> [!NOTE]
>
> <span data-ttu-id="34c8f-111">Pour télécharger Visual Studio Code, accédez à <https://code.visualstudio.com/download>.</span><span class="sxs-lookup"><span data-stu-id="34c8f-111">To download Visual Studio Code, go to <https://code.visualstudio.com/download>.</span></span>
>
> <span data-ttu-id="34c8f-112">Pour télécharger Docker pour Mac et Windows, accédez à <https://www.docker.com/products/docker>.</span><span class="sxs-lookup"><span data-stu-id="34c8f-112">To download Docker for Mac and Windows, go to <https://www.docker.com/products/docker>.</span></span>

### <a name="visual-studio-with-docker-tools-windows-development-machine"></a><span data-ttu-id="34c8f-113">Visual Studio avec des outils Docker (machine de développement Windows)</span><span class="sxs-lookup"><span data-stu-id="34c8f-113">Visual Studio with Docker Tools (Windows development machine)</span></span>

<span data-ttu-id="34c8f-114">Nous vous recommandons d’utiliser Visual Studio 2017 (ou version ultérieure) avec les outils Docker intégrée est activée.</span><span class="sxs-lookup"><span data-stu-id="34c8f-114">We recommend you use Visual Studio 2017 (or later) with the built-in Docker Tools enabled.</span></span> <span data-ttu-id="34c8f-115">Avec Visual Studio, vous pouvez développer, exécuter et valider vos applications directement dans l’environnement Docker choisi.</span><span class="sxs-lookup"><span data-stu-id="34c8f-115">With Visual Studio, you can develop, run, and validate your applications directly in the chosen Docker environment.</span></span> <span data-ttu-id="34c8f-116">Appuyez sur F5 pour déboguer votre application (conteneur unique ou plusieurs conteneurs) directement dans un hôte Docker, ou appuyez sur Ctrl + F5 pour modifier et actualiser votre application sans avoir à recréer le conteneur.</span><span class="sxs-lookup"><span data-stu-id="34c8f-116">Press F5 to debug your application (single container or multiple containers) directly in a Docker host, or press Ctrl+F5 to edit and refresh your app without having to rebuild the container.</span></span> <span data-ttu-id="34c8f-117">Il est le choix le plus simple et plus puissant pour les développeurs Windows créer des conteneurs Docker pour Linux ou Windows.</span><span class="sxs-lookup"><span data-stu-id="34c8f-117">It's the simplest and most powerful choice for Windows developers to create Docker containers for Linux or Windows.</span></span>

### <a name="visual-studio-for-mac-mac-development-machine"></a><span data-ttu-id="34c8f-118">Visual Studio pour Mac (machine de développement Mac)</span><span class="sxs-lookup"><span data-stu-id="34c8f-118">Visual Studio for Mac (Mac development machine)</span></span>

<span data-ttu-id="34c8f-119">Vous pouvez utiliser [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link) lors du développement d’applications basées sur Docker.</span><span class="sxs-lookup"><span data-stu-id="34c8f-119">You can use [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link) when developing Docker-based applications.</span></span> <span data-ttu-id="34c8f-120">Visual Studio pour Mac propose un IDE plus riche par rapport à Visual Studio Code pour Mac.</span><span class="sxs-lookup"><span data-stu-id="34c8f-120">Visual Studio for Mac offers a richer IDE when compared to Visual Studio Code for Mac.</span></span>

## <a name="language-and-framework-choices"></a><span data-ttu-id="34c8f-121">Choix de langage et de framework</span><span class="sxs-lookup"><span data-stu-id="34c8f-121">Language and framework choices</span></span>

<span data-ttu-id="34c8f-122">Vous pouvez développer des applications Docker à l’aide des outils de Microsoft avec les langages les plus récents.</span><span class="sxs-lookup"><span data-stu-id="34c8f-122">You can develop Docker applications using Microsoft tools with most modern languages.</span></span> <span data-ttu-id="34c8f-123">Voici une liste initiale, mais vous n’êtes pas limité à celui-ci :</span><span class="sxs-lookup"><span data-stu-id="34c8f-123">The following is an initial list, but you're not limited to it:</span></span>

- <span data-ttu-id="34c8f-124">.NET Core et ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="34c8f-124">.NET Core and ASP.NET Core</span></span>
- <span data-ttu-id="34c8f-125">Node.js</span><span class="sxs-lookup"><span data-stu-id="34c8f-125">Node.js</span></span>
- <span data-ttu-id="34c8f-126">Go</span><span class="sxs-lookup"><span data-stu-id="34c8f-126">Go</span></span>
- <span data-ttu-id="34c8f-127">Java</span><span class="sxs-lookup"><span data-stu-id="34c8f-127">Java</span></span>
- <span data-ttu-id="34c8f-128">Ruby</span><span class="sxs-lookup"><span data-stu-id="34c8f-128">Ruby</span></span>
- <span data-ttu-id="34c8f-129">Python</span><span class="sxs-lookup"><span data-stu-id="34c8f-129">Python</span></span>

<span data-ttu-id="34c8f-130">En fait, vous pouvez utiliser n’importe quel langage moderne pris en charge par Docker sur Linux ou Windows.</span><span class="sxs-lookup"><span data-stu-id="34c8f-130">Basically, you can use any modern language supported by Docker in Linux or Windows.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="34c8f-131">[Précédent](deploy-azure-kubernetes-service.md)
>[Suivant](docker-apps-inner-loop-workflow.md)</span><span class="sxs-lookup"><span data-stu-id="34c8f-131">[Previous](deploy-azure-kubernetes-service.md)
[Next](docker-apps-inner-loop-workflow.md)</span></span>
