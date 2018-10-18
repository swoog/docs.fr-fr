---
title: Bibliothèques SourceLink et .NET
description: Meilleures pratiques recommandées pour l’utilisation de SourceLink pour améliorer le débogage pour les bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: fa4af47eaa5dd1510640c2bf0ebb2187b56efae0
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49370043"
---
# <a name="sourcelink"></a><span data-ttu-id="a4217-103">SourceLink</span><span class="sxs-lookup"><span data-stu-id="a4217-103">SourceLink</span></span>

<span data-ttu-id="a4217-104">SourceLink est une technologie qui permet le débogage du code source des assemblys .NET à partir de NuGet par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="a4217-104">SourceLink is a technology that enables source code debugging of .NET assemblies from NuGet by developers.</span></span> <span data-ttu-id="a4217-105">SourceLink s’exécute lors de la création du package NuGet et incorpore des métadonnées de contrôle de source à l’intérieur des assemblys et le package.</span><span class="sxs-lookup"><span data-stu-id="a4217-105">SourceLink executes when creating the NuGet package and embeds source control metadata inside assemblies and the package.</span></span> <span data-ttu-id="a4217-106">Les développeurs qui téléchargent le package et ont SourceLink activée dans Visual Studio peuvent accéder à son code source.</span><span class="sxs-lookup"><span data-stu-id="a4217-106">Developers who download the package and have SourceLink enabled in Visual Studio can step into its source code.</span></span> <span data-ttu-id="a4217-107">SourceLink fournit les métadonnées de contrôle de source pour créer une excellente expérience de débogage.</span><span class="sxs-lookup"><span data-stu-id="a4217-107">SourceLink provides source control metadata to create a great debugging experience.</span></span>

## <a name="sourcelink-demo"></a><span data-ttu-id="a4217-108">Démonstration de SourceLink</span><span class="sxs-lookup"><span data-stu-id="a4217-108">SourceLink demo</span></span>

> [!VIDEO https://www.youtube.com/embed/gyRGhCQPkB4?start=61]

## <a name="using-sourcelink"></a><span data-ttu-id="a4217-109">À l’aide de SourceLink</span><span class="sxs-lookup"><span data-stu-id="a4217-109">Using SourceLink</span></span>

<span data-ttu-id="a4217-110">Vous trouverez des instructions sur l’utilisation de SourceLink sur le [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) référentiel GitHub.</span><span class="sxs-lookup"><span data-stu-id="a4217-110">Instructions for using SourceLink can be found on the [dotnet/sourceLink](https://github.com/dotnet/sourcelink/blob/master/README.md) GitHub repository.</span></span>

<span data-ttu-id="a4217-111">Vous pouvez utiliser [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) pour confirmer que les métadonnées SourceLink a été correctement incorporée dans le package.</span><span class="sxs-lookup"><span data-stu-id="a4217-111">You can use [NuGet Package Explorer](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer) to confirm that the SourceLink metadata has been successfully embedded in the package.</span></span> <span data-ttu-id="a4217-112">Vérifier le `Repository` métadonnées soient établie avec un identificateur de commentaire et qui se trouvent les fichiers .pdb avec .dll chaque cible.</span><span class="sxs-lookup"><span data-stu-id="a4217-112">Check the `Repository` metadata is present with a comment identifier and that .pdb files are located with each target's .dll.</span></span>

<span data-ttu-id="a4217-113">![SourceLink dans l’Explorateur de Package NuGet](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink dans l’Explorateur de Package NuGet")</span><span class="sxs-lookup"><span data-stu-id="a4217-113">![SourceLink in NuGet Package Explorer](./media/sourcelink/nuget-package-explorer-sourcelink.png "SourceLink in NuGet Package Explorer")</span></span>

<span data-ttu-id="a4217-114">**ENVISAGEZ de ✔️** à l’aide de SourceLink pour ajouter les métadonnées de contrôle de code source à vos assemblys et le package NuGet.</span><span class="sxs-lookup"><span data-stu-id="a4217-114">**✔️ CONSIDER** using SourceLink to add source control metadata to your assemblies and NuGet package.</span></span>

<span data-ttu-id="a4217-115">**ENVISAGEZ de ✔️** , y compris les fichiers PDB dans le package NuGet.</span><span class="sxs-lookup"><span data-stu-id="a4217-115">**✔️ CONSIDER** including PDB files in the NuGet package.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="a4217-116">[Précédent](./dependencies.md)
[Suivant](./publish-nuget-package.md)</span><span class="sxs-lookup"><span data-stu-id="a4217-116">[Previous](./dependencies.md)
[Next](./publish-nuget-package.md)</span></span>
