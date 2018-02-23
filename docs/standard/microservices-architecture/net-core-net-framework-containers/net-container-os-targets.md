---
title: "Quel système d’exploitation cibler avec les conteneurs .NET"
description: "Architecture de microservices .NET pour les applications .NET en conteneur | Quel système d’exploitation cibler avec les conteneurs .NET"
keywords: Docker, microservices, ASP.NET, conteneur
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ef7a21efa23be3a5181f08066a093abbb915c20f
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="what-os-to-target-with-net-containers"></a><span data-ttu-id="7aafa-104">Quel système d’exploitation cibler avec les conteneurs .NET</span><span class="sxs-lookup"><span data-stu-id="7aafa-104">What OS to target with .NET containers</span></span>

<span data-ttu-id="7aafa-105">Compte tenu de la diversité des systèmes d’exploitation pris en charge par Docker et des différences entre .NET Framework et .NET Core, vous avez tout intérêt à cibler le système d’exploitation et la version en fonction du framework que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="7aafa-105">Given the diversity of operating systems supported by Docker and the differences between .NET Framework and .NET Core, you should target a specific OS and specific versions depending on the framework you are using.</span></span> 

<span data-ttu-id="7aafa-106">Pour Windows, vous pouvez utiliser Windows Server Core ou Windows Nano Server.</span><span class="sxs-lookup"><span data-stu-id="7aafa-106">For Windows, you can use Windows Server Core or Windows Nano Server.</span></span> <span data-ttu-id="7aafa-107">Ces versions de Windows offrent des caractéristiques différentes (IIS dans Windows Server Core et un serveur web auto-hébergé comme Kestrel dans Nano Server) qui peuvent être nécessaires à .NET Framework ou .NET Core, respectivement.</span><span class="sxs-lookup"><span data-stu-id="7aafa-107">These Windows versions provide different characteristics (IIS in Windows Server Core versus a self-hosted web server like Kestrel in Nano Server) that might be needed by .NET Framework or .NET Core, respectively.</span></span> 

<span data-ttu-id="7aafa-108">Pour Linux, plusieurs distributions sont disponibles et prises en charge dans les images .NET Docker officielles (comme Debian).</span><span class="sxs-lookup"><span data-stu-id="7aafa-108">For Linux, multiple distros are available and supported in official .NET Docker images (like Debian).</span></span>

<span data-ttu-id="7aafa-109">La figure 3-1 indique la version du système d’exploitation à utiliser en fonction de la version du .NET Framework utilisée.</span><span class="sxs-lookup"><span data-stu-id="7aafa-109">In Figure 3-1 you can see the possible OS version depending on the .NET framework used.</span></span>

![](./media/image1.png)

<span data-ttu-id="7aafa-110">**Figure 3-1** :</span><span class="sxs-lookup"><span data-stu-id="7aafa-110">**Figure 3-1.**</span></span> <span data-ttu-id="7aafa-111">systèmes d’exploitation à cibler en fonction des versions de .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7aafa-111">Operating systems to target depending on versions of the .NET framework</span></span>

<span data-ttu-id="7aafa-112">Vous pouvez aussi créer votre propre image Docker si souhaitez utiliser une autre distribution Linux ou une image contenant des versions non fournies par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7aafa-112">You can also create your own Docker image in cases where you want to use a different Linux distro or where you want an image with versions not provided by Microsoft.</span></span> <span data-ttu-id="7aafa-113">Par exemple, vous pouvez créer une image avec ASP.NET Core s’exécutant sur le .NET Framework classique et Windows Server Core, ce qui n’est pas un scénario très courant pour Docker.</span><span class="sxs-lookup"><span data-stu-id="7aafa-113">For example, you might create an image with ASP.NET Core running on the traditional .NET Framework and Windows Server Core, which is a not-so-common scenario for Docker.</span></span>

<span data-ttu-id="7aafa-114">Au moment d’ajouter le nom de l’image à votre fichier Dockerfile, vous pouvez sélectionner le système d’exploitation et la version en fonction de la balise que vous utilisez, comme dans les exemples suivants :</span><span class="sxs-lookup"><span data-stu-id="7aafa-114">When you add the image name to your Dockerfile file, you can select the operating system and version depending on the tag you use, as in the following examples:</span></span>

-   <span data-ttu-id="7aafa-115">microsoft/**dotnet:2.0.0-runtime-jessie**</span><span class="sxs-lookup"><span data-stu-id="7aafa-115">microsoft/**dotnet:2.0.0-runtime-jessie**</span></span>

        .NET Core 2.0 runtime-only on Linux

-   <span data-ttu-id="7aafa-116">microsoft/**dotnet:2.0.0-runtime-nanoserver-1709**</span><span class="sxs-lookup"><span data-stu-id="7aafa-116">microsoft/**dotnet:2.0.0-runtime-nanoserver-1709**</span></span> 

        .NET Core 2.0 runtime-only on Windows Nano Server (Windows Server 2016 Fall Creators Update version 1709)

-   <span data-ttu-id="7aafa-117">microsoft/**aspnetcore:2.0**</span><span class="sxs-lookup"><span data-stu-id="7aafa-117">microsoft/**aspnetcore:2.0**</span></span>
    
        .NET Core 2.0 multi-architecture: Supports Linux and Windows Nano Server depending on the Docker host.
        The aspnetcore image has a few optimizations for ASP.NET Core. 





>[!div class="step-by-step"]
<span data-ttu-id="7aafa-118">[Précédent] (container-framework-choice-factors.md) [Suivant] (official-net-docker-images.md)</span><span class="sxs-lookup"><span data-stu-id="7aafa-118">[Previous] (container-framework-choice-factors.md) [Next] (official-net-docker-images.md)</span></span>
