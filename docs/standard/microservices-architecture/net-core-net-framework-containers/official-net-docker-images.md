---
title: Images officielles .NET Docker
description: Architecture de microservices .NET pour les applications .NET en conteneur | Images officielles .NET Docker
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/11/2018
ms.openlocfilehash: 5d42ec77958e056b75b0e379f8ab520ac926c72a
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075567"
---
# <a name="official-net-docker-images"></a>Images officielles .NET Docker

Les images officielles .NET Docker sont des images Docker créées et optimisées par Microsoft. Elles sont accessibles au grand public dans les dépôts Microsoft sur [Docker Hub](https://hub.docker.com/u/microsoft/). Chaque dépôt peut contenir plusieurs images, en fonction des versions de .NET, du système d’exploitation et de ses versions (Linux Debian, Linux Alpine, Windows Nano Server, Windows Server Core, etc.).

Depuis .NET Core 2.1, toutes les images .NET Core, notamment pour ASP.NET Core sont disponibles sur Docker Hub dans le référentiel d’images .NET Core : https://hub.docker.com/r/microsoft/dotnet/

La plupart des dépôts d’images fournissent un balisage complet pour vous aider à sélectionner non seulement une version de framework spécifique, mais aussi un système d’exploitation (distribution Linux ou version de Windows).

## <a name="net-core-and-docker-image-optimizations-for-development-versus-production"></a>Optimisations d’images .NET Core et Docker pour le développement et la production

Au moment de créer des images Docker pour développeurs, Microsoft s’est concentré sur les principaux scénarios suivants :

-   Images utilisées pour *développer* et générer des applications .NET Core

-   Images utilisées pour *exécuter* des applications .NET Core

Pourquoi plusieurs images ? En règle générale, vos propriétés varient selon que vous développez, générez ou exécutez des applications en conteneur. En proposant des images différentes en fonction des tâches, Microsoft permet d’optimiser ces processus distincts que sont le développement, la génération et le déploiement d’applications.

### <a name="during-development-and-build"></a>En phase de développement et de génération

En phase de développement, il importe d’itérer rapidement les modifications et de pouvoir les déboguer. La taille de l’image est moins importante que la possibilité d’apporter des modifications à votre code et de voir rapidement ces modifications. Certains outils et « conteneurs d’agent de build » utilisent l’image de développement .NET Core (*microsoft/dotnet:2.1-sdk*) pendant les processus de développement et de génération. Ce qui importe au moment de générer à l’intérieur d’un conteneur Docker, ce sont les éléments nécessaires à la compilation de l’application. Il s’agit notamment du compilateur et des autres dépendances .NET.

Pourquoi ce type d’image de build est-il important ? Vous ne déployez pas cette image en production. En effet, il s’agit d’une image que vous utilisez pour générer le contenu que vous placez dans une image de production. Cette image est destinée à être utilisée dans votre environnement d’intégration continue (CI) ou votre environnement de génération lorsque vous utilisez des builds Docker à plusieurs phases.

### <a name="in-production"></a>En production

Ce qui importe en production, c’est la vitesse à laquelle vous pouvez déployer et démarrer vos conteneurs basées sur une image .NET Core de production. Par conséquent, l’image runtime basée sur *microsoft/dotnet:2.1-aspnetcore-runtime* est petite de façon à accélérer son transit sur le réseau de votre registre Docker à vos hôtes Docker. Le contenu est prêt à s’exécuter, ce qui permet d’écourter au maximum la durée entre le démarrage du conteneur et le traitement des résultats. Dans le modèle Docker, il n’est pas nécessaire de compiler à partir de code C\# comme c’est le cas lorsque vous exécutez la commande dotnet build ou dotnet publish en utilisant le conteneur de build.

Dans cette image optimisée, vous placez uniquement les fichiers binaires et le reste du contenu nécessaire à l’exécution de l’application. Par exemple, le contenu créé par la commande dotnet publish contient uniquement les fichiers binaires .NET compilés, des images et des fichiers .js et .css. Au fil du temps, vous verrez des images qui contiennent des packages prétraités avec JIT (la compilation du langage intermédiaire en code natif qui se produit lors de l’exécution).

Bien qu’il existe plusieurs versions des images .NET Core et ASP.NET Core, elles partagent toutes une ou plusieurs couches, dont la couche de base. Par conséquent, la quantité d’espace disque nécessaire au stockage d’une image est faible ; elle est uniquement constituée de la différence entre votre image personnalisée et son image de base. De ce fait, l’extraction de l’image de votre registre est très rapide.

En explorant les dépôts d’images .NET dans Docker Hub, vous trouverez plusieurs versions d’images classées ou marquées avec des balises. Ces balises permettent d’identifier la version dont vous avez besoin, comme celles présentées dans le tableau suivant :

| Image                                       | Commentaires                                                                                          |
| ------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| microsoft/dotnet:**2.1-aspnetcore-runtime** | ASP.NET Core, avec le runtime uniquement et les optimisations ASP.NET Core, Linux et Windows (multi-arch) |
| microsoft/dotnet:**2.1-sdk**                | .NET Core, avec les SDK inclus, sur Linux et Windows (multi-arch)                                  |


>[!div class="step-by-step"]
[Précédent](net-container-os-targets.md)
[Suivant](../architect-microservice-container-applications/index.md)
