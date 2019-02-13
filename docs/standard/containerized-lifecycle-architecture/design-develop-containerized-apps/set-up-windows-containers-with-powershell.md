---
title: À l’aide des commandes Windows PowerShell dans un fichier DockerFile pour configurer des conteneurs Windows (Docker standard en fonction)
description: Découvrez comment utiliser PowerShell lorsque vous travaillez avec Docker dans des conteneurs Windows
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 11/23/2018
ms.openlocfilehash: df9e98e3f963b6492e1008455251b61a8cb6e771
ms.sourcegitcommit: 30e2fe5cc4165aa6dde7218ec80a13def3255e98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56219969"
---
# <a name="using-windows-powershell-commands-in-a-dockerfile-to-set-up-windows-containers-docker-standard-based"></a>À l’aide des commandes Windows PowerShell dans un fichier DockerFile pour configurer des conteneurs Windows (Docker standard en fonction)

Avec [les conteneurs Windows](/virtualization/windowscontainers/about/index), vous pouvez convertir vos applications Windows existantes pour les images Docker et les déployer avec les mêmes outils que le reste de l’écosystème Docker.

Pour utiliser les conteneurs Windows, vous devez simplement écrire des commandes Windows PowerShell dans le fichier DockerFile, comme illustré dans l’exemple suivant :

```
FROM microsoft/windowsservercore
LABEL Description="IIS" Vendor="Microsoft" Version="10"
RUN powershell -Command Add-WindowsFeature Web-Server
CMD [ "ping", "localhost", "-t" ]
```

Dans ce cas, nous utilisons Windows PowerShell pour installer une image de base Windows Server Core, mais aussi IIS.

De la même façon, vous pouvez également utiliser des commandes Windows PowerShell pour configurer des composants supplémentaires comme ASP.NET traditionnel 4.x et .NET 4.6 ou tout autre logiciel Windows, comme illustré ici :

```
RUN powershell add-windowsfeature web-asp-net45
```

>[!div class="step-by-step"]
>[Précédent](visual-studio-tools-for-docker.md)
>[Suivant](build-aspnet-core-applications-linux-containers-aks-kubernetes.md)
