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
>[Suivant](../docker-devops-workflow/index.md)
