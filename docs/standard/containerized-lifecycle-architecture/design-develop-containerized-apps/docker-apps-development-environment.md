---
title: Environnement de développement pour les applications Docker
description: Découvrez les options d’outil de développement plus importantes qui prennent en charge le cycle de développement de Docker.
ms.date: 02/15/2019
ms.openlocfilehash: 0f71ffa5e6870f45908e4def6577120a17ec744c
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65641418"
---
# <a name="development-environment-for-docker-apps"></a>Environnement de développement pour les applications Docker

## <a name="development-tools-choices-ide-or-editor"></a>Choix des outils de développement : IDE ou éditeur

Non que si vous préférez un IDE complet et puissant ou un éditeur léger et agile, Microsoft a prévu lorsqu’il s’agit de développer des applications Docker.

### <a name="visual-studio-code-and-docker-cli-cross-platform-tools-for-mac-linux-and-windows"></a>Visual Studio Code et Docker CLI (les outils multiplateformes pour Mac, Linux et Windows)

Si vous préférez un éditeur léger et multiplateforme prenant en charge de n’importe quel langage de développement, vous pouvez utiliser Visual Studio Code et interface CLI Docker. Ces produits fournissent une expérience simple et robuste, ce qui est essentielle pour rationaliser le flux de travail de développeur. En installant « Docker pour Mac » ou « Docker pour Windows » (environnement de développement), les développeurs Docker peuvent utiliser une seule interface CLI Docker pour créer des applications pour Windows ou Linux (environnement d’exécution). En outre, Visual Studio Code prend en charge les extensions pour Docker avec IntelliSense pour les fichiers Dockerfile et les tâches de raccourci exécuter des commandes Docker à partir de l’éditeur.

> [!NOTE]
>
> Pour télécharger Visual Studio Code, accédez à <https://code.visualstudio.com/download>.
>
> Pour télécharger Docker pour Mac et Windows, accédez à <https://www.docker.com/products/docker>.

### <a name="visual-studio-with-docker-tools-windows-development-machine"></a>Visual Studio avec des outils Docker (machine de développement Windows)

Nous vous recommandons d’utiliser Visual Studio 2017 (ou version ultérieure) avec les outils Docker intégrée est activée. Avec Visual Studio, vous pouvez développer, exécuter et valider vos applications directement dans l’environnement Docker choisi. Appuyez sur F5 pour déboguer votre application (conteneur unique ou plusieurs conteneurs) directement dans un hôte Docker, ou appuyez sur Ctrl + F5 pour modifier et actualiser votre application sans avoir à recréer le conteneur. Il est le choix le plus simple et plus puissant pour les développeurs Windows créer des conteneurs Docker pour Linux ou Windows.

### <a name="visual-studio-for-mac-mac-development-machine"></a>Visual Studio pour Mac (machine de développement Mac)

Vous pouvez utiliser [Visual Studio pour Mac](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link) lors du développement d’applications basées sur Docker. Visual Studio pour Mac propose un IDE plus riche par rapport à Visual Studio Code pour Mac.

## <a name="language-and-framework-choices"></a>Choix de langage et de framework

Vous pouvez développer des applications Docker à l’aide des outils de Microsoft avec les langages les plus récents. Voici une liste initiale, mais vous n’êtes pas limité à celui-ci :

- .NET Core et ASP.NET Core
- Node.js
- Go
- Java
- Ruby
- Python

En fait, vous pouvez utiliser n’importe quel langage moderne pris en charge par Docker sur Linux ou Windows.

>[!div class="step-by-step"]
>[Précédent](deploy-azure-kubernetes-service.md)
>[Suivant](docker-apps-inner-loop-workflow.md)
