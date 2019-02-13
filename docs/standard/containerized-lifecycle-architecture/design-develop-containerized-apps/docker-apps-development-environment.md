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
# <a name="development-environment-for-docker-apps"></a>Environnement de développement pour les applications Docker

## <a name="development-tools-choices-ide-or-editor"></a>Choix des outils de développement : IDE ou éditeur

Non que si vous préférez un IDE complet et puissant ou un éditeur léger et agile, Microsoft a prévu lorsqu’il s’agit de développer des applications Docker.

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a>Visual Studio Code et Docker CLI (les outils multiplateformes pour Mac, Linux et Windows)

Si vous préférez un éditeur léger et multiplateforme prenant en charge de n’importe quel langage de développement, vous pouvez utiliser Visual Studio Code et interface CLI Docker. Ces produits fournissent une expérience simple et robuste, ce qui est essentielle pour rationaliser le flux de travail de développeur. En installant « Docker pour Mac » ou « Docker pour Windows » (environnement de développement), les développeurs Docker peuvent utiliser une seule interface CLI Docker pour créer des applications pour Windows ou Linux (environnement d’exécution). En outre, Visual Studio Code prend en charge les extensions pour Docker avec IntelliSense pour les fichiers Dockerfile et les tâches de raccourci exécuter des commandes Docker à partir de l’éditeur.

> [!NOTE]
> Pour télécharger Visual Studio Code, accédez à <https://code.visualstudio.com/download>.

Pour télécharger Docker pour Mac et Windows, accédez à <https://www.docker.com/products/docker>.

### <a name="visual-studio-with-docker-tools"></a>Visual Studio avec des outils Docker

Lorsque vous utilisez Visual Studio 2015, vous pouvez installer les outils de module complémentaire « Outils Docker pour Visual Studio ». Pour Visual Studio 2017, outils Docker sont fournis intégrées déjà. Dans les deux cas, que vous pouvez développer, exécuter et valider vos applications directement dans l’environnement Docker choisi. F5 votre application (conteneur unique ou plusieurs conteneurs) directement dans un Docker héberger avec débogage, ou appuyez sur Ctrl + F5 pour modifier et actualiser votre application sans avoir à recréer le conteneur. Ce choix est le plus simple et plus puissant pour les développeurs Windows en créant des conteneurs Docker pour Linux ou Windows.

> [!NOTE]
> Pour télécharger les outils Docker pour Visual Studio, accédez à <https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4>.

## <a name="language-and-framework-choices"></a>Choix de langage et de framework

Vous pouvez développer des applications de Docker et les outils de Microsoft avec les langages les plus récents. Voici une liste initiale, mais vous n’êtes pas limité à celui-ci :

-   .NET Core et ASP.NET Core
-   Node.js
-   Golang
-   Java
-   Ruby
-   Python

En fait, vous pouvez utiliser n’importe quel langage moderne pris en charge par Docker sur Linux ou Windows.

>[!div class="step-by-step"]
>[Précédent](deploy-azure-kubernetes-service.md)
>[Suivant](docker-apps-inner-loop-workflow.md)