---
title: À l’aide des commandes Windows PowerShell dans un fichier DockerFile pour configurer des conteneurs Windows (Docker standard en fonction)
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/19/2017
ms.openlocfilehash: 5e85beea0efbee6a2b6594e3a49d705505a36e1c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53149391"
---
# <a name="using-windows-powershell-commands-in-a-dockerfile-to-set-up-windows-containers-docker-standard-based"></a><span data-ttu-id="2e0ec-103">À l’aide des commandes Windows PowerShell dans un fichier DockerFile pour configurer des conteneurs Windows (Docker standard en fonction)</span><span class="sxs-lookup"><span data-stu-id="2e0ec-103">Using Windows PowerShell commands in a DockerFile to set up Windows Containers (Docker standard based)</span></span>

<span data-ttu-id="2e0ec-104">Avec [les conteneurs Windows](/virtualization/windowscontainers/about/index), vous pouvez convertir vos applications Windows existantes pour les images Docker et les déployer avec les mêmes outils que le reste de l’écosystème Docker.</span><span class="sxs-lookup"><span data-stu-id="2e0ec-104">With [Windows Containers](/virtualization/windowscontainers/about/index), you can convert your existing Windows applications to Docker images and deploy them with the same tools as the rest of the Docker ecosystem.</span></span>

<span data-ttu-id="2e0ec-105">Pour utiliser les conteneurs Windows, vous devez simplement écrire des commandes Windows PowerShell dans le fichier DockerFile, comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="2e0ec-105">To use Windows Containers, you just need to write Windows PowerShell commands in the DockerFile, as demonstrated in the following example:</span></span>

```
FROM microsoft/windowsservercore
LABEL Description="IIS" Vendor="Microsoft" Version="10"
RUN powershell -Command Add-WindowsFeature Web-Server
CMD [ "ping", "localhost", "-t" ]
```

<span data-ttu-id="2e0ec-106">Dans ce cas, nous utilisons Windows PowerShell pour installer une image de base Windows Server Core, mais aussi IIS.</span><span class="sxs-lookup"><span data-stu-id="2e0ec-106">In this case, we're using Windows PowerShell to install a Windows Server Core base image as well as IIS.</span></span>

<span data-ttu-id="2e0ec-107">De la même façon, vous pouvez également utiliser des commandes Windows PowerShell pour configurer des composants supplémentaires comme ASP.NET traditionnel 4.x et .NET 4.6 ou tout autre logiciel Windows, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="2e0ec-107">In a similar way, you also could use Windows PowerShell commands to set up additional components like the traditional ASP.NET 4.x and .NET 4.6 or any other Windows software, as shown here:</span></span>

```
RUN powershell add-windowsfeature web-asp-net45
```

>[!div class="step-by-step"]
><span data-ttu-id="2e0ec-108">[Précédent](visual-studio-tools-for-docker.md)
>[Suivant](../docker-devops-workflow/index.md)</span><span class="sxs-lookup"><span data-stu-id="2e0ec-108">[Previous](visual-studio-tools-for-docker.md)
[Next](../docker-devops-workflow/index.md)</span></span>
