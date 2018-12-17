---
title: Bibliothèques SourceLink et .NET
description: Recommandations relatives aux bonnes pratiques pour l’utilisation de SourceLink afin d’améliorer le débogage pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 3bc72e158a5773b656095f9ce58b442469f91e67
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128924"
---
# <a name="sourcelink"></a><span data-ttu-id="b10a7-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="b10a7-103">SourceLink</span></span>

<span data-ttu-id="b10a7-104">SourceLink est une technologie qui permet le débogage du code source des assemblys .NET à partir de NuGet par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="b10a7-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="b10a7-105">SourceLink s’exécute lors de la création du package NuGet et incorpore des métadonnées de contrôle de code source à l’intérieur des assemblys et du package.</span><span class="sxs-lookup"><span data-stu-id="b10a7-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="b10a7-106">Les développeurs qui téléchargent le package et activent SourceLink dans Visual Studio peuvent effectuer un pas à pas détaillé dans son code source.</span><span class="sxs-lookup"><span data-stu-id="b10a7-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="b10a7-107">SourceLink fournit des métadonnées de contrôle de code source pour créer une excellente expérience de débogage.</span><span class="sxs-lookup"><span data-stu-id="b10a7-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="b10a7-108">Démonstration de SourceLink</span><span class="sxs-lookup"><span data-stu-id="b10a7-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="b10a7-109">Utilisation de SourceLink</span><span class="sxs-lookup"><span data-stu-id="b10a7-109">Using SourceLink</span></span>

<span data-ttu-id="b10a7-110">Vous trouverez des instructions sur l’utilisation de SourceLink dans le dépôt GitHub [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md).</span><span class="sxs-lookup"><span data-stu-id="b10a7-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="b10a7-111">Vous pouvez utiliser [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) pour confirmer que les métadonnées SourceLink ont été correctement incorporées dans le package.</span><span class="sxs-lookup"><span data-stu-id="b10a7-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="b10a7-112">Vérifiez que les métadonnées `Repository` sont présentes avec un identificateur de commentaire et que les fichiers .pdb se trouvent avec le fichier .dll de chaque cible.</span><span class="sxs-lookup"><span data-stu-id="b10a7-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="b10a7-113">![SourceLink dans NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink dans NuGet Package Explorer")</span><span class="sxs-lookup"><span data-stu-id="b10a7-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="b10a7-114">**✔️ À ENVISAGER** : Utiliser SourceLink pour ajouter des métadonnées de contrôle de code source à vos assemblys et packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="b10a7-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet packages.</span></span>

> [!TIP]
> <span data-ttu-id="b10a7-115">Vous pouvez améliorer davantage l’expérience de débogage d’un développeur en ajoutant des attributs de débogueur à vos types.</span><span class="sxs-lookup"><span data-stu-id="b10a7-115">You can further enhance a developer's debugging experience by adding debugger attributes to your types.</span></span>
> * <span data-ttu-id="b10a7-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> peut personnaliser la façon dont une classe ou un champ s’affiche dans les fenêtres de variables du débogueur.</span><span class="sxs-lookup"><span data-stu-id="b10a7-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> can customize how a class or field is displayed in the debugger variable windows.</span></span>
> * <span data-ttu-id="b10a7-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> demande au débogueur de parcourir le code au lieu d’y effectuer un pas à pas détaillé.</span><span class="sxs-lookup"><span data-stu-id="b10a7-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> instructs the debugger to step through the code instead of stepping into the code.</span></span>
> * <span data-ttu-id="b10a7-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> contrôle si un membre est affiché dans les fenêtres de variables du débogueur.</span><span class="sxs-lookup"><span data-stu-id="b10a7-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> controls whether a member is displayed in the debugger variable windows.</span></span>

<span data-ttu-id="b10a7-119">**✔️ À ENVISAGER** : Inclure des fichiers de symboles (`*.pdb`) dans le package NuGet.</span><span class="sxs-lookup"><span data-stu-id="b10a7-119">**✔️ CONSIDER** including symbol files (`*.pdb`) in the NuGet package.</span></span>

> <span data-ttu-id="b10a7-120">Normalement, vous devez publier les fichiers de symboles dans un [package de symboles](./nuget.md#symbol-packages).</span><span class="sxs-lookup"><span data-stu-id="b10a7-120">Ordinarily, you'd publish symbol files in a [symbol package](./nuget.md#symbol-packages).</span></span> <span data-ttu-id="b10a7-121">Actuellement, l’hôte public principal pour les packages de symboles ne prend pas en charge les fichiers de symboles portables (`*.pdb`) créés par les projets de style SDK et les packages de symboles sont inutiles.</span><span class="sxs-lookup"><span data-stu-id="b10a7-121">Currently the main public host for symbol packages doesn't support the portable symbol files (`*.pdb`) created by SDK-style projects, and symbol packages aren't useful.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="b10a7-122">[Précédent](dependencies.md)
>[Suivant](publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="b10a7-122">[Previous](dependencies.md)
[Next](publish-nuget-package.md)</span></span>