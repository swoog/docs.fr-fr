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
# <a name="dotnet-clean"></a><span data-ttu-id="bfd4e-103">dotnet clean</span><span class="sxs-lookup"><span data-stu-id="bfd4e-103">dotnet clean</span></span>

[!INCLUDE [topic-appliesto-net-core-all](../../../includes/topic-appliesto-net-core-all.md)]

## <a name="name"></a><span data-ttu-id="bfd4e-104">Name</span><span class="sxs-lookup"><span data-stu-id="bfd4e-104">Name</span></span>

<span data-ttu-id="bfd4e-105">`dotnet clean` : Nettoie la sortie d’un projet.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-105">`dotnet clean` - Cleans the output of a project.</span></span>

## <a name="synopsis"></a><span data-ttu-id="bfd4e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bfd4e-106">Synopsis</span></span>

```
dotnet clean [<PROJECT>] [-c|--configuration] [-f|--framework] [-o|--output] [-r|--runtime] [-v|--verbosity]
dotnet clean [-h|--help]
```

## <a name="description"></a><span data-ttu-id="bfd4e-107">Description</span><span class="sxs-lookup"><span data-stu-id="bfd4e-107">Description</span></span>

<span data-ttu-id="bfd4e-108">La commande `dotnet clean` nettoie la sortie de la génération précédente.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-108">The `dotnet clean` command cleans the output of the previous build.</span></span> <span data-ttu-id="bfd4e-109">Comme elle est implémentée en tant que [cible MSBuild](/visualstudio/msbuild/msbuild-targets), le projet est évalué lorsque la commande est exécutée.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-109">It's implemented as an [MSBuild target](/visualstudio/msbuild/msbuild-targets), so the project is evaluated when the command is run.</span></span> <span data-ttu-id="bfd4e-110">Seules les sorties créées lors de la génération sont nettoyées.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-110">Only the outputs created during the build are cleaned.</span></span> <span data-ttu-id="bfd4e-111">Les dossiers de sortie intermédiaire (*obj*) et de sortie finale (*bin*) sont tous deux nettoyés.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-111">Both intermediate (*obj*) and final output (*bin*) folders are cleaned.</span></span>

## <a name="arguments"></a><span data-ttu-id="bfd4e-112">Arguments</span><span class="sxs-lookup"><span data-stu-id="bfd4e-112">Arguments</span></span>

`PROJECT`

<span data-ttu-id="bfd4e-113">Le projet MSBuild à nettoyer.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-113">The MSBuild project to clean.</span></span> <span data-ttu-id="bfd4e-114">Si vous ne spécifiez pas de fichier projet, MSBuild recherche dans le répertoire de travail actuel un fichier avec une extension se terminant par *proj* et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-114">If a project file is not specified, MSBuild searches the current working directory for a file that has a file extension that ends in *proj* and uses that file.</span></span>

## <a name="options"></a><span data-ttu-id="bfd4e-115">Options</span><span class="sxs-lookup"><span data-stu-id="bfd4e-115">Options</span></span>

* **`-c|--configuration {Debug|Release}`**

  <span data-ttu-id="bfd4e-116">Définit la configuration de build.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-116">Defines the build configuration.</span></span> <span data-ttu-id="bfd4e-117">La valeur par défaut est `Debug`.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-117">The default value is `Debug`.</span></span> <span data-ttu-id="bfd4e-118">Cette option est uniquement requise durant le nettoyage si vous l’avez spécifiée au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-118">This option is only required when cleaning if you specified it during build time.</span></span>

* **`-f|--framework <FRAMEWORK>`**

  <span data-ttu-id="bfd4e-119">Le [framework](../../standard/frameworks.md) spécifié au moment de la génération.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-119">The [framework](../../standard/frameworks.md) that was specified at build time.</span></span> <span data-ttu-id="bfd4e-120">Le framework doit être défini dans le [fichier projet](csproj.md).</span><span class="sxs-lookup"><span data-stu-id="bfd4e-120">The framework must be defined in the [project file](csproj.md).</span></span> <span data-ttu-id="bfd4e-121">Si vous avez spécifié le framework au moment de la génération, vous devez spécifier le framework lors du nettoyage.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-121">If you specified the framework at build time, you must specify the framework when cleaning.</span></span>

* **`-h|--help`**

  <span data-ttu-id="bfd4e-122">Affiche une aide brève pour la commande.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-122">Prints out a short help for the command.</span></span>

* **`-o|--output <OUTPUT_DIRECTORY>`**

  <span data-ttu-id="bfd4e-123">Répertoire dans lequel les sorties générées sont placées.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-123">Directory in which the build outputs are placed.</span></span> <span data-ttu-id="bfd4e-124">Spécifiez le commutateur `-f|--framework <FRAMEWORK>` avec le commutateur de répertoire de sortie si vous avez spécifié le framework lorsque le projet a été généré.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-124">Specify the `-f|--framework <FRAMEWORK>` switch with the output directory switch if you specified the framework when the project was built.</span></span>

* **`-r|--runtime <RUNTIME_IDENTIFIER>`**

  <span data-ttu-id="bfd4e-125">Nettoie le dossier de sortie du runtime spécifié.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-125">Cleans the output folder of the specified runtime.</span></span> <span data-ttu-id="bfd4e-126">Cette option est utilisée à la création d’un [déploiement autonome](../deploying/index.md#self-contained-deployments-scd).</span><span class="sxs-lookup"><span data-stu-id="bfd4e-126">This is used when a [self-contained deployment](../deploying/index.md#self-contained-deployments-scd) was created.</span></span> <span data-ttu-id="bfd4e-127">Option disponible à partir du kit SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-127">Option available since .NET Core 2.0 SDK.</span></span>

* **`-v|--verbosity <LEVEL>`**

  <span data-ttu-id="bfd4e-128">Définit le niveau de détail de la commande.</span><span class="sxs-lookup"><span data-stu-id="bfd4e-128">Sets the verbosity level of the command.</span></span> <span data-ttu-id="bfd4e-129">Niveaux autorisés : q[uiet], m[inimal], n[ormal], d[etailed] et diag[nostic].</span><span class="sxs-lookup"><span data-stu-id="bfd4e-129">Allowed levels are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].</span></span>

## <a name="examples"></a><span data-ttu-id="bfd4e-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="bfd4e-130">Examples</span></span>

* <span data-ttu-id="bfd4e-131">Nettoyez une génération par défaut du projet :</span><span class="sxs-lookup"><span data-stu-id="bfd4e-131">Clean a default build of the project:</span></span>

  ```console
  dotnet clean
  ```

* <span data-ttu-id="bfd4e-132">Nettoyez un projet généré à l’aide de la configuration Release :</span><span class="sxs-lookup"><span data-stu-id="bfd4e-132">Clean a project built using the Release configuration:</span></span>

  ```console
  dotnet clean --configuration Release
  ```