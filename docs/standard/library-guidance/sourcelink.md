---
title: Bibliothèques SourceLink et .NET
description: Recommandations relatives aux bonnes pratiques pour l’utilisation de SourceLink afin d’améliorer le débogage pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 01/15/2019
ms.openlocfilehash: be97f868e2fcfc6c45e4bbac45b033f8914f4d99
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333536"
---
# <a name="sourcelink"></a><span data-ttu-id="2f410-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="2f410-103">SourceLink</span></span>

<span data-ttu-id="2f410-104">SourceLink est une technologie qui permet le débogage du code source des assemblys .NET à partir de NuGet par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="2f410-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="2f410-105">SourceLink s’exécute lors de la création du package NuGet et incorpore des métadonnées de contrôle de code source à l’intérieur des assemblys et du package.</span><span class="sxs-lookup"><span data-stu-id="2f410-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="2f410-106">Les développeurs qui téléchargent le package et activent SourceLink dans Visual Studio peuvent effectuer un pas à pas détaillé dans son code source.</span><span class="sxs-lookup"><span data-stu-id="2f410-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="2f410-107">SourceLink fournit des métadonnées de contrôle de code source pour créer une excellente expérience de débogage.</span><span class="sxs-lookup"><span data-stu-id="2f410-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="2f410-108">Démonstration de SourceLink</span><span class="sxs-lookup"><span data-stu-id="2f410-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="2f410-109">Utilisation de SourceLink</span><span class="sxs-lookup"><span data-stu-id="2f410-109">Using SourceLink</span></span>

<span data-ttu-id="2f410-110">Vous trouverez des instructions sur l’utilisation de SourceLink dans le dépôt GitHub [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md).</span><span class="sxs-lookup"><span data-stu-id="2f410-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="2f410-111">Vous pouvez utiliser [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) pour confirmer que les métadonnées SourceLink ont été correctement incorporées dans le package.</span><span class="sxs-lookup"><span data-stu-id="2f410-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="2f410-112">Vérifiez que les métadonnées `Repository` sont présentes avec un identificateur de commentaire et que les fichiers .pdb se trouvent avec le fichier .dll de chaque cible.</span><span class="sxs-lookup"><span data-stu-id="2f410-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="2f410-113">![SourceLink dans NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink dans NuGet Package Explorer")</span><span class="sxs-lookup"><span data-stu-id="2f410-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="2f410-114">**✔️ À ENVISAGER** : Utiliser SourceLink pour ajouter des métadonnées de contrôle de code source à vos assemblys et packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="2f410-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet packages.</span></span>

> [!TIP]
> <span data-ttu-id="2f410-115">Vous pouvez améliorer davantage l’expérience de débogage d’un développeur en ajoutant des attributs de débogueur à vos types.</span><span class="sxs-lookup"><span data-stu-id="2f410-115">You can further enhance a developer's debugging experience by adding debugger attributes to your types.</span></span>
> * <span data-ttu-id="2f410-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> peut personnaliser la façon dont une classe ou un champ s’affiche dans les fenêtres de variables du débogueur.</span><span class="sxs-lookup"><span data-stu-id="2f410-116"><xref:System.Diagnostics.DebuggerDisplayAttribute> can customize how a class or field is displayed in the debugger variable windows.</span></span>
> * <span data-ttu-id="2f410-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> demande au débogueur de parcourir le code au lieu d’y effectuer un pas à pas détaillé.</span><span class="sxs-lookup"><span data-stu-id="2f410-117"><xref:System.Diagnostics.DebuggerStepThroughAttribute> instructs the debugger to step through the code instead of stepping into the code.</span></span>
> * <span data-ttu-id="2f410-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> contrôle si un membre est affiché dans les fenêtres de variables du débogueur.</span><span class="sxs-lookup"><span data-stu-id="2f410-118"><xref:System.Diagnostics.DebuggerBrowsableAttribute> controls whether a member is displayed in the debugger variable windows.</span></span>

<span data-ttu-id="2f410-119">**✔️ À ENVISAGER** : publication des fichiers de symboles (`*.pdb`).</span><span class="sxs-lookup"><span data-stu-id="2f410-119">**✔️ CONSIDER** publishing symbol files (`*.pdb`).</span></span>

> <span data-ttu-id="2f410-120">Pour plus d’informations sur les fichiers de symboles et les packages de symboles, consultez [Packages de symboles](./nuget.md#symbol-packages).</span><span class="sxs-lookup"><span data-stu-id="2f410-120">For more information about symbol files and symbol packages, see [Symbol packages](./nuget.md#symbol-packages).</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="2f410-121">[Précédent](dependencies.md)
>[Suivant](publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="2f410-121">[Previous](dependencies.md)
[Next](publish-nuget-package.md)</span></span>
