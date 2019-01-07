---
title: Commande dotnet clean
description: La commande dotnet clean nettoie le répertoire actif.
ms.date: 12/04/2018
ms.openlocfilehash: a25b7930794795e3dff5051a8ca1dd1b9c261dfd
ms.sourcegitcommit: e6ad58812807937b03f5c581a219dcd7d1726b1d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53169857"
---
# <a name="dotnet-clean"></a>dotnet clean

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a>Name

`dotnet clean` : Nettoie la sortie d’un projet.

## <a name="synopsis"></a>Résumé

```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
dotnet clean [-h|--help]
```

## <a name="description"></a>Description

La commande `dotnet clean` nettoie la sortie de la génération précédente. Comme elle est implémentée en tant que [cible MSBuild](/visualstudio/msbuild/msbuild-targets), le projet est évalué lorsque la commande est exécutée. Seules les sorties créées lors de la génération sont nettoyées. Les dossiers de sortie intermédiaire (*obj*) et de sortie finale (*bin*) sont tous deux nettoyés.

## <a name="arguments"></a>Arguments

`PROJECT`

Le projet MSBuild à nettoyer. Si vous ne spécifiez pas de fichier projet, MSBuild recherche dans le répertoire de travail actuel un fichier avec une extension se terminant par *proj* et l’utilise.

## <a name="options"></a>Options

* **`-c|--configuration {Debug|Release}`**

  Définit la configuration de build. La valeur par défaut est `Debug`. Cette option est uniquement requise durant le nettoyage si vous l’avez spécifiée au moment de la génération.

* **`-f|--framework <FRAMEWORK>`**

  Le [framework](../../standard/frameworks.md) spécifié au moment de la génération. Le framework doit être défini dans le [fichier projet](csproj.md). Si vous avez spécifié le framework au moment de la génération, vous devez spécifier le framework lors du nettoyage.

* **`-h|--help`**

  Affiche une aide brève pour la commande.

* **`-o|--output <OUTPUT_DIRECTORY>`**

  Répertoire dans lequel les sorties générées sont placées. Spécifiez le commutateur `-f|--framework <FRAMEWORK>` avec le commutateur de répertoire de sortie si vous avez spécifié le framework lorsque le projet a été généré.

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  Nettoie le dossier de sortie du runtime spécifié. Cette option est utilisée à la création d’un [déploiement autonome](../deploying/index.md#self-contained-deployments-scd). Option disponible à partir du kit SDK .NET Core 2.0.

* **`-v|--verbosity <LEVEL>`**

  Définit le niveau de détail de la commande. Niveaux autorisés : q[uiet], m[inimal], n[ormal], d[etailed] et diag[nostic].

## <a name="examples"></a>Exemples

* Nettoyez une génération par défaut du projet :

  ```console
  dotnet clean
  ```

* Nettoyez un projet généré à l’aide de la configuration Release :

  ```console
  dotnet clean --configuration Release
  ```