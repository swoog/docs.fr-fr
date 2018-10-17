---
title: Publication d’un package NuGet
description: Meilleures pratiques recommandées pour la publication des bibliothèques .NET sur NuGet.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 0602712311411ef3d59825bec8c5e550bc8d8265
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370049"
---
# <a name="publishing-a-nuget-package"></a>Publication d’un package NuGet

Les packages NuGet sont publiés et consommés à partir de référentiels de packages. Tandis que NuGet.org est le plus largement connue et utilisée, il existe de nombreux endroits pour publier les packages NuGet :

* **[NuGet.org](https://www.nuget.org/)**  est le référentiel principal en ligne pour les packages NuGet. Tous les packages sur NuGet.org sont accessibles à tout le monde. Par défaut, Visual Studio a NuGet.org comme source de package et pour de nombreux développeurs NuGet.org est le seul référentiel de package qu’ils allez interagir avec. NuGet.org est le meilleur endroit pour publier des packages stables et préliminaires les packages que vous voulez les commentaires de la Communauté sur.

* **[MyGet](https://myget.org/)**  prend en charge du service de référentiel [de flux de package personnalisé gratuit pour les projets open source](https://www.myget.org/opensource). Un flux personnalisé public MyGet est un endroit idéal pour publier des packages en préversion créés par votre service d’intégration continue. MyGet fournit également les flux privés dans le commerce.

* Un **[flux local](/nuget/hosting-packages/local-feeds)** vous permet de traiter un dossier comme un référentiel de packages et rend le `*.nupkg` fichiers dans le dossier accessible par NuGet. Un flux local est utile pour tester un package NuGet avant sa publication sur NuGet.org.

> [!NOTE]
> NuGet.org [n’autorise pas un package à supprimer](/nuget/policies/deleting-packages) une fois qu’il est chargé. Un package peut être retirée de la liste afin qu’il ne soit pas publiquement visible dans l’interface utilisateur, mais le `*.nupkg` peut toujours être téléchargé sur la restauration. En outre, nuget.org n’autorise pas les versions de package en double. Pour corriger un package NuGet avec une erreur d’avoir au retirer de la liste le package incorrect, incrémenter le numéro de version et publier une nouvelle version du package.

**FAIRE ✔️** [publier des packages stables et préliminaires](/nuget/create-packages/publish-a-package) vous souhaitez que les commentaires de la Communauté sur NuGet.org.

**ENVISAGEZ de ✔️** packages de préversion de publication pour un MyGet flux à partir d’une build d’intégration continue.

**ENVISAGEZ de ✔️** test des packages dans votre environnement de développement à l’aide d’un flux local ou un MyGet. Vérifier le fonctionnement du package, puis publiez-le sur NuGet.org.

## <a name="nugetorg-security"></a>Sécurité de NuGet.org

Il est important que les mauvais acteurs ne peut pas accéder à votre compte de NuGet et charger une version malveillante de votre bibliothèque. NuGet.org offre deux facteurs d’authentification et les notifications électroniques lors de la publication d’un package. Activer ces fonctionnalités une fois connecté à NuGet.org sur le **paramètres du compte** page.

![texte de remplacement](./media/publish-nuget-package/nuget-2fa.png "sécurité du compte NuGet")

**FAIRE ✔️** utiliser un compte Microsoft pour vous connecter à NuGet.

**FAIRE ✔️** activer l’authentification à deux facteurs pour accéder à NuGet.

**FAIRE ✔️** activer la notification par courrier électronique lorsqu’un package est publié.

>[!div class="step-by-step"]
[Précédent](./sourcelink.md)
[Suivant](./versioning.md)
